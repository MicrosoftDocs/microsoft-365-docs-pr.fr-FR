---
title: Numéro de sécurité sociale de l’UE ou ID équivalent
ms.author: stephow
author: stephow-MSFT
manager: laurawi
ms.date: 8/17/2018
audience: Admin
ms.topic: reference
ms.service: O365-seccomp
ms.collection: M365-security-compliance
localization_priority: Normal
description: Cette rubrique indique ce qu’est une stratégie de protection contre la perte de données (DLP) lorsqu’elle détecte le type d’informations sensibles de l’UE ou d’un ID équivalent. Ce type d’informations sensibles définit différents modèles, Mots clés et autres preuves pour chaque pays.
ms.openlocfilehash: b42a8d927e18f813eb6ef6d1d55b2de15ea9dcd5
ms.sourcegitcommit: 1162d676b036449ea4220de8a6642165190e3398
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/20/2019
ms.locfileid: "37079267"
---
# <a name="eu-social-security-number-or-equivalent-id"></a><span data-ttu-id="040c6-104">Numéro de sécurité sociale de l’UE ou ID équivalent</span><span class="sxs-lookup"><span data-stu-id="040c6-104">EU Social Security Number or Equivalent ID</span></span>

<span data-ttu-id="040c6-105">Cette rubrique présente ce qu’une stratégie de protection contre la perte de données (DLP) recherche lorsqu’elle détecte le type d’informations sensibles de l’UE ou un ID équivalent.</span><span class="sxs-lookup"><span data-stu-id="040c6-105">This topic shows what a data loss prevention (DLP) policy looks for when it detects the EU Social Security Number (SSN) or Equivalent ID sensitive information type.</span></span> <span data-ttu-id="040c6-106">Ce type d’informations sensibles définit différents modèles, Mots clés et autres preuves pour chaque pays.</span><span class="sxs-lookup"><span data-stu-id="040c6-106">This sensitive information type defines different patterns, keywords, and other evidence for each country.</span></span>
  
## <a name="austria"></a><span data-ttu-id="040c6-107">Autriche</span><span class="sxs-lookup"><span data-stu-id="040c6-107">Austria</span></span>

### <a name="format"></a><span data-ttu-id="040c6-108">Format</span><span class="sxs-lookup"><span data-stu-id="040c6-108">Format</span></span>

<span data-ttu-id="040c6-109">10 chiffres au format spécifié</span><span class="sxs-lookup"><span data-stu-id="040c6-109">10 digits in the specified format</span></span>
  
### <a name="pattern"></a><span data-ttu-id="040c6-110">Modèle</span><span class="sxs-lookup"><span data-stu-id="040c6-110">Pattern</span></span>

<span data-ttu-id="040c6-111">10 chiffres :</span><span class="sxs-lookup"><span data-stu-id="040c6-111">10 digits:</span></span>
  
-  <span data-ttu-id="040c6-112">Trois chiffres correspondant à un numéro de série</span><span class="sxs-lookup"><span data-stu-id="040c6-112">Three digits that correspond to a serial number</span></span> 
    
- <span data-ttu-id="040c6-113">Un chiffre de contrôle</span><span class="sxs-lookup"><span data-stu-id="040c6-113">One check digit</span></span>
    
- <span data-ttu-id="040c6-114">Six chiffres correspondant à la date de naissance (JJMMAA)</span><span class="sxs-lookup"><span data-stu-id="040c6-114">Six digits that correspond to the birth date (DDMMYY)</span></span>
    
### <a name="checksum"></a><span data-ttu-id="040c6-115">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="040c6-115">Checksum</span></span>

<span data-ttu-id="040c6-116">Oui</span><span class="sxs-lookup"><span data-stu-id="040c6-116">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="040c6-117">Définition</span><span class="sxs-lookup"><span data-stu-id="040c6-117">Definition</span></span>

<span data-ttu-id="040c6-118">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="040c6-118">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="040c6-119">La fonction `Func_austria_eu_ssn_or_equivalent` trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="040c6-119">The function  `Func_austria_eu_ssn_or_equivalent` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="040c6-120">Un mot clé `Keywords_austria_eu_ssn_or_equivalent` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="040c6-120">A keyword from  `Keywords_austria_eu_ssn_or_equivalent` is found.</span></span> 
    
<span data-ttu-id="040c6-121">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="040c6-121">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="040c6-122">La fonction `Func_austria_eu_ssn_or_equivalent` trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="040c6-122">The function  `Func_austria_eu_ssn_or_equivalent` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="040c6-123">Mots clés</span><span class="sxs-lookup"><span data-stu-id="040c6-123">Keywords</span></span>

#### <a name="keywords_austria_eu_ssn_or_equivalent"></a><span data-ttu-id="040c6-124">Keywords_austria_eu_ssn_or_equivalent</span><span class="sxs-lookup"><span data-stu-id="040c6-124">Keywords_austria_eu_ssn_or_equivalent</span></span>

<span data-ttu-id="040c6-125">Numéro de sécurité sociale</span><span class="sxs-lookup"><span data-stu-id="040c6-125">social security no</span></span>
  
<span data-ttu-id="040c6-126">numéro de sécurité sociale</span><span class="sxs-lookup"><span data-stu-id="040c6-126">social security number</span></span>
  
<span data-ttu-id="040c6-127">code de sécurité sociale</span><span class="sxs-lookup"><span data-stu-id="040c6-127">social security code</span></span>
  
<span data-ttu-id="040c6-128">Numéro d’assurance</span><span class="sxs-lookup"><span data-stu-id="040c6-128">insurance number</span></span>
  
<span data-ttu-id="040c6-129">Numéro de sécurité sociale autrichien</span><span class="sxs-lookup"><span data-stu-id="040c6-129">austrian ssn</span></span>
  
<span data-ttu-id="040c6-130">SSN #</span><span class="sxs-lookup"><span data-stu-id="040c6-130">ssn#</span></span>
  
<span data-ttu-id="040c6-131">SSN</span><span class="sxs-lookup"><span data-stu-id="040c6-131">ssn</span></span>
  
