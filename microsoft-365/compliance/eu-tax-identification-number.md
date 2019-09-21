---
title: Numéro d’identification fiscale de l’UE
ms.author: stephow
author: stephow-MSFT
manager: laurawi
ms.date: 8/17/2018
audience: Admin
ms.topic: reference
ms.service: O365-seccomp
ms.collection: M365-security-compliance
localization_priority: Normal
description: Cette rubrique montre ce qu’une stratégie de protection contre la perte de données (DLP) recherche lorsqu’il détecte le type d’informations sensibles du numéro d’identification fiscale de l’UE. Ce type d’informations sensibles définit différents modèles, Mots clés et autres preuves pour chaque pays.
ms.openlocfilehash: adcd9be9b5f8775ad39010d771ff2ac214df1e17
ms.sourcegitcommit: 1162d676b036449ea4220de8a6642165190e3398
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/20/2019
ms.locfileid: "37079262"
---
# <a name="eu-tax-identification-number"></a><span data-ttu-id="f26cd-104">Numéro d’identification fiscale de l’UE</span><span class="sxs-lookup"><span data-stu-id="f26cd-104">EU Tax Identification Number</span></span>

<span data-ttu-id="f26cd-105">Cette rubrique montre ce qu’une stratégie de protection contre la perte de données (DLP) recherche lorsqu’il détecte le type d’informations sensibles de l’ID taxe de l’UE (TIN).</span><span class="sxs-lookup"><span data-stu-id="f26cd-105">This topic shows what a data loss prevention (DLP) policy looks for when it detects the EU Tax Identification Number (TIN) sensitive information type.</span></span> <span data-ttu-id="f26cd-106">Ce type d’informations sensibles définit différents modèles, Mots clés et autres preuves pour chaque pays.</span><span class="sxs-lookup"><span data-stu-id="f26cd-106">This sensitive information type defines different patterns, keywords, and other evidence for each country.</span></span>
  
## <a name="austria"></a><span data-ttu-id="f26cd-107">Autriche</span><span class="sxs-lookup"><span data-stu-id="f26cd-107">Austria</span></span>

### <a name="format"></a><span data-ttu-id="f26cd-108">Format</span><span class="sxs-lookup"><span data-stu-id="f26cd-108">Format</span></span>

<span data-ttu-id="f26cd-109">Neuf chiffres avec un trait d’union conditionnel et une barre oblique</span><span class="sxs-lookup"><span data-stu-id="f26cd-109">Nine digits with optional hyphen and forward slash</span></span>
  
### <a name="pattern"></a><span data-ttu-id="f26cd-110">Modèle</span><span class="sxs-lookup"><span data-stu-id="f26cd-110">Pattern</span></span>

<span data-ttu-id="f26cd-111">Neuf chiffres avec un trait d’Union et une barre oblique facultatifs :</span><span class="sxs-lookup"><span data-stu-id="f26cd-111">Nine digits with optional hyphen and forward slash:</span></span>
  
-  <span data-ttu-id="f26cd-112">Deux chiffres</span><span class="sxs-lookup"><span data-stu-id="f26cd-112">Two digits</span></span> 
    
- <span data-ttu-id="f26cd-113">Un trait d’union (facultatif)</span><span class="sxs-lookup"><span data-stu-id="f26cd-113">A hyphen (optional)</span></span>
    
- <span data-ttu-id="f26cd-114">Trois chiffres</span><span class="sxs-lookup"><span data-stu-id="f26cd-114">Three digits</span></span>
    
- <span data-ttu-id="f26cd-115">Une barre oblique (facultative)</span><span class="sxs-lookup"><span data-stu-id="f26cd-115">A forward slash (optional)</span></span>
    
- <span data-ttu-id="f26cd-116">Quatre chiffres</span><span class="sxs-lookup"><span data-stu-id="f26cd-116">Four digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="f26cd-117">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="f26cd-117">Checksum</span></span>

<span data-ttu-id="f26cd-118">Oui</span><span class="sxs-lookup"><span data-stu-id="f26cd-118">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="f26cd-119">Définition</span><span class="sxs-lookup"><span data-stu-id="f26cd-119">Definition</span></span>

<span data-ttu-id="f26cd-120">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="f26cd-120">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="f26cd-121">La fonction `Func_austria_eu_tax_file_number` trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="f26cd-121">The function  `Func_austria_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="f26cd-122">Un mot clé `Keywords_austria_eu_tax_file_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="f26cd-122">A keyword from  `Keywords_austria_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="f26cd-123">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="f26cd-123">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="f26cd-124">La fonction `Func_austria_eu_tax_file_number` trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="f26cd-124">The function  `Func_austria_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="f26cd-125">Mots clés</span><span class="sxs-lookup"><span data-stu-id="f26cd-125">Keywords</span></span>

#### <a name="keywords_austria_eu_tax_file_number"></a><span data-ttu-id="f26cd-126">Keywords_austria_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="f26cd-126">Keywords_austria_eu_tax_file_number</span></span>

<span data-ttu-id="f26cd-127">Numéro de taxe</span><span class="sxs-lookup"><span data-stu-id="f26cd-127">tax number</span></span>
  
<span data-ttu-id="f26cd-128">number</span><span class="sxs-lookup"><span data-stu-id="f26cd-128">number</span></span>
  
<span data-ttu-id="f26cd-129">Numéro d’enregistrement taxe</span><span class="sxs-lookup"><span data-stu-id="f26cd-129">tax registration number</span></span>
  
<span data-ttu-id="f26cd-130">id fiscal</span><span class="sxs-lookup"><span data-stu-id="f26cd-130">tax id</span></span>
  
<span data-ttu-id="f26cd-131">st.nr.</span><span class="sxs-lookup"><span data-stu-id="f26cd-131">st.nr.</span></span>
  
<span data-ttu-id="f26cd-132">steuernummer</span><span class="sxs-lookup"><span data-stu-id="f26cd-132">steuernummer</span></span>
  
## <a name="belgium"></a><span data-ttu-id="f26cd-133">Belgique</span><span class="sxs-lookup"><span data-stu-id="f26cd-133">Belgium</span></span>

### <a name="format"></a><span data-ttu-id="f26cd-134">Format</span><span class="sxs-lookup"><span data-stu-id="f26cd-134">Format</span></span>

<span data-ttu-id="f26cd-135">11 chiffres sans espaces ni délimiteurs</span><span class="sxs-lookup"><span data-stu-id="f26cd-135">11 digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="f26cd-136">Modèle</span><span class="sxs-lookup"><span data-stu-id="f26cd-136">Pattern</span></span>

<span data-ttu-id="f26cd-137">11 chiffres :</span><span class="sxs-lookup"><span data-stu-id="f26cd-137">11 digits:</span></span>
  
- <span data-ttu-id="f26cd-138">Deux chiffres</span><span class="sxs-lookup"><span data-stu-id="f26cd-138">Two digits</span></span>
    
- <span data-ttu-id="f26cd-139">« 0 » ou « 1 »</span><span class="sxs-lookup"><span data-stu-id="f26cd-139">A "0" or "1"</span></span>
    
- <span data-ttu-id="f26cd-140">Un chiffre</span><span class="sxs-lookup"><span data-stu-id="f26cd-140">One digit</span></span>
    
- <span data-ttu-id="f26cd-141">« 0 » ou « 1 » ou « 2 » ou « 3 »</span><span class="sxs-lookup"><span data-stu-id="f26cd-141">A "0" or "1" or "2" or "3"</span></span> 
    
- <span data-ttu-id="f26cd-142">Six chiffres</span><span class="sxs-lookup"><span data-stu-id="f26cd-142">Six digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="f26cd-143">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="f26cd-143">Checksum</span></span>

<span data-ttu-id="f26cd-144">Non applicable</span><span class="sxs-lookup"><span data-stu-id="f26cd-144">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="f26cd-145">Définition</span><span class="sxs-lookup"><span data-stu-id="f26cd-145">Definition</span></span>

<span data-ttu-id="f26cd-146">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="f26cd-146">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="f26cd-147">L’expression `Regex_belgium_eu_tax_file_number` régulière trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="f26cd-147">The regular expression  `Regex_belgium_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="f26cd-148">Un mot clé `Keywords_belgium_eu_tax_file_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="f26cd-148">A keyword from  `Keywords_belgium_eu_tax_file_number` is found.</span></span> 
    
```
 <!-- EU Tax File Number -->
<Entity id="e09c07d3-66e5-4783-989d-49ac62748f5f" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_belgium_eu_tax_file_number" />
          <Match idRef="Keywords_belgium_eu_tax_file_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="f26cd-149">Mots clés</span><span class="sxs-lookup"><span data-stu-id="f26cd-149">Keywords</span></span>

#### <a name="keywords_belgium_eu_tax_file_number"></a><span data-ttu-id="f26cd-150">Keywords_belgium_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="f26cd-150">Keywords_belgium_eu_tax_file_number</span></span>

<span data-ttu-id="f26cd-151">Numéro de taxe</span><span class="sxs-lookup"><span data-stu-id="f26cd-151">tax number</span></span>
  
<span data-ttu-id="f26cd-152">Numéro d’enregistrement national</span><span class="sxs-lookup"><span data-stu-id="f26cd-152">national registration number</span></span>
  
<span data-ttu-id="f26cd-153">Numéro d’enregistrement taxe</span><span class="sxs-lookup"><span data-stu-id="f26cd-153">tax registration number</span></span>
  
<span data-ttu-id="f26cd-154">id fiscal</span><span class="sxs-lookup"><span data-stu-id="f26cd-154">tax id</span></span>
  
<span data-ttu-id="f26cd-155">nPour</span><span class="sxs-lookup"><span data-stu-id="f26cd-155">nif</span></span>
  
<span data-ttu-id="f26cd-156">nPour #</span><span class="sxs-lookup"><span data-stu-id="f26cd-156">nif#</span></span>
  
<span data-ttu-id="f26cd-157">Numéro de registre national</span><span class="sxs-lookup"><span data-stu-id="f26cd-157">numéro de registre national</span></span>
  
<span data-ttu-id="f26cd-158">Numéro d’identification fiscale</span><span class="sxs-lookup"><span data-stu-id="f26cd-158">numéro d'identification fiscale</span></span>
  
## <a name="bulgaria"></a><span data-ttu-id="f26cd-159">Bulgarie</span><span class="sxs-lookup"><span data-stu-id="f26cd-159">Bulgaria</span></span>

### <a name="format"></a><span data-ttu-id="f26cd-160">Format</span><span class="sxs-lookup"><span data-stu-id="f26cd-160">Format</span></span>

<span data-ttu-id="f26cd-161">Dix chiffres sans espaces ni délimiteurs</span><span class="sxs-lookup"><span data-stu-id="f26cd-161">Ten digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="f26cd-162">Modèle</span><span class="sxs-lookup"><span data-stu-id="f26cd-162">Pattern</span></span>

<span data-ttu-id="f26cd-163">10 chiffres</span><span class="sxs-lookup"><span data-stu-id="f26cd-163">10 digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="f26cd-164">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="f26cd-164">Checksum</span></span>

<span data-ttu-id="f26cd-165">Oui</span><span class="sxs-lookup"><span data-stu-id="f26cd-165">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="f26cd-166">Définition</span><span class="sxs-lookup"><span data-stu-id="f26cd-166">Definition</span></span>

<span data-ttu-id="f26cd-167">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="f26cd-167">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="f26cd-168">La fonction `Func_bulgaria_eu_tax_file_number` trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="f26cd-168">The function  `Func_bulgaria_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="f26cd-169">Un mot clé `Keywords_bulgaria_eu_tax_file_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="f26cd-169">A keyword from  `Keywords_bulgaria_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="f26cd-170">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="f26cd-170">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="f26cd-171">La fonction `Func_bulgaria_eu_tax_file_number` trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="f26cd-171">The function  `Func_bulgaria_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="f26cd-172">Mots clés</span><span class="sxs-lookup"><span data-stu-id="f26cd-172">Keywords</span></span>

#### <a name="keywords_bulgaria_eu_tax_file_number"></a><span data-ttu-id="f26cd-173">Keywords_bulgaria_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="f26cd-173">Keywords_bulgaria_eu_tax_file_number</span></span>

<span data-ttu-id="f26cd-174">bucn</span><span class="sxs-lookup"><span data-stu-id="f26cd-174">bucn</span></span>
  
<span data-ttu-id="f26cd-175">numéro civil uniforme</span><span class="sxs-lookup"><span data-stu-id="f26cd-175">uniform civil number</span></span>
  
<span data-ttu-id="f26cd-176">bucn #</span><span class="sxs-lookup"><span data-stu-id="f26cd-176">bucn#</span></span>
  
<span data-ttu-id="f26cd-177">uniformcivilnumber #</span><span class="sxs-lookup"><span data-stu-id="f26cd-177">uniformcivilnumber#</span></span>
  
<span data-ttu-id="f26cd-178">ID civil uniforme</span><span class="sxs-lookup"><span data-stu-id="f26cd-178">uniform civil id</span></span>
  
<span data-ttu-id="f26cd-179">non civil uniforme</span><span class="sxs-lookup"><span data-stu-id="f26cd-179">uniform civil no</span></span>
  
<span data-ttu-id="f26cd-180">egn</span><span class="sxs-lookup"><span data-stu-id="f26cd-180">egn</span></span>
  
<span data-ttu-id="f26cd-181">numéro civil uniforme bulgare</span><span class="sxs-lookup"><span data-stu-id="f26cd-181">bulgarian uniform civil number</span></span>
  
<span data-ttu-id="f26cd-182">uniformcivilno #</span><span class="sxs-lookup"><span data-stu-id="f26cd-182">uniformcivilno#</span></span>
  
<span data-ttu-id="f26cd-183">egn #</span><span class="sxs-lookup"><span data-stu-id="f26cd-183">egn#</span></span>
  
<span data-ttu-id="f26cd-184">униформ граждански номер</span><span class="sxs-lookup"><span data-stu-id="f26cd-184">униформ граждански номер</span></span>
  
<span data-ttu-id="f26cd-185">ID униформ</span><span class="sxs-lookup"><span data-stu-id="f26cd-185">униформ id</span></span>
  
<span data-ttu-id="f26cd-186">униформ граждански ID</span><span class="sxs-lookup"><span data-stu-id="f26cd-186">униформ граждански id</span></span>
  
<span data-ttu-id="f26cd-187">униформ граждански не</span><span class="sxs-lookup"><span data-stu-id="f26cd-187">униформ граждански не</span></span>
  
## <a name="croatia"></a><span data-ttu-id="f26cd-188">Croatie</span><span class="sxs-lookup"><span data-stu-id="f26cd-188">Croatia</span></span>

### <a name="format"></a><span data-ttu-id="f26cd-189">Format</span><span class="sxs-lookup"><span data-stu-id="f26cd-189">Format</span></span>

<span data-ttu-id="f26cd-190">11 chiffres sans espaces ni délimiteurs</span><span class="sxs-lookup"><span data-stu-id="f26cd-190">11 digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="f26cd-191">Modèle</span><span class="sxs-lookup"><span data-stu-id="f26cd-191">Pattern</span></span>

<span data-ttu-id="f26cd-192">11 chiffres :</span><span class="sxs-lookup"><span data-stu-id="f26cd-192">11 digits:</span></span>
  
- <span data-ttu-id="f26cd-193">Dix chiffres, choisis de manière aléatoire</span><span class="sxs-lookup"><span data-stu-id="f26cd-193">Ten digits, randomly chosen</span></span>
    
- <span data-ttu-id="f26cd-194">Un chiffre de contrôle</span><span class="sxs-lookup"><span data-stu-id="f26cd-194">One check digit</span></span>
    
### <a name="checksum"></a><span data-ttu-id="f26cd-195">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="f26cd-195">Checksum</span></span>

<span data-ttu-id="f26cd-196">Oui</span><span class="sxs-lookup"><span data-stu-id="f26cd-196">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="f26cd-197">Définition</span><span class="sxs-lookup"><span data-stu-id="f26cd-197">Definition</span></span>

<span data-ttu-id="f26cd-198">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="f26cd-198">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="f26cd-199">La fonction `Func_croatia_eu_tax_file_number` trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="f26cd-199">The function  `Func_croatia_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="f26cd-200">Un mot clé `Keywords_croatia_eu_tax_file_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="f26cd-200">A keyword from  `Keywords_croatia_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="f26cd-201">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="f26cd-201">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="f26cd-202">La fonction `Func_croatia_eu_tax_file_number` trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="f26cd-202">The function  `Func_croatia_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="f26cd-203">Mots clés</span><span class="sxs-lookup"><span data-stu-id="f26cd-203">Keywords</span></span>

#### <a name="keywords_croatia_eu_tax_file_number"></a><span data-ttu-id="f26cd-204">Keywords_croatia_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="f26cd-204">Keywords_croatia_eu_tax_file_number</span></span>

<span data-ttu-id="f26cd-205">Numéro de taxe</span><span class="sxs-lookup"><span data-stu-id="f26cd-205">tax number</span></span>
  
<span data-ttu-id="f26cd-206">codes</span><span class="sxs-lookup"><span data-stu-id="f26cd-206">tax</span></span>
  
<span data-ttu-id="f26cd-207">id fiscal</span><span class="sxs-lookup"><span data-stu-id="f26cd-207">tax id</span></span>
  
<span data-ttu-id="f26cd-208">oid</span><span class="sxs-lookup"><span data-stu-id="f26cd-208">oid</span></span>
  
<span data-ttu-id="f26cd-209">OID #</span><span class="sxs-lookup"><span data-stu-id="f26cd-209">oid#</span></span>
  
<span data-ttu-id="f26cd-210">porezni broj</span><span class="sxs-lookup"><span data-stu-id="f26cd-210">porezni broj</span></span>
  
## <a name="cyprus"></a><span data-ttu-id="f26cd-211">Chypre</span><span class="sxs-lookup"><span data-stu-id="f26cd-211">Cyprus</span></span>

### <a name="format"></a><span data-ttu-id="f26cd-212">Format</span><span class="sxs-lookup"><span data-stu-id="f26cd-212">Format</span></span>

<span data-ttu-id="f26cd-213">Huit chiffres et une lettre dans le modèle spécifié</span><span class="sxs-lookup"><span data-stu-id="f26cd-213">Eight digits and one letter in the specified pattern</span></span>
  
### <a name="pattern"></a><span data-ttu-id="f26cd-214">Modèle</span><span class="sxs-lookup"><span data-stu-id="f26cd-214">Pattern</span></span>

<span data-ttu-id="f26cd-215">Huit chiffres et une lettre :</span><span class="sxs-lookup"><span data-stu-id="f26cd-215">Eight digits and one letter:</span></span>
  
-  <span data-ttu-id="f26cd-216">« 0 »</span><span class="sxs-lookup"><span data-stu-id="f26cd-216">A "0"</span></span> 
    
- <span data-ttu-id="f26cd-217">Sept chiffres </span><span class="sxs-lookup"><span data-stu-id="f26cd-217">Seven digits</span></span>
    
- <span data-ttu-id="f26cd-218">Une lettre (ne respecte pas la casse)</span><span class="sxs-lookup"><span data-stu-id="f26cd-218">One letter (not case-sensitive)</span></span>
    
### <a name="checksum"></a><span data-ttu-id="f26cd-219">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="f26cd-219">Checksum</span></span>

<span data-ttu-id="f26cd-220">Non applicable</span><span class="sxs-lookup"><span data-stu-id="f26cd-220">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="f26cd-221">Définition</span><span class="sxs-lookup"><span data-stu-id="f26cd-221">Definition</span></span>

<span data-ttu-id="f26cd-222">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="f26cd-222">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="f26cd-223">La fonction `Func_cyprus_eu_tax_file_number` trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="f26cd-223">The function  `Func_cyprus_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="f26cd-224">Un mot clé `Keywords_cyprus_eu_tax_file_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="f26cd-224">A keyword from  `Keywords_cyprus_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="f26cd-225">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="f26cd-225">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="f26cd-226">La fonction `Func_cyprus_eu_tax_file_number` trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="f26cd-226">The function  `Func_cyprus_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="f26cd-227">Mots clés</span><span class="sxs-lookup"><span data-stu-id="f26cd-227">Keywords</span></span>

#### <a name="keywords_cyprus_eu_tax_file_number"></a><span data-ttu-id="f26cd-228">Keywords_cyprus_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="f26cd-228">Keywords_cyprus_eu_tax_file_number</span></span>

<span data-ttu-id="f26cd-229">Numéro de taxe</span><span class="sxs-lookup"><span data-stu-id="f26cd-229">tax number</span></span>
  
<span data-ttu-id="f26cd-230">codes</span><span class="sxs-lookup"><span data-stu-id="f26cd-230">tax</span></span>
  
<span data-ttu-id="f26cd-231">id fiscal</span><span class="sxs-lookup"><span data-stu-id="f26cd-231">tax id</span></span>
  
<span data-ttu-id="f26cd-232">code d’identification fiscale</span><span class="sxs-lookup"><span data-stu-id="f26cd-232">tax identification code</span></span>
  
<span data-ttu-id="f26cd-233">graduation</span><span class="sxs-lookup"><span data-stu-id="f26cd-233">tic</span></span>
  
<span data-ttu-id="f26cd-234">graduation #</span><span class="sxs-lookup"><span data-stu-id="f26cd-234">tic#</span></span>
  
<span data-ttu-id="f26cd-235">αριθμός φορολογικού μητρώου</span><span class="sxs-lookup"><span data-stu-id="f26cd-235">αριθμός φορολογικού μητρώου</span></span>
  
<span data-ttu-id="f26cd-236">φορολογική ταυτότητα</span><span class="sxs-lookup"><span data-stu-id="f26cd-236">φορολογική ταυτότητα</span></span>
  
<span data-ttu-id="f26cd-237">κωδικός φορολογικού μητρώου</span><span class="sxs-lookup"><span data-stu-id="f26cd-237">κωδικός φορολογικού μητρώου</span></span>
  
## <a name="czech-republic"></a><span data-ttu-id="f26cd-238">République tchèque</span><span class="sxs-lookup"><span data-stu-id="f26cd-238">Czech Republic</span></span>

### <a name="format"></a><span data-ttu-id="f26cd-239">Format</span><span class="sxs-lookup"><span data-stu-id="f26cd-239">Format</span></span>

<span data-ttu-id="f26cd-240">Neuf ou dix chiffres avec une barre oblique inverse facultative</span><span class="sxs-lookup"><span data-stu-id="f26cd-240">Nine or ten digits with an optional backslash</span></span>
  
### <a name="pattern"></a><span data-ttu-id="f26cd-241">Modèle</span><span class="sxs-lookup"><span data-stu-id="f26cd-241">Pattern</span></span>

<span data-ttu-id="f26cd-242">Neuf ou dix chiffres avec une barre oblique inverse facultative :</span><span class="sxs-lookup"><span data-stu-id="f26cd-242">Nine or ten digits with an optional backslashl:</span></span>
  
- <span data-ttu-id="f26cd-243">Six chiffres</span><span class="sxs-lookup"><span data-stu-id="f26cd-243">Six digits</span></span> 
    
- <span data-ttu-id="f26cd-244">Une barre oblique inverse (facultatif)</span><span class="sxs-lookup"><span data-stu-id="f26cd-244">A backslash (optional)</span></span>
    
- <span data-ttu-id="f26cd-245">3 ou 4 chiffres</span><span class="sxs-lookup"><span data-stu-id="f26cd-245">Three or four digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="f26cd-246">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="f26cd-246">Checksum</span></span>

<span data-ttu-id="f26cd-247">Non applicable</span><span class="sxs-lookup"><span data-stu-id="f26cd-247">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="f26cd-248">Définition</span><span class="sxs-lookup"><span data-stu-id="f26cd-248">Definition</span></span>

<span data-ttu-id="f26cd-249">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="f26cd-249">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="f26cd-250">L’expression `Regex_czech_republic_eu_tax_file_number` régulière trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="f26cd-250">The regular expression  `Regex_czech_republic_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="f26cd-251">Un mot clé `Keywords_czech_republic_eu_tax_file_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="f26cd-251">A keyword from  `Keywords_czech_republic_eu_tax_file_number` is found.</span></span> 
    
```
 <!-- EU Tax File Number -->
