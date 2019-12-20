---
title: Numéro de sécurité sociale de l’UE ou ID équivalent
ms.author: cabailey
author: cabailey
manager: laurawi
ms.date: 8/17/2018
audience: Admin
ms.topic: reference
ms.service: O365-seccomp
ms.collection: M365-security-compliance
localization_priority: Normal
description: Cette rubrique indique ce qu’est une stratégie de protection contre la perte de données (DLP) lorsqu’elle détecte le type d’informations sensibles de l’UE ou d’un ID équivalent. Ce type d’informations sensibles définit différents modèles, Mots clés et autres preuves pour chaque pays.
ms.openlocfilehash: 0666818dc892070f5c2f0c34abd8ca33d1253e33
ms.sourcegitcommit: 0ad0092d9c5cb2d69fc70c990a9b7cc03140611b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/19/2019
ms.locfileid: "40805927"
---
# <a name="eu-social-security-number-or-equivalent-id"></a><span data-ttu-id="8c402-104">Numéro de sécurité sociale de l’UE ou ID équivalent</span><span class="sxs-lookup"><span data-stu-id="8c402-104">EU Social Security Number or Equivalent ID</span></span>

<span data-ttu-id="8c402-105">Cette rubrique présente ce qu’une stratégie de protection contre la perte de données (DLP) recherche lorsqu’elle détecte le type d’informations sensibles de l’UE ou un ID équivalent.</span><span class="sxs-lookup"><span data-stu-id="8c402-105">This topic shows what a data loss prevention (DLP) policy looks for when it detects the EU Social Security Number (SSN) or Equivalent ID sensitive information type.</span></span> <span data-ttu-id="8c402-106">Ce type d’informations sensibles définit différents modèles, Mots clés et autres preuves pour chaque pays.</span><span class="sxs-lookup"><span data-stu-id="8c402-106">This sensitive information type defines different patterns, keywords, and other evidence for each country.</span></span>
  
## <a name="austria"></a><span data-ttu-id="8c402-107">Autriche</span><span class="sxs-lookup"><span data-stu-id="8c402-107">Austria</span></span>

### <a name="format"></a><span data-ttu-id="8c402-108">Format</span><span class="sxs-lookup"><span data-stu-id="8c402-108">Format</span></span>

<span data-ttu-id="8c402-109">10 chiffres au format spécifié</span><span class="sxs-lookup"><span data-stu-id="8c402-109">10 digits in the specified format</span></span>
  
### <a name="pattern"></a><span data-ttu-id="8c402-110">Modèle</span><span class="sxs-lookup"><span data-stu-id="8c402-110">Pattern</span></span>

<span data-ttu-id="8c402-111">10 chiffres :</span><span class="sxs-lookup"><span data-stu-id="8c402-111">10 digits:</span></span>
  
-  <span data-ttu-id="8c402-112">Trois chiffres correspondant à un numéro de série</span><span class="sxs-lookup"><span data-stu-id="8c402-112">Three digits that correspond to a serial number</span></span> 
    
- <span data-ttu-id="8c402-113">Un chiffre de contrôle</span><span class="sxs-lookup"><span data-stu-id="8c402-113">One check digit</span></span>
    
- <span data-ttu-id="8c402-114">Six chiffres correspondant à la date de naissance (JJMMAA)</span><span class="sxs-lookup"><span data-stu-id="8c402-114">Six digits that correspond to the birth date (DDMMYY)</span></span>
    
### <a name="checksum"></a><span data-ttu-id="8c402-115">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="8c402-115">Checksum</span></span>

<span data-ttu-id="8c402-116">Oui</span><span class="sxs-lookup"><span data-stu-id="8c402-116">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="8c402-117">Définition</span><span class="sxs-lookup"><span data-stu-id="8c402-117">Definition</span></span>

<span data-ttu-id="8c402-118">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="8c402-118">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="8c402-119">La fonction `Func_austria_eu_ssn_or_equivalent` trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="8c402-119">The function  `Func_austria_eu_ssn_or_equivalent` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="8c402-120">Un mot clé `Keywords_austria_eu_ssn_or_equivalent` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="8c402-120">A keyword from  `Keywords_austria_eu_ssn_or_equivalent` is found.</span></span> 
    
<span data-ttu-id="8c402-121">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="8c402-121">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="8c402-122">La fonction `Func_austria_eu_ssn_or_equivalent` trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="8c402-122">The function  `Func_austria_eu_ssn_or_equivalent` finds content that matches the pattern.</span></span> 
    