<span data-ttu-id="040c6-132">code d’assurance</span><span class="sxs-lookup"><span data-stu-id="040c6-132">insurance code</span></span>
  
<span data-ttu-id="040c6-133">code d’assurance #</span><span class="sxs-lookup"><span data-stu-id="040c6-133">insurance code#</span></span>
  
<span data-ttu-id="040c6-134">socialsecurityno #</span><span class="sxs-lookup"><span data-stu-id="040c6-134">socialsecurityno#</span></span>
  
<span data-ttu-id="040c6-135">sozialversicherungsnummer</span><span class="sxs-lookup"><span data-stu-id="040c6-135">sozialversicherungsnummer</span></span>
  
<span data-ttu-id="040c6-136">soziale sicherheit kein</span><span class="sxs-lookup"><span data-stu-id="040c6-136">soziale sicherheit kein</span></span>
  
<span data-ttu-id="040c6-137">versicherungsnummer</span><span class="sxs-lookup"><span data-stu-id="040c6-137">versicherungsnummer</span></span>
  
## <a name="belgium"></a><span data-ttu-id="040c6-138">Belgique</span><span class="sxs-lookup"><span data-stu-id="040c6-138">Belgium</span></span>

### <a name="format"></a><span data-ttu-id="040c6-139">Format</span><span class="sxs-lookup"><span data-stu-id="040c6-139">Format</span></span>

<span data-ttu-id="040c6-140">11 chiffres sans espaces ni délimiteurs</span><span class="sxs-lookup"><span data-stu-id="040c6-140">11 digits without spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="040c6-141">Modèle</span><span class="sxs-lookup"><span data-stu-id="040c6-141">Pattern</span></span>

<span data-ttu-id="040c6-142">11 chiffres</span><span class="sxs-lookup"><span data-stu-id="040c6-142">11 digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="040c6-143">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="040c6-143">Checksum</span></span>

<span data-ttu-id="040c6-144">Oui</span><span class="sxs-lookup"><span data-stu-id="040c6-144">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="040c6-145">Définition</span><span class="sxs-lookup"><span data-stu-id="040c6-145">Definition</span></span>

<span data-ttu-id="040c6-146">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="040c6-146">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="040c6-147">La fonction `Func_belgium_eu_ssn_or_equivalent` trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="040c6-147">The function  `Func_belgium_eu_ssn_or_equivalent` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="040c6-148">Un mot clé `Keywords_belgium_eu_ssn_or_equivalent` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="040c6-148">A keyword from  `Keywords_belgium_eu_ssn_or_equivalent` is found.</span></span> 
    
<span data-ttu-id="040c6-149">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="040c6-149">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="040c6-150">La fonction `Func_belgium_eu_ssn_or_equivalent` trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="040c6-150">The function  `Func_belgium_eu_ssn_or_equivalent` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="040c6-151">Mots clés</span><span class="sxs-lookup"><span data-stu-id="040c6-151">Keywords</span></span>

#### <a name="keywords_belgium_eu_ssn_or_equivalent"></a><span data-ttu-id="040c6-152">Keywords_belgium_eu_ssn_or_equivalent</span><span class="sxs-lookup"><span data-stu-id="040c6-152">Keywords_belgium_eu_ssn_or_equivalent</span></span>

<span data-ttu-id="040c6-153">numéro national belge</span><span class="sxs-lookup"><span data-stu-id="040c6-153">belgian national number</span></span>
  
<span data-ttu-id="040c6-154">numéro national</span><span class="sxs-lookup"><span data-stu-id="040c6-154">national number</span></span>
  
<span data-ttu-id="040c6-155">numéro de sécurité sociale</span><span class="sxs-lookup"><span data-stu-id="040c6-155">social security number</span></span>
  
<span data-ttu-id="040c6-156">nationalnumber #</span><span class="sxs-lookup"><span data-stu-id="040c6-156">nationalnumber#</span></span>
  
<span data-ttu-id="040c6-157">SSN #</span><span class="sxs-lookup"><span data-stu-id="040c6-157">ssn#</span></span>
  
<span data-ttu-id="040c6-158">SSN</span><span class="sxs-lookup"><span data-stu-id="040c6-158">ssn</span></span>
  
<span data-ttu-id="040c6-159">nationalnumber</span><span class="sxs-lookup"><span data-stu-id="040c6-159">nationalnumber</span></span>
  
<span data-ttu-id="040c6-160">bnn #</span><span class="sxs-lookup"><span data-stu-id="040c6-160">bnn#</span></span>
  
<span data-ttu-id="040c6-161">bnn</span><span class="sxs-lookup"><span data-stu-id="040c6-161">bnn</span></span>
  
<span data-ttu-id="040c6-162">Numéro d’identification personnel</span><span class="sxs-lookup"><span data-stu-id="040c6-162">personal id number</span></span>
  
<span data-ttu-id="040c6-163">personalidnumber #</span><span class="sxs-lookup"><span data-stu-id="040c6-163">personalidnumber#</span></span>
  
<span data-ttu-id="040c6-164">numéro national</span><span class="sxs-lookup"><span data-stu-id="040c6-164">numéro national</span></span>
  
<span data-ttu-id="040c6-165">numéro de sécurité</span><span class="sxs-lookup"><span data-stu-id="040c6-165">numéro de sécurité</span></span>
  
<span data-ttu-id="040c6-166">numéro d’assuré</span><span class="sxs-lookup"><span data-stu-id="040c6-166">numéro d'assuré</span></span>
  
<span data-ttu-id="040c6-167">identifiant national</span><span class="sxs-lookup"><span data-stu-id="040c6-167">identifiant national</span></span>
  
<span data-ttu-id="040c6-168">identifiantnational #</span><span class="sxs-lookup"><span data-stu-id="040c6-168">identifiantnational#</span></span>
  
<span data-ttu-id="040c6-169">numéronational #</span><span class="sxs-lookup"><span data-stu-id="040c6-169">numéronational#</span></span>
  