<Entity id="e09c07d3-66e5-4783-989d-49ac62748f5f" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_czech_republic_eu_tax_file_number" />
          <Match idRef="Keywords_czech_republic_eu_tax_file_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="f26cd-252">Mots clés</span><span class="sxs-lookup"><span data-stu-id="f26cd-252">Keywords</span></span>

#### <a name="keywords_czech_republic_eu_tax_file_number"></a><span data-ttu-id="f26cd-253">Keywords_czech_republic_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="f26cd-253">Keywords_czech_republic_eu_tax_file_number</span></span>

<span data-ttu-id="f26cd-254">Numéro de taxe</span><span class="sxs-lookup"><span data-stu-id="f26cd-254">tax number</span></span>
  
<span data-ttu-id="f26cd-255">codes</span><span class="sxs-lookup"><span data-stu-id="f26cd-255">tax</span></span>
  
<span data-ttu-id="f26cd-256">id fiscal</span><span class="sxs-lookup"><span data-stu-id="f26cd-256">tax id</span></span>
  
<span data-ttu-id="f26cd-257">numéro personnel</span><span class="sxs-lookup"><span data-stu-id="f26cd-257">personal number</span></span>
  
<span data-ttu-id="f26cd-258">daňové číslo</span><span class="sxs-lookup"><span data-stu-id="f26cd-258">daňové číslo</span></span>
  
<span data-ttu-id="f26cd-259">osobní číslo</span><span class="sxs-lookup"><span data-stu-id="f26cd-259">osobní číslo</span></span>
  
## <a name="denmark"></a><span data-ttu-id="f26cd-260">Danemark</span><span class="sxs-lookup"><span data-stu-id="f26cd-260">Denmark</span></span>

### <a name="format"></a><span data-ttu-id="f26cd-261">Format</span><span class="sxs-lookup"><span data-stu-id="f26cd-261">Format</span></span>

<span data-ttu-id="f26cd-262">Dix chiffres contenant un trait d’Union</span><span class="sxs-lookup"><span data-stu-id="f26cd-262">Ten digits containing a hyphen</span></span>
  
### <a name="pattern"></a><span data-ttu-id="f26cd-263">Modèle</span><span class="sxs-lookup"><span data-stu-id="f26cd-263">Pattern</span></span>

<span data-ttu-id="f26cd-264">Dix chiffres contenant un trait d’Union :</span><span class="sxs-lookup"><span data-stu-id="f26cd-264">Ten digits containing a hyphenl:</span></span>
  
-  <span data-ttu-id="f26cd-265">Six chiffres correspondant à la date de naissance (JJMMAA)</span><span class="sxs-lookup"><span data-stu-id="f26cd-265">Six digits that correspond to the birth date (DDMMYY)</span></span> 
    
- <span data-ttu-id="f26cd-266">Un trait d’union </span><span class="sxs-lookup"><span data-stu-id="f26cd-266">A hyphen</span></span>
    
- <span data-ttu-id="f26cd-267">Quatre chiffres correspondant à un numéro de séquence où le premier chiffre correspond au siècle de naissance et le dernier chiffre correspond au sexe de l’individu (impair pour les hommes et les femmes)</span><span class="sxs-lookup"><span data-stu-id="f26cd-267">Four digits that correspond to a sequence number where the first digit corresponds to the century of birth and the last digit corresponds to the individual's gender (odd for male and even for female)</span></span>
    
### <a name="checksum"></a><span data-ttu-id="f26cd-268">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="f26cd-268">Checksum</span></span>

<span data-ttu-id="f26cd-269">Oui</span><span class="sxs-lookup"><span data-stu-id="f26cd-269">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="f26cd-270">Définition</span><span class="sxs-lookup"><span data-stu-id="f26cd-270">Definition</span></span>

<span data-ttu-id="f26cd-271">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="f26cd-271">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="f26cd-272">La fonction `Func_denmark_eu_tax_file_number` trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="f26cd-272">The function  `Func_denmark_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="f26cd-273">Un mot clé `Keywords_denmark_eu_tax_file_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="f26cd-273">A keyword from  `Keywords_denmark_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="f26cd-274">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="f26cd-274">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="f26cd-275">La fonction `Func_denmark_eu_tax_file_number` trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="f26cd-275">The function  `Func_denmark_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="f26cd-276">Mots clés</span><span class="sxs-lookup"><span data-stu-id="f26cd-276">Keywords</span></span>

#### <a name="keywords_denmark_eu_tax_file_number"></a><span data-ttu-id="f26cd-277">Keywords_denmark_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="f26cd-277">Keywords_denmark_eu_tax_file_number</span></span>

<span data-ttu-id="f26cd-278">Numéro de taxe</span><span class="sxs-lookup"><span data-stu-id="f26cd-278">tax number</span></span>
  
<span data-ttu-id="f26cd-279">codes</span><span class="sxs-lookup"><span data-stu-id="f26cd-279">tax</span></span>
  
<span data-ttu-id="f26cd-280">id fiscal</span><span class="sxs-lookup"><span data-stu-id="f26cd-280">tax id</span></span>
  
<span data-ttu-id="f26cd-281">numéro CPR</span><span class="sxs-lookup"><span data-stu-id="f26cd-281">cpr number</span></span>
  
<span data-ttu-id="f26cd-282">cardio #</span><span class="sxs-lookup"><span data-stu-id="f26cd-282">cpr#</span></span>
  
<span data-ttu-id="f26cd-283">skat nummer</span><span class="sxs-lookup"><span data-stu-id="f26cd-283">skat nummer</span></span>
  
<span data-ttu-id="f26cd-284">ID Skat</span><span class="sxs-lookup"><span data-stu-id="f26cd-284">skat id</span></span>
  
## <a name="estonia"></a><span data-ttu-id="f26cd-285">Estonie</span><span class="sxs-lookup"><span data-stu-id="f26cd-285">Estonia</span></span>

### <a name="format"></a><span data-ttu-id="f26cd-286">Format</span><span class="sxs-lookup"><span data-stu-id="f26cd-286">Format</span></span>

<span data-ttu-id="f26cd-287">11 chiffres sans espaces ni délimiteurs</span><span class="sxs-lookup"><span data-stu-id="f26cd-287">11 digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="f26cd-288">Modèle</span><span class="sxs-lookup"><span data-stu-id="f26cd-288">Pattern</span></span>

<span data-ttu-id="f26cd-289">11 chiffres :</span><span class="sxs-lookup"><span data-stu-id="f26cd-289">11 digits:</span></span>
  
-  <span data-ttu-id="f26cd-290">Un chiffre correspondant au sexe et au siècle de naissance, où un nombre impair indique le mâle et le nombre pair, la femme comme suit : 1,2 pour le 19 siècle ; 3, 4 pour le vingtième siècle ; et 5, 6 pour le 21ème siècle</span><span class="sxs-lookup"><span data-stu-id="f26cd-290">One digit that corresponds to gender and century of birth where an odd number indicates male and the even number indicates female as follows: 1, 2 for the 19th century; 3, 4 for the 20th century; and 5, 6 for the 21st century</span></span> 
    
- <span data-ttu-id="f26cd-291">Six chiffres correspondant à la date de naissance (AAMMJJ)</span><span class="sxs-lookup"><span data-stu-id="f26cd-291">Six digits that correspond to birth date (YYMMDD)</span></span>
    
- <span data-ttu-id="f26cd-292">Trois chiffres correspondant à un numéro de série séparant les personnes nés à la même date</span><span class="sxs-lookup"><span data-stu-id="f26cd-292">Three digits that correspond to a serial number separating persons born on the same date</span></span>
    
- <span data-ttu-id="f26cd-293">Un chiffre de contrôle</span><span class="sxs-lookup"><span data-stu-id="f26cd-293">One check digit</span></span>
    
### <a name="checksum"></a><span data-ttu-id="f26cd-294">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="f26cd-294">Checksum</span></span>

<span data-ttu-id="f26cd-295">Oui</span><span class="sxs-lookup"><span data-stu-id="f26cd-295">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="f26cd-296">Définition</span><span class="sxs-lookup"><span data-stu-id="f26cd-296">Definition</span></span>

<span data-ttu-id="f26cd-297">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="f26cd-297">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="f26cd-298">La fonction `Func_estonia_eu_tax_file_number` trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="f26cd-298">The function  `Func_estonia_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="f26cd-299">Un mot clé `Keywords_estonia_eu_tax_file_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="f26cd-299">A keyword from  `Keywords_estonia_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="f26cd-300">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="f26cd-300">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="f26cd-301">La fonction `Func_estonia_eu_tax_file_number` trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="f26cd-301">The function  `Func_estonia_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="f26cd-302">Mots clés</span><span class="sxs-lookup"><span data-stu-id="f26cd-302">Keywords</span></span>

#### <a name="keywords_estonia_eu_tax_file_number"></a><span data-ttu-id="f26cd-303">Keywords_estonia_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="f26cd-303">Keywords_estonia_eu_tax_file_number</span></span>

<span data-ttu-id="f26cd-304">Numéro de taxe</span><span class="sxs-lookup"><span data-stu-id="f26cd-304">tax number</span></span>
  
<span data-ttu-id="f26cd-305">codes</span><span class="sxs-lookup"><span data-stu-id="f26cd-305">tax</span></span>
  
<span data-ttu-id="f26cd-306">id fiscal</span><span class="sxs-lookup"><span data-stu-id="f26cd-306">tax id</span></span>
  
<span data-ttu-id="f26cd-307">code personnel</span><span class="sxs-lookup"><span data-stu-id="f26cd-307">personal code</span></span>
  
<span data-ttu-id="f26cd-308">maksunumber</span><span class="sxs-lookup"><span data-stu-id="f26cd-308">maksunumber</span></span>
  
<span data-ttu-id="f26cd-309">ID maksu</span><span class="sxs-lookup"><span data-stu-id="f26cd-309">maksu id</span></span>
  