```
 <!-- EU SSN or Equivalent Number -->
<Entity id="d24e32a4-c0bb-4ba8-899d-6303b95742d9" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_austria_eu_ssn_or_equivalent" />
          <Match idRef="Keywords_austria_eu_ssn_or_equivalent" />
        </Pattern>
<Pattern confidenceLevel="75">
            <IdMatch idRef="Func_austria_eu_ssn_or_equivalent" />
          </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="8c402-123">Mots clés</span><span class="sxs-lookup"><span data-stu-id="8c402-123">Keywords</span></span>

#### <a name="keywords_austria_eu_ssn_or_equivalent"></a><span data-ttu-id="8c402-124">Keywords_austria_eu_ssn_or_equivalent</span><span class="sxs-lookup"><span data-stu-id="8c402-124">Keywords_austria_eu_ssn_or_equivalent</span></span>

<span data-ttu-id="8c402-125">Numéro de sécurité sociale</span><span class="sxs-lookup"><span data-stu-id="8c402-125">social security no</span></span>
  
<span data-ttu-id="8c402-126">numéro de sécurité sociale</span><span class="sxs-lookup"><span data-stu-id="8c402-126">social security number</span></span>
  
<span data-ttu-id="8c402-127">code de sécurité sociale</span><span class="sxs-lookup"><span data-stu-id="8c402-127">social security code</span></span>
  
<span data-ttu-id="8c402-128">Numéro d’assurance</span><span class="sxs-lookup"><span data-stu-id="8c402-128">insurance number</span></span>
  
<span data-ttu-id="8c402-129">Numéro de sécurité sociale autrichien</span><span class="sxs-lookup"><span data-stu-id="8c402-129">austrian ssn</span></span>
  
<span data-ttu-id="8c402-130">SSN #</span><span class="sxs-lookup"><span data-stu-id="8c402-130">ssn#</span></span>
  
<span data-ttu-id="8c402-131">SSN</span><span class="sxs-lookup"><span data-stu-id="8c402-131">ssn</span></span>
  
<span data-ttu-id="8c402-132">code d’assurance</span><span class="sxs-lookup"><span data-stu-id="8c402-132">insurance code</span></span>
  
<span data-ttu-id="8c402-133">code d’assurance #</span><span class="sxs-lookup"><span data-stu-id="8c402-133">insurance code#</span></span>
  
<span data-ttu-id="8c402-134">socialsecurityno #</span><span class="sxs-lookup"><span data-stu-id="8c402-134">socialsecurityno#</span></span>
  
<span data-ttu-id="8c402-135">sozialversicherungsnummer</span><span class="sxs-lookup"><span data-stu-id="8c402-135">sozialversicherungsnummer</span></span>
  
<span data-ttu-id="8c402-136">soziale sicherheit kein</span><span class="sxs-lookup"><span data-stu-id="8c402-136">soziale sicherheit kein</span></span>
  
<span data-ttu-id="8c402-137">versicherungsnummer</span><span class="sxs-lookup"><span data-stu-id="8c402-137">versicherungsnummer</span></span>
  
## <a name="belgium"></a><span data-ttu-id="8c402-138">Belgique</span><span class="sxs-lookup"><span data-stu-id="8c402-138">Belgium</span></span>

### <a name="format"></a><span data-ttu-id="8c402-139">Format</span><span class="sxs-lookup"><span data-stu-id="8c402-139">Format</span></span>

<span data-ttu-id="8c402-140">11 chiffres sans espaces ni délimiteurs</span><span class="sxs-lookup"><span data-stu-id="8c402-140">11 digits without spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="8c402-141">Modèle</span><span class="sxs-lookup"><span data-stu-id="8c402-141">Pattern</span></span>

<span data-ttu-id="8c402-142">11 chiffres</span><span class="sxs-lookup"><span data-stu-id="8c402-142">11 digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="8c402-143">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="8c402-143">Checksum</span></span>

<span data-ttu-id="8c402-144">Oui</span><span class="sxs-lookup"><span data-stu-id="8c402-144">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="8c402-145">Définition</span><span class="sxs-lookup"><span data-stu-id="8c402-145">Definition</span></span>

<span data-ttu-id="8c402-146">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="8c402-146">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="8c402-147">La fonction `Func_belgium_eu_ssn_or_equivalent` trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="8c402-147">The function  `Func_belgium_eu_ssn_or_equivalent` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="8c402-148">Un mot clé `Keywords_belgium_eu_ssn_or_equivalent` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="8c402-148">A keyword from  `Keywords_belgium_eu_ssn_or_equivalent` is found.</span></span> 
    
<span data-ttu-id="8c402-149">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="8c402-149">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="8c402-150">La fonction `Func_belgium_eu_ssn_or_equivalent` trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="8c402-150">The function  `Func_belgium_eu_ssn_or_equivalent` finds content that matches the pattern.</span></span> 
    
```
 <!-- EU SSN or Equivalent Number -->
<Entity id="d24e32a4-c0bb-4ba8-899d-6303b95742d9" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_belgium_eu_ssn_or_equivalent" />
          <Match idRef="Keywords_belgium_eu_ssn_or_equivalent" />
        </Pattern> 
       <Pattern confidenceLevel="75">
          <IdMatch idRef="Func_belgium_eu_ssn_or_equivalent" />
        </Pattern>      
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="8c402-151">Mots clés</span><span class="sxs-lookup"><span data-stu-id="8c402-151">Keywords</span></span>

#### <a name="keywords_belgium_eu_ssn_or_equivalent"></a><span data-ttu-id="8c402-152">Keywords_belgium_eu_ssn_or_equivalent</span><span class="sxs-lookup"><span data-stu-id="8c402-152">Keywords_belgium_eu_ssn_or_equivalent</span></span>

<span data-ttu-id="8c402-153">numéro national belge</span><span class="sxs-lookup"><span data-stu-id="8c402-153">belgian national number</span></span>
  
<span data-ttu-id="8c402-154">numéro national</span><span class="sxs-lookup"><span data-stu-id="8c402-154">national number</span></span>
  
<span data-ttu-id="8c402-155">numéro de sécurité sociale</span><span class="sxs-lookup"><span data-stu-id="8c402-155">social security number</span></span>
  
<span data-ttu-id="8c402-156">nationalnumber #</span><span class="sxs-lookup"><span data-stu-id="8c402-156">nationalnumber#</span></span>
  
<span data-ttu-id="8c402-157">SSN #</span><span class="sxs-lookup"><span data-stu-id="8c402-157">ssn#</span></span>
  
<span data-ttu-id="8c402-158">SSN</span><span class="sxs-lookup"><span data-stu-id="8c402-158">ssn</span></span>
  
<span data-ttu-id="8c402-159">nationalnumber</span><span class="sxs-lookup"><span data-stu-id="8c402-159">nationalnumber</span></span>
  
<span data-ttu-id="8c402-160">bnn #</span><span class="sxs-lookup"><span data-stu-id="8c402-160">bnn#</span></span>
  
<span data-ttu-id="8c402-161">bnn</span><span class="sxs-lookup"><span data-stu-id="8c402-161">bnn</span></span>
  
<span data-ttu-id="8c402-162">Numéro d’identification personnel</span><span class="sxs-lookup"><span data-stu-id="8c402-162">personal id number</span></span>
  
<span data-ttu-id="8c402-163">personalidnumber #</span><span class="sxs-lookup"><span data-stu-id="8c402-163">personalidnumber#</span></span>
  
<span data-ttu-id="8c402-164">numéro national</span><span class="sxs-lookup"><span data-stu-id="8c402-164">numéro national</span></span>
  
<span data-ttu-id="8c402-165">numéro de sécurité</span><span class="sxs-lookup"><span data-stu-id="8c402-165">numéro de sécurité</span></span>
  
<span data-ttu-id="8c402-166">numéro d’assuré</span><span class="sxs-lookup"><span data-stu-id="8c402-166">numéro d'assuré</span></span>
  
<span data-ttu-id="8c402-167">identifiant national</span><span class="sxs-lookup"><span data-stu-id="8c402-167">identifiant national</span></span>
  
<span data-ttu-id="8c402-168">identifiantnational #</span><span class="sxs-lookup"><span data-stu-id="8c402-168">identifiantnational#</span></span>
  
<span data-ttu-id="8c402-169">numéronational #</span><span class="sxs-lookup"><span data-stu-id="8c402-169">numéronational#</span></span>
  