## <a name="croatia"></a><span data-ttu-id="040c6-170">Croatie</span><span class="sxs-lookup"><span data-stu-id="040c6-170">Croatia</span></span>

### <a name="format"></a><span data-ttu-id="040c6-171">Format</span><span class="sxs-lookup"><span data-stu-id="040c6-171">Format</span></span>

<span data-ttu-id="040c6-172">11 chiffres sans espaces ni délimiteurs</span><span class="sxs-lookup"><span data-stu-id="040c6-172">11 digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="040c6-173">Modèle</span><span class="sxs-lookup"><span data-stu-id="040c6-173">Pattern</span></span>

 <span data-ttu-id="040c6-174">11 chiffres :</span><span class="sxs-lookup"><span data-stu-id="040c6-174">11 digits:</span></span> 
  
-  <span data-ttu-id="040c6-175">Dix chiffres</span><span class="sxs-lookup"><span data-stu-id="040c6-175">Ten digits</span></span> 
    
- <span data-ttu-id="040c6-176">Un chiffre de contrôle</span><span class="sxs-lookup"><span data-stu-id="040c6-176">One check digit</span></span>
    
### <a name="checksum"></a><span data-ttu-id="040c6-177">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="040c6-177">Checksum</span></span>

<span data-ttu-id="040c6-178">Oui</span><span class="sxs-lookup"><span data-stu-id="040c6-178">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="040c6-179">Définition</span><span class="sxs-lookup"><span data-stu-id="040c6-179">Definition</span></span>

<span data-ttu-id="040c6-180">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="040c6-180">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="040c6-181">La fonction `Func_croatia_eu_ssn_or_equivalent` trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="040c6-181">The function  `Func_croatia_eu_ssn_or_equivalent` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="040c6-182">Un mot clé `Keywords_croatia_eu_ssn_or_equivalent` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="040c6-182">A keyword from  `Keywords_croatia_eu_ssn_or_equivalent` is found.</span></span> 
    
<span data-ttu-id="040c6-183">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="040c6-183">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="040c6-184">La fonction `Func_croatia_eu_ssn_or_equivalent` trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="040c6-184">The function  `Func_croatia_eu_ssn_or_equivalent` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="040c6-185">Mots clés</span><span class="sxs-lookup"><span data-stu-id="040c6-185">Keywords</span></span>

#### <a name="keywords_croatia_eu_ssn_or_equivalent"></a><span data-ttu-id="040c6-186">Keywords_croatia_eu_ssn_or_equivalent</span><span class="sxs-lookup"><span data-stu-id="040c6-186">Keywords_croatia_eu_ssn_or_equivalent</span></span>

<span data-ttu-id="040c6-187">Numéro d’identification personnel</span><span class="sxs-lookup"><span data-stu-id="040c6-187">personal identification number</span></span>
  
<span data-ttu-id="040c6-188">Numéro de citoyen principal</span><span class="sxs-lookup"><span data-stu-id="040c6-188">master citizen number</span></span>
  
<span data-ttu-id="040c6-189">numéro d’identification nationale</span><span class="sxs-lookup"><span data-stu-id="040c6-189">national identification number</span></span>
  
<span data-ttu-id="040c6-190">numéro de sécurité sociale</span><span class="sxs-lookup"><span data-stu-id="040c6-190">social security number</span></span>
  
<span data-ttu-id="040c6-191">nationalnumber #</span><span class="sxs-lookup"><span data-stu-id="040c6-191">nationalnumber#</span></span>
  
<span data-ttu-id="040c6-192">SSN #</span><span class="sxs-lookup"><span data-stu-id="040c6-192">ssn#</span></span>
  
<span data-ttu-id="040c6-193">SSN</span><span class="sxs-lookup"><span data-stu-id="040c6-193">ssn</span></span>
  
<span data-ttu-id="040c6-194">nationalnumber</span><span class="sxs-lookup"><span data-stu-id="040c6-194">nationalnumber</span></span>
  
<span data-ttu-id="040c6-195">bnn #</span><span class="sxs-lookup"><span data-stu-id="040c6-195">bnn#</span></span>
  
<span data-ttu-id="040c6-196">bnn</span><span class="sxs-lookup"><span data-stu-id="040c6-196">bnn</span></span>
  
<span data-ttu-id="040c6-197">Numéro d’identification personnel</span><span class="sxs-lookup"><span data-stu-id="040c6-197">personal id number</span></span>
  
<span data-ttu-id="040c6-198">personalidnumber #</span><span class="sxs-lookup"><span data-stu-id="040c6-198">personalidnumber#</span></span>
  
<span data-ttu-id="040c6-199">OIB</span><span class="sxs-lookup"><span data-stu-id="040c6-199">oib</span></span>
  
<span data-ttu-id="040c6-200">osobni identifikacijski broj</span><span class="sxs-lookup"><span data-stu-id="040c6-200">osobni identifikacijski broj</span></span>
  
## <a name="czech-republic"></a><span data-ttu-id="040c6-201">République tchèque</span><span class="sxs-lookup"><span data-stu-id="040c6-201">Czech Republic</span></span>

### <a name="format"></a><span data-ttu-id="040c6-202">Format</span><span class="sxs-lookup"><span data-stu-id="040c6-202">Format</span></span>

<span data-ttu-id="040c6-203">10 chiffres et une barre oblique inverse dans le modèle spécifié</span><span class="sxs-lookup"><span data-stu-id="040c6-203">Ten digits and a backslash in the specified pattern</span></span>
  
### <a name="pattern"></a><span data-ttu-id="040c6-204">Modèle</span><span class="sxs-lookup"><span data-stu-id="040c6-204">Pattern</span></span>

<span data-ttu-id="040c6-205">Dix chiffres et une barre oblique inverse :</span><span class="sxs-lookup"><span data-stu-id="040c6-205">Ten digits and a backslash:</span></span>
  