<span data-ttu-id="f26cd-310">isikukood</span><span class="sxs-lookup"><span data-stu-id="f26cd-310">isikukood</span></span>
  
## <a name="finland"></a><span data-ttu-id="f26cd-311">Finlande</span><span class="sxs-lookup"><span data-stu-id="f26cd-311">Finland</span></span>

### <a name="format"></a><span data-ttu-id="f26cd-312">Format</span><span class="sxs-lookup"><span data-stu-id="f26cd-312">Format</span></span>

<span data-ttu-id="f26cd-313">Combinaison de 11 caractères chiffres, lettres, et signe plus et moins</span><span class="sxs-lookup"><span data-stu-id="f26cd-313">An 11-character combination of digits, letters, and plus and minus sign</span></span>
  
### <a name="pattern"></a><span data-ttu-id="f26cd-314">Modèle</span><span class="sxs-lookup"><span data-stu-id="f26cd-314">Pattern</span></span>

<span data-ttu-id="f26cd-315">Combinaison de 11 caractères chiffres, lettres, et signe plus et moins :</span><span class="sxs-lookup"><span data-stu-id="f26cd-315">An 11-character combination of digits, letters, and plus and minus sign:</span></span>
  
- <span data-ttu-id="f26cd-316">Six chiffres</span><span class="sxs-lookup"><span data-stu-id="f26cd-316">Six digits</span></span>
    
- <span data-ttu-id="f26cd-317">L’une des options suivantes : un signe plus, un signe moins ou la lettre « A » (ne respectant pas la casse), où le signe plus est né entre 1800-1899, le signe moins est né entre 1900-1999, et « A » désigne né 2000 et after</span><span class="sxs-lookup"><span data-stu-id="f26cd-317">One of the following: a plus sign, a minus sign, or the letter "A" (not case sensitive) where the plus sign means born between 1800-1899, the minus sign means born between 1900-1999, and "A" means born 2000 and after</span></span>
    
- <span data-ttu-id="f26cd-318">Trois chiffres</span><span class="sxs-lookup"><span data-stu-id="f26cd-318">Three digits</span></span>
    
- <span data-ttu-id="f26cd-319">Une lettre ou un chiffre</span><span class="sxs-lookup"><span data-stu-id="f26cd-319">One letter or one number</span></span>
    
### <a name="checksum"></a><span data-ttu-id="f26cd-320">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="f26cd-320">Checksum</span></span>

<span data-ttu-id="f26cd-321">Oui</span><span class="sxs-lookup"><span data-stu-id="f26cd-321">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="f26cd-322">Définition</span><span class="sxs-lookup"><span data-stu-id="f26cd-322">Definition</span></span>

<span data-ttu-id="f26cd-323">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="f26cd-323">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="f26cd-324">La fonction `Func_finland_eu_tax_file_number` trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="f26cd-324">The function  `Func_finland_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="f26cd-325">Un mot clé `Keywords_finland_eu_tax_file_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="f26cd-325">A keyword from  `Keywords_finland_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="f26cd-326">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="f26cd-326">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="f26cd-327">La fonction `Func_finland_eu_tax_file_number` trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="f26cd-327">The function  `Func_finland_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="f26cd-328">Mots clés</span><span class="sxs-lookup"><span data-stu-id="f26cd-328">Keywords</span></span>

#### <a name="keywords_finland_eu_tax_file_number"></a><span data-ttu-id="f26cd-329">Keywords_finland_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="f26cd-329">Keywords_finland_eu_tax_file_number</span></span>

<span data-ttu-id="f26cd-330">numéro d’identification</span><span class="sxs-lookup"><span data-stu-id="f26cd-330">identification number</span></span>
  
<span data-ttu-id="f26cd-331">ID personnel</span><span class="sxs-lookup"><span data-stu-id="f26cd-331">personal id</span></span>
  
<span data-ttu-id="f26cd-332">Numéro d’identité</span><span class="sxs-lookup"><span data-stu-id="f26cd-332">identity number</span></span>
  
<span data-ttu-id="f26cd-333">Numéro d’identification national finnois</span><span class="sxs-lookup"><span data-stu-id="f26cd-333">finnish national id number</span></span>
  
<span data-ttu-id="f26cd-334">personalidnumber #</span><span class="sxs-lookup"><span data-stu-id="f26cd-334">personalidnumber#</span></span>
  
<span data-ttu-id="f26cd-335">numéro d’identification nationale</span><span class="sxs-lookup"><span data-stu-id="f26cd-335">national identification number</span></span>
  
<span data-ttu-id="f26cd-336">Numéro d’identification</span><span class="sxs-lookup"><span data-stu-id="f26cd-336">id number</span></span>
  
<span data-ttu-id="f26cd-337">Numéro d’identification nationale</span><span class="sxs-lookup"><span data-stu-id="f26cd-337">national id no.</span></span>
  
<span data-ttu-id="f26cd-338">Numéro d’identification national</span><span class="sxs-lookup"><span data-stu-id="f26cd-338">national id number</span></span>
  
<span data-ttu-id="f26cd-339">n ° ID</span><span class="sxs-lookup"><span data-stu-id="f26cd-339">id no</span></span>
  
<span data-ttu-id="f26cd-340">tunnistenumero</span><span class="sxs-lookup"><span data-stu-id="f26cd-340">tunnistenumero</span></span>
  
<span data-ttu-id="f26cd-341">henkilötunnus</span><span class="sxs-lookup"><span data-stu-id="f26cd-341">henkilötunnus</span></span>
  
<span data-ttu-id="f26cd-342">yksilöllinen henkilökohtainen tunnistenumero</span><span class="sxs-lookup"><span data-stu-id="f26cd-342">yksilöllinen henkilökohtainen tunnistenumero</span></span>
  
<span data-ttu-id="f26cd-343">ainutlaatuinen henkilökohtainen tunnus</span><span class="sxs-lookup"><span data-stu-id="f26cd-343">ainutlaatuinen henkilökohtainen tunnus</span></span>
  
<span data-ttu-id="f26cd-344">identiteetti numérique</span><span class="sxs-lookup"><span data-stu-id="f26cd-344">identiteetti numero</span></span>
  
<span data-ttu-id="f26cd-345">suomen kansallinen henkilötunnus</span><span class="sxs-lookup"><span data-stu-id="f26cd-345">suomen kansallinen henkilötunnus</span></span>
  
<span data-ttu-id="f26cd-346">henkilötunnusnumero #</span><span class="sxs-lookup"><span data-stu-id="f26cd-346">henkilötunnusnumero#</span></span>
  
<span data-ttu-id="f26cd-347">kansallisen tunnistenumero</span><span class="sxs-lookup"><span data-stu-id="f26cd-347">kansallisen tunnistenumero</span></span>
  
<span data-ttu-id="f26cd-348">tunnusnumero</span><span class="sxs-lookup"><span data-stu-id="f26cd-348">tunnusnumero</span></span>
  
<span data-ttu-id="f26cd-349">Kansallinen tunnus numérique</span><span class="sxs-lookup"><span data-stu-id="f26cd-349">kansallinen tunnus numero</span></span>
  
## <a name="france"></a><span data-ttu-id="f26cd-350">France</span><span class="sxs-lookup"><span data-stu-id="f26cd-350">France</span></span>

### <a name="format"></a><span data-ttu-id="f26cd-351">Format</span><span class="sxs-lookup"><span data-stu-id="f26cd-351">Format</span></span>

<span data-ttu-id="f26cd-352">13 chiffres pour les personnes et neuf chiffres pour les entités</span><span class="sxs-lookup"><span data-stu-id="f26cd-352">13 digits for individuals and nine digits for entities</span></span>
  
### <a name="pattern"></a><span data-ttu-id="f26cd-353">Modèle</span><span class="sxs-lookup"><span data-stu-id="f26cd-353">Pattern</span></span>

<span data-ttu-id="f26cd-354">13 chiffres pour les personnes :</span><span class="sxs-lookup"><span data-stu-id="f26cd-354">13 digits for individuals:</span></span>
  
- <span data-ttu-id="f26cd-355">Un chiffre qui doit être 0, 1, 2 ou 3</span><span class="sxs-lookup"><span data-stu-id="f26cd-355">One digit that must be 0, 1, 2, or 3</span></span>
    
- <span data-ttu-id="f26cd-356">12 chiffres</span><span class="sxs-lookup"><span data-stu-id="f26cd-356">12 digits</span></span>
    
<span data-ttu-id="f26cd-357">Neuf chiffres pour les entités</span><span class="sxs-lookup"><span data-stu-id="f26cd-357">Nine digits for entities</span></span>
  
### <a name="checksum"></a><span data-ttu-id="f26cd-358">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="f26cd-358">Checksum</span></span>

<span data-ttu-id="f26cd-359">Non applicable</span><span class="sxs-lookup"><span data-stu-id="f26cd-359">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="f26cd-360">Définition</span><span class="sxs-lookup"><span data-stu-id="f26cd-360">Definition</span></span>

<span data-ttu-id="f26cd-361">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="f26cd-361">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="f26cd-362">La fonction `Func_france_eu_tax_file_number` trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="f26cd-362">The function  `Func_france_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="f26cd-363">Un mot clé `Keywords_france_eu_tax_file_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="f26cd-363">A keyword from  `Keywords_france_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="f26cd-364">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="f26cd-364">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="f26cd-365">La fonction `Func_france_eu_tax_file_number` trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="f26cd-365">The function  `Func_france_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="f26cd-366">Mots clés</span><span class="sxs-lookup"><span data-stu-id="f26cd-366">Keywords</span></span>

#### <a name="keywords_france_eu_tax_file_number"></a><span data-ttu-id="f26cd-367">Keywords_france_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="f26cd-367">Keywords_france_eu_tax_file_number</span></span>

<span data-ttu-id="f26cd-368">Numéro d’identification de taxe</span><span class="sxs-lookup"><span data-stu-id="f26cd-368">tax identification number</span></span>
  
<span data-ttu-id="f26cd-369">Numéro de taxe</span><span class="sxs-lookup"><span data-stu-id="f26cd-369">tax number</span></span>
  
<span data-ttu-id="f26cd-370">id fiscal</span><span class="sxs-lookup"><span data-stu-id="f26cd-370">tax id</span></span>
  
<span data-ttu-id="f26cd-371">Numéro d’identification fiscale</span><span class="sxs-lookup"><span data-stu-id="f26cd-371">numéro d'identification fiscale</span></span>
  
## <a name="germany"></a><span data-ttu-id="f26cd-372">Allemagne</span><span class="sxs-lookup"><span data-stu-id="f26cd-372">Germany</span></span>

### <a name="format"></a><span data-ttu-id="f26cd-373">Format</span><span class="sxs-lookup"><span data-stu-id="f26cd-373">Format</span></span>

<span data-ttu-id="f26cd-374">11 chiffres sans espaces ni délimiteurs</span><span class="sxs-lookup"><span data-stu-id="f26cd-374">11 digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="f26cd-375">Modèle</span><span class="sxs-lookup"><span data-stu-id="f26cd-375">Pattern</span></span>

<span data-ttu-id="f26cd-376">11 chiffres :</span><span class="sxs-lookup"><span data-stu-id="f26cd-376">11 digits :</span></span>
  
-  <span data-ttu-id="f26cd-377">Dix chiffres</span><span class="sxs-lookup"><span data-stu-id="f26cd-377">Ten digits</span></span> 
    
- <span data-ttu-id="f26cd-378">Un chiffre de contrôle</span><span class="sxs-lookup"><span data-stu-id="f26cd-378">One check digit</span></span>
    
### <a name="checksum"></a><span data-ttu-id="f26cd-379">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="f26cd-379">Checksum</span></span>

<span data-ttu-id="f26cd-380">Oui</span><span class="sxs-lookup"><span data-stu-id="f26cd-380">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="f26cd-381">Définition</span><span class="sxs-lookup"><span data-stu-id="f26cd-381">Definition</span></span>

<span data-ttu-id="f26cd-382">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="f26cd-382">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="f26cd-383">La fonction `Func_germany_eu_tax_file_number` trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="f26cd-383">The function  `Func_germany_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="f26cd-384">Un mot clé `Keywords_germany_eu_tax_file_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="f26cd-384">A keyword from  `Keywords_germany_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="f26cd-385">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="f26cd-385">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="f26cd-386">La fonction `Func_germany_eu_tax_file_number` trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="f26cd-386">The function  `Func_germany_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="f26cd-387">Mots clés</span><span class="sxs-lookup"><span data-stu-id="f26cd-387">Keywords</span></span>

#### <a name="keywords_germany_eu_tax_file_number"></a><span data-ttu-id="f26cd-388">Keywords_germany_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="f26cd-388">Keywords_germany_eu_tax_file_number</span></span>

<span data-ttu-id="f26cd-389">Numéro de taxe</span><span class="sxs-lookup"><span data-stu-id="f26cd-389">tax number</span></span>
  
<span data-ttu-id="f26cd-390">n ° taxe</span><span class="sxs-lookup"><span data-stu-id="f26cd-390">tax no.</span></span>
  
<span data-ttu-id="f26cd-391">taxno #</span><span class="sxs-lookup"><span data-stu-id="f26cd-391">taxno#</span></span>
  
<span data-ttu-id="f26cd-392">taxnumber #</span><span class="sxs-lookup"><span data-stu-id="f26cd-392">taxnumber#</span></span>
  
<span data-ttu-id="f26cd-393">taxnumber</span><span class="sxs-lookup"><span data-stu-id="f26cd-393">taxnumber</span></span>
  
<span data-ttu-id="f26cd-394">id fiscal</span><span class="sxs-lookup"><span data-stu-id="f26cd-394">tax id</span></span>
  
<span data-ttu-id="f26cd-395">taxi #</span><span class="sxs-lookup"><span data-stu-id="f26cd-395">taxid#</span></span>
  
<span data-ttu-id="f26cd-396">Numéro d’identification de taxe</span><span class="sxs-lookup"><span data-stu-id="f26cd-396">tax identification number</span></span>
  
<span data-ttu-id="f26cd-397">n ° d’identification fiscale</span><span class="sxs-lookup"><span data-stu-id="f26cd-397">tax identification no.</span></span>
  
<span data-ttu-id="f26cd-398">steuernummer</span><span class="sxs-lookup"><span data-stu-id="f26cd-398">steuernummer</span></span>
  
<span data-ttu-id="f26cd-399">ID Steuer</span><span class="sxs-lookup"><span data-stu-id="f26cd-399">steuer id</span></span>
  
<span data-ttu-id="f26cd-400">steueridentifikationsnummer</span><span class="sxs-lookup"><span data-stu-id="f26cd-400">steueridentifikationsnummer</span></span>
  
## <a name="greece"></a><span data-ttu-id="f26cd-401">Grèce</span><span class="sxs-lookup"><span data-stu-id="f26cd-401">Greece</span></span>

### <a name="format"></a><span data-ttu-id="f26cd-402">Format</span><span class="sxs-lookup"><span data-stu-id="f26cd-402">Format</span></span>

<span data-ttu-id="f26cd-403">Neuf chiffres sans espaces ni délimiteurs</span><span class="sxs-lookup"><span data-stu-id="f26cd-403">Nine digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="f26cd-404">Modèle</span><span class="sxs-lookup"><span data-stu-id="f26cd-404">Pattern</span></span>

<span data-ttu-id="f26cd-405">Neuf chiffres</span><span class="sxs-lookup"><span data-stu-id="f26cd-405">Nine digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="f26cd-406">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="f26cd-406">Checksum</span></span>

<span data-ttu-id="f26cd-407">Non applicable</span><span class="sxs-lookup"><span data-stu-id="f26cd-407">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="f26cd-408">Définition</span><span class="sxs-lookup"><span data-stu-id="f26cd-408">Definition</span></span>

<span data-ttu-id="f26cd-409">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="f26cd-409">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="f26cd-410">L’expression `Regex_greece_eu_tax_file_number` régulière trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="f26cd-410">The regular expression  `Regex_greece_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="f26cd-411">Un mot clé `Keywords_greece_eu_tax_file_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="f26cd-411">A keyword from  `Keywords_greece_eu_tax_file_number` is found.</span></span> 
    