## <a name="croatia"></a><span data-ttu-id="8c402-170">Croatie</span><span class="sxs-lookup"><span data-stu-id="8c402-170">Croatia</span></span>

### <a name="format"></a><span data-ttu-id="8c402-171">Format</span><span class="sxs-lookup"><span data-stu-id="8c402-171">Format</span></span>

<span data-ttu-id="8c402-172">11 chiffres sans espaces ni délimiteurs</span><span class="sxs-lookup"><span data-stu-id="8c402-172">11 digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="8c402-173">Modèle</span><span class="sxs-lookup"><span data-stu-id="8c402-173">Pattern</span></span>

 <span data-ttu-id="8c402-174">11 chiffres :</span><span class="sxs-lookup"><span data-stu-id="8c402-174">11 digits:</span></span> 
  
-  <span data-ttu-id="8c402-175">Dix chiffres</span><span class="sxs-lookup"><span data-stu-id="8c402-175">Ten digits</span></span> 
    
- <span data-ttu-id="8c402-176">Un chiffre de contrôle</span><span class="sxs-lookup"><span data-stu-id="8c402-176">One check digit</span></span>
    
### <a name="checksum"></a><span data-ttu-id="8c402-177">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="8c402-177">Checksum</span></span>

<span data-ttu-id="8c402-178">Oui</span><span class="sxs-lookup"><span data-stu-id="8c402-178">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="8c402-179">Définition</span><span class="sxs-lookup"><span data-stu-id="8c402-179">Definition</span></span>

<span data-ttu-id="8c402-180">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="8c402-180">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="8c402-181">La fonction `Func_croatia_eu_ssn_or_equivalent` trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="8c402-181">The function  `Func_croatia_eu_ssn_or_equivalent` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="8c402-182">Un mot clé `Keywords_croatia_eu_ssn_or_equivalent` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="8c402-182">A keyword from  `Keywords_croatia_eu_ssn_or_equivalent` is found.</span></span> 
    
<span data-ttu-id="8c402-183">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="8c402-183">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="8c402-184">La fonction `Func_croatia_eu_ssn_or_equivalent` trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="8c402-184">The function  `Func_croatia_eu_ssn_or_equivalent` finds content that matches the pattern.</span></span> 
    
```
 <!-- EU SSN or Equivalent Number -->
<Entity id="d24e32a4-c0bb-4ba8-899d-6303b95742d9" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_croatia_eu_ssn_or_equivalent" />
          <Match idRef="Keywords_croatia_eu_ssn_or_equivalent" />
        </Pattern> 
       <Pattern confidenceLevel="75">
          <IdMatch idRef="Func_croatia_eu_ssn_or_equivalent" />
        </Pattern>      
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="8c402-185">Mots clés</span><span class="sxs-lookup"><span data-stu-id="8c402-185">Keywords</span></span>

#### <a name="keywords_croatia_eu_ssn_or_equivalent"></a><span data-ttu-id="8c402-186">Keywords_croatia_eu_ssn_or_equivalent</span><span class="sxs-lookup"><span data-stu-id="8c402-186">Keywords_croatia_eu_ssn_or_equivalent</span></span>

<span data-ttu-id="8c402-187">Numéro d’identification personnel</span><span class="sxs-lookup"><span data-stu-id="8c402-187">personal identification number</span></span>
  
<span data-ttu-id="8c402-188">Numéro de citoyen principal</span><span class="sxs-lookup"><span data-stu-id="8c402-188">master citizen number</span></span>
  
<span data-ttu-id="8c402-189">numéro d’identification nationale</span><span class="sxs-lookup"><span data-stu-id="8c402-189">national identification number</span></span>
  
<span data-ttu-id="8c402-190">numéro de sécurité sociale</span><span class="sxs-lookup"><span data-stu-id="8c402-190">social security number</span></span>
  
<span data-ttu-id="8c402-191">nationalnumber #</span><span class="sxs-lookup"><span data-stu-id="8c402-191">nationalnumber#</span></span>
  
<span data-ttu-id="8c402-192">SSN #</span><span class="sxs-lookup"><span data-stu-id="8c402-192">ssn#</span></span>
  
<span data-ttu-id="8c402-193">SSN</span><span class="sxs-lookup"><span data-stu-id="8c402-193">ssn</span></span>
  
<span data-ttu-id="8c402-194">nationalnumber</span><span class="sxs-lookup"><span data-stu-id="8c402-194">nationalnumber</span></span>
  
<span data-ttu-id="8c402-195">bnn #</span><span class="sxs-lookup"><span data-stu-id="8c402-195">bnn#</span></span>
  
<span data-ttu-id="8c402-196">bnn</span><span class="sxs-lookup"><span data-stu-id="8c402-196">bnn</span></span>
  
<span data-ttu-id="8c402-197">Numéro d’identification personnel</span><span class="sxs-lookup"><span data-stu-id="8c402-197">personal id number</span></span>
  
<span data-ttu-id="8c402-198">personalidnumber #</span><span class="sxs-lookup"><span data-stu-id="8c402-198">personalidnumber#</span></span>
  
<span data-ttu-id="8c402-199">OIB</span><span class="sxs-lookup"><span data-stu-id="8c402-199">oib</span></span>
  
<span data-ttu-id="8c402-200">osobni identifikacijski broj</span><span class="sxs-lookup"><span data-stu-id="8c402-200">osobni identifikacijski broj</span></span>
  
## <a name="czech-republic"></a><span data-ttu-id="8c402-201">République tchèque</span><span class="sxs-lookup"><span data-stu-id="8c402-201">Czech Republic</span></span>

### <a name="format"></a><span data-ttu-id="8c402-202">Format</span><span class="sxs-lookup"><span data-stu-id="8c402-202">Format</span></span>

<span data-ttu-id="8c402-203">10 chiffres et une barre oblique inverse dans le modèle spécifié</span><span class="sxs-lookup"><span data-stu-id="8c402-203">Ten digits and a backslash in the specified pattern</span></span>
  
### <a name="pattern"></a><span data-ttu-id="8c402-204">Modèle</span><span class="sxs-lookup"><span data-stu-id="8c402-204">Pattern</span></span>

<span data-ttu-id="8c402-205">Dix chiffres et une barre oblique inverse :</span><span class="sxs-lookup"><span data-stu-id="8c402-205">Ten digits and a backslash:</span></span>
  
- <span data-ttu-id="8c402-206">Six chiffres correspondant à la date de naissance (AAMMJJ) :</span><span class="sxs-lookup"><span data-stu-id="8c402-206">Six digits that correspond to the birth date (YYMMDD):</span></span> 
    
- <span data-ttu-id="8c402-207">Une barre oblique inverse</span><span class="sxs-lookup"><span data-stu-id="8c402-207">A backslash</span></span>
    
- <span data-ttu-id="8c402-208">Trois chiffres correspondant à un numéro de série qui sépare les personnes nés à la même date</span><span class="sxs-lookup"><span data-stu-id="8c402-208">Three digits that correspond to a serial number that separates persons born on the same date</span></span>
    
- <span data-ttu-id="8c402-209">Un chiffre de contrôle</span><span class="sxs-lookup"><span data-stu-id="8c402-209">One check digit</span></span>
    
### <a name="checksum"></a><span data-ttu-id="8c402-210">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="8c402-210">Checksum</span></span>

<span data-ttu-id="8c402-211">Oui</span><span class="sxs-lookup"><span data-stu-id="8c402-211">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="8c402-212">Définition</span><span class="sxs-lookup"><span data-stu-id="8c402-212">Definition</span></span>

<span data-ttu-id="8c402-213">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="8c402-213">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="8c402-214">La fonction `Func_czech_republic_eu_ssn_or_equivalent` trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="8c402-214">The function  `Func_czech_republic_eu_ssn_or_equivalent` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="8c402-215">Un mot clé `Keywords_czech_republic_eu_ssn_or_equivalent` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="8c402-215">A keyword from  `Keywords_czech_republic_eu_ssn_or_equivalent` is found.</span></span> 
    
<span data-ttu-id="8c402-216">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="8c402-216">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="8c402-217">La fonction `Func_czech_republic_eu_ssn_or_equivalent` trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="8c402-217">The function  `Func_czech_republic_eu_ssn_or_equivalent` finds content that matches the pattern.</span></span> 
    
```
 <!-- EU SSN or Equivalent Number -->