- <span data-ttu-id="040c6-206">Six chiffres correspondant à la date de naissance (AAMMJJ) :</span><span class="sxs-lookup"><span data-stu-id="040c6-206">Six digits that correspond to the birth date (YYMMDD):</span></span> 
    
- <span data-ttu-id="040c6-207">Une barre oblique inverse</span><span class="sxs-lookup"><span data-stu-id="040c6-207">A backslash</span></span>
    
- <span data-ttu-id="040c6-208">Trois chiffres correspondant à un numéro de série qui sépare les personnes nés à la même date</span><span class="sxs-lookup"><span data-stu-id="040c6-208">Three digits that correspond to a serial number that separates persons born on the same date</span></span>
    
- <span data-ttu-id="040c6-209">Un chiffre de contrôle</span><span class="sxs-lookup"><span data-stu-id="040c6-209">One check digit</span></span>
    
### <a name="checksum"></a><span data-ttu-id="040c6-210">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="040c6-210">Checksum</span></span>

<span data-ttu-id="040c6-211">Oui</span><span class="sxs-lookup"><span data-stu-id="040c6-211">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="040c6-212">Définition</span><span class="sxs-lookup"><span data-stu-id="040c6-212">Definition</span></span>

<span data-ttu-id="040c6-213">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="040c6-213">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="040c6-214">La fonction `Func_czech_republic_eu_ssn_or_equivalent` trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="040c6-214">The function  `Func_czech_republic_eu_ssn_or_equivalent` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="040c6-215">Un mot clé `Keywords_czech_republic_eu_ssn_or_equivalent` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="040c6-215">A keyword from  `Keywords_czech_republic_eu_ssn_or_equivalent` is found.</span></span> 
    
<span data-ttu-id="040c6-216">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="040c6-216">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="040c6-217">La fonction `Func_czech_republic_eu_ssn_or_equivalent` trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="040c6-217">The function  `Func_czech_republic_eu_ssn_or_equivalent` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="040c6-218">Mots clés</span><span class="sxs-lookup"><span data-stu-id="040c6-218">Keywords</span></span>

#### <a name="keywords_czech_republic_eu_ssn_or_equivalent"></a><span data-ttu-id="040c6-219">Keywords_czech_republic_eu_ssn_or_equivalent</span><span class="sxs-lookup"><span data-stu-id="040c6-219">Keywords_czech_republic_eu_ssn_or_equivalent</span></span>

<span data-ttu-id="040c6-220">Numéro de naissance</span><span class="sxs-lookup"><span data-stu-id="040c6-220">birth number</span></span>
  
<span data-ttu-id="040c6-221">numéro d’identification nationale</span><span class="sxs-lookup"><span data-stu-id="040c6-221">national identification number</span></span>
  
<span data-ttu-id="040c6-222">Numéro d’identification personnel</span><span class="sxs-lookup"><span data-stu-id="040c6-222">personal identification number</span></span>
  
<span data-ttu-id="040c6-223">numéro de sécurité sociale</span><span class="sxs-lookup"><span data-stu-id="040c6-223">social security number</span></span>
  
<span data-ttu-id="040c6-224">nationalnumber #</span><span class="sxs-lookup"><span data-stu-id="040c6-224">nationalnumber#</span></span>
  
<span data-ttu-id="040c6-225">SSN #</span><span class="sxs-lookup"><span data-stu-id="040c6-225">ssn#</span></span>
  
<span data-ttu-id="040c6-226">SSN</span><span class="sxs-lookup"><span data-stu-id="040c6-226">ssn</span></span>
  
<span data-ttu-id="040c6-227">numéro national</span><span class="sxs-lookup"><span data-stu-id="040c6-227">national number</span></span>
  
<span data-ttu-id="040c6-228">Numéro d’identification personnel</span><span class="sxs-lookup"><span data-stu-id="040c6-228">personal id number</span></span>
  
<span data-ttu-id="040c6-229">personalidnumber #</span><span class="sxs-lookup"><span data-stu-id="040c6-229">personalidnumber#</span></span>
  
<span data-ttu-id="040c6-230">rč</span><span class="sxs-lookup"><span data-stu-id="040c6-230">rč</span></span>
  
<span data-ttu-id="040c6-231">rodné číslo</span><span class="sxs-lookup"><span data-stu-id="040c6-231">rodné číslo</span></span>
  
<span data-ttu-id="040c6-232">rodne cislo</span><span class="sxs-lookup"><span data-stu-id="040c6-232">rodne cislo</span></span>
  
## <a name="denmark"></a><span data-ttu-id="040c6-233">Danemark</span><span class="sxs-lookup"><span data-stu-id="040c6-233">Denmark</span></span>

### <a name="format"></a><span data-ttu-id="040c6-234">Format</span><span class="sxs-lookup"><span data-stu-id="040c6-234">Format</span></span>

<span data-ttu-id="040c6-235">10 chiffres et un trait d’Union dans le modèle spécifié</span><span class="sxs-lookup"><span data-stu-id="040c6-235">Ten digits and a hyphen in the specified pattern</span></span>
  
### <a name="pattern"></a><span data-ttu-id="040c6-236">Modèle</span><span class="sxs-lookup"><span data-stu-id="040c6-236">Pattern</span></span>

<span data-ttu-id="040c6-237">Dix chiffres et un trait d’Union :</span><span class="sxs-lookup"><span data-stu-id="040c6-237">Ten digits and a hyphen:</span></span>
  
- <span data-ttu-id="040c6-238">Six chiffres correspondant à la date de naissance (JJMMAA)</span><span class="sxs-lookup"><span data-stu-id="040c6-238">Six digits that correspond to the birth date (DDMMYY)</span></span> 
    
- <span data-ttu-id="040c6-239">Un trait d’union </span><span class="sxs-lookup"><span data-stu-id="040c6-239">A hyphen</span></span>
    
- <span data-ttu-id="040c6-240">Quatre chiffres correspondant à un numéro de séquence</span><span class="sxs-lookup"><span data-stu-id="040c6-240">Four digits that correspond to a sequence number</span></span>
    