```
 <!-- EU Tax File Number -->
<Entity id="e09c07d3-66e5-4783-989d-49ac62748f5f" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_greece_eu_tax_file_number" />
          <Match idRef="Keywords_greece_eu_tax_file_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="f26cd-412">Mots clés</span><span class="sxs-lookup"><span data-stu-id="f26cd-412">Keywords</span></span>

#### <a name="keywords_greece_eu_tax_file_number"></a><span data-ttu-id="f26cd-413">Keywords_greece_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="f26cd-413">Keywords_greece_eu_tax_file_number</span></span>

<span data-ttu-id="f26cd-414">financement</span><span class="sxs-lookup"><span data-stu-id="f26cd-414">afm</span></span>
  
<span data-ttu-id="f26cd-415">Etain</span><span class="sxs-lookup"><span data-stu-id="f26cd-415">tin</span></span>
  
<span data-ttu-id="f26cd-416">n ° ID taxe</span><span class="sxs-lookup"><span data-stu-id="f26cd-416">tax id no.</span></span>
  
<span data-ttu-id="f26cd-417">n ° de taxe</span><span class="sxs-lookup"><span data-stu-id="f26cd-417">tax id no</span></span>
  
<span data-ttu-id="f26cd-418">Numéro d’identification de taxe</span><span class="sxs-lookup"><span data-stu-id="f26cd-418">tax identification number</span></span>
  
<span data-ttu-id="f26cd-419">Numéro de registre des taxes</span><span class="sxs-lookup"><span data-stu-id="f26cd-419">tax registry number</span></span>
  
<span data-ttu-id="f26cd-420">n ° de Registre taxe</span><span class="sxs-lookup"><span data-stu-id="f26cd-420">tax registry no.</span></span>
  
<span data-ttu-id="f26cd-421">financement #</span><span class="sxs-lookup"><span data-stu-id="f26cd-421">afm#</span></span>
  
<span data-ttu-id="f26cd-422">Etain #</span><span class="sxs-lookup"><span data-stu-id="f26cd-422">tin#</span></span>
  
<span data-ttu-id="f26cd-423">taxidno #</span><span class="sxs-lookup"><span data-stu-id="f26cd-423">taxidno#</span></span>
  
<span data-ttu-id="f26cd-424">taxregistryno #</span><span class="sxs-lookup"><span data-stu-id="f26cd-424">taxregistryno#</span></span>
  
<span data-ttu-id="f26cd-425">αριθμός φορολογικού μητρώου</span><span class="sxs-lookup"><span data-stu-id="f26cd-425">αριθμός φορολογικού μητρώου</span></span>
  
<span data-ttu-id="f26cd-426">aφμ</span><span class="sxs-lookup"><span data-stu-id="f26cd-426">aφμ</span></span>
  
<span data-ttu-id="f26cd-427">aφμ αριθμός</span><span class="sxs-lookup"><span data-stu-id="f26cd-427">aφμ αριθμός</span></span>
  
<span data-ttu-id="f26cd-428">φορολογικού μητρώου νο.</span><span class="sxs-lookup"><span data-stu-id="f26cd-428">φορολογικού μητρώου νο.</span></span>
  
<span data-ttu-id="f26cd-429">τον αριθμό φορολογικού μητρώου</span><span class="sxs-lookup"><span data-stu-id="f26cd-429">τον αριθμό φορολογικού μητρώου</span></span>
  
## <a name="hungary"></a><span data-ttu-id="f26cd-430">Hongrie</span><span class="sxs-lookup"><span data-stu-id="f26cd-430">Hungary</span></span>

### <a name="format"></a><span data-ttu-id="f26cd-431">Format</span><span class="sxs-lookup"><span data-stu-id="f26cd-431">Format</span></span>

<span data-ttu-id="f26cd-432">Dix chiffres sans espaces ni délimiteurs</span><span class="sxs-lookup"><span data-stu-id="f26cd-432">Ten digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="f26cd-433">Modèle</span><span class="sxs-lookup"><span data-stu-id="f26cd-433">Pattern</span></span>

<span data-ttu-id="f26cd-434">Dix chiffres :</span><span class="sxs-lookup"><span data-stu-id="f26cd-434">Ten digits:</span></span>
  
-  <span data-ttu-id="f26cd-435">Un chiffre qui doit être « 8 »</span><span class="sxs-lookup"><span data-stu-id="f26cd-435">One digit that must be "8"</span></span> 
    
- <span data-ttu-id="f26cd-436">Cinq chiffres correspondant au nombre de jours entre la date 01/01/1867 et la date de naissance de la personne</span><span class="sxs-lookup"><span data-stu-id="f26cd-436">Five digits that correspond to the number of days between the date 01/01/1867 and the date of the birth of the individual</span></span>
    
- <span data-ttu-id="f26cd-437">Trois chiffres correspondant au nombre généré par l’opportunité pour différencier les individus nés le même jour</span><span class="sxs-lookup"><span data-stu-id="f26cd-437">Three digits that correspond to the number generated by chance to differentiate individuals born on the same day</span></span>
    
- <span data-ttu-id="f26cd-438">Un chiffre de contrôle</span><span class="sxs-lookup"><span data-stu-id="f26cd-438">One check digit</span></span>
    
### <a name="checksum"></a><span data-ttu-id="f26cd-439">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="f26cd-439">Checksum</span></span>

<span data-ttu-id="f26cd-440">Oui</span><span class="sxs-lookup"><span data-stu-id="f26cd-440">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="f26cd-441">Définition</span><span class="sxs-lookup"><span data-stu-id="f26cd-441">Definition</span></span>

<span data-ttu-id="f26cd-442">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="f26cd-442">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="f26cd-443">La fonction `Func_hungary_eu_tax_file_number` trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="f26cd-443">The function  `Func_hungary_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="f26cd-444">Un mot clé `Keywords_hungary_eu_tax_file_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="f26cd-444">A keyword from  `Keywords_hungary_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="f26cd-445">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="f26cd-445">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="f26cd-446">La fonction `Func_hungary_eu_tax_file_number` trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="f26cd-446">The function  `Func_hungary_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="f26cd-447">Mots clés</span><span class="sxs-lookup"><span data-stu-id="f26cd-447">Keywords</span></span>

#### <a name="keywords_hungary_eu_tax_file_number"></a><span data-ttu-id="f26cd-448">Keywords_hungary_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="f26cd-448">Keywords_hungary_eu_tax_file_number</span></span>

<span data-ttu-id="f26cd-449">Numéro d’identification de taxe hongrois</span><span class="sxs-lookup"><span data-stu-id="f26cd-449">hungarian tax identification number</span></span>
  
<span data-ttu-id="f26cd-450">étain hongrois</span><span class="sxs-lookup"><span data-stu-id="f26cd-450">hungarian tin</span></span>
  
<span data-ttu-id="f26cd-451">Numéro d’identification de taxe</span><span class="sxs-lookup"><span data-stu-id="f26cd-451">tax id number</span></span>
  
<span data-ttu-id="f26cd-452">Numéro de TVA</span><span class="sxs-lookup"><span data-stu-id="f26cd-452">vat number</span></span>
  
<span data-ttu-id="f26cd-453">Numéro de l’autorité fiscale</span><span class="sxs-lookup"><span data-stu-id="f26cd-453">tax authority no</span></span>
  
<span data-ttu-id="f26cd-454">Numéro d’identité fiscale de l’ID taxe</span><span class="sxs-lookup"><span data-stu-id="f26cd-454">tax id tax identity number</span></span>
  
<span data-ttu-id="f26cd-455">taxidnumber #</span><span class="sxs-lookup"><span data-stu-id="f26cd-455">taxidnumber#</span></span>
  
<span data-ttu-id="f26cd-456">Etain #</span><span class="sxs-lookup"><span data-stu-id="f26cd-456">tin#</span></span>
  
<span data-ttu-id="f26cd-457">hungatiantin #</span><span class="sxs-lookup"><span data-stu-id="f26cd-457">hungatiantin#</span></span>
  
<span data-ttu-id="f26cd-458">n ° d’identification fiscale</span><span class="sxs-lookup"><span data-stu-id="f26cd-458">tax identification no</span></span>
  
<span data-ttu-id="f26cd-459">taxidno #</span><span class="sxs-lookup"><span data-stu-id="f26cd-459">taxidno#</span></span>
  
<span data-ttu-id="f26cd-460">adóazonosító szám</span><span class="sxs-lookup"><span data-stu-id="f26cd-460">adóazonosító szám</span></span>
  
<span data-ttu-id="f26cd-461">adószám</span><span class="sxs-lookup"><span data-stu-id="f26cd-461">adószám</span></span>
  
<span data-ttu-id="f26cd-462">adóhatóság szám</span><span class="sxs-lookup"><span data-stu-id="f26cd-462">adóhatóság szám</span></span>
  
## <a name="ireland"></a><span data-ttu-id="f26cd-463">Irlande</span><span class="sxs-lookup"><span data-stu-id="f26cd-463">Ireland</span></span>

### <a name="format"></a><span data-ttu-id="f26cd-464">Format</span><span class="sxs-lookup"><span data-stu-id="f26cd-464">Format</span></span>

<span data-ttu-id="f26cd-465">Sept chiffres suivis d’une lettre sans espaces ni délimiteurs</span><span class="sxs-lookup"><span data-stu-id="f26cd-465">Seven digits followed by a letter with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="f26cd-466">Modèle</span><span class="sxs-lookup"><span data-stu-id="f26cd-466">Pattern</span></span>

<span data-ttu-id="f26cd-467">Sept chiffres suivis d’une lettre :</span><span class="sxs-lookup"><span data-stu-id="f26cd-467">Seven digits followed by a letter:</span></span>
  
-  <span data-ttu-id="f26cd-468">Sept chiffres </span><span class="sxs-lookup"><span data-stu-id="f26cd-468">Seven digits</span></span> 
    
- <span data-ttu-id="f26cd-469">Une lettre (ne respecte pas la casse)</span><span class="sxs-lookup"><span data-stu-id="f26cd-469">One letter (not case-sensitive)</span></span>
    
### <a name="checksum"></a><span data-ttu-id="f26cd-470">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="f26cd-470">Checksum</span></span>

<span data-ttu-id="f26cd-471">Non applicable</span><span class="sxs-lookup"><span data-stu-id="f26cd-471">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="f26cd-472">Définition</span><span class="sxs-lookup"><span data-stu-id="f26cd-472">Definition</span></span>

<span data-ttu-id="f26cd-473">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="f26cd-473">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="f26cd-474">La fonction `Func_ireland_eu_tax_file_number` trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="f26cd-474">The function  `Func_ireland_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="f26cd-475">Un mot clé `Keywords_ireland_eu_tax_file_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="f26cd-475">A keyword from  `Keywords_ireland_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="f26cd-476">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="f26cd-476">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="f26cd-477">La fonction `Func_ireland_eu_tax_file_number` trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="f26cd-477">The function  `Func_ireland_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="f26cd-478">Mots clés</span><span class="sxs-lookup"><span data-stu-id="f26cd-478">Keywords</span></span>

#### <a name="keywords_ireland_eu_tax_file_number"></a><span data-ttu-id="f26cd-479">Keywords_ireland_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="f26cd-479">Keywords_ireland_eu_tax_file_number</span></span>

<span data-ttu-id="f26cd-480">Numéro de service public</span><span class="sxs-lookup"><span data-stu-id="f26cd-480">public service no</span></span>
  
<span data-ttu-id="f26cd-481">service public personnel</span><span class="sxs-lookup"><span data-stu-id="f26cd-481">personal public service no</span></span>
  
<span data-ttu-id="f26cd-482">n ° PPS</span><span class="sxs-lookup"><span data-stu-id="f26cd-482">pps no</span></span>
  
<span data-ttu-id="f26cd-483">Numéro de service personnel</span><span class="sxs-lookup"><span data-stu-id="f26cd-483">personal service no</span></span>
  
<span data-ttu-id="f26cd-484">n ° de Service PPS</span><span class="sxs-lookup"><span data-stu-id="f26cd-484">pps service no</span></span>
  
<span data-ttu-id="f26cd-485">ppsno #</span><span class="sxs-lookup"><span data-stu-id="f26cd-485">ppsno#</span></span>
  
<span data-ttu-id="f26cd-486">n ° PPS irlandais</span><span class="sxs-lookup"><span data-stu-id="f26cd-486">irish pps no</span></span>
  
<span data-ttu-id="f26cd-487">publicserviceno #</span><span class="sxs-lookup"><span data-stu-id="f26cd-487">publicserviceno#</span></span>
  
<span data-ttu-id="f26cd-488">Numéro de service public</span><span class="sxs-lookup"><span data-stu-id="f26cd-488">personal public service number</span></span>
  
<span data-ttu-id="f26cd-489">uimhir phearsanta seirbhíse poiblí</span><span class="sxs-lookup"><span data-stu-id="f26cd-489">uimhir phearsanta seirbhíse poiblí</span></span>
  
<span data-ttu-id="f26cd-490">PPS uimh</span><span class="sxs-lookup"><span data-stu-id="f26cd-490">pps uimh</span></span>
  
<span data-ttu-id="f26cd-491">uimhir aitheantais phearsanta</span><span class="sxs-lookup"><span data-stu-id="f26cd-491">uimhir aitheantais phearsanta</span></span>
  
## <a name="italy"></a><span data-ttu-id="f26cd-492">Italie</span><span class="sxs-lookup"><span data-stu-id="f26cd-492">Italy</span></span>

### <a name="format"></a><span data-ttu-id="f26cd-493">Format</span><span class="sxs-lookup"><span data-stu-id="f26cd-493">Format</span></span>

<span data-ttu-id="f26cd-494">16 lettres et chiffres dans le modèle spécifié</span><span class="sxs-lookup"><span data-stu-id="f26cd-494">16 letters and digits in the specified pattern</span></span>
  
### <a name="pattern"></a><span data-ttu-id="f26cd-495">Modèle</span><span class="sxs-lookup"><span data-stu-id="f26cd-495">Pattern</span></span>

<span data-ttu-id="f26cd-496">16 lettres et chiffres :</span><span class="sxs-lookup"><span data-stu-id="f26cd-496">16 letters and digits:</span></span>
  
-  <span data-ttu-id="f26cd-497">Trois lettres qui correspondent aux trois premières consonnes du nom de la famille</span><span class="sxs-lookup"><span data-stu-id="f26cd-497">Three letters that correspond to the first three consonants in the family name</span></span> 
    
- <span data-ttu-id="f26cd-498">Trois lettres qui correspondent à la première, troisième et quatrième consonnes du prénom</span><span class="sxs-lookup"><span data-stu-id="f26cd-498">Three letters that correspond to the first, third, and fourth consonants in the first name</span></span>
    
- <span data-ttu-id="f26cd-499">Deux chiffres correspondant aux derniers chiffres de l’année de naissance</span><span class="sxs-lookup"><span data-stu-id="f26cd-499">Two digits that correspond to the last digits of the birth year</span></span>
    
- <span data-ttu-id="f26cd-500">Un chiffre correspondant au mois de naissance : les lettres sont utilisées par ordre alphabétique, mais seules les lettres de A à E, H, L, M, P, R à T sont utilisées (en janvier, A et octobre est R).</span><span class="sxs-lookup"><span data-stu-id="f26cd-500">One digit that corresponds to the month of birth—letters are used in alphabetical order, but only the letters A to E, H, L, M, P, R to T are used (thus, January is A and October is R)</span></span>
    
- <span data-ttu-id="f26cd-501">Deux chiffres correspondant au jour du mois de naissance où 40 est ajouté au jour de naissance pour que les femmes différencient les hommes</span><span class="sxs-lookup"><span data-stu-id="f26cd-501">Two digits that correspond to the day of the month of birth where 40 is added to the day of birth for females to differentiate from males</span></span>
    
- <span data-ttu-id="f26cd-502">Quatre chiffres correspondant à un indicatif régional spécifique à la municipalité où la personne est né — des codes nationaux sont utilisés pour les pays étrangers</span><span class="sxs-lookup"><span data-stu-id="f26cd-502">Four digits that correspond to an area code specific to the municipality where the person was born—country-wide codes are used for foreign countries</span></span>
    
- <span data-ttu-id="f26cd-503">Un chiffre de contrôle</span><span class="sxs-lookup"><span data-stu-id="f26cd-503">One check digit</span></span>
    
### <a name="checksum"></a><span data-ttu-id="f26cd-504">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="f26cd-504">Checksum</span></span>

<span data-ttu-id="f26cd-505">Oui</span><span class="sxs-lookup"><span data-stu-id="f26cd-505">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="f26cd-506">Définition</span><span class="sxs-lookup"><span data-stu-id="f26cd-506">Definition</span></span>

<span data-ttu-id="f26cd-507">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="f26cd-507">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="f26cd-508">La fonction `Func_italy_eu_tax_file_number` trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="f26cd-508">The function  `Func_italy_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="f26cd-509">Un mot clé `Keywords_italy_eu_tax_file_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="f26cd-509">A keyword from  `Keywords_italy_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="f26cd-510">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="f26cd-510">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="f26cd-511">La fonction `Func_italy_eu_tax_file_number` trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="f26cd-511">The function  `Func_italy_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="f26cd-512">Mots clés</span><span class="sxs-lookup"><span data-stu-id="f26cd-512">Keywords</span></span>

#### <a name="keywords_italy_eu_tax_file_number"></a><span data-ttu-id="f26cd-513">Keywords_italy_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="f26cd-513">Keywords_italy_eu_tax_file_number</span></span>

<span data-ttu-id="f26cd-514">Numéro de taxe</span><span class="sxs-lookup"><span data-stu-id="f26cd-514">tax number</span></span>
  
<span data-ttu-id="f26cd-515">n ° taxe</span><span class="sxs-lookup"><span data-stu-id="f26cd-515">tax no.</span></span>
  
<span data-ttu-id="f26cd-516">taxno #</span><span class="sxs-lookup"><span data-stu-id="f26cd-516">taxno#</span></span>
  
<span data-ttu-id="f26cd-517">taxnumber #</span><span class="sxs-lookup"><span data-stu-id="f26cd-517">taxnumber#</span></span>
  
<span data-ttu-id="f26cd-518">taxnumber</span><span class="sxs-lookup"><span data-stu-id="f26cd-518">taxnumber</span></span>
  
<span data-ttu-id="f26cd-519">id fiscal</span><span class="sxs-lookup"><span data-stu-id="f26cd-519">tax id</span></span>
  
<span data-ttu-id="f26cd-520">taxi #</span><span class="sxs-lookup"><span data-stu-id="f26cd-520">taxid#</span></span>
  
<span data-ttu-id="f26cd-521">code fiscal</span><span class="sxs-lookup"><span data-stu-id="f26cd-521">fiscal code</span></span>
  
<span data-ttu-id="f26cd-522">Codice fiscale</span><span class="sxs-lookup"><span data-stu-id="f26cd-522">codice fiscale</span></span>
  
## <a name="latvia"></a><span data-ttu-id="f26cd-523">Lettonie</span><span class="sxs-lookup"><span data-stu-id="f26cd-523">Latvia</span></span>

### <a name="format"></a><span data-ttu-id="f26cd-524">Format</span><span class="sxs-lookup"><span data-stu-id="f26cd-524">Format</span></span>

<span data-ttu-id="f26cd-525">11 chiffres sans espaces ni délimiteurs</span><span class="sxs-lookup"><span data-stu-id="f26cd-525">11 digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="f26cd-526">Modèle</span><span class="sxs-lookup"><span data-stu-id="f26cd-526">Pattern</span></span>

<span data-ttu-id="f26cd-527">11 chiffres dans le modèle spécifié</span><span class="sxs-lookup"><span data-stu-id="f26cd-527">11 digits in the specified pattern</span></span>
  
-  <span data-ttu-id="f26cd-528">Six chiffres correspondant à la date de naissance (JJMMAA)</span><span class="sxs-lookup"><span data-stu-id="f26cd-528">Six digits that correspond to the date of birth (DDMMYY)</span></span> 
    
- <span data-ttu-id="f26cd-529">Un chiffre correspondant au siècle de naissance où « 0 » correspond à 19 siècle, « 1 » correspond au vingtième siècle et « 2 » au 21ème siècle.</span><span class="sxs-lookup"><span data-stu-id="f26cd-529">One digit that corresponds to the century of birth where "0" corresponds to 19th century, "1" corresponds to 20th century, and "2"corresponds to 21st century</span></span>
    
- <span data-ttu-id="f26cd-530">Quatre chiffres</span><span class="sxs-lookup"><span data-stu-id="f26cd-530">Four digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="f26cd-531">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="f26cd-531">Checksum</span></span>

<span data-ttu-id="f26cd-532">Oui</span><span class="sxs-lookup"><span data-stu-id="f26cd-532">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="f26cd-533">Définition</span><span class="sxs-lookup"><span data-stu-id="f26cd-533">Definition</span></span>

<span data-ttu-id="f26cd-534">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="f26cd-534">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="f26cd-535">La fonction `Func_latvia_eu_tax_file_number` trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="f26cd-535">The function  `Func_latvia_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="f26cd-536">Un mot clé `Keywords_latvia_eu_tax_file_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="f26cd-536">A keyword from  `Keywords_latvia_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="f26cd-537">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="f26cd-537">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="f26cd-538">La fonction `Func_latvia_eu_tax_file_number` trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="f26cd-538">The function  `Func_latvia_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="f26cd-539">Mots clés</span><span class="sxs-lookup"><span data-stu-id="f26cd-539">Keywords</span></span>

#### <a name="keywords_latvia_eu_tax_file_number"></a><span data-ttu-id="f26cd-540">Keywords_latvia_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="f26cd-540">Keywords_latvia_eu_tax_file_number</span></span>

<span data-ttu-id="f26cd-541">Numéro de taxe</span><span class="sxs-lookup"><span data-stu-id="f26cd-541">tax number</span></span>
  
<span data-ttu-id="f26cd-542">n ° taxe</span><span class="sxs-lookup"><span data-stu-id="f26cd-542">tax no.</span></span>
  
<span data-ttu-id="f26cd-543">taxno #</span><span class="sxs-lookup"><span data-stu-id="f26cd-543">taxno#</span></span>
  
<span data-ttu-id="f26cd-544">taxnumber #</span><span class="sxs-lookup"><span data-stu-id="f26cd-544">taxnumber#</span></span>
  
<span data-ttu-id="f26cd-545">taxnumber</span><span class="sxs-lookup"><span data-stu-id="f26cd-545">taxnumber</span></span>
  
<span data-ttu-id="f26cd-546">id fiscal</span><span class="sxs-lookup"><span data-stu-id="f26cd-546">tax id</span></span>
  
<span data-ttu-id="f26cd-547">taxi #</span><span class="sxs-lookup"><span data-stu-id="f26cd-547">taxid#</span></span>
  
<span data-ttu-id="f26cd-548">Numéro d’identification de taxe</span><span class="sxs-lookup"><span data-stu-id="f26cd-548">tax identification number</span></span>
  
<span data-ttu-id="f26cd-549">n ° d’identification fiscale</span><span class="sxs-lookup"><span data-stu-id="f26cd-549">tax identification no.</span></span>
  
<span data-ttu-id="f26cd-550">nodokļa numurs</span><span class="sxs-lookup"><span data-stu-id="f26cd-550">nodokļa numurs</span></span>
  
<span data-ttu-id="f26cd-551">nodokļu identifikācijas numurs</span><span class="sxs-lookup"><span data-stu-id="f26cd-551">nodokļu identifikācijas numurs</span></span>
  
<span data-ttu-id="f26cd-552">nodokļu identifikācija numurs</span><span class="sxs-lookup"><span data-stu-id="f26cd-552">nodokļu identifikācija numurs</span></span>
  
## <a name="lithuania"></a><span data-ttu-id="f26cd-553">Lituanie</span><span class="sxs-lookup"><span data-stu-id="f26cd-553">Lithuania</span></span>

### <a name="format"></a><span data-ttu-id="f26cd-554">Format</span><span class="sxs-lookup"><span data-stu-id="f26cd-554">Format</span></span>

<span data-ttu-id="f26cd-555">11 chiffres sans espaces ni délimiteurs</span><span class="sxs-lookup"><span data-stu-id="f26cd-555">11 digits without spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="f26cd-556">Modèle</span><span class="sxs-lookup"><span data-stu-id="f26cd-556">Pattern</span></span>

<span data-ttu-id="f26cd-557">11 chiffres</span><span class="sxs-lookup"><span data-stu-id="f26cd-557">11 digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="f26cd-558">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="f26cd-558">Checksum</span></span>

<span data-ttu-id="f26cd-559">Non applicable</span><span class="sxs-lookup"><span data-stu-id="f26cd-559">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="f26cd-560">Définition</span><span class="sxs-lookup"><span data-stu-id="f26cd-560">Definition</span></span>

<span data-ttu-id="f26cd-561">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="f26cd-561">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="f26cd-562">La fonction `Func_lithuania_eu_tax_file_number` trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="f26cd-562">The function  `Func_lithuania_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="f26cd-563">Un mot clé `Keywords_lithuania_eu_tax_file_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="f26cd-563">A keyword from  `Keywords_lithuania_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="f26cd-564">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="f26cd-564">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="f26cd-565">La fonction `Func_lithuania_eu_tax_file_number` trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="f26cd-565">The function  `Func_lithuania_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="f26cd-566">Mots clés</span><span class="sxs-lookup"><span data-stu-id="f26cd-566">Keywords</span></span>

#### <a name="keywords_lithuania_eu_tax_file_number"></a><span data-ttu-id="f26cd-567">Keywords_lithuania_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="f26cd-567">Keywords_lithuania_eu_tax_file_number</span></span>

<span data-ttu-id="f26cd-568">Numéro de taxe</span><span class="sxs-lookup"><span data-stu-id="f26cd-568">tax number</span></span>
  
<span data-ttu-id="f26cd-569">n ° taxe</span><span class="sxs-lookup"><span data-stu-id="f26cd-569">tax no.</span></span>
  
<span data-ttu-id="f26cd-570">n ° taxe #</span><span class="sxs-lookup"><span data-stu-id="f26cd-570">tax no#</span></span>
  
<span data-ttu-id="f26cd-571">taxnumber #</span><span class="sxs-lookup"><span data-stu-id="f26cd-571">taxnumber#</span></span>
  
<span data-ttu-id="f26cd-572">taxnumber</span><span class="sxs-lookup"><span data-stu-id="f26cd-572">taxnumber</span></span>
  
<span data-ttu-id="f26cd-573">id fiscal</span><span class="sxs-lookup"><span data-stu-id="f26cd-573">tax id</span></span>
  
<span data-ttu-id="f26cd-574">taxi #</span><span class="sxs-lookup"><span data-stu-id="f26cd-574">taxid#</span></span>
  
<span data-ttu-id="f26cd-575">Numéro d’identification de taxe</span><span class="sxs-lookup"><span data-stu-id="f26cd-575">tax identification number</span></span>
  
<span data-ttu-id="f26cd-576">n ° d’identification fiscale</span><span class="sxs-lookup"><span data-stu-id="f26cd-576">tax identification no.</span></span>
  
<span data-ttu-id="f26cd-577">ID mokesčių</span><span class="sxs-lookup"><span data-stu-id="f26cd-577">mokesčių id</span></span>
  
<span data-ttu-id="f26cd-578">mokesčių chiffres</span><span class="sxs-lookup"><span data-stu-id="f26cd-578">mokesčių numeris</span></span>
  
<span data-ttu-id="f26cd-579">mokesčių identifikavimas</span><span class="sxs-lookup"><span data-stu-id="f26cd-579">mokesčių identifikavimas numeris</span></span>
  
## <a name="luxemburg"></a><span data-ttu-id="f26cd-580">Relatif</span><span class="sxs-lookup"><span data-stu-id="f26cd-580">Luxemburg</span></span>

### <a name="format"></a><span data-ttu-id="f26cd-581">Format</span><span class="sxs-lookup"><span data-stu-id="f26cd-581">Format</span></span>

<span data-ttu-id="f26cd-582">13 chiffres sans espaces ni délimiteurs</span><span class="sxs-lookup"><span data-stu-id="f26cd-582">13 digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="f26cd-583">Modèle</span><span class="sxs-lookup"><span data-stu-id="f26cd-583">Pattern</span></span>

<span data-ttu-id="f26cd-584">13 chiffres :</span><span class="sxs-lookup"><span data-stu-id="f26cd-584">13 digits:</span></span>
  
-  <span data-ttu-id="f26cd-585">11 chiffres</span><span class="sxs-lookup"><span data-stu-id="f26cd-585">11 digits</span></span> 
    
- <span data-ttu-id="f26cd-586">Deux chiffres de contrôle</span><span class="sxs-lookup"><span data-stu-id="f26cd-586">Two check digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="f26cd-587">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="f26cd-587">Checksum</span></span>

<span data-ttu-id="f26cd-588">Oui</span><span class="sxs-lookup"><span data-stu-id="f26cd-588">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="f26cd-589">Définition</span><span class="sxs-lookup"><span data-stu-id="f26cd-589">Definition</span></span>

<span data-ttu-id="f26cd-590">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="f26cd-590">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="f26cd-591">La fonction `Func_luxemburg_eu_tax_file_number` trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="f26cd-591">The function  `Func_luxemburg_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="f26cd-592">Un mot clé `Keywords_luxemburg_eu_tax_file_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="f26cd-592">A keyword from  `Keywords_luxemburg_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="f26cd-593">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="f26cd-593">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="f26cd-594">La fonction `Func_luxemburg_eu_tax_file_number` trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="f26cd-594">The function  `Func_luxemburg_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="f26cd-595">Mots clés</span><span class="sxs-lookup"><span data-stu-id="f26cd-595">Keywords</span></span>

#### <a name="keywords_luxemburg_eu_tax_file_number"></a><span data-ttu-id="f26cd-596">Keywords_luxemburg_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="f26cd-596">Keywords_luxemburg_eu_tax_file_number</span></span>

<span data-ttu-id="f26cd-597">Numéro de taxe</span><span class="sxs-lookup"><span data-stu-id="f26cd-597">tax number</span></span>
  
<span data-ttu-id="f26cd-598">n ° taxe</span><span class="sxs-lookup"><span data-stu-id="f26cd-598">tax no.</span></span>
  
<span data-ttu-id="f26cd-599">taxno #</span><span class="sxs-lookup"><span data-stu-id="f26cd-599">taxno#</span></span>
  
<span data-ttu-id="f26cd-600">taxnumber #</span><span class="sxs-lookup"><span data-stu-id="f26cd-600">taxnumber#</span></span>
  
<span data-ttu-id="f26cd-601">taxnumber</span><span class="sxs-lookup"><span data-stu-id="f26cd-601">taxnumber</span></span>
  
<span data-ttu-id="f26cd-602">id fiscal</span><span class="sxs-lookup"><span data-stu-id="f26cd-602">tax id</span></span>
  
<span data-ttu-id="f26cd-603">taxi #</span><span class="sxs-lookup"><span data-stu-id="f26cd-603">taxid#</span></span>
  
<span data-ttu-id="f26cd-604">Numéro d’identification de taxe</span><span class="sxs-lookup"><span data-stu-id="f26cd-604">tax identification number</span></span>
  
<span data-ttu-id="f26cd-605">n ° d’identification fiscale</span><span class="sxs-lookup"><span data-stu-id="f26cd-605">tax identification no.</span></span>
  
<span data-ttu-id="f26cd-606">steuernummer</span><span class="sxs-lookup"><span data-stu-id="f26cd-606">steuernummer</span></span>
  
<span data-ttu-id="f26cd-607">ID Steuer</span><span class="sxs-lookup"><span data-stu-id="f26cd-607">steuer id</span></span>
  
<span data-ttu-id="f26cd-608">steueridentifikationsnummer</span><span class="sxs-lookup"><span data-stu-id="f26cd-608">steueridentifikationsnummer</span></span>
  
## <a name="malta"></a><span data-ttu-id="f26cd-609">Malte</span><span class="sxs-lookup"><span data-stu-id="f26cd-609">Malta</span></span>

### <a name="format"></a><span data-ttu-id="f26cd-610">Format</span><span class="sxs-lookup"><span data-stu-id="f26cd-610">Format</span></span>

<span data-ttu-id="f26cd-611">Pour les ressortissants maltais : 7 chiffres et une lettre dans le modèle spécifié</span><span class="sxs-lookup"><span data-stu-id="f26cd-611">For Maltese nationals: 7 digits and one letter in the specified pattern</span></span>
  
<span data-ttu-id="f26cd-612">Ressortissants non maltaises et entités maltaises : 9 chiffres</span><span class="sxs-lookup"><span data-stu-id="f26cd-612">Non-Maltese nationals and Maltese entities: 9 digits</span></span>
  
### <a name="pattern"></a><span data-ttu-id="f26cd-613">Modèle</span><span class="sxs-lookup"><span data-stu-id="f26cd-613">Pattern</span></span>

<span data-ttu-id="f26cd-614">Ressortissants maltaises : 7 chiffres et une lettre</span><span class="sxs-lookup"><span data-stu-id="f26cd-614">Maltese nationals: 7 digits and one letter</span></span>
  
-  <span data-ttu-id="f26cd-615">Sept chiffres </span><span class="sxs-lookup"><span data-stu-id="f26cd-615">Seven digits</span></span> 
    
- <span data-ttu-id="f26cd-616">Une lettre (ne respecte pas la casse)</span><span class="sxs-lookup"><span data-stu-id="f26cd-616">One letter (not case-sensitive)</span></span>
    
<span data-ttu-id="f26cd-617">Ressortissants non maltaises et entités maltaises : 9 chiffres</span><span class="sxs-lookup"><span data-stu-id="f26cd-617">Non-Maltese nationals and Maltese entities: 9 digits</span></span>
  
-  <span data-ttu-id="f26cd-618">Neuf chiffres</span><span class="sxs-lookup"><span data-stu-id="f26cd-618">Nine digits</span></span> 
    
### <a name="checksum"></a><span data-ttu-id="f26cd-619">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="f26cd-619">Checksum</span></span>

<span data-ttu-id="f26cd-620">Non applicable</span><span class="sxs-lookup"><span data-stu-id="f26cd-620">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="f26cd-621">Définition</span><span class="sxs-lookup"><span data-stu-id="f26cd-621">Definition</span></span>

<span data-ttu-id="f26cd-622">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="f26cd-622">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="f26cd-623">La fonction `Func_malta_eu_tax_file_number` trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="f26cd-623">The function  `Func_malta_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="f26cd-624">Un mot clé `Keywords_malta_eu_tax_file_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="f26cd-624">A keyword from  `Keywords_malta_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="f26cd-625">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 65 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="f26cd-625">A DLP policy is 65% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="f26cd-626">La fonction `Func_malta_eu_tax_file_number` trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="f26cd-626">The function  `Func_malta_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="f26cd-627">Mots clés</span><span class="sxs-lookup"><span data-stu-id="f26cd-627">Keywords</span></span>

#### <a name="keywords_malta_eu_tax_file_number"></a><span data-ttu-id="f26cd-628">Keywords_malta_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="f26cd-628">Keywords_malta_eu_tax_file_number</span></span>

<span data-ttu-id="f26cd-629">Numéro de taxe</span><span class="sxs-lookup"><span data-stu-id="f26cd-629">tax number</span></span>
  
<span data-ttu-id="f26cd-630">n ° taxe</span><span class="sxs-lookup"><span data-stu-id="f26cd-630">tax no.</span></span>
  
<span data-ttu-id="f26cd-631">taxno #</span><span class="sxs-lookup"><span data-stu-id="f26cd-631">taxno#</span></span>
  
<span data-ttu-id="f26cd-632">taxnumber #</span><span class="sxs-lookup"><span data-stu-id="f26cd-632">taxnumber#</span></span>
  
<span data-ttu-id="f26cd-633">taxnumber</span><span class="sxs-lookup"><span data-stu-id="f26cd-633">taxnumber</span></span>
  
<span data-ttu-id="f26cd-634">id fiscal</span><span class="sxs-lookup"><span data-stu-id="f26cd-634">tax id</span></span>
  
<span data-ttu-id="f26cd-635">taxi #</span><span class="sxs-lookup"><span data-stu-id="f26cd-635">taxid#</span></span>
  
<span data-ttu-id="f26cd-636">Numéro d’identification de taxe</span><span class="sxs-lookup"><span data-stu-id="f26cd-636">tax identification number</span></span>
  
<span data-ttu-id="f26cd-637">n ° d’identification fiscale</span><span class="sxs-lookup"><span data-stu-id="f26cd-637">tax identification no.</span></span>
  
<span data-ttu-id="f26cd-638">numru tat-Taxxa</span><span class="sxs-lookup"><span data-stu-id="f26cd-638">numru tat-taxxa</span></span>
  
<span data-ttu-id="f26cd-639">ID tat-Taxxa</span><span class="sxs-lookup"><span data-stu-id="f26cd-639">id tat-taxxa</span></span>
  
<span data-ttu-id="f26cd-640">numru ta’IDENTIFIKAZZJONI tat-Taxxa</span><span class="sxs-lookup"><span data-stu-id="f26cd-640">numru ta 'identifikazzjoni tat-taxxa</span></span>
  
## <a name="netherlands"></a><span data-ttu-id="f26cd-641">Pays-Bas</span><span class="sxs-lookup"><span data-stu-id="f26cd-641">Netherlands</span></span>

### <a name="format"></a><span data-ttu-id="f26cd-642">Format</span><span class="sxs-lookup"><span data-stu-id="f26cd-642">Format</span></span>

<span data-ttu-id="f26cd-643">Neuf chiffres sans espaces ni délimiteurs</span><span class="sxs-lookup"><span data-stu-id="f26cd-643">Nine digits without spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="f26cd-644">Modèle</span><span class="sxs-lookup"><span data-stu-id="f26cd-644">Pattern</span></span>

<span data-ttu-id="f26cd-645">Neuf chiffres</span><span class="sxs-lookup"><span data-stu-id="f26cd-645">Nine digits</span></span> 
  
### <a name="checksum"></a><span data-ttu-id="f26cd-646">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="f26cd-646">Checksum</span></span>

<span data-ttu-id="f26cd-647">Oui</span><span class="sxs-lookup"><span data-stu-id="f26cd-647">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="f26cd-648">Définition</span><span class="sxs-lookup"><span data-stu-id="f26cd-648">Definition</span></span>

<span data-ttu-id="f26cd-649">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="f26cd-649">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="f26cd-650">La fonction `Func_netherlands_eu_tax_file_number` trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="f26cd-650">The function  `Func_netherlands_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="f26cd-651">Un mot clé `Keywords_netherlands_eu_tax_file_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="f26cd-651">A keyword from  `Keywords_netherlands_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="f26cd-652">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="f26cd-652">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="f26cd-653">La fonction `Func_netherlands_eu_tax_file_number` trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="f26cd-653">The function  `Func_netherlands_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="f26cd-654">Mots clés</span><span class="sxs-lookup"><span data-stu-id="f26cd-654">Keywords</span></span>

#### <a name="keywords_netherlands_eu_tax_file_number"></a><span data-ttu-id="f26cd-655">Keywords_netherlands_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="f26cd-655">Keywords_netherlands_eu_tax_file_number</span></span>

<span data-ttu-id="f26cd-656">Numéro d’identification fiscale néerlandaise</span><span class="sxs-lookup"><span data-stu-id="f26cd-656">netherlands tax identification number</span></span>
  
<span data-ttu-id="f26cd-657">identification fiscale néerlandaise</span><span class="sxs-lookup"><span data-stu-id="f26cd-657">netherlands tax identification</span></span>
  
<span data-ttu-id="f26cd-658">Numéro d’identification de taxe de Netherland</span><span class="sxs-lookup"><span data-stu-id="f26cd-658">netherland's tax identification number</span></span>
  
<span data-ttu-id="f26cd-659">identification fiscale de Netherland</span><span class="sxs-lookup"><span data-stu-id="f26cd-659">netherland's tax identification</span></span>
  
<span data-ttu-id="f26cd-660">Numéro d’identification de taxe</span><span class="sxs-lookup"><span data-stu-id="f26cd-660">tax identification number</span></span>
  
<span data-ttu-id="f26cd-661">ID de taxe néerlandaise</span><span class="sxs-lookup"><span data-stu-id="f26cd-661">dutch tax id</span></span>
  
<span data-ttu-id="f26cd-662">Numéro d’identification de taxe néerlandaise</span><span class="sxs-lookup"><span data-stu-id="f26cd-662">dutch tax identification number</span></span>
  
<span data-ttu-id="f26cd-663">id fiscal</span><span class="sxs-lookup"><span data-stu-id="f26cd-663">tax id</span></span>
  
<span data-ttu-id="f26cd-664">ID de taxe #</span><span class="sxs-lookup"><span data-stu-id="f26cd-664">tax id#</span></span>
  
<span data-ttu-id="f26cd-665">Numéro de taxe</span><span class="sxs-lookup"><span data-stu-id="f26cd-665">tax number</span></span>
  
<span data-ttu-id="f26cd-666">n ° taxe #</span><span class="sxs-lookup"><span data-stu-id="f26cd-666">tax no#</span></span>
  
<span data-ttu-id="f26cd-667">codes #</span><span class="sxs-lookup"><span data-stu-id="f26cd-667">tax#</span></span>
  
<span data-ttu-id="f26cd-668">Etain</span><span class="sxs-lookup"><span data-stu-id="f26cd-668">tin</span></span>
  
<span data-ttu-id="f26cd-669">Etain #</span><span class="sxs-lookup"><span data-stu-id="f26cd-669">tin#</span></span>
  
<span data-ttu-id="f26cd-670">étain (Pays-Bas)</span><span class="sxs-lookup"><span data-stu-id="f26cd-670">netherlands tin</span></span>
  
<span data-ttu-id="f26cd-671">Netherland d’étain</span><span class="sxs-lookup"><span data-stu-id="f26cd-671">netherland's tin</span></span>
  
<span data-ttu-id="f26cd-672">néerlandais qui a identificatienummer</span><span class="sxs-lookup"><span data-stu-id="f26cd-672">nederlands belasting identificatienummer</span></span>
  
<span data-ttu-id="f26cd-673">identificatienummer van à l’avant-dernière</span><span class="sxs-lookup"><span data-stu-id="f26cd-673">identificatienummer van belasting</span></span>
  
<span data-ttu-id="f26cd-674">identificatienummer qui a été modifié</span><span class="sxs-lookup"><span data-stu-id="f26cd-674">identificatienummer belasting</span></span>
  
<span data-ttu-id="f26cd-675">néerlandais qui a identificatie</span><span class="sxs-lookup"><span data-stu-id="f26cd-675">nederlands belasting identificatie</span></span>
  
<span data-ttu-id="f26cd-676">néerlandais qui a pour ID Nummer</span><span class="sxs-lookup"><span data-stu-id="f26cd-676">nederlands belasting id nummer</span></span>
  
<span data-ttu-id="f26cd-677">Néerlandais belastingnummer</span><span class="sxs-lookup"><span data-stu-id="f26cd-677">nederlands belastingnummer</span></span>
  
<span data-ttu-id="f26cd-678">btw nummer</span><span class="sxs-lookup"><span data-stu-id="f26cd-678">btw nummer</span></span>
  
<span data-ttu-id="f26cd-679">Nederlandse qui a identificatie</span><span class="sxs-lookup"><span data-stu-id="f26cd-679">nederlandse belasting identificatie</span></span>
  
## <a name="poland"></a><span data-ttu-id="f26cd-680">Pologne</span><span class="sxs-lookup"><span data-stu-id="f26cd-680">Poland</span></span>

### <a name="format"></a><span data-ttu-id="f26cd-681">Format</span><span class="sxs-lookup"><span data-stu-id="f26cd-681">Format</span></span>

<span data-ttu-id="f26cd-682">Onze chiffres sans espaces ni délimiteurs</span><span class="sxs-lookup"><span data-stu-id="f26cd-682">Eleven digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="f26cd-683">Modèle</span><span class="sxs-lookup"><span data-stu-id="f26cd-683">Pattern</span></span>

<span data-ttu-id="f26cd-684">Onze chiffres</span><span class="sxs-lookup"><span data-stu-id="f26cd-684">Eleven digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="f26cd-685">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="f26cd-685">Checksum</span></span>

<span data-ttu-id="f26cd-686">Oui</span><span class="sxs-lookup"><span data-stu-id="f26cd-686">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="f26cd-687">Définition</span><span class="sxs-lookup"><span data-stu-id="f26cd-687">Definition</span></span>

<span data-ttu-id="f26cd-688">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="f26cd-688">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="f26cd-689">La fonction `Func_poland_eu_tax_file_number` trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="f26cd-689">The function  `Func_poland_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="f26cd-690">Un mot clé `Keywords_poland_eu_tax_file_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="f26cd-690">A keyword from  `Keywords_poland_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="f26cd-691">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="f26cd-691">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="f26cd-692">La fonction `Func_poland_eu_tax_file_number` trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="f26cd-692">The function  `Func_poland_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="f26cd-693">Mots clés</span><span class="sxs-lookup"><span data-stu-id="f26cd-693">Keywords</span></span>

#### <a name="keywords_poland_eu_tax_file_number"></a><span data-ttu-id="f26cd-694">Keywords_poland_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="f26cd-694">Keywords_poland_eu_tax_file_number</span></span>

<span data-ttu-id="f26cd-695">Numéro de taxe</span><span class="sxs-lookup"><span data-stu-id="f26cd-695">tax number</span></span>
  
<span data-ttu-id="f26cd-696">n ° taxe</span><span class="sxs-lookup"><span data-stu-id="f26cd-696">tax no.</span></span>
  
<span data-ttu-id="f26cd-697">taxno #</span><span class="sxs-lookup"><span data-stu-id="f26cd-697">taxno#</span></span>
  
<span data-ttu-id="f26cd-698">taxnumber #</span><span class="sxs-lookup"><span data-stu-id="f26cd-698">taxnumber#</span></span>
  
<span data-ttu-id="f26cd-699">taxnumber</span><span class="sxs-lookup"><span data-stu-id="f26cd-699">taxnumber</span></span>
  
<span data-ttu-id="f26cd-700">pince</span><span class="sxs-lookup"><span data-stu-id="f26cd-700">nip</span></span>
  
<span data-ttu-id="f26cd-701">pince #</span><span class="sxs-lookup"><span data-stu-id="f26cd-701">nip#</span></span>
  
<span data-ttu-id="f26cd-702">id fiscal</span><span class="sxs-lookup"><span data-stu-id="f26cd-702">tax id</span></span>
  
<span data-ttu-id="f26cd-703">ID de taxe #</span><span class="sxs-lookup"><span data-stu-id="f26cd-703">tax id#</span></span>
  
<span data-ttu-id="f26cd-704">ID du NIP</span><span class="sxs-lookup"><span data-stu-id="f26cd-704">nip id</span></span>
  
<span data-ttu-id="f26cd-705">ID du NIP #</span><span class="sxs-lookup"><span data-stu-id="f26cd-705">nip id#</span></span>
  
<span data-ttu-id="f26cd-706">Numéro d’identification de taxe</span><span class="sxs-lookup"><span data-stu-id="f26cd-706">tax identification number</span></span>
  
<span data-ttu-id="f26cd-707">n ° d’identification fiscale</span><span class="sxs-lookup"><span data-stu-id="f26cd-707">tax identification no.</span></span>
  
<span data-ttu-id="f26cd-708">Numéro de TVA</span><span class="sxs-lookup"><span data-stu-id="f26cd-708">vat number</span></span>
  
<span data-ttu-id="f26cd-709">n ° TVA</span><span class="sxs-lookup"><span data-stu-id="f26cd-709">vat no.</span></span>
  
<span data-ttu-id="f26cd-710">vatno #</span><span class="sxs-lookup"><span data-stu-id="f26cd-710">vatno#</span></span>
  
<span data-ttu-id="f26cd-711">Numéro de TVA</span><span class="sxs-lookup"><span data-stu-id="f26cd-711">vat id</span></span>
  
<span data-ttu-id="f26cd-712">Numéro de TVA #</span><span class="sxs-lookup"><span data-stu-id="f26cd-712">vat id#</span></span>
  
<span data-ttu-id="f26cd-713">chiffre identyfikacji podatkowej</span><span class="sxs-lookup"><span data-stu-id="f26cd-713">numer identyfikacji podatkowej</span></span>
  
<span data-ttu-id="f26cd-714">Polski identyfikacji podatkowej</span><span class="sxs-lookup"><span data-stu-id="f26cd-714">polski numer identyfikacji podatkowej</span></span>
  
<span data-ttu-id="f26cd-715">numeridentyfikacjipodatkowej #</span><span class="sxs-lookup"><span data-stu-id="f26cd-715">numeridentyfikacjipodatkowej#</span></span>
  
## <a name="portugal"></a><span data-ttu-id="f26cd-716">Portugal</span><span class="sxs-lookup"><span data-stu-id="f26cd-716">Portugal</span></span>

### <a name="format"></a><span data-ttu-id="f26cd-717">Format</span><span class="sxs-lookup"><span data-stu-id="f26cd-717">Format</span></span>

<span data-ttu-id="f26cd-718">Neuf chiffres sans espaces ni délimiteurs</span><span class="sxs-lookup"><span data-stu-id="f26cd-718">Nine digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="f26cd-719">Modèle</span><span class="sxs-lookup"><span data-stu-id="f26cd-719">Pattern</span></span>

<span data-ttu-id="f26cd-720">Neuf chiffres</span><span class="sxs-lookup"><span data-stu-id="f26cd-720">Nine digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="f26cd-721">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="f26cd-721">Checksum</span></span>

<span data-ttu-id="f26cd-722">Oui</span><span class="sxs-lookup"><span data-stu-id="f26cd-722">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="f26cd-723">Définition</span><span class="sxs-lookup"><span data-stu-id="f26cd-723">Definition</span></span>

<span data-ttu-id="f26cd-724">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="f26cd-724">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="f26cd-725">La fonction `Func_portugal_eu_tax_file_number` trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="f26cd-725">The function  `Func_portugal_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="f26cd-726">Un mot clé `Keywords_portugal_eu_tax_file_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="f26cd-726">A keyword from  `Keywords_portugal_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="f26cd-727">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="f26cd-727">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="f26cd-728">La fonction `Func_portugal_eu_tax_file_number` trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="f26cd-728">The function  `Func_portugal_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="f26cd-729">Mots clés</span><span class="sxs-lookup"><span data-stu-id="f26cd-729">Keywords</span></span>

#### <a name="keywords_portugal_eu_tax_file_number"></a><span data-ttu-id="f26cd-730">Keywords_portugal_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="f26cd-730">Keywords_portugal_eu_tax_file_number</span></span>

<span data-ttu-id="f26cd-731">Numéro de taxe</span><span class="sxs-lookup"><span data-stu-id="f26cd-731">tax number</span></span>
  
<span data-ttu-id="f26cd-732">n ° taxe</span><span class="sxs-lookup"><span data-stu-id="f26cd-732">tax no.</span></span>
  
<span data-ttu-id="f26cd-733">taxno #</span><span class="sxs-lookup"><span data-stu-id="f26cd-733">taxno#</span></span>
  
<span data-ttu-id="f26cd-734">taxnumber #</span><span class="sxs-lookup"><span data-stu-id="f26cd-734">taxnumber#</span></span>
  
<span data-ttu-id="f26cd-735">taxnumber</span><span class="sxs-lookup"><span data-stu-id="f26cd-735">taxnumber</span></span>
  
<span data-ttu-id="f26cd-736">nPour</span><span class="sxs-lookup"><span data-stu-id="f26cd-736">nif</span></span>
  
<span data-ttu-id="f26cd-737">nPour #</span><span class="sxs-lookup"><span data-stu-id="f26cd-737">nif#</span></span>
  
<span data-ttu-id="f26cd-738">chiffres fiscaux</span><span class="sxs-lookup"><span data-stu-id="f26cd-738">numero fiscal</span></span>
  
<span data-ttu-id="f26cd-739">Número de identificação fiscal</span><span class="sxs-lookup"><span data-stu-id="f26cd-739">número de identificação fiscal</span></span>
  
## <a name="romania"></a><span data-ttu-id="f26cd-740">Roumanie</span><span class="sxs-lookup"><span data-stu-id="f26cd-740">Romania</span></span>

### <a name="format"></a><span data-ttu-id="f26cd-741">Format</span><span class="sxs-lookup"><span data-stu-id="f26cd-741">Format</span></span>

<span data-ttu-id="f26cd-742">13 chiffres sans espaces ni délimiteurs</span><span class="sxs-lookup"><span data-stu-id="f26cd-742">13 digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="f26cd-743">Modèle</span><span class="sxs-lookup"><span data-stu-id="f26cd-743">Pattern</span></span>

<span data-ttu-id="f26cd-744">13 chiffres</span><span class="sxs-lookup"><span data-stu-id="f26cd-744">13 digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="f26cd-745">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="f26cd-745">Checksum</span></span>

<span data-ttu-id="f26cd-746">Non applicable</span><span class="sxs-lookup"><span data-stu-id="f26cd-746">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="f26cd-747">Définition</span><span class="sxs-lookup"><span data-stu-id="f26cd-747">Definition</span></span>

<span data-ttu-id="f26cd-748">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="f26cd-748">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="f26cd-749">L’expression `Regex_romania_eu_tax_file_number` régulière trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="f26cd-749">The regular expression  `Regex_romania_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="f26cd-750">Un mot clé `Keywords_romania_eu_tax_file_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="f26cd-750">A keyword from  `Keywords_romania_eu_tax_file_number` is found.</span></span> 
    
```
 <!-- EU Tax File Number -->