<Entity id="d24e32a4-c0bb-4ba8-899d-6303b95742d9" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_czech_republic_eu_ssn_or_equivalent" />
          <Match idRef="Keywords_czech_republic_eu_ssn_or_equivalent" />
        </Pattern> 
       <Pattern confidenceLevel="75">
          <IdMatch idRef="Func_czech_republic_eu_ssn_or_equivalent" />
        </Pattern>      
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="8c402-218">Mots clés</span><span class="sxs-lookup"><span data-stu-id="8c402-218">Keywords</span></span>

#### <a name="keywords_czech_republic_eu_ssn_or_equivalent"></a><span data-ttu-id="8c402-219">Keywords_czech_republic_eu_ssn_or_equivalent</span><span class="sxs-lookup"><span data-stu-id="8c402-219">Keywords_czech_republic_eu_ssn_or_equivalent</span></span>

<span data-ttu-id="8c402-220">Numéro de naissance</span><span class="sxs-lookup"><span data-stu-id="8c402-220">birth number</span></span>
  
<span data-ttu-id="8c402-221">numéro d’identification nationale</span><span class="sxs-lookup"><span data-stu-id="8c402-221">national identification number</span></span>
  
<span data-ttu-id="8c402-222">Numéro d’identification personnel</span><span class="sxs-lookup"><span data-stu-id="8c402-222">personal identification number</span></span>
  
<span data-ttu-id="8c402-223">numéro de sécurité sociale</span><span class="sxs-lookup"><span data-stu-id="8c402-223">social security number</span></span>
  
<span data-ttu-id="8c402-224">nationalnumber #</span><span class="sxs-lookup"><span data-stu-id="8c402-224">nationalnumber#</span></span>
  
<span data-ttu-id="8c402-225">SSN #</span><span class="sxs-lookup"><span data-stu-id="8c402-225">ssn#</span></span>
  
<span data-ttu-id="8c402-226">SSN</span><span class="sxs-lookup"><span data-stu-id="8c402-226">ssn</span></span>
  
<span data-ttu-id="8c402-227">numéro national</span><span class="sxs-lookup"><span data-stu-id="8c402-227">national number</span></span>
  
<span data-ttu-id="8c402-228">Numéro d’identification personnel</span><span class="sxs-lookup"><span data-stu-id="8c402-228">personal id number</span></span>
  
<span data-ttu-id="8c402-229">personalidnumber #</span><span class="sxs-lookup"><span data-stu-id="8c402-229">personalidnumber#</span></span>
  
<span data-ttu-id="8c402-230">rč</span><span class="sxs-lookup"><span data-stu-id="8c402-230">rč</span></span>
  
<span data-ttu-id="8c402-231">rodné číslo</span><span class="sxs-lookup"><span data-stu-id="8c402-231">rodné číslo</span></span>
  
<span data-ttu-id="8c402-232">rodne cislo</span><span class="sxs-lookup"><span data-stu-id="8c402-232">rodne cislo</span></span>
  
## <a name="denmark"></a><span data-ttu-id="8c402-233">Danemark</span><span class="sxs-lookup"><span data-stu-id="8c402-233">Denmark</span></span>

### <a name="format"></a><span data-ttu-id="8c402-234">Format</span><span class="sxs-lookup"><span data-stu-id="8c402-234">Format</span></span>

<span data-ttu-id="8c402-235">10 chiffres et un trait d’Union dans le modèle spécifié</span><span class="sxs-lookup"><span data-stu-id="8c402-235">Ten digits and a hyphen in the specified pattern</span></span>
  
### <a name="pattern"></a><span data-ttu-id="8c402-236">Modèle</span><span class="sxs-lookup"><span data-stu-id="8c402-236">Pattern</span></span>

<span data-ttu-id="8c402-237">Dix chiffres et un trait d’Union :</span><span class="sxs-lookup"><span data-stu-id="8c402-237">Ten digits and a hyphen:</span></span>
  
- <span data-ttu-id="8c402-238">Six chiffres correspondant à la date de naissance (JJMMAA)</span><span class="sxs-lookup"><span data-stu-id="8c402-238">Six digits that correspond to the birth date (DDMMYY)</span></span> 
    
- <span data-ttu-id="8c402-239">Un trait d’union </span><span class="sxs-lookup"><span data-stu-id="8c402-239">A hyphen</span></span>
    
- <span data-ttu-id="8c402-240">Quatre chiffres correspondant à un numéro de séquence</span><span class="sxs-lookup"><span data-stu-id="8c402-240">Four digits that correspond to a sequence number</span></span>
    