### <a name="checksum"></a><span data-ttu-id="040c6-241">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="040c6-241">Checksum</span></span>

<span data-ttu-id="040c6-242">Oui</span><span class="sxs-lookup"><span data-stu-id="040c6-242">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="040c6-243">Définition</span><span class="sxs-lookup"><span data-stu-id="040c6-243">Definition</span></span>

<span data-ttu-id="040c6-244">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="040c6-244">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="040c6-245">La fonction `Func_denmark_eu_ssn_or_equivalent` trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="040c6-245">The function  `Func_denmark_eu_ssn_or_equivalent` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="040c6-246">Un mot clé `Keywords_denmark_eu_ssn_or_equivalent` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="040c6-246">A keyword from  `Keywords_denmark_eu_ssn_or_equivalent` is found.</span></span> 
    
<span data-ttu-id="040c6-247">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="040c6-247">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="040c6-248">La fonction `Func_denmark_eu_ssn_or_equivalent` trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="040c6-248">The function  `Func_denmark_eu_ssn_or_equivalent` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="040c6-249">Mots clés</span><span class="sxs-lookup"><span data-stu-id="040c6-249">Keywords</span></span>

#### <a name="keywords_denmark_eu_ssn_or_equivalent"></a><span data-ttu-id="040c6-250">Keywords_denmark_eu_ssn_or_equivalent</span><span class="sxs-lookup"><span data-stu-id="040c6-250">Keywords_denmark_eu_ssn_or_equivalent</span></span>

<span data-ttu-id="040c6-251">Numéro d’identification personnel</span><span class="sxs-lookup"><span data-stu-id="040c6-251">personal identification number</span></span>
  
<span data-ttu-id="040c6-252">numéro d’identification nationale</span><span class="sxs-lookup"><span data-stu-id="040c6-252">national identification number</span></span>
  
<span data-ttu-id="040c6-253">numéro de sécurité sociale</span><span class="sxs-lookup"><span data-stu-id="040c6-253">social security number</span></span>
  
<span data-ttu-id="040c6-254">nationalnumber #</span><span class="sxs-lookup"><span data-stu-id="040c6-254">nationalnumber#</span></span>
  
<span data-ttu-id="040c6-255">SSN #</span><span class="sxs-lookup"><span data-stu-id="040c6-255">ssn#</span></span>
  
<span data-ttu-id="040c6-256">SSN</span><span class="sxs-lookup"><span data-stu-id="040c6-256">ssn</span></span>
  
<span data-ttu-id="040c6-257">numéro national</span><span class="sxs-lookup"><span data-stu-id="040c6-257">national number</span></span>
  
<span data-ttu-id="040c6-258">Numéro d’identification personnel</span><span class="sxs-lookup"><span data-stu-id="040c6-258">personal id number</span></span>
  
<span data-ttu-id="040c6-259">personalidnumber #</span><span class="sxs-lookup"><span data-stu-id="040c6-259">personalidnumber#</span></span>
  
<span data-ttu-id="040c6-260">CPR-nummer</span><span class="sxs-lookup"><span data-stu-id="040c6-260">cpr-nummer</span></span>
  
<span data-ttu-id="040c6-261">personnummer</span><span class="sxs-lookup"><span data-stu-id="040c6-261">personnummer</span></span>
  
## <a name="finland"></a><span data-ttu-id="040c6-262">Finlande</span><span class="sxs-lookup"><span data-stu-id="040c6-262">Finland</span></span>

### <a name="format"></a><span data-ttu-id="040c6-263">Format</span><span class="sxs-lookup"><span data-stu-id="040c6-263">Format</span></span>

<span data-ttu-id="040c6-264">Combinaison de 11 caractères au format spécifié</span><span class="sxs-lookup"><span data-stu-id="040c6-264">An 11-character combination in the specified format</span></span>
  
### <a name="pattern"></a><span data-ttu-id="040c6-265">Modèle</span><span class="sxs-lookup"><span data-stu-id="040c6-265">Pattern</span></span>

<span data-ttu-id="040c6-266">Combinaison de 11 caractères au format spécifié :</span><span class="sxs-lookup"><span data-stu-id="040c6-266">An 11-character combination in the specified format:</span></span>
  
-  <span data-ttu-id="040c6-267">Six chiffres</span><span class="sxs-lookup"><span data-stu-id="040c6-267">Six digits</span></span> 
    
- <span data-ttu-id="040c6-268">Une instance de l’un des éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="040c6-268">One instance of one of the following:</span></span>
    
  - <span data-ttu-id="040c6-269">Symbole plus</span><span class="sxs-lookup"><span data-stu-id="040c6-269">Plus symbol</span></span>
    
  - <span data-ttu-id="040c6-270">Symbole moins</span><span class="sxs-lookup"><span data-stu-id="040c6-270">Minus symbol</span></span>
    
  - <span data-ttu-id="040c6-271">La lettre « A » (ne respecte pas la casse)</span><span class="sxs-lookup"><span data-stu-id="040c6-271">The letter "A" (not case-sensitive)</span></span>
    
- <span data-ttu-id="040c6-272">Trois chiffres</span><span class="sxs-lookup"><span data-stu-id="040c6-272">Three digits</span></span>
    
- <span data-ttu-id="040c6-273">Une lettre ou un chiffre</span><span class="sxs-lookup"><span data-stu-id="040c6-273">One letter or one digit</span></span>
    
### <a name="checksum"></a><span data-ttu-id="040c6-274">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="040c6-274">Checksum</span></span>

<span data-ttu-id="040c6-275">Oui</span><span class="sxs-lookup"><span data-stu-id="040c6-275">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="040c6-276">Définition</span><span class="sxs-lookup"><span data-stu-id="040c6-276">Definition</span></span>

<span data-ttu-id="040c6-277">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="040c6-277">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="040c6-278">La fonction `Func_finland_eu_ssn_or_equivalent` trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="040c6-278">The function  `Func_finland_eu_ssn_or_equivalent` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="040c6-279">Un mot clé `Keywords_finland_eu_ssn_or_equivalent` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="040c6-279">A keyword from  `Keywords_finland_eu_ssn_or_equivalent` is found.</span></span> 
    