<Entity id="e09c07d3-66e5-4783-989d-49ac62748f5f" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_romania_eu_tax_file_number" />
          <Match idRef="Keywords_romania_eu_tax_file_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="f26cd-751">Mots clés</span><span class="sxs-lookup"><span data-stu-id="f26cd-751">Keywords</span></span>

#### <a name="keywords_romania_eu_tax_file_number"></a><span data-ttu-id="f26cd-752">Keywords_romania_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="f26cd-752">Keywords_romania_eu_tax_file_number</span></span>

<span data-ttu-id="f26cd-753">id fiscal</span><span class="sxs-lookup"><span data-stu-id="f26cd-753">tax id</span></span>
  
<span data-ttu-id="f26cd-754">Numéro d’identification de taxe</span><span class="sxs-lookup"><span data-stu-id="f26cd-754">tax id number</span></span>
  
<span data-ttu-id="f26cd-755">n ° fichier taxe</span><span class="sxs-lookup"><span data-stu-id="f26cd-755">tax file no</span></span>
  
<span data-ttu-id="f26cd-756">numéro de dossier fiscal</span><span class="sxs-lookup"><span data-stu-id="f26cd-756">tax file number</span></span>
  
<span data-ttu-id="f26cd-757">n ° taxe</span><span class="sxs-lookup"><span data-stu-id="f26cd-757">tax no</span></span>
  