### <a name="checksum"></a><span data-ttu-id="8c402-241">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="8c402-241">Checksum</span></span>

<span data-ttu-id="8c402-242">Oui</span><span class="sxs-lookup"><span data-stu-id="8c402-242">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="8c402-243">Définition</span><span class="sxs-lookup"><span data-stu-id="8c402-243">Definition</span></span>

<span data-ttu-id="8c402-244">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="8c402-244">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="8c402-245">La fonction `Func_denmark_eu_ssn_or_equivalent` trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="8c402-245">The function  `Func_denmark_eu_ssn_or_equivalent` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="8c402-246">Un mot clé `Keywords_denmark_eu_ssn_or_equivalent` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="8c402-246">A keyword from  `Keywords_denmark_eu_ssn_or_equivalent` is found.</span></span> 
    
<span data-ttu-id="8c402-247">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="8c402-247">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="8c402-248">La fonction `Func_denmark_eu_ssn_or_equivalent` trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="8c402-248">The function  `Func_denmark_eu_ssn_or_equivalent` finds content that matches the pattern.</span></span> 
    
```
 <!-- EU SSN or Equivalent Number -->
<Entity id="d24e32a4-c0bb-4ba8-899d-6303b95742d9" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_denmark_eu_ssn_or_equivalent" />
          <Match idRef="Keywords_denmark_eu_ssn_or_equivalent" />
        </Pattern> 
       <Pattern confidenceLevel="75">
          <IdMatch idRef="Func_denmark_eu_ssn_or_equivalent" />
        </Pattern>      
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="8c402-249">Mots clés</span><span class="sxs-lookup"><span data-stu-id="8c402-249">Keywords</span></span>

#### <a name="keywords_denmark_eu_ssn_or_equivalent"></a><span data-ttu-id="8c402-250">Keywords_denmark_eu_ssn_or_equivalent</span><span class="sxs-lookup"><span data-stu-id="8c402-250">Keywords_denmark_eu_ssn_or_equivalent</span></span>

<span data-ttu-id="8c402-251">Numéro d’identification personnel</span><span class="sxs-lookup"><span data-stu-id="8c402-251">personal identification number</span></span>
  
<span data-ttu-id="8c402-252">numéro d’identification nationale</span><span class="sxs-lookup"><span data-stu-id="8c402-252">national identification number</span></span>
  
<span data-ttu-id="8c402-253">numéro de sécurité sociale</span><span class="sxs-lookup"><span data-stu-id="8c402-253">social security number</span></span>
  
<span data-ttu-id="8c402-254">nationalnumber #</span><span class="sxs-lookup"><span data-stu-id="8c402-254">nationalnumber#</span></span>
  
<span data-ttu-id="8c402-255">SSN #</span><span class="sxs-lookup"><span data-stu-id="8c402-255">ssn#</span></span>
  
<span data-ttu-id="8c402-256">SSN</span><span class="sxs-lookup"><span data-stu-id="8c402-256">ssn</span></span>
  
<span data-ttu-id="8c402-257">numéro national</span><span class="sxs-lookup"><span data-stu-id="8c402-257">national number</span></span>
  
<span data-ttu-id="8c402-258">Numéro d’identification personnel</span><span class="sxs-lookup"><span data-stu-id="8c402-258">personal id number</span></span>
  
<span data-ttu-id="8c402-259">personalidnumber #</span><span class="sxs-lookup"><span data-stu-id="8c402-259">personalidnumber#</span></span>
  
<span data-ttu-id="8c402-260">CPR-nummer</span><span class="sxs-lookup"><span data-stu-id="8c402-260">cpr-nummer</span></span>
  
<span data-ttu-id="8c402-261">personnummer</span><span class="sxs-lookup"><span data-stu-id="8c402-261">personnummer</span></span>
  
## <a name="finland"></a><span data-ttu-id="8c402-262">Finlande</span><span class="sxs-lookup"><span data-stu-id="8c402-262">Finland</span></span>

### <a name="format"></a><span data-ttu-id="8c402-263">Format</span><span class="sxs-lookup"><span data-stu-id="8c402-263">Format</span></span>

<span data-ttu-id="8c402-264">Combinaison de 11 caractères au format spécifié</span><span class="sxs-lookup"><span data-stu-id="8c402-264">An 11-character combination in the specified format</span></span>
  
### <a name="pattern"></a><span data-ttu-id="8c402-265">Modèle</span><span class="sxs-lookup"><span data-stu-id="8c402-265">Pattern</span></span>

<span data-ttu-id="8c402-266">Combinaison de 11 caractères au format spécifié :</span><span class="sxs-lookup"><span data-stu-id="8c402-266">An 11-character combination in the specified format:</span></span>
  
-  <span data-ttu-id="8c402-267">Six chiffres</span><span class="sxs-lookup"><span data-stu-id="8c402-267">Six digits</span></span> 
    
- <span data-ttu-id="8c402-268">Une instance de l’un des éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="8c402-268">One instance of one of the following:</span></span>
    
  - <span data-ttu-id="8c402-269">Symbole plus</span><span class="sxs-lookup"><span data-stu-id="8c402-269">Plus symbol</span></span>
    
  - <span data-ttu-id="8c402-270">Symbole moins</span><span class="sxs-lookup"><span data-stu-id="8c402-270">Minus symbol</span></span>
    
  - <span data-ttu-id="8c402-271">La lettre « A » (ne respecte pas la casse)</span><span class="sxs-lookup"><span data-stu-id="8c402-271">The letter "A" (not case-sensitive)</span></span>
    
- <span data-ttu-id="8c402-272">Trois chiffres</span><span class="sxs-lookup"><span data-stu-id="8c402-272">Three digits</span></span>
    
- <span data-ttu-id="8c402-273">Une lettre ou un chiffre</span><span class="sxs-lookup"><span data-stu-id="8c402-273">One letter or one digit</span></span>
    
### <a name="checksum"></a><span data-ttu-id="8c402-274">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="8c402-274">Checksum</span></span>

<span data-ttu-id="8c402-275">Oui</span><span class="sxs-lookup"><span data-stu-id="8c402-275">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="8c402-276">Définition</span><span class="sxs-lookup"><span data-stu-id="8c402-276">Definition</span></span>

<span data-ttu-id="8c402-277">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="8c402-277">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="8c402-278">La fonction `Func_finland_eu_ssn_or_equivalent` trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="8c402-278">The function  `Func_finland_eu_ssn_or_equivalent` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="8c402-279">Un mot clé `Keywords_finland_eu_ssn_or_equivalent` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="8c402-279">A keyword from  `Keywords_finland_eu_ssn_or_equivalent` is found.</span></span> 
    
<span data-ttu-id="8c402-280">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="8c402-280">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="8c402-281">La fonction `Func_finland_eu_ssn_or_equivalent` trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="8c402-281">The function  `Func_finland_eu_ssn_or_equivalent` finds content that matches the pattern.</span></span> 
    
```
 <!-- EU SSN or Equivalent Number -->