<span data-ttu-id="040c6-280">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="040c6-280">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="040c6-281">La fonction `Func_finland_eu_ssn_or_equivalent` trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="040c6-281">The function  `Func_finland_eu_ssn_or_equivalent` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="040c6-282">Mots clés</span><span class="sxs-lookup"><span data-stu-id="040c6-282">Keywords</span></span>

#### <a name="keywords_finland_eu_ssn_or_equivalent"></a><span data-ttu-id="040c6-283">Keywords_finland_eu_ssn_or_equivalent</span><span class="sxs-lookup"><span data-stu-id="040c6-283">Keywords_finland_eu_ssn_or_equivalent</span></span>

<span data-ttu-id="040c6-284">numéro d’identification</span><span class="sxs-lookup"><span data-stu-id="040c6-284">identification number</span></span>
  
<span data-ttu-id="040c6-285">ID personnel</span><span class="sxs-lookup"><span data-stu-id="040c6-285">personal id</span></span>
  
<span data-ttu-id="040c6-286">Numéro d’identité</span><span class="sxs-lookup"><span data-stu-id="040c6-286">identity number</span></span>
  
<span data-ttu-id="040c6-287">Numéro d’identification national finnois</span><span class="sxs-lookup"><span data-stu-id="040c6-287">finnish national id number</span></span>
  
<span data-ttu-id="040c6-288">personalidnumber #</span><span class="sxs-lookup"><span data-stu-id="040c6-288">personalidnumber#</span></span>
  
<span data-ttu-id="040c6-289">numéro d’identification nationale</span><span class="sxs-lookup"><span data-stu-id="040c6-289">national identification number</span></span>
  
<span data-ttu-id="040c6-290">Numéro d’identification</span><span class="sxs-lookup"><span data-stu-id="040c6-290">id number</span></span>
  
<span data-ttu-id="040c6-291">Numéro d’identification nationale</span><span class="sxs-lookup"><span data-stu-id="040c6-291">national id no.</span></span>
  
<span data-ttu-id="040c6-292">Numéro d’identification national</span><span class="sxs-lookup"><span data-stu-id="040c6-292">national id number</span></span>
  
<span data-ttu-id="040c6-293">n ° ID</span><span class="sxs-lookup"><span data-stu-id="040c6-293">id no</span></span>
  
<span data-ttu-id="040c6-294">tunnistenumero</span><span class="sxs-lookup"><span data-stu-id="040c6-294">tunnistenumero</span></span>
  
<span data-ttu-id="040c6-295">henkilötunnus</span><span class="sxs-lookup"><span data-stu-id="040c6-295">henkilötunnus</span></span>
  
<span data-ttu-id="040c6-296">yksilöllinen henkilökohtainen tunnistenumero</span><span class="sxs-lookup"><span data-stu-id="040c6-296">yksilöllinen henkilökohtainen tunnistenumero</span></span>
  
<span data-ttu-id="040c6-297">ainutlaatuinen henkilökohtainen tunnus</span><span class="sxs-lookup"><span data-stu-id="040c6-297">ainutlaatuinen henkilökohtainen tunnus</span></span>
  
<span data-ttu-id="040c6-298">identiteetti numérique</span><span class="sxs-lookup"><span data-stu-id="040c6-298">identiteetti numero</span></span>
  
<span data-ttu-id="040c6-299">suomen kansallinen henkilötunnus</span><span class="sxs-lookup"><span data-stu-id="040c6-299">suomen kansallinen henkilötunnus</span></span>
  
<span data-ttu-id="040c6-300">henkilötunnusnumero #</span><span class="sxs-lookup"><span data-stu-id="040c6-300">henkilötunnusnumero#</span></span>
  
<span data-ttu-id="040c6-301">kansallisen tunnistenumero</span><span class="sxs-lookup"><span data-stu-id="040c6-301">kansallisen tunnistenumero</span></span>
  
<span data-ttu-id="040c6-302">tunnusnumero</span><span class="sxs-lookup"><span data-stu-id="040c6-302">tunnusnumero</span></span>
  
<span data-ttu-id="040c6-303">Kansallinen tunnus numérique</span><span class="sxs-lookup"><span data-stu-id="040c6-303">kansallinen tunnus numero</span></span>
  
<span data-ttu-id="040c6-304">hetu</span><span class="sxs-lookup"><span data-stu-id="040c6-304">hetu</span></span>
  
## <a name="france"></a><span data-ttu-id="040c6-305">France</span><span class="sxs-lookup"><span data-stu-id="040c6-305">France</span></span>