<span data-ttu-id="f26cd-758">Numéro de taxe</span><span class="sxs-lookup"><span data-stu-id="f26cd-758">tax number</span></span>
  
<span data-ttu-id="f26cd-759">taxi #</span><span class="sxs-lookup"><span data-stu-id="f26cd-759">taxid#</span></span>
  
<span data-ttu-id="f26cd-760">taxno #</span><span class="sxs-lookup"><span data-stu-id="f26cd-760">taxno#</span></span>
  
<span data-ttu-id="f26cd-761">ID-UL taxei</span><span class="sxs-lookup"><span data-stu-id="f26cd-761">id-ul taxei</span></span>
  
<span data-ttu-id="f26cd-762">numărul de IDENTIFICARE fiscală</span><span class="sxs-lookup"><span data-stu-id="f26cd-762">numărul de identificare fiscală</span></span>
  
## <a name="slovakia"></a><span data-ttu-id="f26cd-763">République de Slovaquie</span><span class="sxs-lookup"><span data-stu-id="f26cd-763">Slovakia</span></span>

### <a name="format"></a><span data-ttu-id="f26cd-764">Format</span><span class="sxs-lookup"><span data-stu-id="f26cd-764">Format</span></span>

<span data-ttu-id="f26cd-765">10 chiffres sans espaces ni délimiteurs</span><span class="sxs-lookup"><span data-stu-id="f26cd-765">10 digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="f26cd-766">Modèle</span><span class="sxs-lookup"><span data-stu-id="f26cd-766">Pattern</span></span>