<Entity id="d24e32a4-c0bb-4ba8-899d-6303b95742d9" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_finland_eu_ssn_or_equivalent" />
          <Match idRef="Keywords_finland_eu_ssn_or_equivalent" />
        </Pattern> 
       <Pattern confidenceLevel="75">
          <IdMatch idRef="Func_finland_eu_ssn_or_equivalent" />
        </Pattern>      
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="8c402-282">Mots clés</span><span class="sxs-lookup"><span data-stu-id="8c402-282">Keywords</span></span>

#### <a name="keywords_finland_eu_ssn_or_equivalent"></a><span data-ttu-id="8c402-283">Keywords_finland_eu_ssn_or_equivalent</span><span class="sxs-lookup"><span data-stu-id="8c402-283">Keywords_finland_eu_ssn_or_equivalent</span></span>

<span data-ttu-id="8c402-284">numéro d’identification</span><span class="sxs-lookup"><span data-stu-id="8c402-284">identification number</span></span>
  
<span data-ttu-id="8c402-285">ID personnel</span><span class="sxs-lookup"><span data-stu-id="8c402-285">personal id</span></span>
  
<span data-ttu-id="8c402-286">Numéro d’identité</span><span class="sxs-lookup"><span data-stu-id="8c402-286">identity number</span></span>
  
<span data-ttu-id="8c402-287">Numéro d’identification national finnois</span><span class="sxs-lookup"><span data-stu-id="8c402-287">finnish national id number</span></span>
  
<span data-ttu-id="8c402-288">personalidnumber #</span><span class="sxs-lookup"><span data-stu-id="8c402-288">personalidnumber#</span></span>
  
<span data-ttu-id="8c402-289">numéro d’identification nationale</span><span class="sxs-lookup"><span data-stu-id="8c402-289">national identification number</span></span>
  
<span data-ttu-id="8c402-290">Numéro d’identification</span><span class="sxs-lookup"><span data-stu-id="8c402-290">id number</span></span>
  
<span data-ttu-id="8c402-291">Numéro d’identification nationale</span><span class="sxs-lookup"><span data-stu-id="8c402-291">national id no.</span></span>
  
<span data-ttu-id="8c402-292">Numéro d’identification national</span><span class="sxs-lookup"><span data-stu-id="8c402-292">national id number</span></span>
  
<span data-ttu-id="8c402-293">n ° ID</span><span class="sxs-lookup"><span data-stu-id="8c402-293">id no</span></span>
  
<span data-ttu-id="8c402-294">tunnistenumero</span><span class="sxs-lookup"><span data-stu-id="8c402-294">tunnistenumero</span></span>
  
<span data-ttu-id="8c402-295">henkilötunnus</span><span class="sxs-lookup"><span data-stu-id="8c402-295">henkilötunnus</span></span>
  
<span data-ttu-id="8c402-296">yksilöllinen henkilökohtainen tunnistenumero</span><span class="sxs-lookup"><span data-stu-id="8c402-296">yksilöllinen henkilökohtainen tunnistenumero</span></span>
  
<span data-ttu-id="8c402-297">ainutlaatuinen henkilökohtainen tunnus</span><span class="sxs-lookup"><span data-stu-id="8c402-297">ainutlaatuinen henkilökohtainen tunnus</span></span>
  
<span data-ttu-id="8c402-298">identiteetti numérique</span><span class="sxs-lookup"><span data-stu-id="8c402-298">identiteetti numero</span></span>
  
<span data-ttu-id="8c402-299">suomen kansallinen henkilötunnus</span><span class="sxs-lookup"><span data-stu-id="8c402-299">suomen kansallinen henkilötunnus</span></span>
  
<span data-ttu-id="8c402-300">henkilötunnusnumero #</span><span class="sxs-lookup"><span data-stu-id="8c402-300">henkilötunnusnumero#</span></span>
  
<span data-ttu-id="8c402-301">kansallisen tunnistenumero</span><span class="sxs-lookup"><span data-stu-id="8c402-301">kansallisen tunnistenumero</span></span>
  
<span data-ttu-id="8c402-302">tunnusnumero</span><span class="sxs-lookup"><span data-stu-id="8c402-302">tunnusnumero</span></span>
  
<span data-ttu-id="8c402-303">Kansallinen tunnus numérique</span><span class="sxs-lookup"><span data-stu-id="8c402-303">kansallinen tunnus numero</span></span>
  
<span data-ttu-id="8c402-304">hetu</span><span class="sxs-lookup"><span data-stu-id="8c402-304">hetu</span></span>
  
## <a name="france"></a><span data-ttu-id="8c402-305">France</span><span class="sxs-lookup"><span data-stu-id="8c402-305">France</span></span>