<span data-ttu-id="040c6-306">Pour plus d’informations, reportez-vous à la section « France-numéro de sécurité sociale (INSEE) » dans [la recherche des types d’informations sensibles](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="040c6-306">For details, see the section "France Social Security Number (INSEE)" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="germany"></a><span data-ttu-id="040c6-307">Allemagne</span><span class="sxs-lookup"><span data-stu-id="040c6-307">Germany</span></span>

<span data-ttu-id="040c6-308">Pour plus d’informations, reportez-vous à la section « Germany Identity Card Number » dans les [types d’informations sensibles](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="040c6-308">For details, see the section "Germany Identity Card Number" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="greece"></a><span data-ttu-id="040c6-309">Grèce</span><span class="sxs-lookup"><span data-stu-id="040c6-309">Greece</span></span>

<span data-ttu-id="040c6-310">Pour plus d’informations, reportez-vous à la section « carte d’identité nationale Grèce » dans [ce que recherche les types d’informations sensibles](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="040c6-310">For details, see the section "Greece National ID Card" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="hungary"></a><span data-ttu-id="040c6-311">Hongrie</span><span class="sxs-lookup"><span data-stu-id="040c6-311">Hungary</span></span>

### <a name="format"></a><span data-ttu-id="040c6-312">Format</span><span class="sxs-lookup"><span data-stu-id="040c6-312">Format</span></span>

<span data-ttu-id="040c6-313">Neuf chiffres sans espaces ni délimiteurs</span><span class="sxs-lookup"><span data-stu-id="040c6-313">Nine digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="040c6-314">Modèle</span><span class="sxs-lookup"><span data-stu-id="040c6-314">Pattern</span></span>

<span data-ttu-id="040c6-315">Neuf chiffres</span><span class="sxs-lookup"><span data-stu-id="040c6-315">Nine digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="040c6-316">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="040c6-316">Checksum</span></span>

<span data-ttu-id="040c6-317">Oui</span><span class="sxs-lookup"><span data-stu-id="040c6-317">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="040c6-318">Définition</span><span class="sxs-lookup"><span data-stu-id="040c6-318">Definition</span></span>

<span data-ttu-id="040c6-319">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="040c6-319">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="040c6-320">La fonction `Func_hungary_eu_ssn_or_equivalent` trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="040c6-320">The function  `Func_hungary_eu_ssn_or_equivalent` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="040c6-321">Un mot clé `Keywords_hungary_eu_ssn_or_equivalent` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="040c6-321">A keyword from  `Keywords_hungary_eu_ssn_or_equivalent` is found.</span></span> 
    
<span data-ttu-id="040c6-322">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="040c6-322">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="040c6-323">La fonction `Func_hungary_eu_ssn_or_equivalent` trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="040c6-323">The function  `Func_hungary_eu_ssn_or_equivalent` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="040c6-324">Mots clés</span><span class="sxs-lookup"><span data-stu-id="040c6-324">Keywords</span></span>

#### <a name="keywords_hungary_eu_ssn_or_equivalent"></a><span data-ttu-id="040c6-325">Keywords_hungary_eu_ssn_or_equivalent</span><span class="sxs-lookup"><span data-stu-id="040c6-325">Keywords_hungary_eu_ssn_or_equivalent</span></span>

<span data-ttu-id="040c6-326">Numéro de sécurité sociale hongrois</span><span class="sxs-lookup"><span data-stu-id="040c6-326">hungarian social security number</span></span>
  
<span data-ttu-id="040c6-327">numéro de sécurité sociale</span><span class="sxs-lookup"><span data-stu-id="040c6-327">social security number</span></span>
  
<span data-ttu-id="040c6-328">socialsecuritynumber #</span><span class="sxs-lookup"><span data-stu-id="040c6-328">socialsecuritynumber#</span></span>
  
<span data-ttu-id="040c6-329">hssn #</span><span class="sxs-lookup"><span data-stu-id="040c6-329">hssn#</span></span>
  
<span data-ttu-id="040c6-330">socialsecuritynno</span><span class="sxs-lookup"><span data-stu-id="040c6-330">socialsecuritynno</span></span>
  
<span data-ttu-id="040c6-331">hssn</span><span class="sxs-lookup"><span data-stu-id="040c6-331">hssn</span></span>
  
<span data-ttu-id="040c6-332">taj</span><span class="sxs-lookup"><span data-stu-id="040c6-332">taj</span></span>
  
<span data-ttu-id="040c6-333">taj #</span><span class="sxs-lookup"><span data-stu-id="040c6-333">taj#</span></span>
  
<span data-ttu-id="040c6-334">SSN</span><span class="sxs-lookup"><span data-stu-id="040c6-334">ssn</span></span>
  
<span data-ttu-id="040c6-335">SSN #</span><span class="sxs-lookup"><span data-stu-id="040c6-335">ssn#</span></span>
  
<span data-ttu-id="040c6-336">Numéro de sécurité sociale</span><span class="sxs-lookup"><span data-stu-id="040c6-336">social security no</span></span>
  
<span data-ttu-id="040c6-337">áfa</span><span class="sxs-lookup"><span data-stu-id="040c6-337">áfa</span></span>
  
<span data-ttu-id="040c6-338">közösségi adószám</span><span class="sxs-lookup"><span data-stu-id="040c6-338">közösségi adószám</span></span>
  
<span data-ttu-id="040c6-339">általános forgalmi adó szám</span><span class="sxs-lookup"><span data-stu-id="040c6-339">általános forgalmi adó szám</span></span>
  
<span data-ttu-id="040c6-340">hozzáadottérték adó</span><span class="sxs-lookup"><span data-stu-id="040c6-340">hozzáadottérték adó</span></span>
  
<span data-ttu-id="040c6-341">áfa szám</span><span class="sxs-lookup"><span data-stu-id="040c6-341">áfa szám</span></span>
  
<span data-ttu-id="040c6-342">magyar áfa szám</span><span class="sxs-lookup"><span data-stu-id="040c6-342">magyar áfa szám</span></span>
  
## <a name="portugal"></a><span data-ttu-id="040c6-343">Portugal</span><span class="sxs-lookup"><span data-stu-id="040c6-343">Portugal</span></span>

<span data-ttu-id="040c6-344">Pour plus d’informations, reportez-vous à la section « numéro de carte de citoyen Portugal » dans [la recherche des types d’informations sensibles](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="040c6-344">For details, see the section "Portugal Citizen Card Number" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="spain"></a><span data-ttu-id="040c6-345">Espagne</span><span class="sxs-lookup"><span data-stu-id="040c6-345">Spain</span></span>

<span data-ttu-id="040c6-346">Pour plus d’informations, reportez-vous à la section « numéro de sécurité sociale Espagne » dans les [types d’informations sensibles](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="040c6-346">For details, see the section "Spain Social Security Number (SSN)" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="sweden"></a><span data-ttu-id="040c6-347">Suède</span><span class="sxs-lookup"><span data-stu-id="040c6-347">Sweden</span></span>

### <a name="format"></a><span data-ttu-id="040c6-348">Format</span><span class="sxs-lookup"><span data-stu-id="040c6-348">Format</span></span>

<span data-ttu-id="040c6-349">12 chiffres sans espaces ni délimiteurs</span><span class="sxs-lookup"><span data-stu-id="040c6-349">12 digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="040c6-350">Modèle</span><span class="sxs-lookup"><span data-stu-id="040c6-350">Pattern</span></span>

<span data-ttu-id="040c6-351">12 chiffres :</span><span class="sxs-lookup"><span data-stu-id="040c6-351">12 digits:</span></span>
  
-  <span data-ttu-id="040c6-352">Huit chiffres correspondant à la date de naissance (AAAAMMJJ)</span><span class="sxs-lookup"><span data-stu-id="040c6-352">Eight digits that correspond to the birth date (YYYYMMDD)</span></span> 
    
- <span data-ttu-id="040c6-353">Trois chiffres correspondant à un numéro de série où :</span><span class="sxs-lookup"><span data-stu-id="040c6-353">Three digits that correspond to a serial number where:</span></span> 
    
  - <span data-ttu-id="040c6-354">Le dernier chiffre du numéro de série indique sexe par l’affectation d’un nombre impair pour le mâle et d’un nombre pair pour femelle.</span><span class="sxs-lookup"><span data-stu-id="040c6-354">The last digit in the serial number indicates gender by the assignment of an odd number for male and an even number for female</span></span>
    
  - <span data-ttu-id="040c6-355">Jusqu’à 1990, l’affectation du numéro de série correspond au comté où le porteur du numéro est né ou (en naissance avant 1947) où il a été vivant, en fonction des enregistrements fiscaux, le 1er janvier 1947, avec un code spécial (généralement 9 comme le 7 chiffres) pour immigrants</span><span class="sxs-lookup"><span data-stu-id="040c6-355">Up to 1990, the assignment of serial number corresponded to the county where the bearer of the number was born or (if born before 1947) where he/she had been living, according to tax records, on January 1, 1947, with a special code (usually 9 as the 7th digit) for immigrants</span></span> 
    
- <span data-ttu-id="040c6-356">Un chiffre de contrôle</span><span class="sxs-lookup"><span data-stu-id="040c6-356">One check digit</span></span>
    
### <a name="checksum"></a><span data-ttu-id="040c6-357">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="040c6-357">Checksum</span></span>

<span data-ttu-id="040c6-358">Oui</span><span class="sxs-lookup"><span data-stu-id="040c6-358">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="040c6-359">Définition</span><span class="sxs-lookup"><span data-stu-id="040c6-359">Definition</span></span>

<span data-ttu-id="040c6-360">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="040c6-360">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="040c6-361">La fonction `Func_sweden_eu_ssn_or_equivalent` trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="040c6-361">The function  `Func_sweden_eu_ssn_or_equivalent` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="040c6-362">Un mot clé `Keywords_sweden_eu_ssn_or_equivalent` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="040c6-362">A keyword from  `Keywords_sweden_eu_ssn_or_equivalent` is found.</span></span> 
    
<span data-ttu-id="040c6-363">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="040c6-363">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="040c6-364">La fonction `Func_sweden_eu_ssn_or_equivalent` trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="040c6-364">The function  `Func_sweden_eu_ssn_or_equivalent` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="040c6-365">Mots clés</span><span class="sxs-lookup"><span data-stu-id="040c6-365">Keywords</span></span>

#### <a name="keywords_sweden_eu_ssn_or_equivalent"></a><span data-ttu-id="040c6-366">Keywords_sweden_eu_ssn_or_equivalent</span><span class="sxs-lookup"><span data-stu-id="040c6-366">Keywords_sweden_eu_ssn_or_equivalent</span></span>

<span data-ttu-id="040c6-367">Numéro d’identification personnel</span><span class="sxs-lookup"><span data-stu-id="040c6-367">personal id number</span></span>
  
<span data-ttu-id="040c6-368">numéro d’identification</span><span class="sxs-lookup"><span data-stu-id="040c6-368">identification number</span></span>
  
<span data-ttu-id="040c6-369">Numéro d’identification personnel</span><span class="sxs-lookup"><span data-stu-id="040c6-369">personal id no</span></span>
  
<span data-ttu-id="040c6-370">n ° d’identité</span><span class="sxs-lookup"><span data-stu-id="040c6-370">identity no</span></span>
  
<span data-ttu-id="040c6-371">Numéro d’identification</span><span class="sxs-lookup"><span data-stu-id="040c6-371">identification no</span></span>
  
<span data-ttu-id="040c6-372">Numéro d’identification personnel</span><span class="sxs-lookup"><span data-stu-id="040c6-372">personal identification no</span></span>
  
<span data-ttu-id="040c6-373">ID personnummer</span><span class="sxs-lookup"><span data-stu-id="040c6-373">personnummer id</span></span>
  
<span data-ttu-id="040c6-374">ID personligt-Nummer</span><span class="sxs-lookup"><span data-stu-id="040c6-374">personligt id-nummer</span></span>
  
<span data-ttu-id="040c6-375">ID unikt-Nummer</span><span class="sxs-lookup"><span data-stu-id="040c6-375">unikt id-nummer</span></span>
  
<span data-ttu-id="040c6-376">personnummer</span><span class="sxs-lookup"><span data-stu-id="040c6-376">personnummer</span></span>
  
<span data-ttu-id="040c6-377">identifikationsnumret</span><span class="sxs-lookup"><span data-stu-id="040c6-377">identifikationsnumret</span></span>
  
<span data-ttu-id="040c6-378">personnummer #</span><span class="sxs-lookup"><span data-stu-id="040c6-378">personnummer#</span></span>
  
<span data-ttu-id="040c6-379">identifikationsnumret #</span><span class="sxs-lookup"><span data-stu-id="040c6-379">identifikationsnumret#</span></span>
  
## <a name="see-also"></a><span data-ttu-id="040c6-380">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="040c6-380">See also</span></span>

[<span data-ttu-id="040c6-381">Éléments recherchés par les types d’informations sensibles</span><span class="sxs-lookup"><span data-stu-id="040c6-381">What the sensitive information types look for</span></span>](what-the-sensitive-information-types-look-for.md)