<span data-ttu-id="f26cd-767">10 chiffres</span><span class="sxs-lookup"><span data-stu-id="f26cd-767">10 digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="f26cd-768">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="f26cd-768">Checksum</span></span>

<span data-ttu-id="f26cd-769">Non applicable</span><span class="sxs-lookup"><span data-stu-id="f26cd-769">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="f26cd-770">Définition</span><span class="sxs-lookup"><span data-stu-id="f26cd-770">Definition</span></span>

<span data-ttu-id="f26cd-771">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="f26cd-771">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="f26cd-772">L’expression `Regex_slovakia_eu_tax_file_number` régulière trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="f26cd-772">The regular expression  `Regex_slovakia_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="f26cd-773">Un mot clé `Keywords_slovakia_eu_tax_file_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="f26cd-773">A keyword from  `Keywords_slovakia_eu_tax_file_number` is found.</span></span> 
    
```
 <!-- EU Tax File Number -->
<Entity id="e09c07d3-66e5-4783-989d-49ac62748f5f" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_slovakia_eu_tax_file_number" />
          <Match idRef="Keywords_slovakia_eu_tax_file_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="f26cd-774">Mots clés</span><span class="sxs-lookup"><span data-stu-id="f26cd-774">Keywords</span></span>

#### <a name="keywords_slovakia_eu_tax_file_number"></a><span data-ttu-id="f26cd-775">Keywords_slovakia_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="f26cd-775">Keywords_slovakia_eu_tax_file_number</span></span>

<span data-ttu-id="f26cd-776">id fiscal</span><span class="sxs-lookup"><span data-stu-id="f26cd-776">tax id</span></span>
  
<span data-ttu-id="f26cd-777">Numéro d’identification de taxe</span><span class="sxs-lookup"><span data-stu-id="f26cd-777">tax id number</span></span>
  
<span data-ttu-id="f26cd-778">ID d’étain</span><span class="sxs-lookup"><span data-stu-id="f26cd-778">tin id</span></span>
  
<span data-ttu-id="f26cd-779">n ° d’étain</span><span class="sxs-lookup"><span data-stu-id="f26cd-779">tin no</span></span>
  
<span data-ttu-id="f26cd-780">ID d’étain slovaque</span><span class="sxs-lookup"><span data-stu-id="f26cd-780">slovakian tin id</span></span>
  
<span data-ttu-id="f26cd-781">Etain</span><span class="sxs-lookup"><span data-stu-id="f26cd-781">tin</span></span>
  
<span data-ttu-id="f26cd-782">n ° fichier taxe</span><span class="sxs-lookup"><span data-stu-id="f26cd-782">tax file no</span></span>
  
<span data-ttu-id="f26cd-783">numéro de dossier fiscal</span><span class="sxs-lookup"><span data-stu-id="f26cd-783">tax file number</span></span>
  
<span data-ttu-id="f26cd-784">n ° taxe</span><span class="sxs-lookup"><span data-stu-id="f26cd-784">tax no</span></span>
  
<span data-ttu-id="f26cd-785">Numéro de taxe</span><span class="sxs-lookup"><span data-stu-id="f26cd-785">tax number</span></span>
  
<span data-ttu-id="f26cd-786">taxi #</span><span class="sxs-lookup"><span data-stu-id="f26cd-786">taxid#</span></span>
  
<span data-ttu-id="f26cd-787">taxno #</span><span class="sxs-lookup"><span data-stu-id="f26cd-787">taxno#</span></span>
  
<span data-ttu-id="f26cd-788">daňové identifikačné číslo</span><span class="sxs-lookup"><span data-stu-id="f26cd-788">daňové identifikačné číslo</span></span>
  
<span data-ttu-id="f26cd-789">daňové číslo</span><span class="sxs-lookup"><span data-stu-id="f26cd-789">daňové číslo</span></span>
  
<span data-ttu-id="f26cd-790">daňové číslo súboru</span><span class="sxs-lookup"><span data-stu-id="f26cd-790">daňové číslo súboru</span></span>
  
## <a name="slovenia"></a><span data-ttu-id="f26cd-791">Slovénie</span><span class="sxs-lookup"><span data-stu-id="f26cd-791">Slovenia</span></span>

### <a name="format"></a><span data-ttu-id="f26cd-792">Format</span><span class="sxs-lookup"><span data-stu-id="f26cd-792">Format</span></span>

<span data-ttu-id="f26cd-793">Huit chiffres sans espaces ni délimiteurs</span><span class="sxs-lookup"><span data-stu-id="f26cd-793">Eight digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="f26cd-794">Modèle</span><span class="sxs-lookup"><span data-stu-id="f26cd-794">Pattern</span></span>

<span data-ttu-id="f26cd-795">Huit chiffres</span><span class="sxs-lookup"><span data-stu-id="f26cd-795">Eight digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="f26cd-796">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="f26cd-796">Checksum</span></span>

<span data-ttu-id="f26cd-797">Oui</span><span class="sxs-lookup"><span data-stu-id="f26cd-797">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="f26cd-798">Définition</span><span class="sxs-lookup"><span data-stu-id="f26cd-798">Definition</span></span>

<span data-ttu-id="f26cd-799">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="f26cd-799">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="f26cd-800">La fonction `Func_slovenia_eu_tax_file_number` trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="f26cd-800">The function  `Func_slovenia_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="f26cd-801">Un mot clé `Keywords_slovenia_eu_tax_file_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="f26cd-801">A keyword from  `Keywords_slovenia_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="f26cd-802">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="f26cd-802">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="f26cd-803">La fonction `Func_slovenia_eu_tax_file_number` trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="f26cd-803">The function  `Func_slovenia_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="f26cd-804">Mots clés</span><span class="sxs-lookup"><span data-stu-id="f26cd-804">Keywords</span></span>

#### <a name="keywords_slovenia_eu_tax_file_number"></a><span data-ttu-id="f26cd-805">Keywords_slovenia_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="f26cd-805">Keywords_slovenia_eu_tax_file_number</span></span>

<span data-ttu-id="f26cd-806">id fiscal</span><span class="sxs-lookup"><span data-stu-id="f26cd-806">tax id</span></span>
  
<span data-ttu-id="f26cd-807">Numéro d’identification de taxe</span><span class="sxs-lookup"><span data-stu-id="f26cd-807">tax id number</span></span>
  
<span data-ttu-id="f26cd-808">ID d’étain</span><span class="sxs-lookup"><span data-stu-id="f26cd-808">tin id</span></span>
  
<span data-ttu-id="f26cd-809">n ° d’étain</span><span class="sxs-lookup"><span data-stu-id="f26cd-809">tin no</span></span>
  
<span data-ttu-id="f26cd-810">ID d’étain slovène</span><span class="sxs-lookup"><span data-stu-id="f26cd-810">slovenian tin id</span></span>
  
<span data-ttu-id="f26cd-811">Etain</span><span class="sxs-lookup"><span data-stu-id="f26cd-811">tin</span></span>
  
<span data-ttu-id="f26cd-812">n ° fichier taxe</span><span class="sxs-lookup"><span data-stu-id="f26cd-812">tax file no</span></span>
  
<span data-ttu-id="f26cd-813">numéro de dossier fiscal</span><span class="sxs-lookup"><span data-stu-id="f26cd-813">tax file number</span></span>
  
<span data-ttu-id="f26cd-814">n ° taxe</span><span class="sxs-lookup"><span data-stu-id="f26cd-814">tax no</span></span>
  
<span data-ttu-id="f26cd-815">Numéro de taxe</span><span class="sxs-lookup"><span data-stu-id="f26cd-815">tax number</span></span>
  
<span data-ttu-id="f26cd-816">taxi #</span><span class="sxs-lookup"><span data-stu-id="f26cd-816">taxid#</span></span>
  
<span data-ttu-id="f26cd-817">taxno #</span><span class="sxs-lookup"><span data-stu-id="f26cd-817">taxno#</span></span>
  
<span data-ttu-id="f26cd-818">identifikacijska številka davka</span><span class="sxs-lookup"><span data-stu-id="f26cd-818">identifikacijska številka davka</span></span>
  
<span data-ttu-id="f26cd-819">davčna številka</span><span class="sxs-lookup"><span data-stu-id="f26cd-819">davčna številka</span></span>
  
<span data-ttu-id="f26cd-820">številka davčne datoteke</span><span class="sxs-lookup"><span data-stu-id="f26cd-820">številka davčne datoteke</span></span>
  
## <a name="spain"></a><span data-ttu-id="f26cd-821">Espagne</span><span class="sxs-lookup"><span data-stu-id="f26cd-821">Spain</span></span>

### <a name="format"></a><span data-ttu-id="f26cd-822">Format</span><span class="sxs-lookup"><span data-stu-id="f26cd-822">Format</span></span>

<span data-ttu-id="f26cd-823">Sept ou huit chiffres et une ou deux lettres dans le modèle spécifié</span><span class="sxs-lookup"><span data-stu-id="f26cd-823">Seven or eight digits and one or two letters in the specified pattern</span></span>
  
### <a name="pattern"></a><span data-ttu-id="f26cd-824">Modèle</span><span class="sxs-lookup"><span data-stu-id="f26cd-824">Pattern</span></span>

<span data-ttu-id="f26cd-825">Personnes physiques espagnoles avec une carte d’identité nationale d’Espagne :</span><span class="sxs-lookup"><span data-stu-id="f26cd-825">Spanish Natural Persons with a Spain National Identity Card:</span></span>
  
-  <span data-ttu-id="f26cd-826">Huit chiffres</span><span class="sxs-lookup"><span data-stu-id="f26cd-826">Eight digits</span></span> 
    
- <span data-ttu-id="f26cd-827">Une lettre majuscule (respecte la casse)</span><span class="sxs-lookup"><span data-stu-id="f26cd-827">One uppercase letter (case-sensitive)</span></span> 
    
<span data-ttu-id="f26cd-828">Spaniards non résident sans carte d’identité nationale d’Espagne</span><span class="sxs-lookup"><span data-stu-id="f26cd-828">Non-resident Spaniards without a Spain National Identity Card</span></span>
  
- <span data-ttu-id="f26cd-829">Une lettre majuscule « L » (respecte la casse)</span><span class="sxs-lookup"><span data-stu-id="f26cd-829">One uppercase letter "L" (case-sensitive)</span></span>
    
- <span data-ttu-id="f26cd-830">Sept chiffres </span><span class="sxs-lookup"><span data-stu-id="f26cd-830">Seven digits</span></span>
    
- <span data-ttu-id="f26cd-831">Une lettre majuscule (respecte la casse)</span><span class="sxs-lookup"><span data-stu-id="f26cd-831">One uppercase letter (case-sensitive)</span></span> 
    
<span data-ttu-id="f26cd-832">Spaniards résident de moins de 14 ans sans carte d’identité nationale (Espagne) :</span><span class="sxs-lookup"><span data-stu-id="f26cd-832">Resident Spaniards under the age of 14 years without a Spain National Identity Card :</span></span>
  
- <span data-ttu-id="f26cd-833">Une lettre majuscule « K » (respecte la casse)</span><span class="sxs-lookup"><span data-stu-id="f26cd-833">One uppercase letter"K" (case-sensitive)</span></span>
    
-  <span data-ttu-id="f26cd-834">Sept chiffres </span><span class="sxs-lookup"><span data-stu-id="f26cd-834">Seven digits</span></span> 
    
- <span data-ttu-id="f26cd-835">Une lettre majuscule (respecte la casse)</span><span class="sxs-lookup"><span data-stu-id="f26cd-835">One uppercase letter (case-sensitive)</span></span>
    
<span data-ttu-id="f26cd-836">Foreigners avec le numéro d’identification d’un étranger</span><span class="sxs-lookup"><span data-stu-id="f26cd-836">Foreigners with a Foreigner's Identification Number</span></span>
  
- <span data-ttu-id="f26cd-837">Une lettre majuscule qui est « X », « Y » ou « Z » (respecte la casse)</span><span class="sxs-lookup"><span data-stu-id="f26cd-837">One uppercase letter that is "X", "Y", or "Z" (case-sensitive)</span></span> 
    
- <span data-ttu-id="f26cd-838">Sept chiffres </span><span class="sxs-lookup"><span data-stu-id="f26cd-838">Seven digits</span></span>
    
- <span data-ttu-id="f26cd-839">Une lettre majuscule (respecte la casse)</span><span class="sxs-lookup"><span data-stu-id="f26cd-839">One uppercase letter (case-sensitive)</span></span> 
    
<span data-ttu-id="f26cd-840">Foreigners sans numéro d’identification étranger</span><span class="sxs-lookup"><span data-stu-id="f26cd-840">Foreigners without a Foreigner's Identification Number</span></span>
  
- <span data-ttu-id="f26cd-841">Une lettre majuscule qui est « M » (respecte la casse)</span><span class="sxs-lookup"><span data-stu-id="f26cd-841">One uppercase letter that is "M" (case-sensitive)</span></span> 
    
- <span data-ttu-id="f26cd-842">Sept chiffres </span><span class="sxs-lookup"><span data-stu-id="f26cd-842">Seven digits</span></span>
    
- <span data-ttu-id="f26cd-843">Une lettre majuscule (respecte la casse)</span><span class="sxs-lookup"><span data-stu-id="f26cd-843">One uppercase letter (case-sensitive)</span></span> 
    
### <a name="checksum"></a><span data-ttu-id="f26cd-844">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="f26cd-844">Checksum</span></span>

<span data-ttu-id="f26cd-845">Oui</span><span class="sxs-lookup"><span data-stu-id="f26cd-845">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="f26cd-846">Définition</span><span class="sxs-lookup"><span data-stu-id="f26cd-846">Definition</span></span>

<span data-ttu-id="f26cd-847">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="f26cd-847">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="f26cd-848">La fonction `Func_spain_eu_tax_file_number` trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="f26cd-848">The function  `Func_spain_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="f26cd-849">Un mot clé `Keywords_spain_eu_tax_file_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="f26cd-849">A keyword from  `Keywords_spain_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="f26cd-850">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="f26cd-850">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="f26cd-851">La fonction `Func_spain_eu_tax_file_number` trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="f26cd-851">The function  `Func_spain_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="f26cd-852">Mots clés</span><span class="sxs-lookup"><span data-stu-id="f26cd-852">Keywords</span></span>

#### <a name="keywords_spain_eu_tax_file_number"></a><span data-ttu-id="f26cd-853">Keywords_spain_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="f26cd-853">Keywords_spain_eu_tax_file_number</span></span>

<span data-ttu-id="f26cd-854">id fiscal</span><span class="sxs-lookup"><span data-stu-id="f26cd-854">tax id</span></span>
  
<span data-ttu-id="f26cd-855">Numéro d’identification de taxe</span><span class="sxs-lookup"><span data-stu-id="f26cd-855">tax id number</span></span>
  
<span data-ttu-id="f26cd-856">identifiant CAF</span><span class="sxs-lookup"><span data-stu-id="f26cd-856">cif id</span></span>
  
<span data-ttu-id="f26cd-857">CAF non</span><span class="sxs-lookup"><span data-stu-id="f26cd-857">cif no</span></span>
  
<span data-ttu-id="f26cd-858">ID CAF espagnol</span><span class="sxs-lookup"><span data-stu-id="f26cd-858">spanish cif id</span></span>
  
<span data-ttu-id="f26cd-859">importation</span><span class="sxs-lookup"><span data-stu-id="f26cd-859">cif</span></span>
  
<span data-ttu-id="f26cd-860">n ° fichier taxe</span><span class="sxs-lookup"><span data-stu-id="f26cd-860">tax file no</span></span>
  
<span data-ttu-id="f26cd-861">numéro CAF espagnol</span><span class="sxs-lookup"><span data-stu-id="f26cd-861">spanish cif number</span></span>
  
<span data-ttu-id="f26cd-862">numéro de dossier fiscal</span><span class="sxs-lookup"><span data-stu-id="f26cd-862">tax file number</span></span>
  
<span data-ttu-id="f26cd-863">espagnol (CAF)</span><span class="sxs-lookup"><span data-stu-id="f26cd-863">spanish cif no</span></span>
  
<span data-ttu-id="f26cd-864">n ° taxe</span><span class="sxs-lookup"><span data-stu-id="f26cd-864">tax no</span></span>
  
<span data-ttu-id="f26cd-865">Numéro de taxe</span><span class="sxs-lookup"><span data-stu-id="f26cd-865">tax number</span></span>
  
<span data-ttu-id="f26cd-866">taxi #</span><span class="sxs-lookup"><span data-stu-id="f26cd-866">taxid#</span></span>
  
<span data-ttu-id="f26cd-867">taxno #</span><span class="sxs-lookup"><span data-stu-id="f26cd-867">taxno#</span></span>
  
<span data-ttu-id="f26cd-868">cifid #</span><span class="sxs-lookup"><span data-stu-id="f26cd-868">cifid#</span></span>
  
<span data-ttu-id="f26cd-869">spanishcifid #</span><span class="sxs-lookup"><span data-stu-id="f26cd-869">spanishcifid#</span></span>
  
<span data-ttu-id="f26cd-870">spanishcifno #</span><span class="sxs-lookup"><span data-stu-id="f26cd-870">spanishcifno#</span></span>
  
<span data-ttu-id="f26cd-871">Número de contribuyente</span><span class="sxs-lookup"><span data-stu-id="f26cd-871">número de contribuyente</span></span>
  
<span data-ttu-id="f26cd-872">Número de Impuesto Corporativo</span><span class="sxs-lookup"><span data-stu-id="f26cd-872">número de impuesto corporativo</span></span>
  
<span data-ttu-id="f26cd-873">Número de Identificación fiscal</span><span class="sxs-lookup"><span data-stu-id="f26cd-873">número de identificación fiscal</span></span>
  
<span data-ttu-id="f26cd-874">CIF número</span><span class="sxs-lookup"><span data-stu-id="f26cd-874">cif número</span></span>
  
<span data-ttu-id="f26cd-875">cifnúmero #</span><span class="sxs-lookup"><span data-stu-id="f26cd-875">cifnúmero#</span></span>
  
## <a name="sweden"></a><span data-ttu-id="f26cd-876">Suède</span><span class="sxs-lookup"><span data-stu-id="f26cd-876">Sweden</span></span>

### <a name="format"></a><span data-ttu-id="f26cd-877">Format</span><span class="sxs-lookup"><span data-stu-id="f26cd-877">Format</span></span>

<span data-ttu-id="f26cd-878">Dix chiffres et un symbole dans le modèle spécifié</span><span class="sxs-lookup"><span data-stu-id="f26cd-878">Ten digits and a symbol in the specified pattern</span></span>
  
### <a name="pattern"></a><span data-ttu-id="f26cd-879">Modèle</span><span class="sxs-lookup"><span data-stu-id="f26cd-879">Pattern</span></span>

<span data-ttu-id="f26cd-880">Dix chiffres et un symbole :</span><span class="sxs-lookup"><span data-stu-id="f26cd-880">Ten digits and a symbol:</span></span>
  
-  <span data-ttu-id="f26cd-881">Six chiffres correspondant à la date de naissance (AAMMJJ)</span><span class="sxs-lookup"><span data-stu-id="f26cd-881">Six digits that correspond to the birth date (YYMMDD)</span></span> 
    
- <span data-ttu-id="f26cd-882">Un signe plus, un signe moins ou une barre oblique inverse</span><span class="sxs-lookup"><span data-stu-id="f26cd-882">A plus sign, minus sign, or backslash</span></span>
    
- <span data-ttu-id="f26cd-883">Trois chiffres qui permettent de définir le numéro d’identification unique :</span><span class="sxs-lookup"><span data-stu-id="f26cd-883">Three digits that make the identification number unique where:</span></span> 
    
  - <span data-ttu-id="f26cd-884">Pour les numéros émis avant le 1990, le septième et le huitième chiffre identifient le comté de naissance ou les personnes nées à l’étranger.</span><span class="sxs-lookup"><span data-stu-id="f26cd-884">For numbers issued before 1990, the seventh and eighth digit identify the county of birth or foreign-born people</span></span>
    
  - <span data-ttu-id="f26cd-885">Le chiffre de la neuvième position indique le sexe soit impair, soit pair pour femme.</span><span class="sxs-lookup"><span data-stu-id="f26cd-885">The digit in the ninth position indicates gender by either odd for male or even for female</span></span>
    
- <span data-ttu-id="f26cd-886">Un chiffre de contrôle</span><span class="sxs-lookup"><span data-stu-id="f26cd-886">One check digit</span></span>
    
### <a name="checksum"></a><span data-ttu-id="f26cd-887">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="f26cd-887">Checksum</span></span>

<span data-ttu-id="f26cd-888">Oui</span><span class="sxs-lookup"><span data-stu-id="f26cd-888">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="f26cd-889">Définition</span><span class="sxs-lookup"><span data-stu-id="f26cd-889">Definition</span></span>

<span data-ttu-id="f26cd-890">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="f26cd-890">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="f26cd-891">La fonction `Func_sweden_eu_tax_file_number` trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="f26cd-891">The function  `Func_sweden_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="f26cd-892">Un mot clé `Keywords_sweden_eu_tax_file_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="f26cd-892">A keyword from  `Keywords_sweden_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="f26cd-893">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="f26cd-893">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="f26cd-894">La fonction `Func_sweden_eu_tax_file_number` trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="f26cd-894">The function  `Func_sweden_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="f26cd-895">Mots clés</span><span class="sxs-lookup"><span data-stu-id="f26cd-895">Keywords</span></span>

#### <a name="keywords_sweden_eu_tax_file_number"></a><span data-ttu-id="f26cd-896">Keywords_sweden_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="f26cd-896">Keywords_sweden_eu_tax_file_number</span></span>

<span data-ttu-id="f26cd-897">id fiscal</span><span class="sxs-lookup"><span data-stu-id="f26cd-897">tax id</span></span>
  
<span data-ttu-id="f26cd-898">n ° ID taxe</span><span class="sxs-lookup"><span data-stu-id="f26cd-898">tax id no.</span></span>
  
<span data-ttu-id="f26cd-899">Numéro d’identification de taxe</span><span class="sxs-lookup"><span data-stu-id="f26cd-899">tax id number</span></span>
  
<span data-ttu-id="f26cd-900">identification fiscale</span><span class="sxs-lookup"><span data-stu-id="f26cd-900">tax identification</span></span>
  
<span data-ttu-id="f26cd-901">identification fiscale #</span><span class="sxs-lookup"><span data-stu-id="f26cd-901">tax identification#</span></span>
  
<span data-ttu-id="f26cd-902">n ° taxe</span><span class="sxs-lookup"><span data-stu-id="f26cd-902">tax no.</span></span>
  
<span data-ttu-id="f26cd-903">codes #</span><span class="sxs-lookup"><span data-stu-id="f26cd-903">tax#</span></span>
  
<span data-ttu-id="f26cd-904">taxi #</span><span class="sxs-lookup"><span data-stu-id="f26cd-904">taxid#</span></span>
  
<span data-ttu-id="f26cd-905">fichier taxe</span><span class="sxs-lookup"><span data-stu-id="f26cd-905">tax file</span></span>
  
<span data-ttu-id="f26cd-906">n ° fichier taxe</span><span class="sxs-lookup"><span data-stu-id="f26cd-906">tax file no.</span></span>
  
<span data-ttu-id="f26cd-907">Numéro d’identification personnel</span><span class="sxs-lookup"><span data-stu-id="f26cd-907">personal id number</span></span>
  
<span data-ttu-id="f26cd-908">skatt ID Nummer</span><span class="sxs-lookup"><span data-stu-id="f26cd-908">skatt id nummer</span></span>
  
<span data-ttu-id="f26cd-909">skatt identifikation</span><span class="sxs-lookup"><span data-stu-id="f26cd-909">skatt identifikation</span></span>
  
<span data-ttu-id="f26cd-910">personnummer</span><span class="sxs-lookup"><span data-stu-id="f26cd-910">personnummer</span></span>
  
## <a name="uk"></a><span data-ttu-id="f26cd-911">R.U.</span><span class="sxs-lookup"><span data-stu-id="f26cd-911">UK</span></span>

### <a name="format"></a><span data-ttu-id="f26cd-912">Format</span><span class="sxs-lookup"><span data-stu-id="f26cd-912">Format</span></span>

<span data-ttu-id="f26cd-913">Référence de contribuable unique (UTR) : 10 chiffres sans espaces ni délimiteurs</span><span class="sxs-lookup"><span data-stu-id="f26cd-913">Unique Taxpayer Reference (UTR): 10 digits without spaces and delimiters</span></span>
  
<span data-ttu-id="f26cd-914">Numéro d’assurance nationale (NINO) : pour plus d’informations, reportez-vous à la section «Royaume-Uni</span><span class="sxs-lookup"><span data-stu-id="f26cd-914">National Insurance Number (NINO): For details, see the section "U.K.</span></span> <span data-ttu-id="f26cd-915">National Insurance Number (NINO)» dans [ce que recherche les types d’informations sensibles](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="f26cd-915">National Insurance Number (NINO)" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
### <a name="pattern"></a><span data-ttu-id="f26cd-916">Modèle</span><span class="sxs-lookup"><span data-stu-id="f26cd-916">Pattern</span></span>

<span data-ttu-id="f26cd-917">Référence de contribuable unique (UTR) : 10 chiffres</span><span class="sxs-lookup"><span data-stu-id="f26cd-917">Unique Taxpayer Reference (UTR): 10 digits</span></span>
  
<span data-ttu-id="f26cd-918">Numéro d’assurance nationale (NINO) : pour plus d’informations, reportez-vous à la section «Royaume-Uni</span><span class="sxs-lookup"><span data-stu-id="f26cd-918">National Insurance Number (NINO): For details, see the section "U.K.</span></span> <span data-ttu-id="f26cd-919">National Insurance Number (NINO)» dans [ce que recherche les types d’informations sensibles](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="f26cd-919">National Insurance Number (NINO)" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
### <a name="checksum"></a><span data-ttu-id="f26cd-920">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="f26cd-920">Checksum</span></span>

<span data-ttu-id="f26cd-921">Oui</span><span class="sxs-lookup"><span data-stu-id="f26cd-921">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="f26cd-922">Définition</span><span class="sxs-lookup"><span data-stu-id="f26cd-922">Definition</span></span>

<span data-ttu-id="f26cd-923">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="f26cd-923">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="f26cd-924">La fonction `Func_uk_eu_tax_file_number` trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="f26cd-924">The function  `Func_uk_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="f26cd-925">Un mot clé `Keywords_uk_eu_tax_file_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="f26cd-925">A keyword from  `Keywords_uk_eu_tax_file_number` is found.</span></span> 
    
```
 <!-- EU Tax File Number -->