<span data-ttu-id="8c402-306">Pour plus d’informations, reportez-vous à la section « France-numéro de sécurité sociale (INSEE) » dans [la recherche des types d’informations sensibles](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="8c402-306">For details, see the section "France Social Security Number (INSEE)" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="germany"></a><span data-ttu-id="8c402-307">Allemagne</span><span class="sxs-lookup"><span data-stu-id="8c402-307">Germany</span></span>

<span data-ttu-id="8c402-308">Pour plus d’informations, reportez-vous à la section « Germany Identity Card Number » dans les [types d’informations sensibles](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="8c402-308">For details, see the section "Germany Identity Card Number" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="greece"></a><span data-ttu-id="8c402-309">Grèce</span><span class="sxs-lookup"><span data-stu-id="8c402-309">Greece</span></span>

<span data-ttu-id="8c402-310">Pour plus d’informations, reportez-vous à la section « carte d’identité nationale Grèce » dans [ce que recherche les types d’informations sensibles](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="8c402-310">For details, see the section "Greece National ID Card" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="hungary"></a><span data-ttu-id="8c402-311">Hongrie</span><span class="sxs-lookup"><span data-stu-id="8c402-311">Hungary</span></span>

### <a name="format"></a><span data-ttu-id="8c402-312">Format</span><span class="sxs-lookup"><span data-stu-id="8c402-312">Format</span></span>

<span data-ttu-id="8c402-313">Neuf chiffres sans espaces ni délimiteurs</span><span class="sxs-lookup"><span data-stu-id="8c402-313">Nine digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="8c402-314">Modèle</span><span class="sxs-lookup"><span data-stu-id="8c402-314">Pattern</span></span>

<span data-ttu-id="8c402-315">Neuf chiffres</span><span class="sxs-lookup"><span data-stu-id="8c402-315">Nine digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="8c402-316">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="8c402-316">Checksum</span></span>

<span data-ttu-id="8c402-317">Oui</span><span class="sxs-lookup"><span data-stu-id="8c402-317">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="8c402-318">Définition</span><span class="sxs-lookup"><span data-stu-id="8c402-318">Definition</span></span>

<span data-ttu-id="8c402-319">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="8c402-319">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="8c402-320">La fonction `Func_hungary_eu_ssn_or_equivalent` trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="8c402-320">The function  `Func_hungary_eu_ssn_or_equivalent` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="8c402-321">Un mot clé `Keywords_hungary_eu_ssn_or_equivalent` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="8c402-321">A keyword from  `Keywords_hungary_eu_ssn_or_equivalent` is found.</span></span> 
    
<span data-ttu-id="8c402-322">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="8c402-322">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="8c402-323">La fonction `Func_hungary_eu_ssn_or_equivalent` trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="8c402-323">The function  `Func_hungary_eu_ssn_or_equivalent` finds content that matches the pattern.</span></span> 
    
```
 <!-- EU SSN or Equivalent Number -->
<Entity id="d24e32a4-c0bb-4ba8-899d-6303b95742d9" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_hungary_eu_ssn_or_equivalent" />
          <Match idRef="Keywords_hungary_eu_ssn_or_equivalent" />
        </Pattern> 
       <Pattern confidenceLevel="75">
          <IdMatch idRef="Func_hungary_eu_ssn_or_equivalent" />
        </Pattern>      
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="8c402-324">Mots clés</span><span class="sxs-lookup"><span data-stu-id="8c402-324">Keywords</span></span>

#### <a name="keywords_hungary_eu_ssn_or_equivalent"></a><span data-ttu-id="8c402-325">Keywords_hungary_eu_ssn_or_equivalent</span><span class="sxs-lookup"><span data-stu-id="8c402-325">Keywords_hungary_eu_ssn_or_equivalent</span></span>

<span data-ttu-id="8c402-326">Numéro de sécurité sociale hongrois</span><span class="sxs-lookup"><span data-stu-id="8c402-326">hungarian social security number</span></span>
  
<span data-ttu-id="8c402-327">numéro de sécurité sociale</span><span class="sxs-lookup"><span data-stu-id="8c402-327">social security number</span></span>
  
<span data-ttu-id="8c402-328">socialsecuritynumber #</span><span class="sxs-lookup"><span data-stu-id="8c402-328">socialsecuritynumber#</span></span>
  
<span data-ttu-id="8c402-329">hssn #</span><span class="sxs-lookup"><span data-stu-id="8c402-329">hssn#</span></span>
  
<span data-ttu-id="8c402-330">socialsecuritynno</span><span class="sxs-lookup"><span data-stu-id="8c402-330">socialsecuritynno</span></span>
  
<span data-ttu-id="8c402-331">hssn</span><span class="sxs-lookup"><span data-stu-id="8c402-331">hssn</span></span>
  
<span data-ttu-id="8c402-332">taj</span><span class="sxs-lookup"><span data-stu-id="8c402-332">taj</span></span>
  
<span data-ttu-id="8c402-333">taj #</span><span class="sxs-lookup"><span data-stu-id="8c402-333">taj#</span></span>
  
<span data-ttu-id="8c402-334">SSN</span><span class="sxs-lookup"><span data-stu-id="8c402-334">ssn</span></span>
  
<span data-ttu-id="8c402-335">SSN #</span><span class="sxs-lookup"><span data-stu-id="8c402-335">ssn#</span></span>
  
<span data-ttu-id="8c402-336">Numéro de sécurité sociale</span><span class="sxs-lookup"><span data-stu-id="8c402-336">social security no</span></span>
  
<span data-ttu-id="8c402-337">áfa</span><span class="sxs-lookup"><span data-stu-id="8c402-337">áfa</span></span>
  
<span data-ttu-id="8c402-338">közösségi adószám</span><span class="sxs-lookup"><span data-stu-id="8c402-338">közösségi adószám</span></span>
  
<span data-ttu-id="8c402-339">általános forgalmi adó szám</span><span class="sxs-lookup"><span data-stu-id="8c402-339">általános forgalmi adó szám</span></span>
  
<span data-ttu-id="8c402-340">hozzáadottérték adó</span><span class="sxs-lookup"><span data-stu-id="8c402-340">hozzáadottérték adó</span></span>
  
<span data-ttu-id="8c402-341">áfa szám</span><span class="sxs-lookup"><span data-stu-id="8c402-341">áfa szám</span></span>
  
<span data-ttu-id="8c402-342">magyar áfa szám</span><span class="sxs-lookup"><span data-stu-id="8c402-342">magyar áfa szám</span></span>
  
## <a name="portugal"></a><span data-ttu-id="8c402-343">Portugal</span><span class="sxs-lookup"><span data-stu-id="8c402-343">Portugal</span></span>

<span data-ttu-id="8c402-344">Pour plus d’informations, reportez-vous à la section « numéro de carte de citoyen Portugal » dans [la recherche des types d’informations sensibles](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="8c402-344">For details, see the section "Portugal Citizen Card Number" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="spain"></a><span data-ttu-id="8c402-345">Espagne</span><span class="sxs-lookup"><span data-stu-id="8c402-345">Spain</span></span>

<span data-ttu-id="8c402-346">Pour plus d’informations, reportez-vous à la section « numéro de sécurité sociale Espagne » dans les [types d’informations sensibles](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="8c402-346">For details, see the section "Spain Social Security Number (SSN)" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="sweden"></a><span data-ttu-id="8c402-347">Suède</span><span class="sxs-lookup"><span data-stu-id="8c402-347">Sweden</span></span>

### <a name="format"></a><span data-ttu-id="8c402-348">Format</span><span class="sxs-lookup"><span data-stu-id="8c402-348">Format</span></span>

<span data-ttu-id="8c402-349">12 chiffres sans espaces ni délimiteurs</span><span class="sxs-lookup"><span data-stu-id="8c402-349">12 digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="8c402-350">Modèle</span><span class="sxs-lookup"><span data-stu-id="8c402-350">Pattern</span></span>

<span data-ttu-id="8c402-351">12 chiffres :</span><span class="sxs-lookup"><span data-stu-id="8c402-351">12 digits:</span></span>
  
-  <span data-ttu-id="8c402-352">Huit chiffres correspondant à la date de naissance (AAAAMMJJ)</span><span class="sxs-lookup"><span data-stu-id="8c402-352">Eight digits that correspond to the birth date (YYYYMMDD)</span></span> 
    
- <span data-ttu-id="8c402-353">Trois chiffres correspondant à un numéro de série où :</span><span class="sxs-lookup"><span data-stu-id="8c402-353">Three digits that correspond to a serial number where:</span></span> 
    
  - <span data-ttu-id="8c402-354">Le dernier chiffre du numéro de série indique sexe par l’affectation d’un nombre impair pour le mâle et d’un nombre pair pour femelle.</span><span class="sxs-lookup"><span data-stu-id="8c402-354">The last digit in the serial number indicates gender by the assignment of an odd number for male and an even number for female</span></span>
    
  - <span data-ttu-id="8c402-355">Jusqu’à 1990, l’affectation du numéro de série correspond au comté où le porteur du numéro est né ou (en naissance avant 1947) où il a été vivant, en fonction des enregistrements fiscaux, le 1er janvier 1947, avec un code spécial (généralement 9 comme le 7 chiffres) pour immigrants</span><span class="sxs-lookup"><span data-stu-id="8c402-355">Up to 1990, the assignment of serial number corresponded to the county where the bearer of the number was born or (if born before 1947) where he/she had been living, according to tax records, on January 1, 1947, with a special code (usually 9 as the 7th digit) for immigrants</span></span> 
    
- <span data-ttu-id="8c402-356">Un chiffre de contrôle</span><span class="sxs-lookup"><span data-stu-id="8c402-356">One check digit</span></span>
    
### <a name="checksum"></a><span data-ttu-id="8c402-357">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="8c402-357">Checksum</span></span>

<span data-ttu-id="8c402-358">Oui</span><span class="sxs-lookup"><span data-stu-id="8c402-358">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="8c402-359">Définition</span><span class="sxs-lookup"><span data-stu-id="8c402-359">Definition</span></span>

<span data-ttu-id="8c402-360">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="8c402-360">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="8c402-361">La fonction `Func_sweden_eu_ssn_or_equivalent` trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="8c402-361">The function  `Func_sweden_eu_ssn_or_equivalent` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="8c402-362">Un mot clé `Keywords_sweden_eu_ssn_or_equivalent` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="8c402-362">A keyword from  `Keywords_sweden_eu_ssn_or_equivalent` is found.</span></span> 
    
<span data-ttu-id="8c402-363">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="8c402-363">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="8c402-364">La fonction `Func_sweden_eu_ssn_or_equivalent` trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="8c402-364">The function  `Func_sweden_eu_ssn_or_equivalent` finds content that matches the pattern.</span></span> 
    
```
 <!-- EU SSN or Equivalent Number -->
<Entity id="d24e32a4-c0bb-4ba8-899d-6303b95742d9" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_sweden_eu_ssn_or_equivalent" />
          <Match idRef="Keywords_sweden_eu_ssn_or_equivalent" />
        </Pattern> 
       <Pattern confidenceLevel="75">
          <IdMatch idRef="Func_sweden_eu_ssn_or_equivalent" />
        </Pattern>      
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="8c402-365">Mots clés</span><span class="sxs-lookup"><span data-stu-id="8c402-365">Keywords</span></span>

#### <a name="keywords_sweden_eu_ssn_or_equivalent"></a><span data-ttu-id="8c402-366">Keywords_sweden_eu_ssn_or_equivalent</span><span class="sxs-lookup"><span data-stu-id="8c402-366">Keywords_sweden_eu_ssn_or_equivalent</span></span>

<span data-ttu-id="8c402-367">Numéro d’identification personnel</span><span class="sxs-lookup"><span data-stu-id="8c402-367">personal id number</span></span>
  
<span data-ttu-id="8c402-368">numéro d’identification</span><span class="sxs-lookup"><span data-stu-id="8c402-368">identification number</span></span>
  
<span data-ttu-id="8c402-369">Numéro d’identification personnel</span><span class="sxs-lookup"><span data-stu-id="8c402-369">personal id no</span></span>
  
<span data-ttu-id="8c402-370">n ° d’identité</span><span class="sxs-lookup"><span data-stu-id="8c402-370">identity no</span></span>
  
<span data-ttu-id="8c402-371">Numéro d’identification</span><span class="sxs-lookup"><span data-stu-id="8c402-371">identification no</span></span>
  
<span data-ttu-id="8c402-372">Numéro d’identification personnel</span><span class="sxs-lookup"><span data-stu-id="8c402-372">personal identification no</span></span>
  
<span data-ttu-id="8c402-373">ID personnummer</span><span class="sxs-lookup"><span data-stu-id="8c402-373">personnummer id</span></span>
  
<span data-ttu-id="8c402-374">ID personligt-Nummer</span><span class="sxs-lookup"><span data-stu-id="8c402-374">personligt id-nummer</span></span>
  
<span data-ttu-id="8c402-375">ID unikt-Nummer</span><span class="sxs-lookup"><span data-stu-id="8c402-375">unikt id-nummer</span></span>
  
<span data-ttu-id="8c402-376">personnummer</span><span class="sxs-lookup"><span data-stu-id="8c402-376">personnummer</span></span>
  
<span data-ttu-id="8c402-377">identifikationsnumret</span><span class="sxs-lookup"><span data-stu-id="8c402-377">identifikationsnumret</span></span>
  
<span data-ttu-id="8c402-378">personnummer #</span><span class="sxs-lookup"><span data-stu-id="8c402-378">personnummer#</span></span>
  
<span data-ttu-id="8c402-379">identifikationsnumret #</span><span class="sxs-lookup"><span data-stu-id="8c402-379">identifikationsnumret#</span></span>
  
## <a name="see-also"></a><span data-ttu-id="8c402-380">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8c402-380">See also</span></span>

[<span data-ttu-id="8c402-381">Éléments recherchés par les types d’informations sensibles</span><span class="sxs-lookup"><span data-stu-id="8c402-381">What the sensitive information types look for</span></span>](what-the-sensitive-information-types-look-for.md)

