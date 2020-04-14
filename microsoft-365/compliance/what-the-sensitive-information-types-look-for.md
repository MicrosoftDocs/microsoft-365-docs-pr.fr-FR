---
title: Éléments recherchés par les types d’informations sensibles
f1.keywords:
- CSH
ms.author: chrfox
author: chrfox
manager: laurawi
ms.date: ''
audience: Admin
search.appverid: MET150
ms.topic: reference
f1_keywords:
- ms.o365.cc.UnifiedDLPRuleContainsSensitiveInformation
ms.service: O365-seccomp
localization_priority: Normal
ms.collection:
- M365-security-compliance
description: La protection contre la perte de données (DLP) dans &amp; le centre de sécurité conformité d’Office 365 inclut 80 types d’informations sensibles que vous pouvez utiliser dans vos stratégies DLP. Cette rubrique répertorie tous ces types d'informations sensibles et indique ce qu'une stratégie DLP recherche pour chaque type.
ms.openlocfilehash: aa3a08961ccad92c9986db16c1d8180d9b0cd17e
ms.sourcegitcommit: 4ddbc1c3c29d79d3c4640b7b32f95576784efcca
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/13/2020
ms.locfileid: "43240280"
---
# <a name="what-the-sensitive-information-types-look-for"></a><span data-ttu-id="32d8c-104">Éléments recherchés par les types d’informations sensibles</span><span class="sxs-lookup"><span data-stu-id="32d8c-104">What the sensitive information types look for</span></span>

<span data-ttu-id="32d8c-105">La protection contre la perte de données (DLP) dans &amp; le centre de sécurité conformité Office 365 inclut de nombreux types d’informations sensibles que vous pouvez utiliser dans vos stratégies DLP.</span><span class="sxs-lookup"><span data-stu-id="32d8c-105">Data loss prevention (DLP) in the Office 365 Security &amp; Compliance Center includes many sensitive information types that are ready for you to use in your DLP policies.</span></span> <span data-ttu-id="32d8c-106">Cette rubrique répertorie tous ces types d'informations sensibles et indique ce qu'une stratégie DLP recherche pour chaque type.</span><span class="sxs-lookup"><span data-stu-id="32d8c-106">This topic lists all of these sensitive information types and shows what a DLP policy looks for when it detects each type.</span></span> <span data-ttu-id="32d8c-107">Un type d'informations sensibles est défini par un modèle qui peut être identifié par une fonction ou une expression régulière.</span><span class="sxs-lookup"><span data-stu-id="32d8c-107">A sensitive information type is defined by a pattern that can be identified by a regular expression or a function.</span></span> <span data-ttu-id="32d8c-108">En outre, des preuves corroborantes comme les mots clés et les sommes de contrôle peuvent être utilisées pour identifier un type d'informations sensibles.</span><span class="sxs-lookup"><span data-stu-id="32d8c-108">In addition, corroborative evidence such as keywords and checksums can be used to identify a sensitive information type.</span></span> <span data-ttu-id="32d8c-109">Le niveau de confiance et la proximité sont également utilisés dans le processus d’évaluation.</span><span class="sxs-lookup"><span data-stu-id="32d8c-109">Confidence level and proximity are also used in the evaluation process.</span></span>
  
## <a name="aba-routing-number"></a><span data-ttu-id="32d8c-110">Numéro de routage ABA</span><span class="sxs-lookup"><span data-stu-id="32d8c-110">ABA Routing Number</span></span>

### <a name="format"></a><span data-ttu-id="32d8c-111">Format</span><span class="sxs-lookup"><span data-stu-id="32d8c-111">Format</span></span>

<span data-ttu-id="32d8c-112">9 chiffres mis en forme ou non mis en forme</span><span class="sxs-lookup"><span data-stu-id="32d8c-112">9 digits which may be in a formatted or unformatted pattern</span></span>

### <a name="pattern"></a><span data-ttu-id="32d8c-113">Modèle</span><span class="sxs-lookup"><span data-stu-id="32d8c-113">Pattern</span></span>

<span data-ttu-id="32d8c-114">Avec</span><span class="sxs-lookup"><span data-stu-id="32d8c-114">Formatted:</span></span>
- <span data-ttu-id="32d8c-115">Quatre chiffres commençant par 0, 1, 2, 3, 6, 7 ou 8</span><span class="sxs-lookup"><span data-stu-id="32d8c-115">Four digits beginning with 0, 1, 2, 3, 6, 7, or 8</span></span>
- <span data-ttu-id="32d8c-116">Un trait d’union </span><span class="sxs-lookup"><span data-stu-id="32d8c-116">A hyphen</span></span>
- <span data-ttu-id="32d8c-117">Quatre chiffres</span><span class="sxs-lookup"><span data-stu-id="32d8c-117">Four digits</span></span>
- <span data-ttu-id="32d8c-118">Un trait d’union </span><span class="sxs-lookup"><span data-stu-id="32d8c-118">A hyphen</span></span>
- <span data-ttu-id="32d8c-119">Un chiffre</span><span class="sxs-lookup"><span data-stu-id="32d8c-119">A digit</span></span>

<span data-ttu-id="32d8c-120">Non mis en forme : 9 chiffres consécutifs commençant par 0, 1, 2, 3, 6, 7 ou 8</span><span class="sxs-lookup"><span data-stu-id="32d8c-120">Unformatted: 9 consecutive digits beginning with 0, 1, 2, 3, 6, 7, or 8</span></span> 

### <a name="checksum"></a><span data-ttu-id="32d8c-121">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="32d8c-121">Checksum</span></span>

<span data-ttu-id="32d8c-122">Non</span><span class="sxs-lookup"><span data-stu-id="32d8c-122">No</span></span>

### <a name="definition"></a><span data-ttu-id="32d8c-123">Définition</span><span class="sxs-lookup"><span data-stu-id="32d8c-123">Definition</span></span>

<span data-ttu-id="32d8c-124">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="32d8c-124">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="32d8c-125">La fonction Func_aba_routing trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="32d8c-125">The function Func_aba_routing finds content that matches the pattern.</span></span>
- <span data-ttu-id="32d8c-126">Un mot clé figurant dans la liste Keyword_ABA_Routing est trouvé.</span><span class="sxs-lookup"><span data-stu-id="32d8c-126">A keyword from Keyword_ABA_Routing is found.</span></span>

```xml
<!-- ABA Routing Number -->
<Entity id="cb353f78-2b72-4c3c-8827-92ebe4f69fdf" patternsProximity="300" recommendedConfidence="75">
      <Pattern confidenceLevel="75">
        <IdMatch idRef="Func_aba_routing" />
        <Match idRef="Keyword_ABA_Routing" />
      </Pattern>
 </Entity>
```


### <a name="keywords"></a><span data-ttu-id="32d8c-127">Mots clés</span><span class="sxs-lookup"><span data-stu-id="32d8c-127">Keywords</span></span>

#### <a name="keyword_aba_routing"></a><span data-ttu-id="32d8c-128">Keyword_ABA_Routing</span><span class="sxs-lookup"><span data-stu-id="32d8c-128">Keyword_ABA_Routing</span></span>

- <span data-ttu-id="32d8c-129">ABA</span><span class="sxs-lookup"><span data-stu-id="32d8c-129">aba</span></span>
- <span data-ttu-id="32d8c-130"># aba</span><span class="sxs-lookup"><span data-stu-id="32d8c-130">aba #</span></span>
- <span data-ttu-id="32d8c-131"># routage aba</span><span class="sxs-lookup"><span data-stu-id="32d8c-131">aba routing #</span></span>
- <span data-ttu-id="32d8c-132">numéro de routage aba</span><span class="sxs-lookup"><span data-stu-id="32d8c-132">aba routing number</span></span>
- <span data-ttu-id="32d8c-133">ABA #</span><span class="sxs-lookup"><span data-stu-id="32d8c-133">aba#</span></span>
- <span data-ttu-id="32d8c-134">abarouting #</span><span class="sxs-lookup"><span data-stu-id="32d8c-134">abarouting#</span></span>
- <span data-ttu-id="32d8c-135">numéro aba</span><span class="sxs-lookup"><span data-stu-id="32d8c-135">aba number</span></span>
- <span data-ttu-id="32d8c-136">abaroutingnumber</span><span class="sxs-lookup"><span data-stu-id="32d8c-136">abaroutingnumber</span></span>
- <span data-ttu-id="32d8c-137"># routage american bank association</span><span class="sxs-lookup"><span data-stu-id="32d8c-137">american bank association routing #</span></span>
- <span data-ttu-id="32d8c-138">numéro de routage american bank association</span><span class="sxs-lookup"><span data-stu-id="32d8c-138">american bank association routing number</span></span>
- <span data-ttu-id="32d8c-139">americanbankassociationrouting #</span><span class="sxs-lookup"><span data-stu-id="32d8c-139">americanbankassociationrouting#</span></span>
- <span data-ttu-id="32d8c-140">americanbankassociationroutingnumber</span><span class="sxs-lookup"><span data-stu-id="32d8c-140">americanbankassociationroutingnumber</span></span>
- <span data-ttu-id="32d8c-141">numéro de routage bancaire</span><span class="sxs-lookup"><span data-stu-id="32d8c-141">bank routing number</span></span>
- <span data-ttu-id="32d8c-142">bankrouting #</span><span class="sxs-lookup"><span data-stu-id="32d8c-142">bankrouting#</span></span>
- <span data-ttu-id="32d8c-143">bankroutingnumber</span><span class="sxs-lookup"><span data-stu-id="32d8c-143">bankroutingnumber</span></span>
- <span data-ttu-id="32d8c-144">numéro de routage</span><span class="sxs-lookup"><span data-stu-id="32d8c-144">routing transit number</span></span>
- <span data-ttu-id="32d8c-145">RTN</span><span class="sxs-lookup"><span data-stu-id="32d8c-145">RTN</span></span> 
   
## <a name="argentina-national-identity-dni-number"></a><span data-ttu-id="32d8c-146">Numéro d’identité nationale (DNI) pour l’Argentine</span><span class="sxs-lookup"><span data-stu-id="32d8c-146">Argentina National Identity (DNI) Number</span></span>

### <a name="format"></a><span data-ttu-id="32d8c-147">Format</span><span class="sxs-lookup"><span data-stu-id="32d8c-147">Format</span></span>

<span data-ttu-id="32d8c-148">Huit chiffres séparés par des points</span><span class="sxs-lookup"><span data-stu-id="32d8c-148">Eight digits separated by periods</span></span>

### <a name="pattern"></a><span data-ttu-id="32d8c-149">Modèle</span><span class="sxs-lookup"><span data-stu-id="32d8c-149">Pattern</span></span>

<span data-ttu-id="32d8c-150">Huit chiffres :</span><span class="sxs-lookup"><span data-stu-id="32d8c-150">Eight digits:</span></span>
- <span data-ttu-id="32d8c-151">Deux chiffres</span><span class="sxs-lookup"><span data-stu-id="32d8c-151">Two digits</span></span>
- <span data-ttu-id="32d8c-152">Un point </span><span class="sxs-lookup"><span data-stu-id="32d8c-152">A period</span></span>
- <span data-ttu-id="32d8c-153">Trois chiffres </span><span class="sxs-lookup"><span data-stu-id="32d8c-153">Three digits</span></span>
- <span data-ttu-id="32d8c-154">Un point </span><span class="sxs-lookup"><span data-stu-id="32d8c-154">A period</span></span>
- <span data-ttu-id="32d8c-155">Trois chiffres </span><span class="sxs-lookup"><span data-stu-id="32d8c-155">Three digits</span></span>

### <a name="checksum"></a><span data-ttu-id="32d8c-156">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="32d8c-156">Checksum</span></span>

<span data-ttu-id="32d8c-157">Non</span><span class="sxs-lookup"><span data-stu-id="32d8c-157">No</span></span>

### <a name="definition"></a><span data-ttu-id="32d8c-158">Définition</span><span class="sxs-lookup"><span data-stu-id="32d8c-158">Definition</span></span>

<span data-ttu-id="32d8c-159">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="32d8c-159">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="32d8c-160">L’expression régulière Regex_argentina_national_id trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="32d8c-160">The regular expression Regex_argentina_national_id finds content that matches the pattern.</span></span>
- <span data-ttu-id="32d8c-161">Un mot clé figurant dans la liste Keyword_argentina_national_id est trouvé.</span><span class="sxs-lookup"><span data-stu-id="32d8c-161">A keyword from Keyword_argentina_national_id is found.</span></span>

```xml
<!-- Argentina National Identity (DNI) Number -->
<Entity id="eefbb00e-8282-433c-8620-8f1da3bffdb2" recommendedConfidence="75" patternsProximity="300">
   <Pattern confidenceLevel="75">
      <IdMatch idRef="Regex_argentina_national_id"/>
      <Match idRef="Keyword_argentina_national_id"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="32d8c-162">Mots clés</span><span class="sxs-lookup"><span data-stu-id="32d8c-162">Keywords</span></span>

#### <a name="keyword_argentina_national_id"></a><span data-ttu-id="32d8c-163">Keyword_argentina_national_id</span><span class="sxs-lookup"><span data-stu-id="32d8c-163">Keyword_argentina_national_id</span></span>

- <span data-ttu-id="32d8c-164">Argentina National Identity number</span><span class="sxs-lookup"><span data-stu-id="32d8c-164">Argentina National Identity number</span></span> 
- <span data-ttu-id="32d8c-165">Identité</span><span class="sxs-lookup"><span data-stu-id="32d8c-165">Identity</span></span> 
- <span data-ttu-id="32d8c-166">Identification de la carte d’identité nationale</span><span class="sxs-lookup"><span data-stu-id="32d8c-166">Identification National Identity Card</span></span> 
- <span data-ttu-id="32d8c-167">DNI</span><span class="sxs-lookup"><span data-stu-id="32d8c-167">DNI</span></span> 
- <span data-ttu-id="32d8c-168">Carte d’interface réseau nationale du registre des personnes</span><span class="sxs-lookup"><span data-stu-id="32d8c-168">NIC National Registry of Persons</span></span> 
- <span data-ttu-id="32d8c-169">Documento Nacional de Identidad</span><span class="sxs-lookup"><span data-stu-id="32d8c-169">Documento Nacional de Identidad</span></span> 
- <span data-ttu-id="32d8c-170">Registro Nacional de las Personas</span><span class="sxs-lookup"><span data-stu-id="32d8c-170">Registro Nacional de las Personas</span></span> 
- <span data-ttu-id="32d8c-171">Identidad</span><span class="sxs-lookup"><span data-stu-id="32d8c-171">Identidad</span></span> 
- <span data-ttu-id="32d8c-172">Identificación</span><span class="sxs-lookup"><span data-stu-id="32d8c-172">Identificación</span></span> 
   
## <a name="australia-bank-account-number"></a><span data-ttu-id="32d8c-173">Numéro de compte bancaire Australie</span><span class="sxs-lookup"><span data-stu-id="32d8c-173">Australia Bank Account Number</span></span>

### <a name="format"></a><span data-ttu-id="32d8c-174">Format</span><span class="sxs-lookup"><span data-stu-id="32d8c-174">Format</span></span>

<span data-ttu-id="32d8c-175">6 à 10 chiffres avec ou sans le numéro d’agence bancaire de l’État</span><span class="sxs-lookup"><span data-stu-id="32d8c-175">6-10 digits with or without a bank state branch number</span></span>

### <a name="pattern"></a><span data-ttu-id="32d8c-176">Modèle</span><span class="sxs-lookup"><span data-stu-id="32d8c-176">Pattern</span></span>

<span data-ttu-id="32d8c-177">Le numéro de compte est composé de 6 à 10 chiffres.</span><span class="sxs-lookup"><span data-stu-id="32d8c-177">Account number is 6-10 digits.</span></span>
<span data-ttu-id="32d8c-178">Numéro de succursale bancaire en Australie :</span><span class="sxs-lookup"><span data-stu-id="32d8c-178">Australia bank state branch number:</span></span>
- <span data-ttu-id="32d8c-179">Trois chiffres</span><span class="sxs-lookup"><span data-stu-id="32d8c-179">Three digits</span></span> 
- <span data-ttu-id="32d8c-180">Un trait d’union</span><span class="sxs-lookup"><span data-stu-id="32d8c-180">A hyphen</span></span> 
- <span data-ttu-id="32d8c-181">Trois chiffres</span><span class="sxs-lookup"><span data-stu-id="32d8c-181">Three digits</span></span>

### <a name="checksum"></a><span data-ttu-id="32d8c-182">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="32d8c-182">Checksum</span></span>

<span data-ttu-id="32d8c-183">Non</span><span class="sxs-lookup"><span data-stu-id="32d8c-183">No</span></span>

### <a name="definition"></a><span data-ttu-id="32d8c-184">Définition</span><span class="sxs-lookup"><span data-stu-id="32d8c-184">Definition</span></span>

<span data-ttu-id="32d8c-185">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="32d8c-185">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="32d8c-186">L’expression régulière Regex_australia_bank_account_number trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="32d8c-186">The regular expression Regex_australia_bank_account_number finds content that matches the pattern..</span></span>
- <span data-ttu-id="32d8c-187">Un mot clé figurant dans la liste Keyword_australia_bank_account_number est trouvé.</span><span class="sxs-lookup"><span data-stu-id="32d8c-187">A keyword from Keyword_australia_bank_account_number is found.</span></span>
- <span data-ttu-id="32d8c-188">L’expression régulière Regex_australia_bank_account_number_bsb trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="32d8c-188">The regular expression Regex_australia_bank_account_number_bsb finds content that matches the pattern.</span></span>

<span data-ttu-id="32d8c-189">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="32d8c-189">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="32d8c-190">L’expression régulière Regex_australia_bank_account_number trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="32d8c-190">The regular expression Regex_australia_bank_account_number finds content that matches the pattern..</span></span>
- <span data-ttu-id="32d8c-191">Un mot clé figurant dans la liste Keyword_australia_bank_account_number est trouvé.</span><span class="sxs-lookup"><span data-stu-id="32d8c-191">A keyword from Keyword_australia_bank_account_number is found.</span></span>

```xml
<!-- Australia Bank Account Number -->
<Entity id="74a54de9-2a30-4aa0-a8aa-3d9327fc07c7" patternsProximity="300" recommendedConfidence="75">
  <Pattern confidenceLevel="85">
        <IdMatch idRef="Regex_australia_bank_account_number" />
        <Match idRef="Keyword_australia_bank_account_number" />
        <Match idRef="Regex_australia_bank_account_number_bsb" />
  </Pattern>
  <Pattern confidenceLevel="75">
        <IdMatch idRef="Regex_australia_bank_account_number" />
        <Match idRef="Keyword_australia_bank_account_number" />
  </Pattern>
 </Entity>
```

### <a name="keywords"></a><span data-ttu-id="32d8c-192">Mots clés</span><span class="sxs-lookup"><span data-stu-id="32d8c-192">Keywords</span></span>

#### <a name="keyword_australia_bank_account_number"></a><span data-ttu-id="32d8c-193">Keyword_australia_bank_account_number</span><span class="sxs-lookup"><span data-stu-id="32d8c-193">Keyword_australia_bank_account_number</span></span>

- <span data-ttu-id="32d8c-194">code swift banque</span><span class="sxs-lookup"><span data-stu-id="32d8c-194">swift bank code</span></span>
- <span data-ttu-id="32d8c-195">banque correspondante</span><span class="sxs-lookup"><span data-stu-id="32d8c-195">correspondent bank</span></span>
- <span data-ttu-id="32d8c-196">devise de base</span><span class="sxs-lookup"><span data-stu-id="32d8c-196">base currency</span></span>
- <span data-ttu-id="32d8c-197">compte aux États-Unis</span><span class="sxs-lookup"><span data-stu-id="32d8c-197">usa account</span></span>
- <span data-ttu-id="32d8c-198">adresse du titulaire</span><span class="sxs-lookup"><span data-stu-id="32d8c-198">holder address</span></span>
- <span data-ttu-id="32d8c-199">adresse de la banque</span><span class="sxs-lookup"><span data-stu-id="32d8c-199">bank address</span></span>
- <span data-ttu-id="32d8c-200">informations du compte</span><span class="sxs-lookup"><span data-stu-id="32d8c-200">information account</span></span>
- <span data-ttu-id="32d8c-201">transferts de fonds</span><span class="sxs-lookup"><span data-stu-id="32d8c-201">fund transfers</span></span>
- <span data-ttu-id="32d8c-202">frais bancaires</span><span class="sxs-lookup"><span data-stu-id="32d8c-202">bank charges</span></span>
- <span data-ttu-id="32d8c-203">informations sur la banque</span><span class="sxs-lookup"><span data-stu-id="32d8c-203">bank details</span></span>
- <span data-ttu-id="32d8c-204">informations bancaires</span><span class="sxs-lookup"><span data-stu-id="32d8c-204">banking information</span></span>
- <span data-ttu-id="32d8c-205">noms complets</span><span class="sxs-lookup"><span data-stu-id="32d8c-205">full names</span></span>
- <span data-ttu-id="32d8c-206">auront</span><span class="sxs-lookup"><span data-stu-id="32d8c-206">iaea</span></span>

   
## <a name="australia-drivers-license-number"></a><span data-ttu-id="32d8c-207">Numéro de permis de conduire Australie</span><span class="sxs-lookup"><span data-stu-id="32d8c-207">Australia Driver's License Number</span></span>

### <a name="format"></a><span data-ttu-id="32d8c-208">Format</span><span class="sxs-lookup"><span data-stu-id="32d8c-208">Format</span></span>

<span data-ttu-id="32d8c-209">Neuf lettres et chiffres</span><span class="sxs-lookup"><span data-stu-id="32d8c-209">Nine letters and digits</span></span>

### <a name="pattern"></a><span data-ttu-id="32d8c-210">Modèle</span><span class="sxs-lookup"><span data-stu-id="32d8c-210">Pattern</span></span>

<span data-ttu-id="32d8c-211">Neuf lettres et chiffres :</span><span class="sxs-lookup"><span data-stu-id="32d8c-211">Nine letters and digits:</span></span> 

- <span data-ttu-id="32d8c-212">Deux chiffres ou lettres (ne respectent pas la casse)</span><span class="sxs-lookup"><span data-stu-id="32d8c-212">Two digits or letters (not case sensitive)</span></span> 
- <span data-ttu-id="32d8c-213">Deux chiffres</span><span class="sxs-lookup"><span data-stu-id="32d8c-213">Two digits</span></span> 
- <span data-ttu-id="32d8c-214">Cinq chiffres ou lettres (ne respectent pas la casse)</span><span class="sxs-lookup"><span data-stu-id="32d8c-214">Five digits or letters (not case sensitive)</span></span>

<span data-ttu-id="32d8c-215">OR</span><span class="sxs-lookup"><span data-stu-id="32d8c-215">OR</span></span>

- <span data-ttu-id="32d8c-216">1 ou 2 lettres facultatives (ne respectant pas la casse) </span><span class="sxs-lookup"><span data-stu-id="32d8c-216">1-2 optional letters (not case sensitive)</span></span> 
- <span data-ttu-id="32d8c-217">4 à 9 chiffres</span><span class="sxs-lookup"><span data-stu-id="32d8c-217">4-9 digits</span></span>

<span data-ttu-id="32d8c-218">OR</span><span class="sxs-lookup"><span data-stu-id="32d8c-218">OR</span></span>

- <span data-ttu-id="32d8c-219">Neuf chiffres ou lettres (ne respectant pas la casse)</span><span class="sxs-lookup"><span data-stu-id="32d8c-219">Nine digits or letters (not case sensitive)</span></span>

### <a name="checksum"></a><span data-ttu-id="32d8c-220">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="32d8c-220">Checksum</span></span>

<span data-ttu-id="32d8c-221">Non</span><span class="sxs-lookup"><span data-stu-id="32d8c-221">No</span></span>

### <a name="definition"></a><span data-ttu-id="32d8c-222">Définition</span><span class="sxs-lookup"><span data-stu-id="32d8c-222">Definition</span></span>

<span data-ttu-id="32d8c-223">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="32d8c-223">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="32d8c-224">L’expression régulière Regex_australia_drivers_license_number trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="32d8c-224">The regular expression Regex_australia_drivers_license_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="32d8c-225">Un mot clé figurant dans la liste Keyword_australia_drivers_license_number est trouvé.</span><span class="sxs-lookup"><span data-stu-id="32d8c-225">A keyword from Keyword_australia_drivers_license_number is found.</span></span>
- <span data-ttu-id="32d8c-226">Aucun mot clé figurant dans la liste Keyword_australia_drivers_license_number_exclusions n’est trouvé.</span><span class="sxs-lookup"><span data-stu-id="32d8c-226">No keyword from Keyword_australia_drivers_license_number_exclusions is found.</span></span>

```xml
<!-- Australia Drivers License Number -->
<Entity id="1cbbc8f5-9216-4392-9eb5-5ac2298d1356" patternsProximity="300" recommendedConfidence="75">
   <Pattern confidenceLevel="75">
        <IdMatch idRef="Regex_australia_drivers_license_number" />
        <Match idRef="Keyword_australia_drivers_license_number" />
        <Any minMatches="0" maxMatches="0">
          <Match idRef="Keyword_australia_drivers_license_number_exclusions" />
        </Any>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="32d8c-227">Mots clés</span><span class="sxs-lookup"><span data-stu-id="32d8c-227">Keywords</span></span>

#### <a name="keyword_australia_drivers_license_number"></a><span data-ttu-id="32d8c-228">Keyword_australia_drivers_license_number</span><span class="sxs-lookup"><span data-stu-id="32d8c-228">Keyword_australia_drivers_license_number</span></span>

- <span data-ttu-id="32d8c-229">permis de conduite internationaux</span><span class="sxs-lookup"><span data-stu-id="32d8c-229">international driving permits</span></span>
- <span data-ttu-id="32d8c-230">australian automobile association</span><span class="sxs-lookup"><span data-stu-id="32d8c-230">australian automobile association</span></span>
- <span data-ttu-id="32d8c-231">permis de conduite international</span><span class="sxs-lookup"><span data-stu-id="32d8c-231">international driving permit</span></span>
- <span data-ttu-id="32d8c-232">DriverLicence</span><span class="sxs-lookup"><span data-stu-id="32d8c-232">DriverLicence</span></span>
- <span data-ttu-id="32d8c-233">DriverLicences</span><span class="sxs-lookup"><span data-stu-id="32d8c-233">DriverLicences</span></span>
- <span data-ttu-id="32d8c-234">Permis conduire</span><span class="sxs-lookup"><span data-stu-id="32d8c-234">Driver Lic</span></span>
- <span data-ttu-id="32d8c-235">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="32d8c-235">Driver Licence</span></span>
- <span data-ttu-id="32d8c-236">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="32d8c-236">Driver Licences</span></span>
- <span data-ttu-id="32d8c-237">DriversLic</span><span class="sxs-lookup"><span data-stu-id="32d8c-237">DriversLic</span></span>
- <span data-ttu-id="32d8c-238">DriversLicence</span><span class="sxs-lookup"><span data-stu-id="32d8c-238">DriversLicence</span></span>
- <span data-ttu-id="32d8c-239">DriversLicences</span><span class="sxs-lookup"><span data-stu-id="32d8c-239">DriversLicences</span></span>
- <span data-ttu-id="32d8c-240">Permis conduire</span><span class="sxs-lookup"><span data-stu-id="32d8c-240">Drivers Lic</span></span>
- <span data-ttu-id="32d8c-241">Permis conduire</span><span class="sxs-lookup"><span data-stu-id="32d8c-241">Drivers Lics</span></span>
- <span data-ttu-id="32d8c-242">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="32d8c-242">Drivers Licence</span></span>
- <span data-ttu-id="32d8c-243">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="32d8c-243">Drivers Licences</span></span>
- <span data-ttu-id="32d8c-244">Driver'Lic</span><span class="sxs-lookup"><span data-stu-id="32d8c-244">Driver'Lic</span></span>
- <span data-ttu-id="32d8c-245">Driver'Lics</span><span class="sxs-lookup"><span data-stu-id="32d8c-245">Driver'Lics</span></span>
- <span data-ttu-id="32d8c-246">Driver'Licence</span><span class="sxs-lookup"><span data-stu-id="32d8c-246">Driver'Licence</span></span>
- <span data-ttu-id="32d8c-247">Driver'Licences</span><span class="sxs-lookup"><span data-stu-id="32d8c-247">Driver'Licences</span></span>
- <span data-ttu-id="32d8c-248">Permis conduire</span><span class="sxs-lookup"><span data-stu-id="32d8c-248">Driver' Lic</span></span>
- <span data-ttu-id="32d8c-249">Permis conduire</span><span class="sxs-lookup"><span data-stu-id="32d8c-249">Driver' Lics</span></span>
- <span data-ttu-id="32d8c-250">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="32d8c-250">Driver' Licence</span></span>
- <span data-ttu-id="32d8c-251">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="32d8c-251">Driver' Licences</span></span>
- <span data-ttu-id="32d8c-252">Driver'sLic</span><span class="sxs-lookup"><span data-stu-id="32d8c-252">Driver'sLic</span></span>
- <span data-ttu-id="32d8c-253">Driver'sLics</span><span class="sxs-lookup"><span data-stu-id="32d8c-253">Driver'sLics</span></span>
- <span data-ttu-id="32d8c-254">Driver'sLicence</span><span class="sxs-lookup"><span data-stu-id="32d8c-254">Driver'sLicence</span></span>
- <span data-ttu-id="32d8c-255">Driver'sLicences</span><span class="sxs-lookup"><span data-stu-id="32d8c-255">Driver'sLicences</span></span>
- <span data-ttu-id="32d8c-256">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="32d8c-256">Driver's Lic</span></span>
- <span data-ttu-id="32d8c-257">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="32d8c-257">Driver's Lics</span></span>
- <span data-ttu-id="32d8c-258">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="32d8c-258">Driver's Licence</span></span>
- <span data-ttu-id="32d8c-259">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="32d8c-259">Driver's Licences</span></span>
- <span data-ttu-id="32d8c-260">DriverLic #</span><span class="sxs-lookup"><span data-stu-id="32d8c-260">DriverLic#</span></span>
- <span data-ttu-id="32d8c-261">DriverLics #</span><span class="sxs-lookup"><span data-stu-id="32d8c-261">DriverLics#</span></span>
- <span data-ttu-id="32d8c-262">DriverLicence #</span><span class="sxs-lookup"><span data-stu-id="32d8c-262">DriverLicence#</span></span>
- <span data-ttu-id="32d8c-263">DriverLicences #</span><span class="sxs-lookup"><span data-stu-id="32d8c-263">DriverLicences#</span></span>
- <span data-ttu-id="32d8c-264">#Permis conduire</span><span class="sxs-lookup"><span data-stu-id="32d8c-264">Driver Lic#</span></span>
- <span data-ttu-id="32d8c-265">#Permis conduire</span><span class="sxs-lookup"><span data-stu-id="32d8c-265">Driver Lics#</span></span>
- <span data-ttu-id="32d8c-266">#Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="32d8c-266">Driver Licence#</span></span>
- <span data-ttu-id="32d8c-267">#Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="32d8c-267">Driver Licences#</span></span>
- <span data-ttu-id="32d8c-268">DriversLic #</span><span class="sxs-lookup"><span data-stu-id="32d8c-268">DriversLic#</span></span>
- <span data-ttu-id="32d8c-269">DriversLics #</span><span class="sxs-lookup"><span data-stu-id="32d8c-269">DriversLics#</span></span>
- <span data-ttu-id="32d8c-270">DriversLicence #</span><span class="sxs-lookup"><span data-stu-id="32d8c-270">DriversLicence#</span></span>
- <span data-ttu-id="32d8c-271">DriversLicences #</span><span class="sxs-lookup"><span data-stu-id="32d8c-271">DriversLicences#</span></span>
- <span data-ttu-id="32d8c-272">#Permis conduire</span><span class="sxs-lookup"><span data-stu-id="32d8c-272">Drivers Lic#</span></span>
- <span data-ttu-id="32d8c-273">#Permis conduire</span><span class="sxs-lookup"><span data-stu-id="32d8c-273">Drivers Lics#</span></span>
- <span data-ttu-id="32d8c-274">#Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="32d8c-274">Drivers Licence#</span></span>
- <span data-ttu-id="32d8c-275">#Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="32d8c-275">Drivers Licences#</span></span>
- <span data-ttu-id="32d8c-276">Driver'Lic #</span><span class="sxs-lookup"><span data-stu-id="32d8c-276">Driver'Lic#</span></span>
- <span data-ttu-id="32d8c-277">Driver'Lics #</span><span class="sxs-lookup"><span data-stu-id="32d8c-277">Driver'Lics#</span></span>
- <span data-ttu-id="32d8c-278">Driver'Licence #</span><span class="sxs-lookup"><span data-stu-id="32d8c-278">Driver'Licence#</span></span>
- <span data-ttu-id="32d8c-279">Driver'Licences #</span><span class="sxs-lookup"><span data-stu-id="32d8c-279">Driver'Licences#</span></span>
- <span data-ttu-id="32d8c-280">#Permis conduire</span><span class="sxs-lookup"><span data-stu-id="32d8c-280">Driver' Lic#</span></span>
- <span data-ttu-id="32d8c-281">#Permis conduire</span><span class="sxs-lookup"><span data-stu-id="32d8c-281">Driver' Lics#</span></span>
- <span data-ttu-id="32d8c-282">#Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="32d8c-282">Driver' Licence#</span></span>
- <span data-ttu-id="32d8c-283">#Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="32d8c-283">Driver' Licences#</span></span>
- <span data-ttu-id="32d8c-284">Driver'sLic #</span><span class="sxs-lookup"><span data-stu-id="32d8c-284">Driver'sLic#</span></span>
- <span data-ttu-id="32d8c-285">Driver'sLics #</span><span class="sxs-lookup"><span data-stu-id="32d8c-285">Driver'sLics#</span></span>
- <span data-ttu-id="32d8c-286">Driver'sLicence #</span><span class="sxs-lookup"><span data-stu-id="32d8c-286">Driver'sLicence#</span></span>
- <span data-ttu-id="32d8c-287">Driver'sLicences #</span><span class="sxs-lookup"><span data-stu-id="32d8c-287">Driver'sLicences#</span></span>
- <span data-ttu-id="32d8c-288">#Permisconduire</span><span class="sxs-lookup"><span data-stu-id="32d8c-288">Driver's Lic#</span></span>
- <span data-ttu-id="32d8c-289">#Permisconduire</span><span class="sxs-lookup"><span data-stu-id="32d8c-289">Driver's Lics#</span></span>
- <span data-ttu-id="32d8c-290">#Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="32d8c-290">Driver's Licence#</span></span>
- <span data-ttu-id="32d8c-291">#Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="32d8c-291">Driver's Licences#</span></span> 

#### <a name="keyword_australia_drivers_license_number_exclusions"></a><span data-ttu-id="32d8c-292">Keyword_australia_drivers_license_number_exclusions</span><span class="sxs-lookup"><span data-stu-id="32d8c-292">Keyword_australia_drivers_license_number_exclusions</span></span>

- <span data-ttu-id="32d8c-293">AAA</span><span class="sxs-lookup"><span data-stu-id="32d8c-293">aaa</span></span>
- <span data-ttu-id="32d8c-294">DriverLicense</span><span class="sxs-lookup"><span data-stu-id="32d8c-294">DriverLicense</span></span>
- <span data-ttu-id="32d8c-295">DriverLicenses</span><span class="sxs-lookup"><span data-stu-id="32d8c-295">DriverLicenses</span></span>
- <span data-ttu-id="32d8c-296">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="32d8c-296">Driver License</span></span>
- <span data-ttu-id="32d8c-297">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="32d8c-297">Driver Licenses</span></span>
- <span data-ttu-id="32d8c-298">DriversLicense</span><span class="sxs-lookup"><span data-stu-id="32d8c-298">DriversLicense</span></span>
- <span data-ttu-id="32d8c-299">DriversLicenses</span><span class="sxs-lookup"><span data-stu-id="32d8c-299">DriversLicenses</span></span>
- <span data-ttu-id="32d8c-300">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="32d8c-300">Drivers License</span></span>
- <span data-ttu-id="32d8c-301">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="32d8c-301">Drivers Licenses</span></span>
- <span data-ttu-id="32d8c-302">Driver'License</span><span class="sxs-lookup"><span data-stu-id="32d8c-302">Driver'License</span></span>
- <span data-ttu-id="32d8c-303">Driver'Licenses</span><span class="sxs-lookup"><span data-stu-id="32d8c-303">Driver'Licenses</span></span>
- <span data-ttu-id="32d8c-304">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="32d8c-304">Driver' License</span></span>
- <span data-ttu-id="32d8c-305">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="32d8c-305">Driver' Licenses</span></span>
- <span data-ttu-id="32d8c-306">Driver'sLicense</span><span class="sxs-lookup"><span data-stu-id="32d8c-306">Driver'sLicense</span></span>
- <span data-ttu-id="32d8c-307">Driver'sLicenses</span><span class="sxs-lookup"><span data-stu-id="32d8c-307">Driver'sLicenses</span></span>
- <span data-ttu-id="32d8c-308">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="32d8c-308">Driver's License</span></span>
- <span data-ttu-id="32d8c-309">Driver’s Licenses</span><span class="sxs-lookup"><span data-stu-id="32d8c-309">Driver's Licenses</span></span>
- <span data-ttu-id="32d8c-310">DriverLicense #</span><span class="sxs-lookup"><span data-stu-id="32d8c-310">DriverLicense#</span></span>
- <span data-ttu-id="32d8c-311">DriverLicenses #</span><span class="sxs-lookup"><span data-stu-id="32d8c-311">DriverLicenses#</span></span>
- <span data-ttu-id="32d8c-312">#Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="32d8c-312">Driver License#</span></span>
- <span data-ttu-id="32d8c-313">#Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="32d8c-313">Driver Licenses#</span></span>
- <span data-ttu-id="32d8c-314">DriversLicense #</span><span class="sxs-lookup"><span data-stu-id="32d8c-314">DriversLicense#</span></span>
- <span data-ttu-id="32d8c-315">DriversLicenses #</span><span class="sxs-lookup"><span data-stu-id="32d8c-315">DriversLicenses#</span></span>
- <span data-ttu-id="32d8c-316">#Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="32d8c-316">Drivers License#</span></span>
- <span data-ttu-id="32d8c-317">#Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="32d8c-317">Drivers Licenses#</span></span>
- <span data-ttu-id="32d8c-318">Driver'License #</span><span class="sxs-lookup"><span data-stu-id="32d8c-318">Driver'License#</span></span>
- <span data-ttu-id="32d8c-319">Driver'Licenses #</span><span class="sxs-lookup"><span data-stu-id="32d8c-319">Driver'Licenses#</span></span>
- <span data-ttu-id="32d8c-320">#Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="32d8c-320">Driver' License#</span></span>
- <span data-ttu-id="32d8c-321">#Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="32d8c-321">Driver' Licenses#</span></span>
- <span data-ttu-id="32d8c-322">Driver'sLicense #</span><span class="sxs-lookup"><span data-stu-id="32d8c-322">Driver'sLicense#</span></span>
- <span data-ttu-id="32d8c-323">Driver'sLicenses #</span><span class="sxs-lookup"><span data-stu-id="32d8c-323">Driver'sLicenses#</span></span>
- <span data-ttu-id="32d8c-324">#Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="32d8c-324">Driver's License#</span></span>
- <span data-ttu-id="32d8c-325">#Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="32d8c-325">Driver's Licenses#</span></span>
   
## <a name="australia-medical-account-number"></a><span data-ttu-id="32d8c-326">Numéro de dossier médical Australie</span><span class="sxs-lookup"><span data-stu-id="32d8c-326">Australia Medical Account Number</span></span>

### <a name="format"></a><span data-ttu-id="32d8c-327">Format</span><span class="sxs-lookup"><span data-stu-id="32d8c-327">Format</span></span>

<span data-ttu-id="32d8c-328">10 à 11 chiffres</span><span class="sxs-lookup"><span data-stu-id="32d8c-328">10-11 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="32d8c-329">Modèle</span><span class="sxs-lookup"><span data-stu-id="32d8c-329">Pattern</span></span>

<span data-ttu-id="32d8c-330">10 à 11 chiffres :</span><span class="sxs-lookup"><span data-stu-id="32d8c-330">10-11 digits:</span></span>
- <span data-ttu-id="32d8c-331">Le premier chiffre est compris entre 2 et 6</span><span class="sxs-lookup"><span data-stu-id="32d8c-331">First digit is in the range 2-6</span></span>
- <span data-ttu-id="32d8c-332">Le neuvième chiffre est un chiffre de contrôle</span><span class="sxs-lookup"><span data-stu-id="32d8c-332">Ninth digit is a check digit</span></span>
- <span data-ttu-id="32d8c-333">Le dixième chiffre est le chiffre d’émission</span><span class="sxs-lookup"><span data-stu-id="32d8c-333">Tenth digit is the issue digit</span></span>
- <span data-ttu-id="32d8c-334">Le onzième chiffre (facultatif) est le numéro individuel</span><span class="sxs-lookup"><span data-stu-id="32d8c-334">Eleventh digit (optional) is the individual number</span></span>

### <a name="checksum"></a><span data-ttu-id="32d8c-335">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="32d8c-335">Checksum</span></span>

<span data-ttu-id="32d8c-336">Oui</span><span class="sxs-lookup"><span data-stu-id="32d8c-336">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="32d8c-337">Définition</span><span class="sxs-lookup"><span data-stu-id="32d8c-337">Definition</span></span>

<span data-ttu-id="32d8c-338">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 95 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="32d8c-338">A DLP policy is 95% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="32d8c-339">La fonction Func_australian_medical_account_number trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="32d8c-339">The function Func_australian_medical_account_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="32d8c-340">Un mot clé figurant dans la liste Keyword_Australia_Medical_Account_Number est trouvé.</span><span class="sxs-lookup"><span data-stu-id="32d8c-340">A keyword from Keyword_Australia_Medical_Account_Number is found.</span></span>
- <span data-ttu-id="32d8c-341">La somme de contrôle est correcte.</span><span class="sxs-lookup"><span data-stu-id="32d8c-341">The checksum passes.</span></span>

<span data-ttu-id="32d8c-342">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="32d8c-342">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="32d8c-343">La fonction Func_australian_medical_account_number trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="32d8c-343">The function Func_australian_medical_account_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="32d8c-344">La somme de contrôle est correcte.</span><span class="sxs-lookup"><span data-stu-id="32d8c-344">The checksum passes.</span></span>

```xml
  <!-- Australia Medical Account Number -->
<Entity id="104a99a0-3d3b-4542-a40d-ab0b9e1efe63" recommendedConfidence="85" patternsProximity="300">
    <Pattern confidenceLevel="95">
     <IdMatch idRef="Func_australian_medical_account_number"/>
     <Any minMatches="1">
     <Match idRef="Keyword_Australia_Medical_Account_Number"/>
     </Any>
  </Pattern>
<Pattern confidenceLevel="85">
     <IdMatch idRef="Func_australian_medical_account_number"/>
     <Any minMatches="0" maxMatches="0">
  <Match idRef="Keyword_Australia_Medical_Account_Number"/>
     </Any>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="32d8c-345">Mots clés</span><span class="sxs-lookup"><span data-stu-id="32d8c-345">Keywords</span></span>

#### <a name="keyword_australia_medical_account_number"></a><span data-ttu-id="32d8c-346">Keyword_Australia_Medical_Account_Number</span><span class="sxs-lookup"><span data-stu-id="32d8c-346">Keyword_Australia_Medical_Account_Number</span></span>

- <span data-ttu-id="32d8c-347">informations sur le compte bancaire</span><span class="sxs-lookup"><span data-stu-id="32d8c-347">bank account details</span></span>
- <span data-ttu-id="32d8c-348">remboursements d’assurance maladie</span><span class="sxs-lookup"><span data-stu-id="32d8c-348">medicare payments</span></span>
- <span data-ttu-id="32d8c-349">compte de prêts immobiliers</span><span class="sxs-lookup"><span data-stu-id="32d8c-349">mortgage account</span></span>
- <span data-ttu-id="32d8c-350">paiements bancaires</span><span class="sxs-lookup"><span data-stu-id="32d8c-350">bank payments</span></span>
- <span data-ttu-id="32d8c-351">direction de l’information</span><span class="sxs-lookup"><span data-stu-id="32d8c-351">information branch</span></span>
- <span data-ttu-id="32d8c-352">prêt sur carte de crédit</span><span class="sxs-lookup"><span data-stu-id="32d8c-352">credit card loan</span></span>
- <span data-ttu-id="32d8c-353">département des services sociaux</span><span class="sxs-lookup"><span data-stu-id="32d8c-353">department of human services</span></span>
- <span data-ttu-id="32d8c-354">service local</span><span class="sxs-lookup"><span data-stu-id="32d8c-354">local service</span></span>
- <span data-ttu-id="32d8c-355">médicaux</span><span class="sxs-lookup"><span data-stu-id="32d8c-355">medicare</span></span>

   
## <a name="australia-passport-number"></a><span data-ttu-id="32d8c-356">Numéro de passeport Australie</span><span class="sxs-lookup"><span data-stu-id="32d8c-356">Australia Passport Number</span></span>

### <a name="format"></a><span data-ttu-id="32d8c-357">Format</span><span class="sxs-lookup"><span data-stu-id="32d8c-357">Format</span></span>

<span data-ttu-id="32d8c-358">Une lettre suivie de sept chiffres</span><span class="sxs-lookup"><span data-stu-id="32d8c-358">A letter followed by seven digits</span></span>

### <a name="pattern"></a><span data-ttu-id="32d8c-359">Modèle</span><span class="sxs-lookup"><span data-stu-id="32d8c-359">Pattern</span></span>

<span data-ttu-id="32d8c-360">Une lettre (ne respectant pas la casse) suivie de sept chiffres</span><span class="sxs-lookup"><span data-stu-id="32d8c-360">A letter (not case sensitive) followed by seven digits</span></span>

### <a name="checksum"></a><span data-ttu-id="32d8c-361">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="32d8c-361">Checksum</span></span>

<span data-ttu-id="32d8c-362">Non</span><span class="sxs-lookup"><span data-stu-id="32d8c-362">No</span></span>

### <a name="definition"></a><span data-ttu-id="32d8c-363">Définition</span><span class="sxs-lookup"><span data-stu-id="32d8c-363">Definition</span></span>

<span data-ttu-id="32d8c-364">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="32d8c-364">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="32d8c-365">L’expression régulière Regex_australia_passport_number trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="32d8c-365">The regular expression Regex_australia_passport_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="32d8c-366">Un mot clé depuis Keyword_passport ou Keyword_australia_passport_number est trouvé.</span><span class="sxs-lookup"><span data-stu-id="32d8c-366">A keyword from Keyword_passport or Keyword_australia_passport_number is found.</span></span>

```xml
<!-- Australia Passport Number -->
<Entity id="29869db6-602d-4853-ab93-3484f905df50" patternsProximity="300" recommendedConfidence="75">
  <Pattern confidenceLevel="75">
        <IdMatch idRef="Regex_australia_passport_number" />
        <Any minMatches="1">
          <Match idRef="Keyword_passport" />
          <Match idRef="Keyword_australia_passport_number" />
        </Any>
   </Pattern>
</Entity>   
```

### <a name="keywords"></a><span data-ttu-id="32d8c-367">Mots clés</span><span class="sxs-lookup"><span data-stu-id="32d8c-367">Keywords</span></span>

#### <a name="keyword_passport"></a><span data-ttu-id="32d8c-368">Keyword_passport</span><span class="sxs-lookup"><span data-stu-id="32d8c-368">Keyword_passport</span></span>

- <span data-ttu-id="32d8c-369">Numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="32d8c-369">Passport Number</span></span>
- <span data-ttu-id="32d8c-370">N° de passeport</span><span class="sxs-lookup"><span data-stu-id="32d8c-370">Passport No</span></span>
- <span data-ttu-id="32d8c-371"># Passeport</span><span class="sxs-lookup"><span data-stu-id="32d8c-371">Passport #</span></span>
- <span data-ttu-id="32d8c-372">Tel #</span><span class="sxs-lookup"><span data-stu-id="32d8c-372">Passport#</span></span>
- <span data-ttu-id="32d8c-373">PassportID</span><span class="sxs-lookup"><span data-stu-id="32d8c-373">PassportID</span></span>
- <span data-ttu-id="32d8c-374">N ° passeport</span><span class="sxs-lookup"><span data-stu-id="32d8c-374">Passportno</span></span>
- <span data-ttu-id="32d8c-375">passportnumber</span><span class="sxs-lookup"><span data-stu-id="32d8c-375">passportnumber</span></span>
- <span data-ttu-id="32d8c-376">パスポート</span><span class="sxs-lookup"><span data-stu-id="32d8c-376">パスポート</span></span>
- <span data-ttu-id="32d8c-377">パスポート番号</span><span class="sxs-lookup"><span data-stu-id="32d8c-377">パスポート番号</span></span>
- <span data-ttu-id="32d8c-378">パスポートのNum</span><span class="sxs-lookup"><span data-stu-id="32d8c-378">パスポートのNum</span></span>
- <span data-ttu-id="32d8c-379">パスポート＃</span><span class="sxs-lookup"><span data-stu-id="32d8c-379">パスポート ＃</span></span> 
- <span data-ttu-id="32d8c-380">Numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="32d8c-380">Numéro de passeport</span></span>
- <span data-ttu-id="32d8c-381">Passeport n°</span><span class="sxs-lookup"><span data-stu-id="32d8c-381">Passeport n °</span></span>
- <span data-ttu-id="32d8c-382">Passeport numéro</span><span class="sxs-lookup"><span data-stu-id="32d8c-382">Passeport Non</span></span>
- <span data-ttu-id="32d8c-383"># Passeport</span><span class="sxs-lookup"><span data-stu-id="32d8c-383">Passeport #</span></span>
- <span data-ttu-id="32d8c-384">Passeport #</span><span class="sxs-lookup"><span data-stu-id="32d8c-384">Passeport#</span></span>
- <span data-ttu-id="32d8c-385">PasseportNon</span><span class="sxs-lookup"><span data-stu-id="32d8c-385">PasseportNon</span></span>
- <span data-ttu-id="32d8c-386">Passeportn °</span><span class="sxs-lookup"><span data-stu-id="32d8c-386">Passeportn °</span></span>

#### <a name="keyword_australia_passport_number"></a><span data-ttu-id="32d8c-387">Keyword_australia_passport_number</span><span class="sxs-lookup"><span data-stu-id="32d8c-387">Keyword_australia_passport_number</span></span>

- <span data-ttu-id="32d8c-388">tel</span><span class="sxs-lookup"><span data-stu-id="32d8c-388">passport</span></span>
- <span data-ttu-id="32d8c-389">informations sur le passeport</span><span class="sxs-lookup"><span data-stu-id="32d8c-389">passport details</span></span>
- <span data-ttu-id="32d8c-390">immigration et citoyenneté</span><span class="sxs-lookup"><span data-stu-id="32d8c-390">immigration and citizenship</span></span>
- <span data-ttu-id="32d8c-391">Australie</span><span class="sxs-lookup"><span data-stu-id="32d8c-391">commonwealth of australia</span></span>
- <span data-ttu-id="32d8c-392">service de l’immigration</span><span class="sxs-lookup"><span data-stu-id="32d8c-392">department of immigration</span></span>
- <span data-ttu-id="32d8c-393">adresse de résidence</span><span class="sxs-lookup"><span data-stu-id="32d8c-393">residential address</span></span>
- <span data-ttu-id="32d8c-394">service de l’immigration et de la citoyenneté</span><span class="sxs-lookup"><span data-stu-id="32d8c-394">department of immigration and citizenship</span></span>
- <span data-ttu-id="32d8c-395">délivrance</span><span class="sxs-lookup"><span data-stu-id="32d8c-395">visa</span></span>
- <span data-ttu-id="32d8c-396">Carte nationale d’identité</span><span class="sxs-lookup"><span data-stu-id="32d8c-396">national identity card</span></span>
- <span data-ttu-id="32d8c-397">numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="32d8c-397">passport number</span></span>
- <span data-ttu-id="32d8c-398">document de voyage</span><span class="sxs-lookup"><span data-stu-id="32d8c-398">travel document</span></span>
- <span data-ttu-id="32d8c-399">autorité émettrice</span><span class="sxs-lookup"><span data-stu-id="32d8c-399">issuing authority</span></span>
   
## <a name="australia-tax-file-number"></a><span data-ttu-id="32d8c-400">Numéro de dossier fiscal Australie</span><span class="sxs-lookup"><span data-stu-id="32d8c-400">Australia Tax File Number</span></span>

### <a name="format"></a><span data-ttu-id="32d8c-401">Format</span><span class="sxs-lookup"><span data-stu-id="32d8c-401">Format</span></span>

<span data-ttu-id="32d8c-402">8 ou 9 chiffres</span><span class="sxs-lookup"><span data-stu-id="32d8c-402">8-9 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="32d8c-403">Modèle</span><span class="sxs-lookup"><span data-stu-id="32d8c-403">Pattern</span></span>

<span data-ttu-id="32d8c-404">8 à 9 chiffres généralement entrecoupés d’espaces comme suit :</span><span class="sxs-lookup"><span data-stu-id="32d8c-404">8-9 digits typically presented with spaces as follows:</span></span>
- <span data-ttu-id="32d8c-405">Trois chiffres</span><span class="sxs-lookup"><span data-stu-id="32d8c-405">Three digits</span></span> 
- <span data-ttu-id="32d8c-406">Un espace facultatif</span><span class="sxs-lookup"><span data-stu-id="32d8c-406">An optional space</span></span> 
- <span data-ttu-id="32d8c-407">Trois chiffres</span><span class="sxs-lookup"><span data-stu-id="32d8c-407">Three digits</span></span> 
- <span data-ttu-id="32d8c-408">Un espace facultatif</span><span class="sxs-lookup"><span data-stu-id="32d8c-408">An optional space</span></span> 
- <span data-ttu-id="32d8c-409">2 à 3 chiffres où le dernier chiffre est un chiffre de contrôle</span><span class="sxs-lookup"><span data-stu-id="32d8c-409">2-3 digits where the last digit is a check digit</span></span>

### <a name="checksum"></a><span data-ttu-id="32d8c-410">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="32d8c-410">Checksum</span></span>

<span data-ttu-id="32d8c-411">Oui</span><span class="sxs-lookup"><span data-stu-id="32d8c-411">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="32d8c-412">Définition</span><span class="sxs-lookup"><span data-stu-id="32d8c-412">Definition</span></span>

<span data-ttu-id="32d8c-413">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="32d8c-413">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="32d8c-414">La fonction Func_australian_tax_file_number trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="32d8c-414">The function Func_australian_tax_file_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="32d8c-415">Aucun mot clé figurant dans la liste Keyword_Australia_Tax_File_Number ou Keyword_number_exclusions n’est trouvé.</span><span class="sxs-lookup"><span data-stu-id="32d8c-415">No keyword from Keyword_Australia_Tax_File_Number or Keyword_number_exclusions is found.</span></span>
- <span data-ttu-id="32d8c-416">La somme de contrôle est correcte.</span><span class="sxs-lookup"><span data-stu-id="32d8c-416">The checksum passes.</span></span>

```xml
   <!-- Australia Tax File Number -->
    <Entity id="e29bc95f-ff70-4a37-aa01-04d17360a4c5" patternsProximity="300" recommendedConfidence="85">
      <Pattern confidenceLevel="85">
        <IdMatch idRef="Func_australian_tax_file_number" />
        <Match idRef="Keyword_Australia_Tax_File_Number" />
        <Any minMatches="0" maxMatches="0">
          <Match idRef="Keyword_number_exclusions" />
        </Any>
      </Pattern>
    </Entity>
```

### <a name="keywords"></a><span data-ttu-id="32d8c-417">Mots clés</span><span class="sxs-lookup"><span data-stu-id="32d8c-417">Keywords</span></span>

#### <a name="keyword_australia_tax_file_number"></a><span data-ttu-id="32d8c-418">Keyword_Australia_Tax_File_Number</span><span class="sxs-lookup"><span data-stu-id="32d8c-418">Keyword_Australia_Tax_File_Number</span></span>

- <span data-ttu-id="32d8c-419">numéro d’entreprise australien</span><span class="sxs-lookup"><span data-stu-id="32d8c-419">australian business number</span></span>
- <span data-ttu-id="32d8c-420">taux d’imposition marginale</span><span class="sxs-lookup"><span data-stu-id="32d8c-420">marginal tax rate</span></span>
- <span data-ttu-id="32d8c-421">prélèvement d’assurance maladie</span><span class="sxs-lookup"><span data-stu-id="32d8c-421">medicare levy</span></span>
- <span data-ttu-id="32d8c-422">numéro de portefeuille</span><span class="sxs-lookup"><span data-stu-id="32d8c-422">portfolio number</span></span>
- <span data-ttu-id="32d8c-423">service des vétérans</span><span class="sxs-lookup"><span data-stu-id="32d8c-423">service veterans</span></span>
- <span data-ttu-id="32d8c-424">retenue à la source</span><span class="sxs-lookup"><span data-stu-id="32d8c-424">withholding tax</span></span>
- <span data-ttu-id="32d8c-425">déclaration d’impôts individuels</span><span class="sxs-lookup"><span data-stu-id="32d8c-425">individual tax return</span></span>
- <span data-ttu-id="32d8c-426">numéro de dossier fiscal</span><span class="sxs-lookup"><span data-stu-id="32d8c-426">tax file number</span></span>

#### <a name="keyword_number_exclusions"></a><span data-ttu-id="32d8c-427">Keyword_number_exclusions</span><span class="sxs-lookup"><span data-stu-id="32d8c-427">Keyword_number_exclusions</span></span>

- <span data-ttu-id="32d8c-428">00000000</span><span class="sxs-lookup"><span data-stu-id="32d8c-428">00000000</span></span>
- <span data-ttu-id="32d8c-429">11111111</span><span class="sxs-lookup"><span data-stu-id="32d8c-429">11111111</span></span>
- <span data-ttu-id="32d8c-430">22222222</span><span class="sxs-lookup"><span data-stu-id="32d8c-430">22222222</span></span>
- <span data-ttu-id="32d8c-431">33333333</span><span class="sxs-lookup"><span data-stu-id="32d8c-431">33333333</span></span>
- <span data-ttu-id="32d8c-432">44444444</span><span class="sxs-lookup"><span data-stu-id="32d8c-432">44444444</span></span>
- <span data-ttu-id="32d8c-433">55555555</span><span class="sxs-lookup"><span data-stu-id="32d8c-433">55555555</span></span>
- <span data-ttu-id="32d8c-434">66666666</span><span class="sxs-lookup"><span data-stu-id="32d8c-434">66666666</span></span>
- <span data-ttu-id="32d8c-435">77777777</span><span class="sxs-lookup"><span data-stu-id="32d8c-435">77777777</span></span>
- <span data-ttu-id="32d8c-436">88888888</span><span class="sxs-lookup"><span data-stu-id="32d8c-436">88888888</span></span>
- <span data-ttu-id="32d8c-437">99999999</span><span class="sxs-lookup"><span data-stu-id="32d8c-437">99999999</span></span>
- <span data-ttu-id="32d8c-438">000000000</span><span class="sxs-lookup"><span data-stu-id="32d8c-438">000000000</span></span>
- <span data-ttu-id="32d8c-439">111111111</span><span class="sxs-lookup"><span data-stu-id="32d8c-439">111111111</span></span>
- <span data-ttu-id="32d8c-440">222222222</span><span class="sxs-lookup"><span data-stu-id="32d8c-440">222222222</span></span>
- <span data-ttu-id="32d8c-441">333333333</span><span class="sxs-lookup"><span data-stu-id="32d8c-441">333333333</span></span>
- <span data-ttu-id="32d8c-442">444444444</span><span class="sxs-lookup"><span data-stu-id="32d8c-442">444444444</span></span>
- <span data-ttu-id="32d8c-443">555555555</span><span class="sxs-lookup"><span data-stu-id="32d8c-443">555555555</span></span>
- <span data-ttu-id="32d8c-444">666666666</span><span class="sxs-lookup"><span data-stu-id="32d8c-444">666666666</span></span>
- <span data-ttu-id="32d8c-445">777777777</span><span class="sxs-lookup"><span data-stu-id="32d8c-445">777777777</span></span>
- <span data-ttu-id="32d8c-446">888888888</span><span class="sxs-lookup"><span data-stu-id="32d8c-446">888888888</span></span>
- <span data-ttu-id="32d8c-447">999999999</span><span class="sxs-lookup"><span data-stu-id="32d8c-447">999999999</span></span>
- <span data-ttu-id="32d8c-448">0000000000</span><span class="sxs-lookup"><span data-stu-id="32d8c-448">0000000000</span></span>
- <span data-ttu-id="32d8c-449">1111111111</span><span class="sxs-lookup"><span data-stu-id="32d8c-449">1111111111</span></span>
- <span data-ttu-id="32d8c-450">2222222222</span><span class="sxs-lookup"><span data-stu-id="32d8c-450">2222222222</span></span>
- <span data-ttu-id="32d8c-451">3333333333</span><span class="sxs-lookup"><span data-stu-id="32d8c-451">3333333333</span></span>
- <span data-ttu-id="32d8c-452">4444444444</span><span class="sxs-lookup"><span data-stu-id="32d8c-452">4444444444</span></span>
- <span data-ttu-id="32d8c-453">5555555555</span><span class="sxs-lookup"><span data-stu-id="32d8c-453">5555555555</span></span>
- <span data-ttu-id="32d8c-454">6666666666</span><span class="sxs-lookup"><span data-stu-id="32d8c-454">6666666666</span></span>
- <span data-ttu-id="32d8c-455">7777777777</span><span class="sxs-lookup"><span data-stu-id="32d8c-455">7777777777</span></span>
- <span data-ttu-id="32d8c-456">8888888888</span><span class="sxs-lookup"><span data-stu-id="32d8c-456">8888888888</span></span>
- <span data-ttu-id="32d8c-457">9999999999</span><span class="sxs-lookup"><span data-stu-id="32d8c-457">9999999999</span></span>

## <a name="azure-documentdb-auth-key"></a><span data-ttu-id="32d8c-458">Clé d’authentification Azure DocumentDB</span><span class="sxs-lookup"><span data-stu-id="32d8c-458">Azure DocumentDB Auth Key</span></span>

### <a name="format"></a><span data-ttu-id="32d8c-459">Format</span><span class="sxs-lookup"><span data-stu-id="32d8c-459">Format</span></span>

<span data-ttu-id="32d8c-460">La chaîne « DocumentDb » suivie des caractères et des chaînes présentés dans le modèle ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="32d8c-460">The string "DocumentDb" followed by the characters and strings outlined in the pattern below.</span></span>

### <a name="pattern"></a><span data-ttu-id="32d8c-461">Modèle</span><span class="sxs-lookup"><span data-stu-id="32d8c-461">Pattern</span></span>

- <span data-ttu-id="32d8c-462">La chaîne « DocumentDb »</span><span class="sxs-lookup"><span data-stu-id="32d8c-462">The string "DocumentDb"</span></span>
- <span data-ttu-id="32d8c-463">N’importe quelle combinaison entre 3-200 majuscules ou minuscules, des chiffres, des symboles, des caractères spéciaux ou des espaces</span><span class="sxs-lookup"><span data-stu-id="32d8c-463">Any combination of between 3-200 lower- or uppercase letters, digits, symbols, special characters, or spaces</span></span>
- <span data-ttu-id="32d8c-464">Symbole supérieur à (>), signe égal (=), guillemet (") ou apostrophe (')</span><span class="sxs-lookup"><span data-stu-id="32d8c-464">A greater than symbol (>), an equal sign (=), a quotation mark ("), or an apostrophe (')</span></span>
- <span data-ttu-id="32d8c-465">Toute combinaison de 86 lettres majuscules ou minuscules, des chiffres, une barre oblique (/) ou un signe plus (+)</span><span class="sxs-lookup"><span data-stu-id="32d8c-465">Any combination of 86 lower- or uppercase letters, digits, forward slash (/), or plus sign (+)</span></span>
- <span data-ttu-id="32d8c-466">Deux signes égal (=)</span><span class="sxs-lookup"><span data-stu-id="32d8c-466">Two equal signs (=)</span></span>

### <a name="checksum"></a><span data-ttu-id="32d8c-467">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="32d8c-467">Checksum</span></span>

<span data-ttu-id="32d8c-468">Non</span><span class="sxs-lookup"><span data-stu-id="32d8c-468">No</span></span>

### <a name="definition"></a><span data-ttu-id="32d8c-469">Définition</span><span class="sxs-lookup"><span data-stu-id="32d8c-469">Definition</span></span>

<span data-ttu-id="32d8c-470">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="32d8c-470">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="32d8c-471">L’expression régulière CEP_Regex_AzureDocumentDBAuthKey trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="32d8c-471">The regular expression CEP_Regex_AzureDocumentDBAuthKey finds content that matches the pattern.</span></span>
- <span data-ttu-id="32d8c-472">L’expression régulière CEP_CommonExampleKeywords ne trouve **pas** le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="32d8c-472">The regular expression CEP_CommonExampleKeywords does **not** find content that matches the pattern.</span></span>

```xml
<!-- Azure Document DB Auth Key -->
<Entity id="0f587d92-eb28-44a9-bd1c-90f2892b47aa" patternsProximity="300" recommendedConfidence="85">
  <Pattern confidenceLevel="85">
        <IdMatch idRef="CEP_Regex_AzureDocumentDBAuthKey" />
        <Any minMatches="0" maxMatches="0">
            <Match idRef="CEP_CommonExampleKeywords" />
          </Any>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="32d8c-473">Mots clés</span><span class="sxs-lookup"><span data-stu-id="32d8c-473">Keywords</span></span>

#### <a name="cep_commonexamplekeywords"></a><span data-ttu-id="32d8c-474">CEP_CommonExampleKeywords</span><span class="sxs-lookup"><span data-stu-id="32d8c-474">CEP_CommonExampleKeywords</span></span>

<span data-ttu-id="32d8c-475">(Notez que techniquement, ce type d’informations sensibles identifie ces mots clés à l’aide d’une expression régulière, et non d’une liste de mots clés.)</span><span class="sxs-lookup"><span data-stu-id="32d8c-475">(Note that technically, this sensitive information type identifies these keywords by using a regular expression, not a keyword list.)</span></span>

- <span data-ttu-id="32d8c-476">contoso</span><span class="sxs-lookup"><span data-stu-id="32d8c-476">contoso</span></span>
- <span data-ttu-id="32d8c-477">société</span><span class="sxs-lookup"><span data-stu-id="32d8c-477">fabrikam</span></span>
- <span data-ttu-id="32d8c-478">Northwind</span><span class="sxs-lookup"><span data-stu-id="32d8c-478">northwind</span></span>
- <span data-ttu-id="32d8c-479">immédiatement</span><span class="sxs-lookup"><span data-stu-id="32d8c-479">sandbox</span></span>
- <span data-ttu-id="32d8c-480">onebox</span><span class="sxs-lookup"><span data-stu-id="32d8c-480">onebox</span></span>
- <span data-ttu-id="32d8c-481">hôte</span><span class="sxs-lookup"><span data-stu-id="32d8c-481">localhost</span></span>
- <span data-ttu-id="32d8c-482">bouclage</span><span class="sxs-lookup"><span data-stu-id="32d8c-482">127.0.0.1</span></span>
- <span data-ttu-id="32d8c-483">testacs.</span><span class="sxs-lookup"><span data-stu-id="32d8c-483">testacs.</span></span><!--no-hyperlink--><span data-ttu-id="32d8c-484">com</span><span class="sxs-lookup"><span data-stu-id="32d8c-484">com</span></span>
- <span data-ttu-id="32d8c-485">s-int.</span><span class="sxs-lookup"><span data-stu-id="32d8c-485">s-int.</span></span><!--no-hyperlink--><span data-ttu-id="32d8c-486">NET</span><span class="sxs-lookup"><span data-stu-id="32d8c-486">net</span></span>

## <a name="azure-iaas-database-connection-string-and-azure-sql-connection-string"></a><span data-ttu-id="32d8c-487">Chaîne de connexion à la base de données IAAS Azure et chaîne de connexion Azure SQL</span><span class="sxs-lookup"><span data-stu-id="32d8c-487">Azure IAAS Database Connection String and Azure SQL Connection String</span></span>

### <a name="format"></a><span data-ttu-id="32d8c-488">Format</span><span class="sxs-lookup"><span data-stu-id="32d8c-488">Format</span></span>

<span data-ttu-id="32d8c-489">La chaîne « Server », « Server » ou « Data source » suivie des caractères et des chaînes décrits dans le modèle ci-dessous, y compris la chaîne «cloudapp. Azure.</span><span class="sxs-lookup"><span data-stu-id="32d8c-489">The string "Server", "server", or "data source" followed by the characters and strings outlined in the pattern below, including the string "cloudapp.azure.</span></span><!--no-hyperlink--><span data-ttu-id="32d8c-490">com» ou «cloudapp. Azure.</span><span class="sxs-lookup"><span data-stu-id="32d8c-490">com" or "cloudapp.azure.</span></span><!--no-hyperlink--><span data-ttu-id="32d8c-491">NET "ou" Database. Windows.</span><span class="sxs-lookup"><span data-stu-id="32d8c-491">net" or "database.windows.</span></span><!--no-hyperlink--><span data-ttu-id="32d8c-492">NET ", et la chaîne" password "ou" password "ou" PWD ".</span><span class="sxs-lookup"><span data-stu-id="32d8c-492">net", and the string "Password" or "password" or "pwd".</span></span>

### <a name="pattern"></a><span data-ttu-id="32d8c-493">Modèle</span><span class="sxs-lookup"><span data-stu-id="32d8c-493">Pattern</span></span>

- <span data-ttu-id="32d8c-494">Chaîne « serveur », « serveur » ou « source de données »</span><span class="sxs-lookup"><span data-stu-id="32d8c-494">The string "Server", "server", or "data source"</span></span>
- <span data-ttu-id="32d8c-495">0-2 espaces blancs</span><span class="sxs-lookup"><span data-stu-id="32d8c-495">0-2 whitespace characters</span></span>
- <span data-ttu-id="32d8c-496">Signe égal (=)</span><span class="sxs-lookup"><span data-stu-id="32d8c-496">An equal sign (=)</span></span>
- <span data-ttu-id="32d8c-497">0-2 espaces blancs</span><span class="sxs-lookup"><span data-stu-id="32d8c-497">0-2 whitespace characters</span></span>
- <span data-ttu-id="32d8c-498">N’importe quelle combinaison entre 1-200 majuscules ou minuscules, des chiffres, des symboles, des caractères spéciaux ou des espaces</span><span class="sxs-lookup"><span data-stu-id="32d8c-498">Any combination of between 1-200 lower- or uppercase letters, digits, symbols, special characters, or spaces</span></span>
- <span data-ttu-id="32d8c-499">La chaîne «cloudapp. Azure.</span><span class="sxs-lookup"><span data-stu-id="32d8c-499">The string "cloudapp.azure.</span></span><!--no-hyperlink--><span data-ttu-id="32d8c-500">com "," cloudapp. Azure.</span><span class="sxs-lookup"><span data-stu-id="32d8c-500">com", "cloudapp.azure.</span></span><!--no-hyperlink--><span data-ttu-id="32d8c-501">NET "ou" Database. Windows.</span><span class="sxs-lookup"><span data-stu-id="32d8c-501">net", or "database.windows.</span></span><!--no-hyperlink--><span data-ttu-id="32d8c-502">NET</span><span class="sxs-lookup"><span data-stu-id="32d8c-502">net"</span></span>
- <span data-ttu-id="32d8c-503">N’importe quelle combinaison entre 1-300 majuscules ou minuscules, des chiffres, des symboles, des caractères spéciaux ou des espaces</span><span class="sxs-lookup"><span data-stu-id="32d8c-503">Any combination of between 1-300 lower- or uppercase letters, digits, symbols, special characters, or spaces</span></span>
- <span data-ttu-id="32d8c-504">La chaîne "password", "password" ou "PWD"</span><span class="sxs-lookup"><span data-stu-id="32d8c-504">The string "Password", "password", or "pwd"</span></span>
- <span data-ttu-id="32d8c-505">0-2 espaces blancs</span><span class="sxs-lookup"><span data-stu-id="32d8c-505">0-2 whitespace characters</span></span>
- <span data-ttu-id="32d8c-506">Signe égal (=)</span><span class="sxs-lookup"><span data-stu-id="32d8c-506">An equal sign (=)</span></span>
- <span data-ttu-id="32d8c-507">0-2 espaces blancs</span><span class="sxs-lookup"><span data-stu-id="32d8c-507">0-2 whitespace characters</span></span>
- <span data-ttu-id="32d8c-508">Un ou plusieurs caractères qui ne sont pas des points-virgules (;), guillemets (") ou apostrophe (')</span><span class="sxs-lookup"><span data-stu-id="32d8c-508">One or more characters that is not a semicolon (;), quotation mark ("), or apostrophe (')</span></span>
- <span data-ttu-id="32d8c-509">Un point-virgule (;), guillemet (") ou apostrophe (')</span><span class="sxs-lookup"><span data-stu-id="32d8c-509">A semicolon (;), quotation mark ("), or apostrophe (')</span></span>

### <a name="checksum"></a><span data-ttu-id="32d8c-510">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="32d8c-510">Checksum</span></span>

<span data-ttu-id="32d8c-511">Non</span><span class="sxs-lookup"><span data-stu-id="32d8c-511">No</span></span>

### <a name="definition"></a><span data-ttu-id="32d8c-512">Définition</span><span class="sxs-lookup"><span data-stu-id="32d8c-512">Definition</span></span>

<span data-ttu-id="32d8c-513">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="32d8c-513">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="32d8c-514">L’expression régulière CEP_Regex_AzureConnectionString trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="32d8c-514">The regular expression CEP_Regex_AzureConnectionString finds content that matches the pattern.</span></span>
- <span data-ttu-id="32d8c-515">L’expression régulière CEP_CommonExampleKeywords ne trouve **pas** le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="32d8c-515">The regular expression CEP_CommonExampleKeywords does **not** find content that matches the pattern.</span></span>

```xml
<!--Azure IAAS Database Connection String and Azure SQL Connection String-->
<Entity id="ce1a126d-186f-4700-8c0c-486157b953fd" patternsProximity="300" recommendedConfidence="85">
  <Pattern confidenceLevel="85">
        <IdMatch idRef="CEP_Regex_AzureConnectionString" />
        <Any minMatches="0" maxMatches="0">
            <Match idRef="CEP_CommonExampleKeywords" />
        </Any>
    </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="32d8c-516">Mots clés</span><span class="sxs-lookup"><span data-stu-id="32d8c-516">Keywords</span></span>

#### <a name="cep_commonexamplekeywords"></a><span data-ttu-id="32d8c-517">CEP_CommonExampleKeywords</span><span class="sxs-lookup"><span data-stu-id="32d8c-517">CEP_CommonExampleKeywords</span></span>

<span data-ttu-id="32d8c-518">(Notez que techniquement, ce type d’informations sensibles identifie ces mots clés à l’aide d’une expression régulière, et non d’une liste de mots clés.)</span><span class="sxs-lookup"><span data-stu-id="32d8c-518">(Note that technically, this sensitive information type identifies these keywords by using a regular expression, not a keyword list.)</span></span>

- <span data-ttu-id="32d8c-519">contoso</span><span class="sxs-lookup"><span data-stu-id="32d8c-519">contoso</span></span>
- <span data-ttu-id="32d8c-520">société</span><span class="sxs-lookup"><span data-stu-id="32d8c-520">fabrikam</span></span>
- <span data-ttu-id="32d8c-521">Northwind</span><span class="sxs-lookup"><span data-stu-id="32d8c-521">northwind</span></span>
- <span data-ttu-id="32d8c-522">immédiatement</span><span class="sxs-lookup"><span data-stu-id="32d8c-522">sandbox</span></span>
- <span data-ttu-id="32d8c-523">onebox</span><span class="sxs-lookup"><span data-stu-id="32d8c-523">onebox</span></span>
- <span data-ttu-id="32d8c-524">hôte</span><span class="sxs-lookup"><span data-stu-id="32d8c-524">localhost</span></span>
- <span data-ttu-id="32d8c-525">bouclage</span><span class="sxs-lookup"><span data-stu-id="32d8c-525">127.0.0.1</span></span>
- <span data-ttu-id="32d8c-526">testacs.</span><span class="sxs-lookup"><span data-stu-id="32d8c-526">testacs.</span></span><!--no-hyperlink--><span data-ttu-id="32d8c-527">com</span><span class="sxs-lookup"><span data-stu-id="32d8c-527">com</span></span>
- <span data-ttu-id="32d8c-528">s-int.</span><span class="sxs-lookup"><span data-stu-id="32d8c-528">s-int.</span></span><!--no-hyperlink--><span data-ttu-id="32d8c-529">NET</span><span class="sxs-lookup"><span data-stu-id="32d8c-529">net</span></span>

## <a name="azure-iot-connection-string"></a><span data-ttu-id="32d8c-530">Chaîne de connexion Azure IoT</span><span class="sxs-lookup"><span data-stu-id="32d8c-530">Azure IoT Connection String</span></span>

### <a name="format"></a><span data-ttu-id="32d8c-531">Format</span><span class="sxs-lookup"><span data-stu-id="32d8c-531">Format</span></span>

<span data-ttu-id="32d8c-532">La chaîne « nomhôte » suivie des caractères et des chaînes décrits dans le modèle ci-dessous, y compris les chaînes «Azure-appareils.</span><span class="sxs-lookup"><span data-stu-id="32d8c-532">The string "HostName" followed by the characters and strings outlined in the pattern below, including the strings "azure-devices.</span></span><!--no-hyperlink--><span data-ttu-id="32d8c-533">NET "et" SharedAccessKey ".</span><span class="sxs-lookup"><span data-stu-id="32d8c-533">net" and "SharedAccessKey".</span></span>

### <a name="pattern"></a><span data-ttu-id="32d8c-534">Modèle</span><span class="sxs-lookup"><span data-stu-id="32d8c-534">Pattern</span></span>

- <span data-ttu-id="32d8c-535">La chaîne « nomhôte »</span><span class="sxs-lookup"><span data-stu-id="32d8c-535">The string "HostName"</span></span>
- <span data-ttu-id="32d8c-536">0-2 espaces blancs</span><span class="sxs-lookup"><span data-stu-id="32d8c-536">0-2 whitespace characters</span></span>
- <span data-ttu-id="32d8c-537">Signe égal (=)</span><span class="sxs-lookup"><span data-stu-id="32d8c-537">An equal sign (=)</span></span>
- <span data-ttu-id="32d8c-538">0-2 espaces blancs</span><span class="sxs-lookup"><span data-stu-id="32d8c-538">0-2 whitespace characters</span></span>
- <span data-ttu-id="32d8c-539">N’importe quelle combinaison entre 1-200 majuscules ou minuscules, des chiffres, des symboles, des caractères spéciaux ou des espaces</span><span class="sxs-lookup"><span data-stu-id="32d8c-539">Any combination of between 1-200 lower- or uppercase letters, digits, symbols, special characters, or spaces</span></span>
- <span data-ttu-id="32d8c-540">La chaîne «Azure-appareils.</span><span class="sxs-lookup"><span data-stu-id="32d8c-540">The string "azure-devices.</span></span><!--no-hyperlink--><span data-ttu-id="32d8c-541">NET</span><span class="sxs-lookup"><span data-stu-id="32d8c-541">net"</span></span>
- <span data-ttu-id="32d8c-542">N’importe quelle combinaison entre 1-200 majuscules ou minuscules, des chiffres, des symboles, des caractères spéciaux ou des espaces</span><span class="sxs-lookup"><span data-stu-id="32d8c-542">Any combination of between 1-200 lower- or uppercase letters, digits, symbols, special characters, or spaces</span></span>
- <span data-ttu-id="32d8c-543">La chaîne « SharedAccessKey »</span><span class="sxs-lookup"><span data-stu-id="32d8c-543">The string "SharedAccessKey"</span></span>
- <span data-ttu-id="32d8c-544">0-2 espaces blancs</span><span class="sxs-lookup"><span data-stu-id="32d8c-544">0-2 whitespace characters</span></span>
- <span data-ttu-id="32d8c-545">Signe égal (=)</span><span class="sxs-lookup"><span data-stu-id="32d8c-545">An equal sign (=)</span></span>
- <span data-ttu-id="32d8c-546">0-2 espaces blancs</span><span class="sxs-lookup"><span data-stu-id="32d8c-546">0-2 whitespace characters</span></span>
- <span data-ttu-id="32d8c-547">Toute combinaison de 43 lettres majuscules ou minuscules, des chiffres, une barre oblique (/) ou un signe plus (+)</span><span class="sxs-lookup"><span data-stu-id="32d8c-547">Any combination of 43 lower- or uppercase letters, digits, forward slash (/), or plus sign (+)</span></span>
- <span data-ttu-id="32d8c-548">Signe égal (=)</span><span class="sxs-lookup"><span data-stu-id="32d8c-548">An equal sign (=)</span></span>

### <a name="checksum"></a><span data-ttu-id="32d8c-549">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="32d8c-549">Checksum</span></span>

<span data-ttu-id="32d8c-550">Non</span><span class="sxs-lookup"><span data-stu-id="32d8c-550">No</span></span>

### <a name="definition"></a><span data-ttu-id="32d8c-551">Définition</span><span class="sxs-lookup"><span data-stu-id="32d8c-551">Definition</span></span>

<span data-ttu-id="32d8c-552">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="32d8c-552">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="32d8c-553">L’expression régulière CEP_Regex_AzureIoTConnectionString trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="32d8c-553">The regular expression CEP_Regex_AzureIoTConnectionString finds content that matches the pattern.</span></span>
- <span data-ttu-id="32d8c-554">L’expression régulière CEP_CommonExampleKeywords ne trouve **pas** le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="32d8c-554">The regular expression CEP_CommonExampleKeywords does **not** find content that matches the pattern.</span></span>

```xml
<!--Azure IoT Connection String-->
<Entity id="0b34bec3-d5d6-4974-b7b0-dcdb5c90c29d" patternsProximity="300" recommendedConfidence="85">
  <Pattern confidenceLevel="85">
        <IdMatch idRef="CEP_Regex_AzureIoTConnectionString" />
        <Any minMatches="0" maxMatches="0">
            <Match idRef="CEP_CommonExampleKeywords" />
        </Any>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="32d8c-555">Mots clés</span><span class="sxs-lookup"><span data-stu-id="32d8c-555">Keywords</span></span>

#### <a name="cep_commonexamplekeywords"></a><span data-ttu-id="32d8c-556">CEP_CommonExampleKeywords</span><span class="sxs-lookup"><span data-stu-id="32d8c-556">CEP_CommonExampleKeywords</span></span>

<span data-ttu-id="32d8c-557">(Notez que techniquement, ce type d’informations sensibles identifie ces mots clés à l’aide d’une expression régulière, et non d’une liste de mots clés.)</span><span class="sxs-lookup"><span data-stu-id="32d8c-557">(Note that technically, this sensitive information type identifies these keywords by using a regular expression, not a keyword list.)</span></span>

- <span data-ttu-id="32d8c-558">contoso</span><span class="sxs-lookup"><span data-stu-id="32d8c-558">contoso</span></span>
- <span data-ttu-id="32d8c-559">société</span><span class="sxs-lookup"><span data-stu-id="32d8c-559">fabrikam</span></span>
- <span data-ttu-id="32d8c-560">Northwind</span><span class="sxs-lookup"><span data-stu-id="32d8c-560">northwind</span></span>
- <span data-ttu-id="32d8c-561">immédiatement</span><span class="sxs-lookup"><span data-stu-id="32d8c-561">sandbox</span></span>
- <span data-ttu-id="32d8c-562">onebox</span><span class="sxs-lookup"><span data-stu-id="32d8c-562">onebox</span></span>
- <span data-ttu-id="32d8c-563">hôte</span><span class="sxs-lookup"><span data-stu-id="32d8c-563">localhost</span></span>
- <span data-ttu-id="32d8c-564">bouclage</span><span class="sxs-lookup"><span data-stu-id="32d8c-564">127.0.0.1</span></span>
- <span data-ttu-id="32d8c-565">testacs.</span><span class="sxs-lookup"><span data-stu-id="32d8c-565">testacs.</span></span><!--no-hyperlink--><span data-ttu-id="32d8c-566">com</span><span class="sxs-lookup"><span data-stu-id="32d8c-566">com</span></span>
- <span data-ttu-id="32d8c-567">s-int.</span><span class="sxs-lookup"><span data-stu-id="32d8c-567">s-int.</span></span><!--no-hyperlink--><span data-ttu-id="32d8c-568">NET</span><span class="sxs-lookup"><span data-stu-id="32d8c-568">net</span></span>

## <a name="azure-publish-setting-password"></a><span data-ttu-id="32d8c-569">Mot de passe de paramètre de publication Azure</span><span class="sxs-lookup"><span data-stu-id="32d8c-569">Azure Publish Setting Password</span></span>

### <a name="format"></a><span data-ttu-id="32d8c-570">Format</span><span class="sxs-lookup"><span data-stu-id="32d8c-570">Format</span></span>

<span data-ttu-id="32d8c-571">La chaîne « userpwd = » suivie d’une chaîne alphanumérique.</span><span class="sxs-lookup"><span data-stu-id="32d8c-571">The string "userpwd=" followed by an alphanumeric string.</span></span>

### <a name="pattern"></a><span data-ttu-id="32d8c-572">Modèle</span><span class="sxs-lookup"><span data-stu-id="32d8c-572">Pattern</span></span>

- <span data-ttu-id="32d8c-573">La chaîne « userpwd = »</span><span class="sxs-lookup"><span data-stu-id="32d8c-573">The string "userpwd="</span></span>
- <span data-ttu-id="32d8c-574">N’importe quelle combinaison de 60 lettres minuscules ou chiffres</span><span class="sxs-lookup"><span data-stu-id="32d8c-574">Any combination of 60 lowercase letters or digits</span></span>
- <span data-ttu-id="32d8c-575">Guillemet (")</span><span class="sxs-lookup"><span data-stu-id="32d8c-575">A quotation mark (")</span></span>

### <a name="checksum"></a><span data-ttu-id="32d8c-576">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="32d8c-576">Checksum</span></span>

<span data-ttu-id="32d8c-577">Non</span><span class="sxs-lookup"><span data-stu-id="32d8c-577">No</span></span>

### <a name="definition"></a><span data-ttu-id="32d8c-578">Définition</span><span class="sxs-lookup"><span data-stu-id="32d8c-578">Definition</span></span>

<span data-ttu-id="32d8c-579">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="32d8c-579">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="32d8c-580">L’expression régulière CEP_Regex_AzurePublishSettingPasswords trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="32d8c-580">The regular expression CEP_Regex_AzurePublishSettingPasswords finds content that matches the pattern.</span></span>
- <span data-ttu-id="32d8c-581">L’expression régulière CEP_CommonExampleKeywords ne trouve **pas** le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="32d8c-581">The regular expression CEP_CommonExampleKeywords does **not** find content that matches the pattern.</span></span>


```xml
<!--Azure Publish Setting Password-->
<Entity id="75f4cc8a-a68e-49e5-89ce-fa8f03d286a5" patternsProximity="300" recommendedConfidence="85">
  <Pattern confidenceLevel="85">
       <IdMatch idRef="CEP_Regex_AzurePublishSettingPasswords" />
       <Any minMatches="0" maxMatches="0">
           <Match idRef="CEP_CommonExampleKeywords" />
       </Any>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="32d8c-582">Mots clés</span><span class="sxs-lookup"><span data-stu-id="32d8c-582">Keywords</span></span>

#### <a name="cep_commonexamplekeywords"></a><span data-ttu-id="32d8c-583">CEP_CommonExampleKeywords</span><span class="sxs-lookup"><span data-stu-id="32d8c-583">CEP_CommonExampleKeywords</span></span>

<span data-ttu-id="32d8c-584">(Notez que techniquement, ce type d’informations sensibles identifie ces mots clés à l’aide d’une expression régulière, et non d’une liste de mots clés.)</span><span class="sxs-lookup"><span data-stu-id="32d8c-584">(Note that technically, this sensitive information type identifies these keywords by using a regular expression, not a keyword list.)</span></span>

- <span data-ttu-id="32d8c-585">contoso</span><span class="sxs-lookup"><span data-stu-id="32d8c-585">contoso</span></span>
- <span data-ttu-id="32d8c-586">société</span><span class="sxs-lookup"><span data-stu-id="32d8c-586">fabrikam</span></span>
- <span data-ttu-id="32d8c-587">Northwind</span><span class="sxs-lookup"><span data-stu-id="32d8c-587">northwind</span></span>
- <span data-ttu-id="32d8c-588">immédiatement</span><span class="sxs-lookup"><span data-stu-id="32d8c-588">sandbox</span></span>
- <span data-ttu-id="32d8c-589">onebox</span><span class="sxs-lookup"><span data-stu-id="32d8c-589">onebox</span></span>
- <span data-ttu-id="32d8c-590">hôte</span><span class="sxs-lookup"><span data-stu-id="32d8c-590">localhost</span></span>
- <span data-ttu-id="32d8c-591">bouclage</span><span class="sxs-lookup"><span data-stu-id="32d8c-591">127.0.0.1</span></span>
- <span data-ttu-id="32d8c-592">testacs.</span><span class="sxs-lookup"><span data-stu-id="32d8c-592">testacs.</span></span><!--no-hyperlink--><span data-ttu-id="32d8c-593">com</span><span class="sxs-lookup"><span data-stu-id="32d8c-593">com</span></span>
- <span data-ttu-id="32d8c-594">s-int.</span><span class="sxs-lookup"><span data-stu-id="32d8c-594">s-int.</span></span><!--no-hyperlink--><span data-ttu-id="32d8c-595">NET</span><span class="sxs-lookup"><span data-stu-id="32d8c-595">net</span></span>

## <a name="azure-redis-cache-connection-string"></a><span data-ttu-id="32d8c-596">Chaîne de connexion au cache des inversions Azure</span><span class="sxs-lookup"><span data-stu-id="32d8c-596">Azure Redis Cache Connection String</span></span>

### <a name="format"></a><span data-ttu-id="32d8c-597">Format</span><span class="sxs-lookup"><span data-stu-id="32d8c-597">Format</span></span>

<span data-ttu-id="32d8c-598">La chaîne «ReDim. cache. Windows.</span><span class="sxs-lookup"><span data-stu-id="32d8c-598">The string "redis.cache.windows.</span></span><!--no-hyperlink--><span data-ttu-id="32d8c-599">NET "suivi des caractères et des chaînes décrits dans le modèle ci-dessous, y compris la chaîne" password "ou" PWD ".</span><span class="sxs-lookup"><span data-stu-id="32d8c-599">net" followed by the characters and strings outlined in the pattern below, including the string "password" or "pwd".</span></span>

### <a name="pattern"></a><span data-ttu-id="32d8c-600">Modèle</span><span class="sxs-lookup"><span data-stu-id="32d8c-600">Pattern</span></span>

- <span data-ttu-id="32d8c-601">La chaîne «ReDim. cache. Windows.</span><span class="sxs-lookup"><span data-stu-id="32d8c-601">The string "redis.cache.windows.</span></span><!--no-hyperlink--><span data-ttu-id="32d8c-602">NET</span><span class="sxs-lookup"><span data-stu-id="32d8c-602">net"</span></span>
- <span data-ttu-id="32d8c-603">N’importe quelle combinaison entre 1-200 majuscules ou minuscules, des chiffres, des symboles, des caractères spéciaux ou des espaces</span><span class="sxs-lookup"><span data-stu-id="32d8c-603">Any combination of between 1-200 lower- or uppercase letters, digits, symbols, special characters, or spaces</span></span>
- <span data-ttu-id="32d8c-604">La chaîne « password » ou « pwd »</span><span class="sxs-lookup"><span data-stu-id="32d8c-604">The string "password" or "pwd"</span></span>
- <span data-ttu-id="32d8c-605">0-2 espaces blancs</span><span class="sxs-lookup"><span data-stu-id="32d8c-605">0-2 whitespace characters</span></span>
- <span data-ttu-id="32d8c-606">Signe égal (=)</span><span class="sxs-lookup"><span data-stu-id="32d8c-606">An equal sign (=)</span></span>
- <span data-ttu-id="32d8c-607">0-2 espaces blancs</span><span class="sxs-lookup"><span data-stu-id="32d8c-607">0-2 whitespace characters</span></span>
- <span data-ttu-id="32d8c-608">Toute combinaison de 43 caractères majuscules ou minuscules, des chiffres, une barre oblique (/) ou un signe plus (+)</span><span class="sxs-lookup"><span data-stu-id="32d8c-608">Any combination of 43 characters that are lower- or uppercase letters, digits, forward slash (/), or plus sign (+)</span></span>
- <span data-ttu-id="32d8c-609">Signe égal (=)</span><span class="sxs-lookup"><span data-stu-id="32d8c-609">An equal sign (=)</span></span>

### <a name="checksum"></a><span data-ttu-id="32d8c-610">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="32d8c-610">Checksum</span></span>

<span data-ttu-id="32d8c-611">Non</span><span class="sxs-lookup"><span data-stu-id="32d8c-611">No</span></span>

### <a name="definition"></a><span data-ttu-id="32d8c-612">Définition</span><span class="sxs-lookup"><span data-stu-id="32d8c-612">Definition</span></span>

<span data-ttu-id="32d8c-613">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="32d8c-613">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="32d8c-614">L’expression régulière CEP_Regex_AzureRedisCacheConnectionString trouve le contenu qui correspond au modèle..</span><span class="sxs-lookup"><span data-stu-id="32d8c-614">The regular expression CEP_Regex_AzureRedisCacheConnectionString finds content that matches the pattern..</span></span>
- <span data-ttu-id="32d8c-615">L’expression régulière CEP_CommonExampleKeywords ne trouve **pas** le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="32d8c-615">The regular expression CEP_CommonExampleKeywords does **not** find content that matches the pattern.</span></span>

```xml
<!--Azure Redis Cache Connection String-->
<Entity id="095a7e6c-efd8-46d5-af7b-5298d53a49fc" patternsProximity="300" recommendedConfidence="85">
  <Pattern confidenceLevel="85">
        <IdMatch idRef="CEP_Regex_AzureRedisCacheConnectionString" />
        <Any minMatches="0" maxMatches="0">
            <Match idRef="CEP_CommonExampleKeywords" />
        </Any>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="32d8c-616">Mots clés</span><span class="sxs-lookup"><span data-stu-id="32d8c-616">Keywords</span></span>

#### <a name="cep_commonexamplekeywords"></a><span data-ttu-id="32d8c-617">CEP_CommonExampleKeywords</span><span class="sxs-lookup"><span data-stu-id="32d8c-617">CEP_CommonExampleKeywords</span></span>

<span data-ttu-id="32d8c-618">(Notez que techniquement, ce type d’informations sensibles identifie ces mots clés à l’aide d’une expression régulière, et non d’une liste de mots clés.)</span><span class="sxs-lookup"><span data-stu-id="32d8c-618">(Note that technically, this sensitive information type identifies these keywords by using a regular expression, not a keyword list.)</span></span>

- <span data-ttu-id="32d8c-619">contoso</span><span class="sxs-lookup"><span data-stu-id="32d8c-619">contoso</span></span>
- <span data-ttu-id="32d8c-620">société</span><span class="sxs-lookup"><span data-stu-id="32d8c-620">fabrikam</span></span>
- <span data-ttu-id="32d8c-621">Northwind</span><span class="sxs-lookup"><span data-stu-id="32d8c-621">northwind</span></span>
- <span data-ttu-id="32d8c-622">immédiatement</span><span class="sxs-lookup"><span data-stu-id="32d8c-622">sandbox</span></span>
- <span data-ttu-id="32d8c-623">onebox</span><span class="sxs-lookup"><span data-stu-id="32d8c-623">onebox</span></span>
- <span data-ttu-id="32d8c-624">hôte</span><span class="sxs-lookup"><span data-stu-id="32d8c-624">localhost</span></span>
- <span data-ttu-id="32d8c-625">bouclage</span><span class="sxs-lookup"><span data-stu-id="32d8c-625">127.0.0.1</span></span>
- <span data-ttu-id="32d8c-626">testacs.</span><span class="sxs-lookup"><span data-stu-id="32d8c-626">testacs.</span></span><!--no-hyperlink--><span data-ttu-id="32d8c-627">com</span><span class="sxs-lookup"><span data-stu-id="32d8c-627">com</span></span>
- <span data-ttu-id="32d8c-628">s-int.</span><span class="sxs-lookup"><span data-stu-id="32d8c-628">s-int.</span></span><!--no-hyperlink--><span data-ttu-id="32d8c-629">NET</span><span class="sxs-lookup"><span data-stu-id="32d8c-629">net</span></span>

## <a name="azure-sas"></a><span data-ttu-id="32d8c-630">SAS Azure</span><span class="sxs-lookup"><span data-stu-id="32d8c-630">Azure SAS</span></span>

### <a name="format"></a><span data-ttu-id="32d8c-631">Format</span><span class="sxs-lookup"><span data-stu-id="32d8c-631">Format</span></span>

<span data-ttu-id="32d8c-632">La chaîne « SIG » suivie des caractères et des chaînes présentés dans le modèle ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="32d8c-632">The string "sig" followed by the characters and strings outlined in the pattern below.</span></span>

### <a name="pattern"></a><span data-ttu-id="32d8c-633">Modèle</span><span class="sxs-lookup"><span data-stu-id="32d8c-633">Pattern</span></span>

- <span data-ttu-id="32d8c-634">La chaîne « SIG »</span><span class="sxs-lookup"><span data-stu-id="32d8c-634">The string "sig"</span></span>
- <span data-ttu-id="32d8c-635">0-2 espaces blancs</span><span class="sxs-lookup"><span data-stu-id="32d8c-635">0-2 whitespace characters</span></span>
- <span data-ttu-id="32d8c-636">Signe égal (=)</span><span class="sxs-lookup"><span data-stu-id="32d8c-636">An equal sign (=)</span></span>
- <span data-ttu-id="32d8c-637">0-2 espaces blancs</span><span class="sxs-lookup"><span data-stu-id="32d8c-637">0-2 whitespace characters</span></span>
- <span data-ttu-id="32d8c-638">Toute combinaison comprise entre 43-53 caractères majuscules ou minuscules, des chiffres ou le signe pourcentage (%)</span><span class="sxs-lookup"><span data-stu-id="32d8c-638">Any combination of between 43-53 characters that are lower- or uppercase letters, digits, or the percent sign (%)</span></span>
- <span data-ttu-id="32d8c-639">La chaîne « % 3D »</span><span class="sxs-lookup"><span data-stu-id="32d8c-639">The string "%3d"</span></span>
- <span data-ttu-id="32d8c-640">Tout caractère qui n’est pas une lettre majuscule, un chiffre ou un signe de pourcentage (%)</span><span class="sxs-lookup"><span data-stu-id="32d8c-640">Any character that is not a lower- or uppercase letter, digit, or percent sign (%)</span></span>

### <a name="checksum"></a><span data-ttu-id="32d8c-641">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="32d8c-641">Checksum</span></span>

<span data-ttu-id="32d8c-642">Non</span><span class="sxs-lookup"><span data-stu-id="32d8c-642">No</span></span>

### <a name="definition"></a><span data-ttu-id="32d8c-643">Définition</span><span class="sxs-lookup"><span data-stu-id="32d8c-643">Definition</span></span>

<span data-ttu-id="32d8c-644">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="32d8c-644">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="32d8c-645">L’expression régulière CEP_Regex_AzureSAS trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="32d8c-645">The regular expression CEP_Regex_AzureSAS finds content that matches the pattern.</span></span>

```xml
<!--Azure SAS-->
<Entity id="4d235014-e564-47f4-a6fb-6ebb4a826834" patternsProximity="300" recommendedConfidence="85">
  <Pattern confidenceLevel="85">
        <IdMatch idRef="CEP_Regex_AzureSAS" />
  </Pattern>
</Entity>
```

## <a name="azure-service-bus-connection-string"></a><span data-ttu-id="32d8c-646">Chaîne de connexion au bus des services Azure</span><span class="sxs-lookup"><span data-stu-id="32d8c-646">Azure Service Bus Connection String</span></span>

### <a name="format"></a><span data-ttu-id="32d8c-647">Format</span><span class="sxs-lookup"><span data-stu-id="32d8c-647">Format</span></span>

<span data-ttu-id="32d8c-648">La chaîne « point de terminaison » suivie des caractères et des chaînes décrits dans le modèle ci-dessous, y compris les chaînes «ServiceBus. Windows.</span><span class="sxs-lookup"><span data-stu-id="32d8c-648">The string "EndPoint" followed by the characters and strings outlined in the pattern below, including the strings "servicebus.windows.</span></span><!--no-hyperlink--><span data-ttu-id="32d8c-649">NET "et" SharedAccesKey ".</span><span class="sxs-lookup"><span data-stu-id="32d8c-649">net" and "SharedAccesKey".</span></span>

### <a name="pattern"></a><span data-ttu-id="32d8c-650">Modèle</span><span class="sxs-lookup"><span data-stu-id="32d8c-650">Pattern</span></span>

- <span data-ttu-id="32d8c-651">Chaîne « point de terminaison »</span><span class="sxs-lookup"><span data-stu-id="32d8c-651">The string "EndPoint"</span></span>
- <span data-ttu-id="32d8c-652">0-2 espaces blancs</span><span class="sxs-lookup"><span data-stu-id="32d8c-652">0-2 whitespace characters</span></span>
- <span data-ttu-id="32d8c-653">Signe égal (=)</span><span class="sxs-lookup"><span data-stu-id="32d8c-653">An equal sign (=)</span></span>
- <span data-ttu-id="32d8c-654">0-2 espaces blancs</span><span class="sxs-lookup"><span data-stu-id="32d8c-654">0-2 whitespace characters</span></span>
- <span data-ttu-id="32d8c-655">N’importe quelle combinaison entre 1-200 majuscules ou minuscules, des chiffres, des symboles, des caractères spéciaux ou des espaces</span><span class="sxs-lookup"><span data-stu-id="32d8c-655">Any combination of between 1-200 lower- or uppercase letters, digits, symbols, special characters, or spaces</span></span>
- <span data-ttu-id="32d8c-656">La chaîne «ServiceBus. Windows.</span><span class="sxs-lookup"><span data-stu-id="32d8c-656">The string "servicebus.windows.</span></span><!--no-hyperlink--><span data-ttu-id="32d8c-657">NET</span><span class="sxs-lookup"><span data-stu-id="32d8c-657">net"</span></span>
- <span data-ttu-id="32d8c-658">N’importe quelle combinaison entre 1-200 majuscules ou minuscules, des chiffres, des symboles, des caractères spéciaux ou des espaces</span><span class="sxs-lookup"><span data-stu-id="32d8c-658">Any combination of between 1-200 lower- or uppercase letters, digits, symbols, special characters, or spaces</span></span>
- <span data-ttu-id="32d8c-659">La chaîne « SharedAccessKey »</span><span class="sxs-lookup"><span data-stu-id="32d8c-659">The string "SharedAccessKey"</span></span>
- <span data-ttu-id="32d8c-660">0-2 espaces blancs</span><span class="sxs-lookup"><span data-stu-id="32d8c-660">0-2 whitespace characters</span></span>
- <span data-ttu-id="32d8c-661">Signe égal (=)</span><span class="sxs-lookup"><span data-stu-id="32d8c-661">An equal sign (=)</span></span>
- <span data-ttu-id="32d8c-662">0-2 espaces blancs</span><span class="sxs-lookup"><span data-stu-id="32d8c-662">0-2 whitespace characters</span></span>
- <span data-ttu-id="32d8c-663">Toute combinaison de 43 caractères majuscules ou minuscules, des chiffres, une barre oblique (/) ou un signe plus (+)</span><span class="sxs-lookup"><span data-stu-id="32d8c-663">Any combination of 43 characters that are lower- or uppercase letters, digits, forward slash (/), or plus sign (+)</span></span>
- <span data-ttu-id="32d8c-664">Signe égal (=)</span><span class="sxs-lookup"><span data-stu-id="32d8c-664">An equal sign (=)</span></span>

### <a name="checksum"></a><span data-ttu-id="32d8c-665">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="32d8c-665">Checksum</span></span>

<span data-ttu-id="32d8c-666">Non</span><span class="sxs-lookup"><span data-stu-id="32d8c-666">No</span></span>

### <a name="definition"></a><span data-ttu-id="32d8c-667">Définition</span><span class="sxs-lookup"><span data-stu-id="32d8c-667">Definition</span></span>

<span data-ttu-id="32d8c-668">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="32d8c-668">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="32d8c-669">L’expression régulière CEP_Regex_AzureServiceBusConnectionString trouve le contenu qui correspond au modèle..</span><span class="sxs-lookup"><span data-stu-id="32d8c-669">The regular expression CEP_Regex_AzureServiceBusConnectionString finds content that matches the pattern..</span></span>
- <span data-ttu-id="32d8c-670">L’expression régulière CEP_CommonExampleKeywords ne trouve **pas** le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="32d8c-670">The regular expression CEP_CommonExampleKeywords does **not** find content that matches the pattern.</span></span>

```xml
<!--Azure Service Bus Connection String-->
<Entity id="b9a6578f-a83f-4fcd-bf44-2130bae49a6f" patternsProximity="300" recommendedConfidence="85">
  <Pattern confidenceLevel="85">
        <IdMatch idRef="CEP_Regex_AzureServiceBusConnectionString" />
        <Any minMatches="0" maxMatches="0">
            <Match idRef="CEP_CommonExampleKeywords" />
        </Any>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="32d8c-671">Mots clés</span><span class="sxs-lookup"><span data-stu-id="32d8c-671">Keywords</span></span>

#### <a name="cep_commonexamplekeywords"></a><span data-ttu-id="32d8c-672">CEP_CommonExampleKeywords</span><span class="sxs-lookup"><span data-stu-id="32d8c-672">CEP_CommonExampleKeywords</span></span>

<span data-ttu-id="32d8c-673">(Notez que techniquement, ce type d’informations sensibles identifie ces mots clés à l’aide d’une expression régulière, et non d’une liste de mots clés.)</span><span class="sxs-lookup"><span data-stu-id="32d8c-673">(Note that technically, this sensitive information type identifies these keywords by using a regular expression, not a keyword list.)</span></span>

- <span data-ttu-id="32d8c-674">contoso</span><span class="sxs-lookup"><span data-stu-id="32d8c-674">contoso</span></span>
- <span data-ttu-id="32d8c-675">société</span><span class="sxs-lookup"><span data-stu-id="32d8c-675">fabrikam</span></span>
- <span data-ttu-id="32d8c-676">Northwind</span><span class="sxs-lookup"><span data-stu-id="32d8c-676">northwind</span></span>
- <span data-ttu-id="32d8c-677">immédiatement</span><span class="sxs-lookup"><span data-stu-id="32d8c-677">sandbox</span></span>
- <span data-ttu-id="32d8c-678">onebox</span><span class="sxs-lookup"><span data-stu-id="32d8c-678">onebox</span></span>
- <span data-ttu-id="32d8c-679">hôte</span><span class="sxs-lookup"><span data-stu-id="32d8c-679">localhost</span></span>
- <span data-ttu-id="32d8c-680">bouclage</span><span class="sxs-lookup"><span data-stu-id="32d8c-680">127.0.0.1</span></span>
- <span data-ttu-id="32d8c-681">testacs.</span><span class="sxs-lookup"><span data-stu-id="32d8c-681">testacs.</span></span><!--no-hyperlink--><span data-ttu-id="32d8c-682">com</span><span class="sxs-lookup"><span data-stu-id="32d8c-682">com</span></span>
- <span data-ttu-id="32d8c-683">s-int.</span><span class="sxs-lookup"><span data-stu-id="32d8c-683">s-int.</span></span><!--no-hyperlink--><span data-ttu-id="32d8c-684">NET</span><span class="sxs-lookup"><span data-stu-id="32d8c-684">net</span></span>

## <a name="azure-storage-account-key"></a><span data-ttu-id="32d8c-685">Clé de compte de stockage Azure</span><span class="sxs-lookup"><span data-stu-id="32d8c-685">Azure Storage Account Key</span></span>

### <a name="format"></a><span data-ttu-id="32d8c-686">Format</span><span class="sxs-lookup"><span data-stu-id="32d8c-686">Format</span></span>

<span data-ttu-id="32d8c-687">La chaîne « DefaultEndpointsProtocol » suivie des caractères et des chaînes décrits dans le modèle ci-dessous, y compris la chaîne « AccountKey ».</span><span class="sxs-lookup"><span data-stu-id="32d8c-687">The string "DefaultEndpointsProtocol" followed by the characters and strings outlined in the pattern below, including the string "AccountKey".</span></span>

### <a name="pattern"></a><span data-ttu-id="32d8c-688">Modèle</span><span class="sxs-lookup"><span data-stu-id="32d8c-688">Pattern</span></span>

- <span data-ttu-id="32d8c-689">La chaîne « DefaultEndpointsProtocol »</span><span class="sxs-lookup"><span data-stu-id="32d8c-689">The string "DefaultEndpointsProtocol"</span></span>
- <span data-ttu-id="32d8c-690">0-2 espaces blancs</span><span class="sxs-lookup"><span data-stu-id="32d8c-690">0-2 whitespace characters</span></span>
- <span data-ttu-id="32d8c-691">Signe égal (=)</span><span class="sxs-lookup"><span data-stu-id="32d8c-691">An equal sign (=)</span></span>
- <span data-ttu-id="32d8c-692">0-2 espaces blancs</span><span class="sxs-lookup"><span data-stu-id="32d8c-692">0-2 whitespace characters</span></span>
- <span data-ttu-id="32d8c-693">N’importe quelle combinaison entre 1-200 majuscules ou minuscules, des chiffres, des symboles, des caractères spéciaux ou des espaces</span><span class="sxs-lookup"><span data-stu-id="32d8c-693">Any combination of between 1-200 lower- or uppercase letters, digits, symbols, special characters, or spaces</span></span>
- <span data-ttu-id="32d8c-694">La chaîne « AccountKey »</span><span class="sxs-lookup"><span data-stu-id="32d8c-694">The string "AccountKey"</span></span>
- <span data-ttu-id="32d8c-695">0-2 espaces blancs</span><span class="sxs-lookup"><span data-stu-id="32d8c-695">0-2 whitespace characters</span></span>
- <span data-ttu-id="32d8c-696">Signe égal (=)</span><span class="sxs-lookup"><span data-stu-id="32d8c-696">An equal sign (=)</span></span>
- <span data-ttu-id="32d8c-697">0-2 espaces blancs</span><span class="sxs-lookup"><span data-stu-id="32d8c-697">0-2 whitespace characters</span></span>
- <span data-ttu-id="32d8c-698">Toute combinaison de 86 caractères majuscules ou minuscules, des chiffres, une barre oblique (/) ou un signe plus (+)</span><span class="sxs-lookup"><span data-stu-id="32d8c-698">Any combination of 86 characters that are lower- or uppercase letters, digits, forward slash (/), or plus sign (+)</span></span>
- <span data-ttu-id="32d8c-699">Deux signes égal (=)</span><span class="sxs-lookup"><span data-stu-id="32d8c-699">Two equal signs (=)</span></span>

### <a name="checksum"></a><span data-ttu-id="32d8c-700">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="32d8c-700">Checksum</span></span>

<span data-ttu-id="32d8c-701">Non</span><span class="sxs-lookup"><span data-stu-id="32d8c-701">No</span></span>

### <a name="definition"></a><span data-ttu-id="32d8c-702">Définition</span><span class="sxs-lookup"><span data-stu-id="32d8c-702">Definition</span></span>

<span data-ttu-id="32d8c-703">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="32d8c-703">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="32d8c-704">L’expression régulière CEP_Regex_AzureStorageAccountKey trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="32d8c-704">The regular expression CEP_Regex_AzureStorageAccountKey finds content that matches the pattern.</span></span>
- <span data-ttu-id="32d8c-705">L’expression régulière CEP_AzureEmulatorStorageAccountFilter ne trouve **pas** le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="32d8c-705">The regular expression CEP_AzureEmulatorStorageAccountFilter does **not** find content that matches the pattern.</span></span>
- <span data-ttu-id="32d8c-706">L’expression régulière CEP_CommonExampleKeywords ne trouve **pas** le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="32d8c-706">The regular expression CEP_CommonExampleKeywords does **not** find content that matches the pattern.</span></span>

```xml
<!--Azure Storage Account Key-->
<Entity id="c7bc98e8-551a-4c35-a92d-d2c8cda714a7" patternsProximity="300" recommendedConfidence="85">
  <Pattern confidenceLevel="85">
        <IdMatch idRef="CEP_Regex_AzureStorageAccountKey" />
        <Any minMatches="0" maxMatches="0">
            <Match idRef="CEP_AzureEmulatorStorageAccountFilter" />
            <Match idRef="CEP_CommonExampleKeywords" />
        </Any>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="32d8c-707">Mots clés</span><span class="sxs-lookup"><span data-stu-id="32d8c-707">Keywords</span></span>

#### <a name="cep_azureemulatorstorageaccountfilter"></a><span data-ttu-id="32d8c-708">CEP_AzureEmulatorStorageAccountFilter</span><span class="sxs-lookup"><span data-stu-id="32d8c-708">CEP_AzureEmulatorStorageAccountFilter</span></span>

<span data-ttu-id="32d8c-709">(Notez que techniquement, ce type d’informations sensibles identifie ces mots clés à l’aide d’une expression régulière, et non d’une liste de mots clés.)</span><span class="sxs-lookup"><span data-stu-id="32d8c-709">(Note that technically, this sensitive information type identifies these keywords by using a regular expression, not a keyword list.)</span></span>

- <span data-ttu-id="32d8c-710">Eby8vdM02xNOcqFlqUwJPLlmEtlCDXJ1OUzFT50uSRZ6IFsuFq2UVErCz4I6tq/K1SZFPTOtr/KBHBeksoGMGw = =</span><span class="sxs-lookup"><span data-stu-id="32d8c-710">Eby8vdM02xNOcqFlqUwJPLlmEtlCDXJ1OUzFT50uSRZ6IFsuFq2UVErCz4I6tq/K1SZFPTOtr/KBHBeksoGMGw==</span></span>

#### <a name="cep_commonexamplekeywords"></a><span data-ttu-id="32d8c-711">CEP_CommonExampleKeywords</span><span class="sxs-lookup"><span data-stu-id="32d8c-711">CEP_CommonExampleKeywords</span></span>

<span data-ttu-id="32d8c-712">(Notez que techniquement, ce type d’informations sensibles identifie ces mots clés à l’aide d’une expression régulière, et non d’une liste de mots clés.)</span><span class="sxs-lookup"><span data-stu-id="32d8c-712">(Note that technically, this sensitive information type identifies these keywords by using a regular expression, not a keyword list.)</span></span>

- <span data-ttu-id="32d8c-713">contoso</span><span class="sxs-lookup"><span data-stu-id="32d8c-713">contoso</span></span>
- <span data-ttu-id="32d8c-714">société</span><span class="sxs-lookup"><span data-stu-id="32d8c-714">fabrikam</span></span>
- <span data-ttu-id="32d8c-715">Northwind</span><span class="sxs-lookup"><span data-stu-id="32d8c-715">northwind</span></span>
- <span data-ttu-id="32d8c-716">immédiatement</span><span class="sxs-lookup"><span data-stu-id="32d8c-716">sandbox</span></span>
- <span data-ttu-id="32d8c-717">onebox</span><span class="sxs-lookup"><span data-stu-id="32d8c-717">onebox</span></span>
- <span data-ttu-id="32d8c-718">hôte</span><span class="sxs-lookup"><span data-stu-id="32d8c-718">localhost</span></span>
- <span data-ttu-id="32d8c-719">bouclage</span><span class="sxs-lookup"><span data-stu-id="32d8c-719">127.0.0.1</span></span>
- <span data-ttu-id="32d8c-720">testacs.</span><span class="sxs-lookup"><span data-stu-id="32d8c-720">testacs.</span></span><!--no-hyperlink--><span data-ttu-id="32d8c-721">com</span><span class="sxs-lookup"><span data-stu-id="32d8c-721">com</span></span>
- <span data-ttu-id="32d8c-722">s-int.</span><span class="sxs-lookup"><span data-stu-id="32d8c-722">s-int.</span></span><!--no-hyperlink--><span data-ttu-id="32d8c-723">NET</span><span class="sxs-lookup"><span data-stu-id="32d8c-723">net</span></span>

## <a name="azure-storage-account-key-generic"></a><span data-ttu-id="32d8c-724">Clé de compte de stockage Azure (Générique)</span><span class="sxs-lookup"><span data-stu-id="32d8c-724">Azure Storage Account Key (Generic)</span></span>

### <a name="format"></a><span data-ttu-id="32d8c-725">Format</span><span class="sxs-lookup"><span data-stu-id="32d8c-725">Format</span></span>

<span data-ttu-id="32d8c-726">Toute combinaison de 86 lettres majuscules ou minuscules, des chiffres, la barre oblique (/) ou le signe plus (+), précédée ou suivie des caractères décrits dans le modèle ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="32d8c-726">Any combination of 86 lower- or uppercase letters, digits, the forward slash (/), or plus sign (+), preceded or followed by the characters outlined in the pattern below.</span></span>

### <a name="pattern"></a><span data-ttu-id="32d8c-727">Modèle</span><span class="sxs-lookup"><span data-stu-id="32d8c-727">Pattern</span></span>

- <span data-ttu-id="32d8c-728">0-1 du symbole supérieur à (>), apostrophe ('), signe égal (=), guillemet (") ou dièse (#)</span><span class="sxs-lookup"><span data-stu-id="32d8c-728">0-1 of the greater than symbol (>), apostrophe ('), equal sign (=), quotation mark ("), or number sign (#)</span></span>
- <span data-ttu-id="32d8c-729">Toute combinaison de 86 caractères majuscules ou minuscules, des chiffres, la barre oblique (/) ou le signe plus (+)</span><span class="sxs-lookup"><span data-stu-id="32d8c-729">Any combination of 86 characters that are lower- or uppercase letters, digits, the forward slash (/), or plus sign (+)</span></span>
- <span data-ttu-id="32d8c-730">Deux signes égal (=)</span><span class="sxs-lookup"><span data-stu-id="32d8c-730">Two equal signs (=)</span></span>


### <a name="checksum"></a><span data-ttu-id="32d8c-731">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="32d8c-731">Checksum</span></span>

<span data-ttu-id="32d8c-732">Non</span><span class="sxs-lookup"><span data-stu-id="32d8c-732">No</span></span>

### <a name="definition"></a><span data-ttu-id="32d8c-733">Définition</span><span class="sxs-lookup"><span data-stu-id="32d8c-733">Definition</span></span>

<span data-ttu-id="32d8c-734">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="32d8c-734">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="32d8c-735">L’expression régulière CEP_Regex_AzureStorageAccountKeyGeneric trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="32d8c-735">The regular expression CEP_Regex_AzureStorageAccountKeyGeneric finds content that matches the pattern.</span></span>

```xml
<!--Azure Storage Account Key (Generic)-->
<Entity id="7ff41bd0-5419-4523-91d6-383b3a37f084" patternsProximity="300" recommendedConfidence="85">
  <Pattern confidenceLevel="85">
        <IdMatch idRef="CEP_Regex_AzureStorageAccountKeyGeneric" />
  </Pattern>
</Entity>
```

## <a name="belgium-national-number"></a><span data-ttu-id="32d8c-736">Numéro national Belgique</span><span class="sxs-lookup"><span data-stu-id="32d8c-736">Belgium National Number</span></span>

### <a name="format"></a><span data-ttu-id="32d8c-737">Format</span><span class="sxs-lookup"><span data-stu-id="32d8c-737">Format</span></span>

<span data-ttu-id="32d8c-738">11 chiffres plus des délimiteurs</span><span class="sxs-lookup"><span data-stu-id="32d8c-738">11 digits plus delimiters</span></span>

### <a name="pattern"></a><span data-ttu-id="32d8c-739">Modèle</span><span class="sxs-lookup"><span data-stu-id="32d8c-739">Pattern</span></span>

<span data-ttu-id="32d8c-740">11 chiffres plus des délimiteurs :</span><span class="sxs-lookup"><span data-stu-id="32d8c-740">11 digits plus delimiters:</span></span>
- <span data-ttu-id="32d8c-741">Six chiffres et deux points au format AA.MM.JJ pour la date de naissance </span><span class="sxs-lookup"><span data-stu-id="32d8c-741">Six digits and two periods in the format YY.MM.DD for date of birth</span></span> 
- <span data-ttu-id="32d8c-742">Un trait d’union</span><span class="sxs-lookup"><span data-stu-id="32d8c-742">A hyphen</span></span> 
- <span data-ttu-id="32d8c-743">Trois chiffres séquentiels (impairs pour les hommes, pairs pour les femmes) </span><span class="sxs-lookup"><span data-stu-id="32d8c-743">Three sequential digits (odd for males, even for females)</span></span> 
- <span data-ttu-id="32d8c-744">Un point</span><span class="sxs-lookup"><span data-stu-id="32d8c-744">A period</span></span> 
- <span data-ttu-id="32d8c-745">Deux chiffres de contrôle</span><span class="sxs-lookup"><span data-stu-id="32d8c-745">Two digits that are a check digit</span></span>

### <a name="checksum"></a><span data-ttu-id="32d8c-746">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="32d8c-746">Checksum</span></span>

<span data-ttu-id="32d8c-747">Oui</span><span class="sxs-lookup"><span data-stu-id="32d8c-747">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="32d8c-748">Définition</span><span class="sxs-lookup"><span data-stu-id="32d8c-748">Definition</span></span>

<span data-ttu-id="32d8c-749">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="32d8c-749">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="32d8c-750">La fonction Func_belgium_national_number trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="32d8c-750">The function Func_belgium_national_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="32d8c-751">Un mot clé figurant dans la liste Keyword_belgium_national_number est trouvé.</span><span class="sxs-lookup"><span data-stu-id="32d8c-751">A keyword from Keyword_belgium_national_number is found.</span></span>
- <span data-ttu-id="32d8c-752">La somme de contrôle est correcte.</span><span class="sxs-lookup"><span data-stu-id="32d8c-752">The checksum passes.</span></span>

```xml
<!-- Belgium National Number -->
  <Entity id="fb969c9e-0fd1-4b18-8091-a2123c5e6a54" recommendedConfidence="75" patternsProximity="300">
   <Pattern confidenceLevel="75">
     <IdMatch idRef="Func_belgium_national_number"/>
     <Match idRef="Keyword_belgium_national_number"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="32d8c-753">Mots clés</span><span class="sxs-lookup"><span data-stu-id="32d8c-753">Keywords</span></span>

#### <a name="keyword_belgium_national_number"></a><span data-ttu-id="32d8c-754">Keyword_belgium_national_number</span><span class="sxs-lookup"><span data-stu-id="32d8c-754">Keyword_belgium_national_number</span></span>

- <span data-ttu-id="32d8c-755">Identité</span><span class="sxs-lookup"><span data-stu-id="32d8c-755">Identity</span></span>
- <span data-ttu-id="32d8c-756">Son</span><span class="sxs-lookup"><span data-stu-id="32d8c-756">Registration</span></span>
- <span data-ttu-id="32d8c-757">Identificateur</span><span class="sxs-lookup"><span data-stu-id="32d8c-757">Identification</span></span> 
- <span data-ttu-id="32d8c-758">ID</span><span class="sxs-lookup"><span data-stu-id="32d8c-758">ID</span></span> 
- <span data-ttu-id="32d8c-759">Identiteitskaart</span><span class="sxs-lookup"><span data-stu-id="32d8c-759">Identiteitskaart</span></span>
- <span data-ttu-id="32d8c-760">Registratie nummer</span><span class="sxs-lookup"><span data-stu-id="32d8c-760">Registratie nummer</span></span> 
- <span data-ttu-id="32d8c-761">Identificatie nummer</span><span class="sxs-lookup"><span data-stu-id="32d8c-761">Identificatie nummer</span></span> 
- <span data-ttu-id="32d8c-762">Identiteit</span><span class="sxs-lookup"><span data-stu-id="32d8c-762">Identiteit</span></span>
- <span data-ttu-id="32d8c-763">Registratie</span><span class="sxs-lookup"><span data-stu-id="32d8c-763">Registratie</span></span>
- <span data-ttu-id="32d8c-764">Identificatie</span><span class="sxs-lookup"><span data-stu-id="32d8c-764">Identificatie</span></span> 
- <span data-ttu-id="32d8c-765">Carte d’identité</span><span class="sxs-lookup"><span data-stu-id="32d8c-765">Carte d'identité</span></span> 
- <span data-ttu-id="32d8c-766">numéro d’immatriculation</span><span class="sxs-lookup"><span data-stu-id="32d8c-766">numéro d'immatriculation</span></span>
- <span data-ttu-id="32d8c-767">numéro d’identification</span><span class="sxs-lookup"><span data-stu-id="32d8c-767">numéro d'identification</span></span>
- <span data-ttu-id="32d8c-768">identité</span><span class="sxs-lookup"><span data-stu-id="32d8c-768">identité</span></span> 
- <span data-ttu-id="32d8c-769">inscriptions</span><span class="sxs-lookup"><span data-stu-id="32d8c-769">inscription</span></span> 
- <span data-ttu-id="32d8c-770">Identifikation</span><span class="sxs-lookup"><span data-stu-id="32d8c-770">Identifikation</span></span>
- <span data-ttu-id="32d8c-771">Identifizierung</span><span class="sxs-lookup"><span data-stu-id="32d8c-771">Identifizierung</span></span>
- <span data-ttu-id="32d8c-772">Identifikationsnummer</span><span class="sxs-lookup"><span data-stu-id="32d8c-772">Identifikationsnummer</span></span>
- <span data-ttu-id="32d8c-773">Personalausweis</span><span class="sxs-lookup"><span data-stu-id="32d8c-773">Personalausweis</span></span>
- <span data-ttu-id="32d8c-774">Registrierung</span><span class="sxs-lookup"><span data-stu-id="32d8c-774">Registrierung</span></span>
- <span data-ttu-id="32d8c-775">Registrationsnummer</span><span class="sxs-lookup"><span data-stu-id="32d8c-775">Registrationsnummer</span></span>

   
## <a name="brazil-cpf-number"></a><span data-ttu-id="32d8c-776">Numéro CPF Brésil</span><span class="sxs-lookup"><span data-stu-id="32d8c-776">Brazil CPF Number</span></span>

### <a name="format"></a><span data-ttu-id="32d8c-777">Format</span><span class="sxs-lookup"><span data-stu-id="32d8c-777">Format</span></span>

<span data-ttu-id="32d8c-778">11 chiffres qui incluent un chiffre de contrôle et peuvent ou non être mis en forme </span><span class="sxs-lookup"><span data-stu-id="32d8c-778">11 digits that include a check digit and can be formatted or unformatted</span></span>

### <a name="pattern"></a><span data-ttu-id="32d8c-779">Modèle</span><span class="sxs-lookup"><span data-stu-id="32d8c-779">Pattern</span></span>

<span data-ttu-id="32d8c-780">Avec</span><span class="sxs-lookup"><span data-stu-id="32d8c-780">Formatted:</span></span>
- <span data-ttu-id="32d8c-781">Trois chiffres</span><span class="sxs-lookup"><span data-stu-id="32d8c-781">Three digits</span></span> 
- <span data-ttu-id="32d8c-782">Un point </span><span class="sxs-lookup"><span data-stu-id="32d8c-782">A period</span></span> 
- <span data-ttu-id="32d8c-783">Trois chiffres</span><span class="sxs-lookup"><span data-stu-id="32d8c-783">Three digits</span></span> 
- <span data-ttu-id="32d8c-784">Un point </span><span class="sxs-lookup"><span data-stu-id="32d8c-784">A period</span></span> 
- <span data-ttu-id="32d8c-785">Trois chiffres</span><span class="sxs-lookup"><span data-stu-id="32d8c-785">Three digits</span></span> 
- <span data-ttu-id="32d8c-786">Un trait d’union </span><span class="sxs-lookup"><span data-stu-id="32d8c-786">A hyphen</span></span> 
- <span data-ttu-id="32d8c-787">Deux chiffres de contrôle</span><span class="sxs-lookup"><span data-stu-id="32d8c-787">Two digits which are check digits</span></span>

<span data-ttu-id="32d8c-788">Non</span><span class="sxs-lookup"><span data-stu-id="32d8c-788">Unformatted:</span></span>
- <span data-ttu-id="32d8c-789">11 chiffres où les deux derniers sont des chiffres de contrôle</span><span class="sxs-lookup"><span data-stu-id="32d8c-789">11 digits where the last two digits are check digits</span></span>

### <a name="checksum"></a><span data-ttu-id="32d8c-790">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="32d8c-790">Checksum</span></span>

<span data-ttu-id="32d8c-791">Oui</span><span class="sxs-lookup"><span data-stu-id="32d8c-791">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="32d8c-792">Définition</span><span class="sxs-lookup"><span data-stu-id="32d8c-792">Definition</span></span>

<span data-ttu-id="32d8c-793">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="32d8c-793">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="32d8c-794">La fonction Func_brazil_cpf trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="32d8c-794">The function Func_brazil_cpf finds content that matches the pattern.</span></span>
- <span data-ttu-id="32d8c-795">Un mot clé figurant dans la liste Keyword_brazil_cpf est trouvé.</span><span class="sxs-lookup"><span data-stu-id="32d8c-795">A keyword from Keyword_brazil_cpf is found.</span></span>
- <span data-ttu-id="32d8c-796">La somme de contrôle est correcte.</span><span class="sxs-lookup"><span data-stu-id="32d8c-796">The checksum passes.</span></span>

<span data-ttu-id="32d8c-797">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="32d8c-797">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="32d8c-798">La fonction Func_brazil_cpf trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="32d8c-798">The function Func_brazil_cpf finds content that matches the pattern.</span></span>
- <span data-ttu-id="32d8c-799">La somme de contrôle est correcte.</span><span class="sxs-lookup"><span data-stu-id="32d8c-799">The checksum passes.</span></span>

```xml
<!-- Brazil CPF Number -->
<Entity id="78e09124-f2c3-4656-b32a-c1a132cd2711" recommendedConfidence="85" patternsProximity="300">
  <Pattern confidenceLevel="85">
     <IdMatch idRef="Func_brazil_cpf"/>
     <Match idRef="Keyword_brazil_cpf"/>
  </Pattern>
  <Pattern confidenceLevel="75">
     <IdMatch idRef="Func_brazil_cpf"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="32d8c-800">Mots clés</span><span class="sxs-lookup"><span data-stu-id="32d8c-800">Keywords</span></span>

#### <a name="keyword_brazil_cpf"></a><span data-ttu-id="32d8c-801">Keyword_brazil_cpf</span><span class="sxs-lookup"><span data-stu-id="32d8c-801">Keyword_brazil_cpf</span></span>

- <span data-ttu-id="32d8c-802">CPF</span><span class="sxs-lookup"><span data-stu-id="32d8c-802">CPF</span></span>
- <span data-ttu-id="32d8c-803">Identificateur</span><span class="sxs-lookup"><span data-stu-id="32d8c-803">Identification</span></span>
- <span data-ttu-id="32d8c-804">Son</span><span class="sxs-lookup"><span data-stu-id="32d8c-804">Registration</span></span>
- <span data-ttu-id="32d8c-805">Parts</span><span class="sxs-lookup"><span data-stu-id="32d8c-805">Revenue</span></span>
- <span data-ttu-id="32d8c-806">Cadastro de Pessoas Físicas</span><span class="sxs-lookup"><span data-stu-id="32d8c-806">Cadastro de Pessoas Físicas</span></span> 
- <span data-ttu-id="32d8c-807">Imposto</span><span class="sxs-lookup"><span data-stu-id="32d8c-807">Imposto</span></span> 
- <span data-ttu-id="32d8c-808">Identificação</span><span class="sxs-lookup"><span data-stu-id="32d8c-808">Identificação</span></span> 
- <span data-ttu-id="32d8c-809">Inscrição</span><span class="sxs-lookup"><span data-stu-id="32d8c-809">Inscrição</span></span> 
- <span data-ttu-id="32d8c-810">Receita</span><span class="sxs-lookup"><span data-stu-id="32d8c-810">Receita</span></span> 
   
## <a name="brazil-legal-entity-number-cnpj"></a><span data-ttu-id="32d8c-811">Numéro d’entité juridique (CNPJ) Brésil</span><span class="sxs-lookup"><span data-stu-id="32d8c-811">Brazil Legal Entity Number (CNPJ)</span></span>

### <a name="format"></a><span data-ttu-id="32d8c-812">Format</span><span class="sxs-lookup"><span data-stu-id="32d8c-812">Format</span></span>

<span data-ttu-id="32d8c-813">14 chiffres qui incluent un numéro d’enregistrement, un numéro de succursale et des chiffres de contrôle, avec des délimiteurs en plus</span><span class="sxs-lookup"><span data-stu-id="32d8c-813">14 digits that include a registration number, branch number, and check digits, plus delimiters</span></span>

### <a name="pattern"></a><span data-ttu-id="32d8c-814">Modèle</span><span class="sxs-lookup"><span data-stu-id="32d8c-814">Pattern</span></span>
<span data-ttu-id="32d8c-815">14 chiffres plus des délimiteurs :</span><span class="sxs-lookup"><span data-stu-id="32d8c-815">14 digits, plus delimiters:</span></span>
- <span data-ttu-id="32d8c-816">Deux chiffres</span><span class="sxs-lookup"><span data-stu-id="32d8c-816">Two digits</span></span> 
- <span data-ttu-id="32d8c-817">Un point </span><span class="sxs-lookup"><span data-stu-id="32d8c-817">A period</span></span> 
- <span data-ttu-id="32d8c-818">Trois chiffres</span><span class="sxs-lookup"><span data-stu-id="32d8c-818">Three digits</span></span> 
- <span data-ttu-id="32d8c-819">Un point </span><span class="sxs-lookup"><span data-stu-id="32d8c-819">A period</span></span> 
- <span data-ttu-id="32d8c-820">Trois chiffres (ces huit premiers chiffres composent le numéro d’enregistrement) </span><span class="sxs-lookup"><span data-stu-id="32d8c-820">Three digits (these first eight digits are the registration number)</span></span> 
- <span data-ttu-id="32d8c-821">Une barre oblique </span><span class="sxs-lookup"><span data-stu-id="32d8c-821">A forward slash</span></span> 
- <span data-ttu-id="32d8c-822">Le numéro de succursale à quatre chiffres </span><span class="sxs-lookup"><span data-stu-id="32d8c-822">Four-digit branch number</span></span> 
- <span data-ttu-id="32d8c-823">Un trait d’union </span><span class="sxs-lookup"><span data-stu-id="32d8c-823">A hyphen</span></span> 
- <span data-ttu-id="32d8c-824">Deux chiffres de contrôle</span><span class="sxs-lookup"><span data-stu-id="32d8c-824">Two digits which are check digits</span></span>

### <a name="checksum"></a><span data-ttu-id="32d8c-825">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="32d8c-825">Checksum</span></span>

<span data-ttu-id="32d8c-826">Oui</span><span class="sxs-lookup"><span data-stu-id="32d8c-826">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="32d8c-827">Définition</span><span class="sxs-lookup"><span data-stu-id="32d8c-827">Definition</span></span>

<span data-ttu-id="32d8c-828">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="32d8c-828">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="32d8c-829">La fonction Func_brazil_cnpj trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="32d8c-829">The function Func_brazil_cnpj finds content that matches the pattern.</span></span>
- <span data-ttu-id="32d8c-830">Un mot clé figurant dans la liste Keyword_brazil_cnpj est trouvé.</span><span class="sxs-lookup"><span data-stu-id="32d8c-830">A keyword from Keyword_brazil_cnpj is found.</span></span>
- <span data-ttu-id="32d8c-831">La somme de contrôle est correcte.</span><span class="sxs-lookup"><span data-stu-id="32d8c-831">The checksum passes.</span></span>

<span data-ttu-id="32d8c-832">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="32d8c-832">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="32d8c-833">La fonction Func_brazil_cnpj trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="32d8c-833">The function Func_brazil_cnpj finds content that matches the pattern.</span></span>
- <span data-ttu-id="32d8c-834">La somme de contrôle est correcte.</span><span class="sxs-lookup"><span data-stu-id="32d8c-834">The checksum passes.</span></span>

```xml
<!-- Brazil Legal Entity Number (CNPJ) -->
<Entity id="9b58b5cd-5e90-4df6-b34f-1ebcc88ceae4" recommendedConfidence="85" patternsProximity="300">
   <Pattern confidenceLevel="85">
     <IdMatch idRef="Func_brazil_cnpj"/>
     <Match idRef="Keyword_brazil_cnpj"/>
  </Pattern>
  <Pattern confidenceLevel="75">
     <IdMatch idRef="Func_brazil_cnpj"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="32d8c-835">Mots clés</span><span class="sxs-lookup"><span data-stu-id="32d8c-835">Keywords</span></span>

#### <a name="keyword_brazil_cnpj"></a><span data-ttu-id="32d8c-836">Keyword_brazil_cnpj</span><span class="sxs-lookup"><span data-stu-id="32d8c-836">Keyword_brazil_cnpj</span></span>

- <span data-ttu-id="32d8c-837">CNPJ</span><span class="sxs-lookup"><span data-stu-id="32d8c-837">CNPJ</span></span> 
- <span data-ttu-id="32d8c-838">CNPJ/MF</span><span class="sxs-lookup"><span data-stu-id="32d8c-838">CNPJ/MF</span></span> 
- <span data-ttu-id="32d8c-839">CNPJ-MF</span><span class="sxs-lookup"><span data-stu-id="32d8c-839">CNPJ-MF</span></span> 
- <span data-ttu-id="32d8c-840">National Registry of Legal Entities</span><span class="sxs-lookup"><span data-stu-id="32d8c-840">National Registry of Legal Entities</span></span> 
- <span data-ttu-id="32d8c-841">Taxpayers Registry</span><span class="sxs-lookup"><span data-stu-id="32d8c-841">Taxpayers Registry</span></span> 
- <span data-ttu-id="32d8c-842">Legal entity</span><span class="sxs-lookup"><span data-stu-id="32d8c-842">Legal entity</span></span> 
- <span data-ttu-id="32d8c-843">Legal entities</span><span class="sxs-lookup"><span data-stu-id="32d8c-843">Legal entities</span></span> 
- <span data-ttu-id="32d8c-844">Registration Status</span><span class="sxs-lookup"><span data-stu-id="32d8c-844">Registration Status</span></span> 
- <span data-ttu-id="32d8c-845">Business</span><span class="sxs-lookup"><span data-stu-id="32d8c-845">Business</span></span> 
- <span data-ttu-id="32d8c-846">Company</span><span class="sxs-lookup"><span data-stu-id="32d8c-846">Company</span></span>
- <span data-ttu-id="32d8c-847">CNPJ</span><span class="sxs-lookup"><span data-stu-id="32d8c-847">CNPJ</span></span> 
- <span data-ttu-id="32d8c-848">Cadastro Nacional da Pessoa Jurídica</span><span class="sxs-lookup"><span data-stu-id="32d8c-848">Cadastro Nacional da Pessoa Jurídica</span></span> 
- <span data-ttu-id="32d8c-849">Cadastro Geral de Contribuintes</span><span class="sxs-lookup"><span data-stu-id="32d8c-849">Cadastro Geral de Contribuintes</span></span> 
- <span data-ttu-id="32d8c-850">CGC</span><span class="sxs-lookup"><span data-stu-id="32d8c-850">CGC</span></span> 
- <span data-ttu-id="32d8c-851">Pessoa jurídica</span><span class="sxs-lookup"><span data-stu-id="32d8c-851">Pessoa jurídica</span></span> 
- <span data-ttu-id="32d8c-852">Pessoas jurídicas</span><span class="sxs-lookup"><span data-stu-id="32d8c-852">Pessoas jurídicas</span></span> 
- <span data-ttu-id="32d8c-853">Situação cadastral</span><span class="sxs-lookup"><span data-stu-id="32d8c-853">Situação cadastral</span></span> 
- <span data-ttu-id="32d8c-854">Inscrição</span><span class="sxs-lookup"><span data-stu-id="32d8c-854">Inscrição</span></span> 
- <span data-ttu-id="32d8c-855">Empresa</span><span class="sxs-lookup"><span data-stu-id="32d8c-855">Empresa</span></span> 
   
## <a name="brazil-national-id-card-rg"></a><span data-ttu-id="32d8c-856">	Brazil National ID Card (RG)</span><span class="sxs-lookup"><span data-stu-id="32d8c-856">Brazil National ID Card (RG)</span></span>

### <a name="format"></a><span data-ttu-id="32d8c-857">Format</span><span class="sxs-lookup"><span data-stu-id="32d8c-857">Format</span></span>

<span data-ttu-id="32d8c-858">Registro Geral (ancien format) : neuf chiffres</span><span class="sxs-lookup"><span data-stu-id="32d8c-858">Registro Geral (old format): Nine digits</span></span>

<span data-ttu-id="32d8c-859">Registro de identidade (RIC) (nouveau format) : 11 chiffres</span><span class="sxs-lookup"><span data-stu-id="32d8c-859">Registro de Identidade (RIC) (new format): 11 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="32d8c-860">Modèle</span><span class="sxs-lookup"><span data-stu-id="32d8c-860">Pattern</span></span>

<span data-ttu-id="32d8c-861">Registro Geral (ancien format) :</span><span class="sxs-lookup"><span data-stu-id="32d8c-861">Registro Geral (old format):</span></span>
- <span data-ttu-id="32d8c-862">Deux chiffres</span><span class="sxs-lookup"><span data-stu-id="32d8c-862">Two digits</span></span> 
- <span data-ttu-id="32d8c-863">Un point </span><span class="sxs-lookup"><span data-stu-id="32d8c-863">A period</span></span> 
- <span data-ttu-id="32d8c-864">Trois chiffres</span><span class="sxs-lookup"><span data-stu-id="32d8c-864">Three digits</span></span> 
- <span data-ttu-id="32d8c-865">Un point </span><span class="sxs-lookup"><span data-stu-id="32d8c-865">A period</span></span> 
- <span data-ttu-id="32d8c-866">Trois chiffres</span><span class="sxs-lookup"><span data-stu-id="32d8c-866">Three digits</span></span> 
- <span data-ttu-id="32d8c-867">Un trait d’union </span><span class="sxs-lookup"><span data-stu-id="32d8c-867">A hyphen</span></span> 
- <span data-ttu-id="32d8c-868">Un chiffre de contrôle</span><span class="sxs-lookup"><span data-stu-id="32d8c-868">One digit which is a check digit</span></span>

<span data-ttu-id="32d8c-869">Registro de identidade (RIC) (nouveau format) :</span><span class="sxs-lookup"><span data-stu-id="32d8c-869">Registro de Identidade (RIC) (new format):</span></span>
- <span data-ttu-id="32d8c-870">10 chiffres</span><span class="sxs-lookup"><span data-stu-id="32d8c-870">10 digits</span></span> 
- <span data-ttu-id="32d8c-871">Un trait d’union </span><span class="sxs-lookup"><span data-stu-id="32d8c-871">A hyphen</span></span> 
- <span data-ttu-id="32d8c-872">Un chiffre de contrôle</span><span class="sxs-lookup"><span data-stu-id="32d8c-872">One digit which is a check digit</span></span>

### <a name="checksum"></a><span data-ttu-id="32d8c-873">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="32d8c-873">Checksum</span></span>

<span data-ttu-id="32d8c-874">Oui</span><span class="sxs-lookup"><span data-stu-id="32d8c-874">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="32d8c-875">Définition</span><span class="sxs-lookup"><span data-stu-id="32d8c-875">Definition</span></span>

<span data-ttu-id="32d8c-876">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="32d8c-876">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="32d8c-877">La fonction Func_brazil_rg trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="32d8c-877">The function Func_brazil_rg finds content that matches the pattern.</span></span>
- <span data-ttu-id="32d8c-878">Un mot clé figurant dans la liste Keyword_brazil_rg est trouvé.</span><span class="sxs-lookup"><span data-stu-id="32d8c-878">A keyword from Keyword_brazil_rg is found.</span></span>
- <span data-ttu-id="32d8c-879">La somme de contrôle est correcte.</span><span class="sxs-lookup"><span data-stu-id="32d8c-879">The checksum passes.</span></span>

<span data-ttu-id="32d8c-880">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="32d8c-880">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="32d8c-881">La fonction Func_brazil_rg trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="32d8c-881">The function Func_brazil_rg finds content that matches the pattern.</span></span>
- <span data-ttu-id="32d8c-882">La somme de contrôle est correcte.</span><span class="sxs-lookup"><span data-stu-id="32d8c-882">The checksum passes.</span></span>

```xml
<!-- Brazil National ID Card (RG) -->
<Entity id="486de900-db70-41b3-a886-abdf25af119c" recommendedConfidence="85" patternsProximity="300">
  <Pattern confidenceLevel="85">
     <IdMatch idRef="Func_brazil_rg"/>
     <Match idRef="Keyword_brazil_rg"/>
  </Pattern>
  <Pattern confidenceLevel="75">
     <IdMatch idRef="Func_brazil_rg"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="32d8c-883">Mots clés</span><span class="sxs-lookup"><span data-stu-id="32d8c-883">Keywords</span></span>

#### <a name="keyword_brazil_rg"></a><span data-ttu-id="32d8c-884">Keyword_brazil_rg</span><span class="sxs-lookup"><span data-stu-id="32d8c-884">Keyword_brazil_rg</span></span>

<span data-ttu-id="32d8c-885">Cédula de identidade carte d’identité número de rregistro Registro de identidade Registro Geral RG (ce mot clé respecte la casse) RIC (ce mot clé respecte la casse)</span><span class="sxs-lookup"><span data-stu-id="32d8c-885">Cédula de identidade identity card national id número de rregistro registro de Iidentidade registro geral RG (this keyword is case sensitive) RIC (this keyword is case sensitive)</span></span> 
   
## <a name="canada-bank-account-number"></a><span data-ttu-id="32d8c-886">Numéro de compte bancaire Canada</span><span class="sxs-lookup"><span data-stu-id="32d8c-886">Canada Bank Account Number</span></span>

### <a name="format"></a><span data-ttu-id="32d8c-887">Format</span><span class="sxs-lookup"><span data-stu-id="32d8c-887">Format</span></span>

<span data-ttu-id="32d8c-888">Sept ou douze chiffres</span><span class="sxs-lookup"><span data-stu-id="32d8c-888">Seven or twelve digits</span></span>

### <a name="pattern"></a><span data-ttu-id="32d8c-889">Modèle</span><span class="sxs-lookup"><span data-stu-id="32d8c-889">Pattern</span></span>

<span data-ttu-id="32d8c-890">Un numéro de compte bancaire au Canada est composé de sept ou douze chiffres.</span><span class="sxs-lookup"><span data-stu-id="32d8c-890">A Canada Bank Account Number is seven or twelve digits.</span></span>

<span data-ttu-id="32d8c-891">Un numéro de transit de compte bancaire du Canada est indiqué au format suivant :</span><span class="sxs-lookup"><span data-stu-id="32d8c-891">A Canada bank account transit number is:</span></span>
- <span data-ttu-id="32d8c-892">Cinq chiffres</span><span class="sxs-lookup"><span data-stu-id="32d8c-892">Five digits</span></span> 
- <span data-ttu-id="32d8c-893">Un trait d’union </span><span class="sxs-lookup"><span data-stu-id="32d8c-893">A hyphen</span></span> 
- <span data-ttu-id="32d8c-894">Trois chiffres ou</span><span class="sxs-lookup"><span data-stu-id="32d8c-894">Three digits OR</span></span>
- <span data-ttu-id="32d8c-895">Un zéro « 0 » </span><span class="sxs-lookup"><span data-stu-id="32d8c-895">A zero "0"</span></span> 
- <span data-ttu-id="32d8c-896">Huit chiffres</span><span class="sxs-lookup"><span data-stu-id="32d8c-896">Eight digits</span></span>

### <a name="checksum"></a><span data-ttu-id="32d8c-897">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="32d8c-897">Checksum</span></span>

<span data-ttu-id="32d8c-898">Non</span><span class="sxs-lookup"><span data-stu-id="32d8c-898">No</span></span>

### <a name="definition"></a><span data-ttu-id="32d8c-899">Définition</span><span class="sxs-lookup"><span data-stu-id="32d8c-899">Definition</span></span>

<span data-ttu-id="32d8c-900">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="32d8c-900">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="32d8c-901">L’expression régulière Regex_canada_bank_account_number trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="32d8c-901">The regular expression Regex_canada_bank_account_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="32d8c-902">Un mot clé figurant dans la liste Keyword_canada_bank_account_number est trouvé.</span><span class="sxs-lookup"><span data-stu-id="32d8c-902">A keyword from Keyword_canada_bank_account_number is found.</span></span>
- <span data-ttu-id="32d8c-903">L’expression régulière Regex_canada_bank_account_transit_number trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="32d8c-903">The regular expression Regex_canada_bank_account_transit_number finds content that matches the pattern.</span></span>

<span data-ttu-id="32d8c-904">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="32d8c-904">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="32d8c-905">L’expression régulière Regex_canada_bank_account_number trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="32d8c-905">The regular expression Regex_canada_bank_account_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="32d8c-906">Un mot clé figurant dans la liste Keyword_canada_bank_account_number est trouvé.</span><span class="sxs-lookup"><span data-stu-id="32d8c-906">A keyword from Keyword_canada_bank_account_number is found.</span></span>

```xml
<!-- Canada Bank Account Number -->
<Entity id="552e814c-cb50-4d94-bbaa-bb1d1ffb34de" patternsProximity="300" recommendedConfidence="75">
  <Pattern confidenceLevel="85">
        <IdMatch idRef="Regex_canada_bank_account_number" />
        <Match idRef="Keyword_canada_bank_account_number" />
        <Match idRef="Regex_canada_bank_account_transit_number" />
   </Pattern>
   <Pattern confidenceLevel="75">
        <IdMatch idRef="Regex_canada_bank_account_number" />
        <Match idRef="Keyword_canada_bank_account_number" />
   </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="32d8c-907">Mots clés</span><span class="sxs-lookup"><span data-stu-id="32d8c-907">Keywords</span></span>

#### <a name="keyword_canada_bank_account_number"></a><span data-ttu-id="32d8c-908">Keyword_canada_bank_account_number</span><span class="sxs-lookup"><span data-stu-id="32d8c-908">Keyword_canada_bank_account_number</span></span>

- <span data-ttu-id="32d8c-909">obligations d’épargne du Canada</span><span class="sxs-lookup"><span data-stu-id="32d8c-909">canada savings bonds</span></span>
- <span data-ttu-id="32d8c-910">agence du revenu du Canada</span><span class="sxs-lookup"><span data-stu-id="32d8c-910">canada revenue agency</span></span>
- <span data-ttu-id="32d8c-911">institution financière du Canada</span><span class="sxs-lookup"><span data-stu-id="32d8c-911">canadian financial institution</span></span>
- <span data-ttu-id="32d8c-912">formulaire de dépôt direct</span><span class="sxs-lookup"><span data-stu-id="32d8c-912">direct deposit form</span></span>
- <span data-ttu-id="32d8c-913">citoyen canadien</span><span class="sxs-lookup"><span data-stu-id="32d8c-913">canadian citizen</span></span>
- <span data-ttu-id="32d8c-914">représentant légal</span><span class="sxs-lookup"><span data-stu-id="32d8c-914">legal representative</span></span>
- <span data-ttu-id="32d8c-915">notaire</span><span class="sxs-lookup"><span data-stu-id="32d8c-915">notary public</span></span>
- <span data-ttu-id="32d8c-916">commissaire à l’assermentation</span><span class="sxs-lookup"><span data-stu-id="32d8c-916">commissioner for oaths</span></span>
- <span data-ttu-id="32d8c-917">prestation pour la garde d’enfants</span><span class="sxs-lookup"><span data-stu-id="32d8c-917">child care benefit</span></span>
- <span data-ttu-id="32d8c-918">prestation universelle pour la garde d’enfants</span><span class="sxs-lookup"><span data-stu-id="32d8c-918">universal child care</span></span>
- <span data-ttu-id="32d8c-919">prestation fiscale canadienne pour enfants</span><span class="sxs-lookup"><span data-stu-id="32d8c-919">canada child tax benefit</span></span>
- <span data-ttu-id="32d8c-920">prestation fiscale pour le revenu gagné</span><span class="sxs-lookup"><span data-stu-id="32d8c-920">income tax benefit</span></span>
- <span data-ttu-id="32d8c-921">taxe de vente harmonisée</span><span class="sxs-lookup"><span data-stu-id="32d8c-921">harmonized sales tax</span></span>
- <span data-ttu-id="32d8c-922">numéro d’assurance sociale</span><span class="sxs-lookup"><span data-stu-id="32d8c-922">social insurance number</span></span>
- <span data-ttu-id="32d8c-923">remboursement d’impôt</span><span class="sxs-lookup"><span data-stu-id="32d8c-923">income tax refund</span></span>
- <span data-ttu-id="32d8c-924">prestation fiscale pour enfants</span><span class="sxs-lookup"><span data-stu-id="32d8c-924">child tax benefit</span></span>
- <span data-ttu-id="32d8c-925">paiements aux territoires</span><span class="sxs-lookup"><span data-stu-id="32d8c-925">territorial payments</span></span>
- <span data-ttu-id="32d8c-926">numéro d’institution</span><span class="sxs-lookup"><span data-stu-id="32d8c-926">institution number</span></span>
- <span data-ttu-id="32d8c-927">demande de dépôt</span><span class="sxs-lookup"><span data-stu-id="32d8c-927">deposit request</span></span>
- <span data-ttu-id="32d8c-928">informations bancaires</span><span class="sxs-lookup"><span data-stu-id="32d8c-928">banking information</span></span>
- <span data-ttu-id="32d8c-929">dépôt direct</span><span class="sxs-lookup"><span data-stu-id="32d8c-929">direct deposit</span></span>
   
## <a name="canada-drivers-license-number"></a><span data-ttu-id="32d8c-930">Numéro de permis de conduire Canada</span><span class="sxs-lookup"><span data-stu-id="32d8c-930">Canada Driver's License Number</span></span>

### <a name="format"></a><span data-ttu-id="32d8c-931">Format</span><span class="sxs-lookup"><span data-stu-id="32d8c-931">Format</span></span>

<span data-ttu-id="32d8c-932">Varie selon la province</span><span class="sxs-lookup"><span data-stu-id="32d8c-932">Varies by province</span></span>

### <a name="pattern"></a><span data-ttu-id="32d8c-933">Modèle</span><span class="sxs-lookup"><span data-stu-id="32d8c-933">Pattern</span></span>

<span data-ttu-id="32d8c-934">Plusieurs modèles pour les différentes provinces : Alberta, Colombie-Britannique, Manitoba, Nouveau-Brunswick, Terre-Neuve-et-Labrador, Nouvelle-Écosse, Ontario, Île-du-Prince-Édouard, Québec et Saskatchewan</span><span class="sxs-lookup"><span data-stu-id="32d8c-934">Various patterns covering Alberta, British Columbia, Manitoba, New Brunswick, Newfoundland/Labrador, Nova Scotia, Ontario, Prince Edward Island, Quebec, and Saskatchewan</span></span>

### <a name="checksum"></a><span data-ttu-id="32d8c-935">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="32d8c-935">Checksum</span></span>

<span data-ttu-id="32d8c-936">Non</span><span class="sxs-lookup"><span data-stu-id="32d8c-936">No</span></span>

### <a name="definition"></a><span data-ttu-id="32d8c-937">Définition</span><span class="sxs-lookup"><span data-stu-id="32d8c-937">Definition</span></span>

<span data-ttu-id="32d8c-938">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="32d8c-938">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="32d8c-939">La fonction Func_[province_name]_drivers_license_number trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="32d8c-939">The function Func_[province_name]_drivers_license_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="32d8c-940">Un mot clé figurant dans la liste Keyword_[province_name]_drivers_license_name est trouvé.</span><span class="sxs-lookup"><span data-stu-id="32d8c-940">A keyword from Keyword_[province_name]_drivers_license_name is found.</span></span>
- <span data-ttu-id="32d8c-941">Un mot clé figurant dans la liste Keyword_canada_drivers_license est trouvé.</span><span class="sxs-lookup"><span data-stu-id="32d8c-941">A keyword from Keyword_canada_drivers_license is found.</span></span>

```xml
<!-- Canada Driver's License Number -->
    <Entity id="37186abb-8e48-4800-ad3c-e3d1610b3db0" patternsProximity="300" recommendedConfidence="75">
      <Pattern confidenceLevel="75">
        <IdMatch idRef="Func_alberta_drivers_license_number" />
        <Match idRef="Keyword_alberta_drivers_license_name" />
        <Match idRef="Keyword_canada_drivers_license" />
      </Pattern>
      <Pattern confidenceLevel="75">
        <IdMatch idRef="Func_british_columbia_drivers_license_number" />
        <Match idRef="Keyword_british_columbia_drivers_license_name" />
        <Match idRef="Keyword_canada_drivers_license" />
      </Pattern>
      <Pattern confidenceLevel="75">
        <IdMatch idRef="Func_manitoba_drivers_license_number" />
        <Match idRef="Keyword_manitoba_drivers_license_name" />
        <Match idRef="Keyword_canada_drivers_license" />
      </Pattern>
      <Pattern confidenceLevel="75">
        <IdMatch idRef="Func_new_brunswick_drivers_license_number" />
        <Match idRef="Keyword_new_brunswick_drivers_license_name" />
        <Match idRef="Keyword_canada_drivers_license" />
      </Pattern>
      <Pattern confidenceLevel="75">
        <IdMatch idRef="Func_newfoundland_labrador_drivers_license_number" />
        <Match idRef="Keyword_newfoundland_labrador_drivers_license_name" />
        <Match idRef="Keyword_canada_drivers_license" />
      </Pattern>
      <Pattern confidenceLevel="75">
        <IdMatch idRef="Func_nova_scotia_drivers_license_number" />
        <Match idRef="Keyword_nova_scotia_drivers_license_name" />
        <Match idRef="Keyword_canada_drivers_license" />
      </Pattern>
      <Pattern confidenceLevel="75">
        <IdMatch idRef="Func_ontario_drivers_license_number" />
        <Match idRef="Keyword_ontario_drivers_license_name" />
        <Match idRef="Keyword_canada_drivers_license" />
      </Pattern>
      <Pattern confidenceLevel="75">
        <IdMatch idRef="Func_prince_edward_island_drivers_license_number" />
        <Match idRef="Keyword_prince_edward_island_drivers_license_name" />
        <Match idRef="Keyword_canada_drivers_license" />
      </Pattern>
      <Pattern confidenceLevel="75">
        <IdMatch idRef="Func_quebec_drivers_license_number" />
        <Match idRef="Keyword_quebec_drivers_license_name" />
        <Match idRef="Keyword_canada_drivers_license" />
      </Pattern>
      <Pattern confidenceLevel="75">
        <IdMatch idRef="Func_saskatchewan_drivers_license_number" />
        <Match idRef="Keyword_saskatchewan_drivers_license_name" />
        <Match idRef="Keyword_canada_drivers_license" />
      </Pattern>
    </Entity>
```

### <a name="keywords"></a><span data-ttu-id="32d8c-942">Mots clés</span><span class="sxs-lookup"><span data-stu-id="32d8c-942">Keywords</span></span>

#### <a name="keyword_province_name_drivers_license_name"></a><span data-ttu-id="32d8c-943">Keyword_ [province_name] _drivers_license_name</span><span class="sxs-lookup"><span data-stu-id="32d8c-943">Keyword_[province_name]_drivers_license_name</span></span>

- <span data-ttu-id="32d8c-944">L’abréviation de la province, par exemple AB</span><span class="sxs-lookup"><span data-stu-id="32d8c-944">The province abbreviation, for example AB</span></span>
- <span data-ttu-id="32d8c-945">Le nom de la province, par exemple Alberta</span><span class="sxs-lookup"><span data-stu-id="32d8c-945">The province name, for example Alberta</span></span>

#### <a name="keyword_canada_drivers_license"></a><span data-ttu-id="32d8c-946">Keyword_canada_drivers_license</span><span class="sxs-lookup"><span data-stu-id="32d8c-946">Keyword_canada_drivers_license</span></span>

- <span data-ttu-id="32d8c-947">LD</span><span class="sxs-lookup"><span data-stu-id="32d8c-947">DL</span></span>
- <span data-ttu-id="32d8c-948">DISTRIBUTION</span><span class="sxs-lookup"><span data-stu-id="32d8c-948">DLS</span></span>
- <span data-ttu-id="32d8c-949">CÈDE</span><span class="sxs-lookup"><span data-stu-id="32d8c-949">CDL</span></span>
- <span data-ttu-id="32d8c-950">CDLS</span><span class="sxs-lookup"><span data-stu-id="32d8c-950">CDLS</span></span>
- <span data-ttu-id="32d8c-951">DriverLic</span><span class="sxs-lookup"><span data-stu-id="32d8c-951">DriverLic</span></span>
- <span data-ttu-id="32d8c-952">DriverLics</span><span class="sxs-lookup"><span data-stu-id="32d8c-952">DriverLics</span></span>
- <span data-ttu-id="32d8c-953">DriverLicense</span><span class="sxs-lookup"><span data-stu-id="32d8c-953">DriverLicense</span></span>
- <span data-ttu-id="32d8c-954">DriverLicenses</span><span class="sxs-lookup"><span data-stu-id="32d8c-954">DriverLicenses</span></span>
- <span data-ttu-id="32d8c-955">DriverLicence</span><span class="sxs-lookup"><span data-stu-id="32d8c-955">DriverLicence</span></span>
- <span data-ttu-id="32d8c-956">DriverLicences</span><span class="sxs-lookup"><span data-stu-id="32d8c-956">DriverLicences</span></span>
- <span data-ttu-id="32d8c-957">Permis conduire</span><span class="sxs-lookup"><span data-stu-id="32d8c-957">Driver Lic</span></span>
- <span data-ttu-id="32d8c-958">Permis conduire</span><span class="sxs-lookup"><span data-stu-id="32d8c-958">Driver Lics</span></span>
- <span data-ttu-id="32d8c-959">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="32d8c-959">Driver License</span></span>
- <span data-ttu-id="32d8c-960">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="32d8c-960">Driver Licenses</span></span>
- <span data-ttu-id="32d8c-961">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="32d8c-961">Driver Licence</span></span>
- <span data-ttu-id="32d8c-962">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="32d8c-962">Driver Licences</span></span>
- <span data-ttu-id="32d8c-963">DriversLic</span><span class="sxs-lookup"><span data-stu-id="32d8c-963">DriversLic</span></span>
- <span data-ttu-id="32d8c-964">DriversLics</span><span class="sxs-lookup"><span data-stu-id="32d8c-964">DriversLics</span></span>
- <span data-ttu-id="32d8c-965">DriversLicence</span><span class="sxs-lookup"><span data-stu-id="32d8c-965">DriversLicence</span></span>
- <span data-ttu-id="32d8c-966">DriversLicences</span><span class="sxs-lookup"><span data-stu-id="32d8c-966">DriversLicences</span></span>
- <span data-ttu-id="32d8c-967">DriversLicense</span><span class="sxs-lookup"><span data-stu-id="32d8c-967">DriversLicense</span></span>
- <span data-ttu-id="32d8c-968">DriversLicenses</span><span class="sxs-lookup"><span data-stu-id="32d8c-968">DriversLicenses</span></span>
- <span data-ttu-id="32d8c-969">Permis conduire</span><span class="sxs-lookup"><span data-stu-id="32d8c-969">Drivers Lic</span></span>
- <span data-ttu-id="32d8c-970">Permis conduire</span><span class="sxs-lookup"><span data-stu-id="32d8c-970">Drivers Lics</span></span>
- <span data-ttu-id="32d8c-971">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="32d8c-971">Drivers License</span></span>
- <span data-ttu-id="32d8c-972">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="32d8c-972">Drivers Licenses</span></span>
- <span data-ttu-id="32d8c-973">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="32d8c-973">Drivers Licence</span></span>
- <span data-ttu-id="32d8c-974">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="32d8c-974">Drivers Licences</span></span>
- <span data-ttu-id="32d8c-975">Driver'Lic</span><span class="sxs-lookup"><span data-stu-id="32d8c-975">Driver'Lic</span></span>
- <span data-ttu-id="32d8c-976">Driver'Lics</span><span class="sxs-lookup"><span data-stu-id="32d8c-976">Driver'Lics</span></span>
- <span data-ttu-id="32d8c-977">Driver'License</span><span class="sxs-lookup"><span data-stu-id="32d8c-977">Driver'License</span></span>
- <span data-ttu-id="32d8c-978">Driver'Licenses</span><span class="sxs-lookup"><span data-stu-id="32d8c-978">Driver'Licenses</span></span>
- <span data-ttu-id="32d8c-979">Driver'Licence</span><span class="sxs-lookup"><span data-stu-id="32d8c-979">Driver'Licence</span></span>
- <span data-ttu-id="32d8c-980">Driver'Licences</span><span class="sxs-lookup"><span data-stu-id="32d8c-980">Driver'Licences</span></span>
- <span data-ttu-id="32d8c-981">Permis conduire</span><span class="sxs-lookup"><span data-stu-id="32d8c-981">Driver' Lic</span></span>
- <span data-ttu-id="32d8c-982">Permis conduire</span><span class="sxs-lookup"><span data-stu-id="32d8c-982">Driver' Lics</span></span>
- <span data-ttu-id="32d8c-983">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="32d8c-983">Driver' License</span></span>
- <span data-ttu-id="32d8c-984">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="32d8c-984">Driver' Licenses</span></span>
- <span data-ttu-id="32d8c-985">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="32d8c-985">Driver' Licence</span></span>
- <span data-ttu-id="32d8c-986">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="32d8c-986">Driver' Licences</span></span>
- <span data-ttu-id="32d8c-987">Driver'sLic</span><span class="sxs-lookup"><span data-stu-id="32d8c-987">Driver'sLic</span></span>
- <span data-ttu-id="32d8c-988">Driver'sLics</span><span class="sxs-lookup"><span data-stu-id="32d8c-988">Driver'sLics</span></span>
- <span data-ttu-id="32d8c-989">Driver'sLicense</span><span class="sxs-lookup"><span data-stu-id="32d8c-989">Driver'sLicense</span></span>
- <span data-ttu-id="32d8c-990">Driver'sLicenses</span><span class="sxs-lookup"><span data-stu-id="32d8c-990">Driver'sLicenses</span></span>
- <span data-ttu-id="32d8c-991">Driver'sLicence</span><span class="sxs-lookup"><span data-stu-id="32d8c-991">Driver'sLicence</span></span>
- <span data-ttu-id="32d8c-992">Driver'sLicences</span><span class="sxs-lookup"><span data-stu-id="32d8c-992">Driver'sLicences</span></span>
- <span data-ttu-id="32d8c-993">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="32d8c-993">Driver's Lic</span></span>
- <span data-ttu-id="32d8c-994">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="32d8c-994">Driver's Lics</span></span>
- <span data-ttu-id="32d8c-995">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="32d8c-995">Driver's License</span></span>
- <span data-ttu-id="32d8c-996">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="32d8c-996">Driver's Licenses</span></span>
- <span data-ttu-id="32d8c-997">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="32d8c-997">Driver's Licence</span></span>
- <span data-ttu-id="32d8c-998">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="32d8c-998">Driver's Licences</span></span>
- <span data-ttu-id="32d8c-999">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="32d8c-999">Permis de Conduire</span></span>
- <span data-ttu-id="32d8c-1000">id</span><span class="sxs-lookup"><span data-stu-id="32d8c-1000">id</span></span>
- <span data-ttu-id="32d8c-1001">Ids</span><span class="sxs-lookup"><span data-stu-id="32d8c-1001">ids</span></span>
- <span data-ttu-id="32d8c-1002">numéro carte d’identification</span><span class="sxs-lookup"><span data-stu-id="32d8c-1002">idcard number</span></span>
- <span data-ttu-id="32d8c-1003">numéros carte d’identification</span><span class="sxs-lookup"><span data-stu-id="32d8c-1003">idcard numbers</span></span>
- <span data-ttu-id="32d8c-1004"># carte d’identification</span><span class="sxs-lookup"><span data-stu-id="32d8c-1004">idcard #</span></span>
- <span data-ttu-id="32d8c-1005"># carte d’identification</span><span class="sxs-lookup"><span data-stu-id="32d8c-1005">idcard #s</span></span>
- <span data-ttu-id="32d8c-1006">carte d’identification</span><span class="sxs-lookup"><span data-stu-id="32d8c-1006">idcard card</span></span>
- <span data-ttu-id="32d8c-1007">cartes d’identification</span><span class="sxs-lookup"><span data-stu-id="32d8c-1007">idcard cards</span></span>
- <span data-ttu-id="32d8c-1008">carte d’identification</span><span class="sxs-lookup"><span data-stu-id="32d8c-1008">idcard</span></span>
- <span data-ttu-id="32d8c-1009">numéro d’identification</span><span class="sxs-lookup"><span data-stu-id="32d8c-1009">identification number</span></span>
- <span data-ttu-id="32d8c-1010">numéros d’identification</span><span class="sxs-lookup"><span data-stu-id="32d8c-1010">identification numbers</span></span>
- <span data-ttu-id="32d8c-1011"># identification</span><span class="sxs-lookup"><span data-stu-id="32d8c-1011">identification #</span></span>
- <span data-ttu-id="32d8c-1012"># identification</span><span class="sxs-lookup"><span data-stu-id="32d8c-1012">identification #s</span></span>
- <span data-ttu-id="32d8c-1013">carte d’identification</span><span class="sxs-lookup"><span data-stu-id="32d8c-1013">identification card</span></span>
- <span data-ttu-id="32d8c-1014">cartes d’identification</span><span class="sxs-lookup"><span data-stu-id="32d8c-1014">identification cards</span></span>
- <span data-ttu-id="32d8c-1015">identificateur</span><span class="sxs-lookup"><span data-stu-id="32d8c-1015">identification</span></span> 
- <span data-ttu-id="32d8c-1016">LD #</span><span class="sxs-lookup"><span data-stu-id="32d8c-1016">DL#</span></span>
- <span data-ttu-id="32d8c-1017">DISTRIBUTION #</span><span class="sxs-lookup"><span data-stu-id="32d8c-1017">DLS#</span></span> 
- <span data-ttu-id="32d8c-1018">CÈDE #</span><span class="sxs-lookup"><span data-stu-id="32d8c-1018">CDL#</span></span> 
- <span data-ttu-id="32d8c-1019">CDLS #</span><span class="sxs-lookup"><span data-stu-id="32d8c-1019">CDLS#</span></span> 
- <span data-ttu-id="32d8c-1020">DriverLic #</span><span class="sxs-lookup"><span data-stu-id="32d8c-1020">DriverLic#</span></span> 
- <span data-ttu-id="32d8c-1021">DriverLics #</span><span class="sxs-lookup"><span data-stu-id="32d8c-1021">DriverLics#</span></span> 
- <span data-ttu-id="32d8c-1022">DriverLicense #</span><span class="sxs-lookup"><span data-stu-id="32d8c-1022">DriverLicense#</span></span> 
- <span data-ttu-id="32d8c-1023">DriverLicenses #</span><span class="sxs-lookup"><span data-stu-id="32d8c-1023">DriverLicenses#</span></span> 
- <span data-ttu-id="32d8c-1024">DriverLicence #</span><span class="sxs-lookup"><span data-stu-id="32d8c-1024">DriverLicence#</span></span> 
- <span data-ttu-id="32d8c-1025">DriverLicences #</span><span class="sxs-lookup"><span data-stu-id="32d8c-1025">DriverLicences#</span></span> 
- <span data-ttu-id="32d8c-1026">#Permis conduire</span><span class="sxs-lookup"><span data-stu-id="32d8c-1026">Driver Lic#</span></span>
- <span data-ttu-id="32d8c-1027">#Permis conduire</span><span class="sxs-lookup"><span data-stu-id="32d8c-1027">Driver Lics#</span></span> 
- <span data-ttu-id="32d8c-1028">#Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="32d8c-1028">Driver License#</span></span> 
- <span data-ttu-id="32d8c-1029">#Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="32d8c-1029">Driver Licenses#</span></span> 
- <span data-ttu-id="32d8c-1030">#Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="32d8c-1030">Driver License#</span></span> 
- <span data-ttu-id="32d8c-1031">#Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="32d8c-1031">Driver Licences#</span></span> 
- <span data-ttu-id="32d8c-1032">DriversLic #</span><span class="sxs-lookup"><span data-stu-id="32d8c-1032">DriversLic#</span></span> 
- <span data-ttu-id="32d8c-1033">DriversLics #</span><span class="sxs-lookup"><span data-stu-id="32d8c-1033">DriversLics#</span></span> 
- <span data-ttu-id="32d8c-1034">DriversLicense #</span><span class="sxs-lookup"><span data-stu-id="32d8c-1034">DriversLicense#</span></span> 
- <span data-ttu-id="32d8c-1035">DriversLicenses #</span><span class="sxs-lookup"><span data-stu-id="32d8c-1035">DriversLicenses#</span></span> 
- <span data-ttu-id="32d8c-1036">DriversLicence #</span><span class="sxs-lookup"><span data-stu-id="32d8c-1036">DriversLicence#</span></span> 
- <span data-ttu-id="32d8c-1037">DriversLicences #</span><span class="sxs-lookup"><span data-stu-id="32d8c-1037">DriversLicences#</span></span> 
- <span data-ttu-id="32d8c-1038">#Permis conduire</span><span class="sxs-lookup"><span data-stu-id="32d8c-1038">Drivers Lic#</span></span> 
- <span data-ttu-id="32d8c-1039">#Permis conduire</span><span class="sxs-lookup"><span data-stu-id="32d8c-1039">Drivers Lics#</span></span> 
- <span data-ttu-id="32d8c-1040">#Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="32d8c-1040">Drivers License#</span></span> 
- <span data-ttu-id="32d8c-1041">#Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="32d8c-1041">Drivers Licenses#</span></span> 
- <span data-ttu-id="32d8c-1042">#Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="32d8c-1042">Drivers Licence#</span></span> 
- <span data-ttu-id="32d8c-1043">#Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="32d8c-1043">Drivers Licences#</span></span> 
- <span data-ttu-id="32d8c-1044">Driver'Lic #</span><span class="sxs-lookup"><span data-stu-id="32d8c-1044">Driver'Lic#</span></span> 
- <span data-ttu-id="32d8c-1045">Driver'Lics #</span><span class="sxs-lookup"><span data-stu-id="32d8c-1045">Driver'Lics#</span></span> 
- <span data-ttu-id="32d8c-1046">Driver'License #</span><span class="sxs-lookup"><span data-stu-id="32d8c-1046">Driver'License#</span></span> 
- <span data-ttu-id="32d8c-1047">Driver'Licenses #</span><span class="sxs-lookup"><span data-stu-id="32d8c-1047">Driver'Licenses#</span></span> 
- <span data-ttu-id="32d8c-1048">Driver'Licence #</span><span class="sxs-lookup"><span data-stu-id="32d8c-1048">Driver'Licence#</span></span> 
- <span data-ttu-id="32d8c-1049">Driver'Licences #</span><span class="sxs-lookup"><span data-stu-id="32d8c-1049">Driver'Licences#</span></span> 
- <span data-ttu-id="32d8c-1050">#Permis conduire</span><span class="sxs-lookup"><span data-stu-id="32d8c-1050">Driver' Lic#</span></span> 
- <span data-ttu-id="32d8c-1051">#Permis conduire</span><span class="sxs-lookup"><span data-stu-id="32d8c-1051">Driver' Lics#</span></span> 
- <span data-ttu-id="32d8c-1052">#Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="32d8c-1052">Driver' License#</span></span> 
- <span data-ttu-id="32d8c-1053">#Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="32d8c-1053">Driver' Licenses#</span></span> 
- <span data-ttu-id="32d8c-1054">#Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="32d8c-1054">Driver' Licence#</span></span> 
- <span data-ttu-id="32d8c-1055">#Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="32d8c-1055">Driver' Licences#</span></span> 
- <span data-ttu-id="32d8c-1056">Driver'sLic #</span><span class="sxs-lookup"><span data-stu-id="32d8c-1056">Driver'sLic#</span></span> 
- <span data-ttu-id="32d8c-1057">Driver'sLics #</span><span class="sxs-lookup"><span data-stu-id="32d8c-1057">Driver'sLics#</span></span> 
- <span data-ttu-id="32d8c-1058">Driver'sLicense #</span><span class="sxs-lookup"><span data-stu-id="32d8c-1058">Driver'sLicense#</span></span> 
- <span data-ttu-id="32d8c-1059">Driver'sLicenses #</span><span class="sxs-lookup"><span data-stu-id="32d8c-1059">Driver'sLicenses#</span></span> 
- <span data-ttu-id="32d8c-1060">Driver'sLicence #</span><span class="sxs-lookup"><span data-stu-id="32d8c-1060">Driver'sLicence#</span></span> 
- <span data-ttu-id="32d8c-1061">Driver'sLicences #</span><span class="sxs-lookup"><span data-stu-id="32d8c-1061">Driver'sLicences#</span></span> 
- <span data-ttu-id="32d8c-1062">#Permisconduire</span><span class="sxs-lookup"><span data-stu-id="32d8c-1062">Driver's Lic#</span></span> 
- <span data-ttu-id="32d8c-1063">#Permisconduire</span><span class="sxs-lookup"><span data-stu-id="32d8c-1063">Driver's Lics#</span></span> 
- <span data-ttu-id="32d8c-1064">#Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="32d8c-1064">Driver's License#</span></span> 
- <span data-ttu-id="32d8c-1065">#Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="32d8c-1065">Driver's Licenses#</span></span> 
- <span data-ttu-id="32d8c-1066">#Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="32d8c-1066">Driver's Licence#</span></span> 
- <span data-ttu-id="32d8c-1067">#Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="32d8c-1067">Driver's Licences#</span></span> 
- <span data-ttu-id="32d8c-1068">Permis de conduire #</span><span class="sxs-lookup"><span data-stu-id="32d8c-1068">Permis de Conduire#</span></span> 
- <span data-ttu-id="32d8c-1069">Réf #</span><span class="sxs-lookup"><span data-stu-id="32d8c-1069">id#</span></span> 
- <span data-ttu-id="32d8c-1070">codes #</span><span class="sxs-lookup"><span data-stu-id="32d8c-1070">ids#</span></span> 
- <span data-ttu-id="32d8c-1071">#carte carte d’identification</span><span class="sxs-lookup"><span data-stu-id="32d8c-1071">idcard card#</span></span> 
- <span data-ttu-id="32d8c-1072">#cartes carte d’identification</span><span class="sxs-lookup"><span data-stu-id="32d8c-1072">idcard cards#</span></span> 
- <span data-ttu-id="32d8c-1073">carte d’identification #</span><span class="sxs-lookup"><span data-stu-id="32d8c-1073">idcard#</span></span> 
- <span data-ttu-id="32d8c-1074">#carte d’identification</span><span class="sxs-lookup"><span data-stu-id="32d8c-1074">identification card#</span></span> 
- <span data-ttu-id="32d8c-1075">#cartes d’identification</span><span class="sxs-lookup"><span data-stu-id="32d8c-1075">identification cards#</span></span> 
- <span data-ttu-id="32d8c-1076">identificateur #</span><span class="sxs-lookup"><span data-stu-id="32d8c-1076">identification#</span></span> 
   
## <a name="canada-health-service-number"></a><span data-ttu-id="32d8c-1077">Numéro de service de santé Canada</span><span class="sxs-lookup"><span data-stu-id="32d8c-1077">Canada Health Service Number</span></span>

### <a name="format"></a><span data-ttu-id="32d8c-1078">Format</span><span class="sxs-lookup"><span data-stu-id="32d8c-1078">Format</span></span>

<span data-ttu-id="32d8c-1079">10 chiffres</span><span class="sxs-lookup"><span data-stu-id="32d8c-1079">10 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="32d8c-1080">Modèle</span><span class="sxs-lookup"><span data-stu-id="32d8c-1080">Pattern</span></span>

<span data-ttu-id="32d8c-1081">10 chiffres</span><span class="sxs-lookup"><span data-stu-id="32d8c-1081">10 digits</span></span>

### <a name="checksum"></a><span data-ttu-id="32d8c-1082">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="32d8c-1082">Checksum</span></span>

<span data-ttu-id="32d8c-1083">Non</span><span class="sxs-lookup"><span data-stu-id="32d8c-1083">No</span></span>

### <a name="definition"></a><span data-ttu-id="32d8c-1084">Définition</span><span class="sxs-lookup"><span data-stu-id="32d8c-1084">Definition</span></span>

<span data-ttu-id="32d8c-1085">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="32d8c-1085">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="32d8c-1086">L’expression régulière Regex_canada_health_service_number trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="32d8c-1086">The regular expression Regex_canada_health_service_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="32d8c-1087">Un mot clé figurant dans la liste Keyword_canada_health_service_number est trouvé.</span><span class="sxs-lookup"><span data-stu-id="32d8c-1087">A keyword from Keyword_canada_health_service_number is found.</span></span>

```xml
<!-- Canada Health Service Number -->
<Entity id="59c0bf39-7fab-482c-af25-00faa4384c94" patternsProximity="300" recommendedConfidence="75">
  <Pattern confidenceLevel="75">
        <IdMatch idRef="Regex_canada_health_service_number" />
        <Any minMatches="1">
          <Match idRef="Keyword_canada_health_service_number" />
        </Any>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="32d8c-1088">Mots clés</span><span class="sxs-lookup"><span data-stu-id="32d8c-1088">Keywords</span></span>

#### <a name="keyword_canada_health_service_number"></a><span data-ttu-id="32d8c-1089">Keyword_canada_health_service_number</span><span class="sxs-lookup"><span data-stu-id="32d8c-1089">Keyword_canada_health_service_number</span></span>

- <span data-ttu-id="32d8c-1090">numéro d’assurance-maladie</span><span class="sxs-lookup"><span data-stu-id="32d8c-1090">personal health number</span></span>
- <span data-ttu-id="32d8c-1091">informations sur le patient</span><span class="sxs-lookup"><span data-stu-id="32d8c-1091">patient information</span></span>
- <span data-ttu-id="32d8c-1092">services de santé</span><span class="sxs-lookup"><span data-stu-id="32d8c-1092">health services</span></span>
- <span data-ttu-id="32d8c-1093">services spécialisés</span><span class="sxs-lookup"><span data-stu-id="32d8c-1093">speciality services</span></span>
- <span data-ttu-id="32d8c-1094">accident automobile</span><span class="sxs-lookup"><span data-stu-id="32d8c-1094">automobile accident</span></span>
- <span data-ttu-id="32d8c-1095">hôpital pour malades</span><span class="sxs-lookup"><span data-stu-id="32d8c-1095">patient hospital</span></span>
- <span data-ttu-id="32d8c-1096">psychiatrist</span><span class="sxs-lookup"><span data-stu-id="32d8c-1096">psychiatrist</span></span>
- <span data-ttu-id="32d8c-1097">indemnisation des salariés</span><span class="sxs-lookup"><span data-stu-id="32d8c-1097">workers compensation</span></span>
- <span data-ttu-id="32d8c-1098">incapacité</span><span class="sxs-lookup"><span data-stu-id="32d8c-1098">disability</span></span>
      
## <a name="canada-passport-number"></a><span data-ttu-id="32d8c-1099">Numéro de passeport Canada</span><span class="sxs-lookup"><span data-stu-id="32d8c-1099">Canada Passport Number</span></span>

### <a name="format"></a><span data-ttu-id="32d8c-1100">Format</span><span class="sxs-lookup"><span data-stu-id="32d8c-1100">Format</span></span>

<span data-ttu-id="32d8c-1101">Deux lettres majuscules suivies de six chiffres</span><span class="sxs-lookup"><span data-stu-id="32d8c-1101">Two uppercase letters followed by six digits</span></span>

### <a name="pattern"></a><span data-ttu-id="32d8c-1102">Modèle</span><span class="sxs-lookup"><span data-stu-id="32d8c-1102">Pattern</span></span>

<span data-ttu-id="32d8c-1103">Deux lettres majuscules suivies de six chiffres</span><span class="sxs-lookup"><span data-stu-id="32d8c-1103">Two uppercase letters followed by six digits</span></span>

### <a name="checksum"></a><span data-ttu-id="32d8c-1104">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="32d8c-1104">Checksum</span></span>

<span data-ttu-id="32d8c-1105">Non</span><span class="sxs-lookup"><span data-stu-id="32d8c-1105">No</span></span>

### <a name="definition"></a><span data-ttu-id="32d8c-1106">Définition</span><span class="sxs-lookup"><span data-stu-id="32d8c-1106">Definition</span></span>

<span data-ttu-id="32d8c-1107">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="32d8c-1107">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="32d8c-1108">L’expression régulière Regex_canada_passport_number trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="32d8c-1108">The regular expression Regex_canada_passport_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="32d8c-1109">Un mot clé depuis Keyword_canada_passport_number ou Keyword_passport est trouvé.</span><span class="sxs-lookup"><span data-stu-id="32d8c-1109">A keyword from Keyword_canada_passport_number or Keyword_passport is found.</span></span>

```xml 
<!-- Canada Passport Number -->
<Entity id="14d0db8b-498a-43ed-9fca-f6097ae687eb" patternsProximity="300" recommendedConfidence="75">
  <Pattern confidenceLevel="75">
        <IdMatch idRef="Regex_canada_passport_number" />
        <Any minMatches="1">
          <Match idRef="Keyword_canada_passport_number" />
          <Match idRef="Keyword_passport" />
        </Any>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="32d8c-1110">Mots clés</span><span class="sxs-lookup"><span data-stu-id="32d8c-1110">Keywords</span></span>

#### <a name="keyword_canada_passport_number"></a><span data-ttu-id="32d8c-1111">Keyword_canada_passport_number</span><span class="sxs-lookup"><span data-stu-id="32d8c-1111">Keyword_canada_passport_number</span></span>

- <span data-ttu-id="32d8c-1112">citoyenneté canadienne</span><span class="sxs-lookup"><span data-stu-id="32d8c-1112">canadian citizenship</span></span>
- <span data-ttu-id="32d8c-1113">passeport canadien</span><span class="sxs-lookup"><span data-stu-id="32d8c-1113">canadian passport</span></span>
- <span data-ttu-id="32d8c-1114">demande de passeport</span><span class="sxs-lookup"><span data-stu-id="32d8c-1114">passport application</span></span>
- <span data-ttu-id="32d8c-1115">photos pour passeport</span><span class="sxs-lookup"><span data-stu-id="32d8c-1115">passport photos</span></span>
- <span data-ttu-id="32d8c-1116">traducteur agréé</span><span class="sxs-lookup"><span data-stu-id="32d8c-1116">certified translator</span></span>
- <span data-ttu-id="32d8c-1117">citoyens canadiens</span><span class="sxs-lookup"><span data-stu-id="32d8c-1117">canadian citizens</span></span>
- <span data-ttu-id="32d8c-1118">temps de traitement</span><span class="sxs-lookup"><span data-stu-id="32d8c-1118">processing times</span></span>
- <span data-ttu-id="32d8c-1119">demande de renouvellement</span><span class="sxs-lookup"><span data-stu-id="32d8c-1119">renewal application</span></span>

#### <a name="keyword_passport"></a><span data-ttu-id="32d8c-1120">Keyword_passport</span><span class="sxs-lookup"><span data-stu-id="32d8c-1120">Keyword_passport</span></span>

- <span data-ttu-id="32d8c-1121">Numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="32d8c-1121">Passport Number</span></span>
- <span data-ttu-id="32d8c-1122">N° de passeport</span><span class="sxs-lookup"><span data-stu-id="32d8c-1122">Passport No</span></span>
- <span data-ttu-id="32d8c-1123"># Passeport</span><span class="sxs-lookup"><span data-stu-id="32d8c-1123">Passport #</span></span>
- <span data-ttu-id="32d8c-1124">Tel #</span><span class="sxs-lookup"><span data-stu-id="32d8c-1124">Passport#</span></span>
- <span data-ttu-id="32d8c-1125">PassportID</span><span class="sxs-lookup"><span data-stu-id="32d8c-1125">PassportID</span></span>
- <span data-ttu-id="32d8c-1126">N ° passeport</span><span class="sxs-lookup"><span data-stu-id="32d8c-1126">Passportno</span></span>
- <span data-ttu-id="32d8c-1127">passportnumber</span><span class="sxs-lookup"><span data-stu-id="32d8c-1127">passportnumber</span></span>
- <span data-ttu-id="32d8c-1128">パスポート</span><span class="sxs-lookup"><span data-stu-id="32d8c-1128">パスポート</span></span>
- <span data-ttu-id="32d8c-1129">パスポート番号</span><span class="sxs-lookup"><span data-stu-id="32d8c-1129">パスポート番号</span></span>
- <span data-ttu-id="32d8c-1130">パスポートのNum</span><span class="sxs-lookup"><span data-stu-id="32d8c-1130">パスポートのNum</span></span>
- <span data-ttu-id="32d8c-1131">パスポート＃</span><span class="sxs-lookup"><span data-stu-id="32d8c-1131">パスポート＃</span></span>
- <span data-ttu-id="32d8c-1132">Numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="32d8c-1132">Numéro de passeport</span></span>
- <span data-ttu-id="32d8c-1133">Passeport n°</span><span class="sxs-lookup"><span data-stu-id="32d8c-1133">Passeport n °</span></span>
- <span data-ttu-id="32d8c-1134">Passeport numéro</span><span class="sxs-lookup"><span data-stu-id="32d8c-1134">Passeport Non</span></span>
- <span data-ttu-id="32d8c-1135"># Passeport</span><span class="sxs-lookup"><span data-stu-id="32d8c-1135">Passeport #</span></span>
- <span data-ttu-id="32d8c-1136">Passeport #</span><span class="sxs-lookup"><span data-stu-id="32d8c-1136">Passeport#</span></span>
- <span data-ttu-id="32d8c-1137">PasseportNon</span><span class="sxs-lookup"><span data-stu-id="32d8c-1137">PasseportNon</span></span>
- <span data-ttu-id="32d8c-1138">Passeportn °</span><span class="sxs-lookup"><span data-stu-id="32d8c-1138">Passeportn °</span></span>
   
## <a name="canada-personal-health-identification-number-phin"></a><span data-ttu-id="32d8c-1139">NIMP (numéro d’identification médicale personnel) Canada</span><span class="sxs-lookup"><span data-stu-id="32d8c-1139">Canada Personal Health Identification Number (PHIN)</span></span>

### <a name="format"></a><span data-ttu-id="32d8c-1140">Format</span><span class="sxs-lookup"><span data-stu-id="32d8c-1140">Format</span></span>

<span data-ttu-id="32d8c-1141">Neuf chiffres</span><span class="sxs-lookup"><span data-stu-id="32d8c-1141">Nine digits</span></span>

### <a name="pattern"></a><span data-ttu-id="32d8c-1142">Modèle</span><span class="sxs-lookup"><span data-stu-id="32d8c-1142">Pattern</span></span>

<span data-ttu-id="32d8c-1143">Neuf chiffres</span><span class="sxs-lookup"><span data-stu-id="32d8c-1143">Nine digits</span></span>

### <a name="checksum"></a><span data-ttu-id="32d8c-1144">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="32d8c-1144">Checksum</span></span>

<span data-ttu-id="32d8c-1145">Non</span><span class="sxs-lookup"><span data-stu-id="32d8c-1145">No</span></span>

### <a name="definition"></a><span data-ttu-id="32d8c-1146">Définition</span><span class="sxs-lookup"><span data-stu-id="32d8c-1146">Definition</span></span>

<span data-ttu-id="32d8c-1147">Une stratégie DLP est sûre à 75% d’avoir détecté ce type d’informations sensibles si, dans une proximité de 300 caractères : l’expression régulière Regex_canada_phin trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="32d8c-1147">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters: The regular expression Regex_canada_phin finds content that matches the pattern.</span></span>
<span data-ttu-id="32d8c-1148">Au moins deux mots clés provenant d’Keyword_canada_phin ou de Keyword_canada_provinces sont trouvés..</span><span class="sxs-lookup"><span data-stu-id="32d8c-1148">At least two keywords from Keyword_canada_phin or Keyword_canada_provinces are found..</span></span>

```xml
<!-- Canada PHIN -->
<Entity id="722e12ac-c89a-4ec8-a1b7-fea3469f89db" patternsProximity="300" recommendedConfidence="75">
  <Pattern confidenceLevel="75">
        <IdMatch idRef="Regex_canada_phin" />
        <Any minMatches="2">
          <Match idRef="Keyword_canada_phin" />
          <Match idRef="Keyword_canada_provinces" />
        </Any>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="32d8c-1149">Mots clés</span><span class="sxs-lookup"><span data-stu-id="32d8c-1149">Keywords</span></span>

#### <a name="keyword_canada_phin"></a><span data-ttu-id="32d8c-1150">Keyword_canada_phin</span><span class="sxs-lookup"><span data-stu-id="32d8c-1150">Keyword_canada_phin</span></span>

- <span data-ttu-id="32d8c-1151">numéro d’assurance sociale</span><span class="sxs-lookup"><span data-stu-id="32d8c-1151">social insurance number</span></span>
- <span data-ttu-id="32d8c-1152">loi sur les renseignements médicaux</span><span class="sxs-lookup"><span data-stu-id="32d8c-1152">health information act</span></span>
- <span data-ttu-id="32d8c-1153">renseignements relatifs à l’impôt sur le revenu</span><span class="sxs-lookup"><span data-stu-id="32d8c-1153">income tax information</span></span>
- <span data-ttu-id="32d8c-1154">santé Manitoba</span><span class="sxs-lookup"><span data-stu-id="32d8c-1154">manitoba health</span></span>
- <span data-ttu-id="32d8c-1155">enregistrement aux services de santé</span><span class="sxs-lookup"><span data-stu-id="32d8c-1155">health registration</span></span>
- <span data-ttu-id="32d8c-1156">achats de médicaments sur ordonnance</span><span class="sxs-lookup"><span data-stu-id="32d8c-1156">prescription purchases</span></span>
- <span data-ttu-id="32d8c-1157">admissibilité aux prestations</span><span class="sxs-lookup"><span data-stu-id="32d8c-1157">benefit eligibility</span></span>
- <span data-ttu-id="32d8c-1158">santé personnelle</span><span class="sxs-lookup"><span data-stu-id="32d8c-1158">personal health</span></span>
- <span data-ttu-id="32d8c-1159">procuration</span><span class="sxs-lookup"><span data-stu-id="32d8c-1159">power of attorney</span></span>
- <span data-ttu-id="32d8c-1160">numéro d’enregistrement</span><span class="sxs-lookup"><span data-stu-id="32d8c-1160">registration number</span></span>
- <span data-ttu-id="32d8c-1161">numéro d’assurance-maladie</span><span class="sxs-lookup"><span data-stu-id="32d8c-1161">personal health number</span></span>
- <span data-ttu-id="32d8c-1162">recommandation par le médecin</span><span class="sxs-lookup"><span data-stu-id="32d8c-1162">practitioner referral</span></span>
- <span data-ttu-id="32d8c-1163">professionnel de bien-être</span><span class="sxs-lookup"><span data-stu-id="32d8c-1163">wellness professional</span></span>
- <span data-ttu-id="32d8c-1164">orientation d’un patient</span><span class="sxs-lookup"><span data-stu-id="32d8c-1164">patient referral</span></span>
- <span data-ttu-id="32d8c-1165">santé et bien-être</span><span class="sxs-lookup"><span data-stu-id="32d8c-1165">health and wellness</span></span>

#### <a name="keyword_canada_provinces"></a><span data-ttu-id="32d8c-1166">Keyword_canada_provinces</span><span class="sxs-lookup"><span data-stu-id="32d8c-1166">Keyword_canada_provinces</span></span>

- <span data-ttu-id="32d8c-1167">Nunavut</span><span class="sxs-lookup"><span data-stu-id="32d8c-1167">Nunavut</span></span>
- <span data-ttu-id="32d8c-1168">Régime</span><span class="sxs-lookup"><span data-stu-id="32d8c-1168">Quebec</span></span>
- <span data-ttu-id="32d8c-1169">Territoires du Nord-Ouest</span><span class="sxs-lookup"><span data-stu-id="32d8c-1169">Northwest Territories</span></span>
- <span data-ttu-id="32d8c-1170">Brand</span><span class="sxs-lookup"><span data-stu-id="32d8c-1170">Ontario</span></span>
- <span data-ttu-id="32d8c-1171">Colombie-britannique</span><span class="sxs-lookup"><span data-stu-id="32d8c-1171">British Columbia</span></span>
- <span data-ttu-id="32d8c-1172">Alberta</span><span class="sxs-lookup"><span data-stu-id="32d8c-1172">Alberta</span></span>
- <span data-ttu-id="32d8c-1173">En-dessus</span><span class="sxs-lookup"><span data-stu-id="32d8c-1173">Saskatchewan</span></span>
- <span data-ttu-id="32d8c-1174">Manitoba</span><span class="sxs-lookup"><span data-stu-id="32d8c-1174">Manitoba</span></span>
- <span data-ttu-id="32d8c-1175">Yukon</span><span class="sxs-lookup"><span data-stu-id="32d8c-1175">Yukon</span></span>
- <span data-ttu-id="32d8c-1176">Terre-Neuve-et-Labrador</span><span class="sxs-lookup"><span data-stu-id="32d8c-1176">Newfoundland and Labrador</span></span>
- <span data-ttu-id="32d8c-1177">Nouveau-Brunswick</span><span class="sxs-lookup"><span data-stu-id="32d8c-1177">New Brunswick</span></span>
- <span data-ttu-id="32d8c-1178">Nouvelle-Écosse</span><span class="sxs-lookup"><span data-stu-id="32d8c-1178">Nova Scotia</span></span>
- <span data-ttu-id="32d8c-1179">Île-du-Prince-Édouard</span><span class="sxs-lookup"><span data-stu-id="32d8c-1179">Prince Edward Island</span></span>
- <span data-ttu-id="32d8c-1180">Canada</span><span class="sxs-lookup"><span data-stu-id="32d8c-1180">Canada</span></span>
   
## <a name="canada-social-insurance-number"></a><span data-ttu-id="32d8c-1181">Numéro d'assurance sociale Canada</span><span class="sxs-lookup"><span data-stu-id="32d8c-1181">Canada Social Insurance Number</span></span>

### <a name="format"></a><span data-ttu-id="32d8c-1182">Format</span><span class="sxs-lookup"><span data-stu-id="32d8c-1182">Format</span></span>

<span data-ttu-id="32d8c-1183">Neuf chiffres avec éventuellement des traits d’union ou des espaces</span><span class="sxs-lookup"><span data-stu-id="32d8c-1183">Nine digits with optional hyphens or spaces</span></span>

### <a name="pattern"></a><span data-ttu-id="32d8c-1184">Modèle</span><span class="sxs-lookup"><span data-stu-id="32d8c-1184">Pattern</span></span>

<span data-ttu-id="32d8c-1185">Avec</span><span class="sxs-lookup"><span data-stu-id="32d8c-1185">Formatted:</span></span>
- <span data-ttu-id="32d8c-1186">Trois chiffres</span><span class="sxs-lookup"><span data-stu-id="32d8c-1186">Three digits</span></span> 
- <span data-ttu-id="32d8c-1187">Un trait d’union ou un espace</span><span class="sxs-lookup"><span data-stu-id="32d8c-1187">A hyphen or space</span></span> 
- <span data-ttu-id="32d8c-1188">Trois chiffres</span><span class="sxs-lookup"><span data-stu-id="32d8c-1188">Three digits</span></span> 
- <span data-ttu-id="32d8c-1189">Un trait d’union ou un espace</span><span class="sxs-lookup"><span data-stu-id="32d8c-1189">A hyphen or space</span></span> 
- <span data-ttu-id="32d8c-1190">Trois chiffres</span><span class="sxs-lookup"><span data-stu-id="32d8c-1190">Three digits</span></span>

<span data-ttu-id="32d8c-1191">Non mis en forme : neuf chiffres</span><span class="sxs-lookup"><span data-stu-id="32d8c-1191">Unformatted: Nine digits</span></span>

### <a name="checksum"></a><span data-ttu-id="32d8c-1192">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="32d8c-1192">Checksum</span></span>

<span data-ttu-id="32d8c-1193">Oui</span><span class="sxs-lookup"><span data-stu-id="32d8c-1193">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="32d8c-1194">Définition</span><span class="sxs-lookup"><span data-stu-id="32d8c-1194">Definition</span></span>

<span data-ttu-id="32d8c-1195">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="32d8c-1195">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="32d8c-1196">La fonction Func_canadian_sin trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="32d8c-1196">The function Func_canadian_sin finds content that matches the pattern.</span></span>
- <span data-ttu-id="32d8c-1197">Au moins deux des éléments suivants, quelle que soit la combinaison :</span><span class="sxs-lookup"><span data-stu-id="32d8c-1197">At least two of any combination of the following:</span></span>
    - <span data-ttu-id="32d8c-1198">Un mot clé figurant dans la liste Keyword_sin est trouvé.</span><span class="sxs-lookup"><span data-stu-id="32d8c-1198">A keyword from Keyword_sin is found.</span></span>
    - <span data-ttu-id="32d8c-1199">Un mot clé figurant dans la liste Keyword_sin_collaborative est trouvé.</span><span class="sxs-lookup"><span data-stu-id="32d8c-1199">A keyword from Keyword_sin_collaborative is found.</span></span>
    - <span data-ttu-id="32d8c-1200">La fonction Func_eu_date trouve une date au format correct.</span><span class="sxs-lookup"><span data-stu-id="32d8c-1200">The function Func_eu_date finds a date in the right date format.</span></span>
- <span data-ttu-id="32d8c-1201">La somme de contrôle est correcte.</span><span class="sxs-lookup"><span data-stu-id="32d8c-1201">The checksum passes.</span></span>

<span data-ttu-id="32d8c-1202">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="32d8c-1202">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="32d8c-1203">La fonction Func_unformatted_canadian_sin trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="32d8c-1203">The function Func_unformatted_canadian_sin finds content that matches the pattern.</span></span>
- <span data-ttu-id="32d8c-1204">Un mot clé figurant dans la liste Keyword_sin est trouvé.</span><span class="sxs-lookup"><span data-stu-id="32d8c-1204">A keyword from Keyword_sin is found.</span></span>
- <span data-ttu-id="32d8c-1205">La somme de contrôle est correcte.</span><span class="sxs-lookup"><span data-stu-id="32d8c-1205">The checksum passes.</span></span>

```xml
<!-- Canada Social Insurance Number -->
<Entity id="a2f29c85-ecb8-4514-a610-364790c0773e" patternsProximity="300" recommendedConfidence="75">
  <Pattern confidenceLevel="85">
        <IdMatch idRef="Func_canadian_sin" />
        <Any minMatches="2">
          <Match idRef="Keyword_sin" />
          <Match idRef="Keyword_sin_collaborative" />
          <Match idRef="Func_eu_date" />
        </Any>
  </Pattern>
  <Pattern confidenceLevel="75">
        <IdMatch idRef="Func_unformatted_canadian_sin" />
        <Match idRef="Keyword_sin" />
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="32d8c-1206">Mots clés</span><span class="sxs-lookup"><span data-stu-id="32d8c-1206">Keywords</span></span>

#### <a name="keyword_sin"></a><span data-ttu-id="32d8c-1207">Keyword_sin</span><span class="sxs-lookup"><span data-stu-id="32d8c-1207">Keyword_sin</span></span>

- <span data-ttu-id="32d8c-1208">assoc</span><span class="sxs-lookup"><span data-stu-id="32d8c-1208">sin</span></span> 
- <span data-ttu-id="32d8c-1209">assurance sociale</span><span class="sxs-lookup"><span data-stu-id="32d8c-1209">social insurance</span></span> 
- <span data-ttu-id="32d8c-1210">numéro d’assurance sociale</span><span class="sxs-lookup"><span data-stu-id="32d8c-1210">numero d'assurance sociale</span></span> 
- <span data-ttu-id="32d8c-1211">péchés</span><span class="sxs-lookup"><span data-stu-id="32d8c-1211">sins</span></span> 
- <span data-ttu-id="32d8c-1212">SSN</span><span class="sxs-lookup"><span data-stu-id="32d8c-1212">ssn</span></span> 
- <span data-ttu-id="32d8c-1213">numéros</span><span class="sxs-lookup"><span data-stu-id="32d8c-1213">ssns</span></span> 
- <span data-ttu-id="32d8c-1214">sécurité sociale</span><span class="sxs-lookup"><span data-stu-id="32d8c-1214">social security</span></span> 
- <span data-ttu-id="32d8c-1215">numéro d’assurance sociale</span><span class="sxs-lookup"><span data-stu-id="32d8c-1215">numero d'assurance social</span></span> 
- <span data-ttu-id="32d8c-1216">numéro d’identification nationale</span><span class="sxs-lookup"><span data-stu-id="32d8c-1216">national identification number</span></span> 
- <span data-ttu-id="32d8c-1217">id national</span><span class="sxs-lookup"><span data-stu-id="32d8c-1217">national id</span></span> 
- <span data-ttu-id="32d8c-1218">sine #</span><span class="sxs-lookup"><span data-stu-id="32d8c-1218">sin#</span></span> 
- <span data-ttu-id="32d8c-1219">ass soc</span><span class="sxs-lookup"><span data-stu-id="32d8c-1219">soc ins</span></span> 
- <span data-ttu-id="32d8c-1220">ass sociale</span><span class="sxs-lookup"><span data-stu-id="32d8c-1220">social ins</span></span> 

#### <a name="keyword_sin_collaborative"></a><span data-ttu-id="32d8c-1221">Keyword_sin_collaborative</span><span class="sxs-lookup"><span data-stu-id="32d8c-1221">Keyword_sin_collaborative</span></span>

- <span data-ttu-id="32d8c-1222">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="32d8c-1222">driver's license</span></span> 
- <span data-ttu-id="32d8c-1223">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="32d8c-1223">drivers license</span></span> 
- <span data-ttu-id="32d8c-1224">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="32d8c-1224">driver's licence</span></span> 
- <span data-ttu-id="32d8c-1225">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="32d8c-1225">drivers licence</span></span> 
- <span data-ttu-id="32d8c-1226">DOB</span><span class="sxs-lookup"><span data-stu-id="32d8c-1226">DOB</span></span> 
- <span data-ttu-id="32d8c-1227">Birthdate</span><span class="sxs-lookup"><span data-stu-id="32d8c-1227">Birthdate</span></span> 
- <span data-ttu-id="32d8c-1228">Birthday</span><span class="sxs-lookup"><span data-stu-id="32d8c-1228">Birthday</span></span> 
- <span data-ttu-id="32d8c-1229">Date of Birth</span><span class="sxs-lookup"><span data-stu-id="32d8c-1229">Date of Birth</span></span> 
   
## <a name="chile-identity-card-number"></a><span data-ttu-id="32d8c-1230">	Numéro de carte d’identité Chili</span><span class="sxs-lookup"><span data-stu-id="32d8c-1230">Chile Identity Card Number</span></span>

### <a name="format"></a><span data-ttu-id="32d8c-1231">Format</span><span class="sxs-lookup"><span data-stu-id="32d8c-1231">Format</span></span>

<span data-ttu-id="32d8c-1232">7-8 chiffres plus des délimiteurs un chiffre ou une lettre</span><span class="sxs-lookup"><span data-stu-id="32d8c-1232">7-8 digits plus delimiters a check digit or letter</span></span>

### <a name="pattern"></a><span data-ttu-id="32d8c-1233">Modèle</span><span class="sxs-lookup"><span data-stu-id="32d8c-1233">Pattern</span></span>

<span data-ttu-id="32d8c-1234">7 ou 8 chiffres, plus des délimiteurs :</span><span class="sxs-lookup"><span data-stu-id="32d8c-1234">7-8 digits plus delimiters:</span></span>
- <span data-ttu-id="32d8c-1235">1 ou 2 chiffres </span><span class="sxs-lookup"><span data-stu-id="32d8c-1235">1-2 digits</span></span> 
- <span data-ttu-id="32d8c-1236">Un point </span><span class="sxs-lookup"><span data-stu-id="32d8c-1236">A period</span></span> 
- <span data-ttu-id="32d8c-1237">Trois chiffres</span><span class="sxs-lookup"><span data-stu-id="32d8c-1237">Three digits</span></span> 
- <span data-ttu-id="32d8c-1238">Un point </span><span class="sxs-lookup"><span data-stu-id="32d8c-1238">A period</span></span> 
- <span data-ttu-id="32d8c-1239">Trois chiffres</span><span class="sxs-lookup"><span data-stu-id="32d8c-1239">Three digits</span></span> 
- <span data-ttu-id="32d8c-1240">Un tiret</span><span class="sxs-lookup"><span data-stu-id="32d8c-1240">A dash</span></span> 
- <span data-ttu-id="32d8c-1241">Un chiffre ou une lettre (ne respectant pas la casse) de contrôle</span><span class="sxs-lookup"><span data-stu-id="32d8c-1241">One digit or letter (not case sensitive) which is a check digit</span></span>

### <a name="checksum"></a><span data-ttu-id="32d8c-1242">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="32d8c-1242">Checksum</span></span>

<span data-ttu-id="32d8c-1243">Oui</span><span class="sxs-lookup"><span data-stu-id="32d8c-1243">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="32d8c-1244">Définition</span><span class="sxs-lookup"><span data-stu-id="32d8c-1244">Definition</span></span>

<span data-ttu-id="32d8c-1245">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="32d8c-1245">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="32d8c-1246">La fonction Func_chile_id_card trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="32d8c-1246">The function Func_chile_id_card finds content that matches the pattern.</span></span>
- <span data-ttu-id="32d8c-1247">Un mot clé figurant dans la liste Keyword_chile_id_card est trouvé.</span><span class="sxs-lookup"><span data-stu-id="32d8c-1247">A keyword from Keyword_chile_id_card is found.</span></span>
- <span data-ttu-id="32d8c-1248">La somme de contrôle est correcte.</span><span class="sxs-lookup"><span data-stu-id="32d8c-1248">The checksum passes.</span></span>

<span data-ttu-id="32d8c-1249">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="32d8c-1249">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="32d8c-1250">La fonction Func_chile_id_card trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="32d8c-1250">The function Func_chile_id_card finds content that matches the pattern.</span></span>
- <span data-ttu-id="32d8c-1251">La somme de contrôle est correcte.</span><span class="sxs-lookup"><span data-stu-id="32d8c-1251">The checksum passes.</span></span>

```xml
<!-- Chile Identity Card Number -->
<Entity id="4e979794-49a0-407e-a0b9-2c536937b925" recommendedConfidence="85" patternsProximity="300">
  <Pattern confidenceLevel="85">
     <IdMatch idRef="Func_chile_id_card"/>
     <Match idRef="Keyword_chile_id_card"/>
  </Pattern>
  <Pattern confidenceLevel="75">
     <IdMatch idRef="Func_chile_id_card"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="32d8c-1252">Mots clés</span><span class="sxs-lookup"><span data-stu-id="32d8c-1252">Keywords</span></span>

#### <a name="keyword_chile_id_card"></a><span data-ttu-id="32d8c-1253">Keyword_chile_id_card</span><span class="sxs-lookup"><span data-stu-id="32d8c-1253">Keyword_chile_id_card</span></span>

- <span data-ttu-id="32d8c-1254">National Identification Number</span><span class="sxs-lookup"><span data-stu-id="32d8c-1254">National Identification Number</span></span> 
- <span data-ttu-id="32d8c-1255">Identity card</span><span class="sxs-lookup"><span data-stu-id="32d8c-1255">Identity card</span></span> 
- <span data-ttu-id="32d8c-1256">ID</span><span class="sxs-lookup"><span data-stu-id="32d8c-1256">ID</span></span> 
- <span data-ttu-id="32d8c-1257">Identificateur</span><span class="sxs-lookup"><span data-stu-id="32d8c-1257">Identification</span></span> 
- <span data-ttu-id="32d8c-1258">Rol Único Nacional</span><span class="sxs-lookup"><span data-stu-id="32d8c-1258">Rol Único Nacional</span></span> 
- <span data-ttu-id="32d8c-1259">GÉNÉRER</span><span class="sxs-lookup"><span data-stu-id="32d8c-1259">RUN</span></span> 
- <span data-ttu-id="32d8c-1260">Rol Único Tributario</span><span class="sxs-lookup"><span data-stu-id="32d8c-1260">Rol Único Tributario</span></span> 
- <span data-ttu-id="32d8c-1261">ROUTINE</span><span class="sxs-lookup"><span data-stu-id="32d8c-1261">RUT</span></span> 
- <span data-ttu-id="32d8c-1262">Cédula de Identidad</span><span class="sxs-lookup"><span data-stu-id="32d8c-1262">Cédula de Identidad</span></span> 
- <span data-ttu-id="32d8c-1263">Número De Identificación Nacional</span><span class="sxs-lookup"><span data-stu-id="32d8c-1263">Número De Identificación Nacional</span></span> 
- <span data-ttu-id="32d8c-1264">Tarjeta de identificación</span><span class="sxs-lookup"><span data-stu-id="32d8c-1264">Tarjeta de identificación</span></span> 
- <span data-ttu-id="32d8c-1265">Identificación</span><span class="sxs-lookup"><span data-stu-id="32d8c-1265">Identificación</span></span> 
   
## <a name="china-resident-identity-card-prc-number"></a><span data-ttu-id="32d8c-1266">	Numéro de carte d’identité de résident Chine (RPC)</span><span class="sxs-lookup"><span data-stu-id="32d8c-1266">China Resident Identity Card (PRC) Number</span></span>

### <a name="format"></a><span data-ttu-id="32d8c-1267">Format</span><span class="sxs-lookup"><span data-stu-id="32d8c-1267">Format</span></span>

<span data-ttu-id="32d8c-1268">18 chiffres</span><span class="sxs-lookup"><span data-stu-id="32d8c-1268">18 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="32d8c-1269">Modèle</span><span class="sxs-lookup"><span data-stu-id="32d8c-1269">Pattern</span></span>

<span data-ttu-id="32d8c-1270">18 chiffres :</span><span class="sxs-lookup"><span data-stu-id="32d8c-1270">18 digits:</span></span>
- <span data-ttu-id="32d8c-1271">Six chiffres qui composent un code d’adresse </span><span class="sxs-lookup"><span data-stu-id="32d8c-1271">Six digits which are an address code</span></span> 
- <span data-ttu-id="32d8c-1272">Huit chiffres sous la forme AAAAMMJJ qui correspondent à la date de naissance </span><span class="sxs-lookup"><span data-stu-id="32d8c-1272">Eight digits in the form YYYYMMDD which are the date of birth</span></span> 
- <span data-ttu-id="32d8c-1273">Trois chiffres qui correspondent à un code d’opération </span><span class="sxs-lookup"><span data-stu-id="32d8c-1273">Three digits which are an order code</span></span> 
- <span data-ttu-id="32d8c-1274">Un chiffre de contrôle</span><span class="sxs-lookup"><span data-stu-id="32d8c-1274">One digit which is a check digit</span></span>

### <a name="checksum"></a><span data-ttu-id="32d8c-1275">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="32d8c-1275">Checksum</span></span>

<span data-ttu-id="32d8c-1276">Oui</span><span class="sxs-lookup"><span data-stu-id="32d8c-1276">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="32d8c-1277">Définition</span><span class="sxs-lookup"><span data-stu-id="32d8c-1277">Definition</span></span>

<span data-ttu-id="32d8c-1278">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="32d8c-1278">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="32d8c-1279">La fonction Func_china_resident_id trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="32d8c-1279">The function Func_china_resident_id finds content that matches the pattern.</span></span>
- <span data-ttu-id="32d8c-1280">Un mot clé figurant dans la liste Keyword_china_resident_id est trouvé.</span><span class="sxs-lookup"><span data-stu-id="32d8c-1280">A keyword from Keyword_china_resident_id is found.</span></span>
- <span data-ttu-id="32d8c-1281">La somme de contrôle est correcte.</span><span class="sxs-lookup"><span data-stu-id="32d8c-1281">The checksum passes.</span></span>

<span data-ttu-id="32d8c-1282">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="32d8c-1282">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="32d8c-1283">La fonction Func_china_resident_id trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="32d8c-1283">The function Func_china_resident_id finds content that matches the pattern.</span></span>
- <span data-ttu-id="32d8c-1284">La somme de contrôle est correcte.</span><span class="sxs-lookup"><span data-stu-id="32d8c-1284">The checksum passes.</span></span>

```xml
<!-- China Resident Identity Card (PRC) Number -->
<Entity id="c92daa86-2d16-4871-901f-816b3f554fc1" recommendedConfidence="85" patternsProximity="300">
  <Pattern confidenceLevel="85">
     <IdMatch idRef="Func_china_resident_id"/>
     <Match idRef="Keyword_china_resident_id"/>
  </Pattern>
  <Pattern confidenceLevel="75">
     <IdMatch idRef="Func_china_resident_id"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="32d8c-1285">Mots clés</span><span class="sxs-lookup"><span data-stu-id="32d8c-1285">Keywords</span></span>

### <a name="keyword_china_resident_id"></a><span data-ttu-id="32d8c-1286">Keyword_china_resident_id</span><span class="sxs-lookup"><span data-stu-id="32d8c-1286">Keyword_china_resident_id</span></span>

- <span data-ttu-id="32d8c-1287">Resident Identity Card</span><span class="sxs-lookup"><span data-stu-id="32d8c-1287">Resident Identity Card</span></span> 
- <span data-ttu-id="32d8c-1288">FIGURANT</span><span class="sxs-lookup"><span data-stu-id="32d8c-1288">PRC</span></span> 
- <span data-ttu-id="32d8c-1289">National Identification Card</span><span class="sxs-lookup"><span data-stu-id="32d8c-1289">National Identification Card</span></span> 
- <span data-ttu-id="32d8c-1290">身份证</span><span class="sxs-lookup"><span data-stu-id="32d8c-1290">身份证</span></span> 
- <span data-ttu-id="32d8c-1291">居民 身份证</span><span class="sxs-lookup"><span data-stu-id="32d8c-1291">居民 身份证</span></span> 
- <span data-ttu-id="32d8c-1292">居民身份证</span><span class="sxs-lookup"><span data-stu-id="32d8c-1292">居民身份证</span></span> 
- <span data-ttu-id="32d8c-1293">鉴定</span><span class="sxs-lookup"><span data-stu-id="32d8c-1293">鉴定</span></span> 
- <span data-ttu-id="32d8c-1294">身分證</span><span class="sxs-lookup"><span data-stu-id="32d8c-1294">身分證</span></span> 
- <span data-ttu-id="32d8c-1295">居民 身份證</span><span class="sxs-lookup"><span data-stu-id="32d8c-1295">居民 身份證</span></span>
- <span data-ttu-id="32d8c-1296">鑑定</span><span class="sxs-lookup"><span data-stu-id="32d8c-1296">鑑定</span></span> 
   
## <a name="credit-card-number"></a><span data-ttu-id="32d8c-1297">Numéro de carte de crédit</span><span class="sxs-lookup"><span data-stu-id="32d8c-1297">Credit Card Number</span></span>

### <a name="format"></a><span data-ttu-id="32d8c-1298">Format</span><span class="sxs-lookup"><span data-stu-id="32d8c-1298">Format</span></span>

<span data-ttu-id="32d8c-1299">14 à 16 chiffres qui peuvent être mis en forme ou non (dddddddddddddddd) et qui doivent réussir le test Luhn.</span><span class="sxs-lookup"><span data-stu-id="32d8c-1299">14 to 16 digits which can be formatted or unformatted (dddddddddddddddd) and which must pass the Luhn test.</span></span>

### <a name="pattern"></a><span data-ttu-id="32d8c-1300">Modèle</span><span class="sxs-lookup"><span data-stu-id="32d8c-1300">Pattern</span></span>

<span data-ttu-id="32d8c-1301">Modèle très complexe et puissant qui détecte les cartes de visite de toutes les principales marques du monde, notamment Visa, MasterCard, Discover Card, JCB, American Express, etc.</span><span class="sxs-lookup"><span data-stu-id="32d8c-1301">Very complex and robust pattern that detects cards from all major brands worldwide, including Visa, MasterCard, Discover Card, JCB, American Express, gift cards, and diner cards.</span></span>

### <a name="checksum"></a><span data-ttu-id="32d8c-1302">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="32d8c-1302">Checksum</span></span>

<span data-ttu-id="32d8c-1303">Oui, la somme de contrôle de Luhn</span><span class="sxs-lookup"><span data-stu-id="32d8c-1303">Yes, the Luhn checksum</span></span>

### <a name="definition"></a><span data-ttu-id="32d8c-1304">Définition</span><span class="sxs-lookup"><span data-stu-id="32d8c-1304">Definition</span></span>

<span data-ttu-id="32d8c-1305">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="32d8c-1305">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="32d8c-1306">La fonction Func_credit_card trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="32d8c-1306">The function Func_credit_card finds content that matches the pattern.</span></span>
- <span data-ttu-id="32d8c-1307">L’une des affirmations suivantes est vraie :</span><span class="sxs-lookup"><span data-stu-id="32d8c-1307">One of the following is true:</span></span>
    - <span data-ttu-id="32d8c-1308">Un mot clé figurant dans la liste Keyword_cc_verification est trouvé.</span><span class="sxs-lookup"><span data-stu-id="32d8c-1308">A keyword from Keyword_cc_verification is found.</span></span>
    - <span data-ttu-id="32d8c-1309">Un mot clé figurant dans la liste Keyword_cc_name est trouvé.</span><span class="sxs-lookup"><span data-stu-id="32d8c-1309">A keyword from Keyword_cc_name is found.</span></span>
    - <span data-ttu-id="32d8c-1310">La fonction Func_expiration_date trouve une date au format correct.</span><span class="sxs-lookup"><span data-stu-id="32d8c-1310">The function Func_expiration_date finds a date in the right date format.</span></span>
- <span data-ttu-id="32d8c-1311">La somme de contrôle est correcte.</span><span class="sxs-lookup"><span data-stu-id="32d8c-1311">The checksum passes.</span></span>

<span data-ttu-id="32d8c-1312">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 65 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="32d8c-1312">A DLP policy is 65% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="32d8c-1313">La fonction Func_credit_card trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="32d8c-1313">The function Func_credit_card finds content that matches the pattern.</span></span>
- <span data-ttu-id="32d8c-1314">La somme de contrôle est correcte.</span><span class="sxs-lookup"><span data-stu-id="32d8c-1314">The checksum passes.</span></span>

```xml
<!-- Credit Card Number -->
<Entity id="50842eb7-edc8-4019-85dd-5a5c1f2bb085" patternsProximity="300" recommendedConfidence="85">
  <Pattern confidenceLevel="85">
        <IdMatch idRef="Func_credit_card" />
        <Any minMatches="1">
          <Match idRef="Keyword_cc_verification" />
          <Match idRef="Keyword_cc_name" />
          <Match idRef="Func_expiration_date" />
        </Any>
  </Pattern>
  <Pattern confidenceLevel="65">
        <IdMatch idRef="Func_credit_card" />
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="32d8c-1315">Mots clés</span><span class="sxs-lookup"><span data-stu-id="32d8c-1315">Keywords</span></span>

#### <a name="keyword_cc_verification"></a><span data-ttu-id="32d8c-1316">Keyword_cc_verification</span><span class="sxs-lookup"><span data-stu-id="32d8c-1316">Keyword_cc_verification</span></span>

- <span data-ttu-id="32d8c-1317">vérification de la carte</span><span class="sxs-lookup"><span data-stu-id="32d8c-1317">card verification</span></span>
- <span data-ttu-id="32d8c-1318">numéro d’identification de la carte</span><span class="sxs-lookup"><span data-stu-id="32d8c-1318">card identification number</span></span>
- <span data-ttu-id="32d8c-1319">cryptogramme</span><span class="sxs-lookup"><span data-stu-id="32d8c-1319">cvn</span></span>
- <span data-ttu-id="32d8c-1320">nic</span><span class="sxs-lookup"><span data-stu-id="32d8c-1320">cid</span></span>
- <span data-ttu-id="32d8c-1321">cvc2</span><span class="sxs-lookup"><span data-stu-id="32d8c-1321">cvc2</span></span>
- <span data-ttu-id="32d8c-1322">cvv2</span><span class="sxs-lookup"><span data-stu-id="32d8c-1322">cvv2</span></span>
- <span data-ttu-id="32d8c-1323">pin block</span><span class="sxs-lookup"><span data-stu-id="32d8c-1323">pin block</span></span>
- <span data-ttu-id="32d8c-1324">code de sécurité</span><span class="sxs-lookup"><span data-stu-id="32d8c-1324">security code</span></span>
- <span data-ttu-id="32d8c-1325">numéro de sécurité</span><span class="sxs-lookup"><span data-stu-id="32d8c-1325">security number</span></span>
- <span data-ttu-id="32d8c-1326">n° de sécurité</span><span class="sxs-lookup"><span data-stu-id="32d8c-1326">security no</span></span>
- <span data-ttu-id="32d8c-1327">numéro d’émission</span><span class="sxs-lookup"><span data-stu-id="32d8c-1327">issue number</span></span>
- <span data-ttu-id="32d8c-1328">n° d’émission</span><span class="sxs-lookup"><span data-stu-id="32d8c-1328">issue no</span></span>
- <span data-ttu-id="32d8c-1329">cryptogramme</span><span class="sxs-lookup"><span data-stu-id="32d8c-1329">cryptogramme</span></span>
- <span data-ttu-id="32d8c-1330">numéro de sécurité</span><span class="sxs-lookup"><span data-stu-id="32d8c-1330">numéro de sécurité</span></span>
- <span data-ttu-id="32d8c-1331">numéro de sécurité</span><span class="sxs-lookup"><span data-stu-id="32d8c-1331">numero de securite</span></span>
- <span data-ttu-id="32d8c-1332">kreditkartenprüfnummer</span><span class="sxs-lookup"><span data-stu-id="32d8c-1332">kreditkartenprüfnummer</span></span>
- <span data-ttu-id="32d8c-1333">kreditkartenprufnummer</span><span class="sxs-lookup"><span data-stu-id="32d8c-1333">kreditkartenprufnummer</span></span>
- <span data-ttu-id="32d8c-1334">prüfziffer</span><span class="sxs-lookup"><span data-stu-id="32d8c-1334">prüfziffer</span></span>
- <span data-ttu-id="32d8c-1335">prufziffer</span><span class="sxs-lookup"><span data-stu-id="32d8c-1335">prufziffer</span></span>
- <span data-ttu-id="32d8c-1336">sicherheits Kode</span><span class="sxs-lookup"><span data-stu-id="32d8c-1336">sicherheits Kode</span></span>
- <span data-ttu-id="32d8c-1337">sicherheitscode</span><span class="sxs-lookup"><span data-stu-id="32d8c-1337">sicherheitscode</span></span>
- <span data-ttu-id="32d8c-1338">sicherheitsnummer</span><span class="sxs-lookup"><span data-stu-id="32d8c-1338">sicherheitsnummer</span></span>
- <span data-ttu-id="32d8c-1339">verfalldatum</span><span class="sxs-lookup"><span data-stu-id="32d8c-1339">verfalldatum</span></span>
- <span data-ttu-id="32d8c-1340">codice di verifica</span><span class="sxs-lookup"><span data-stu-id="32d8c-1340">codice di verifica</span></span>
- <span data-ttu-id="32d8c-1341">contre.</span><span class="sxs-lookup"><span data-stu-id="32d8c-1341">cod.</span></span> <span data-ttu-id="32d8c-1342">sicurezza</span><span class="sxs-lookup"><span data-stu-id="32d8c-1342">sicurezza</span></span>
- <span data-ttu-id="32d8c-1343">cod sicurezza</span><span class="sxs-lookup"><span data-stu-id="32d8c-1343">cod sicurezza</span></span>
- <span data-ttu-id="32d8c-1344">n autorizzazione</span><span class="sxs-lookup"><span data-stu-id="32d8c-1344">n autorizzazione</span></span>
- <span data-ttu-id="32d8c-1345">código</span><span class="sxs-lookup"><span data-stu-id="32d8c-1345">código</span></span>
- <span data-ttu-id="32d8c-1346">codigo</span><span class="sxs-lookup"><span data-stu-id="32d8c-1346">codigo</span></span>
- <span data-ttu-id="32d8c-1347">contre.</span><span class="sxs-lookup"><span data-stu-id="32d8c-1347">cod.</span></span> <span data-ttu-id="32d8c-1348">SEG</span><span class="sxs-lookup"><span data-stu-id="32d8c-1348">seg</span></span>
- <span data-ttu-id="32d8c-1349">cod seg</span><span class="sxs-lookup"><span data-stu-id="32d8c-1349">cod seg</span></span>
- <span data-ttu-id="32d8c-1350">código de segurança</span><span class="sxs-lookup"><span data-stu-id="32d8c-1350">código de segurança</span></span>
- <span data-ttu-id="32d8c-1351">codigo de seguranca</span><span class="sxs-lookup"><span data-stu-id="32d8c-1351">codigo de seguranca</span></span>
- <span data-ttu-id="32d8c-1352">codigo de segurança</span><span class="sxs-lookup"><span data-stu-id="32d8c-1352">codigo de segurança</span></span>
- <span data-ttu-id="32d8c-1353">código de seguranca</span><span class="sxs-lookup"><span data-stu-id="32d8c-1353">código de seguranca</span></span>
- <span data-ttu-id="32d8c-1354">cód.</span><span class="sxs-lookup"><span data-stu-id="32d8c-1354">cód.</span></span> <span data-ttu-id="32d8c-1355">segurança</span><span class="sxs-lookup"><span data-stu-id="32d8c-1355">segurança</span></span>
- <span data-ttu-id="32d8c-1356">contre.</span><span class="sxs-lookup"><span data-stu-id="32d8c-1356">cod.</span></span> <span data-ttu-id="32d8c-1357">Seguranca COD.</span><span class="sxs-lookup"><span data-stu-id="32d8c-1357">seguranca cod.</span></span> <span data-ttu-id="32d8c-1358">segurança</span><span class="sxs-lookup"><span data-stu-id="32d8c-1358">segurança</span></span>
- <span data-ttu-id="32d8c-1359">cód.</span><span class="sxs-lookup"><span data-stu-id="32d8c-1359">cód.</span></span> <span data-ttu-id="32d8c-1360">seguranca</span><span class="sxs-lookup"><span data-stu-id="32d8c-1360">seguranca</span></span>
- <span data-ttu-id="32d8c-1361">cód segurança</span><span class="sxs-lookup"><span data-stu-id="32d8c-1361">cód segurança</span></span>
- <span data-ttu-id="32d8c-1362">COD Seguranca COD Segurança</span><span class="sxs-lookup"><span data-stu-id="32d8c-1362">cod seguranca cod segurança</span></span>
- <span data-ttu-id="32d8c-1363">cód seguranca</span><span class="sxs-lookup"><span data-stu-id="32d8c-1363">cód seguranca</span></span>
- <span data-ttu-id="32d8c-1364">número de verificação</span><span class="sxs-lookup"><span data-stu-id="32d8c-1364">número de verificação</span></span>
- <span data-ttu-id="32d8c-1365">numero de verificacao</span><span class="sxs-lookup"><span data-stu-id="32d8c-1365">numero de verificacao</span></span>
- <span data-ttu-id="32d8c-1366">ablauf</span><span class="sxs-lookup"><span data-stu-id="32d8c-1366">ablauf</span></span>
- <span data-ttu-id="32d8c-1367">gültig bis</span><span class="sxs-lookup"><span data-stu-id="32d8c-1367">gültig bis</span></span>
- <span data-ttu-id="32d8c-1368">gültigkeitsdatum</span><span class="sxs-lookup"><span data-stu-id="32d8c-1368">gültigkeitsdatum</span></span>
- <span data-ttu-id="32d8c-1369">gultig bis</span><span class="sxs-lookup"><span data-stu-id="32d8c-1369">gultig bis</span></span>
- <span data-ttu-id="32d8c-1370">gultigkeitsdatum</span><span class="sxs-lookup"><span data-stu-id="32d8c-1370">gultigkeitsdatum</span></span>
- <span data-ttu-id="32d8c-1371">scadenza</span><span class="sxs-lookup"><span data-stu-id="32d8c-1371">scadenza</span></span>
- <span data-ttu-id="32d8c-1372">data scad</span><span class="sxs-lookup"><span data-stu-id="32d8c-1372">data scad</span></span>
- <span data-ttu-id="32d8c-1373">fecha de expiracion</span><span class="sxs-lookup"><span data-stu-id="32d8c-1373">fecha de expiracion</span></span>
- <span data-ttu-id="32d8c-1374">fecha de venc</span><span class="sxs-lookup"><span data-stu-id="32d8c-1374">fecha de venc</span></span>
- <span data-ttu-id="32d8c-1375">vencimiento</span><span class="sxs-lookup"><span data-stu-id="32d8c-1375">vencimiento</span></span>
- <span data-ttu-id="32d8c-1376">válido hasta</span><span class="sxs-lookup"><span data-stu-id="32d8c-1376">válido hasta</span></span>
- <span data-ttu-id="32d8c-1377">valido hasta</span><span class="sxs-lookup"><span data-stu-id="32d8c-1377">valido hasta</span></span>
- <span data-ttu-id="32d8c-1378">vto</span><span class="sxs-lookup"><span data-stu-id="32d8c-1378">vto</span></span>
- <span data-ttu-id="32d8c-1379">data de expiração</span><span class="sxs-lookup"><span data-stu-id="32d8c-1379">data de expiração</span></span>
- <span data-ttu-id="32d8c-1380">data de expiracao</span><span class="sxs-lookup"><span data-stu-id="32d8c-1380">data de expiracao</span></span>
- <span data-ttu-id="32d8c-1381">data em que expira</span><span class="sxs-lookup"><span data-stu-id="32d8c-1381">data em que expira</span></span>
- <span data-ttu-id="32d8c-1382">validade</span><span class="sxs-lookup"><span data-stu-id="32d8c-1382">validade</span></span>
- <span data-ttu-id="32d8c-1383">valorisation</span><span class="sxs-lookup"><span data-stu-id="32d8c-1383">valor</span></span>
- <span data-ttu-id="32d8c-1384">vencimento</span><span class="sxs-lookup"><span data-stu-id="32d8c-1384">vencimento</span></span>
- <span data-ttu-id="32d8c-1385">Venc</span><span class="sxs-lookup"><span data-stu-id="32d8c-1385">Venc</span></span> 

#### <a name="keyword_cc_name"></a><span data-ttu-id="32d8c-1386">Keyword_cc_name</span><span class="sxs-lookup"><span data-stu-id="32d8c-1386">Keyword_cc_name</span></span>

- <span data-ttu-id="32d8c-1387">American</span><span class="sxs-lookup"><span data-stu-id="32d8c-1387">amex</span></span>
- <span data-ttu-id="32d8c-1388">american express</span><span class="sxs-lookup"><span data-stu-id="32d8c-1388">american express</span></span>
- <span data-ttu-id="32d8c-1389">americanexpress</span><span class="sxs-lookup"><span data-stu-id="32d8c-1389">americanexpress</span></span>
- <span data-ttu-id="32d8c-1390">Délivrance</span><span class="sxs-lookup"><span data-stu-id="32d8c-1390">Visa</span></span>
- <span data-ttu-id="32d8c-1391">MasterCard</span><span class="sxs-lookup"><span data-stu-id="32d8c-1391">mastercard</span></span>
- <span data-ttu-id="32d8c-1392">master card</span><span class="sxs-lookup"><span data-stu-id="32d8c-1392">master card</span></span>
- <span data-ttu-id="32d8c-1393">McDonald</span><span class="sxs-lookup"><span data-stu-id="32d8c-1393">mc</span></span> 
- <span data-ttu-id="32d8c-1394">MasterCard</span><span class="sxs-lookup"><span data-stu-id="32d8c-1394">mastercards</span></span>
- <span data-ttu-id="32d8c-1395">master cards</span><span class="sxs-lookup"><span data-stu-id="32d8c-1395">master cards</span></span>
- <span data-ttu-id="32d8c-1396">diner’s Club</span><span class="sxs-lookup"><span data-stu-id="32d8c-1396">diner's Club</span></span>
- <span data-ttu-id="32d8c-1397">diners club</span><span class="sxs-lookup"><span data-stu-id="32d8c-1397">diners club</span></span>
- <span data-ttu-id="32d8c-1398">dinersclub</span><span class="sxs-lookup"><span data-stu-id="32d8c-1398">dinersclub</span></span>
- <span data-ttu-id="32d8c-1399">discover card</span><span class="sxs-lookup"><span data-stu-id="32d8c-1399">discover card</span></span>
- <span data-ttu-id="32d8c-1400">discovercard</span><span class="sxs-lookup"><span data-stu-id="32d8c-1400">discovercard</span></span>
- <span data-ttu-id="32d8c-1401">discover cards</span><span class="sxs-lookup"><span data-stu-id="32d8c-1401">discover cards</span></span>
- <span data-ttu-id="32d8c-1402">JCB</span><span class="sxs-lookup"><span data-stu-id="32d8c-1402">JCB</span></span>
- <span data-ttu-id="32d8c-1403">japanese card bureau</span><span class="sxs-lookup"><span data-stu-id="32d8c-1403">japanese card bureau</span></span>
- <span data-ttu-id="32d8c-1404">carte blanche</span><span class="sxs-lookup"><span data-stu-id="32d8c-1404">carte blanche</span></span>
- <span data-ttu-id="32d8c-1405">carteblanche</span><span class="sxs-lookup"><span data-stu-id="32d8c-1405">carteblanche</span></span>
- <span data-ttu-id="32d8c-1406">carte de crédit</span><span class="sxs-lookup"><span data-stu-id="32d8c-1406">credit card</span></span>
- <span data-ttu-id="32d8c-1407">CC #</span><span class="sxs-lookup"><span data-stu-id="32d8c-1407">cc#</span></span>
- <span data-ttu-id="32d8c-1408">n ° de CC :</span><span class="sxs-lookup"><span data-stu-id="32d8c-1408">cc#:</span></span>
- <span data-ttu-id="32d8c-1409">date d’expiration</span><span class="sxs-lookup"><span data-stu-id="32d8c-1409">expiration date</span></span>
- <span data-ttu-id="32d8c-1410">date d’exp</span><span class="sxs-lookup"><span data-stu-id="32d8c-1410">exp date</span></span>
- <span data-ttu-id="32d8c-1411">date d’expiration</span><span class="sxs-lookup"><span data-stu-id="32d8c-1411">expiry date</span></span>
- <span data-ttu-id="32d8c-1412">Date d’expiration</span><span class="sxs-lookup"><span data-stu-id="32d8c-1412">date d'expiration</span></span>
- <span data-ttu-id="32d8c-1413">date d’exp</span><span class="sxs-lookup"><span data-stu-id="32d8c-1413">date d'exp</span></span>
- <span data-ttu-id="32d8c-1414">date expiration</span><span class="sxs-lookup"><span data-stu-id="32d8c-1414">date expiration</span></span>
- <span data-ttu-id="32d8c-1415">carte bancaire</span><span class="sxs-lookup"><span data-stu-id="32d8c-1415">bank card</span></span>
- <span data-ttu-id="32d8c-1416">bankcard</span><span class="sxs-lookup"><span data-stu-id="32d8c-1416">bankcard</span></span>
- <span data-ttu-id="32d8c-1417">numéro de carte</span><span class="sxs-lookup"><span data-stu-id="32d8c-1417">card number</span></span>
- <span data-ttu-id="32d8c-1418">num de carte</span><span class="sxs-lookup"><span data-stu-id="32d8c-1418">card num</span></span>
- <span data-ttu-id="32d8c-1419">carte</span><span class="sxs-lookup"><span data-stu-id="32d8c-1419">cardnumber</span></span>
- <span data-ttu-id="32d8c-1420">carte</span><span class="sxs-lookup"><span data-stu-id="32d8c-1420">cardnumbers</span></span>
- <span data-ttu-id="32d8c-1421">numéros de carte</span><span class="sxs-lookup"><span data-stu-id="32d8c-1421">card numbers</span></span>
- <span data-ttu-id="32d8c-1422">CreditCard</span><span class="sxs-lookup"><span data-stu-id="32d8c-1422">creditcard</span></span>
- <span data-ttu-id="32d8c-1423">cartes de crédit</span><span class="sxs-lookup"><span data-stu-id="32d8c-1423">credit cards</span></span>
- <span data-ttu-id="32d8c-1424">crédit</span><span class="sxs-lookup"><span data-stu-id="32d8c-1424">creditcards</span></span>
- <span data-ttu-id="32d8c-1425">CCN</span><span class="sxs-lookup"><span data-stu-id="32d8c-1425">ccn</span></span>
- <span data-ttu-id="32d8c-1426">titulaire de la carte</span><span class="sxs-lookup"><span data-stu-id="32d8c-1426">card holder</span></span>
- <span data-ttu-id="32d8c-1427">titulaires</span><span class="sxs-lookup"><span data-stu-id="32d8c-1427">cardholder</span></span>
- <span data-ttu-id="32d8c-1428">titulaires de la carte</span><span class="sxs-lookup"><span data-stu-id="32d8c-1428">card holders</span></span>
- <span data-ttu-id="32d8c-1429">titulaires</span><span class="sxs-lookup"><span data-stu-id="32d8c-1429">cardholders</span></span>
- <span data-ttu-id="32d8c-1430">carte de vérification</span><span class="sxs-lookup"><span data-stu-id="32d8c-1430">check card</span></span>
- <span data-ttu-id="32d8c-1431">carte</span><span class="sxs-lookup"><span data-stu-id="32d8c-1431">checkcard</span></span>
- <span data-ttu-id="32d8c-1432">cartes de vérification</span><span class="sxs-lookup"><span data-stu-id="32d8c-1432">check cards</span></span>
- <span data-ttu-id="32d8c-1433">cartes</span><span class="sxs-lookup"><span data-stu-id="32d8c-1433">checkcards</span></span>
- <span data-ttu-id="32d8c-1434">carte de débit</span><span class="sxs-lookup"><span data-stu-id="32d8c-1434">debit card</span></span>
- <span data-ttu-id="32d8c-1435">débit</span><span class="sxs-lookup"><span data-stu-id="32d8c-1435">debitcard</span></span>
- <span data-ttu-id="32d8c-1436">cartes de débit</span><span class="sxs-lookup"><span data-stu-id="32d8c-1436">debit cards</span></span>
- <span data-ttu-id="32d8c-1437">débit</span><span class="sxs-lookup"><span data-stu-id="32d8c-1437">debitcards</span></span>
- <span data-ttu-id="32d8c-1438">carte de retrait</span><span class="sxs-lookup"><span data-stu-id="32d8c-1438">atm card</span></span>
- <span data-ttu-id="32d8c-1439">retrait</span><span class="sxs-lookup"><span data-stu-id="32d8c-1439">atmcard</span></span>
- <span data-ttu-id="32d8c-1440">cartes de retrait</span><span class="sxs-lookup"><span data-stu-id="32d8c-1440">atm cards</span></span>
- <span data-ttu-id="32d8c-1441">retrait</span><span class="sxs-lookup"><span data-stu-id="32d8c-1441">atmcards</span></span>
- <span data-ttu-id="32d8c-1442">envoier</span><span class="sxs-lookup"><span data-stu-id="32d8c-1442">enroute</span></span>
- <span data-ttu-id="32d8c-1443">en route</span><span class="sxs-lookup"><span data-stu-id="32d8c-1443">en route</span></span>
- <span data-ttu-id="32d8c-1444">type de carte</span><span class="sxs-lookup"><span data-stu-id="32d8c-1444">card type</span></span>
- <span data-ttu-id="32d8c-1445">carte bancaire</span><span class="sxs-lookup"><span data-stu-id="32d8c-1445">carte bancaire</span></span>
- <span data-ttu-id="32d8c-1446">carte de crédit</span><span class="sxs-lookup"><span data-stu-id="32d8c-1446">carte de crédit</span></span>
- <span data-ttu-id="32d8c-1447">carte de credit</span><span class="sxs-lookup"><span data-stu-id="32d8c-1447">carte de credit</span></span>
- <span data-ttu-id="32d8c-1448">numéro de carte</span><span class="sxs-lookup"><span data-stu-id="32d8c-1448">numéro de carte</span></span>
- <span data-ttu-id="32d8c-1449">numero de carte</span><span class="sxs-lookup"><span data-stu-id="32d8c-1449">numero de carte</span></span>
- <span data-ttu-id="32d8c-1450">nº de la carte</span><span class="sxs-lookup"><span data-stu-id="32d8c-1450">nº de la carte</span></span>
- <span data-ttu-id="32d8c-1451">nº de carte</span><span class="sxs-lookup"><span data-stu-id="32d8c-1451">nº de carte</span></span>
- <span data-ttu-id="32d8c-1452">kreditkarte</span><span class="sxs-lookup"><span data-stu-id="32d8c-1452">kreditkarte</span></span>
- <span data-ttu-id="32d8c-1453">karte</span><span class="sxs-lookup"><span data-stu-id="32d8c-1453">karte</span></span>
- <span data-ttu-id="32d8c-1454">karteninhaber</span><span class="sxs-lookup"><span data-stu-id="32d8c-1454">karteninhaber</span></span>
- <span data-ttu-id="32d8c-1455">karteninhabers</span><span class="sxs-lookup"><span data-stu-id="32d8c-1455">karteninhabers</span></span>
- <span data-ttu-id="32d8c-1456">kreditkarteninhaber</span><span class="sxs-lookup"><span data-stu-id="32d8c-1456">kreditkarteninhaber</span></span>
- <span data-ttu-id="32d8c-1457">kreditkarteninstitut</span><span class="sxs-lookup"><span data-stu-id="32d8c-1457">kreditkarteninstitut</span></span>
- <span data-ttu-id="32d8c-1458">kreditkartentyp</span><span class="sxs-lookup"><span data-stu-id="32d8c-1458">kreditkartentyp</span></span>
- <span data-ttu-id="32d8c-1459">eigentümername</span><span class="sxs-lookup"><span data-stu-id="32d8c-1459">eigentümername</span></span>
- <span data-ttu-id="32d8c-1460">kartennr</span><span class="sxs-lookup"><span data-stu-id="32d8c-1460">kartennr</span></span> 
- <span data-ttu-id="32d8c-1461">kartennummer</span><span class="sxs-lookup"><span data-stu-id="32d8c-1461">kartennummer</span></span>
- <span data-ttu-id="32d8c-1462">kreditkartennummer</span><span class="sxs-lookup"><span data-stu-id="32d8c-1462">kreditkartennummer</span></span>
- <span data-ttu-id="32d8c-1463">kreditkarten-nummer</span><span class="sxs-lookup"><span data-stu-id="32d8c-1463">kreditkarten-nummer</span></span>
- <span data-ttu-id="32d8c-1464">Carta di credito</span><span class="sxs-lookup"><span data-stu-id="32d8c-1464">carta di credito</span></span>
- <span data-ttu-id="32d8c-1465">Carta credito</span><span class="sxs-lookup"><span data-stu-id="32d8c-1465">carta credito</span></span>
- <span data-ttu-id="32d8c-1466">Carta</span><span class="sxs-lookup"><span data-stu-id="32d8c-1466">carta</span></span>
- <span data-ttu-id="32d8c-1467">n carta</span><span class="sxs-lookup"><span data-stu-id="32d8c-1467">n carta</span></span>
- <span data-ttu-id="32d8c-1468">Nr.</span><span class="sxs-lookup"><span data-stu-id="32d8c-1468">nr.</span></span> <span data-ttu-id="32d8c-1469">Carta</span><span class="sxs-lookup"><span data-stu-id="32d8c-1469">carta</span></span>
- <span data-ttu-id="32d8c-1470">nr carta</span><span class="sxs-lookup"><span data-stu-id="32d8c-1470">nr carta</span></span>
- <span data-ttu-id="32d8c-1471">numero carta</span><span class="sxs-lookup"><span data-stu-id="32d8c-1471">numero carta</span></span>
- <span data-ttu-id="32d8c-1472">numero della carta</span><span class="sxs-lookup"><span data-stu-id="32d8c-1472">numero della carta</span></span>
- <span data-ttu-id="32d8c-1473">numero di carta</span><span class="sxs-lookup"><span data-stu-id="32d8c-1473">numero di carta</span></span>
- <span data-ttu-id="32d8c-1474">tarjeta credito</span><span class="sxs-lookup"><span data-stu-id="32d8c-1474">tarjeta credito</span></span>
- <span data-ttu-id="32d8c-1475">tarjeta de credito</span><span class="sxs-lookup"><span data-stu-id="32d8c-1475">tarjeta de credito</span></span>
- <span data-ttu-id="32d8c-1476">tarjeta crédito</span><span class="sxs-lookup"><span data-stu-id="32d8c-1476">tarjeta crédito</span></span>
- <span data-ttu-id="32d8c-1477">tarjeta de crédito</span><span class="sxs-lookup"><span data-stu-id="32d8c-1477">tarjeta de crédito</span></span>
- <span data-ttu-id="32d8c-1478">tarjeta de atm</span><span class="sxs-lookup"><span data-stu-id="32d8c-1478">tarjeta de atm</span></span>
- <span data-ttu-id="32d8c-1479">tarjeta atm</span><span class="sxs-lookup"><span data-stu-id="32d8c-1479">tarjeta atm</span></span>
- <span data-ttu-id="32d8c-1480">tarjeta debito</span><span class="sxs-lookup"><span data-stu-id="32d8c-1480">tarjeta debito</span></span>
- <span data-ttu-id="32d8c-1481">tarjeta de debito</span><span class="sxs-lookup"><span data-stu-id="32d8c-1481">tarjeta de debito</span></span>
- <span data-ttu-id="32d8c-1482">tarjeta débito</span><span class="sxs-lookup"><span data-stu-id="32d8c-1482">tarjeta débito</span></span>
- <span data-ttu-id="32d8c-1483">tarjeta de débito</span><span class="sxs-lookup"><span data-stu-id="32d8c-1483">tarjeta de débito</span></span>
- <span data-ttu-id="32d8c-1484">nº de tarjeta</span><span class="sxs-lookup"><span data-stu-id="32d8c-1484">nº de tarjeta</span></span>
- <span data-ttu-id="32d8c-1485">Nbre.</span><span class="sxs-lookup"><span data-stu-id="32d8c-1485">no.</span></span> <span data-ttu-id="32d8c-1486">de tarjeta</span><span class="sxs-lookup"><span data-stu-id="32d8c-1486">de tarjeta</span></span>
- <span data-ttu-id="32d8c-1487">no de tarjeta</span><span class="sxs-lookup"><span data-stu-id="32d8c-1487">no de tarjeta</span></span>
- <span data-ttu-id="32d8c-1488">numero de tarjeta</span><span class="sxs-lookup"><span data-stu-id="32d8c-1488">numero de tarjeta</span></span>
- <span data-ttu-id="32d8c-1489">número de tarjeta</span><span class="sxs-lookup"><span data-stu-id="32d8c-1489">número de tarjeta</span></span>
- <span data-ttu-id="32d8c-1490">tarjeta no</span><span class="sxs-lookup"><span data-stu-id="32d8c-1490">tarjeta no</span></span>
- <span data-ttu-id="32d8c-1491">tarjetahabiente</span><span class="sxs-lookup"><span data-stu-id="32d8c-1491">tarjetahabiente</span></span>
- <span data-ttu-id="32d8c-1492">cartão de crédito</span><span class="sxs-lookup"><span data-stu-id="32d8c-1492">cartão de crédito</span></span>
- <span data-ttu-id="32d8c-1493">cartão de credito</span><span class="sxs-lookup"><span data-stu-id="32d8c-1493">cartão de credito</span></span>
- <span data-ttu-id="32d8c-1494">cartao de crédito</span><span class="sxs-lookup"><span data-stu-id="32d8c-1494">cartao de crédito</span></span>
- <span data-ttu-id="32d8c-1495">cartao de credito</span><span class="sxs-lookup"><span data-stu-id="32d8c-1495">cartao de credito</span></span>
- <span data-ttu-id="32d8c-1496">cartão de débito</span><span class="sxs-lookup"><span data-stu-id="32d8c-1496">cartão de débito</span></span>
- <span data-ttu-id="32d8c-1497">cartao de débito</span><span class="sxs-lookup"><span data-stu-id="32d8c-1497">cartao de débito</span></span>
- <span data-ttu-id="32d8c-1498">cartão de debito</span><span class="sxs-lookup"><span data-stu-id="32d8c-1498">cartão de debito</span></span>
- <span data-ttu-id="32d8c-1499">cartao de debito</span><span class="sxs-lookup"><span data-stu-id="32d8c-1499">cartao de debito</span></span>
- <span data-ttu-id="32d8c-1500">débito automático</span><span class="sxs-lookup"><span data-stu-id="32d8c-1500">débito automático</span></span>
- <span data-ttu-id="32d8c-1501">debito automatico</span><span class="sxs-lookup"><span data-stu-id="32d8c-1501">debito automatico</span></span>
- <span data-ttu-id="32d8c-1502">número do cartão</span><span class="sxs-lookup"><span data-stu-id="32d8c-1502">número do cartão</span></span>
- <span data-ttu-id="32d8c-1503">numero do cartão</span><span class="sxs-lookup"><span data-stu-id="32d8c-1503">numero do cartão</span></span> 
- <span data-ttu-id="32d8c-1504">número do cartao</span><span class="sxs-lookup"><span data-stu-id="32d8c-1504">número do cartao</span></span>
- <span data-ttu-id="32d8c-1505">numero do cartao</span><span class="sxs-lookup"><span data-stu-id="32d8c-1505">numero do cartao</span></span>
- <span data-ttu-id="32d8c-1506">número de cartão</span><span class="sxs-lookup"><span data-stu-id="32d8c-1506">número de cartão</span></span>
- <span data-ttu-id="32d8c-1507">numero de cartão</span><span class="sxs-lookup"><span data-stu-id="32d8c-1507">numero de cartão</span></span>
- <span data-ttu-id="32d8c-1508">número de cartao</span><span class="sxs-lookup"><span data-stu-id="32d8c-1508">número de cartao</span></span>
- <span data-ttu-id="32d8c-1509">numero de cartao</span><span class="sxs-lookup"><span data-stu-id="32d8c-1509">numero de cartao</span></span>
- <span data-ttu-id="32d8c-1510">nº do cartão</span><span class="sxs-lookup"><span data-stu-id="32d8c-1510">nº do cartão</span></span>
- <span data-ttu-id="32d8c-1511">nº do cartao</span><span class="sxs-lookup"><span data-stu-id="32d8c-1511">nº do cartao</span></span>
- <span data-ttu-id="32d8c-1512">n º.</span><span class="sxs-lookup"><span data-stu-id="32d8c-1512">nº.</span></span> <span data-ttu-id="32d8c-1513">do cartão</span><span class="sxs-lookup"><span data-stu-id="32d8c-1513">do cartão</span></span>
- <span data-ttu-id="32d8c-1514">no do cartão</span><span class="sxs-lookup"><span data-stu-id="32d8c-1514">no do cartão</span></span>
- <span data-ttu-id="32d8c-1515">no do cartao</span><span class="sxs-lookup"><span data-stu-id="32d8c-1515">no do cartao</span></span>
- <span data-ttu-id="32d8c-1516">Nbre.</span><span class="sxs-lookup"><span data-stu-id="32d8c-1516">no.</span></span> <span data-ttu-id="32d8c-1517">do cartão</span><span class="sxs-lookup"><span data-stu-id="32d8c-1517">do cartão</span></span>
- <span data-ttu-id="32d8c-1518">Nbre.</span><span class="sxs-lookup"><span data-stu-id="32d8c-1518">no.</span></span> <span data-ttu-id="32d8c-1519">do cartao</span><span class="sxs-lookup"><span data-stu-id="32d8c-1519">do cartao</span></span> 
   
## <a name="croatia-identity-card-number"></a><span data-ttu-id="32d8c-1520">	Numéro de carte d’identité Croatie</span><span class="sxs-lookup"><span data-stu-id="32d8c-1520">Croatia Identity Card Number</span></span>

### <a name="format"></a><span data-ttu-id="32d8c-1521">Format</span><span class="sxs-lookup"><span data-stu-id="32d8c-1521">Format</span></span>

<span data-ttu-id="32d8c-1522">Neuf chiffres</span><span class="sxs-lookup"><span data-stu-id="32d8c-1522">Nine digits</span></span>

### <a name="pattern"></a><span data-ttu-id="32d8c-1523">Modèle</span><span class="sxs-lookup"><span data-stu-id="32d8c-1523">Pattern</span></span>

<span data-ttu-id="32d8c-1524">Neuf chiffres consécutifs</span><span class="sxs-lookup"><span data-stu-id="32d8c-1524">Nine consecutive digits</span></span>

### <a name="checksum"></a><span data-ttu-id="32d8c-1525">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="32d8c-1525">Checksum</span></span>

<span data-ttu-id="32d8c-1526">Non</span><span class="sxs-lookup"><span data-stu-id="32d8c-1526">No</span></span>

### <a name="definition"></a><span data-ttu-id="32d8c-1527">Définition</span><span class="sxs-lookup"><span data-stu-id="32d8c-1527">Definition</span></span>

<span data-ttu-id="32d8c-1528">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="32d8c-1528">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="32d8c-1529">La fonction Func_croatia_id_card trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="32d8c-1529">The function Func_croatia_id_card finds content that matches the pattern.</span></span>
- <span data-ttu-id="32d8c-1530">Un mot clé figurant dans la liste Keyword_croatia_id_card est trouvé.</span><span class="sxs-lookup"><span data-stu-id="32d8c-1530">A keyword from Keyword_croatia_id_card is found.</span></span>

```xml
<!--Croatia Identity Card Number-->
<Entity id="ff12f884-c20a-4189-b185-34c8e7258d47" recommendedConfidence="75" patternsProximity="300">
  <Pattern confidenceLevel="75">
     <IdMatch idRef="Func_croatia_id_card"/>
     <Match idRef="Keyword_croatia_id_card"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="32d8c-1531">Mots clés</span><span class="sxs-lookup"><span data-stu-id="32d8c-1531">Keywords</span></span>

#### <a name="keyword_croatia_id_card"></a><span data-ttu-id="32d8c-1532">Keyword_croatia_id_card</span><span class="sxs-lookup"><span data-stu-id="32d8c-1532">Keyword_croatia_id_card</span></span>

- <span data-ttu-id="32d8c-1533">Croatian identity card</span><span class="sxs-lookup"><span data-stu-id="32d8c-1533">Croatian identity card</span></span>
- <span data-ttu-id="32d8c-1534">Osobna iskaznica</span><span class="sxs-lookup"><span data-stu-id="32d8c-1534">Osobna iskaznica</span></span>

   
## <a name="croatia-personal-identification-oib-number"></a><span data-ttu-id="32d8c-1535">	Numéro d’identification personnel (OIB) Croatie</span><span class="sxs-lookup"><span data-stu-id="32d8c-1535">Croatia Personal Identification (OIB) Number</span></span>

### <a name="format"></a><span data-ttu-id="32d8c-1536">Format</span><span class="sxs-lookup"><span data-stu-id="32d8c-1536">Format</span></span>

<span data-ttu-id="32d8c-1537">11 chiffres</span><span class="sxs-lookup"><span data-stu-id="32d8c-1537">11 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="32d8c-1538">Modèle</span><span class="sxs-lookup"><span data-stu-id="32d8c-1538">Pattern</span></span>

<span data-ttu-id="32d8c-1539">11 chiffres :</span><span class="sxs-lookup"><span data-stu-id="32d8c-1539">11 digits:</span></span>
- <span data-ttu-id="32d8c-1540">10 chiffres</span><span class="sxs-lookup"><span data-stu-id="32d8c-1540">10 digits</span></span> 
- <span data-ttu-id="32d8c-1541">Le chiffre final est un chiffre de contrôle aux fins de l’échange de données internationales, les lettres HR sont ajoutées avant les onze chiffres.</span><span class="sxs-lookup"><span data-stu-id="32d8c-1541">Final digit is a check digit For the purposes of international data exchange, the letters HR are added preceding the eleven digits.</span></span>

### <a name="checksum"></a><span data-ttu-id="32d8c-1542">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="32d8c-1542">Checksum</span></span>

<span data-ttu-id="32d8c-1543">Oui</span><span class="sxs-lookup"><span data-stu-id="32d8c-1543">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="32d8c-1544">Définition</span><span class="sxs-lookup"><span data-stu-id="32d8c-1544">Definition</span></span>

<span data-ttu-id="32d8c-1545">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="32d8c-1545">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="32d8c-1546">La fonction Func_croatia_oib_number trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="32d8c-1546">The function Func_croatia_oib_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="32d8c-1547">Un mot clé figurant dans la liste Keyword_croatia_oib_number est trouvé.</span><span class="sxs-lookup"><span data-stu-id="32d8c-1547">A keyword from Keyword_croatia_oib_number is found.</span></span>
- <span data-ttu-id="32d8c-1548">La somme de contrôle est correcte.</span><span class="sxs-lookup"><span data-stu-id="32d8c-1548">The checksum passes.</span></span>

<span data-ttu-id="32d8c-1549">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="32d8c-1549">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="32d8c-1550">La fonction Func_croatia_oib_number trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="32d8c-1550">The function Func_croatia_oib_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="32d8c-1551">La somme de contrôle est correcte.</span><span class="sxs-lookup"><span data-stu-id="32d8c-1551">The checksum passes.</span></span>

```xml
<!-- Croatia Personal Identification (OIB) Number -->
<Entity id="31983b6d-db95-4eb2-a630-b44bd091968d" recommendedConfidence="85" patternsProximity="300">
  <Pattern confidenceLevel="85">
     <IdMatch idRef="Func_croatia_oib_number"/>
     <Match idRef="Keyword_croatia_oib_number"/>
  </Pattern>
  <Pattern confidenceLevel="75">
     <IdMatch idRef="Func_croatia_oib_number"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="32d8c-1552">Mots clés</span><span class="sxs-lookup"><span data-stu-id="32d8c-1552">Keywords</span></span>

#### <a name="keyword_croatia_oib_number"></a><span data-ttu-id="32d8c-1553">Keyword_croatia_oib_number</span><span class="sxs-lookup"><span data-stu-id="32d8c-1553">Keyword_croatia_oib_number</span></span>

- <span data-ttu-id="32d8c-1554">Personal Identification Number</span><span class="sxs-lookup"><span data-stu-id="32d8c-1554">Personal Identification Number</span></span>
- <span data-ttu-id="32d8c-1555">Osobni identifikacijski broj</span><span class="sxs-lookup"><span data-stu-id="32d8c-1555">Osobni identifikacijski broj</span></span> 
- <span data-ttu-id="32d8c-1556">OIB</span><span class="sxs-lookup"><span data-stu-id="32d8c-1556">OIB</span></span> 

   
## <a name="czech-personal-identity-number"></a><span data-ttu-id="32d8c-1557">Numéro d’identité personnelle tchèque</span><span class="sxs-lookup"><span data-stu-id="32d8c-1557">Czech Personal Identity Number</span></span>

### <a name="format"></a><span data-ttu-id="32d8c-1558">Format</span><span class="sxs-lookup"><span data-stu-id="32d8c-1558">Format</span></span>

<span data-ttu-id="32d8c-1559">Neuf chiffres avec une barre oblique inverse facultative (ancien format) 10 chiffres avec une barre oblique facultative (nouveau format)</span><span class="sxs-lookup"><span data-stu-id="32d8c-1559">Nine digits with optional forward slash (old format) 10 digits with optional forward slash (new format)</span></span>

### <a name="pattern"></a><span data-ttu-id="32d8c-1560">Modèle</span><span class="sxs-lookup"><span data-stu-id="32d8c-1560">Pattern</span></span>

<span data-ttu-id="32d8c-1561">Neuf chiffres (ancien format) :</span><span class="sxs-lookup"><span data-stu-id="32d8c-1561">Nine digits (old format):</span></span>
- <span data-ttu-id="32d8c-1562">Neuf chiffres</span><span class="sxs-lookup"><span data-stu-id="32d8c-1562">Nine digits</span></span>

<span data-ttu-id="32d8c-1563">OR</span><span class="sxs-lookup"><span data-stu-id="32d8c-1563">OR</span></span>

- <span data-ttu-id="32d8c-1564">Six chiffres qui représentent la date de naissance</span><span class="sxs-lookup"><span data-stu-id="32d8c-1564">Six digits that represent date of birth</span></span>
- <span data-ttu-id="32d8c-1565">Une barre oblique </span><span class="sxs-lookup"><span data-stu-id="32d8c-1565">A forward slash</span></span>
- <span data-ttu-id="32d8c-1566">Trois chiffres</span><span class="sxs-lookup"><span data-stu-id="32d8c-1566">Three digits</span></span>

<span data-ttu-id="32d8c-1567">10 chiffres (nouveau format) :</span><span class="sxs-lookup"><span data-stu-id="32d8c-1567">10 digits (new format):</span></span>
- <span data-ttu-id="32d8c-1568">10 chiffres</span><span class="sxs-lookup"><span data-stu-id="32d8c-1568">10 digits</span></span>

<span data-ttu-id="32d8c-1569">OR</span><span class="sxs-lookup"><span data-stu-id="32d8c-1569">OR</span></span>

- <span data-ttu-id="32d8c-1570">Six chiffres qui représentent la date de naissance</span><span class="sxs-lookup"><span data-stu-id="32d8c-1570">Six digits that represent date of birth</span></span>
- <span data-ttu-id="32d8c-1571">Une barre oblique </span><span class="sxs-lookup"><span data-stu-id="32d8c-1571">A forward slash</span></span> 
- <span data-ttu-id="32d8c-1572">Quatre chiffres où le dernier chiffre est un chiffre de contrôle</span><span class="sxs-lookup"><span data-stu-id="32d8c-1572">Four digits where last digit is a check digit</span></span>

### <a name="checksum"></a><span data-ttu-id="32d8c-1573">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="32d8c-1573">Checksum</span></span>

<span data-ttu-id="32d8c-1574">Oui</span><span class="sxs-lookup"><span data-stu-id="32d8c-1574">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="32d8c-1575">Définition</span><span class="sxs-lookup"><span data-stu-id="32d8c-1575">Definition</span></span>

<span data-ttu-id="32d8c-1576">Une stratégie DLP est sûre à 85% d’avoir détecté ce type d’informations sensibles si, dans une proximité de 300 caractères : la fonction Func_czech_id_card trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="32d8c-1576">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters: The function Func_czech_id_card finds content that matches the pattern.</span></span>
<span data-ttu-id="32d8c-1577">Un mot clé figurant dans la liste Keyword_czech_id_card est trouvé.</span><span class="sxs-lookup"><span data-stu-id="32d8c-1577">A keyword from Keyword_czech_id_card is found.</span></span>
<span data-ttu-id="32d8c-1578">La somme de contrôle est correcte.</span><span class="sxs-lookup"><span data-stu-id="32d8c-1578">The checksum passes.</span></span>

```xml
<!-- Czech Personal Identity Number -->
<Entity id="60c0725a-4eb6-455b-9dda-05d8a7396497"      patternsProximity="300" recommendedConfidence="85">
   <Pattern confidenceLevel="85">
      <IdMatch idRef="Func_czech_id_card" />
      <Match idRef="Keyword_czech_id_card" />
   </Pattern>
</Entity>
```
### <a name="keywords"></a><span data-ttu-id="32d8c-1579">Mots clés</span><span class="sxs-lookup"><span data-stu-id="32d8c-1579">Keywords</span></span>

- <span data-ttu-id="32d8c-1580">Numéro d’identité personnelle tchèque</span><span class="sxs-lookup"><span data-stu-id="32d8c-1580">czech personal identity number</span></span>
- <span data-ttu-id="32d8c-1581">Rodné číslo</span><span class="sxs-lookup"><span data-stu-id="32d8c-1581">Rodné číslo</span></span>
   
## <a name="denmark-personal-identification-number"></a><span data-ttu-id="32d8c-1582">	Numéro d’identification personnel Danemark</span><span class="sxs-lookup"><span data-stu-id="32d8c-1582">Denmark Personal Identification Number</span></span>

### <a name="format"></a><span data-ttu-id="32d8c-1583">Format</span><span class="sxs-lookup"><span data-stu-id="32d8c-1583">Format</span></span>

<span data-ttu-id="32d8c-1584">10 chiffres contenant un trait d’union</span><span class="sxs-lookup"><span data-stu-id="32d8c-1584">10 digits containing a hyphen</span></span>

### <a name="pattern"></a><span data-ttu-id="32d8c-1585">Modèle</span><span class="sxs-lookup"><span data-stu-id="32d8c-1585">Pattern</span></span>

<span data-ttu-id="32d8c-1586">10 chiffres :</span><span class="sxs-lookup"><span data-stu-id="32d8c-1586">10 digits:</span></span>
- <span data-ttu-id="32d8c-1587">Six chiffres au format JJMMAA qui correspondent à la date de naissance </span><span class="sxs-lookup"><span data-stu-id="32d8c-1587">Six digits in the format DDMMYY which are the date of birth</span></span> 
- <span data-ttu-id="32d8c-1588">Un trait d’union </span><span class="sxs-lookup"><span data-stu-id="32d8c-1588">A hyphen</span></span> 
- <span data-ttu-id="32d8c-1589">Quatre chiffres où le dernier chiffre est un chiffre de contrôle</span><span class="sxs-lookup"><span data-stu-id="32d8c-1589">Four digits where the final digit is a check digit</span></span>

### <a name="checksum"></a><span data-ttu-id="32d8c-1590">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="32d8c-1590">Checksum</span></span>

<span data-ttu-id="32d8c-1591">Oui</span><span class="sxs-lookup"><span data-stu-id="32d8c-1591">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="32d8c-1592">Définition</span><span class="sxs-lookup"><span data-stu-id="32d8c-1592">Definition</span></span>

<span data-ttu-id="32d8c-1593">Une stratégie DLP est sûre à 75% d’avoir détecté ce type d’informations sensibles si, dans une proximité de 300 caractères : l’expression régulière Regex_denmark_id trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="32d8c-1593">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters: The regular expression Regex_denmark_id finds content that matches the pattern.</span></span>
<span data-ttu-id="32d8c-1594">Un mot clé figurant dans la liste Keyword_denmark_id est trouvé.</span><span class="sxs-lookup"><span data-stu-id="32d8c-1594">A keyword from Keyword_denmark_id is found.</span></span>
<span data-ttu-id="32d8c-1595">La somme de contrôle est correcte.</span><span class="sxs-lookup"><span data-stu-id="32d8c-1595">The checksum passes.</span></span>

```xml
<!-- Denmark Personal Identification Number -->
<Entity id="6c4f2fef-56e1-4c00-8093-88d7a01cf460" recommendedConfidence="75" patternsProximity="300">
  <Pattern confidenceLevel="75">
     <IdMatch idRef="Regex_denmark_id"/>
     <Match idRef="Keyword_denmark_id"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="32d8c-1596">Mots clés</span><span class="sxs-lookup"><span data-stu-id="32d8c-1596">Keywords</span></span>

#### <a name="keyword_denmark_id"></a><span data-ttu-id="32d8c-1597">Keyword_denmark_id</span><span class="sxs-lookup"><span data-stu-id="32d8c-1597">Keyword_denmark_id</span></span>

- <span data-ttu-id="32d8c-1598">Personal Identification Number</span><span class="sxs-lookup"><span data-stu-id="32d8c-1598">Personal Identification Number</span></span>
- <span data-ttu-id="32d8c-1599">CARDIO</span><span class="sxs-lookup"><span data-stu-id="32d8c-1599">CPR</span></span>
- <span data-ttu-id="32d8c-1600">Det Centrale Personregister</span><span class="sxs-lookup"><span data-stu-id="32d8c-1600">Det Centrale Personregister</span></span>
- <span data-ttu-id="32d8c-1601">Personnummer</span><span class="sxs-lookup"><span data-stu-id="32d8c-1601">Personnummer</span></span>
   
## <a name="drug-enforcement-agency-dea-number"></a><span data-ttu-id="32d8c-1602">Numéro de la Drug Enforcement Agency (DEA)</span><span class="sxs-lookup"><span data-stu-id="32d8c-1602">Drug Enforcement Agency (DEA) Number</span></span>

### <a name="format"></a><span data-ttu-id="32d8c-1603">Format</span><span class="sxs-lookup"><span data-stu-id="32d8c-1603">Format</span></span>

<span data-ttu-id="32d8c-1604">Deux lettres suivies de sept chiffres</span><span class="sxs-lookup"><span data-stu-id="32d8c-1604">Two letters followed by seven digits</span></span>

### <a name="pattern"></a><span data-ttu-id="32d8c-1605">Modèle</span><span class="sxs-lookup"><span data-stu-id="32d8c-1605">Pattern</span></span>

<span data-ttu-id="32d8c-1606">Le modèle doit inclure tous les éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="32d8c-1606">Pattern must include all of the following:</span></span>
- <span data-ttu-id="32d8c-1607">Une lettre (ne respecte pas la casse) à partir de cet ensemble de lettres possibles : abcdefghjklmnprstux, qui est un code d’utilisateur enregistré</span><span class="sxs-lookup"><span data-stu-id="32d8c-1607">One letter (not case sensitive) from this set of possible letters: abcdefghjklmnprstux, which is a registrant code</span></span> 
- <span data-ttu-id="32d8c-1608">Une lettre (ne respecte pas la casse), qui est la première lettre du nom de l’utilisateur enregistré</span><span class="sxs-lookup"><span data-stu-id="32d8c-1608">One letter (not case sensitive), which is the first letter of the registrant's last name</span></span> 
- <span data-ttu-id="32d8c-1609">Sept chiffres, le dernier est le chiffre de contrôle</span><span class="sxs-lookup"><span data-stu-id="32d8c-1609">Seven digits, the last of which is the check digit</span></span>

### <a name="checksum"></a><span data-ttu-id="32d8c-1610">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="32d8c-1610">Checksum</span></span>

<span data-ttu-id="32d8c-1611">Oui</span><span class="sxs-lookup"><span data-stu-id="32d8c-1611">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="32d8c-1612">Définition</span><span class="sxs-lookup"><span data-stu-id="32d8c-1612">Definition</span></span>

<span data-ttu-id="32d8c-1613">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="32d8c-1613">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="32d8c-1614">La fonction Func_dea_number trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="32d8c-1614">The function Func_dea_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="32d8c-1615">La somme de contrôle est correcte.</span><span class="sxs-lookup"><span data-stu-id="32d8c-1615">The checksum passes.</span></span>

```xml
<!-- DEA Number -->
<Entity id="9a5445ad-406e-43eb-8bd7-cac17ab6d0e4" recommendedConfidence="85" patternsProximity="300">
  <Pattern confidenceLevel="85">
     <IdMatch idRef="Func_dea_number"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="32d8c-1616">Mots clés</span><span class="sxs-lookup"><span data-stu-id="32d8c-1616">Keywords</span></span>

<span data-ttu-id="32d8c-1617">Aucun</span><span class="sxs-lookup"><span data-stu-id="32d8c-1617">None</span></span>

   
## <a name="eu-debit-card-number"></a><span data-ttu-id="32d8c-1618">Numéro de carte de débit Union européenne</span><span class="sxs-lookup"><span data-stu-id="32d8c-1618">EU Debit Card Number</span></span>

### <a name="format"></a><span data-ttu-id="32d8c-1619">Format</span><span class="sxs-lookup"><span data-stu-id="32d8c-1619">Format</span></span>

<span data-ttu-id="32d8c-1620">16 chiffres</span><span class="sxs-lookup"><span data-stu-id="32d8c-1620">16 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="32d8c-1621">Modèle</span><span class="sxs-lookup"><span data-stu-id="32d8c-1621">Pattern</span></span>

<span data-ttu-id="32d8c-1622">Modèle très complexe et puissant</span><span class="sxs-lookup"><span data-stu-id="32d8c-1622">Very complex and robust pattern</span></span>

### <a name="checksum"></a><span data-ttu-id="32d8c-1623">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="32d8c-1623">Checksum</span></span>

<span data-ttu-id="32d8c-1624">Oui</span><span class="sxs-lookup"><span data-stu-id="32d8c-1624">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="32d8c-1625">Définition</span><span class="sxs-lookup"><span data-stu-id="32d8c-1625">Definition</span></span>

<span data-ttu-id="32d8c-1626">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="32d8c-1626">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="32d8c-1627">La fonction Func_eu_debit_card trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="32d8c-1627">The function Func_eu_debit_card finds content that matches the pattern.</span></span>
- <span data-ttu-id="32d8c-1628">Au moins une des affirmations suivantes est vraie :</span><span class="sxs-lookup"><span data-stu-id="32d8c-1628">At least one of the following is true:</span></span>
    - <span data-ttu-id="32d8c-1629">Un mot clé figurant dans la liste Keyword_eu_debit_card est trouvé.</span><span class="sxs-lookup"><span data-stu-id="32d8c-1629">A keyword from Keyword_eu_debit_card is found.</span></span>
    - <span data-ttu-id="32d8c-1630">Un mot clé figurant dans la liste Keyword_card_terms_dict est trouvé.</span><span class="sxs-lookup"><span data-stu-id="32d8c-1630">A keyword from Keyword_card_terms_dict is found.</span></span>
    - <span data-ttu-id="32d8c-1631">Un mot clé figurant dans la liste Keyword_card_security_terms_dict est trouvé.</span><span class="sxs-lookup"><span data-stu-id="32d8c-1631">A keyword from Keyword_card_security_terms_dict is found.</span></span>
    - <span data-ttu-id="32d8c-1632">Un mot clé figurant dans la liste Keyword_card_expiration_terms_dict est trouvé.</span><span class="sxs-lookup"><span data-stu-id="32d8c-1632">A keyword from Keyword_card_expiration_terms_dict is found.</span></span>
    - <span data-ttu-id="32d8c-1633">La fonction Func_expiration_date trouve une date au format correct.</span><span class="sxs-lookup"><span data-stu-id="32d8c-1633">The function Func_expiration_date finds a date in the right date format.</span></span>
- <span data-ttu-id="32d8c-1634">La somme de contrôle est correcte.</span><span class="sxs-lookup"><span data-stu-id="32d8c-1634">The checksum passes.</span></span>

```xml
    <!-- EU Debit Card Number -->
    <Entity id="0e9b3178-9678-47dd-a509-37222ca96b42" patternsProximity="300" recommendedConfidence="85">
      <Pattern confidenceLevel="85">
        <IdMatch idRef="Func_eu_debit_card" />
        <Any minMatches="1">
          <Match idRef="Keyword_eu_debit_card" />
          <Match idRef="Keyword_card_terms_dict" />
          <Match idRef="Keyword_card_security_terms_dict" />
          <Match idRef="Keyword_card_expiration_terms_dict" />
          <Match idRef="Func_expiration_date" />
        </Any>
      </Pattern>
    </Entity>
```

### <a name="keywords"></a><span data-ttu-id="32d8c-1635">Mots clés</span><span class="sxs-lookup"><span data-stu-id="32d8c-1635">Keywords</span></span>

#### <a name="keyword_eu_debit_card"></a><span data-ttu-id="32d8c-1636">Keyword_eu_debit_card</span><span class="sxs-lookup"><span data-stu-id="32d8c-1636">Keyword_eu_debit_card</span></span>

- <span data-ttu-id="32d8c-1637">numéro de compte</span><span class="sxs-lookup"><span data-stu-id="32d8c-1637">account number</span></span> 
- <span data-ttu-id="32d8c-1638">numéro de carte</span><span class="sxs-lookup"><span data-stu-id="32d8c-1638">card number</span></span> 
- <span data-ttu-id="32d8c-1639">n° carte</span><span class="sxs-lookup"><span data-stu-id="32d8c-1639">card no.</span></span> 
- <span data-ttu-id="32d8c-1640">numéro de sécurité</span><span class="sxs-lookup"><span data-stu-id="32d8c-1640">security number</span></span> 
- <span data-ttu-id="32d8c-1641">CC #</span><span class="sxs-lookup"><span data-stu-id="32d8c-1641">cc#</span></span> 

#### <a name="keyword_card_terms_dict"></a><span data-ttu-id="32d8c-1642">Keyword_card_terms_dict</span><span class="sxs-lookup"><span data-stu-id="32d8c-1642">Keyword_card_terms_dict</span></span>

- <span data-ttu-id="32d8c-1643">num de compte</span><span class="sxs-lookup"><span data-stu-id="32d8c-1643">acct nbr</span></span> 
- <span data-ttu-id="32d8c-1644">num de compte</span><span class="sxs-lookup"><span data-stu-id="32d8c-1644">acct num</span></span> 
- <span data-ttu-id="32d8c-1645">n° compte</span><span class="sxs-lookup"><span data-stu-id="32d8c-1645">acct no</span></span> 
- <span data-ttu-id="32d8c-1646">american express</span><span class="sxs-lookup"><span data-stu-id="32d8c-1646">american express</span></span> 
- <span data-ttu-id="32d8c-1647">americanexpress</span><span class="sxs-lookup"><span data-stu-id="32d8c-1647">americanexpress</span></span> 
- <span data-ttu-id="32d8c-1648">americano espresso</span><span class="sxs-lookup"><span data-stu-id="32d8c-1648">americano espresso</span></span> 
- <span data-ttu-id="32d8c-1649">American</span><span class="sxs-lookup"><span data-stu-id="32d8c-1649">amex</span></span> 
- <span data-ttu-id="32d8c-1650">carte de retrait</span><span class="sxs-lookup"><span data-stu-id="32d8c-1650">atm card</span></span> 
- <span data-ttu-id="32d8c-1651">cartes de retrait</span><span class="sxs-lookup"><span data-stu-id="32d8c-1651">atm cards</span></span> 
- <span data-ttu-id="32d8c-1652">atm kaart</span><span class="sxs-lookup"><span data-stu-id="32d8c-1652">atm kaart</span></span> 
- <span data-ttu-id="32d8c-1653">retrait</span><span class="sxs-lookup"><span data-stu-id="32d8c-1653">atmcard</span></span> 
- <span data-ttu-id="32d8c-1654">retrait</span><span class="sxs-lookup"><span data-stu-id="32d8c-1654">atmcards</span></span> 
- <span data-ttu-id="32d8c-1655">atmkaart</span><span class="sxs-lookup"><span data-stu-id="32d8c-1655">atmkaart</span></span> 
- <span data-ttu-id="32d8c-1656">atmkaarten</span><span class="sxs-lookup"><span data-stu-id="32d8c-1656">atmkaarten</span></span> 
- <span data-ttu-id="32d8c-1657">bancontact</span><span class="sxs-lookup"><span data-stu-id="32d8c-1657">bancontact</span></span> 
- <span data-ttu-id="32d8c-1658">carte bancaire</span><span class="sxs-lookup"><span data-stu-id="32d8c-1658">bank card</span></span> 
- <span data-ttu-id="32d8c-1659">bankkaart</span><span class="sxs-lookup"><span data-stu-id="32d8c-1659">bankkaart</span></span> 
- <span data-ttu-id="32d8c-1660">titulaire de la carte</span><span class="sxs-lookup"><span data-stu-id="32d8c-1660">card holder</span></span> 
- <span data-ttu-id="32d8c-1661">titulaires de la carte</span><span class="sxs-lookup"><span data-stu-id="32d8c-1661">card holders</span></span> 
- <span data-ttu-id="32d8c-1662">num de carte</span><span class="sxs-lookup"><span data-stu-id="32d8c-1662">card num</span></span> 
- <span data-ttu-id="32d8c-1663">numéro de carte</span><span class="sxs-lookup"><span data-stu-id="32d8c-1663">card number</span></span> 
- <span data-ttu-id="32d8c-1664">numéros de carte</span><span class="sxs-lookup"><span data-stu-id="32d8c-1664">card numbers</span></span> 
- <span data-ttu-id="32d8c-1665">type de carte</span><span class="sxs-lookup"><span data-stu-id="32d8c-1665">card type</span></span> 
- <span data-ttu-id="32d8c-1666">cardano numerico</span><span class="sxs-lookup"><span data-stu-id="32d8c-1666">cardano numerico</span></span> 
- <span data-ttu-id="32d8c-1667">titulaires</span><span class="sxs-lookup"><span data-stu-id="32d8c-1667">cardholder</span></span> 
- <span data-ttu-id="32d8c-1668">titulaires</span><span class="sxs-lookup"><span data-stu-id="32d8c-1668">cardholders</span></span> 
- <span data-ttu-id="32d8c-1669">carte</span><span class="sxs-lookup"><span data-stu-id="32d8c-1669">cardnumber</span></span> 
- <span data-ttu-id="32d8c-1670">carte</span><span class="sxs-lookup"><span data-stu-id="32d8c-1670">cardnumbers</span></span> 
- <span data-ttu-id="32d8c-1671">carta bianca</span><span class="sxs-lookup"><span data-stu-id="32d8c-1671">carta bianca</span></span> 
- <span data-ttu-id="32d8c-1672">Carta credito</span><span class="sxs-lookup"><span data-stu-id="32d8c-1672">carta credito</span></span> 
- <span data-ttu-id="32d8c-1673">Carta di credito</span><span class="sxs-lookup"><span data-stu-id="32d8c-1673">carta di credito</span></span> 
- <span data-ttu-id="32d8c-1674">cartao de credito</span><span class="sxs-lookup"><span data-stu-id="32d8c-1674">cartao de credito</span></span> 
- <span data-ttu-id="32d8c-1675">cartao de crédito</span><span class="sxs-lookup"><span data-stu-id="32d8c-1675">cartao de crédito</span></span> 
- <span data-ttu-id="32d8c-1676">cartao de debito</span><span class="sxs-lookup"><span data-stu-id="32d8c-1676">cartao de debito</span></span> 
- <span data-ttu-id="32d8c-1677">cartao de débito</span><span class="sxs-lookup"><span data-stu-id="32d8c-1677">cartao de débito</span></span> 
- <span data-ttu-id="32d8c-1678">carte bancaire</span><span class="sxs-lookup"><span data-stu-id="32d8c-1678">carte bancaire</span></span> 
- <span data-ttu-id="32d8c-1679">carte blanche</span><span class="sxs-lookup"><span data-stu-id="32d8c-1679">carte blanche</span></span> 
- <span data-ttu-id="32d8c-1680">carte bleue</span><span class="sxs-lookup"><span data-stu-id="32d8c-1680">carte bleue</span></span> 
- <span data-ttu-id="32d8c-1681">carte de credit</span><span class="sxs-lookup"><span data-stu-id="32d8c-1681">carte de credit</span></span> 
- <span data-ttu-id="32d8c-1682">carte de crédit</span><span class="sxs-lookup"><span data-stu-id="32d8c-1682">carte de crédit</span></span> 
- <span data-ttu-id="32d8c-1683">carte di credito</span><span class="sxs-lookup"><span data-stu-id="32d8c-1683">carte di credito</span></span> 
- <span data-ttu-id="32d8c-1684">carteblanche</span><span class="sxs-lookup"><span data-stu-id="32d8c-1684">carteblanche</span></span> 
- <span data-ttu-id="32d8c-1685">cartão de credito</span><span class="sxs-lookup"><span data-stu-id="32d8c-1685">cartão de credito</span></span> 
- <span data-ttu-id="32d8c-1686">cartão de crédito</span><span class="sxs-lookup"><span data-stu-id="32d8c-1686">cartão de crédito</span></span> 
- <span data-ttu-id="32d8c-1687">cartão de debito</span><span class="sxs-lookup"><span data-stu-id="32d8c-1687">cartão de debito</span></span> 
- <span data-ttu-id="32d8c-1688">cartão de débito</span><span class="sxs-lookup"><span data-stu-id="32d8c-1688">cartão de débito</span></span> 
- <span data-ttu-id="32d8c-1689">cb</span><span class="sxs-lookup"><span data-stu-id="32d8c-1689">cb</span></span> 
- <span data-ttu-id="32d8c-1690">CCN</span><span class="sxs-lookup"><span data-stu-id="32d8c-1690">ccn</span></span> 
- <span data-ttu-id="32d8c-1691">carte de vérification</span><span class="sxs-lookup"><span data-stu-id="32d8c-1691">check card</span></span> 
- <span data-ttu-id="32d8c-1692">cartes de vérification</span><span class="sxs-lookup"><span data-stu-id="32d8c-1692">check cards</span></span> 
- <span data-ttu-id="32d8c-1693">carte</span><span class="sxs-lookup"><span data-stu-id="32d8c-1693">checkcard</span></span>
- <span data-ttu-id="32d8c-1694">cartes</span><span class="sxs-lookup"><span data-stu-id="32d8c-1694">checkcards</span></span> 
- <span data-ttu-id="32d8c-1695">chequekaart</span><span class="sxs-lookup"><span data-stu-id="32d8c-1695">chequekaart</span></span> 
- <span data-ttu-id="32d8c-1696">Cirrus</span><span class="sxs-lookup"><span data-stu-id="32d8c-1696">cirrus</span></span> 
- <span data-ttu-id="32d8c-1697">Cirrus-EDC-Maestro</span><span class="sxs-lookup"><span data-stu-id="32d8c-1697">cirrus-edc-maestro</span></span> 
- <span data-ttu-id="32d8c-1698">controlekaart</span><span class="sxs-lookup"><span data-stu-id="32d8c-1698">controlekaart</span></span> 
- <span data-ttu-id="32d8c-1699">controlekaarten</span><span class="sxs-lookup"><span data-stu-id="32d8c-1699">controlekaarten</span></span> 
- <span data-ttu-id="32d8c-1700">carte de crédit</span><span class="sxs-lookup"><span data-stu-id="32d8c-1700">credit card</span></span> 
- <span data-ttu-id="32d8c-1701">cartes de crédit</span><span class="sxs-lookup"><span data-stu-id="32d8c-1701">credit cards</span></span> 
- <span data-ttu-id="32d8c-1702">CreditCard</span><span class="sxs-lookup"><span data-stu-id="32d8c-1702">creditcard</span></span> 
- <span data-ttu-id="32d8c-1703">crédit</span><span class="sxs-lookup"><span data-stu-id="32d8c-1703">creditcards</span></span> 
- <span data-ttu-id="32d8c-1704">debetkaart</span><span class="sxs-lookup"><span data-stu-id="32d8c-1704">debetkaart</span></span> 
- <span data-ttu-id="32d8c-1705">debetkaarten</span><span class="sxs-lookup"><span data-stu-id="32d8c-1705">debetkaarten</span></span> 
- <span data-ttu-id="32d8c-1706">carte de débit</span><span class="sxs-lookup"><span data-stu-id="32d8c-1706">debit card</span></span> 
- <span data-ttu-id="32d8c-1707">cartes de débit</span><span class="sxs-lookup"><span data-stu-id="32d8c-1707">debit cards</span></span> 
- <span data-ttu-id="32d8c-1708">débit</span><span class="sxs-lookup"><span data-stu-id="32d8c-1708">debitcard</span></span> 
- <span data-ttu-id="32d8c-1709">débit</span><span class="sxs-lookup"><span data-stu-id="32d8c-1709">debitcards</span></span> 
- <span data-ttu-id="32d8c-1710">debito automatico</span><span class="sxs-lookup"><span data-stu-id="32d8c-1710">debito automatico</span></span> 
- <span data-ttu-id="32d8c-1711">diners club</span><span class="sxs-lookup"><span data-stu-id="32d8c-1711">diners club</span></span> 
- <span data-ttu-id="32d8c-1712">dinersclub</span><span class="sxs-lookup"><span data-stu-id="32d8c-1712">dinersclub</span></span> 
- <span data-ttu-id="32d8c-1713">connaissance</span><span class="sxs-lookup"><span data-stu-id="32d8c-1713">discover</span></span> 
- <span data-ttu-id="32d8c-1714">discover card</span><span class="sxs-lookup"><span data-stu-id="32d8c-1714">discover card</span></span> 
- <span data-ttu-id="32d8c-1715">discover cards</span><span class="sxs-lookup"><span data-stu-id="32d8c-1715">discover cards</span></span> 
- <span data-ttu-id="32d8c-1716">discovercard</span><span class="sxs-lookup"><span data-stu-id="32d8c-1716">discovercard</span></span> 
- <span data-ttu-id="32d8c-1717">discovercards</span><span class="sxs-lookup"><span data-stu-id="32d8c-1717">discovercards</span></span> 
- <span data-ttu-id="32d8c-1718">débito automático</span><span class="sxs-lookup"><span data-stu-id="32d8c-1718">débito automático</span></span>
- <span data-ttu-id="32d8c-1719">EDC</span><span class="sxs-lookup"><span data-stu-id="32d8c-1719">edc</span></span> 
- <span data-ttu-id="32d8c-1720">eigentümername</span><span class="sxs-lookup"><span data-stu-id="32d8c-1720">eigentümername</span></span> 
- <span data-ttu-id="32d8c-1721">carte de crédit européenne</span><span class="sxs-lookup"><span data-stu-id="32d8c-1721">european debit card</span></span> 
- <span data-ttu-id="32d8c-1722">hoofdkaart</span><span class="sxs-lookup"><span data-stu-id="32d8c-1722">hoofdkaart</span></span> 
- <span data-ttu-id="32d8c-1723">hoofdkaarten</span><span class="sxs-lookup"><span data-stu-id="32d8c-1723">hoofdkaarten</span></span> 
- <span data-ttu-id="32d8c-1724">in viaggio</span><span class="sxs-lookup"><span data-stu-id="32d8c-1724">in viaggio</span></span> 
- <span data-ttu-id="32d8c-1725">japanese card bureau</span><span class="sxs-lookup"><span data-stu-id="32d8c-1725">japanese card bureau</span></span> 
- <span data-ttu-id="32d8c-1726">japanse kaartdienst</span><span class="sxs-lookup"><span data-stu-id="32d8c-1726">japanse kaartdienst</span></span> 
- <span data-ttu-id="32d8c-1727">JCB</span><span class="sxs-lookup"><span data-stu-id="32d8c-1727">jcb</span></span> 
- <span data-ttu-id="32d8c-1728">kaart</span><span class="sxs-lookup"><span data-stu-id="32d8c-1728">kaart</span></span> 
- <span data-ttu-id="32d8c-1729">kaart num</span><span class="sxs-lookup"><span data-stu-id="32d8c-1729">kaart num</span></span> 
- <span data-ttu-id="32d8c-1730">kaartaantal</span><span class="sxs-lookup"><span data-stu-id="32d8c-1730">kaartaantal</span></span> 
- <span data-ttu-id="32d8c-1731">kaartaantallen</span><span class="sxs-lookup"><span data-stu-id="32d8c-1731">kaartaantallen</span></span> 
- <span data-ttu-id="32d8c-1732">kaarthouder</span><span class="sxs-lookup"><span data-stu-id="32d8c-1732">kaarthouder</span></span> 
- <span data-ttu-id="32d8c-1733">kaarthouders</span><span class="sxs-lookup"><span data-stu-id="32d8c-1733">kaarthouders</span></span> 
- <span data-ttu-id="32d8c-1734">karte</span><span class="sxs-lookup"><span data-stu-id="32d8c-1734">karte</span></span>  
- <span data-ttu-id="32d8c-1735">karteninhaber</span><span class="sxs-lookup"><span data-stu-id="32d8c-1735">karteninhaber</span></span> 
- <span data-ttu-id="32d8c-1736">karteninhabers</span><span class="sxs-lookup"><span data-stu-id="32d8c-1736">karteninhabers</span></span>
- <span data-ttu-id="32d8c-1737">kartennr</span><span class="sxs-lookup"><span data-stu-id="32d8c-1737">kartennr</span></span> 
- <span data-ttu-id="32d8c-1738">kartennummer</span><span class="sxs-lookup"><span data-stu-id="32d8c-1738">kartennummer</span></span> 
- <span data-ttu-id="32d8c-1739">kreditkarte</span><span class="sxs-lookup"><span data-stu-id="32d8c-1739">kreditkarte</span></span> 
- <span data-ttu-id="32d8c-1740">kreditkarten-nummer</span><span class="sxs-lookup"><span data-stu-id="32d8c-1740">kreditkarten-nummer</span></span> 
- <span data-ttu-id="32d8c-1741">kreditkarteninhaber</span><span class="sxs-lookup"><span data-stu-id="32d8c-1741">kreditkarteninhaber</span></span> 
- <span data-ttu-id="32d8c-1742">kreditkarteninstitut</span><span class="sxs-lookup"><span data-stu-id="32d8c-1742">kreditkarteninstitut</span></span> 
- <span data-ttu-id="32d8c-1743">kreditkartennummer</span><span class="sxs-lookup"><span data-stu-id="32d8c-1743">kreditkartennummer</span></span> 
- <span data-ttu-id="32d8c-1744">kreditkartentyp</span><span class="sxs-lookup"><span data-stu-id="32d8c-1744">kreditkartentyp</span></span> 
- <span data-ttu-id="32d8c-1745">sonne</span><span class="sxs-lookup"><span data-stu-id="32d8c-1745">maestro</span></span> 
- <span data-ttu-id="32d8c-1746">master card</span><span class="sxs-lookup"><span data-stu-id="32d8c-1746">master card</span></span> 
- <span data-ttu-id="32d8c-1747">master cards</span><span class="sxs-lookup"><span data-stu-id="32d8c-1747">master cards</span></span> 
- <span data-ttu-id="32d8c-1748">MasterCard</span><span class="sxs-lookup"><span data-stu-id="32d8c-1748">mastercard</span></span> 
- <span data-ttu-id="32d8c-1749">MasterCard</span><span class="sxs-lookup"><span data-stu-id="32d8c-1749">mastercards</span></span> 
- <span data-ttu-id="32d8c-1750">McDonald</span><span class="sxs-lookup"><span data-stu-id="32d8c-1750">mc</span></span> 
- <span data-ttu-id="32d8c-1751">mister cash</span><span class="sxs-lookup"><span data-stu-id="32d8c-1751">mister cash</span></span> 
- <span data-ttu-id="32d8c-1752">n carta</span><span class="sxs-lookup"><span data-stu-id="32d8c-1752">n carta</span></span> 
- <span data-ttu-id="32d8c-1753">Carta</span><span class="sxs-lookup"><span data-stu-id="32d8c-1753">carta</span></span> 
- <span data-ttu-id="32d8c-1754">no de tarjeta</span><span class="sxs-lookup"><span data-stu-id="32d8c-1754">no de tarjeta</span></span> 
- <span data-ttu-id="32d8c-1755">no do cartao</span><span class="sxs-lookup"><span data-stu-id="32d8c-1755">no do cartao</span></span> 
- <span data-ttu-id="32d8c-1756">no do cartão</span><span class="sxs-lookup"><span data-stu-id="32d8c-1756">no do cartão</span></span> 
- <span data-ttu-id="32d8c-1757">Nbre.</span><span class="sxs-lookup"><span data-stu-id="32d8c-1757">no.</span></span> <span data-ttu-id="32d8c-1758">de tarjeta</span><span class="sxs-lookup"><span data-stu-id="32d8c-1758">de tarjeta</span></span> 
- <span data-ttu-id="32d8c-1759">Nbre.</span><span class="sxs-lookup"><span data-stu-id="32d8c-1759">no.</span></span> <span data-ttu-id="32d8c-1760">do cartao</span><span class="sxs-lookup"><span data-stu-id="32d8c-1760">do cartao</span></span> 
- <span data-ttu-id="32d8c-1761">Nbre.</span><span class="sxs-lookup"><span data-stu-id="32d8c-1761">no.</span></span> <span data-ttu-id="32d8c-1762">do cartão</span><span class="sxs-lookup"><span data-stu-id="32d8c-1762">do cartão</span></span> 
- <span data-ttu-id="32d8c-1763">nr carta</span><span class="sxs-lookup"><span data-stu-id="32d8c-1763">nr carta</span></span> 
- <span data-ttu-id="32d8c-1764">Nr.</span><span class="sxs-lookup"><span data-stu-id="32d8c-1764">nr.</span></span> <span data-ttu-id="32d8c-1765">Carta</span><span class="sxs-lookup"><span data-stu-id="32d8c-1765">carta</span></span> 
- <span data-ttu-id="32d8c-1766">numeri di scheda</span><span class="sxs-lookup"><span data-stu-id="32d8c-1766">numeri di scheda</span></span> 
- <span data-ttu-id="32d8c-1767">numero carta</span><span class="sxs-lookup"><span data-stu-id="32d8c-1767">numero carta</span></span> 
- <span data-ttu-id="32d8c-1768">numero de cartao</span><span class="sxs-lookup"><span data-stu-id="32d8c-1768">numero de cartao</span></span> 
- <span data-ttu-id="32d8c-1769">numero de carte</span><span class="sxs-lookup"><span data-stu-id="32d8c-1769">numero de carte</span></span> 
- <span data-ttu-id="32d8c-1770">numero de cartão</span><span class="sxs-lookup"><span data-stu-id="32d8c-1770">numero de cartão</span></span> 
- <span data-ttu-id="32d8c-1771">numero de tarjeta</span><span class="sxs-lookup"><span data-stu-id="32d8c-1771">numero de tarjeta</span></span>
- <span data-ttu-id="32d8c-1772">numero della carta</span><span class="sxs-lookup"><span data-stu-id="32d8c-1772">numero della carta</span></span> 
- <span data-ttu-id="32d8c-1773">numero di carta</span><span class="sxs-lookup"><span data-stu-id="32d8c-1773">numero di carta</span></span> 
- <span data-ttu-id="32d8c-1774">numero di scheda</span><span class="sxs-lookup"><span data-stu-id="32d8c-1774">numero di scheda</span></span> 
- <span data-ttu-id="32d8c-1775">numero do cartao</span><span class="sxs-lookup"><span data-stu-id="32d8c-1775">numero do cartao</span></span> 
- <span data-ttu-id="32d8c-1776">numero do cartão</span><span class="sxs-lookup"><span data-stu-id="32d8c-1776">numero do cartão</span></span> 
- <span data-ttu-id="32d8c-1777">numéro de carte</span><span class="sxs-lookup"><span data-stu-id="32d8c-1777">numéro de carte</span></span> 
- <span data-ttu-id="32d8c-1778">nº carta</span><span class="sxs-lookup"><span data-stu-id="32d8c-1778">nº carta</span></span> 
- <span data-ttu-id="32d8c-1779">nº de carte</span><span class="sxs-lookup"><span data-stu-id="32d8c-1779">nº de carte</span></span> 
- <span data-ttu-id="32d8c-1780">nº de la carte</span><span class="sxs-lookup"><span data-stu-id="32d8c-1780">nº de la carte</span></span> 
- <span data-ttu-id="32d8c-1781">nº de tarjeta</span><span class="sxs-lookup"><span data-stu-id="32d8c-1781">nº de tarjeta</span></span> 
- <span data-ttu-id="32d8c-1782">nº do cartao</span><span class="sxs-lookup"><span data-stu-id="32d8c-1782">nº do cartao</span></span> 
- <span data-ttu-id="32d8c-1783">nº do cartão</span><span class="sxs-lookup"><span data-stu-id="32d8c-1783">nº do cartão</span></span> 
- <span data-ttu-id="32d8c-1784">n º.</span><span class="sxs-lookup"><span data-stu-id="32d8c-1784">nº.</span></span> <span data-ttu-id="32d8c-1785">do cartão</span><span class="sxs-lookup"><span data-stu-id="32d8c-1785">do cartão</span></span> 
- <span data-ttu-id="32d8c-1786">número de cartao</span><span class="sxs-lookup"><span data-stu-id="32d8c-1786">número de cartao</span></span> 
- <span data-ttu-id="32d8c-1787">número de cartão</span><span class="sxs-lookup"><span data-stu-id="32d8c-1787">número de cartão</span></span> 
- <span data-ttu-id="32d8c-1788">número de tarjeta</span><span class="sxs-lookup"><span data-stu-id="32d8c-1788">número de tarjeta</span></span> 
- <span data-ttu-id="32d8c-1789">número do cartao</span><span class="sxs-lookup"><span data-stu-id="32d8c-1789">número do cartao</span></span> 
- <span data-ttu-id="32d8c-1790">scheda dell’assegno</span><span class="sxs-lookup"><span data-stu-id="32d8c-1790">scheda dell'assegno</span></span> 
- <span data-ttu-id="32d8c-1791">scheda dell’atmosfera</span><span class="sxs-lookup"><span data-stu-id="32d8c-1791">scheda dell'atmosfera</span></span> 
- <span data-ttu-id="32d8c-1792">scheda dell’atmosfera</span><span class="sxs-lookup"><span data-stu-id="32d8c-1792">scheda dell'atmosfera</span></span> 
- <span data-ttu-id="32d8c-1793">scheda della banca</span><span class="sxs-lookup"><span data-stu-id="32d8c-1793">scheda della banca</span></span> 
- <span data-ttu-id="32d8c-1794">scheda di controllo</span><span class="sxs-lookup"><span data-stu-id="32d8c-1794">scheda di controllo</span></span> 
- <span data-ttu-id="32d8c-1795">scheda di debito</span><span class="sxs-lookup"><span data-stu-id="32d8c-1795">scheda di debito</span></span> 
- <span data-ttu-id="32d8c-1796">scheda matrice</span><span class="sxs-lookup"><span data-stu-id="32d8c-1796">scheda matrice</span></span> 
- <span data-ttu-id="32d8c-1797">schede dell’atmosfera</span><span class="sxs-lookup"><span data-stu-id="32d8c-1797">schede dell'atmosfera</span></span> 
- <span data-ttu-id="32d8c-1798">schede di controllo</span><span class="sxs-lookup"><span data-stu-id="32d8c-1798">schede di controllo</span></span> 
- <span data-ttu-id="32d8c-1799">schede di debito</span><span class="sxs-lookup"><span data-stu-id="32d8c-1799">schede di debito</span></span> 
- <span data-ttu-id="32d8c-1800">schede matrici</span><span class="sxs-lookup"><span data-stu-id="32d8c-1800">schede matrici</span></span> 
- <span data-ttu-id="32d8c-1801">scoprono la scheda</span><span class="sxs-lookup"><span data-stu-id="32d8c-1801">scoprono la scheda</span></span> 
- <span data-ttu-id="32d8c-1802">scoprono le schede</span><span class="sxs-lookup"><span data-stu-id="32d8c-1802">scoprono le schede</span></span> 
- <span data-ttu-id="32d8c-1803">tracteur</span><span class="sxs-lookup"><span data-stu-id="32d8c-1803">solo</span></span> 
- <span data-ttu-id="32d8c-1804">supporti di scheda</span><span class="sxs-lookup"><span data-stu-id="32d8c-1804">supporti di scheda</span></span> 
- <span data-ttu-id="32d8c-1805">supporto di scheda</span><span class="sxs-lookup"><span data-stu-id="32d8c-1805">supporto di scheda</span></span> 
- <span data-ttu-id="32d8c-1806">accéder</span><span class="sxs-lookup"><span data-stu-id="32d8c-1806">switch</span></span> 
- <span data-ttu-id="32d8c-1807">tarjeta atm</span><span class="sxs-lookup"><span data-stu-id="32d8c-1807">tarjeta atm</span></span> 
- <span data-ttu-id="32d8c-1808">tarjeta credito</span><span class="sxs-lookup"><span data-stu-id="32d8c-1808">tarjeta credito</span></span> 
- <span data-ttu-id="32d8c-1809">tarjeta de atm</span><span class="sxs-lookup"><span data-stu-id="32d8c-1809">tarjeta de atm</span></span> 
- <span data-ttu-id="32d8c-1810">tarjeta de credito</span><span class="sxs-lookup"><span data-stu-id="32d8c-1810">tarjeta de credito</span></span> 
- <span data-ttu-id="32d8c-1811">tarjeta de debito</span><span class="sxs-lookup"><span data-stu-id="32d8c-1811">tarjeta de debito</span></span> 
- <span data-ttu-id="32d8c-1812">tarjeta debito</span><span class="sxs-lookup"><span data-stu-id="32d8c-1812">tarjeta debito</span></span> 
- <span data-ttu-id="32d8c-1813">tarjeta no</span><span class="sxs-lookup"><span data-stu-id="32d8c-1813">tarjeta no</span></span>
- <span data-ttu-id="32d8c-1814">tarjetahabiente</span><span class="sxs-lookup"><span data-stu-id="32d8c-1814">tarjetahabiente</span></span> 
- <span data-ttu-id="32d8c-1815">tipo della scheda</span><span class="sxs-lookup"><span data-stu-id="32d8c-1815">tipo della scheda</span></span> 
- <span data-ttu-id="32d8c-1816">ufficio giapponese della</span><span class="sxs-lookup"><span data-stu-id="32d8c-1816">ufficio giapponese della</span></span> 
- <span data-ttu-id="32d8c-1817">scheda</span><span class="sxs-lookup"><span data-stu-id="32d8c-1817">scheda</span></span> 
- <span data-ttu-id="32d8c-1818">v pay</span><span class="sxs-lookup"><span data-stu-id="32d8c-1818">v pay</span></span> 
- <span data-ttu-id="32d8c-1819">v-Pay</span><span class="sxs-lookup"><span data-stu-id="32d8c-1819">v-pay</span></span> 
- <span data-ttu-id="32d8c-1820">délivrance</span><span class="sxs-lookup"><span data-stu-id="32d8c-1820">visa</span></span> 
- <span data-ttu-id="32d8c-1821">visa plus</span><span class="sxs-lookup"><span data-stu-id="32d8c-1821">visa plus</span></span> 
- <span data-ttu-id="32d8c-1822">visa electron</span><span class="sxs-lookup"><span data-stu-id="32d8c-1822">visa electron</span></span> 
- <span data-ttu-id="32d8c-1823">visto</span><span class="sxs-lookup"><span data-stu-id="32d8c-1823">visto</span></span> 
- <span data-ttu-id="32d8c-1824">visum</span><span class="sxs-lookup"><span data-stu-id="32d8c-1824">visum</span></span> 
- <span data-ttu-id="32d8c-1825">vpay</span><span class="sxs-lookup"><span data-stu-id="32d8c-1825">vpay</span></span>   

#### <a name="keyword_card_security_terms_dict"></a><span data-ttu-id="32d8c-1826">Keyword_card_security_terms_dict</span><span class="sxs-lookup"><span data-stu-id="32d8c-1826">Keyword_card_security_terms_dict</span></span>

- <span data-ttu-id="32d8c-1827">numéro d’identification de la carte</span><span class="sxs-lookup"><span data-stu-id="32d8c-1827">card identification number</span></span>
- <span data-ttu-id="32d8c-1828">vérification de la carte</span><span class="sxs-lookup"><span data-stu-id="32d8c-1828">card verification</span></span> 
- <span data-ttu-id="32d8c-1829">cardi la verifica</span><span class="sxs-lookup"><span data-stu-id="32d8c-1829">cardi la verifica</span></span> 
- <span data-ttu-id="32d8c-1830">nic</span><span class="sxs-lookup"><span data-stu-id="32d8c-1830">cid</span></span> 
- <span data-ttu-id="32d8c-1831">cod seg</span><span class="sxs-lookup"><span data-stu-id="32d8c-1831">cod seg</span></span> 
- <span data-ttu-id="32d8c-1832">cod seguranca</span><span class="sxs-lookup"><span data-stu-id="32d8c-1832">cod seguranca</span></span> 
- <span data-ttu-id="32d8c-1833">cod segurança</span><span class="sxs-lookup"><span data-stu-id="32d8c-1833">cod segurança</span></span> 
- <span data-ttu-id="32d8c-1834">cod sicurezza</span><span class="sxs-lookup"><span data-stu-id="32d8c-1834">cod sicurezza</span></span> 
- <span data-ttu-id="32d8c-1835">contre.</span><span class="sxs-lookup"><span data-stu-id="32d8c-1835">cod.</span></span> <span data-ttu-id="32d8c-1836">SEG</span><span class="sxs-lookup"><span data-stu-id="32d8c-1836">seg</span></span> 
- <span data-ttu-id="32d8c-1837">contre.</span><span class="sxs-lookup"><span data-stu-id="32d8c-1837">cod.</span></span> <span data-ttu-id="32d8c-1838">seguranca</span><span class="sxs-lookup"><span data-stu-id="32d8c-1838">seguranca</span></span> 
- <span data-ttu-id="32d8c-1839">contre.</span><span class="sxs-lookup"><span data-stu-id="32d8c-1839">cod.</span></span> <span data-ttu-id="32d8c-1840">segurança</span><span class="sxs-lookup"><span data-stu-id="32d8c-1840">segurança</span></span> 
- <span data-ttu-id="32d8c-1841">contre.</span><span class="sxs-lookup"><span data-stu-id="32d8c-1841">cod.</span></span> <span data-ttu-id="32d8c-1842">sicurezza</span><span class="sxs-lookup"><span data-stu-id="32d8c-1842">sicurezza</span></span> 
- <span data-ttu-id="32d8c-1843">codice di sicurezza</span><span class="sxs-lookup"><span data-stu-id="32d8c-1843">codice di sicurezza</span></span> 
- <span data-ttu-id="32d8c-1844">codice di verifica</span><span class="sxs-lookup"><span data-stu-id="32d8c-1844">codice di verifica</span></span> 
- <span data-ttu-id="32d8c-1845">codigo</span><span class="sxs-lookup"><span data-stu-id="32d8c-1845">codigo</span></span> 
- <span data-ttu-id="32d8c-1846">codigo de seguranca</span><span class="sxs-lookup"><span data-stu-id="32d8c-1846">codigo de seguranca</span></span> 
- <span data-ttu-id="32d8c-1847">codigo de segurança</span><span class="sxs-lookup"><span data-stu-id="32d8c-1847">codigo de segurança</span></span> 
- <span data-ttu-id="32d8c-1848">crittogramma</span><span class="sxs-lookup"><span data-stu-id="32d8c-1848">crittogramma</span></span> 
- <span data-ttu-id="32d8c-1849">cryptogram</span><span class="sxs-lookup"><span data-stu-id="32d8c-1849">cryptogram</span></span> 
- <span data-ttu-id="32d8c-1850">cryptogramme</span><span class="sxs-lookup"><span data-stu-id="32d8c-1850">cryptogramme</span></span> 
- <span data-ttu-id="32d8c-1851">cv2</span><span class="sxs-lookup"><span data-stu-id="32d8c-1851">cv2</span></span> 
- <span data-ttu-id="32d8c-1852">lâche</span><span class="sxs-lookup"><span data-stu-id="32d8c-1852">cvc</span></span> 
- <span data-ttu-id="32d8c-1853">cvc2</span><span class="sxs-lookup"><span data-stu-id="32d8c-1853">cvc2</span></span> 
- <span data-ttu-id="32d8c-1854">cryptogramme</span><span class="sxs-lookup"><span data-stu-id="32d8c-1854">cvn</span></span> 
- <span data-ttu-id="32d8c-1855">cvv</span><span class="sxs-lookup"><span data-stu-id="32d8c-1855">cvv</span></span> 
- <span data-ttu-id="32d8c-1856">cvv2</span><span class="sxs-lookup"><span data-stu-id="32d8c-1856">cvv2</span></span> 
- <span data-ttu-id="32d8c-1857">cód seguranca</span><span class="sxs-lookup"><span data-stu-id="32d8c-1857">cód seguranca</span></span> 
- <span data-ttu-id="32d8c-1858">cód segurança</span><span class="sxs-lookup"><span data-stu-id="32d8c-1858">cód segurança</span></span> 
- <span data-ttu-id="32d8c-1859">cód.</span><span class="sxs-lookup"><span data-stu-id="32d8c-1859">cód.</span></span> <span data-ttu-id="32d8c-1860">seguranca</span><span class="sxs-lookup"><span data-stu-id="32d8c-1860">seguranca</span></span> 
- <span data-ttu-id="32d8c-1861">cód.</span><span class="sxs-lookup"><span data-stu-id="32d8c-1861">cód.</span></span> <span data-ttu-id="32d8c-1862">segurança</span><span class="sxs-lookup"><span data-stu-id="32d8c-1862">segurança</span></span> 
- <span data-ttu-id="32d8c-1863">código</span><span class="sxs-lookup"><span data-stu-id="32d8c-1863">código</span></span> 
- <span data-ttu-id="32d8c-1864">código de seguranca</span><span class="sxs-lookup"><span data-stu-id="32d8c-1864">código de seguranca</span></span> 
- <span data-ttu-id="32d8c-1865">código de segurança</span><span class="sxs-lookup"><span data-stu-id="32d8c-1865">código de segurança</span></span> 
- <span data-ttu-id="32d8c-1866">de kaart controle</span><span class="sxs-lookup"><span data-stu-id="32d8c-1866">de kaart controle</span></span> 
- <span data-ttu-id="32d8c-1867">geeft nr suit</span><span class="sxs-lookup"><span data-stu-id="32d8c-1867">geeft nr uit</span></span> 
- <span data-ttu-id="32d8c-1868">n° d’émission</span><span class="sxs-lookup"><span data-stu-id="32d8c-1868">issue no</span></span> 
- <span data-ttu-id="32d8c-1869">numéro d’émission</span><span class="sxs-lookup"><span data-stu-id="32d8c-1869">issue number</span></span> 
- <span data-ttu-id="32d8c-1870">kaartidentificatienummer</span><span class="sxs-lookup"><span data-stu-id="32d8c-1870">kaartidentificatienummer</span></span> 
- <span data-ttu-id="32d8c-1871">kreditkartenprufnummer</span><span class="sxs-lookup"><span data-stu-id="32d8c-1871">kreditkartenprufnummer</span></span> 
- <span data-ttu-id="32d8c-1872">kreditkartenprüfnummer</span><span class="sxs-lookup"><span data-stu-id="32d8c-1872">kreditkartenprüfnummer</span></span> 
- <span data-ttu-id="32d8c-1873">kwestieaantal</span><span class="sxs-lookup"><span data-stu-id="32d8c-1873">kwestieaantal</span></span> 
- <span data-ttu-id="32d8c-1874">Nbre.</span><span class="sxs-lookup"><span data-stu-id="32d8c-1874">no.</span></span> <span data-ttu-id="32d8c-1875">dell'edizione</span><span class="sxs-lookup"><span data-stu-id="32d8c-1875">dell'edizione</span></span> 
- <span data-ttu-id="32d8c-1876">Nbre.</span><span class="sxs-lookup"><span data-stu-id="32d8c-1876">no.</span></span> <span data-ttu-id="32d8c-1877">di sicurezza</span><span class="sxs-lookup"><span data-stu-id="32d8c-1877">di sicurezza</span></span> 
- <span data-ttu-id="32d8c-1878">numéro de sécurité</span><span class="sxs-lookup"><span data-stu-id="32d8c-1878">numero de securite</span></span> 
- <span data-ttu-id="32d8c-1879">numero de verificacao</span><span class="sxs-lookup"><span data-stu-id="32d8c-1879">numero de verificacao</span></span> 
- <span data-ttu-id="32d8c-1880">numero dell’edizione</span><span class="sxs-lookup"><span data-stu-id="32d8c-1880">numero dell'edizione</span></span> 
- <span data-ttu-id="32d8c-1881">numero di identificazione della</span><span class="sxs-lookup"><span data-stu-id="32d8c-1881">numero di identificazione della</span></span> 
- <span data-ttu-id="32d8c-1882">scheda</span><span class="sxs-lookup"><span data-stu-id="32d8c-1882">scheda</span></span> 
- <span data-ttu-id="32d8c-1883">numero di sicurezza</span><span class="sxs-lookup"><span data-stu-id="32d8c-1883">numero di sicurezza</span></span> 
- <span data-ttu-id="32d8c-1884">numero van veiligheid</span><span class="sxs-lookup"><span data-stu-id="32d8c-1884">numero van veiligheid</span></span> 
- <span data-ttu-id="32d8c-1885">numéro de sécurité</span><span class="sxs-lookup"><span data-stu-id="32d8c-1885">numéro de sécurité</span></span> 
- <span data-ttu-id="32d8c-1886">nº autorizzazione</span><span class="sxs-lookup"><span data-stu-id="32d8c-1886">nº autorizzazione</span></span> 
- <span data-ttu-id="32d8c-1887">número de verificação</span><span class="sxs-lookup"><span data-stu-id="32d8c-1887">número de verificação</span></span> 
- <span data-ttu-id="32d8c-1888">perno il blocco</span><span class="sxs-lookup"><span data-stu-id="32d8c-1888">perno il blocco</span></span> 
- <span data-ttu-id="32d8c-1889">pin block</span><span class="sxs-lookup"><span data-stu-id="32d8c-1889">pin block</span></span> 
- <span data-ttu-id="32d8c-1890">prufziffer</span><span class="sxs-lookup"><span data-stu-id="32d8c-1890">prufziffer</span></span> 
- <span data-ttu-id="32d8c-1891">prüfziffer</span><span class="sxs-lookup"><span data-stu-id="32d8c-1891">prüfziffer</span></span> 
- <span data-ttu-id="32d8c-1892">code de sécurité</span><span class="sxs-lookup"><span data-stu-id="32d8c-1892">security code</span></span> 
- <span data-ttu-id="32d8c-1893">n° de sécurité</span><span class="sxs-lookup"><span data-stu-id="32d8c-1893">security no</span></span> 
- <span data-ttu-id="32d8c-1894">numéro de sécurité</span><span class="sxs-lookup"><span data-stu-id="32d8c-1894">security number</span></span> 
- <span data-ttu-id="32d8c-1895">sicherheits kode</span><span class="sxs-lookup"><span data-stu-id="32d8c-1895">sicherheits kode</span></span> 
- <span data-ttu-id="32d8c-1896">sicherheitscode</span><span class="sxs-lookup"><span data-stu-id="32d8c-1896">sicherheitscode</span></span> 
- <span data-ttu-id="32d8c-1897">sicherheitsnummer</span><span class="sxs-lookup"><span data-stu-id="32d8c-1897">sicherheitsnummer</span></span> 
- <span data-ttu-id="32d8c-1898">speldblok</span><span class="sxs-lookup"><span data-stu-id="32d8c-1898">speldblok</span></span> 
- <span data-ttu-id="32d8c-1899">veiligheid nr</span><span class="sxs-lookup"><span data-stu-id="32d8c-1899">veiligheid nr</span></span> 
- <span data-ttu-id="32d8c-1900">veiligheidsaantal</span><span class="sxs-lookup"><span data-stu-id="32d8c-1900">veiligheidsaantal</span></span> 
- <span data-ttu-id="32d8c-1901">veiligheidscode</span><span class="sxs-lookup"><span data-stu-id="32d8c-1901">veiligheidscode</span></span> 
- <span data-ttu-id="32d8c-1902">veiligheidsnummer</span><span class="sxs-lookup"><span data-stu-id="32d8c-1902">veiligheidsnummer</span></span> 
- <span data-ttu-id="32d8c-1903">verfalldatum</span><span class="sxs-lookup"><span data-stu-id="32d8c-1903">verfalldatum</span></span> 

#### <a name="keyword_card_expiration_terms_dict"></a><span data-ttu-id="32d8c-1904">Keyword_card_expiration_terms_dict</span><span class="sxs-lookup"><span data-stu-id="32d8c-1904">Keyword_card_expiration_terms_dict</span></span>

- <span data-ttu-id="32d8c-1905">ablauf</span><span class="sxs-lookup"><span data-stu-id="32d8c-1905">ablauf</span></span> 
- <span data-ttu-id="32d8c-1906">data de expiracao</span><span class="sxs-lookup"><span data-stu-id="32d8c-1906">data de expiracao</span></span> 
- <span data-ttu-id="32d8c-1907">data de expiração</span><span class="sxs-lookup"><span data-stu-id="32d8c-1907">data de expiração</span></span> 
- <span data-ttu-id="32d8c-1908">data del exp</span><span class="sxs-lookup"><span data-stu-id="32d8c-1908">data del exp</span></span> 
- <span data-ttu-id="32d8c-1909">data di exp</span><span class="sxs-lookup"><span data-stu-id="32d8c-1909">data di exp</span></span> 
- <span data-ttu-id="32d8c-1910">data di scadenza</span><span class="sxs-lookup"><span data-stu-id="32d8c-1910">data di scadenza</span></span> 
- <span data-ttu-id="32d8c-1911">data em que expira</span><span class="sxs-lookup"><span data-stu-id="32d8c-1911">data em que expira</span></span> 
- <span data-ttu-id="32d8c-1912">data scad</span><span class="sxs-lookup"><span data-stu-id="32d8c-1912">data scad</span></span> 
- <span data-ttu-id="32d8c-1913">data scadenza</span><span class="sxs-lookup"><span data-stu-id="32d8c-1913">data scadenza</span></span> 
- <span data-ttu-id="32d8c-1914">date de validité</span><span class="sxs-lookup"><span data-stu-id="32d8c-1914">date de validité</span></span> 
- <span data-ttu-id="32d8c-1915">datum afloop</span><span class="sxs-lookup"><span data-stu-id="32d8c-1915">datum afloop</span></span> 
- <span data-ttu-id="32d8c-1916">datum van exp</span><span class="sxs-lookup"><span data-stu-id="32d8c-1916">datum van exp</span></span> 
- <span data-ttu-id="32d8c-1917">de afloop</span><span class="sxs-lookup"><span data-stu-id="32d8c-1917">de afloop</span></span> 
- <span data-ttu-id="32d8c-1918">espira</span><span class="sxs-lookup"><span data-stu-id="32d8c-1918">espira</span></span> 
- <span data-ttu-id="32d8c-1919">espira</span><span class="sxs-lookup"><span data-stu-id="32d8c-1919">espira</span></span> 
- <span data-ttu-id="32d8c-1920">date d’exp</span><span class="sxs-lookup"><span data-stu-id="32d8c-1920">exp date</span></span> 
- <span data-ttu-id="32d8c-1921">exp datum</span><span class="sxs-lookup"><span data-stu-id="32d8c-1921">exp datum</span></span> 
- <span data-ttu-id="32d8c-1922">pire</span><span class="sxs-lookup"><span data-stu-id="32d8c-1922">expiration</span></span> 
- <span data-ttu-id="32d8c-1923">expiration</span><span class="sxs-lookup"><span data-stu-id="32d8c-1923">expire</span></span> 
- <span data-ttu-id="32d8c-1924">expire</span><span class="sxs-lookup"><span data-stu-id="32d8c-1924">expires</span></span> 
- <span data-ttu-id="32d8c-1925">expiration</span><span class="sxs-lookup"><span data-stu-id="32d8c-1925">expiry</span></span> 
- <span data-ttu-id="32d8c-1926">fecha de expiracion</span><span class="sxs-lookup"><span data-stu-id="32d8c-1926">fecha de expiracion</span></span> 
- <span data-ttu-id="32d8c-1927">fecha de venc</span><span class="sxs-lookup"><span data-stu-id="32d8c-1927">fecha de venc</span></span> 
- <span data-ttu-id="32d8c-1928">gultig bis</span><span class="sxs-lookup"><span data-stu-id="32d8c-1928">gultig bis</span></span> 
- <span data-ttu-id="32d8c-1929">gultigkeitsdatum</span><span class="sxs-lookup"><span data-stu-id="32d8c-1929">gultigkeitsdatum</span></span> 
- <span data-ttu-id="32d8c-1930">gültig bis</span><span class="sxs-lookup"><span data-stu-id="32d8c-1930">gültig bis</span></span> 
- <span data-ttu-id="32d8c-1931">gültigkeitsdatum</span><span class="sxs-lookup"><span data-stu-id="32d8c-1931">gültigkeitsdatum</span></span> 
- <span data-ttu-id="32d8c-1932">la scadenza</span><span class="sxs-lookup"><span data-stu-id="32d8c-1932">la scadenza</span></span> 
- <span data-ttu-id="32d8c-1933">scadenza</span><span class="sxs-lookup"><span data-stu-id="32d8c-1933">scadenza</span></span> 
- <span data-ttu-id="32d8c-1934">valable</span><span class="sxs-lookup"><span data-stu-id="32d8c-1934">valable</span></span> 
- <span data-ttu-id="32d8c-1935">validade</span><span class="sxs-lookup"><span data-stu-id="32d8c-1935">validade</span></span> 
- <span data-ttu-id="32d8c-1936">valido hasta</span><span class="sxs-lookup"><span data-stu-id="32d8c-1936">valido hasta</span></span> 
- <span data-ttu-id="32d8c-1937">valorisation</span><span class="sxs-lookup"><span data-stu-id="32d8c-1937">valor</span></span> 
- <span data-ttu-id="32d8c-1938">venc</span><span class="sxs-lookup"><span data-stu-id="32d8c-1938">venc</span></span> 
- <span data-ttu-id="32d8c-1939">vencimento</span><span class="sxs-lookup"><span data-stu-id="32d8c-1939">vencimento</span></span> 
- <span data-ttu-id="32d8c-1940">vencimiento</span><span class="sxs-lookup"><span data-stu-id="32d8c-1940">vencimiento</span></span> 
- <span data-ttu-id="32d8c-1941">verloopt</span><span class="sxs-lookup"><span data-stu-id="32d8c-1941">verloopt</span></span> 
- <span data-ttu-id="32d8c-1942">vervaldag</span><span class="sxs-lookup"><span data-stu-id="32d8c-1942">vervaldag</span></span> 
- <span data-ttu-id="32d8c-1943">vervaldatum</span><span class="sxs-lookup"><span data-stu-id="32d8c-1943">vervaldatum</span></span> 
- <span data-ttu-id="32d8c-1944">vto</span><span class="sxs-lookup"><span data-stu-id="32d8c-1944">vto</span></span> 
- <span data-ttu-id="32d8c-1945">válido hasta</span><span class="sxs-lookup"><span data-stu-id="32d8c-1945">válido hasta</span></span> 
   
## <a name="eu-drivers-license-number"></a><span data-ttu-id="32d8c-1946">Numéro de permis de conduire de l’UE</span><span class="sxs-lookup"><span data-stu-id="32d8c-1946">EU Driver's License Number</span></span>

<span data-ttu-id="32d8c-1947">Pour en savoir plus, consultez [la rubrique informations sensibles sur le numéro de permis de conduire du pilote de l’UE](eu-driver-s-license-number.md).</span><span class="sxs-lookup"><span data-stu-id="32d8c-1947">To learn more, see [EU Driver's License Number sensitive information type](eu-driver-s-license-number.md).</span></span>
  
## <a name="eu-national-identification-number"></a><span data-ttu-id="32d8c-1948">Numéro d’identification nationale de l’UE</span><span class="sxs-lookup"><span data-stu-id="32d8c-1948">EU National Identification Number</span></span>

<span data-ttu-id="32d8c-1949">Pour en savoir plus, consultez la rubrique [informations sensibles du numéro d’identification national](eu-national-identification-number.md)de l’UE.</span><span class="sxs-lookup"><span data-stu-id="32d8c-1949">To learn more, see [EU National Identification Number sensitive information type](eu-national-identification-number.md).</span></span>
  
## <a name="eu-passport-number"></a><span data-ttu-id="32d8c-1950">Numéro de passeport UE</span><span class="sxs-lookup"><span data-stu-id="32d8c-1950">EU Passport Number</span></span>

<span data-ttu-id="32d8c-1951">Pour en savoir plus, consultez la rubrique [type d’informations sensibles du numéro de passeport européen](eu-passport-number.md).</span><span class="sxs-lookup"><span data-stu-id="32d8c-1951">To learn more, see [EU Passport Number sensitive information type](eu-passport-number.md).</span></span>
  
## <a name="eu-social-security-number-or-equivalent-id"></a><span data-ttu-id="32d8c-1952">Numéro de sécurité sociale de l’UE ou ID équivalent</span><span class="sxs-lookup"><span data-stu-id="32d8c-1952">EU Social Security Number or Equivalent ID</span></span>

<span data-ttu-id="32d8c-1953">Pour en savoir plus, consultez la rubrique [numéro de sécurité sociale de l’UE ou type d’informations sensibles ID équivalent](eu-social-security-number-or-equivalent-id.md).</span><span class="sxs-lookup"><span data-stu-id="32d8c-1953">To learn more, see [EU Social Security Number or Equivalent ID sensitive information type](eu-social-security-number-or-equivalent-id.md).</span></span>
  
## <a name="eu-tax-identification-number"></a><span data-ttu-id="32d8c-1954">Numéro d’identification fiscale de l’UE</span><span class="sxs-lookup"><span data-stu-id="32d8c-1954">EU Tax Identification Number</span></span>

<span data-ttu-id="32d8c-1955">Pour en savoir plus, consultez la rubrique [euro Tax identification number sensitive type information](eu-tax-identification-number.md).</span><span class="sxs-lookup"><span data-stu-id="32d8c-1955">To learn more, see [EU Tax Identification Number sensitive information type](eu-tax-identification-number.md).</span></span>
  
## <a name="finland-national-id"></a><span data-ttu-id="32d8c-1956">ID national finlandais</span><span class="sxs-lookup"><span data-stu-id="32d8c-1956">Finland National ID</span></span>

### <a name="format"></a><span data-ttu-id="32d8c-1957">Format</span><span class="sxs-lookup"><span data-stu-id="32d8c-1957">Format</span></span>

<span data-ttu-id="32d8c-1958">Six chiffres plus un caractère indiquant un siècle plus trois chiffres plus un chiffre de contrôle</span><span class="sxs-lookup"><span data-stu-id="32d8c-1958">Six digits plus a character indicating a century plus three digits plus a check digit</span></span>

### <a name="pattern"></a><span data-ttu-id="32d8c-1959">Modèle</span><span class="sxs-lookup"><span data-stu-id="32d8c-1959">Pattern</span></span>

<span data-ttu-id="32d8c-1960">Le modèle doit inclure tous les éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="32d8c-1960">Pattern must include all of the following:</span></span>
- <span data-ttu-id="32d8c-1961">Six chiffres au format JJMMAA qui représentent la date de naissance</span><span class="sxs-lookup"><span data-stu-id="32d8c-1961">Six digits in the format format DDMMYY which are a date of birth</span></span> 
- <span data-ttu-id="32d8c-1962">Marqueur de siècle (soit « - », « + » ou « a »)</span><span class="sxs-lookup"><span data-stu-id="32d8c-1962">Century marker (either '-', '+' or 'a')</span></span> 
- <span data-ttu-id="32d8c-1963">Numéro d’identification personnel à trois chiffres</span><span class="sxs-lookup"><span data-stu-id="32d8c-1963">Three-digit personal identification number</span></span> 
- <span data-ttu-id="32d8c-1964">Un chiffre ou une lettre (ne respectant pas la casse) de contrôle</span><span class="sxs-lookup"><span data-stu-id="32d8c-1964">A digit or letter (case insensitive) which is a check digit</span></span>

### <a name="checksum"></a><span data-ttu-id="32d8c-1965">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="32d8c-1965">Checksum</span></span>

<span data-ttu-id="32d8c-1966">Oui</span><span class="sxs-lookup"><span data-stu-id="32d8c-1966">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="32d8c-1967">Définition</span><span class="sxs-lookup"><span data-stu-id="32d8c-1967">Definition</span></span>

<span data-ttu-id="32d8c-1968">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="32d8c-1968">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="32d8c-1969">La fonction Func_finnish_national_id trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="32d8c-1969">The function Func_finnish_national_id finds content that matches the pattern.</span></span>
- <span data-ttu-id="32d8c-1970">Un mot clé figurant dans la liste Keyword_finnish_national_id est trouvé.</span><span class="sxs-lookup"><span data-stu-id="32d8c-1970">A keyword from Keyword_finnish_national_id is found.</span></span>
- <span data-ttu-id="32d8c-1971">La somme de contrôle est correcte.</span><span class="sxs-lookup"><span data-stu-id="32d8c-1971">The checksum passes.</span></span>

```xml
<!-- Finnish National ID-->
<Entity id="338FD995-4CB5-4F87-AD35-79BD1DD926C1" patternsProximity="300" recommendedConfidence="85">
  <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_finnish_national_id" />
          <Match idRef="Keyword_finnish_national_id" />
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="32d8c-1972">Mots clés</span><span class="sxs-lookup"><span data-stu-id="32d8c-1972">Keywords</span></span>

- <span data-ttu-id="32d8c-1973">Keyword_finnish_national_id</span><span class="sxs-lookup"><span data-stu-id="32d8c-1973">Keyword_finnish_national_id</span></span>
- <span data-ttu-id="32d8c-1974">Sosiaaliturvatunnus</span><span class="sxs-lookup"><span data-stu-id="32d8c-1974">Sosiaaliturvatunnus</span></span>
- <span data-ttu-id="32d8c-1975">SOTU Henkilötunnus HETU</span><span class="sxs-lookup"><span data-stu-id="32d8c-1975">SOTU Henkilötunnus HETU</span></span>
- <span data-ttu-id="32d8c-1976">Personbeteckning</span><span class="sxs-lookup"><span data-stu-id="32d8c-1976">Personbeteckning</span></span>
- <span data-ttu-id="32d8c-1977">Personnummer</span><span class="sxs-lookup"><span data-stu-id="32d8c-1977">Personnummer</span></span>
   
## <a name="finland-passport-number"></a><span data-ttu-id="32d8c-1978">Numéro de passeport Finlande</span><span class="sxs-lookup"><span data-stu-id="32d8c-1978">Finland Passport Number</span></span>

### <a name="format"></a><span data-ttu-id="32d8c-1979">Format</span><span class="sxs-lookup"><span data-stu-id="32d8c-1979">Format</span></span>
<span data-ttu-id="32d8c-1980">Combinaison de neuf lettres et chiffres</span><span class="sxs-lookup"><span data-stu-id="32d8c-1980">Combination of nine letters and digits</span></span>

### <a name="pattern"></a><span data-ttu-id="32d8c-1981">Modèle</span><span class="sxs-lookup"><span data-stu-id="32d8c-1981">Pattern</span></span>
<span data-ttu-id="32d8c-1982">Combinaison de neuf lettres et chiffres : deux lettres (ne respectant pas la casse) sept chiffres</span><span class="sxs-lookup"><span data-stu-id="32d8c-1982">Combination of nine letters and digits: Two letters (not case sensitive) Seven digits</span></span>

### <a name="checksum"></a><span data-ttu-id="32d8c-1983">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="32d8c-1983">Checksum</span></span>
<span data-ttu-id="32d8c-1984">Non</span><span class="sxs-lookup"><span data-stu-id="32d8c-1984">No</span></span>

### <a name="definition"></a><span data-ttu-id="32d8c-1985">Définition</span><span class="sxs-lookup"><span data-stu-id="32d8c-1985">Definition</span></span>
<span data-ttu-id="32d8c-1986">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="32d8c-1986">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="32d8c-1987">L’expression régulière Regex_finland_passport_number trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="32d8c-1987">The regular expression Regex_finland_passport_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="32d8c-1988">Un mot clé figurant dans la liste Keyword_finland_passport_number est trouvé.</span><span class="sxs-lookup"><span data-stu-id="32d8c-1988">A keyword from Keyword_finland_passport_number is found.</span></span>
<!-- Finland Passport Number -->
```xml
<Entity id="d1685ac3-1d3a-40f8-8198-32ef5669c7a5" recommendedConfidence="75" patternsProximity="300">
  <Pattern confidenceLevel="75">
     <IdMatch idRef="Regex_finland_passport_number"/>
     <Match idRef="Keyword_finland_passport_number"/>
  </Pattern>
</Entity>
```
### <a name="keywords"></a><span data-ttu-id="32d8c-1989">Mots clés</span><span class="sxs-lookup"><span data-stu-id="32d8c-1989">Keywords</span></span>
- <span data-ttu-id="32d8c-1990">Keyword_finland_passport_number</span><span class="sxs-lookup"><span data-stu-id="32d8c-1990">Keyword_finland_passport_number</span></span>
- <span data-ttu-id="32d8c-1991">Tel</span><span class="sxs-lookup"><span data-stu-id="32d8c-1991">Passport</span></span>
- <span data-ttu-id="32d8c-1992">Transfert</span><span class="sxs-lookup"><span data-stu-id="32d8c-1992">Passi</span></span>
   
## <a name="france-drivers-license-number"></a><span data-ttu-id="32d8c-1993">Numéro de permis de conduire France</span><span class="sxs-lookup"><span data-stu-id="32d8c-1993">France Driver's License Number</span></span>

### <a name="format"></a><span data-ttu-id="32d8c-1994">Format</span><span class="sxs-lookup"><span data-stu-id="32d8c-1994">Format</span></span>

<span data-ttu-id="32d8c-1995">12 chiffres</span><span class="sxs-lookup"><span data-stu-id="32d8c-1995">12 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="32d8c-1996">Modèle</span><span class="sxs-lookup"><span data-stu-id="32d8c-1996">Pattern</span></span>

<span data-ttu-id="32d8c-1997">12 chiffres avec validation pour écarter les modèles similaires, comme les numéros de téléphone français</span><span class="sxs-lookup"><span data-stu-id="32d8c-1997">12 digits with validation to discount similar patterns such as French telephone numbers</span></span>

### <a name="checksum"></a><span data-ttu-id="32d8c-1998">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="32d8c-1998">Checksum</span></span>

<span data-ttu-id="32d8c-1999">Non</span><span class="sxs-lookup"><span data-stu-id="32d8c-1999">No</span></span>

### <a name="definition"></a><span data-ttu-id="32d8c-2000">Définition</span><span class="sxs-lookup"><span data-stu-id="32d8c-2000">Definition</span></span>

<span data-ttu-id="32d8c-2001">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="32d8c-2001">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="32d8c-2002">La fonction Func_french_drivers_license trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="32d8c-2002">The function Func_french_drivers_license finds content that matches the pattern.</span></span>
- <span data-ttu-id="32d8c-2003">Au moins une des affirmations suivantes est vraie :</span><span class="sxs-lookup"><span data-stu-id="32d8c-2003">At least one of the following is true:</span></span>
- <span data-ttu-id="32d8c-2004">Un mot clé figurant dans la liste Keyword_french_drivers_license est trouvé.</span><span class="sxs-lookup"><span data-stu-id="32d8c-2004">A keyword from Keyword_french_drivers_license is found.</span></span>
- <span data-ttu-id="32d8c-2005">La fonction Func_eu_date trouve une date au format correct.</span><span class="sxs-lookup"><span data-stu-id="32d8c-2005">The function Func_eu_date finds a date in the right date format.</span></span>

```xml
<!-- France Driver's License Number -->
<Entity id="18e55a36-a01b-4b0f-943d-dc10282a1824" patternsProximity="300" recommendedConfidence="75">
  <Pattern confidenceLevel="75">
        <IdMatch idRef="Func_french_drivers_license" />
        <Any minMatches="1">
          <Match idRef="Keyword_french_drivers_license" />
          <Match idRef="Func_eu_date" />
        </Any>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="32d8c-2006">Mots clés</span><span class="sxs-lookup"><span data-stu-id="32d8c-2006">Keywords</span></span>

#### <a name="keyword_french_drivers_license"></a><span data-ttu-id="32d8c-2007">Keyword_french_drivers_license</span><span class="sxs-lookup"><span data-stu-id="32d8c-2007">Keyword_french_drivers_license</span></span>

- <span data-ttu-id="32d8c-2008">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="32d8c-2008">drivers licence</span></span>
- <span data-ttu-id="32d8c-2009">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="32d8c-2009">drivers license</span></span>
- <span data-ttu-id="32d8c-2010">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="32d8c-2010">driving licence</span></span>
- <span data-ttu-id="32d8c-2011">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="32d8c-2011">driving license</span></span>
- <span data-ttu-id="32d8c-2012">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="32d8c-2012">permis de conduire</span></span>
- <span data-ttu-id="32d8c-2013">numéro de permis</span><span class="sxs-lookup"><span data-stu-id="32d8c-2013">licence number</span></span>
- <span data-ttu-id="32d8c-2014">numéro de permis</span><span class="sxs-lookup"><span data-stu-id="32d8c-2014">license number</span></span>
- <span data-ttu-id="32d8c-2015">numéros de permis</span><span class="sxs-lookup"><span data-stu-id="32d8c-2015">licence numbers</span></span>
- <span data-ttu-id="32d8c-2016">numéros de permis</span><span class="sxs-lookup"><span data-stu-id="32d8c-2016">license numbers</span></span>

## <a name="france-national-id-card-cni"></a><span data-ttu-id="32d8c-2017">Carte nationale d’identité (CNI) France</span><span class="sxs-lookup"><span data-stu-id="32d8c-2017">France National ID Card (CNI)</span></span>

### <a name="format"></a><span data-ttu-id="32d8c-2018">Format</span><span class="sxs-lookup"><span data-stu-id="32d8c-2018">Format</span></span>

<span data-ttu-id="32d8c-2019">12 chiffres</span><span class="sxs-lookup"><span data-stu-id="32d8c-2019">12 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="32d8c-2020">Modèle</span><span class="sxs-lookup"><span data-stu-id="32d8c-2020">Pattern</span></span>

<span data-ttu-id="32d8c-2021">12 chiffres</span><span class="sxs-lookup"><span data-stu-id="32d8c-2021">12 digits</span></span>

### <a name="checksum"></a><span data-ttu-id="32d8c-2022">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="32d8c-2022">Checksum</span></span>

<span data-ttu-id="32d8c-2023">Non</span><span class="sxs-lookup"><span data-stu-id="32d8c-2023">No</span></span>

### <a name="definition"></a><span data-ttu-id="32d8c-2024">Définition</span><span class="sxs-lookup"><span data-stu-id="32d8c-2024">Definition</span></span>

<span data-ttu-id="32d8c-2025">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 65 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="32d8c-2025">A DLP policy is 65% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="32d8c-2026">L’expression régulière Regex_france_cni trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="32d8c-2026">The regular expression Regex_france_cni finds content that matches the pattern.</span></span>

```xml
<!-- France CNI -->
<Entity id="f741ac74-1bc0-4665-b69b-f0c7f927c0c4" patternsProximity="300" recommendedConfidence="65">
  <Pattern confidenceLevel="65">
        <IdMatch idRef="Regex_france_cni" />
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="32d8c-2027">Mots clés</span><span class="sxs-lookup"><span data-stu-id="32d8c-2027">Keywords</span></span>

<span data-ttu-id="32d8c-2028">Aucun</span><span class="sxs-lookup"><span data-stu-id="32d8c-2028">None</span></span>
   
## <a name="france-passport-number"></a><span data-ttu-id="32d8c-2029">Numéro de passeport France</span><span class="sxs-lookup"><span data-stu-id="32d8c-2029">France Passport Number</span></span>

### <a name="format"></a><span data-ttu-id="32d8c-2030">Format</span><span class="sxs-lookup"><span data-stu-id="32d8c-2030">Format</span></span>

<span data-ttu-id="32d8c-2031">Neuf chiffres et lettres</span><span class="sxs-lookup"><span data-stu-id="32d8c-2031">Nine digits and letters</span></span>

### <a name="pattern"></a><span data-ttu-id="32d8c-2032">Modèle</span><span class="sxs-lookup"><span data-stu-id="32d8c-2032">Pattern</span></span>

<span data-ttu-id="32d8c-2033">Neuf chiffres et lettres :</span><span class="sxs-lookup"><span data-stu-id="32d8c-2033">Nine digits and letters:</span></span>
- <span data-ttu-id="32d8c-2034">Deux chiffres</span><span class="sxs-lookup"><span data-stu-id="32d8c-2034">Two digits</span></span> 
- <span data-ttu-id="32d8c-2035">Deux lettres (ne respectent pas la casse)</span><span class="sxs-lookup"><span data-stu-id="32d8c-2035">Two letters (not case sensitive)</span></span> 
- <span data-ttu-id="32d8c-2036">Cinq chiffres</span><span class="sxs-lookup"><span data-stu-id="32d8c-2036">Five digits</span></span>

### <a name="checksum"></a><span data-ttu-id="32d8c-2037">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="32d8c-2037">Checksum</span></span>

<span data-ttu-id="32d8c-2038">Non</span><span class="sxs-lookup"><span data-stu-id="32d8c-2038">No</span></span>

### <a name="definition"></a><span data-ttu-id="32d8c-2039">Définition</span><span class="sxs-lookup"><span data-stu-id="32d8c-2039">Definition</span></span>

<span data-ttu-id="32d8c-2040">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="32d8c-2040">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="32d8c-2041">La fonction Func_fr_passport trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="32d8c-2041">The function Func_fr_passport finds content that matches the pattern.</span></span>
- <span data-ttu-id="32d8c-2042">Un mot clé figurant dans la liste Keyword_passport est trouvé.</span><span class="sxs-lookup"><span data-stu-id="32d8c-2042">A keyword from Keyword_passport is found.</span></span>

```xml
<!-- France Passport Number -->
<Entity id="3008b884-8c8c-4cd8-a289-99f34fc7ff5d" patternsProximity="300" recommendedConfidence="75">
  <Pattern confidenceLevel="75">
        <IdMatch idRef="Func_fr_passport" />
        <Match idRef="Keyword_passport" />
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="32d8c-2043">Mots clés</span><span class="sxs-lookup"><span data-stu-id="32d8c-2043">Keywords</span></span>

#### <a name="keyword_passport"></a><span data-ttu-id="32d8c-2044">Keyword_passport</span><span class="sxs-lookup"><span data-stu-id="32d8c-2044">Keyword_passport</span></span>

- <span data-ttu-id="32d8c-2045">Numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="32d8c-2045">Passport Number</span></span>
- <span data-ttu-id="32d8c-2046">N° de passeport</span><span class="sxs-lookup"><span data-stu-id="32d8c-2046">Passport No</span></span>
- <span data-ttu-id="32d8c-2047"># Passeport</span><span class="sxs-lookup"><span data-stu-id="32d8c-2047">Passport #</span></span>
- <span data-ttu-id="32d8c-2048">Tel #</span><span class="sxs-lookup"><span data-stu-id="32d8c-2048">Passport#</span></span>
- <span data-ttu-id="32d8c-2049">PassportID</span><span class="sxs-lookup"><span data-stu-id="32d8c-2049">PassportID</span></span>
- <span data-ttu-id="32d8c-2050">N ° passeport</span><span class="sxs-lookup"><span data-stu-id="32d8c-2050">Passportno</span></span>
- <span data-ttu-id="32d8c-2051">passportnumber</span><span class="sxs-lookup"><span data-stu-id="32d8c-2051">passportnumber</span></span>
- <span data-ttu-id="32d8c-2052">パスポート</span><span class="sxs-lookup"><span data-stu-id="32d8c-2052">パスポート</span></span>
- <span data-ttu-id="32d8c-2053">パスポート番号</span><span class="sxs-lookup"><span data-stu-id="32d8c-2053">パスポート番号</span></span>
- <span data-ttu-id="32d8c-2054">パスポートのNum</span><span class="sxs-lookup"><span data-stu-id="32d8c-2054">パスポートのNum</span></span>
- <span data-ttu-id="32d8c-2055">パスポート＃</span><span class="sxs-lookup"><span data-stu-id="32d8c-2055">パスポート ＃</span></span> 
- <span data-ttu-id="32d8c-2056">Numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="32d8c-2056">Numéro de passeport</span></span>
- <span data-ttu-id="32d8c-2057">Passeport n°</span><span class="sxs-lookup"><span data-stu-id="32d8c-2057">Passeport n °</span></span>
- <span data-ttu-id="32d8c-2058">Passeport numéro</span><span class="sxs-lookup"><span data-stu-id="32d8c-2058">Passeport Non</span></span>
- <span data-ttu-id="32d8c-2059"># Passeport</span><span class="sxs-lookup"><span data-stu-id="32d8c-2059">Passeport #</span></span>
- <span data-ttu-id="32d8c-2060">Passeport #</span><span class="sxs-lookup"><span data-stu-id="32d8c-2060">Passeport#</span></span>
- <span data-ttu-id="32d8c-2061">PasseportNon</span><span class="sxs-lookup"><span data-stu-id="32d8c-2061">PasseportNon</span></span>
- <span data-ttu-id="32d8c-2062">Passeportn °</span><span class="sxs-lookup"><span data-stu-id="32d8c-2062">Passeportn °</span></span>

      
## <a name="france-social-security-number-insee"></a><span data-ttu-id="32d8c-2063">Numéro de sécurité sociale (INSEE) France</span><span class="sxs-lookup"><span data-stu-id="32d8c-2063">France Social Security Number (INSEE)</span></span>

### <a name="format"></a><span data-ttu-id="32d8c-2064">Format</span><span class="sxs-lookup"><span data-stu-id="32d8c-2064">Format</span></span>

<span data-ttu-id="32d8c-2065">15 chiffres</span><span class="sxs-lookup"><span data-stu-id="32d8c-2065">15 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="32d8c-2066">Modèle</span><span class="sxs-lookup"><span data-stu-id="32d8c-2066">Pattern</span></span>

<span data-ttu-id="32d8c-2067">Doit correspondre à l’un des deux modèles suivants :</span><span class="sxs-lookup"><span data-stu-id="32d8c-2067">Must match one of two patterns:</span></span>
- <span data-ttu-id="32d8c-2068">13 chiffres suivis d’un espace suivi de deux chiffres</span><span class="sxs-lookup"><span data-stu-id="32d8c-2068">13 digits followed by a space followed by two digits</span></span><br/>
<span data-ttu-id="32d8c-2069">ou</span><span class="sxs-lookup"><span data-stu-id="32d8c-2069">or</span></span>
- <span data-ttu-id="32d8c-2070">15 chiffres consécutifs</span><span class="sxs-lookup"><span data-stu-id="32d8c-2070">15 consecutive digits</span></span>

### <a name="checksum"></a><span data-ttu-id="32d8c-2071">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="32d8c-2071">Checksum</span></span>

<span data-ttu-id="32d8c-2072">Oui</span><span class="sxs-lookup"><span data-stu-id="32d8c-2072">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="32d8c-2073">Définition</span><span class="sxs-lookup"><span data-stu-id="32d8c-2073">Definition</span></span>

<span data-ttu-id="32d8c-2074">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 95 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="32d8c-2074">A DLP policy is 95% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="32d8c-2075">La fonction Func_french_insee ou Func_fr_insee trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="32d8c-2075">The function Func_french_insee or Func_fr_insee finds content that matches the pattern.</span></span>
- <span data-ttu-id="32d8c-2076">Un mot clé figurant dans la liste Keyword_fr_insee est trouvé.</span><span class="sxs-lookup"><span data-stu-id="32d8c-2076">A keyword from Keyword_fr_insee is found.</span></span>
- <span data-ttu-id="32d8c-2077">La somme de contrôle est correcte.</span><span class="sxs-lookup"><span data-stu-id="32d8c-2077">The checksum passes.</span></span>

<span data-ttu-id="32d8c-2078">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="32d8c-2078">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="32d8c-2079">La fonction Func_french_insee ou Func_fr_insee trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="32d8c-2079">The function Func_french_insee or Func_fr_insee finds content that matches the pattern.</span></span>
- <span data-ttu-id="32d8c-2080">Aucun mot clé figurant dans la liste Keyword_fr_insee n’est trouvé.</span><span class="sxs-lookup"><span data-stu-id="32d8c-2080">No keyword from Keyword_fr_insee is found.</span></span>
- <span data-ttu-id="32d8c-2081">La somme de contrôle est correcte.</span><span class="sxs-lookup"><span data-stu-id="32d8c-2081">The checksum passes.</span></span>

```xml
<!-- France INSEE -->
<Entity id="71f62b97-efe0-4aa1-aa49-e14de253619d" patternsProximity="300" recommendedConfidence="85">
  <Pattern confidenceLevel="95">
        <IdMatch idRef="Func_french_insee" />
        <Match idRef="Func_fr_insee" />
        <Any minMatches="1">
          <Match idRef="Keyword_fr_insee" />
        </Any>
  </Pattern>
  <Pattern confidenceLevel="85">
        <IdMatch idRef="Func_french_insee" />
        <Match idRef="Func_fr_insee" />
        <Any minMatches="0" maxMatches="0">
          <Match idRef="Keyword_fr_insee" />
        </Any>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="32d8c-2082">Mots clés</span><span class="sxs-lookup"><span data-stu-id="32d8c-2082">Keywords</span></span>

#### <a name="keyword_fr_insee"></a><span data-ttu-id="32d8c-2083">Keyword_fr_insee</span><span class="sxs-lookup"><span data-stu-id="32d8c-2083">Keyword_fr_insee</span></span>

- <span data-ttu-id="32d8c-2084">INSEE</span><span class="sxs-lookup"><span data-stu-id="32d8c-2084">insee</span></span>
- <span data-ttu-id="32d8c-2085">securité sociale</span><span class="sxs-lookup"><span data-stu-id="32d8c-2085">securité sociale</span></span>
- <span data-ttu-id="32d8c-2086">securite sociale</span><span class="sxs-lookup"><span data-stu-id="32d8c-2086">securite sociale</span></span>
- <span data-ttu-id="32d8c-2087">id national</span><span class="sxs-lookup"><span data-stu-id="32d8c-2087">national id</span></span>
- <span data-ttu-id="32d8c-2088">numéro d’identification nationale</span><span class="sxs-lookup"><span data-stu-id="32d8c-2088">national identification</span></span>
- <span data-ttu-id="32d8c-2089">numéro d’identité</span><span class="sxs-lookup"><span data-stu-id="32d8c-2089">numéro d'identité</span></span>
- <span data-ttu-id="32d8c-2090">n° d’identité</span><span class="sxs-lookup"><span data-stu-id="32d8c-2090">no d'identité</span></span>
- <span data-ttu-id="32d8c-2091">Nbre.</span><span class="sxs-lookup"><span data-stu-id="32d8c-2091">no.</span></span> <span data-ttu-id="32d8c-2092">d’identité</span><span class="sxs-lookup"><span data-stu-id="32d8c-2092">d'identité</span></span>
- <span data-ttu-id="32d8c-2093">numéro d’identité</span><span class="sxs-lookup"><span data-stu-id="32d8c-2093">numero d'identite</span></span>
- <span data-ttu-id="32d8c-2094">n° d’identité</span><span class="sxs-lookup"><span data-stu-id="32d8c-2094">no d'identite</span></span>
- <span data-ttu-id="32d8c-2095">Nbre.</span><span class="sxs-lookup"><span data-stu-id="32d8c-2095">no.</span></span> <span data-ttu-id="32d8c-2096">d’identite</span><span class="sxs-lookup"><span data-stu-id="32d8c-2096">d'identite</span></span>
- <span data-ttu-id="32d8c-2097">numéro de sécurité sociale</span><span class="sxs-lookup"><span data-stu-id="32d8c-2097">social security number</span></span>
- <span data-ttu-id="32d8c-2098">code de sécurité sociale</span><span class="sxs-lookup"><span data-stu-id="32d8c-2098">social security code</span></span>
- <span data-ttu-id="32d8c-2099">numéro d’assurance sociale</span><span class="sxs-lookup"><span data-stu-id="32d8c-2099">social insurance number</span></span>
- <span data-ttu-id="32d8c-2100">le numéro d’identification nationale</span><span class="sxs-lookup"><span data-stu-id="32d8c-2100">le numéro d'identification nationale</span></span>
- <span data-ttu-id="32d8c-2101">d’identité nationale</span><span class="sxs-lookup"><span data-stu-id="32d8c-2101">d'identité nationale</span></span>
- <span data-ttu-id="32d8c-2102">numéro de sécurité sociale</span><span class="sxs-lookup"><span data-stu-id="32d8c-2102">numéro de sécurité sociale</span></span>
- <span data-ttu-id="32d8c-2103">le code de la sécurité sociale</span><span class="sxs-lookup"><span data-stu-id="32d8c-2103">le code de la sécurité sociale</span></span>
- <span data-ttu-id="32d8c-2104">numéro d’assurance sociale</span><span class="sxs-lookup"><span data-stu-id="32d8c-2104">numéro d'assurance sociale</span></span>
- <span data-ttu-id="32d8c-2105">numéro de sécu</span><span class="sxs-lookup"><span data-stu-id="32d8c-2105">numéro de sécu</span></span>
- <span data-ttu-id="32d8c-2106">code sécu</span><span class="sxs-lookup"><span data-stu-id="32d8c-2106">code sécu</span></span> 
   
## <a name="german-drivers-license-number"></a><span data-ttu-id="32d8c-2107">Numéro de permis de conduire Allemagne</span><span class="sxs-lookup"><span data-stu-id="32d8c-2107">German Driver's License Number</span></span>

### <a name="format"></a><span data-ttu-id="32d8c-2108">Format</span><span class="sxs-lookup"><span data-stu-id="32d8c-2108">Format</span></span>

<span data-ttu-id="32d8c-2109">Combinaison de 11 chiffres et lettres</span><span class="sxs-lookup"><span data-stu-id="32d8c-2109">Combination of 11 digits and letters</span></span>

### <a name="pattern"></a><span data-ttu-id="32d8c-2110">Modèle</span><span class="sxs-lookup"><span data-stu-id="32d8c-2110">Pattern</span></span>

<span data-ttu-id="32d8c-2111">11 chiffres et lettres (ne respectent pas la casse) :</span><span class="sxs-lookup"><span data-stu-id="32d8c-2111">11 digits and letters (not case sensitive):</span></span>
- <span data-ttu-id="32d8c-2112">Un chiffre ou une lettre</span><span class="sxs-lookup"><span data-stu-id="32d8c-2112">A digit or letter</span></span> 
- <span data-ttu-id="32d8c-2113">Deux chiffres</span><span class="sxs-lookup"><span data-stu-id="32d8c-2113">Two digits</span></span> 
- <span data-ttu-id="32d8c-2114">Six chiffres ou lettres</span><span class="sxs-lookup"><span data-stu-id="32d8c-2114">Six digits or letters</span></span> 
- <span data-ttu-id="32d8c-2115">Un chiffre</span><span class="sxs-lookup"><span data-stu-id="32d8c-2115">A digit</span></span> 
- <span data-ttu-id="32d8c-2116">Un chiffre ou une lettre</span><span class="sxs-lookup"><span data-stu-id="32d8c-2116">A digit or letter</span></span>

### <a name="checksum"></a><span data-ttu-id="32d8c-2117">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="32d8c-2117">Checksum</span></span>

<span data-ttu-id="32d8c-2118">Oui</span><span class="sxs-lookup"><span data-stu-id="32d8c-2118">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="32d8c-2119">Définition</span><span class="sxs-lookup"><span data-stu-id="32d8c-2119">Definition</span></span>

<span data-ttu-id="32d8c-2120">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="32d8c-2120">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="32d8c-2121">La fonction Func_german_drivers_license trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="32d8c-2121">The function Func_german_drivers_license finds content that matches the pattern.</span></span>
- <span data-ttu-id="32d8c-2122">Au moins une des affirmations suivantes est vraie :</span><span class="sxs-lookup"><span data-stu-id="32d8c-2122">At least one of the following is true:</span></span>
    - <span data-ttu-id="32d8c-2123">Un mot clé figurant dans la liste Keyword_german_drivers_license_number est trouvé.</span><span class="sxs-lookup"><span data-stu-id="32d8c-2123">A keyword from Keyword_german_drivers_license_number is found.</span></span>
    - <span data-ttu-id="32d8c-2124">Un mot clé figurant dans la liste Keyword_german_drivers_license_collaborative est trouvé.</span><span class="sxs-lookup"><span data-stu-id="32d8c-2124">A keyword from Keyword_german_drivers_license_collaborative is found.</span></span>
    - <span data-ttu-id="32d8c-2125">Un mot clé figurant dans la liste Keyword_german_drivers_license est trouvé.</span><span class="sxs-lookup"><span data-stu-id="32d8c-2125">A keyword from Keyword_german_drivers_license is found.</span></span>
- <span data-ttu-id="32d8c-2126">La somme de contrôle est correcte.</span><span class="sxs-lookup"><span data-stu-id="32d8c-2126">The checksum passes.</span></span>

```xml
<!-- German Driver's License Number -->
<Entity id="91da9335-1edb-45b7-a95f-5fe41a16c63c" patternsProximity="300" recommendedConfidence="75">
  <Pattern confidenceLevel="75">
        <IdMatch idRef="Func_german_drivers_license" />
        <Any minMatches="1">
          <Match idRef="Keyword_german_drivers_license_number" />
          <Match idRef="Keyword_german_drivers_license_collaborative" />
          <Match idRef="Keyword_german_drivers_license" />
        </Any>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="32d8c-2127">Mots clés</span><span class="sxs-lookup"><span data-stu-id="32d8c-2127">Keywords</span></span>

#### <a name="keyword_german_drivers_license_number"></a><span data-ttu-id="32d8c-2128">Keyword_german_drivers_license_number</span><span class="sxs-lookup"><span data-stu-id="32d8c-2128">Keyword_german_drivers_license_number</span></span>

- <span data-ttu-id="32d8c-2129">Führerschein</span><span class="sxs-lookup"><span data-stu-id="32d8c-2129">Führerschein</span></span>
- <span data-ttu-id="32d8c-2130">Fuhrerschein</span><span class="sxs-lookup"><span data-stu-id="32d8c-2130">Fuhrerschein</span></span>
- <span data-ttu-id="32d8c-2131">Fuehrerschein</span><span class="sxs-lookup"><span data-stu-id="32d8c-2131">Fuehrerschein</span></span>
- <span data-ttu-id="32d8c-2132">Führerscheinnummer</span><span class="sxs-lookup"><span data-stu-id="32d8c-2132">Führerscheinnummer</span></span>
- <span data-ttu-id="32d8c-2133">Fuhrerscheinnummer</span><span class="sxs-lookup"><span data-stu-id="32d8c-2133">Fuhrerscheinnummer</span></span>
- <span data-ttu-id="32d8c-2134">Fuehrerscheinnummer</span><span class="sxs-lookup"><span data-stu-id="32d8c-2134">Fuehrerscheinnummer</span></span>
- <span data-ttu-id="32d8c-2135">Führerschein</span><span class="sxs-lookup"><span data-stu-id="32d8c-2135">Führerschein-</span></span> 
- <span data-ttu-id="32d8c-2136">Fuhrerschein</span><span class="sxs-lookup"><span data-stu-id="32d8c-2136">Fuhrerschein-</span></span> 
- <span data-ttu-id="32d8c-2137">Fuehrerschein</span><span class="sxs-lookup"><span data-stu-id="32d8c-2137">Fuehrerschein-</span></span> 
- <span data-ttu-id="32d8c-2138">FührerscheinnummerNr</span><span class="sxs-lookup"><span data-stu-id="32d8c-2138">FührerscheinnummerNr</span></span>
- <span data-ttu-id="32d8c-2139">FuhrerscheinnummerNr</span><span class="sxs-lookup"><span data-stu-id="32d8c-2139">FuhrerscheinnummerNr</span></span>
- <span data-ttu-id="32d8c-2140">FuehrerscheinnummerNr</span><span class="sxs-lookup"><span data-stu-id="32d8c-2140">FuehrerscheinnummerNr</span></span>
- <span data-ttu-id="32d8c-2141">FührerscheinnummerKlasse</span><span class="sxs-lookup"><span data-stu-id="32d8c-2141">FührerscheinnummerKlasse</span></span>
- <span data-ttu-id="32d8c-2142">FuhrerscheinnummerKlasse</span><span class="sxs-lookup"><span data-stu-id="32d8c-2142">FuhrerscheinnummerKlasse</span></span>
- <span data-ttu-id="32d8c-2143">FuehrerscheinnummerKlasse</span><span class="sxs-lookup"><span data-stu-id="32d8c-2143">FuehrerscheinnummerKlasse</span></span>
- <span data-ttu-id="32d8c-2144">Führerschein - Nr</span><span class="sxs-lookup"><span data-stu-id="32d8c-2144">Führerschein- Nr</span></span>
- <span data-ttu-id="32d8c-2145">Fuhrerschein - Nr</span><span class="sxs-lookup"><span data-stu-id="32d8c-2145">Fuhrerschein- Nr</span></span>
- <span data-ttu-id="32d8c-2146">Fuehrerschein - Nr</span><span class="sxs-lookup"><span data-stu-id="32d8c-2146">Fuehrerschein- Nr</span></span> 
- <span data-ttu-id="32d8c-2147">Führerschein - Klasse</span><span class="sxs-lookup"><span data-stu-id="32d8c-2147">Führerschein- Klasse</span></span> 
- <span data-ttu-id="32d8c-2148">Fuhrerschein - Klasse</span><span class="sxs-lookup"><span data-stu-id="32d8c-2148">Fuhrerschein- Klasse</span></span> 
- <span data-ttu-id="32d8c-2149">Fuehrerschein - Klasse</span><span class="sxs-lookup"><span data-stu-id="32d8c-2149">Fuehrerschein- Klasse</span></span>
- <span data-ttu-id="32d8c-2150">FührerscheinnummerNr</span><span class="sxs-lookup"><span data-stu-id="32d8c-2150">FührerscheinnummerNr</span></span> 
- <span data-ttu-id="32d8c-2151">FuhrerscheinnummerNr</span><span class="sxs-lookup"><span data-stu-id="32d8c-2151">FuhrerscheinnummerNr</span></span> 
- <span data-ttu-id="32d8c-2152">FuehrerscheinnummerNr</span><span class="sxs-lookup"><span data-stu-id="32d8c-2152">FuehrerscheinnummerNr</span></span> 
- <span data-ttu-id="32d8c-2153">FührerscheinnummerKlasse</span><span class="sxs-lookup"><span data-stu-id="32d8c-2153">FührerscheinnummerKlasse</span></span> 
- <span data-ttu-id="32d8c-2154">FuhrerscheinnummerKlasse</span><span class="sxs-lookup"><span data-stu-id="32d8c-2154">FuhrerscheinnummerKlasse</span></span> 
- <span data-ttu-id="32d8c-2155">FuehrerscheinnummerKlasse</span><span class="sxs-lookup"><span data-stu-id="32d8c-2155">FuehrerscheinnummerKlasse</span></span> 
- <span data-ttu-id="32d8c-2156">Führerschein - Nr</span><span class="sxs-lookup"><span data-stu-id="32d8c-2156">Führerschein- Nr</span></span> 
- <span data-ttu-id="32d8c-2157">Fuhrerschein - Nr</span><span class="sxs-lookup"><span data-stu-id="32d8c-2157">Fuhrerschein- Nr</span></span> 
- <span data-ttu-id="32d8c-2158">Fuehrerschein - Nr</span><span class="sxs-lookup"><span data-stu-id="32d8c-2158">Fuehrerschein- Nr</span></span> 
- <span data-ttu-id="32d8c-2159">Führerschein - Klasse</span><span class="sxs-lookup"><span data-stu-id="32d8c-2159">Führerschein- Klasse</span></span> 
- <span data-ttu-id="32d8c-2160">Fuhrerschein - Klasse</span><span class="sxs-lookup"><span data-stu-id="32d8c-2160">Fuhrerschein- Klasse</span></span> 
- <span data-ttu-id="32d8c-2161">Fuehrerschein - Klasse</span><span class="sxs-lookup"><span data-stu-id="32d8c-2161">Fuehrerschein- Klasse</span></span> 
- <span data-ttu-id="32d8c-2162">LD</span><span class="sxs-lookup"><span data-stu-id="32d8c-2162">DL</span></span> 
- <span data-ttu-id="32d8c-2163">DISTRIBUTION</span><span class="sxs-lookup"><span data-stu-id="32d8c-2163">DLS</span></span>
- <span data-ttu-id="32d8c-2164">Permis conduire</span><span class="sxs-lookup"><span data-stu-id="32d8c-2164">Driv Lic</span></span> 
- <span data-ttu-id="32d8c-2165">Permis conduire</span><span class="sxs-lookup"><span data-stu-id="32d8c-2165">Driv Licen</span></span> 
- <span data-ttu-id="32d8c-2166">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="32d8c-2166">Driv License</span></span>
- <span data-ttu-id="32d8c-2167">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="32d8c-2167">Driv Licenses</span></span> 
- <span data-ttu-id="32d8c-2168">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="32d8c-2168">Driv Licence</span></span> 
- <span data-ttu-id="32d8c-2169">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="32d8c-2169">Driv Licences</span></span> 
- <span data-ttu-id="32d8c-2170">Permis conduire</span><span class="sxs-lookup"><span data-stu-id="32d8c-2170">Driv Lic</span></span> 
- <span data-ttu-id="32d8c-2171">Permis conduire</span><span class="sxs-lookup"><span data-stu-id="32d8c-2171">Driver Licen</span></span> 
- <span data-ttu-id="32d8c-2172">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="32d8c-2172">Driver License</span></span> 
- <span data-ttu-id="32d8c-2173">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="32d8c-2173">Driver Licenses</span></span> 
- <span data-ttu-id="32d8c-2174">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="32d8c-2174">Driver Licence</span></span> 
- <span data-ttu-id="32d8c-2175">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="32d8c-2175">Driver Licences</span></span> 
- <span data-ttu-id="32d8c-2176">Permis conduire</span><span class="sxs-lookup"><span data-stu-id="32d8c-2176">Drivers Lic</span></span> 
- <span data-ttu-id="32d8c-2177">Permis conduire</span><span class="sxs-lookup"><span data-stu-id="32d8c-2177">Drivers Licen</span></span> 
- <span data-ttu-id="32d8c-2178">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="32d8c-2178">Drivers License</span></span> 
- <span data-ttu-id="32d8c-2179">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="32d8c-2179">Drivers Licenses</span></span> 
- <span data-ttu-id="32d8c-2180">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="32d8c-2180">Drivers Licence</span></span> 
- <span data-ttu-id="32d8c-2181">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="32d8c-2181">Drivers Licences</span></span> 
- <span data-ttu-id="32d8c-2182">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="32d8c-2182">Driver's Lic</span></span> 
- <span data-ttu-id="32d8c-2183">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="32d8c-2183">Driver's Licen</span></span> 
- <span data-ttu-id="32d8c-2184">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="32d8c-2184">Driver's License</span></span> 
- <span data-ttu-id="32d8c-2185">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="32d8c-2185">Driver's Licenses</span></span> 
- <span data-ttu-id="32d8c-2186">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="32d8c-2186">Driver's Licence</span></span> 
- <span data-ttu-id="32d8c-2187">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="32d8c-2187">Driver's Licences</span></span> 
- <span data-ttu-id="32d8c-2188">Permis conduire</span><span class="sxs-lookup"><span data-stu-id="32d8c-2188">Driving Lic</span></span> 
- <span data-ttu-id="32d8c-2189">Permis conduire</span><span class="sxs-lookup"><span data-stu-id="32d8c-2189">Driving Licen</span></span> 
- <span data-ttu-id="32d8c-2190">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="32d8c-2190">Driving License</span></span> 
- <span data-ttu-id="32d8c-2191">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="32d8c-2191">Driving Licenses</span></span> 
- <span data-ttu-id="32d8c-2192">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="32d8c-2192">Driving Licence</span></span> 
- <span data-ttu-id="32d8c-2193">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="32d8c-2193">Driving Licences</span></span>

#### <a name="keyword_german_drivers_license_collaborative"></a><span data-ttu-id="32d8c-2194">Keyword_german_drivers_license_collaborative</span><span class="sxs-lookup"><span data-stu-id="32d8c-2194">Keyword_german_drivers_license_collaborative</span></span>

- <span data-ttu-id="32d8c-2195">Nr-Führerschein</span><span class="sxs-lookup"><span data-stu-id="32d8c-2195">Nr-Führerschein</span></span> 
- <span data-ttu-id="32d8c-2196">Nr-Fuhrerschein</span><span class="sxs-lookup"><span data-stu-id="32d8c-2196">Nr-Fuhrerschein</span></span> 
- <span data-ttu-id="32d8c-2197">Nr-Fuehrerschein</span><span class="sxs-lookup"><span data-stu-id="32d8c-2197">Nr-Fuehrerschein</span></span> 
- <span data-ttu-id="32d8c-2198">Non-Führerschein</span><span class="sxs-lookup"><span data-stu-id="32d8c-2198">No-Führerschein</span></span> 
- <span data-ttu-id="32d8c-2199">Non-Fuhrerschein</span><span class="sxs-lookup"><span data-stu-id="32d8c-2199">No-Fuhrerschein</span></span> 
- <span data-ttu-id="32d8c-2200">Non-Fuehrerschein</span><span class="sxs-lookup"><span data-stu-id="32d8c-2200">No-Fuehrerschein</span></span> 
- <span data-ttu-id="32d8c-2201">N-Führerschein</span><span class="sxs-lookup"><span data-stu-id="32d8c-2201">N-Führerschein</span></span> 
- <span data-ttu-id="32d8c-2202">N-Fuhrerschein</span><span class="sxs-lookup"><span data-stu-id="32d8c-2202">N-Fuhrerschein</span></span> 
- <span data-ttu-id="32d8c-2203">N-Fuehrerschein</span><span class="sxs-lookup"><span data-stu-id="32d8c-2203">N-Fuehrerschein</span></span>
- <span data-ttu-id="32d8c-2204">Nr-Führerschein</span><span class="sxs-lookup"><span data-stu-id="32d8c-2204">Nr-Führerschein</span></span> 
- <span data-ttu-id="32d8c-2205">Nr-Fuhrerschein</span><span class="sxs-lookup"><span data-stu-id="32d8c-2205">Nr-Fuhrerschein</span></span> 
- <span data-ttu-id="32d8c-2206">Nr-Fuehrerschein</span><span class="sxs-lookup"><span data-stu-id="32d8c-2206">Nr-Fuehrerschein</span></span> 
- <span data-ttu-id="32d8c-2207">Non-Führerschein</span><span class="sxs-lookup"><span data-stu-id="32d8c-2207">No-Führerschein</span></span> 
- <span data-ttu-id="32d8c-2208">Non-Fuhrerschein</span><span class="sxs-lookup"><span data-stu-id="32d8c-2208">No-Fuhrerschein</span></span> 
- <span data-ttu-id="32d8c-2209">Non-Fuehrerschein</span><span class="sxs-lookup"><span data-stu-id="32d8c-2209">No-Fuehrerschein</span></span> 
- <span data-ttu-id="32d8c-2210">N-Führerschein</span><span class="sxs-lookup"><span data-stu-id="32d8c-2210">N-Führerschein</span></span> 
- <span data-ttu-id="32d8c-2211">N-Fuhrerschein</span><span class="sxs-lookup"><span data-stu-id="32d8c-2211">N-Fuhrerschein</span></span> 
- <span data-ttu-id="32d8c-2212">N-Fuehrerschein</span><span class="sxs-lookup"><span data-stu-id="32d8c-2212">N-Fuehrerschein</span></span> 

#### <a name="keyword_german_drivers_license"></a><span data-ttu-id="32d8c-2213">Keyword_german_drivers_license</span><span class="sxs-lookup"><span data-stu-id="32d8c-2213">Keyword_german_drivers_license</span></span>

- <span data-ttu-id="32d8c-2214">ausstellungsdatum</span><span class="sxs-lookup"><span data-stu-id="32d8c-2214">ausstellungsdatum</span></span>
- <span data-ttu-id="32d8c-2215">ausstellungsort</span><span class="sxs-lookup"><span data-stu-id="32d8c-2215">ausstellungsort</span></span>
- <span data-ttu-id="32d8c-2216">ausstellende behöde</span><span class="sxs-lookup"><span data-stu-id="32d8c-2216">ausstellende behöde</span></span>
- <span data-ttu-id="32d8c-2217">ausstellende behorde</span><span class="sxs-lookup"><span data-stu-id="32d8c-2217">ausstellende behorde</span></span>
- <span data-ttu-id="32d8c-2218">ausstellende behoerde</span><span class="sxs-lookup"><span data-stu-id="32d8c-2218">ausstellende behoerde</span></span>
   
## <a name="german-passport-number"></a><span data-ttu-id="32d8c-2219">Numéro de passeport Allemagne</span><span class="sxs-lookup"><span data-stu-id="32d8c-2219">German Passport Number</span></span>

### <a name="format"></a><span data-ttu-id="32d8c-2220">Format</span><span class="sxs-lookup"><span data-stu-id="32d8c-2220">Format</span></span>

<span data-ttu-id="32d8c-2221">10 chiffres ou lettres</span><span class="sxs-lookup"><span data-stu-id="32d8c-2221">10 digits or letters</span></span>

### <a name="pattern"></a><span data-ttu-id="32d8c-2222">Modèle</span><span class="sxs-lookup"><span data-stu-id="32d8c-2222">Pattern</span></span>

<span data-ttu-id="32d8c-2223">Le modèle doit inclure tous les éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="32d8c-2223">Pattern must include all of the following:</span></span>
- <span data-ttu-id="32d8c-2224">Le premier caractère est un chiffre ou une lettre de cet ensemble (C, F, G, H, J, K)</span><span class="sxs-lookup"><span data-stu-id="32d8c-2224">First character is a digit or a letter from this set (C, F, G, H, J, K)</span></span> 
- <span data-ttu-id="32d8c-2225">Trois chiffres</span><span class="sxs-lookup"><span data-stu-id="32d8c-2225">Three digits</span></span> 
- <span data-ttu-id="32d8c-2226">Cinq chiffres ou lettres à partir de cet ensemble (C, -H, J-N, P, R, T, V-Z)</span><span class="sxs-lookup"><span data-stu-id="32d8c-2226">Five digits or letters from this set (C, -H, J-N, P, R, T, V-Z)</span></span> 
- <span data-ttu-id="32d8c-2227">Un chiffre</span><span class="sxs-lookup"><span data-stu-id="32d8c-2227">A digit</span></span>

### <a name="checksum"></a><span data-ttu-id="32d8c-2228">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="32d8c-2228">Checksum</span></span>

<span data-ttu-id="32d8c-2229">Oui</span><span class="sxs-lookup"><span data-stu-id="32d8c-2229">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="32d8c-2230">Définition</span><span class="sxs-lookup"><span data-stu-id="32d8c-2230">Definition</span></span>

<span data-ttu-id="32d8c-2231">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="32d8c-2231">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="32d8c-2232">La fonction Func_german_passport trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="32d8c-2232">The function Func_german_passport finds content that matches the pattern.</span></span>
- <span data-ttu-id="32d8c-2233">Un mot clé présent dans l’une des cinq listes de mots clés est trouvé.</span><span class="sxs-lookup"><span data-stu-id="32d8c-2233">A keyword from any of the five keyword lists is found.</span></span>
- <span data-ttu-id="32d8c-2234">La somme de contrôle est correcte.</span><span class="sxs-lookup"><span data-stu-id="32d8c-2234">The checksum passes.</span></span>

<span data-ttu-id="32d8c-2235">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="32d8c-2235">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="32d8c-2236">La fonction Func_german_passport_data trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="32d8c-2236">The function Func_german_passport_data finds content that matches the pattern.</span></span>
- <span data-ttu-id="32d8c-2237">Un mot clé présent dans l’une des cinq listes de mots clés est trouvé.</span><span class="sxs-lookup"><span data-stu-id="32d8c-2237">A keyword from any of the five keyword lists is found.</span></span>
- <span data-ttu-id="32d8c-2238">La somme de contrôle est correcte.</span><span class="sxs-lookup"><span data-stu-id="32d8c-2238">The checksum passes.</span></span>

```xml
<!-- German Passport Number -->
<Entity id="2e3da144-d42b-47ed-b123-fbf78604e52c" patternsProximity="300" recommendedConfidence="75">
  <Pattern confidenceLevel="85">
        <IdMatch idRef="Func_german_passport" />
        <Any minMatches="1">
          <Match idRef="Keyword_german_passport" />
          <Match idRef="Keyword_german_passport_collaborative" />
          <Match idRef="Keyword_german_passport_number" />
          <Match idRef="Keyword_german_passport1" />
          <Match idRef="Keyword_german_passport2" />
        </Any>
  </Pattern>
  <Pattern confidenceLevel="75">
        <IdMatch idRef="Func_german_passport_data" />
        <Any minMatches="1">
          <Match idRef="Keyword_german_passport" />
          <Match idRef="Keyword_german_passport_collaborative" />
          <Match idRef="Keyword_german_passport_number" />
          <Match idRef="Keyword_german_passport1" />
          <Match idRef="Keyword_german_passport2" />
        </Any>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="32d8c-2239">Mots clés</span><span class="sxs-lookup"><span data-stu-id="32d8c-2239">Keywords</span></span>

#### <a name="keyword_german_passport"></a><span data-ttu-id="32d8c-2240">Keyword_german_passport</span><span class="sxs-lookup"><span data-stu-id="32d8c-2240">Keyword_german_passport</span></span>

- <span data-ttu-id="32d8c-2241">reisepass</span><span class="sxs-lookup"><span data-stu-id="32d8c-2241">reisepass</span></span>
- <span data-ttu-id="32d8c-2242">reisepasse</span><span class="sxs-lookup"><span data-stu-id="32d8c-2242">reisepasse</span></span>
- <span data-ttu-id="32d8c-2243">reisepassnummer</span><span class="sxs-lookup"><span data-stu-id="32d8c-2243">reisepassnummer</span></span>
- <span data-ttu-id="32d8c-2244">tel</span><span class="sxs-lookup"><span data-stu-id="32d8c-2244">passport</span></span>
- <span data-ttu-id="32d8c-2245">passeports</span><span class="sxs-lookup"><span data-stu-id="32d8c-2245">passports</span></span>

#### <a name="keyword_german_passport_collaborative"></a><span data-ttu-id="32d8c-2246">Keyword_german_passport_collaborative</span><span class="sxs-lookup"><span data-stu-id="32d8c-2246">Keyword_german_passport_collaborative</span></span>

- <span data-ttu-id="32d8c-2247">geburtsdatum</span><span class="sxs-lookup"><span data-stu-id="32d8c-2247">geburtsdatum</span></span>
- <span data-ttu-id="32d8c-2248">ausstellungsdatum</span><span class="sxs-lookup"><span data-stu-id="32d8c-2248">ausstellungsdatum</span></span>
- <span data-ttu-id="32d8c-2249">ausstellungsort</span><span class="sxs-lookup"><span data-stu-id="32d8c-2249">ausstellungsort</span></span>

#### <a name="keyword_german_passport_number"></a><span data-ttu-id="32d8c-2250">Keyword_german_passport_number</span><span class="sxs-lookup"><span data-stu-id="32d8c-2250">Keyword_german_passport_number</span></span>

<span data-ttu-id="32d8c-2251">No-Reisepass Nr-Reisepass</span><span class="sxs-lookup"><span data-stu-id="32d8c-2251">No-Reisepass Nr-Reisepass</span></span>

#### <a name="keyword_german_passport1"></a><span data-ttu-id="32d8c-2252">Keyword_german_passport1</span><span class="sxs-lookup"><span data-stu-id="32d8c-2252">Keyword_german_passport1</span></span>

<span data-ttu-id="32d8c-2253">Reisepass-Nr</span><span class="sxs-lookup"><span data-stu-id="32d8c-2253">Reisepass-Nr</span></span>

#### <a name="keyword_german_passport2"></a><span data-ttu-id="32d8c-2254">Keyword_german_passport2</span><span class="sxs-lookup"><span data-stu-id="32d8c-2254">Keyword_german_passport2</span></span>

<span data-ttu-id="32d8c-2255">bnationalit. t</span><span class="sxs-lookup"><span data-stu-id="32d8c-2255">bnationalit.t</span></span>
   
## <a name="germany-identity-card-number"></a><span data-ttu-id="32d8c-2256">Numéro de carte d’identité allemand</span><span class="sxs-lookup"><span data-stu-id="32d8c-2256">Germany Identity Card Number</span></span>

### <a name="format"></a><span data-ttu-id="32d8c-2257">Format</span><span class="sxs-lookup"><span data-stu-id="32d8c-2257">Format</span></span>

<span data-ttu-id="32d8c-2258">Depuis le 1er novembre 2010 : neuf lettres et chiffres</span><span class="sxs-lookup"><span data-stu-id="32d8c-2258">Since 1 November 2010: Nine letters and digits</span></span>

<span data-ttu-id="32d8c-2259">Du 1er avril 1987 au 31 octobre 2010:10 chiffres</span><span class="sxs-lookup"><span data-stu-id="32d8c-2259">From 1 April 1987 until 31 October 2010: 10 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="32d8c-2260">Modèle</span><span class="sxs-lookup"><span data-stu-id="32d8c-2260">Pattern</span></span>

<span data-ttu-id="32d8c-2261">Depuis le 1er novembre 2010 :</span><span class="sxs-lookup"><span data-stu-id="32d8c-2261">Since 1 November 2010:</span></span>
- <span data-ttu-id="32d8c-2262">Une lettre (ne respectant pas la casse) </span><span class="sxs-lookup"><span data-stu-id="32d8c-2262">One letter (not case sensitive)</span></span> 
- <span data-ttu-id="32d8c-2263">Huit chiffres</span><span class="sxs-lookup"><span data-stu-id="32d8c-2263">Eight digits</span></span>

<span data-ttu-id="32d8c-2264">Du 1er avril 1987 au 31 octobre 2010 :</span><span class="sxs-lookup"><span data-stu-id="32d8c-2264">From 1 April 1987 until 31 October 2010:</span></span>
- <span data-ttu-id="32d8c-2265">10 chiffres</span><span class="sxs-lookup"><span data-stu-id="32d8c-2265">10 digits</span></span>

### <a name="checksum"></a><span data-ttu-id="32d8c-2266">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="32d8c-2266">Checksum</span></span>

<span data-ttu-id="32d8c-2267">Non</span><span class="sxs-lookup"><span data-stu-id="32d8c-2267">No</span></span>

### <a name="definition"></a><span data-ttu-id="32d8c-2268">Définition</span><span class="sxs-lookup"><span data-stu-id="32d8c-2268">Definition</span></span>

<span data-ttu-id="32d8c-2269">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 65 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="32d8c-2269">A DLP policy is 65% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="32d8c-2270">L’expression régulière Regex_germany_id_card trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="32d8c-2270">The regular expression Regex_germany_id_card finds content that matches the pattern.</span></span>
- <span data-ttu-id="32d8c-2271">Un mot clé figurant dans la liste Keyword_germany_id_card est trouvé.</span><span class="sxs-lookup"><span data-stu-id="32d8c-2271">A keyword from Keyword_germany_id_card is found.</span></span>

```xml
<!-- Germany Identity Card Number -->
<Entity id="e577372f-c42e-47a0-9d85-bebed1c237d4" recommendedConfidence="65" patternsProximity="300">
  <Pattern confidenceLevel="65">
     <IdMatch idRef="Regex_germany_id_card"/>
     <Match idRef="Keyword_germany_id_card"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="32d8c-2272">Mots clés</span><span class="sxs-lookup"><span data-stu-id="32d8c-2272">Keywords</span></span>

#### <a name="keyword_germany_id_card"></a><span data-ttu-id="32d8c-2273">Keyword_germany_id_card</span><span class="sxs-lookup"><span data-stu-id="32d8c-2273">Keyword_germany_id_card</span></span>

- <span data-ttu-id="32d8c-2274">Identity Card</span><span class="sxs-lookup"><span data-stu-id="32d8c-2274">Identity Card</span></span>
- <span data-ttu-id="32d8c-2275">ID</span><span class="sxs-lookup"><span data-stu-id="32d8c-2275">ID</span></span>
- <span data-ttu-id="32d8c-2276">Identificateur</span><span class="sxs-lookup"><span data-stu-id="32d8c-2276">Identification</span></span>
- <span data-ttu-id="32d8c-2277">Personalausweis</span><span class="sxs-lookup"><span data-stu-id="32d8c-2277">Personalausweis</span></span>
- <span data-ttu-id="32d8c-2278">Identifizierungsnummer</span><span class="sxs-lookup"><span data-stu-id="32d8c-2278">Identifizierungsnummer</span></span>
- <span data-ttu-id="32d8c-2279">Ausweis</span><span class="sxs-lookup"><span data-stu-id="32d8c-2279">Ausweis</span></span>
- <span data-ttu-id="32d8c-2280">Identifikation</span><span class="sxs-lookup"><span data-stu-id="32d8c-2280">Identifikation</span></span>
   
## <a name="greece-national-id-card"></a><span data-ttu-id="32d8c-2281">Carte d’identité nationale Grèce</span><span class="sxs-lookup"><span data-stu-id="32d8c-2281">Greece National ID Card</span></span>

### <a name="format"></a><span data-ttu-id="32d8c-2282">Format</span><span class="sxs-lookup"><span data-stu-id="32d8c-2282">Format</span></span>

<span data-ttu-id="32d8c-2283">Combinaison de 7 ou 8 lettres et chiffres, plus un tiret</span><span class="sxs-lookup"><span data-stu-id="32d8c-2283">Combination of 7-8 letters and numbers plus a dash</span></span>

### <a name="pattern"></a><span data-ttu-id="32d8c-2284">Modèle</span><span class="sxs-lookup"><span data-stu-id="32d8c-2284">Pattern</span></span>

<span data-ttu-id="32d8c-2285">Sept lettres et chiffres (ancien format) :</span><span class="sxs-lookup"><span data-stu-id="32d8c-2285">Seven letters and numbers (old format):</span></span>
- <span data-ttu-id="32d8c-2286">Une lettre (de l’alphabet grec) </span><span class="sxs-lookup"><span data-stu-id="32d8c-2286">One letter (any letter of the Greek alphabet)</span></span> 
- <span data-ttu-id="32d8c-2287">Un tiret</span><span class="sxs-lookup"><span data-stu-id="32d8c-2287">A dash</span></span> 
- <span data-ttu-id="32d8c-2288">Six chiffres</span><span class="sxs-lookup"><span data-stu-id="32d8c-2288">Six digits</span></span>

<span data-ttu-id="32d8c-2289">Huit lettres et chiffres (nouveau format) :</span><span class="sxs-lookup"><span data-stu-id="32d8c-2289">Eight letters and numbers (new format):</span></span>
- <span data-ttu-id="32d8c-2290">Deux lettres dont le caractère majuscule figure à la fois dans l’alphabet grec et l’alphabet latin (ABEZHIKMNOPTYX) </span><span class="sxs-lookup"><span data-stu-id="32d8c-2290">Two letters whose uppercase character occurs in both the Greek and Latin alphabets (ABEZHIKMNOPTYX)</span></span> 
- <span data-ttu-id="32d8c-2291">Un tiret</span><span class="sxs-lookup"><span data-stu-id="32d8c-2291">A dash</span></span> 
- <span data-ttu-id="32d8c-2292">Six chiffres</span><span class="sxs-lookup"><span data-stu-id="32d8c-2292">Six digits</span></span>

### <a name="checksum"></a><span data-ttu-id="32d8c-2293">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="32d8c-2293">Checksum</span></span>

<span data-ttu-id="32d8c-2294">Non</span><span class="sxs-lookup"><span data-stu-id="32d8c-2294">No</span></span>

### <a name="definition"></a><span data-ttu-id="32d8c-2295">Définition</span><span class="sxs-lookup"><span data-stu-id="32d8c-2295">Definition</span></span>

<span data-ttu-id="32d8c-2296">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="32d8c-2296">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="32d8c-2297">L’expression régulière Regex_greece_id_card trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="32d8c-2297">The regular expression Regex_greece_id_card finds content that matches the pattern.</span></span>
- <span data-ttu-id="32d8c-2298">Un mot clé figurant dans la liste Keyword_greece_id_card est trouvé.</span><span class="sxs-lookup"><span data-stu-id="32d8c-2298">A keyword from Keyword_greece_id_card is found.</span></span>

```xml
<!-- Greece National ID Card -->
<Entity id="82568215-1da1-46d3-874a-d2294d81b5ac" recommendedConfidence="85" patternsProximity="300">
  <Pattern confidenceLevel="85">
     <IdMatch idRef="Regex_greece_id_card"/>
     <Match idRef="Keyword_greece_id_card"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="32d8c-2299">Mots clés</span><span class="sxs-lookup"><span data-stu-id="32d8c-2299">Keywords</span></span>

#### <a name="keyword_greece_id_card"></a><span data-ttu-id="32d8c-2300">Keyword_greece_id_card</span><span class="sxs-lookup"><span data-stu-id="32d8c-2300">Keyword_greece_id_card</span></span>

- <span data-ttu-id="32d8c-2301">Greek identity Card</span><span class="sxs-lookup"><span data-stu-id="32d8c-2301">Greek identity Card</span></span>
- <span data-ttu-id="32d8c-2302">Tautotita</span><span class="sxs-lookup"><span data-stu-id="32d8c-2302">Tautotita</span></span>
- <span data-ttu-id="32d8c-2303">Δελτίο αστυνομικής ταυτότητας</span><span class="sxs-lookup"><span data-stu-id="32d8c-2303">Δελτίο αστυνομικής ταυτότητας</span></span>
- <span data-ttu-id="32d8c-2304">Ταυτότητα</span><span class="sxs-lookup"><span data-stu-id="32d8c-2304">Ταυτότητα</span></span>
   
## <a name="hong-kong-identity-card-hkid-number"></a><span data-ttu-id="32d8c-2305">Numéro de carte d’identité (HKID) Hong Kong</span><span class="sxs-lookup"><span data-stu-id="32d8c-2305">Hong Kong Identity Card (HKID) Number</span></span>

### <a name="format"></a><span data-ttu-id="32d8c-2306">Format</span><span class="sxs-lookup"><span data-stu-id="32d8c-2306">Format</span></span>

<span data-ttu-id="32d8c-2307">Combinaison de 8 ou 9 lettres et chiffres plus éventuellement des parenthèses autour du dernier caractère</span><span class="sxs-lookup"><span data-stu-id="32d8c-2307">Combination of 8-9 letters and numbers plus optional parentheses around the final character</span></span>

### <a name="pattern"></a><span data-ttu-id="32d8c-2308">Modèle</span><span class="sxs-lookup"><span data-stu-id="32d8c-2308">Pattern</span></span>

<span data-ttu-id="32d8c-2309">Combinaison de 8 ou 9 lettres :</span><span class="sxs-lookup"><span data-stu-id="32d8c-2309">Combination of 8-9 letters:</span></span>
- <span data-ttu-id="32d8c-2310">1 ou 2 lettres (ne respectant pas la casse) </span><span class="sxs-lookup"><span data-stu-id="32d8c-2310">1-2 letters (not case sensitive)</span></span> 
- <span data-ttu-id="32d8c-2311">Six chiffres</span><span class="sxs-lookup"><span data-stu-id="32d8c-2311">Six digits</span></span> 
- <span data-ttu-id="32d8c-2312">Le dernier caractère (un chiffre ou la lettre A), qui est le chiffre de contrôle et est éventuellement entre parenthèses.</span><span class="sxs-lookup"><span data-stu-id="32d8c-2312">The final character (any digit or the letter A), which is the check digit and is optionally enclosed in parentheses.</span></span>

### <a name="checksum"></a><span data-ttu-id="32d8c-2313">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="32d8c-2313">Checksum</span></span>

<span data-ttu-id="32d8c-2314">Oui</span><span class="sxs-lookup"><span data-stu-id="32d8c-2314">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="32d8c-2315">Définition</span><span class="sxs-lookup"><span data-stu-id="32d8c-2315">Definition</span></span>

<span data-ttu-id="32d8c-2316">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="32d8c-2316">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="32d8c-2317">La fonction Func_hong_kong_id_card trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="32d8c-2317">The function Func_hong_kong_id_card finds content that matches the pattern.</span></span>
- <span data-ttu-id="32d8c-2318">Un mot clé figurant dans la liste Keyword_hong_kong_id_card est trouvé.</span><span class="sxs-lookup"><span data-stu-id="32d8c-2318">A keyword from Keyword_hong_kong_id_card is found.</span></span>
- <span data-ttu-id="32d8c-2319">La somme de contrôle est correcte.</span><span class="sxs-lookup"><span data-stu-id="32d8c-2319">The checksum passes.</span></span>

<span data-ttu-id="32d8c-2320">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 65 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="32d8c-2320">A DLP policy is 65% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="32d8c-2321">La fonction Func_hong_kong_id_card trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="32d8c-2321">The function Func_hong_kong_id_card finds content that matches the pattern.</span></span>
- <span data-ttu-id="32d8c-2322">La somme de contrôle est correcte.</span><span class="sxs-lookup"><span data-stu-id="32d8c-2322">The checksum passes.</span></span>

```xml
<!-- Hong Kong Identity Card (HKID) number -->
<Entity id="e63c28a7-ad29-4c17-a41a-3d2a0b70fd9c" recommendedConfidence="75" patternsProximity="300">
  <Pattern confidenceLevel="75">
     <IdMatch idRef="Func_hong_kong_id_card"/>
     <Match idRef="Keyword_hong_kong_id_card"/>
  </Pattern>
  <Pattern confidenceLevel="65">
     <IdMatch idRef="Func_hong_kong_id_card"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="32d8c-2323">Mots clés</span><span class="sxs-lookup"><span data-stu-id="32d8c-2323">Keywords</span></span>

#### <a name="keyword_hong_kong_id_card"></a><span data-ttu-id="32d8c-2324">Keyword_hong_kong_id_card</span><span class="sxs-lookup"><span data-stu-id="32d8c-2324">Keyword_hong_kong_id_card</span></span>

- <span data-ttu-id="32d8c-2325">carte d’identité de Hong Kong</span><span class="sxs-lookup"><span data-stu-id="32d8c-2325">hong kong identity card</span></span>
- <span data-ttu-id="32d8c-2326">HKIDC</span><span class="sxs-lookup"><span data-stu-id="32d8c-2326">HKIDC</span></span>
- <span data-ttu-id="32d8c-2327">carte d’identité</span><span class="sxs-lookup"><span data-stu-id="32d8c-2327">id card</span></span>
- <span data-ttu-id="32d8c-2328">Carte d’identité</span><span class="sxs-lookup"><span data-stu-id="32d8c-2328">identity card</span></span>
- <span data-ttu-id="32d8c-2329">carte d’identité HK</span><span class="sxs-lookup"><span data-stu-id="32d8c-2329">hk identity card</span></span>
- <span data-ttu-id="32d8c-2330">ID Hong Kong</span><span class="sxs-lookup"><span data-stu-id="32d8c-2330">hong kong id</span></span>
- <span data-ttu-id="32d8c-2331">香港身份證</span><span class="sxs-lookup"><span data-stu-id="32d8c-2331">香港身份證</span></span>
- <span data-ttu-id="32d8c-2332">香港永久性居民身份證</span><span class="sxs-lookup"><span data-stu-id="32d8c-2332">香港永久性居民身份證</span></span>
- <span data-ttu-id="32d8c-2333">身份證</span><span class="sxs-lookup"><span data-stu-id="32d8c-2333">身份證</span></span>
- <span data-ttu-id="32d8c-2334">身份証</span><span class="sxs-lookup"><span data-stu-id="32d8c-2334">身份証</span></span>
- <span data-ttu-id="32d8c-2335">身分證</span><span class="sxs-lookup"><span data-stu-id="32d8c-2335">身分證</span></span>
- <span data-ttu-id="32d8c-2336">身分証</span><span class="sxs-lookup"><span data-stu-id="32d8c-2336">身分証</span></span>
- <span data-ttu-id="32d8c-2337">香港身份証</span><span class="sxs-lookup"><span data-stu-id="32d8c-2337">香港身份証</span></span>
- <span data-ttu-id="32d8c-2338">香港身分證</span><span class="sxs-lookup"><span data-stu-id="32d8c-2338">香港身分證</span></span>
- <span data-ttu-id="32d8c-2339">香港身分証</span><span class="sxs-lookup"><span data-stu-id="32d8c-2339">香港身分証</span></span>
- <span data-ttu-id="32d8c-2340">香港身份證</span><span class="sxs-lookup"><span data-stu-id="32d8c-2340">香港身份證</span></span>
- <span data-ttu-id="32d8c-2341">香港居民身份證</span><span class="sxs-lookup"><span data-stu-id="32d8c-2341">香港居民身份證</span></span>
- <span data-ttu-id="32d8c-2342">香港居民身份証</span><span class="sxs-lookup"><span data-stu-id="32d8c-2342">香港居民身份証</span></span>
- <span data-ttu-id="32d8c-2343">香港居民身分證</span><span class="sxs-lookup"><span data-stu-id="32d8c-2343">香港居民身分證</span></span>
- <span data-ttu-id="32d8c-2344">香港居民身分証</span><span class="sxs-lookup"><span data-stu-id="32d8c-2344">香港居民身分証</span></span>
- <span data-ttu-id="32d8c-2345">香港永久性居民身份証</span><span class="sxs-lookup"><span data-stu-id="32d8c-2345">香港永久性居民身份証</span></span>
- <span data-ttu-id="32d8c-2346">香港永久性居民身分證</span><span class="sxs-lookup"><span data-stu-id="32d8c-2346">香港永久性居民身分證</span></span>
- <span data-ttu-id="32d8c-2347">香港永久性居民身分証</span><span class="sxs-lookup"><span data-stu-id="32d8c-2347">香港永久性居民身分証</span></span>
- <span data-ttu-id="32d8c-2348">香港永久性居民身份證</span><span class="sxs-lookup"><span data-stu-id="32d8c-2348">香港永久性居民身份證</span></span>
- <span data-ttu-id="32d8c-2349">香港非永久性居民身份證</span><span class="sxs-lookup"><span data-stu-id="32d8c-2349">香港非永久性居民身份證</span></span>
- <span data-ttu-id="32d8c-2350">香港非永久性居民身份証</span><span class="sxs-lookup"><span data-stu-id="32d8c-2350">香港非永久性居民身份証</span></span>
- <span data-ttu-id="32d8c-2351">香港非永久性居民身分證</span><span class="sxs-lookup"><span data-stu-id="32d8c-2351">香港非永久性居民身分證</span></span>
- <span data-ttu-id="32d8c-2352">香港非永久性居民身分証</span><span class="sxs-lookup"><span data-stu-id="32d8c-2352">香港非永久性居民身分証</span></span>
- <span data-ttu-id="32d8c-2353">香港特別行政區永久性居民身份證</span><span class="sxs-lookup"><span data-stu-id="32d8c-2353">香港特別行政區永久性居民身份證</span></span>
- <span data-ttu-id="32d8c-2354">香港特別行政區永久性居民身份証</span><span class="sxs-lookup"><span data-stu-id="32d8c-2354">香港特別行政區永久性居民身份証</span></span>
- <span data-ttu-id="32d8c-2355">香港特別行政區永久性居民身分證</span><span class="sxs-lookup"><span data-stu-id="32d8c-2355">香港特別行政區永久性居民身分證</span></span>
- <span data-ttu-id="32d8c-2356">香港特別行政區永久性居民身分証</span><span class="sxs-lookup"><span data-stu-id="32d8c-2356">香港特別行政區永久性居民身分証</span></span>
- <span data-ttu-id="32d8c-2357">香港特別行政區非永久性居民身份證</span><span class="sxs-lookup"><span data-stu-id="32d8c-2357">香港特別行政區非永久性居民身份證</span></span>
- <span data-ttu-id="32d8c-2358">香港特別行政區非永久性居民身份証</span><span class="sxs-lookup"><span data-stu-id="32d8c-2358">香港特別行政區非永久性居民身份証</span></span>
- <span data-ttu-id="32d8c-2359">香港特別行政區非永久性居民身分證</span><span class="sxs-lookup"><span data-stu-id="32d8c-2359">香港特別行政區非永久性居民身分證</span></span>
- <span data-ttu-id="32d8c-2360">香港特別行政區非永久性居民身分証</span><span class="sxs-lookup"><span data-stu-id="32d8c-2360">香港特別行政區非永久性居民身分証</span></span>
   
## <a name="india-permanent-account-number-pan"></a><span data-ttu-id="32d8c-2361">Numéro de compte permanent Inde</span><span class="sxs-lookup"><span data-stu-id="32d8c-2361">India Permanent Account Number (PAN)</span></span>

### <a name="format"></a><span data-ttu-id="32d8c-2362">Format</span><span class="sxs-lookup"><span data-stu-id="32d8c-2362">Format</span></span>

<span data-ttu-id="32d8c-2363">10 lettres ou chiffres</span><span class="sxs-lookup"><span data-stu-id="32d8c-2363">10 letters or digits</span></span>

### <a name="pattern"></a><span data-ttu-id="32d8c-2364">Modèle</span><span class="sxs-lookup"><span data-stu-id="32d8c-2364">Pattern</span></span>

<span data-ttu-id="32d8c-2365">10 lettres ou chiffres :</span><span class="sxs-lookup"><span data-stu-id="32d8c-2365">10 letters or digits:</span></span>
- <span data-ttu-id="32d8c-2366">Cinq lettres (ne respectant pas la casse) </span><span class="sxs-lookup"><span data-stu-id="32d8c-2366">Five letters (not case sensitive)</span></span> 
- <span data-ttu-id="32d8c-2367">Quatre chiffres</span><span class="sxs-lookup"><span data-stu-id="32d8c-2367">Four digits</span></span> 
- <span data-ttu-id="32d8c-2368">Une lettre qui est un chiffre de contrôle alphabétique</span><span class="sxs-lookup"><span data-stu-id="32d8c-2368">A letter which is an alphabetic check digit</span></span>

### <a name="checksum"></a><span data-ttu-id="32d8c-2369">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="32d8c-2369">Checksum</span></span>

<span data-ttu-id="32d8c-2370">Oui</span><span class="sxs-lookup"><span data-stu-id="32d8c-2370">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="32d8c-2371">Définition</span><span class="sxs-lookup"><span data-stu-id="32d8c-2371">Definition</span></span>

<span data-ttu-id="32d8c-2372">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="32d8c-2372">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="32d8c-2373">L’expression régulière Regex_india_permanent_account_number trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="32d8c-2373">The regular expression Regex_india_permanent_account_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="32d8c-2374">Un mot clé figurant dans la liste Keyword_india_permanent_account_number est trouvé.</span><span class="sxs-lookup"><span data-stu-id="32d8c-2374">A keyword from Keyword_india_permanent_account_number is found.</span></span>
- <span data-ttu-id="32d8c-2375">La somme de contrôle est correcte.</span><span class="sxs-lookup"><span data-stu-id="32d8c-2375">The checksum passes.</span></span>

```xml
<!-- India Permanent Account Number -->
<Entity id="2602bfee-9bb0-47a5-a7a6-2bf3053e2804" recommendedConfidence="85" patternsProximity="300">
  <Pattern confidenceLevel="85">
     <IdMatch idRef="Regex_india_permanent_account_number"/>
     <Match idRef="Keyword_india_permanent_account_number"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="32d8c-2376">Mots clés</span><span class="sxs-lookup"><span data-stu-id="32d8c-2376">Keywords</span></span>

#### <a name="keyword_india_permanent_account_number"></a><span data-ttu-id="32d8c-2377">Keyword_india_permanent_account_number</span><span class="sxs-lookup"><span data-stu-id="32d8c-2377">Keyword_india_permanent_account_number</span></span>

- <span data-ttu-id="32d8c-2378">Permanent Account Number</span><span class="sxs-lookup"><span data-stu-id="32d8c-2378">Permanent Account Number</span></span> 
- <span data-ttu-id="32d8c-2379">PANEUROPÉENNES</span><span class="sxs-lookup"><span data-stu-id="32d8c-2379">PAN</span></span> 
   
## <a name="india-unique-identification-aadhaar-number"></a><span data-ttu-id="32d8c-2380">Numéro d’identification unique (Aadhaar) Inde</span><span class="sxs-lookup"><span data-stu-id="32d8c-2380">India Unique Identification (Aadhaar) Number</span></span>

### <a name="format"></a><span data-ttu-id="32d8c-2381">Format</span><span class="sxs-lookup"><span data-stu-id="32d8c-2381">Format</span></span>

<span data-ttu-id="32d8c-2382">12 chiffres contenant éventuellement des espaces ou des tirets</span><span class="sxs-lookup"><span data-stu-id="32d8c-2382">12 digits containing optional spaces or dashes</span></span>

### <a name="pattern"></a><span data-ttu-id="32d8c-2383">Modèle</span><span class="sxs-lookup"><span data-stu-id="32d8c-2383">Pattern</span></span>

<span data-ttu-id="32d8c-2384">12 chiffres :</span><span class="sxs-lookup"><span data-stu-id="32d8c-2384">12 digits:</span></span>
- <span data-ttu-id="32d8c-2385">Quatre chiffres</span><span class="sxs-lookup"><span data-stu-id="32d8c-2385">Four digits</span></span> 
- <span data-ttu-id="32d8c-2386">Éventuellement un tiret ou un espace </span><span class="sxs-lookup"><span data-stu-id="32d8c-2386">An optional space or dash</span></span> 
- <span data-ttu-id="32d8c-2387">Quatre chiffres</span><span class="sxs-lookup"><span data-stu-id="32d8c-2387">Four digits</span></span> 
- <span data-ttu-id="32d8c-2388">Éventuellement un tiret ou un espace </span><span class="sxs-lookup"><span data-stu-id="32d8c-2388">An optional space or dash</span></span> 
- <span data-ttu-id="32d8c-2389">Le chiffre final, qui est le chiffre de contrôle</span><span class="sxs-lookup"><span data-stu-id="32d8c-2389">The final digit which is the check digit</span></span>

### <a name="checksum"></a><span data-ttu-id="32d8c-2390">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="32d8c-2390">Checksum</span></span>

<span data-ttu-id="32d8c-2391">Oui</span><span class="sxs-lookup"><span data-stu-id="32d8c-2391">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="32d8c-2392">Définition</span><span class="sxs-lookup"><span data-stu-id="32d8c-2392">Definition</span></span>

<span data-ttu-id="32d8c-2393">Une stratégie DLP est sûre à 85% d’avoir détecté ce type d’informations sensibles si, dans une proximité de 300 caractères : la fonction Func_india_aadhaar trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="32d8c-2393">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters: The function Func_india_aadhaar finds content that matches the pattern.</span></span>
<span data-ttu-id="32d8c-2394">Un mot clé figurant dans la liste Keyword_india_aadhar est trouvé.</span><span class="sxs-lookup"><span data-stu-id="32d8c-2394">A keyword from Keyword_india_aadhar is found.</span></span>
<span data-ttu-id="32d8c-2395">La somme de contrôle est correcte.</span><span class="sxs-lookup"><span data-stu-id="32d8c-2395">The checksum passes.</span></span>
<span data-ttu-id="32d8c-2396">Une stratégie DLP est sûre à 75% d’avoir détecté ce type d’informations sensibles si, dans une proximité de 300 caractères : la fonction Func_india_aadhaar trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="32d8c-2396">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters: The function Func_india_aadhaar finds content that matches the pattern.</span></span>
<span data-ttu-id="32d8c-2397">La somme de contrôle est correcte.</span><span class="sxs-lookup"><span data-stu-id="32d8c-2397">The checksum passes.</span></span>
```xml
<!-- India Unique Identification (Aadhaar) number -->
<Entity id="1ca46b29-76f5-4f46-9383-cfa15e91048f" recommendedConfidence="85" patternsProximity="300">
  <Pattern confidenceLevel="85">
     <IdMatch idRef="Func_india_aadhaar"/>
     <Match idRef="Keyword_india_aadhar"/>
  </Pattern>
  <Pattern confidenceLevel="75">
     <IdMatch idRef="Func_india_aadhaar"/>
  </Pattern>
</Entity>
```
### <a name="keywords"></a><span data-ttu-id="32d8c-2398">Mots clés</span><span class="sxs-lookup"><span data-stu-id="32d8c-2398">Keywords</span></span>
   
#### <a name="keyword_india_aadhar"></a><span data-ttu-id="32d8c-2399">Keyword_india_aadhar</span><span class="sxs-lookup"><span data-stu-id="32d8c-2399">Keyword_india_aadhar</span></span>
- <span data-ttu-id="32d8c-2400">Aadhar</span><span class="sxs-lookup"><span data-stu-id="32d8c-2400">Aadhar</span></span>
- <span data-ttu-id="32d8c-2401">Aadhaar</span><span class="sxs-lookup"><span data-stu-id="32d8c-2401">Aadhaar</span></span>
- <span data-ttu-id="32d8c-2402">UID</span><span class="sxs-lookup"><span data-stu-id="32d8c-2402">UID</span></span>
- <span data-ttu-id="32d8c-2403">आधार</span><span class="sxs-lookup"><span data-stu-id="32d8c-2403">आधार</span></span>
   
## <a name="indonesia-identity-card-ktp-number"></a><span data-ttu-id="32d8c-2404">Numéro de carte d’identité (KTP) Indonésie</span><span class="sxs-lookup"><span data-stu-id="32d8c-2404">Indonesia Identity Card (KTP) Number</span></span>

### <a name="format"></a><span data-ttu-id="32d8c-2405">Format</span><span class="sxs-lookup"><span data-stu-id="32d8c-2405">Format</span></span>

<span data-ttu-id="32d8c-2406">16 chiffres contenant éventuellement des points</span><span class="sxs-lookup"><span data-stu-id="32d8c-2406">16 digits containing optional periods</span></span>

### <a name="pattern"></a><span data-ttu-id="32d8c-2407">Modèle</span><span class="sxs-lookup"><span data-stu-id="32d8c-2407">Pattern</span></span>

<span data-ttu-id="32d8c-2408">16 chiffres :</span><span class="sxs-lookup"><span data-stu-id="32d8c-2408">16 digits:</span></span>
- <span data-ttu-id="32d8c-2409">Code à deux chiffres désignant la province </span><span class="sxs-lookup"><span data-stu-id="32d8c-2409">Two-digit province code</span></span> 
- <span data-ttu-id="32d8c-2410">Un point (facultatif) </span><span class="sxs-lookup"><span data-stu-id="32d8c-2410">A period (optional)</span></span> 
- <span data-ttu-id="32d8c-2411">Code à deux chiffres désignant une régence ou une ville </span><span class="sxs-lookup"><span data-stu-id="32d8c-2411">Two-digit regency or city code</span></span> 
- <span data-ttu-id="32d8c-2412">Code à deux chiffres désignant un sous-district </span><span class="sxs-lookup"><span data-stu-id="32d8c-2412">Two-digit subdistrict code</span></span> 
- <span data-ttu-id="32d8c-2413">Un point (facultatif) </span><span class="sxs-lookup"><span data-stu-id="32d8c-2413">A period (optional)</span></span> 
- <span data-ttu-id="32d8c-2414">Six chiffres au format JJMMAA qui correspondent à la date de naissance </span><span class="sxs-lookup"><span data-stu-id="32d8c-2414">Six digits in the format DDMMYY which are the date of birth</span></span> 
- <span data-ttu-id="32d8c-2415">Un point (facultatif) </span><span class="sxs-lookup"><span data-stu-id="32d8c-2415">A period (optional)</span></span> 
- <span data-ttu-id="32d8c-2416">Quatre chiffres</span><span class="sxs-lookup"><span data-stu-id="32d8c-2416">Four digits</span></span>

### <a name="checksum"></a><span data-ttu-id="32d8c-2417">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="32d8c-2417">Checksum</span></span>

<span data-ttu-id="32d8c-2418">Non</span><span class="sxs-lookup"><span data-stu-id="32d8c-2418">No</span></span>

### <a name="definition"></a><span data-ttu-id="32d8c-2419">Définition</span><span class="sxs-lookup"><span data-stu-id="32d8c-2419">Definition</span></span>

<span data-ttu-id="32d8c-2420">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="32d8c-2420">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="32d8c-2421">L’expression régulière Regex_indonesia_id_card trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="32d8c-2421">The regular expression Regex_indonesia_id_card finds content that matches the pattern.</span></span>
- <span data-ttu-id="32d8c-2422">Un mot clé figurant dans la liste Keyword_indonesia_id_card est trouvé.</span><span class="sxs-lookup"><span data-stu-id="32d8c-2422">A keyword from Keyword_indonesia_id_card is found.</span></span>

<span data-ttu-id="32d8c-2423">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="32d8c-2423">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="32d8c-2424">L’expression régulière Regex_indonesia_id_card trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="32d8c-2424">The regular expression Regex_indonesia_id_card finds content that matches the pattern.</span></span>

```xml
<!-- Indonesia Identity Card (KTP) Number -->
<Entity id="da68fdb0-f383-4981-8c86-82689d3b7d55" recommendedConfidence="85" patternsProximity="300">
  <Pattern confidenceLevel="85">
     <IdMatch idRef="Regex_indonesia_id_card"/>
     <Match idRef="Keyword_indonesia_id_card"/>
  </Pattern>
  <Pattern confidenceLevel="75">
     <IdMatch idRef="Regex_indonesia_id_card"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="32d8c-2425">Mots clés</span><span class="sxs-lookup"><span data-stu-id="32d8c-2425">Keywords</span></span>
   
#### <a name="keyword_indonesia_id_card"></a><span data-ttu-id="32d8c-2426">Keyword_indonesia_id_card</span><span class="sxs-lookup"><span data-stu-id="32d8c-2426">Keyword_indonesia_id_card</span></span>

- <span data-ttu-id="32d8c-2427">KTP</span><span class="sxs-lookup"><span data-stu-id="32d8c-2427">KTP</span></span>
- <span data-ttu-id="32d8c-2428">Kartu Tanda Penduduk</span><span class="sxs-lookup"><span data-stu-id="32d8c-2428">Kartu Tanda Penduduk</span></span> 
- <span data-ttu-id="32d8c-2429">Nomor Induk Kependudukan</span><span class="sxs-lookup"><span data-stu-id="32d8c-2429">Nomor Induk Kependudukan</span></span> 
   
## <a name="international-banking-account-number-iban"></a><span data-ttu-id="32d8c-2430">Numéro de compte bancaire international (IBAN)</span><span class="sxs-lookup"><span data-stu-id="32d8c-2430">International Banking Account Number (IBAN)</span></span>

### <a name="format"></a><span data-ttu-id="32d8c-2431">Format</span><span class="sxs-lookup"><span data-stu-id="32d8c-2431">Format</span></span>

<span data-ttu-id="32d8c-2432">Code pays (à deux lettres) plus chiffres de contrôle (à deux chiffres) plus numéro BBAN (jusqu’à 30 chiffres)</span><span class="sxs-lookup"><span data-stu-id="32d8c-2432">Country code (two letters) plus check digits (two digits) plus bban number (up to 30 characters)</span></span>

### <a name="pattern"></a><span data-ttu-id="32d8c-2433">Modèle</span><span class="sxs-lookup"><span data-stu-id="32d8c-2433">Pattern</span></span>

<span data-ttu-id="32d8c-2434">Le modèle doit inclure tous les éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="32d8c-2434">Pattern must include all of the following:</span></span>

- <span data-ttu-id="32d8c-2435">Code pays à deux lettres</span><span class="sxs-lookup"><span data-stu-id="32d8c-2435">Two-letter country code</span></span>
- <span data-ttu-id="32d8c-2436">Deux chiffres de contrôle (suivis d’un espace facultatif) </span><span class="sxs-lookup"><span data-stu-id="32d8c-2436">Two check digits (followed by an optional space)</span></span> 
- <span data-ttu-id="32d8c-2437">1 à 7 groupes de quatre lettres ou chiffres (séparés par des espaces facultatifs)</span><span class="sxs-lookup"><span data-stu-id="32d8c-2437">1-7 groups of four letters or digits (can be separated by spaces)</span></span>
- <span data-ttu-id="32d8c-2438">1 à 3 lettres ou chiffres</span><span class="sxs-lookup"><span data-stu-id="32d8c-2438">1-3 letters or digits</span></span>

<span data-ttu-id="32d8c-p133">Le format pour chaque pays est légèrement différent. Le type d’informations sensibles IBAN recouvre ces 60 pays :</span><span class="sxs-lookup"><span data-stu-id="32d8c-p133">The format for each country is slightly different. The IBAN sensitive information type covers these 60 countries:</span></span>

<span data-ttu-id="32d8c-2441">ad, ae, al, at, az, ba, be, bg, bh, ch, cr, cy, cz, de, dk, do, ee, es, fi, fo, fr, gb, ge, gi, gl, gr, hr, hu, ie, il, is, it, kw, kz, lb, li, lt, lu, lv, mc, md, me, mk, mr, mt, mu, nl, no, pl, pt, ro, rs, sa, se, si, sk, sm, tn, tr, vg</span><span class="sxs-lookup"><span data-stu-id="32d8c-2441">ad, ae, al, at, az, ba, be, bg, bh, ch, cr, cy, cz, de, dk, do, ee, es, fi, fo, fr, gb, ge, gi, gl, gr, hr, hu, ie, il, is, it, kw, kz, lb, li, lt, lu, lv, mc, md, me, mk, mr, mt, mu, nl, no, pl, pt, ro, rs, sa, se, si, sk, sm, tn, tr, vg</span></span>

### <a name="checksum"></a><span data-ttu-id="32d8c-2442">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="32d8c-2442">Checksum</span></span>

<span data-ttu-id="32d8c-2443">Oui</span><span class="sxs-lookup"><span data-stu-id="32d8c-2443">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="32d8c-2444">Définition</span><span class="sxs-lookup"><span data-stu-id="32d8c-2444">Definition</span></span>

<span data-ttu-id="32d8c-2445">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="32d8c-2445">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="32d8c-2446">La fonction Func_iban trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="32d8c-2446">The function Func_iban finds content that matches the pattern.</span></span>
- <span data-ttu-id="32d8c-2447">La somme de contrôle est correcte.</span><span class="sxs-lookup"><span data-stu-id="32d8c-2447">The checksum passes.</span></span>

```xml
<Entity id="e7dc4711-11b7-4cb0-b88b-2c394a771f0e" patternsProximity="300" recommendedConfidence="85">
  <Pattern confidenceLevel="85">
        <IdMatch idRef="Func_iban" />
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="32d8c-2448">Mots clés</span><span class="sxs-lookup"><span data-stu-id="32d8c-2448">Keywords</span></span>

<span data-ttu-id="32d8c-2449">Aucun</span><span class="sxs-lookup"><span data-stu-id="32d8c-2449">None</span></span>

   
## <a name="ip-address"></a><span data-ttu-id="32d8c-2450">Adresse IP</span><span class="sxs-lookup"><span data-stu-id="32d8c-2450">IP Address</span></span>

### <a name="format"></a><span data-ttu-id="32d8c-2451">Format</span><span class="sxs-lookup"><span data-stu-id="32d8c-2451">Format</span></span>

#### <a name="ipv4"></a><span data-ttu-id="32d8c-2452">IPv6</span><span class="sxs-lookup"><span data-stu-id="32d8c-2452">IPv4:</span></span>
<span data-ttu-id="32d8c-2453">Modèle complexe qui tient compte des versions mises en forme (points) et non mises en forme (sans points) des adresses IPv4</span><span class="sxs-lookup"><span data-stu-id="32d8c-2453">Complex pattern which accounts for formatted (periods) and unformatted (no periods) versions of the IPv4 addresses</span></span>

#### <a name="ipv6"></a><span data-ttu-id="32d8c-2454">IPv4/IPv6</span><span class="sxs-lookup"><span data-stu-id="32d8c-2454">IPv6:</span></span>
<span data-ttu-id="32d8c-2455"> Modèle complexe qui tient compte des numéros IPv6 mis en forme (qui incluent les signes deux-points)</span><span class="sxs-lookup"><span data-stu-id="32d8c-2455">Complex pattern which accounts for formatted IPv6 numbers (which include colons)</span></span>

### <a name="pattern"></a><span data-ttu-id="32d8c-2456">Modèle</span><span class="sxs-lookup"><span data-stu-id="32d8c-2456">Pattern</span></span>

### <a name="checksum"></a><span data-ttu-id="32d8c-2457">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="32d8c-2457">Checksum</span></span>

<span data-ttu-id="32d8c-2458">Non</span><span class="sxs-lookup"><span data-stu-id="32d8c-2458">No</span></span>

### <a name="definition"></a><span data-ttu-id="32d8c-2459">Définition</span><span class="sxs-lookup"><span data-stu-id="32d8c-2459">Definition</span></span>

<span data-ttu-id="32d8c-2460">Pour IPv6, le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="32d8c-2460">For IPv6, a DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="32d8c-2461">L’expression régulière Regex_ipv6_address trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="32d8c-2461">The regular expression Regex_ipv6_address finds content that matches the pattern.</span></span>
- <span data-ttu-id="32d8c-2462">Aucun mot clé figurant dans la liste Keyword_ipaddress n’est trouvé.</span><span class="sxs-lookup"><span data-stu-id="32d8c-2462">No keyword from Keyword_ipaddress is found.</span></span>

<span data-ttu-id="32d8c-2463">Pour IPv4, le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 95 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="32d8c-2463">For IPv4, a DLP policy is 95% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="32d8c-2464">L’expression régulière Regex_ipv4_address trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="32d8c-2464">The regular expression Regex_ipv4_address finds content that matches the pattern.</span></span>
- <span data-ttu-id="32d8c-2465">Un mot clé figurant dans la liste Keyword_ipaddress est trouvé.</span><span class="sxs-lookup"><span data-stu-id="32d8c-2465">A keyword from Keyword_ipaddress is found.</span></span>

<span data-ttu-id="32d8c-2466">Pour IPv6, le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 95 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="32d8c-2466">For IPv6, a DLP policy is 95% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="32d8c-2467">L’expression régulière Regex_ipv6_address trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="32d8c-2467">The regular expression Regex_ipv6_address finds content that matches the pattern.</span></span>
- <span data-ttu-id="32d8c-2468">Aucun mot clé figurant dans la liste Keyword_ipaddress n’est trouvé.</span><span class="sxs-lookup"><span data-stu-id="32d8c-2468">No keyword from Keyword_ipaddress is found.</span></span>

```xml
    <!-- IP Address -->
    <Entity id="1daa4ad5-e2dd-4ca4-a788-54722c09efb2" patternsProximity="300" recommendedConfidence="85">
      <Pattern confidenceLevel="85">
        <IdMatch idRef="Regex_ipv6_address" />
        <Any minMatches="0" maxMatches="0">
          <Match idRef="Keyword_ipaddress" />
        </Any>
      </Pattern>
      <Pattern confidenceLevel="95">
        <IdMatch idRef="Regex_ipv4_address" />
        <Any minMatches="1">
          <Match idRef="Keyword_ipaddress" />
        </Any>
      </Pattern>
      <Pattern confidenceLevel="95">
        <IdMatch idRef="Regex_ipv6_address" />
        <Any minMatches="1">
          <Match idRef="Keyword_ipaddress" />
        </Any>
      </Pattern>
    </Entity>
```

### <a name="keywords"></a><span data-ttu-id="32d8c-2469">Mots clés</span><span class="sxs-lookup"><span data-stu-id="32d8c-2469">Keywords</span></span>

#### <a name="keyword_ipaddress"></a><span data-ttu-id="32d8c-2470">Keyword_ipaddress</span><span class="sxs-lookup"><span data-stu-id="32d8c-2470">Keyword_ipaddress</span></span>

- <span data-ttu-id="32d8c-2471">IP (ce mot clé respecte la casse)</span><span class="sxs-lookup"><span data-stu-id="32d8c-2471">IP (this keyword is case sensitive)</span></span>
- <span data-ttu-id="32d8c-2472">ip address</span><span class="sxs-lookup"><span data-stu-id="32d8c-2472">ip address</span></span> 
- <span data-ttu-id="32d8c-2473">adresses IP</span><span class="sxs-lookup"><span data-stu-id="32d8c-2473">ip addresses</span></span>
- <span data-ttu-id="32d8c-2474">protocole internet</span><span class="sxs-lookup"><span data-stu-id="32d8c-2474">internet protocol</span></span>
- <span data-ttu-id="32d8c-2475">IP-כתובת ה</span><span class="sxs-lookup"><span data-stu-id="32d8c-2475">IP-כתובת ה</span></span> 
   
## <a name="international-classification-of-diseases-icd-10-cm"></a><span data-ttu-id="32d8c-2476">Classification internationale des maladies (ICD-10-CM)</span><span class="sxs-lookup"><span data-stu-id="32d8c-2476">International Classification of Diseases (ICD-10-CM)</span></span>

### <a name="format"></a><span data-ttu-id="32d8c-2477">Format</span><span class="sxs-lookup"><span data-stu-id="32d8c-2477">Format</span></span>

<span data-ttu-id="32d8c-2478">Dictionary</span><span class="sxs-lookup"><span data-stu-id="32d8c-2478">Dictionary</span></span>

### <a name="pattern"></a><span data-ttu-id="32d8c-2479">Modèle</span><span class="sxs-lookup"><span data-stu-id="32d8c-2479">Pattern</span></span>

<span data-ttu-id="32d8c-2480">Mot clé</span><span class="sxs-lookup"><span data-stu-id="32d8c-2480">Keyword</span></span>

### <a name="checksum"></a><span data-ttu-id="32d8c-2481">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="32d8c-2481">Checksum</span></span>

<span data-ttu-id="32d8c-2482">Non</span><span class="sxs-lookup"><span data-stu-id="32d8c-2482">No</span></span>

### <a name="definition"></a><span data-ttu-id="32d8c-2483">Définition</span><span class="sxs-lookup"><span data-stu-id="32d8c-2483">Definition</span></span>

<span data-ttu-id="32d8c-2484">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="32d8c-2484">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="32d8c-2485">Un mot clé depuis Dictionary_icd_10_updated est trouvé.</span><span class="sxs-lookup"><span data-stu-id="32d8c-2485">A keyword from Dictionary_icd_10_updated is found.</span></span>
- <span data-ttu-id="32d8c-2486">Un mot clé depuis Dictionary_icd_10_codes est trouvé.</span><span class="sxs-lookup"><span data-stu-id="32d8c-2486">A keyword from Dictionary_icd_10_codes is found.</span></span>

<span data-ttu-id="32d8c-2487">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="32d8c-2487">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="32d8c-2488">Un mot clé depuis Dictionary_icd_10_ mis à jour est trouvé.</span><span class="sxs-lookup"><span data-stu-id="32d8c-2488">A keyword from Dictionary_icd_10_ updated is found.</span></span>

```xml
      <!-- ICD-10 CM -->
      <Entity id="3356946c-6bb7-449b-b253-6ffa419c0ce7" patternsProximity="300" recommendedConfidence="85">
        <Pattern confidenceLevel="85">
          <IdMatch idRef="Dictionary_icd_10_updated" />
          <Match idRef="Dictionary_icd_10_codes" />
        </Pattern>
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Dictionary_icd_10_updated" />
        </Pattern>

```

<span data-ttu-id="32d8c-2489">Mots clés</span><span class="sxs-lookup"><span data-stu-id="32d8c-2489">Keywords</span></span>

<span data-ttu-id="32d8c-2490">Tout terme du dictionnaire de mots clés Dictionary_icd_10_updated, qui est basé sur la [Classification internationale des maladies, dixième révision, modification clinique (ICD-10-cm)](https://go.microsoft.com/fwlink/?linkid=852604).</span><span class="sxs-lookup"><span data-stu-id="32d8c-2490">Any term from the Dictionary_icd_10_updated keyword dictionary, which is based on the [International Classification of Diseases, Tenth Revision, Clinical Modification (ICD-10-CM)](https://go.microsoft.com/fwlink/?linkid=852604).</span></span> <span data-ttu-id="32d8c-2491">Ce type recherche uniquement le terme, pas les codes d’assurance.</span><span class="sxs-lookup"><span data-stu-id="32d8c-2491">This type looks only for the term, not the insurance codes.</span></span>

<span data-ttu-id="32d8c-2492">Tout terme du dictionnaire de mots clés Dictionary_icd_10_codes, qui est basé sur la [Classification internationale des maladies, dixième révision, modification clinique (ICD-10-cm)](https://go.microsoft.com/fwlink/?linkid=852604).</span><span class="sxs-lookup"><span data-stu-id="32d8c-2492">Any term from the Dictionary_icd_10_codes keyword dictionary, which is based on the [International Classification of Diseases, Tenth Revision, Clinical Modification (ICD-10-CM)](https://go.microsoft.com/fwlink/?linkid=852604).</span></span> <span data-ttu-id="32d8c-2493">Ce type recherche uniquement les codes d’assurance, pas la description.</span><span class="sxs-lookup"><span data-stu-id="32d8c-2493">This type looks only for insurance codes, not the description.</span></span>

## <a name="international-classification-of-diseases-icd-9-cm"></a><span data-ttu-id="32d8c-2494">Classification internationale des maladies (ICD-9-CM)</span><span class="sxs-lookup"><span data-stu-id="32d8c-2494">International Classification of Diseases (ICD-9-CM)</span></span>

### <a name="format"></a><span data-ttu-id="32d8c-2495">Format</span><span class="sxs-lookup"><span data-stu-id="32d8c-2495">Format</span></span>

<span data-ttu-id="32d8c-2496">Dictionary</span><span class="sxs-lookup"><span data-stu-id="32d8c-2496">Dictionary</span></span>

### <a name="pattern"></a><span data-ttu-id="32d8c-2497">Modèle</span><span class="sxs-lookup"><span data-stu-id="32d8c-2497">Pattern</span></span>

<span data-ttu-id="32d8c-2498">Mot clé</span><span class="sxs-lookup"><span data-stu-id="32d8c-2498">Keyword</span></span>

### <a name="checksum"></a><span data-ttu-id="32d8c-2499">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="32d8c-2499">Checksum</span></span>

<span data-ttu-id="32d8c-2500">Non</span><span class="sxs-lookup"><span data-stu-id="32d8c-2500">No</span></span>

### <a name="definition"></a><span data-ttu-id="32d8c-2501">Définition</span><span class="sxs-lookup"><span data-stu-id="32d8c-2501">Definition</span></span>

<span data-ttu-id="32d8c-2502">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="32d8c-2502">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="32d8c-2503">Un mot clé depuis Dictionary_icd_9_updated est trouvé.</span><span class="sxs-lookup"><span data-stu-id="32d8c-2503">A keyword from Dictionary_icd_9_updated is found.</span></span>
- <span data-ttu-id="32d8c-2504">Un mot clé depuis Dictionary_icd_9_codes est trouvé.</span><span class="sxs-lookup"><span data-stu-id="32d8c-2504">A keyword from Dictionary_icd_9_codes is found.</span></span>

<span data-ttu-id="32d8c-2505">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="32d8c-2505">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="32d8c-2506">Un mot clé depuis Dictionary_icd_9_updated est trouvé.</span><span class="sxs-lookup"><span data-stu-id="32d8c-2506">A keyword from Dictionary_icd_9_updated is found.</span></span>

```xml
    <Entity id="fa3f9c74-ee07-4c52-b5f2-085d6b2c0ec4" patternsProximity="300" recommendedConfidence="85">
        <Pattern confidenceLevel="85">
          <IdMatch idRef="Dictionary_icd_9_updated" />
          <Match idRef="Dictionary_icd_9_codes" />
        </Pattern>
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Dictionary_icd_9_updated" />
        </Pattern>
      </Entity>
```

### <a name="keywords"></a><span data-ttu-id="32d8c-2507">Mots clés</span><span class="sxs-lookup"><span data-stu-id="32d8c-2507">Keywords</span></span>

<span data-ttu-id="32d8c-2508">Tout terme du dictionnaire de mots clés Dictionary_icd_9_updated, qui est basé sur la [Classification internationale des maladies, neuvième révision, modification clinique (ICD-9-cm)](https://go.microsoft.com/fwlink/?linkid=852605).</span><span class="sxs-lookup"><span data-stu-id="32d8c-2508">Any term from the Dictionary_icd_9_updated keyword dictionary, which is based on the [International Classification of Diseases,Ninth Revision, Clinical Modification (ICD-9-CM)](https://go.microsoft.com/fwlink/?linkid=852605).</span></span> <span data-ttu-id="32d8c-2509">Ce type recherche uniquement le terme, pas les codes d’assurance.</span><span class="sxs-lookup"><span data-stu-id="32d8c-2509">This type looks only for the term, not the insurance codes.</span></span>

<span data-ttu-id="32d8c-2510">Tout terme du dictionnaire de mots clés Dictionary_icd_9_codes, qui est basé sur la [Classification internationale des maladies, neuvième révision, modification clinique (ICD-9-cm)](https://go.microsoft.com/fwlink/?linkid=852605).</span><span class="sxs-lookup"><span data-stu-id="32d8c-2510">Any term from the Dictionary_icd_9_codes keyword dictionary, which is based on the [International Classification of Diseases,Ninth Revision, Clinical Modification (ICD-9-CM)](https://go.microsoft.com/fwlink/?linkid=852605).</span></span> <span data-ttu-id="32d8c-2511">Ce type recherche uniquement les codes d’assurance, pas la description.</span><span class="sxs-lookup"><span data-stu-id="32d8c-2511">This type looks only for insurance codes, not the description.</span></span>

## <a name="ireland-personal-public-service-pps-number"></a><span data-ttu-id="32d8c-2512">Numéro de service public personnel (PPS) Irlande</span><span class="sxs-lookup"><span data-stu-id="32d8c-2512">Ireland Personal Public Service (PPS) Number</span></span>

### <a name="format"></a><span data-ttu-id="32d8c-2513">Format</span><span class="sxs-lookup"><span data-stu-id="32d8c-2513">Format</span></span>

<span data-ttu-id="32d8c-2514">Ancien format (jusqu’au 31 décembre 2012) :</span><span class="sxs-lookup"><span data-stu-id="32d8c-2514">Old format (until 31 Dec 2012):</span></span>
- <span data-ttu-id="32d8c-2515">Sept chiffres suivis de 1 ou 2 lettres </span><span class="sxs-lookup"><span data-stu-id="32d8c-2515">Seven digits followed by 1-2 letters</span></span> 

<span data-ttu-id="32d8c-2516">Nouveau format (1er janvier 2013 et après) :</span><span class="sxs-lookup"><span data-stu-id="32d8c-2516">New format (1 Jan 2013 and after):</span></span>
- <span data-ttu-id="32d8c-2517">Sept chiffres suivis de deux lettres</span><span class="sxs-lookup"><span data-stu-id="32d8c-2517">Seven digits followed by two letters</span></span>

### <a name="pattern"></a><span data-ttu-id="32d8c-2518">Modèle</span><span class="sxs-lookup"><span data-stu-id="32d8c-2518">Pattern</span></span>

<span data-ttu-id="32d8c-2519">Ancien format (jusqu’au 31 décembre 2012) :</span><span class="sxs-lookup"><span data-stu-id="32d8c-2519">Old format (until 31 Dec 2012):</span></span>
- <span data-ttu-id="32d8c-2520">Sept chiffres </span><span class="sxs-lookup"><span data-stu-id="32d8c-2520">Seven digits</span></span> 
- <span data-ttu-id="32d8c-2521">1 ou 2 lettres (ne respectant pas la casse) </span><span class="sxs-lookup"><span data-stu-id="32d8c-2521">1-2 letters (not case sensitive)</span></span> 

<span data-ttu-id="32d8c-2522">Nouveau format (1er janvier 2013 et après) :</span><span class="sxs-lookup"><span data-stu-id="32d8c-2522">New format (1 Jan 2013 and after):</span></span>
- <span data-ttu-id="32d8c-2523">Sept chiffres </span><span class="sxs-lookup"><span data-stu-id="32d8c-2523">Seven digits</span></span> 
- <span data-ttu-id="32d8c-2524">Une lettre (ne respectant pas la casse), qui est un chiffre de contrôle alphabétique </span><span class="sxs-lookup"><span data-stu-id="32d8c-2524">A letter (not case sensitive) which is an alphabetic check digit</span></span> 
- <span data-ttu-id="32d8c-2525">La lettre « A » ou « H » (ne respectant pas la casse)</span><span class="sxs-lookup"><span data-stu-id="32d8c-2525">The letter "A" or "H" (not case sensitive)</span></span>

### <a name="checksum"></a><span data-ttu-id="32d8c-2526">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="32d8c-2526">Checksum</span></span>

<span data-ttu-id="32d8c-2527">Oui</span><span class="sxs-lookup"><span data-stu-id="32d8c-2527">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="32d8c-2528">Définition</span><span class="sxs-lookup"><span data-stu-id="32d8c-2528">Definition</span></span>

<span data-ttu-id="32d8c-2529">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="32d8c-2529">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="32d8c-2530">La fonction Func_ireland_pps trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="32d8c-2530">The function Func_ireland_pps finds content that matches the pattern.</span></span>
- <span data-ttu-id="32d8c-2531">L’une des affirmations suivantes est vraie :</span><span class="sxs-lookup"><span data-stu-id="32d8c-2531">One of the following is true:</span></span>
    - <span data-ttu-id="32d8c-2532">Un mot clé figurant dans la liste Keyword_ireland_pps est trouvé.</span><span class="sxs-lookup"><span data-stu-id="32d8c-2532">A keyword from Keyword_ireland_pps is found.</span></span>
    - <span data-ttu-id="32d8c-2533">La fonction Func_eu_date trouve une date au format correct.</span><span class="sxs-lookup"><span data-stu-id="32d8c-2533">The function Func_eu_date finds a date in the right date format.</span></span>
- <span data-ttu-id="32d8c-2534">La somme de contrôle est correcte.</span><span class="sxs-lookup"><span data-stu-id="32d8c-2534">The checksum passes.</span></span>

<span data-ttu-id="32d8c-2535">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 65 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="32d8c-2535">A DLP policy is 65% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="32d8c-2536">La fonction Func_ireland_pps trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="32d8c-2536">The function Func_ireland_pps finds content that matches the pattern.</span></span>
- <span data-ttu-id="32d8c-2537">La somme de contrôle est correcte.</span><span class="sxs-lookup"><span data-stu-id="32d8c-2537">The checksum passes.</span></span>

```xml
<!-- Ireland Personal Public Service (PPS) Number -->
<Entity id="1cdb674d-c19a-4fcf-9f4b-7f56cc87345a" recommendedConfidence="85" patternsProximity="300">
  <Pattern confidenceLevel="85">
     <IdMatch idRef="Func_ireland_pps"/>
     <Any minMatches="1">
  <Match idRef="Keyword_ireland_pps"/>
  <Match idRef="Func_eu_date"/>
     </Any>
  </Pattern>
  <Pattern confidenceLevel="65">
     <IdMatch idRef="Func_ireland_pps"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="32d8c-2538">Mots clés</span><span class="sxs-lookup"><span data-stu-id="32d8c-2538">Keywords</span></span>

#### <a name="keyword_ireland_pps"></a><span data-ttu-id="32d8c-2539">Keyword_ireland_pps</span><span class="sxs-lookup"><span data-stu-id="32d8c-2539">Keyword_ireland_pps</span></span>

- <span data-ttu-id="32d8c-2540">Personal Public Service Number</span><span class="sxs-lookup"><span data-stu-id="32d8c-2540">Personal Public Service Number</span></span> 
- <span data-ttu-id="32d8c-2541">PPS Number</span><span class="sxs-lookup"><span data-stu-id="32d8c-2541">PPS Number</span></span> 
- <span data-ttu-id="32d8c-2542">PPS Num</span><span class="sxs-lookup"><span data-stu-id="32d8c-2542">PPS Num</span></span> 
- <span data-ttu-id="32d8c-2543">PPS No.</span><span class="sxs-lookup"><span data-stu-id="32d8c-2543">PPS No.</span></span> 
- <span data-ttu-id="32d8c-2544">PPS #</span><span class="sxs-lookup"><span data-stu-id="32d8c-2544">PPS #</span></span> 
- <span data-ttu-id="32d8c-2545">Spa #</span><span class="sxs-lookup"><span data-stu-id="32d8c-2545">PPS#</span></span> 
- <span data-ttu-id="32d8c-2546">PPSN</span><span class="sxs-lookup"><span data-stu-id="32d8c-2546">PPSN</span></span> 
- <span data-ttu-id="32d8c-2547">Public Services Card</span><span class="sxs-lookup"><span data-stu-id="32d8c-2547">Public Services Card</span></span> 
- <span data-ttu-id="32d8c-2548">Uimhir Phearsanta Seirbhíse Poiblí</span><span class="sxs-lookup"><span data-stu-id="32d8c-2548">Uimhir Phearsanta Seirbhíse Poiblí</span></span> 
- <span data-ttu-id="32d8c-2549">Uimh.</span><span class="sxs-lookup"><span data-stu-id="32d8c-2549">Uimh.</span></span> <span data-ttu-id="32d8c-2550">TOXINE</span><span class="sxs-lookup"><span data-stu-id="32d8c-2550">PSP</span></span> 
- <span data-ttu-id="32d8c-2551">TOXINE</span><span class="sxs-lookup"><span data-stu-id="32d8c-2551">PSP</span></span> 
   
## <a name="israel-bank-account-number"></a><span data-ttu-id="32d8c-2552">Numéro de compte bancaire Israël</span><span class="sxs-lookup"><span data-stu-id="32d8c-2552">Israel Bank Account Number</span></span>

### <a name="format"></a><span data-ttu-id="32d8c-2553">Format</span><span class="sxs-lookup"><span data-stu-id="32d8c-2553">Format</span></span>

<span data-ttu-id="32d8c-2554">13 chiffres</span><span class="sxs-lookup"><span data-stu-id="32d8c-2554">13 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="32d8c-2555">Modèle</span><span class="sxs-lookup"><span data-stu-id="32d8c-2555">Pattern</span></span>

<span data-ttu-id="32d8c-2556">Avec</span><span class="sxs-lookup"><span data-stu-id="32d8c-2556">Formatted:</span></span>
- <span data-ttu-id="32d8c-2557">Deux chiffres</span><span class="sxs-lookup"><span data-stu-id="32d8c-2557">Two digits</span></span> 
- <span data-ttu-id="32d8c-2558">Un tiret</span><span class="sxs-lookup"><span data-stu-id="32d8c-2558">A dash</span></span> 
- <span data-ttu-id="32d8c-2559">Trois chiffres</span><span class="sxs-lookup"><span data-stu-id="32d8c-2559">Three digits</span></span> 
- <span data-ttu-id="32d8c-2560">Un tiret</span><span class="sxs-lookup"><span data-stu-id="32d8c-2560">A dash</span></span> 
- <span data-ttu-id="32d8c-2561">Huit chiffres</span><span class="sxs-lookup"><span data-stu-id="32d8c-2561">Eight digits</span></span>

<span data-ttu-id="32d8c-2562">Non</span><span class="sxs-lookup"><span data-stu-id="32d8c-2562">Unformatted:</span></span>
- <span data-ttu-id="32d8c-2563">	13 chiffres consécutifs</span><span class="sxs-lookup"><span data-stu-id="32d8c-2563">13 consecutive digits</span></span>

### <a name="checksum"></a><span data-ttu-id="32d8c-2564">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="32d8c-2564">Checksum</span></span>

<span data-ttu-id="32d8c-2565">Non</span><span class="sxs-lookup"><span data-stu-id="32d8c-2565">No</span></span>

### <a name="definition"></a><span data-ttu-id="32d8c-2566">Définition</span><span class="sxs-lookup"><span data-stu-id="32d8c-2566">Definition</span></span>

<span data-ttu-id="32d8c-2567">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="32d8c-2567">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="32d8c-2568">L’expression régulière Regex_israel_bank_account_number trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="32d8c-2568">The regular expression Regex_israel_bank_account_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="32d8c-2569">Un mot clé figurant dans la liste Keyword_israel_bank_account_number est trouvé.</span><span class="sxs-lookup"><span data-stu-id="32d8c-2569">A keyword from Keyword_israel_bank_account_number is found.</span></span>

```xml
<!-- Israel Bank Account Number -->
<Entity id="7d08b2ff-a0b9-437f-957c-aeddbf9b2b25" patternsProximity="300" recommendedConfidence="75">
    <Pattern confidenceLevel="75">
        <IdMatch idRef="Regex_israel_bank_account_number" />
        <Any minMatches="1">
          <Match idRef="Keyword_israel_bank_account_number" />
        </Any>
    </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="32d8c-2570">Mots clés</span><span class="sxs-lookup"><span data-stu-id="32d8c-2570">Keywords</span></span>

#### <a name="keyword_israel_bank_account_number"></a><span data-ttu-id="32d8c-2571">Keyword_israel_bank_account_number</span><span class="sxs-lookup"><span data-stu-id="32d8c-2571">Keyword_israel_bank_account_number</span></span>

- <span data-ttu-id="32d8c-2572">Bank Account Number</span><span class="sxs-lookup"><span data-stu-id="32d8c-2572">Bank Account Number</span></span> 
- <span data-ttu-id="32d8c-2573">Bank Account</span><span class="sxs-lookup"><span data-stu-id="32d8c-2573">Bank Account</span></span> 
- <span data-ttu-id="32d8c-2574">Numéro de compte</span><span class="sxs-lookup"><span data-stu-id="32d8c-2574">Account Number</span></span> 
- <span data-ttu-id="32d8c-2575">מספר חשבון בנק</span><span class="sxs-lookup"><span data-stu-id="32d8c-2575">מספר חשבון בנק</span></span> 
   
## <a name="israel-national-id"></a><span data-ttu-id="32d8c-2576">Carte nationale d’identité Israël</span><span class="sxs-lookup"><span data-stu-id="32d8c-2576">Israel National ID</span></span>

### <a name="format"></a><span data-ttu-id="32d8c-2577">Format</span><span class="sxs-lookup"><span data-stu-id="32d8c-2577">Format</span></span>

<span data-ttu-id="32d8c-2578">Neuf chiffres</span><span class="sxs-lookup"><span data-stu-id="32d8c-2578">Nine digits</span></span>

### <a name="pattern"></a><span data-ttu-id="32d8c-2579">Modèle</span><span class="sxs-lookup"><span data-stu-id="32d8c-2579">Pattern</span></span>

<span data-ttu-id="32d8c-2580">Neuf chiffres consécutifs</span><span class="sxs-lookup"><span data-stu-id="32d8c-2580">Nine consecutive digits</span></span>

### <a name="checksum"></a><span data-ttu-id="32d8c-2581">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="32d8c-2581">Checksum</span></span>

<span data-ttu-id="32d8c-2582">Oui</span><span class="sxs-lookup"><span data-stu-id="32d8c-2582">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="32d8c-2583">Définition</span><span class="sxs-lookup"><span data-stu-id="32d8c-2583">Definition</span></span>

<span data-ttu-id="32d8c-2584">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="32d8c-2584">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="32d8c-2585">La fonction Func_israeli_national_id_number trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="32d8c-2585">The function Func_israeli_national_id_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="32d8c-2586">Un mot clé figurant dans la liste Keyword_Israel_National_ID est trouvé.</span><span class="sxs-lookup"><span data-stu-id="32d8c-2586">A keyword from Keyword_Israel_National_ID is found.</span></span>
- <span data-ttu-id="32d8c-2587">La somme de contrôle est correcte.</span><span class="sxs-lookup"><span data-stu-id="32d8c-2587">The checksum passes.</span></span>

```xml
<!-- Israel National ID Number -->
<Entity id="e05881f5-1db1-418c-89aa-a3ac5c5277ee" patternsProximity="300" recommendedConfidence="75">
    <Pattern confidenceLevel="75">
        <IdMatch idRef="Func_israeli_national_id_number" />
        <Any minMatches="1">
          <Match idRef="Keyword_Israel_National_ID" />
        </Any>
    </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="32d8c-2588">Mots clés</span><span class="sxs-lookup"><span data-stu-id="32d8c-2588">Keywords</span></span>

#### <a name="keyword_israel_national_id"></a><span data-ttu-id="32d8c-2589">Keyword_Israel_National_ID</span><span class="sxs-lookup"><span data-stu-id="32d8c-2589">Keyword_Israel_National_ID</span></span>

- <span data-ttu-id="32d8c-2590">מספר זהות</span><span class="sxs-lookup"><span data-stu-id="32d8c-2590">מספר זהות</span></span> 
- <span data-ttu-id="32d8c-2591">Numéro d’identification nationale</span><span class="sxs-lookup"><span data-stu-id="32d8c-2591">National ID Number</span></span>
   
## <a name="italy-drivers-license-number"></a><span data-ttu-id="32d8c-2592">Numéro de permis de conduire Italie</span><span class="sxs-lookup"><span data-stu-id="32d8c-2592">Italy Driver's License Number</span></span>

### <a name="format"></a><span data-ttu-id="32d8c-2593">Format</span><span class="sxs-lookup"><span data-stu-id="32d8c-2593">Format</span></span>

<span data-ttu-id="32d8c-2594">Une combinaison de 10 lettres et chiffres</span><span class="sxs-lookup"><span data-stu-id="32d8c-2594">A combination of 10 letters and digits</span></span>

### <a name="pattern"></a><span data-ttu-id="32d8c-2595">Modèle</span><span class="sxs-lookup"><span data-stu-id="32d8c-2595">Pattern</span></span>

- <span data-ttu-id="32d8c-2596">Une combinaison de 10 lettres et chiffres :</span><span class="sxs-lookup"><span data-stu-id="32d8c-2596">A combination of 10 letters and digits:</span></span>
- <span data-ttu-id="32d8c-2597">Une lettre (ne respecte pas la casse)</span><span class="sxs-lookup"><span data-stu-id="32d8c-2597">One letter (not case sensitive)</span></span> 
- <span data-ttu-id="32d8c-2598">La lettre « A » ou « V » (ne respecte pas la casse)</span><span class="sxs-lookup"><span data-stu-id="32d8c-2598">The letter "A" or "V" (not case sensitive)</span></span> 
- <span data-ttu-id="32d8c-2599">Sept lettres (ne respectent pas la casse), des chiffres ou le trait de soulignement</span><span class="sxs-lookup"><span data-stu-id="32d8c-2599">Seven letters (not case sensitive), digits, or the underscore character</span></span> 
- <span data-ttu-id="32d8c-2600">Une lettre (ne respecte pas la casse)</span><span class="sxs-lookup"><span data-stu-id="32d8c-2600">One letter (not case sensitive)</span></span>

### <a name="checksum"></a><span data-ttu-id="32d8c-2601">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="32d8c-2601">Checksum</span></span>

<span data-ttu-id="32d8c-2602">Non</span><span class="sxs-lookup"><span data-stu-id="32d8c-2602">No</span></span>

### <a name="definition"></a><span data-ttu-id="32d8c-2603">Définition</span><span class="sxs-lookup"><span data-stu-id="32d8c-2603">Definition</span></span>

<span data-ttu-id="32d8c-2604">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="32d8c-2604">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="32d8c-2605">L’expression régulière Regex_italy_drivers_license_number trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="32d8c-2605">The regular expression Regex_italy_drivers_license_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="32d8c-2606">Un mot clé figurant dans la liste Keyword_italy_drivers_license_number est trouvé.</span><span class="sxs-lookup"><span data-stu-id="32d8c-2606">A keyword from Keyword_italy_drivers_license_number is found.</span></span>

```xml
<!-- Italy Driver's license Number -->
<Entity id="97d6244f-9157-41bd-8e0c-9d669a5c4d71" patternsProximity="300" recommendedConfidence="75">
    <Pattern confidenceLevel="75">
        <IdMatch idRef="Regex_italy_drivers_license_number" />
        <Any minMatches="1">
          <Match idRef="Keyword_italy_drivers_license_number" />
        </Any>
    </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="32d8c-2607">Mots clés</span><span class="sxs-lookup"><span data-stu-id="32d8c-2607">Keywords</span></span>

#### <a name="keyword_italy_drivers_license_number"></a><span data-ttu-id="32d8c-2608">Keyword_italy_drivers_license_number</span><span class="sxs-lookup"><span data-stu-id="32d8c-2608">Keyword_italy_drivers_license_number</span></span>

- <span data-ttu-id="32d8c-2609">numero di patente di guida</span><span class="sxs-lookup"><span data-stu-id="32d8c-2609">numero di patente di guida</span></span> 
- <span data-ttu-id="32d8c-2610">patente di guida</span><span class="sxs-lookup"><span data-stu-id="32d8c-2610">patente di guida</span></span> 
   
## <a name="japan-bank-account-number"></a><span data-ttu-id="32d8c-2611">Numéro de compte bancaire Japon</span><span class="sxs-lookup"><span data-stu-id="32d8c-2611">Japan Bank Account Number</span></span>

### <a name="format"></a><span data-ttu-id="32d8c-2612">Format</span><span class="sxs-lookup"><span data-stu-id="32d8c-2612">Format</span></span>

<span data-ttu-id="32d8c-2613">Sept ou huit chiffres</span><span class="sxs-lookup"><span data-stu-id="32d8c-2613">Seven or eight digits</span></span>

### <a name="pattern"></a><span data-ttu-id="32d8c-2614">Modèle</span><span class="sxs-lookup"><span data-stu-id="32d8c-2614">Pattern</span></span>

<span data-ttu-id="32d8c-2615">Numéro de compte bancaire :</span><span class="sxs-lookup"><span data-stu-id="32d8c-2615">Bank account number:</span></span>
- <span data-ttu-id="32d8c-2616">Sept ou huit chiffres</span><span class="sxs-lookup"><span data-stu-id="32d8c-2616">Seven or eight digits</span></span>
- <span data-ttu-id="32d8c-2617">Code guichet du compte bancaire :</span><span class="sxs-lookup"><span data-stu-id="32d8c-2617">Bank account branch code:</span></span>
- <span data-ttu-id="32d8c-2618">Quatre chiffres</span><span class="sxs-lookup"><span data-stu-id="32d8c-2618">Four digits</span></span> 
- <span data-ttu-id="32d8c-2619">Un espace ou un tiret (facultatif)</span><span class="sxs-lookup"><span data-stu-id="32d8c-2619">A space or dash (optional)</span></span> 
- <span data-ttu-id="32d8c-2620">Trois chiffres</span><span class="sxs-lookup"><span data-stu-id="32d8c-2620">Three digits</span></span>

<span data-ttu-id="32d8c-2621">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="32d8c-2621">Checksum</span></span>

<span data-ttu-id="32d8c-2622">Non</span><span class="sxs-lookup"><span data-stu-id="32d8c-2622">No</span></span>

### <a name="definition"></a><span data-ttu-id="32d8c-2623">Définition</span><span class="sxs-lookup"><span data-stu-id="32d8c-2623">Definition</span></span>

<span data-ttu-id="32d8c-2624">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="32d8c-2624">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="32d8c-2625">La fonction Func_jp_bank_account trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="32d8c-2625">The function Func_jp_bank_account finds content that matches the pattern.</span></span>
- <span data-ttu-id="32d8c-2626">Un mot clé figurant dans la liste Keyword_jp_bank_account est trouvé.</span><span class="sxs-lookup"><span data-stu-id="32d8c-2626">A keyword from Keyword_jp_bank_account is found.</span></span>
- <span data-ttu-id="32d8c-2627">L’une des affirmations suivantes est vraie :</span><span class="sxs-lookup"><span data-stu-id="32d8c-2627">One of the following is true:</span></span>
- <span data-ttu-id="32d8c-2628">La fonction Func_jp_bank_account_branch_code trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="32d8c-2628">The function Func_jp_bank_account_branch_code finds content that matches the pattern.</span></span>
- <span data-ttu-id="32d8c-2629">Un mot clé figurant dans la liste Keyword_jp_bank_branch_code est trouvé.</span><span class="sxs-lookup"><span data-stu-id="32d8c-2629">A keyword from Keyword_jp_bank_branch_code is found.</span></span>

<span data-ttu-id="32d8c-2630">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="32d8c-2630">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="32d8c-2631">La fonction Func_jp_bank_account trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="32d8c-2631">The function Func_jp_bank_account finds content that matches the pattern.</span></span>
- <span data-ttu-id="32d8c-2632">Un mot clé figurant dans la liste Keyword_jp_bank_account est trouvé.</span><span class="sxs-lookup"><span data-stu-id="32d8c-2632">A keyword from Keyword_jp_bank_account is found.</span></span>

```xml
<!-- Japan Bank Account Number -->
<Entity id="d354f95b-96ee-4b80-80bc-4377312b55bc" patternsProximity="300" recommendedConfidence="75">
  <Version minEngineVersion="15.01.0131.000">
    <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_jp_bank_account" />
          <Match idRef="Keyword_jp_bank_account" />
          <Any minMatches="1">
            <Match idRef="Func_jp_bank_account_branch_code" />
            <Match idRef="Keyword_jp_bank_branch_code" />
          </Any>
      </Pattern>
  </Version>    
     <Pattern confidenceLevel="75">
        <IdMatch idRef="Func_jp_bank_account" />
        <Match idRef="Keyword_jp_bank_account" />
    </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="32d8c-2633">Mots clés</span><span class="sxs-lookup"><span data-stu-id="32d8c-2633">Keywords</span></span>

#### <a name="keyword_jp_bank_account"></a><span data-ttu-id="32d8c-2634">Keyword_jp_bank_account</span><span class="sxs-lookup"><span data-stu-id="32d8c-2634">Keyword_jp_bank_account</span></span>

- <span data-ttu-id="32d8c-2635">Numéro de compte courant</span><span class="sxs-lookup"><span data-stu-id="32d8c-2635">Checking Account Number</span></span> 
- <span data-ttu-id="32d8c-2636">Compte courant</span><span class="sxs-lookup"><span data-stu-id="32d8c-2636">Checking Account</span></span> 
- <span data-ttu-id="32d8c-2637"># compte courant</span><span class="sxs-lookup"><span data-stu-id="32d8c-2637">Checking Account #</span></span> 
- <span data-ttu-id="32d8c-2638">Numéro compte courant</span><span class="sxs-lookup"><span data-stu-id="32d8c-2638">Checking Acct Number</span></span> 
- <span data-ttu-id="32d8c-2639"># compte courant</span><span class="sxs-lookup"><span data-stu-id="32d8c-2639">Checking Acct #</span></span> 
- <span data-ttu-id="32d8c-2640">N° de compte courant</span><span class="sxs-lookup"><span data-stu-id="32d8c-2640">Checking Acct No.</span></span> 
- <span data-ttu-id="32d8c-2641">N° de compte courant</span><span class="sxs-lookup"><span data-stu-id="32d8c-2641">Checking Account No.</span></span> 
- <span data-ttu-id="32d8c-2642">Numéro de compte bancaire</span><span class="sxs-lookup"><span data-stu-id="32d8c-2642">Bank Account Number</span></span> 
- <span data-ttu-id="32d8c-2643">Compte bancaire</span><span class="sxs-lookup"><span data-stu-id="32d8c-2643">Bank Account</span></span> 
- <span data-ttu-id="32d8c-2644"># Compte bancaire</span><span class="sxs-lookup"><span data-stu-id="32d8c-2644">Bank Account #</span></span> 
- <span data-ttu-id="32d8c-2645">Numéro de compte bancaire</span><span class="sxs-lookup"><span data-stu-id="32d8c-2645">Bank Acct Number</span></span> 
- <span data-ttu-id="32d8c-2646"># Compte bancaire</span><span class="sxs-lookup"><span data-stu-id="32d8c-2646">Bank Acct #</span></span> 
- <span data-ttu-id="32d8c-2647">N° de compte bancaire</span><span class="sxs-lookup"><span data-stu-id="32d8c-2647">Bank Acct No.</span></span> 
- <span data-ttu-id="32d8c-2648">N° de compte bancaire</span><span class="sxs-lookup"><span data-stu-id="32d8c-2648">Bank Account No.</span></span> 
- <span data-ttu-id="32d8c-2649">Numéro de compte d’épargne</span><span class="sxs-lookup"><span data-stu-id="32d8c-2649">Savings Account Number</span></span> 
- <span data-ttu-id="32d8c-2650">Compte d’épargne</span><span class="sxs-lookup"><span data-stu-id="32d8c-2650">Savings Account</span></span> 
- <span data-ttu-id="32d8c-2651">N° de compte d’épargne</span><span class="sxs-lookup"><span data-stu-id="32d8c-2651">Savings Account #</span></span> 
- <span data-ttu-id="32d8c-2652">Numéro de compte d’épargne</span><span class="sxs-lookup"><span data-stu-id="32d8c-2652">Savings Acct Number</span></span> 
- <span data-ttu-id="32d8c-2653"># compte d’épargne</span><span class="sxs-lookup"><span data-stu-id="32d8c-2653">Savings Acct #</span></span> 
- <span data-ttu-id="32d8c-2654">N° de compte d’épargne</span><span class="sxs-lookup"><span data-stu-id="32d8c-2654">Savings Acct No.</span></span> 
- <span data-ttu-id="32d8c-2655">N° de compte d’épargne</span><span class="sxs-lookup"><span data-stu-id="32d8c-2655">Savings Account No.</span></span> 
- <span data-ttu-id="32d8c-2656">Numéro de compte de débit</span><span class="sxs-lookup"><span data-stu-id="32d8c-2656">Debit Account Number</span></span> 
- <span data-ttu-id="32d8c-2657">Compte de débit</span><span class="sxs-lookup"><span data-stu-id="32d8c-2657">Debit Account</span></span> 
- <span data-ttu-id="32d8c-2658"># Compte de débit</span><span class="sxs-lookup"><span data-stu-id="32d8c-2658">Debit Account #</span></span> 
- <span data-ttu-id="32d8c-2659">Numéro de compte de débit</span><span class="sxs-lookup"><span data-stu-id="32d8c-2659">Debit Acct Number</span></span> 
- <span data-ttu-id="32d8c-2660"># Compte de débit</span><span class="sxs-lookup"><span data-stu-id="32d8c-2660">Debit Acct #</span></span> 
- <span data-ttu-id="32d8c-2661">N° de compte de débit</span><span class="sxs-lookup"><span data-stu-id="32d8c-2661">Debit Acct No.</span></span> 
- <span data-ttu-id="32d8c-2662">N° de compte de débit</span><span class="sxs-lookup"><span data-stu-id="32d8c-2662">Debit Account No.</span></span> 
- <span data-ttu-id="32d8c-2663">口座番号を当座預金口座の確認</span><span class="sxs-lookup"><span data-stu-id="32d8c-2663">口座番号を当座預金口座の確認</span></span> 
- <span data-ttu-id="32d8c-2664">#アカウントの確認 、 勘定番号の確認</span><span class="sxs-lookup"><span data-stu-id="32d8c-2664">＃アカウントの確認、勘定番号の確認</span></span> 
- <span data-ttu-id="32d8c-2665">#勘定の確認</span><span class="sxs-lookup"><span data-stu-id="32d8c-2665">＃勘定の確認</span></span> 
- <span data-ttu-id="32d8c-2666">勘定番号の確認</span><span class="sxs-lookup"><span data-stu-id="32d8c-2666">勘定番号の確認</span></span> 
- <span data-ttu-id="32d8c-2667">口座番号の確認</span><span class="sxs-lookup"><span data-stu-id="32d8c-2667">口座番号の確認</span></span> 
- <span data-ttu-id="32d8c-2668">銀行口座番号</span><span class="sxs-lookup"><span data-stu-id="32d8c-2668">銀行口座番号</span></span> 
- <span data-ttu-id="32d8c-2669">銀行口座</span><span class="sxs-lookup"><span data-stu-id="32d8c-2669">銀行口座</span></span> 
- <span data-ttu-id="32d8c-2670">銀行口座＃</span><span class="sxs-lookup"><span data-stu-id="32d8c-2670">銀行口座＃</span></span> 
- <span data-ttu-id="32d8c-2671">銀行の勘定番号</span><span class="sxs-lookup"><span data-stu-id="32d8c-2671">銀行の勘定番号</span></span> 
- <span data-ttu-id="32d8c-2672">銀行のacct＃</span><span class="sxs-lookup"><span data-stu-id="32d8c-2672">銀行のacct＃</span></span> 
- <span data-ttu-id="32d8c-2673">銀行の勘定いいえ</span><span class="sxs-lookup"><span data-stu-id="32d8c-2673">銀行の勘定いいえ</span></span> 
- <span data-ttu-id="32d8c-2674">銀行口座番号</span><span class="sxs-lookup"><span data-stu-id="32d8c-2674">銀行口座番号</span></span>
- <span data-ttu-id="32d8c-2675">普通預金口座番号</span><span class="sxs-lookup"><span data-stu-id="32d8c-2675">普通預金口座番号</span></span> 
- <span data-ttu-id="32d8c-2676">預金口座</span><span class="sxs-lookup"><span data-stu-id="32d8c-2676">預金口座</span></span> 
- <span data-ttu-id="32d8c-2677">貯蓄口座＃</span><span class="sxs-lookup"><span data-stu-id="32d8c-2677">貯蓄口座＃</span></span> 
- <span data-ttu-id="32d8c-2678">貯蓄勘定の数</span><span class="sxs-lookup"><span data-stu-id="32d8c-2678">貯蓄勘定の数</span></span> 
- <span data-ttu-id="32d8c-2679">貯蓄勘定＃</span><span class="sxs-lookup"><span data-stu-id="32d8c-2679">貯蓄勘定＃</span></span> 
- <span data-ttu-id="32d8c-2680">貯蓄勘定番号</span><span class="sxs-lookup"><span data-stu-id="32d8c-2680">貯蓄勘定番号</span></span> 
- <span data-ttu-id="32d8c-2681">普通預金口座番号</span><span class="sxs-lookup"><span data-stu-id="32d8c-2681">普通預金口座番号</span></span> 
- <span data-ttu-id="32d8c-2682">引き落とし口座番号</span><span class="sxs-lookup"><span data-stu-id="32d8c-2682">引き落とし口座番号</span></span> 
- <span data-ttu-id="32d8c-2683">口座番号</span><span class="sxs-lookup"><span data-stu-id="32d8c-2683">口座番号</span></span> 
- <span data-ttu-id="32d8c-2684">口座番号＃</span><span class="sxs-lookup"><span data-stu-id="32d8c-2684">口座番号＃</span></span> 
- <span data-ttu-id="32d8c-2685">デビットのacct番号</span><span class="sxs-lookup"><span data-stu-id="32d8c-2685">デビットのacct番号</span></span> 
- <span data-ttu-id="32d8c-2686">デビット勘定＃</span><span class="sxs-lookup"><span data-stu-id="32d8c-2686">デビット勘定＃</span></span> 
- <span data-ttu-id="32d8c-2687">デビットACCTの番号</span><span class="sxs-lookup"><span data-stu-id="32d8c-2687">デビットACCTの番号</span></span> 
- <span data-ttu-id="32d8c-2688">デビット口座番号</span><span class="sxs-lookup"><span data-stu-id="32d8c-2688">デビット口座番号</span></span> 

#### <a name="keyword_jp_bank_branch_code"></a><span data-ttu-id="32d8c-2689">Keyword_jp_bank_branch_code</span><span class="sxs-lookup"><span data-stu-id="32d8c-2689">Keyword_jp_bank_branch_code</span></span>

<span data-ttu-id="32d8c-2690">Otemachi</span><span class="sxs-lookup"><span data-stu-id="32d8c-2690">Otemachi</span></span>

## <a name="japan-drivers-license-number"></a><span data-ttu-id="32d8c-2691">Numéro de permis de conduire Japon</span><span class="sxs-lookup"><span data-stu-id="32d8c-2691">Japan Driver's License Number</span></span>

### <a name="format"></a><span data-ttu-id="32d8c-2692">Format</span><span class="sxs-lookup"><span data-stu-id="32d8c-2692">Format</span></span>

<span data-ttu-id="32d8c-2693">12 chiffres</span><span class="sxs-lookup"><span data-stu-id="32d8c-2693">12 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="32d8c-2694">Modèle</span><span class="sxs-lookup"><span data-stu-id="32d8c-2694">Pattern</span></span>

<span data-ttu-id="32d8c-2695">12 chiffres consécutifs</span><span class="sxs-lookup"><span data-stu-id="32d8c-2695">12 consecutive digits</span></span>

### <a name="checksum"></a><span data-ttu-id="32d8c-2696">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="32d8c-2696">Checksum</span></span>

<span data-ttu-id="32d8c-2697">Non</span><span class="sxs-lookup"><span data-stu-id="32d8c-2697">No</span></span>

### <a name="definition"></a><span data-ttu-id="32d8c-2698">Définition</span><span class="sxs-lookup"><span data-stu-id="32d8c-2698">Definition</span></span>

<span data-ttu-id="32d8c-2699">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="32d8c-2699">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="32d8c-2700">La fonction Func_jp_drivers_license_number trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="32d8c-2700">The function Func_jp_drivers_license_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="32d8c-2701">Un mot clé figurant dans la liste Keyword_jp_drivers_license_number est trouvé.</span><span class="sxs-lookup"><span data-stu-id="32d8c-2701">A keyword from Keyword_jp_drivers_license_number is found.</span></span>

```xml
<!-- Japan Driver's License Number -->
<Entity id="c6011143-d087-451c-8313-7f6d4aed2270" patternsProximity="300" recommendedConfidence="75">
    <Pattern confidenceLevel="75">
        <IdMatch idRef="Func_jp_drivers_license_number" />
        <Match idRef ="Keyword_jp_drivers_license_number" />
    </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="32d8c-2702">Mots clés</span><span class="sxs-lookup"><span data-stu-id="32d8c-2702">Keywords</span></span>

#### <a name="keyword_jp_drivers_license_number"></a><span data-ttu-id="32d8c-2703">Keyword_jp_drivers_license_number</span><span class="sxs-lookup"><span data-stu-id="32d8c-2703">Keyword_jp_drivers_license_number</span></span>

- <span data-ttu-id="32d8c-2704">LD #</span><span class="sxs-lookup"><span data-stu-id="32d8c-2704">dl#</span></span> 
- <span data-ttu-id="32d8c-2705">LD</span><span class="sxs-lookup"><span data-stu-id="32d8c-2705">DL＃</span></span> 
- <span data-ttu-id="32d8c-2706">distribution #</span><span class="sxs-lookup"><span data-stu-id="32d8c-2706">dls#</span></span> 
- <span data-ttu-id="32d8c-2707">DISTRIBUTION</span><span class="sxs-lookup"><span data-stu-id="32d8c-2707">DLS＃</span></span> 
- <span data-ttu-id="32d8c-2708">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="32d8c-2708">driver license</span></span> 
- <span data-ttu-id="32d8c-2709">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="32d8c-2709">driver licenses</span></span> 
- <span data-ttu-id="32d8c-2710">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="32d8c-2710">drivers license</span></span> 
- <span data-ttu-id="32d8c-2711">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="32d8c-2711">driver's license</span></span> 
- <span data-ttu-id="32d8c-2712">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="32d8c-2712">drivers licenses</span></span> 
- <span data-ttu-id="32d8c-2713">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="32d8c-2713">driver's licenses</span></span> 
- <span data-ttu-id="32d8c-2714">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="32d8c-2714">driving licence</span></span> 
- <span data-ttu-id="32d8c-2715">Profil #</span><span class="sxs-lookup"><span data-stu-id="32d8c-2715">lic#</span></span> 
- <span data-ttu-id="32d8c-2716">Profil</span><span class="sxs-lookup"><span data-stu-id="32d8c-2716">LIC＃</span></span> 
- <span data-ttu-id="32d8c-2717">conduire #</span><span class="sxs-lookup"><span data-stu-id="32d8c-2717">lics#</span></span> 
- <span data-ttu-id="32d8c-2718">id d’état</span><span class="sxs-lookup"><span data-stu-id="32d8c-2718">state id</span></span> 
- <span data-ttu-id="32d8c-2719">identification d’état</span><span class="sxs-lookup"><span data-stu-id="32d8c-2719">state identification</span></span> 
- <span data-ttu-id="32d8c-2720">numéro d’identification d’état</span><span class="sxs-lookup"><span data-stu-id="32d8c-2720">state identification number</span></span> 
- <span data-ttu-id="32d8c-2721">低所得国＃</span><span class="sxs-lookup"><span data-stu-id="32d8c-2721">低所得国＃</span></span> 
- <span data-ttu-id="32d8c-2722">免許証</span><span class="sxs-lookup"><span data-stu-id="32d8c-2722">免許証</span></span> 
- <span data-ttu-id="32d8c-2723">状態ID</span><span class="sxs-lookup"><span data-stu-id="32d8c-2723">状態ID</span></span>
- <span data-ttu-id="32d8c-2724">状態の識別</span><span class="sxs-lookup"><span data-stu-id="32d8c-2724">状態の識別</span></span> 
- <span data-ttu-id="32d8c-2725">状態の識別番号</span><span class="sxs-lookup"><span data-stu-id="32d8c-2725">状態の識別番号</span></span> 
- <span data-ttu-id="32d8c-2726">運転免許</span><span class="sxs-lookup"><span data-stu-id="32d8c-2726">運転免許</span></span> 
- <span data-ttu-id="32d8c-2727">運転免許証</span><span class="sxs-lookup"><span data-stu-id="32d8c-2727">運転免許証</span></span> 
- <span data-ttu-id="32d8c-2728">運転免許証番号</span><span class="sxs-lookup"><span data-stu-id="32d8c-2728">運転免許証番号</span></span> 
   
## <a name="japan-passport-number"></a><span data-ttu-id="32d8c-2729">Numéro de passeport Japon</span><span class="sxs-lookup"><span data-stu-id="32d8c-2729">Japan Passport Number</span></span>

### <a name="format"></a><span data-ttu-id="32d8c-2730">Format</span><span class="sxs-lookup"><span data-stu-id="32d8c-2730">Format</span></span>

<span data-ttu-id="32d8c-2731">Deux lettres suivies de sept chiffres</span><span class="sxs-lookup"><span data-stu-id="32d8c-2731">Two letters followed by seven digits</span></span>

### <a name="pattern"></a><span data-ttu-id="32d8c-2732">Modèle</span><span class="sxs-lookup"><span data-stu-id="32d8c-2732">Pattern</span></span>

<span data-ttu-id="32d8c-2733">Deux lettres (ne respectant pas la casse) suivies de sept chiffres</span><span class="sxs-lookup"><span data-stu-id="32d8c-2733">Two letters (not case sensitive) followed by seven digits</span></span>

### <a name="checksum"></a><span data-ttu-id="32d8c-2734">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="32d8c-2734">Checksum</span></span>

<span data-ttu-id="32d8c-2735">Non</span><span class="sxs-lookup"><span data-stu-id="32d8c-2735">No</span></span>

### <a name="definition"></a><span data-ttu-id="32d8c-2736">Définition</span><span class="sxs-lookup"><span data-stu-id="32d8c-2736">Definition</span></span>

<span data-ttu-id="32d8c-2737">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="32d8c-2737">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="32d8c-2738">La fonction Func_jp_passport trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="32d8c-2738">The function Func_jp_passport finds content that matches the pattern.</span></span>
- <span data-ttu-id="32d8c-2739">Un mot clé figurant dans la liste Keyword_jp_passport est trouvé.</span><span class="sxs-lookup"><span data-stu-id="32d8c-2739">A keyword from Keyword_jp_passport is found.</span></span>

```xml
<!-- Japan Passport Number -->
<Entity id="75177310-1a09-4613-bf6d-833aae3743f8" patternsProximity="300" recommendedConfidence="75">
    <Pattern confidenceLevel="75">
        <IdMatch idRef="Func_jp_passport" />
        <Match idRef="Keyword_jp_passport" />
    </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="32d8c-2740">Mots clés</span><span class="sxs-lookup"><span data-stu-id="32d8c-2740">Keywords</span></span>

#### <a name="keyword_jp_passport"></a><span data-ttu-id="32d8c-2741">Keyword_jp_passport</span><span class="sxs-lookup"><span data-stu-id="32d8c-2741">Keyword_jp_passport</span></span>

- <span data-ttu-id="32d8c-2742">パスポート</span><span class="sxs-lookup"><span data-stu-id="32d8c-2742">パスポート</span></span> 
- <span data-ttu-id="32d8c-2743">パスポート番号</span><span class="sxs-lookup"><span data-stu-id="32d8c-2743">パスポート番号</span></span> 
- <span data-ttu-id="32d8c-2744">パスポートのNum</span><span class="sxs-lookup"><span data-stu-id="32d8c-2744">パスポートのNum</span></span> 
- <span data-ttu-id="32d8c-2745">パスポート＃</span><span class="sxs-lookup"><span data-stu-id="32d8c-2745">パスポート＃</span></span> 
   
## <a name="japan-resident-registration-number"></a><span data-ttu-id="32d8c-2746">Matricule de résident Japon</span><span class="sxs-lookup"><span data-stu-id="32d8c-2746">Japan Resident Registration Number</span></span>

### <a name="format"></a><span data-ttu-id="32d8c-2747">Format</span><span class="sxs-lookup"><span data-stu-id="32d8c-2747">Format</span></span>

<span data-ttu-id="32d8c-2748">11 chiffres</span><span class="sxs-lookup"><span data-stu-id="32d8c-2748">11 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="32d8c-2749">Modèle</span><span class="sxs-lookup"><span data-stu-id="32d8c-2749">Pattern</span></span>

<span data-ttu-id="32d8c-2750">11 chiffres consécutifs</span><span class="sxs-lookup"><span data-stu-id="32d8c-2750">11 consecutive digits</span></span>

### <a name="checksum"></a><span data-ttu-id="32d8c-2751">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="32d8c-2751">Checksum</span></span>

<span data-ttu-id="32d8c-2752">Non</span><span class="sxs-lookup"><span data-stu-id="32d8c-2752">No</span></span>

### <a name="definition"></a><span data-ttu-id="32d8c-2753">Définition</span><span class="sxs-lookup"><span data-stu-id="32d8c-2753">Definition</span></span>

<span data-ttu-id="32d8c-2754">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="32d8c-2754">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="32d8c-2755">La fonction Func_jp_resident_registration_number trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="32d8c-2755">The function Func_jp_resident_registration_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="32d8c-2756">Un mot clé figurant dans la liste Keyword_jp_resident_registration_number est trouvé.</span><span class="sxs-lookup"><span data-stu-id="32d8c-2756">A keyword from Keyword_jp_resident_registration_number is found.</span></span>

```xml
<!-- Japan Resident Registration Number -->
<Entity id="01c1209b-6389-4faf-a5f8-3f7e13899652" patternsProximity="300" recommendedConfidence="75">
    <Pattern confidenceLevel="75">
        <IdMatch idRef="Func_jp_resident_registration_number" />
        <Match idRef ="Keyword_jp_resident_registration_number" />
    </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="32d8c-2757">Mots clés</span><span class="sxs-lookup"><span data-stu-id="32d8c-2757">Keywords</span></span>

#### <a name="keyword_jp_resident_registration_number"></a><span data-ttu-id="32d8c-2758">Keyword_jp_resident_registration_number</span><span class="sxs-lookup"><span data-stu-id="32d8c-2758">Keyword_jp_resident_registration_number</span></span>

- <span data-ttu-id="32d8c-2759">Numéro d’enregistrement du résident</span><span class="sxs-lookup"><span data-stu-id="32d8c-2759">Resident Registration Number</span></span>
- <span data-ttu-id="32d8c-2760">Numéro d’enregistrement du résident</span><span class="sxs-lookup"><span data-stu-id="32d8c-2760">Resident Register Number</span></span> 
- <span data-ttu-id="32d8c-2761">Numéro de base d’enregistrement des résidents</span><span class="sxs-lookup"><span data-stu-id="32d8c-2761">Residents Basic Registry Number</span></span> 
- <span data-ttu-id="32d8c-2762">N° d’enregistrement du résident</span><span class="sxs-lookup"><span data-stu-id="32d8c-2762">Resident Registration No.</span></span> 
- <span data-ttu-id="32d8c-2763">N° d’enregistrement du résident</span><span class="sxs-lookup"><span data-stu-id="32d8c-2763">Resident Register No.</span></span> 
- <span data-ttu-id="32d8c-2764">N° de base d’enregistrement des résidents</span><span class="sxs-lookup"><span data-stu-id="32d8c-2764">Residents Basic Registry No.</span></span> 
- <span data-ttu-id="32d8c-2765">N° d’enregistrement du résident de base</span><span class="sxs-lookup"><span data-stu-id="32d8c-2765">Basic Resident Register No.</span></span> 
- <span data-ttu-id="32d8c-2766">住民登録番号、登録番号をレジデント</span><span class="sxs-lookup"><span data-stu-id="32d8c-2766">住民登録番号、登録番号をレジデント</span></span> 
- <span data-ttu-id="32d8c-2767">住民基本登録番号、登録番号</span><span class="sxs-lookup"><span data-stu-id="32d8c-2767">住民基本登録番号、登録番号</span></span> 
- <span data-ttu-id="32d8c-2768">住民基本レジストリ番号を常駐</span><span class="sxs-lookup"><span data-stu-id="32d8c-2768">住民基本レジストリ番号を常駐</span></span> 
- <span data-ttu-id="32d8c-2769">登録番号を常駐住民基本台帳登録番号</span><span class="sxs-lookup"><span data-stu-id="32d8c-2769">登録番号を常駐住民基本台帳登録番号</span></span> 

   
## <a name="japan-social-insurance-number-sin"></a><span data-ttu-id="32d8c-2770">Numéro d’assurance sociale Japon</span><span class="sxs-lookup"><span data-stu-id="32d8c-2770">Japan Social Insurance Number (SIN)</span></span>

### <a name="format"></a><span data-ttu-id="32d8c-2771">Format</span><span class="sxs-lookup"><span data-stu-id="32d8c-2771">Format</span></span>

<span data-ttu-id="32d8c-2772">7 à 12 chiffres</span><span class="sxs-lookup"><span data-stu-id="32d8c-2772">7-12 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="32d8c-2773">Modèle</span><span class="sxs-lookup"><span data-stu-id="32d8c-2773">Pattern</span></span>

<span data-ttu-id="32d8c-2774">7 à 12 chiffres :</span><span class="sxs-lookup"><span data-stu-id="32d8c-2774">7-12 digits:</span></span>
- <span data-ttu-id="32d8c-2775">Quatre chiffres</span><span class="sxs-lookup"><span data-stu-id="32d8c-2775">Four digits</span></span> 
- <span data-ttu-id="32d8c-2776">Un trait d’union (facultatif)</span><span class="sxs-lookup"><span data-stu-id="32d8c-2776">A hyphen (optional)</span></span> 
- <span data-ttu-id="32d8c-2777">Six chiffres ou</span><span class="sxs-lookup"><span data-stu-id="32d8c-2777">Six digits OR</span></span>
- <span data-ttu-id="32d8c-2778">7 à 12 chiffres consécutifs</span><span class="sxs-lookup"><span data-stu-id="32d8c-2778">7-12 consecutive digits</span></span>

### <a name="checksum"></a><span data-ttu-id="32d8c-2779">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="32d8c-2779">Checksum</span></span>

<span data-ttu-id="32d8c-2780">Non</span><span class="sxs-lookup"><span data-stu-id="32d8c-2780">No</span></span>

### <a name="definition"></a><span data-ttu-id="32d8c-2781">Définition</span><span class="sxs-lookup"><span data-stu-id="32d8c-2781">Definition</span></span>

<span data-ttu-id="32d8c-2782">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="32d8c-2782">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="32d8c-2783">La fonction Func_jp_sin trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="32d8c-2783">The function Func_jp_sin finds content that matches the pattern.</span></span>
- <span data-ttu-id="32d8c-2784">Un mot clé figurant dans la liste Keyword_jp_sin est trouvé.</span><span class="sxs-lookup"><span data-stu-id="32d8c-2784">A keyword from Keyword_jp_sin is found.</span></span>

<span data-ttu-id="32d8c-2785">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="32d8c-2785">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="32d8c-2786">La fonction Func_jp_sin_pre_1997 trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="32d8c-2786">The function Func_jp_sin_pre_1997 finds content that matches the pattern.</span></span>
- <span data-ttu-id="32d8c-2787">Un mot clé figurant dans la liste Keyword_jp_sin est trouvé.</span><span class="sxs-lookup"><span data-stu-id="32d8c-2787">A keyword from Keyword_jp_sin is found.</span></span>

```xml
<!-- Japan Social Insurance Number -->
<Entity id="c840e719-0896-45bb-84fd-1ed5c95e45ff" patternsProximity="300" recommendedConfidence="75">
    <Pattern confidenceLevel="85">
        <IdMatch idRef="Func_jp_sin" />
        <Match idRef="Keyword_jp_sin" />
    </Pattern>
    <Pattern confidenceLevel="75">
        <IdMatch idRef="Func_jp_sin_pre_1997" />
        <Match idRef="Keyword_jp_sin" />
    </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="32d8c-2788">Mots clés</span><span class="sxs-lookup"><span data-stu-id="32d8c-2788">Keywords</span></span>

#### <a name="keyword_jp_sin"></a><span data-ttu-id="32d8c-2789">Keyword_jp_sin</span><span class="sxs-lookup"><span data-stu-id="32d8c-2789">Keyword_jp_sin</span></span>

- <span data-ttu-id="32d8c-2790">N° d’assurance sociale</span><span class="sxs-lookup"><span data-stu-id="32d8c-2790">Social Insurance No.</span></span> 
- <span data-ttu-id="32d8c-2791">Numéro d’assurance sociale</span><span class="sxs-lookup"><span data-stu-id="32d8c-2791">Social Insurance Num</span></span> 
- <span data-ttu-id="32d8c-2792">Numéro d’assurance sociale</span><span class="sxs-lookup"><span data-stu-id="32d8c-2792">Social Insurance Number</span></span> 
- <span data-ttu-id="32d8c-2793">社会保険のテンキー</span><span class="sxs-lookup"><span data-stu-id="32d8c-2793">社会保険のテンキー</span></span> 
- <span data-ttu-id="32d8c-2794">社会保険番号</span><span class="sxs-lookup"><span data-stu-id="32d8c-2794">社会保険番号</span></span> 

## <a name="japanese-residence-card-number"></a><span data-ttu-id="32d8c-2795">Numéro de carte de séjour japonaise</span><span class="sxs-lookup"><span data-stu-id="32d8c-2795">Japanese Residence Card Number</span></span>

### <a name="format"></a><span data-ttu-id="32d8c-2796">Format</span><span class="sxs-lookup"><span data-stu-id="32d8c-2796">Format</span></span>

<span data-ttu-id="32d8c-2797">12 lettres et chiffres</span><span class="sxs-lookup"><span data-stu-id="32d8c-2797">12 letters and digits</span></span>

### <a name="pattern"></a><span data-ttu-id="32d8c-2798">Modèle</span><span class="sxs-lookup"><span data-stu-id="32d8c-2798">Pattern</span></span>

<span data-ttu-id="32d8c-2799">12 lettres et chiffres :</span><span class="sxs-lookup"><span data-stu-id="32d8c-2799">12 letters and digits:</span></span>
- <span data-ttu-id="32d8c-2800">Deux lettres (ne respectant pas la casse) </span><span class="sxs-lookup"><span data-stu-id="32d8c-2800">Two letters (not case sensitive)</span></span>
- <span data-ttu-id="32d8c-2801">Huit chiffres</span><span class="sxs-lookup"><span data-stu-id="32d8c-2801">Eight digits</span></span> 
- <span data-ttu-id="32d8c-2802">Deux lettres (ne respectant pas la casse) </span><span class="sxs-lookup"><span data-stu-id="32d8c-2802">Two letters (not case sensitive)</span></span>

### <a name="checksum"></a><span data-ttu-id="32d8c-2803">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="32d8c-2803">Checksum</span></span>

<span data-ttu-id="32d8c-2804">Non</span><span class="sxs-lookup"><span data-stu-id="32d8c-2804">No</span></span>

### <a name="definition"></a><span data-ttu-id="32d8c-2805">Définition</span><span class="sxs-lookup"><span data-stu-id="32d8c-2805">Definition</span></span>

<span data-ttu-id="32d8c-2806">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="32d8c-2806">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="32d8c-2807">L’expression régulière Regex_jp_residence_card_number trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="32d8c-2807">The regular expression Regex_jp_residence_card_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="32d8c-2808">Un mot clé depuis Keyword_jp_residence_card_number est trouvé.</span><span class="sxs-lookup"><span data-stu-id="32d8c-2808">A keyword from Keyword_jp_residence_card_number is found.</span></span>

```xml
<!--Japan Residence Card Number-->
-<Entity id="ac36fef2-a289-4e2c-bb48-b02366e89fc0" recommendedConfidence="75" patternsProximity="300">
   -<Pattern confidenceLevel="75">
      <IdMatch idRef="Regex_jp_residence_card_number"/>
      <Match idRef="Keyword_jp_residence_card_number"/>
   </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="32d8c-2809">Mots clés</span><span class="sxs-lookup"><span data-stu-id="32d8c-2809">Keywords</span></span>

#### <a name="keyword_jp_residence_card_number"></a><span data-ttu-id="32d8c-2810">Keyword_jp_residence_card_number</span><span class="sxs-lookup"><span data-stu-id="32d8c-2810">Keyword_jp_residence_card_number</span></span>

- <span data-ttu-id="32d8c-2811">Numéro de carte de séjour</span><span class="sxs-lookup"><span data-stu-id="32d8c-2811">Residence card number</span></span>
- <span data-ttu-id="32d8c-2812">N ° carte de séjour</span><span class="sxs-lookup"><span data-stu-id="32d8c-2812">Residence card no</span></span>
- <span data-ttu-id="32d8c-2813">Carte de séjour #</span><span class="sxs-lookup"><span data-stu-id="32d8c-2813">Residence card #</span></span>
- <span data-ttu-id="32d8c-2814">在留カード番号</span><span class="sxs-lookup"><span data-stu-id="32d8c-2814">在留カード番号</span></span>
   
## <a name="malaysia-id-card-number"></a><span data-ttu-id="32d8c-2815">Numéro de carte d’identité Malaisie</span><span class="sxs-lookup"><span data-stu-id="32d8c-2815">Malaysia ID Card Number</span></span>

### <a name="format"></a><span data-ttu-id="32d8c-2816">Format</span><span class="sxs-lookup"><span data-stu-id="32d8c-2816">Format</span></span>

<span data-ttu-id="32d8c-2817">12 chiffres contenant éventuellement des traits d’union</span><span class="sxs-lookup"><span data-stu-id="32d8c-2817">12 digits containing optional hyphens</span></span>

### <a name="pattern"></a><span data-ttu-id="32d8c-2818">Modèle</span><span class="sxs-lookup"><span data-stu-id="32d8c-2818">Pattern</span></span>

<span data-ttu-id="32d8c-2819">12 chiffres :</span><span class="sxs-lookup"><span data-stu-id="32d8c-2819">12 digits:</span></span>
- <span data-ttu-id="32d8c-2820">Six chiffres au format AAMMJJ correspondant à la date de naissance </span><span class="sxs-lookup"><span data-stu-id="32d8c-2820">Six digits in the format YYMMDD which are the date of birth</span></span> 
- <span data-ttu-id="32d8c-2821">Un tiret (facultatif) </span><span class="sxs-lookup"><span data-stu-id="32d8c-2821">A dash (optional)</span></span> 
- <span data-ttu-id="32d8c-2822">Le code à deux lettres du lieu de naissance </span><span class="sxs-lookup"><span data-stu-id="32d8c-2822">Two-letter place-of-birth code</span></span> 
- <span data-ttu-id="32d8c-2823">Un tiret (facultatif) </span><span class="sxs-lookup"><span data-stu-id="32d8c-2823">A dash (optional)</span></span> 
- <span data-ttu-id="32d8c-2824">Trois chiffres aléatoires </span><span class="sxs-lookup"><span data-stu-id="32d8c-2824">Three random digits</span></span> 
- <span data-ttu-id="32d8c-2825">Code de sexe à un chiffre</span><span class="sxs-lookup"><span data-stu-id="32d8c-2825">One-digit gender code</span></span>

### <a name="checksum"></a><span data-ttu-id="32d8c-2826">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="32d8c-2826">Checksum</span></span>

<span data-ttu-id="32d8c-2827">Non</span><span class="sxs-lookup"><span data-stu-id="32d8c-2827">No</span></span>

### <a name="definition"></a><span data-ttu-id="32d8c-2828">Définition</span><span class="sxs-lookup"><span data-stu-id="32d8c-2828">Definition</span></span>

<span data-ttu-id="32d8c-2829">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="32d8c-2829">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="32d8c-2830">L’expression régulière Regex_malaysia_id_card_number trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="32d8c-2830">The regular expression Regex_malaysia_id_card_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="32d8c-2831">Un mot clé figurant dans la liste Keyword_malaysia_id_card_number est trouvé.</span><span class="sxs-lookup"><span data-stu-id="32d8c-2831">A keyword from Keyword_malaysia_id_card_number is found.</span></span>

```xml
<!-- Malaysia ID Card Number -->
</Entity>
      <Entity id="7f0e921c-9677-435b-aba2-bb8f1013c749" patternsProximity="300" recommendedConfidence="85">
        <Pattern confidenceLevel="85">
            <IdMatch idRef="Regex_malaysia_id_card_number" />
            <Match idRef="Keyword_malaysia_id_card_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="32d8c-2832">Mots clés</span><span class="sxs-lookup"><span data-stu-id="32d8c-2832">Keywords</span></span>
   
#### <a name="keyword_malaysia_id_card_number"></a><span data-ttu-id="32d8c-2833">Keyword_malaysia_id_card_number</span><span class="sxs-lookup"><span data-stu-id="32d8c-2833">Keyword_malaysia_id_card_number</span></span>

- <span data-ttu-id="32d8c-2834">carte d’application numérique</span><span class="sxs-lookup"><span data-stu-id="32d8c-2834">digital application card</span></span>
- <span data-ttu-id="32d8c-2835">i/c</span><span class="sxs-lookup"><span data-stu-id="32d8c-2835">i/c</span></span>
- <span data-ttu-id="32d8c-2836">n ° i/c non</span><span class="sxs-lookup"><span data-stu-id="32d8c-2836">i/c no</span></span>
- <span data-ttu-id="32d8c-2837">combustion</span><span class="sxs-lookup"><span data-stu-id="32d8c-2837">ic</span></span>
- <span data-ttu-id="32d8c-2838">n ° IC</span><span class="sxs-lookup"><span data-stu-id="32d8c-2838">ic no</span></span>
- <span data-ttu-id="32d8c-2839">carte d’identité</span><span class="sxs-lookup"><span data-stu-id="32d8c-2839">id card</span></span>
- <span data-ttu-id="32d8c-2840">Carte d’identification</span><span class="sxs-lookup"><span data-stu-id="32d8c-2840">identification Card</span></span>
- <span data-ttu-id="32d8c-2841">Carte d’identité</span><span class="sxs-lookup"><span data-stu-id="32d8c-2841">identity card</span></span>
- <span data-ttu-id="32d8c-2842">k/p</span><span class="sxs-lookup"><span data-stu-id="32d8c-2842">k/p</span></span>
- <span data-ttu-id="32d8c-2843">n ° k/p</span><span class="sxs-lookup"><span data-stu-id="32d8c-2843">k/p no</span></span>
- <span data-ttu-id="32d8c-2844">kad akuan diri</span><span class="sxs-lookup"><span data-stu-id="32d8c-2844">kad akuan diri</span></span>
- <span data-ttu-id="32d8c-2845">Kad aplikasi numérique</span><span class="sxs-lookup"><span data-stu-id="32d8c-2845">kad aplikasi digital</span></span>
- <span data-ttu-id="32d8c-2846">Kad Pengenalan Malaisie</span><span class="sxs-lookup"><span data-stu-id="32d8c-2846">kad pengenalan malaysia</span></span>
- <span data-ttu-id="32d8c-2847">kgf</span><span class="sxs-lookup"><span data-stu-id="32d8c-2847">kp</span></span>
- <span data-ttu-id="32d8c-2848">KP non</span><span class="sxs-lookup"><span data-stu-id="32d8c-2848">kp no</span></span>
- <span data-ttu-id="32d8c-2849">mykad</span><span class="sxs-lookup"><span data-stu-id="32d8c-2849">mykad</span></span>
- <span data-ttu-id="32d8c-2850">mykas</span><span class="sxs-lookup"><span data-stu-id="32d8c-2850">mykas</span></span>
- <span data-ttu-id="32d8c-2851">mykid</span><span class="sxs-lookup"><span data-stu-id="32d8c-2851">mykid</span></span>
- <span data-ttu-id="32d8c-2852">mypr</span><span class="sxs-lookup"><span data-stu-id="32d8c-2852">mypr</span></span>
- <span data-ttu-id="32d8c-2853">mytentera</span><span class="sxs-lookup"><span data-stu-id="32d8c-2853">mytentera</span></span>
- <span data-ttu-id="32d8c-2854">carte d’identité Malaisie</span><span class="sxs-lookup"><span data-stu-id="32d8c-2854">malaysia identity card</span></span>
- <span data-ttu-id="32d8c-2855">carte d’identité malais</span><span class="sxs-lookup"><span data-stu-id="32d8c-2855">malaysian identity card</span></span>
- <span data-ttu-id="32d8c-2856">NRIC</span><span class="sxs-lookup"><span data-stu-id="32d8c-2856">nric</span></span>
- <span data-ttu-id="32d8c-2857">carte d’identification personnelle</span><span class="sxs-lookup"><span data-stu-id="32d8c-2857">personal identification card</span></span>
   
## <a name="netherlands-citizens-service-bsn-number"></a><span data-ttu-id="32d8c-2858">Numéro de service du citoyen (BSN) Pays-Bas</span><span class="sxs-lookup"><span data-stu-id="32d8c-2858">Netherlands Citizen's Service (BSN) Number</span></span>

### <a name="format"></a><span data-ttu-id="32d8c-2859">Format</span><span class="sxs-lookup"><span data-stu-id="32d8c-2859">Format</span></span>

<span data-ttu-id="32d8c-2860">8 à 9 chiffres contenant éventuellement des espaces</span><span class="sxs-lookup"><span data-stu-id="32d8c-2860">8-9 digits containing optional spaces</span></span>

### <a name="pattern"></a><span data-ttu-id="32d8c-2861">Modèle</span><span class="sxs-lookup"><span data-stu-id="32d8c-2861">Pattern</span></span>

<span data-ttu-id="32d8c-2862">8 à 9 chiffres :</span><span class="sxs-lookup"><span data-stu-id="32d8c-2862">8-9 digits:</span></span>
- <span data-ttu-id="32d8c-2863">Trois chiffres</span><span class="sxs-lookup"><span data-stu-id="32d8c-2863">Three digits</span></span> 
- <span data-ttu-id="32d8c-2864">Un espace (facultatif) </span><span class="sxs-lookup"><span data-stu-id="32d8c-2864">A space (optional)</span></span> 
- <span data-ttu-id="32d8c-2865">Trois chiffres</span><span class="sxs-lookup"><span data-stu-id="32d8c-2865">Three digits</span></span> 
- <span data-ttu-id="32d8c-2866">Un espace (facultatif) </span><span class="sxs-lookup"><span data-stu-id="32d8c-2866">A space (optional)</span></span> 
- <span data-ttu-id="32d8c-2867">2 à 3 chiffres</span><span class="sxs-lookup"><span data-stu-id="32d8c-2867">2-3 digits</span></span>

### <a name="checksum"></a><span data-ttu-id="32d8c-2868">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="32d8c-2868">Checksum</span></span>

<span data-ttu-id="32d8c-2869">Oui</span><span class="sxs-lookup"><span data-stu-id="32d8c-2869">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="32d8c-2870">Définition</span><span class="sxs-lookup"><span data-stu-id="32d8c-2870">Definition</span></span>

<span data-ttu-id="32d8c-2871">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="32d8c-2871">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="32d8c-2872">La fonction Func_netherlands_bsn trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="32d8c-2872">The function Func_netherlands_bsn finds content that matches the pattern.</span></span>
- <span data-ttu-id="32d8c-2873">Un mot clé figurant dans la liste Keyword_netherlands_bsn est trouvé.</span><span class="sxs-lookup"><span data-stu-id="32d8c-2873">A keyword from Keyword_netherlands_bsn is found.</span></span>
- <span data-ttu-id="32d8c-2874">La fonction Func_eu_date2 trouve une date au format correct.</span><span class="sxs-lookup"><span data-stu-id="32d8c-2874">The function Func_eu_date2 finds a date in the right date format.</span></span>
- <span data-ttu-id="32d8c-2875">La somme de contrôle est correcte.</span><span class="sxs-lookup"><span data-stu-id="32d8c-2875">The checksum passes.</span></span>

```xml
<!-- Netherlands Citizen's Service (BSN) Number -->
<Entity id="c5f54253-ef7e-44f6-a578-440ed67e946d" patternsProximity="300" recommendedConfidence="85">
  <Pattern confidenceLevel="85">
       <IdMatch idRef="Func_netherlands_bsn" /> 
       <Match idRef="Keyword_netherlands_bsn" /> 
       <Match idRef="Func_eu_date2" /> 
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="32d8c-2876">Mots clés</span><span class="sxs-lookup"><span data-stu-id="32d8c-2876">Keywords</span></span>

#### <a name="keyword_netherlands_bsn"></a><span data-ttu-id="32d8c-2877">Keyword_netherlands_bsn</span><span class="sxs-lookup"><span data-stu-id="32d8c-2877">Keyword_netherlands_bsn</span></span>

- <span data-ttu-id="32d8c-2878">Citizen service number</span><span class="sxs-lookup"><span data-stu-id="32d8c-2878">Citizen service number</span></span> 
- <span data-ttu-id="32d8c-2879">BSN</span><span class="sxs-lookup"><span data-stu-id="32d8c-2879">BSN</span></span> 
- <span data-ttu-id="32d8c-2880">Burgerservicenummer</span><span class="sxs-lookup"><span data-stu-id="32d8c-2880">Burgerservicenummer</span></span> 
- <span data-ttu-id="32d8c-2881">Sofinummer</span><span class="sxs-lookup"><span data-stu-id="32d8c-2881">Sofinummer</span></span> 
- <span data-ttu-id="32d8c-2882">Persoonsgebonden nummer</span><span class="sxs-lookup"><span data-stu-id="32d8c-2882">Persoonsgebonden nummer</span></span> 
- <span data-ttu-id="32d8c-2883">Persoonsnummer</span><span class="sxs-lookup"><span data-stu-id="32d8c-2883">Persoonsnummer</span></span>    

   
## <a name="new-zealand-ministry-of-health-number"></a><span data-ttu-id="32d8c-2884">Numéro du Ministère de la santé Nouvelle-Zélande</span><span class="sxs-lookup"><span data-stu-id="32d8c-2884">New Zealand Ministry of Health Number</span></span>

### <a name="format"></a><span data-ttu-id="32d8c-2885">Format</span><span class="sxs-lookup"><span data-stu-id="32d8c-2885">Format</span></span>

<span data-ttu-id="32d8c-2886">Trois lettres, un espace (facultatif) et quatre chiffres</span><span class="sxs-lookup"><span data-stu-id="32d8c-2886">Three letters, a space (optional), and four digits</span></span>

### <a name="pattern"></a><span data-ttu-id="32d8c-2887">Modèle</span><span class="sxs-lookup"><span data-stu-id="32d8c-2887">Pattern</span></span>

<span data-ttu-id="32d8c-2888">Trois lettres (ne respectant pas la casse) un espace (facultatif) quatre chiffres</span><span class="sxs-lookup"><span data-stu-id="32d8c-2888">Three letters (not case sensitive) a space (optional) four digits</span></span>

### <a name="checksum"></a><span data-ttu-id="32d8c-2889">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="32d8c-2889">Checksum</span></span>

<span data-ttu-id="32d8c-2890">Oui</span><span class="sxs-lookup"><span data-stu-id="32d8c-2890">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="32d8c-2891">Définition</span><span class="sxs-lookup"><span data-stu-id="32d8c-2891">Definition</span></span>

<span data-ttu-id="32d8c-2892">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="32d8c-2892">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="32d8c-2893">La fonction Func_new_zealand_ministry_of_health_number trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="32d8c-2893">The function Func_new_zealand_ministry_of_health_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="32d8c-2894">Un mot clé figurant dans la liste Keyword_nz_terms est trouvé.</span><span class="sxs-lookup"><span data-stu-id="32d8c-2894">A keyword from Keyword_nz_terms is found.</span></span>
- <span data-ttu-id="32d8c-2895">La somme de contrôle est correcte.</span><span class="sxs-lookup"><span data-stu-id="32d8c-2895">The checksum passes.</span></span>

```xml
<!-- New Zealand Health Number -->
<Entity id="2b71c1c8-d14e-4430-82dc-fd1ed6bf05c7" patternsProximity="300" recommendedConfidence="85">
    <Pattern confidenceLevel="85">
        <IdMatch idRef="Func_new_zealand_ministry_of_health_number" />
        <Any minMatches="1">
          <Match idRef="Keyword_nz_terms" />
        </Any>
    </Pattern>
</Entity>
```

<span data-ttu-id="32d8c-2896">Mots clés</span><span class="sxs-lookup"><span data-stu-id="32d8c-2896">Keywords</span></span>

<span data-ttu-id="32d8c-2897">Keyword_nz_terms</span><span class="sxs-lookup"><span data-stu-id="32d8c-2897">Keyword_nz_terms</span></span>

- <span data-ttu-id="32d8c-2898">NHI</span><span class="sxs-lookup"><span data-stu-id="32d8c-2898">NHI</span></span> 
- <span data-ttu-id="32d8c-2899">Nouvelle-Zélande</span><span class="sxs-lookup"><span data-stu-id="32d8c-2899">New Zealand</span></span> 
- <span data-ttu-id="32d8c-2900">Intégrité</span><span class="sxs-lookup"><span data-stu-id="32d8c-2900">Health</span></span> 
- <span data-ttu-id="32d8c-2901">destinations</span><span class="sxs-lookup"><span data-stu-id="32d8c-2901">treatment</span></span> 
   
## <a name="norway-identification-number"></a><span data-ttu-id="32d8c-2902">Numéro d’identification Norvège</span><span class="sxs-lookup"><span data-stu-id="32d8c-2902">Norway Identification Number</span></span>

### <a name="format"></a><span data-ttu-id="32d8c-2903">Format</span><span class="sxs-lookup"><span data-stu-id="32d8c-2903">Format</span></span>

<span data-ttu-id="32d8c-2904">11 chiffres</span><span class="sxs-lookup"><span data-stu-id="32d8c-2904">11 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="32d8c-2905">Modèle</span><span class="sxs-lookup"><span data-stu-id="32d8c-2905">Pattern</span></span>

<span data-ttu-id="32d8c-2906">11 chiffres :</span><span class="sxs-lookup"><span data-stu-id="32d8c-2906">11 digits:</span></span>
- <span data-ttu-id="32d8c-2907">Six chiffres au format JJMMAA qui correspondent à la date de naissance </span><span class="sxs-lookup"><span data-stu-id="32d8c-2907">Six digits in the format DDMMYY which are the date of birth</span></span> 
- <span data-ttu-id="32d8c-2908">Numéro individuel à trois chiffres </span><span class="sxs-lookup"><span data-stu-id="32d8c-2908">Three-digit individual number</span></span> 
- <span data-ttu-id="32d8c-2909">Deux chiffres de contrôle</span><span class="sxs-lookup"><span data-stu-id="32d8c-2909">Two check digits</span></span>

### <a name="checksum"></a><span data-ttu-id="32d8c-2910">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="32d8c-2910">Checksum</span></span>

<span data-ttu-id="32d8c-2911">Oui</span><span class="sxs-lookup"><span data-stu-id="32d8c-2911">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="32d8c-2912">Définition</span><span class="sxs-lookup"><span data-stu-id="32d8c-2912">Definition</span></span>

<span data-ttu-id="32d8c-2913">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="32d8c-2913">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="32d8c-2914">La fonction Func_norway_id_number trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="32d8c-2914">The function Func_norway_id_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="32d8c-2915">Un mot clé figurant dans la liste Keyword_norway_id_number est trouvé.</span><span class="sxs-lookup"><span data-stu-id="32d8c-2915">A keyword from Keyword_norway_id_number is found.</span></span>
- <span data-ttu-id="32d8c-2916">La somme de contrôle est correcte.</span><span class="sxs-lookup"><span data-stu-id="32d8c-2916">The checksum passes.</span></span>
- <span data-ttu-id="32d8c-2917">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="32d8c-2917">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="32d8c-2918">La fonction Func_norway_id_numbe trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="32d8c-2918">The function Func_norway_id_numbe finds content that matches the pattern.</span></span>
- <span data-ttu-id="32d8c-2919">La somme de contrôle est correcte.</span><span class="sxs-lookup"><span data-stu-id="32d8c-2919">The checksum passes.</span></span>

```xml
<!-- Norway Identification Number -->
<Entity id="d4c8a798-e9f2-4bd3-9652-500d24080fc3" recommendedConfidence="85" patternsProximity="300">
  <Pattern confidenceLevel="85">
     <IdMatch idRef="Func_norway_id_number"/>
     <Match idRef="Keyword_norway_id_number"/>
  </Pattern>
  <Pattern confidenceLevel="75">
     <IdMatch idRef="Func_norway_id_number"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="32d8c-2920">Mots clés</span><span class="sxs-lookup"><span data-stu-id="32d8c-2920">Keywords</span></span>

#### <a name="keyword_norway_id_number"></a><span data-ttu-id="32d8c-2921">Keyword_norway_id_number</span><span class="sxs-lookup"><span data-stu-id="32d8c-2921">Keyword_norway_id_number</span></span>

- <span data-ttu-id="32d8c-2922">Personal identification number</span><span class="sxs-lookup"><span data-stu-id="32d8c-2922">Personal identification number</span></span>
- <span data-ttu-id="32d8c-2923">Norwegian ID Number</span><span class="sxs-lookup"><span data-stu-id="32d8c-2923">Norwegian ID Number</span></span>
- <span data-ttu-id="32d8c-2924">ID Number</span><span class="sxs-lookup"><span data-stu-id="32d8c-2924">ID Number</span></span>
- <span data-ttu-id="32d8c-2925">Identificateur</span><span class="sxs-lookup"><span data-stu-id="32d8c-2925">Identification</span></span>
- <span data-ttu-id="32d8c-2926">Personnummer</span><span class="sxs-lookup"><span data-stu-id="32d8c-2926">Personnummer</span></span>
- <span data-ttu-id="32d8c-2927">Fødselsnummer</span><span class="sxs-lookup"><span data-stu-id="32d8c-2927">Fødselsnummer</span></span>

   
## <a name="philippines-unified-multi-purpose-id-number"></a><span data-ttu-id="32d8c-2928">Numéro d’identification multifonction unifié Philippines</span><span class="sxs-lookup"><span data-stu-id="32d8c-2928">Philippines Unified Multi-Purpose ID Number</span></span>

### <a name="format"></a><span data-ttu-id="32d8c-2929">Format</span><span class="sxs-lookup"><span data-stu-id="32d8c-2929">Format</span></span>

<span data-ttu-id="32d8c-2930">12 chiffres séparés par des traits d’union</span><span class="sxs-lookup"><span data-stu-id="32d8c-2930">12 digits separated by hyphens</span></span>

### <a name="pattern"></a><span data-ttu-id="32d8c-2931">Modèle</span><span class="sxs-lookup"><span data-stu-id="32d8c-2931">Pattern</span></span>

<span data-ttu-id="32d8c-2932">12 chiffres :</span><span class="sxs-lookup"><span data-stu-id="32d8c-2932">12 digits:</span></span>
- <span data-ttu-id="32d8c-2933">Quatre chiffres</span><span class="sxs-lookup"><span data-stu-id="32d8c-2933">Four digits</span></span> 
- <span data-ttu-id="32d8c-2934">Un trait d’union </span><span class="sxs-lookup"><span data-stu-id="32d8c-2934">A hyphen</span></span> 
- <span data-ttu-id="32d8c-2935">Sept chiffres </span><span class="sxs-lookup"><span data-stu-id="32d8c-2935">Seven digits</span></span> 
- <span data-ttu-id="32d8c-2936">Un trait d’union </span><span class="sxs-lookup"><span data-stu-id="32d8c-2936">A hyphen</span></span> 
- <span data-ttu-id="32d8c-2937">Un chiffre</span><span class="sxs-lookup"><span data-stu-id="32d8c-2937">One digit</span></span>

### <a name="checksum"></a><span data-ttu-id="32d8c-2938">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="32d8c-2938">Checksum</span></span>

<span data-ttu-id="32d8c-2939">Non</span><span class="sxs-lookup"><span data-stu-id="32d8c-2939">No</span></span>

### <a name="definition"></a><span data-ttu-id="32d8c-2940">Définition</span><span class="sxs-lookup"><span data-stu-id="32d8c-2940">Definition</span></span>

<span data-ttu-id="32d8c-2941">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="32d8c-2941">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="32d8c-2942">L’expression régulière Regex_philippines_unified_id trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="32d8c-2942">The regular expression Regex_philippines_unified_id finds content that matches the pattern.</span></span>
- <span data-ttu-id="32d8c-2943">Un mot clé figurant dans la liste Keyword_philippines_id est trouvé.</span><span class="sxs-lookup"><span data-stu-id="32d8c-2943">A keyword from Keyword_philippines_id is found.</span></span>

```xml
<!-- Philippines Unified Multi-Purpose ID number -->
<Entity id="019b39dd-8c25-4765-91a3-d9c6baf3c3b3" recommendedConfidence="75" patternsProximity="300">
  <Pattern confidenceLevel="75">
     <IdMatch idRef="Regex_philippines_unified_id"/>
     <Match idRef="Keyword_philippines_id"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="32d8c-2944">Mots clés</span><span class="sxs-lookup"><span data-stu-id="32d8c-2944">Keywords</span></span>
   
#### <a name="keyword_philippines_id"></a><span data-ttu-id="32d8c-2945">Keyword_philippines_id</span><span class="sxs-lookup"><span data-stu-id="32d8c-2945">Keyword_philippines_id</span></span>

- <span data-ttu-id="32d8c-2946">Unified Multi-Purpose ID</span><span class="sxs-lookup"><span data-stu-id="32d8c-2946">Unified Multi-Purpose ID</span></span> 
- <span data-ttu-id="32d8c-2947">UMID</span><span class="sxs-lookup"><span data-stu-id="32d8c-2947">UMID</span></span> 
- <span data-ttu-id="32d8c-2948">Identity Card</span><span class="sxs-lookup"><span data-stu-id="32d8c-2948">Identity Card</span></span> 
- <span data-ttu-id="32d8c-2949">Pinag-isang Multi-Layunin ID</span><span class="sxs-lookup"><span data-stu-id="32d8c-2949">Pinag-isang Multi-Layunin ID</span></span>
   
## <a name="poland-identity-card"></a><span data-ttu-id="32d8c-2950">Carte d'identité Pologne</span><span class="sxs-lookup"><span data-stu-id="32d8c-2950">Poland Identity Card</span></span>

### <a name="format"></a><span data-ttu-id="32d8c-2951">Format</span><span class="sxs-lookup"><span data-stu-id="32d8c-2951">Format</span></span>

<span data-ttu-id="32d8c-2952">Trois lettres et six chiffres</span><span class="sxs-lookup"><span data-stu-id="32d8c-2952">Three letters and six digits</span></span>

### <a name="pattern"></a><span data-ttu-id="32d8c-2953">Modèle</span><span class="sxs-lookup"><span data-stu-id="32d8c-2953">Pattern</span></span>

<span data-ttu-id="32d8c-2954">Trois lettres (ne respectant pas la casse) suivis de six chiffres</span><span class="sxs-lookup"><span data-stu-id="32d8c-2954">Three letters (not case sensitive) followed by six digits</span></span>

### <a name="checksum"></a><span data-ttu-id="32d8c-2955">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="32d8c-2955">Checksum</span></span>

<span data-ttu-id="32d8c-2956">Oui</span><span class="sxs-lookup"><span data-stu-id="32d8c-2956">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="32d8c-2957">Définition</span><span class="sxs-lookup"><span data-stu-id="32d8c-2957">Definition</span></span>

<span data-ttu-id="32d8c-2958">Une stratégie DLP est sûre à 75% d’avoir détecté ce type d’informations sensibles si, dans une proximité de 300 caractères : la fonction Func_polish_national_id trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="32d8c-2958">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters: The function Func_polish_national_id finds content that matches the pattern.</span></span>
<span data-ttu-id="32d8c-2959">Un mot clé figurant dans la liste Keyword_polish_national_id_passport_number est trouvé.</span><span class="sxs-lookup"><span data-stu-id="32d8c-2959">A keyword from Keyword_polish_national_id_passport_number is found.</span></span>
<span data-ttu-id="32d8c-2960">La somme de contrôle est correcte.</span><span class="sxs-lookup"><span data-stu-id="32d8c-2960">The checksum passes.</span></span>

```xml
<!-- Poland Identity Card-->
<Entity id="25E64989-ED5D-40CA-A939-6C14183BB7BF" patternsProximity="300" recommendedConfidence="85">
      <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_polish_national_id" />
          <Match idRef="Keyword_polish_national_id_passport_number" />
      </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="32d8c-2961">Mots clés</span><span class="sxs-lookup"><span data-stu-id="32d8c-2961">Keywords</span></span>

#### <a name="keyword_polish_national_id_passport_number"></a><span data-ttu-id="32d8c-2962">Keyword_polish_national_id_passport_number</span><span class="sxs-lookup"><span data-stu-id="32d8c-2962">Keyword_polish_national_id_passport_number</span></span>

- <span data-ttu-id="32d8c-2963">Dowód osobisty</span><span class="sxs-lookup"><span data-stu-id="32d8c-2963">Dowód osobisty</span></span>
- <span data-ttu-id="32d8c-2964">Chiffre dowodu osobistego</span><span class="sxs-lookup"><span data-stu-id="32d8c-2964">Numer dowodu osobistego</span></span>
- <span data-ttu-id="32d8c-2965">Nazwa i dowodu osobistego</span><span class="sxs-lookup"><span data-stu-id="32d8c-2965">Nazwa i numer dowodu osobistego</span></span>
- <span data-ttu-id="32d8c-2966">Nazwa i Nr dowodu osobistego</span><span class="sxs-lookup"><span data-stu-id="32d8c-2966">Nazwa i nr dowodu osobistego</span></span>
- <span data-ttu-id="32d8c-2967">Nazwa je nr dowodu tożsamości</span><span class="sxs-lookup"><span data-stu-id="32d8c-2967">Nazwa i nr dowodu tożsamości</span></span>
- <span data-ttu-id="32d8c-2968">Dowód Tożsamości</span><span class="sxs-lookup"><span data-stu-id="32d8c-2968">Dowód Tożsamości</span></span>
- <span data-ttu-id="32d8c-2969">Dow.</span><span class="sxs-lookup"><span data-stu-id="32d8c-2969">dow.</span></span> <span data-ttu-id="32d8c-2970">OS.</span><span class="sxs-lookup"><span data-stu-id="32d8c-2970">os.</span></span>

   
## <a name="poland-national-id-pesel"></a><span data-ttu-id="32d8c-2971">ID national polonais (PESEL)</span><span class="sxs-lookup"><span data-stu-id="32d8c-2971">Poland National ID (PESEL)</span></span>

### <a name="format"></a><span data-ttu-id="32d8c-2972">Format</span><span class="sxs-lookup"><span data-stu-id="32d8c-2972">Format</span></span>

<span data-ttu-id="32d8c-2973">11 chiffres</span><span class="sxs-lookup"><span data-stu-id="32d8c-2973">11 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="32d8c-2974">Modèle</span><span class="sxs-lookup"><span data-stu-id="32d8c-2974">Pattern</span></span>

<span data-ttu-id="32d8c-2975">11 chiffres consécutifs</span><span class="sxs-lookup"><span data-stu-id="32d8c-2975">11 consecutive digits</span></span>

### <a name="checksum"></a><span data-ttu-id="32d8c-2976">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="32d8c-2976">Checksum</span></span>

<span data-ttu-id="32d8c-2977">Oui</span><span class="sxs-lookup"><span data-stu-id="32d8c-2977">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="32d8c-2978">Définition</span><span class="sxs-lookup"><span data-stu-id="32d8c-2978">Definition</span></span>

<span data-ttu-id="32d8c-2979">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="32d8c-2979">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="32d8c-2980">La fonction Func_pesel_identification_number trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="32d8c-2980">The function Func_pesel_identification_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="32d8c-2981">Un mot clé figurant dans la liste Keyword_pesel_identification_number est trouvé.</span><span class="sxs-lookup"><span data-stu-id="32d8c-2981">A keyword from Keyword_pesel_identification_number is found.</span></span>
- <span data-ttu-id="32d8c-2982">La somme de contrôle est correcte.</span><span class="sxs-lookup"><span data-stu-id="32d8c-2982">The checksum passes.</span></span>

```xml
<!-- Poland National ID (PESEL) -->      
<Entity id="E3AAF206-4297-412F-9E06-BA8487E22456" patternsProximity="300" recommendedConfidence="85">
      <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_pesel_identification_number" />
          <Match idRef="Keyword_pesel_identification_number" />
      </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="32d8c-2983">Mots clés</span><span class="sxs-lookup"><span data-stu-id="32d8c-2983">Keywords</span></span>

#### <a name="keyword_pesel_identification_number"></a><span data-ttu-id="32d8c-2984">Keyword_pesel_identification_number</span><span class="sxs-lookup"><span data-stu-id="32d8c-2984">Keyword_pesel_identification_number</span></span>

- <span data-ttu-id="32d8c-2985">Nr PESEL</span><span class="sxs-lookup"><span data-stu-id="32d8c-2985">Nr PESEL</span></span>
- <span data-ttu-id="32d8c-2986">PESEL</span><span class="sxs-lookup"><span data-stu-id="32d8c-2986">PESEL</span></span>   

   
## <a name="poland-passport"></a><span data-ttu-id="32d8c-2987">Passeport Pologne</span><span class="sxs-lookup"><span data-stu-id="32d8c-2987">Poland Passport</span></span>

### <a name="format"></a><span data-ttu-id="32d8c-2988">Format</span><span class="sxs-lookup"><span data-stu-id="32d8c-2988">Format</span></span>

<span data-ttu-id="32d8c-2989">Deux lettres et sept chiffres</span><span class="sxs-lookup"><span data-stu-id="32d8c-2989">Two letters and seven digits</span></span>

### <a name="pattern"></a><span data-ttu-id="32d8c-2990">Modèle</span><span class="sxs-lookup"><span data-stu-id="32d8c-2990">Pattern</span></span>

<span data-ttu-id="32d8c-2991">Deux lettres (ne respectant pas la casse) suivies de sept chiffres</span><span class="sxs-lookup"><span data-stu-id="32d8c-2991">Two letters (not case sensitive) followed by seven digits</span></span>

### <a name="checksum"></a><span data-ttu-id="32d8c-2992">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="32d8c-2992">Checksum</span></span>

<span data-ttu-id="32d8c-2993">Oui</span><span class="sxs-lookup"><span data-stu-id="32d8c-2993">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="32d8c-2994">Définition</span><span class="sxs-lookup"><span data-stu-id="32d8c-2994">Definition</span></span>

<span data-ttu-id="32d8c-2995">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="32d8c-2995">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="32d8c-2996">La fonction Func_polish_passport_number trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="32d8c-2996">The function Func_polish_passport_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="32d8c-2997">Un mot clé figurant dans la liste Keyword_polish_national_id_passport_number est trouvé.</span><span class="sxs-lookup"><span data-stu-id="32d8c-2997">A keyword from Keyword_polish_national_id_passport_number is found.</span></span>
- <span data-ttu-id="32d8c-2998">La somme de contrôle est correcte.</span><span class="sxs-lookup"><span data-stu-id="32d8c-2998">The checksum passes.</span></span>

```xml
<!-- Poland Passport Number -->
<Entity id="03937FB5-D2B6-4487-B61F-0F8BFF7C3517" patternsProximity="300" recommendedConfidence="85">
      <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_polish_passport_number" />
          <Match idRef="Keyword_polish_national_id_passport_number" />
      </Pattern>
</Entity>
</Version>
```

### <a name="keywords"></a><span data-ttu-id="32d8c-2999">Mots clés</span><span class="sxs-lookup"><span data-stu-id="32d8c-2999">Keywords</span></span>

#### <a name="keyword_polish_national_id_passport_number"></a><span data-ttu-id="32d8c-3000">Keyword_polish_national_id_passport_number</span><span class="sxs-lookup"><span data-stu-id="32d8c-3000">Keyword_polish_national_id_passport_number</span></span>

- <span data-ttu-id="32d8c-3001">Numéro paszportu</span><span class="sxs-lookup"><span data-stu-id="32d8c-3001">Numer paszportu</span></span>
- <span data-ttu-id="32d8c-3002">Nr.</span><span class="sxs-lookup"><span data-stu-id="32d8c-3002">Nr.</span></span> <span data-ttu-id="32d8c-3003">Paszportu</span><span class="sxs-lookup"><span data-stu-id="32d8c-3003">Paszportu</span></span>
- <span data-ttu-id="32d8c-3004">Paszport</span><span class="sxs-lookup"><span data-stu-id="32d8c-3004">Paszport</span></span>

   
## <a name="portugal-citizen-card-number"></a><span data-ttu-id="32d8c-3005">Numéro de carte de citoyen Portugal</span><span class="sxs-lookup"><span data-stu-id="32d8c-3005">Portugal Citizen Card Number</span></span>

### <a name="format"></a><span data-ttu-id="32d8c-3006">Format</span><span class="sxs-lookup"><span data-stu-id="32d8c-3006">Format</span></span>

<span data-ttu-id="32d8c-3007">Huit chiffres</span><span class="sxs-lookup"><span data-stu-id="32d8c-3007">Eight digits</span></span>

### <a name="pattern"></a><span data-ttu-id="32d8c-3008">Modèle</span><span class="sxs-lookup"><span data-stu-id="32d8c-3008">Pattern</span></span>

<span data-ttu-id="32d8c-3009">Huit chiffres</span><span class="sxs-lookup"><span data-stu-id="32d8c-3009">Eight digits</span></span>

### <a name="checksum"></a><span data-ttu-id="32d8c-3010">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="32d8c-3010">Checksum</span></span>

<span data-ttu-id="32d8c-3011">Non</span><span class="sxs-lookup"><span data-stu-id="32d8c-3011">No</span></span>

### <a name="definition"></a><span data-ttu-id="32d8c-3012">Définition</span><span class="sxs-lookup"><span data-stu-id="32d8c-3012">Definition</span></span>

<span data-ttu-id="32d8c-3013">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="32d8c-3013">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="32d8c-3014">L’expression régulière Regex_portugal_citizen_card trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="32d8c-3014">The regular expression Regex_portugal_citizen_card finds content that matches the pattern.</span></span>
- <span data-ttu-id="32d8c-3015">Un mot clé figurant dans la liste Keyword_portugal_citizen_card est trouvé.</span><span class="sxs-lookup"><span data-stu-id="32d8c-3015">A keyword from Keyword_portugal_citizen_card is found.</span></span>

```xml
<!-- Portugal Citizen Card Number -->
<Entity id="91a7ece2-add4-4986-9a15-c84544d81ecd" recommendedConfidence="85" patternsProximity="300">
  <Pattern confidenceLevel="85">
     <IdMatch idRef="Regex_portugal_citizen_card"/>
     <Match idRef="Keyword_portugal_citizen_card"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="32d8c-3016">Mots clés</span><span class="sxs-lookup"><span data-stu-id="32d8c-3016">Keywords</span></span>

#### <a name="keyword_portugal_citizen_card"></a><span data-ttu-id="32d8c-3017">Keyword_portugal_citizen_card</span><span class="sxs-lookup"><span data-stu-id="32d8c-3017">Keyword_portugal_citizen_card</span></span>

- <span data-ttu-id="32d8c-3018">Citizen Card</span><span class="sxs-lookup"><span data-stu-id="32d8c-3018">Citizen Card</span></span>
- <span data-ttu-id="32d8c-3019">National ID Card</span><span class="sxs-lookup"><span data-stu-id="32d8c-3019">National ID Card</span></span>
- <span data-ttu-id="32d8c-3020">Cc</span><span class="sxs-lookup"><span data-stu-id="32d8c-3020">CC</span></span>
- <span data-ttu-id="32d8c-3021">Cartão de Cidadão</span><span class="sxs-lookup"><span data-stu-id="32d8c-3021">Cartão de Cidadão</span></span>
- <span data-ttu-id="32d8c-3022">Bilhete de Identidade</span><span class="sxs-lookup"><span data-stu-id="32d8c-3022">Bilhete de Identidade</span></span>
   
## <a name="saudi-arabia-national-id"></a><span data-ttu-id="32d8c-3023">ID national Arabie saoudite</span><span class="sxs-lookup"><span data-stu-id="32d8c-3023">Saudi Arabia National ID</span></span>

### <a name="format"></a><span data-ttu-id="32d8c-3024">Format</span><span class="sxs-lookup"><span data-stu-id="32d8c-3024">Format</span></span>

<span data-ttu-id="32d8c-3025">10 chiffres</span><span class="sxs-lookup"><span data-stu-id="32d8c-3025">10 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="32d8c-3026">Modèle</span><span class="sxs-lookup"><span data-stu-id="32d8c-3026">Pattern</span></span>

<span data-ttu-id="32d8c-3027">10 chiffres consécutifs</span><span class="sxs-lookup"><span data-stu-id="32d8c-3027">10 consecutive digits</span></span>

### <a name="checksum"></a><span data-ttu-id="32d8c-3028">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="32d8c-3028">Checksum</span></span>

<span data-ttu-id="32d8c-3029">Non</span><span class="sxs-lookup"><span data-stu-id="32d8c-3029">No</span></span>

### <a name="definition"></a><span data-ttu-id="32d8c-3030">Définition</span><span class="sxs-lookup"><span data-stu-id="32d8c-3030">Definition</span></span>

<span data-ttu-id="32d8c-3031">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="32d8c-3031">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="32d8c-3032">L’expression régulière Regex_saudi_arabia_national_id trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="32d8c-3032">The regular expression Regex_saudi_arabia_national_id finds content that matches the pattern.</span></span>
- <span data-ttu-id="32d8c-3033">Un mot clé figurant dans la liste Keyword_saudi_arabia_national_id est trouvé.</span><span class="sxs-lookup"><span data-stu-id="32d8c-3033">A keyword from Keyword_saudi_arabia_national_id is found.</span></span>

```xml
<!-- Saudi Arabia National ID -->
<Entity id="8c5a0ba8-404a-41a3-8871-746aa21ee6c0" patternsProximity="300" recommendedConfidence="75">
    <Pattern confidenceLevel="75">
        <IdMatch idRef="Regex_saudi_arabia_national_id" />
        <Any minMatches="1">
          <Match idRef="Keyword_saudi_arabia_national_id" />
        </Any>
    </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="32d8c-3034">Mots clés</span><span class="sxs-lookup"><span data-stu-id="32d8c-3034">Keywords</span></span>

#### <a name="keyword_saudi_arabia_national_id"></a><span data-ttu-id="32d8c-3035">Keyword_saudi_arabia_national_id</span><span class="sxs-lookup"><span data-stu-id="32d8c-3035">Keyword_saudi_arabia_national_id</span></span>

- <span data-ttu-id="32d8c-3036">Carte d’identification</span><span class="sxs-lookup"><span data-stu-id="32d8c-3036">Identification Card</span></span> 
- <span data-ttu-id="32d8c-3037">numéro de carte d’identité</span><span class="sxs-lookup"><span data-stu-id="32d8c-3037">I card number</span></span> 
- <span data-ttu-id="32d8c-3038">Numéro d’identification</span><span class="sxs-lookup"><span data-stu-id="32d8c-3038">ID number</span></span> 
- <span data-ttu-id="32d8c-3039">الوطنية الهوية بطاقة رقم</span><span class="sxs-lookup"><span data-stu-id="32d8c-3039">الوطنية الهوية بطاقة رقم</span></span> 

   
## <a name="singapore-national-registration-identity-card-nric-number"></a><span data-ttu-id="32d8c-3040">Numéro de carte d’identité d’enregistrement national (NRIC) Singapour</span><span class="sxs-lookup"><span data-stu-id="32d8c-3040">Singapore National Registration Identity Card (NRIC) Number</span></span>

### <a name="format"></a><span data-ttu-id="32d8c-3041">Format</span><span class="sxs-lookup"><span data-stu-id="32d8c-3041">Format</span></span>

<span data-ttu-id="32d8c-3042">Neuf lettres et chiffres</span><span class="sxs-lookup"><span data-stu-id="32d8c-3042">Nine letters and digits</span></span>

### <a name="pattern"></a><span data-ttu-id="32d8c-3043">Modèle</span><span class="sxs-lookup"><span data-stu-id="32d8c-3043">Pattern</span></span>

- <span data-ttu-id="32d8c-3044">Neuf lettres et chiffres :</span><span class="sxs-lookup"><span data-stu-id="32d8c-3044">Nine letters and digits:</span></span>
- <span data-ttu-id="32d8c-3045">La lettre « F », « G », « S » ou « T » (ne respectant pas la casse) </span><span class="sxs-lookup"><span data-stu-id="32d8c-3045">The letter "F", "G", "S", or "T" (not case sensitive)</span></span> 
- <span data-ttu-id="32d8c-3046">Sept chiffres </span><span class="sxs-lookup"><span data-stu-id="32d8c-3046">Seven digits</span></span> 
- <span data-ttu-id="32d8c-3047">Un chiffre de contrôle alphabétique</span><span class="sxs-lookup"><span data-stu-id="32d8c-3047">An alphabetic check digit</span></span>

### <a name="checksum"></a><span data-ttu-id="32d8c-3048">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="32d8c-3048">Checksum</span></span>

<span data-ttu-id="32d8c-3049">Oui</span><span class="sxs-lookup"><span data-stu-id="32d8c-3049">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="32d8c-3050">Définition</span><span class="sxs-lookup"><span data-stu-id="32d8c-3050">Definition</span></span>

<span data-ttu-id="32d8c-3051">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="32d8c-3051">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="32d8c-3052">L’expression régulière Regex_singapore_nric trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="32d8c-3052">The regular expression Regex_singapore_nric finds content that matches the pattern.</span></span>
- <span data-ttu-id="32d8c-3053">Un mot clé figurant dans la liste Keyword_singapore_nric est trouvé.</span><span class="sxs-lookup"><span data-stu-id="32d8c-3053">A keyword from Keyword_singapore_nric is found.</span></span>
- <span data-ttu-id="32d8c-3054">La somme de contrôle est correcte.</span><span class="sxs-lookup"><span data-stu-id="32d8c-3054">The checksum passes.</span></span>

<span data-ttu-id="32d8c-3055">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="32d8c-3055">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="32d8c-3056">L’expression régulière Regex_singapore_nric trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="32d8c-3056">The regular expression Regex_singapore_nric finds content that matches the pattern.</span></span>
- <span data-ttu-id="32d8c-3057">La somme de contrôle est correcte.</span><span class="sxs-lookup"><span data-stu-id="32d8c-3057">The checksum passes.</span></span>

```xml
<!-- Singapore National Registration Identity Card (NRIC) Number -->
<Entity id="cead390a-dd83-4856-9751-fb6dc98c34da" recommendedConfidence="75" patternsProximity="300">
  <Pattern confidenceLevel="85">
     <IdMatch idRef="Regex_singapore_nric"/>
     <Match idRef="Keyword_singapore_nric"/>
  </Pattern>
  <Pattern confidenceLevel="75">
     <IdMatch idRef="Regex_singapore_nric"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="32d8c-3058">Mots clés</span><span class="sxs-lookup"><span data-stu-id="32d8c-3058">Keywords</span></span>
   
#### <a name="keyword_singapore_nric"></a><span data-ttu-id="32d8c-3059">Keyword_singapore_nric</span><span class="sxs-lookup"><span data-stu-id="32d8c-3059">Keyword_singapore_nric</span></span>

- <span data-ttu-id="32d8c-3060">National Registration Identity Card</span><span class="sxs-lookup"><span data-stu-id="32d8c-3060">National Registration Identity Card</span></span> 
- <span data-ttu-id="32d8c-3061">Identity Card Number</span><span class="sxs-lookup"><span data-stu-id="32d8c-3061">Identity Card Number</span></span> 
- <span data-ttu-id="32d8c-3062">NRIC</span><span class="sxs-lookup"><span data-stu-id="32d8c-3062">NRIC</span></span> 
- <span data-ttu-id="32d8c-3063">COMBUSTION</span><span class="sxs-lookup"><span data-stu-id="32d8c-3063">IC</span></span> 
- <span data-ttu-id="32d8c-3064">Foreign Identification Number</span><span class="sxs-lookup"><span data-stu-id="32d8c-3064">Foreign Identification Number</span></span> 
- <span data-ttu-id="32d8c-3065">ECHERCHER</span><span class="sxs-lookup"><span data-stu-id="32d8c-3065">FIN</span></span> 
- <span data-ttu-id="32d8c-3066">身份证</span><span class="sxs-lookup"><span data-stu-id="32d8c-3066">身份证</span></span> 
- <span data-ttu-id="32d8c-3067">身份證</span><span class="sxs-lookup"><span data-stu-id="32d8c-3067">身份證</span></span> 
   
## <a name="south-africa-identification-number"></a><span data-ttu-id="32d8c-3068">Numéro d’identification Afrique du Sud</span><span class="sxs-lookup"><span data-stu-id="32d8c-3068">South Africa Identification Number</span></span>

### <a name="format"></a><span data-ttu-id="32d8c-3069">Format</span><span class="sxs-lookup"><span data-stu-id="32d8c-3069">Format</span></span>

<span data-ttu-id="32d8c-3070">13 chiffres pouvant contenir des espaces</span><span class="sxs-lookup"><span data-stu-id="32d8c-3070">13 digits that may contain spaces</span></span>

### <a name="pattern"></a><span data-ttu-id="32d8c-3071">Modèle</span><span class="sxs-lookup"><span data-stu-id="32d8c-3071">Pattern</span></span>

<span data-ttu-id="32d8c-3072">13 chiffres :</span><span class="sxs-lookup"><span data-stu-id="32d8c-3072">13 digits:</span></span>
- <span data-ttu-id="32d8c-3073">Six chiffres au format AAMMJJ correspondant à la date de naissance </span><span class="sxs-lookup"><span data-stu-id="32d8c-3073">Six digits in the format YYMMDD which are the date of birth</span></span> 
- <span data-ttu-id="32d8c-3074">Quatre chiffres</span><span class="sxs-lookup"><span data-stu-id="32d8c-3074">Four digits</span></span> 
- <span data-ttu-id="32d8c-3075">Un indicateur de citoyenneté à un chiffre </span><span class="sxs-lookup"><span data-stu-id="32d8c-3075">A single-digit citizenship indicator</span></span> 
- <span data-ttu-id="32d8c-3076">Le chiffre « 8 » ou « 9 » </span><span class="sxs-lookup"><span data-stu-id="32d8c-3076">The digit "8" or "9"</span></span> 
- <span data-ttu-id="32d8c-3077">Un chiffre pour la somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="32d8c-3077">One digit which is a checksum digit</span></span>

### <a name="checksum"></a><span data-ttu-id="32d8c-3078">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="32d8c-3078">Checksum</span></span>

<span data-ttu-id="32d8c-3079">Oui</span><span class="sxs-lookup"><span data-stu-id="32d8c-3079">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="32d8c-3080">Définition</span><span class="sxs-lookup"><span data-stu-id="32d8c-3080">Definition</span></span>

<span data-ttu-id="32d8c-3081">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="32d8c-3081">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="32d8c-3082">La fonction Func_south_africa_identification_number trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="32d8c-3082">The function Func_south_africa_identification_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="32d8c-3083">Un mot clé figurant dans la liste Keyword_south_africa_identification_number est trouvé.</span><span class="sxs-lookup"><span data-stu-id="32d8c-3083">A keyword from Keyword_south_africa_identification_number is found.</span></span>
- <span data-ttu-id="32d8c-3084">La somme de contrôle est correcte.</span><span class="sxs-lookup"><span data-stu-id="32d8c-3084">The checksum passes.</span></span>

```xml
<!-- South Africa Identification Number -->
<Entity id="e2adf7cb-8ea6-4048-a2ed-d89eb65f2780" recommendedConfidence="85" patternsProximity="300">
  <Pattern confidenceLevel="85">
     <IdMatch idRef="Func_south_africa_identification_number"/>
     <Match idRef="Keyword_south_africa_identification_number"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="32d8c-3085">Mots clés</span><span class="sxs-lookup"><span data-stu-id="32d8c-3085">Keywords</span></span>
   
#### <a name="keyword_south_africa_identification_number"></a><span data-ttu-id="32d8c-3086">Keyword_south_africa_identification_number</span><span class="sxs-lookup"><span data-stu-id="32d8c-3086">Keyword_south_africa_identification_number</span></span>

- <span data-ttu-id="32d8c-3087">Identity card</span><span class="sxs-lookup"><span data-stu-id="32d8c-3087">Identity card</span></span>
- <span data-ttu-id="32d8c-3088">ID</span><span class="sxs-lookup"><span data-stu-id="32d8c-3088">ID</span></span>
- <span data-ttu-id="32d8c-3089">Identificateur</span><span class="sxs-lookup"><span data-stu-id="32d8c-3089">Identification</span></span> 
   
## <a name="south-korea-resident-registration-number"></a><span data-ttu-id="32d8c-3090">Matricule de résident Corée du Sud</span><span class="sxs-lookup"><span data-stu-id="32d8c-3090">South Korea Resident Registration Number</span></span>

### <a name="format"></a><span data-ttu-id="32d8c-3091">Format</span><span class="sxs-lookup"><span data-stu-id="32d8c-3091">Format</span></span>

<span data-ttu-id="32d8c-3092">13 chiffres contenant un trait d’union</span><span class="sxs-lookup"><span data-stu-id="32d8c-3092">13 digits containing a hyphen</span></span>

### <a name="pattern"></a><span data-ttu-id="32d8c-3093">Modèle</span><span class="sxs-lookup"><span data-stu-id="32d8c-3093">Pattern</span></span>

<span data-ttu-id="32d8c-3094">13 chiffres :</span><span class="sxs-lookup"><span data-stu-id="32d8c-3094">13 digits:</span></span>
- <span data-ttu-id="32d8c-3095">Six chiffres au format AAMMJJ correspondant à la date de naissance </span><span class="sxs-lookup"><span data-stu-id="32d8c-3095">Six digits in the format YYMMDD which are the date of birth</span></span> 
- <span data-ttu-id="32d8c-3096">Un trait d’union </span><span class="sxs-lookup"><span data-stu-id="32d8c-3096">A hyphen</span></span> 
- <span data-ttu-id="32d8c-3097">Un chiffre déterminé par le siècle et le sexe </span><span class="sxs-lookup"><span data-stu-id="32d8c-3097">One digit determined by the century and gender</span></span> 
- <span data-ttu-id="32d8c-3098">Code à quatre chiffres désignant la région de naissance </span><span class="sxs-lookup"><span data-stu-id="32d8c-3098">Four-digit region-of-birth code</span></span> 
- <span data-ttu-id="32d8c-3099">Un chiffre utilisé pour différencier les personnes dont les chiffres précédents sont identiques. </span><span class="sxs-lookup"><span data-stu-id="32d8c-3099">One digit used to differentiate people for whom the preceding numbers are identical</span></span> 
- <span data-ttu-id="32d8c-3100">Un chiffre de contrôle.</span><span class="sxs-lookup"><span data-stu-id="32d8c-3100">A check digit.</span></span>

### <a name="checksum"></a><span data-ttu-id="32d8c-3101">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="32d8c-3101">Checksum</span></span>

<span data-ttu-id="32d8c-3102">Oui</span><span class="sxs-lookup"><span data-stu-id="32d8c-3102">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="32d8c-3103">Définition</span><span class="sxs-lookup"><span data-stu-id="32d8c-3103">Definition</span></span>

<span data-ttu-id="32d8c-3104">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="32d8c-3104">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="32d8c-3105">La fonction Func_south_korea_resident_number trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="32d8c-3105">The function Func_south_korea_resident_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="32d8c-3106">Un mot clé figurant dans la liste Keyword_south_korea_resident_number est trouvé.</span><span class="sxs-lookup"><span data-stu-id="32d8c-3106">A keyword from Keyword_south_korea_resident_number is found.</span></span>
- <span data-ttu-id="32d8c-3107">La somme de contrôle est correcte.</span><span class="sxs-lookup"><span data-stu-id="32d8c-3107">The checksum passes.</span></span>

<span data-ttu-id="32d8c-3108">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="32d8c-3108">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="32d8c-3109">La fonction Func_south_korea_resident_number trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="32d8c-3109">The function Func_south_korea_resident_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="32d8c-3110">La somme de contrôle est correcte.</span><span class="sxs-lookup"><span data-stu-id="32d8c-3110">The checksum passes.</span></span>

```xml
<!-- South Korea Resident Registration Number -->
<Entity id="5b802e18-ba80-44c4-bc83-bf2ad36ae36a" recommendedConfidence="85" patternsProximity="300">
  <Pattern confidenceLevel="85">
     <IdMatch idRef="Func_south_korea_resident_number"/>
     <Match idRef="Keyword_south_korea_resident_number"/>
  </Pattern>
  <Pattern confidenceLevel="75">
     <IdMatch idRef="Func_south_korea_resident_number"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="32d8c-3111">Mots clés</span><span class="sxs-lookup"><span data-stu-id="32d8c-3111">Keywords</span></span>
   
#### <a name="keyword_south_korea_resident_number"></a><span data-ttu-id="32d8c-3112">Keyword_south_korea_resident_number</span><span class="sxs-lookup"><span data-stu-id="32d8c-3112">Keyword_south_korea_resident_number</span></span>

- <span data-ttu-id="32d8c-3113">National ID card</span><span class="sxs-lookup"><span data-stu-id="32d8c-3113">National ID card</span></span> 
- <span data-ttu-id="32d8c-3114">Citizen’s Registration Number</span><span class="sxs-lookup"><span data-stu-id="32d8c-3114">Citizen's Registration Number</span></span> 
- <span data-ttu-id="32d8c-3115">Jumin deungnok beonho</span><span class="sxs-lookup"><span data-stu-id="32d8c-3115">Jumin deungnok beonho</span></span> 
- <span data-ttu-id="32d8c-3116">RRN</span><span class="sxs-lookup"><span data-stu-id="32d8c-3116">RRN</span></span> 
- <span data-ttu-id="32d8c-3117">주민등록번호</span><span class="sxs-lookup"><span data-stu-id="32d8c-3117">주민등록번호</span></span>
   
## <a name="spain-social-security-number-ssn"></a><span data-ttu-id="32d8c-3118">Numéro de sécurité sociale Espagne</span><span class="sxs-lookup"><span data-stu-id="32d8c-3118">Spain Social Security Number (SSN)</span></span>

### <a name="format"></a><span data-ttu-id="32d8c-3119">Format</span><span class="sxs-lookup"><span data-stu-id="32d8c-3119">Format</span></span>

<span data-ttu-id="32d8c-3120">11 à 12 chiffres</span><span class="sxs-lookup"><span data-stu-id="32d8c-3120">11-12 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="32d8c-3121">Modèle</span><span class="sxs-lookup"><span data-stu-id="32d8c-3121">Pattern</span></span>

<span data-ttu-id="32d8c-3122">11-12 chiffres :</span><span class="sxs-lookup"><span data-stu-id="32d8c-3122">11-12 digits:</span></span>
- <span data-ttu-id="32d8c-3123">Deux chiffres</span><span class="sxs-lookup"><span data-stu-id="32d8c-3123">Two digits</span></span> 
- <span data-ttu-id="32d8c-3124">Une barre oblique (facultative)</span><span class="sxs-lookup"><span data-stu-id="32d8c-3124">A forward slash (optional)</span></span> 
- <span data-ttu-id="32d8c-3125">7 à 8 chiffres</span><span class="sxs-lookup"><span data-stu-id="32d8c-3125">7-8 digits</span></span> 
- <span data-ttu-id="32d8c-3126">Une barre oblique (facultative)</span><span class="sxs-lookup"><span data-stu-id="32d8c-3126">A forward slash (optional)</span></span> 
- <span data-ttu-id="32d8c-3127">Deux chiffres</span><span class="sxs-lookup"><span data-stu-id="32d8c-3127">Two digits</span></span>

### <a name="checksum"></a><span data-ttu-id="32d8c-3128">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="32d8c-3128">Checksum</span></span>

<span data-ttu-id="32d8c-3129">Oui</span><span class="sxs-lookup"><span data-stu-id="32d8c-3129">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="32d8c-3130">Définition</span><span class="sxs-lookup"><span data-stu-id="32d8c-3130">Definition</span></span>

<span data-ttu-id="32d8c-3131">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="32d8c-3131">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="32d8c-3132">La fonction Func_spanish_social_security_number trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="32d8c-3132">The function Func_spanish_social_security_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="32d8c-3133">La somme de contrôle est correcte.</span><span class="sxs-lookup"><span data-stu-id="32d8c-3133">The checksum passes.</span></span>

```xml
<!-- Spain SSN -->
<Entity id="5df987c0-8eae-4bce-ace7-b316347f3070" patternsProximity="300" recommendedConfidence="85">
    <Pattern confidenceLevel="85">
        <IdMatch idRef="Func_spanish_social_security_number" />
    </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="32d8c-3134">Mots clés</span><span class="sxs-lookup"><span data-stu-id="32d8c-3134">Keywords</span></span>

<span data-ttu-id="32d8c-3135">Aucun</span><span class="sxs-lookup"><span data-stu-id="32d8c-3135">None</span></span>

## <a name="sql-server-connection-string"></a><span data-ttu-id="32d8c-3136">Chaîne de connexion SQL Server</span><span class="sxs-lookup"><span data-stu-id="32d8c-3136">SQL Server Connection String</span></span>

### <a name="format"></a><span data-ttu-id="32d8c-3137">Format</span><span class="sxs-lookup"><span data-stu-id="32d8c-3137">Format</span></span>

<span data-ttu-id="32d8c-3138">La chaîne « User ID », « User ID », « UID » ou « UserId » suivi des caractères et des chaînes décrits dans le modèle ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="32d8c-3138">The string "User Id", "User ID", "uid", or "UserId" followed by the characters and strings outlined in the pattern below.</span></span>

### <a name="pattern"></a><span data-ttu-id="32d8c-3139">Modèle</span><span class="sxs-lookup"><span data-stu-id="32d8c-3139">Pattern</span></span>

- <span data-ttu-id="32d8c-3140">La chaîne « User ID », « User ID », « UID » ou « UserId »</span><span class="sxs-lookup"><span data-stu-id="32d8c-3140">The string "User Id", "User ID", "uid", or "UserId"</span></span>
- <span data-ttu-id="32d8c-3141">N’importe quelle combinaison entre 1-200 majuscules ou minuscules, des chiffres, des symboles, des caractères spéciaux ou des espaces</span><span class="sxs-lookup"><span data-stu-id="32d8c-3141">Any combination of between 1-200 lower- or uppercase letters, digits, symbols, special characters, or spaces</span></span>
- <span data-ttu-id="32d8c-3142">La chaîne "password" ou "PWD" où "PWD" n’est pas précédé d’une lettre minuscule</span><span class="sxs-lookup"><span data-stu-id="32d8c-3142">The string "Password" or "pwd" where "pwd" is not preceded by a lowercase letter</span></span>
- <span data-ttu-id="32d8c-3143">Signe égal (=)</span><span class="sxs-lookup"><span data-stu-id="32d8c-3143">An equal sign (=)</span></span>
- <span data-ttu-id="32d8c-3144">Tout caractère qui n’est pas un signe dollar ($), un symbole de pourcentage (%), un symbole supérieur à (>), un symbole (@), un guillemet ("), un point-virgule (;), une accolade ouvrante ([) ou un crochet gauche ({)</span><span class="sxs-lookup"><span data-stu-id="32d8c-3144">Any character that is not a dollar sign ($), percent symbol (%), greater than symbol (>), at symbol (@), quotation mark ("), semicolon (;), left brace ([), or left bracket ({)</span></span>
- <span data-ttu-id="32d8c-3145">N’importe quelle combinaison de 7-128 caractères qui ne sont pas des points-virgules (;), barre oblique (/) ou guillemets (")</span><span class="sxs-lookup"><span data-stu-id="32d8c-3145">Any combination of 7-128 characters that are not a semicolon (;), forward slash (/), or quotation mark (")</span></span>
- <span data-ttu-id="32d8c-3146">Un point-virgule (;) ou guillemets (")</span><span class="sxs-lookup"><span data-stu-id="32d8c-3146">A semicolon (;) or quotation mark (")</span></span>

### <a name="checksum"></a><span data-ttu-id="32d8c-3147">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="32d8c-3147">Checksum</span></span>

<span data-ttu-id="32d8c-3148">Non</span><span class="sxs-lookup"><span data-stu-id="32d8c-3148">No</span></span>

### <a name="definition"></a><span data-ttu-id="32d8c-3149">Définition</span><span class="sxs-lookup"><span data-stu-id="32d8c-3149">Definition</span></span>

<span data-ttu-id="32d8c-3150">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="32d8c-3150">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="32d8c-3151">L’expression régulière CEP_Regex_SQLServerConnectionString trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="32d8c-3151">The regular expression CEP_Regex_SQLServerConnectionString finds content that matches the pattern.</span></span>
- <span data-ttu-id="32d8c-3152">Un mot clé depuis CEP_GlobalFilter **est introuvable** .</span><span class="sxs-lookup"><span data-stu-id="32d8c-3152">A keyword from CEP_GlobalFilter is **not** found.</span></span>
- <span data-ttu-id="32d8c-3153">L’expression régulière CEP_PasswordPlaceHolder ne trouve **pas** le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="32d8c-3153">The regular expression CEP_PasswordPlaceHolder does **not** find content that matches the pattern.</span></span>
- <span data-ttu-id="32d8c-3154">L’expression régulière CEP_CommonExampleKeywords ne trouve **pas** le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="32d8c-3154">The regular expression CEP_CommonExampleKeywords does **not** find content that matches the pattern.</span></span>

```sql
<!---SQL Server Connection String>
<Entity id="e76b6205-d3cb-46f2-bd63-c90153f2f97d" patternsProximity="300" recommendedConfidence="85">
  <Pattern confidenceLevel="85">
        <IdMatch idRef="CEP_Regex_SQLServerConnectionString" />
        <Any minMatches="0" maxMatches="0">
            <Match idRef="CEP_GlobalFilter" />
            <Match idRef="CEP_PasswordPlaceHolder" />
            <Match idRef="CEP_CommonExampleKeywords" />
        </Any>
    </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="32d8c-3155">Mots clés</span><span class="sxs-lookup"><span data-stu-id="32d8c-3155">Keywords</span></span>

#### <a name="cep_globalfilter"></a><span data-ttu-id="32d8c-3156">CEP_GlobalFilter</span><span class="sxs-lookup"><span data-stu-id="32d8c-3156">CEP_GlobalFilter</span></span>

- <span data-ttu-id="32d8c-3157">some-password</span><span class="sxs-lookup"><span data-stu-id="32d8c-3157">some-password</span></span>
- <span data-ttu-id="32d8c-3158">somepassword</span><span class="sxs-lookup"><span data-stu-id="32d8c-3158">somepassword</span></span>
- <span data-ttu-id="32d8c-3159">secretPassword</span><span class="sxs-lookup"><span data-stu-id="32d8c-3159">secretPassword</span></span>
- <span data-ttu-id="32d8c-3160">échantillonnage</span><span class="sxs-lookup"><span data-stu-id="32d8c-3160">sample</span></span>

#### <a name="cep_passwordplaceholder"></a><span data-ttu-id="32d8c-3161">CEP_PasswordPlaceHolder</span><span class="sxs-lookup"><span data-stu-id="32d8c-3161">CEP_PasswordPlaceHolder</span></span>

<span data-ttu-id="32d8c-3162">(Notez que techniquement, ce type d’informations sensibles identifie ces mots clés à l’aide d’une expression régulière, et non d’une liste de mots clés.)</span><span class="sxs-lookup"><span data-stu-id="32d8c-3162">(Note that technically, this sensitive information type identifies these keywords by using a regular expression, not a keyword list.)</span></span>

- <span data-ttu-id="32d8c-3163">Mot de passe ou mot de passe suivi par 0-2 espaces, un signe égal (=), 0-2 espaces et un astérisque (\*)--ou--</span><span class="sxs-lookup"><span data-stu-id="32d8c-3163">Password or pwd followed by 0-2 spaces, an equal sign (=), 0-2 spaces, and an asterisk (\*) --OR--</span></span>
- <span data-ttu-id="32d8c-3164">Mot de passe ou mot de passe suivi par :</span><span class="sxs-lookup"><span data-stu-id="32d8c-3164">Password or pwd followed by:</span></span>
    - <span data-ttu-id="32d8c-3165">Signe égal (=)</span><span class="sxs-lookup"><span data-stu-id="32d8c-3165">Equal sign (=)</span></span>
    - <span data-ttu-id="32d8c-3166">Symbole inférieur à (<)</span><span class="sxs-lookup"><span data-stu-id="32d8c-3166">Less than symbol (<)</span></span>
    - <span data-ttu-id="32d8c-3167">Toute combinaison de 1-200 caractères qui sont des lettres majuscules ou minuscules, des chiffres, un astérisque (\*), un tiret (-), un trait de soulignement (_) ou un espace blanc</span><span class="sxs-lookup"><span data-stu-id="32d8c-3167">Any combination of 1-200 characters that are upper- or lowercase letters, digits, an asterisk (\*), hyphen (-), underline (_), or whitespace character</span></span>
    - <span data-ttu-id="32d8c-3168">Symbole supérieur à (>)</span><span class="sxs-lookup"><span data-stu-id="32d8c-3168">Greater than symbol (>)</span></span>

#### <a name="cep_commonexamplekeywords"></a><span data-ttu-id="32d8c-3169">CEP_CommonExampleKeywords</span><span class="sxs-lookup"><span data-stu-id="32d8c-3169">CEP_CommonExampleKeywords</span></span>

<span data-ttu-id="32d8c-3170">(Notez que techniquement, ce type d’informations sensibles identifie ces mots clés à l’aide d’une expression régulière, et non d’une liste de mots clés.)</span><span class="sxs-lookup"><span data-stu-id="32d8c-3170">(Note that technically, this sensitive information type identifies these keywords by using a regular expression, not a keyword list.)</span></span>

- <span data-ttu-id="32d8c-3171">contoso</span><span class="sxs-lookup"><span data-stu-id="32d8c-3171">contoso</span></span>
- <span data-ttu-id="32d8c-3172">société</span><span class="sxs-lookup"><span data-stu-id="32d8c-3172">fabrikam</span></span>
- <span data-ttu-id="32d8c-3173">Northwind</span><span class="sxs-lookup"><span data-stu-id="32d8c-3173">northwind</span></span>
- <span data-ttu-id="32d8c-3174">immédiatement</span><span class="sxs-lookup"><span data-stu-id="32d8c-3174">sandbox</span></span>
- <span data-ttu-id="32d8c-3175">onebox</span><span class="sxs-lookup"><span data-stu-id="32d8c-3175">onebox</span></span>
- <span data-ttu-id="32d8c-3176">hôte</span><span class="sxs-lookup"><span data-stu-id="32d8c-3176">localhost</span></span>
- <span data-ttu-id="32d8c-3177">bouclage</span><span class="sxs-lookup"><span data-stu-id="32d8c-3177">127.0.0.1</span></span>
- <span data-ttu-id="32d8c-3178">testacs.</span><span class="sxs-lookup"><span data-stu-id="32d8c-3178">testacs.</span></span><!--no-hyperlink--><span data-ttu-id="32d8c-3179">com</span><span class="sxs-lookup"><span data-stu-id="32d8c-3179">com</span></span>
- <span data-ttu-id="32d8c-3180">s-int.</span><span class="sxs-lookup"><span data-stu-id="32d8c-3180">s-int.</span></span><!--no-hyperlink--><span data-ttu-id="32d8c-3181">NET</span><span class="sxs-lookup"><span data-stu-id="32d8c-3181">net</span></span>

## <a name="sweden-national-id"></a><span data-ttu-id="32d8c-3182">ID national Suède</span><span class="sxs-lookup"><span data-stu-id="32d8c-3182">Sweden National ID</span></span>

### <a name="format"></a><span data-ttu-id="32d8c-3183">Format</span><span class="sxs-lookup"><span data-stu-id="32d8c-3183">Format</span></span>

<span data-ttu-id="32d8c-3184">10 ou 12 chiffres et éventuellement un délimiteur</span><span class="sxs-lookup"><span data-stu-id="32d8c-3184">10 or 12 digits and an optional delimiter</span></span>

### <a name="pattern"></a><span data-ttu-id="32d8c-3185">Modèle</span><span class="sxs-lookup"><span data-stu-id="32d8c-3185">Pattern</span></span>

<span data-ttu-id="32d8c-3186">10 ou 12 chiffres et un délimiteur facultatif :</span><span class="sxs-lookup"><span data-stu-id="32d8c-3186">10 or 12 digits and an optional delimiter:</span></span>
- <span data-ttu-id="32d8c-3187">2 à 4 chiffres (facultatifs)</span><span class="sxs-lookup"><span data-stu-id="32d8c-3187">2-4 digits (optional)</span></span> 
- <span data-ttu-id="32d8c-3188">Six chiffres au format de date AAMMJJ</span><span class="sxs-lookup"><span data-stu-id="32d8c-3188">Six digits in date format YYMMDD</span></span> 
- <span data-ttu-id="32d8c-3189">Séparateur de « - » ou « + » (facultatif), plus</span><span class="sxs-lookup"><span data-stu-id="32d8c-3189">Delimiter of "-" or "+" (optional), plus</span></span>
- <span data-ttu-id="32d8c-3190">Quatre chiffres</span><span class="sxs-lookup"><span data-stu-id="32d8c-3190">Four digits</span></span>

### <a name="checksum"></a><span data-ttu-id="32d8c-3191">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="32d8c-3191">Checksum</span></span>

<span data-ttu-id="32d8c-3192">Oui</span><span class="sxs-lookup"><span data-stu-id="32d8c-3192">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="32d8c-3193">Définition</span><span class="sxs-lookup"><span data-stu-id="32d8c-3193">Definition</span></span>

<span data-ttu-id="32d8c-3194">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="32d8c-3194">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="32d8c-3195">La fonction Func_swedish_national_identifier trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="32d8c-3195">The function Func_swedish_national_identifier finds content that matches the pattern.</span></span>
- <span data-ttu-id="32d8c-3196">La somme de contrôle est correcte.</span><span class="sxs-lookup"><span data-stu-id="32d8c-3196">The checksum passes.</span></span>

```xml
<!-- Sweden National ID -->
<Entity id="f69aaf40-79be-4fac-8f05-fd1910d272c8" patternsProximity="300" recommendedConfidence="85">
    <Pattern confidenceLevel="85">
        <IdMatch idRef="Func_swedish_national_identifier" />
    </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="32d8c-3197">Mots clés</span><span class="sxs-lookup"><span data-stu-id="32d8c-3197">Keywords</span></span>

<span data-ttu-id="32d8c-3198">Non</span><span class="sxs-lookup"><span data-stu-id="32d8c-3198">No</span></span>
   
## <a name="sweden-passport-number"></a><span data-ttu-id="32d8c-3199">Numéro de passeport Suède</span><span class="sxs-lookup"><span data-stu-id="32d8c-3199">Sweden Passport Number</span></span>

### <a name="format"></a><span data-ttu-id="32d8c-3200">Format</span><span class="sxs-lookup"><span data-stu-id="32d8c-3200">Format</span></span>

<span data-ttu-id="32d8c-3201">Huit chiffres</span><span class="sxs-lookup"><span data-stu-id="32d8c-3201">Eight digits</span></span>

### <a name="pattern"></a><span data-ttu-id="32d8c-3202">Modèle</span><span class="sxs-lookup"><span data-stu-id="32d8c-3202">Pattern</span></span>

<span data-ttu-id="32d8c-3203">Huit chiffres consécutifs</span><span class="sxs-lookup"><span data-stu-id="32d8c-3203">Eight consecutive digits</span></span>

### <a name="checksum"></a><span data-ttu-id="32d8c-3204">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="32d8c-3204">Checksum</span></span>

<span data-ttu-id="32d8c-3205">Non</span><span class="sxs-lookup"><span data-stu-id="32d8c-3205">No</span></span>

### <a name="definition"></a><span data-ttu-id="32d8c-3206">Définition</span><span class="sxs-lookup"><span data-stu-id="32d8c-3206">Definition</span></span>

<span data-ttu-id="32d8c-3207">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="32d8c-3207">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="32d8c-3208">L’expression régulière Regex_sweden_passport_number trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="32d8c-3208">The regular expression Regex_sweden_passport_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="32d8c-3209">L’une des affirmations suivantes est vraie :</span><span class="sxs-lookup"><span data-stu-id="32d8c-3209">One of the following is true:</span></span>
    - <span data-ttu-id="32d8c-3210">Un mot clé figurant dans la liste Keyword_passport est trouvé.</span><span class="sxs-lookup"><span data-stu-id="32d8c-3210">A keyword from Keyword_passport is found.</span></span>
    - <span data-ttu-id="32d8c-3211">Un mot clé figurant dans la liste Keyword_sweden_passport est trouvé.</span><span class="sxs-lookup"><span data-stu-id="32d8c-3211">A keyword from Keyword_sweden_passport is found.</span></span>

```xml
<!-- Sweden Passport Number -->
<Entity id="ba4e7456-55a9-4d89-9140-c33673553526" patternsProximity="300" recommendedConfidence="75">
    <Pattern confidenceLevel="75">
        <IdMatch idRef="Regex_sweden_passport_number" />
        <Any minMatches="1">
          <Match idRef="Keyword_passport" />
          <Match idRef="Keyword_sweden_passport" />
        </Any>
    </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="32d8c-3212">Mots clés</span><span class="sxs-lookup"><span data-stu-id="32d8c-3212">Keywords</span></span>
   
#### <a name="keyword_sweden_passport"></a><span data-ttu-id="32d8c-3213">Keyword_sweden_passport</span><span class="sxs-lookup"><span data-stu-id="32d8c-3213">Keyword_sweden_passport</span></span>

- <span data-ttu-id="32d8c-3214">exigences en matière de visa</span><span class="sxs-lookup"><span data-stu-id="32d8c-3214">visa requirements</span></span> 
- <span data-ttu-id="32d8c-3215">Carte d’enregistrement d’une personne étrangère</span><span class="sxs-lookup"><span data-stu-id="32d8c-3215">Alien Registration Card</span></span> 
- <span data-ttu-id="32d8c-3216">Visas Schengen</span><span class="sxs-lookup"><span data-stu-id="32d8c-3216">Schengen visas</span></span> 
- <span data-ttu-id="32d8c-3217">Visa Schengen</span><span class="sxs-lookup"><span data-stu-id="32d8c-3217">Schengen visa</span></span> 
- <span data-ttu-id="32d8c-3218">Traitement du visa</span><span class="sxs-lookup"><span data-stu-id="32d8c-3218">Visa Processing</span></span> 
- <span data-ttu-id="32d8c-3219">Type de visa</span><span class="sxs-lookup"><span data-stu-id="32d8c-3219">Visa Type</span></span> 
- <span data-ttu-id="32d8c-3220">Entrée unique</span><span class="sxs-lookup"><span data-stu-id="32d8c-3220">Single Entry</span></span> 
- <span data-ttu-id="32d8c-3221">Entrée multiple</span><span class="sxs-lookup"><span data-stu-id="32d8c-3221">Multiple Entry</span></span> 
- <span data-ttu-id="32d8c-3222">Frais de traitement G3</span><span class="sxs-lookup"><span data-stu-id="32d8c-3222">G3 Processing Fees</span></span> 

#### <a name="keyword_passport"></a><span data-ttu-id="32d8c-3223">Keyword_passport</span><span class="sxs-lookup"><span data-stu-id="32d8c-3223">Keyword_passport</span></span>

- <span data-ttu-id="32d8c-3224">Numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="32d8c-3224">Passport Number</span></span> 
- <span data-ttu-id="32d8c-3225">N° de passeport</span><span class="sxs-lookup"><span data-stu-id="32d8c-3225">Passport No</span></span> 
- <span data-ttu-id="32d8c-3226"># Passeport</span><span class="sxs-lookup"><span data-stu-id="32d8c-3226">Passport #</span></span> 
- <span data-ttu-id="32d8c-3227">Tel #</span><span class="sxs-lookup"><span data-stu-id="32d8c-3227">Passport#</span></span> 
- <span data-ttu-id="32d8c-3228">PassportID</span><span class="sxs-lookup"><span data-stu-id="32d8c-3228">PassportID</span></span> 
- <span data-ttu-id="32d8c-3229">N ° passeport</span><span class="sxs-lookup"><span data-stu-id="32d8c-3229">Passportno</span></span> 
- <span data-ttu-id="32d8c-3230">passportnumber</span><span class="sxs-lookup"><span data-stu-id="32d8c-3230">passportnumber</span></span> 
- <span data-ttu-id="32d8c-3231">パスポート</span><span class="sxs-lookup"><span data-stu-id="32d8c-3231">パスポート</span></span> 
- <span data-ttu-id="32d8c-3232">パスポート番号</span><span class="sxs-lookup"><span data-stu-id="32d8c-3232">パスポート番号</span></span> 
- <span data-ttu-id="32d8c-3233">パスポートのNum</span><span class="sxs-lookup"><span data-stu-id="32d8c-3233">パスポートのNum</span></span> 
- <span data-ttu-id="32d8c-3234">パスポート＃</span><span class="sxs-lookup"><span data-stu-id="32d8c-3234">パスポート＃</span></span> 
- <span data-ttu-id="32d8c-3235">Numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="32d8c-3235">Numéro de passeport</span></span> 
- <span data-ttu-id="32d8c-3236">Passeport n°</span><span class="sxs-lookup"><span data-stu-id="32d8c-3236">Passeport n °</span></span> 
- <span data-ttu-id="32d8c-3237">Passeport numéro</span><span class="sxs-lookup"><span data-stu-id="32d8c-3237">Passeport Non</span></span> 
- <span data-ttu-id="32d8c-3238"># Passeport</span><span class="sxs-lookup"><span data-stu-id="32d8c-3238">Passeport #</span></span> 
- <span data-ttu-id="32d8c-3239">Passeport #</span><span class="sxs-lookup"><span data-stu-id="32d8c-3239">Passeport#</span></span> 
- <span data-ttu-id="32d8c-3240">PasseportNon</span><span class="sxs-lookup"><span data-stu-id="32d8c-3240">PasseportNon</span></span> 
- <span data-ttu-id="32d8c-3241">Passeportn °</span><span class="sxs-lookup"><span data-stu-id="32d8c-3241">Passeportn °</span></span> 
   
## <a name="swift-code"></a><span data-ttu-id="32d8c-3242">Code SWIFT</span><span class="sxs-lookup"><span data-stu-id="32d8c-3242">SWIFT Code</span></span>

### <a name="format"></a><span data-ttu-id="32d8c-3243">Format</span><span class="sxs-lookup"><span data-stu-id="32d8c-3243">Format</span></span>

<span data-ttu-id="32d8c-3244">Quatre lettres suivies de 5 à 31 lettres ou chiffres</span><span class="sxs-lookup"><span data-stu-id="32d8c-3244">Four letters followed by 5-31 letters or digits</span></span>

### <a name="pattern"></a><span data-ttu-id="32d8c-3245">Modèle</span><span class="sxs-lookup"><span data-stu-id="32d8c-3245">Pattern</span></span>

<span data-ttu-id="32d8c-3246">Quatre lettres suivies de 5 à 31 lettres ou chiffres :</span><span class="sxs-lookup"><span data-stu-id="32d8c-3246">Four letters followed by 5-31 letters or digits:</span></span>
- <span data-ttu-id="32d8c-3247">Code bancaire à quatre lettres (ne respectent pas la casse)</span><span class="sxs-lookup"><span data-stu-id="32d8c-3247">Four-letter bank code (not case sensitive)</span></span> 
- <span data-ttu-id="32d8c-3248">Un espace facultatif</span><span class="sxs-lookup"><span data-stu-id="32d8c-3248">An optional space</span></span> 
- <span data-ttu-id="32d8c-3249">4 à 28 lettres ou chiffres (numéro de compte bancaire de base (BBAN))</span><span class="sxs-lookup"><span data-stu-id="32d8c-3249">4-28 letters or digits (the Basic Bank Account Number (BBAN))</span></span> 
- <span data-ttu-id="32d8c-3250">Un espace facultatif</span><span class="sxs-lookup"><span data-stu-id="32d8c-3250">An optional space</span></span> 
- <span data-ttu-id="32d8c-3251">1 à 3 lettres ou chiffres (reste du BBAN)</span><span class="sxs-lookup"><span data-stu-id="32d8c-3251">1-3 letters or digits (remainder of the BBAN)</span></span>

### <a name="checksum"></a><span data-ttu-id="32d8c-3252">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="32d8c-3252">Checksum</span></span>

<span data-ttu-id="32d8c-3253">Non</span><span class="sxs-lookup"><span data-stu-id="32d8c-3253">No</span></span>

### <a name="definition"></a><span data-ttu-id="32d8c-3254">Définition</span><span class="sxs-lookup"><span data-stu-id="32d8c-3254">Definition</span></span>

<span data-ttu-id="32d8c-3255">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="32d8c-3255">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="32d8c-3256">L’expression régulière Regex_swift trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="32d8c-3256">The regular expression Regex_swift finds content that matches the pattern.</span></span>
- <span data-ttu-id="32d8c-3257">Un mot clé figurant dans la liste Keyword_swift est trouvé.</span><span class="sxs-lookup"><span data-stu-id="32d8c-3257">A keyword from Keyword_swift is found.</span></span>

```xml
<Entity id="cb2ab58c-9cb8-4c81-baf8-a4e106791df4" patternsProximity="300" recommendedConfidence="75">
<Pattern confidenceLevel="75">
        <IdMatch idRef="Regex_swift" />
        <Match idRef="Keyword_swift" />
    </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="32d8c-3258">Mots clés</span><span class="sxs-lookup"><span data-stu-id="32d8c-3258">Keywords</span></span>
   
#### <a name="keyword_swift"></a><span data-ttu-id="32d8c-3259">Keyword_swift</span><span class="sxs-lookup"><span data-stu-id="32d8c-3259">Keyword_swift</span></span>

- <span data-ttu-id="32d8c-3260">organisation internationale de normalisation 9362</span><span class="sxs-lookup"><span data-stu-id="32d8c-3260">international organization for standardization 9362</span></span> 
- <span data-ttu-id="32d8c-3261">ISO 9362</span><span class="sxs-lookup"><span data-stu-id="32d8c-3261">iso 9362</span></span> 
- <span data-ttu-id="32d8c-3262">iso9362</span><span class="sxs-lookup"><span data-stu-id="32d8c-3262">iso9362</span></span> 
- <span data-ttu-id="32d8c-3263">rapide\#</span><span class="sxs-lookup"><span data-stu-id="32d8c-3263">swift\#</span></span> 
- <span data-ttu-id="32d8c-3264">swiftcode</span><span class="sxs-lookup"><span data-stu-id="32d8c-3264">swiftcode</span></span> 
- <span data-ttu-id="32d8c-3265">swiftnumber</span><span class="sxs-lookup"><span data-stu-id="32d8c-3265">swiftnumber</span></span> 
- <span data-ttu-id="32d8c-3266">swiftroutingnumber</span><span class="sxs-lookup"><span data-stu-id="32d8c-3266">swiftroutingnumber</span></span> 
- <span data-ttu-id="32d8c-3267">code swift</span><span class="sxs-lookup"><span data-stu-id="32d8c-3267">swift code</span></span> 
- <span data-ttu-id="32d8c-3268"># numéro swift</span><span class="sxs-lookup"><span data-stu-id="32d8c-3268">swift number #</span></span> 
- <span data-ttu-id="32d8c-3269">numéro d’acheminement swift</span><span class="sxs-lookup"><span data-stu-id="32d8c-3269">swift routing number</span></span> 
- <span data-ttu-id="32d8c-3270">numéro BIC</span><span class="sxs-lookup"><span data-stu-id="32d8c-3270">bic number</span></span> 
- <span data-ttu-id="32d8c-3271">code BIC</span><span class="sxs-lookup"><span data-stu-id="32d8c-3271">bic code</span></span> 
- <span data-ttu-id="32d8c-3272">BIC\#</span><span class="sxs-lookup"><span data-stu-id="32d8c-3272">bic \#</span></span> 
- <span data-ttu-id="32d8c-3273">BIC\#</span><span class="sxs-lookup"><span data-stu-id="32d8c-3273">bic\#</span></span> 
- <span data-ttu-id="32d8c-3274">code d’identification bancaire</span><span class="sxs-lookup"><span data-stu-id="32d8c-3274">bank identifier code</span></span> 
- <span data-ttu-id="32d8c-3275">標準化 9362</span><span class="sxs-lookup"><span data-stu-id="32d8c-3275">標準化9362</span></span> 
- <span data-ttu-id="32d8c-3276">迅速＃</span><span class="sxs-lookup"><span data-stu-id="32d8c-3276">迅速＃</span></span> 
- <span data-ttu-id="32d8c-3277">SWIFTコード</span><span class="sxs-lookup"><span data-stu-id="32d8c-3277">SWIFTコード</span></span> 
- <span data-ttu-id="32d8c-3278">SWIFT番号</span><span class="sxs-lookup"><span data-stu-id="32d8c-3278">SWIFT番号</span></span> 
- <span data-ttu-id="32d8c-3279">迅速なルーティング番号</span><span class="sxs-lookup"><span data-stu-id="32d8c-3279">迅速なルーティング番号</span></span> 
- <span data-ttu-id="32d8c-3280">BIC番号</span><span class="sxs-lookup"><span data-stu-id="32d8c-3280">BIC番号</span></span> 
- <span data-ttu-id="32d8c-3281">BICコード</span><span class="sxs-lookup"><span data-stu-id="32d8c-3281">BICコード</span></span> 
- <span data-ttu-id="32d8c-3282">銀行識別コードのための国際組織</span><span class="sxs-lookup"><span data-stu-id="32d8c-3282">銀行識別コードのための国際組織</span></span> 
- <span data-ttu-id="32d8c-3283">Organisation internationale de normalisation 9362</span><span class="sxs-lookup"><span data-stu-id="32d8c-3283">Organisation internationale de normalisation 9362</span></span> 
- <span data-ttu-id="32d8c-3284">rapide\#</span><span class="sxs-lookup"><span data-stu-id="32d8c-3284">rapide \#</span></span> 
- <span data-ttu-id="32d8c-3285">code SWIFT</span><span class="sxs-lookup"><span data-stu-id="32d8c-3285">code SWIFT</span></span> 
- <span data-ttu-id="32d8c-3286">le numéro de swift</span><span class="sxs-lookup"><span data-stu-id="32d8c-3286">le numéro de swift</span></span> 
- <span data-ttu-id="32d8c-3287">swift numéro d’acheminement</span><span class="sxs-lookup"><span data-stu-id="32d8c-3287">swift numéro d'acheminement</span></span> 
- <span data-ttu-id="32d8c-3288">le numéro BIC</span><span class="sxs-lookup"><span data-stu-id="32d8c-3288">le numéro BIC</span></span> 
- <span data-ttu-id="32d8c-3289">\#BIC</span><span class="sxs-lookup"><span data-stu-id="32d8c-3289">\# BIC</span></span> 
- <span data-ttu-id="32d8c-3290">code identificateur de banque</span><span class="sxs-lookup"><span data-stu-id="32d8c-3290">code identificateur de banque</span></span> 
   
## <a name="taiwan-national-id"></a><span data-ttu-id="32d8c-3291">ID national à Taïwan</span><span class="sxs-lookup"><span data-stu-id="32d8c-3291">Taiwan National ID</span></span>

### <a name="format"></a><span data-ttu-id="32d8c-3292">Format</span><span class="sxs-lookup"><span data-stu-id="32d8c-3292">Format</span></span>

<span data-ttu-id="32d8c-3293">Une lettre  suivie de neuf chiffres</span><span class="sxs-lookup"><span data-stu-id="32d8c-3293">One letter (in English) followed by nine digits</span></span>

### <a name="pattern"></a><span data-ttu-id="32d8c-3294">Modèle</span><span class="sxs-lookup"><span data-stu-id="32d8c-3294">Pattern</span></span>

<span data-ttu-id="32d8c-3295">Une lettre suivie de neuf chiffres :</span><span class="sxs-lookup"><span data-stu-id="32d8c-3295">One letter (in English) followed by nine digits:</span></span>
- <span data-ttu-id="32d8c-3296">Une lettre (en anglais, ne respecte pas la casse)</span><span class="sxs-lookup"><span data-stu-id="32d8c-3296">One letter (in English, not case sensitive)</span></span> 
- <span data-ttu-id="32d8c-3297">Le chiffre « 1 » ou « 2 »</span><span class="sxs-lookup"><span data-stu-id="32d8c-3297">The digit "1" or "2"</span></span> 
- <span data-ttu-id="32d8c-3298">Huit chiffres</span><span class="sxs-lookup"><span data-stu-id="32d8c-3298">Eight digits</span></span>

### <a name="checksum"></a><span data-ttu-id="32d8c-3299">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="32d8c-3299">Checksum</span></span>

<span data-ttu-id="32d8c-3300">Oui</span><span class="sxs-lookup"><span data-stu-id="32d8c-3300">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="32d8c-3301">Définition</span><span class="sxs-lookup"><span data-stu-id="32d8c-3301">Definition</span></span>

<span data-ttu-id="32d8c-3302">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="32d8c-3302">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="32d8c-3303">La fonction Func_taiwanese_national_id trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="32d8c-3303">The function Func_taiwanese_national_id finds content that matches the pattern.</span></span>
- <span data-ttu-id="32d8c-3304">Un mot clé figurant dans la liste Keyword_taiwanese_national_id est trouvé.</span><span class="sxs-lookup"><span data-stu-id="32d8c-3304">A keyword from Keyword_taiwanese_national_id is found.</span></span>
- <span data-ttu-id="32d8c-3305">La somme de contrôle est correcte.</span><span class="sxs-lookup"><span data-stu-id="32d8c-3305">The checksum passes.</span></span>

```xml
<!-- Taiwanese National ID -->
<Entity id="4C7BFC34-8DD1-421D-8FB7-6C6182C2AF03" patternsProximity="300" recommendedConfidence="85">
      <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_taiwanese_national_id" />
          <Match idRef="Keyword_taiwanese_national_id" />
      </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="32d8c-3306">Mots clés</span><span class="sxs-lookup"><span data-stu-id="32d8c-3306">Keywords</span></span>

#### <a name="keyword_taiwanese_national_id"></a><span data-ttu-id="32d8c-3307">Keyword_taiwanese_national_id</span><span class="sxs-lookup"><span data-stu-id="32d8c-3307">Keyword_taiwanese_national_id</span></span>

- <span data-ttu-id="32d8c-3308">身份證字號</span><span class="sxs-lookup"><span data-stu-id="32d8c-3308">身份證字號</span></span> 
- <span data-ttu-id="32d8c-3309">身份證</span><span class="sxs-lookup"><span data-stu-id="32d8c-3309">身份證</span></span> 
- <span data-ttu-id="32d8c-3310">身份證號碼</span><span class="sxs-lookup"><span data-stu-id="32d8c-3310">身份證號碼</span></span> 
- <span data-ttu-id="32d8c-3311">身份證號</span><span class="sxs-lookup"><span data-stu-id="32d8c-3311">身份證號</span></span> 
- <span data-ttu-id="32d8c-3312">身分證字號</span><span class="sxs-lookup"><span data-stu-id="32d8c-3312">身分證字號</span></span> 
- <span data-ttu-id="32d8c-3313">身分證</span><span class="sxs-lookup"><span data-stu-id="32d8c-3313">身分證</span></span> 
- <span data-ttu-id="32d8c-3314">身分證號碼</span><span class="sxs-lookup"><span data-stu-id="32d8c-3314">身分證號碼</span></span> 
- <span data-ttu-id="32d8c-3315">身份證號</span><span class="sxs-lookup"><span data-stu-id="32d8c-3315">身份證號</span></span> 
- <span data-ttu-id="32d8c-3316">身分證統一編號</span><span class="sxs-lookup"><span data-stu-id="32d8c-3316">身分證統一編號</span></span> 
- <span data-ttu-id="32d8c-3317">國民身分證統一編號</span><span class="sxs-lookup"><span data-stu-id="32d8c-3317">國民身分證統一編號</span></span> 
- <span data-ttu-id="32d8c-3318">簽名</span><span class="sxs-lookup"><span data-stu-id="32d8c-3318">簽名</span></span> 
- <span data-ttu-id="32d8c-3319">蓋章</span><span class="sxs-lookup"><span data-stu-id="32d8c-3319">蓋章</span></span> 
- <span data-ttu-id="32d8c-3320">簽名或蓋章</span><span class="sxs-lookup"><span data-stu-id="32d8c-3320">簽名或蓋章</span></span> 
- <span data-ttu-id="32d8c-3321">簽章</span><span class="sxs-lookup"><span data-stu-id="32d8c-3321">簽章</span></span>   
   
## <a name="taiwan-passport-number"></a><span data-ttu-id="32d8c-3322">	Numéro de passeport Taïwan</span><span class="sxs-lookup"><span data-stu-id="32d8c-3322">Taiwan Passport Number</span></span>

### <a name="format"></a><span data-ttu-id="32d8c-3323">Format</span><span class="sxs-lookup"><span data-stu-id="32d8c-3323">Format</span></span>

- <span data-ttu-id="32d8c-3324">Numéro de passeport biométrique : neuf chiffres</span><span class="sxs-lookup"><span data-stu-id="32d8c-3324">Biometric passport number: Nine digits</span></span>
- <span data-ttu-id="32d8c-3325">Numéro de passeport non biométrique : neuf chiffres</span><span class="sxs-lookup"><span data-stu-id="32d8c-3325">Non-biometric passport number: Nine digits</span></span>

### <a name="pattern"></a><span data-ttu-id="32d8c-3326">Modèle</span><span class="sxs-lookup"><span data-stu-id="32d8c-3326">Pattern</span></span>
<span data-ttu-id="32d8c-3327">Numéro de passeport biométrique :</span><span class="sxs-lookup"><span data-stu-id="32d8c-3327">Biometric passport number:</span></span>
- <span data-ttu-id="32d8c-3328">Le chiffre « 3 » </span><span class="sxs-lookup"><span data-stu-id="32d8c-3328">The digit "3"</span></span> 
- <span data-ttu-id="32d8c-3329">Huit chiffres</span><span class="sxs-lookup"><span data-stu-id="32d8c-3329">Eight digits</span></span>

<span data-ttu-id="32d8c-3330">Numéro de passeport non biométrique :</span><span class="sxs-lookup"><span data-stu-id="32d8c-3330">Non-biometric passport number:</span></span>
- <span data-ttu-id="32d8c-3331">Neuf chiffres</span><span class="sxs-lookup"><span data-stu-id="32d8c-3331">Nine digits</span></span>

### <a name="checksum"></a><span data-ttu-id="32d8c-3332">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="32d8c-3332">Checksum</span></span>

<span data-ttu-id="32d8c-3333">Non</span><span class="sxs-lookup"><span data-stu-id="32d8c-3333">No</span></span>

### <a name="definition"></a><span data-ttu-id="32d8c-3334">Définition</span><span class="sxs-lookup"><span data-stu-id="32d8c-3334">Definition</span></span>

<span data-ttu-id="32d8c-3335">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="32d8c-3335">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="32d8c-3336">L’expression régulière Regex_taiwan_passport trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="32d8c-3336">The regular expression Regex_taiwan_passport finds content that matches the pattern.</span></span>
- <span data-ttu-id="32d8c-3337">Un mot clé figurant dans la liste Keyword_taiwan_passport est trouvé.</span><span class="sxs-lookup"><span data-stu-id="32d8c-3337">A keyword from Keyword_taiwan_passport is found.</span></span>

```xml
<!-- Taiwan Passport Number -->
<Entity id="e7251cb4-4c2c-41df-963e-924eb3dae04a" recommendedConfidence="75" patternsProximity="300">
  <Pattern confidenceLevel="75">
     <IdMatch idRef="Regex_taiwan_passport"/>
     <Match idRef="Keyword_taiwan_passport"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="32d8c-3338">Mots clés</span><span class="sxs-lookup"><span data-stu-id="32d8c-3338">Keywords</span></span>

#### <a name="keyword_taiwan_passport"></a><span data-ttu-id="32d8c-3339">Keyword_taiwan_passport</span><span class="sxs-lookup"><span data-stu-id="32d8c-3339">Keyword_taiwan_passport</span></span>

- <span data-ttu-id="32d8c-3340">ROC passport number</span><span class="sxs-lookup"><span data-stu-id="32d8c-3340">ROC passport number</span></span> 
- <span data-ttu-id="32d8c-3341">Passport number</span><span class="sxs-lookup"><span data-stu-id="32d8c-3341">Passport number</span></span> 
- <span data-ttu-id="32d8c-3342">Passport no</span><span class="sxs-lookup"><span data-stu-id="32d8c-3342">Passport no</span></span> 
- <span data-ttu-id="32d8c-3343">Passport Num</span><span class="sxs-lookup"><span data-stu-id="32d8c-3343">Passport Num</span></span> 
- <span data-ttu-id="32d8c-3344">Passport #</span><span class="sxs-lookup"><span data-stu-id="32d8c-3344">Passport #</span></span> 
- <span data-ttu-id="32d8c-3345">护照</span><span class="sxs-lookup"><span data-stu-id="32d8c-3345">护照</span></span> 
- <span data-ttu-id="32d8c-3346">中華民國護照</span><span class="sxs-lookup"><span data-stu-id="32d8c-3346">中華民國護照</span></span> 
- <span data-ttu-id="32d8c-3347">Zhōnghuá Mínguó hùzhào</span><span class="sxs-lookup"><span data-stu-id="32d8c-3347">Zhōnghuá Mínguó hùzhào</span></span>
   
## <a name="taiwan-resident-certificate-arctarc-number"></a><span data-ttu-id="32d8c-3348">Numéro de certificat de résident (ARC/TARC) Taïwan</span><span class="sxs-lookup"><span data-stu-id="32d8c-3348">Taiwan Resident Certificate (ARC/TARC) Number</span></span>

### <a name="format"></a><span data-ttu-id="32d8c-3349">Format</span><span class="sxs-lookup"><span data-stu-id="32d8c-3349">Format</span></span>

<span data-ttu-id="32d8c-3350">10 lettres et chiffres</span><span class="sxs-lookup"><span data-stu-id="32d8c-3350">10 letters and digits</span></span>

### <a name="pattern"></a><span data-ttu-id="32d8c-3351">Modèle</span><span class="sxs-lookup"><span data-stu-id="32d8c-3351">Pattern</span></span>

<span data-ttu-id="32d8c-3352">10 lettres et chiffres :</span><span class="sxs-lookup"><span data-stu-id="32d8c-3352">10 letters and digits:</span></span>
- <span data-ttu-id="32d8c-3353">Deux lettres (ne respectant pas la casse) </span><span class="sxs-lookup"><span data-stu-id="32d8c-3353">Two letters (not case sensitive)</span></span> 
- <span data-ttu-id="32d8c-3354">Huit chiffres</span><span class="sxs-lookup"><span data-stu-id="32d8c-3354">Eight digits</span></span>

### <a name="checksum"></a><span data-ttu-id="32d8c-3355">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="32d8c-3355">Checksum</span></span>

<span data-ttu-id="32d8c-3356">Non</span><span class="sxs-lookup"><span data-stu-id="32d8c-3356">No</span></span>

### <a name="definition"></a><span data-ttu-id="32d8c-3357">Définition</span><span class="sxs-lookup"><span data-stu-id="32d8c-3357">Definition</span></span>

<span data-ttu-id="32d8c-3358">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="32d8c-3358">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="32d8c-3359">L’expression régulière Regex_taiwan_resident_certificate trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="32d8c-3359">The regular expression Regex_taiwan_resident_certificate finds content that matches the pattern.</span></span>
- <span data-ttu-id="32d8c-3360">Un mot clé figurant dans la liste Keyword_taiwan_resident_certificate est trouvé.</span><span class="sxs-lookup"><span data-stu-id="32d8c-3360">A keyword from Keyword_taiwan_resident_certificate is found.</span></span>

```xml
<!-- Taiwan Resident Certificate (ARC/TARC) -->
<Entity id="48269fec-05ea-46ea-b326-f5623a58c6e9" recommendedConfidence="75" patternsProximity="300">
  <Pattern confidenceLevel="75">
     <IdMatch idRef="Regex_taiwan_resident_certificate"/>
     <Match idRef="Keyword_taiwan_resident_certificate"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="32d8c-3361">Mots clés</span><span class="sxs-lookup"><span data-stu-id="32d8c-3361">Keywords</span></span>

#### <a name="keyword_taiwan_resident_certificate"></a><span data-ttu-id="32d8c-3362">Keyword_taiwan_resident_certificate</span><span class="sxs-lookup"><span data-stu-id="32d8c-3362">Keyword_taiwan_resident_certificate</span></span>

- <span data-ttu-id="32d8c-3363">Resident Certificate</span><span class="sxs-lookup"><span data-stu-id="32d8c-3363">Resident Certificate</span></span> 
- <span data-ttu-id="32d8c-3364">Resident Cert</span><span class="sxs-lookup"><span data-stu-id="32d8c-3364">Resident Cert</span></span> 
- <span data-ttu-id="32d8c-3365">Resident Cert.</span><span class="sxs-lookup"><span data-stu-id="32d8c-3365">Resident Cert.</span></span> 
- <span data-ttu-id="32d8c-3366">Identification card</span><span class="sxs-lookup"><span data-stu-id="32d8c-3366">Identification card</span></span> 
- <span data-ttu-id="32d8c-3367">Alien Resident Certificate</span><span class="sxs-lookup"><span data-stu-id="32d8c-3367">Alien Resident Certificate</span></span> 
- <span data-ttu-id="32d8c-3368">ARC</span><span class="sxs-lookup"><span data-stu-id="32d8c-3368">ARC</span></span> 
- <span data-ttu-id="32d8c-3369">Taiwan Area Resident Certificate</span><span class="sxs-lookup"><span data-stu-id="32d8c-3369">Taiwan Area Resident Certificate</span></span> 
- <span data-ttu-id="32d8c-3370">TARC</span><span class="sxs-lookup"><span data-stu-id="32d8c-3370">TARC</span></span> 
- <span data-ttu-id="32d8c-3371">居留證</span><span class="sxs-lookup"><span data-stu-id="32d8c-3371">居留證</span></span> 
- <span data-ttu-id="32d8c-3372">外僑居留證</span><span class="sxs-lookup"><span data-stu-id="32d8c-3372">外僑居留證</span></span> 
- <span data-ttu-id="32d8c-3373">台灣地區居留證</span><span class="sxs-lookup"><span data-stu-id="32d8c-3373">台灣地區居留證</span></span> 

## <a name="thai-population-identification-code"></a><span data-ttu-id="32d8c-3374">Code d’identification du remplissage thaï</span><span class="sxs-lookup"><span data-stu-id="32d8c-3374">Thai Population Identification Code</span></span>

### <a name="format"></a><span data-ttu-id="32d8c-3375">Format</span><span class="sxs-lookup"><span data-stu-id="32d8c-3375">Format</span></span>

<span data-ttu-id="32d8c-3376">13 chiffres</span><span class="sxs-lookup"><span data-stu-id="32d8c-3376">13 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="32d8c-3377">Modèle</span><span class="sxs-lookup"><span data-stu-id="32d8c-3377">Pattern</span></span>

<span data-ttu-id="32d8c-3378">13 chiffres :</span><span class="sxs-lookup"><span data-stu-id="32d8c-3378">13 digits:</span></span>
- <span data-ttu-id="32d8c-3379">Le premier chiffre est différent de 0 ou de 9</span><span class="sxs-lookup"><span data-stu-id="32d8c-3379">First digit is not 0 or 9</span></span> 
- <span data-ttu-id="32d8c-3380">12 chiffres</span><span class="sxs-lookup"><span data-stu-id="32d8c-3380">12 digits</span></span>

### <a name="checksum"></a><span data-ttu-id="32d8c-3381">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="32d8c-3381">Checksum</span></span>

<span data-ttu-id="32d8c-3382">Oui</span><span class="sxs-lookup"><span data-stu-id="32d8c-3382">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="32d8c-3383">Définition</span><span class="sxs-lookup"><span data-stu-id="32d8c-3383">Definition</span></span>

<span data-ttu-id="32d8c-3384">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="32d8c-3384">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="32d8c-3385">La fonction Func_Thai_Citizen_Id trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="32d8c-3385">The function Func_Thai_Citizen_Id finds content that matches the pattern.</span></span>
- <span data-ttu-id="32d8c-3386">Un mot clé depuis Keyword_Thai_Citizen_Id est trouvé.</span><span class="sxs-lookup"><span data-stu-id="32d8c-3386">A keyword from Keyword_Thai_Citizen_Id is found.</span></span>

<span data-ttu-id="32d8c-3387">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="32d8c-3387">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="32d8c-3388">La fonction Func_Thai_Citizen_Id trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="32d8c-3388">The function Func_Thai_Citizen_Id finds content that matches the pattern.</span></span>

```xml
<!-- Thai Citizen ID -->
-<Entity id="44ca9e86-ead7-4c5d-884a-e2eaa401515e" recommendedConfidence="75" patternsProximity="300">
   -<Pattern confidenceLevel="85">
      <IdMatch idRef="Func_Thai_Citizen_Id"/>
      <Match idRef="Keyword_Thai_Citizen_Id"/>
   </Pattern>
   -<Pattern confidenceLevel="75">
      <IdMatch idRef="Func_Thai_Citizen_Id"/>
   </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="32d8c-3389">Mots clés</span><span class="sxs-lookup"><span data-stu-id="32d8c-3389">Keywords</span></span>

#### <a name="keyword_thai_citizen_id"></a><span data-ttu-id="32d8c-3390">Keyword_Thai_Citizen_Id</span><span class="sxs-lookup"><span data-stu-id="32d8c-3390">Keyword_Thai_Citizen_Id</span></span>

- <span data-ttu-id="32d8c-3391">ID Number</span><span class="sxs-lookup"><span data-stu-id="32d8c-3391">ID Number</span></span>
- <span data-ttu-id="32d8c-3392">Numéro d’identification</span><span class="sxs-lookup"><span data-stu-id="32d8c-3392">Identification Number</span></span>
- <span data-ttu-id="32d8c-3393">บัตรประชาชน</span><span class="sxs-lookup"><span data-stu-id="32d8c-3393">บัตรประชาชน</span></span>
- <span data-ttu-id="32d8c-3394">รหัสบัตรประชาชน</span><span class="sxs-lookup"><span data-stu-id="32d8c-3394">รหัสบัตรประชาชน</span></span>
- <span data-ttu-id="32d8c-3395">บัตรประชาชน</span><span class="sxs-lookup"><span data-stu-id="32d8c-3395">บัตรประชาชน</span></span>
- <span data-ttu-id="32d8c-3396">รหัสบัตรประชาชน</span><span class="sxs-lookup"><span data-stu-id="32d8c-3396">รหัสบัตรประชาชน</span></span>
  
## <a name="turkish-national-identification-number"></a><span data-ttu-id="32d8c-3397">Numéro d’identification national turc</span><span class="sxs-lookup"><span data-stu-id="32d8c-3397">Turkish National Identification Number</span></span>

### <a name="format"></a><span data-ttu-id="32d8c-3398">Format</span><span class="sxs-lookup"><span data-stu-id="32d8c-3398">Format</span></span>

<span data-ttu-id="32d8c-3399">11 chiffres</span><span class="sxs-lookup"><span data-stu-id="32d8c-3399">11 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="32d8c-3400">Modèle</span><span class="sxs-lookup"><span data-stu-id="32d8c-3400">Pattern</span></span>

<span data-ttu-id="32d8c-3401">11 chiffres</span><span class="sxs-lookup"><span data-stu-id="32d8c-3401">11 digits</span></span>

### <a name="checksum"></a><span data-ttu-id="32d8c-3402">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="32d8c-3402">Checksum</span></span>

<span data-ttu-id="32d8c-3403">Oui</span><span class="sxs-lookup"><span data-stu-id="32d8c-3403">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="32d8c-3404">Définition</span><span class="sxs-lookup"><span data-stu-id="32d8c-3404">Definition</span></span>

<span data-ttu-id="32d8c-3405">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="32d8c-3405">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="32d8c-3406">La fonction Func_Turkish_National_Id trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="32d8c-3406">The function Func_Turkish_National_Id finds content that matches the pattern.</span></span>
- <span data-ttu-id="32d8c-3407">Un mot clé depuis Keyword_Turkish_National_Id est trouvé.</span><span class="sxs-lookup"><span data-stu-id="32d8c-3407">A keyword from Keyword_Turkish_National_Id is found.</span></span>

<span data-ttu-id="32d8c-3408">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="32d8c-3408">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="32d8c-3409">La fonction Func_Turkish_National_Id trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="32d8c-3409">The function Func_Turkish_National_Id finds content that matches the pattern.</span></span>

```xml
<!-- Turkish National Identity -->
-<Entity id="fb621f20-3876-4cfc-acec-8c8e73ca32c7" recommendedConfidence="75" patternsProximity="300">
   -<Pattern confidenceLevel="85">
      <IdMatch idRef="Func_Turkish_National_Id"/>
      <Match idRef="Keyword_Turkish_National_Id"/>
   </Pattern>
   -<Pattern confidenceLevel="75">
      <IdMatch idRef="Func_Turkish_National_Id"/>
   </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="32d8c-3410">Mots clés</span><span class="sxs-lookup"><span data-stu-id="32d8c-3410">Keywords</span></span>

#### <a name="keyword_turkish_national_id"></a><span data-ttu-id="32d8c-3411">Keyword_Turkish_National_Id</span><span class="sxs-lookup"><span data-stu-id="32d8c-3411">Keyword_Turkish_National_Id</span></span>

- <span data-ttu-id="32d8c-3412">TC Kimlik non</span><span class="sxs-lookup"><span data-stu-id="32d8c-3412">TC Kimlik No</span></span>
- <span data-ttu-id="32d8c-3413">TC Kimlik numarası</span><span class="sxs-lookup"><span data-stu-id="32d8c-3413">TC Kimlik numarası</span></span>
- <span data-ttu-id="32d8c-3414">Vatandaşlık numarası</span><span class="sxs-lookup"><span data-stu-id="32d8c-3414">Vatandaşlık numarası</span></span>
- <span data-ttu-id="32d8c-3415">Vatandaşlık non</span><span class="sxs-lookup"><span data-stu-id="32d8c-3415">Vatandaşlık no</span></span>

## <a name="uk-drivers-license-number"></a><span data-ttu-id="32d8c-p142">Numéro de permis de conduire Royaume-Uni</span><span class="sxs-lookup"><span data-stu-id="32d8c-p142">U.K. Driver's License Number</span></span>

### <a name="format"></a><span data-ttu-id="32d8c-3418">Format</span><span class="sxs-lookup"><span data-stu-id="32d8c-3418">Format</span></span>

<span data-ttu-id="32d8c-3419">Combinaison de 18 lettres et chiffres au format spécifié</span><span class="sxs-lookup"><span data-stu-id="32d8c-3419">Combination of 18 letters and digits in the specified format</span></span>

### <a name="pattern"></a><span data-ttu-id="32d8c-3420">Modèle</span><span class="sxs-lookup"><span data-stu-id="32d8c-3420">Pattern</span></span>

<span data-ttu-id="32d8c-3421">18 lettres et chiffres</span><span class="sxs-lookup"><span data-stu-id="32d8c-3421">18 letters and digits:</span></span>
- <span data-ttu-id="32d8c-3422">Cinq lettres (ne respectent pas la casse) ou le chiffre « 9 » à la place d’une lettre</span><span class="sxs-lookup"><span data-stu-id="32d8c-3422">Five letters (not case sensitive) or the digit "9" in place of a letter</span></span> 
- <span data-ttu-id="32d8c-3423">Un chiffre</span><span class="sxs-lookup"><span data-stu-id="32d8c-3423">One digit</span></span> 
- <span data-ttu-id="32d8c-3424">Cinq chiffres au format de date MMDDY pour la date de naissance (7 caractères sont incrémentés de 50 si le pilote est femelle, c’est-à-dire 51 vers 62 au lieu de 01 à 12)</span><span class="sxs-lookup"><span data-stu-id="32d8c-3424">Five digits in the date format MMDDY for date of birth (7th character is incremented by 50 if driver is female, i.e. 51 to 62 instead of 01 to 12)</span></span>
- <span data-ttu-id="32d8c-3425">Deux lettres (ne respectent pas la casse) ou le chiffre « 9 » à la place d’une lettre</span><span class="sxs-lookup"><span data-stu-id="32d8c-3425">Two letters (not case sensitive) or the digit "9" in place of a letter</span></span> 
- <span data-ttu-id="32d8c-3426">Cinq chiffres</span><span class="sxs-lookup"><span data-stu-id="32d8c-3426">Five digits</span></span>

### <a name="checksum"></a><span data-ttu-id="32d8c-3427">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="32d8c-3427">Checksum</span></span>

<span data-ttu-id="32d8c-3428">Oui</span><span class="sxs-lookup"><span data-stu-id="32d8c-3428">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="32d8c-3429">Définition</span><span class="sxs-lookup"><span data-stu-id="32d8c-3429">Definition</span></span>

<span data-ttu-id="32d8c-3430">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="32d8c-3430">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="32d8c-3431">La fonction Func_uk_drivers_license trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="32d8c-3431">The function Func_uk_drivers_license finds content that matches the pattern.</span></span>
- <span data-ttu-id="32d8c-3432">Un mot clé figurant dans la liste Keyword_uk_drivers_license est trouvé.</span><span class="sxs-lookup"><span data-stu-id="32d8c-3432">A keyword from Keyword_uk_drivers_license is found.</span></span>
- <span data-ttu-id="32d8c-3433">La somme de contrôle est correcte.</span><span class="sxs-lookup"><span data-stu-id="32d8c-3433">The checksum passes.</span></span>

```xml
<!-- U.K. Driver's License Number -->
<Entity id="f93de4be-d94c-40df-a8be-461738047551" patternsProximity="300" recommendedConfidence="75">
    <Pattern confidenceLevel="75">
        <IdMatch idRef="Func_uk_drivers_license" />
        <Match idRef="Keyword_uk_drivers_license" />
    </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="32d8c-3434">Mots clés</span><span class="sxs-lookup"><span data-stu-id="32d8c-3434">Keywords</span></span>

#### <a name="keyword_uk_drivers_license"></a><span data-ttu-id="32d8c-3435">Keyword_uk_drivers_license</span><span class="sxs-lookup"><span data-stu-id="32d8c-3435">Keyword_uk_drivers_license</span></span>

- <span data-ttu-id="32d8c-3436">DVLA</span><span class="sxs-lookup"><span data-stu-id="32d8c-3436">DVLA</span></span> 
- <span data-ttu-id="32d8c-3437">véhicule utilitaire léger</span><span class="sxs-lookup"><span data-stu-id="32d8c-3437">light vans</span></span> 
- <span data-ttu-id="32d8c-3438">quadbikes</span><span class="sxs-lookup"><span data-stu-id="32d8c-3438">quadbikes</span></span> 
- <span data-ttu-id="32d8c-3439">automobiles</span><span class="sxs-lookup"><span data-stu-id="32d8c-3439">motor cars</span></span> 
- <span data-ttu-id="32d8c-3440">125cc</span><span class="sxs-lookup"><span data-stu-id="32d8c-3440">125cc</span></span> 
- <span data-ttu-id="32d8c-3441">annexes</span><span class="sxs-lookup"><span data-stu-id="32d8c-3441">sidecar</span></span> 
- <span data-ttu-id="32d8c-3442">tricycles</span><span class="sxs-lookup"><span data-stu-id="32d8c-3442">tricycles</span></span> 
- <span data-ttu-id="32d8c-3443">Side</span><span class="sxs-lookup"><span data-stu-id="32d8c-3443">motorcycles</span></span> 
- <span data-ttu-id="32d8c-3444">permis de conduire plastifié</span><span class="sxs-lookup"><span data-stu-id="32d8c-3444">photocard licence</span></span> 
- <span data-ttu-id="32d8c-3445">apprentis conducteurs</span><span class="sxs-lookup"><span data-stu-id="32d8c-3445">learner drivers</span></span> 
- <span data-ttu-id="32d8c-3446">titulaire du permis</span><span class="sxs-lookup"><span data-stu-id="32d8c-3446">licence holder</span></span> 
- <span data-ttu-id="32d8c-3447">titulaires du permis</span><span class="sxs-lookup"><span data-stu-id="32d8c-3447">licence holders</span></span> 
- <span data-ttu-id="32d8c-3448">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="32d8c-3448">driving licences</span></span> 
- <span data-ttu-id="32d8c-3449">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="32d8c-3449">driving licence</span></span> 
- <span data-ttu-id="32d8c-3450">voiture à double commande</span><span class="sxs-lookup"><span data-stu-id="32d8c-3450">dual control car</span></span> 
   
## <a name="uk-electoral-roll-number"></a><span data-ttu-id="32d8c-p143">Numéro de liste électorale Royaume-Uni</span><span class="sxs-lookup"><span data-stu-id="32d8c-p143">U.K. Electoral Roll Number</span></span>

### <a name="format"></a><span data-ttu-id="32d8c-3453">Format</span><span class="sxs-lookup"><span data-stu-id="32d8c-3453">Format</span></span>

<span data-ttu-id="32d8c-3454">Deux lettres suivies de 1 à 4 chiffres</span><span class="sxs-lookup"><span data-stu-id="32d8c-3454">Two letters followed by 1-4 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="32d8c-3455">Modèle</span><span class="sxs-lookup"><span data-stu-id="32d8c-3455">Pattern</span></span>

<span data-ttu-id="32d8c-3456">Deux lettres (ne respectant pas la casse) suivies de 1 à 4 chiffres</span><span class="sxs-lookup"><span data-stu-id="32d8c-3456">Two letters (not case sensitive) followed by 1-4 numbers</span></span>

### <a name="checksum"></a><span data-ttu-id="32d8c-3457">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="32d8c-3457">Checksum</span></span>

<span data-ttu-id="32d8c-3458">Non</span><span class="sxs-lookup"><span data-stu-id="32d8c-3458">No</span></span>

### <a name="definition"></a><span data-ttu-id="32d8c-3459">Définition</span><span class="sxs-lookup"><span data-stu-id="32d8c-3459">Definition</span></span>

<span data-ttu-id="32d8c-3460">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="32d8c-3460">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="32d8c-3461">L’expression régulière Regex_uk_electoral trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="32d8c-3461">The regular expression Regex_uk_electoral finds content that matches the pattern.</span></span>
- <span data-ttu-id="32d8c-3462">Un mot clé figurant dans la liste Keyword_uk_electoral est trouvé.</span><span class="sxs-lookup"><span data-stu-id="32d8c-3462">A keyword from Keyword_uk_electoral is found.</span></span>

```xml
<!-- U.K. Electoral Number -->
<Entity id="a3eea206-dc0c-4f06-9e22-aa1be3059963" patternsProximity="300" recommendedConfidence="75">
    <Pattern confidenceLevel="75">
        <IdMatch idRef="Regex_uk_electoral" />
        <Any minMatches="1">
          <Match idRef="Keyword_uk_electoral" />
        </Any>
    </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="32d8c-3463">Mots clés</span><span class="sxs-lookup"><span data-stu-id="32d8c-3463">Keywords</span></span>

#### <a name="keyword_uk_electoral"></a><span data-ttu-id="32d8c-3464">Keyword_uk_electoral</span><span class="sxs-lookup"><span data-stu-id="32d8c-3464">Keyword_uk_electoral</span></span>

- <span data-ttu-id="32d8c-3465">nomination au conseil</span><span class="sxs-lookup"><span data-stu-id="32d8c-3465">council nomination</span></span> 
- <span data-ttu-id="32d8c-3466">formulaire de nomination</span><span class="sxs-lookup"><span data-stu-id="32d8c-3466">nomination form</span></span> 
- <span data-ttu-id="32d8c-3467">registre électoral</span><span class="sxs-lookup"><span data-stu-id="32d8c-3467">electoral register</span></span> 
- <span data-ttu-id="32d8c-3468">liste électorale</span><span class="sxs-lookup"><span data-stu-id="32d8c-3468">electoral roll</span></span>

   
## <a name="uk-national-health-service-number"></a><span data-ttu-id="32d8c-p144">Numéro national des services de santé Royaume-Uni</span><span class="sxs-lookup"><span data-stu-id="32d8c-p144">U.K. National Health Service Number</span></span>

### <a name="format"></a><span data-ttu-id="32d8c-3471">Format</span><span class="sxs-lookup"><span data-stu-id="32d8c-3471">Format</span></span>

<span data-ttu-id="32d8c-3472">10 à 17 chiffres séparés par des espaces</span><span class="sxs-lookup"><span data-stu-id="32d8c-3472">10-17 digits separated by spaces</span></span>

### <a name="pattern"></a><span data-ttu-id="32d8c-3473">Modèle</span><span class="sxs-lookup"><span data-stu-id="32d8c-3473">Pattern</span></span>

<span data-ttu-id="32d8c-3474">10 à 17 chiffres :</span><span class="sxs-lookup"><span data-stu-id="32d8c-3474">10-17 digits:</span></span>
- <span data-ttu-id="32d8c-3475">3 ou 10 chiffres</span><span class="sxs-lookup"><span data-stu-id="32d8c-3475">Either 3 or 10 digits</span></span> 
- <span data-ttu-id="32d8c-3476">Un espace</span><span class="sxs-lookup"><span data-stu-id="32d8c-3476">A space</span></span> 
- <span data-ttu-id="32d8c-3477">Trois chiffres</span><span class="sxs-lookup"><span data-stu-id="32d8c-3477">Three digits</span></span> 
- <span data-ttu-id="32d8c-3478">Un espace</span><span class="sxs-lookup"><span data-stu-id="32d8c-3478">A space</span></span> 
- <span data-ttu-id="32d8c-3479">Quatre chiffres</span><span class="sxs-lookup"><span data-stu-id="32d8c-3479">Four digits</span></span>

### <a name="checksum"></a><span data-ttu-id="32d8c-3480">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="32d8c-3480">Checksum</span></span>

<span data-ttu-id="32d8c-3481">Oui</span><span class="sxs-lookup"><span data-stu-id="32d8c-3481">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="32d8c-3482">Définition</span><span class="sxs-lookup"><span data-stu-id="32d8c-3482">Definition</span></span>

<span data-ttu-id="32d8c-3483">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="32d8c-3483">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="32d8c-3484">La fonction Func_uk_nhs_number trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="32d8c-3484">The function Func_uk_nhs_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="32d8c-3485">L’une des affirmations suivantes est vraie :</span><span class="sxs-lookup"><span data-stu-id="32d8c-3485">One of the following is true:</span></span>
    - <span data-ttu-id="32d8c-3486">Un mot clé figurant dans la liste Keyword_uk_nhs_number est trouvé.</span><span class="sxs-lookup"><span data-stu-id="32d8c-3486">A keyword from Keyword_uk_nhs_number is found.</span></span>
    - <span data-ttu-id="32d8c-3487">Un mot clé figurant dans la liste Keyword_uk_nhs_number1 est trouvé.</span><span class="sxs-lookup"><span data-stu-id="32d8c-3487">A keyword from Keyword_uk_nhs_number1 is found.</span></span>
    - <span data-ttu-id="32d8c-3488">Un mot clé figurant dans la liste Keyword_uk_nhs_number_dob est trouvé.</span><span class="sxs-lookup"><span data-stu-id="32d8c-3488">A keyword from Keyword_uk_nhs_number_dob is found.</span></span>
- <span data-ttu-id="32d8c-3489">La somme de contrôle est correcte.</span><span class="sxs-lookup"><span data-stu-id="32d8c-3489">The checksum passes.</span></span>

```xml
<!-- U.K. NHS Number -->
<Entity id="3192014e-2a16-44e9-aa69-4b20375c9a78" patternsProximity="300" recommendedConfidence="85">
    <Pattern confidenceLevel="85">
        <IdMatch idRef="Func_uk_nhs_number" />
        <Any minMatches="1">
          <Match idRef="Keyword_uk_nhs_number" />
          <Match idRef="Keyword_uk_nhs_number1" />
          <Match idRef="Keyword_uk_nhs_number_dob" />
        </Any>
    </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="32d8c-3490">Mots clés</span><span class="sxs-lookup"><span data-stu-id="32d8c-3490">Keywords</span></span>
   
#### <a name="keyword_uk_nhs_number"></a><span data-ttu-id="32d8c-3491">Keyword_uk_nhs_number</span><span class="sxs-lookup"><span data-stu-id="32d8c-3491">Keyword_uk_nhs_number</span></span>

- <span data-ttu-id="32d8c-3492">service national de santé</span><span class="sxs-lookup"><span data-stu-id="32d8c-3492">national health service</span></span> 
- <span data-ttu-id="32d8c-3493">NHS</span><span class="sxs-lookup"><span data-stu-id="32d8c-3493">nhs</span></span> 
- <span data-ttu-id="32d8c-3494">administration des services de santé</span><span class="sxs-lookup"><span data-stu-id="32d8c-3494">health services authority</span></span> 
- <span data-ttu-id="32d8c-3495">administration de la santé</span><span class="sxs-lookup"><span data-stu-id="32d8c-3495">health authority</span></span>

#### <a name="keyword_uk_nhs_number1"></a><span data-ttu-id="32d8c-3496">Keyword_uk_nhs_number1</span><span class="sxs-lookup"><span data-stu-id="32d8c-3496">Keyword_uk_nhs_number1</span></span>

- <span data-ttu-id="32d8c-3497">id du patient</span><span class="sxs-lookup"><span data-stu-id="32d8c-3497">patient id</span></span> 
- <span data-ttu-id="32d8c-3498">identification du patient</span><span class="sxs-lookup"><span data-stu-id="32d8c-3498">patient identification</span></span> 
- <span data-ttu-id="32d8c-3499">n° patient</span><span class="sxs-lookup"><span data-stu-id="32d8c-3499">patient no</span></span> 
- <span data-ttu-id="32d8c-3500">numéro de patient</span><span class="sxs-lookup"><span data-stu-id="32d8c-3500">patient number</span></span>

#### <a name="keyword_uk_nhs_number_dob"></a><span data-ttu-id="32d8c-3501">Keyword_uk_nhs_number_dob</span><span class="sxs-lookup"><span data-stu-id="32d8c-3501">Keyword_uk_nhs_number_dob</span></span>

- <span data-ttu-id="32d8c-3502">GP</span><span class="sxs-lookup"><span data-stu-id="32d8c-3502">GP</span></span> 
- <span data-ttu-id="32d8c-3503">DOB</span><span class="sxs-lookup"><span data-stu-id="32d8c-3503">DOB</span></span> 
- <span data-ttu-id="32d8c-3504">D. O. B</span><span class="sxs-lookup"><span data-stu-id="32d8c-3504">D.O.B</span></span> 
- <span data-ttu-id="32d8c-3505">Date of Birth</span><span class="sxs-lookup"><span data-stu-id="32d8c-3505">Date of Birth</span></span> 
- <span data-ttu-id="32d8c-3506">Birth Date</span><span class="sxs-lookup"><span data-stu-id="32d8c-3506">Birth Date</span></span> 
   
## <a name="uk-national-insurance-number-nino"></a><span data-ttu-id="32d8c-p145">Numéro d'assurance nationale (NINO) Royaume-Uni</span><span class="sxs-lookup"><span data-stu-id="32d8c-p145">U.K. National Insurance Number (NINO)</span></span>

### <a name="format"></a><span data-ttu-id="32d8c-3509">Format</span><span class="sxs-lookup"><span data-stu-id="32d8c-3509">Format</span></span>

<span data-ttu-id="32d8c-3510">7 caractères ou 9 caractères séparés par des espaces ou des tirets</span><span class="sxs-lookup"><span data-stu-id="32d8c-3510">7 characters or 9 characters separated by spaces or dashes</span></span>

### <a name="pattern"></a><span data-ttu-id="32d8c-3511">Modèle</span><span class="sxs-lookup"><span data-stu-id="32d8c-3511">Pattern</span></span>

<span data-ttu-id="32d8c-3512">Deux modèles possibles :</span><span class="sxs-lookup"><span data-stu-id="32d8c-3512">Two possible patterns:</span></span>

- <span data-ttu-id="32d8c-3513">Deux lettres (valides NINOs Utilisez uniquement certains caractères dans ce préfixe, que ce modèle valide ; ne respecte pas la casse)</span><span class="sxs-lookup"><span data-stu-id="32d8c-3513">Two letters (valid NINOs use only certain characters in this prefix, which this pattern validates; not case sensitive)</span></span>
- <span data-ttu-id="32d8c-3514">Six chiffres</span><span class="sxs-lookup"><span data-stu-id="32d8c-3514">Six digits</span></span>
- <span data-ttu-id="32d8c-3515">« A », « B », « C » ou « d » (comme le préfixe, seuls certains caractères sont autorisés dans le suffixe ; ne respectent pas la casse)</span><span class="sxs-lookup"><span data-stu-id="32d8c-3515">Either 'A', 'B', 'C', or 'D' (like the prefix, only certain characters are allowed in the suffix; not case sensitive)</span></span>

<span data-ttu-id="32d8c-3516">OR</span><span class="sxs-lookup"><span data-stu-id="32d8c-3516">OR</span></span>

- <span data-ttu-id="32d8c-3517">Deux lettres</span><span class="sxs-lookup"><span data-stu-id="32d8c-3517">Two letters</span></span>
- <span data-ttu-id="32d8c-3518">Un espace ou un tiret</span><span class="sxs-lookup"><span data-stu-id="32d8c-3518">A space or dash</span></span>
- <span data-ttu-id="32d8c-3519">Deux chiffres</span><span class="sxs-lookup"><span data-stu-id="32d8c-3519">Two digits</span></span>
- <span data-ttu-id="32d8c-3520">Un espace ou un tiret</span><span class="sxs-lookup"><span data-stu-id="32d8c-3520">A space or dash</span></span>
- <span data-ttu-id="32d8c-3521">Deux chiffres</span><span class="sxs-lookup"><span data-stu-id="32d8c-3521">Two digits</span></span>
- <span data-ttu-id="32d8c-3522">Un espace ou un tiret</span><span class="sxs-lookup"><span data-stu-id="32d8c-3522">A space or dash</span></span>
- <span data-ttu-id="32d8c-3523">Deux chiffres</span><span class="sxs-lookup"><span data-stu-id="32d8c-3523">Two digits</span></span>
- <span data-ttu-id="32d8c-3524">Un espace ou un tiret</span><span class="sxs-lookup"><span data-stu-id="32d8c-3524">A space or dash</span></span>
- <span data-ttu-id="32d8c-3525">« A », « B », « C » ou « d »</span><span class="sxs-lookup"><span data-stu-id="32d8c-3525">Either 'A', 'B', 'C', or 'D'</span></span>

### <a name="checksum"></a><span data-ttu-id="32d8c-3526">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="32d8c-3526">Checksum</span></span>

<span data-ttu-id="32d8c-3527">Non</span><span class="sxs-lookup"><span data-stu-id="32d8c-3527">No</span></span>

### <a name="definition"></a><span data-ttu-id="32d8c-3528">Définition</span><span class="sxs-lookup"><span data-stu-id="32d8c-3528">Definition</span></span>

<span data-ttu-id="32d8c-3529">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="32d8c-3529">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="32d8c-3530">La fonction Func_uk_nino trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="32d8c-3530">The function Func_uk_nino finds content that matches the pattern.</span></span>
- <span data-ttu-id="32d8c-3531">Un mot clé figurant dans la liste Keyword_uk_nino est trouvé.</span><span class="sxs-lookup"><span data-stu-id="32d8c-3531">A keyword from Keyword_uk_nino is found.</span></span>

<span data-ttu-id="32d8c-3532">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="32d8c-3532">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="32d8c-3533">La fonction Func_uk_nino trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="32d8c-3533">The function Func_uk_nino finds content that matches the pattern.</span></span>
- <span data-ttu-id="32d8c-3534">Aucun mot clé figurant dans la liste Keyword_uk_nino n’est trouvé.</span><span class="sxs-lookup"><span data-stu-id="32d8c-3534">No keyword from Keyword_uk_nino is found.</span></span>

```xml
<!-- U.K. NINO -->
<Entity id="16c07343-c26f-49d2-a987-3daf717e94cc" patternsProximity="300" recommendedConfidence="75">
    <Pattern confidenceLevel="85">
        <IdMatch idRef="Func_uk_nino" />
        <Any minMatches="1">
          <Match idRef="Keyword_uk_nino" />
        </Any>
    </Pattern>    
     <Pattern confidenceLevel="75">
        <IdMatch idRef="Func_uk_nino" />
        <Any minMatches="0" maxMatches="0">
          <Match idRef="Keyword_uk_nino" />
        </Any>
    </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="32d8c-3535">Mots clés</span><span class="sxs-lookup"><span data-stu-id="32d8c-3535">Keywords</span></span>

#### <a name="keyword_uk_nino"></a><span data-ttu-id="32d8c-3536">Keyword_uk_nino</span><span class="sxs-lookup"><span data-stu-id="32d8c-3536">Keyword_uk_nino</span></span>

- <span data-ttu-id="32d8c-3537">numéro d’assurance nationale</span><span class="sxs-lookup"><span data-stu-id="32d8c-3537">national insurance number</span></span> 
- <span data-ttu-id="32d8c-3538">cotisations sociales</span><span class="sxs-lookup"><span data-stu-id="32d8c-3538">national insurance contributions</span></span> 
- <span data-ttu-id="32d8c-3539">loi sur la protection</span><span class="sxs-lookup"><span data-stu-id="32d8c-3539">protection act</span></span> 
- <span data-ttu-id="32d8c-3540">cotisations</span><span class="sxs-lookup"><span data-stu-id="32d8c-3540">insurance</span></span> 
- <span data-ttu-id="32d8c-3541">numéro de sécurité sociale</span><span class="sxs-lookup"><span data-stu-id="32d8c-3541">social security number</span></span> 
- <span data-ttu-id="32d8c-3542">demande d’assurance</span><span class="sxs-lookup"><span data-stu-id="32d8c-3542">insurance application</span></span> 
- <span data-ttu-id="32d8c-3543">demande de soins médicaux</span><span class="sxs-lookup"><span data-stu-id="32d8c-3543">medical application</span></span> 
- <span data-ttu-id="32d8c-3544">assurance sociale</span><span class="sxs-lookup"><span data-stu-id="32d8c-3544">social insurance</span></span> 
- <span data-ttu-id="32d8c-3545">soins médicaux</span><span class="sxs-lookup"><span data-stu-id="32d8c-3545">medical attention</span></span> 
- <span data-ttu-id="32d8c-3546">sécurité sociale</span><span class="sxs-lookup"><span data-stu-id="32d8c-3546">social security</span></span> 
- <span data-ttu-id="32d8c-3547">grande-bretagne</span><span class="sxs-lookup"><span data-stu-id="32d8c-3547">great britain</span></span> 
- <span data-ttu-id="32d8c-3548">cotisations</span><span class="sxs-lookup"><span data-stu-id="32d8c-3548">insurance</span></span>    
   
## <a name="us--uk-passport-number"></a><span data-ttu-id="32d8c-p146">Numéro de passeport États-Unis/Royaume-Uni</span><span class="sxs-lookup"><span data-stu-id="32d8c-p146">U.S. / U.K. Passport Number</span></span>

### <a name="format"></a><span data-ttu-id="32d8c-3551">Format</span><span class="sxs-lookup"><span data-stu-id="32d8c-3551">Format</span></span>

<span data-ttu-id="32d8c-3552">Neuf chiffres</span><span class="sxs-lookup"><span data-stu-id="32d8c-3552">Nine digits</span></span>

### <a name="pattern"></a><span data-ttu-id="32d8c-3553">Modèle</span><span class="sxs-lookup"><span data-stu-id="32d8c-3553">Pattern</span></span>

<span data-ttu-id="32d8c-3554">Neuf chiffres consécutifs</span><span class="sxs-lookup"><span data-stu-id="32d8c-3554">Nine consecutive digits</span></span>

### <a name="checksum"></a><span data-ttu-id="32d8c-3555">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="32d8c-3555">Checksum</span></span>

<span data-ttu-id="32d8c-3556">Non</span><span class="sxs-lookup"><span data-stu-id="32d8c-3556">No</span></span>

### <a name="definition"></a><span data-ttu-id="32d8c-3557">Définition</span><span class="sxs-lookup"><span data-stu-id="32d8c-3557">Definition</span></span>

<span data-ttu-id="32d8c-3558">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="32d8c-3558">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="32d8c-3559">La fonction Func_usa_uk_passport trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="32d8c-3559">The function Func_usa_uk_passport finds content that matches the pattern.</span></span>
- <span data-ttu-id="32d8c-3560">Un mot clé figurant dans la liste Keyword_passport est trouvé.</span><span class="sxs-lookup"><span data-stu-id="32d8c-3560">A keyword from Keyword_passport is found.</span></span>

```xml
<Entity id="178ec42a-18b4-47cc-85c7-d62c92fd67f8" patternsProximity="300" recommendedConfidence="75">
    <Pattern confidenceLevel="75">
        <IdMatch idRef="Func_usa_uk_passport" />
        <Match idRef="Keyword_passport" />
    </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="32d8c-3561">Mots clés</span><span class="sxs-lookup"><span data-stu-id="32d8c-3561">Keywords</span></span>

#### <a name="keyword_passport"></a><span data-ttu-id="32d8c-3562">Keyword_passport</span><span class="sxs-lookup"><span data-stu-id="32d8c-3562">Keyword_passport</span></span>

- <span data-ttu-id="32d8c-3563">Numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="32d8c-3563">Passport Number</span></span> 
- <span data-ttu-id="32d8c-3564">N° de passeport</span><span class="sxs-lookup"><span data-stu-id="32d8c-3564">Passport No</span></span> 
- <span data-ttu-id="32d8c-3565"># Passeport</span><span class="sxs-lookup"><span data-stu-id="32d8c-3565">Passport #</span></span> 
- <span data-ttu-id="32d8c-3566">Tel #</span><span class="sxs-lookup"><span data-stu-id="32d8c-3566">Passport#</span></span> 
- <span data-ttu-id="32d8c-3567">PassportID</span><span class="sxs-lookup"><span data-stu-id="32d8c-3567">PassportID</span></span> 
- <span data-ttu-id="32d8c-3568">N ° passeport</span><span class="sxs-lookup"><span data-stu-id="32d8c-3568">Passportno</span></span> 
- <span data-ttu-id="32d8c-3569">passportnumber</span><span class="sxs-lookup"><span data-stu-id="32d8c-3569">passportnumber</span></span> 
- <span data-ttu-id="32d8c-3570">パスポート</span><span class="sxs-lookup"><span data-stu-id="32d8c-3570">パスポート</span></span> 
- <span data-ttu-id="32d8c-3571">パスポート番号</span><span class="sxs-lookup"><span data-stu-id="32d8c-3571">パスポート番号</span></span> 
- <span data-ttu-id="32d8c-3572">パスポートのNum</span><span class="sxs-lookup"><span data-stu-id="32d8c-3572">パスポートのNum</span></span> 
- <span data-ttu-id="32d8c-3573">パスポート＃</span><span class="sxs-lookup"><span data-stu-id="32d8c-3573">パスポート＃</span></span> 
- <span data-ttu-id="32d8c-3574">Numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="32d8c-3574">Numéro de passeport</span></span> 
- <span data-ttu-id="32d8c-3575">Passeport n°</span><span class="sxs-lookup"><span data-stu-id="32d8c-3575">Passeport n °</span></span> 
- <span data-ttu-id="32d8c-3576">Passeport numéro</span><span class="sxs-lookup"><span data-stu-id="32d8c-3576">Passeport Non</span></span> 
- <span data-ttu-id="32d8c-3577"># Passeport</span><span class="sxs-lookup"><span data-stu-id="32d8c-3577">Passeport #</span></span> 
- <span data-ttu-id="32d8c-3578">Passeport #</span><span class="sxs-lookup"><span data-stu-id="32d8c-3578">Passeport#</span></span> 
- <span data-ttu-id="32d8c-3579">PasseportNon</span><span class="sxs-lookup"><span data-stu-id="32d8c-3579">PasseportNon</span></span> 
- <span data-ttu-id="32d8c-3580">Passeportn °</span><span class="sxs-lookup"><span data-stu-id="32d8c-3580">Passeportn °</span></span> 
   
## <a name="us-bank-account-number"></a><span data-ttu-id="32d8c-3581">Numéro de compte bancaire États-Unis</span><span class="sxs-lookup"><span data-stu-id="32d8c-3581">U.S. Bank Account Number</span></span>

### <a name="format"></a><span data-ttu-id="32d8c-3582">Format</span><span class="sxs-lookup"><span data-stu-id="32d8c-3582">Format</span></span>

<span data-ttu-id="32d8c-3583">8-17 chiffres</span><span class="sxs-lookup"><span data-stu-id="32d8c-3583">8-17 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="32d8c-3584">Modèle</span><span class="sxs-lookup"><span data-stu-id="32d8c-3584">Pattern</span></span>

<span data-ttu-id="32d8c-3585">8 à 17 chiffres consécutifs</span><span class="sxs-lookup"><span data-stu-id="32d8c-3585">8-17 consecutive digits</span></span>

### <a name="checksum"></a><span data-ttu-id="32d8c-3586">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="32d8c-3586">Checksum</span></span>

<span data-ttu-id="32d8c-3587">Non</span><span class="sxs-lookup"><span data-stu-id="32d8c-3587">No</span></span>

### <a name="definition"></a><span data-ttu-id="32d8c-3588">Définition</span><span class="sxs-lookup"><span data-stu-id="32d8c-3588">Definition</span></span>

<span data-ttu-id="32d8c-3589">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="32d8c-3589">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="32d8c-3590">L’expression régulière Regex_usa_bank_account_number trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="32d8c-3590">The regular expression Regex_usa_bank_account_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="32d8c-3591">Un mot clé figurant dans la liste Keyword_usa_Bank_Account est trouvé.</span><span class="sxs-lookup"><span data-stu-id="32d8c-3591">A keyword from Keyword_usa_Bank_Account is found.</span></span>

```xml
<!-- U.S. Bank Account Number -->
<Entity id="a2ce32a8-f935-4bb6-8e96-2a5157672e2c" patternsProximity="300" recommendedConfidence="75">
    <Pattern confidenceLevel="75">
        <IdMatch idRef="Regex_usa_bank_account_number" />
        <Match idRef="Keyword_usa_Bank_Account" />
    </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="32d8c-3592">Mots clés</span><span class="sxs-lookup"><span data-stu-id="32d8c-3592">Keywords</span></span>

#### <a name="keyword_usa_bank_account"></a><span data-ttu-id="32d8c-3593">Keyword_usa_Bank_Account</span><span class="sxs-lookup"><span data-stu-id="32d8c-3593">Keyword_usa_Bank_Account</span></span>

- <span data-ttu-id="32d8c-3594">Numéro de compte courant</span><span class="sxs-lookup"><span data-stu-id="32d8c-3594">Checking Account Number</span></span> 
- <span data-ttu-id="32d8c-3595">Compte courant</span><span class="sxs-lookup"><span data-stu-id="32d8c-3595">Checking Account</span></span> 
- <span data-ttu-id="32d8c-3596"># compte courant</span><span class="sxs-lookup"><span data-stu-id="32d8c-3596">Checking Account #</span></span> 
- <span data-ttu-id="32d8c-3597">Numéro compte courant</span><span class="sxs-lookup"><span data-stu-id="32d8c-3597">Checking Acct Number</span></span> 
- <span data-ttu-id="32d8c-3598"># compte courant</span><span class="sxs-lookup"><span data-stu-id="32d8c-3598">Checking Acct #</span></span> 
- <span data-ttu-id="32d8c-3599">N° de compte courant</span><span class="sxs-lookup"><span data-stu-id="32d8c-3599">Checking Acct No.</span></span> 
- <span data-ttu-id="32d8c-3600">N° de compte courant</span><span class="sxs-lookup"><span data-stu-id="32d8c-3600">Checking Account No.</span></span> 
- <span data-ttu-id="32d8c-3601">Numéro de compte bancaire</span><span class="sxs-lookup"><span data-stu-id="32d8c-3601">Bank Account Number</span></span> 
- <span data-ttu-id="32d8c-3602"># Compte bancaire</span><span class="sxs-lookup"><span data-stu-id="32d8c-3602">Bank Account #</span></span> 
- <span data-ttu-id="32d8c-3603">Numéro de compte bancaire</span><span class="sxs-lookup"><span data-stu-id="32d8c-3603">Bank Acct Number</span></span> 
- <span data-ttu-id="32d8c-3604"># Compte bancaire</span><span class="sxs-lookup"><span data-stu-id="32d8c-3604">Bank Acct #</span></span> 
- <span data-ttu-id="32d8c-3605">N° de compte bancaire</span><span class="sxs-lookup"><span data-stu-id="32d8c-3605">Bank Acct No.</span></span> 
- <span data-ttu-id="32d8c-3606">N° de compte bancaire</span><span class="sxs-lookup"><span data-stu-id="32d8c-3606">Bank Account No.</span></span> 
- <span data-ttu-id="32d8c-3607">Numéro de compte d’épargne</span><span class="sxs-lookup"><span data-stu-id="32d8c-3607">Savings Account Number</span></span> 
- <span data-ttu-id="32d8c-3608">Compte d’épargne.</span><span class="sxs-lookup"><span data-stu-id="32d8c-3608">Savings Account.</span></span> 
- <span data-ttu-id="32d8c-3609">N° de compte d’épargne</span><span class="sxs-lookup"><span data-stu-id="32d8c-3609">Savings Account #</span></span> 
- <span data-ttu-id="32d8c-3610">Numéro de compte d’épargne</span><span class="sxs-lookup"><span data-stu-id="32d8c-3610">Savings Acct Number</span></span> 
- <span data-ttu-id="32d8c-3611"># compte d’épargne</span><span class="sxs-lookup"><span data-stu-id="32d8c-3611">Savings Acct #</span></span> 
- <span data-ttu-id="32d8c-3612">N° de compte d’épargne</span><span class="sxs-lookup"><span data-stu-id="32d8c-3612">Savings Acct No.</span></span> 
- <span data-ttu-id="32d8c-3613">N° de compte d’épargne</span><span class="sxs-lookup"><span data-stu-id="32d8c-3613">Savings Account No.</span></span> 
- <span data-ttu-id="32d8c-3614">Numéro de compte de débit</span><span class="sxs-lookup"><span data-stu-id="32d8c-3614">Debit Account Number</span></span> 
- <span data-ttu-id="32d8c-3615">Compte de débit</span><span class="sxs-lookup"><span data-stu-id="32d8c-3615">Debit Account</span></span> 
- <span data-ttu-id="32d8c-3616"># Compte de débit</span><span class="sxs-lookup"><span data-stu-id="32d8c-3616">Debit Account #</span></span> 
- <span data-ttu-id="32d8c-3617">Numéro de compte de débit</span><span class="sxs-lookup"><span data-stu-id="32d8c-3617">Debit Acct Number</span></span> 
- <span data-ttu-id="32d8c-3618"># Compte de débit</span><span class="sxs-lookup"><span data-stu-id="32d8c-3618">Debit Acct #</span></span> 
- <span data-ttu-id="32d8c-3619">N° de compte de débit</span><span class="sxs-lookup"><span data-stu-id="32d8c-3619">Debit Acct No.</span></span> 
- <span data-ttu-id="32d8c-3620">N° de compte de débit</span><span class="sxs-lookup"><span data-stu-id="32d8c-3620">Debit Account No.</span></span> 
   
## <a name="us-drivers-license-number"></a><span data-ttu-id="32d8c-3621">Numéro de permis de conduire États-Unis</span><span class="sxs-lookup"><span data-stu-id="32d8c-3621">U.S. Driver's License Number</span></span>

### <a name="format"></a><span data-ttu-id="32d8c-3622">Format</span><span class="sxs-lookup"><span data-stu-id="32d8c-3622">Format</span></span>

<span data-ttu-id="32d8c-3623">Dépend de l’État</span><span class="sxs-lookup"><span data-stu-id="32d8c-3623">Depends on the state</span></span>

### <a name="pattern"></a><span data-ttu-id="32d8c-3624">Modèle</span><span class="sxs-lookup"><span data-stu-id="32d8c-3624">Pattern</span></span>

<span data-ttu-id="32d8c-3625">Dépend de l’État, par exemple, New York :</span><span class="sxs-lookup"><span data-stu-id="32d8c-3625">Depends on the state -- for example, New York:</span></span>
- <span data-ttu-id="32d8c-3626">Neuf chiffres au format DDD DDD DDD correspondront.</span><span class="sxs-lookup"><span data-stu-id="32d8c-3626">Nine digits formatted like ddd ddd ddd will match.</span></span>
- <span data-ttu-id="32d8c-3627">Neuf chiffres au format ddddddddd ne correspondront pas.</span><span class="sxs-lookup"><span data-stu-id="32d8c-3627">Nine digits like ddddddddd will not match.</span></span>

### <a name="checksum"></a><span data-ttu-id="32d8c-3628">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="32d8c-3628">Checksum</span></span>

<span data-ttu-id="32d8c-3629">Non</span><span class="sxs-lookup"><span data-stu-id="32d8c-3629">No</span></span>

### <a name="definition"></a><span data-ttu-id="32d8c-3630">Définition</span><span class="sxs-lookup"><span data-stu-id="32d8c-3630">Definition</span></span>

<span data-ttu-id="32d8c-3631">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="32d8c-3631">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="32d8c-3632">La fonction Func_new_york_drivers_license_number trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="32d8c-3632">The function Func_new_york_drivers_license_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="32d8c-3633">Un mot clé figurant dans la liste Keyword_[state_name]_drivers_license_name est trouvé.</span><span class="sxs-lookup"><span data-stu-id="32d8c-3633">A keyword from Keyword_[state_name]_drivers_license_name is found.</span></span>
- <span data-ttu-id="32d8c-3634">Un mot clé figurant dans la liste Keyword_us_drivers_license est trouvé.</span><span class="sxs-lookup"><span data-stu-id="32d8c-3634">A keyword from Keyword_us_drivers_license is found.</span></span>

<span data-ttu-id="32d8c-3635">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 65 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="32d8c-3635">A DLP policy is 65% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="32d8c-3636">La fonction Func_new_york_drivers_license_number trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="32d8c-3636">The function Func_new_york_drivers_license_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="32d8c-3637">Un mot clé figurant dans la liste Keyword_[state_name]_drivers_license_name est trouvé.</span><span class="sxs-lookup"><span data-stu-id="32d8c-3637">A keyword from Keyword_[state_name]_drivers_license_name is found.</span></span>
- <span data-ttu-id="32d8c-3638">Un mot clé figurant dans la liste Keyword_us_drivers_license_abbreviations est trouvé.</span><span class="sxs-lookup"><span data-stu-id="32d8c-3638">A keyword from Keyword_us_drivers_license_abbreviations is found.</span></span>
- <span data-ttu-id="32d8c-3639">Aucun mot clé figurant dans la liste Keyword_us_drivers_license n’est trouvé.</span><span class="sxs-lookup"><span data-stu-id="32d8c-3639">No keyword from Keyword_us_drivers_license is found.</span></span>

```xml
<Entity id="dfeb356f-61cd-459e-bf0f-7c6d28b458c6 patternsProximity="300">
    <Pattern confidenceLevel="75">
        <IdMatch idRef="Func_new_york_drivers_license_number" />
        <Match idRef="Keyword_new_york_drivers_license_name" />
        <Match idRef="Keyword_us_drivers_license" />
    </Pattern>
    <Pattern confidenceLevel="65">
        <IdMatch idRef="Func_new_york_drivers_license_number" />
        <Match idRef="Keyword_new_york_drivers_license_name" />
        <Match idRef="Keyword_us_drivers_license_abbreviations" />
        <Any minMatches="0" maxMatches="0">
          <Match idRef="Keyword_us_drivers_license" />
        </Any>
    </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="32d8c-3640">Mots clés</span><span class="sxs-lookup"><span data-stu-id="32d8c-3640">Keywords</span></span>

#### <a name="keyword_us_drivers_license_abbreviations"></a><span data-ttu-id="32d8c-3641">Keyword_us_drivers_license_abbreviations</span><span class="sxs-lookup"><span data-stu-id="32d8c-3641">Keyword_us_drivers_license_abbreviations</span></span>

- <span data-ttu-id="32d8c-3642">LD</span><span class="sxs-lookup"><span data-stu-id="32d8c-3642">DL</span></span> 
- <span data-ttu-id="32d8c-3643">DISTRIBUTION</span><span class="sxs-lookup"><span data-stu-id="32d8c-3643">DLS</span></span> 
- <span data-ttu-id="32d8c-3644">CÈDE</span><span class="sxs-lookup"><span data-stu-id="32d8c-3644">CDL</span></span> 
- <span data-ttu-id="32d8c-3645">CDLS</span><span class="sxs-lookup"><span data-stu-id="32d8c-3645">CDLS</span></span> 
- <span data-ttu-id="32d8c-3646">ID</span><span class="sxs-lookup"><span data-stu-id="32d8c-3646">ID</span></span> 
- <span data-ttu-id="32d8c-3647">Codes</span><span class="sxs-lookup"><span data-stu-id="32d8c-3647">IDs</span></span> 
- <span data-ttu-id="32d8c-3648">LD #</span><span class="sxs-lookup"><span data-stu-id="32d8c-3648">DL#</span></span> 
- <span data-ttu-id="32d8c-3649">DISTRIBUTION #</span><span class="sxs-lookup"><span data-stu-id="32d8c-3649">DLS#</span></span> 
- <span data-ttu-id="32d8c-3650">CÈDE #</span><span class="sxs-lookup"><span data-stu-id="32d8c-3650">CDL#</span></span> 
- <span data-ttu-id="32d8c-3651">CDLS #</span><span class="sxs-lookup"><span data-stu-id="32d8c-3651">CDLS#</span></span> 
- <span data-ttu-id="32d8c-3652">Réf #</span><span class="sxs-lookup"><span data-stu-id="32d8c-3652">ID#</span></span>
- <span data-ttu-id="32d8c-3653">Codes #</span><span class="sxs-lookup"><span data-stu-id="32d8c-3653">IDs#</span></span> 
- <span data-ttu-id="32d8c-3654">Numéro d’identification</span><span class="sxs-lookup"><span data-stu-id="32d8c-3654">ID number</span></span> 
- <span data-ttu-id="32d8c-3655">Numéros d’identification</span><span class="sxs-lookup"><span data-stu-id="32d8c-3655">ID numbers</span></span> 
- <span data-ttu-id="32d8c-3656">Profil</span><span class="sxs-lookup"><span data-stu-id="32d8c-3656">LIC</span></span> 
- <span data-ttu-id="32d8c-3657">Profil #</span><span class="sxs-lookup"><span data-stu-id="32d8c-3657">LIC#</span></span> 

#### <a name="keyword_us_drivers_license"></a><span data-ttu-id="32d8c-3658">Keyword_us_drivers_license</span><span class="sxs-lookup"><span data-stu-id="32d8c-3658">Keyword_us_drivers_license</span></span>

- <span data-ttu-id="32d8c-3659">DriverLic</span><span class="sxs-lookup"><span data-stu-id="32d8c-3659">DriverLic</span></span> 
- <span data-ttu-id="32d8c-3660">DriverLics</span><span class="sxs-lookup"><span data-stu-id="32d8c-3660">DriverLics</span></span> 
- <span data-ttu-id="32d8c-3661">DriverLicense</span><span class="sxs-lookup"><span data-stu-id="32d8c-3661">DriverLicense</span></span> 
- <span data-ttu-id="32d8c-3662">DriverLicenses</span><span class="sxs-lookup"><span data-stu-id="32d8c-3662">DriverLicenses</span></span> 
- <span data-ttu-id="32d8c-3663">Permis conduire</span><span class="sxs-lookup"><span data-stu-id="32d8c-3663">Driver Lic</span></span> 
- <span data-ttu-id="32d8c-3664">Permis conduire</span><span class="sxs-lookup"><span data-stu-id="32d8c-3664">Driver Lics</span></span> 
- <span data-ttu-id="32d8c-3665">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="32d8c-3665">Driver License</span></span> 
- <span data-ttu-id="32d8c-3666">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="32d8c-3666">Driver Licenses</span></span> 
- <span data-ttu-id="32d8c-3667">DriversLic</span><span class="sxs-lookup"><span data-stu-id="32d8c-3667">DriversLic</span></span> 
- <span data-ttu-id="32d8c-3668">DriversLics</span><span class="sxs-lookup"><span data-stu-id="32d8c-3668">DriversLics</span></span> 
- <span data-ttu-id="32d8c-3669">DriversLicense</span><span class="sxs-lookup"><span data-stu-id="32d8c-3669">DriversLicense</span></span> 
- <span data-ttu-id="32d8c-3670">DriversLicenses</span><span class="sxs-lookup"><span data-stu-id="32d8c-3670">DriversLicenses</span></span> 
- <span data-ttu-id="32d8c-3671">Permis conduire</span><span class="sxs-lookup"><span data-stu-id="32d8c-3671">Drivers Lic</span></span> 
- <span data-ttu-id="32d8c-3672">Permis conduire</span><span class="sxs-lookup"><span data-stu-id="32d8c-3672">Drivers Lics</span></span> 
- <span data-ttu-id="32d8c-3673">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="32d8c-3673">Drivers License</span></span> 
- <span data-ttu-id="32d8c-3674">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="32d8c-3674">Drivers Licenses</span></span> 
- <span data-ttu-id="32d8c-3675">Driver'Lic</span><span class="sxs-lookup"><span data-stu-id="32d8c-3675">Driver'Lic</span></span> 
- <span data-ttu-id="32d8c-3676">Driver'Lics</span><span class="sxs-lookup"><span data-stu-id="32d8c-3676">Driver'Lics</span></span> 
- <span data-ttu-id="32d8c-3677">Driver'License</span><span class="sxs-lookup"><span data-stu-id="32d8c-3677">Driver'License</span></span> 
- <span data-ttu-id="32d8c-3678">Driver'Licenses</span><span class="sxs-lookup"><span data-stu-id="32d8c-3678">Driver'Licenses</span></span> 
- <span data-ttu-id="32d8c-3679">Permis conduire</span><span class="sxs-lookup"><span data-stu-id="32d8c-3679">Driver' Lic</span></span> 
- <span data-ttu-id="32d8c-3680">Permis conduire</span><span class="sxs-lookup"><span data-stu-id="32d8c-3680">Driver' Lics</span></span> 
- <span data-ttu-id="32d8c-3681">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="32d8c-3681">Driver' License</span></span> 
- <span data-ttu-id="32d8c-3682">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="32d8c-3682">Driver' Licenses</span></span>
- <span data-ttu-id="32d8c-3683">Driver'sLic</span><span class="sxs-lookup"><span data-stu-id="32d8c-3683">Driver'sLic</span></span> 
- <span data-ttu-id="32d8c-3684">Driver'sLics</span><span class="sxs-lookup"><span data-stu-id="32d8c-3684">Driver'sLics</span></span> 
- <span data-ttu-id="32d8c-3685">Driver'sLicense</span><span class="sxs-lookup"><span data-stu-id="32d8c-3685">Driver'sLicense</span></span> 
- <span data-ttu-id="32d8c-3686">Driver'sLicenses</span><span class="sxs-lookup"><span data-stu-id="32d8c-3686">Driver'sLicenses</span></span> 
- <span data-ttu-id="32d8c-3687">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="32d8c-3687">Driver's Lic</span></span> 
- <span data-ttu-id="32d8c-3688">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="32d8c-3688">Driver's Lics</span></span> 
- <span data-ttu-id="32d8c-3689">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="32d8c-3689">Driver's License</span></span> 
- <span data-ttu-id="32d8c-3690">Driver’s Licenses</span><span class="sxs-lookup"><span data-stu-id="32d8c-3690">Driver's Licenses</span></span> 
- <span data-ttu-id="32d8c-3691">numéro d’identification</span><span class="sxs-lookup"><span data-stu-id="32d8c-3691">identification number</span></span> 
- <span data-ttu-id="32d8c-3692">numéros d’identification</span><span class="sxs-lookup"><span data-stu-id="32d8c-3692">identification numbers</span></span> 
- <span data-ttu-id="32d8c-3693"># identification</span><span class="sxs-lookup"><span data-stu-id="32d8c-3693">identification #</span></span> 
- <span data-ttu-id="32d8c-3694">carte d’identité</span><span class="sxs-lookup"><span data-stu-id="32d8c-3694">id card</span></span> 
- <span data-ttu-id="32d8c-3695">cartes d’identité</span><span class="sxs-lookup"><span data-stu-id="32d8c-3695">id cards</span></span> 
- <span data-ttu-id="32d8c-3696">carte d’identification</span><span class="sxs-lookup"><span data-stu-id="32d8c-3696">identification card</span></span> 
- <span data-ttu-id="32d8c-3697">cartes d’identification</span><span class="sxs-lookup"><span data-stu-id="32d8c-3697">identification cards</span></span> 
- <span data-ttu-id="32d8c-3698">DriverLic #</span><span class="sxs-lookup"><span data-stu-id="32d8c-3698">DriverLic#</span></span> 
- <span data-ttu-id="32d8c-3699">DriverLics #</span><span class="sxs-lookup"><span data-stu-id="32d8c-3699">DriverLics#</span></span> 
- <span data-ttu-id="32d8c-3700">DriverLicense #</span><span class="sxs-lookup"><span data-stu-id="32d8c-3700">DriverLicense#</span></span> 
- <span data-ttu-id="32d8c-3701">DriverLicenses #</span><span class="sxs-lookup"><span data-stu-id="32d8c-3701">DriverLicenses#</span></span> 
- <span data-ttu-id="32d8c-3702">#Permis conduire</span><span class="sxs-lookup"><span data-stu-id="32d8c-3702">Driver Lic#</span></span> 
- <span data-ttu-id="32d8c-3703">#Permis conduire</span><span class="sxs-lookup"><span data-stu-id="32d8c-3703">Driver Lics#</span></span> 
- <span data-ttu-id="32d8c-3704">#Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="32d8c-3704">Driver License#</span></span> 
- <span data-ttu-id="32d8c-3705">#Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="32d8c-3705">Driver Licenses#</span></span> 
- <span data-ttu-id="32d8c-3706">DriversLic #</span><span class="sxs-lookup"><span data-stu-id="32d8c-3706">DriversLic#</span></span> 
- <span data-ttu-id="32d8c-3707">DriversLics #</span><span class="sxs-lookup"><span data-stu-id="32d8c-3707">DriversLics#</span></span> 
- <span data-ttu-id="32d8c-3708">DriversLicense #</span><span class="sxs-lookup"><span data-stu-id="32d8c-3708">DriversLicense#</span></span> 
- <span data-ttu-id="32d8c-3709">DriversLicenses #</span><span class="sxs-lookup"><span data-stu-id="32d8c-3709">DriversLicenses#</span></span> 
- <span data-ttu-id="32d8c-3710">#Permis conduire</span><span class="sxs-lookup"><span data-stu-id="32d8c-3710">Drivers Lic#</span></span> 
- <span data-ttu-id="32d8c-3711">#Permis conduire</span><span class="sxs-lookup"><span data-stu-id="32d8c-3711">Drivers Lics#</span></span> 
- <span data-ttu-id="32d8c-3712">#Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="32d8c-3712">Drivers License#</span></span> 
- <span data-ttu-id="32d8c-3713">#Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="32d8c-3713">Drivers Licenses#</span></span> 
- <span data-ttu-id="32d8c-3714">Driver'Lic #</span><span class="sxs-lookup"><span data-stu-id="32d8c-3714">Driver'Lic#</span></span> 
- <span data-ttu-id="32d8c-3715">Driver'Lics #</span><span class="sxs-lookup"><span data-stu-id="32d8c-3715">Driver'Lics#</span></span> 
- <span data-ttu-id="32d8c-3716">Driver'License #</span><span class="sxs-lookup"><span data-stu-id="32d8c-3716">Driver'License#</span></span> 
- <span data-ttu-id="32d8c-3717">Driver'Licenses #</span><span class="sxs-lookup"><span data-stu-id="32d8c-3717">Driver'Licenses#</span></span> 
- <span data-ttu-id="32d8c-3718">#Permis conduire</span><span class="sxs-lookup"><span data-stu-id="32d8c-3718">Driver' Lic#</span></span> 
- <span data-ttu-id="32d8c-3719">#Permis conduire</span><span class="sxs-lookup"><span data-stu-id="32d8c-3719">Driver' Lics#</span></span> 
- <span data-ttu-id="32d8c-3720">#Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="32d8c-3720">Driver' License#</span></span> 
- <span data-ttu-id="32d8c-3721">#Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="32d8c-3721">Driver' Licenses#</span></span> 
- <span data-ttu-id="32d8c-3722">Driver'sLic #</span><span class="sxs-lookup"><span data-stu-id="32d8c-3722">Driver'sLic#</span></span> 
- <span data-ttu-id="32d8c-3723">Driver'sLics #</span><span class="sxs-lookup"><span data-stu-id="32d8c-3723">Driver'sLics#</span></span> 
- <span data-ttu-id="32d8c-3724">Driver'sLicense #</span><span class="sxs-lookup"><span data-stu-id="32d8c-3724">Driver'sLicense#</span></span> 
- <span data-ttu-id="32d8c-3725">Driver'sLicenses #</span><span class="sxs-lookup"><span data-stu-id="32d8c-3725">Driver'sLicenses#</span></span> 
- <span data-ttu-id="32d8c-3726">#Permisconduire</span><span class="sxs-lookup"><span data-stu-id="32d8c-3726">Driver's Lic#</span></span> 
- <span data-ttu-id="32d8c-3727">#Permisconduire</span><span class="sxs-lookup"><span data-stu-id="32d8c-3727">Driver's Lics#</span></span> 
- <span data-ttu-id="32d8c-3728">#Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="32d8c-3728">Driver's License#</span></span> 
- <span data-ttu-id="32d8c-3729">#Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="32d8c-3729">Driver's Licenses#</span></span> 
- <span data-ttu-id="32d8c-3730"># carte d’identité</span><span class="sxs-lookup"><span data-stu-id="32d8c-3730">id card#</span></span> 
- <span data-ttu-id="32d8c-3731"># cartes d’identité</span><span class="sxs-lookup"><span data-stu-id="32d8c-3731">id cards#</span></span> 
- <span data-ttu-id="32d8c-3732">#carte d’identification</span><span class="sxs-lookup"><span data-stu-id="32d8c-3732">identification card#</span></span> 
- <span data-ttu-id="32d8c-3733">#cartes d’identification</span><span class="sxs-lookup"><span data-stu-id="32d8c-3733">identification cards#</span></span> 


#### <a name="keyword_state_name_drivers_license_name"></a><span data-ttu-id="32d8c-3734">Keyword_ [state_name] _drivers_license_name</span><span class="sxs-lookup"><span data-stu-id="32d8c-3734">Keyword_[state_name]_drivers_license_name</span></span>

- <span data-ttu-id="32d8c-3735">Abréviation de l’État (par exemple, « NY »)</span><span class="sxs-lookup"><span data-stu-id="32d8c-3735">State abbreviation (for example, "NY")</span></span> 
- <span data-ttu-id="32d8c-3736">Nom de l’État (par exemple, « New York »)</span><span class="sxs-lookup"><span data-stu-id="32d8c-3736">State name (for example, "New York")</span></span>    
   
## <a name="us-individual-taxpayer-identification-number-itin"></a><span data-ttu-id="32d8c-3737">Numéro d’identification fiscale individuel (ITIN) États-Unis</span><span class="sxs-lookup"><span data-stu-id="32d8c-3737">U.S. Individual Taxpayer Identification Number (ITIN)</span></span>

### <a name="format"></a><span data-ttu-id="32d8c-3738">Format</span><span class="sxs-lookup"><span data-stu-id="32d8c-3738">Format</span></span>

<span data-ttu-id="32d8c-3739">Neuf chiffres, le premier étant le « 9 », le quatrième le « 7 » ou le « 8 », éventuellement mis en forme avec des espaces ou des tirets</span><span class="sxs-lookup"><span data-stu-id="32d8c-3739">Nine digits that start with a "9" and contain a "7" or "8" as the fourth digit, optionally formatted with spaces or dashes</span></span>

### <a name="pattern"></a><span data-ttu-id="32d8c-3740">Modèle</span><span class="sxs-lookup"><span data-stu-id="32d8c-3740">Pattern</span></span>

<span data-ttu-id="32d8c-3741">Avec</span><span class="sxs-lookup"><span data-stu-id="32d8c-3741">Formatted:</span></span>
- <span data-ttu-id="32d8c-3742">Le chiffre « 9 »</span><span class="sxs-lookup"><span data-stu-id="32d8c-3742">The digit "9"</span></span> 
- <span data-ttu-id="32d8c-3743">Deux chiffres</span><span class="sxs-lookup"><span data-stu-id="32d8c-3743">Two digits</span></span> 
- <span data-ttu-id="32d8c-3744">Un espace ou un tiret</span><span class="sxs-lookup"><span data-stu-id="32d8c-3744">A space or dash</span></span> 
- <span data-ttu-id="32d8c-3745">Un « 7 » ou un « 8 »</span><span class="sxs-lookup"><span data-stu-id="32d8c-3745">A "7" or "8"</span></span> 
- <span data-ttu-id="32d8c-3746">Un chiffre</span><span class="sxs-lookup"><span data-stu-id="32d8c-3746">A digit</span></span> 
- <span data-ttu-id="32d8c-3747">Un espace ou tiret</span><span class="sxs-lookup"><span data-stu-id="32d8c-3747">A space, or dash</span></span> 
- <span data-ttu-id="32d8c-3748">Quatre chiffres</span><span class="sxs-lookup"><span data-stu-id="32d8c-3748">Four digits</span></span>

<span data-ttu-id="32d8c-3749">Non</span><span class="sxs-lookup"><span data-stu-id="32d8c-3749">Unformatted:</span></span>
- <span data-ttu-id="32d8c-3750">Le chiffre « 9 »</span><span class="sxs-lookup"><span data-stu-id="32d8c-3750">The digit "9"</span></span> 
- <span data-ttu-id="32d8c-3751">Deux chiffres</span><span class="sxs-lookup"><span data-stu-id="32d8c-3751">Two digits</span></span> 
- <span data-ttu-id="32d8c-3752">Un « 7 » ou un « 8 »</span><span class="sxs-lookup"><span data-stu-id="32d8c-3752">A "7" or "8"</span></span> 
- <span data-ttu-id="32d8c-3753">Cinq chiffres</span><span class="sxs-lookup"><span data-stu-id="32d8c-3753">Five digits</span></span>

### <a name="checksum"></a><span data-ttu-id="32d8c-3754">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="32d8c-3754">Checksum</span></span>

<span data-ttu-id="32d8c-3755">Non</span><span class="sxs-lookup"><span data-stu-id="32d8c-3755">No</span></span>

### <a name="definition"></a><span data-ttu-id="32d8c-3756">Définition</span><span class="sxs-lookup"><span data-stu-id="32d8c-3756">Definition</span></span>

<span data-ttu-id="32d8c-3757">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="32d8c-3757">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="32d8c-3758">La fonction Func_formatted_itin trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="32d8c-3758">The function Func_formatted_itin finds content that matches the pattern.</span></span>
- <span data-ttu-id="32d8c-3759">Au moins une des affirmations suivantes est vraie :</span><span class="sxs-lookup"><span data-stu-id="32d8c-3759">At least one of the following is true:</span></span>
    - <span data-ttu-id="32d8c-3760">Un mot clé figurant dans la liste Keyword_itin est trouvé.</span><span class="sxs-lookup"><span data-stu-id="32d8c-3760">A keyword from Keyword_itin is found.</span></span>
    - <span data-ttu-id="32d8c-3761">La fonction Func_us_address trouve une adresse au format correct.</span><span class="sxs-lookup"><span data-stu-id="32d8c-3761">The function Func_us_address finds an address in the right date format.</span></span>
    - <span data-ttu-id="32d8c-3762">La fonction Func_us_date trouve une date au format correct.</span><span class="sxs-lookup"><span data-stu-id="32d8c-3762">The function Func_us_date finds a date in the right date format.</span></span>
    - <span data-ttu-id="32d8c-3763">Un mot clé figurant dans la liste Keyword_itin_collaborative est trouvé.</span><span class="sxs-lookup"><span data-stu-id="32d8c-3763">A keyword from Keyword_itin_collaborative is found.</span></span>

<span data-ttu-id="32d8c-3764">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="32d8c-3764">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="32d8c-3765">La fonction Func_unformatted_itin trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="32d8c-3765">The function Func_unformatted_itin finds content that matches the pattern.</span></span>
- <span data-ttu-id="32d8c-3766">Au moins une des affirmations suivantes est vraie :</span><span class="sxs-lookup"><span data-stu-id="32d8c-3766">At least one of the following is true:</span></span>
    - <span data-ttu-id="32d8c-3767">Un mot clé figurant dans la liste Keyword_itin_collaborative est trouvé.</span><span class="sxs-lookup"><span data-stu-id="32d8c-3767">A keyword from Keyword_itin_collaborative is found.</span></span>
    - <span data-ttu-id="32d8c-3768">La fonction Func_us_address trouve une adresse au format correct.</span><span class="sxs-lookup"><span data-stu-id="32d8c-3768">The function Func_us_address finds an address in the right date format.</span></span>
    - <span data-ttu-id="32d8c-3769">La fonction Func_us_date trouve une date au format correct.</span><span class="sxs-lookup"><span data-stu-id="32d8c-3769">The function Func_us_date finds a date in the right date format.</span></span>

```xml
<!-- U.S. Individual Taxpayer Identification Number (ITIN) -->
<Entity id="e55e2a32-f92d-4985-a35d-a0b269eb687b" patternsProximity="300" recommendedConfidence="75">
    <Pattern confidenceLevel="85">
        <IdMatch idRef="Func_formatted_itin" />
        <Any minMatches="1">
          <Match idRef="Keyword_itin" />
          <Match idRef="Func_us_address" />
          <Match idRef="Func_us_date" />
          <Match idRef="Keyword_itin_collaborative" />
        </Any>
    </Pattern>
    <Pattern confidenceLevel="75">
        <IdMatch idRef="Func_unformatted_itin" />
        <Match idRef="Keyword_itin" />
        <Any minMatches="1">
          <Match idRef="Keyword_itin_collaborative" />
          <Match idRef="Func_us_address" />
          <Match idRef="Func_us_date" />
        </Any>
    </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="32d8c-3770">Mots clés</span><span class="sxs-lookup"><span data-stu-id="32d8c-3770">Keywords</span></span>

#### <a name="keyword_itin"></a><span data-ttu-id="32d8c-3771">Keyword_itin</span><span class="sxs-lookup"><span data-stu-id="32d8c-3771">Keyword_itin</span></span>

- <span data-ttu-id="32d8c-3772">redevable</span><span class="sxs-lookup"><span data-stu-id="32d8c-3772">taxpayer</span></span> 
- <span data-ttu-id="32d8c-3773">id fiscal</span><span class="sxs-lookup"><span data-stu-id="32d8c-3773">tax id</span></span> 
- <span data-ttu-id="32d8c-3774">identification fiscale</span><span class="sxs-lookup"><span data-stu-id="32d8c-3774">tax identification</span></span> 
- <span data-ttu-id="32d8c-3775">itin</span><span class="sxs-lookup"><span data-stu-id="32d8c-3775">itin</span></span> 
- <span data-ttu-id="32d8c-3776">SSN</span><span class="sxs-lookup"><span data-stu-id="32d8c-3776">ssn</span></span> 
- <span data-ttu-id="32d8c-3777">Etain</span><span class="sxs-lookup"><span data-stu-id="32d8c-3777">tin</span></span> 
- <span data-ttu-id="32d8c-3778">sécurité sociale</span><span class="sxs-lookup"><span data-stu-id="32d8c-3778">social security</span></span> 
- <span data-ttu-id="32d8c-3779">contribuable</span><span class="sxs-lookup"><span data-stu-id="32d8c-3779">tax payer</span></span> 
- <span data-ttu-id="32d8c-3780">itins</span><span class="sxs-lookup"><span data-stu-id="32d8c-3780">itins</span></span> 
- <span data-ttu-id="32d8c-3781">taxi</span><span class="sxs-lookup"><span data-stu-id="32d8c-3781">taxid</span></span> 
- <span data-ttu-id="32d8c-3782">contribuable individuel</span><span class="sxs-lookup"><span data-stu-id="32d8c-3782">individual taxpayer</span></span> 

#### <a name="keyword_itin_collaborative"></a><span data-ttu-id="32d8c-3783">Keyword_itin_collaborative</span><span class="sxs-lookup"><span data-stu-id="32d8c-3783">Keyword_itin_collaborative</span></span>

- <span data-ttu-id="32d8c-3784">Licence</span><span class="sxs-lookup"><span data-stu-id="32d8c-3784">License</span></span> 
- <span data-ttu-id="32d8c-3785">LD</span><span class="sxs-lookup"><span data-stu-id="32d8c-3785">DL</span></span> 
- <span data-ttu-id="32d8c-3786">DOB</span><span class="sxs-lookup"><span data-stu-id="32d8c-3786">DOB</span></span> 
- <span data-ttu-id="32d8c-3787">Birthdate</span><span class="sxs-lookup"><span data-stu-id="32d8c-3787">Birthdate</span></span> 
- <span data-ttu-id="32d8c-3788">Birthday</span><span class="sxs-lookup"><span data-stu-id="32d8c-3788">Birthday</span></span> 
- <span data-ttu-id="32d8c-3789">Date of Birth</span><span class="sxs-lookup"><span data-stu-id="32d8c-3789">Date of Birth</span></span> 
   
## <a name="us-social-security-number-ssn"></a><span data-ttu-id="32d8c-3790">Numéro de sécurité sociale (SSN) États-Unis</span><span class="sxs-lookup"><span data-stu-id="32d8c-3790">U.S. Social Security Number (SSN)</span></span>

### <a name="format"></a><span data-ttu-id="32d8c-3791">Format</span><span class="sxs-lookup"><span data-stu-id="32d8c-3791">Format</span></span>

<span data-ttu-id="32d8c-3792">9 chiffres, qui peuvent être mis en forme ou non mis en forme</span><span class="sxs-lookup"><span data-stu-id="32d8c-3792">9 digits, which may be in a formatted or unformatted pattern</span></span>

> [!NOTE]
> <span data-ttu-id="32d8c-3793">La mise en forme d’un numéro de sécurité sociale émis avant le milieu de l’année 2011 est fixe et certaines parties du numéro doivent se situer dans certaines plages pour qu’il soit valide (mais il n’y a pas de somme de contrôle).</span><span class="sxs-lookup"><span data-stu-id="32d8c-3793">If issued before mid-2011, an SSN has strong formatting where certain parts of the number must fall within certain ranges to be valid (but there's no checksum).</span></span>

### <a name="pattern"></a><span data-ttu-id="32d8c-3794">Modèle</span><span class="sxs-lookup"><span data-stu-id="32d8c-3794">Pattern</span></span>

<span data-ttu-id="32d8c-3795">Quatre fonctions permettent de rechercher des numéros de sécurité sociale avec quatre différents modèles :</span><span class="sxs-lookup"><span data-stu-id="32d8c-3795">Four functions look for SSNs in four different patterns:</span></span>
- <span data-ttu-id="32d8c-3796">Func_ssn recherche des numéros de sécurité sociale avec une mise en forme fixe d’avant l’année 2011, mis en forme avec des tirets ou des espaces (ddd-dd-dddd OU ddd dd dddd)</span><span class="sxs-lookup"><span data-stu-id="32d8c-3796">Func_ssn finds SSNs with pre-2011 strong formatting that are formatted with dashes or spaces (ddd-dd-dddd OR ddd dd dddd)</span></span>
- <span data-ttu-id="32d8c-3797">Func_unformatted_ssn recherche des numéros de sécurité sociale avec une mise en forme fixe d’avant l’année 2011, avec neuf chiffres consécutifs non mis en forme (ddddddddd)</span><span class="sxs-lookup"><span data-stu-id="32d8c-3797">Func_unformatted_ssn finds SSNs with pre-2011 strong formatting that are unformatted as nine consecutive digits (ddddddddd)</span></span>
- <span data-ttu-id="32d8c-3798">Func_randomized_formatted_ssn recherche des numéros de sécurité sociale d’après l’année 2011, mis en forme avec des tirets ou des espaces  (ddd-dd-dddd OU ddd dd dddd)</span><span class="sxs-lookup"><span data-stu-id="32d8c-3798">Func_randomized_formatted_ssn finds post-2011 SSNs that are formatted with dashes or spaces (ddd-dd-dddd OR ddd dd dddd)</span></span>
- <span data-ttu-id="32d8c-3799">Func_randomized_unformatted_ssn recherche des numéros de sécurité sociale d’après l’année 2011, avec neuf chiffres consécutifs non mis en forme (ddddddddd)</span><span class="sxs-lookup"><span data-stu-id="32d8c-3799">Func_randomized_unformatted_ssn finds post-2011 SSNs that are unformatted as nine consecutive digits (ddddddddd)</span></span>

### <a name="checksum"></a><span data-ttu-id="32d8c-3800">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="32d8c-3800">Checksum</span></span>

<span data-ttu-id="32d8c-3801">Non</span><span class="sxs-lookup"><span data-stu-id="32d8c-3801">No</span></span>


### <a name="definition"></a><span data-ttu-id="32d8c-3802">Définition</span><span class="sxs-lookup"><span data-stu-id="32d8c-3802">Definition</span></span>

<span data-ttu-id="32d8c-3803">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="32d8c-3803">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="32d8c-3804">La fonction Func_ssn trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="32d8c-3804">The function Func_ssn finds content that matches the pattern.</span></span>
- <span data-ttu-id="32d8c-3805">Un mot clé figurant dans la liste Keyword_ssn est trouvé.</span><span class="sxs-lookup"><span data-stu-id="32d8c-3805">A keyword from Keyword_ssn is found.</span></span>

<span data-ttu-id="32d8c-3806">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="32d8c-3806">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="32d8c-3807">La fonction Func_unformatted_ssn trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="32d8c-3807">The function Func_unformatted_ssn finds content that matches the pattern.</span></span>
- <span data-ttu-id="32d8c-3808">Un mot clé figurant dans la liste Keyword_ssn est trouvé.</span><span class="sxs-lookup"><span data-stu-id="32d8c-3808">A keyword from Keyword_ssn is found.</span></span>

<span data-ttu-id="32d8c-3809">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 65 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="32d8c-3809">A DLP policy is 65% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="32d8c-3810">La fonction Func_randomized_formatted_ssn trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="32d8c-3810">The function Func_randomized_formatted_ssn finds content that matches the pattern.</span></span>
- <span data-ttu-id="32d8c-3811">Un mot clé figurant dans la liste Keyword_ssn est trouvé.</span><span class="sxs-lookup"><span data-stu-id="32d8c-3811">A keyword from Keyword_ssn is found.</span></span>

<span data-ttu-id="32d8c-3812">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 55 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="32d8c-3812">A DLP policy is 55% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="32d8c-3813">La fonction Func_randomized_unformatted_ssn trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="32d8c-3813">The function Func_randomized_unformatted_ssn finds content that matches the pattern.</span></span>
- <span data-ttu-id="32d8c-3814">Un mot clé figurant dans la liste Keyword_ssn est trouvé.</span><span class="sxs-lookup"><span data-stu-id="32d8c-3814">A keyword from Keyword_ssn is found.</span></span>


```xml
<!-- U.S. Social Security Number (SSN) -->
  <Entity id="a44669fe-0d48-453d-a9b1-2cc83f2cba77" patternsProximity="300" recommendedConfidence="75">
      <Pattern confidenceLevel="85">
        <IdMatch idRef="Func_ssn" />
        <Match idRef="Keyword_ssn" />
      </Pattern>
      <Pattern confidenceLevel="75">
        <IdMatch idRef="Func_unformatted_ssn" />
        <Match idRef="Keyword_ssn" />
      </Pattern>
      <Pattern confidenceLevel="65">
        <IdMatch idRef="Func_randomized_formatted_ssn" />
        <Match idRef="Keyword_ssn" />
      </Pattern>
      <Pattern confidenceLevel="55">
        <IdMatch idRef="Func_randomized_unformatted_ssn" />
        <Match idRef="Keyword_ssn" />
      </Pattern>
  </Entity>
```

### <a name="keywords"></a><span data-ttu-id="32d8c-3815">Mots clés</span><span class="sxs-lookup"><span data-stu-id="32d8c-3815">Keywords</span></span>

#### <a name="keyword_ssn"></a><span data-ttu-id="32d8c-3816">Keyword_ssn</span><span class="sxs-lookup"><span data-stu-id="32d8c-3816">Keyword_ssn</span></span>

- <span data-ttu-id="32d8c-3817">Sécurité sociale</span><span class="sxs-lookup"><span data-stu-id="32d8c-3817">Social Security</span></span> 
- <span data-ttu-id="32d8c-3818"># sécurité sociale</span><span class="sxs-lookup"><span data-stu-id="32d8c-3818">Social Security#</span></span> 
- <span data-ttu-id="32d8c-3819">Sécu sociale</span><span class="sxs-lookup"><span data-stu-id="32d8c-3819">Soc Sec</span></span> 
- <span data-ttu-id="32d8c-3820">SSN</span><span class="sxs-lookup"><span data-stu-id="32d8c-3820">SSN</span></span> 
- <span data-ttu-id="32d8c-3821">NUMÉROS</span><span class="sxs-lookup"><span data-stu-id="32d8c-3821">SSNS</span></span> 
- <span data-ttu-id="32d8c-3822">SSN #</span><span class="sxs-lookup"><span data-stu-id="32d8c-3822">SSN#</span></span> 
- <span data-ttu-id="32d8c-3823">SOCIALE #</span><span class="sxs-lookup"><span data-stu-id="32d8c-3823">SS#</span></span> 
- <span data-ttu-id="32d8c-3824">Identifiant SSID</span><span class="sxs-lookup"><span data-stu-id="32d8c-3824">SSID</span></span> 
   