<Entity id="e09c07d3-66e5-4783-989d-49ac62748f5f" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Func_uk_eu_tax_file_number" />
          <Match idRef="Keywords_uk_eu_tax_file_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="f26cd-926">Mots clés</span><span class="sxs-lookup"><span data-stu-id="f26cd-926">Keywords</span></span>

#### <a name="keywords_uk_eu_tax_file_number"></a><span data-ttu-id="f26cd-927">Keywords_uk_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="f26cd-927">Keywords_uk_eu_tax_file_number</span></span>

<span data-ttu-id="f26cd-928">id fiscal</span><span class="sxs-lookup"><span data-stu-id="f26cd-928">tax id</span></span>
  
<span data-ttu-id="f26cd-929">n ° ID taxe</span><span class="sxs-lookup"><span data-stu-id="f26cd-929">tax id no.</span></span>
  
<span data-ttu-id="f26cd-930">Numéro d’identification de taxe</span><span class="sxs-lookup"><span data-stu-id="f26cd-930">tax id number</span></span>
  
<span data-ttu-id="f26cd-931">identification fiscale</span><span class="sxs-lookup"><span data-stu-id="f26cd-931">tax identification</span></span>
  
<span data-ttu-id="f26cd-932">identification fiscale #</span><span class="sxs-lookup"><span data-stu-id="f26cd-932">tax identification#</span></span>
  
<span data-ttu-id="f26cd-933">n ° taxe</span><span class="sxs-lookup"><span data-stu-id="f26cd-933">tax no.</span></span>
  
<span data-ttu-id="f26cd-934">codes #</span><span class="sxs-lookup"><span data-stu-id="f26cd-934">tax#</span></span>
  
<span data-ttu-id="f26cd-935">taxi #</span><span class="sxs-lookup"><span data-stu-id="f26cd-935">taxid#</span></span>
  
<span data-ttu-id="f26cd-936">fichier taxe</span><span class="sxs-lookup"><span data-stu-id="f26cd-936">tax file</span></span>
  
<span data-ttu-id="f26cd-937">n ° fichier taxe</span><span class="sxs-lookup"><span data-stu-id="f26cd-937">tax file no.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="f26cd-938">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f26cd-938">See also</span></span>

[<span data-ttu-id="f26cd-939">Éléments recherchés par les types d’informations sensibles</span><span class="sxs-lookup"><span data-stu-id="f26cd-939">What the sensitive information types look for</span></span>](what-the-sensitive-information-types-look-for.md)

