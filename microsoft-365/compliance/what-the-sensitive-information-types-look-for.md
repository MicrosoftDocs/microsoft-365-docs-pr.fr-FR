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
ms.openlocfilehash: 517ff6ae711d61b783e837aebeeb991dfaa53daa
ms.sourcegitcommit: 3dd9944a6070a7f35c4bc2b57df397f844c3fe79
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/15/2020
ms.locfileid: "42084333"
---
# <a name="what-the-sensitive-information-types-look-for"></a><span data-ttu-id="319ad-104">Éléments recherchés par les types d’informations sensibles</span><span class="sxs-lookup"><span data-stu-id="319ad-104">What the sensitive information types look for</span></span>

<span data-ttu-id="319ad-105">La protection contre la perte de données (DLP) dans &amp; le centre de sécurité conformité Office 365 inclut de nombreux types d’informations sensibles que vous pouvez utiliser dans vos stratégies DLP.</span><span class="sxs-lookup"><span data-stu-id="319ad-105">Data loss prevention (DLP) in the Office 365 Security &amp; Compliance Center includes many sensitive information types that are ready for you to use in your DLP policies.</span></span> <span data-ttu-id="319ad-106">Cette rubrique répertorie tous ces types d'informations sensibles et indique ce qu'une stratégie DLP recherche pour chaque type.</span><span class="sxs-lookup"><span data-stu-id="319ad-106">This topic lists all of these sensitive information types and shows what a DLP policy looks for when it detects each type.</span></span> <span data-ttu-id="319ad-107">Un type d'informations sensibles est défini par un modèle qui peut être identifié par une fonction ou une expression régulière.</span><span class="sxs-lookup"><span data-stu-id="319ad-107">A sensitive information type is defined by a pattern that can be identified by a regular expression or a function.</span></span> <span data-ttu-id="319ad-108">En outre, des preuves corroborantes comme les mots clés et les sommes de contrôle peuvent être utilisées pour identifier un type d'informations sensibles.</span><span class="sxs-lookup"><span data-stu-id="319ad-108">In addition, corroborative evidence such as keywords and checksums can be used to identify a sensitive information type.</span></span> <span data-ttu-id="319ad-109">Le niveau de confiance et la proximité sont également utilisés dans le processus d’évaluation.</span><span class="sxs-lookup"><span data-stu-id="319ad-109">Confidence level and proximity are also used in the evaluation process.</span></span>
  
## <a name="aba-routing-number"></a><span data-ttu-id="319ad-110">Numéro de routage ABA</span><span class="sxs-lookup"><span data-stu-id="319ad-110">ABA Routing Number</span></span>

### <a name="format"></a><span data-ttu-id="319ad-111">Format</span><span class="sxs-lookup"><span data-stu-id="319ad-111">Format</span></span>

<span data-ttu-id="319ad-112">9 chiffres mis en forme ou non mis en forme</span><span class="sxs-lookup"><span data-stu-id="319ad-112">9 digits which may be in a formatted or unformatted pattern</span></span>

### <a name="pattern"></a><span data-ttu-id="319ad-113">Modèle</span><span class="sxs-lookup"><span data-stu-id="319ad-113">Pattern</span></span>

<span data-ttu-id="319ad-114">Avec</span><span class="sxs-lookup"><span data-stu-id="319ad-114">Formatted:</span></span>
- <span data-ttu-id="319ad-115">Quatre chiffres commençant par 0, 1, 2, 3, 6, 7 ou 8</span><span class="sxs-lookup"><span data-stu-id="319ad-115">Four digits beginning with 0, 1, 2, 3, 6, 7, or 8</span></span>
- <span data-ttu-id="319ad-116">Un trait d’union </span><span class="sxs-lookup"><span data-stu-id="319ad-116">A hyphen</span></span>
- <span data-ttu-id="319ad-117">Quatre chiffres</span><span class="sxs-lookup"><span data-stu-id="319ad-117">Four digits</span></span>
- <span data-ttu-id="319ad-118">Un trait d’union </span><span class="sxs-lookup"><span data-stu-id="319ad-118">A hyphen</span></span>
- <span data-ttu-id="319ad-119">Un chiffre</span><span class="sxs-lookup"><span data-stu-id="319ad-119">A digit</span></span>

<span data-ttu-id="319ad-120">Non mis en forme : 9 chiffres consécutifs commençant par 0, 1, 2, 3, 6, 7 ou 8</span><span class="sxs-lookup"><span data-stu-id="319ad-120">Unformatted: 9 consecutive digits beginning with 0, 1, 2, 3, 6, 7, or 8</span></span> 

### <a name="checksum"></a><span data-ttu-id="319ad-121">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="319ad-121">Checksum</span></span>

<span data-ttu-id="319ad-122">Non</span><span class="sxs-lookup"><span data-stu-id="319ad-122">No</span></span>

### <a name="definition"></a><span data-ttu-id="319ad-123">Définition</span><span class="sxs-lookup"><span data-stu-id="319ad-123">Definition</span></span>

<span data-ttu-id="319ad-124">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="319ad-124">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="319ad-125">La fonction Func_aba_routing trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="319ad-125">The function Func_aba_routing finds content that matches the pattern.</span></span>
- <span data-ttu-id="319ad-126">Un mot clé figurant dans la liste Keyword_ABA_Routing est trouvé.</span><span class="sxs-lookup"><span data-stu-id="319ad-126">A keyword from Keyword_ABA_Routing is found.</span></span>

```xml
<!-- ABA Routing Number -->
<Entity id="cb353f78-2b72-4c3c-8827-92ebe4f69fdf" patternsProximity="300" recommendedConfidence="75">
      <Pattern confidenceLevel="75">
        <IdMatch idRef="Func_aba_routing" />
        <Match idRef="Keyword_ABA_Routing" />
      </Pattern>
 </Entity>
```


### <a name="keywords"></a><span data-ttu-id="319ad-127">Mots-clés</span><span class="sxs-lookup"><span data-stu-id="319ad-127">Keywords</span></span>

#### <a name="keyword_aba_routing"></a><span data-ttu-id="319ad-128">Keyword_ABA_Routing</span><span class="sxs-lookup"><span data-stu-id="319ad-128">Keyword_ABA_Routing</span></span>

- <span data-ttu-id="319ad-129">ABA</span><span class="sxs-lookup"><span data-stu-id="319ad-129">aba</span></span>
- <span data-ttu-id="319ad-130"># aba</span><span class="sxs-lookup"><span data-stu-id="319ad-130">aba #</span></span>
- <span data-ttu-id="319ad-131"># routage aba</span><span class="sxs-lookup"><span data-stu-id="319ad-131">aba routing #</span></span>
- <span data-ttu-id="319ad-132">numéro de routage aba</span><span class="sxs-lookup"><span data-stu-id="319ad-132">aba routing number</span></span>
- <span data-ttu-id="319ad-133">ABA #</span><span class="sxs-lookup"><span data-stu-id="319ad-133">aba#</span></span>
- <span data-ttu-id="319ad-134">abarouting #</span><span class="sxs-lookup"><span data-stu-id="319ad-134">abarouting#</span></span>
- <span data-ttu-id="319ad-135">numéro aba</span><span class="sxs-lookup"><span data-stu-id="319ad-135">aba number</span></span>
- <span data-ttu-id="319ad-136">abaroutingnumber</span><span class="sxs-lookup"><span data-stu-id="319ad-136">abaroutingnumber</span></span>
- <span data-ttu-id="319ad-137"># routage american bank association</span><span class="sxs-lookup"><span data-stu-id="319ad-137">american bank association routing #</span></span>
- <span data-ttu-id="319ad-138">numéro de routage american bank association</span><span class="sxs-lookup"><span data-stu-id="319ad-138">american bank association routing number</span></span>
- <span data-ttu-id="319ad-139">americanbankassociationrouting #</span><span class="sxs-lookup"><span data-stu-id="319ad-139">americanbankassociationrouting#</span></span>
- <span data-ttu-id="319ad-140">americanbankassociationroutingnumber</span><span class="sxs-lookup"><span data-stu-id="319ad-140">americanbankassociationroutingnumber</span></span>
- <span data-ttu-id="319ad-141">numéro de routage bancaire</span><span class="sxs-lookup"><span data-stu-id="319ad-141">bank routing number</span></span>
- <span data-ttu-id="319ad-142">bankrouting #</span><span class="sxs-lookup"><span data-stu-id="319ad-142">bankrouting#</span></span>
- <span data-ttu-id="319ad-143">bankroutingnumber</span><span class="sxs-lookup"><span data-stu-id="319ad-143">bankroutingnumber</span></span>
- <span data-ttu-id="319ad-144">numéro de routage</span><span class="sxs-lookup"><span data-stu-id="319ad-144">routing transit number</span></span>
- <span data-ttu-id="319ad-145">RTN</span><span class="sxs-lookup"><span data-stu-id="319ad-145">RTN</span></span> 
   
## <a name="argentina-national-identity-dni-number"></a><span data-ttu-id="319ad-146">Numéro d’identité nationale (DNI) pour l’Argentine</span><span class="sxs-lookup"><span data-stu-id="319ad-146">Argentina National Identity (DNI) Number</span></span>

### <a name="format"></a><span data-ttu-id="319ad-147">Format</span><span class="sxs-lookup"><span data-stu-id="319ad-147">Format</span></span>

<span data-ttu-id="319ad-148">Huit chiffres séparés par des points</span><span class="sxs-lookup"><span data-stu-id="319ad-148">Eight digits separated by periods</span></span>

### <a name="pattern"></a><span data-ttu-id="319ad-149">Modèle</span><span class="sxs-lookup"><span data-stu-id="319ad-149">Pattern</span></span>

<span data-ttu-id="319ad-150">Huit chiffres :</span><span class="sxs-lookup"><span data-stu-id="319ad-150">Eight digits:</span></span>
- <span data-ttu-id="319ad-151">Deux chiffres</span><span class="sxs-lookup"><span data-stu-id="319ad-151">Two digits</span></span>
- <span data-ttu-id="319ad-152">Un point </span><span class="sxs-lookup"><span data-stu-id="319ad-152">A period</span></span>
- <span data-ttu-id="319ad-153">Trois chiffres </span><span class="sxs-lookup"><span data-stu-id="319ad-153">Three digits</span></span>
- <span data-ttu-id="319ad-154">Un point </span><span class="sxs-lookup"><span data-stu-id="319ad-154">A period</span></span>
- <span data-ttu-id="319ad-155">Trois chiffres </span><span class="sxs-lookup"><span data-stu-id="319ad-155">Three digits</span></span>

### <a name="checksum"></a><span data-ttu-id="319ad-156">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="319ad-156">Checksum</span></span>

<span data-ttu-id="319ad-157">Non</span><span class="sxs-lookup"><span data-stu-id="319ad-157">No</span></span>

### <a name="definition"></a><span data-ttu-id="319ad-158">Définition</span><span class="sxs-lookup"><span data-stu-id="319ad-158">Definition</span></span>

<span data-ttu-id="319ad-159">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="319ad-159">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="319ad-160">L’expression régulière Regex_argentina_national_id trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="319ad-160">The regular expression Regex_argentina_national_id finds content that matches the pattern.</span></span>
- <span data-ttu-id="319ad-161">Un mot clé figurant dans la liste Keyword_argentina_national_id est trouvé.</span><span class="sxs-lookup"><span data-stu-id="319ad-161">A keyword from Keyword_argentina_national_id is found.</span></span>

```xml
<!-- Argentina National Identity (DNI) Number -->
<Entity id="eefbb00e-8282-433c-8620-8f1da3bffdb2" recommendedConfidence="75" patternsProximity="300">
   <Pattern confidenceLevel="75">
      <IdMatch idRef="Regex_argentina_national_id"/>
      <Match idRef="Keyword_argentina_national_id"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="319ad-162">Mots-clés</span><span class="sxs-lookup"><span data-stu-id="319ad-162">Keywords</span></span>

#### <a name="keyword_argentina_national_id"></a><span data-ttu-id="319ad-163">Keyword_argentina_national_id</span><span class="sxs-lookup"><span data-stu-id="319ad-163">Keyword_argentina_national_id</span></span>

- <span data-ttu-id="319ad-164">Argentina National Identity number</span><span class="sxs-lookup"><span data-stu-id="319ad-164">Argentina National Identity number</span></span> 
- <span data-ttu-id="319ad-165">Identité</span><span class="sxs-lookup"><span data-stu-id="319ad-165">Identity</span></span> 
- <span data-ttu-id="319ad-166">Identification de la carte d’identité nationale</span><span class="sxs-lookup"><span data-stu-id="319ad-166">Identification National Identity Card</span></span> 
- <span data-ttu-id="319ad-167">DNI</span><span class="sxs-lookup"><span data-stu-id="319ad-167">DNI</span></span> 
- <span data-ttu-id="319ad-168">Carte d’interface réseau nationale du registre des personnes</span><span class="sxs-lookup"><span data-stu-id="319ad-168">NIC National Registry of Persons</span></span> 
- <span data-ttu-id="319ad-169">Documento Nacional de Identidad</span><span class="sxs-lookup"><span data-stu-id="319ad-169">Documento Nacional de Identidad</span></span> 
- <span data-ttu-id="319ad-170">Registro Nacional de las Personas</span><span class="sxs-lookup"><span data-stu-id="319ad-170">Registro Nacional de las Personas</span></span> 
- <span data-ttu-id="319ad-171">Identidad</span><span class="sxs-lookup"><span data-stu-id="319ad-171">Identidad</span></span> 
- <span data-ttu-id="319ad-172">Identificación</span><span class="sxs-lookup"><span data-stu-id="319ad-172">Identificación</span></span> 
   
## <a name="australia-bank-account-number"></a><span data-ttu-id="319ad-173">Numéro de compte bancaire Australie</span><span class="sxs-lookup"><span data-stu-id="319ad-173">Australia Bank Account Number</span></span>

### <a name="format"></a><span data-ttu-id="319ad-174">Format</span><span class="sxs-lookup"><span data-stu-id="319ad-174">Format</span></span>

<span data-ttu-id="319ad-175">6 à 10 chiffres avec ou sans le numéro d’agence bancaire de l’État</span><span class="sxs-lookup"><span data-stu-id="319ad-175">6-10 digits with or without a bank state branch number</span></span>

### <a name="pattern"></a><span data-ttu-id="319ad-176">Modèle</span><span class="sxs-lookup"><span data-stu-id="319ad-176">Pattern</span></span>

<span data-ttu-id="319ad-177">Le numéro de compte est composé de 6 à 10 chiffres.</span><span class="sxs-lookup"><span data-stu-id="319ad-177">Account number is 6-10 digits.</span></span>
<span data-ttu-id="319ad-178">Numéro de succursale bancaire en Australie :</span><span class="sxs-lookup"><span data-stu-id="319ad-178">Australia bank state branch number:</span></span>
- <span data-ttu-id="319ad-179">Trois chiffres</span><span class="sxs-lookup"><span data-stu-id="319ad-179">Three digits</span></span> 
- <span data-ttu-id="319ad-180">Un trait d’union</span><span class="sxs-lookup"><span data-stu-id="319ad-180">A hyphen</span></span> 
- <span data-ttu-id="319ad-181">Trois chiffres</span><span class="sxs-lookup"><span data-stu-id="319ad-181">Three digits</span></span>

### <a name="checksum"></a><span data-ttu-id="319ad-182">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="319ad-182">Checksum</span></span>

<span data-ttu-id="319ad-183">Non</span><span class="sxs-lookup"><span data-stu-id="319ad-183">No</span></span>

### <a name="definition"></a><span data-ttu-id="319ad-184">Définition</span><span class="sxs-lookup"><span data-stu-id="319ad-184">Definition</span></span>

<span data-ttu-id="319ad-185">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="319ad-185">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="319ad-186">L’expression régulière Regex_australia_bank_account_number trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="319ad-186">The regular expression Regex_australia_bank_account_number finds content that matches the pattern..</span></span>
- <span data-ttu-id="319ad-187">Un mot clé figurant dans la liste Keyword_australia_bank_account_number est trouvé.</span><span class="sxs-lookup"><span data-stu-id="319ad-187">A keyword from Keyword_australia_bank_account_number is found.</span></span>
- <span data-ttu-id="319ad-188">L’expression régulière Regex_australia_bank_account_number_bsb trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="319ad-188">The regular expression Regex_australia_bank_account_number_bsb finds content that matches the pattern.</span></span>

<span data-ttu-id="319ad-189">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="319ad-189">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="319ad-190">L’expression régulière Regex_australia_bank_account_number trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="319ad-190">The regular expression Regex_australia_bank_account_number finds content that matches the pattern..</span></span>
- <span data-ttu-id="319ad-191">Un mot clé figurant dans la liste Keyword_australia_bank_account_number est trouvé.</span><span class="sxs-lookup"><span data-stu-id="319ad-191">A keyword from Keyword_australia_bank_account_number is found.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="319ad-192">Mots-clés</span><span class="sxs-lookup"><span data-stu-id="319ad-192">Keywords</span></span>

#### <a name="keyword_australia_bank_account_number"></a><span data-ttu-id="319ad-193">Keyword_australia_bank_account_number</span><span class="sxs-lookup"><span data-stu-id="319ad-193">Keyword_australia_bank_account_number</span></span>

- <span data-ttu-id="319ad-194">code swift banque</span><span class="sxs-lookup"><span data-stu-id="319ad-194">swift bank code</span></span>
- <span data-ttu-id="319ad-195">banque correspondante</span><span class="sxs-lookup"><span data-stu-id="319ad-195">correspondent bank</span></span>
- <span data-ttu-id="319ad-196">devise de base</span><span class="sxs-lookup"><span data-stu-id="319ad-196">base currency</span></span>
- <span data-ttu-id="319ad-197">compte aux États-Unis</span><span class="sxs-lookup"><span data-stu-id="319ad-197">usa account</span></span>
- <span data-ttu-id="319ad-198">adresse du titulaire</span><span class="sxs-lookup"><span data-stu-id="319ad-198">holder address</span></span>
- <span data-ttu-id="319ad-199">adresse de la banque</span><span class="sxs-lookup"><span data-stu-id="319ad-199">bank address</span></span>
- <span data-ttu-id="319ad-200">informations du compte</span><span class="sxs-lookup"><span data-stu-id="319ad-200">information account</span></span>
- <span data-ttu-id="319ad-201">transferts de fonds</span><span class="sxs-lookup"><span data-stu-id="319ad-201">fund transfers</span></span>
- <span data-ttu-id="319ad-202">frais bancaires</span><span class="sxs-lookup"><span data-stu-id="319ad-202">bank charges</span></span>
- <span data-ttu-id="319ad-203">informations sur la banque</span><span class="sxs-lookup"><span data-stu-id="319ad-203">bank details</span></span>
- <span data-ttu-id="319ad-204">informations bancaires</span><span class="sxs-lookup"><span data-stu-id="319ad-204">banking information</span></span>
- <span data-ttu-id="319ad-205">noms complets</span><span class="sxs-lookup"><span data-stu-id="319ad-205">full names</span></span>
- <span data-ttu-id="319ad-206">auront</span><span class="sxs-lookup"><span data-stu-id="319ad-206">iaea</span></span>

   
## <a name="australia-drivers-license-number"></a><span data-ttu-id="319ad-207">Numéro de permis de conduire Australie</span><span class="sxs-lookup"><span data-stu-id="319ad-207">Australia Driver's License Number</span></span>

### <a name="format"></a><span data-ttu-id="319ad-208">Format</span><span class="sxs-lookup"><span data-stu-id="319ad-208">Format</span></span>

<span data-ttu-id="319ad-209">Neuf lettres et chiffres</span><span class="sxs-lookup"><span data-stu-id="319ad-209">Nine letters and digits</span></span>

### <a name="pattern"></a><span data-ttu-id="319ad-210">Modèle</span><span class="sxs-lookup"><span data-stu-id="319ad-210">Pattern</span></span>

<span data-ttu-id="319ad-211">Neuf lettres et chiffres :</span><span class="sxs-lookup"><span data-stu-id="319ad-211">Nine letters and digits:</span></span> 

- <span data-ttu-id="319ad-212">Deux chiffres ou lettres (ne respectent pas la casse)</span><span class="sxs-lookup"><span data-stu-id="319ad-212">Two digits or letters (not case sensitive)</span></span> 
- <span data-ttu-id="319ad-213">Deux chiffres</span><span class="sxs-lookup"><span data-stu-id="319ad-213">Two digits</span></span> 
- <span data-ttu-id="319ad-214">Cinq chiffres ou lettres (ne respectent pas la casse)</span><span class="sxs-lookup"><span data-stu-id="319ad-214">Five digits or letters (not case sensitive)</span></span>

<span data-ttu-id="319ad-215">OU</span><span class="sxs-lookup"><span data-stu-id="319ad-215">OR</span></span>

- <span data-ttu-id="319ad-216">1 ou 2 lettres facultatives (ne respectant pas la casse) </span><span class="sxs-lookup"><span data-stu-id="319ad-216">1-2 optional letters (not case sensitive)</span></span> 
- <span data-ttu-id="319ad-217">4 à 9 chiffres</span><span class="sxs-lookup"><span data-stu-id="319ad-217">4-9 digits</span></span>

<span data-ttu-id="319ad-218">OU</span><span class="sxs-lookup"><span data-stu-id="319ad-218">OR</span></span>

- <span data-ttu-id="319ad-219">Neuf chiffres ou lettres (ne respectant pas la casse)</span><span class="sxs-lookup"><span data-stu-id="319ad-219">Nine digits or letters (not case sensitive)</span></span>

### <a name="checksum"></a><span data-ttu-id="319ad-220">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="319ad-220">Checksum</span></span>

<span data-ttu-id="319ad-221">Non</span><span class="sxs-lookup"><span data-stu-id="319ad-221">No</span></span>

### <a name="definition"></a><span data-ttu-id="319ad-222">Définition</span><span class="sxs-lookup"><span data-stu-id="319ad-222">Definition</span></span>

<span data-ttu-id="319ad-223">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="319ad-223">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="319ad-224">L’expression régulière Regex_australia_drivers_license_number trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="319ad-224">The regular expression Regex_australia_drivers_license_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="319ad-225">Un mot clé figurant dans la liste Keyword_australia_drivers_license_number est trouvé.</span><span class="sxs-lookup"><span data-stu-id="319ad-225">A keyword from Keyword_australia_drivers_license_number is found.</span></span>
- <span data-ttu-id="319ad-226">Aucun mot clé figurant dans la liste Keyword_australia_drivers_license_number_exclusions n’est trouvé.</span><span class="sxs-lookup"><span data-stu-id="319ad-226">No keyword from Keyword_australia_drivers_license_number_exclusions is found.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="319ad-227">Mots-clés</span><span class="sxs-lookup"><span data-stu-id="319ad-227">Keywords</span></span>

#### <a name="keyword_australia_drivers_license_number"></a><span data-ttu-id="319ad-228">Keyword_australia_drivers_license_number</span><span class="sxs-lookup"><span data-stu-id="319ad-228">Keyword_australia_drivers_license_number</span></span>

- <span data-ttu-id="319ad-229">permis de conduite internationaux</span><span class="sxs-lookup"><span data-stu-id="319ad-229">international driving permits</span></span>
- <span data-ttu-id="319ad-230">australian automobile association</span><span class="sxs-lookup"><span data-stu-id="319ad-230">australian automobile association</span></span>
- <span data-ttu-id="319ad-231">permis de conduite international</span><span class="sxs-lookup"><span data-stu-id="319ad-231">international driving permit</span></span>
- <span data-ttu-id="319ad-232">DriverLicence</span><span class="sxs-lookup"><span data-stu-id="319ad-232">DriverLicence</span></span>
- <span data-ttu-id="319ad-233">DriverLicences</span><span class="sxs-lookup"><span data-stu-id="319ad-233">DriverLicences</span></span>
- <span data-ttu-id="319ad-234">Permis conduire</span><span class="sxs-lookup"><span data-stu-id="319ad-234">Driver Lic</span></span>
- <span data-ttu-id="319ad-235">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="319ad-235">Driver Licence</span></span>
- <span data-ttu-id="319ad-236">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="319ad-236">Driver Licences</span></span>
- <span data-ttu-id="319ad-237">DriversLic</span><span class="sxs-lookup"><span data-stu-id="319ad-237">DriversLic</span></span>
- <span data-ttu-id="319ad-238">DriversLicence</span><span class="sxs-lookup"><span data-stu-id="319ad-238">DriversLicence</span></span>
- <span data-ttu-id="319ad-239">DriversLicences</span><span class="sxs-lookup"><span data-stu-id="319ad-239">DriversLicences</span></span>
- <span data-ttu-id="319ad-240">Permis conduire</span><span class="sxs-lookup"><span data-stu-id="319ad-240">Drivers Lic</span></span>
- <span data-ttu-id="319ad-241">Permis conduire</span><span class="sxs-lookup"><span data-stu-id="319ad-241">Drivers Lics</span></span>
- <span data-ttu-id="319ad-242">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="319ad-242">Drivers Licence</span></span>
- <span data-ttu-id="319ad-243">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="319ad-243">Drivers Licences</span></span>
- <span data-ttu-id="319ad-244">Driver'Lic</span><span class="sxs-lookup"><span data-stu-id="319ad-244">Driver'Lic</span></span>
- <span data-ttu-id="319ad-245">Driver'Lics</span><span class="sxs-lookup"><span data-stu-id="319ad-245">Driver'Lics</span></span>
- <span data-ttu-id="319ad-246">Driver'Licence</span><span class="sxs-lookup"><span data-stu-id="319ad-246">Driver'Licence</span></span>
- <span data-ttu-id="319ad-247">Driver'Licences</span><span class="sxs-lookup"><span data-stu-id="319ad-247">Driver'Licences</span></span>
- <span data-ttu-id="319ad-248">Permis conduire</span><span class="sxs-lookup"><span data-stu-id="319ad-248">Driver' Lic</span></span>
- <span data-ttu-id="319ad-249">Permis conduire</span><span class="sxs-lookup"><span data-stu-id="319ad-249">Driver' Lics</span></span>
- <span data-ttu-id="319ad-250">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="319ad-250">Driver' Licence</span></span>
- <span data-ttu-id="319ad-251">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="319ad-251">Driver' Licences</span></span>
- <span data-ttu-id="319ad-252">Driver'sLic</span><span class="sxs-lookup"><span data-stu-id="319ad-252">Driver'sLic</span></span>
- <span data-ttu-id="319ad-253">Driver'sLics</span><span class="sxs-lookup"><span data-stu-id="319ad-253">Driver'sLics</span></span>
- <span data-ttu-id="319ad-254">Driver'sLicence</span><span class="sxs-lookup"><span data-stu-id="319ad-254">Driver'sLicence</span></span>
- <span data-ttu-id="319ad-255">Driver'sLicences</span><span class="sxs-lookup"><span data-stu-id="319ad-255">Driver'sLicences</span></span>
- <span data-ttu-id="319ad-256">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="319ad-256">Driver's Lic</span></span>
- <span data-ttu-id="319ad-257">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="319ad-257">Driver's Lics</span></span>
- <span data-ttu-id="319ad-258">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="319ad-258">Driver's Licence</span></span>
- <span data-ttu-id="319ad-259">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="319ad-259">Driver's Licences</span></span>
- <span data-ttu-id="319ad-260">DriverLic #</span><span class="sxs-lookup"><span data-stu-id="319ad-260">DriverLic#</span></span>
- <span data-ttu-id="319ad-261">DriverLics #</span><span class="sxs-lookup"><span data-stu-id="319ad-261">DriverLics#</span></span>
- <span data-ttu-id="319ad-262">DriverLicence #</span><span class="sxs-lookup"><span data-stu-id="319ad-262">DriverLicence#</span></span>
- <span data-ttu-id="319ad-263">DriverLicences #</span><span class="sxs-lookup"><span data-stu-id="319ad-263">DriverLicences#</span></span>
- <span data-ttu-id="319ad-264">#Permis conduire</span><span class="sxs-lookup"><span data-stu-id="319ad-264">Driver Lic#</span></span>
- <span data-ttu-id="319ad-265">#Permis conduire</span><span class="sxs-lookup"><span data-stu-id="319ad-265">Driver Lics#</span></span>
- <span data-ttu-id="319ad-266">#Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="319ad-266">Driver Licence#</span></span>
- <span data-ttu-id="319ad-267">#Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="319ad-267">Driver Licences#</span></span>
- <span data-ttu-id="319ad-268">DriversLic #</span><span class="sxs-lookup"><span data-stu-id="319ad-268">DriversLic#</span></span>
- <span data-ttu-id="319ad-269">DriversLics #</span><span class="sxs-lookup"><span data-stu-id="319ad-269">DriversLics#</span></span>
- <span data-ttu-id="319ad-270">DriversLicence #</span><span class="sxs-lookup"><span data-stu-id="319ad-270">DriversLicence#</span></span>
- <span data-ttu-id="319ad-271">DriversLicences #</span><span class="sxs-lookup"><span data-stu-id="319ad-271">DriversLicences#</span></span>
- <span data-ttu-id="319ad-272">#Permis conduire</span><span class="sxs-lookup"><span data-stu-id="319ad-272">Drivers Lic#</span></span>
- <span data-ttu-id="319ad-273">#Permis conduire</span><span class="sxs-lookup"><span data-stu-id="319ad-273">Drivers Lics#</span></span>
- <span data-ttu-id="319ad-274">#Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="319ad-274">Drivers Licence#</span></span>
- <span data-ttu-id="319ad-275">#Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="319ad-275">Drivers Licences#</span></span>
- <span data-ttu-id="319ad-276">Driver'Lic #</span><span class="sxs-lookup"><span data-stu-id="319ad-276">Driver'Lic#</span></span>
- <span data-ttu-id="319ad-277">Driver'Lics #</span><span class="sxs-lookup"><span data-stu-id="319ad-277">Driver'Lics#</span></span>
- <span data-ttu-id="319ad-278">Driver'Licence #</span><span class="sxs-lookup"><span data-stu-id="319ad-278">Driver'Licence#</span></span>
- <span data-ttu-id="319ad-279">Driver'Licences #</span><span class="sxs-lookup"><span data-stu-id="319ad-279">Driver'Licences#</span></span>
- <span data-ttu-id="319ad-280">#Permis conduire</span><span class="sxs-lookup"><span data-stu-id="319ad-280">Driver' Lic#</span></span>
- <span data-ttu-id="319ad-281">#Permis conduire</span><span class="sxs-lookup"><span data-stu-id="319ad-281">Driver' Lics#</span></span>
- <span data-ttu-id="319ad-282">#Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="319ad-282">Driver' Licence#</span></span>
- <span data-ttu-id="319ad-283">#Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="319ad-283">Driver' Licences#</span></span>
- <span data-ttu-id="319ad-284">Driver'sLic #</span><span class="sxs-lookup"><span data-stu-id="319ad-284">Driver'sLic#</span></span>
- <span data-ttu-id="319ad-285">Driver'sLics #</span><span class="sxs-lookup"><span data-stu-id="319ad-285">Driver'sLics#</span></span>
- <span data-ttu-id="319ad-286">Driver'sLicence #</span><span class="sxs-lookup"><span data-stu-id="319ad-286">Driver'sLicence#</span></span>
- <span data-ttu-id="319ad-287">Driver'sLicences #</span><span class="sxs-lookup"><span data-stu-id="319ad-287">Driver'sLicences#</span></span>
- <span data-ttu-id="319ad-288">#Permisconduire</span><span class="sxs-lookup"><span data-stu-id="319ad-288">Driver's Lic#</span></span>
- <span data-ttu-id="319ad-289">#Permisconduire</span><span class="sxs-lookup"><span data-stu-id="319ad-289">Driver's Lics#</span></span>
- <span data-ttu-id="319ad-290">#Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="319ad-290">Driver's Licence#</span></span>
- <span data-ttu-id="319ad-291">#Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="319ad-291">Driver's Licences#</span></span> 

#### <a name="keyword_australia_drivers_license_number_exclusions"></a><span data-ttu-id="319ad-292">Keyword_australia_drivers_license_number_exclusions</span><span class="sxs-lookup"><span data-stu-id="319ad-292">Keyword_australia_drivers_license_number_exclusions</span></span>

- <span data-ttu-id="319ad-293">AAA</span><span class="sxs-lookup"><span data-stu-id="319ad-293">aaa</span></span>
- <span data-ttu-id="319ad-294">DriverLicense</span><span class="sxs-lookup"><span data-stu-id="319ad-294">DriverLicense</span></span>
- <span data-ttu-id="319ad-295">DriverLicenses</span><span class="sxs-lookup"><span data-stu-id="319ad-295">DriverLicenses</span></span>
- <span data-ttu-id="319ad-296">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="319ad-296">Driver License</span></span>
- <span data-ttu-id="319ad-297">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="319ad-297">Driver Licenses</span></span>
- <span data-ttu-id="319ad-298">DriversLicense</span><span class="sxs-lookup"><span data-stu-id="319ad-298">DriversLicense</span></span>
- <span data-ttu-id="319ad-299">DriversLicenses</span><span class="sxs-lookup"><span data-stu-id="319ad-299">DriversLicenses</span></span>
- <span data-ttu-id="319ad-300">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="319ad-300">Drivers License</span></span>
- <span data-ttu-id="319ad-301">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="319ad-301">Drivers Licenses</span></span>
- <span data-ttu-id="319ad-302">Driver'License</span><span class="sxs-lookup"><span data-stu-id="319ad-302">Driver'License</span></span>
- <span data-ttu-id="319ad-303">Driver'Licenses</span><span class="sxs-lookup"><span data-stu-id="319ad-303">Driver'Licenses</span></span>
- <span data-ttu-id="319ad-304">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="319ad-304">Driver' License</span></span>
- <span data-ttu-id="319ad-305">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="319ad-305">Driver' Licenses</span></span>
- <span data-ttu-id="319ad-306">Driver'sLicense</span><span class="sxs-lookup"><span data-stu-id="319ad-306">Driver'sLicense</span></span>
- <span data-ttu-id="319ad-307">Driver'sLicenses</span><span class="sxs-lookup"><span data-stu-id="319ad-307">Driver'sLicenses</span></span>
- <span data-ttu-id="319ad-308">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="319ad-308">Driver's License</span></span>
- <span data-ttu-id="319ad-309">Driver’s Licenses</span><span class="sxs-lookup"><span data-stu-id="319ad-309">Driver's Licenses</span></span>
- <span data-ttu-id="319ad-310">DriverLicense #</span><span class="sxs-lookup"><span data-stu-id="319ad-310">DriverLicense#</span></span>
- <span data-ttu-id="319ad-311">DriverLicenses #</span><span class="sxs-lookup"><span data-stu-id="319ad-311">DriverLicenses#</span></span>
- <span data-ttu-id="319ad-312">#Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="319ad-312">Driver License#</span></span>
- <span data-ttu-id="319ad-313">#Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="319ad-313">Driver Licenses#</span></span>
- <span data-ttu-id="319ad-314">DriversLicense #</span><span class="sxs-lookup"><span data-stu-id="319ad-314">DriversLicense#</span></span>
- <span data-ttu-id="319ad-315">DriversLicenses #</span><span class="sxs-lookup"><span data-stu-id="319ad-315">DriversLicenses#</span></span>
- <span data-ttu-id="319ad-316">#Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="319ad-316">Drivers License#</span></span>
- <span data-ttu-id="319ad-317">#Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="319ad-317">Drivers Licenses#</span></span>
- <span data-ttu-id="319ad-318">Driver'License #</span><span class="sxs-lookup"><span data-stu-id="319ad-318">Driver'License#</span></span>
- <span data-ttu-id="319ad-319">Driver'Licenses #</span><span class="sxs-lookup"><span data-stu-id="319ad-319">Driver'Licenses#</span></span>
- <span data-ttu-id="319ad-320">#Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="319ad-320">Driver' License#</span></span>
- <span data-ttu-id="319ad-321">#Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="319ad-321">Driver' Licenses#</span></span>
- <span data-ttu-id="319ad-322">Driver'sLicense #</span><span class="sxs-lookup"><span data-stu-id="319ad-322">Driver'sLicense#</span></span>
- <span data-ttu-id="319ad-323">Driver'sLicenses #</span><span class="sxs-lookup"><span data-stu-id="319ad-323">Driver'sLicenses#</span></span>
- <span data-ttu-id="319ad-324">#Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="319ad-324">Driver's License#</span></span>
- <span data-ttu-id="319ad-325">#Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="319ad-325">Driver's Licenses#</span></span>
   
## <a name="australia-medical-account-number"></a><span data-ttu-id="319ad-326">Numéro de dossier médical Australie</span><span class="sxs-lookup"><span data-stu-id="319ad-326">Australia Medical Account Number</span></span>

### <a name="format"></a><span data-ttu-id="319ad-327">Format</span><span class="sxs-lookup"><span data-stu-id="319ad-327">Format</span></span>

<span data-ttu-id="319ad-328">10 à 11 chiffres</span><span class="sxs-lookup"><span data-stu-id="319ad-328">10-11 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="319ad-329">Modèle</span><span class="sxs-lookup"><span data-stu-id="319ad-329">Pattern</span></span>

<span data-ttu-id="319ad-330">10 à 11 chiffres :</span><span class="sxs-lookup"><span data-stu-id="319ad-330">10-11 digits:</span></span>
- <span data-ttu-id="319ad-331">Le premier chiffre est compris entre 2 et 6</span><span class="sxs-lookup"><span data-stu-id="319ad-331">First digit is in the range 2-6</span></span>
- <span data-ttu-id="319ad-332">Le neuvième chiffre est un chiffre de contrôle</span><span class="sxs-lookup"><span data-stu-id="319ad-332">Ninth digit is a check digit</span></span>
- <span data-ttu-id="319ad-333">Le dixième chiffre est le chiffre d’émission</span><span class="sxs-lookup"><span data-stu-id="319ad-333">Tenth digit is the issue digit</span></span>
- <span data-ttu-id="319ad-334">Le onzième chiffre (facultatif) est le numéro individuel</span><span class="sxs-lookup"><span data-stu-id="319ad-334">Eleventh digit (optional) is the individual number</span></span>

### <a name="checksum"></a><span data-ttu-id="319ad-335">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="319ad-335">Checksum</span></span>

<span data-ttu-id="319ad-336">Oui</span><span class="sxs-lookup"><span data-stu-id="319ad-336">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="319ad-337">Définition</span><span class="sxs-lookup"><span data-stu-id="319ad-337">Definition</span></span>

<span data-ttu-id="319ad-338">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 95 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="319ad-338">A DLP policy is 95% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="319ad-339">La fonction Func_australian_medical_account_number trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="319ad-339">The function Func_australian_medical_account_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="319ad-340">Un mot clé figurant dans la liste Keyword_Australia_Medical_Account_Number est trouvé.</span><span class="sxs-lookup"><span data-stu-id="319ad-340">A keyword from Keyword_Australia_Medical_Account_Number is found.</span></span>
- <span data-ttu-id="319ad-341">La somme de contrôle est correcte.</span><span class="sxs-lookup"><span data-stu-id="319ad-341">The checksum passes.</span></span>

<span data-ttu-id="319ad-342">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="319ad-342">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="319ad-343">La fonction Func_australian_medical_account_number trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="319ad-343">The function Func_australian_medical_account_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="319ad-344">La somme de contrôle est correcte.</span><span class="sxs-lookup"><span data-stu-id="319ad-344">The checksum passes.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="319ad-345">Mots-clés</span><span class="sxs-lookup"><span data-stu-id="319ad-345">Keywords</span></span>

#### <a name="keyword_australia_medical_account_number"></a><span data-ttu-id="319ad-346">Keyword_Australia_Medical_Account_Number</span><span class="sxs-lookup"><span data-stu-id="319ad-346">Keyword_Australia_Medical_Account_Number</span></span>

- <span data-ttu-id="319ad-347">informations sur le compte bancaire</span><span class="sxs-lookup"><span data-stu-id="319ad-347">bank account details</span></span>
- <span data-ttu-id="319ad-348">remboursements d’assurance maladie</span><span class="sxs-lookup"><span data-stu-id="319ad-348">medicare payments</span></span>
- <span data-ttu-id="319ad-349">compte de prêts immobiliers</span><span class="sxs-lookup"><span data-stu-id="319ad-349">mortgage account</span></span>
- <span data-ttu-id="319ad-350">paiements bancaires</span><span class="sxs-lookup"><span data-stu-id="319ad-350">bank payments</span></span>
- <span data-ttu-id="319ad-351">direction de l’information</span><span class="sxs-lookup"><span data-stu-id="319ad-351">information branch</span></span>
- <span data-ttu-id="319ad-352">prêt sur carte de crédit</span><span class="sxs-lookup"><span data-stu-id="319ad-352">credit card loan</span></span>
- <span data-ttu-id="319ad-353">département des services sociaux</span><span class="sxs-lookup"><span data-stu-id="319ad-353">department of human services</span></span>
- <span data-ttu-id="319ad-354">service local</span><span class="sxs-lookup"><span data-stu-id="319ad-354">local service</span></span>
- <span data-ttu-id="319ad-355">médicaux</span><span class="sxs-lookup"><span data-stu-id="319ad-355">medicare</span></span>

   
## <a name="australia-passport-number"></a><span data-ttu-id="319ad-356">Numéro de passeport Australie</span><span class="sxs-lookup"><span data-stu-id="319ad-356">Australia Passport Number</span></span>

### <a name="format"></a><span data-ttu-id="319ad-357">Format</span><span class="sxs-lookup"><span data-stu-id="319ad-357">Format</span></span>

<span data-ttu-id="319ad-358">Une lettre suivie de sept chiffres</span><span class="sxs-lookup"><span data-stu-id="319ad-358">A letter followed by seven digits</span></span>

### <a name="pattern"></a><span data-ttu-id="319ad-359">Modèle</span><span class="sxs-lookup"><span data-stu-id="319ad-359">Pattern</span></span>

<span data-ttu-id="319ad-360">Une lettre (ne respectant pas la casse) suivie de sept chiffres</span><span class="sxs-lookup"><span data-stu-id="319ad-360">A letter (not case sensitive) followed by seven digits</span></span>

### <a name="checksum"></a><span data-ttu-id="319ad-361">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="319ad-361">Checksum</span></span>

<span data-ttu-id="319ad-362">Non</span><span class="sxs-lookup"><span data-stu-id="319ad-362">No</span></span>

### <a name="definition"></a><span data-ttu-id="319ad-363">Définition</span><span class="sxs-lookup"><span data-stu-id="319ad-363">Definition</span></span>

<span data-ttu-id="319ad-364">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="319ad-364">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="319ad-365">L’expression régulière Regex_australia_passport_number trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="319ad-365">The regular expression Regex_australia_passport_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="319ad-366">Un mot clé depuis Keyword_passport ou Keyword_australia_passport_number est trouvé.</span><span class="sxs-lookup"><span data-stu-id="319ad-366">A keyword from Keyword_passport or Keyword_australia_passport_number is found.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="319ad-367">Mots-clés</span><span class="sxs-lookup"><span data-stu-id="319ad-367">Keywords</span></span>

#### <a name="keyword_passport"></a><span data-ttu-id="319ad-368">Keyword_passport</span><span class="sxs-lookup"><span data-stu-id="319ad-368">Keyword_passport</span></span>

- <span data-ttu-id="319ad-369">Numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="319ad-369">Passport Number</span></span>
- <span data-ttu-id="319ad-370">N° de passeport</span><span class="sxs-lookup"><span data-stu-id="319ad-370">Passport No</span></span>
- <span data-ttu-id="319ad-371"># Passeport</span><span class="sxs-lookup"><span data-stu-id="319ad-371">Passport #</span></span>
- <span data-ttu-id="319ad-372">Tel #</span><span class="sxs-lookup"><span data-stu-id="319ad-372">Passport#</span></span>
- <span data-ttu-id="319ad-373">PassportID</span><span class="sxs-lookup"><span data-stu-id="319ad-373">PassportID</span></span>
- <span data-ttu-id="319ad-374">N ° passeport</span><span class="sxs-lookup"><span data-stu-id="319ad-374">Passportno</span></span>
- <span data-ttu-id="319ad-375">passportnumber</span><span class="sxs-lookup"><span data-stu-id="319ad-375">passportnumber</span></span>
- <span data-ttu-id="319ad-376">パスポート</span><span class="sxs-lookup"><span data-stu-id="319ad-376">パスポート</span></span>
- <span data-ttu-id="319ad-377">パスポート番号</span><span class="sxs-lookup"><span data-stu-id="319ad-377">パスポート番号</span></span>
- <span data-ttu-id="319ad-378">パスポートのNum</span><span class="sxs-lookup"><span data-stu-id="319ad-378">パスポートのNum</span></span>
- <span data-ttu-id="319ad-379">パスポート＃</span><span class="sxs-lookup"><span data-stu-id="319ad-379">パスポート ＃</span></span> 
- <span data-ttu-id="319ad-380">Numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="319ad-380">Numéro de passeport</span></span>
- <span data-ttu-id="319ad-381">Passeport n°</span><span class="sxs-lookup"><span data-stu-id="319ad-381">Passeport n °</span></span>
- <span data-ttu-id="319ad-382">Passeport numéro</span><span class="sxs-lookup"><span data-stu-id="319ad-382">Passeport Non</span></span>
- <span data-ttu-id="319ad-383"># Passeport</span><span class="sxs-lookup"><span data-stu-id="319ad-383">Passeport #</span></span>
- <span data-ttu-id="319ad-384">Passeport #</span><span class="sxs-lookup"><span data-stu-id="319ad-384">Passeport#</span></span>
- <span data-ttu-id="319ad-385">PasseportNon</span><span class="sxs-lookup"><span data-stu-id="319ad-385">PasseportNon</span></span>
- <span data-ttu-id="319ad-386">Passeportn °</span><span class="sxs-lookup"><span data-stu-id="319ad-386">Passeportn °</span></span>

#### <a name="keyword_australia_passport_number"></a><span data-ttu-id="319ad-387">Keyword_australia_passport_number</span><span class="sxs-lookup"><span data-stu-id="319ad-387">Keyword_australia_passport_number</span></span>

- <span data-ttu-id="319ad-388">tel</span><span class="sxs-lookup"><span data-stu-id="319ad-388">passport</span></span>
- <span data-ttu-id="319ad-389">informations sur le passeport</span><span class="sxs-lookup"><span data-stu-id="319ad-389">passport details</span></span>
- <span data-ttu-id="319ad-390">immigration et citoyenneté</span><span class="sxs-lookup"><span data-stu-id="319ad-390">immigration and citizenship</span></span>
- <span data-ttu-id="319ad-391">Australie</span><span class="sxs-lookup"><span data-stu-id="319ad-391">commonwealth of australia</span></span>
- <span data-ttu-id="319ad-392">service de l’immigration</span><span class="sxs-lookup"><span data-stu-id="319ad-392">department of immigration</span></span>
- <span data-ttu-id="319ad-393">adresse de résidence</span><span class="sxs-lookup"><span data-stu-id="319ad-393">residential address</span></span>
- <span data-ttu-id="319ad-394">service de l’immigration et de la citoyenneté</span><span class="sxs-lookup"><span data-stu-id="319ad-394">department of immigration and citizenship</span></span>
- <span data-ttu-id="319ad-395">délivrance</span><span class="sxs-lookup"><span data-stu-id="319ad-395">visa</span></span>
- <span data-ttu-id="319ad-396">Carte nationale d’identité</span><span class="sxs-lookup"><span data-stu-id="319ad-396">national identity card</span></span>
- <span data-ttu-id="319ad-397">numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="319ad-397">passport number</span></span>
- <span data-ttu-id="319ad-398">document de voyage</span><span class="sxs-lookup"><span data-stu-id="319ad-398">travel document</span></span>
- <span data-ttu-id="319ad-399">autorité émettrice</span><span class="sxs-lookup"><span data-stu-id="319ad-399">issuing authority</span></span>
   
## <a name="australia-tax-file-number"></a><span data-ttu-id="319ad-400">Numéro de dossier fiscal Australie</span><span class="sxs-lookup"><span data-stu-id="319ad-400">Australia Tax File Number</span></span>

### <a name="format"></a><span data-ttu-id="319ad-401">Format</span><span class="sxs-lookup"><span data-stu-id="319ad-401">Format</span></span>

<span data-ttu-id="319ad-402">8 ou 9 chiffres</span><span class="sxs-lookup"><span data-stu-id="319ad-402">8-9 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="319ad-403">Modèle</span><span class="sxs-lookup"><span data-stu-id="319ad-403">Pattern</span></span>

<span data-ttu-id="319ad-404">8 à 9 chiffres généralement entrecoupés d’espaces comme suit :</span><span class="sxs-lookup"><span data-stu-id="319ad-404">8-9 digits typically presented with spaces as follows:</span></span>
- <span data-ttu-id="319ad-405">Trois chiffres</span><span class="sxs-lookup"><span data-stu-id="319ad-405">Three digits</span></span> 
- <span data-ttu-id="319ad-406">Un espace facultatif</span><span class="sxs-lookup"><span data-stu-id="319ad-406">An optional space</span></span> 
- <span data-ttu-id="319ad-407">Trois chiffres</span><span class="sxs-lookup"><span data-stu-id="319ad-407">Three digits</span></span> 
- <span data-ttu-id="319ad-408">Un espace facultatif</span><span class="sxs-lookup"><span data-stu-id="319ad-408">An optional space</span></span> 
- <span data-ttu-id="319ad-409">2 à 3 chiffres où le dernier chiffre est un chiffre de contrôle</span><span class="sxs-lookup"><span data-stu-id="319ad-409">2-3 digits where the last digit is a check digit</span></span>

### <a name="checksum"></a><span data-ttu-id="319ad-410">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="319ad-410">Checksum</span></span>

<span data-ttu-id="319ad-411">Oui</span><span class="sxs-lookup"><span data-stu-id="319ad-411">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="319ad-412">Définition</span><span class="sxs-lookup"><span data-stu-id="319ad-412">Definition</span></span>

<span data-ttu-id="319ad-413">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="319ad-413">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="319ad-414">La fonction Func_australian_tax_file_number trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="319ad-414">The function Func_australian_tax_file_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="319ad-415">Aucun mot clé figurant dans la liste Keyword_Australia_Tax_File_Number ou Keyword_number_exclusions n’est trouvé.</span><span class="sxs-lookup"><span data-stu-id="319ad-415">No keyword from Keyword_Australia_Tax_File_Number or Keyword_number_exclusions is found.</span></span>
- <span data-ttu-id="319ad-416">La somme de contrôle est correcte.</span><span class="sxs-lookup"><span data-stu-id="319ad-416">The checksum passes.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="319ad-417">Mots-clés</span><span class="sxs-lookup"><span data-stu-id="319ad-417">Keywords</span></span>

#### <a name="keyword_australia_tax_file_number"></a><span data-ttu-id="319ad-418">Keyword_Australia_Tax_File_Number</span><span class="sxs-lookup"><span data-stu-id="319ad-418">Keyword_Australia_Tax_File_Number</span></span>

- <span data-ttu-id="319ad-419">numéro d’entreprise australien</span><span class="sxs-lookup"><span data-stu-id="319ad-419">australian business number</span></span>
- <span data-ttu-id="319ad-420">taux d’imposition marginale</span><span class="sxs-lookup"><span data-stu-id="319ad-420">marginal tax rate</span></span>
- <span data-ttu-id="319ad-421">prélèvement d’assurance maladie</span><span class="sxs-lookup"><span data-stu-id="319ad-421">medicare levy</span></span>
- <span data-ttu-id="319ad-422">numéro de portefeuille</span><span class="sxs-lookup"><span data-stu-id="319ad-422">portfolio number</span></span>
- <span data-ttu-id="319ad-423">service des vétérans</span><span class="sxs-lookup"><span data-stu-id="319ad-423">service veterans</span></span>
- <span data-ttu-id="319ad-424">retenue à la source</span><span class="sxs-lookup"><span data-stu-id="319ad-424">withholding tax</span></span>
- <span data-ttu-id="319ad-425">déclaration d’impôts individuels</span><span class="sxs-lookup"><span data-stu-id="319ad-425">individual tax return</span></span>
- <span data-ttu-id="319ad-426">numéro de dossier fiscal</span><span class="sxs-lookup"><span data-stu-id="319ad-426">tax file number</span></span>

#### <a name="keyword_number_exclusions"></a><span data-ttu-id="319ad-427">Keyword_number_exclusions</span><span class="sxs-lookup"><span data-stu-id="319ad-427">Keyword_number_exclusions</span></span>

- <span data-ttu-id="319ad-428">00000000</span><span class="sxs-lookup"><span data-stu-id="319ad-428">00000000</span></span>
- <span data-ttu-id="319ad-429">11111111</span><span class="sxs-lookup"><span data-stu-id="319ad-429">11111111</span></span>
- <span data-ttu-id="319ad-430">22222222</span><span class="sxs-lookup"><span data-stu-id="319ad-430">22222222</span></span>
- <span data-ttu-id="319ad-431">33333333</span><span class="sxs-lookup"><span data-stu-id="319ad-431">33333333</span></span>
- <span data-ttu-id="319ad-432">44444444</span><span class="sxs-lookup"><span data-stu-id="319ad-432">44444444</span></span>
- <span data-ttu-id="319ad-433">55555555</span><span class="sxs-lookup"><span data-stu-id="319ad-433">55555555</span></span>
- <span data-ttu-id="319ad-434">66666666</span><span class="sxs-lookup"><span data-stu-id="319ad-434">66666666</span></span>
- <span data-ttu-id="319ad-435">77777777</span><span class="sxs-lookup"><span data-stu-id="319ad-435">77777777</span></span>
- <span data-ttu-id="319ad-436">88888888</span><span class="sxs-lookup"><span data-stu-id="319ad-436">88888888</span></span>
- <span data-ttu-id="319ad-437">99999999</span><span class="sxs-lookup"><span data-stu-id="319ad-437">99999999</span></span>
- <span data-ttu-id="319ad-438">000000000</span><span class="sxs-lookup"><span data-stu-id="319ad-438">000000000</span></span>
- <span data-ttu-id="319ad-439">111111111</span><span class="sxs-lookup"><span data-stu-id="319ad-439">111111111</span></span>
- <span data-ttu-id="319ad-440">222222222</span><span class="sxs-lookup"><span data-stu-id="319ad-440">222222222</span></span>
- <span data-ttu-id="319ad-441">333333333</span><span class="sxs-lookup"><span data-stu-id="319ad-441">333333333</span></span>
- <span data-ttu-id="319ad-442">444444444</span><span class="sxs-lookup"><span data-stu-id="319ad-442">444444444</span></span>
- <span data-ttu-id="319ad-443">555555555</span><span class="sxs-lookup"><span data-stu-id="319ad-443">555555555</span></span>
- <span data-ttu-id="319ad-444">666666666</span><span class="sxs-lookup"><span data-stu-id="319ad-444">666666666</span></span>
- <span data-ttu-id="319ad-445">777777777</span><span class="sxs-lookup"><span data-stu-id="319ad-445">777777777</span></span>
- <span data-ttu-id="319ad-446">888888888</span><span class="sxs-lookup"><span data-stu-id="319ad-446">888888888</span></span>
- <span data-ttu-id="319ad-447">999999999</span><span class="sxs-lookup"><span data-stu-id="319ad-447">999999999</span></span>
- <span data-ttu-id="319ad-448">0000000000</span><span class="sxs-lookup"><span data-stu-id="319ad-448">0000000000</span></span>
- <span data-ttu-id="319ad-449">1111111111</span><span class="sxs-lookup"><span data-stu-id="319ad-449">1111111111</span></span>
- <span data-ttu-id="319ad-450">2222222222</span><span class="sxs-lookup"><span data-stu-id="319ad-450">2222222222</span></span>
- <span data-ttu-id="319ad-451">3333333333</span><span class="sxs-lookup"><span data-stu-id="319ad-451">3333333333</span></span>
- <span data-ttu-id="319ad-452">4444444444</span><span class="sxs-lookup"><span data-stu-id="319ad-452">4444444444</span></span>
- <span data-ttu-id="319ad-453">5555555555</span><span class="sxs-lookup"><span data-stu-id="319ad-453">5555555555</span></span>
- <span data-ttu-id="319ad-454">6666666666</span><span class="sxs-lookup"><span data-stu-id="319ad-454">6666666666</span></span>
- <span data-ttu-id="319ad-455">7777777777</span><span class="sxs-lookup"><span data-stu-id="319ad-455">7777777777</span></span>
- <span data-ttu-id="319ad-456">8888888888</span><span class="sxs-lookup"><span data-stu-id="319ad-456">8888888888</span></span>
- <span data-ttu-id="319ad-457">9999999999</span><span class="sxs-lookup"><span data-stu-id="319ad-457">9999999999</span></span>

## <a name="azure-documentdb-auth-key"></a><span data-ttu-id="319ad-458">Clé d’authentification Azure DocumentDB</span><span class="sxs-lookup"><span data-stu-id="319ad-458">Azure DocumentDB Auth Key</span></span>

### <a name="format"></a><span data-ttu-id="319ad-459">Format</span><span class="sxs-lookup"><span data-stu-id="319ad-459">Format</span></span>

<span data-ttu-id="319ad-460">La chaîne « DocumentDb » suivie des caractères et des chaînes présentés dans le modèle ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="319ad-460">The string "DocumentDb" followed by the characters and strings outlined in the pattern below.</span></span>

### <a name="pattern"></a><span data-ttu-id="319ad-461">Modèle</span><span class="sxs-lookup"><span data-stu-id="319ad-461">Pattern</span></span>

- <span data-ttu-id="319ad-462">La chaîne « DocumentDb »</span><span class="sxs-lookup"><span data-stu-id="319ad-462">The string "DocumentDb"</span></span>
- <span data-ttu-id="319ad-463">N’importe quelle combinaison entre 3-200 majuscules ou minuscules, des chiffres, des symboles, des caractères spéciaux ou des espaces</span><span class="sxs-lookup"><span data-stu-id="319ad-463">Any combination of between 3-200 lower- or uppercase letters, digits, symbols, special characters, or spaces</span></span>
- <span data-ttu-id="319ad-464">Symbole supérieur à (>), signe égal (=), guillemet (") ou apostrophe (')</span><span class="sxs-lookup"><span data-stu-id="319ad-464">A greater than symbol (>), an equal sign (=), a quotation mark ("), or an apostrophe (')</span></span>
- <span data-ttu-id="319ad-465">Toute combinaison de 86 lettres majuscules ou minuscules, des chiffres, une barre oblique (/) ou un signe plus (+)</span><span class="sxs-lookup"><span data-stu-id="319ad-465">Any combination of 86 lower- or uppercase letters, digits, forward slash (/), or plus sign (+)</span></span>
- <span data-ttu-id="319ad-466">Deux signes égal (=)</span><span class="sxs-lookup"><span data-stu-id="319ad-466">Two equal signs (=)</span></span>

### <a name="checksum"></a><span data-ttu-id="319ad-467">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="319ad-467">Checksum</span></span>

<span data-ttu-id="319ad-468">Non</span><span class="sxs-lookup"><span data-stu-id="319ad-468">No</span></span>

### <a name="definition"></a><span data-ttu-id="319ad-469">Définition</span><span class="sxs-lookup"><span data-stu-id="319ad-469">Definition</span></span>

<span data-ttu-id="319ad-470">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="319ad-470">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="319ad-471">L’expression régulière CEP_Regex_AzureDocumentDBAuthKey trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="319ad-471">The regular expression CEP_Regex_AzureDocumentDBAuthKey finds content that matches the pattern.</span></span>
- <span data-ttu-id="319ad-472">L’expression régulière CEP_CommonExampleKeywords ne trouve **pas** le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="319ad-472">The regular expression CEP_CommonExampleKeywords does **not** find content that matches the pattern.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="319ad-473">Mots-clés</span><span class="sxs-lookup"><span data-stu-id="319ad-473">Keywords</span></span>

#### <a name="cep_commonexamplekeywords"></a><span data-ttu-id="319ad-474">CEP_CommonExampleKeywords</span><span class="sxs-lookup"><span data-stu-id="319ad-474">CEP_CommonExampleKeywords</span></span>

<span data-ttu-id="319ad-475">(Notez que techniquement, ce type d’informations sensibles identifie ces mots clés à l’aide d’une expression régulière, et non d’une liste de mots clés.)</span><span class="sxs-lookup"><span data-stu-id="319ad-475">(Note that technically, this sensitive information type identifies these keywords by using a regular expression, not a keyword list.)</span></span>

- <span data-ttu-id="319ad-476">contoso</span><span class="sxs-lookup"><span data-stu-id="319ad-476">contoso</span></span>
- <span data-ttu-id="319ad-477">société</span><span class="sxs-lookup"><span data-stu-id="319ad-477">fabrikam</span></span>
- <span data-ttu-id="319ad-478">Northwind</span><span class="sxs-lookup"><span data-stu-id="319ad-478">northwind</span></span>
- <span data-ttu-id="319ad-479">immédiatement</span><span class="sxs-lookup"><span data-stu-id="319ad-479">sandbox</span></span>
- <span data-ttu-id="319ad-480">onebox</span><span class="sxs-lookup"><span data-stu-id="319ad-480">onebox</span></span>
- <span data-ttu-id="319ad-481">hôte</span><span class="sxs-lookup"><span data-stu-id="319ad-481">localhost</span></span>
- <span data-ttu-id="319ad-482">bouclage</span><span class="sxs-lookup"><span data-stu-id="319ad-482">127.0.0.1</span></span>
- <span data-ttu-id="319ad-483">testacs.</span><span class="sxs-lookup"><span data-stu-id="319ad-483">testacs.</span></span><!--no-hyperlink--><span data-ttu-id="319ad-484">com</span><span class="sxs-lookup"><span data-stu-id="319ad-484">com</span></span>
- <span data-ttu-id="319ad-485">s-int.</span><span class="sxs-lookup"><span data-stu-id="319ad-485">s-int.</span></span><!--no-hyperlink--><span data-ttu-id="319ad-486">NET</span><span class="sxs-lookup"><span data-stu-id="319ad-486">net</span></span>

## <a name="azure-iaas-database-connection-string-and-azure-sql-connection-string"></a><span data-ttu-id="319ad-487">Chaîne de connexion à la base de données IAAS Azure et chaîne de connexion Azure SQL</span><span class="sxs-lookup"><span data-stu-id="319ad-487">Azure IAAS Database Connection String and Azure SQL Connection String</span></span>

### <a name="format"></a><span data-ttu-id="319ad-488">Format</span><span class="sxs-lookup"><span data-stu-id="319ad-488">Format</span></span>

<span data-ttu-id="319ad-489">La chaîne « Server », « Server » ou « Data source » suivie des caractères et des chaînes décrits dans le modèle ci-dessous, y compris la chaîne «cloudapp. Azure.</span><span class="sxs-lookup"><span data-stu-id="319ad-489">The string "Server", "server", or "data source" followed by the characters and strings outlined in the pattern below, including the string "cloudapp.azure.</span></span><!--no-hyperlink--><span data-ttu-id="319ad-490">com» ou «cloudapp. Azure.</span><span class="sxs-lookup"><span data-stu-id="319ad-490">com" or "cloudapp.azure.</span></span><!--no-hyperlink--><span data-ttu-id="319ad-491">NET "ou" Database. Windows.</span><span class="sxs-lookup"><span data-stu-id="319ad-491">net" or "database.windows.</span></span><!--no-hyperlink--><span data-ttu-id="319ad-492">NET ", et la chaîne" password "ou" password "ou" PWD ".</span><span class="sxs-lookup"><span data-stu-id="319ad-492">net", and the string "Password" or "password" or "pwd".</span></span>

### <a name="pattern"></a><span data-ttu-id="319ad-493">Modèle</span><span class="sxs-lookup"><span data-stu-id="319ad-493">Pattern</span></span>

- <span data-ttu-id="319ad-494">Chaîne « serveur », « serveur » ou « source de données »</span><span class="sxs-lookup"><span data-stu-id="319ad-494">The string "Server", "server", or "data source"</span></span>
- <span data-ttu-id="319ad-495">0-2 espaces blancs</span><span class="sxs-lookup"><span data-stu-id="319ad-495">0-2 whitespace characters</span></span>
- <span data-ttu-id="319ad-496">Signe égal (=)</span><span class="sxs-lookup"><span data-stu-id="319ad-496">An equal sign (=)</span></span>
- <span data-ttu-id="319ad-497">0-2 espaces blancs</span><span class="sxs-lookup"><span data-stu-id="319ad-497">0-2 whitespace characters</span></span>
- <span data-ttu-id="319ad-498">N’importe quelle combinaison entre 1-200 majuscules ou minuscules, des chiffres, des symboles, des caractères spéciaux ou des espaces</span><span class="sxs-lookup"><span data-stu-id="319ad-498">Any combination of between 1-200 lower- or uppercase letters, digits, symbols, special characters, or spaces</span></span>
- <span data-ttu-id="319ad-499">La chaîne «cloudapp. Azure.</span><span class="sxs-lookup"><span data-stu-id="319ad-499">The string "cloudapp.azure.</span></span><!--no-hyperlink--><span data-ttu-id="319ad-500">com "," cloudapp. Azure.</span><span class="sxs-lookup"><span data-stu-id="319ad-500">com", "cloudapp.azure.</span></span><!--no-hyperlink--><span data-ttu-id="319ad-501">NET "ou" Database. Windows.</span><span class="sxs-lookup"><span data-stu-id="319ad-501">net", or "database.windows.</span></span><!--no-hyperlink--><span data-ttu-id="319ad-502">NET</span><span class="sxs-lookup"><span data-stu-id="319ad-502">net"</span></span>
- <span data-ttu-id="319ad-503">N’importe quelle combinaison entre 1-300 majuscules ou minuscules, des chiffres, des symboles, des caractères spéciaux ou des espaces</span><span class="sxs-lookup"><span data-stu-id="319ad-503">Any combination of between 1-300 lower- or uppercase letters, digits, symbols, special characters, or spaces</span></span>
- <span data-ttu-id="319ad-504">La chaîne "password", "password" ou "PWD"</span><span class="sxs-lookup"><span data-stu-id="319ad-504">The string "Password", "password", or "pwd"</span></span>
- <span data-ttu-id="319ad-505">0-2 espaces blancs</span><span class="sxs-lookup"><span data-stu-id="319ad-505">0-2 whitespace characters</span></span>
- <span data-ttu-id="319ad-506">Signe égal (=)</span><span class="sxs-lookup"><span data-stu-id="319ad-506">An equal sign (=)</span></span>
- <span data-ttu-id="319ad-507">0-2 espaces blancs</span><span class="sxs-lookup"><span data-stu-id="319ad-507">0-2 whitespace characters</span></span>
- <span data-ttu-id="319ad-508">Un ou plusieurs caractères qui ne sont pas des points-virgules (;), guillemets (") ou apostrophe (')</span><span class="sxs-lookup"><span data-stu-id="319ad-508">One or more characters that is not a semicolon (;), quotation mark ("), or apostrophe (')</span></span>
- <span data-ttu-id="319ad-509">Un point-virgule (;), guillemet (") ou apostrophe (')</span><span class="sxs-lookup"><span data-stu-id="319ad-509">A semicolon (;), quotation mark ("), or apostrophe (')</span></span>

### <a name="checksum"></a><span data-ttu-id="319ad-510">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="319ad-510">Checksum</span></span>

<span data-ttu-id="319ad-511">Non</span><span class="sxs-lookup"><span data-stu-id="319ad-511">No</span></span>

### <a name="definition"></a><span data-ttu-id="319ad-512">Définition</span><span class="sxs-lookup"><span data-stu-id="319ad-512">Definition</span></span>

<span data-ttu-id="319ad-513">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="319ad-513">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="319ad-514">L’expression régulière CEP_Regex_AzureConnectionString trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="319ad-514">The regular expression CEP_Regex_AzureConnectionString finds content that matches the pattern.</span></span>
- <span data-ttu-id="319ad-515">L’expression régulière CEP_CommonExampleKeywords ne trouve **pas** le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="319ad-515">The regular expression CEP_CommonExampleKeywords does **not** find content that matches the pattern.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="319ad-516">Mots-clés</span><span class="sxs-lookup"><span data-stu-id="319ad-516">Keywords</span></span>

#### <a name="cep_commonexamplekeywords"></a><span data-ttu-id="319ad-517">CEP_CommonExampleKeywords</span><span class="sxs-lookup"><span data-stu-id="319ad-517">CEP_CommonExampleKeywords</span></span>

<span data-ttu-id="319ad-518">(Notez que techniquement, ce type d’informations sensibles identifie ces mots clés à l’aide d’une expression régulière, et non d’une liste de mots clés.)</span><span class="sxs-lookup"><span data-stu-id="319ad-518">(Note that technically, this sensitive information type identifies these keywords by using a regular expression, not a keyword list.)</span></span>

- <span data-ttu-id="319ad-519">contoso</span><span class="sxs-lookup"><span data-stu-id="319ad-519">contoso</span></span>
- <span data-ttu-id="319ad-520">société</span><span class="sxs-lookup"><span data-stu-id="319ad-520">fabrikam</span></span>
- <span data-ttu-id="319ad-521">Northwind</span><span class="sxs-lookup"><span data-stu-id="319ad-521">northwind</span></span>
- <span data-ttu-id="319ad-522">immédiatement</span><span class="sxs-lookup"><span data-stu-id="319ad-522">sandbox</span></span>
- <span data-ttu-id="319ad-523">onebox</span><span class="sxs-lookup"><span data-stu-id="319ad-523">onebox</span></span>
- <span data-ttu-id="319ad-524">hôte</span><span class="sxs-lookup"><span data-stu-id="319ad-524">localhost</span></span>
- <span data-ttu-id="319ad-525">bouclage</span><span class="sxs-lookup"><span data-stu-id="319ad-525">127.0.0.1</span></span>
- <span data-ttu-id="319ad-526">testacs.</span><span class="sxs-lookup"><span data-stu-id="319ad-526">testacs.</span></span><!--no-hyperlink--><span data-ttu-id="319ad-527">com</span><span class="sxs-lookup"><span data-stu-id="319ad-527">com</span></span>
- <span data-ttu-id="319ad-528">s-int.</span><span class="sxs-lookup"><span data-stu-id="319ad-528">s-int.</span></span><!--no-hyperlink--><span data-ttu-id="319ad-529">NET</span><span class="sxs-lookup"><span data-stu-id="319ad-529">net</span></span>

## <a name="azure-iot-connection-string"></a><span data-ttu-id="319ad-530">Chaîne de connexion Azure IoT</span><span class="sxs-lookup"><span data-stu-id="319ad-530">Azure IoT Connection String</span></span>

### <a name="format"></a><span data-ttu-id="319ad-531">Format</span><span class="sxs-lookup"><span data-stu-id="319ad-531">Format</span></span>

<span data-ttu-id="319ad-532">La chaîne « nomhôte » suivie des caractères et des chaînes décrits dans le modèle ci-dessous, y compris les chaînes «Azure-appareils.</span><span class="sxs-lookup"><span data-stu-id="319ad-532">The string "HostName" followed by the characters and strings outlined in the pattern below, including the strings "azure-devices.</span></span><!--no-hyperlink--><span data-ttu-id="319ad-533">NET "et" SharedAccessKey ".</span><span class="sxs-lookup"><span data-stu-id="319ad-533">net" and "SharedAccessKey".</span></span>

### <a name="pattern"></a><span data-ttu-id="319ad-534">Modèle</span><span class="sxs-lookup"><span data-stu-id="319ad-534">Pattern</span></span>

- <span data-ttu-id="319ad-535">La chaîne « nomhôte »</span><span class="sxs-lookup"><span data-stu-id="319ad-535">The string "HostName"</span></span>
- <span data-ttu-id="319ad-536">0-2 espaces blancs</span><span class="sxs-lookup"><span data-stu-id="319ad-536">0-2 whitespace characters</span></span>
- <span data-ttu-id="319ad-537">Signe égal (=)</span><span class="sxs-lookup"><span data-stu-id="319ad-537">An equal sign (=)</span></span>
- <span data-ttu-id="319ad-538">0-2 espaces blancs</span><span class="sxs-lookup"><span data-stu-id="319ad-538">0-2 whitespace characters</span></span>
- <span data-ttu-id="319ad-539">N’importe quelle combinaison entre 1-200 majuscules ou minuscules, des chiffres, des symboles, des caractères spéciaux ou des espaces</span><span class="sxs-lookup"><span data-stu-id="319ad-539">Any combination of between 1-200 lower- or uppercase letters, digits, symbols, special characters, or spaces</span></span>
- <span data-ttu-id="319ad-540">La chaîne «Azure-appareils.</span><span class="sxs-lookup"><span data-stu-id="319ad-540">The string "azure-devices.</span></span><!--no-hyperlink--><span data-ttu-id="319ad-541">NET</span><span class="sxs-lookup"><span data-stu-id="319ad-541">net"</span></span>
- <span data-ttu-id="319ad-542">N’importe quelle combinaison entre 1-200 majuscules ou minuscules, des chiffres, des symboles, des caractères spéciaux ou des espaces</span><span class="sxs-lookup"><span data-stu-id="319ad-542">Any combination of between 1-200 lower- or uppercase letters, digits, symbols, special characters, or spaces</span></span>
- <span data-ttu-id="319ad-543">La chaîne « SharedAccessKey »</span><span class="sxs-lookup"><span data-stu-id="319ad-543">The string "SharedAccessKey"</span></span>
- <span data-ttu-id="319ad-544">0-2 espaces blancs</span><span class="sxs-lookup"><span data-stu-id="319ad-544">0-2 whitespace characters</span></span>
- <span data-ttu-id="319ad-545">Signe égal (=)</span><span class="sxs-lookup"><span data-stu-id="319ad-545">An equal sign (=)</span></span>
- <span data-ttu-id="319ad-546">0-2 espaces blancs</span><span class="sxs-lookup"><span data-stu-id="319ad-546">0-2 whitespace characters</span></span>
- <span data-ttu-id="319ad-547">Toute combinaison de 43 lettres majuscules ou minuscules, des chiffres, une barre oblique (/) ou un signe plus (+)</span><span class="sxs-lookup"><span data-stu-id="319ad-547">Any combination of 43 lower- or uppercase letters, digits, forward slash (/), or plus sign (+)</span></span>
- <span data-ttu-id="319ad-548">Signe égal (=)</span><span class="sxs-lookup"><span data-stu-id="319ad-548">An equal sign (=)</span></span>

### <a name="checksum"></a><span data-ttu-id="319ad-549">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="319ad-549">Checksum</span></span>

<span data-ttu-id="319ad-550">Non</span><span class="sxs-lookup"><span data-stu-id="319ad-550">No</span></span>

### <a name="definition"></a><span data-ttu-id="319ad-551">Définition</span><span class="sxs-lookup"><span data-stu-id="319ad-551">Definition</span></span>

<span data-ttu-id="319ad-552">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="319ad-552">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="319ad-553">L’expression régulière CEP_Regex_AzureIoTConnectionString trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="319ad-553">The regular expression CEP_Regex_AzureIoTConnectionString finds content that matches the pattern.</span></span>
- <span data-ttu-id="319ad-554">L’expression régulière CEP_CommonExampleKeywords ne trouve **pas** le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="319ad-554">The regular expression CEP_CommonExampleKeywords does **not** find content that matches the pattern.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="319ad-555">Mots-clés</span><span class="sxs-lookup"><span data-stu-id="319ad-555">Keywords</span></span>

#### <a name="cep_commonexamplekeywords"></a><span data-ttu-id="319ad-556">CEP_CommonExampleKeywords</span><span class="sxs-lookup"><span data-stu-id="319ad-556">CEP_CommonExampleKeywords</span></span>

<span data-ttu-id="319ad-557">(Notez que techniquement, ce type d’informations sensibles identifie ces mots clés à l’aide d’une expression régulière, et non d’une liste de mots clés.)</span><span class="sxs-lookup"><span data-stu-id="319ad-557">(Note that technically, this sensitive information type identifies these keywords by using a regular expression, not a keyword list.)</span></span>

- <span data-ttu-id="319ad-558">contoso</span><span class="sxs-lookup"><span data-stu-id="319ad-558">contoso</span></span>
- <span data-ttu-id="319ad-559">société</span><span class="sxs-lookup"><span data-stu-id="319ad-559">fabrikam</span></span>
- <span data-ttu-id="319ad-560">Northwind</span><span class="sxs-lookup"><span data-stu-id="319ad-560">northwind</span></span>
- <span data-ttu-id="319ad-561">immédiatement</span><span class="sxs-lookup"><span data-stu-id="319ad-561">sandbox</span></span>
- <span data-ttu-id="319ad-562">onebox</span><span class="sxs-lookup"><span data-stu-id="319ad-562">onebox</span></span>
- <span data-ttu-id="319ad-563">hôte</span><span class="sxs-lookup"><span data-stu-id="319ad-563">localhost</span></span>
- <span data-ttu-id="319ad-564">bouclage</span><span class="sxs-lookup"><span data-stu-id="319ad-564">127.0.0.1</span></span>
- <span data-ttu-id="319ad-565">testacs.</span><span class="sxs-lookup"><span data-stu-id="319ad-565">testacs.</span></span><!--no-hyperlink--><span data-ttu-id="319ad-566">com</span><span class="sxs-lookup"><span data-stu-id="319ad-566">com</span></span>
- <span data-ttu-id="319ad-567">s-int.</span><span class="sxs-lookup"><span data-stu-id="319ad-567">s-int.</span></span><!--no-hyperlink--><span data-ttu-id="319ad-568">NET</span><span class="sxs-lookup"><span data-stu-id="319ad-568">net</span></span>

## <a name="azure-publish-setting-password"></a><span data-ttu-id="319ad-569">Mot de passe de paramètre de publication Azure</span><span class="sxs-lookup"><span data-stu-id="319ad-569">Azure Publish Setting Password</span></span>

### <a name="format"></a><span data-ttu-id="319ad-570">Format</span><span class="sxs-lookup"><span data-stu-id="319ad-570">Format</span></span>

<span data-ttu-id="319ad-571">La chaîne « userpwd = » suivie d’une chaîne alphanumérique.</span><span class="sxs-lookup"><span data-stu-id="319ad-571">The string "userpwd=" followed by an alphanumeric string.</span></span>

### <a name="pattern"></a><span data-ttu-id="319ad-572">Modèle</span><span class="sxs-lookup"><span data-stu-id="319ad-572">Pattern</span></span>

- <span data-ttu-id="319ad-573">La chaîne « userpwd = »</span><span class="sxs-lookup"><span data-stu-id="319ad-573">The string "userpwd="</span></span>
- <span data-ttu-id="319ad-574">N’importe quelle combinaison de 60 lettres minuscules ou chiffres</span><span class="sxs-lookup"><span data-stu-id="319ad-574">Any combination of 60 lowercase letters or digits</span></span>
- <span data-ttu-id="319ad-575">Guillemet (")</span><span class="sxs-lookup"><span data-stu-id="319ad-575">A quotation mark (")</span></span>

### <a name="checksum"></a><span data-ttu-id="319ad-576">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="319ad-576">Checksum</span></span>

<span data-ttu-id="319ad-577">Non</span><span class="sxs-lookup"><span data-stu-id="319ad-577">No</span></span>

### <a name="definition"></a><span data-ttu-id="319ad-578">Définition</span><span class="sxs-lookup"><span data-stu-id="319ad-578">Definition</span></span>

<span data-ttu-id="319ad-579">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="319ad-579">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="319ad-580">L’expression régulière CEP_Regex_AzurePublishSettingPasswords trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="319ad-580">The regular expression CEP_Regex_AzurePublishSettingPasswords finds content that matches the pattern.</span></span>
- <span data-ttu-id="319ad-581">L’expression régulière CEP_CommonExampleKeywords ne trouve **pas** le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="319ad-581">The regular expression CEP_CommonExampleKeywords does **not** find content that matches the pattern.</span></span>


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

### <a name="keywords"></a><span data-ttu-id="319ad-582">Mots-clés</span><span class="sxs-lookup"><span data-stu-id="319ad-582">Keywords</span></span>

#### <a name="cep_commonexamplekeywords"></a><span data-ttu-id="319ad-583">CEP_CommonExampleKeywords</span><span class="sxs-lookup"><span data-stu-id="319ad-583">CEP_CommonExampleKeywords</span></span>

<span data-ttu-id="319ad-584">(Notez que techniquement, ce type d’informations sensibles identifie ces mots clés à l’aide d’une expression régulière, et non d’une liste de mots clés.)</span><span class="sxs-lookup"><span data-stu-id="319ad-584">(Note that technically, this sensitive information type identifies these keywords by using a regular expression, not a keyword list.)</span></span>

- <span data-ttu-id="319ad-585">contoso</span><span class="sxs-lookup"><span data-stu-id="319ad-585">contoso</span></span>
- <span data-ttu-id="319ad-586">société</span><span class="sxs-lookup"><span data-stu-id="319ad-586">fabrikam</span></span>
- <span data-ttu-id="319ad-587">Northwind</span><span class="sxs-lookup"><span data-stu-id="319ad-587">northwind</span></span>
- <span data-ttu-id="319ad-588">immédiatement</span><span class="sxs-lookup"><span data-stu-id="319ad-588">sandbox</span></span>
- <span data-ttu-id="319ad-589">onebox</span><span class="sxs-lookup"><span data-stu-id="319ad-589">onebox</span></span>
- <span data-ttu-id="319ad-590">hôte</span><span class="sxs-lookup"><span data-stu-id="319ad-590">localhost</span></span>
- <span data-ttu-id="319ad-591">bouclage</span><span class="sxs-lookup"><span data-stu-id="319ad-591">127.0.0.1</span></span>
- <span data-ttu-id="319ad-592">testacs.</span><span class="sxs-lookup"><span data-stu-id="319ad-592">testacs.</span></span><!--no-hyperlink--><span data-ttu-id="319ad-593">com</span><span class="sxs-lookup"><span data-stu-id="319ad-593">com</span></span>
- <span data-ttu-id="319ad-594">s-int.</span><span class="sxs-lookup"><span data-stu-id="319ad-594">s-int.</span></span><!--no-hyperlink--><span data-ttu-id="319ad-595">NET</span><span class="sxs-lookup"><span data-stu-id="319ad-595">net</span></span>

## <a name="azure-redis-cache-connection-string"></a><span data-ttu-id="319ad-596">Chaîne de connexion au cache des inversions Azure</span><span class="sxs-lookup"><span data-stu-id="319ad-596">Azure Redis Cache Connection String</span></span>

### <a name="format"></a><span data-ttu-id="319ad-597">Format</span><span class="sxs-lookup"><span data-stu-id="319ad-597">Format</span></span>

<span data-ttu-id="319ad-598">La chaîne «ReDim. cache. Windows.</span><span class="sxs-lookup"><span data-stu-id="319ad-598">The string "redis.cache.windows.</span></span><!--no-hyperlink--><span data-ttu-id="319ad-599">NET "suivi des caractères et des chaînes décrits dans le modèle ci-dessous, y compris la chaîne" password "ou" PWD ".</span><span class="sxs-lookup"><span data-stu-id="319ad-599">net" followed by the characters and strings outlined in the pattern below, including the string "password" or "pwd".</span></span>

### <a name="pattern"></a><span data-ttu-id="319ad-600">Modèle</span><span class="sxs-lookup"><span data-stu-id="319ad-600">Pattern</span></span>

- <span data-ttu-id="319ad-601">La chaîne «ReDim. cache. Windows.</span><span class="sxs-lookup"><span data-stu-id="319ad-601">The string "redis.cache.windows.</span></span><!--no-hyperlink--><span data-ttu-id="319ad-602">NET</span><span class="sxs-lookup"><span data-stu-id="319ad-602">net"</span></span>
- <span data-ttu-id="319ad-603">N’importe quelle combinaison entre 1-200 majuscules ou minuscules, des chiffres, des symboles, des caractères spéciaux ou des espaces</span><span class="sxs-lookup"><span data-stu-id="319ad-603">Any combination of between 1-200 lower- or uppercase letters, digits, symbols, special characters, or spaces</span></span>
- <span data-ttu-id="319ad-604">La chaîne « password » ou « pwd »</span><span class="sxs-lookup"><span data-stu-id="319ad-604">The string "password" or "pwd"</span></span>
- <span data-ttu-id="319ad-605">0-2 espaces blancs</span><span class="sxs-lookup"><span data-stu-id="319ad-605">0-2 whitespace characters</span></span>
- <span data-ttu-id="319ad-606">Signe égal (=)</span><span class="sxs-lookup"><span data-stu-id="319ad-606">An equal sign (=)</span></span>
- <span data-ttu-id="319ad-607">0-2 espaces blancs</span><span class="sxs-lookup"><span data-stu-id="319ad-607">0-2 whitespace characters</span></span>
- <span data-ttu-id="319ad-608">Toute combinaison de 43 caractères majuscules ou minuscules, des chiffres, une barre oblique (/) ou un signe plus (+)</span><span class="sxs-lookup"><span data-stu-id="319ad-608">Any combination of 43 characters that are lower- or uppercase letters, digits, forward slash (/), or plus sign (+)</span></span>
- <span data-ttu-id="319ad-609">Signe égal (=)</span><span class="sxs-lookup"><span data-stu-id="319ad-609">An equal sign (=)</span></span>

### <a name="checksum"></a><span data-ttu-id="319ad-610">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="319ad-610">Checksum</span></span>

<span data-ttu-id="319ad-611">Non</span><span class="sxs-lookup"><span data-stu-id="319ad-611">No</span></span>

### <a name="definition"></a><span data-ttu-id="319ad-612">Définition</span><span class="sxs-lookup"><span data-stu-id="319ad-612">Definition</span></span>

<span data-ttu-id="319ad-613">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="319ad-613">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="319ad-614">L’expression régulière CEP_Regex_AzureRedisCacheConnectionString trouve le contenu qui correspond au modèle..</span><span class="sxs-lookup"><span data-stu-id="319ad-614">The regular expression CEP_Regex_AzureRedisCacheConnectionString finds content that matches the pattern..</span></span>
- <span data-ttu-id="319ad-615">L’expression régulière CEP_CommonExampleKeywords ne trouve **pas** le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="319ad-615">The regular expression CEP_CommonExampleKeywords does **not** find content that matches the pattern.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="319ad-616">Mots-clés</span><span class="sxs-lookup"><span data-stu-id="319ad-616">Keywords</span></span>

#### <a name="cep_commonexamplekeywords"></a><span data-ttu-id="319ad-617">CEP_CommonExampleKeywords</span><span class="sxs-lookup"><span data-stu-id="319ad-617">CEP_CommonExampleKeywords</span></span>

<span data-ttu-id="319ad-618">(Notez que techniquement, ce type d’informations sensibles identifie ces mots clés à l’aide d’une expression régulière, et non d’une liste de mots clés.)</span><span class="sxs-lookup"><span data-stu-id="319ad-618">(Note that technically, this sensitive information type identifies these keywords by using a regular expression, not a keyword list.)</span></span>

- <span data-ttu-id="319ad-619">contoso</span><span class="sxs-lookup"><span data-stu-id="319ad-619">contoso</span></span>
- <span data-ttu-id="319ad-620">société</span><span class="sxs-lookup"><span data-stu-id="319ad-620">fabrikam</span></span>
- <span data-ttu-id="319ad-621">Northwind</span><span class="sxs-lookup"><span data-stu-id="319ad-621">northwind</span></span>
- <span data-ttu-id="319ad-622">immédiatement</span><span class="sxs-lookup"><span data-stu-id="319ad-622">sandbox</span></span>
- <span data-ttu-id="319ad-623">onebox</span><span class="sxs-lookup"><span data-stu-id="319ad-623">onebox</span></span>
- <span data-ttu-id="319ad-624">hôte</span><span class="sxs-lookup"><span data-stu-id="319ad-624">localhost</span></span>
- <span data-ttu-id="319ad-625">bouclage</span><span class="sxs-lookup"><span data-stu-id="319ad-625">127.0.0.1</span></span>
- <span data-ttu-id="319ad-626">testacs.</span><span class="sxs-lookup"><span data-stu-id="319ad-626">testacs.</span></span><!--no-hyperlink--><span data-ttu-id="319ad-627">com</span><span class="sxs-lookup"><span data-stu-id="319ad-627">com</span></span>
- <span data-ttu-id="319ad-628">s-int.</span><span class="sxs-lookup"><span data-stu-id="319ad-628">s-int.</span></span><!--no-hyperlink--><span data-ttu-id="319ad-629">NET</span><span class="sxs-lookup"><span data-stu-id="319ad-629">net</span></span>

## <a name="azure-sas"></a><span data-ttu-id="319ad-630">SAS Azure</span><span class="sxs-lookup"><span data-stu-id="319ad-630">Azure SAS</span></span>

### <a name="format"></a><span data-ttu-id="319ad-631">Format</span><span class="sxs-lookup"><span data-stu-id="319ad-631">Format</span></span>

<span data-ttu-id="319ad-632">La chaîne « SIG » suivie des caractères et des chaînes présentés dans le modèle ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="319ad-632">The string "sig" followed by the characters and strings outlined in the pattern below.</span></span>

### <a name="pattern"></a><span data-ttu-id="319ad-633">Modèle</span><span class="sxs-lookup"><span data-stu-id="319ad-633">Pattern</span></span>

- <span data-ttu-id="319ad-634">La chaîne « SIG »</span><span class="sxs-lookup"><span data-stu-id="319ad-634">The string "sig"</span></span>
- <span data-ttu-id="319ad-635">0-2 espaces blancs</span><span class="sxs-lookup"><span data-stu-id="319ad-635">0-2 whitespace characters</span></span>
- <span data-ttu-id="319ad-636">Signe égal (=)</span><span class="sxs-lookup"><span data-stu-id="319ad-636">An equal sign (=)</span></span>
- <span data-ttu-id="319ad-637">0-2 espaces blancs</span><span class="sxs-lookup"><span data-stu-id="319ad-637">0-2 whitespace characters</span></span>
- <span data-ttu-id="319ad-638">Toute combinaison comprise entre 43-53 caractères majuscules ou minuscules, des chiffres ou le signe pourcentage (%)</span><span class="sxs-lookup"><span data-stu-id="319ad-638">Any combination of between 43-53 characters that are lower- or uppercase letters, digits, or the percent sign (%)</span></span>
- <span data-ttu-id="319ad-639">La chaîne « % 3D »</span><span class="sxs-lookup"><span data-stu-id="319ad-639">The string "%3d"</span></span>
- <span data-ttu-id="319ad-640">Tout caractère qui n’est pas une lettre majuscule, un chiffre ou un signe de pourcentage (%)</span><span class="sxs-lookup"><span data-stu-id="319ad-640">Any character that is not a lower- or uppercase letter, digit, or percent sign (%)</span></span>

### <a name="checksum"></a><span data-ttu-id="319ad-641">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="319ad-641">Checksum</span></span>

<span data-ttu-id="319ad-642">Non</span><span class="sxs-lookup"><span data-stu-id="319ad-642">No</span></span>

### <a name="definition"></a><span data-ttu-id="319ad-643">Définition</span><span class="sxs-lookup"><span data-stu-id="319ad-643">Definition</span></span>

<span data-ttu-id="319ad-644">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="319ad-644">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="319ad-645">L’expression régulière CEP_Regex_AzureSAS trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="319ad-645">The regular expression CEP_Regex_AzureSAS finds content that matches the pattern.</span></span>

```xml
<!--Azure SAS-->
<Entity id="4d235014-e564-47f4-a6fb-6ebb4a826834" patternsProximity="300" recommendedConfidence="85">
  <Pattern confidenceLevel="85">
        <IdMatch idRef="CEP_Regex_AzureSAS" />
  </Pattern>
</Entity>
```

## <a name="azure-service-bus-connection-string"></a><span data-ttu-id="319ad-646">Chaîne de connexion au bus des services Azure</span><span class="sxs-lookup"><span data-stu-id="319ad-646">Azure Service Bus Connection String</span></span>

### <a name="format"></a><span data-ttu-id="319ad-647">Format</span><span class="sxs-lookup"><span data-stu-id="319ad-647">Format</span></span>

<span data-ttu-id="319ad-648">La chaîne « point de terminaison » suivie des caractères et des chaînes décrits dans le modèle ci-dessous, y compris les chaînes «ServiceBus. Windows.</span><span class="sxs-lookup"><span data-stu-id="319ad-648">The string "EndPoint" followed by the characters and strings outlined in the pattern below, including the strings "servicebus.windows.</span></span><!--no-hyperlink--><span data-ttu-id="319ad-649">NET "et" SharedAccesKey ".</span><span class="sxs-lookup"><span data-stu-id="319ad-649">net" and "SharedAccesKey".</span></span>

### <a name="pattern"></a><span data-ttu-id="319ad-650">Modèle</span><span class="sxs-lookup"><span data-stu-id="319ad-650">Pattern</span></span>

- <span data-ttu-id="319ad-651">Chaîne « point de terminaison »</span><span class="sxs-lookup"><span data-stu-id="319ad-651">The string "EndPoint"</span></span>
- <span data-ttu-id="319ad-652">0-2 espaces blancs</span><span class="sxs-lookup"><span data-stu-id="319ad-652">0-2 whitespace characters</span></span>
- <span data-ttu-id="319ad-653">Signe égal (=)</span><span class="sxs-lookup"><span data-stu-id="319ad-653">An equal sign (=)</span></span>
- <span data-ttu-id="319ad-654">0-2 espaces blancs</span><span class="sxs-lookup"><span data-stu-id="319ad-654">0-2 whitespace characters</span></span>
- <span data-ttu-id="319ad-655">N’importe quelle combinaison entre 1-200 majuscules ou minuscules, des chiffres, des symboles, des caractères spéciaux ou des espaces</span><span class="sxs-lookup"><span data-stu-id="319ad-655">Any combination of between 1-200 lower- or uppercase letters, digits, symbols, special characters, or spaces</span></span>
- <span data-ttu-id="319ad-656">La chaîne «ServiceBus. Windows.</span><span class="sxs-lookup"><span data-stu-id="319ad-656">The string "servicebus.windows.</span></span><!--no-hyperlink--><span data-ttu-id="319ad-657">NET</span><span class="sxs-lookup"><span data-stu-id="319ad-657">net"</span></span>
- <span data-ttu-id="319ad-658">N’importe quelle combinaison entre 1-200 majuscules ou minuscules, des chiffres, des symboles, des caractères spéciaux ou des espaces</span><span class="sxs-lookup"><span data-stu-id="319ad-658">Any combination of between 1-200 lower- or uppercase letters, digits, symbols, special characters, or spaces</span></span>
- <span data-ttu-id="319ad-659">La chaîne « SharedAccessKey »</span><span class="sxs-lookup"><span data-stu-id="319ad-659">The string "SharedAccessKey"</span></span>
- <span data-ttu-id="319ad-660">0-2 espaces blancs</span><span class="sxs-lookup"><span data-stu-id="319ad-660">0-2 whitespace characters</span></span>
- <span data-ttu-id="319ad-661">Signe égal (=)</span><span class="sxs-lookup"><span data-stu-id="319ad-661">An equal sign (=)</span></span>
- <span data-ttu-id="319ad-662">0-2 espaces blancs</span><span class="sxs-lookup"><span data-stu-id="319ad-662">0-2 whitespace characters</span></span>
- <span data-ttu-id="319ad-663">Toute combinaison de 43 caractères majuscules ou minuscules, des chiffres, une barre oblique (/) ou un signe plus (+)</span><span class="sxs-lookup"><span data-stu-id="319ad-663">Any combination of 43 characters that are lower- or uppercase letters, digits, forward slash (/), or plus sign (+)</span></span>
- <span data-ttu-id="319ad-664">Signe égal (=)</span><span class="sxs-lookup"><span data-stu-id="319ad-664">An equal sign (=)</span></span>

### <a name="checksum"></a><span data-ttu-id="319ad-665">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="319ad-665">Checksum</span></span>

<span data-ttu-id="319ad-666">Non</span><span class="sxs-lookup"><span data-stu-id="319ad-666">No</span></span>

### <a name="definition"></a><span data-ttu-id="319ad-667">Définition</span><span class="sxs-lookup"><span data-stu-id="319ad-667">Definition</span></span>

<span data-ttu-id="319ad-668">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="319ad-668">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="319ad-669">L’expression régulière CEP_Regex_AzureServiceBusConnectionString trouve le contenu qui correspond au modèle..</span><span class="sxs-lookup"><span data-stu-id="319ad-669">The regular expression CEP_Regex_AzureServiceBusConnectionString finds content that matches the pattern..</span></span>
- <span data-ttu-id="319ad-670">L’expression régulière CEP_CommonExampleKeywords ne trouve **pas** le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="319ad-670">The regular expression CEP_CommonExampleKeywords does **not** find content that matches the pattern.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="319ad-671">Mots-clés</span><span class="sxs-lookup"><span data-stu-id="319ad-671">Keywords</span></span>

#### <a name="cep_commonexamplekeywords"></a><span data-ttu-id="319ad-672">CEP_CommonExampleKeywords</span><span class="sxs-lookup"><span data-stu-id="319ad-672">CEP_CommonExampleKeywords</span></span>

<span data-ttu-id="319ad-673">(Notez que techniquement, ce type d’informations sensibles identifie ces mots clés à l’aide d’une expression régulière, et non d’une liste de mots clés.)</span><span class="sxs-lookup"><span data-stu-id="319ad-673">(Note that technically, this sensitive information type identifies these keywords by using a regular expression, not a keyword list.)</span></span>

- <span data-ttu-id="319ad-674">contoso</span><span class="sxs-lookup"><span data-stu-id="319ad-674">contoso</span></span>
- <span data-ttu-id="319ad-675">société</span><span class="sxs-lookup"><span data-stu-id="319ad-675">fabrikam</span></span>
- <span data-ttu-id="319ad-676">Northwind</span><span class="sxs-lookup"><span data-stu-id="319ad-676">northwind</span></span>
- <span data-ttu-id="319ad-677">immédiatement</span><span class="sxs-lookup"><span data-stu-id="319ad-677">sandbox</span></span>
- <span data-ttu-id="319ad-678">onebox</span><span class="sxs-lookup"><span data-stu-id="319ad-678">onebox</span></span>
- <span data-ttu-id="319ad-679">hôte</span><span class="sxs-lookup"><span data-stu-id="319ad-679">localhost</span></span>
- <span data-ttu-id="319ad-680">bouclage</span><span class="sxs-lookup"><span data-stu-id="319ad-680">127.0.0.1</span></span>
- <span data-ttu-id="319ad-681">testacs.</span><span class="sxs-lookup"><span data-stu-id="319ad-681">testacs.</span></span><!--no-hyperlink--><span data-ttu-id="319ad-682">com</span><span class="sxs-lookup"><span data-stu-id="319ad-682">com</span></span>
- <span data-ttu-id="319ad-683">s-int.</span><span class="sxs-lookup"><span data-stu-id="319ad-683">s-int.</span></span><!--no-hyperlink--><span data-ttu-id="319ad-684">NET</span><span class="sxs-lookup"><span data-stu-id="319ad-684">net</span></span>

## <a name="azure-storage-account-key"></a><span data-ttu-id="319ad-685">Clé de compte de stockage Azure</span><span class="sxs-lookup"><span data-stu-id="319ad-685">Azure Storage Account Key</span></span>

### <a name="format"></a><span data-ttu-id="319ad-686">Format</span><span class="sxs-lookup"><span data-stu-id="319ad-686">Format</span></span>

<span data-ttu-id="319ad-687">La chaîne « DefaultEndpointsProtocol » suivie des caractères et des chaînes décrits dans le modèle ci-dessous, y compris la chaîne « AccountKey ».</span><span class="sxs-lookup"><span data-stu-id="319ad-687">The string "DefaultEndpointsProtocol" followed by the characters and strings outlined in the pattern below, including the string "AccountKey".</span></span>

### <a name="pattern"></a><span data-ttu-id="319ad-688">Modèle</span><span class="sxs-lookup"><span data-stu-id="319ad-688">Pattern</span></span>

- <span data-ttu-id="319ad-689">La chaîne « DefaultEndpointsProtocol »</span><span class="sxs-lookup"><span data-stu-id="319ad-689">The string "DefaultEndpointsProtocol"</span></span>
- <span data-ttu-id="319ad-690">0-2 espaces blancs</span><span class="sxs-lookup"><span data-stu-id="319ad-690">0-2 whitespace characters</span></span>
- <span data-ttu-id="319ad-691">Signe égal (=)</span><span class="sxs-lookup"><span data-stu-id="319ad-691">An equal sign (=)</span></span>
- <span data-ttu-id="319ad-692">0-2 espaces blancs</span><span class="sxs-lookup"><span data-stu-id="319ad-692">0-2 whitespace characters</span></span>
- <span data-ttu-id="319ad-693">N’importe quelle combinaison entre 1-200 majuscules ou minuscules, des chiffres, des symboles, des caractères spéciaux ou des espaces</span><span class="sxs-lookup"><span data-stu-id="319ad-693">Any combination of between 1-200 lower- or uppercase letters, digits, symbols, special characters, or spaces</span></span>
- <span data-ttu-id="319ad-694">La chaîne « AccountKey »</span><span class="sxs-lookup"><span data-stu-id="319ad-694">The string "AccountKey"</span></span>
- <span data-ttu-id="319ad-695">0-2 espaces blancs</span><span class="sxs-lookup"><span data-stu-id="319ad-695">0-2 whitespace characters</span></span>
- <span data-ttu-id="319ad-696">Signe égal (=)</span><span class="sxs-lookup"><span data-stu-id="319ad-696">An equal sign (=)</span></span>
- <span data-ttu-id="319ad-697">0-2 espaces blancs</span><span class="sxs-lookup"><span data-stu-id="319ad-697">0-2 whitespace characters</span></span>
- <span data-ttu-id="319ad-698">Toute combinaison de 86 caractères majuscules ou minuscules, des chiffres, une barre oblique (/) ou un signe plus (+)</span><span class="sxs-lookup"><span data-stu-id="319ad-698">Any combination of 86 characters that are lower- or uppercase letters, digits, forward slash (/), or plus sign (+)</span></span>
- <span data-ttu-id="319ad-699">Deux signes égal (=)</span><span class="sxs-lookup"><span data-stu-id="319ad-699">Two equal signs (=)</span></span>

### <a name="checksum"></a><span data-ttu-id="319ad-700">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="319ad-700">Checksum</span></span>

<span data-ttu-id="319ad-701">Non</span><span class="sxs-lookup"><span data-stu-id="319ad-701">No</span></span>

### <a name="definition"></a><span data-ttu-id="319ad-702">Définition</span><span class="sxs-lookup"><span data-stu-id="319ad-702">Definition</span></span>

<span data-ttu-id="319ad-703">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="319ad-703">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="319ad-704">L’expression régulière CEP_Regex_AzureStorageAccountKey trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="319ad-704">The regular expression CEP_Regex_AzureStorageAccountKey finds content that matches the pattern.</span></span>
- <span data-ttu-id="319ad-705">L’expression régulière CEP_AzureEmulatorStorageAccountFilter ne trouve **pas** le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="319ad-705">The regular expression CEP_AzureEmulatorStorageAccountFilter does **not** find content that matches the pattern.</span></span>
- <span data-ttu-id="319ad-706">L’expression régulière CEP_CommonExampleKeywords ne trouve **pas** le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="319ad-706">The regular expression CEP_CommonExampleKeywords does **not** find content that matches the pattern.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="319ad-707">Mots-clés</span><span class="sxs-lookup"><span data-stu-id="319ad-707">Keywords</span></span>

#### <a name="cep_azureemulatorstorageaccountfilter"></a><span data-ttu-id="319ad-708">CEP_AzureEmulatorStorageAccountFilter</span><span class="sxs-lookup"><span data-stu-id="319ad-708">CEP_AzureEmulatorStorageAccountFilter</span></span>

<span data-ttu-id="319ad-709">(Notez que techniquement, ce type d’informations sensibles identifie ces mots clés à l’aide d’une expression régulière, et non d’une liste de mots clés.)</span><span class="sxs-lookup"><span data-stu-id="319ad-709">(Note that technically, this sensitive information type identifies these keywords by using a regular expression, not a keyword list.)</span></span>

- <span data-ttu-id="319ad-710">Eby8vdM02xNOcqFlqUwJPLlmEtlCDXJ1OUzFT50uSRZ6IFsuFq2UVErCz4I6tq/K1SZFPTOtr/KBHBeksoGMGw = =</span><span class="sxs-lookup"><span data-stu-id="319ad-710">Eby8vdM02xNOcqFlqUwJPLlmEtlCDXJ1OUzFT50uSRZ6IFsuFq2UVErCz4I6tq/K1SZFPTOtr/KBHBeksoGMGw==</span></span>

#### <a name="cep_commonexamplekeywords"></a><span data-ttu-id="319ad-711">CEP_CommonExampleKeywords</span><span class="sxs-lookup"><span data-stu-id="319ad-711">CEP_CommonExampleKeywords</span></span>

<span data-ttu-id="319ad-712">(Notez que techniquement, ce type d’informations sensibles identifie ces mots clés à l’aide d’une expression régulière, et non d’une liste de mots clés.)</span><span class="sxs-lookup"><span data-stu-id="319ad-712">(Note that technically, this sensitive information type identifies these keywords by using a regular expression, not a keyword list.)</span></span>

- <span data-ttu-id="319ad-713">contoso</span><span class="sxs-lookup"><span data-stu-id="319ad-713">contoso</span></span>
- <span data-ttu-id="319ad-714">société</span><span class="sxs-lookup"><span data-stu-id="319ad-714">fabrikam</span></span>
- <span data-ttu-id="319ad-715">Northwind</span><span class="sxs-lookup"><span data-stu-id="319ad-715">northwind</span></span>
- <span data-ttu-id="319ad-716">immédiatement</span><span class="sxs-lookup"><span data-stu-id="319ad-716">sandbox</span></span>
- <span data-ttu-id="319ad-717">onebox</span><span class="sxs-lookup"><span data-stu-id="319ad-717">onebox</span></span>
- <span data-ttu-id="319ad-718">hôte</span><span class="sxs-lookup"><span data-stu-id="319ad-718">localhost</span></span>
- <span data-ttu-id="319ad-719">bouclage</span><span class="sxs-lookup"><span data-stu-id="319ad-719">127.0.0.1</span></span>
- <span data-ttu-id="319ad-720">testacs.</span><span class="sxs-lookup"><span data-stu-id="319ad-720">testacs.</span></span><!--no-hyperlink--><span data-ttu-id="319ad-721">com</span><span class="sxs-lookup"><span data-stu-id="319ad-721">com</span></span>
- <span data-ttu-id="319ad-722">s-int.</span><span class="sxs-lookup"><span data-stu-id="319ad-722">s-int.</span></span><!--no-hyperlink--><span data-ttu-id="319ad-723">NET</span><span class="sxs-lookup"><span data-stu-id="319ad-723">net</span></span>

## <a name="azure-storage-account-key-generic"></a><span data-ttu-id="319ad-724">Clé de compte de stockage Azure (Générique)</span><span class="sxs-lookup"><span data-stu-id="319ad-724">Azure Storage Account Key (Generic)</span></span>

### <a name="format"></a><span data-ttu-id="319ad-725">Format</span><span class="sxs-lookup"><span data-stu-id="319ad-725">Format</span></span>

<span data-ttu-id="319ad-726">Toute combinaison de 86 lettres majuscules ou minuscules, des chiffres, la barre oblique (/) ou le signe plus (+), précédée ou suivie des caractères décrits dans le modèle ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="319ad-726">Any combination of 86 lower- or uppercase letters, digits, the forward slash (/), or plus sign (+), preceded or followed by the characters outlined in the pattern below.</span></span>

### <a name="pattern"></a><span data-ttu-id="319ad-727">Modèle</span><span class="sxs-lookup"><span data-stu-id="319ad-727">Pattern</span></span>

- <span data-ttu-id="319ad-728">0-1 du symbole supérieur à (>), apostrophe ('), signe égal (=), guillemet (") ou dièse (#)</span><span class="sxs-lookup"><span data-stu-id="319ad-728">0-1 of the greater than symbol (>), apostrophe ('), equal sign (=), quotation mark ("), or number sign (#)</span></span>
- <span data-ttu-id="319ad-729">Toute combinaison de 86 caractères majuscules ou minuscules, des chiffres, la barre oblique (/) ou le signe plus (+)</span><span class="sxs-lookup"><span data-stu-id="319ad-729">Any combination of 86 characters that are lower- or uppercase letters, digits, the forward slash (/), or plus sign (+)</span></span>
- <span data-ttu-id="319ad-730">Deux signes égal (=)</span><span class="sxs-lookup"><span data-stu-id="319ad-730">Two equal signs (=)</span></span>


### <a name="checksum"></a><span data-ttu-id="319ad-731">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="319ad-731">Checksum</span></span>

<span data-ttu-id="319ad-732">Non</span><span class="sxs-lookup"><span data-stu-id="319ad-732">No</span></span>

### <a name="definition"></a><span data-ttu-id="319ad-733">Définition</span><span class="sxs-lookup"><span data-stu-id="319ad-733">Definition</span></span>

<span data-ttu-id="319ad-734">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="319ad-734">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="319ad-735">L’expression régulière CEP_Regex_AzureStorageAccountKeyGeneric trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="319ad-735">The regular expression CEP_Regex_AzureStorageAccountKeyGeneric finds content that matches the pattern.</span></span>

```xml
<!--Azure Storage Account Key (Generic)-->
<Entity id="7ff41bd0-5419-4523-91d6-383b3a37f084" patternsProximity="300" recommendedConfidence="85">
  <Pattern confidenceLevel="85">
        <IdMatch idRef="CEP_Regex_AzureStorageAccountKeyGeneric" />
  </Pattern>
</Entity>
```

## <a name="belgium-national-number"></a><span data-ttu-id="319ad-736">Numéro national Belgique</span><span class="sxs-lookup"><span data-stu-id="319ad-736">Belgium National Number</span></span>

### <a name="format"></a><span data-ttu-id="319ad-737">Format</span><span class="sxs-lookup"><span data-stu-id="319ad-737">Format</span></span>

<span data-ttu-id="319ad-738">11 chiffres plus des délimiteurs</span><span class="sxs-lookup"><span data-stu-id="319ad-738">11 digits plus delimiters</span></span>

### <a name="pattern"></a><span data-ttu-id="319ad-739">Modèle</span><span class="sxs-lookup"><span data-stu-id="319ad-739">Pattern</span></span>

<span data-ttu-id="319ad-740">11 chiffres plus des délimiteurs :</span><span class="sxs-lookup"><span data-stu-id="319ad-740">11 digits plus delimiters:</span></span>
- <span data-ttu-id="319ad-741">Six chiffres et deux points au format AA.MM.JJ pour la date de naissance </span><span class="sxs-lookup"><span data-stu-id="319ad-741">Six digits and two periods in the format YY.MM.DD for date of birth</span></span> 
- <span data-ttu-id="319ad-742">Un trait d’union</span><span class="sxs-lookup"><span data-stu-id="319ad-742">A hyphen</span></span> 
- <span data-ttu-id="319ad-743">Trois chiffres séquentiels (impairs pour les hommes, pairs pour les femmes) </span><span class="sxs-lookup"><span data-stu-id="319ad-743">Three sequential digits (odd for males, even for females)</span></span> 
- <span data-ttu-id="319ad-744">Un point</span><span class="sxs-lookup"><span data-stu-id="319ad-744">A period</span></span> 
- <span data-ttu-id="319ad-745">Deux chiffres de contrôle</span><span class="sxs-lookup"><span data-stu-id="319ad-745">Two digits that are a check digit</span></span>

### <a name="checksum"></a><span data-ttu-id="319ad-746">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="319ad-746">Checksum</span></span>

<span data-ttu-id="319ad-747">Oui</span><span class="sxs-lookup"><span data-stu-id="319ad-747">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="319ad-748">Définition</span><span class="sxs-lookup"><span data-stu-id="319ad-748">Definition</span></span>

<span data-ttu-id="319ad-749">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="319ad-749">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="319ad-750">La fonction Func_belgium_national_number trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="319ad-750">The function Func_belgium_national_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="319ad-751">Un mot clé figurant dans la liste Keyword_belgium_national_number est trouvé.</span><span class="sxs-lookup"><span data-stu-id="319ad-751">A keyword from Keyword_belgium_national_number is found.</span></span>
- <span data-ttu-id="319ad-752">La somme de contrôle est correcte.</span><span class="sxs-lookup"><span data-stu-id="319ad-752">The checksum passes.</span></span>

```xml
<!-- Belgium National Number -->
  <Entity id="fb969c9e-0fd1-4b18-8091-a2123c5e6a54" recommendedConfidence="75" patternsProximity="300">
   <Pattern confidenceLevel="75">
     <IdMatch idRef="Func_belgium_national_number"/>
     <Match idRef="Keyword_belgium_national_number"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="319ad-753">Mots-clés</span><span class="sxs-lookup"><span data-stu-id="319ad-753">Keywords</span></span>

#### <a name="keyword_belgium_national_number"></a><span data-ttu-id="319ad-754">Keyword_belgium_national_number</span><span class="sxs-lookup"><span data-stu-id="319ad-754">Keyword_belgium_national_number</span></span>

- <span data-ttu-id="319ad-755">Identité</span><span class="sxs-lookup"><span data-stu-id="319ad-755">Identity</span></span>
- <span data-ttu-id="319ad-756">Son</span><span class="sxs-lookup"><span data-stu-id="319ad-756">Registration</span></span>
- <span data-ttu-id="319ad-757">Identificateur</span><span class="sxs-lookup"><span data-stu-id="319ad-757">Identification</span></span> 
- <span data-ttu-id="319ad-758">ID</span><span class="sxs-lookup"><span data-stu-id="319ad-758">ID</span></span> 
- <span data-ttu-id="319ad-759">Identiteitskaart</span><span class="sxs-lookup"><span data-stu-id="319ad-759">Identiteitskaart</span></span>
- <span data-ttu-id="319ad-760">Registratie nummer</span><span class="sxs-lookup"><span data-stu-id="319ad-760">Registratie nummer</span></span> 
- <span data-ttu-id="319ad-761">Identificatie nummer</span><span class="sxs-lookup"><span data-stu-id="319ad-761">Identificatie nummer</span></span> 
- <span data-ttu-id="319ad-762">Identiteit</span><span class="sxs-lookup"><span data-stu-id="319ad-762">Identiteit</span></span>
- <span data-ttu-id="319ad-763">Registratie</span><span class="sxs-lookup"><span data-stu-id="319ad-763">Registratie</span></span>
- <span data-ttu-id="319ad-764">Identificatie</span><span class="sxs-lookup"><span data-stu-id="319ad-764">Identificatie</span></span> 
- <span data-ttu-id="319ad-765">Carte d’identité</span><span class="sxs-lookup"><span data-stu-id="319ad-765">Carte d’identité</span></span> 
- <span data-ttu-id="319ad-766">numéro d’immatriculation</span><span class="sxs-lookup"><span data-stu-id="319ad-766">numéro d'immatriculation</span></span>
- <span data-ttu-id="319ad-767">numéro d’identification</span><span class="sxs-lookup"><span data-stu-id="319ad-767">numéro d'identification</span></span>
- <span data-ttu-id="319ad-768">identité</span><span class="sxs-lookup"><span data-stu-id="319ad-768">identité</span></span> 
- <span data-ttu-id="319ad-769">inscriptions</span><span class="sxs-lookup"><span data-stu-id="319ad-769">inscription</span></span> 
- <span data-ttu-id="319ad-770">Identifikation</span><span class="sxs-lookup"><span data-stu-id="319ad-770">Identifikation</span></span>
- <span data-ttu-id="319ad-771">Identifizierung</span><span class="sxs-lookup"><span data-stu-id="319ad-771">Identifizierung</span></span>
- <span data-ttu-id="319ad-772">Identifikationsnummer</span><span class="sxs-lookup"><span data-stu-id="319ad-772">Identifikationsnummer</span></span>
- <span data-ttu-id="319ad-773">Personalausweis</span><span class="sxs-lookup"><span data-stu-id="319ad-773">Personalausweis</span></span>
- <span data-ttu-id="319ad-774">Registrierung</span><span class="sxs-lookup"><span data-stu-id="319ad-774">Registrierung</span></span>
- <span data-ttu-id="319ad-775">Registrationsnummer</span><span class="sxs-lookup"><span data-stu-id="319ad-775">Registrationsnummer</span></span>

   
## <a name="brazil-cpf-number"></a><span data-ttu-id="319ad-776">Numéro CPF Brésil</span><span class="sxs-lookup"><span data-stu-id="319ad-776">Brazil CPF Number</span></span>

### <a name="format"></a><span data-ttu-id="319ad-777">Format</span><span class="sxs-lookup"><span data-stu-id="319ad-777">Format</span></span>

<span data-ttu-id="319ad-778">11 chiffres qui incluent un chiffre de contrôle et peuvent ou non être mis en forme </span><span class="sxs-lookup"><span data-stu-id="319ad-778">11 digits that include a check digit and can be formatted or unformatted</span></span>

### <a name="pattern"></a><span data-ttu-id="319ad-779">Modèle</span><span class="sxs-lookup"><span data-stu-id="319ad-779">Pattern</span></span>

<span data-ttu-id="319ad-780">Avec</span><span class="sxs-lookup"><span data-stu-id="319ad-780">Formatted:</span></span>
- <span data-ttu-id="319ad-781">Trois chiffres</span><span class="sxs-lookup"><span data-stu-id="319ad-781">Three digits</span></span> 
- <span data-ttu-id="319ad-782">Un point </span><span class="sxs-lookup"><span data-stu-id="319ad-782">A period</span></span> 
- <span data-ttu-id="319ad-783">Trois chiffres</span><span class="sxs-lookup"><span data-stu-id="319ad-783">Three digits</span></span> 
- <span data-ttu-id="319ad-784">Un point </span><span class="sxs-lookup"><span data-stu-id="319ad-784">A period</span></span> 
- <span data-ttu-id="319ad-785">Trois chiffres</span><span class="sxs-lookup"><span data-stu-id="319ad-785">Three digits</span></span> 
- <span data-ttu-id="319ad-786">Un trait d’union </span><span class="sxs-lookup"><span data-stu-id="319ad-786">A hyphen</span></span> 
- <span data-ttu-id="319ad-787">Deux chiffres de contrôle</span><span class="sxs-lookup"><span data-stu-id="319ad-787">Two digits which are check digits</span></span>

<span data-ttu-id="319ad-788">Non</span><span class="sxs-lookup"><span data-stu-id="319ad-788">Unformatted:</span></span>
- <span data-ttu-id="319ad-789">11 chiffres où les deux derniers sont des chiffres de contrôle</span><span class="sxs-lookup"><span data-stu-id="319ad-789">11 digits where the last two digits are check digits</span></span>

### <a name="checksum"></a><span data-ttu-id="319ad-790">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="319ad-790">Checksum</span></span>

<span data-ttu-id="319ad-791">Oui</span><span class="sxs-lookup"><span data-stu-id="319ad-791">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="319ad-792">Définition</span><span class="sxs-lookup"><span data-stu-id="319ad-792">Definition</span></span>

<span data-ttu-id="319ad-793">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="319ad-793">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="319ad-794">La fonction Func_brazil_cpf trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="319ad-794">The function Func_brazil_cpf finds content that matches the pattern.</span></span>
- <span data-ttu-id="319ad-795">Un mot clé figurant dans la liste Keyword_brazil_cpf est trouvé.</span><span class="sxs-lookup"><span data-stu-id="319ad-795">A keyword from Keyword_brazil_cpf is found.</span></span>
- <span data-ttu-id="319ad-796">La somme de contrôle est correcte.</span><span class="sxs-lookup"><span data-stu-id="319ad-796">The checksum passes.</span></span>

<span data-ttu-id="319ad-797">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="319ad-797">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="319ad-798">La fonction Func_brazil_cpf trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="319ad-798">The function Func_brazil_cpf finds content that matches the pattern.</span></span>
- <span data-ttu-id="319ad-799">La somme de contrôle est correcte.</span><span class="sxs-lookup"><span data-stu-id="319ad-799">The checksum passes.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="319ad-800">Mots-clés</span><span class="sxs-lookup"><span data-stu-id="319ad-800">Keywords</span></span>

#### <a name="keyword_brazil_cpf"></a><span data-ttu-id="319ad-801">Keyword_brazil_cpf</span><span class="sxs-lookup"><span data-stu-id="319ad-801">Keyword_brazil_cpf</span></span>

- <span data-ttu-id="319ad-802">CPF</span><span class="sxs-lookup"><span data-stu-id="319ad-802">CPF</span></span>
- <span data-ttu-id="319ad-803">Identificateur</span><span class="sxs-lookup"><span data-stu-id="319ad-803">Identification</span></span>
- <span data-ttu-id="319ad-804">Son</span><span class="sxs-lookup"><span data-stu-id="319ad-804">Registration</span></span>
- <span data-ttu-id="319ad-805">Parts</span><span class="sxs-lookup"><span data-stu-id="319ad-805">Revenue</span></span>
- <span data-ttu-id="319ad-806">Cadastro de Pessoas Físicas</span><span class="sxs-lookup"><span data-stu-id="319ad-806">Cadastro de Pessoas Físicas</span></span> 
- <span data-ttu-id="319ad-807">Imposto</span><span class="sxs-lookup"><span data-stu-id="319ad-807">Imposto</span></span> 
- <span data-ttu-id="319ad-808">Identificação</span><span class="sxs-lookup"><span data-stu-id="319ad-808">Identificação</span></span> 
- <span data-ttu-id="319ad-809">Inscrição</span><span class="sxs-lookup"><span data-stu-id="319ad-809">Inscrição</span></span> 
- <span data-ttu-id="319ad-810">Receita</span><span class="sxs-lookup"><span data-stu-id="319ad-810">Receita</span></span> 
   
## <a name="brazil-legal-entity-number-cnpj"></a><span data-ttu-id="319ad-811">Numéro d’entité juridique (CNPJ) Brésil</span><span class="sxs-lookup"><span data-stu-id="319ad-811">Brazil Legal Entity Number (CNPJ)</span></span>

### <a name="format"></a><span data-ttu-id="319ad-812">Format</span><span class="sxs-lookup"><span data-stu-id="319ad-812">Format</span></span>

<span data-ttu-id="319ad-813">14 chiffres qui incluent un numéro d’enregistrement, un numéro de succursale et des chiffres de contrôle, avec des délimiteurs en plus</span><span class="sxs-lookup"><span data-stu-id="319ad-813">14 digits that include a registration number, branch number, and check digits, plus delimiters</span></span>

### <a name="pattern"></a><span data-ttu-id="319ad-814">Modèle</span><span class="sxs-lookup"><span data-stu-id="319ad-814">Pattern</span></span>
<span data-ttu-id="319ad-815">14 chiffres plus des délimiteurs :</span><span class="sxs-lookup"><span data-stu-id="319ad-815">14 digits, plus delimiters:</span></span>
- <span data-ttu-id="319ad-816">Deux chiffres</span><span class="sxs-lookup"><span data-stu-id="319ad-816">Two digits</span></span> 
- <span data-ttu-id="319ad-817">Un point </span><span class="sxs-lookup"><span data-stu-id="319ad-817">A period</span></span> 
- <span data-ttu-id="319ad-818">Trois chiffres</span><span class="sxs-lookup"><span data-stu-id="319ad-818">Three digits</span></span> 
- <span data-ttu-id="319ad-819">Un point </span><span class="sxs-lookup"><span data-stu-id="319ad-819">A period</span></span> 
- <span data-ttu-id="319ad-820">Trois chiffres (ces huit premiers chiffres composent le numéro d’enregistrement) </span><span class="sxs-lookup"><span data-stu-id="319ad-820">Three digits (these first eight digits are the registration number)</span></span> 
- <span data-ttu-id="319ad-821">Une barre oblique </span><span class="sxs-lookup"><span data-stu-id="319ad-821">A forward slash</span></span> 
- <span data-ttu-id="319ad-822">Le numéro de succursale à quatre chiffres </span><span class="sxs-lookup"><span data-stu-id="319ad-822">Four-digit branch number</span></span> 
- <span data-ttu-id="319ad-823">Un trait d’union </span><span class="sxs-lookup"><span data-stu-id="319ad-823">A hyphen</span></span> 
- <span data-ttu-id="319ad-824">Deux chiffres de contrôle</span><span class="sxs-lookup"><span data-stu-id="319ad-824">Two digits which are check digits</span></span>

### <a name="checksum"></a><span data-ttu-id="319ad-825">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="319ad-825">Checksum</span></span>

<span data-ttu-id="319ad-826">Oui</span><span class="sxs-lookup"><span data-stu-id="319ad-826">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="319ad-827">Définition</span><span class="sxs-lookup"><span data-stu-id="319ad-827">Definition</span></span>

<span data-ttu-id="319ad-828">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="319ad-828">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="319ad-829">La fonction Func_brazil_cnpj trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="319ad-829">The function Func_brazil_cnpj finds content that matches the pattern.</span></span>
- <span data-ttu-id="319ad-830">Un mot clé figurant dans la liste Keyword_brazil_cnpj est trouvé.</span><span class="sxs-lookup"><span data-stu-id="319ad-830">A keyword from Keyword_brazil_cnpj is found.</span></span>
- <span data-ttu-id="319ad-831">La somme de contrôle est correcte.</span><span class="sxs-lookup"><span data-stu-id="319ad-831">The checksum passes.</span></span>

<span data-ttu-id="319ad-832">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="319ad-832">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="319ad-833">La fonction Func_brazil_cnpj trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="319ad-833">The function Func_brazil_cnpj finds content that matches the pattern.</span></span>
- <span data-ttu-id="319ad-834">La somme de contrôle est correcte.</span><span class="sxs-lookup"><span data-stu-id="319ad-834">The checksum passes.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="319ad-835">Mots-clés</span><span class="sxs-lookup"><span data-stu-id="319ad-835">Keywords</span></span>

#### <a name="keyword_brazil_cnpj"></a><span data-ttu-id="319ad-836">Keyword_brazil_cnpj</span><span class="sxs-lookup"><span data-stu-id="319ad-836">Keyword_brazil_cnpj</span></span>

- <span data-ttu-id="319ad-837">CNPJ</span><span class="sxs-lookup"><span data-stu-id="319ad-837">CNPJ</span></span> 
- <span data-ttu-id="319ad-838">CNPJ/MF</span><span class="sxs-lookup"><span data-stu-id="319ad-838">CNPJ/MF</span></span> 
- <span data-ttu-id="319ad-839">CNPJ-MF</span><span class="sxs-lookup"><span data-stu-id="319ad-839">CNPJ-MF</span></span> 
- <span data-ttu-id="319ad-840">National Registry of Legal Entities</span><span class="sxs-lookup"><span data-stu-id="319ad-840">National Registry of Legal Entities</span></span> 
- <span data-ttu-id="319ad-841">Taxpayers Registry</span><span class="sxs-lookup"><span data-stu-id="319ad-841">Taxpayers Registry</span></span> 
- <span data-ttu-id="319ad-842">Legal entity</span><span class="sxs-lookup"><span data-stu-id="319ad-842">Legal entity</span></span> 
- <span data-ttu-id="319ad-843">Legal entities</span><span class="sxs-lookup"><span data-stu-id="319ad-843">Legal entities</span></span> 
- <span data-ttu-id="319ad-844">Registration Status</span><span class="sxs-lookup"><span data-stu-id="319ad-844">Registration Status</span></span> 
- <span data-ttu-id="319ad-845">Business</span><span class="sxs-lookup"><span data-stu-id="319ad-845">Business</span></span> 
- <span data-ttu-id="319ad-846">Company</span><span class="sxs-lookup"><span data-stu-id="319ad-846">Company</span></span>
- <span data-ttu-id="319ad-847">CNPJ</span><span class="sxs-lookup"><span data-stu-id="319ad-847">CNPJ</span></span> 
- <span data-ttu-id="319ad-848">Cadastro Nacional da Pessoa Jurídica</span><span class="sxs-lookup"><span data-stu-id="319ad-848">Cadastro Nacional da Pessoa Jurídica</span></span> 
- <span data-ttu-id="319ad-849">Cadastro Geral de Contribuintes</span><span class="sxs-lookup"><span data-stu-id="319ad-849">Cadastro Geral de Contribuintes</span></span> 
- <span data-ttu-id="319ad-850">CGC</span><span class="sxs-lookup"><span data-stu-id="319ad-850">CGC</span></span> 
- <span data-ttu-id="319ad-851">Pessoa jurídica</span><span class="sxs-lookup"><span data-stu-id="319ad-851">Pessoa jurídica</span></span> 
- <span data-ttu-id="319ad-852">Pessoas jurídicas</span><span class="sxs-lookup"><span data-stu-id="319ad-852">Pessoas jurídicas</span></span> 
- <span data-ttu-id="319ad-853">Situação cadastral</span><span class="sxs-lookup"><span data-stu-id="319ad-853">Situação cadastral</span></span> 
- <span data-ttu-id="319ad-854">Inscrição</span><span class="sxs-lookup"><span data-stu-id="319ad-854">Inscrição</span></span> 
- <span data-ttu-id="319ad-855">Empresa</span><span class="sxs-lookup"><span data-stu-id="319ad-855">Empresa</span></span> 
   
## <a name="brazil-national-id-card-rg"></a><span data-ttu-id="319ad-856">	Brazil National ID Card (RG)</span><span class="sxs-lookup"><span data-stu-id="319ad-856">Brazil National ID Card (RG)</span></span>

### <a name="format"></a><span data-ttu-id="319ad-857">Format</span><span class="sxs-lookup"><span data-stu-id="319ad-857">Format</span></span>

<span data-ttu-id="319ad-858">Registro Geral (ancien format) : neuf chiffres</span><span class="sxs-lookup"><span data-stu-id="319ad-858">Registro Geral (old format): Nine digits</span></span>

<span data-ttu-id="319ad-859">Registro de identidade (RIC) (nouveau format) : 11 chiffres</span><span class="sxs-lookup"><span data-stu-id="319ad-859">Registro de Identidade (RIC) (new format): 11 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="319ad-860">Modèle</span><span class="sxs-lookup"><span data-stu-id="319ad-860">Pattern</span></span>

<span data-ttu-id="319ad-861">Registro Geral (ancien format) :</span><span class="sxs-lookup"><span data-stu-id="319ad-861">Registro Geral (old format):</span></span>
- <span data-ttu-id="319ad-862">Deux chiffres</span><span class="sxs-lookup"><span data-stu-id="319ad-862">Two digits</span></span> 
- <span data-ttu-id="319ad-863">Un point </span><span class="sxs-lookup"><span data-stu-id="319ad-863">A period</span></span> 
- <span data-ttu-id="319ad-864">Trois chiffres</span><span class="sxs-lookup"><span data-stu-id="319ad-864">Three digits</span></span> 
- <span data-ttu-id="319ad-865">Un point </span><span class="sxs-lookup"><span data-stu-id="319ad-865">A period</span></span> 
- <span data-ttu-id="319ad-866">Trois chiffres</span><span class="sxs-lookup"><span data-stu-id="319ad-866">Three digits</span></span> 
- <span data-ttu-id="319ad-867">Un trait d’union </span><span class="sxs-lookup"><span data-stu-id="319ad-867">A hyphen</span></span> 
- <span data-ttu-id="319ad-868">Un chiffre de contrôle</span><span class="sxs-lookup"><span data-stu-id="319ad-868">One digit which is a check digit</span></span>

<span data-ttu-id="319ad-869">Registro de identidade (RIC) (nouveau format) :</span><span class="sxs-lookup"><span data-stu-id="319ad-869">Registro de Identidade (RIC) (new format):</span></span>
- <span data-ttu-id="319ad-870">10 chiffres</span><span class="sxs-lookup"><span data-stu-id="319ad-870">10 digits</span></span> 
- <span data-ttu-id="319ad-871">Un trait d’union </span><span class="sxs-lookup"><span data-stu-id="319ad-871">A hyphen</span></span> 
- <span data-ttu-id="319ad-872">Un chiffre de contrôle</span><span class="sxs-lookup"><span data-stu-id="319ad-872">One digit which is a check digit</span></span>

### <a name="checksum"></a><span data-ttu-id="319ad-873">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="319ad-873">Checksum</span></span>

<span data-ttu-id="319ad-874">Oui</span><span class="sxs-lookup"><span data-stu-id="319ad-874">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="319ad-875">Définition</span><span class="sxs-lookup"><span data-stu-id="319ad-875">Definition</span></span>

<span data-ttu-id="319ad-876">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="319ad-876">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="319ad-877">La fonction Func_brazil_rg trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="319ad-877">The function Func_brazil_rg finds content that matches the pattern.</span></span>
- <span data-ttu-id="319ad-878">Un mot clé figurant dans la liste Keyword_brazil_rg est trouvé.</span><span class="sxs-lookup"><span data-stu-id="319ad-878">A keyword from Keyword_brazil_rg is found.</span></span>
- <span data-ttu-id="319ad-879">La somme de contrôle est correcte.</span><span class="sxs-lookup"><span data-stu-id="319ad-879">The checksum passes.</span></span>

<span data-ttu-id="319ad-880">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="319ad-880">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="319ad-881">La fonction Func_brazil_rg trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="319ad-881">The function Func_brazil_rg finds content that matches the pattern.</span></span>
- <span data-ttu-id="319ad-882">La somme de contrôle est correcte.</span><span class="sxs-lookup"><span data-stu-id="319ad-882">The checksum passes.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="319ad-883">Mots-clés</span><span class="sxs-lookup"><span data-stu-id="319ad-883">Keywords</span></span>

#### <a name="keyword_brazil_rg"></a><span data-ttu-id="319ad-884">Keyword_brazil_rg</span><span class="sxs-lookup"><span data-stu-id="319ad-884">Keyword_brazil_rg</span></span>

<span data-ttu-id="319ad-885">Cédula de identidade carte d’identité número de rregistro Registro de identidade Registro Geral RG (ce mot clé respecte la casse) RIC (ce mot clé respecte la casse)</span><span class="sxs-lookup"><span data-stu-id="319ad-885">Cédula de identidade identity card national id número de rregistro registro de Iidentidade registro geral RG (this keyword is case sensitive) RIC (this keyword is case sensitive)</span></span> 
   
## <a name="canada-bank-account-number"></a><span data-ttu-id="319ad-886">Numéro de compte bancaire Canada</span><span class="sxs-lookup"><span data-stu-id="319ad-886">Canada Bank Account Number</span></span>

### <a name="format"></a><span data-ttu-id="319ad-887">Format</span><span class="sxs-lookup"><span data-stu-id="319ad-887">Format</span></span>

<span data-ttu-id="319ad-888">Sept ou douze chiffres</span><span class="sxs-lookup"><span data-stu-id="319ad-888">Seven or twelve digits</span></span>

### <a name="pattern"></a><span data-ttu-id="319ad-889">Modèle</span><span class="sxs-lookup"><span data-stu-id="319ad-889">Pattern</span></span>

<span data-ttu-id="319ad-890">Un numéro de compte bancaire au Canada est composé de sept ou douze chiffres.</span><span class="sxs-lookup"><span data-stu-id="319ad-890">A Canada Bank Account Number is seven or twelve digits.</span></span>

<span data-ttu-id="319ad-891">Un numéro de transit de compte bancaire du Canada est indiqué au format suivant :</span><span class="sxs-lookup"><span data-stu-id="319ad-891">A Canada bank account transit number is:</span></span>
- <span data-ttu-id="319ad-892">Cinq chiffres</span><span class="sxs-lookup"><span data-stu-id="319ad-892">Five digits</span></span> 
- <span data-ttu-id="319ad-893">Un trait d’union </span><span class="sxs-lookup"><span data-stu-id="319ad-893">A hyphen</span></span> 
- <span data-ttu-id="319ad-894">Trois chiffres ou</span><span class="sxs-lookup"><span data-stu-id="319ad-894">Three digits OR</span></span>
- <span data-ttu-id="319ad-895">Un zéro « 0 » </span><span class="sxs-lookup"><span data-stu-id="319ad-895">A zero "0"</span></span> 
- <span data-ttu-id="319ad-896">Huit chiffres</span><span class="sxs-lookup"><span data-stu-id="319ad-896">Eight digits</span></span>

### <a name="checksum"></a><span data-ttu-id="319ad-897">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="319ad-897">Checksum</span></span>

<span data-ttu-id="319ad-898">Non</span><span class="sxs-lookup"><span data-stu-id="319ad-898">No</span></span>

### <a name="definition"></a><span data-ttu-id="319ad-899">Définition</span><span class="sxs-lookup"><span data-stu-id="319ad-899">Definition</span></span>

<span data-ttu-id="319ad-900">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="319ad-900">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="319ad-901">L’expression régulière Regex_canada_bank_account_number trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="319ad-901">The regular expression Regex_canada_bank_account_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="319ad-902">Un mot clé figurant dans la liste Keyword_canada_bank_account_number est trouvé.</span><span class="sxs-lookup"><span data-stu-id="319ad-902">A keyword from Keyword_canada_bank_account_number is found.</span></span>
- <span data-ttu-id="319ad-903">L’expression régulière Regex_canada_bank_account_transit_number trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="319ad-903">The regular expression Regex_canada_bank_account_transit_number finds content that matches the pattern.</span></span>

<span data-ttu-id="319ad-904">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="319ad-904">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="319ad-905">L’expression régulière Regex_canada_bank_account_number trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="319ad-905">The regular expression Regex_canada_bank_account_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="319ad-906">Un mot clé figurant dans la liste Keyword_canada_bank_account_number est trouvé.</span><span class="sxs-lookup"><span data-stu-id="319ad-906">A keyword from Keyword_canada_bank_account_number is found.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="319ad-907">Mots-clés</span><span class="sxs-lookup"><span data-stu-id="319ad-907">Keywords</span></span>

#### <a name="keyword_canada_bank_account_number"></a><span data-ttu-id="319ad-908">Keyword_canada_bank_account_number</span><span class="sxs-lookup"><span data-stu-id="319ad-908">Keyword_canada_bank_account_number</span></span>

- <span data-ttu-id="319ad-909">obligations d’épargne du Canada</span><span class="sxs-lookup"><span data-stu-id="319ad-909">canada savings bonds</span></span>
- <span data-ttu-id="319ad-910">agence du revenu du Canada</span><span class="sxs-lookup"><span data-stu-id="319ad-910">canada revenue agency</span></span>
- <span data-ttu-id="319ad-911">institution financière du Canada</span><span class="sxs-lookup"><span data-stu-id="319ad-911">canadian financial institution</span></span>
- <span data-ttu-id="319ad-912">formulaire de dépôt direct</span><span class="sxs-lookup"><span data-stu-id="319ad-912">direct deposit form</span></span>
- <span data-ttu-id="319ad-913">citoyen canadien</span><span class="sxs-lookup"><span data-stu-id="319ad-913">canadian citizen</span></span>
- <span data-ttu-id="319ad-914">représentant légal</span><span class="sxs-lookup"><span data-stu-id="319ad-914">legal representative</span></span>
- <span data-ttu-id="319ad-915">notaire</span><span class="sxs-lookup"><span data-stu-id="319ad-915">notary public</span></span>
- <span data-ttu-id="319ad-916">commissaire à l’assermentation</span><span class="sxs-lookup"><span data-stu-id="319ad-916">commissioner for oaths</span></span>
- <span data-ttu-id="319ad-917">prestation pour la garde d’enfants</span><span class="sxs-lookup"><span data-stu-id="319ad-917">child care benefit</span></span>
- <span data-ttu-id="319ad-918">prestation universelle pour la garde d’enfants</span><span class="sxs-lookup"><span data-stu-id="319ad-918">universal child care</span></span>
- <span data-ttu-id="319ad-919">prestation fiscale canadienne pour enfants</span><span class="sxs-lookup"><span data-stu-id="319ad-919">canada child tax benefit</span></span>
- <span data-ttu-id="319ad-920">prestation fiscale pour le revenu gagné</span><span class="sxs-lookup"><span data-stu-id="319ad-920">income tax benefit</span></span>
- <span data-ttu-id="319ad-921">taxe de vente harmonisée</span><span class="sxs-lookup"><span data-stu-id="319ad-921">harmonized sales tax</span></span>
- <span data-ttu-id="319ad-922">numéro d’assurance sociale</span><span class="sxs-lookup"><span data-stu-id="319ad-922">social insurance number</span></span>
- <span data-ttu-id="319ad-923">remboursement d’impôt</span><span class="sxs-lookup"><span data-stu-id="319ad-923">income tax refund</span></span>
- <span data-ttu-id="319ad-924">prestation fiscale pour enfants</span><span class="sxs-lookup"><span data-stu-id="319ad-924">child tax benefit</span></span>
- <span data-ttu-id="319ad-925">paiements aux territoires</span><span class="sxs-lookup"><span data-stu-id="319ad-925">territorial payments</span></span>
- <span data-ttu-id="319ad-926">numéro d’institution</span><span class="sxs-lookup"><span data-stu-id="319ad-926">institution number</span></span>
- <span data-ttu-id="319ad-927">demande de dépôt</span><span class="sxs-lookup"><span data-stu-id="319ad-927">deposit request</span></span>
- <span data-ttu-id="319ad-928">informations bancaires</span><span class="sxs-lookup"><span data-stu-id="319ad-928">banking information</span></span>
- <span data-ttu-id="319ad-929">dépôt direct</span><span class="sxs-lookup"><span data-stu-id="319ad-929">direct deposit</span></span>
   
## <a name="canada-drivers-license-number"></a><span data-ttu-id="319ad-930">Numéro de permis de conduire Canada</span><span class="sxs-lookup"><span data-stu-id="319ad-930">Canada Driver's License Number</span></span>

### <a name="format"></a><span data-ttu-id="319ad-931">Format</span><span class="sxs-lookup"><span data-stu-id="319ad-931">Format</span></span>

<span data-ttu-id="319ad-932">Varie selon la province</span><span class="sxs-lookup"><span data-stu-id="319ad-932">Varies by province</span></span>

### <a name="pattern"></a><span data-ttu-id="319ad-933">Modèle</span><span class="sxs-lookup"><span data-stu-id="319ad-933">Pattern</span></span>

<span data-ttu-id="319ad-934">Plusieurs modèles pour les différentes provinces : Alberta, Colombie-Britannique, Manitoba, Nouveau-Brunswick, Terre-Neuve-et-Labrador, Nouvelle-Écosse, Ontario, Île-du-Prince-Édouard, Québec et Saskatchewan</span><span class="sxs-lookup"><span data-stu-id="319ad-934">Various patterns covering Alberta, British Columbia, Manitoba, New Brunswick, Newfoundland/Labrador, Nova Scotia, Ontario, Prince Edward Island, Quebec, and Saskatchewan</span></span>

### <a name="checksum"></a><span data-ttu-id="319ad-935">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="319ad-935">Checksum</span></span>

<span data-ttu-id="319ad-936">Non</span><span class="sxs-lookup"><span data-stu-id="319ad-936">No</span></span>

### <a name="definition"></a><span data-ttu-id="319ad-937">Définition</span><span class="sxs-lookup"><span data-stu-id="319ad-937">Definition</span></span>

<span data-ttu-id="319ad-938">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="319ad-938">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="319ad-939">La fonction Func_[province_name]_drivers_license_number trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="319ad-939">The function Func_[province_name]_drivers_license_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="319ad-940">Un mot clé figurant dans la liste Keyword_[province_name]_drivers_license_name est trouvé.</span><span class="sxs-lookup"><span data-stu-id="319ad-940">A keyword from Keyword_[province_name]_drivers_license_name is found.</span></span>
- <span data-ttu-id="319ad-941">Un mot clé figurant dans la liste Keyword_canada_drivers_license est trouvé.</span><span class="sxs-lookup"><span data-stu-id="319ad-941">A keyword from Keyword_canada_drivers_license is found.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="319ad-942">Mots-clés</span><span class="sxs-lookup"><span data-stu-id="319ad-942">Keywords</span></span>

#### <a name="keyword_province_name_drivers_license_name"></a><span data-ttu-id="319ad-943">Keyword_ [province_name] _drivers_license_name</span><span class="sxs-lookup"><span data-stu-id="319ad-943">Keyword_[province_name]_drivers_license_name</span></span>

- <span data-ttu-id="319ad-944">L’abréviation de la province, par exemple AB</span><span class="sxs-lookup"><span data-stu-id="319ad-944">The province abbreviation, for example AB</span></span>
- <span data-ttu-id="319ad-945">Le nom de la province, par exemple Alberta</span><span class="sxs-lookup"><span data-stu-id="319ad-945">The province name, for example Alberta</span></span>

#### <a name="keyword_canada_drivers_license"></a><span data-ttu-id="319ad-946">Keyword_canada_drivers_license</span><span class="sxs-lookup"><span data-stu-id="319ad-946">Keyword_canada_drivers_license</span></span>

- <span data-ttu-id="319ad-947">LD</span><span class="sxs-lookup"><span data-stu-id="319ad-947">DL</span></span>
- <span data-ttu-id="319ad-948">DISTRIBUTION</span><span class="sxs-lookup"><span data-stu-id="319ad-948">DLS</span></span>
- <span data-ttu-id="319ad-949">CÈDE</span><span class="sxs-lookup"><span data-stu-id="319ad-949">CDL</span></span>
- <span data-ttu-id="319ad-950">CDLS</span><span class="sxs-lookup"><span data-stu-id="319ad-950">CDLS</span></span>
- <span data-ttu-id="319ad-951">DriverLic</span><span class="sxs-lookup"><span data-stu-id="319ad-951">DriverLic</span></span>
- <span data-ttu-id="319ad-952">DriverLics</span><span class="sxs-lookup"><span data-stu-id="319ad-952">DriverLics</span></span>
- <span data-ttu-id="319ad-953">DriverLicense</span><span class="sxs-lookup"><span data-stu-id="319ad-953">DriverLicense</span></span>
- <span data-ttu-id="319ad-954">DriverLicenses</span><span class="sxs-lookup"><span data-stu-id="319ad-954">DriverLicenses</span></span>
- <span data-ttu-id="319ad-955">DriverLicence</span><span class="sxs-lookup"><span data-stu-id="319ad-955">DriverLicence</span></span>
- <span data-ttu-id="319ad-956">DriverLicences</span><span class="sxs-lookup"><span data-stu-id="319ad-956">DriverLicences</span></span>
- <span data-ttu-id="319ad-957">Permis conduire</span><span class="sxs-lookup"><span data-stu-id="319ad-957">Driver Lic</span></span>
- <span data-ttu-id="319ad-958">Permis conduire</span><span class="sxs-lookup"><span data-stu-id="319ad-958">Driver Lics</span></span>
- <span data-ttu-id="319ad-959">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="319ad-959">Driver License</span></span>
- <span data-ttu-id="319ad-960">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="319ad-960">Driver Licenses</span></span>
- <span data-ttu-id="319ad-961">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="319ad-961">Driver Licence</span></span>
- <span data-ttu-id="319ad-962">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="319ad-962">Driver Licences</span></span>
- <span data-ttu-id="319ad-963">DriversLic</span><span class="sxs-lookup"><span data-stu-id="319ad-963">DriversLic</span></span>
- <span data-ttu-id="319ad-964">DriversLics</span><span class="sxs-lookup"><span data-stu-id="319ad-964">DriversLics</span></span>
- <span data-ttu-id="319ad-965">DriversLicence</span><span class="sxs-lookup"><span data-stu-id="319ad-965">DriversLicence</span></span>
- <span data-ttu-id="319ad-966">DriversLicences</span><span class="sxs-lookup"><span data-stu-id="319ad-966">DriversLicences</span></span>
- <span data-ttu-id="319ad-967">DriversLicense</span><span class="sxs-lookup"><span data-stu-id="319ad-967">DriversLicense</span></span>
- <span data-ttu-id="319ad-968">DriversLicenses</span><span class="sxs-lookup"><span data-stu-id="319ad-968">DriversLicenses</span></span>
- <span data-ttu-id="319ad-969">Permis conduire</span><span class="sxs-lookup"><span data-stu-id="319ad-969">Drivers Lic</span></span>
- <span data-ttu-id="319ad-970">Permis conduire</span><span class="sxs-lookup"><span data-stu-id="319ad-970">Drivers Lics</span></span>
- <span data-ttu-id="319ad-971">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="319ad-971">Drivers License</span></span>
- <span data-ttu-id="319ad-972">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="319ad-972">Drivers Licenses</span></span>
- <span data-ttu-id="319ad-973">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="319ad-973">Drivers Licence</span></span>
- <span data-ttu-id="319ad-974">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="319ad-974">Drivers Licences</span></span>
- <span data-ttu-id="319ad-975">Driver'Lic</span><span class="sxs-lookup"><span data-stu-id="319ad-975">Driver'Lic</span></span>
- <span data-ttu-id="319ad-976">Driver'Lics</span><span class="sxs-lookup"><span data-stu-id="319ad-976">Driver'Lics</span></span>
- <span data-ttu-id="319ad-977">Driver'License</span><span class="sxs-lookup"><span data-stu-id="319ad-977">Driver'License</span></span>
- <span data-ttu-id="319ad-978">Driver'Licenses</span><span class="sxs-lookup"><span data-stu-id="319ad-978">Driver'Licenses</span></span>
- <span data-ttu-id="319ad-979">Driver'Licence</span><span class="sxs-lookup"><span data-stu-id="319ad-979">Driver'Licence</span></span>
- <span data-ttu-id="319ad-980">Driver'Licences</span><span class="sxs-lookup"><span data-stu-id="319ad-980">Driver'Licences</span></span>
- <span data-ttu-id="319ad-981">Permis conduire</span><span class="sxs-lookup"><span data-stu-id="319ad-981">Driver' Lic</span></span>
- <span data-ttu-id="319ad-982">Permis conduire</span><span class="sxs-lookup"><span data-stu-id="319ad-982">Driver' Lics</span></span>
- <span data-ttu-id="319ad-983">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="319ad-983">Driver' License</span></span>
- <span data-ttu-id="319ad-984">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="319ad-984">Driver' Licenses</span></span>
- <span data-ttu-id="319ad-985">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="319ad-985">Driver' Licence</span></span>
- <span data-ttu-id="319ad-986">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="319ad-986">Driver' Licences</span></span>
- <span data-ttu-id="319ad-987">Driver'sLic</span><span class="sxs-lookup"><span data-stu-id="319ad-987">Driver'sLic</span></span>
- <span data-ttu-id="319ad-988">Driver'sLics</span><span class="sxs-lookup"><span data-stu-id="319ad-988">Driver'sLics</span></span>
- <span data-ttu-id="319ad-989">Driver'sLicense</span><span class="sxs-lookup"><span data-stu-id="319ad-989">Driver'sLicense</span></span>
- <span data-ttu-id="319ad-990">Driver'sLicenses</span><span class="sxs-lookup"><span data-stu-id="319ad-990">Driver'sLicenses</span></span>
- <span data-ttu-id="319ad-991">Driver'sLicence</span><span class="sxs-lookup"><span data-stu-id="319ad-991">Driver'sLicence</span></span>
- <span data-ttu-id="319ad-992">Driver'sLicences</span><span class="sxs-lookup"><span data-stu-id="319ad-992">Driver'sLicences</span></span>
- <span data-ttu-id="319ad-993">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="319ad-993">Driver's Lic</span></span>
- <span data-ttu-id="319ad-994">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="319ad-994">Driver's Lics</span></span>
- <span data-ttu-id="319ad-995">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="319ad-995">Driver's License</span></span>
- <span data-ttu-id="319ad-996">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="319ad-996">Driver's Licenses</span></span>
- <span data-ttu-id="319ad-997">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="319ad-997">Driver's Licence</span></span>
- <span data-ttu-id="319ad-998">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="319ad-998">Driver's Licences</span></span>
- <span data-ttu-id="319ad-999">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="319ad-999">Permis de Conduire</span></span>
- <span data-ttu-id="319ad-1000">id</span><span class="sxs-lookup"><span data-stu-id="319ad-1000">id</span></span>
- <span data-ttu-id="319ad-1001">Ids</span><span class="sxs-lookup"><span data-stu-id="319ad-1001">ids</span></span>
- <span data-ttu-id="319ad-1002">numéro carte d’identification</span><span class="sxs-lookup"><span data-stu-id="319ad-1002">idcard number</span></span>
- <span data-ttu-id="319ad-1003">numéros carte d’identification</span><span class="sxs-lookup"><span data-stu-id="319ad-1003">idcard numbers</span></span>
- <span data-ttu-id="319ad-1004"># carte d’identification</span><span class="sxs-lookup"><span data-stu-id="319ad-1004">idcard #</span></span>
- <span data-ttu-id="319ad-1005"># carte d’identification</span><span class="sxs-lookup"><span data-stu-id="319ad-1005">idcard #s</span></span>
- <span data-ttu-id="319ad-1006">carte d’identification</span><span class="sxs-lookup"><span data-stu-id="319ad-1006">idcard card</span></span>
- <span data-ttu-id="319ad-1007">cartes d’identification</span><span class="sxs-lookup"><span data-stu-id="319ad-1007">idcard cards</span></span>
- <span data-ttu-id="319ad-1008">carte d’identification</span><span class="sxs-lookup"><span data-stu-id="319ad-1008">idcard</span></span>
- <span data-ttu-id="319ad-1009">numéro d’identification</span><span class="sxs-lookup"><span data-stu-id="319ad-1009">identification number</span></span>
- <span data-ttu-id="319ad-1010">numéros d’identification</span><span class="sxs-lookup"><span data-stu-id="319ad-1010">identification numbers</span></span>
- <span data-ttu-id="319ad-1011"># identification</span><span class="sxs-lookup"><span data-stu-id="319ad-1011">identification #</span></span>
- <span data-ttu-id="319ad-1012"># identification</span><span class="sxs-lookup"><span data-stu-id="319ad-1012">identification #s</span></span>
- <span data-ttu-id="319ad-1013">carte d’identification</span><span class="sxs-lookup"><span data-stu-id="319ad-1013">identification card</span></span>
- <span data-ttu-id="319ad-1014">cartes d’identification</span><span class="sxs-lookup"><span data-stu-id="319ad-1014">identification cards</span></span>
- <span data-ttu-id="319ad-1015">identificateur</span><span class="sxs-lookup"><span data-stu-id="319ad-1015">identification</span></span> 
- <span data-ttu-id="319ad-1016">LD #</span><span class="sxs-lookup"><span data-stu-id="319ad-1016">DL#</span></span>
- <span data-ttu-id="319ad-1017">DISTRIBUTION #</span><span class="sxs-lookup"><span data-stu-id="319ad-1017">DLS#</span></span> 
- <span data-ttu-id="319ad-1018">CÈDE #</span><span class="sxs-lookup"><span data-stu-id="319ad-1018">CDL#</span></span> 
- <span data-ttu-id="319ad-1019">CDLS #</span><span class="sxs-lookup"><span data-stu-id="319ad-1019">CDLS#</span></span> 
- <span data-ttu-id="319ad-1020">DriverLic #</span><span class="sxs-lookup"><span data-stu-id="319ad-1020">DriverLic#</span></span> 
- <span data-ttu-id="319ad-1021">DriverLics #</span><span class="sxs-lookup"><span data-stu-id="319ad-1021">DriverLics#</span></span> 
- <span data-ttu-id="319ad-1022">DriverLicense #</span><span class="sxs-lookup"><span data-stu-id="319ad-1022">DriverLicense#</span></span> 
- <span data-ttu-id="319ad-1023">DriverLicenses #</span><span class="sxs-lookup"><span data-stu-id="319ad-1023">DriverLicenses#</span></span> 
- <span data-ttu-id="319ad-1024">DriverLicence #</span><span class="sxs-lookup"><span data-stu-id="319ad-1024">DriverLicence#</span></span> 
- <span data-ttu-id="319ad-1025">DriverLicences #</span><span class="sxs-lookup"><span data-stu-id="319ad-1025">DriverLicences#</span></span> 
- <span data-ttu-id="319ad-1026">#Permis conduire</span><span class="sxs-lookup"><span data-stu-id="319ad-1026">Driver Lic#</span></span>
- <span data-ttu-id="319ad-1027">#Permis conduire</span><span class="sxs-lookup"><span data-stu-id="319ad-1027">Driver Lics#</span></span> 
- <span data-ttu-id="319ad-1028">#Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="319ad-1028">Driver License#</span></span> 
- <span data-ttu-id="319ad-1029">#Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="319ad-1029">Driver Licenses#</span></span> 
- <span data-ttu-id="319ad-1030">#Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="319ad-1030">Driver License#</span></span> 
- <span data-ttu-id="319ad-1031">#Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="319ad-1031">Driver Licences#</span></span> 
- <span data-ttu-id="319ad-1032">DriversLic #</span><span class="sxs-lookup"><span data-stu-id="319ad-1032">DriversLic#</span></span> 
- <span data-ttu-id="319ad-1033">DriversLics #</span><span class="sxs-lookup"><span data-stu-id="319ad-1033">DriversLics#</span></span> 
- <span data-ttu-id="319ad-1034">DriversLicense #</span><span class="sxs-lookup"><span data-stu-id="319ad-1034">DriversLicense#</span></span> 
- <span data-ttu-id="319ad-1035">DriversLicenses #</span><span class="sxs-lookup"><span data-stu-id="319ad-1035">DriversLicenses#</span></span> 
- <span data-ttu-id="319ad-1036">DriversLicence #</span><span class="sxs-lookup"><span data-stu-id="319ad-1036">DriversLicence#</span></span> 
- <span data-ttu-id="319ad-1037">DriversLicences #</span><span class="sxs-lookup"><span data-stu-id="319ad-1037">DriversLicences#</span></span> 
- <span data-ttu-id="319ad-1038">#Permis conduire</span><span class="sxs-lookup"><span data-stu-id="319ad-1038">Drivers Lic#</span></span> 
- <span data-ttu-id="319ad-1039">#Permis conduire</span><span class="sxs-lookup"><span data-stu-id="319ad-1039">Drivers Lics#</span></span> 
- <span data-ttu-id="319ad-1040">#Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="319ad-1040">Drivers License#</span></span> 
- <span data-ttu-id="319ad-1041">#Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="319ad-1041">Drivers Licenses#</span></span> 
- <span data-ttu-id="319ad-1042">#Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="319ad-1042">Drivers Licence#</span></span> 
- <span data-ttu-id="319ad-1043">#Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="319ad-1043">Drivers Licences#</span></span> 
- <span data-ttu-id="319ad-1044">Driver'Lic #</span><span class="sxs-lookup"><span data-stu-id="319ad-1044">Driver'Lic#</span></span> 
- <span data-ttu-id="319ad-1045">Driver'Lics #</span><span class="sxs-lookup"><span data-stu-id="319ad-1045">Driver'Lics#</span></span> 
- <span data-ttu-id="319ad-1046">Driver'License #</span><span class="sxs-lookup"><span data-stu-id="319ad-1046">Driver'License#</span></span> 
- <span data-ttu-id="319ad-1047">Driver'Licenses #</span><span class="sxs-lookup"><span data-stu-id="319ad-1047">Driver'Licenses#</span></span> 
- <span data-ttu-id="319ad-1048">Driver'Licence #</span><span class="sxs-lookup"><span data-stu-id="319ad-1048">Driver'Licence#</span></span> 
- <span data-ttu-id="319ad-1049">Driver'Licences #</span><span class="sxs-lookup"><span data-stu-id="319ad-1049">Driver'Licences#</span></span> 
- <span data-ttu-id="319ad-1050">#Permis conduire</span><span class="sxs-lookup"><span data-stu-id="319ad-1050">Driver' Lic#</span></span> 
- <span data-ttu-id="319ad-1051">#Permis conduire</span><span class="sxs-lookup"><span data-stu-id="319ad-1051">Driver' Lics#</span></span> 
- <span data-ttu-id="319ad-1052">#Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="319ad-1052">Driver' License#</span></span> 
- <span data-ttu-id="319ad-1053">#Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="319ad-1053">Driver' Licenses#</span></span> 
- <span data-ttu-id="319ad-1054">#Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="319ad-1054">Driver' Licence#</span></span> 
- <span data-ttu-id="319ad-1055">#Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="319ad-1055">Driver' Licences#</span></span> 
- <span data-ttu-id="319ad-1056">Driver'sLic #</span><span class="sxs-lookup"><span data-stu-id="319ad-1056">Driver'sLic#</span></span> 
- <span data-ttu-id="319ad-1057">Driver'sLics #</span><span class="sxs-lookup"><span data-stu-id="319ad-1057">Driver'sLics#</span></span> 
- <span data-ttu-id="319ad-1058">Driver'sLicense #</span><span class="sxs-lookup"><span data-stu-id="319ad-1058">Driver'sLicense#</span></span> 
- <span data-ttu-id="319ad-1059">Driver'sLicenses #</span><span class="sxs-lookup"><span data-stu-id="319ad-1059">Driver'sLicenses#</span></span> 
- <span data-ttu-id="319ad-1060">Driver'sLicence #</span><span class="sxs-lookup"><span data-stu-id="319ad-1060">Driver'sLicence#</span></span> 
- <span data-ttu-id="319ad-1061">Driver'sLicences #</span><span class="sxs-lookup"><span data-stu-id="319ad-1061">Driver'sLicences#</span></span> 
- <span data-ttu-id="319ad-1062">#Permisconduire</span><span class="sxs-lookup"><span data-stu-id="319ad-1062">Driver's Lic#</span></span> 
- <span data-ttu-id="319ad-1063">#Permisconduire</span><span class="sxs-lookup"><span data-stu-id="319ad-1063">Driver's Lics#</span></span> 
- <span data-ttu-id="319ad-1064">#Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="319ad-1064">Driver's License#</span></span> 
- <span data-ttu-id="319ad-1065">#Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="319ad-1065">Driver's Licenses#</span></span> 
- <span data-ttu-id="319ad-1066">#Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="319ad-1066">Driver's Licence#</span></span> 
- <span data-ttu-id="319ad-1067">#Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="319ad-1067">Driver's Licences#</span></span> 
- <span data-ttu-id="319ad-1068">Permis de conduire #</span><span class="sxs-lookup"><span data-stu-id="319ad-1068">Permis de Conduire#</span></span> 
- <span data-ttu-id="319ad-1069">Réf #</span><span class="sxs-lookup"><span data-stu-id="319ad-1069">id#</span></span> 
- <span data-ttu-id="319ad-1070">codes #</span><span class="sxs-lookup"><span data-stu-id="319ad-1070">ids#</span></span> 
- <span data-ttu-id="319ad-1071">#carte carte d’identification</span><span class="sxs-lookup"><span data-stu-id="319ad-1071">idcard card#</span></span> 
- <span data-ttu-id="319ad-1072">#cartes carte d’identification</span><span class="sxs-lookup"><span data-stu-id="319ad-1072">idcard cards#</span></span> 
- <span data-ttu-id="319ad-1073">carte d’identification #</span><span class="sxs-lookup"><span data-stu-id="319ad-1073">idcard#</span></span> 
- <span data-ttu-id="319ad-1074">#carte d’identification</span><span class="sxs-lookup"><span data-stu-id="319ad-1074">identification card#</span></span> 
- <span data-ttu-id="319ad-1075">#cartes d’identification</span><span class="sxs-lookup"><span data-stu-id="319ad-1075">identification cards#</span></span> 
- <span data-ttu-id="319ad-1076">identificateur #</span><span class="sxs-lookup"><span data-stu-id="319ad-1076">identification#</span></span> 
   
## <a name="canada-health-service-number"></a><span data-ttu-id="319ad-1077">Numéro de service de santé Canada</span><span class="sxs-lookup"><span data-stu-id="319ad-1077">Canada Health Service Number</span></span>

### <a name="format"></a><span data-ttu-id="319ad-1078">Format</span><span class="sxs-lookup"><span data-stu-id="319ad-1078">Format</span></span>

<span data-ttu-id="319ad-1079">10 chiffres</span><span class="sxs-lookup"><span data-stu-id="319ad-1079">10 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="319ad-1080">Modèle</span><span class="sxs-lookup"><span data-stu-id="319ad-1080">Pattern</span></span>

<span data-ttu-id="319ad-1081">10 chiffres</span><span class="sxs-lookup"><span data-stu-id="319ad-1081">10 digits</span></span>

### <a name="checksum"></a><span data-ttu-id="319ad-1082">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="319ad-1082">Checksum</span></span>

<span data-ttu-id="319ad-1083">Non</span><span class="sxs-lookup"><span data-stu-id="319ad-1083">No</span></span>

### <a name="definition"></a><span data-ttu-id="319ad-1084">Définition</span><span class="sxs-lookup"><span data-stu-id="319ad-1084">Definition</span></span>

<span data-ttu-id="319ad-1085">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="319ad-1085">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="319ad-1086">L’expression régulière Regex_canada_health_service_number trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="319ad-1086">The regular expression Regex_canada_health_service_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="319ad-1087">Un mot clé figurant dans la liste Keyword_canada_health_service_number est trouvé.</span><span class="sxs-lookup"><span data-stu-id="319ad-1087">A keyword from Keyword_canada_health_service_number is found.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="319ad-1088">Mots-clés</span><span class="sxs-lookup"><span data-stu-id="319ad-1088">Keywords</span></span>

#### <a name="keyword_canada_health_service_number"></a><span data-ttu-id="319ad-1089">Keyword_canada_health_service_number</span><span class="sxs-lookup"><span data-stu-id="319ad-1089">Keyword_canada_health_service_number</span></span>

- <span data-ttu-id="319ad-1090">numéro d’assurance-maladie</span><span class="sxs-lookup"><span data-stu-id="319ad-1090">personal health number</span></span>
- <span data-ttu-id="319ad-1091">informations sur le patient</span><span class="sxs-lookup"><span data-stu-id="319ad-1091">patient information</span></span>
- <span data-ttu-id="319ad-1092">services de santé</span><span class="sxs-lookup"><span data-stu-id="319ad-1092">health services</span></span>
- <span data-ttu-id="319ad-1093">services spécialisés</span><span class="sxs-lookup"><span data-stu-id="319ad-1093">speciality services</span></span>
- <span data-ttu-id="319ad-1094">accident automobile</span><span class="sxs-lookup"><span data-stu-id="319ad-1094">automobile accident</span></span>
- <span data-ttu-id="319ad-1095">hôpital pour malades</span><span class="sxs-lookup"><span data-stu-id="319ad-1095">patient hospital</span></span>
- <span data-ttu-id="319ad-1096">psychiatrist</span><span class="sxs-lookup"><span data-stu-id="319ad-1096">psychiatrist</span></span>
- <span data-ttu-id="319ad-1097">indemnisation des salariés</span><span class="sxs-lookup"><span data-stu-id="319ad-1097">workers compensation</span></span>
- <span data-ttu-id="319ad-1098">incapacité</span><span class="sxs-lookup"><span data-stu-id="319ad-1098">disability</span></span>
      
## <a name="canada-passport-number"></a><span data-ttu-id="319ad-1099">Numéro de passeport Canada</span><span class="sxs-lookup"><span data-stu-id="319ad-1099">Canada Passport Number</span></span>

### <a name="format"></a><span data-ttu-id="319ad-1100">Format</span><span class="sxs-lookup"><span data-stu-id="319ad-1100">Format</span></span>

<span data-ttu-id="319ad-1101">Deux lettres majuscules suivies de six chiffres</span><span class="sxs-lookup"><span data-stu-id="319ad-1101">Two uppercase letters followed by six digits</span></span>

### <a name="pattern"></a><span data-ttu-id="319ad-1102">Modèle</span><span class="sxs-lookup"><span data-stu-id="319ad-1102">Pattern</span></span>

<span data-ttu-id="319ad-1103">Deux lettres majuscules suivies de six chiffres</span><span class="sxs-lookup"><span data-stu-id="319ad-1103">Two uppercase letters followed by six digits</span></span>

### <a name="checksum"></a><span data-ttu-id="319ad-1104">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="319ad-1104">Checksum</span></span>

<span data-ttu-id="319ad-1105">Non</span><span class="sxs-lookup"><span data-stu-id="319ad-1105">No</span></span>

### <a name="definition"></a><span data-ttu-id="319ad-1106">Définition</span><span class="sxs-lookup"><span data-stu-id="319ad-1106">Definition</span></span>

<span data-ttu-id="319ad-1107">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="319ad-1107">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="319ad-1108">L’expression régulière Regex_canada_passport_number trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="319ad-1108">The regular expression Regex_canada_passport_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="319ad-1109">Un mot clé depuis Keyword_canada_passport_number ou Keyword_passport est trouvé.</span><span class="sxs-lookup"><span data-stu-id="319ad-1109">A keyword from Keyword_canada_passport_number or Keyword_passport is found.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="319ad-1110">Mots-clés</span><span class="sxs-lookup"><span data-stu-id="319ad-1110">Keywords</span></span>

#### <a name="keyword_canada_passport_number"></a><span data-ttu-id="319ad-1111">Keyword_canada_passport_number</span><span class="sxs-lookup"><span data-stu-id="319ad-1111">Keyword_canada_passport_number</span></span>

- <span data-ttu-id="319ad-1112">citoyenneté canadienne</span><span class="sxs-lookup"><span data-stu-id="319ad-1112">canadian citizenship</span></span>
- <span data-ttu-id="319ad-1113">passeport canadien</span><span class="sxs-lookup"><span data-stu-id="319ad-1113">canadian passport</span></span>
- <span data-ttu-id="319ad-1114">demande de passeport</span><span class="sxs-lookup"><span data-stu-id="319ad-1114">passport application</span></span>
- <span data-ttu-id="319ad-1115">photos pour passeport</span><span class="sxs-lookup"><span data-stu-id="319ad-1115">passport photos</span></span>
- <span data-ttu-id="319ad-1116">traducteur agréé</span><span class="sxs-lookup"><span data-stu-id="319ad-1116">certified translator</span></span>
- <span data-ttu-id="319ad-1117">citoyens canadiens</span><span class="sxs-lookup"><span data-stu-id="319ad-1117">canadian citizens</span></span>
- <span data-ttu-id="319ad-1118">temps de traitement</span><span class="sxs-lookup"><span data-stu-id="319ad-1118">processing times</span></span>
- <span data-ttu-id="319ad-1119">demande de renouvellement</span><span class="sxs-lookup"><span data-stu-id="319ad-1119">renewal application</span></span>

#### <a name="keyword_passport"></a><span data-ttu-id="319ad-1120">Keyword_passport</span><span class="sxs-lookup"><span data-stu-id="319ad-1120">Keyword_passport</span></span>

- <span data-ttu-id="319ad-1121">Numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="319ad-1121">Passport Number</span></span>
- <span data-ttu-id="319ad-1122">N° de passeport</span><span class="sxs-lookup"><span data-stu-id="319ad-1122">Passport No</span></span>
- <span data-ttu-id="319ad-1123"># Passeport</span><span class="sxs-lookup"><span data-stu-id="319ad-1123">Passport #</span></span>
- <span data-ttu-id="319ad-1124">Tel #</span><span class="sxs-lookup"><span data-stu-id="319ad-1124">Passport#</span></span>
- <span data-ttu-id="319ad-1125">PassportID</span><span class="sxs-lookup"><span data-stu-id="319ad-1125">PassportID</span></span>
- <span data-ttu-id="319ad-1126">N ° passeport</span><span class="sxs-lookup"><span data-stu-id="319ad-1126">Passportno</span></span>
- <span data-ttu-id="319ad-1127">passportnumber</span><span class="sxs-lookup"><span data-stu-id="319ad-1127">passportnumber</span></span>
- <span data-ttu-id="319ad-1128">パスポート</span><span class="sxs-lookup"><span data-stu-id="319ad-1128">パスポート</span></span>
- <span data-ttu-id="319ad-1129">パスポート番号</span><span class="sxs-lookup"><span data-stu-id="319ad-1129">パスポート番号</span></span>
- <span data-ttu-id="319ad-1130">パスポートのNum</span><span class="sxs-lookup"><span data-stu-id="319ad-1130">パスポートのNum</span></span>
- <span data-ttu-id="319ad-1131">パスポート＃</span><span class="sxs-lookup"><span data-stu-id="319ad-1131">パスポート＃</span></span>
- <span data-ttu-id="319ad-1132">Numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="319ad-1132">Numéro de passeport</span></span>
- <span data-ttu-id="319ad-1133">Passeport n°</span><span class="sxs-lookup"><span data-stu-id="319ad-1133">Passeport n °</span></span>
- <span data-ttu-id="319ad-1134">Passeport numéro</span><span class="sxs-lookup"><span data-stu-id="319ad-1134">Passeport Non</span></span>
- <span data-ttu-id="319ad-1135"># Passeport</span><span class="sxs-lookup"><span data-stu-id="319ad-1135">Passeport #</span></span>
- <span data-ttu-id="319ad-1136">Passeport #</span><span class="sxs-lookup"><span data-stu-id="319ad-1136">Passeport#</span></span>
- <span data-ttu-id="319ad-1137">PasseportNon</span><span class="sxs-lookup"><span data-stu-id="319ad-1137">PasseportNon</span></span>
- <span data-ttu-id="319ad-1138">Passeportn °</span><span class="sxs-lookup"><span data-stu-id="319ad-1138">Passeportn °</span></span>
   
## <a name="canada-personal-health-identification-number-phin"></a><span data-ttu-id="319ad-1139">NIMP (numéro d’identification médicale personnel) Canada</span><span class="sxs-lookup"><span data-stu-id="319ad-1139">Canada Personal Health Identification Number (PHIN)</span></span>

### <a name="format"></a><span data-ttu-id="319ad-1140">Format</span><span class="sxs-lookup"><span data-stu-id="319ad-1140">Format</span></span>

<span data-ttu-id="319ad-1141">Neuf chiffres</span><span class="sxs-lookup"><span data-stu-id="319ad-1141">Nine digits</span></span>

### <a name="pattern"></a><span data-ttu-id="319ad-1142">Modèle</span><span class="sxs-lookup"><span data-stu-id="319ad-1142">Pattern</span></span>

<span data-ttu-id="319ad-1143">Neuf chiffres</span><span class="sxs-lookup"><span data-stu-id="319ad-1143">Nine digits</span></span>

### <a name="checksum"></a><span data-ttu-id="319ad-1144">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="319ad-1144">Checksum</span></span>

<span data-ttu-id="319ad-1145">Non</span><span class="sxs-lookup"><span data-stu-id="319ad-1145">No</span></span>

### <a name="definition"></a><span data-ttu-id="319ad-1146">Définition</span><span class="sxs-lookup"><span data-stu-id="319ad-1146">Definition</span></span>

<span data-ttu-id="319ad-1147">Une stratégie DLP est sûre à 75% d’avoir détecté ce type d’informations sensibles si, dans une proximité de 300 caractères : l’expression régulière Regex_canada_phin trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="319ad-1147">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters: The regular expression Regex_canada_phin finds content that matches the pattern.</span></span>
<span data-ttu-id="319ad-1148">Au moins deux mots clés provenant d’Keyword_canada_phin ou de Keyword_canada_provinces sont trouvés..</span><span class="sxs-lookup"><span data-stu-id="319ad-1148">At least two keywords from Keyword_canada_phin or Keyword_canada_provinces are found..</span></span>

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

### <a name="keywords"></a><span data-ttu-id="319ad-1149">Mots-clés</span><span class="sxs-lookup"><span data-stu-id="319ad-1149">Keywords</span></span>

#### <a name="keyword_canada_phin"></a><span data-ttu-id="319ad-1150">Keyword_canada_phin</span><span class="sxs-lookup"><span data-stu-id="319ad-1150">Keyword_canada_phin</span></span>

- <span data-ttu-id="319ad-1151">numéro d’assurance sociale</span><span class="sxs-lookup"><span data-stu-id="319ad-1151">social insurance number</span></span>
- <span data-ttu-id="319ad-1152">loi sur les renseignements médicaux</span><span class="sxs-lookup"><span data-stu-id="319ad-1152">health information act</span></span>
- <span data-ttu-id="319ad-1153">renseignements relatifs à l’impôt sur le revenu</span><span class="sxs-lookup"><span data-stu-id="319ad-1153">income tax information</span></span>
- <span data-ttu-id="319ad-1154">santé Manitoba</span><span class="sxs-lookup"><span data-stu-id="319ad-1154">manitoba health</span></span>
- <span data-ttu-id="319ad-1155">enregistrement aux services de santé</span><span class="sxs-lookup"><span data-stu-id="319ad-1155">health registration</span></span>
- <span data-ttu-id="319ad-1156">achats de médicaments sur ordonnance</span><span class="sxs-lookup"><span data-stu-id="319ad-1156">prescription purchases</span></span>
- <span data-ttu-id="319ad-1157">admissibilité aux prestations</span><span class="sxs-lookup"><span data-stu-id="319ad-1157">benefit eligibility</span></span>
- <span data-ttu-id="319ad-1158">santé personnelle</span><span class="sxs-lookup"><span data-stu-id="319ad-1158">personal health</span></span>
- <span data-ttu-id="319ad-1159">procuration</span><span class="sxs-lookup"><span data-stu-id="319ad-1159">power of attorney</span></span>
- <span data-ttu-id="319ad-1160">numéro d’enregistrement</span><span class="sxs-lookup"><span data-stu-id="319ad-1160">registration number</span></span>
- <span data-ttu-id="319ad-1161">numéro d’assurance-maladie</span><span class="sxs-lookup"><span data-stu-id="319ad-1161">personal health number</span></span>
- <span data-ttu-id="319ad-1162">recommandation par le médecin</span><span class="sxs-lookup"><span data-stu-id="319ad-1162">practitioner referral</span></span>
- <span data-ttu-id="319ad-1163">professionnel de bien-être</span><span class="sxs-lookup"><span data-stu-id="319ad-1163">wellness professional</span></span>
- <span data-ttu-id="319ad-1164">orientation d’un patient</span><span class="sxs-lookup"><span data-stu-id="319ad-1164">patient referral</span></span>
- <span data-ttu-id="319ad-1165">santé et bien-être</span><span class="sxs-lookup"><span data-stu-id="319ad-1165">health and wellness</span></span>

#### <a name="keyword_canada_provinces"></a><span data-ttu-id="319ad-1166">Keyword_canada_provinces</span><span class="sxs-lookup"><span data-stu-id="319ad-1166">Keyword_canada_provinces</span></span>

- <span data-ttu-id="319ad-1167">Nunavut</span><span class="sxs-lookup"><span data-stu-id="319ad-1167">Nunavut</span></span>
- <span data-ttu-id="319ad-1168">Régime</span><span class="sxs-lookup"><span data-stu-id="319ad-1168">Quebec</span></span>
- <span data-ttu-id="319ad-1169">Territoires du Nord-Ouest</span><span class="sxs-lookup"><span data-stu-id="319ad-1169">Northwest Territories</span></span>
- <span data-ttu-id="319ad-1170">Brand</span><span class="sxs-lookup"><span data-stu-id="319ad-1170">Ontario</span></span>
- <span data-ttu-id="319ad-1171">Colombie-britannique</span><span class="sxs-lookup"><span data-stu-id="319ad-1171">British Columbia</span></span>
- <span data-ttu-id="319ad-1172">Alberta</span><span class="sxs-lookup"><span data-stu-id="319ad-1172">Alberta</span></span>
- <span data-ttu-id="319ad-1173">En-dessus</span><span class="sxs-lookup"><span data-stu-id="319ad-1173">Saskatchewan</span></span>
- <span data-ttu-id="319ad-1174">Manitoba</span><span class="sxs-lookup"><span data-stu-id="319ad-1174">Manitoba</span></span>
- <span data-ttu-id="319ad-1175">Yukon</span><span class="sxs-lookup"><span data-stu-id="319ad-1175">Yukon</span></span>
- <span data-ttu-id="319ad-1176">Terre-Neuve-et-Labrador</span><span class="sxs-lookup"><span data-stu-id="319ad-1176">Newfoundland and Labrador</span></span>
- <span data-ttu-id="319ad-1177">Nouveau-Brunswick</span><span class="sxs-lookup"><span data-stu-id="319ad-1177">New Brunswick</span></span>
- <span data-ttu-id="319ad-1178">Nouvelle-Écosse</span><span class="sxs-lookup"><span data-stu-id="319ad-1178">Nova Scotia</span></span>
- <span data-ttu-id="319ad-1179">Île-du-Prince-Édouard</span><span class="sxs-lookup"><span data-stu-id="319ad-1179">Prince Edward Island</span></span>
- <span data-ttu-id="319ad-1180">Canada</span><span class="sxs-lookup"><span data-stu-id="319ad-1180">Canada</span></span>
   
## <a name="canada-social-insurance-number"></a><span data-ttu-id="319ad-1181">Numéro d'assurance sociale Canada</span><span class="sxs-lookup"><span data-stu-id="319ad-1181">Canada Social Insurance Number</span></span>

### <a name="format"></a><span data-ttu-id="319ad-1182">Format</span><span class="sxs-lookup"><span data-stu-id="319ad-1182">Format</span></span>

<span data-ttu-id="319ad-1183">Neuf chiffres avec éventuellement des traits d’union ou des espaces</span><span class="sxs-lookup"><span data-stu-id="319ad-1183">Nine digits with optional hyphens or spaces</span></span>

### <a name="pattern"></a><span data-ttu-id="319ad-1184">Modèle</span><span class="sxs-lookup"><span data-stu-id="319ad-1184">Pattern</span></span>

<span data-ttu-id="319ad-1185">Avec</span><span class="sxs-lookup"><span data-stu-id="319ad-1185">Formatted:</span></span>
- <span data-ttu-id="319ad-1186">Trois chiffres</span><span class="sxs-lookup"><span data-stu-id="319ad-1186">Three digits</span></span> 
- <span data-ttu-id="319ad-1187">Un trait d’union ou un espace</span><span class="sxs-lookup"><span data-stu-id="319ad-1187">A hyphen or space</span></span> 
- <span data-ttu-id="319ad-1188">Trois chiffres</span><span class="sxs-lookup"><span data-stu-id="319ad-1188">Three digits</span></span> 
- <span data-ttu-id="319ad-1189">Un trait d’union ou un espace</span><span class="sxs-lookup"><span data-stu-id="319ad-1189">A hyphen or space</span></span> 
- <span data-ttu-id="319ad-1190">Trois chiffres</span><span class="sxs-lookup"><span data-stu-id="319ad-1190">Three digits</span></span>

<span data-ttu-id="319ad-1191">Non mis en forme : neuf chiffres</span><span class="sxs-lookup"><span data-stu-id="319ad-1191">Unformatted: Nine digits</span></span>

### <a name="checksum"></a><span data-ttu-id="319ad-1192">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="319ad-1192">Checksum</span></span>

<span data-ttu-id="319ad-1193">Oui</span><span class="sxs-lookup"><span data-stu-id="319ad-1193">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="319ad-1194">Définition</span><span class="sxs-lookup"><span data-stu-id="319ad-1194">Definition</span></span>

<span data-ttu-id="319ad-1195">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="319ad-1195">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="319ad-1196">La fonction Func_canadian_sin trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="319ad-1196">The function Func_canadian_sin finds content that matches the pattern.</span></span>
- <span data-ttu-id="319ad-1197">Au moins deux des éléments suivants, quelle que soit la combinaison :</span><span class="sxs-lookup"><span data-stu-id="319ad-1197">At least two of any combination of the following:</span></span>
    - <span data-ttu-id="319ad-1198">Un mot clé figurant dans la liste Keyword_sin est trouvé.</span><span class="sxs-lookup"><span data-stu-id="319ad-1198">A keyword from Keyword_sin is found.</span></span>
    - <span data-ttu-id="319ad-1199">Un mot clé figurant dans la liste Keyword_sin_collaborative est trouvé.</span><span class="sxs-lookup"><span data-stu-id="319ad-1199">A keyword from Keyword_sin_collaborative is found.</span></span>
    - <span data-ttu-id="319ad-1200">La fonction Func_eu_date trouve une date au format correct.</span><span class="sxs-lookup"><span data-stu-id="319ad-1200">The function Func_eu_date finds a date in the right date format.</span></span>
- <span data-ttu-id="319ad-1201">La somme de contrôle est correcte.</span><span class="sxs-lookup"><span data-stu-id="319ad-1201">The checksum passes.</span></span>

<span data-ttu-id="319ad-1202">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="319ad-1202">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="319ad-1203">La fonction Func_unformatted_canadian_sin trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="319ad-1203">The function Func_unformatted_canadian_sin finds content that matches the pattern.</span></span>
- <span data-ttu-id="319ad-1204">Un mot clé figurant dans la liste Keyword_sin est trouvé.</span><span class="sxs-lookup"><span data-stu-id="319ad-1204">A keyword from Keyword_sin is found.</span></span>
- <span data-ttu-id="319ad-1205">La somme de contrôle est correcte.</span><span class="sxs-lookup"><span data-stu-id="319ad-1205">The checksum passes.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="319ad-1206">Mots-clés</span><span class="sxs-lookup"><span data-stu-id="319ad-1206">Keywords</span></span>

#### <a name="keyword_sin"></a><span data-ttu-id="319ad-1207">Keyword_sin</span><span class="sxs-lookup"><span data-stu-id="319ad-1207">Keyword_sin</span></span>

- <span data-ttu-id="319ad-1208">assoc</span><span class="sxs-lookup"><span data-stu-id="319ad-1208">sin</span></span> 
- <span data-ttu-id="319ad-1209">assurance sociale</span><span class="sxs-lookup"><span data-stu-id="319ad-1209">social insurance</span></span> 
- <span data-ttu-id="319ad-1210">numéro d’assurance sociale</span><span class="sxs-lookup"><span data-stu-id="319ad-1210">numero d'assurance sociale</span></span> 
- <span data-ttu-id="319ad-1211">péchés</span><span class="sxs-lookup"><span data-stu-id="319ad-1211">sins</span></span> 
- <span data-ttu-id="319ad-1212">SSN</span><span class="sxs-lookup"><span data-stu-id="319ad-1212">ssn</span></span> 
- <span data-ttu-id="319ad-1213">numéros</span><span class="sxs-lookup"><span data-stu-id="319ad-1213">ssns</span></span> 
- <span data-ttu-id="319ad-1214">sécurité sociale</span><span class="sxs-lookup"><span data-stu-id="319ad-1214">social security</span></span> 
- <span data-ttu-id="319ad-1215">numéro d’assurance sociale</span><span class="sxs-lookup"><span data-stu-id="319ad-1215">numero d'assurance social</span></span> 
- <span data-ttu-id="319ad-1216">numéro d’identification nationale</span><span class="sxs-lookup"><span data-stu-id="319ad-1216">national identification number</span></span> 
- <span data-ttu-id="319ad-1217">id national</span><span class="sxs-lookup"><span data-stu-id="319ad-1217">national id</span></span> 
- <span data-ttu-id="319ad-1218">sine #</span><span class="sxs-lookup"><span data-stu-id="319ad-1218">sin#</span></span> 
- <span data-ttu-id="319ad-1219">ass soc</span><span class="sxs-lookup"><span data-stu-id="319ad-1219">soc ins</span></span> 
- <span data-ttu-id="319ad-1220">ass sociale</span><span class="sxs-lookup"><span data-stu-id="319ad-1220">social ins</span></span> 

#### <a name="keyword_sin_collaborative"></a><span data-ttu-id="319ad-1221">Keyword_sin_collaborative</span><span class="sxs-lookup"><span data-stu-id="319ad-1221">Keyword_sin_collaborative</span></span>

- <span data-ttu-id="319ad-1222">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="319ad-1222">driver's license</span></span> 
- <span data-ttu-id="319ad-1223">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="319ad-1223">drivers license</span></span> 
- <span data-ttu-id="319ad-1224">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="319ad-1224">driver's licence</span></span> 
- <span data-ttu-id="319ad-1225">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="319ad-1225">drivers licence</span></span> 
- <span data-ttu-id="319ad-1226">DOB</span><span class="sxs-lookup"><span data-stu-id="319ad-1226">DOB</span></span> 
- <span data-ttu-id="319ad-1227">Birthdate</span><span class="sxs-lookup"><span data-stu-id="319ad-1227">Birthdate</span></span> 
- <span data-ttu-id="319ad-1228">Birthday</span><span class="sxs-lookup"><span data-stu-id="319ad-1228">Birthday</span></span> 
- <span data-ttu-id="319ad-1229">Date of Birth</span><span class="sxs-lookup"><span data-stu-id="319ad-1229">Date of Birth</span></span> 
   
## <a name="chile-identity-card-number"></a><span data-ttu-id="319ad-1230">	Numéro de carte d’identité Chili</span><span class="sxs-lookup"><span data-stu-id="319ad-1230">Chile Identity Card Number</span></span>

### <a name="format"></a><span data-ttu-id="319ad-1231">Format</span><span class="sxs-lookup"><span data-stu-id="319ad-1231">Format</span></span>

<span data-ttu-id="319ad-1232">7-8 chiffres plus des délimiteurs un chiffre ou une lettre</span><span class="sxs-lookup"><span data-stu-id="319ad-1232">7-8 digits plus delimiters a check digit or letter</span></span>

### <a name="pattern"></a><span data-ttu-id="319ad-1233">Modèle</span><span class="sxs-lookup"><span data-stu-id="319ad-1233">Pattern</span></span>

<span data-ttu-id="319ad-1234">7 ou 8 chiffres, plus des délimiteurs :</span><span class="sxs-lookup"><span data-stu-id="319ad-1234">7-8 digits plus delimiters:</span></span>
- <span data-ttu-id="319ad-1235">1 ou 2 chiffres </span><span class="sxs-lookup"><span data-stu-id="319ad-1235">1-2 digits</span></span> 
- <span data-ttu-id="319ad-1236">Un point </span><span class="sxs-lookup"><span data-stu-id="319ad-1236">A period</span></span> 
- <span data-ttu-id="319ad-1237">Trois chiffres</span><span class="sxs-lookup"><span data-stu-id="319ad-1237">Three digits</span></span> 
- <span data-ttu-id="319ad-1238">Un point </span><span class="sxs-lookup"><span data-stu-id="319ad-1238">A period</span></span> 
- <span data-ttu-id="319ad-1239">Trois chiffres</span><span class="sxs-lookup"><span data-stu-id="319ad-1239">Three digits</span></span> 
- <span data-ttu-id="319ad-1240">Un tiret</span><span class="sxs-lookup"><span data-stu-id="319ad-1240">A dash</span></span> 
- <span data-ttu-id="319ad-1241">Un chiffre ou une lettre (ne respectant pas la casse) de contrôle</span><span class="sxs-lookup"><span data-stu-id="319ad-1241">One digit or letter (not case sensitive) which is a check digit</span></span>

### <a name="checksum"></a><span data-ttu-id="319ad-1242">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="319ad-1242">Checksum</span></span>

<span data-ttu-id="319ad-1243">Oui</span><span class="sxs-lookup"><span data-stu-id="319ad-1243">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="319ad-1244">Définition</span><span class="sxs-lookup"><span data-stu-id="319ad-1244">Definition</span></span>

<span data-ttu-id="319ad-1245">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="319ad-1245">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="319ad-1246">La fonction Func_chile_id_card trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="319ad-1246">The function Func_chile_id_card finds content that matches the pattern.</span></span>
- <span data-ttu-id="319ad-1247">Un mot clé figurant dans la liste Keyword_chile_id_card est trouvé.</span><span class="sxs-lookup"><span data-stu-id="319ad-1247">A keyword from Keyword_chile_id_card is found.</span></span>
- <span data-ttu-id="319ad-1248">La somme de contrôle est correcte.</span><span class="sxs-lookup"><span data-stu-id="319ad-1248">The checksum passes.</span></span>

<span data-ttu-id="319ad-1249">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="319ad-1249">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="319ad-1250">La fonction Func_chile_id_card trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="319ad-1250">The function Func_chile_id_card finds content that matches the pattern.</span></span>
- <span data-ttu-id="319ad-1251">La somme de contrôle est correcte.</span><span class="sxs-lookup"><span data-stu-id="319ad-1251">The checksum passes.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="319ad-1252">Mots-clés</span><span class="sxs-lookup"><span data-stu-id="319ad-1252">Keywords</span></span>

#### <a name="keyword_chile_id_card"></a><span data-ttu-id="319ad-1253">Keyword_chile_id_card</span><span class="sxs-lookup"><span data-stu-id="319ad-1253">Keyword_chile_id_card</span></span>

- <span data-ttu-id="319ad-1254">National Identification Number</span><span class="sxs-lookup"><span data-stu-id="319ad-1254">National Identification Number</span></span> 
- <span data-ttu-id="319ad-1255">Identity card</span><span class="sxs-lookup"><span data-stu-id="319ad-1255">Identity card</span></span> 
- <span data-ttu-id="319ad-1256">ID</span><span class="sxs-lookup"><span data-stu-id="319ad-1256">ID</span></span> 
- <span data-ttu-id="319ad-1257">Identificateur</span><span class="sxs-lookup"><span data-stu-id="319ad-1257">Identification</span></span> 
- <span data-ttu-id="319ad-1258">Rol Único Nacional</span><span class="sxs-lookup"><span data-stu-id="319ad-1258">Rol Único Nacional</span></span> 
- <span data-ttu-id="319ad-1259">GÉNÉRER</span><span class="sxs-lookup"><span data-stu-id="319ad-1259">RUN</span></span> 
- <span data-ttu-id="319ad-1260">Rol Único Tributario</span><span class="sxs-lookup"><span data-stu-id="319ad-1260">Rol Único Tributario</span></span> 
- <span data-ttu-id="319ad-1261">ROUTINE</span><span class="sxs-lookup"><span data-stu-id="319ad-1261">RUT</span></span> 
- <span data-ttu-id="319ad-1262">Cédula de Identidad</span><span class="sxs-lookup"><span data-stu-id="319ad-1262">Cédula de Identidad</span></span> 
- <span data-ttu-id="319ad-1263">Número De Identificación Nacional</span><span class="sxs-lookup"><span data-stu-id="319ad-1263">Número De Identificación Nacional</span></span> 
- <span data-ttu-id="319ad-1264">Tarjeta de identificación</span><span class="sxs-lookup"><span data-stu-id="319ad-1264">Tarjeta de identificación</span></span> 
- <span data-ttu-id="319ad-1265">Identificación</span><span class="sxs-lookup"><span data-stu-id="319ad-1265">Identificación</span></span> 
   
## <a name="china-resident-identity-card-prc-number"></a><span data-ttu-id="319ad-1266">	Numéro de carte d’identité de résident Chine (RPC)</span><span class="sxs-lookup"><span data-stu-id="319ad-1266">China Resident Identity Card (PRC) Number</span></span>

### <a name="format"></a><span data-ttu-id="319ad-1267">Format</span><span class="sxs-lookup"><span data-stu-id="319ad-1267">Format</span></span>

<span data-ttu-id="319ad-1268">18 chiffres</span><span class="sxs-lookup"><span data-stu-id="319ad-1268">18 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="319ad-1269">Modèle</span><span class="sxs-lookup"><span data-stu-id="319ad-1269">Pattern</span></span>

<span data-ttu-id="319ad-1270">18 chiffres :</span><span class="sxs-lookup"><span data-stu-id="319ad-1270">18 digits:</span></span>
- <span data-ttu-id="319ad-1271">Six chiffres qui composent un code d’adresse </span><span class="sxs-lookup"><span data-stu-id="319ad-1271">Six digits which are an address code</span></span> 
- <span data-ttu-id="319ad-1272">Huit chiffres sous la forme AAAAMMJJ qui correspondent à la date de naissance </span><span class="sxs-lookup"><span data-stu-id="319ad-1272">Eight digits in the form YYYYMMDD which are the date of birth</span></span> 
- <span data-ttu-id="319ad-1273">Trois chiffres qui correspondent à un code d’opération </span><span class="sxs-lookup"><span data-stu-id="319ad-1273">Three digits which are an order code</span></span> 
- <span data-ttu-id="319ad-1274">Un chiffre de contrôle</span><span class="sxs-lookup"><span data-stu-id="319ad-1274">One digit which is a check digit</span></span>

### <a name="checksum"></a><span data-ttu-id="319ad-1275">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="319ad-1275">Checksum</span></span>

<span data-ttu-id="319ad-1276">Oui</span><span class="sxs-lookup"><span data-stu-id="319ad-1276">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="319ad-1277">Définition</span><span class="sxs-lookup"><span data-stu-id="319ad-1277">Definition</span></span>

<span data-ttu-id="319ad-1278">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="319ad-1278">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="319ad-1279">La fonction Func_china_resident_id trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="319ad-1279">The function Func_china_resident_id finds content that matches the pattern.</span></span>
- <span data-ttu-id="319ad-1280">Un mot clé figurant dans la liste Keyword_china_resident_id est trouvé.</span><span class="sxs-lookup"><span data-stu-id="319ad-1280">A keyword from Keyword_china_resident_id is found.</span></span>
- <span data-ttu-id="319ad-1281">La somme de contrôle est correcte.</span><span class="sxs-lookup"><span data-stu-id="319ad-1281">The checksum passes.</span></span>

<span data-ttu-id="319ad-1282">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="319ad-1282">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="319ad-1283">La fonction Func_china_resident_id trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="319ad-1283">The function Func_china_resident_id finds content that matches the pattern.</span></span>
- <span data-ttu-id="319ad-1284">La somme de contrôle est correcte.</span><span class="sxs-lookup"><span data-stu-id="319ad-1284">The checksum passes.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="319ad-1285">Mots-clés</span><span class="sxs-lookup"><span data-stu-id="319ad-1285">Keywords</span></span>

### <a name="keyword_china_resident_id"></a><span data-ttu-id="319ad-1286">Keyword_china_resident_id</span><span class="sxs-lookup"><span data-stu-id="319ad-1286">Keyword_china_resident_id</span></span>

- <span data-ttu-id="319ad-1287">Resident Identity Card</span><span class="sxs-lookup"><span data-stu-id="319ad-1287">Resident Identity Card</span></span> 
- <span data-ttu-id="319ad-1288">FIGURANT</span><span class="sxs-lookup"><span data-stu-id="319ad-1288">PRC</span></span> 
- <span data-ttu-id="319ad-1289">National Identification Card</span><span class="sxs-lookup"><span data-stu-id="319ad-1289">National Identification Card</span></span> 
- <span data-ttu-id="319ad-1290">身份证</span><span class="sxs-lookup"><span data-stu-id="319ad-1290">身份证</span></span> 
- <span data-ttu-id="319ad-1291">居民 身份证</span><span class="sxs-lookup"><span data-stu-id="319ad-1291">居民 身份证</span></span> 
- <span data-ttu-id="319ad-1292">居民身份证</span><span class="sxs-lookup"><span data-stu-id="319ad-1292">居民身份证</span></span> 
- <span data-ttu-id="319ad-1293">鉴定</span><span class="sxs-lookup"><span data-stu-id="319ad-1293">鉴定</span></span> 
- <span data-ttu-id="319ad-1294">身分證</span><span class="sxs-lookup"><span data-stu-id="319ad-1294">身分證</span></span> 
- <span data-ttu-id="319ad-1295">居民 身份證</span><span class="sxs-lookup"><span data-stu-id="319ad-1295">居民 身份證</span></span>
- <span data-ttu-id="319ad-1296">鑑定</span><span class="sxs-lookup"><span data-stu-id="319ad-1296">鑑定</span></span> 
   
## <a name="credit-card-number"></a><span data-ttu-id="319ad-1297">Numéro de carte de crédit</span><span class="sxs-lookup"><span data-stu-id="319ad-1297">Credit Card Number</span></span>

### <a name="format"></a><span data-ttu-id="319ad-1298">Format</span><span class="sxs-lookup"><span data-stu-id="319ad-1298">Format</span></span>

<span data-ttu-id="319ad-1299">16 chiffres qui peuvent être mis en forme ou non (dddddddddddddddd) et doivent réussir le test Luhn.</span><span class="sxs-lookup"><span data-stu-id="319ad-1299">16 digits which can be formatted or unformatted (dddddddddddddddd) and must pass the Luhn test.</span></span>

### <a name="pattern"></a><span data-ttu-id="319ad-1300">Modèle</span><span class="sxs-lookup"><span data-stu-id="319ad-1300">Pattern</span></span>

<span data-ttu-id="319ad-1301">Modèle très complexe et puissant qui détecte les cartes de visite de toutes les principales marques du monde, notamment Visa, MasterCard, Discover Card, JCB, American Express, etc.</span><span class="sxs-lookup"><span data-stu-id="319ad-1301">Very complex and robust pattern that detects cards from all major brands worldwide, including Visa, MasterCard, Discover Card, JCB, American Express, gift cards, and diner cards.</span></span>

### <a name="checksum"></a><span data-ttu-id="319ad-1302">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="319ad-1302">Checksum</span></span>

<span data-ttu-id="319ad-1303">Oui, la somme de contrôle de Luhn</span><span class="sxs-lookup"><span data-stu-id="319ad-1303">Yes, the Luhn checksum</span></span>

### <a name="definition"></a><span data-ttu-id="319ad-1304">Définition</span><span class="sxs-lookup"><span data-stu-id="319ad-1304">Definition</span></span>

<span data-ttu-id="319ad-1305">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="319ad-1305">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="319ad-1306">La fonction Func_credit_card trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="319ad-1306">The function Func_credit_card finds content that matches the pattern.</span></span>
- <span data-ttu-id="319ad-1307">L’une des affirmations suivantes est vraie :</span><span class="sxs-lookup"><span data-stu-id="319ad-1307">One of the following is true:</span></span>
    - <span data-ttu-id="319ad-1308">Un mot clé figurant dans la liste Keyword_cc_verification est trouvé.</span><span class="sxs-lookup"><span data-stu-id="319ad-1308">A keyword from Keyword_cc_verification is found.</span></span>
    - <span data-ttu-id="319ad-1309">Un mot clé figurant dans la liste Keyword_cc_name est trouvé.</span><span class="sxs-lookup"><span data-stu-id="319ad-1309">A keyword from Keyword_cc_name is found.</span></span>
    - <span data-ttu-id="319ad-1310">La fonction Func_expiration_date trouve une date au format correct.</span><span class="sxs-lookup"><span data-stu-id="319ad-1310">The function Func_expiration_date finds a date in the right date format.</span></span>
- <span data-ttu-id="319ad-1311">La somme de contrôle est correcte.</span><span class="sxs-lookup"><span data-stu-id="319ad-1311">The checksum passes.</span></span>

<span data-ttu-id="319ad-1312">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 65 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="319ad-1312">A DLP policy is 65% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="319ad-1313">La fonction Func_credit_card trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="319ad-1313">The function Func_credit_card finds content that matches the pattern.</span></span>
- <span data-ttu-id="319ad-1314">La somme de contrôle est correcte.</span><span class="sxs-lookup"><span data-stu-id="319ad-1314">The checksum passes.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="319ad-1315">Mots-clés</span><span class="sxs-lookup"><span data-stu-id="319ad-1315">Keywords</span></span>

#### <a name="keyword_cc_verification"></a><span data-ttu-id="319ad-1316">Keyword_cc_verification</span><span class="sxs-lookup"><span data-stu-id="319ad-1316">Keyword_cc_verification</span></span>

- <span data-ttu-id="319ad-1317">vérification de la carte</span><span class="sxs-lookup"><span data-stu-id="319ad-1317">card verification</span></span>
- <span data-ttu-id="319ad-1318">numéro d’identification de la carte</span><span class="sxs-lookup"><span data-stu-id="319ad-1318">card identification number</span></span>
- <span data-ttu-id="319ad-1319">cryptogramme</span><span class="sxs-lookup"><span data-stu-id="319ad-1319">cvn</span></span>
- <span data-ttu-id="319ad-1320">nic</span><span class="sxs-lookup"><span data-stu-id="319ad-1320">cid</span></span>
- <span data-ttu-id="319ad-1321">cvc2</span><span class="sxs-lookup"><span data-stu-id="319ad-1321">cvc2</span></span>
- <span data-ttu-id="319ad-1322">cvv2</span><span class="sxs-lookup"><span data-stu-id="319ad-1322">cvv2</span></span>
- <span data-ttu-id="319ad-1323">pin block</span><span class="sxs-lookup"><span data-stu-id="319ad-1323">pin block</span></span>
- <span data-ttu-id="319ad-1324">code de sécurité</span><span class="sxs-lookup"><span data-stu-id="319ad-1324">security code</span></span>
- <span data-ttu-id="319ad-1325">numéro de sécurité</span><span class="sxs-lookup"><span data-stu-id="319ad-1325">security number</span></span>
- <span data-ttu-id="319ad-1326">n° de sécurité</span><span class="sxs-lookup"><span data-stu-id="319ad-1326">security no</span></span>
- <span data-ttu-id="319ad-1327">numéro d’émission</span><span class="sxs-lookup"><span data-stu-id="319ad-1327">issue number</span></span>
- <span data-ttu-id="319ad-1328">n° d’émission</span><span class="sxs-lookup"><span data-stu-id="319ad-1328">issue no</span></span>
- <span data-ttu-id="319ad-1329">cryptogramme</span><span class="sxs-lookup"><span data-stu-id="319ad-1329">cryptogramme</span></span>
- <span data-ttu-id="319ad-1330">numéro de sécurité</span><span class="sxs-lookup"><span data-stu-id="319ad-1330">numéro de sécurité</span></span>
- <span data-ttu-id="319ad-1331">numéro de sécurité</span><span class="sxs-lookup"><span data-stu-id="319ad-1331">numero de securite</span></span>
- <span data-ttu-id="319ad-1332">kreditkartenprüfnummer</span><span class="sxs-lookup"><span data-stu-id="319ad-1332">kreditkartenprüfnummer</span></span>
- <span data-ttu-id="319ad-1333">kreditkartenprufnummer</span><span class="sxs-lookup"><span data-stu-id="319ad-1333">kreditkartenprufnummer</span></span>
- <span data-ttu-id="319ad-1334">prüfziffer</span><span class="sxs-lookup"><span data-stu-id="319ad-1334">prüfziffer</span></span>
- <span data-ttu-id="319ad-1335">prufziffer</span><span class="sxs-lookup"><span data-stu-id="319ad-1335">prufziffer</span></span>
- <span data-ttu-id="319ad-1336">sicherheits Kode</span><span class="sxs-lookup"><span data-stu-id="319ad-1336">sicherheits Kode</span></span>
- <span data-ttu-id="319ad-1337">sicherheitscode</span><span class="sxs-lookup"><span data-stu-id="319ad-1337">sicherheitscode</span></span>
- <span data-ttu-id="319ad-1338">sicherheitsnummer</span><span class="sxs-lookup"><span data-stu-id="319ad-1338">sicherheitsnummer</span></span>
- <span data-ttu-id="319ad-1339">verfalldatum</span><span class="sxs-lookup"><span data-stu-id="319ad-1339">verfalldatum</span></span>
- <span data-ttu-id="319ad-1340">codice di verifica</span><span class="sxs-lookup"><span data-stu-id="319ad-1340">codice di verifica</span></span>
- <span data-ttu-id="319ad-1341">contre.</span><span class="sxs-lookup"><span data-stu-id="319ad-1341">cod.</span></span> <span data-ttu-id="319ad-1342">sicurezza</span><span class="sxs-lookup"><span data-stu-id="319ad-1342">sicurezza</span></span>
- <span data-ttu-id="319ad-1343">cod sicurezza</span><span class="sxs-lookup"><span data-stu-id="319ad-1343">cod sicurezza</span></span>
- <span data-ttu-id="319ad-1344">n autorizzazione</span><span class="sxs-lookup"><span data-stu-id="319ad-1344">n autorizzazione</span></span>
- <span data-ttu-id="319ad-1345">código</span><span class="sxs-lookup"><span data-stu-id="319ad-1345">código</span></span>
- <span data-ttu-id="319ad-1346">codigo</span><span class="sxs-lookup"><span data-stu-id="319ad-1346">codigo</span></span>
- <span data-ttu-id="319ad-1347">contre.</span><span class="sxs-lookup"><span data-stu-id="319ad-1347">cod.</span></span> <span data-ttu-id="319ad-1348">SEG</span><span class="sxs-lookup"><span data-stu-id="319ad-1348">seg</span></span>
- <span data-ttu-id="319ad-1349">cod seg</span><span class="sxs-lookup"><span data-stu-id="319ad-1349">cod seg</span></span>
- <span data-ttu-id="319ad-1350">código de segurança</span><span class="sxs-lookup"><span data-stu-id="319ad-1350">código de segurança</span></span>
- <span data-ttu-id="319ad-1351">codigo de seguranca</span><span class="sxs-lookup"><span data-stu-id="319ad-1351">codigo de seguranca</span></span>
- <span data-ttu-id="319ad-1352">codigo de segurança</span><span class="sxs-lookup"><span data-stu-id="319ad-1352">codigo de segurança</span></span>
- <span data-ttu-id="319ad-1353">código de seguranca</span><span class="sxs-lookup"><span data-stu-id="319ad-1353">código de seguranca</span></span>
- <span data-ttu-id="319ad-1354">cód.</span><span class="sxs-lookup"><span data-stu-id="319ad-1354">cód.</span></span> <span data-ttu-id="319ad-1355">segurança</span><span class="sxs-lookup"><span data-stu-id="319ad-1355">segurança</span></span>
- <span data-ttu-id="319ad-1356">contre.</span><span class="sxs-lookup"><span data-stu-id="319ad-1356">cod.</span></span> <span data-ttu-id="319ad-1357">Seguranca COD.</span><span class="sxs-lookup"><span data-stu-id="319ad-1357">seguranca cod.</span></span> <span data-ttu-id="319ad-1358">segurança</span><span class="sxs-lookup"><span data-stu-id="319ad-1358">segurança</span></span>
- <span data-ttu-id="319ad-1359">cód.</span><span class="sxs-lookup"><span data-stu-id="319ad-1359">cód.</span></span> <span data-ttu-id="319ad-1360">seguranca</span><span class="sxs-lookup"><span data-stu-id="319ad-1360">seguranca</span></span>
- <span data-ttu-id="319ad-1361">cód segurança</span><span class="sxs-lookup"><span data-stu-id="319ad-1361">cód segurança</span></span>
- <span data-ttu-id="319ad-1362">COD Seguranca COD Segurança</span><span class="sxs-lookup"><span data-stu-id="319ad-1362">cod seguranca cod segurança</span></span>
- <span data-ttu-id="319ad-1363">cód seguranca</span><span class="sxs-lookup"><span data-stu-id="319ad-1363">cód seguranca</span></span>
- <span data-ttu-id="319ad-1364">número de verificação</span><span class="sxs-lookup"><span data-stu-id="319ad-1364">número de verificação</span></span>
- <span data-ttu-id="319ad-1365">numero de verificacao</span><span class="sxs-lookup"><span data-stu-id="319ad-1365">numero de verificacao</span></span>
- <span data-ttu-id="319ad-1366">ablauf</span><span class="sxs-lookup"><span data-stu-id="319ad-1366">ablauf</span></span>
- <span data-ttu-id="319ad-1367">gültig bis</span><span class="sxs-lookup"><span data-stu-id="319ad-1367">gültig bis</span></span>
- <span data-ttu-id="319ad-1368">gültigkeitsdatum</span><span class="sxs-lookup"><span data-stu-id="319ad-1368">gültigkeitsdatum</span></span>
- <span data-ttu-id="319ad-1369">gultig bis</span><span class="sxs-lookup"><span data-stu-id="319ad-1369">gultig bis</span></span>
- <span data-ttu-id="319ad-1370">gultigkeitsdatum</span><span class="sxs-lookup"><span data-stu-id="319ad-1370">gultigkeitsdatum</span></span>
- <span data-ttu-id="319ad-1371">scadenza</span><span class="sxs-lookup"><span data-stu-id="319ad-1371">scadenza</span></span>
- <span data-ttu-id="319ad-1372">data scad</span><span class="sxs-lookup"><span data-stu-id="319ad-1372">data scad</span></span>
- <span data-ttu-id="319ad-1373">fecha de expiracion</span><span class="sxs-lookup"><span data-stu-id="319ad-1373">fecha de expiracion</span></span>
- <span data-ttu-id="319ad-1374">fecha de venc</span><span class="sxs-lookup"><span data-stu-id="319ad-1374">fecha de venc</span></span>
- <span data-ttu-id="319ad-1375">vencimiento</span><span class="sxs-lookup"><span data-stu-id="319ad-1375">vencimiento</span></span>
- <span data-ttu-id="319ad-1376">válido hasta</span><span class="sxs-lookup"><span data-stu-id="319ad-1376">válido hasta</span></span>
- <span data-ttu-id="319ad-1377">valido hasta</span><span class="sxs-lookup"><span data-stu-id="319ad-1377">valido hasta</span></span>
- <span data-ttu-id="319ad-1378">vto</span><span class="sxs-lookup"><span data-stu-id="319ad-1378">vto</span></span>
- <span data-ttu-id="319ad-1379">data de expiração</span><span class="sxs-lookup"><span data-stu-id="319ad-1379">data de expiração</span></span>
- <span data-ttu-id="319ad-1380">data de expiracao</span><span class="sxs-lookup"><span data-stu-id="319ad-1380">data de expiracao</span></span>
- <span data-ttu-id="319ad-1381">data em que expira</span><span class="sxs-lookup"><span data-stu-id="319ad-1381">data em que expira</span></span>
- <span data-ttu-id="319ad-1382">validade</span><span class="sxs-lookup"><span data-stu-id="319ad-1382">validade</span></span>
- <span data-ttu-id="319ad-1383">valorisation</span><span class="sxs-lookup"><span data-stu-id="319ad-1383">valor</span></span>
- <span data-ttu-id="319ad-1384">vencimento</span><span class="sxs-lookup"><span data-stu-id="319ad-1384">vencimento</span></span>
- <span data-ttu-id="319ad-1385">Venc</span><span class="sxs-lookup"><span data-stu-id="319ad-1385">Venc</span></span> 

#### <a name="keyword_cc_name"></a><span data-ttu-id="319ad-1386">Keyword_cc_name</span><span class="sxs-lookup"><span data-stu-id="319ad-1386">Keyword_cc_name</span></span>

- <span data-ttu-id="319ad-1387">American</span><span class="sxs-lookup"><span data-stu-id="319ad-1387">amex</span></span>
- <span data-ttu-id="319ad-1388">american express</span><span class="sxs-lookup"><span data-stu-id="319ad-1388">american express</span></span>
- <span data-ttu-id="319ad-1389">americanexpress</span><span class="sxs-lookup"><span data-stu-id="319ad-1389">americanexpress</span></span>
- <span data-ttu-id="319ad-1390">Délivrance</span><span class="sxs-lookup"><span data-stu-id="319ad-1390">Visa</span></span>
- <span data-ttu-id="319ad-1391">MasterCard</span><span class="sxs-lookup"><span data-stu-id="319ad-1391">mastercard</span></span>
- <span data-ttu-id="319ad-1392">master card</span><span class="sxs-lookup"><span data-stu-id="319ad-1392">master card</span></span>
- <span data-ttu-id="319ad-1393">McDonald</span><span class="sxs-lookup"><span data-stu-id="319ad-1393">mc</span></span> 
- <span data-ttu-id="319ad-1394">MasterCard</span><span class="sxs-lookup"><span data-stu-id="319ad-1394">mastercards</span></span>
- <span data-ttu-id="319ad-1395">master cards</span><span class="sxs-lookup"><span data-stu-id="319ad-1395">master cards</span></span>
- <span data-ttu-id="319ad-1396">diner’s Club</span><span class="sxs-lookup"><span data-stu-id="319ad-1396">diner's Club</span></span>
- <span data-ttu-id="319ad-1397">diners club</span><span class="sxs-lookup"><span data-stu-id="319ad-1397">diners club</span></span>
- <span data-ttu-id="319ad-1398">dinersclub</span><span class="sxs-lookup"><span data-stu-id="319ad-1398">dinersclub</span></span>
- <span data-ttu-id="319ad-1399">discover card</span><span class="sxs-lookup"><span data-stu-id="319ad-1399">discover card</span></span>
- <span data-ttu-id="319ad-1400">discovercard</span><span class="sxs-lookup"><span data-stu-id="319ad-1400">discovercard</span></span>
- <span data-ttu-id="319ad-1401">discover cards</span><span class="sxs-lookup"><span data-stu-id="319ad-1401">discover cards</span></span>
- <span data-ttu-id="319ad-1402">JCB</span><span class="sxs-lookup"><span data-stu-id="319ad-1402">JCB</span></span>
- <span data-ttu-id="319ad-1403">japanese card bureau</span><span class="sxs-lookup"><span data-stu-id="319ad-1403">japanese card bureau</span></span>
- <span data-ttu-id="319ad-1404">carte blanche</span><span class="sxs-lookup"><span data-stu-id="319ad-1404">carte blanche</span></span>
- <span data-ttu-id="319ad-1405">carteblanche</span><span class="sxs-lookup"><span data-stu-id="319ad-1405">carteblanche</span></span>
- <span data-ttu-id="319ad-1406">carte de crédit</span><span class="sxs-lookup"><span data-stu-id="319ad-1406">credit card</span></span>
- <span data-ttu-id="319ad-1407">CC #</span><span class="sxs-lookup"><span data-stu-id="319ad-1407">cc#</span></span>
- <span data-ttu-id="319ad-1408">n ° de CC :</span><span class="sxs-lookup"><span data-stu-id="319ad-1408">cc#:</span></span>
- <span data-ttu-id="319ad-1409">date d’expiration</span><span class="sxs-lookup"><span data-stu-id="319ad-1409">expiration date</span></span>
- <span data-ttu-id="319ad-1410">date d’exp</span><span class="sxs-lookup"><span data-stu-id="319ad-1410">exp date</span></span>
- <span data-ttu-id="319ad-1411">date d’expiration</span><span class="sxs-lookup"><span data-stu-id="319ad-1411">expiry date</span></span>
- <span data-ttu-id="319ad-1412">date d’expiration</span><span class="sxs-lookup"><span data-stu-id="319ad-1412">date d’expiration</span></span>
- <span data-ttu-id="319ad-1413">date d’exp</span><span class="sxs-lookup"><span data-stu-id="319ad-1413">date d'exp</span></span>
- <span data-ttu-id="319ad-1414">date expiration</span><span class="sxs-lookup"><span data-stu-id="319ad-1414">date expiration</span></span>
- <span data-ttu-id="319ad-1415">carte bancaire</span><span class="sxs-lookup"><span data-stu-id="319ad-1415">bank card</span></span>
- <span data-ttu-id="319ad-1416">bankcard</span><span class="sxs-lookup"><span data-stu-id="319ad-1416">bankcard</span></span>
- <span data-ttu-id="319ad-1417">numéro de carte</span><span class="sxs-lookup"><span data-stu-id="319ad-1417">card number</span></span>
- <span data-ttu-id="319ad-1418">num de carte</span><span class="sxs-lookup"><span data-stu-id="319ad-1418">card num</span></span>
- <span data-ttu-id="319ad-1419">carte</span><span class="sxs-lookup"><span data-stu-id="319ad-1419">cardnumber</span></span>
- <span data-ttu-id="319ad-1420">carte</span><span class="sxs-lookup"><span data-stu-id="319ad-1420">cardnumbers</span></span>
- <span data-ttu-id="319ad-1421">numéros de carte</span><span class="sxs-lookup"><span data-stu-id="319ad-1421">card numbers</span></span>
- <span data-ttu-id="319ad-1422">CreditCard</span><span class="sxs-lookup"><span data-stu-id="319ad-1422">creditcard</span></span>
- <span data-ttu-id="319ad-1423">cartes de crédit</span><span class="sxs-lookup"><span data-stu-id="319ad-1423">credit cards</span></span>
- <span data-ttu-id="319ad-1424">crédit</span><span class="sxs-lookup"><span data-stu-id="319ad-1424">creditcards</span></span>
- <span data-ttu-id="319ad-1425">CCN</span><span class="sxs-lookup"><span data-stu-id="319ad-1425">ccn</span></span>
- <span data-ttu-id="319ad-1426">titulaire de la carte</span><span class="sxs-lookup"><span data-stu-id="319ad-1426">card holder</span></span>
- <span data-ttu-id="319ad-1427">titulaires</span><span class="sxs-lookup"><span data-stu-id="319ad-1427">cardholder</span></span>
- <span data-ttu-id="319ad-1428">titulaires de la carte</span><span class="sxs-lookup"><span data-stu-id="319ad-1428">card holders</span></span>
- <span data-ttu-id="319ad-1429">titulaires</span><span class="sxs-lookup"><span data-stu-id="319ad-1429">cardholders</span></span>
- <span data-ttu-id="319ad-1430">carte de vérification</span><span class="sxs-lookup"><span data-stu-id="319ad-1430">check card</span></span>
- <span data-ttu-id="319ad-1431">carte</span><span class="sxs-lookup"><span data-stu-id="319ad-1431">checkcard</span></span>
- <span data-ttu-id="319ad-1432">cartes de vérification</span><span class="sxs-lookup"><span data-stu-id="319ad-1432">check cards</span></span>
- <span data-ttu-id="319ad-1433">cartes</span><span class="sxs-lookup"><span data-stu-id="319ad-1433">checkcards</span></span>
- <span data-ttu-id="319ad-1434">carte de débit</span><span class="sxs-lookup"><span data-stu-id="319ad-1434">debit card</span></span>
- <span data-ttu-id="319ad-1435">débit</span><span class="sxs-lookup"><span data-stu-id="319ad-1435">debitcard</span></span>
- <span data-ttu-id="319ad-1436">cartes de débit</span><span class="sxs-lookup"><span data-stu-id="319ad-1436">debit cards</span></span>
- <span data-ttu-id="319ad-1437">débit</span><span class="sxs-lookup"><span data-stu-id="319ad-1437">debitcards</span></span>
- <span data-ttu-id="319ad-1438">carte de retrait</span><span class="sxs-lookup"><span data-stu-id="319ad-1438">atm card</span></span>
- <span data-ttu-id="319ad-1439">retrait</span><span class="sxs-lookup"><span data-stu-id="319ad-1439">atmcard</span></span>
- <span data-ttu-id="319ad-1440">cartes de retrait</span><span class="sxs-lookup"><span data-stu-id="319ad-1440">atm cards</span></span>
- <span data-ttu-id="319ad-1441">retrait</span><span class="sxs-lookup"><span data-stu-id="319ad-1441">atmcards</span></span>
- <span data-ttu-id="319ad-1442">envoier</span><span class="sxs-lookup"><span data-stu-id="319ad-1442">enroute</span></span>
- <span data-ttu-id="319ad-1443">en route</span><span class="sxs-lookup"><span data-stu-id="319ad-1443">en route</span></span>
- <span data-ttu-id="319ad-1444">type de carte</span><span class="sxs-lookup"><span data-stu-id="319ad-1444">card type</span></span>
- <span data-ttu-id="319ad-1445">carte bancaire</span><span class="sxs-lookup"><span data-stu-id="319ad-1445">carte bancaire</span></span>
- <span data-ttu-id="319ad-1446">carte de crédit</span><span class="sxs-lookup"><span data-stu-id="319ad-1446">carte de crédit</span></span>
- <span data-ttu-id="319ad-1447">carte de credit</span><span class="sxs-lookup"><span data-stu-id="319ad-1447">carte de credit</span></span>
- <span data-ttu-id="319ad-1448">numéro de carte</span><span class="sxs-lookup"><span data-stu-id="319ad-1448">numéro de carte</span></span>
- <span data-ttu-id="319ad-1449">numero de carte</span><span class="sxs-lookup"><span data-stu-id="319ad-1449">numero de carte</span></span>
- <span data-ttu-id="319ad-1450">nº de la carte</span><span class="sxs-lookup"><span data-stu-id="319ad-1450">nº de la carte</span></span>
- <span data-ttu-id="319ad-1451">nº de carte</span><span class="sxs-lookup"><span data-stu-id="319ad-1451">nº de carte</span></span>
- <span data-ttu-id="319ad-1452">kreditkarte</span><span class="sxs-lookup"><span data-stu-id="319ad-1452">kreditkarte</span></span>
- <span data-ttu-id="319ad-1453">karte</span><span class="sxs-lookup"><span data-stu-id="319ad-1453">karte</span></span>
- <span data-ttu-id="319ad-1454">karteninhaber</span><span class="sxs-lookup"><span data-stu-id="319ad-1454">karteninhaber</span></span>
- <span data-ttu-id="319ad-1455">karteninhabers</span><span class="sxs-lookup"><span data-stu-id="319ad-1455">karteninhabers</span></span>
- <span data-ttu-id="319ad-1456">kreditkarteninhaber</span><span class="sxs-lookup"><span data-stu-id="319ad-1456">kreditkarteninhaber</span></span>
- <span data-ttu-id="319ad-1457">kreditkarteninstitut</span><span class="sxs-lookup"><span data-stu-id="319ad-1457">kreditkarteninstitut</span></span>
- <span data-ttu-id="319ad-1458">kreditkartentyp</span><span class="sxs-lookup"><span data-stu-id="319ad-1458">kreditkartentyp</span></span>
- <span data-ttu-id="319ad-1459">eigentümername</span><span class="sxs-lookup"><span data-stu-id="319ad-1459">eigentümername</span></span>
- <span data-ttu-id="319ad-1460">kartennr</span><span class="sxs-lookup"><span data-stu-id="319ad-1460">kartennr</span></span> 
- <span data-ttu-id="319ad-1461">kartennummer</span><span class="sxs-lookup"><span data-stu-id="319ad-1461">kartennummer</span></span>
- <span data-ttu-id="319ad-1462">kreditkartennummer</span><span class="sxs-lookup"><span data-stu-id="319ad-1462">kreditkartennummer</span></span>
- <span data-ttu-id="319ad-1463">kreditkarten-nummer</span><span class="sxs-lookup"><span data-stu-id="319ad-1463">kreditkarten-nummer</span></span>
- <span data-ttu-id="319ad-1464">Carta di credito</span><span class="sxs-lookup"><span data-stu-id="319ad-1464">carta di credito</span></span>
- <span data-ttu-id="319ad-1465">Carta credito</span><span class="sxs-lookup"><span data-stu-id="319ad-1465">carta credito</span></span>
- <span data-ttu-id="319ad-1466">Carta</span><span class="sxs-lookup"><span data-stu-id="319ad-1466">carta</span></span>
- <span data-ttu-id="319ad-1467">n carta</span><span class="sxs-lookup"><span data-stu-id="319ad-1467">n carta</span></span>
- <span data-ttu-id="319ad-1468">Nr.</span><span class="sxs-lookup"><span data-stu-id="319ad-1468">nr.</span></span> <span data-ttu-id="319ad-1469">Carta</span><span class="sxs-lookup"><span data-stu-id="319ad-1469">carta</span></span>
- <span data-ttu-id="319ad-1470">nr carta</span><span class="sxs-lookup"><span data-stu-id="319ad-1470">nr carta</span></span>
- <span data-ttu-id="319ad-1471">numero carta</span><span class="sxs-lookup"><span data-stu-id="319ad-1471">numero carta</span></span>
- <span data-ttu-id="319ad-1472">numero della carta</span><span class="sxs-lookup"><span data-stu-id="319ad-1472">numero della carta</span></span>
- <span data-ttu-id="319ad-1473">numero di carta</span><span class="sxs-lookup"><span data-stu-id="319ad-1473">numero di carta</span></span>
- <span data-ttu-id="319ad-1474">tarjeta credito</span><span class="sxs-lookup"><span data-stu-id="319ad-1474">tarjeta credito</span></span>
- <span data-ttu-id="319ad-1475">tarjeta de credito</span><span class="sxs-lookup"><span data-stu-id="319ad-1475">tarjeta de credito</span></span>
- <span data-ttu-id="319ad-1476">tarjeta crédito</span><span class="sxs-lookup"><span data-stu-id="319ad-1476">tarjeta crédito</span></span>
- <span data-ttu-id="319ad-1477">tarjeta de crédito</span><span class="sxs-lookup"><span data-stu-id="319ad-1477">tarjeta de crédito</span></span>
- <span data-ttu-id="319ad-1478">tarjeta de atm</span><span class="sxs-lookup"><span data-stu-id="319ad-1478">tarjeta de atm</span></span>
- <span data-ttu-id="319ad-1479">tarjeta atm</span><span class="sxs-lookup"><span data-stu-id="319ad-1479">tarjeta atm</span></span>
- <span data-ttu-id="319ad-1480">tarjeta debito</span><span class="sxs-lookup"><span data-stu-id="319ad-1480">tarjeta debito</span></span>
- <span data-ttu-id="319ad-1481">tarjeta de debito</span><span class="sxs-lookup"><span data-stu-id="319ad-1481">tarjeta de debito</span></span>
- <span data-ttu-id="319ad-1482">tarjeta débito</span><span class="sxs-lookup"><span data-stu-id="319ad-1482">tarjeta débito</span></span>
- <span data-ttu-id="319ad-1483">tarjeta de débito</span><span class="sxs-lookup"><span data-stu-id="319ad-1483">tarjeta de débito</span></span>
- <span data-ttu-id="319ad-1484">nº de tarjeta</span><span class="sxs-lookup"><span data-stu-id="319ad-1484">nº de tarjeta</span></span>
- <span data-ttu-id="319ad-1485">Nbre.</span><span class="sxs-lookup"><span data-stu-id="319ad-1485">no.</span></span> <span data-ttu-id="319ad-1486">de tarjeta</span><span class="sxs-lookup"><span data-stu-id="319ad-1486">de tarjeta</span></span>
- <span data-ttu-id="319ad-1487">no de tarjeta</span><span class="sxs-lookup"><span data-stu-id="319ad-1487">no de tarjeta</span></span>
- <span data-ttu-id="319ad-1488">numero de tarjeta</span><span class="sxs-lookup"><span data-stu-id="319ad-1488">numero de tarjeta</span></span>
- <span data-ttu-id="319ad-1489">número de tarjeta</span><span class="sxs-lookup"><span data-stu-id="319ad-1489">número de tarjeta</span></span>
- <span data-ttu-id="319ad-1490">tarjeta no</span><span class="sxs-lookup"><span data-stu-id="319ad-1490">tarjeta no</span></span>
- <span data-ttu-id="319ad-1491">tarjetahabiente</span><span class="sxs-lookup"><span data-stu-id="319ad-1491">tarjetahabiente</span></span>
- <span data-ttu-id="319ad-1492">cartão de crédito</span><span class="sxs-lookup"><span data-stu-id="319ad-1492">cartão de crédito</span></span>
- <span data-ttu-id="319ad-1493">cartão de credito</span><span class="sxs-lookup"><span data-stu-id="319ad-1493">cartão de credito</span></span>
- <span data-ttu-id="319ad-1494">cartao de crédito</span><span class="sxs-lookup"><span data-stu-id="319ad-1494">cartao de crédito</span></span>
- <span data-ttu-id="319ad-1495">cartao de credito</span><span class="sxs-lookup"><span data-stu-id="319ad-1495">cartao de credito</span></span>
- <span data-ttu-id="319ad-1496">cartão de débito</span><span class="sxs-lookup"><span data-stu-id="319ad-1496">cartão de débito</span></span>
- <span data-ttu-id="319ad-1497">cartao de débito</span><span class="sxs-lookup"><span data-stu-id="319ad-1497">cartao de débito</span></span>
- <span data-ttu-id="319ad-1498">cartão de debito</span><span class="sxs-lookup"><span data-stu-id="319ad-1498">cartão de debito</span></span>
- <span data-ttu-id="319ad-1499">cartao de debito</span><span class="sxs-lookup"><span data-stu-id="319ad-1499">cartao de debito</span></span>
- <span data-ttu-id="319ad-1500">débito automático</span><span class="sxs-lookup"><span data-stu-id="319ad-1500">débito automático</span></span>
- <span data-ttu-id="319ad-1501">debito automatico</span><span class="sxs-lookup"><span data-stu-id="319ad-1501">debito automatico</span></span>
- <span data-ttu-id="319ad-1502">número do cartão</span><span class="sxs-lookup"><span data-stu-id="319ad-1502">número do cartão</span></span>
- <span data-ttu-id="319ad-1503">numero do cartão</span><span class="sxs-lookup"><span data-stu-id="319ad-1503">numero do cartão</span></span> 
- <span data-ttu-id="319ad-1504">número do cartao</span><span class="sxs-lookup"><span data-stu-id="319ad-1504">número do cartao</span></span>
- <span data-ttu-id="319ad-1505">numero do cartao</span><span class="sxs-lookup"><span data-stu-id="319ad-1505">numero do cartao</span></span>
- <span data-ttu-id="319ad-1506">número de cartão</span><span class="sxs-lookup"><span data-stu-id="319ad-1506">número de cartão</span></span>
- <span data-ttu-id="319ad-1507">numero de cartão</span><span class="sxs-lookup"><span data-stu-id="319ad-1507">numero de cartão</span></span>
- <span data-ttu-id="319ad-1508">número de cartao</span><span class="sxs-lookup"><span data-stu-id="319ad-1508">número de cartao</span></span>
- <span data-ttu-id="319ad-1509">numero de cartao</span><span class="sxs-lookup"><span data-stu-id="319ad-1509">numero de cartao</span></span>
- <span data-ttu-id="319ad-1510">nº do cartão</span><span class="sxs-lookup"><span data-stu-id="319ad-1510">nº do cartão</span></span>
- <span data-ttu-id="319ad-1511">nº do cartao</span><span class="sxs-lookup"><span data-stu-id="319ad-1511">nº do cartao</span></span>
- <span data-ttu-id="319ad-1512">n º.</span><span class="sxs-lookup"><span data-stu-id="319ad-1512">nº.</span></span> <span data-ttu-id="319ad-1513">do cartão</span><span class="sxs-lookup"><span data-stu-id="319ad-1513">do cartão</span></span>
- <span data-ttu-id="319ad-1514">no do cartão</span><span class="sxs-lookup"><span data-stu-id="319ad-1514">no do cartão</span></span>
- <span data-ttu-id="319ad-1515">no do cartao</span><span class="sxs-lookup"><span data-stu-id="319ad-1515">no do cartao</span></span>
- <span data-ttu-id="319ad-1516">Nbre.</span><span class="sxs-lookup"><span data-stu-id="319ad-1516">no.</span></span> <span data-ttu-id="319ad-1517">do cartão</span><span class="sxs-lookup"><span data-stu-id="319ad-1517">do cartão</span></span>
- <span data-ttu-id="319ad-1518">Nbre.</span><span class="sxs-lookup"><span data-stu-id="319ad-1518">no.</span></span> <span data-ttu-id="319ad-1519">do cartao</span><span class="sxs-lookup"><span data-stu-id="319ad-1519">do cartao</span></span> 
   
## <a name="croatia-identity-card-number"></a><span data-ttu-id="319ad-1520">	Numéro de carte d’identité Croatie</span><span class="sxs-lookup"><span data-stu-id="319ad-1520">Croatia Identity Card Number</span></span>

### <a name="format"></a><span data-ttu-id="319ad-1521">Format</span><span class="sxs-lookup"><span data-stu-id="319ad-1521">Format</span></span>

<span data-ttu-id="319ad-1522">Neuf chiffres</span><span class="sxs-lookup"><span data-stu-id="319ad-1522">Nine digits</span></span>

### <a name="pattern"></a><span data-ttu-id="319ad-1523">Modèle</span><span class="sxs-lookup"><span data-stu-id="319ad-1523">Pattern</span></span>

<span data-ttu-id="319ad-1524">Neuf chiffres consécutifs</span><span class="sxs-lookup"><span data-stu-id="319ad-1524">Nine consecutive digits</span></span>

### <a name="checksum"></a><span data-ttu-id="319ad-1525">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="319ad-1525">Checksum</span></span>

<span data-ttu-id="319ad-1526">Non</span><span class="sxs-lookup"><span data-stu-id="319ad-1526">No</span></span>

### <a name="definition"></a><span data-ttu-id="319ad-1527">Définition</span><span class="sxs-lookup"><span data-stu-id="319ad-1527">Definition</span></span>

<span data-ttu-id="319ad-1528">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="319ad-1528">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="319ad-1529">La fonction Func_croatia_id_card trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="319ad-1529">The function Func_croatia_id_card finds content that matches the pattern.</span></span>
- <span data-ttu-id="319ad-1530">Un mot clé figurant dans la liste Keyword_croatia_id_card est trouvé.</span><span class="sxs-lookup"><span data-stu-id="319ad-1530">A keyword from Keyword_croatia_id_card is found.</span></span>

```xml
<!--Croatia Identity Card Number-->
<Entity id="ff12f884-c20a-4189-b185-34c8e7258d47" recommendedConfidence="75" patternsProximity="300">
  <Pattern confidenceLevel="75">
     <IdMatch idRef="Func_croatia_id_card"/>
     <Match idRef="Keyword_croatia_id_card"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="319ad-1531">Mots-clés</span><span class="sxs-lookup"><span data-stu-id="319ad-1531">Keywords</span></span>

#### <a name="keyword_croatia_id_card"></a><span data-ttu-id="319ad-1532">Keyword_croatia_id_card</span><span class="sxs-lookup"><span data-stu-id="319ad-1532">Keyword_croatia_id_card</span></span>

- <span data-ttu-id="319ad-1533">Croatian identity card</span><span class="sxs-lookup"><span data-stu-id="319ad-1533">Croatian identity card</span></span>
- <span data-ttu-id="319ad-1534">Osobna iskaznica</span><span class="sxs-lookup"><span data-stu-id="319ad-1534">Osobna iskaznica</span></span>

   
## <a name="croatia-personal-identification-oib-number"></a><span data-ttu-id="319ad-1535">	Numéro d’identification personnel (OIB) Croatie</span><span class="sxs-lookup"><span data-stu-id="319ad-1535">Croatia Personal Identification (OIB) Number</span></span>

### <a name="format"></a><span data-ttu-id="319ad-1536">Format</span><span class="sxs-lookup"><span data-stu-id="319ad-1536">Format</span></span>

<span data-ttu-id="319ad-1537">11 chiffres</span><span class="sxs-lookup"><span data-stu-id="319ad-1537">11 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="319ad-1538">Modèle</span><span class="sxs-lookup"><span data-stu-id="319ad-1538">Pattern</span></span>

<span data-ttu-id="319ad-1539">11 chiffres :</span><span class="sxs-lookup"><span data-stu-id="319ad-1539">11 digits:</span></span>
- <span data-ttu-id="319ad-1540">10 chiffres</span><span class="sxs-lookup"><span data-stu-id="319ad-1540">10 digits</span></span> 
- <span data-ttu-id="319ad-1541">Le chiffre final est un chiffre de contrôle aux fins de l’échange de données internationales, les lettres HR sont ajoutées avant les onze chiffres.</span><span class="sxs-lookup"><span data-stu-id="319ad-1541">Final digit is a check digit For the purposes of international data exchange, the letters HR are added preceding the eleven digits.</span></span>

### <a name="checksum"></a><span data-ttu-id="319ad-1542">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="319ad-1542">Checksum</span></span>

<span data-ttu-id="319ad-1543">Oui</span><span class="sxs-lookup"><span data-stu-id="319ad-1543">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="319ad-1544">Définition</span><span class="sxs-lookup"><span data-stu-id="319ad-1544">Definition</span></span>

<span data-ttu-id="319ad-1545">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="319ad-1545">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="319ad-1546">La fonction Func_croatia_oib_number trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="319ad-1546">The function Func_croatia_oib_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="319ad-1547">Un mot clé figurant dans la liste Keyword_croatia_oib_number est trouvé.</span><span class="sxs-lookup"><span data-stu-id="319ad-1547">A keyword from Keyword_croatia_oib_number is found.</span></span>
- <span data-ttu-id="319ad-1548">La somme de contrôle est correcte.</span><span class="sxs-lookup"><span data-stu-id="319ad-1548">The checksum passes.</span></span>

<span data-ttu-id="319ad-1549">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="319ad-1549">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="319ad-1550">La fonction Func_croatia_oib_number trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="319ad-1550">The function Func_croatia_oib_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="319ad-1551">La somme de contrôle est correcte.</span><span class="sxs-lookup"><span data-stu-id="319ad-1551">The checksum passes.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="319ad-1552">Mots-clés</span><span class="sxs-lookup"><span data-stu-id="319ad-1552">Keywords</span></span>

#### <a name="keyword_croatia_oib_number"></a><span data-ttu-id="319ad-1553">Keyword_croatia_oib_number</span><span class="sxs-lookup"><span data-stu-id="319ad-1553">Keyword_croatia_oib_number</span></span>

- <span data-ttu-id="319ad-1554">Personal Identification Number</span><span class="sxs-lookup"><span data-stu-id="319ad-1554">Personal Identification Number</span></span>
- <span data-ttu-id="319ad-1555">Osobni identifikacijski broj</span><span class="sxs-lookup"><span data-stu-id="319ad-1555">Osobni identifikacijski broj</span></span> 
- <span data-ttu-id="319ad-1556">OIB</span><span class="sxs-lookup"><span data-stu-id="319ad-1556">OIB</span></span> 

   
## <a name="czech-personal-identity-number"></a><span data-ttu-id="319ad-1557">Numéro d’identité personnelle tchèque</span><span class="sxs-lookup"><span data-stu-id="319ad-1557">Czech Personal Identity Number</span></span>

### <a name="format"></a><span data-ttu-id="319ad-1558">Format</span><span class="sxs-lookup"><span data-stu-id="319ad-1558">Format</span></span>

<span data-ttu-id="319ad-1559">Neuf chiffres avec une barre oblique inverse facultative (ancien format) 10 chiffres avec une barre oblique facultative (nouveau format)</span><span class="sxs-lookup"><span data-stu-id="319ad-1559">Nine digits with optional forward slash (old format) 10 digits with optional forward slash (new format)</span></span>

### <a name="pattern"></a><span data-ttu-id="319ad-1560">Modèle</span><span class="sxs-lookup"><span data-stu-id="319ad-1560">Pattern</span></span>

<span data-ttu-id="319ad-1561">Neuf chiffres (ancien format) :</span><span class="sxs-lookup"><span data-stu-id="319ad-1561">Nine digits (old format):</span></span>
- <span data-ttu-id="319ad-1562">Neuf chiffres</span><span class="sxs-lookup"><span data-stu-id="319ad-1562">Nine digits</span></span>

<span data-ttu-id="319ad-1563">OU</span><span class="sxs-lookup"><span data-stu-id="319ad-1563">OR</span></span>

- <span data-ttu-id="319ad-1564">Six chiffres qui représentent la date de naissance</span><span class="sxs-lookup"><span data-stu-id="319ad-1564">Six digits that represent date of birth</span></span>
- <span data-ttu-id="319ad-1565">Une barre oblique </span><span class="sxs-lookup"><span data-stu-id="319ad-1565">A forward slash</span></span>
- <span data-ttu-id="319ad-1566">Trois chiffres</span><span class="sxs-lookup"><span data-stu-id="319ad-1566">Three digits</span></span>

<span data-ttu-id="319ad-1567">10 chiffres (nouveau format) :</span><span class="sxs-lookup"><span data-stu-id="319ad-1567">10 digits (new format):</span></span>
- <span data-ttu-id="319ad-1568">10 chiffres</span><span class="sxs-lookup"><span data-stu-id="319ad-1568">10 digits</span></span>

<span data-ttu-id="319ad-1569">OU</span><span class="sxs-lookup"><span data-stu-id="319ad-1569">OR</span></span>

- <span data-ttu-id="319ad-1570">Six chiffres qui représentent la date de naissance</span><span class="sxs-lookup"><span data-stu-id="319ad-1570">Six digits that represent date of birth</span></span>
- <span data-ttu-id="319ad-1571">Une barre oblique </span><span class="sxs-lookup"><span data-stu-id="319ad-1571">A forward slash</span></span> 
- <span data-ttu-id="319ad-1572">Quatre chiffres où le dernier chiffre est un chiffre de contrôle</span><span class="sxs-lookup"><span data-stu-id="319ad-1572">Four digits where last digit is a check digit</span></span>

### <a name="checksum"></a><span data-ttu-id="319ad-1573">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="319ad-1573">Checksum</span></span>

<span data-ttu-id="319ad-1574">Oui</span><span class="sxs-lookup"><span data-stu-id="319ad-1574">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="319ad-1575">Définition</span><span class="sxs-lookup"><span data-stu-id="319ad-1575">Definition</span></span>

<span data-ttu-id="319ad-1576">Une stratégie DLP est sûre à 85% d’avoir détecté ce type d’informations sensibles si, dans une proximité de 300 caractères : la fonction Func_czech_id_card trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="319ad-1576">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters: The function Func_czech_id_card finds content that matches the pattern.</span></span>
<span data-ttu-id="319ad-1577">Un mot clé figurant dans la liste Keyword_czech_id_card est trouvé.</span><span class="sxs-lookup"><span data-stu-id="319ad-1577">A keyword from Keyword_czech_id_card is found.</span></span>
<span data-ttu-id="319ad-1578">La somme de contrôle est correcte.</span><span class="sxs-lookup"><span data-stu-id="319ad-1578">The checksum passes.</span></span>

```xml
<!-- Czech Personal Identity Number -->
<Entity id="60c0725a-4eb6-455b-9dda-05d8a7396497"      patternsProximity="300" recommendedConfidence="85">
   <Pattern confidenceLevel="85">
      <IdMatch idRef="Func_czech_id_card" />
      <Match idRef="Keyword_czech_id_card" />
   </Pattern>
</Entity>
```
### <a name="keywords"></a><span data-ttu-id="319ad-1579">Mots-clés</span><span class="sxs-lookup"><span data-stu-id="319ad-1579">Keywords</span></span>

- <span data-ttu-id="319ad-1580">Numéro d’identité personnelle tchèque</span><span class="sxs-lookup"><span data-stu-id="319ad-1580">czech personal identity number</span></span>
- <span data-ttu-id="319ad-1581">Rodné číslo</span><span class="sxs-lookup"><span data-stu-id="319ad-1581">Rodné číslo</span></span>
   
## <a name="denmark-personal-identification-number"></a><span data-ttu-id="319ad-1582">	Numéro d’identification personnel Danemark</span><span class="sxs-lookup"><span data-stu-id="319ad-1582">Denmark Personal Identification Number</span></span>

### <a name="format"></a><span data-ttu-id="319ad-1583">Format</span><span class="sxs-lookup"><span data-stu-id="319ad-1583">Format</span></span>

<span data-ttu-id="319ad-1584">10 chiffres contenant un trait d’union</span><span class="sxs-lookup"><span data-stu-id="319ad-1584">10 digits containing a hyphen</span></span>

### <a name="pattern"></a><span data-ttu-id="319ad-1585">Modèle</span><span class="sxs-lookup"><span data-stu-id="319ad-1585">Pattern</span></span>

<span data-ttu-id="319ad-1586">10 chiffres :</span><span class="sxs-lookup"><span data-stu-id="319ad-1586">10 digits:</span></span>
- <span data-ttu-id="319ad-1587">Six chiffres au format JJMMAA qui correspondent à la date de naissance </span><span class="sxs-lookup"><span data-stu-id="319ad-1587">Six digits in the format DDMMYY which are the date of birth</span></span> 
- <span data-ttu-id="319ad-1588">Un trait d’union </span><span class="sxs-lookup"><span data-stu-id="319ad-1588">A hyphen</span></span> 
- <span data-ttu-id="319ad-1589">Quatre chiffres où le dernier chiffre est un chiffre de contrôle</span><span class="sxs-lookup"><span data-stu-id="319ad-1589">Four digits where the final digit is a check digit</span></span>

### <a name="checksum"></a><span data-ttu-id="319ad-1590">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="319ad-1590">Checksum</span></span>

<span data-ttu-id="319ad-1591">Oui</span><span class="sxs-lookup"><span data-stu-id="319ad-1591">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="319ad-1592">Définition</span><span class="sxs-lookup"><span data-stu-id="319ad-1592">Definition</span></span>

<span data-ttu-id="319ad-1593">Une stratégie DLP est sûre à 75% d’avoir détecté ce type d’informations sensibles si, dans une proximité de 300 caractères : l’expression régulière Regex_denmark_id trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="319ad-1593">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters: The regular expression Regex_denmark_id finds content that matches the pattern.</span></span>
<span data-ttu-id="319ad-1594">Un mot clé figurant dans la liste Keyword_denmark_id est trouvé.</span><span class="sxs-lookup"><span data-stu-id="319ad-1594">A keyword from Keyword_denmark_id is found.</span></span>
<span data-ttu-id="319ad-1595">La somme de contrôle est correcte.</span><span class="sxs-lookup"><span data-stu-id="319ad-1595">The checksum passes.</span></span>

```xml
<!-- Denmark Personal Identification Number -->
<Entity id="6c4f2fef-56e1-4c00-8093-88d7a01cf460" recommendedConfidence="75" patternsProximity="300">
  <Pattern confidenceLevel="75">
     <IdMatch idRef="Regex_denmark_id"/>
     <Match idRef="Keyword_denmark_id"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="319ad-1596">Mots-clés</span><span class="sxs-lookup"><span data-stu-id="319ad-1596">Keywords</span></span>

#### <a name="keyword_denmark_id"></a><span data-ttu-id="319ad-1597">Keyword_denmark_id</span><span class="sxs-lookup"><span data-stu-id="319ad-1597">Keyword_denmark_id</span></span>

- <span data-ttu-id="319ad-1598">Personal Identification Number</span><span class="sxs-lookup"><span data-stu-id="319ad-1598">Personal Identification Number</span></span>
- <span data-ttu-id="319ad-1599">CARDIO</span><span class="sxs-lookup"><span data-stu-id="319ad-1599">CPR</span></span>
- <span data-ttu-id="319ad-1600">Det Centrale Personregister</span><span class="sxs-lookup"><span data-stu-id="319ad-1600">Det Centrale Personregister</span></span>
- <span data-ttu-id="319ad-1601">Personnummer</span><span class="sxs-lookup"><span data-stu-id="319ad-1601">Personnummer</span></span>
   
## <a name="drug-enforcement-agency-dea-number"></a><span data-ttu-id="319ad-1602">Numéro de la Drug Enforcement Agency (DEA)</span><span class="sxs-lookup"><span data-stu-id="319ad-1602">Drug Enforcement Agency (DEA) Number</span></span>

### <a name="format"></a><span data-ttu-id="319ad-1603">Format</span><span class="sxs-lookup"><span data-stu-id="319ad-1603">Format</span></span>

<span data-ttu-id="319ad-1604">Deux lettres suivies de sept chiffres</span><span class="sxs-lookup"><span data-stu-id="319ad-1604">Two letters followed by seven digits</span></span>

### <a name="pattern"></a><span data-ttu-id="319ad-1605">Modèle</span><span class="sxs-lookup"><span data-stu-id="319ad-1605">Pattern</span></span>

<span data-ttu-id="319ad-1606">Le modèle doit inclure tous les éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="319ad-1606">Pattern must include all of the following:</span></span>
- <span data-ttu-id="319ad-1607">Une lettre (ne respecte pas la casse) à partir de cet ensemble de lettres possibles : abcdefghjklmnprstux, qui est un code d’utilisateur enregistré</span><span class="sxs-lookup"><span data-stu-id="319ad-1607">One letter (not case sensitive) from this set of possible letters: abcdefghjklmnprstux, which is a registrant code</span></span> 
- <span data-ttu-id="319ad-1608">Une lettre (ne respecte pas la casse), qui est la première lettre du nom de l’utilisateur enregistré</span><span class="sxs-lookup"><span data-stu-id="319ad-1608">One letter (not case sensitive), which is the first letter of the registrant's last name</span></span> 
- <span data-ttu-id="319ad-1609">Sept chiffres, le dernier est le chiffre de contrôle</span><span class="sxs-lookup"><span data-stu-id="319ad-1609">Seven digits, the last of which is the check digit</span></span>

### <a name="checksum"></a><span data-ttu-id="319ad-1610">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="319ad-1610">Checksum</span></span>

<span data-ttu-id="319ad-1611">Oui</span><span class="sxs-lookup"><span data-stu-id="319ad-1611">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="319ad-1612">Définition</span><span class="sxs-lookup"><span data-stu-id="319ad-1612">Definition</span></span>

<span data-ttu-id="319ad-1613">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="319ad-1613">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="319ad-1614">La fonction Func_dea_number trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="319ad-1614">The function Func_dea_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="319ad-1615">La somme de contrôle est correcte.</span><span class="sxs-lookup"><span data-stu-id="319ad-1615">The checksum passes.</span></span>

```xml
<!-- DEA Number -->
<Entity id="9a5445ad-406e-43eb-8bd7-cac17ab6d0e4" recommendedConfidence="85" patternsProximity="300">
  <Pattern confidenceLevel="85">
     <IdMatch idRef="Func_dea_number"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="319ad-1616">Mots-clés</span><span class="sxs-lookup"><span data-stu-id="319ad-1616">Keywords</span></span>

<span data-ttu-id="319ad-1617">Aucun</span><span class="sxs-lookup"><span data-stu-id="319ad-1617">None</span></span>

   
## <a name="eu-debit-card-number"></a><span data-ttu-id="319ad-1618">Numéro de carte de débit Union européenne</span><span class="sxs-lookup"><span data-stu-id="319ad-1618">EU Debit Card Number</span></span>

### <a name="format"></a><span data-ttu-id="319ad-1619">Format</span><span class="sxs-lookup"><span data-stu-id="319ad-1619">Format</span></span>

<span data-ttu-id="319ad-1620">16 chiffres</span><span class="sxs-lookup"><span data-stu-id="319ad-1620">16 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="319ad-1621">Modèle</span><span class="sxs-lookup"><span data-stu-id="319ad-1621">Pattern</span></span>

<span data-ttu-id="319ad-1622">Modèle très complexe et puissant</span><span class="sxs-lookup"><span data-stu-id="319ad-1622">Very complex and robust pattern</span></span>

### <a name="checksum"></a><span data-ttu-id="319ad-1623">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="319ad-1623">Checksum</span></span>

<span data-ttu-id="319ad-1624">Oui</span><span class="sxs-lookup"><span data-stu-id="319ad-1624">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="319ad-1625">Définition</span><span class="sxs-lookup"><span data-stu-id="319ad-1625">Definition</span></span>

<span data-ttu-id="319ad-1626">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="319ad-1626">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="319ad-1627">La fonction Func_eu_debit_card trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="319ad-1627">The function Func_eu_debit_card finds content that matches the pattern.</span></span>
- <span data-ttu-id="319ad-1628">Au moins une des affirmations suivantes est vraie :</span><span class="sxs-lookup"><span data-stu-id="319ad-1628">At least one of the following is true:</span></span>
    - <span data-ttu-id="319ad-1629">Un mot clé figurant dans la liste Keyword_eu_debit_card est trouvé.</span><span class="sxs-lookup"><span data-stu-id="319ad-1629">A keyword from Keyword_eu_debit_card is found.</span></span>
    - <span data-ttu-id="319ad-1630">Un mot clé figurant dans la liste Keyword_card_terms_dict est trouvé.</span><span class="sxs-lookup"><span data-stu-id="319ad-1630">A keyword from Keyword_card_terms_dict is found.</span></span>
    - <span data-ttu-id="319ad-1631">Un mot clé figurant dans la liste Keyword_card_security_terms_dict est trouvé.</span><span class="sxs-lookup"><span data-stu-id="319ad-1631">A keyword from Keyword_card_security_terms_dict is found.</span></span>
    - <span data-ttu-id="319ad-1632">Un mot clé figurant dans la liste Keyword_card_expiration_terms_dict est trouvé.</span><span class="sxs-lookup"><span data-stu-id="319ad-1632">A keyword from Keyword_card_expiration_terms_dict is found.</span></span>
    - <span data-ttu-id="319ad-1633">La fonction Func_expiration_date trouve une date au format correct.</span><span class="sxs-lookup"><span data-stu-id="319ad-1633">The function Func_expiration_date finds a date in the right date format.</span></span>
- <span data-ttu-id="319ad-1634">La somme de contrôle est correcte.</span><span class="sxs-lookup"><span data-stu-id="319ad-1634">The checksum passes.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="319ad-1635">Mots-clés</span><span class="sxs-lookup"><span data-stu-id="319ad-1635">Keywords</span></span>

#### <a name="keyword_eu_debit_card"></a><span data-ttu-id="319ad-1636">Keyword_eu_debit_card</span><span class="sxs-lookup"><span data-stu-id="319ad-1636">Keyword_eu_debit_card</span></span>

- <span data-ttu-id="319ad-1637">numéro de compte</span><span class="sxs-lookup"><span data-stu-id="319ad-1637">account number</span></span> 
- <span data-ttu-id="319ad-1638">numéro de carte</span><span class="sxs-lookup"><span data-stu-id="319ad-1638">card number</span></span> 
- <span data-ttu-id="319ad-1639">n° carte</span><span class="sxs-lookup"><span data-stu-id="319ad-1639">card no.</span></span> 
- <span data-ttu-id="319ad-1640">numéro de sécurité</span><span class="sxs-lookup"><span data-stu-id="319ad-1640">security number</span></span> 
- <span data-ttu-id="319ad-1641">CC #</span><span class="sxs-lookup"><span data-stu-id="319ad-1641">cc#</span></span> 

#### <a name="keyword_card_terms_dict"></a><span data-ttu-id="319ad-1642">Keyword_card_terms_dict</span><span class="sxs-lookup"><span data-stu-id="319ad-1642">Keyword_card_terms_dict</span></span>

- <span data-ttu-id="319ad-1643">num de compte</span><span class="sxs-lookup"><span data-stu-id="319ad-1643">acct nbr</span></span> 
- <span data-ttu-id="319ad-1644">num de compte</span><span class="sxs-lookup"><span data-stu-id="319ad-1644">acct num</span></span> 
- <span data-ttu-id="319ad-1645">n° compte</span><span class="sxs-lookup"><span data-stu-id="319ad-1645">acct no</span></span> 
- <span data-ttu-id="319ad-1646">american express</span><span class="sxs-lookup"><span data-stu-id="319ad-1646">american express</span></span> 
- <span data-ttu-id="319ad-1647">americanexpress</span><span class="sxs-lookup"><span data-stu-id="319ad-1647">americanexpress</span></span> 
- <span data-ttu-id="319ad-1648">americano espresso</span><span class="sxs-lookup"><span data-stu-id="319ad-1648">americano espresso</span></span> 
- <span data-ttu-id="319ad-1649">American</span><span class="sxs-lookup"><span data-stu-id="319ad-1649">amex</span></span> 
- <span data-ttu-id="319ad-1650">carte de retrait</span><span class="sxs-lookup"><span data-stu-id="319ad-1650">atm card</span></span> 
- <span data-ttu-id="319ad-1651">cartes de retrait</span><span class="sxs-lookup"><span data-stu-id="319ad-1651">atm cards</span></span> 
- <span data-ttu-id="319ad-1652">atm kaart</span><span class="sxs-lookup"><span data-stu-id="319ad-1652">atm kaart</span></span> 
- <span data-ttu-id="319ad-1653">retrait</span><span class="sxs-lookup"><span data-stu-id="319ad-1653">atmcard</span></span> 
- <span data-ttu-id="319ad-1654">retrait</span><span class="sxs-lookup"><span data-stu-id="319ad-1654">atmcards</span></span> 
- <span data-ttu-id="319ad-1655">atmkaart</span><span class="sxs-lookup"><span data-stu-id="319ad-1655">atmkaart</span></span> 
- <span data-ttu-id="319ad-1656">atmkaarten</span><span class="sxs-lookup"><span data-stu-id="319ad-1656">atmkaarten</span></span> 
- <span data-ttu-id="319ad-1657">bancontact</span><span class="sxs-lookup"><span data-stu-id="319ad-1657">bancontact</span></span> 
- <span data-ttu-id="319ad-1658">carte bancaire</span><span class="sxs-lookup"><span data-stu-id="319ad-1658">bank card</span></span> 
- <span data-ttu-id="319ad-1659">bankkaart</span><span class="sxs-lookup"><span data-stu-id="319ad-1659">bankkaart</span></span> 
- <span data-ttu-id="319ad-1660">titulaire de la carte</span><span class="sxs-lookup"><span data-stu-id="319ad-1660">card holder</span></span> 
- <span data-ttu-id="319ad-1661">titulaires de la carte</span><span class="sxs-lookup"><span data-stu-id="319ad-1661">card holders</span></span> 
- <span data-ttu-id="319ad-1662">num de carte</span><span class="sxs-lookup"><span data-stu-id="319ad-1662">card num</span></span> 
- <span data-ttu-id="319ad-1663">numéro de carte</span><span class="sxs-lookup"><span data-stu-id="319ad-1663">card number</span></span> 
- <span data-ttu-id="319ad-1664">numéros de carte</span><span class="sxs-lookup"><span data-stu-id="319ad-1664">card numbers</span></span> 
- <span data-ttu-id="319ad-1665">type de carte</span><span class="sxs-lookup"><span data-stu-id="319ad-1665">card type</span></span> 
- <span data-ttu-id="319ad-1666">cardano numerico</span><span class="sxs-lookup"><span data-stu-id="319ad-1666">cardano numerico</span></span> 
- <span data-ttu-id="319ad-1667">titulaires</span><span class="sxs-lookup"><span data-stu-id="319ad-1667">cardholder</span></span> 
- <span data-ttu-id="319ad-1668">titulaires</span><span class="sxs-lookup"><span data-stu-id="319ad-1668">cardholders</span></span> 
- <span data-ttu-id="319ad-1669">carte</span><span class="sxs-lookup"><span data-stu-id="319ad-1669">cardnumber</span></span> 
- <span data-ttu-id="319ad-1670">carte</span><span class="sxs-lookup"><span data-stu-id="319ad-1670">cardnumbers</span></span> 
- <span data-ttu-id="319ad-1671">carta bianca</span><span class="sxs-lookup"><span data-stu-id="319ad-1671">carta bianca</span></span> 
- <span data-ttu-id="319ad-1672">Carta credito</span><span class="sxs-lookup"><span data-stu-id="319ad-1672">carta credito</span></span> 
- <span data-ttu-id="319ad-1673">Carta di credito</span><span class="sxs-lookup"><span data-stu-id="319ad-1673">carta di credito</span></span> 
- <span data-ttu-id="319ad-1674">cartao de credito</span><span class="sxs-lookup"><span data-stu-id="319ad-1674">cartao de credito</span></span> 
- <span data-ttu-id="319ad-1675">cartao de crédito</span><span class="sxs-lookup"><span data-stu-id="319ad-1675">cartao de crédito</span></span> 
- <span data-ttu-id="319ad-1676">cartao de debito</span><span class="sxs-lookup"><span data-stu-id="319ad-1676">cartao de debito</span></span> 
- <span data-ttu-id="319ad-1677">cartao de débito</span><span class="sxs-lookup"><span data-stu-id="319ad-1677">cartao de débito</span></span> 
- <span data-ttu-id="319ad-1678">carte bancaire</span><span class="sxs-lookup"><span data-stu-id="319ad-1678">carte bancaire</span></span> 
- <span data-ttu-id="319ad-1679">carte blanche</span><span class="sxs-lookup"><span data-stu-id="319ad-1679">carte blanche</span></span> 
- <span data-ttu-id="319ad-1680">carte bleue</span><span class="sxs-lookup"><span data-stu-id="319ad-1680">carte bleue</span></span> 
- <span data-ttu-id="319ad-1681">carte de credit</span><span class="sxs-lookup"><span data-stu-id="319ad-1681">carte de credit</span></span> 
- <span data-ttu-id="319ad-1682">carte de crédit</span><span class="sxs-lookup"><span data-stu-id="319ad-1682">carte de crédit</span></span> 
- <span data-ttu-id="319ad-1683">carte di credito</span><span class="sxs-lookup"><span data-stu-id="319ad-1683">carte di credito</span></span> 
- <span data-ttu-id="319ad-1684">carteblanche</span><span class="sxs-lookup"><span data-stu-id="319ad-1684">carteblanche</span></span> 
- <span data-ttu-id="319ad-1685">cartão de credito</span><span class="sxs-lookup"><span data-stu-id="319ad-1685">cartão de credito</span></span> 
- <span data-ttu-id="319ad-1686">cartão de crédito</span><span class="sxs-lookup"><span data-stu-id="319ad-1686">cartão de crédito</span></span> 
- <span data-ttu-id="319ad-1687">cartão de debito</span><span class="sxs-lookup"><span data-stu-id="319ad-1687">cartão de debito</span></span> 
- <span data-ttu-id="319ad-1688">cartão de débito</span><span class="sxs-lookup"><span data-stu-id="319ad-1688">cartão de débito</span></span> 
- <span data-ttu-id="319ad-1689">cb</span><span class="sxs-lookup"><span data-stu-id="319ad-1689">cb</span></span> 
- <span data-ttu-id="319ad-1690">CCN</span><span class="sxs-lookup"><span data-stu-id="319ad-1690">ccn</span></span> 
- <span data-ttu-id="319ad-1691">carte de vérification</span><span class="sxs-lookup"><span data-stu-id="319ad-1691">check card</span></span> 
- <span data-ttu-id="319ad-1692">cartes de vérification</span><span class="sxs-lookup"><span data-stu-id="319ad-1692">check cards</span></span> 
- <span data-ttu-id="319ad-1693">carte</span><span class="sxs-lookup"><span data-stu-id="319ad-1693">checkcard</span></span>
- <span data-ttu-id="319ad-1694">cartes</span><span class="sxs-lookup"><span data-stu-id="319ad-1694">checkcards</span></span> 
- <span data-ttu-id="319ad-1695">chequekaart</span><span class="sxs-lookup"><span data-stu-id="319ad-1695">chequekaart</span></span> 
- <span data-ttu-id="319ad-1696">Cirrus</span><span class="sxs-lookup"><span data-stu-id="319ad-1696">cirrus</span></span> 
- <span data-ttu-id="319ad-1697">Cirrus-EDC-Maestro</span><span class="sxs-lookup"><span data-stu-id="319ad-1697">cirrus-edc-maestro</span></span> 
- <span data-ttu-id="319ad-1698">controlekaart</span><span class="sxs-lookup"><span data-stu-id="319ad-1698">controlekaart</span></span> 
- <span data-ttu-id="319ad-1699">controlekaarten</span><span class="sxs-lookup"><span data-stu-id="319ad-1699">controlekaarten</span></span> 
- <span data-ttu-id="319ad-1700">carte de crédit</span><span class="sxs-lookup"><span data-stu-id="319ad-1700">credit card</span></span> 
- <span data-ttu-id="319ad-1701">cartes de crédit</span><span class="sxs-lookup"><span data-stu-id="319ad-1701">credit cards</span></span> 
- <span data-ttu-id="319ad-1702">CreditCard</span><span class="sxs-lookup"><span data-stu-id="319ad-1702">creditcard</span></span> 
- <span data-ttu-id="319ad-1703">crédit</span><span class="sxs-lookup"><span data-stu-id="319ad-1703">creditcards</span></span> 
- <span data-ttu-id="319ad-1704">debetkaart</span><span class="sxs-lookup"><span data-stu-id="319ad-1704">debetkaart</span></span> 
- <span data-ttu-id="319ad-1705">debetkaarten</span><span class="sxs-lookup"><span data-stu-id="319ad-1705">debetkaarten</span></span> 
- <span data-ttu-id="319ad-1706">carte de débit</span><span class="sxs-lookup"><span data-stu-id="319ad-1706">debit card</span></span> 
- <span data-ttu-id="319ad-1707">cartes de débit</span><span class="sxs-lookup"><span data-stu-id="319ad-1707">debit cards</span></span> 
- <span data-ttu-id="319ad-1708">débit</span><span class="sxs-lookup"><span data-stu-id="319ad-1708">debitcard</span></span> 
- <span data-ttu-id="319ad-1709">débit</span><span class="sxs-lookup"><span data-stu-id="319ad-1709">debitcards</span></span> 
- <span data-ttu-id="319ad-1710">debito automatico</span><span class="sxs-lookup"><span data-stu-id="319ad-1710">debito automatico</span></span> 
- <span data-ttu-id="319ad-1711">diners club</span><span class="sxs-lookup"><span data-stu-id="319ad-1711">diners club</span></span> 
- <span data-ttu-id="319ad-1712">dinersclub</span><span class="sxs-lookup"><span data-stu-id="319ad-1712">dinersclub</span></span> 
- <span data-ttu-id="319ad-1713">connaissance</span><span class="sxs-lookup"><span data-stu-id="319ad-1713">discover</span></span> 
- <span data-ttu-id="319ad-1714">discover card</span><span class="sxs-lookup"><span data-stu-id="319ad-1714">discover card</span></span> 
- <span data-ttu-id="319ad-1715">discover cards</span><span class="sxs-lookup"><span data-stu-id="319ad-1715">discover cards</span></span> 
- <span data-ttu-id="319ad-1716">discovercard</span><span class="sxs-lookup"><span data-stu-id="319ad-1716">discovercard</span></span> 
- <span data-ttu-id="319ad-1717">discovercards</span><span class="sxs-lookup"><span data-stu-id="319ad-1717">discovercards</span></span> 
- <span data-ttu-id="319ad-1718">débito automático</span><span class="sxs-lookup"><span data-stu-id="319ad-1718">débito automático</span></span>
- <span data-ttu-id="319ad-1719">EDC</span><span class="sxs-lookup"><span data-stu-id="319ad-1719">edc</span></span> 
- <span data-ttu-id="319ad-1720">eigentümername</span><span class="sxs-lookup"><span data-stu-id="319ad-1720">eigentümername</span></span> 
- <span data-ttu-id="319ad-1721">carte de crédit européenne</span><span class="sxs-lookup"><span data-stu-id="319ad-1721">european debit card</span></span> 
- <span data-ttu-id="319ad-1722">hoofdkaart</span><span class="sxs-lookup"><span data-stu-id="319ad-1722">hoofdkaart</span></span> 
- <span data-ttu-id="319ad-1723">hoofdkaarten</span><span class="sxs-lookup"><span data-stu-id="319ad-1723">hoofdkaarten</span></span> 
- <span data-ttu-id="319ad-1724">in viaggio</span><span class="sxs-lookup"><span data-stu-id="319ad-1724">in viaggio</span></span> 
- <span data-ttu-id="319ad-1725">japanese card bureau</span><span class="sxs-lookup"><span data-stu-id="319ad-1725">japanese card bureau</span></span> 
- <span data-ttu-id="319ad-1726">japanse kaartdienst</span><span class="sxs-lookup"><span data-stu-id="319ad-1726">japanse kaartdienst</span></span> 
- <span data-ttu-id="319ad-1727">JCB</span><span class="sxs-lookup"><span data-stu-id="319ad-1727">jcb</span></span> 
- <span data-ttu-id="319ad-1728">kaart</span><span class="sxs-lookup"><span data-stu-id="319ad-1728">kaart</span></span> 
- <span data-ttu-id="319ad-1729">kaart num</span><span class="sxs-lookup"><span data-stu-id="319ad-1729">kaart num</span></span> 
- <span data-ttu-id="319ad-1730">kaartaantal</span><span class="sxs-lookup"><span data-stu-id="319ad-1730">kaartaantal</span></span> 
- <span data-ttu-id="319ad-1731">kaartaantallen</span><span class="sxs-lookup"><span data-stu-id="319ad-1731">kaartaantallen</span></span> 
- <span data-ttu-id="319ad-1732">kaarthouder</span><span class="sxs-lookup"><span data-stu-id="319ad-1732">kaarthouder</span></span> 
- <span data-ttu-id="319ad-1733">kaarthouders</span><span class="sxs-lookup"><span data-stu-id="319ad-1733">kaarthouders</span></span> 
- <span data-ttu-id="319ad-1734">karte</span><span class="sxs-lookup"><span data-stu-id="319ad-1734">karte</span></span>  
- <span data-ttu-id="319ad-1735">karteninhaber</span><span class="sxs-lookup"><span data-stu-id="319ad-1735">karteninhaber</span></span> 
- <span data-ttu-id="319ad-1736">karteninhabers</span><span class="sxs-lookup"><span data-stu-id="319ad-1736">karteninhabers</span></span>
- <span data-ttu-id="319ad-1737">kartennr</span><span class="sxs-lookup"><span data-stu-id="319ad-1737">kartennr</span></span> 
- <span data-ttu-id="319ad-1738">kartennummer</span><span class="sxs-lookup"><span data-stu-id="319ad-1738">kartennummer</span></span> 
- <span data-ttu-id="319ad-1739">kreditkarte</span><span class="sxs-lookup"><span data-stu-id="319ad-1739">kreditkarte</span></span> 
- <span data-ttu-id="319ad-1740">kreditkarten-nummer</span><span class="sxs-lookup"><span data-stu-id="319ad-1740">kreditkarten-nummer</span></span> 
- <span data-ttu-id="319ad-1741">kreditkarteninhaber</span><span class="sxs-lookup"><span data-stu-id="319ad-1741">kreditkarteninhaber</span></span> 
- <span data-ttu-id="319ad-1742">kreditkarteninstitut</span><span class="sxs-lookup"><span data-stu-id="319ad-1742">kreditkarteninstitut</span></span> 
- <span data-ttu-id="319ad-1743">kreditkartennummer</span><span class="sxs-lookup"><span data-stu-id="319ad-1743">kreditkartennummer</span></span> 
- <span data-ttu-id="319ad-1744">kreditkartentyp</span><span class="sxs-lookup"><span data-stu-id="319ad-1744">kreditkartentyp</span></span> 
- <span data-ttu-id="319ad-1745">sonne</span><span class="sxs-lookup"><span data-stu-id="319ad-1745">maestro</span></span> 
- <span data-ttu-id="319ad-1746">master card</span><span class="sxs-lookup"><span data-stu-id="319ad-1746">master card</span></span> 
- <span data-ttu-id="319ad-1747">master cards</span><span class="sxs-lookup"><span data-stu-id="319ad-1747">master cards</span></span> 
- <span data-ttu-id="319ad-1748">MasterCard</span><span class="sxs-lookup"><span data-stu-id="319ad-1748">mastercard</span></span> 
- <span data-ttu-id="319ad-1749">MasterCard</span><span class="sxs-lookup"><span data-stu-id="319ad-1749">mastercards</span></span> 
- <span data-ttu-id="319ad-1750">McDonald</span><span class="sxs-lookup"><span data-stu-id="319ad-1750">mc</span></span> 
- <span data-ttu-id="319ad-1751">mister cash</span><span class="sxs-lookup"><span data-stu-id="319ad-1751">mister cash</span></span> 
- <span data-ttu-id="319ad-1752">n carta</span><span class="sxs-lookup"><span data-stu-id="319ad-1752">n carta</span></span> 
- <span data-ttu-id="319ad-1753">Carta</span><span class="sxs-lookup"><span data-stu-id="319ad-1753">carta</span></span> 
- <span data-ttu-id="319ad-1754">no de tarjeta</span><span class="sxs-lookup"><span data-stu-id="319ad-1754">no de tarjeta</span></span> 
- <span data-ttu-id="319ad-1755">no do cartao</span><span class="sxs-lookup"><span data-stu-id="319ad-1755">no do cartao</span></span> 
- <span data-ttu-id="319ad-1756">no do cartão</span><span class="sxs-lookup"><span data-stu-id="319ad-1756">no do cartão</span></span> 
- <span data-ttu-id="319ad-1757">Nbre.</span><span class="sxs-lookup"><span data-stu-id="319ad-1757">no.</span></span> <span data-ttu-id="319ad-1758">de tarjeta</span><span class="sxs-lookup"><span data-stu-id="319ad-1758">de tarjeta</span></span> 
- <span data-ttu-id="319ad-1759">Nbre.</span><span class="sxs-lookup"><span data-stu-id="319ad-1759">no.</span></span> <span data-ttu-id="319ad-1760">do cartao</span><span class="sxs-lookup"><span data-stu-id="319ad-1760">do cartao</span></span> 
- <span data-ttu-id="319ad-1761">Nbre.</span><span class="sxs-lookup"><span data-stu-id="319ad-1761">no.</span></span> <span data-ttu-id="319ad-1762">do cartão</span><span class="sxs-lookup"><span data-stu-id="319ad-1762">do cartão</span></span> 
- <span data-ttu-id="319ad-1763">nr carta</span><span class="sxs-lookup"><span data-stu-id="319ad-1763">nr carta</span></span> 
- <span data-ttu-id="319ad-1764">Nr.</span><span class="sxs-lookup"><span data-stu-id="319ad-1764">nr.</span></span> <span data-ttu-id="319ad-1765">Carta</span><span class="sxs-lookup"><span data-stu-id="319ad-1765">carta</span></span> 
- <span data-ttu-id="319ad-1766">numeri di scheda</span><span class="sxs-lookup"><span data-stu-id="319ad-1766">numeri di scheda</span></span> 
- <span data-ttu-id="319ad-1767">numero carta</span><span class="sxs-lookup"><span data-stu-id="319ad-1767">numero carta</span></span> 
- <span data-ttu-id="319ad-1768">numero de cartao</span><span class="sxs-lookup"><span data-stu-id="319ad-1768">numero de cartao</span></span> 
- <span data-ttu-id="319ad-1769">numero de carte</span><span class="sxs-lookup"><span data-stu-id="319ad-1769">numero de carte</span></span> 
- <span data-ttu-id="319ad-1770">numero de cartão</span><span class="sxs-lookup"><span data-stu-id="319ad-1770">numero de cartão</span></span> 
- <span data-ttu-id="319ad-1771">numero de tarjeta</span><span class="sxs-lookup"><span data-stu-id="319ad-1771">numero de tarjeta</span></span>
- <span data-ttu-id="319ad-1772">numero della carta</span><span class="sxs-lookup"><span data-stu-id="319ad-1772">numero della carta</span></span> 
- <span data-ttu-id="319ad-1773">numero di carta</span><span class="sxs-lookup"><span data-stu-id="319ad-1773">numero di carta</span></span> 
- <span data-ttu-id="319ad-1774">numero di scheda</span><span class="sxs-lookup"><span data-stu-id="319ad-1774">numero di scheda</span></span> 
- <span data-ttu-id="319ad-1775">numero do cartao</span><span class="sxs-lookup"><span data-stu-id="319ad-1775">numero do cartao</span></span> 
- <span data-ttu-id="319ad-1776">numero do cartão</span><span class="sxs-lookup"><span data-stu-id="319ad-1776">numero do cartão</span></span> 
- <span data-ttu-id="319ad-1777">numéro de carte</span><span class="sxs-lookup"><span data-stu-id="319ad-1777">numéro de carte</span></span> 
- <span data-ttu-id="319ad-1778">nº carta</span><span class="sxs-lookup"><span data-stu-id="319ad-1778">nº carta</span></span> 
- <span data-ttu-id="319ad-1779">nº de carte</span><span class="sxs-lookup"><span data-stu-id="319ad-1779">nº de carte</span></span> 
- <span data-ttu-id="319ad-1780">nº de la carte</span><span class="sxs-lookup"><span data-stu-id="319ad-1780">nº de la carte</span></span> 
- <span data-ttu-id="319ad-1781">nº de tarjeta</span><span class="sxs-lookup"><span data-stu-id="319ad-1781">nº de tarjeta</span></span> 
- <span data-ttu-id="319ad-1782">nº do cartao</span><span class="sxs-lookup"><span data-stu-id="319ad-1782">nº do cartao</span></span> 
- <span data-ttu-id="319ad-1783">nº do cartão</span><span class="sxs-lookup"><span data-stu-id="319ad-1783">nº do cartão</span></span> 
- <span data-ttu-id="319ad-1784">n º.</span><span class="sxs-lookup"><span data-stu-id="319ad-1784">nº.</span></span> <span data-ttu-id="319ad-1785">do cartão</span><span class="sxs-lookup"><span data-stu-id="319ad-1785">do cartão</span></span> 
- <span data-ttu-id="319ad-1786">número de cartao</span><span class="sxs-lookup"><span data-stu-id="319ad-1786">número de cartao</span></span> 
- <span data-ttu-id="319ad-1787">número de cartão</span><span class="sxs-lookup"><span data-stu-id="319ad-1787">número de cartão</span></span> 
- <span data-ttu-id="319ad-1788">número de tarjeta</span><span class="sxs-lookup"><span data-stu-id="319ad-1788">número de tarjeta</span></span> 
- <span data-ttu-id="319ad-1789">número do cartao</span><span class="sxs-lookup"><span data-stu-id="319ad-1789">número do cartao</span></span> 
- <span data-ttu-id="319ad-1790">scheda dell’assegno</span><span class="sxs-lookup"><span data-stu-id="319ad-1790">scheda dell'assegno</span></span> 
- <span data-ttu-id="319ad-1791">scheda dell’atmosfera</span><span class="sxs-lookup"><span data-stu-id="319ad-1791">scheda dell'atmosfera</span></span> 
- <span data-ttu-id="319ad-1792">scheda dell’atmosfera</span><span class="sxs-lookup"><span data-stu-id="319ad-1792">scheda dell'atmosfera</span></span> 
- <span data-ttu-id="319ad-1793">scheda della banca</span><span class="sxs-lookup"><span data-stu-id="319ad-1793">scheda della banca</span></span> 
- <span data-ttu-id="319ad-1794">scheda di controllo</span><span class="sxs-lookup"><span data-stu-id="319ad-1794">scheda di controllo</span></span> 
- <span data-ttu-id="319ad-1795">scheda di debito</span><span class="sxs-lookup"><span data-stu-id="319ad-1795">scheda di debito</span></span> 
- <span data-ttu-id="319ad-1796">scheda matrice</span><span class="sxs-lookup"><span data-stu-id="319ad-1796">scheda matrice</span></span> 
- <span data-ttu-id="319ad-1797">schede dell’atmosfera</span><span class="sxs-lookup"><span data-stu-id="319ad-1797">schede dell'atmosfera</span></span> 
- <span data-ttu-id="319ad-1798">schede di controllo</span><span class="sxs-lookup"><span data-stu-id="319ad-1798">schede di controllo</span></span> 
- <span data-ttu-id="319ad-1799">schede di debito</span><span class="sxs-lookup"><span data-stu-id="319ad-1799">schede di debito</span></span> 
- <span data-ttu-id="319ad-1800">schede matrici</span><span class="sxs-lookup"><span data-stu-id="319ad-1800">schede matrici</span></span> 
- <span data-ttu-id="319ad-1801">scoprono la scheda</span><span class="sxs-lookup"><span data-stu-id="319ad-1801">scoprono la scheda</span></span> 
- <span data-ttu-id="319ad-1802">scoprono le schede</span><span class="sxs-lookup"><span data-stu-id="319ad-1802">scoprono le schede</span></span> 
- <span data-ttu-id="319ad-1803">tracteur</span><span class="sxs-lookup"><span data-stu-id="319ad-1803">solo</span></span> 
- <span data-ttu-id="319ad-1804">supporti di scheda</span><span class="sxs-lookup"><span data-stu-id="319ad-1804">supporti di scheda</span></span> 
- <span data-ttu-id="319ad-1805">supporto di scheda</span><span class="sxs-lookup"><span data-stu-id="319ad-1805">supporto di scheda</span></span> 
- <span data-ttu-id="319ad-1806">accéder</span><span class="sxs-lookup"><span data-stu-id="319ad-1806">switch</span></span> 
- <span data-ttu-id="319ad-1807">tarjeta atm</span><span class="sxs-lookup"><span data-stu-id="319ad-1807">tarjeta atm</span></span> 
- <span data-ttu-id="319ad-1808">tarjeta credito</span><span class="sxs-lookup"><span data-stu-id="319ad-1808">tarjeta credito</span></span> 
- <span data-ttu-id="319ad-1809">tarjeta de atm</span><span class="sxs-lookup"><span data-stu-id="319ad-1809">tarjeta de atm</span></span> 
- <span data-ttu-id="319ad-1810">tarjeta de credito</span><span class="sxs-lookup"><span data-stu-id="319ad-1810">tarjeta de credito</span></span> 
- <span data-ttu-id="319ad-1811">tarjeta de debito</span><span class="sxs-lookup"><span data-stu-id="319ad-1811">tarjeta de debito</span></span> 
- <span data-ttu-id="319ad-1812">tarjeta debito</span><span class="sxs-lookup"><span data-stu-id="319ad-1812">tarjeta debito</span></span> 
- <span data-ttu-id="319ad-1813">tarjeta no</span><span class="sxs-lookup"><span data-stu-id="319ad-1813">tarjeta no</span></span>
- <span data-ttu-id="319ad-1814">tarjetahabiente</span><span class="sxs-lookup"><span data-stu-id="319ad-1814">tarjetahabiente</span></span> 
- <span data-ttu-id="319ad-1815">tipo della scheda</span><span class="sxs-lookup"><span data-stu-id="319ad-1815">tipo della scheda</span></span> 
- <span data-ttu-id="319ad-1816">ufficio giapponese della</span><span class="sxs-lookup"><span data-stu-id="319ad-1816">ufficio giapponese della</span></span> 
- <span data-ttu-id="319ad-1817">scheda</span><span class="sxs-lookup"><span data-stu-id="319ad-1817">scheda</span></span> 
- <span data-ttu-id="319ad-1818">v pay</span><span class="sxs-lookup"><span data-stu-id="319ad-1818">v pay</span></span> 
- <span data-ttu-id="319ad-1819">v-Pay</span><span class="sxs-lookup"><span data-stu-id="319ad-1819">v-pay</span></span> 
- <span data-ttu-id="319ad-1820">délivrance</span><span class="sxs-lookup"><span data-stu-id="319ad-1820">visa</span></span> 
- <span data-ttu-id="319ad-1821">visa plus</span><span class="sxs-lookup"><span data-stu-id="319ad-1821">visa plus</span></span> 
- <span data-ttu-id="319ad-1822">visa electron</span><span class="sxs-lookup"><span data-stu-id="319ad-1822">visa electron</span></span> 
- <span data-ttu-id="319ad-1823">visto</span><span class="sxs-lookup"><span data-stu-id="319ad-1823">visto</span></span> 
- <span data-ttu-id="319ad-1824">visum</span><span class="sxs-lookup"><span data-stu-id="319ad-1824">visum</span></span> 
- <span data-ttu-id="319ad-1825">vpay</span><span class="sxs-lookup"><span data-stu-id="319ad-1825">vpay</span></span>   

#### <a name="keyword_card_security_terms_dict"></a><span data-ttu-id="319ad-1826">Keyword_card_security_terms_dict</span><span class="sxs-lookup"><span data-stu-id="319ad-1826">Keyword_card_security_terms_dict</span></span>

- <span data-ttu-id="319ad-1827">numéro d’identification de la carte</span><span class="sxs-lookup"><span data-stu-id="319ad-1827">card identification number</span></span>
- <span data-ttu-id="319ad-1828">vérification de la carte</span><span class="sxs-lookup"><span data-stu-id="319ad-1828">card verification</span></span> 
- <span data-ttu-id="319ad-1829">cardi la verifica</span><span class="sxs-lookup"><span data-stu-id="319ad-1829">cardi la verifica</span></span> 
- <span data-ttu-id="319ad-1830">nic</span><span class="sxs-lookup"><span data-stu-id="319ad-1830">cid</span></span> 
- <span data-ttu-id="319ad-1831">cod seg</span><span class="sxs-lookup"><span data-stu-id="319ad-1831">cod seg</span></span> 
- <span data-ttu-id="319ad-1832">cod seguranca</span><span class="sxs-lookup"><span data-stu-id="319ad-1832">cod seguranca</span></span> 
- <span data-ttu-id="319ad-1833">cod segurança</span><span class="sxs-lookup"><span data-stu-id="319ad-1833">cod segurança</span></span> 
- <span data-ttu-id="319ad-1834">cod sicurezza</span><span class="sxs-lookup"><span data-stu-id="319ad-1834">cod sicurezza</span></span> 
- <span data-ttu-id="319ad-1835">contre.</span><span class="sxs-lookup"><span data-stu-id="319ad-1835">cod.</span></span> <span data-ttu-id="319ad-1836">SEG</span><span class="sxs-lookup"><span data-stu-id="319ad-1836">seg</span></span> 
- <span data-ttu-id="319ad-1837">contre.</span><span class="sxs-lookup"><span data-stu-id="319ad-1837">cod.</span></span> <span data-ttu-id="319ad-1838">seguranca</span><span class="sxs-lookup"><span data-stu-id="319ad-1838">seguranca</span></span> 
- <span data-ttu-id="319ad-1839">contre.</span><span class="sxs-lookup"><span data-stu-id="319ad-1839">cod.</span></span> <span data-ttu-id="319ad-1840">segurança</span><span class="sxs-lookup"><span data-stu-id="319ad-1840">segurança</span></span> 
- <span data-ttu-id="319ad-1841">contre.</span><span class="sxs-lookup"><span data-stu-id="319ad-1841">cod.</span></span> <span data-ttu-id="319ad-1842">sicurezza</span><span class="sxs-lookup"><span data-stu-id="319ad-1842">sicurezza</span></span> 
- <span data-ttu-id="319ad-1843">codice di sicurezza</span><span class="sxs-lookup"><span data-stu-id="319ad-1843">codice di sicurezza</span></span> 
- <span data-ttu-id="319ad-1844">codice di verifica</span><span class="sxs-lookup"><span data-stu-id="319ad-1844">codice di verifica</span></span> 
- <span data-ttu-id="319ad-1845">codigo</span><span class="sxs-lookup"><span data-stu-id="319ad-1845">codigo</span></span> 
- <span data-ttu-id="319ad-1846">codigo de seguranca</span><span class="sxs-lookup"><span data-stu-id="319ad-1846">codigo de seguranca</span></span> 
- <span data-ttu-id="319ad-1847">codigo de segurança</span><span class="sxs-lookup"><span data-stu-id="319ad-1847">codigo de segurança</span></span> 
- <span data-ttu-id="319ad-1848">crittogramma</span><span class="sxs-lookup"><span data-stu-id="319ad-1848">crittogramma</span></span> 
- <span data-ttu-id="319ad-1849">cryptogram</span><span class="sxs-lookup"><span data-stu-id="319ad-1849">cryptogram</span></span> 
- <span data-ttu-id="319ad-1850">cryptogramme</span><span class="sxs-lookup"><span data-stu-id="319ad-1850">cryptogramme</span></span> 
- <span data-ttu-id="319ad-1851">cv2</span><span class="sxs-lookup"><span data-stu-id="319ad-1851">cv2</span></span> 
- <span data-ttu-id="319ad-1852">lâche</span><span class="sxs-lookup"><span data-stu-id="319ad-1852">cvc</span></span> 
- <span data-ttu-id="319ad-1853">cvc2</span><span class="sxs-lookup"><span data-stu-id="319ad-1853">cvc2</span></span> 
- <span data-ttu-id="319ad-1854">cryptogramme</span><span class="sxs-lookup"><span data-stu-id="319ad-1854">cvn</span></span> 
- <span data-ttu-id="319ad-1855">cvv</span><span class="sxs-lookup"><span data-stu-id="319ad-1855">cvv</span></span> 
- <span data-ttu-id="319ad-1856">cvv2</span><span class="sxs-lookup"><span data-stu-id="319ad-1856">cvv2</span></span> 
- <span data-ttu-id="319ad-1857">cód seguranca</span><span class="sxs-lookup"><span data-stu-id="319ad-1857">cód seguranca</span></span> 
- <span data-ttu-id="319ad-1858">cód segurança</span><span class="sxs-lookup"><span data-stu-id="319ad-1858">cód segurança</span></span> 
- <span data-ttu-id="319ad-1859">cód.</span><span class="sxs-lookup"><span data-stu-id="319ad-1859">cód.</span></span> <span data-ttu-id="319ad-1860">seguranca</span><span class="sxs-lookup"><span data-stu-id="319ad-1860">seguranca</span></span> 
- <span data-ttu-id="319ad-1861">cód.</span><span class="sxs-lookup"><span data-stu-id="319ad-1861">cód.</span></span> <span data-ttu-id="319ad-1862">segurança</span><span class="sxs-lookup"><span data-stu-id="319ad-1862">segurança</span></span> 
- <span data-ttu-id="319ad-1863">código</span><span class="sxs-lookup"><span data-stu-id="319ad-1863">código</span></span> 
- <span data-ttu-id="319ad-1864">código de seguranca</span><span class="sxs-lookup"><span data-stu-id="319ad-1864">código de seguranca</span></span> 
- <span data-ttu-id="319ad-1865">código de segurança</span><span class="sxs-lookup"><span data-stu-id="319ad-1865">código de segurança</span></span> 
- <span data-ttu-id="319ad-1866">de kaart controle</span><span class="sxs-lookup"><span data-stu-id="319ad-1866">de kaart controle</span></span> 
- <span data-ttu-id="319ad-1867">geeft nr suit</span><span class="sxs-lookup"><span data-stu-id="319ad-1867">geeft nr uit</span></span> 
- <span data-ttu-id="319ad-1868">n° d’émission</span><span class="sxs-lookup"><span data-stu-id="319ad-1868">issue no</span></span> 
- <span data-ttu-id="319ad-1869">numéro d’émission</span><span class="sxs-lookup"><span data-stu-id="319ad-1869">issue number</span></span> 
- <span data-ttu-id="319ad-1870">kaartidentificatienummer</span><span class="sxs-lookup"><span data-stu-id="319ad-1870">kaartidentificatienummer</span></span> 
- <span data-ttu-id="319ad-1871">kreditkartenprufnummer</span><span class="sxs-lookup"><span data-stu-id="319ad-1871">kreditkartenprufnummer</span></span> 
- <span data-ttu-id="319ad-1872">kreditkartenprüfnummer</span><span class="sxs-lookup"><span data-stu-id="319ad-1872">kreditkartenprüfnummer</span></span> 
- <span data-ttu-id="319ad-1873">kwestieaantal</span><span class="sxs-lookup"><span data-stu-id="319ad-1873">kwestieaantal</span></span> 
- <span data-ttu-id="319ad-1874">Nbre.</span><span class="sxs-lookup"><span data-stu-id="319ad-1874">no.</span></span> <span data-ttu-id="319ad-1875">dell'edizione</span><span class="sxs-lookup"><span data-stu-id="319ad-1875">dell'edizione</span></span> 
- <span data-ttu-id="319ad-1876">Nbre.</span><span class="sxs-lookup"><span data-stu-id="319ad-1876">no.</span></span> <span data-ttu-id="319ad-1877">di sicurezza</span><span class="sxs-lookup"><span data-stu-id="319ad-1877">di sicurezza</span></span> 
- <span data-ttu-id="319ad-1878">numéro de sécurité</span><span class="sxs-lookup"><span data-stu-id="319ad-1878">numero de securite</span></span> 
- <span data-ttu-id="319ad-1879">numero de verificacao</span><span class="sxs-lookup"><span data-stu-id="319ad-1879">numero de verificacao</span></span> 
- <span data-ttu-id="319ad-1880">numero dell’edizione</span><span class="sxs-lookup"><span data-stu-id="319ad-1880">numero dell'edizione</span></span> 
- <span data-ttu-id="319ad-1881">numero di identificazione della</span><span class="sxs-lookup"><span data-stu-id="319ad-1881">numero di identificazione della</span></span> 
- <span data-ttu-id="319ad-1882">scheda</span><span class="sxs-lookup"><span data-stu-id="319ad-1882">scheda</span></span> 
- <span data-ttu-id="319ad-1883">numero di sicurezza</span><span class="sxs-lookup"><span data-stu-id="319ad-1883">numero di sicurezza</span></span> 
- <span data-ttu-id="319ad-1884">numero van veiligheid</span><span class="sxs-lookup"><span data-stu-id="319ad-1884">numero van veiligheid</span></span> 
- <span data-ttu-id="319ad-1885">numéro de sécurité</span><span class="sxs-lookup"><span data-stu-id="319ad-1885">numéro de sécurité</span></span> 
- <span data-ttu-id="319ad-1886">nº autorizzazione</span><span class="sxs-lookup"><span data-stu-id="319ad-1886">nº autorizzazione</span></span> 
- <span data-ttu-id="319ad-1887">número de verificação</span><span class="sxs-lookup"><span data-stu-id="319ad-1887">número de verificação</span></span> 
- <span data-ttu-id="319ad-1888">perno il blocco</span><span class="sxs-lookup"><span data-stu-id="319ad-1888">perno il blocco</span></span> 
- <span data-ttu-id="319ad-1889">pin block</span><span class="sxs-lookup"><span data-stu-id="319ad-1889">pin block</span></span> 
- <span data-ttu-id="319ad-1890">prufziffer</span><span class="sxs-lookup"><span data-stu-id="319ad-1890">prufziffer</span></span> 
- <span data-ttu-id="319ad-1891">prüfziffer</span><span class="sxs-lookup"><span data-stu-id="319ad-1891">prüfziffer</span></span> 
- <span data-ttu-id="319ad-1892">code de sécurité</span><span class="sxs-lookup"><span data-stu-id="319ad-1892">security code</span></span> 
- <span data-ttu-id="319ad-1893">n° de sécurité</span><span class="sxs-lookup"><span data-stu-id="319ad-1893">security no</span></span> 
- <span data-ttu-id="319ad-1894">numéro de sécurité</span><span class="sxs-lookup"><span data-stu-id="319ad-1894">security number</span></span> 
- <span data-ttu-id="319ad-1895">sicherheits kode</span><span class="sxs-lookup"><span data-stu-id="319ad-1895">sicherheits kode</span></span> 
- <span data-ttu-id="319ad-1896">sicherheitscode</span><span class="sxs-lookup"><span data-stu-id="319ad-1896">sicherheitscode</span></span> 
- <span data-ttu-id="319ad-1897">sicherheitsnummer</span><span class="sxs-lookup"><span data-stu-id="319ad-1897">sicherheitsnummer</span></span> 
- <span data-ttu-id="319ad-1898">speldblok</span><span class="sxs-lookup"><span data-stu-id="319ad-1898">speldblok</span></span> 
- <span data-ttu-id="319ad-1899">veiligheid nr</span><span class="sxs-lookup"><span data-stu-id="319ad-1899">veiligheid nr</span></span> 
- <span data-ttu-id="319ad-1900">veiligheidsaantal</span><span class="sxs-lookup"><span data-stu-id="319ad-1900">veiligheidsaantal</span></span> 
- <span data-ttu-id="319ad-1901">veiligheidscode</span><span class="sxs-lookup"><span data-stu-id="319ad-1901">veiligheidscode</span></span> 
- <span data-ttu-id="319ad-1902">veiligheidsnummer</span><span class="sxs-lookup"><span data-stu-id="319ad-1902">veiligheidsnummer</span></span> 
- <span data-ttu-id="319ad-1903">verfalldatum</span><span class="sxs-lookup"><span data-stu-id="319ad-1903">verfalldatum</span></span> 

#### <a name="keyword_card_expiration_terms_dict"></a><span data-ttu-id="319ad-1904">Keyword_card_expiration_terms_dict</span><span class="sxs-lookup"><span data-stu-id="319ad-1904">Keyword_card_expiration_terms_dict</span></span>

- <span data-ttu-id="319ad-1905">ablauf</span><span class="sxs-lookup"><span data-stu-id="319ad-1905">ablauf</span></span> 
- <span data-ttu-id="319ad-1906">data de expiracao</span><span class="sxs-lookup"><span data-stu-id="319ad-1906">data de expiracao</span></span> 
- <span data-ttu-id="319ad-1907">data de expiração</span><span class="sxs-lookup"><span data-stu-id="319ad-1907">data de expiração</span></span> 
- <span data-ttu-id="319ad-1908">data del exp</span><span class="sxs-lookup"><span data-stu-id="319ad-1908">data del exp</span></span> 
- <span data-ttu-id="319ad-1909">data di exp</span><span class="sxs-lookup"><span data-stu-id="319ad-1909">data di exp</span></span> 
- <span data-ttu-id="319ad-1910">data di scadenza</span><span class="sxs-lookup"><span data-stu-id="319ad-1910">data di scadenza</span></span> 
- <span data-ttu-id="319ad-1911">data em que expira</span><span class="sxs-lookup"><span data-stu-id="319ad-1911">data em que expira</span></span> 
- <span data-ttu-id="319ad-1912">data scad</span><span class="sxs-lookup"><span data-stu-id="319ad-1912">data scad</span></span> 
- <span data-ttu-id="319ad-1913">data scadenza</span><span class="sxs-lookup"><span data-stu-id="319ad-1913">data scadenza</span></span> 
- <span data-ttu-id="319ad-1914">date de validité</span><span class="sxs-lookup"><span data-stu-id="319ad-1914">date de validité</span></span> 
- <span data-ttu-id="319ad-1915">datum afloop</span><span class="sxs-lookup"><span data-stu-id="319ad-1915">datum afloop</span></span> 
- <span data-ttu-id="319ad-1916">datum van exp</span><span class="sxs-lookup"><span data-stu-id="319ad-1916">datum van exp</span></span> 
- <span data-ttu-id="319ad-1917">de afloop</span><span class="sxs-lookup"><span data-stu-id="319ad-1917">de afloop</span></span> 
- <span data-ttu-id="319ad-1918">espira</span><span class="sxs-lookup"><span data-stu-id="319ad-1918">espira</span></span> 
- <span data-ttu-id="319ad-1919">espira</span><span class="sxs-lookup"><span data-stu-id="319ad-1919">espira</span></span> 
- <span data-ttu-id="319ad-1920">date d’exp</span><span class="sxs-lookup"><span data-stu-id="319ad-1920">exp date</span></span> 
- <span data-ttu-id="319ad-1921">exp datum</span><span class="sxs-lookup"><span data-stu-id="319ad-1921">exp datum</span></span> 
- <span data-ttu-id="319ad-1922">pire</span><span class="sxs-lookup"><span data-stu-id="319ad-1922">expiration</span></span> 
- <span data-ttu-id="319ad-1923">expiration</span><span class="sxs-lookup"><span data-stu-id="319ad-1923">expire</span></span> 
- <span data-ttu-id="319ad-1924">expire</span><span class="sxs-lookup"><span data-stu-id="319ad-1924">expires</span></span> 
- <span data-ttu-id="319ad-1925">expiration</span><span class="sxs-lookup"><span data-stu-id="319ad-1925">expiry</span></span> 
- <span data-ttu-id="319ad-1926">fecha de expiracion</span><span class="sxs-lookup"><span data-stu-id="319ad-1926">fecha de expiracion</span></span> 
- <span data-ttu-id="319ad-1927">fecha de venc</span><span class="sxs-lookup"><span data-stu-id="319ad-1927">fecha de venc</span></span> 
- <span data-ttu-id="319ad-1928">gultig bis</span><span class="sxs-lookup"><span data-stu-id="319ad-1928">gultig bis</span></span> 
- <span data-ttu-id="319ad-1929">gultigkeitsdatum</span><span class="sxs-lookup"><span data-stu-id="319ad-1929">gultigkeitsdatum</span></span> 
- <span data-ttu-id="319ad-1930">gültig bis</span><span class="sxs-lookup"><span data-stu-id="319ad-1930">gültig bis</span></span> 
- <span data-ttu-id="319ad-1931">gültigkeitsdatum</span><span class="sxs-lookup"><span data-stu-id="319ad-1931">gültigkeitsdatum</span></span> 
- <span data-ttu-id="319ad-1932">la scadenza</span><span class="sxs-lookup"><span data-stu-id="319ad-1932">la scadenza</span></span> 
- <span data-ttu-id="319ad-1933">scadenza</span><span class="sxs-lookup"><span data-stu-id="319ad-1933">scadenza</span></span> 
- <span data-ttu-id="319ad-1934">valable</span><span class="sxs-lookup"><span data-stu-id="319ad-1934">valable</span></span> 
- <span data-ttu-id="319ad-1935">validade</span><span class="sxs-lookup"><span data-stu-id="319ad-1935">validade</span></span> 
- <span data-ttu-id="319ad-1936">valido hasta</span><span class="sxs-lookup"><span data-stu-id="319ad-1936">valido hasta</span></span> 
- <span data-ttu-id="319ad-1937">valorisation</span><span class="sxs-lookup"><span data-stu-id="319ad-1937">valor</span></span> 
- <span data-ttu-id="319ad-1938">venc</span><span class="sxs-lookup"><span data-stu-id="319ad-1938">venc</span></span> 
- <span data-ttu-id="319ad-1939">vencimento</span><span class="sxs-lookup"><span data-stu-id="319ad-1939">vencimento</span></span> 
- <span data-ttu-id="319ad-1940">vencimiento</span><span class="sxs-lookup"><span data-stu-id="319ad-1940">vencimiento</span></span> 
- <span data-ttu-id="319ad-1941">verloopt</span><span class="sxs-lookup"><span data-stu-id="319ad-1941">verloopt</span></span> 
- <span data-ttu-id="319ad-1942">vervaldag</span><span class="sxs-lookup"><span data-stu-id="319ad-1942">vervaldag</span></span> 
- <span data-ttu-id="319ad-1943">vervaldatum</span><span class="sxs-lookup"><span data-stu-id="319ad-1943">vervaldatum</span></span> 
- <span data-ttu-id="319ad-1944">vto</span><span class="sxs-lookup"><span data-stu-id="319ad-1944">vto</span></span> 
- <span data-ttu-id="319ad-1945">válido hasta</span><span class="sxs-lookup"><span data-stu-id="319ad-1945">válido hasta</span></span> 
   
## <a name="eu-drivers-license-number"></a><span data-ttu-id="319ad-1946">Numéro de permis de conduire de l’UE</span><span class="sxs-lookup"><span data-stu-id="319ad-1946">EU Driver's License Number</span></span>

<span data-ttu-id="319ad-1947">Pour en savoir plus, consultez [la rubrique informations sensibles sur le numéro de permis de conduire du pilote de l’UE](eu-driver-s-license-number.md).</span><span class="sxs-lookup"><span data-stu-id="319ad-1947">To learn more, see [EU Driver's License Number sensitive information type](eu-driver-s-license-number.md).</span></span>
  
## <a name="eu-national-identification-number"></a><span data-ttu-id="319ad-1948">Numéro d’identification nationale de l’UE</span><span class="sxs-lookup"><span data-stu-id="319ad-1948">EU National Identification Number</span></span>

<span data-ttu-id="319ad-1949">Pour en savoir plus, consultez la rubrique [informations sensibles du numéro d’identification national](eu-national-identification-number.md)de l’UE.</span><span class="sxs-lookup"><span data-stu-id="319ad-1949">To learn more, see [EU National Identification Number sensitive information type](eu-national-identification-number.md).</span></span>
  
## <a name="eu-passport-number"></a><span data-ttu-id="319ad-1950">Numéro de passeport UE</span><span class="sxs-lookup"><span data-stu-id="319ad-1950">EU Passport Number</span></span>

<span data-ttu-id="319ad-1951">Pour en savoir plus, consultez la rubrique [type d’informations sensibles du numéro de passeport européen](eu-passport-number.md).</span><span class="sxs-lookup"><span data-stu-id="319ad-1951">To learn more, see [EU Passport Number sensitive information type](eu-passport-number.md).</span></span>
  
## <a name="eu-social-security-number-or-equivalent-id"></a><span data-ttu-id="319ad-1952">Numéro de sécurité sociale de l’UE ou ID équivalent</span><span class="sxs-lookup"><span data-stu-id="319ad-1952">EU Social Security Number or Equivalent ID</span></span>

<span data-ttu-id="319ad-1953">Pour en savoir plus, consultez la rubrique [numéro de sécurité sociale de l’UE ou type d’informations sensibles ID équivalent](eu-social-security-number-or-equivalent-id.md).</span><span class="sxs-lookup"><span data-stu-id="319ad-1953">To learn more, see [EU Social Security Number or Equivalent ID sensitive information type](eu-social-security-number-or-equivalent-id.md).</span></span>
  
## <a name="eu-tax-identification-number"></a><span data-ttu-id="319ad-1954">Numéro d’identification fiscale de l’UE</span><span class="sxs-lookup"><span data-stu-id="319ad-1954">EU Tax Identification Number</span></span>

<span data-ttu-id="319ad-1955">Pour en savoir plus, consultez la rubrique [euro Tax identification number sensitive type information](eu-tax-identification-number.md).</span><span class="sxs-lookup"><span data-stu-id="319ad-1955">To learn more, see [EU Tax Identification Number sensitive information type](eu-tax-identification-number.md).</span></span>
  
## <a name="finland-national-id"></a><span data-ttu-id="319ad-1956">ID national finlandais</span><span class="sxs-lookup"><span data-stu-id="319ad-1956">Finland National ID</span></span>

### <a name="format"></a><span data-ttu-id="319ad-1957">Format</span><span class="sxs-lookup"><span data-stu-id="319ad-1957">Format</span></span>

<span data-ttu-id="319ad-1958">Six chiffres plus un caractère indiquant un siècle plus trois chiffres plus un chiffre de contrôle</span><span class="sxs-lookup"><span data-stu-id="319ad-1958">Six digits plus a character indicating a century plus three digits plus a check digit</span></span>

### <a name="pattern"></a><span data-ttu-id="319ad-1959">Modèle</span><span class="sxs-lookup"><span data-stu-id="319ad-1959">Pattern</span></span>

<span data-ttu-id="319ad-1960">Le modèle doit inclure tous les éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="319ad-1960">Pattern must include all of the following:</span></span>
- <span data-ttu-id="319ad-1961">Six chiffres au format JJMMAA qui représentent la date de naissance</span><span class="sxs-lookup"><span data-stu-id="319ad-1961">Six digits in the format format DDMMYY which are a date of birth</span></span> 
- <span data-ttu-id="319ad-1962">Marqueur de siècle (soit « - », « + » ou « a »)</span><span class="sxs-lookup"><span data-stu-id="319ad-1962">Century marker (either '-', '+' or 'a')</span></span> 
- <span data-ttu-id="319ad-1963">Numéro d’identification personnel à trois chiffres</span><span class="sxs-lookup"><span data-stu-id="319ad-1963">Three-digit personal identification number</span></span> 
- <span data-ttu-id="319ad-1964">Un chiffre ou une lettre (ne respectant pas la casse) de contrôle</span><span class="sxs-lookup"><span data-stu-id="319ad-1964">A digit or letter (case insensitive) which is a check digit</span></span>

### <a name="checksum"></a><span data-ttu-id="319ad-1965">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="319ad-1965">Checksum</span></span>

<span data-ttu-id="319ad-1966">Oui</span><span class="sxs-lookup"><span data-stu-id="319ad-1966">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="319ad-1967">Définition</span><span class="sxs-lookup"><span data-stu-id="319ad-1967">Definition</span></span>

<span data-ttu-id="319ad-1968">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="319ad-1968">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="319ad-1969">La fonction Func_finnish_national_id trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="319ad-1969">The function Func_finnish_national_id finds content that matches the pattern.</span></span>
- <span data-ttu-id="319ad-1970">Un mot clé figurant dans la liste Keyword_finnish_national_id est trouvé.</span><span class="sxs-lookup"><span data-stu-id="319ad-1970">A keyword from Keyword_finnish_national_id is found.</span></span>
- <span data-ttu-id="319ad-1971">La somme de contrôle est correcte.</span><span class="sxs-lookup"><span data-stu-id="319ad-1971">The checksum passes.</span></span>

```xml
<!-- Finnish National ID-->
<Entity id="338FD995-4CB5-4F87-AD35-79BD1DD926C1" patternsProximity="300" recommendedConfidence="85">
  <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_finnish_national_id" />
          <Match idRef="Keyword_finnish_national_id" />
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="319ad-1972">Mots-clés</span><span class="sxs-lookup"><span data-stu-id="319ad-1972">Keywords</span></span>

- <span data-ttu-id="319ad-1973">Keyword_finnish_national_id</span><span class="sxs-lookup"><span data-stu-id="319ad-1973">Keyword_finnish_national_id</span></span>
- <span data-ttu-id="319ad-1974">Sosiaaliturvatunnus</span><span class="sxs-lookup"><span data-stu-id="319ad-1974">Sosiaaliturvatunnus</span></span>
- <span data-ttu-id="319ad-1975">SOTU Henkilötunnus HETU</span><span class="sxs-lookup"><span data-stu-id="319ad-1975">SOTU Henkilötunnus HETU</span></span>
- <span data-ttu-id="319ad-1976">Personbeteckning</span><span class="sxs-lookup"><span data-stu-id="319ad-1976">Personbeteckning</span></span>
- <span data-ttu-id="319ad-1977">Personnummer</span><span class="sxs-lookup"><span data-stu-id="319ad-1977">Personnummer</span></span>
   
## <a name="finland-passport-number"></a><span data-ttu-id="319ad-1978">Numéro de passeport Finlande</span><span class="sxs-lookup"><span data-stu-id="319ad-1978">Finland Passport Number</span></span>

<span data-ttu-id="319ad-1979">Combinaison de format de neuf lettres et chiffres combinaison de neuf lettres et chiffres : deux lettres (ne respectant pas la casse) sept chiffres somme de contrôle no la stratégie DLP est de 75% en certitude qu’elle a détecté ce type d’informations sensibles si, dans un proximité de 300 caractères : l’expression régulière Regex_finland_passport_number trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="319ad-1979">Format Combination of nine letters and digits Pattern Combination of nine letters and digits: Two letters (not case sensitive) Seven digits Checksum No Definition A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters: The regular expression Regex_finland_passport_number finds content that matches the pattern.</span></span>
<span data-ttu-id="319ad-1980">Un mot clé figurant dans la liste Keyword_finland_passport_number est trouvé.</span><span class="sxs-lookup"><span data-stu-id="319ad-1980">A keyword from Keyword_finland_passport_number is found.</span></span>
<!-- Finland Passport Number -->
<span data-ttu-id="319ad-1981"><Entity id="d1685ac3-1d3a-40f8-8198-32ef5669c7a5" recommendedConfidence="75" patternsProximity="300"> <Pattern confidenceLevel="75"> <IdMatch idRef="Regex_finland_passport_number"/> <Match idRef="Keyword_finland_passport_number"/> </Pattern>
</Entity></span><span class="sxs-lookup"><span data-stu-id="319ad-1981"><Entity id="d1685ac3-1d3a-40f8-8198-32ef5669c7a5" recommendedConfidence="75" patternsProximity="300"> <Pattern confidenceLevel="75"> <IdMatch idRef="Regex_finland_passport_number"/> <Match idRef="Keyword_finland_passport_number"/> </Pattern>
</Entity></span></span>
<span data-ttu-id="319ad-1982">Mots clés Keyword_finland_passport_number Passport passes</span><span class="sxs-lookup"><span data-stu-id="319ad-1982">Keywords Keyword_finland_passport_number Passport Passi</span></span>
   
## <a name="france-drivers-license-number"></a><span data-ttu-id="319ad-1983">Numéro de permis de conduire France</span><span class="sxs-lookup"><span data-stu-id="319ad-1983">France Driver's License Number</span></span>

### <a name="format"></a><span data-ttu-id="319ad-1984">Format</span><span class="sxs-lookup"><span data-stu-id="319ad-1984">Format</span></span>

<span data-ttu-id="319ad-1985">12 chiffres</span><span class="sxs-lookup"><span data-stu-id="319ad-1985">12 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="319ad-1986">Modèle</span><span class="sxs-lookup"><span data-stu-id="319ad-1986">Pattern</span></span>

<span data-ttu-id="319ad-1987">12 chiffres avec validation pour écarter les modèles similaires, comme les numéros de téléphone français</span><span class="sxs-lookup"><span data-stu-id="319ad-1987">12 digits with validation to discount similar patterns such as French telephone numbers</span></span>

### <a name="checksum"></a><span data-ttu-id="319ad-1988">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="319ad-1988">Checksum</span></span>

<span data-ttu-id="319ad-1989">Non</span><span class="sxs-lookup"><span data-stu-id="319ad-1989">No</span></span>

### <a name="definition"></a><span data-ttu-id="319ad-1990">Définition</span><span class="sxs-lookup"><span data-stu-id="319ad-1990">Definition</span></span>

<span data-ttu-id="319ad-1991">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="319ad-1991">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="319ad-1992">La fonction Func_french_drivers_license trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="319ad-1992">The function Func_french_drivers_license finds content that matches the pattern.</span></span>
- <span data-ttu-id="319ad-1993">Au moins une des affirmations suivantes est vraie :</span><span class="sxs-lookup"><span data-stu-id="319ad-1993">At least one of the following is true:</span></span>
- <span data-ttu-id="319ad-1994">Un mot clé figurant dans la liste Keyword_french_drivers_license est trouvé.</span><span class="sxs-lookup"><span data-stu-id="319ad-1994">A keyword from Keyword_french_drivers_license is found.</span></span>
- <span data-ttu-id="319ad-1995">La fonction Func_eu_date trouve une date au format correct.</span><span class="sxs-lookup"><span data-stu-id="319ad-1995">The function Func_eu_date finds a date in the right date format.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="319ad-1996">Mots-clés</span><span class="sxs-lookup"><span data-stu-id="319ad-1996">Keywords</span></span>

#### <a name="keyword_french_drivers_license"></a><span data-ttu-id="319ad-1997">Keyword_french_drivers_license</span><span class="sxs-lookup"><span data-stu-id="319ad-1997">Keyword_french_drivers_license</span></span>

- <span data-ttu-id="319ad-1998">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="319ad-1998">drivers licence</span></span>
- <span data-ttu-id="319ad-1999">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="319ad-1999">drivers license</span></span>
- <span data-ttu-id="319ad-2000">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="319ad-2000">driving licence</span></span>
- <span data-ttu-id="319ad-2001">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="319ad-2001">driving license</span></span>
- <span data-ttu-id="319ad-2002">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="319ad-2002">permis de conduire</span></span>
- <span data-ttu-id="319ad-2003">numéro de permis</span><span class="sxs-lookup"><span data-stu-id="319ad-2003">licence number</span></span>
- <span data-ttu-id="319ad-2004">numéro de permis</span><span class="sxs-lookup"><span data-stu-id="319ad-2004">license number</span></span>
- <span data-ttu-id="319ad-2005">numéros de permis</span><span class="sxs-lookup"><span data-stu-id="319ad-2005">licence numbers</span></span>
- <span data-ttu-id="319ad-2006">numéros de permis</span><span class="sxs-lookup"><span data-stu-id="319ad-2006">license numbers</span></span>

## <a name="france-national-id-card-cni"></a><span data-ttu-id="319ad-2007">Carte nationale d’identité (CNI) France</span><span class="sxs-lookup"><span data-stu-id="319ad-2007">France National ID Card (CNI)</span></span>

### <a name="format"></a><span data-ttu-id="319ad-2008">Format</span><span class="sxs-lookup"><span data-stu-id="319ad-2008">Format</span></span>

<span data-ttu-id="319ad-2009">12 chiffres</span><span class="sxs-lookup"><span data-stu-id="319ad-2009">12 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="319ad-2010">Modèle</span><span class="sxs-lookup"><span data-stu-id="319ad-2010">Pattern</span></span>

<span data-ttu-id="319ad-2011">12 chiffres</span><span class="sxs-lookup"><span data-stu-id="319ad-2011">12 digits</span></span>

### <a name="checksum"></a><span data-ttu-id="319ad-2012">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="319ad-2012">Checksum</span></span>

<span data-ttu-id="319ad-2013">Non</span><span class="sxs-lookup"><span data-stu-id="319ad-2013">No</span></span>

### <a name="definition"></a><span data-ttu-id="319ad-2014">Définition</span><span class="sxs-lookup"><span data-stu-id="319ad-2014">Definition</span></span>

<span data-ttu-id="319ad-2015">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 65 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="319ad-2015">A DLP policy is 65% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="319ad-2016">L’expression régulière Regex_france_cni trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="319ad-2016">The regular expression Regex_france_cni finds content that matches the pattern.</span></span>

```xml
<!-- France CNI -->
<Entity id="f741ac74-1bc0-4665-b69b-f0c7f927c0c4" patternsProximity="300" recommendedConfidence="65">
  <Pattern confidenceLevel="65">
        <IdMatch idRef="Regex_france_cni" />
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="319ad-2017">Mots-clés</span><span class="sxs-lookup"><span data-stu-id="319ad-2017">Keywords</span></span>

<span data-ttu-id="319ad-2018">Aucun</span><span class="sxs-lookup"><span data-stu-id="319ad-2018">None</span></span>
   
## <a name="france-passport-number"></a><span data-ttu-id="319ad-2019">Numéro de passeport France</span><span class="sxs-lookup"><span data-stu-id="319ad-2019">France Passport Number</span></span>

### <a name="format"></a><span data-ttu-id="319ad-2020">Format</span><span class="sxs-lookup"><span data-stu-id="319ad-2020">Format</span></span>

<span data-ttu-id="319ad-2021">Neuf chiffres et lettres</span><span class="sxs-lookup"><span data-stu-id="319ad-2021">Nine digits and letters</span></span>

### <a name="pattern"></a><span data-ttu-id="319ad-2022">Modèle</span><span class="sxs-lookup"><span data-stu-id="319ad-2022">Pattern</span></span>

<span data-ttu-id="319ad-2023">Neuf chiffres et lettres :</span><span class="sxs-lookup"><span data-stu-id="319ad-2023">Nine digits and letters:</span></span>
- <span data-ttu-id="319ad-2024">Deux chiffres</span><span class="sxs-lookup"><span data-stu-id="319ad-2024">Two digits</span></span> 
- <span data-ttu-id="319ad-2025">Deux lettres (ne respectent pas la casse)</span><span class="sxs-lookup"><span data-stu-id="319ad-2025">Two letters (not case sensitive)</span></span> 
- <span data-ttu-id="319ad-2026">Cinq chiffres</span><span class="sxs-lookup"><span data-stu-id="319ad-2026">Five digits</span></span>

### <a name="checksum"></a><span data-ttu-id="319ad-2027">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="319ad-2027">Checksum</span></span>

<span data-ttu-id="319ad-2028">Non</span><span class="sxs-lookup"><span data-stu-id="319ad-2028">No</span></span>

### <a name="definition"></a><span data-ttu-id="319ad-2029">Définition</span><span class="sxs-lookup"><span data-stu-id="319ad-2029">Definition</span></span>

<span data-ttu-id="319ad-2030">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="319ad-2030">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="319ad-2031">La fonction Func_fr_passport trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="319ad-2031">The function Func_fr_passport finds content that matches the pattern.</span></span>
- <span data-ttu-id="319ad-2032">Un mot clé figurant dans la liste Keyword_passport est trouvé.</span><span class="sxs-lookup"><span data-stu-id="319ad-2032">A keyword from Keyword_passport is found.</span></span>

```xml
<!-- France Passport Number -->
<Entity id="3008b884-8c8c-4cd8-a289-99f34fc7ff5d" patternsProximity="300" recommendedConfidence="75">
  <Pattern confidenceLevel="75">
        <IdMatch idRef="Func_fr_passport" />
        <Match idRef="Keyword_passport" />
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="319ad-2033">Mots-clés</span><span class="sxs-lookup"><span data-stu-id="319ad-2033">Keywords</span></span>

#### <a name="keyword_passport"></a><span data-ttu-id="319ad-2034">Keyword_passport</span><span class="sxs-lookup"><span data-stu-id="319ad-2034">Keyword_passport</span></span>

- <span data-ttu-id="319ad-2035">Numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="319ad-2035">Passport Number</span></span>
- <span data-ttu-id="319ad-2036">N° de passeport</span><span class="sxs-lookup"><span data-stu-id="319ad-2036">Passport No</span></span>
- <span data-ttu-id="319ad-2037"># Passeport</span><span class="sxs-lookup"><span data-stu-id="319ad-2037">Passport #</span></span>
- <span data-ttu-id="319ad-2038">Tel #</span><span class="sxs-lookup"><span data-stu-id="319ad-2038">Passport#</span></span>
- <span data-ttu-id="319ad-2039">PassportID</span><span class="sxs-lookup"><span data-stu-id="319ad-2039">PassportID</span></span>
- <span data-ttu-id="319ad-2040">N ° passeport</span><span class="sxs-lookup"><span data-stu-id="319ad-2040">Passportno</span></span>
- <span data-ttu-id="319ad-2041">passportnumber</span><span class="sxs-lookup"><span data-stu-id="319ad-2041">passportnumber</span></span>
- <span data-ttu-id="319ad-2042">パスポート</span><span class="sxs-lookup"><span data-stu-id="319ad-2042">パスポート</span></span>
- <span data-ttu-id="319ad-2043">パスポート番号</span><span class="sxs-lookup"><span data-stu-id="319ad-2043">パスポート番号</span></span>
- <span data-ttu-id="319ad-2044">パスポートのNum</span><span class="sxs-lookup"><span data-stu-id="319ad-2044">パスポートのNum</span></span>
- <span data-ttu-id="319ad-2045">パスポート＃</span><span class="sxs-lookup"><span data-stu-id="319ad-2045">パスポート ＃</span></span> 
- <span data-ttu-id="319ad-2046">Numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="319ad-2046">Numéro de passeport</span></span>
- <span data-ttu-id="319ad-2047">Passeport n°</span><span class="sxs-lookup"><span data-stu-id="319ad-2047">Passeport n °</span></span>
- <span data-ttu-id="319ad-2048">Passeport numéro</span><span class="sxs-lookup"><span data-stu-id="319ad-2048">Passeport Non</span></span>
- <span data-ttu-id="319ad-2049"># Passeport</span><span class="sxs-lookup"><span data-stu-id="319ad-2049">Passeport #</span></span>
- <span data-ttu-id="319ad-2050">Passeport #</span><span class="sxs-lookup"><span data-stu-id="319ad-2050">Passeport#</span></span>
- <span data-ttu-id="319ad-2051">PasseportNon</span><span class="sxs-lookup"><span data-stu-id="319ad-2051">PasseportNon</span></span>
- <span data-ttu-id="319ad-2052">Passeportn °</span><span class="sxs-lookup"><span data-stu-id="319ad-2052">Passeportn °</span></span>

      
## <a name="france-social-security-number-insee"></a><span data-ttu-id="319ad-2053">Numéro de sécurité sociale (INSEE) France</span><span class="sxs-lookup"><span data-stu-id="319ad-2053">France Social Security Number (INSEE)</span></span>

### <a name="format"></a><span data-ttu-id="319ad-2054">Format</span><span class="sxs-lookup"><span data-stu-id="319ad-2054">Format</span></span>

<span data-ttu-id="319ad-2055">15 chiffres</span><span class="sxs-lookup"><span data-stu-id="319ad-2055">15 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="319ad-2056">Modèle</span><span class="sxs-lookup"><span data-stu-id="319ad-2056">Pattern</span></span>

<span data-ttu-id="319ad-2057">Doit correspondre à l’un des deux modèles suivants :</span><span class="sxs-lookup"><span data-stu-id="319ad-2057">Must match one of two patterns:</span></span>
- <span data-ttu-id="319ad-2058">13 chiffres suivis d’un espace suivi de deux chiffres</span><span class="sxs-lookup"><span data-stu-id="319ad-2058">13 digits followed by a space followed by two digits</span></span><br/>
<span data-ttu-id="319ad-2059">ou</span><span class="sxs-lookup"><span data-stu-id="319ad-2059">or</span></span>
- <span data-ttu-id="319ad-2060">15 chiffres consécutifs</span><span class="sxs-lookup"><span data-stu-id="319ad-2060">15 consecutive digits</span></span>

### <a name="checksum"></a><span data-ttu-id="319ad-2061">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="319ad-2061">Checksum</span></span>

<span data-ttu-id="319ad-2062">Oui</span><span class="sxs-lookup"><span data-stu-id="319ad-2062">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="319ad-2063">Définition</span><span class="sxs-lookup"><span data-stu-id="319ad-2063">Definition</span></span>

<span data-ttu-id="319ad-2064">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 95 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="319ad-2064">A DLP policy is 95% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="319ad-2065">La fonction Func_french_insee ou Func_fr_insee trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="319ad-2065">The function Func_french_insee or Func_fr_insee finds content that matches the pattern.</span></span>
- <span data-ttu-id="319ad-2066">Un mot clé figurant dans la liste Keyword_fr_insee est trouvé.</span><span class="sxs-lookup"><span data-stu-id="319ad-2066">A keyword from Keyword_fr_insee is found.</span></span>
- <span data-ttu-id="319ad-2067">La somme de contrôle est correcte.</span><span class="sxs-lookup"><span data-stu-id="319ad-2067">The checksum passes.</span></span>

<span data-ttu-id="319ad-2068">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="319ad-2068">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="319ad-2069">La fonction Func_french_insee ou Func_fr_insee trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="319ad-2069">The function Func_french_insee or Func_fr_insee finds content that matches the pattern.</span></span>
- <span data-ttu-id="319ad-2070">Aucun mot clé figurant dans la liste Keyword_fr_insee n’est trouvé.</span><span class="sxs-lookup"><span data-stu-id="319ad-2070">No keyword from Keyword_fr_insee is found.</span></span>
- <span data-ttu-id="319ad-2071">La somme de contrôle est correcte.</span><span class="sxs-lookup"><span data-stu-id="319ad-2071">The checksum passes.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="319ad-2072">Mots-clés</span><span class="sxs-lookup"><span data-stu-id="319ad-2072">Keywords</span></span>

#### <a name="keyword_fr_insee"></a><span data-ttu-id="319ad-2073">Keyword_fr_insee</span><span class="sxs-lookup"><span data-stu-id="319ad-2073">Keyword_fr_insee</span></span>

- <span data-ttu-id="319ad-2074">INSEE</span><span class="sxs-lookup"><span data-stu-id="319ad-2074">insee</span></span>
- <span data-ttu-id="319ad-2075">securité sociale</span><span class="sxs-lookup"><span data-stu-id="319ad-2075">securité sociale</span></span>
- <span data-ttu-id="319ad-2076">securite sociale</span><span class="sxs-lookup"><span data-stu-id="319ad-2076">securite sociale</span></span>
- <span data-ttu-id="319ad-2077">id national</span><span class="sxs-lookup"><span data-stu-id="319ad-2077">national id</span></span>
- <span data-ttu-id="319ad-2078">numéro d’identification nationale</span><span class="sxs-lookup"><span data-stu-id="319ad-2078">national identification</span></span>
- <span data-ttu-id="319ad-2079">numéro d’identité</span><span class="sxs-lookup"><span data-stu-id="319ad-2079">numéro d'identité</span></span>
- <span data-ttu-id="319ad-2080">n° d’identité</span><span class="sxs-lookup"><span data-stu-id="319ad-2080">no d'identité</span></span>
- <span data-ttu-id="319ad-2081">Nbre.</span><span class="sxs-lookup"><span data-stu-id="319ad-2081">no.</span></span> <span data-ttu-id="319ad-2082">d’identité</span><span class="sxs-lookup"><span data-stu-id="319ad-2082">d'identité</span></span>
- <span data-ttu-id="319ad-2083">numéro d’identité</span><span class="sxs-lookup"><span data-stu-id="319ad-2083">numero d'identite</span></span>
- <span data-ttu-id="319ad-2084">n° d’identité</span><span class="sxs-lookup"><span data-stu-id="319ad-2084">no d'identite</span></span>
- <span data-ttu-id="319ad-2085">Nbre.</span><span class="sxs-lookup"><span data-stu-id="319ad-2085">no.</span></span> <span data-ttu-id="319ad-2086">d’identite</span><span class="sxs-lookup"><span data-stu-id="319ad-2086">d'identite</span></span>
- <span data-ttu-id="319ad-2087">numéro de sécurité sociale</span><span class="sxs-lookup"><span data-stu-id="319ad-2087">social security number</span></span>
- <span data-ttu-id="319ad-2088">code de sécurité sociale</span><span class="sxs-lookup"><span data-stu-id="319ad-2088">social security code</span></span>
- <span data-ttu-id="319ad-2089">numéro d’assurance sociale</span><span class="sxs-lookup"><span data-stu-id="319ad-2089">social insurance number</span></span>
- <span data-ttu-id="319ad-2090">le numéro d’identification nationale</span><span class="sxs-lookup"><span data-stu-id="319ad-2090">le numéro d'identification nationale</span></span>
- <span data-ttu-id="319ad-2091">d’identité nationale</span><span class="sxs-lookup"><span data-stu-id="319ad-2091">d'identité nationale</span></span>
- <span data-ttu-id="319ad-2092">numéro de sécurité sociale</span><span class="sxs-lookup"><span data-stu-id="319ad-2092">numéro de sécurité sociale</span></span>
- <span data-ttu-id="319ad-2093">le code de la sécurité sociale</span><span class="sxs-lookup"><span data-stu-id="319ad-2093">le code de la sécurité sociale</span></span>
- <span data-ttu-id="319ad-2094">numéro d’assurance sociale</span><span class="sxs-lookup"><span data-stu-id="319ad-2094">numéro d'assurance sociale</span></span>
- <span data-ttu-id="319ad-2095">numéro de sécu</span><span class="sxs-lookup"><span data-stu-id="319ad-2095">numéro de sécu</span></span>
- <span data-ttu-id="319ad-2096">code sécu</span><span class="sxs-lookup"><span data-stu-id="319ad-2096">code sécu</span></span> 
   
## <a name="german-drivers-license-number"></a><span data-ttu-id="319ad-2097">Numéro de permis de conduire Allemagne</span><span class="sxs-lookup"><span data-stu-id="319ad-2097">German Driver's License Number</span></span>

### <a name="format"></a><span data-ttu-id="319ad-2098">Format</span><span class="sxs-lookup"><span data-stu-id="319ad-2098">Format</span></span>

<span data-ttu-id="319ad-2099">Combinaison de 11 chiffres et lettres</span><span class="sxs-lookup"><span data-stu-id="319ad-2099">Combination of 11 digits and letters</span></span>

### <a name="pattern"></a><span data-ttu-id="319ad-2100">Modèle</span><span class="sxs-lookup"><span data-stu-id="319ad-2100">Pattern</span></span>

<span data-ttu-id="319ad-2101">11 chiffres et lettres (ne respectent pas la casse) :</span><span class="sxs-lookup"><span data-stu-id="319ad-2101">11 digits and letters (not case sensitive):</span></span>
- <span data-ttu-id="319ad-2102">Un chiffre ou une lettre</span><span class="sxs-lookup"><span data-stu-id="319ad-2102">A digit or letter</span></span> 
- <span data-ttu-id="319ad-2103">Deux chiffres</span><span class="sxs-lookup"><span data-stu-id="319ad-2103">Two digits</span></span> 
- <span data-ttu-id="319ad-2104">Six chiffres ou lettres</span><span class="sxs-lookup"><span data-stu-id="319ad-2104">Six digits or letters</span></span> 
- <span data-ttu-id="319ad-2105">Un chiffre</span><span class="sxs-lookup"><span data-stu-id="319ad-2105">A digit</span></span> 
- <span data-ttu-id="319ad-2106">Un chiffre ou une lettre</span><span class="sxs-lookup"><span data-stu-id="319ad-2106">A digit or letter</span></span>

### <a name="checksum"></a><span data-ttu-id="319ad-2107">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="319ad-2107">Checksum</span></span>

<span data-ttu-id="319ad-2108">Oui</span><span class="sxs-lookup"><span data-stu-id="319ad-2108">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="319ad-2109">Définition</span><span class="sxs-lookup"><span data-stu-id="319ad-2109">Definition</span></span>

<span data-ttu-id="319ad-2110">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="319ad-2110">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="319ad-2111">La fonction Func_german_drivers_license trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="319ad-2111">The function Func_german_drivers_license finds content that matches the pattern.</span></span>
- <span data-ttu-id="319ad-2112">Au moins une des affirmations suivantes est vraie :</span><span class="sxs-lookup"><span data-stu-id="319ad-2112">At least one of the following is true:</span></span>
    - <span data-ttu-id="319ad-2113">Un mot clé figurant dans la liste Keyword_german_drivers_license_number est trouvé.</span><span class="sxs-lookup"><span data-stu-id="319ad-2113">A keyword from Keyword_german_drivers_license_number is found.</span></span>
    - <span data-ttu-id="319ad-2114">Un mot clé figurant dans la liste Keyword_german_drivers_license_collaborative est trouvé.</span><span class="sxs-lookup"><span data-stu-id="319ad-2114">A keyword from Keyword_german_drivers_license_collaborative is found.</span></span>
    - <span data-ttu-id="319ad-2115">Un mot clé figurant dans la liste Keyword_german_drivers_license est trouvé.</span><span class="sxs-lookup"><span data-stu-id="319ad-2115">A keyword from Keyword_german_drivers_license is found.</span></span>
- <span data-ttu-id="319ad-2116">La somme de contrôle est correcte.</span><span class="sxs-lookup"><span data-stu-id="319ad-2116">The checksum passes.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="319ad-2117">Mots-clés</span><span class="sxs-lookup"><span data-stu-id="319ad-2117">Keywords</span></span>

#### <a name="keyword_german_drivers_license_number"></a><span data-ttu-id="319ad-2118">Keyword_german_drivers_license_number</span><span class="sxs-lookup"><span data-stu-id="319ad-2118">Keyword_german_drivers_license_number</span></span>

- <span data-ttu-id="319ad-2119">Führerschein</span><span class="sxs-lookup"><span data-stu-id="319ad-2119">Führerschein</span></span>
- <span data-ttu-id="319ad-2120">Fuhrerschein</span><span class="sxs-lookup"><span data-stu-id="319ad-2120">Fuhrerschein</span></span>
- <span data-ttu-id="319ad-2121">Fuehrerschein</span><span class="sxs-lookup"><span data-stu-id="319ad-2121">Fuehrerschein</span></span>
- <span data-ttu-id="319ad-2122">Führerscheinnummer</span><span class="sxs-lookup"><span data-stu-id="319ad-2122">Führerscheinnummer</span></span>
- <span data-ttu-id="319ad-2123">Fuhrerscheinnummer</span><span class="sxs-lookup"><span data-stu-id="319ad-2123">Fuhrerscheinnummer</span></span>
- <span data-ttu-id="319ad-2124">Fuehrerscheinnummer</span><span class="sxs-lookup"><span data-stu-id="319ad-2124">Fuehrerscheinnummer</span></span>
- <span data-ttu-id="319ad-2125">Führerschein</span><span class="sxs-lookup"><span data-stu-id="319ad-2125">Führerschein-</span></span> 
- <span data-ttu-id="319ad-2126">Fuhrerschein</span><span class="sxs-lookup"><span data-stu-id="319ad-2126">Fuhrerschein-</span></span> 
- <span data-ttu-id="319ad-2127">Fuehrerschein</span><span class="sxs-lookup"><span data-stu-id="319ad-2127">Fuehrerschein-</span></span> 
- <span data-ttu-id="319ad-2128">FührerscheinnummerNr</span><span class="sxs-lookup"><span data-stu-id="319ad-2128">FührerscheinnummerNr</span></span>
- <span data-ttu-id="319ad-2129">FuhrerscheinnummerNr</span><span class="sxs-lookup"><span data-stu-id="319ad-2129">FuhrerscheinnummerNr</span></span>
- <span data-ttu-id="319ad-2130">FuehrerscheinnummerNr</span><span class="sxs-lookup"><span data-stu-id="319ad-2130">FuehrerscheinnummerNr</span></span>
- <span data-ttu-id="319ad-2131">FührerscheinnummerKlasse</span><span class="sxs-lookup"><span data-stu-id="319ad-2131">FührerscheinnummerKlasse</span></span>
- <span data-ttu-id="319ad-2132">FuhrerscheinnummerKlasse</span><span class="sxs-lookup"><span data-stu-id="319ad-2132">FuhrerscheinnummerKlasse</span></span>
- <span data-ttu-id="319ad-2133">FuehrerscheinnummerKlasse</span><span class="sxs-lookup"><span data-stu-id="319ad-2133">FuehrerscheinnummerKlasse</span></span>
- <span data-ttu-id="319ad-2134">Führerschein - Nr</span><span class="sxs-lookup"><span data-stu-id="319ad-2134">Führerschein- Nr</span></span>
- <span data-ttu-id="319ad-2135">Fuhrerschein - Nr</span><span class="sxs-lookup"><span data-stu-id="319ad-2135">Fuhrerschein- Nr</span></span>
- <span data-ttu-id="319ad-2136">Fuehrerschein - Nr</span><span class="sxs-lookup"><span data-stu-id="319ad-2136">Fuehrerschein- Nr</span></span> 
- <span data-ttu-id="319ad-2137">Führerschein - Klasse</span><span class="sxs-lookup"><span data-stu-id="319ad-2137">Führerschein- Klasse</span></span> 
- <span data-ttu-id="319ad-2138">Fuhrerschein - Klasse</span><span class="sxs-lookup"><span data-stu-id="319ad-2138">Fuhrerschein- Klasse</span></span> 
- <span data-ttu-id="319ad-2139">Fuehrerschein - Klasse</span><span class="sxs-lookup"><span data-stu-id="319ad-2139">Fuehrerschein- Klasse</span></span>
- <span data-ttu-id="319ad-2140">FührerscheinnummerNr</span><span class="sxs-lookup"><span data-stu-id="319ad-2140">FührerscheinnummerNr</span></span> 
- <span data-ttu-id="319ad-2141">FuhrerscheinnummerNr</span><span class="sxs-lookup"><span data-stu-id="319ad-2141">FuhrerscheinnummerNr</span></span> 
- <span data-ttu-id="319ad-2142">FuehrerscheinnummerNr</span><span class="sxs-lookup"><span data-stu-id="319ad-2142">FuehrerscheinnummerNr</span></span> 
- <span data-ttu-id="319ad-2143">FührerscheinnummerKlasse</span><span class="sxs-lookup"><span data-stu-id="319ad-2143">FührerscheinnummerKlasse</span></span> 
- <span data-ttu-id="319ad-2144">FuhrerscheinnummerKlasse</span><span class="sxs-lookup"><span data-stu-id="319ad-2144">FuhrerscheinnummerKlasse</span></span> 
- <span data-ttu-id="319ad-2145">FuehrerscheinnummerKlasse</span><span class="sxs-lookup"><span data-stu-id="319ad-2145">FuehrerscheinnummerKlasse</span></span> 
- <span data-ttu-id="319ad-2146">Führerschein - Nr</span><span class="sxs-lookup"><span data-stu-id="319ad-2146">Führerschein- Nr</span></span> 
- <span data-ttu-id="319ad-2147">Fuhrerschein - Nr</span><span class="sxs-lookup"><span data-stu-id="319ad-2147">Fuhrerschein- Nr</span></span> 
- <span data-ttu-id="319ad-2148">Fuehrerschein - Nr</span><span class="sxs-lookup"><span data-stu-id="319ad-2148">Fuehrerschein- Nr</span></span> 
- <span data-ttu-id="319ad-2149">Führerschein - Klasse</span><span class="sxs-lookup"><span data-stu-id="319ad-2149">Führerschein- Klasse</span></span> 
- <span data-ttu-id="319ad-2150">Fuhrerschein - Klasse</span><span class="sxs-lookup"><span data-stu-id="319ad-2150">Fuhrerschein- Klasse</span></span> 
- <span data-ttu-id="319ad-2151">Fuehrerschein - Klasse</span><span class="sxs-lookup"><span data-stu-id="319ad-2151">Fuehrerschein- Klasse</span></span> 
- <span data-ttu-id="319ad-2152">LD</span><span class="sxs-lookup"><span data-stu-id="319ad-2152">DL</span></span> 
- <span data-ttu-id="319ad-2153">DISTRIBUTION</span><span class="sxs-lookup"><span data-stu-id="319ad-2153">DLS</span></span>
- <span data-ttu-id="319ad-2154">Permis conduire</span><span class="sxs-lookup"><span data-stu-id="319ad-2154">Driv Lic</span></span> 
- <span data-ttu-id="319ad-2155">Permis conduire</span><span class="sxs-lookup"><span data-stu-id="319ad-2155">Driv Licen</span></span> 
- <span data-ttu-id="319ad-2156">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="319ad-2156">Driv License</span></span>
- <span data-ttu-id="319ad-2157">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="319ad-2157">Driv Licenses</span></span> 
- <span data-ttu-id="319ad-2158">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="319ad-2158">Driv Licence</span></span> 
- <span data-ttu-id="319ad-2159">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="319ad-2159">Driv Licences</span></span> 
- <span data-ttu-id="319ad-2160">Permis conduire</span><span class="sxs-lookup"><span data-stu-id="319ad-2160">Driv Lic</span></span> 
- <span data-ttu-id="319ad-2161">Permis conduire</span><span class="sxs-lookup"><span data-stu-id="319ad-2161">Driver Licen</span></span> 
- <span data-ttu-id="319ad-2162">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="319ad-2162">Driver License</span></span> 
- <span data-ttu-id="319ad-2163">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="319ad-2163">Driver Licenses</span></span> 
- <span data-ttu-id="319ad-2164">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="319ad-2164">Driver Licence</span></span> 
- <span data-ttu-id="319ad-2165">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="319ad-2165">Driver Licences</span></span> 
- <span data-ttu-id="319ad-2166">Permis conduire</span><span class="sxs-lookup"><span data-stu-id="319ad-2166">Drivers Lic</span></span> 
- <span data-ttu-id="319ad-2167">Permis conduire</span><span class="sxs-lookup"><span data-stu-id="319ad-2167">Drivers Licen</span></span> 
- <span data-ttu-id="319ad-2168">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="319ad-2168">Drivers License</span></span> 
- <span data-ttu-id="319ad-2169">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="319ad-2169">Drivers Licenses</span></span> 
- <span data-ttu-id="319ad-2170">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="319ad-2170">Drivers Licence</span></span> 
- <span data-ttu-id="319ad-2171">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="319ad-2171">Drivers Licences</span></span> 
- <span data-ttu-id="319ad-2172">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="319ad-2172">Driver's Lic</span></span> 
- <span data-ttu-id="319ad-2173">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="319ad-2173">Driver's Licen</span></span> 
- <span data-ttu-id="319ad-2174">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="319ad-2174">Driver's License</span></span> 
- <span data-ttu-id="319ad-2175">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="319ad-2175">Driver's Licenses</span></span> 
- <span data-ttu-id="319ad-2176">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="319ad-2176">Driver's Licence</span></span> 
- <span data-ttu-id="319ad-2177">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="319ad-2177">Driver's Licences</span></span> 
- <span data-ttu-id="319ad-2178">Permis conduire</span><span class="sxs-lookup"><span data-stu-id="319ad-2178">Driving Lic</span></span> 
- <span data-ttu-id="319ad-2179">Permis conduire</span><span class="sxs-lookup"><span data-stu-id="319ad-2179">Driving Licen</span></span> 
- <span data-ttu-id="319ad-2180">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="319ad-2180">Driving License</span></span> 
- <span data-ttu-id="319ad-2181">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="319ad-2181">Driving Licenses</span></span> 
- <span data-ttu-id="319ad-2182">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="319ad-2182">Driving Licence</span></span> 
- <span data-ttu-id="319ad-2183">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="319ad-2183">Driving Licences</span></span>

#### <a name="keyword_german_drivers_license_collaborative"></a><span data-ttu-id="319ad-2184">Keyword_german_drivers_license_collaborative</span><span class="sxs-lookup"><span data-stu-id="319ad-2184">Keyword_german_drivers_license_collaborative</span></span>

- <span data-ttu-id="319ad-2185">Nr-Führerschein</span><span class="sxs-lookup"><span data-stu-id="319ad-2185">Nr-Führerschein</span></span> 
- <span data-ttu-id="319ad-2186">Nr-Fuhrerschein</span><span class="sxs-lookup"><span data-stu-id="319ad-2186">Nr-Fuhrerschein</span></span> 
- <span data-ttu-id="319ad-2187">Nr-Fuehrerschein</span><span class="sxs-lookup"><span data-stu-id="319ad-2187">Nr-Fuehrerschein</span></span> 
- <span data-ttu-id="319ad-2188">Non-Führerschein</span><span class="sxs-lookup"><span data-stu-id="319ad-2188">No-Führerschein</span></span> 
- <span data-ttu-id="319ad-2189">Non-Fuhrerschein</span><span class="sxs-lookup"><span data-stu-id="319ad-2189">No-Fuhrerschein</span></span> 
- <span data-ttu-id="319ad-2190">Non-Fuehrerschein</span><span class="sxs-lookup"><span data-stu-id="319ad-2190">No-Fuehrerschein</span></span> 
- <span data-ttu-id="319ad-2191">N-Führerschein</span><span class="sxs-lookup"><span data-stu-id="319ad-2191">N-Führerschein</span></span> 
- <span data-ttu-id="319ad-2192">N-Fuhrerschein</span><span class="sxs-lookup"><span data-stu-id="319ad-2192">N-Fuhrerschein</span></span> 
- <span data-ttu-id="319ad-2193">N-Fuehrerschein</span><span class="sxs-lookup"><span data-stu-id="319ad-2193">N-Fuehrerschein</span></span>
- <span data-ttu-id="319ad-2194">Nr-Führerschein</span><span class="sxs-lookup"><span data-stu-id="319ad-2194">Nr-Führerschein</span></span> 
- <span data-ttu-id="319ad-2195">Nr-Fuhrerschein</span><span class="sxs-lookup"><span data-stu-id="319ad-2195">Nr-Fuhrerschein</span></span> 
- <span data-ttu-id="319ad-2196">Nr-Fuehrerschein</span><span class="sxs-lookup"><span data-stu-id="319ad-2196">Nr-Fuehrerschein</span></span> 
- <span data-ttu-id="319ad-2197">Non-Führerschein</span><span class="sxs-lookup"><span data-stu-id="319ad-2197">No-Führerschein</span></span> 
- <span data-ttu-id="319ad-2198">Non-Fuhrerschein</span><span class="sxs-lookup"><span data-stu-id="319ad-2198">No-Fuhrerschein</span></span> 
- <span data-ttu-id="319ad-2199">Non-Fuehrerschein</span><span class="sxs-lookup"><span data-stu-id="319ad-2199">No-Fuehrerschein</span></span> 
- <span data-ttu-id="319ad-2200">N-Führerschein</span><span class="sxs-lookup"><span data-stu-id="319ad-2200">N-Führerschein</span></span> 
- <span data-ttu-id="319ad-2201">N-Fuhrerschein</span><span class="sxs-lookup"><span data-stu-id="319ad-2201">N-Fuhrerschein</span></span> 
- <span data-ttu-id="319ad-2202">N-Fuehrerschein</span><span class="sxs-lookup"><span data-stu-id="319ad-2202">N-Fuehrerschein</span></span> 

#### <a name="keyword_german_drivers_license"></a><span data-ttu-id="319ad-2203">Keyword_german_drivers_license</span><span class="sxs-lookup"><span data-stu-id="319ad-2203">Keyword_german_drivers_license</span></span>

- <span data-ttu-id="319ad-2204">ausstellungsdatum</span><span class="sxs-lookup"><span data-stu-id="319ad-2204">ausstellungsdatum</span></span>
- <span data-ttu-id="319ad-2205">ausstellungsort</span><span class="sxs-lookup"><span data-stu-id="319ad-2205">ausstellungsort</span></span>
- <span data-ttu-id="319ad-2206">ausstellende behöde</span><span class="sxs-lookup"><span data-stu-id="319ad-2206">ausstellende behöde</span></span>
- <span data-ttu-id="319ad-2207">ausstellende behorde</span><span class="sxs-lookup"><span data-stu-id="319ad-2207">ausstellende behorde</span></span>
- <span data-ttu-id="319ad-2208">ausstellende behoerde</span><span class="sxs-lookup"><span data-stu-id="319ad-2208">ausstellende behoerde</span></span>
   
## <a name="german-passport-number"></a><span data-ttu-id="319ad-2209">Numéro de passeport Allemagne</span><span class="sxs-lookup"><span data-stu-id="319ad-2209">German Passport Number</span></span>

### <a name="format"></a><span data-ttu-id="319ad-2210">Format</span><span class="sxs-lookup"><span data-stu-id="319ad-2210">Format</span></span>

<span data-ttu-id="319ad-2211">10 chiffres ou lettres</span><span class="sxs-lookup"><span data-stu-id="319ad-2211">10 digits or letters</span></span>

### <a name="pattern"></a><span data-ttu-id="319ad-2212">Modèle</span><span class="sxs-lookup"><span data-stu-id="319ad-2212">Pattern</span></span>

<span data-ttu-id="319ad-2213">Le modèle doit inclure tous les éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="319ad-2213">Pattern must include all of the following:</span></span>
- <span data-ttu-id="319ad-2214">Le premier caractère est un chiffre ou une lettre de cet ensemble (C, F, G, H, J, K)</span><span class="sxs-lookup"><span data-stu-id="319ad-2214">First character is a digit or a letter from this set (C, F, G, H, J, K)</span></span> 
- <span data-ttu-id="319ad-2215">Trois chiffres</span><span class="sxs-lookup"><span data-stu-id="319ad-2215">Three digits</span></span> 
- <span data-ttu-id="319ad-2216">Cinq chiffres ou lettres à partir de cet ensemble (C, -H, J-N, P, R, T, V-Z)</span><span class="sxs-lookup"><span data-stu-id="319ad-2216">Five digits or letters from this set (C, -H, J-N, P, R, T, V-Z)</span></span> 
- <span data-ttu-id="319ad-2217">Un chiffre</span><span class="sxs-lookup"><span data-stu-id="319ad-2217">A digit</span></span>

### <a name="checksum"></a><span data-ttu-id="319ad-2218">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="319ad-2218">Checksum</span></span>

<span data-ttu-id="319ad-2219">Oui</span><span class="sxs-lookup"><span data-stu-id="319ad-2219">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="319ad-2220">Définition</span><span class="sxs-lookup"><span data-stu-id="319ad-2220">Definition</span></span>

<span data-ttu-id="319ad-2221">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="319ad-2221">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="319ad-2222">La fonction Func_german_passport trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="319ad-2222">The function Func_german_passport finds content that matches the pattern.</span></span>
- <span data-ttu-id="319ad-2223">Un mot clé présent dans l’une des cinq listes de mots clés est trouvé.</span><span class="sxs-lookup"><span data-stu-id="319ad-2223">A keyword from any of the five keyword lists is found.</span></span>
- <span data-ttu-id="319ad-2224">La somme de contrôle est correcte.</span><span class="sxs-lookup"><span data-stu-id="319ad-2224">The checksum passes.</span></span>

<span data-ttu-id="319ad-2225">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="319ad-2225">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="319ad-2226">La fonction Func_german_passport_data trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="319ad-2226">The function Func_german_passport_data finds content that matches the pattern.</span></span>
- <span data-ttu-id="319ad-2227">Un mot clé présent dans l’une des cinq listes de mots clés est trouvé.</span><span class="sxs-lookup"><span data-stu-id="319ad-2227">A keyword from any of the five keyword lists is found.</span></span>
- <span data-ttu-id="319ad-2228">La somme de contrôle est correcte.</span><span class="sxs-lookup"><span data-stu-id="319ad-2228">The checksum passes.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="319ad-2229">Mots-clés</span><span class="sxs-lookup"><span data-stu-id="319ad-2229">Keywords</span></span>

#### <a name="keyword_german_passport"></a><span data-ttu-id="319ad-2230">Keyword_german_passport</span><span class="sxs-lookup"><span data-stu-id="319ad-2230">Keyword_german_passport</span></span>

- <span data-ttu-id="319ad-2231">reisepass</span><span class="sxs-lookup"><span data-stu-id="319ad-2231">reisepass</span></span>
- <span data-ttu-id="319ad-2232">reisepasse</span><span class="sxs-lookup"><span data-stu-id="319ad-2232">reisepasse</span></span>
- <span data-ttu-id="319ad-2233">reisepassnummer</span><span class="sxs-lookup"><span data-stu-id="319ad-2233">reisepassnummer</span></span>
- <span data-ttu-id="319ad-2234">tel</span><span class="sxs-lookup"><span data-stu-id="319ad-2234">passport</span></span>
- <span data-ttu-id="319ad-2235">passeports</span><span class="sxs-lookup"><span data-stu-id="319ad-2235">passports</span></span>

#### <a name="keyword_german_passport_collaborative"></a><span data-ttu-id="319ad-2236">Keyword_german_passport_collaborative</span><span class="sxs-lookup"><span data-stu-id="319ad-2236">Keyword_german_passport_collaborative</span></span>

- <span data-ttu-id="319ad-2237">geburtsdatum</span><span class="sxs-lookup"><span data-stu-id="319ad-2237">geburtsdatum</span></span>
- <span data-ttu-id="319ad-2238">ausstellungsdatum</span><span class="sxs-lookup"><span data-stu-id="319ad-2238">ausstellungsdatum</span></span>
- <span data-ttu-id="319ad-2239">ausstellungsort</span><span class="sxs-lookup"><span data-stu-id="319ad-2239">ausstellungsort</span></span>

#### <a name="keyword_german_passport_number"></a><span data-ttu-id="319ad-2240">Keyword_german_passport_number</span><span class="sxs-lookup"><span data-stu-id="319ad-2240">Keyword_german_passport_number</span></span>

<span data-ttu-id="319ad-2241">No-Reisepass Nr-Reisepass</span><span class="sxs-lookup"><span data-stu-id="319ad-2241">No-Reisepass Nr-Reisepass</span></span>

#### <a name="keyword_german_passport1"></a><span data-ttu-id="319ad-2242">Keyword_german_passport1</span><span class="sxs-lookup"><span data-stu-id="319ad-2242">Keyword_german_passport1</span></span>

<span data-ttu-id="319ad-2243">Reisepass-Nr</span><span class="sxs-lookup"><span data-stu-id="319ad-2243">Reisepass-Nr</span></span>

#### <a name="keyword_german_passport2"></a><span data-ttu-id="319ad-2244">Keyword_german_passport2</span><span class="sxs-lookup"><span data-stu-id="319ad-2244">Keyword_german_passport2</span></span>

<span data-ttu-id="319ad-2245">bnationalit. t</span><span class="sxs-lookup"><span data-stu-id="319ad-2245">bnationalit.t</span></span>
   
## <a name="germany-identity-card-number"></a><span data-ttu-id="319ad-2246">Numéro de carte d’identité allemand</span><span class="sxs-lookup"><span data-stu-id="319ad-2246">Germany Identity Card Number</span></span>

### <a name="format"></a><span data-ttu-id="319ad-2247">Format</span><span class="sxs-lookup"><span data-stu-id="319ad-2247">Format</span></span>

<span data-ttu-id="319ad-2248">Depuis le 1er novembre 2010 : neuf lettres et chiffres</span><span class="sxs-lookup"><span data-stu-id="319ad-2248">Since 1 November 2010: Nine letters and digits</span></span>

<span data-ttu-id="319ad-2249">Du 1er avril 1987 au 31 octobre 2010:10 chiffres</span><span class="sxs-lookup"><span data-stu-id="319ad-2249">From 1 April 1987 until 31 October 2010: 10 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="319ad-2250">Modèle</span><span class="sxs-lookup"><span data-stu-id="319ad-2250">Pattern</span></span>

<span data-ttu-id="319ad-2251">Depuis le 1er novembre 2010 :</span><span class="sxs-lookup"><span data-stu-id="319ad-2251">Since 1 November 2010:</span></span>
- <span data-ttu-id="319ad-2252">Une lettre (ne respectant pas la casse) </span><span class="sxs-lookup"><span data-stu-id="319ad-2252">One letter (not case sensitive)</span></span> 
- <span data-ttu-id="319ad-2253">Huit chiffres</span><span class="sxs-lookup"><span data-stu-id="319ad-2253">Eight digits</span></span>

<span data-ttu-id="319ad-2254">Du 1er avril 1987 au 31 octobre 2010 :</span><span class="sxs-lookup"><span data-stu-id="319ad-2254">From 1 April 1987 until 31 October 2010:</span></span>
- <span data-ttu-id="319ad-2255">10 chiffres</span><span class="sxs-lookup"><span data-stu-id="319ad-2255">10 digits</span></span>

### <a name="checksum"></a><span data-ttu-id="319ad-2256">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="319ad-2256">Checksum</span></span>

<span data-ttu-id="319ad-2257">Non</span><span class="sxs-lookup"><span data-stu-id="319ad-2257">No</span></span>

### <a name="definition"></a><span data-ttu-id="319ad-2258">Définition</span><span class="sxs-lookup"><span data-stu-id="319ad-2258">Definition</span></span>

<span data-ttu-id="319ad-2259">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 65 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="319ad-2259">A DLP policy is 65% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="319ad-2260">L’expression régulière Regex_germany_id_card trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="319ad-2260">The regular expression Regex_germany_id_card finds content that matches the pattern.</span></span>
- <span data-ttu-id="319ad-2261">Un mot clé figurant dans la liste Keyword_germany_id_card est trouvé.</span><span class="sxs-lookup"><span data-stu-id="319ad-2261">A keyword from Keyword_germany_id_card is found.</span></span>

```xml
<!-- Germany Identity Card Number -->
<Entity id="e577372f-c42e-47a0-9d85-bebed1c237d4" recommendedConfidence="65" patternsProximity="300">
  <Pattern confidenceLevel="65">
     <IdMatch idRef="Regex_germany_id_card"/>
     <Match idRef="Keyword_germany_id_card"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="319ad-2262">Mots-clés</span><span class="sxs-lookup"><span data-stu-id="319ad-2262">Keywords</span></span>

#### <a name="keyword_germany_id_card"></a><span data-ttu-id="319ad-2263">Keyword_germany_id_card</span><span class="sxs-lookup"><span data-stu-id="319ad-2263">Keyword_germany_id_card</span></span>

- <span data-ttu-id="319ad-2264">Identity Card</span><span class="sxs-lookup"><span data-stu-id="319ad-2264">Identity Card</span></span>
- <span data-ttu-id="319ad-2265">ID</span><span class="sxs-lookup"><span data-stu-id="319ad-2265">ID</span></span>
- <span data-ttu-id="319ad-2266">Identificateur</span><span class="sxs-lookup"><span data-stu-id="319ad-2266">Identification</span></span>
- <span data-ttu-id="319ad-2267">Personalausweis</span><span class="sxs-lookup"><span data-stu-id="319ad-2267">Personalausweis</span></span>
- <span data-ttu-id="319ad-2268">Identifizierungsnummer</span><span class="sxs-lookup"><span data-stu-id="319ad-2268">Identifizierungsnummer</span></span>
- <span data-ttu-id="319ad-2269">Ausweis</span><span class="sxs-lookup"><span data-stu-id="319ad-2269">Ausweis</span></span>
- <span data-ttu-id="319ad-2270">Identifikation</span><span class="sxs-lookup"><span data-stu-id="319ad-2270">Identifikation</span></span>
   
## <a name="greece-national-id-card"></a><span data-ttu-id="319ad-2271">Carte d’identité nationale Grèce</span><span class="sxs-lookup"><span data-stu-id="319ad-2271">Greece National ID Card</span></span>

### <a name="format"></a><span data-ttu-id="319ad-2272">Format</span><span class="sxs-lookup"><span data-stu-id="319ad-2272">Format</span></span>

<span data-ttu-id="319ad-2273">Combinaison de 7 ou 8 lettres et chiffres, plus un tiret</span><span class="sxs-lookup"><span data-stu-id="319ad-2273">Combination of 7-8 letters and numbers plus a dash</span></span>

### <a name="pattern"></a><span data-ttu-id="319ad-2274">Modèle</span><span class="sxs-lookup"><span data-stu-id="319ad-2274">Pattern</span></span>

<span data-ttu-id="319ad-2275">Sept lettres et chiffres (ancien format) :</span><span class="sxs-lookup"><span data-stu-id="319ad-2275">Seven letters and numbers (old format):</span></span>
- <span data-ttu-id="319ad-2276">Une lettre (de l’alphabet grec) </span><span class="sxs-lookup"><span data-stu-id="319ad-2276">One letter (any letter of the Greek alphabet)</span></span> 
- <span data-ttu-id="319ad-2277">Un tiret</span><span class="sxs-lookup"><span data-stu-id="319ad-2277">A dash</span></span> 
- <span data-ttu-id="319ad-2278">Six chiffres</span><span class="sxs-lookup"><span data-stu-id="319ad-2278">Six digits</span></span>

<span data-ttu-id="319ad-2279">Huit lettres et chiffres (nouveau format) :</span><span class="sxs-lookup"><span data-stu-id="319ad-2279">Eight letters and numbers (new format):</span></span>
- <span data-ttu-id="319ad-2280">Deux lettres dont le caractère majuscule figure à la fois dans l’alphabet grec et l’alphabet latin (ABEZHIKMNOPTYX) </span><span class="sxs-lookup"><span data-stu-id="319ad-2280">Two letters whose uppercase character occurs in both the Greek and Latin alphabets (ABEZHIKMNOPTYX)</span></span> 
- <span data-ttu-id="319ad-2281">Un tiret</span><span class="sxs-lookup"><span data-stu-id="319ad-2281">A dash</span></span> 
- <span data-ttu-id="319ad-2282">Six chiffres</span><span class="sxs-lookup"><span data-stu-id="319ad-2282">Six digits</span></span>

### <a name="checksum"></a><span data-ttu-id="319ad-2283">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="319ad-2283">Checksum</span></span>

<span data-ttu-id="319ad-2284">Non</span><span class="sxs-lookup"><span data-stu-id="319ad-2284">No</span></span>

### <a name="definition"></a><span data-ttu-id="319ad-2285">Définition</span><span class="sxs-lookup"><span data-stu-id="319ad-2285">Definition</span></span>

<span data-ttu-id="319ad-2286">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="319ad-2286">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="319ad-2287">L’expression régulière Regex_greece_id_card trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="319ad-2287">The regular expression Regex_greece_id_card finds content that matches the pattern.</span></span>
- <span data-ttu-id="319ad-2288">Un mot clé figurant dans la liste Keyword_greece_id_card est trouvé.</span><span class="sxs-lookup"><span data-stu-id="319ad-2288">A keyword from Keyword_greece_id_card is found.</span></span>

```xml
<!-- Greece National ID Card -->
<Entity id="82568215-1da1-46d3-874a-d2294d81b5ac" recommendedConfidence="85" patternsProximity="300">
  <Pattern confidenceLevel="85">
     <IdMatch idRef="Regex_greece_id_card"/>
     <Match idRef="Keyword_greece_id_card"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="319ad-2289">Mots-clés</span><span class="sxs-lookup"><span data-stu-id="319ad-2289">Keywords</span></span>

#### <a name="keyword_greece_id_card"></a><span data-ttu-id="319ad-2290">Keyword_greece_id_card</span><span class="sxs-lookup"><span data-stu-id="319ad-2290">Keyword_greece_id_card</span></span>

- <span data-ttu-id="319ad-2291">Greek identity Card</span><span class="sxs-lookup"><span data-stu-id="319ad-2291">Greek identity Card</span></span>
- <span data-ttu-id="319ad-2292">Tautotita</span><span class="sxs-lookup"><span data-stu-id="319ad-2292">Tautotita</span></span>
- <span data-ttu-id="319ad-2293">Δελτίο αστυνομικής ταυτότητας</span><span class="sxs-lookup"><span data-stu-id="319ad-2293">Δελτίο αστυνομικής ταυτότητας</span></span>
- <span data-ttu-id="319ad-2294">Ταυτότητα</span><span class="sxs-lookup"><span data-stu-id="319ad-2294">Ταυτότητα</span></span>
   
## <a name="hong-kong-identity-card-hkid-number"></a><span data-ttu-id="319ad-2295">Numéro de carte d’identité (HKID) Hong Kong</span><span class="sxs-lookup"><span data-stu-id="319ad-2295">Hong Kong Identity Card (HKID) Number</span></span>

### <a name="format"></a><span data-ttu-id="319ad-2296">Format</span><span class="sxs-lookup"><span data-stu-id="319ad-2296">Format</span></span>

<span data-ttu-id="319ad-2297">Combinaison de 8 ou 9 lettres et chiffres plus éventuellement des parenthèses autour du dernier caractère</span><span class="sxs-lookup"><span data-stu-id="319ad-2297">Combination of 8-9 letters and numbers plus optional parentheses around the final character</span></span>

### <a name="pattern"></a><span data-ttu-id="319ad-2298">Modèle</span><span class="sxs-lookup"><span data-stu-id="319ad-2298">Pattern</span></span>

<span data-ttu-id="319ad-2299">Combinaison de 8 ou 9 lettres :</span><span class="sxs-lookup"><span data-stu-id="319ad-2299">Combination of 8-9 letters:</span></span>
- <span data-ttu-id="319ad-2300">1 ou 2 lettres (ne respectant pas la casse) </span><span class="sxs-lookup"><span data-stu-id="319ad-2300">1-2 letters (not case sensitive)</span></span> 
- <span data-ttu-id="319ad-2301">Six chiffres</span><span class="sxs-lookup"><span data-stu-id="319ad-2301">Six digits</span></span> 
- <span data-ttu-id="319ad-2302">Le dernier caractère (un chiffre ou la lettre A), qui est le chiffre de contrôle et est éventuellement entre parenthèses.</span><span class="sxs-lookup"><span data-stu-id="319ad-2302">The final character (any digit or the letter A), which is the check digit and is optionally enclosed in parentheses.</span></span>

### <a name="checksum"></a><span data-ttu-id="319ad-2303">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="319ad-2303">Checksum</span></span>

<span data-ttu-id="319ad-2304">Oui</span><span class="sxs-lookup"><span data-stu-id="319ad-2304">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="319ad-2305">Définition</span><span class="sxs-lookup"><span data-stu-id="319ad-2305">Definition</span></span>

<span data-ttu-id="319ad-2306">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="319ad-2306">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="319ad-2307">La fonction Func_hong_kong_id_card trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="319ad-2307">The function Func_hong_kong_id_card finds content that matches the pattern.</span></span>
- <span data-ttu-id="319ad-2308">Un mot clé figurant dans la liste Keyword_hong_kong_id_card est trouvé.</span><span class="sxs-lookup"><span data-stu-id="319ad-2308">A keyword from Keyword_hong_kong_id_card is found.</span></span>
- <span data-ttu-id="319ad-2309">La somme de contrôle est correcte.</span><span class="sxs-lookup"><span data-stu-id="319ad-2309">The checksum passes.</span></span>

<span data-ttu-id="319ad-2310">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 65 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="319ad-2310">A DLP policy is 65% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="319ad-2311">La fonction Func_hong_kong_id_card trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="319ad-2311">The function Func_hong_kong_id_card finds content that matches the pattern.</span></span>
- <span data-ttu-id="319ad-2312">La somme de contrôle est correcte.</span><span class="sxs-lookup"><span data-stu-id="319ad-2312">The checksum passes.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="319ad-2313">Mots-clés</span><span class="sxs-lookup"><span data-stu-id="319ad-2313">Keywords</span></span>

#### <a name="keyword_hong_kong_id_card"></a><span data-ttu-id="319ad-2314">Keyword_hong_kong_id_card</span><span class="sxs-lookup"><span data-stu-id="319ad-2314">Keyword_hong_kong_id_card</span></span>

- <span data-ttu-id="319ad-2315">carte d’identité de Hong Kong</span><span class="sxs-lookup"><span data-stu-id="319ad-2315">hong kong identity card</span></span>
- <span data-ttu-id="319ad-2316">HKIDC</span><span class="sxs-lookup"><span data-stu-id="319ad-2316">HKIDC</span></span>
- <span data-ttu-id="319ad-2317">carte d’identité</span><span class="sxs-lookup"><span data-stu-id="319ad-2317">id card</span></span>
- <span data-ttu-id="319ad-2318">Carte d’identité</span><span class="sxs-lookup"><span data-stu-id="319ad-2318">identity card</span></span>
- <span data-ttu-id="319ad-2319">carte d’identité HK</span><span class="sxs-lookup"><span data-stu-id="319ad-2319">hk identity card</span></span>
- <span data-ttu-id="319ad-2320">ID Hong Kong</span><span class="sxs-lookup"><span data-stu-id="319ad-2320">hong kong id</span></span>
- <span data-ttu-id="319ad-2321">香港身份證</span><span class="sxs-lookup"><span data-stu-id="319ad-2321">香港身份證</span></span>
- <span data-ttu-id="319ad-2322">香港永久性居民身份證</span><span class="sxs-lookup"><span data-stu-id="319ad-2322">香港永久性居民身份證</span></span>
- <span data-ttu-id="319ad-2323">身份證</span><span class="sxs-lookup"><span data-stu-id="319ad-2323">身份證</span></span>
- <span data-ttu-id="319ad-2324">身份証</span><span class="sxs-lookup"><span data-stu-id="319ad-2324">身份証</span></span>
- <span data-ttu-id="319ad-2325">身分證</span><span class="sxs-lookup"><span data-stu-id="319ad-2325">身分證</span></span>
- <span data-ttu-id="319ad-2326">身分証</span><span class="sxs-lookup"><span data-stu-id="319ad-2326">身分証</span></span>
- <span data-ttu-id="319ad-2327">香港身份証</span><span class="sxs-lookup"><span data-stu-id="319ad-2327">香港身份証</span></span>
- <span data-ttu-id="319ad-2328">香港身分證</span><span class="sxs-lookup"><span data-stu-id="319ad-2328">香港身分證</span></span>
- <span data-ttu-id="319ad-2329">香港身分証</span><span class="sxs-lookup"><span data-stu-id="319ad-2329">香港身分証</span></span>
- <span data-ttu-id="319ad-2330">香港身份證</span><span class="sxs-lookup"><span data-stu-id="319ad-2330">香港身份證</span></span>
- <span data-ttu-id="319ad-2331">香港居民身份證</span><span class="sxs-lookup"><span data-stu-id="319ad-2331">香港居民身份證</span></span>
- <span data-ttu-id="319ad-2332">香港居民身份証</span><span class="sxs-lookup"><span data-stu-id="319ad-2332">香港居民身份証</span></span>
- <span data-ttu-id="319ad-2333">香港居民身分證</span><span class="sxs-lookup"><span data-stu-id="319ad-2333">香港居民身分證</span></span>
- <span data-ttu-id="319ad-2334">香港居民身分証</span><span class="sxs-lookup"><span data-stu-id="319ad-2334">香港居民身分証</span></span>
- <span data-ttu-id="319ad-2335">香港永久性居民身份証</span><span class="sxs-lookup"><span data-stu-id="319ad-2335">香港永久性居民身份証</span></span>
- <span data-ttu-id="319ad-2336">香港永久性居民身分證</span><span class="sxs-lookup"><span data-stu-id="319ad-2336">香港永久性居民身分證</span></span>
- <span data-ttu-id="319ad-2337">香港永久性居民身分証</span><span class="sxs-lookup"><span data-stu-id="319ad-2337">香港永久性居民身分証</span></span>
- <span data-ttu-id="319ad-2338">香港永久性居民身份證</span><span class="sxs-lookup"><span data-stu-id="319ad-2338">香港永久性居民身份證</span></span>
- <span data-ttu-id="319ad-2339">香港非永久性居民身份證</span><span class="sxs-lookup"><span data-stu-id="319ad-2339">香港非永久性居民身份證</span></span>
- <span data-ttu-id="319ad-2340">香港非永久性居民身份証</span><span class="sxs-lookup"><span data-stu-id="319ad-2340">香港非永久性居民身份証</span></span>
- <span data-ttu-id="319ad-2341">香港非永久性居民身分證</span><span class="sxs-lookup"><span data-stu-id="319ad-2341">香港非永久性居民身分證</span></span>
- <span data-ttu-id="319ad-2342">香港非永久性居民身分証</span><span class="sxs-lookup"><span data-stu-id="319ad-2342">香港非永久性居民身分証</span></span>
- <span data-ttu-id="319ad-2343">香港特別行政區永久性居民身份證</span><span class="sxs-lookup"><span data-stu-id="319ad-2343">香港特別行政區永久性居民身份證</span></span>
- <span data-ttu-id="319ad-2344">香港特別行政區永久性居民身份証</span><span class="sxs-lookup"><span data-stu-id="319ad-2344">香港特別行政區永久性居民身份証</span></span>
- <span data-ttu-id="319ad-2345">香港特別行政區永久性居民身分證</span><span class="sxs-lookup"><span data-stu-id="319ad-2345">香港特別行政區永久性居民身分證</span></span>
- <span data-ttu-id="319ad-2346">香港特別行政區永久性居民身分証</span><span class="sxs-lookup"><span data-stu-id="319ad-2346">香港特別行政區永久性居民身分証</span></span>
- <span data-ttu-id="319ad-2347">香港特別行政區非永久性居民身份證</span><span class="sxs-lookup"><span data-stu-id="319ad-2347">香港特別行政區非永久性居民身份證</span></span>
- <span data-ttu-id="319ad-2348">香港特別行政區非永久性居民身份証</span><span class="sxs-lookup"><span data-stu-id="319ad-2348">香港特別行政區非永久性居民身份証</span></span>
- <span data-ttu-id="319ad-2349">香港特別行政區非永久性居民身分證</span><span class="sxs-lookup"><span data-stu-id="319ad-2349">香港特別行政區非永久性居民身分證</span></span>
- <span data-ttu-id="319ad-2350">香港特別行政區非永久性居民身分証</span><span class="sxs-lookup"><span data-stu-id="319ad-2350">香港特別行政區非永久性居民身分証</span></span>
   
## <a name="india-permanent-account-number-pan"></a><span data-ttu-id="319ad-2351">Numéro de compte permanent Inde</span><span class="sxs-lookup"><span data-stu-id="319ad-2351">India Permanent Account Number (PAN)</span></span>

### <a name="format"></a><span data-ttu-id="319ad-2352">Format</span><span class="sxs-lookup"><span data-stu-id="319ad-2352">Format</span></span>

<span data-ttu-id="319ad-2353">10 lettres ou chiffres</span><span class="sxs-lookup"><span data-stu-id="319ad-2353">10 letters or digits</span></span>

### <a name="pattern"></a><span data-ttu-id="319ad-2354">Modèle</span><span class="sxs-lookup"><span data-stu-id="319ad-2354">Pattern</span></span>

<span data-ttu-id="319ad-2355">10 lettres ou chiffres :</span><span class="sxs-lookup"><span data-stu-id="319ad-2355">10 letters or digits:</span></span>
- <span data-ttu-id="319ad-2356">Cinq lettres (ne respectant pas la casse) </span><span class="sxs-lookup"><span data-stu-id="319ad-2356">Five letters (not case sensitive)</span></span> 
- <span data-ttu-id="319ad-2357">Quatre chiffres</span><span class="sxs-lookup"><span data-stu-id="319ad-2357">Four digits</span></span> 
- <span data-ttu-id="319ad-2358">Une lettre qui est un chiffre de contrôle alphabétique</span><span class="sxs-lookup"><span data-stu-id="319ad-2358">A letter which is an alphabetic check digit</span></span>

### <a name="checksum"></a><span data-ttu-id="319ad-2359">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="319ad-2359">Checksum</span></span>

<span data-ttu-id="319ad-2360">Oui</span><span class="sxs-lookup"><span data-stu-id="319ad-2360">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="319ad-2361">Définition</span><span class="sxs-lookup"><span data-stu-id="319ad-2361">Definition</span></span>

<span data-ttu-id="319ad-2362">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="319ad-2362">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="319ad-2363">L’expression régulière Regex_india_permanent_account_number trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="319ad-2363">The regular expression Regex_india_permanent_account_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="319ad-2364">Un mot clé figurant dans la liste Keyword_india_permanent_account_number est trouvé.</span><span class="sxs-lookup"><span data-stu-id="319ad-2364">A keyword from Keyword_india_permanent_account_number is found.</span></span>
- <span data-ttu-id="319ad-2365">La somme de contrôle est correcte.</span><span class="sxs-lookup"><span data-stu-id="319ad-2365">The checksum passes.</span></span>

```xml
<!-- India Permanent Account Number -->
<Entity id="2602bfee-9bb0-47a5-a7a6-2bf3053e2804" recommendedConfidence="85" patternsProximity="300">
  <Pattern confidenceLevel="85">
     <IdMatch idRef="Regex_india_permanent_account_number"/>
     <Match idRef="Keyword_india_permanent_account_number"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="319ad-2366">Mots-clés</span><span class="sxs-lookup"><span data-stu-id="319ad-2366">Keywords</span></span>

#### <a name="keyword_india_permanent_account_number"></a><span data-ttu-id="319ad-2367">Keyword_india_permanent_account_number</span><span class="sxs-lookup"><span data-stu-id="319ad-2367">Keyword_india_permanent_account_number</span></span>

- <span data-ttu-id="319ad-2368">Permanent Account Number</span><span class="sxs-lookup"><span data-stu-id="319ad-2368">Permanent Account Number</span></span> 
- <span data-ttu-id="319ad-2369">PANEUROPÉENNES</span><span class="sxs-lookup"><span data-stu-id="319ad-2369">PAN</span></span> 
   
## <a name="india-unique-identification-aadhaar-number"></a><span data-ttu-id="319ad-2370">Numéro d’identification unique (Aadhaar) Inde</span><span class="sxs-lookup"><span data-stu-id="319ad-2370">India Unique Identification (Aadhaar) Number</span></span>

### <a name="format"></a><span data-ttu-id="319ad-2371">Format</span><span class="sxs-lookup"><span data-stu-id="319ad-2371">Format</span></span>

<span data-ttu-id="319ad-2372">12 chiffres contenant éventuellement des espaces ou des tirets</span><span class="sxs-lookup"><span data-stu-id="319ad-2372">12 digits containing optional spaces or dashes</span></span>

### <a name="pattern"></a><span data-ttu-id="319ad-2373">Modèle</span><span class="sxs-lookup"><span data-stu-id="319ad-2373">Pattern</span></span>

<span data-ttu-id="319ad-2374">12 chiffres :</span><span class="sxs-lookup"><span data-stu-id="319ad-2374">12 digits:</span></span>
- <span data-ttu-id="319ad-2375">Quatre chiffres</span><span class="sxs-lookup"><span data-stu-id="319ad-2375">Four digits</span></span> 
- <span data-ttu-id="319ad-2376">Éventuellement un tiret ou un espace </span><span class="sxs-lookup"><span data-stu-id="319ad-2376">An optional space or dash</span></span> 
- <span data-ttu-id="319ad-2377">Quatre chiffres</span><span class="sxs-lookup"><span data-stu-id="319ad-2377">Four digits</span></span> 
- <span data-ttu-id="319ad-2378">Éventuellement un tiret ou un espace </span><span class="sxs-lookup"><span data-stu-id="319ad-2378">An optional space or dash</span></span> 
- <span data-ttu-id="319ad-2379">Le chiffre final, qui est le chiffre de contrôle</span><span class="sxs-lookup"><span data-stu-id="319ad-2379">The final digit which is the check digit</span></span>

### <a name="checksum"></a><span data-ttu-id="319ad-2380">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="319ad-2380">Checksum</span></span>

<span data-ttu-id="319ad-2381">Oui</span><span class="sxs-lookup"><span data-stu-id="319ad-2381">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="319ad-2382">Définition</span><span class="sxs-lookup"><span data-stu-id="319ad-2382">Definition</span></span>

<span data-ttu-id="319ad-2383">Une stratégie DLP est sûre à 85% d’avoir détecté ce type d’informations sensibles si, dans une proximité de 300 caractères : la fonction Func_india_aadhaar trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="319ad-2383">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters: The function Func_india_aadhaar finds content that matches the pattern.</span></span>
<span data-ttu-id="319ad-2384">Un mot clé figurant dans la liste Keyword_india_aadhar est trouvé.</span><span class="sxs-lookup"><span data-stu-id="319ad-2384">A keyword from Keyword_india_aadhar is found.</span></span>
<span data-ttu-id="319ad-2385">La somme de contrôle est correcte.</span><span class="sxs-lookup"><span data-stu-id="319ad-2385">The checksum passes.</span></span>
<span data-ttu-id="319ad-2386">Une stratégie DLP est sûre à 75% d’avoir détecté ce type d’informations sensibles si, dans une proximité de 300 caractères : la fonction Func_india_aadhaar trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="319ad-2386">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters: The function Func_india_aadhaar finds content that matches the pattern.</span></span>
<span data-ttu-id="319ad-2387">La somme de contrôle est correcte.</span><span class="sxs-lookup"><span data-stu-id="319ad-2387">The checksum passes.</span></span>
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
### <a name="keywords"></a><span data-ttu-id="319ad-2388">Mots-clés</span><span class="sxs-lookup"><span data-stu-id="319ad-2388">Keywords</span></span>
   
#### <a name="keyword_india_aadhar"></a><span data-ttu-id="319ad-2389">Keyword_india_aadhar</span><span class="sxs-lookup"><span data-stu-id="319ad-2389">Keyword_india_aadhar</span></span>
- <span data-ttu-id="319ad-2390">Aadhar</span><span class="sxs-lookup"><span data-stu-id="319ad-2390">Aadhar</span></span>
- <span data-ttu-id="319ad-2391">Aadhaar</span><span class="sxs-lookup"><span data-stu-id="319ad-2391">Aadhaar</span></span>
- <span data-ttu-id="319ad-2392">UID</span><span class="sxs-lookup"><span data-stu-id="319ad-2392">UID</span></span>
- <span data-ttu-id="319ad-2393">आधार</span><span class="sxs-lookup"><span data-stu-id="319ad-2393">आधार</span></span>
   
## <a name="indonesia-identity-card-ktp-number"></a><span data-ttu-id="319ad-2394">Numéro de carte d’identité (KTP) Indonésie</span><span class="sxs-lookup"><span data-stu-id="319ad-2394">Indonesia Identity Card (KTP) Number</span></span>

### <a name="format"></a><span data-ttu-id="319ad-2395">Format</span><span class="sxs-lookup"><span data-stu-id="319ad-2395">Format</span></span>

<span data-ttu-id="319ad-2396">16 chiffres contenant éventuellement des points</span><span class="sxs-lookup"><span data-stu-id="319ad-2396">16 digits containing optional periods</span></span>

### <a name="pattern"></a><span data-ttu-id="319ad-2397">Modèle</span><span class="sxs-lookup"><span data-stu-id="319ad-2397">Pattern</span></span>

<span data-ttu-id="319ad-2398">16 chiffres :</span><span class="sxs-lookup"><span data-stu-id="319ad-2398">16 digits:</span></span>
- <span data-ttu-id="319ad-2399">Code à deux chiffres désignant la province </span><span class="sxs-lookup"><span data-stu-id="319ad-2399">Two-digit province code</span></span> 
- <span data-ttu-id="319ad-2400">Un point (facultatif) </span><span class="sxs-lookup"><span data-stu-id="319ad-2400">A period (optional)</span></span> 
- <span data-ttu-id="319ad-2401">Code à deux chiffres désignant une régence ou une ville </span><span class="sxs-lookup"><span data-stu-id="319ad-2401">Two-digit regency or city code</span></span> 
- <span data-ttu-id="319ad-2402">Code à deux chiffres désignant un sous-district </span><span class="sxs-lookup"><span data-stu-id="319ad-2402">Two-digit subdistrict code</span></span> 
- <span data-ttu-id="319ad-2403">Un point (facultatif) </span><span class="sxs-lookup"><span data-stu-id="319ad-2403">A period (optional)</span></span> 
- <span data-ttu-id="319ad-2404">Six chiffres au format JJMMAA qui correspondent à la date de naissance </span><span class="sxs-lookup"><span data-stu-id="319ad-2404">Six digits in the format DDMMYY which are the date of birth</span></span> 
- <span data-ttu-id="319ad-2405">Un point (facultatif) </span><span class="sxs-lookup"><span data-stu-id="319ad-2405">A period (optional)</span></span> 
- <span data-ttu-id="319ad-2406">Quatre chiffres</span><span class="sxs-lookup"><span data-stu-id="319ad-2406">Four digits</span></span>

### <a name="checksum"></a><span data-ttu-id="319ad-2407">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="319ad-2407">Checksum</span></span>

<span data-ttu-id="319ad-2408">Non</span><span class="sxs-lookup"><span data-stu-id="319ad-2408">No</span></span>

### <a name="definition"></a><span data-ttu-id="319ad-2409">Définition</span><span class="sxs-lookup"><span data-stu-id="319ad-2409">Definition</span></span>

<span data-ttu-id="319ad-2410">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="319ad-2410">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="319ad-2411">L’expression régulière Regex_indonesia_id_card trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="319ad-2411">The regular expression Regex_indonesia_id_card finds content that matches the pattern.</span></span>
- <span data-ttu-id="319ad-2412">Un mot clé figurant dans la liste Keyword_indonesia_id_card est trouvé.</span><span class="sxs-lookup"><span data-stu-id="319ad-2412">A keyword from Keyword_indonesia_id_card is found.</span></span>

<span data-ttu-id="319ad-2413">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="319ad-2413">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="319ad-2414">L’expression régulière Regex_indonesia_id_card trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="319ad-2414">The regular expression Regex_indonesia_id_card finds content that matches the pattern.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="319ad-2415">Mots-clés</span><span class="sxs-lookup"><span data-stu-id="319ad-2415">Keywords</span></span>
   
#### <a name="keyword_indonesia_id_card"></a><span data-ttu-id="319ad-2416">Keyword_indonesia_id_card</span><span class="sxs-lookup"><span data-stu-id="319ad-2416">Keyword_indonesia_id_card</span></span>

- <span data-ttu-id="319ad-2417">KTP</span><span class="sxs-lookup"><span data-stu-id="319ad-2417">KTP</span></span>
- <span data-ttu-id="319ad-2418">Kartu Tanda Penduduk</span><span class="sxs-lookup"><span data-stu-id="319ad-2418">Kartu Tanda Penduduk</span></span> 
- <span data-ttu-id="319ad-2419">Nomor Induk Kependudukan</span><span class="sxs-lookup"><span data-stu-id="319ad-2419">Nomor Induk Kependudukan</span></span> 
   
## <a name="international-banking-account-number-iban"></a><span data-ttu-id="319ad-2420">Numéro de compte bancaire international (IBAN)</span><span class="sxs-lookup"><span data-stu-id="319ad-2420">International Banking Account Number (IBAN)</span></span>

### <a name="format"></a><span data-ttu-id="319ad-2421">Format</span><span class="sxs-lookup"><span data-stu-id="319ad-2421">Format</span></span>

<span data-ttu-id="319ad-2422">Code pays (à deux lettres) plus chiffres de contrôle (à deux chiffres) plus numéro BBAN (jusqu’à 30 chiffres)</span><span class="sxs-lookup"><span data-stu-id="319ad-2422">Country code (two letters) plus check digits (two digits) plus bban number (up to 30 characters)</span></span>

### <a name="pattern"></a><span data-ttu-id="319ad-2423">Modèle</span><span class="sxs-lookup"><span data-stu-id="319ad-2423">Pattern</span></span>

<span data-ttu-id="319ad-2424">Le modèle doit inclure tous les éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="319ad-2424">Pattern must include all of the following:</span></span>

- <span data-ttu-id="319ad-2425">Code pays à deux lettres</span><span class="sxs-lookup"><span data-stu-id="319ad-2425">Two-letter country code</span></span>
- <span data-ttu-id="319ad-2426">Deux chiffres de contrôle (suivis d’un espace facultatif) </span><span class="sxs-lookup"><span data-stu-id="319ad-2426">Two check digits (followed by an optional space)</span></span> 
- <span data-ttu-id="319ad-2427">1 à 7 groupes de quatre lettres ou chiffres (séparés par des espaces facultatifs)</span><span class="sxs-lookup"><span data-stu-id="319ad-2427">1-7 groups of four letters or digits (can be separated by spaces)</span></span>
- <span data-ttu-id="319ad-2428">1 à 3 lettres ou chiffres</span><span class="sxs-lookup"><span data-stu-id="319ad-2428">1-3 letters or digits</span></span>

<span data-ttu-id="319ad-p135">Le format pour chaque pays est légèrement différent. Le type d’informations sensibles IBAN recouvre ces 60 pays :</span><span class="sxs-lookup"><span data-stu-id="319ad-p135">The format for each country is slightly different. The IBAN sensitive information type covers these 60 countries:</span></span>

<span data-ttu-id="319ad-2431">ad, ae, al, at, az, ba, be, bg, bh, ch, cr, cy, cz, de, dk, do, ee, es, fi, fo, fr, gb, ge, gi, gl, gr, hr, hu, ie, il, is, it, kw, kz, lb, li, lt, lu, lv, mc, md, me, mk, mr, mt, mu, nl, no, pl, pt, ro, rs, sa, se, si, sk, sm, tn, tr, vg</span><span class="sxs-lookup"><span data-stu-id="319ad-2431">ad, ae, al, at, az, ba, be, bg, bh, ch, cr, cy, cz, de, dk, do, ee, es, fi, fo, fr, gb, ge, gi, gl, gr, hr, hu, ie, il, is, it, kw, kz, lb, li, lt, lu, lv, mc, md, me, mk, mr, mt, mu, nl, no, pl, pt, ro, rs, sa, se, si, sk, sm, tn, tr, vg</span></span>

### <a name="checksum"></a><span data-ttu-id="319ad-2432">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="319ad-2432">Checksum</span></span>

<span data-ttu-id="319ad-2433">Oui</span><span class="sxs-lookup"><span data-stu-id="319ad-2433">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="319ad-2434">Définition</span><span class="sxs-lookup"><span data-stu-id="319ad-2434">Definition</span></span>

<span data-ttu-id="319ad-2435">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="319ad-2435">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="319ad-2436">La fonction Func_iban trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="319ad-2436">The function Func_iban finds content that matches the pattern.</span></span>
- <span data-ttu-id="319ad-2437">La somme de contrôle est correcte.</span><span class="sxs-lookup"><span data-stu-id="319ad-2437">The checksum passes.</span></span>

```xml
<Entity id="e7dc4711-11b7-4cb0-b88b-2c394a771f0e" patternsProximity="300" recommendedConfidence="85">
  <Pattern confidenceLevel="85">
        <IdMatch idRef="Func_iban" />
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="319ad-2438">Mots-clés</span><span class="sxs-lookup"><span data-stu-id="319ad-2438">Keywords</span></span>

<span data-ttu-id="319ad-2439">Aucun</span><span class="sxs-lookup"><span data-stu-id="319ad-2439">None</span></span>

   
## <a name="ip-address"></a><span data-ttu-id="319ad-2440">Adresse IP</span><span class="sxs-lookup"><span data-stu-id="319ad-2440">IP Address</span></span>

### <a name="format"></a><span data-ttu-id="319ad-2441">Format</span><span class="sxs-lookup"><span data-stu-id="319ad-2441">Format</span></span>

#### <a name="ipv4"></a><span data-ttu-id="319ad-2442">IPv6</span><span class="sxs-lookup"><span data-stu-id="319ad-2442">IPv4:</span></span>
<span data-ttu-id="319ad-2443">Modèle complexe qui tient compte des versions mises en forme (points) et non mises en forme (sans points) des adresses IPv4</span><span class="sxs-lookup"><span data-stu-id="319ad-2443">Complex pattern which accounts for formatted (periods) and unformatted (no periods) versions of the IPv4 addresses</span></span>

#### <a name="ipv6"></a><span data-ttu-id="319ad-2444">IPv4/IPv6</span><span class="sxs-lookup"><span data-stu-id="319ad-2444">IPv6:</span></span>
<span data-ttu-id="319ad-2445"> Modèle complexe qui tient compte des numéros IPv6 mis en forme (qui incluent les signes deux-points)</span><span class="sxs-lookup"><span data-stu-id="319ad-2445">Complex pattern which accounts for formatted IPv6 numbers (which include colons)</span></span>

### <a name="pattern"></a><span data-ttu-id="319ad-2446">Modèle</span><span class="sxs-lookup"><span data-stu-id="319ad-2446">Pattern</span></span>

### <a name="checksum"></a><span data-ttu-id="319ad-2447">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="319ad-2447">Checksum</span></span>

<span data-ttu-id="319ad-2448">Non</span><span class="sxs-lookup"><span data-stu-id="319ad-2448">No</span></span>

### <a name="definition"></a><span data-ttu-id="319ad-2449">Définition</span><span class="sxs-lookup"><span data-stu-id="319ad-2449">Definition</span></span>

<span data-ttu-id="319ad-2450">Pour IPv6, le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="319ad-2450">For IPv6, a DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="319ad-2451">L’expression régulière Regex_ipv6_address trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="319ad-2451">The regular expression Regex_ipv6_address finds content that matches the pattern.</span></span>
- <span data-ttu-id="319ad-2452">Aucun mot clé figurant dans la liste Keyword_ipaddress n’est trouvé.</span><span class="sxs-lookup"><span data-stu-id="319ad-2452">No keyword from Keyword_ipaddress is found.</span></span>

<span data-ttu-id="319ad-2453">Pour IPv4, le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 95 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="319ad-2453">For IPv4, a DLP policy is 95% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="319ad-2454">L’expression régulière Regex_ipv4_address trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="319ad-2454">The regular expression Regex_ipv4_address finds content that matches the pattern.</span></span>
- <span data-ttu-id="319ad-2455">Un mot clé figurant dans la liste Keyword_ipaddress est trouvé.</span><span class="sxs-lookup"><span data-stu-id="319ad-2455">A keyword from Keyword_ipaddress is found.</span></span>

<span data-ttu-id="319ad-2456">Pour IPv6, le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 95 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="319ad-2456">For IPv6, a DLP policy is 95% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="319ad-2457">L’expression régulière Regex_ipv6_address trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="319ad-2457">The regular expression Regex_ipv6_address finds content that matches the pattern.</span></span>
- <span data-ttu-id="319ad-2458">Aucun mot clé figurant dans la liste Keyword_ipaddress n’est trouvé.</span><span class="sxs-lookup"><span data-stu-id="319ad-2458">No keyword from Keyword_ipaddress is found.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="319ad-2459">Mots-clés</span><span class="sxs-lookup"><span data-stu-id="319ad-2459">Keywords</span></span>

#### <a name="keyword_ipaddress"></a><span data-ttu-id="319ad-2460">Keyword_ipaddress</span><span class="sxs-lookup"><span data-stu-id="319ad-2460">Keyword_ipaddress</span></span>

- <span data-ttu-id="319ad-2461">IP (ce mot clé respecte la casse)</span><span class="sxs-lookup"><span data-stu-id="319ad-2461">IP (this keyword is case sensitive)</span></span>
- <span data-ttu-id="319ad-2462">ip address</span><span class="sxs-lookup"><span data-stu-id="319ad-2462">ip address</span></span> 
- <span data-ttu-id="319ad-2463">adresses IP</span><span class="sxs-lookup"><span data-stu-id="319ad-2463">ip addresses</span></span>
- <span data-ttu-id="319ad-2464">protocole internet</span><span class="sxs-lookup"><span data-stu-id="319ad-2464">internet protocol</span></span>
- <span data-ttu-id="319ad-2465">IP-כתובת ה</span><span class="sxs-lookup"><span data-stu-id="319ad-2465">IP-כתובת ה</span></span> 
   
## <a name="international-classification-of-diseases-icd-10-cm"></a><span data-ttu-id="319ad-2466">Classification internationale des maladies (ICD-10-CM)</span><span class="sxs-lookup"><span data-stu-id="319ad-2466">International Classification of Diseases (ICD-10-CM)</span></span>

### <a name="format"></a><span data-ttu-id="319ad-2467">Format</span><span class="sxs-lookup"><span data-stu-id="319ad-2467">Format</span></span>

<span data-ttu-id="319ad-2468">Dictionary</span><span class="sxs-lookup"><span data-stu-id="319ad-2468">Dictionary</span></span>

### <a name="pattern"></a><span data-ttu-id="319ad-2469">Modèle</span><span class="sxs-lookup"><span data-stu-id="319ad-2469">Pattern</span></span>

<span data-ttu-id="319ad-2470">Mot clé</span><span class="sxs-lookup"><span data-stu-id="319ad-2470">Keyword</span></span>

### <a name="checksum"></a><span data-ttu-id="319ad-2471">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="319ad-2471">Checksum</span></span>

<span data-ttu-id="319ad-2472">Non</span><span class="sxs-lookup"><span data-stu-id="319ad-2472">No</span></span>

### <a name="definition"></a><span data-ttu-id="319ad-2473">Définition</span><span class="sxs-lookup"><span data-stu-id="319ad-2473">Definition</span></span>

<span data-ttu-id="319ad-2474">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="319ad-2474">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="319ad-2475">Un mot clé depuis Dictionary_icd_10_updated est trouvé.</span><span class="sxs-lookup"><span data-stu-id="319ad-2475">A keyword from Dictionary_icd_10_updated is found.</span></span>
- <span data-ttu-id="319ad-2476">Un mot clé depuis Dictionary_icd_10_codes est trouvé.</span><span class="sxs-lookup"><span data-stu-id="319ad-2476">A keyword from Dictionary_icd_10_codes is found.</span></span>

<span data-ttu-id="319ad-2477">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="319ad-2477">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="319ad-2478">Un mot clé depuis Dictionary_icd_10_ mis à jour est trouvé.</span><span class="sxs-lookup"><span data-stu-id="319ad-2478">A keyword from Dictionary_icd_10_ updated is found.</span></span>

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

<span data-ttu-id="319ad-2479">Mots-clés</span><span class="sxs-lookup"><span data-stu-id="319ad-2479">Keywords</span></span>

<span data-ttu-id="319ad-2480">Tout terme du dictionnaire de mots clés Dictionary_icd_10_updated, qui est basé sur la [Classification internationale des maladies, dixième révision, modification clinique (ICD-10-cm)](https://go.microsoft.com/fwlink/?linkid=852604).</span><span class="sxs-lookup"><span data-stu-id="319ad-2480">Any term from the Dictionary_icd_10_updated keyword dictionary, which is based on the [International Classification of Diseases, Tenth Revision, Clinical Modification (ICD-10-CM)](https://go.microsoft.com/fwlink/?linkid=852604).</span></span> <span data-ttu-id="319ad-2481">Ce type recherche uniquement le terme, pas les codes d’assurance.</span><span class="sxs-lookup"><span data-stu-id="319ad-2481">This type looks only for the term, not the insurance codes.</span></span>

<span data-ttu-id="319ad-2482">Tout terme du dictionnaire de mots clés Dictionary_icd_10_codes, qui est basé sur la [Classification internationale des maladies, dixième révision, modification clinique (ICD-10-cm)](https://go.microsoft.com/fwlink/?linkid=852604).</span><span class="sxs-lookup"><span data-stu-id="319ad-2482">Any term from the Dictionary_icd_10_codes keyword dictionary, which is based on the [International Classification of Diseases, Tenth Revision, Clinical Modification (ICD-10-CM)](https://go.microsoft.com/fwlink/?linkid=852604).</span></span> <span data-ttu-id="319ad-2483">Ce type recherche uniquement les codes d’assurance, pas la description.</span><span class="sxs-lookup"><span data-stu-id="319ad-2483">This type looks only for insurance codes, not the description.</span></span>

## <a name="international-classification-of-diseases-icd-9-cm"></a><span data-ttu-id="319ad-2484">Classification internationale des maladies (ICD-9-CM)</span><span class="sxs-lookup"><span data-stu-id="319ad-2484">International Classification of Diseases (ICD-9-CM)</span></span>

### <a name="format"></a><span data-ttu-id="319ad-2485">Format</span><span class="sxs-lookup"><span data-stu-id="319ad-2485">Format</span></span>

<span data-ttu-id="319ad-2486">Dictionary</span><span class="sxs-lookup"><span data-stu-id="319ad-2486">Dictionary</span></span>

### <a name="pattern"></a><span data-ttu-id="319ad-2487">Modèle</span><span class="sxs-lookup"><span data-stu-id="319ad-2487">Pattern</span></span>

<span data-ttu-id="319ad-2488">Mot clé</span><span class="sxs-lookup"><span data-stu-id="319ad-2488">Keyword</span></span>

### <a name="checksum"></a><span data-ttu-id="319ad-2489">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="319ad-2489">Checksum</span></span>

<span data-ttu-id="319ad-2490">Non</span><span class="sxs-lookup"><span data-stu-id="319ad-2490">No</span></span>

### <a name="definition"></a><span data-ttu-id="319ad-2491">Définition</span><span class="sxs-lookup"><span data-stu-id="319ad-2491">Definition</span></span>

<span data-ttu-id="319ad-2492">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="319ad-2492">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="319ad-2493">Un mot clé depuis Dictionary_icd_9_updated est trouvé.</span><span class="sxs-lookup"><span data-stu-id="319ad-2493">A keyword from Dictionary_icd_9_updated is found.</span></span>
- <span data-ttu-id="319ad-2494">Un mot clé depuis Dictionary_icd_9_codes est trouvé.</span><span class="sxs-lookup"><span data-stu-id="319ad-2494">A keyword from Dictionary_icd_9_codes is found.</span></span>

<span data-ttu-id="319ad-2495">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="319ad-2495">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="319ad-2496">Un mot clé depuis Dictionary_icd_9_updated est trouvé.</span><span class="sxs-lookup"><span data-stu-id="319ad-2496">A keyword from Dictionary_icd_9_updated is found.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="319ad-2497">Mots-clés</span><span class="sxs-lookup"><span data-stu-id="319ad-2497">Keywords</span></span>

<span data-ttu-id="319ad-2498">Tout terme du dictionnaire de mots clés Dictionary_icd_9_updated, qui est basé sur la [Classification internationale des maladies, neuvième révision, modification clinique (ICD-9-cm)](https://go.microsoft.com/fwlink/?linkid=852605).</span><span class="sxs-lookup"><span data-stu-id="319ad-2498">Any term from the Dictionary_icd_9_updated keyword dictionary, which is based on the [International Classification of Diseases,Ninth Revision, Clinical Modification (ICD-9-CM)](https://go.microsoft.com/fwlink/?linkid=852605).</span></span> <span data-ttu-id="319ad-2499">Ce type recherche uniquement le terme, pas les codes d’assurance.</span><span class="sxs-lookup"><span data-stu-id="319ad-2499">This type looks only for the term, not the insurance codes.</span></span>

<span data-ttu-id="319ad-2500">Tout terme du dictionnaire de mots clés Dictionary_icd_9_codes, qui est basé sur la [Classification internationale des maladies, neuvième révision, modification clinique (ICD-9-cm)](https://go.microsoft.com/fwlink/?linkid=852605).</span><span class="sxs-lookup"><span data-stu-id="319ad-2500">Any term from the Dictionary_icd_9_codes keyword dictionary, which is based on the [International Classification of Diseases,Ninth Revision, Clinical Modification (ICD-9-CM)](https://go.microsoft.com/fwlink/?linkid=852605).</span></span> <span data-ttu-id="319ad-2501">Ce type recherche uniquement les codes d’assurance, pas la description.</span><span class="sxs-lookup"><span data-stu-id="319ad-2501">This type looks only for insurance codes, not the description.</span></span>

## <a name="ireland-personal-public-service-pps-number"></a><span data-ttu-id="319ad-2502">Numéro de service public personnel (PPS) Irlande</span><span class="sxs-lookup"><span data-stu-id="319ad-2502">Ireland Personal Public Service (PPS) Number</span></span>

### <a name="format"></a><span data-ttu-id="319ad-2503">Format</span><span class="sxs-lookup"><span data-stu-id="319ad-2503">Format</span></span>

<span data-ttu-id="319ad-2504">Ancien format (jusqu’au 31 décembre 2012) :</span><span class="sxs-lookup"><span data-stu-id="319ad-2504">Old format (until 31 Dec 2012):</span></span>
- <span data-ttu-id="319ad-2505">Sept chiffres suivis de 1 ou 2 lettres </span><span class="sxs-lookup"><span data-stu-id="319ad-2505">Seven digits followed by 1-2 letters</span></span> 

<span data-ttu-id="319ad-2506">Nouveau format (1er janvier 2013 et après) :</span><span class="sxs-lookup"><span data-stu-id="319ad-2506">New format (1 Jan 2013 and after):</span></span>
- <span data-ttu-id="319ad-2507">Sept chiffres suivis de deux lettres</span><span class="sxs-lookup"><span data-stu-id="319ad-2507">Seven digits followed by two letters</span></span>

### <a name="pattern"></a><span data-ttu-id="319ad-2508">Modèle</span><span class="sxs-lookup"><span data-stu-id="319ad-2508">Pattern</span></span>

<span data-ttu-id="319ad-2509">Ancien format (jusqu’au 31 décembre 2012) :</span><span class="sxs-lookup"><span data-stu-id="319ad-2509">Old format (until 31 Dec 2012):</span></span>
- <span data-ttu-id="319ad-2510">Sept chiffres </span><span class="sxs-lookup"><span data-stu-id="319ad-2510">Seven digits</span></span> 
- <span data-ttu-id="319ad-2511">1 ou 2 lettres (ne respectant pas la casse) </span><span class="sxs-lookup"><span data-stu-id="319ad-2511">1-2 letters (not case sensitive)</span></span> 

<span data-ttu-id="319ad-2512">Nouveau format (1er janvier 2013 et après) :</span><span class="sxs-lookup"><span data-stu-id="319ad-2512">New format (1 Jan 2013 and after):</span></span>
- <span data-ttu-id="319ad-2513">Sept chiffres </span><span class="sxs-lookup"><span data-stu-id="319ad-2513">Seven digits</span></span> 
- <span data-ttu-id="319ad-2514">Une lettre (ne respectant pas la casse), qui est un chiffre de contrôle alphabétique </span><span class="sxs-lookup"><span data-stu-id="319ad-2514">A letter (not case sensitive) which is an alphabetic check digit</span></span> 
- <span data-ttu-id="319ad-2515">La lettre « A » ou « H » (ne respectant pas la casse)</span><span class="sxs-lookup"><span data-stu-id="319ad-2515">The letter "A" or "H" (not case sensitive)</span></span>

### <a name="checksum"></a><span data-ttu-id="319ad-2516">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="319ad-2516">Checksum</span></span>

<span data-ttu-id="319ad-2517">Oui</span><span class="sxs-lookup"><span data-stu-id="319ad-2517">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="319ad-2518">Définition</span><span class="sxs-lookup"><span data-stu-id="319ad-2518">Definition</span></span>

<span data-ttu-id="319ad-2519">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="319ad-2519">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="319ad-2520">La fonction Func_ireland_pps trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="319ad-2520">The function Func_ireland_pps finds content that matches the pattern.</span></span>
- <span data-ttu-id="319ad-2521">L’une des affirmations suivantes est vraie :</span><span class="sxs-lookup"><span data-stu-id="319ad-2521">One of the following is true:</span></span>
    - <span data-ttu-id="319ad-2522">Un mot clé figurant dans la liste Keyword_ireland_pps est trouvé.</span><span class="sxs-lookup"><span data-stu-id="319ad-2522">A keyword from Keyword_ireland_pps is found.</span></span>
    - <span data-ttu-id="319ad-2523">La fonction Func_eu_date trouve une date au format correct.</span><span class="sxs-lookup"><span data-stu-id="319ad-2523">The function Func_eu_date finds a date in the right date format.</span></span>
- <span data-ttu-id="319ad-2524">La somme de contrôle est correcte.</span><span class="sxs-lookup"><span data-stu-id="319ad-2524">The checksum passes.</span></span>

<span data-ttu-id="319ad-2525">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 65 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="319ad-2525">A DLP policy is 65% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="319ad-2526">La fonction Func_ireland_pps trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="319ad-2526">The function Func_ireland_pps finds content that matches the pattern.</span></span>
- <span data-ttu-id="319ad-2527">La somme de contrôle est correcte.</span><span class="sxs-lookup"><span data-stu-id="319ad-2527">The checksum passes.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="319ad-2528">Mots-clés</span><span class="sxs-lookup"><span data-stu-id="319ad-2528">Keywords</span></span>

#### <a name="keyword_ireland_pps"></a><span data-ttu-id="319ad-2529">Keyword_ireland_pps</span><span class="sxs-lookup"><span data-stu-id="319ad-2529">Keyword_ireland_pps</span></span>

- <span data-ttu-id="319ad-2530">Personal Public Service Number</span><span class="sxs-lookup"><span data-stu-id="319ad-2530">Personal Public Service Number</span></span> 
- <span data-ttu-id="319ad-2531">PPS Number</span><span class="sxs-lookup"><span data-stu-id="319ad-2531">PPS Number</span></span> 
- <span data-ttu-id="319ad-2532">PPS Num</span><span class="sxs-lookup"><span data-stu-id="319ad-2532">PPS Num</span></span> 
- <span data-ttu-id="319ad-2533">PPS No.</span><span class="sxs-lookup"><span data-stu-id="319ad-2533">PPS No.</span></span> 
- <span data-ttu-id="319ad-2534">PPS #</span><span class="sxs-lookup"><span data-stu-id="319ad-2534">PPS #</span></span> 
- <span data-ttu-id="319ad-2535">Spa #</span><span class="sxs-lookup"><span data-stu-id="319ad-2535">PPS#</span></span> 
- <span data-ttu-id="319ad-2536">PPSN</span><span class="sxs-lookup"><span data-stu-id="319ad-2536">PPSN</span></span> 
- <span data-ttu-id="319ad-2537">Public Services Card</span><span class="sxs-lookup"><span data-stu-id="319ad-2537">Public Services Card</span></span> 
- <span data-ttu-id="319ad-2538">Uimhir Phearsanta Seirbhíse Poiblí</span><span class="sxs-lookup"><span data-stu-id="319ad-2538">Uimhir Phearsanta Seirbhíse Poiblí</span></span> 
- <span data-ttu-id="319ad-2539">Uimh.</span><span class="sxs-lookup"><span data-stu-id="319ad-2539">Uimh.</span></span> <span data-ttu-id="319ad-2540">TOXINE</span><span class="sxs-lookup"><span data-stu-id="319ad-2540">PSP</span></span> 
- <span data-ttu-id="319ad-2541">TOXINE</span><span class="sxs-lookup"><span data-stu-id="319ad-2541">PSP</span></span> 
   
## <a name="israel-bank-account-number"></a><span data-ttu-id="319ad-2542">Numéro de compte bancaire Israël</span><span class="sxs-lookup"><span data-stu-id="319ad-2542">Israel Bank Account Number</span></span>

### <a name="format"></a><span data-ttu-id="319ad-2543">Format</span><span class="sxs-lookup"><span data-stu-id="319ad-2543">Format</span></span>

<span data-ttu-id="319ad-2544">13 chiffres</span><span class="sxs-lookup"><span data-stu-id="319ad-2544">13 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="319ad-2545">Modèle</span><span class="sxs-lookup"><span data-stu-id="319ad-2545">Pattern</span></span>

<span data-ttu-id="319ad-2546">Avec</span><span class="sxs-lookup"><span data-stu-id="319ad-2546">Formatted:</span></span>
- <span data-ttu-id="319ad-2547">Deux chiffres</span><span class="sxs-lookup"><span data-stu-id="319ad-2547">Two digits</span></span> 
- <span data-ttu-id="319ad-2548">Un tiret</span><span class="sxs-lookup"><span data-stu-id="319ad-2548">A dash</span></span> 
- <span data-ttu-id="319ad-2549">Trois chiffres</span><span class="sxs-lookup"><span data-stu-id="319ad-2549">Three digits</span></span> 
- <span data-ttu-id="319ad-2550">Un tiret</span><span class="sxs-lookup"><span data-stu-id="319ad-2550">A dash</span></span> 
- <span data-ttu-id="319ad-2551">Huit chiffres</span><span class="sxs-lookup"><span data-stu-id="319ad-2551">Eight digits</span></span>

<span data-ttu-id="319ad-2552">Non</span><span class="sxs-lookup"><span data-stu-id="319ad-2552">Unformatted:</span></span>
- <span data-ttu-id="319ad-2553">	13 chiffres consécutifs</span><span class="sxs-lookup"><span data-stu-id="319ad-2553">13 consecutive digits</span></span>

### <a name="checksum"></a><span data-ttu-id="319ad-2554">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="319ad-2554">Checksum</span></span>

<span data-ttu-id="319ad-2555">Non</span><span class="sxs-lookup"><span data-stu-id="319ad-2555">No</span></span>

### <a name="definition"></a><span data-ttu-id="319ad-2556">Définition</span><span class="sxs-lookup"><span data-stu-id="319ad-2556">Definition</span></span>

<span data-ttu-id="319ad-2557">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="319ad-2557">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="319ad-2558">L’expression régulière Regex_israel_bank_account_number trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="319ad-2558">The regular expression Regex_israel_bank_account_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="319ad-2559">Un mot clé figurant dans la liste Keyword_israel_bank_account_number est trouvé.</span><span class="sxs-lookup"><span data-stu-id="319ad-2559">A keyword from Keyword_israel_bank_account_number is found.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="319ad-2560">Mots-clés</span><span class="sxs-lookup"><span data-stu-id="319ad-2560">Keywords</span></span>

#### <a name="keyword_israel_bank_account_number"></a><span data-ttu-id="319ad-2561">Keyword_israel_bank_account_number</span><span class="sxs-lookup"><span data-stu-id="319ad-2561">Keyword_israel_bank_account_number</span></span>

- <span data-ttu-id="319ad-2562">Bank Account Number</span><span class="sxs-lookup"><span data-stu-id="319ad-2562">Bank Account Number</span></span> 
- <span data-ttu-id="319ad-2563">Bank Account</span><span class="sxs-lookup"><span data-stu-id="319ad-2563">Bank Account</span></span> 
- <span data-ttu-id="319ad-2564">Numéro de compte</span><span class="sxs-lookup"><span data-stu-id="319ad-2564">Account Number</span></span> 
- <span data-ttu-id="319ad-2565">מספר חשבון בנק</span><span class="sxs-lookup"><span data-stu-id="319ad-2565">מספר חשבון בנק</span></span> 
   
## <a name="israel-national-id"></a><span data-ttu-id="319ad-2566">Carte nationale d’identité Israël</span><span class="sxs-lookup"><span data-stu-id="319ad-2566">Israel National ID</span></span>

### <a name="format"></a><span data-ttu-id="319ad-2567">Format</span><span class="sxs-lookup"><span data-stu-id="319ad-2567">Format</span></span>

<span data-ttu-id="319ad-2568">Neuf chiffres</span><span class="sxs-lookup"><span data-stu-id="319ad-2568">Nine digits</span></span>

### <a name="pattern"></a><span data-ttu-id="319ad-2569">Modèle</span><span class="sxs-lookup"><span data-stu-id="319ad-2569">Pattern</span></span>

<span data-ttu-id="319ad-2570">Neuf chiffres consécutifs</span><span class="sxs-lookup"><span data-stu-id="319ad-2570">Nine consecutive digits</span></span>

### <a name="checksum"></a><span data-ttu-id="319ad-2571">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="319ad-2571">Checksum</span></span>

<span data-ttu-id="319ad-2572">Oui</span><span class="sxs-lookup"><span data-stu-id="319ad-2572">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="319ad-2573">Définition</span><span class="sxs-lookup"><span data-stu-id="319ad-2573">Definition</span></span>

<span data-ttu-id="319ad-2574">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="319ad-2574">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="319ad-2575">La fonction Func_israeli_national_id_number trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="319ad-2575">The function Func_israeli_national_id_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="319ad-2576">Un mot clé figurant dans la liste Keyword_Israel_National_ID est trouvé.</span><span class="sxs-lookup"><span data-stu-id="319ad-2576">A keyword from Keyword_Israel_National_ID is found.</span></span>
- <span data-ttu-id="319ad-2577">La somme de contrôle est correcte.</span><span class="sxs-lookup"><span data-stu-id="319ad-2577">The checksum passes.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="319ad-2578">Mots-clés</span><span class="sxs-lookup"><span data-stu-id="319ad-2578">Keywords</span></span>

#### <a name="keyword_israel_national_id"></a><span data-ttu-id="319ad-2579">Keyword_Israel_National_ID</span><span class="sxs-lookup"><span data-stu-id="319ad-2579">Keyword_Israel_National_ID</span></span>

- <span data-ttu-id="319ad-2580">מספר זהות</span><span class="sxs-lookup"><span data-stu-id="319ad-2580">מספר זהות</span></span> 
- <span data-ttu-id="319ad-2581">Numéro d’identification nationale</span><span class="sxs-lookup"><span data-stu-id="319ad-2581">National ID Number</span></span>
   
## <a name="italy-drivers-license-number"></a><span data-ttu-id="319ad-2582">Numéro de permis de conduire Italie</span><span class="sxs-lookup"><span data-stu-id="319ad-2582">Italy Driver's License Number</span></span>

### <a name="format"></a><span data-ttu-id="319ad-2583">Format</span><span class="sxs-lookup"><span data-stu-id="319ad-2583">Format</span></span>

<span data-ttu-id="319ad-2584">Une combinaison de 10 lettres et chiffres</span><span class="sxs-lookup"><span data-stu-id="319ad-2584">A combination of 10 letters and digits</span></span>

### <a name="pattern"></a><span data-ttu-id="319ad-2585">Modèle</span><span class="sxs-lookup"><span data-stu-id="319ad-2585">Pattern</span></span>

- <span data-ttu-id="319ad-2586">Une combinaison de 10 lettres et chiffres :</span><span class="sxs-lookup"><span data-stu-id="319ad-2586">A combination of 10 letters and digits:</span></span>
- <span data-ttu-id="319ad-2587">Une lettre (ne respecte pas la casse)</span><span class="sxs-lookup"><span data-stu-id="319ad-2587">One letter (not case sensitive)</span></span> 
- <span data-ttu-id="319ad-2588">La lettre « A » ou « V » (ne respecte pas la casse)</span><span class="sxs-lookup"><span data-stu-id="319ad-2588">The letter "A" or "V" (not case sensitive)</span></span> 
- <span data-ttu-id="319ad-2589">Sept lettres (ne respectent pas la casse), des chiffres ou le trait de soulignement</span><span class="sxs-lookup"><span data-stu-id="319ad-2589">Seven letters (not case sensitive), digits, or the underscore character</span></span> 
- <span data-ttu-id="319ad-2590">Une lettre (ne respecte pas la casse)</span><span class="sxs-lookup"><span data-stu-id="319ad-2590">One letter (not case sensitive)</span></span>

### <a name="checksum"></a><span data-ttu-id="319ad-2591">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="319ad-2591">Checksum</span></span>

<span data-ttu-id="319ad-2592">Non</span><span class="sxs-lookup"><span data-stu-id="319ad-2592">No</span></span>

### <a name="definition"></a><span data-ttu-id="319ad-2593">Définition</span><span class="sxs-lookup"><span data-stu-id="319ad-2593">Definition</span></span>

<span data-ttu-id="319ad-2594">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="319ad-2594">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="319ad-2595">L’expression régulière Regex_italy_drivers_license_number trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="319ad-2595">The regular expression Regex_italy_drivers_license_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="319ad-2596">Un mot clé figurant dans la liste Keyword_italy_drivers_license_number est trouvé.</span><span class="sxs-lookup"><span data-stu-id="319ad-2596">A keyword from Keyword_italy_drivers_license_number is found.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="319ad-2597">Mots-clés</span><span class="sxs-lookup"><span data-stu-id="319ad-2597">Keywords</span></span>

#### <a name="keyword_italy_drivers_license_number"></a><span data-ttu-id="319ad-2598">Keyword_italy_drivers_license_number</span><span class="sxs-lookup"><span data-stu-id="319ad-2598">Keyword_italy_drivers_license_number</span></span>

- <span data-ttu-id="319ad-2599">numero di patente di guida</span><span class="sxs-lookup"><span data-stu-id="319ad-2599">numero di patente di guida</span></span> 
- <span data-ttu-id="319ad-2600">patente di guida</span><span class="sxs-lookup"><span data-stu-id="319ad-2600">patente di guida</span></span> 
   
## <a name="japan-bank-account-number"></a><span data-ttu-id="319ad-2601">Numéro de compte bancaire Japon</span><span class="sxs-lookup"><span data-stu-id="319ad-2601">Japan Bank Account Number</span></span>

### <a name="format"></a><span data-ttu-id="319ad-2602">Format</span><span class="sxs-lookup"><span data-stu-id="319ad-2602">Format</span></span>

<span data-ttu-id="319ad-2603">Sept ou huit chiffres</span><span class="sxs-lookup"><span data-stu-id="319ad-2603">Seven or eight digits</span></span>

### <a name="pattern"></a><span data-ttu-id="319ad-2604">Modèle</span><span class="sxs-lookup"><span data-stu-id="319ad-2604">Pattern</span></span>

<span data-ttu-id="319ad-2605">Numéro de compte bancaire :</span><span class="sxs-lookup"><span data-stu-id="319ad-2605">Bank account number:</span></span>
- <span data-ttu-id="319ad-2606">Sept ou huit chiffres</span><span class="sxs-lookup"><span data-stu-id="319ad-2606">Seven or eight digits</span></span>
- <span data-ttu-id="319ad-2607">Code guichet du compte bancaire :</span><span class="sxs-lookup"><span data-stu-id="319ad-2607">Bank account branch code:</span></span>
- <span data-ttu-id="319ad-2608">Quatre chiffres</span><span class="sxs-lookup"><span data-stu-id="319ad-2608">Four digits</span></span> 
- <span data-ttu-id="319ad-2609">Un espace ou un tiret (facultatif)</span><span class="sxs-lookup"><span data-stu-id="319ad-2609">A space or dash (optional)</span></span> 
- <span data-ttu-id="319ad-2610">Trois chiffres</span><span class="sxs-lookup"><span data-stu-id="319ad-2610">Three digits</span></span>

<span data-ttu-id="319ad-2611">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="319ad-2611">Checksum</span></span>

<span data-ttu-id="319ad-2612">Non</span><span class="sxs-lookup"><span data-stu-id="319ad-2612">No</span></span>

### <a name="definition"></a><span data-ttu-id="319ad-2613">Définition</span><span class="sxs-lookup"><span data-stu-id="319ad-2613">Definition</span></span>

<span data-ttu-id="319ad-2614">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="319ad-2614">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="319ad-2615">La fonction Func_jp_bank_account trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="319ad-2615">The function Func_jp_bank_account finds content that matches the pattern.</span></span>
- <span data-ttu-id="319ad-2616">Un mot clé figurant dans la liste Keyword_jp_bank_account est trouvé.</span><span class="sxs-lookup"><span data-stu-id="319ad-2616">A keyword from Keyword_jp_bank_account is found.</span></span>
- <span data-ttu-id="319ad-2617">L’une des affirmations suivantes est vraie :</span><span class="sxs-lookup"><span data-stu-id="319ad-2617">One of the following is true:</span></span>
- <span data-ttu-id="319ad-2618">La fonction Func_jp_bank_account_branch_code trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="319ad-2618">The function Func_jp_bank_account_branch_code finds content that matches the pattern.</span></span>
- <span data-ttu-id="319ad-2619">Un mot clé figurant dans la liste Keyword_jp_bank_branch_code est trouvé.</span><span class="sxs-lookup"><span data-stu-id="319ad-2619">A keyword from Keyword_jp_bank_branch_code is found.</span></span>

<span data-ttu-id="319ad-2620">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="319ad-2620">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="319ad-2621">La fonction Func_jp_bank_account trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="319ad-2621">The function Func_jp_bank_account finds content that matches the pattern.</span></span>
- <span data-ttu-id="319ad-2622">Un mot clé figurant dans la liste Keyword_jp_bank_account est trouvé.</span><span class="sxs-lookup"><span data-stu-id="319ad-2622">A keyword from Keyword_jp_bank_account is found.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="319ad-2623">Mots-clés</span><span class="sxs-lookup"><span data-stu-id="319ad-2623">Keywords</span></span>

#### <a name="keyword_jp_bank_account"></a><span data-ttu-id="319ad-2624">Keyword_jp_bank_account</span><span class="sxs-lookup"><span data-stu-id="319ad-2624">Keyword_jp_bank_account</span></span>

- <span data-ttu-id="319ad-2625">Numéro de compte courant</span><span class="sxs-lookup"><span data-stu-id="319ad-2625">Checking Account Number</span></span> 
- <span data-ttu-id="319ad-2626">Compte courant</span><span class="sxs-lookup"><span data-stu-id="319ad-2626">Checking Account</span></span> 
- <span data-ttu-id="319ad-2627"># compte courant</span><span class="sxs-lookup"><span data-stu-id="319ad-2627">Checking Account #</span></span> 
- <span data-ttu-id="319ad-2628">Numéro compte courant</span><span class="sxs-lookup"><span data-stu-id="319ad-2628">Checking Acct Number</span></span> 
- <span data-ttu-id="319ad-2629"># compte courant</span><span class="sxs-lookup"><span data-stu-id="319ad-2629">Checking Acct #</span></span> 
- <span data-ttu-id="319ad-2630">N° de compte courant</span><span class="sxs-lookup"><span data-stu-id="319ad-2630">Checking Acct No.</span></span> 
- <span data-ttu-id="319ad-2631">N° de compte courant</span><span class="sxs-lookup"><span data-stu-id="319ad-2631">Checking Account No.</span></span> 
- <span data-ttu-id="319ad-2632">Numéro de compte bancaire</span><span class="sxs-lookup"><span data-stu-id="319ad-2632">Bank Account Number</span></span> 
- <span data-ttu-id="319ad-2633">Compte bancaire</span><span class="sxs-lookup"><span data-stu-id="319ad-2633">Bank Account</span></span> 
- <span data-ttu-id="319ad-2634"># Compte bancaire</span><span class="sxs-lookup"><span data-stu-id="319ad-2634">Bank Account #</span></span> 
- <span data-ttu-id="319ad-2635">Numéro de compte bancaire</span><span class="sxs-lookup"><span data-stu-id="319ad-2635">Bank Acct Number</span></span> 
- <span data-ttu-id="319ad-2636"># Compte bancaire</span><span class="sxs-lookup"><span data-stu-id="319ad-2636">Bank Acct #</span></span> 
- <span data-ttu-id="319ad-2637">N° de compte bancaire</span><span class="sxs-lookup"><span data-stu-id="319ad-2637">Bank Acct No.</span></span> 
- <span data-ttu-id="319ad-2638">N° de compte bancaire</span><span class="sxs-lookup"><span data-stu-id="319ad-2638">Bank Account No.</span></span> 
- <span data-ttu-id="319ad-2639">Numéro de compte d’épargne</span><span class="sxs-lookup"><span data-stu-id="319ad-2639">Savings Account Number</span></span> 
- <span data-ttu-id="319ad-2640">Compte d’épargne</span><span class="sxs-lookup"><span data-stu-id="319ad-2640">Savings Account</span></span> 
- <span data-ttu-id="319ad-2641">N° de compte d’épargne</span><span class="sxs-lookup"><span data-stu-id="319ad-2641">Savings Account #</span></span> 
- <span data-ttu-id="319ad-2642">Numéro de compte d’épargne</span><span class="sxs-lookup"><span data-stu-id="319ad-2642">Savings Acct Number</span></span> 
- <span data-ttu-id="319ad-2643"># compte d’épargne</span><span class="sxs-lookup"><span data-stu-id="319ad-2643">Savings Acct #</span></span> 
- <span data-ttu-id="319ad-2644">N° de compte d’épargne</span><span class="sxs-lookup"><span data-stu-id="319ad-2644">Savings Acct No.</span></span> 
- <span data-ttu-id="319ad-2645">N° de compte d’épargne</span><span class="sxs-lookup"><span data-stu-id="319ad-2645">Savings Account No.</span></span> 
- <span data-ttu-id="319ad-2646">Numéro de compte de débit</span><span class="sxs-lookup"><span data-stu-id="319ad-2646">Debit Account Number</span></span> 
- <span data-ttu-id="319ad-2647">Compte de débit</span><span class="sxs-lookup"><span data-stu-id="319ad-2647">Debit Account</span></span> 
- <span data-ttu-id="319ad-2648"># Compte de débit</span><span class="sxs-lookup"><span data-stu-id="319ad-2648">Debit Account #</span></span> 
- <span data-ttu-id="319ad-2649">Numéro de compte de débit</span><span class="sxs-lookup"><span data-stu-id="319ad-2649">Debit Acct Number</span></span> 
- <span data-ttu-id="319ad-2650"># Compte de débit</span><span class="sxs-lookup"><span data-stu-id="319ad-2650">Debit Acct #</span></span> 
- <span data-ttu-id="319ad-2651">N° de compte de débit</span><span class="sxs-lookup"><span data-stu-id="319ad-2651">Debit Acct No.</span></span> 
- <span data-ttu-id="319ad-2652">N° de compte de débit</span><span class="sxs-lookup"><span data-stu-id="319ad-2652">Debit Account No.</span></span> 
- <span data-ttu-id="319ad-2653">口座番号を当座預金口座の確認</span><span class="sxs-lookup"><span data-stu-id="319ad-2653">口座番号を当座預金口座の確認</span></span> 
- <span data-ttu-id="319ad-2654">#アカウントの確認 、 勘定番号の確認</span><span class="sxs-lookup"><span data-stu-id="319ad-2654">＃アカウントの確認、勘定番号の確認</span></span> 
- <span data-ttu-id="319ad-2655">#勘定の確認</span><span class="sxs-lookup"><span data-stu-id="319ad-2655">＃勘定の確認</span></span> 
- <span data-ttu-id="319ad-2656">勘定番号の確認</span><span class="sxs-lookup"><span data-stu-id="319ad-2656">勘定番号の確認</span></span> 
- <span data-ttu-id="319ad-2657">口座番号の確認</span><span class="sxs-lookup"><span data-stu-id="319ad-2657">口座番号の確認</span></span> 
- <span data-ttu-id="319ad-2658">銀行口座番号</span><span class="sxs-lookup"><span data-stu-id="319ad-2658">銀行口座番号</span></span> 
- <span data-ttu-id="319ad-2659">銀行口座</span><span class="sxs-lookup"><span data-stu-id="319ad-2659">銀行口座</span></span> 
- <span data-ttu-id="319ad-2660">銀行口座＃</span><span class="sxs-lookup"><span data-stu-id="319ad-2660">銀行口座＃</span></span> 
- <span data-ttu-id="319ad-2661">銀行の勘定番号</span><span class="sxs-lookup"><span data-stu-id="319ad-2661">銀行の勘定番号</span></span> 
- <span data-ttu-id="319ad-2662">銀行のacct＃</span><span class="sxs-lookup"><span data-stu-id="319ad-2662">銀行のacct＃</span></span> 
- <span data-ttu-id="319ad-2663">銀行の勘定いいえ</span><span class="sxs-lookup"><span data-stu-id="319ad-2663">銀行の勘定いいえ</span></span> 
- <span data-ttu-id="319ad-2664">銀行口座番号</span><span class="sxs-lookup"><span data-stu-id="319ad-2664">銀行口座番号</span></span>
- <span data-ttu-id="319ad-2665">普通預金口座番号</span><span class="sxs-lookup"><span data-stu-id="319ad-2665">普通預金口座番号</span></span> 
- <span data-ttu-id="319ad-2666">預金口座</span><span class="sxs-lookup"><span data-stu-id="319ad-2666">預金口座</span></span> 
- <span data-ttu-id="319ad-2667">貯蓄口座＃</span><span class="sxs-lookup"><span data-stu-id="319ad-2667">貯蓄口座＃</span></span> 
- <span data-ttu-id="319ad-2668">貯蓄勘定の数</span><span class="sxs-lookup"><span data-stu-id="319ad-2668">貯蓄勘定の数</span></span> 
- <span data-ttu-id="319ad-2669">貯蓄勘定＃</span><span class="sxs-lookup"><span data-stu-id="319ad-2669">貯蓄勘定＃</span></span> 
- <span data-ttu-id="319ad-2670">貯蓄勘定番号</span><span class="sxs-lookup"><span data-stu-id="319ad-2670">貯蓄勘定番号</span></span> 
- <span data-ttu-id="319ad-2671">普通預金口座番号</span><span class="sxs-lookup"><span data-stu-id="319ad-2671">普通預金口座番号</span></span> 
- <span data-ttu-id="319ad-2672">引き落とし口座番号</span><span class="sxs-lookup"><span data-stu-id="319ad-2672">引き落とし口座番号</span></span> 
- <span data-ttu-id="319ad-2673">口座番号</span><span class="sxs-lookup"><span data-stu-id="319ad-2673">口座番号</span></span> 
- <span data-ttu-id="319ad-2674">口座番号＃</span><span class="sxs-lookup"><span data-stu-id="319ad-2674">口座番号＃</span></span> 
- <span data-ttu-id="319ad-2675">デビットのacct番号</span><span class="sxs-lookup"><span data-stu-id="319ad-2675">デビットのacct番号</span></span> 
- <span data-ttu-id="319ad-2676">デビット勘定＃</span><span class="sxs-lookup"><span data-stu-id="319ad-2676">デビット勘定＃</span></span> 
- <span data-ttu-id="319ad-2677">デビットACCTの番号</span><span class="sxs-lookup"><span data-stu-id="319ad-2677">デビットACCTの番号</span></span> 
- <span data-ttu-id="319ad-2678">デビット口座番号</span><span class="sxs-lookup"><span data-stu-id="319ad-2678">デビット口座番号</span></span> 

#### <a name="keyword_jp_bank_branch_code"></a><span data-ttu-id="319ad-2679">Keyword_jp_bank_branch_code</span><span class="sxs-lookup"><span data-stu-id="319ad-2679">Keyword_jp_bank_branch_code</span></span>

<span data-ttu-id="319ad-2680">Otemachi</span><span class="sxs-lookup"><span data-stu-id="319ad-2680">Otemachi</span></span>

## <a name="japan-drivers-license-number"></a><span data-ttu-id="319ad-2681">Numéro de permis de conduire Japon</span><span class="sxs-lookup"><span data-stu-id="319ad-2681">Japan Driver's License Number</span></span>

### <a name="format"></a><span data-ttu-id="319ad-2682">Format</span><span class="sxs-lookup"><span data-stu-id="319ad-2682">Format</span></span>

<span data-ttu-id="319ad-2683">12 chiffres</span><span class="sxs-lookup"><span data-stu-id="319ad-2683">12 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="319ad-2684">Modèle</span><span class="sxs-lookup"><span data-stu-id="319ad-2684">Pattern</span></span>

<span data-ttu-id="319ad-2685">12 chiffres consécutifs</span><span class="sxs-lookup"><span data-stu-id="319ad-2685">12 consecutive digits</span></span>

### <a name="checksum"></a><span data-ttu-id="319ad-2686">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="319ad-2686">Checksum</span></span>

<span data-ttu-id="319ad-2687">Non</span><span class="sxs-lookup"><span data-stu-id="319ad-2687">No</span></span>

### <a name="definition"></a><span data-ttu-id="319ad-2688">Définition</span><span class="sxs-lookup"><span data-stu-id="319ad-2688">Definition</span></span>

<span data-ttu-id="319ad-2689">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="319ad-2689">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="319ad-2690">La fonction Func_jp_drivers_license_number trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="319ad-2690">The function Func_jp_drivers_license_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="319ad-2691">Un mot clé figurant dans la liste Keyword_jp_drivers_license_number est trouvé.</span><span class="sxs-lookup"><span data-stu-id="319ad-2691">A keyword from Keyword_jp_drivers_license_number is found.</span></span>

```xml
<!-- Japan Driver's License Number -->
<Entity id="c6011143-d087-451c-8313-7f6d4aed2270" patternsProximity="300" recommendedConfidence="75">
    <Pattern confidenceLevel="75">
        <IdMatch idRef="Func_jp_drivers_license_number" />
        <Match idRef ="Keyword_jp_drivers_license_number" />
    </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="319ad-2692">Mots-clés</span><span class="sxs-lookup"><span data-stu-id="319ad-2692">Keywords</span></span>

#### <a name="keyword_jp_drivers_license_number"></a><span data-ttu-id="319ad-2693">Keyword_jp_drivers_license_number</span><span class="sxs-lookup"><span data-stu-id="319ad-2693">Keyword_jp_drivers_license_number</span></span>

- <span data-ttu-id="319ad-2694">LD #</span><span class="sxs-lookup"><span data-stu-id="319ad-2694">dl#</span></span> 
- <span data-ttu-id="319ad-2695">LD</span><span class="sxs-lookup"><span data-stu-id="319ad-2695">DL＃</span></span> 
- <span data-ttu-id="319ad-2696">distribution #</span><span class="sxs-lookup"><span data-stu-id="319ad-2696">dls#</span></span> 
- <span data-ttu-id="319ad-2697">DISTRIBUTION</span><span class="sxs-lookup"><span data-stu-id="319ad-2697">DLS＃</span></span> 
- <span data-ttu-id="319ad-2698">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="319ad-2698">driver license</span></span> 
- <span data-ttu-id="319ad-2699">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="319ad-2699">driver licenses</span></span> 
- <span data-ttu-id="319ad-2700">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="319ad-2700">drivers license</span></span> 
- <span data-ttu-id="319ad-2701">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="319ad-2701">driver's license</span></span> 
- <span data-ttu-id="319ad-2702">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="319ad-2702">drivers licenses</span></span> 
- <span data-ttu-id="319ad-2703">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="319ad-2703">driver's licenses</span></span> 
- <span data-ttu-id="319ad-2704">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="319ad-2704">driving licence</span></span> 
- <span data-ttu-id="319ad-2705">Profil #</span><span class="sxs-lookup"><span data-stu-id="319ad-2705">lic#</span></span> 
- <span data-ttu-id="319ad-2706">Profil</span><span class="sxs-lookup"><span data-stu-id="319ad-2706">LIC＃</span></span> 
- <span data-ttu-id="319ad-2707">conduire #</span><span class="sxs-lookup"><span data-stu-id="319ad-2707">lics#</span></span> 
- <span data-ttu-id="319ad-2708">id d’état</span><span class="sxs-lookup"><span data-stu-id="319ad-2708">state id</span></span> 
- <span data-ttu-id="319ad-2709">identification d’état</span><span class="sxs-lookup"><span data-stu-id="319ad-2709">state identification</span></span> 
- <span data-ttu-id="319ad-2710">numéro d’identification d’état</span><span class="sxs-lookup"><span data-stu-id="319ad-2710">state identification number</span></span> 
- <span data-ttu-id="319ad-2711">低所得国＃</span><span class="sxs-lookup"><span data-stu-id="319ad-2711">低所得国＃</span></span> 
- <span data-ttu-id="319ad-2712">免許証</span><span class="sxs-lookup"><span data-stu-id="319ad-2712">免許証</span></span> 
- <span data-ttu-id="319ad-2713">状態ID</span><span class="sxs-lookup"><span data-stu-id="319ad-2713">状態ID</span></span>
- <span data-ttu-id="319ad-2714">状態の識別</span><span class="sxs-lookup"><span data-stu-id="319ad-2714">状態の識別</span></span> 
- <span data-ttu-id="319ad-2715">状態の識別番号</span><span class="sxs-lookup"><span data-stu-id="319ad-2715">状態の識別番号</span></span> 
- <span data-ttu-id="319ad-2716">運転免許</span><span class="sxs-lookup"><span data-stu-id="319ad-2716">運転免許</span></span> 
- <span data-ttu-id="319ad-2717">運転免許証</span><span class="sxs-lookup"><span data-stu-id="319ad-2717">運転免許証</span></span> 
- <span data-ttu-id="319ad-2718">運転免許証番号</span><span class="sxs-lookup"><span data-stu-id="319ad-2718">運転免許証番号</span></span> 
   
## <a name="japan-passport-number"></a><span data-ttu-id="319ad-2719">Numéro de passeport Japon</span><span class="sxs-lookup"><span data-stu-id="319ad-2719">Japan Passport Number</span></span>

### <a name="format"></a><span data-ttu-id="319ad-2720">Format</span><span class="sxs-lookup"><span data-stu-id="319ad-2720">Format</span></span>

<span data-ttu-id="319ad-2721">Deux lettres suivies de sept chiffres</span><span class="sxs-lookup"><span data-stu-id="319ad-2721">Two letters followed by seven digits</span></span>

### <a name="pattern"></a><span data-ttu-id="319ad-2722">Modèle</span><span class="sxs-lookup"><span data-stu-id="319ad-2722">Pattern</span></span>

<span data-ttu-id="319ad-2723">Deux lettres (ne respectant pas la casse) suivies de sept chiffres</span><span class="sxs-lookup"><span data-stu-id="319ad-2723">Two letters (not case sensitive) followed by seven digits</span></span>

### <a name="checksum"></a><span data-ttu-id="319ad-2724">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="319ad-2724">Checksum</span></span>

<span data-ttu-id="319ad-2725">Non</span><span class="sxs-lookup"><span data-stu-id="319ad-2725">No</span></span>

### <a name="definition"></a><span data-ttu-id="319ad-2726">Définition</span><span class="sxs-lookup"><span data-stu-id="319ad-2726">Definition</span></span>

<span data-ttu-id="319ad-2727">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="319ad-2727">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="319ad-2728">La fonction Func_jp_passport trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="319ad-2728">The function Func_jp_passport finds content that matches the pattern.</span></span>
- <span data-ttu-id="319ad-2729">Un mot clé figurant dans la liste Keyword_jp_passport est trouvé.</span><span class="sxs-lookup"><span data-stu-id="319ad-2729">A keyword from Keyword_jp_passport is found.</span></span>

```xml
<!-- Japan Passport Number -->
<Entity id="75177310-1a09-4613-bf6d-833aae3743f8" patternsProximity="300" recommendedConfidence="75">
    <Pattern confidenceLevel="75">
        <IdMatch idRef="Func_jp_passport" />
        <Match idRef="Keyword_jp_passport" />
    </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="319ad-2730">Mots-clés</span><span class="sxs-lookup"><span data-stu-id="319ad-2730">Keywords</span></span>

#### <a name="keyword_jp_passport"></a><span data-ttu-id="319ad-2731">Keyword_jp_passport</span><span class="sxs-lookup"><span data-stu-id="319ad-2731">Keyword_jp_passport</span></span>

- <span data-ttu-id="319ad-2732">パスポート</span><span class="sxs-lookup"><span data-stu-id="319ad-2732">パスポート</span></span> 
- <span data-ttu-id="319ad-2733">パスポート番号</span><span class="sxs-lookup"><span data-stu-id="319ad-2733">パスポート番号</span></span> 
- <span data-ttu-id="319ad-2734">パスポートのNum</span><span class="sxs-lookup"><span data-stu-id="319ad-2734">パスポートのNum</span></span> 
- <span data-ttu-id="319ad-2735">パスポート＃</span><span class="sxs-lookup"><span data-stu-id="319ad-2735">パスポート＃</span></span> 
   
## <a name="japan-resident-registration-number"></a><span data-ttu-id="319ad-2736">Matricule de résident Japon</span><span class="sxs-lookup"><span data-stu-id="319ad-2736">Japan Resident Registration Number</span></span>

### <a name="format"></a><span data-ttu-id="319ad-2737">Format</span><span class="sxs-lookup"><span data-stu-id="319ad-2737">Format</span></span>

<span data-ttu-id="319ad-2738">11 chiffres</span><span class="sxs-lookup"><span data-stu-id="319ad-2738">11 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="319ad-2739">Modèle</span><span class="sxs-lookup"><span data-stu-id="319ad-2739">Pattern</span></span>

<span data-ttu-id="319ad-2740">11 chiffres consécutifs</span><span class="sxs-lookup"><span data-stu-id="319ad-2740">11 consecutive digits</span></span>

### <a name="checksum"></a><span data-ttu-id="319ad-2741">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="319ad-2741">Checksum</span></span>

<span data-ttu-id="319ad-2742">Non</span><span class="sxs-lookup"><span data-stu-id="319ad-2742">No</span></span>

### <a name="definition"></a><span data-ttu-id="319ad-2743">Définition</span><span class="sxs-lookup"><span data-stu-id="319ad-2743">Definition</span></span>

<span data-ttu-id="319ad-2744">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="319ad-2744">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="319ad-2745">La fonction Func_jp_resident_registration_number trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="319ad-2745">The function Func_jp_resident_registration_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="319ad-2746">Un mot clé figurant dans la liste Keyword_jp_resident_registration_number est trouvé.</span><span class="sxs-lookup"><span data-stu-id="319ad-2746">A keyword from Keyword_jp_resident_registration_number is found.</span></span>

```xml
<!-- Japan Resident Registration Number -->
<Entity id="01c1209b-6389-4faf-a5f8-3f7e13899652" patternsProximity="300" recommendedConfidence="75">
    <Pattern confidenceLevel="75">
        <IdMatch idRef="Func_jp_resident_registration_number" />
        <Match idRef ="Keyword_jp_resident_registration_number" />
    </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="319ad-2747">Mots-clés</span><span class="sxs-lookup"><span data-stu-id="319ad-2747">Keywords</span></span>

#### <a name="keyword_jp_resident_registration_number"></a><span data-ttu-id="319ad-2748">Keyword_jp_resident_registration_number</span><span class="sxs-lookup"><span data-stu-id="319ad-2748">Keyword_jp_resident_registration_number</span></span>

- <span data-ttu-id="319ad-2749">Numéro d’enregistrement du résident</span><span class="sxs-lookup"><span data-stu-id="319ad-2749">Resident Registration Number</span></span>
- <span data-ttu-id="319ad-2750">Numéro d’enregistrement du résident</span><span class="sxs-lookup"><span data-stu-id="319ad-2750">Resident Register Number</span></span> 
- <span data-ttu-id="319ad-2751">Numéro de base d’enregistrement des résidents</span><span class="sxs-lookup"><span data-stu-id="319ad-2751">Residents Basic Registry Number</span></span> 
- <span data-ttu-id="319ad-2752">N° d’enregistrement du résident</span><span class="sxs-lookup"><span data-stu-id="319ad-2752">Resident Registration No.</span></span> 
- <span data-ttu-id="319ad-2753">N° d’enregistrement du résident</span><span class="sxs-lookup"><span data-stu-id="319ad-2753">Resident Register No.</span></span> 
- <span data-ttu-id="319ad-2754">N° de base d’enregistrement des résidents</span><span class="sxs-lookup"><span data-stu-id="319ad-2754">Residents Basic Registry No.</span></span> 
- <span data-ttu-id="319ad-2755">N° d’enregistrement du résident de base</span><span class="sxs-lookup"><span data-stu-id="319ad-2755">Basic Resident Register No.</span></span> 
- <span data-ttu-id="319ad-2756">住民登録番号、登録番号をレジデント</span><span class="sxs-lookup"><span data-stu-id="319ad-2756">住民登録番号、登録番号をレジデント</span></span> 
- <span data-ttu-id="319ad-2757">住民基本登録番号、登録番号</span><span class="sxs-lookup"><span data-stu-id="319ad-2757">住民基本登録番号、登録番号</span></span> 
- <span data-ttu-id="319ad-2758">住民基本レジストリ番号を常駐</span><span class="sxs-lookup"><span data-stu-id="319ad-2758">住民基本レジストリ番号を常駐</span></span> 
- <span data-ttu-id="319ad-2759">登録番号を常駐住民基本台帳登録番号</span><span class="sxs-lookup"><span data-stu-id="319ad-2759">登録番号を常駐住民基本台帳登録番号</span></span> 

   
## <a name="japan-social-insurance-number-sin"></a><span data-ttu-id="319ad-2760">Numéro d’assurance sociale Japon</span><span class="sxs-lookup"><span data-stu-id="319ad-2760">Japan Social Insurance Number (SIN)</span></span>

### <a name="format"></a><span data-ttu-id="319ad-2761">Format</span><span class="sxs-lookup"><span data-stu-id="319ad-2761">Format</span></span>

<span data-ttu-id="319ad-2762">7 à 12 chiffres</span><span class="sxs-lookup"><span data-stu-id="319ad-2762">7-12 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="319ad-2763">Modèle</span><span class="sxs-lookup"><span data-stu-id="319ad-2763">Pattern</span></span>

<span data-ttu-id="319ad-2764">7 à 12 chiffres :</span><span class="sxs-lookup"><span data-stu-id="319ad-2764">7-12 digits:</span></span>
- <span data-ttu-id="319ad-2765">Quatre chiffres</span><span class="sxs-lookup"><span data-stu-id="319ad-2765">Four digits</span></span> 
- <span data-ttu-id="319ad-2766">Un trait d’union (facultatif)</span><span class="sxs-lookup"><span data-stu-id="319ad-2766">A hyphen (optional)</span></span> 
- <span data-ttu-id="319ad-2767">Six chiffres ou</span><span class="sxs-lookup"><span data-stu-id="319ad-2767">Six digits OR</span></span>
- <span data-ttu-id="319ad-2768">7 à 12 chiffres consécutifs</span><span class="sxs-lookup"><span data-stu-id="319ad-2768">7-12 consecutive digits</span></span>

### <a name="checksum"></a><span data-ttu-id="319ad-2769">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="319ad-2769">Checksum</span></span>

<span data-ttu-id="319ad-2770">Non</span><span class="sxs-lookup"><span data-stu-id="319ad-2770">No</span></span>

### <a name="definition"></a><span data-ttu-id="319ad-2771">Définition</span><span class="sxs-lookup"><span data-stu-id="319ad-2771">Definition</span></span>

<span data-ttu-id="319ad-2772">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="319ad-2772">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="319ad-2773">La fonction Func_jp_sin trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="319ad-2773">The function Func_jp_sin finds content that matches the pattern.</span></span>
- <span data-ttu-id="319ad-2774">Un mot clé figurant dans la liste Keyword_jp_sin est trouvé.</span><span class="sxs-lookup"><span data-stu-id="319ad-2774">A keyword from Keyword_jp_sin is found.</span></span>

<span data-ttu-id="319ad-2775">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="319ad-2775">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="319ad-2776">La fonction Func_jp_sin_pre_1997 trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="319ad-2776">The function Func_jp_sin_pre_1997 finds content that matches the pattern.</span></span>
- <span data-ttu-id="319ad-2777">Un mot clé figurant dans la liste Keyword_jp_sin est trouvé.</span><span class="sxs-lookup"><span data-stu-id="319ad-2777">A keyword from Keyword_jp_sin is found.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="319ad-2778">Mots-clés</span><span class="sxs-lookup"><span data-stu-id="319ad-2778">Keywords</span></span>

#### <a name="keyword_jp_sin"></a><span data-ttu-id="319ad-2779">Keyword_jp_sin</span><span class="sxs-lookup"><span data-stu-id="319ad-2779">Keyword_jp_sin</span></span>

- <span data-ttu-id="319ad-2780">N° d’assurance sociale</span><span class="sxs-lookup"><span data-stu-id="319ad-2780">Social Insurance No.</span></span> 
- <span data-ttu-id="319ad-2781">Numéro d’assurance sociale</span><span class="sxs-lookup"><span data-stu-id="319ad-2781">Social Insurance Num</span></span> 
- <span data-ttu-id="319ad-2782">Numéro d’assurance sociale</span><span class="sxs-lookup"><span data-stu-id="319ad-2782">Social Insurance Number</span></span> 
- <span data-ttu-id="319ad-2783">社会保険のテンキー</span><span class="sxs-lookup"><span data-stu-id="319ad-2783">社会保険のテンキー</span></span> 
- <span data-ttu-id="319ad-2784">社会保険番号</span><span class="sxs-lookup"><span data-stu-id="319ad-2784">社会保険番号</span></span> 

## <a name="japanese-residence-card-number"></a><span data-ttu-id="319ad-2785">Numéro de carte de séjour japonaise</span><span class="sxs-lookup"><span data-stu-id="319ad-2785">Japanese Residence Card Number</span></span>

### <a name="format"></a><span data-ttu-id="319ad-2786">Format</span><span class="sxs-lookup"><span data-stu-id="319ad-2786">Format</span></span>

<span data-ttu-id="319ad-2787">12 lettres et chiffres</span><span class="sxs-lookup"><span data-stu-id="319ad-2787">12 letters and digits</span></span>

### <a name="pattern"></a><span data-ttu-id="319ad-2788">Modèle</span><span class="sxs-lookup"><span data-stu-id="319ad-2788">Pattern</span></span>

<span data-ttu-id="319ad-2789">12 lettres et chiffres :</span><span class="sxs-lookup"><span data-stu-id="319ad-2789">12 letters and digits:</span></span>
- <span data-ttu-id="319ad-2790">Deux lettres (ne respectant pas la casse) </span><span class="sxs-lookup"><span data-stu-id="319ad-2790">Two letters (not case sensitive)</span></span>
- <span data-ttu-id="319ad-2791">Huit chiffres</span><span class="sxs-lookup"><span data-stu-id="319ad-2791">Eight digits</span></span> 
- <span data-ttu-id="319ad-2792">Deux lettres (ne respectant pas la casse) </span><span class="sxs-lookup"><span data-stu-id="319ad-2792">Two letters (not case sensitive)</span></span>

### <a name="checksum"></a><span data-ttu-id="319ad-2793">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="319ad-2793">Checksum</span></span>

<span data-ttu-id="319ad-2794">Non</span><span class="sxs-lookup"><span data-stu-id="319ad-2794">No</span></span>

### <a name="definition"></a><span data-ttu-id="319ad-2795">Définition</span><span class="sxs-lookup"><span data-stu-id="319ad-2795">Definition</span></span>

<span data-ttu-id="319ad-2796">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="319ad-2796">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="319ad-2797">L’expression régulière Regex_jp_residence_card_number trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="319ad-2797">The regular expression Regex_jp_residence_card_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="319ad-2798">Un mot clé depuis Keyword_jp_residence_card_number est trouvé.</span><span class="sxs-lookup"><span data-stu-id="319ad-2798">A keyword from Keyword_jp_residence_card_number is found.</span></span>

```xml
<!--Japan Residence Card Number-->
-<Entity id="ac36fef2-a289-4e2c-bb48-b02366e89fc0" recommendedConfidence="75" patternsProximity="300">
   -<Pattern confidenceLevel="75">
      <IdMatch idRef="Regex_jp_residence_card_number"/>
      <Match idRef="Keyword_jp_residence_card_number"/>
   </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="319ad-2799">Mots-clés</span><span class="sxs-lookup"><span data-stu-id="319ad-2799">Keywords</span></span>

#### <a name="keyword_jp_residence_card_number"></a><span data-ttu-id="319ad-2800">Keyword_jp_residence_card_number</span><span class="sxs-lookup"><span data-stu-id="319ad-2800">Keyword_jp_residence_card_number</span></span>

- <span data-ttu-id="319ad-2801">Numéro de carte de séjour</span><span class="sxs-lookup"><span data-stu-id="319ad-2801">Residence card number</span></span>
- <span data-ttu-id="319ad-2802">N ° carte de séjour</span><span class="sxs-lookup"><span data-stu-id="319ad-2802">Residence card no</span></span>
- <span data-ttu-id="319ad-2803">Carte de séjour #</span><span class="sxs-lookup"><span data-stu-id="319ad-2803">Residence card #</span></span>
- <span data-ttu-id="319ad-2804">在留カード番号</span><span class="sxs-lookup"><span data-stu-id="319ad-2804">在留カード番号</span></span>
   
## <a name="malaysia-id-card-number"></a><span data-ttu-id="319ad-2805">Numéro de carte d’identité Malaisie</span><span class="sxs-lookup"><span data-stu-id="319ad-2805">Malaysia ID Card Number</span></span>

### <a name="format"></a><span data-ttu-id="319ad-2806">Format</span><span class="sxs-lookup"><span data-stu-id="319ad-2806">Format</span></span>

<span data-ttu-id="319ad-2807">12 chiffres contenant éventuellement des traits d’union</span><span class="sxs-lookup"><span data-stu-id="319ad-2807">12 digits containing optional hyphens</span></span>

### <a name="pattern"></a><span data-ttu-id="319ad-2808">Modèle</span><span class="sxs-lookup"><span data-stu-id="319ad-2808">Pattern</span></span>

<span data-ttu-id="319ad-2809">12 chiffres :</span><span class="sxs-lookup"><span data-stu-id="319ad-2809">12 digits:</span></span>
- <span data-ttu-id="319ad-2810">Six chiffres au format AAMMJJ correspondant à la date de naissance </span><span class="sxs-lookup"><span data-stu-id="319ad-2810">Six digits in the format YYMMDD which are the date of birth</span></span> 
- <span data-ttu-id="319ad-2811">Un tiret (facultatif) </span><span class="sxs-lookup"><span data-stu-id="319ad-2811">A dash (optional)</span></span> 
- <span data-ttu-id="319ad-2812">Le code à deux lettres du lieu de naissance </span><span class="sxs-lookup"><span data-stu-id="319ad-2812">Two-letter place-of-birth code</span></span> 
- <span data-ttu-id="319ad-2813">Un tiret (facultatif) </span><span class="sxs-lookup"><span data-stu-id="319ad-2813">A dash (optional)</span></span> 
- <span data-ttu-id="319ad-2814">Trois chiffres aléatoires </span><span class="sxs-lookup"><span data-stu-id="319ad-2814">Three random digits</span></span> 
- <span data-ttu-id="319ad-2815">Code de sexe à un chiffre</span><span class="sxs-lookup"><span data-stu-id="319ad-2815">One-digit gender code</span></span>

### <a name="checksum"></a><span data-ttu-id="319ad-2816">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="319ad-2816">Checksum</span></span>

<span data-ttu-id="319ad-2817">Non</span><span class="sxs-lookup"><span data-stu-id="319ad-2817">No</span></span>

### <a name="definition"></a><span data-ttu-id="319ad-2818">Définition</span><span class="sxs-lookup"><span data-stu-id="319ad-2818">Definition</span></span>

<span data-ttu-id="319ad-2819">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="319ad-2819">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="319ad-2820">L’expression régulière Regex_malaysia_id_card_number trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="319ad-2820">The regular expression Regex_malaysia_id_card_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="319ad-2821">Un mot clé figurant dans la liste Keyword_malaysia_id_card_number est trouvé.</span><span class="sxs-lookup"><span data-stu-id="319ad-2821">A keyword from Keyword_malaysia_id_card_number is found.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="319ad-2822">Mots-clés</span><span class="sxs-lookup"><span data-stu-id="319ad-2822">Keywords</span></span>
   
#### <a name="keyword_malaysia_id_card_number"></a><span data-ttu-id="319ad-2823">Keyword_malaysia_id_card_number</span><span class="sxs-lookup"><span data-stu-id="319ad-2823">Keyword_malaysia_id_card_number</span></span>

- <span data-ttu-id="319ad-2824">carte d’application numérique</span><span class="sxs-lookup"><span data-stu-id="319ad-2824">digital application card</span></span>
- <span data-ttu-id="319ad-2825">i/c</span><span class="sxs-lookup"><span data-stu-id="319ad-2825">i/c</span></span>
- <span data-ttu-id="319ad-2826">n ° i/c non</span><span class="sxs-lookup"><span data-stu-id="319ad-2826">i/c no</span></span>
- <span data-ttu-id="319ad-2827">combustion</span><span class="sxs-lookup"><span data-stu-id="319ad-2827">ic</span></span>
- <span data-ttu-id="319ad-2828">n ° IC</span><span class="sxs-lookup"><span data-stu-id="319ad-2828">ic no</span></span>
- <span data-ttu-id="319ad-2829">carte d’identité</span><span class="sxs-lookup"><span data-stu-id="319ad-2829">id card</span></span>
- <span data-ttu-id="319ad-2830">Carte d’identification</span><span class="sxs-lookup"><span data-stu-id="319ad-2830">identification Card</span></span>
- <span data-ttu-id="319ad-2831">Carte d’identité</span><span class="sxs-lookup"><span data-stu-id="319ad-2831">identity card</span></span>
- <span data-ttu-id="319ad-2832">k/p</span><span class="sxs-lookup"><span data-stu-id="319ad-2832">k/p</span></span>
- <span data-ttu-id="319ad-2833">n ° k/p</span><span class="sxs-lookup"><span data-stu-id="319ad-2833">k/p no</span></span>
- <span data-ttu-id="319ad-2834">kad akuan diri</span><span class="sxs-lookup"><span data-stu-id="319ad-2834">kad akuan diri</span></span>
- <span data-ttu-id="319ad-2835">Kad aplikasi numérique</span><span class="sxs-lookup"><span data-stu-id="319ad-2835">kad aplikasi digital</span></span>
- <span data-ttu-id="319ad-2836">Kad Pengenalan Malaisie</span><span class="sxs-lookup"><span data-stu-id="319ad-2836">kad pengenalan malaysia</span></span>
- <span data-ttu-id="319ad-2837">kgf</span><span class="sxs-lookup"><span data-stu-id="319ad-2837">kp</span></span>
- <span data-ttu-id="319ad-2838">KP non</span><span class="sxs-lookup"><span data-stu-id="319ad-2838">kp no</span></span>
- <span data-ttu-id="319ad-2839">mykad</span><span class="sxs-lookup"><span data-stu-id="319ad-2839">mykad</span></span>
- <span data-ttu-id="319ad-2840">mykas</span><span class="sxs-lookup"><span data-stu-id="319ad-2840">mykas</span></span>
- <span data-ttu-id="319ad-2841">mykid</span><span class="sxs-lookup"><span data-stu-id="319ad-2841">mykid</span></span>
- <span data-ttu-id="319ad-2842">mypr</span><span class="sxs-lookup"><span data-stu-id="319ad-2842">mypr</span></span>
- <span data-ttu-id="319ad-2843">mytentera</span><span class="sxs-lookup"><span data-stu-id="319ad-2843">mytentera</span></span>
- <span data-ttu-id="319ad-2844">carte d’identité Malaisie</span><span class="sxs-lookup"><span data-stu-id="319ad-2844">malaysia identity card</span></span>
- <span data-ttu-id="319ad-2845">carte d’identité malais</span><span class="sxs-lookup"><span data-stu-id="319ad-2845">malaysian identity card</span></span>
- <span data-ttu-id="319ad-2846">NRIC</span><span class="sxs-lookup"><span data-stu-id="319ad-2846">nric</span></span>
- <span data-ttu-id="319ad-2847">carte d’identification personnelle</span><span class="sxs-lookup"><span data-stu-id="319ad-2847">personal identification card</span></span>
   
## <a name="netherlands-citizens-service-bsn-number"></a><span data-ttu-id="319ad-2848">Numéro de service du citoyen (BSN) Pays-Bas</span><span class="sxs-lookup"><span data-stu-id="319ad-2848">Netherlands Citizen's Service (BSN) Number</span></span>

### <a name="format"></a><span data-ttu-id="319ad-2849">Format</span><span class="sxs-lookup"><span data-stu-id="319ad-2849">Format</span></span>

<span data-ttu-id="319ad-2850">8 à 9 chiffres contenant éventuellement des espaces</span><span class="sxs-lookup"><span data-stu-id="319ad-2850">8-9 digits containing optional spaces</span></span>

### <a name="pattern"></a><span data-ttu-id="319ad-2851">Modèle</span><span class="sxs-lookup"><span data-stu-id="319ad-2851">Pattern</span></span>

<span data-ttu-id="319ad-2852">8 à 9 chiffres :</span><span class="sxs-lookup"><span data-stu-id="319ad-2852">8-9 digits:</span></span>
- <span data-ttu-id="319ad-2853">Trois chiffres</span><span class="sxs-lookup"><span data-stu-id="319ad-2853">Three digits</span></span> 
- <span data-ttu-id="319ad-2854">Un espace (facultatif) </span><span class="sxs-lookup"><span data-stu-id="319ad-2854">A space (optional)</span></span> 
- <span data-ttu-id="319ad-2855">Trois chiffres</span><span class="sxs-lookup"><span data-stu-id="319ad-2855">Three digits</span></span> 
- <span data-ttu-id="319ad-2856">Un espace (facultatif) </span><span class="sxs-lookup"><span data-stu-id="319ad-2856">A space (optional)</span></span> 
- <span data-ttu-id="319ad-2857">2 à 3 chiffres</span><span class="sxs-lookup"><span data-stu-id="319ad-2857">2-3 digits</span></span>

### <a name="checksum"></a><span data-ttu-id="319ad-2858">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="319ad-2858">Checksum</span></span>

<span data-ttu-id="319ad-2859">Oui</span><span class="sxs-lookup"><span data-stu-id="319ad-2859">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="319ad-2860">Définition</span><span class="sxs-lookup"><span data-stu-id="319ad-2860">Definition</span></span>

<span data-ttu-id="319ad-2861">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="319ad-2861">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="319ad-2862">La fonction Func_netherlands_bsn trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="319ad-2862">The function Func_netherlands_bsn finds content that matches the pattern.</span></span>
- <span data-ttu-id="319ad-2863">Un mot clé figurant dans la liste Keyword_netherlands_bsn est trouvé.</span><span class="sxs-lookup"><span data-stu-id="319ad-2863">A keyword from Keyword_netherlands_bsn is found.</span></span>
- <span data-ttu-id="319ad-2864">La fonction Func_eu_date2 trouve une date au format correct.</span><span class="sxs-lookup"><span data-stu-id="319ad-2864">The function Func_eu_date2 finds a date in the right date format.</span></span>
- <span data-ttu-id="319ad-2865">La somme de contrôle est correcte.</span><span class="sxs-lookup"><span data-stu-id="319ad-2865">The checksum passes.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="319ad-2866">Mots-clés</span><span class="sxs-lookup"><span data-stu-id="319ad-2866">Keywords</span></span>

#### <a name="keyword_netherlands_bsn"></a><span data-ttu-id="319ad-2867">Keyword_netherlands_bsn</span><span class="sxs-lookup"><span data-stu-id="319ad-2867">Keyword_netherlands_bsn</span></span>

- <span data-ttu-id="319ad-2868">Citizen service number</span><span class="sxs-lookup"><span data-stu-id="319ad-2868">Citizen service number</span></span> 
- <span data-ttu-id="319ad-2869">BSN</span><span class="sxs-lookup"><span data-stu-id="319ad-2869">BSN</span></span> 
- <span data-ttu-id="319ad-2870">Burgerservicenummer</span><span class="sxs-lookup"><span data-stu-id="319ad-2870">Burgerservicenummer</span></span> 
- <span data-ttu-id="319ad-2871">Sofinummer</span><span class="sxs-lookup"><span data-stu-id="319ad-2871">Sofinummer</span></span> 
- <span data-ttu-id="319ad-2872">Persoonsgebonden nummer</span><span class="sxs-lookup"><span data-stu-id="319ad-2872">Persoonsgebonden nummer</span></span> 
- <span data-ttu-id="319ad-2873">Persoonsnummer</span><span class="sxs-lookup"><span data-stu-id="319ad-2873">Persoonsnummer</span></span>    

   
## <a name="new-zealand-ministry-of-health-number"></a><span data-ttu-id="319ad-2874">Numéro du Ministère de la santé Nouvelle-Zélande</span><span class="sxs-lookup"><span data-stu-id="319ad-2874">New Zealand Ministry of Health Number</span></span>

### <a name="format"></a><span data-ttu-id="319ad-2875">Format</span><span class="sxs-lookup"><span data-stu-id="319ad-2875">Format</span></span>

<span data-ttu-id="319ad-2876">Trois lettres, un espace (facultatif) et quatre chiffres</span><span class="sxs-lookup"><span data-stu-id="319ad-2876">Three letters, a space (optional), and four digits</span></span>

### <a name="pattern"></a><span data-ttu-id="319ad-2877">Modèle</span><span class="sxs-lookup"><span data-stu-id="319ad-2877">Pattern</span></span>

<span data-ttu-id="319ad-2878">Trois lettres (ne respectant pas la casse) un espace (facultatif) quatre chiffres</span><span class="sxs-lookup"><span data-stu-id="319ad-2878">Three letters (not case sensitive) a space (optional) four digits</span></span>

### <a name="checksum"></a><span data-ttu-id="319ad-2879">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="319ad-2879">Checksum</span></span>

<span data-ttu-id="319ad-2880">Oui</span><span class="sxs-lookup"><span data-stu-id="319ad-2880">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="319ad-2881">Définition</span><span class="sxs-lookup"><span data-stu-id="319ad-2881">Definition</span></span>

<span data-ttu-id="319ad-2882">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="319ad-2882">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="319ad-2883">La fonction Func_new_zealand_ministry_of_health_number trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="319ad-2883">The function Func_new_zealand_ministry_of_health_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="319ad-2884">Un mot clé figurant dans la liste Keyword_nz_terms est trouvé.</span><span class="sxs-lookup"><span data-stu-id="319ad-2884">A keyword from Keyword_nz_terms is found.</span></span>
- <span data-ttu-id="319ad-2885">La somme de contrôle est correcte.</span><span class="sxs-lookup"><span data-stu-id="319ad-2885">The checksum passes.</span></span>

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

<span data-ttu-id="319ad-2886">Mots-clés</span><span class="sxs-lookup"><span data-stu-id="319ad-2886">Keywords</span></span>

<span data-ttu-id="319ad-2887">Keyword_nz_terms</span><span class="sxs-lookup"><span data-stu-id="319ad-2887">Keyword_nz_terms</span></span>

- <span data-ttu-id="319ad-2888">NHI</span><span class="sxs-lookup"><span data-stu-id="319ad-2888">NHI</span></span> 
- <span data-ttu-id="319ad-2889">Nouvelle-Zélande</span><span class="sxs-lookup"><span data-stu-id="319ad-2889">New Zealand</span></span> 
- <span data-ttu-id="319ad-2890">Intégrité</span><span class="sxs-lookup"><span data-stu-id="319ad-2890">Health</span></span> 
- <span data-ttu-id="319ad-2891">destinations</span><span class="sxs-lookup"><span data-stu-id="319ad-2891">treatment</span></span> 
   
## <a name="norway-identification-number"></a><span data-ttu-id="319ad-2892">Numéro d’identification Norvège</span><span class="sxs-lookup"><span data-stu-id="319ad-2892">Norway Identification Number</span></span>

### <a name="format"></a><span data-ttu-id="319ad-2893">Format</span><span class="sxs-lookup"><span data-stu-id="319ad-2893">Format</span></span>

<span data-ttu-id="319ad-2894">11 chiffres</span><span class="sxs-lookup"><span data-stu-id="319ad-2894">11 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="319ad-2895">Modèle</span><span class="sxs-lookup"><span data-stu-id="319ad-2895">Pattern</span></span>

<span data-ttu-id="319ad-2896">11 chiffres :</span><span class="sxs-lookup"><span data-stu-id="319ad-2896">11 digits:</span></span>
- <span data-ttu-id="319ad-2897">Six chiffres au format JJMMAA qui correspondent à la date de naissance </span><span class="sxs-lookup"><span data-stu-id="319ad-2897">Six digits in the format DDMMYY which are the date of birth</span></span> 
- <span data-ttu-id="319ad-2898">Numéro individuel à trois chiffres </span><span class="sxs-lookup"><span data-stu-id="319ad-2898">Three-digit individual number</span></span> 
- <span data-ttu-id="319ad-2899">Deux chiffres de contrôle</span><span class="sxs-lookup"><span data-stu-id="319ad-2899">Two check digits</span></span>

### <a name="checksum"></a><span data-ttu-id="319ad-2900">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="319ad-2900">Checksum</span></span>

<span data-ttu-id="319ad-2901">Oui</span><span class="sxs-lookup"><span data-stu-id="319ad-2901">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="319ad-2902">Définition</span><span class="sxs-lookup"><span data-stu-id="319ad-2902">Definition</span></span>

<span data-ttu-id="319ad-2903">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="319ad-2903">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="319ad-2904">La fonction Func_norway_id_number trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="319ad-2904">The function Func_norway_id_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="319ad-2905">Un mot clé figurant dans la liste Keyword_norway_id_number est trouvé.</span><span class="sxs-lookup"><span data-stu-id="319ad-2905">A keyword from Keyword_norway_id_number is found.</span></span>
- <span data-ttu-id="319ad-2906">La somme de contrôle est correcte.</span><span class="sxs-lookup"><span data-stu-id="319ad-2906">The checksum passes.</span></span>
- <span data-ttu-id="319ad-2907">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="319ad-2907">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="319ad-2908">La fonction Func_norway_id_numbe trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="319ad-2908">The function Func_norway_id_numbe finds content that matches the pattern.</span></span>
- <span data-ttu-id="319ad-2909">La somme de contrôle est correcte.</span><span class="sxs-lookup"><span data-stu-id="319ad-2909">The checksum passes.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="319ad-2910">Mots-clés</span><span class="sxs-lookup"><span data-stu-id="319ad-2910">Keywords</span></span>

#### <a name="keyword_norway_id_number"></a><span data-ttu-id="319ad-2911">Keyword_norway_id_number</span><span class="sxs-lookup"><span data-stu-id="319ad-2911">Keyword_norway_id_number</span></span>

- <span data-ttu-id="319ad-2912">Personal identification number</span><span class="sxs-lookup"><span data-stu-id="319ad-2912">Personal identification number</span></span>
- <span data-ttu-id="319ad-2913">Norwegian ID Number</span><span class="sxs-lookup"><span data-stu-id="319ad-2913">Norwegian ID Number</span></span>
- <span data-ttu-id="319ad-2914">ID Number</span><span class="sxs-lookup"><span data-stu-id="319ad-2914">ID Number</span></span>
- <span data-ttu-id="319ad-2915">Identificateur</span><span class="sxs-lookup"><span data-stu-id="319ad-2915">Identification</span></span>
- <span data-ttu-id="319ad-2916">Personnummer</span><span class="sxs-lookup"><span data-stu-id="319ad-2916">Personnummer</span></span>
- <span data-ttu-id="319ad-2917">Fødselsnummer</span><span class="sxs-lookup"><span data-stu-id="319ad-2917">Fødselsnummer</span></span>

   
## <a name="philippines-unified-multi-purpose-id-number"></a><span data-ttu-id="319ad-2918">Numéro d’identification multifonction unifié Philippines</span><span class="sxs-lookup"><span data-stu-id="319ad-2918">Philippines Unified Multi-Purpose ID Number</span></span>

### <a name="format"></a><span data-ttu-id="319ad-2919">Format</span><span class="sxs-lookup"><span data-stu-id="319ad-2919">Format</span></span>

<span data-ttu-id="319ad-2920">12 chiffres séparés par des traits d’union</span><span class="sxs-lookup"><span data-stu-id="319ad-2920">12 digits separated by hyphens</span></span>

### <a name="pattern"></a><span data-ttu-id="319ad-2921">Modèle</span><span class="sxs-lookup"><span data-stu-id="319ad-2921">Pattern</span></span>

<span data-ttu-id="319ad-2922">12 chiffres :</span><span class="sxs-lookup"><span data-stu-id="319ad-2922">12 digits:</span></span>
- <span data-ttu-id="319ad-2923">Quatre chiffres</span><span class="sxs-lookup"><span data-stu-id="319ad-2923">Four digits</span></span> 
- <span data-ttu-id="319ad-2924">Un trait d’union </span><span class="sxs-lookup"><span data-stu-id="319ad-2924">A hyphen</span></span> 
- <span data-ttu-id="319ad-2925">Sept chiffres </span><span class="sxs-lookup"><span data-stu-id="319ad-2925">Seven digits</span></span> 
- <span data-ttu-id="319ad-2926">Un trait d’union </span><span class="sxs-lookup"><span data-stu-id="319ad-2926">A hyphen</span></span> 
- <span data-ttu-id="319ad-2927">Un chiffre</span><span class="sxs-lookup"><span data-stu-id="319ad-2927">One digit</span></span>

### <a name="checksum"></a><span data-ttu-id="319ad-2928">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="319ad-2928">Checksum</span></span>

<span data-ttu-id="319ad-2929">Non</span><span class="sxs-lookup"><span data-stu-id="319ad-2929">No</span></span>

### <a name="definition"></a><span data-ttu-id="319ad-2930">Définition</span><span class="sxs-lookup"><span data-stu-id="319ad-2930">Definition</span></span>

<span data-ttu-id="319ad-2931">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="319ad-2931">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="319ad-2932">L’expression régulière Regex_philippines_unified_id trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="319ad-2932">The regular expression Regex_philippines_unified_id finds content that matches the pattern.</span></span>
- <span data-ttu-id="319ad-2933">Un mot clé figurant dans la liste Keyword_philippines_id est trouvé.</span><span class="sxs-lookup"><span data-stu-id="319ad-2933">A keyword from Keyword_philippines_id is found.</span></span>

```xml
<!-- Philippines Unified Multi-Purpose ID number -->
<Entity id="019b39dd-8c25-4765-91a3-d9c6baf3c3b3" recommendedConfidence="75" patternsProximity="300">
  <Pattern confidenceLevel="75">
     <IdMatch idRef="Regex_philippines_unified_id"/>
     <Match idRef="Keyword_philippines_id"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="319ad-2934">Mots-clés</span><span class="sxs-lookup"><span data-stu-id="319ad-2934">Keywords</span></span>
   
#### <a name="keyword_philippines_id"></a><span data-ttu-id="319ad-2935">Keyword_philippines_id</span><span class="sxs-lookup"><span data-stu-id="319ad-2935">Keyword_philippines_id</span></span>

- <span data-ttu-id="319ad-2936">Unified Multi-Purpose ID</span><span class="sxs-lookup"><span data-stu-id="319ad-2936">Unified Multi-Purpose ID</span></span> 
- <span data-ttu-id="319ad-2937">UMID</span><span class="sxs-lookup"><span data-stu-id="319ad-2937">UMID</span></span> 
- <span data-ttu-id="319ad-2938">Identity Card</span><span class="sxs-lookup"><span data-stu-id="319ad-2938">Identity Card</span></span> 
- <span data-ttu-id="319ad-2939">Pinag-isang Multi-Layunin ID</span><span class="sxs-lookup"><span data-stu-id="319ad-2939">Pinag-isang Multi-Layunin ID</span></span>
   
## <a name="poland-identity-card"></a><span data-ttu-id="319ad-2940">Carte d'identité Pologne</span><span class="sxs-lookup"><span data-stu-id="319ad-2940">Poland Identity Card</span></span>

### <a name="format"></a><span data-ttu-id="319ad-2941">Format</span><span class="sxs-lookup"><span data-stu-id="319ad-2941">Format</span></span>

<span data-ttu-id="319ad-2942">Trois lettres et six chiffres</span><span class="sxs-lookup"><span data-stu-id="319ad-2942">Three letters and six digits</span></span>

### <a name="pattern"></a><span data-ttu-id="319ad-2943">Modèle</span><span class="sxs-lookup"><span data-stu-id="319ad-2943">Pattern</span></span>

<span data-ttu-id="319ad-2944">Trois lettres (ne respectant pas la casse) suivis de six chiffres</span><span class="sxs-lookup"><span data-stu-id="319ad-2944">Three letters (not case sensitive) followed by six digits</span></span>

### <a name="checksum"></a><span data-ttu-id="319ad-2945">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="319ad-2945">Checksum</span></span>

<span data-ttu-id="319ad-2946">Oui</span><span class="sxs-lookup"><span data-stu-id="319ad-2946">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="319ad-2947">Définition</span><span class="sxs-lookup"><span data-stu-id="319ad-2947">Definition</span></span>

<span data-ttu-id="319ad-2948">Une stratégie DLP est sûre à 75% d’avoir détecté ce type d’informations sensibles si, dans une proximité de 300 caractères : la fonction Func_polish_national_id trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="319ad-2948">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters: The function Func_polish_national_id finds content that matches the pattern.</span></span>
<span data-ttu-id="319ad-2949">Un mot clé figurant dans la liste Keyword_polish_national_id_passport_number est trouvé.</span><span class="sxs-lookup"><span data-stu-id="319ad-2949">A keyword from Keyword_polish_national_id_passport_number is found.</span></span>
<span data-ttu-id="319ad-2950">La somme de contrôle est correcte.</span><span class="sxs-lookup"><span data-stu-id="319ad-2950">The checksum passes.</span></span>

```xml
<!-- Poland Identity Card-->
<Entity id="25E64989-ED5D-40CA-A939-6C14183BB7BF" patternsProximity="300" recommendedConfidence="85">
      <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_polish_national_id" />
          <Match idRef="Keyword_polish_national_id_passport_number" />
      </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="319ad-2951">Mots-clés</span><span class="sxs-lookup"><span data-stu-id="319ad-2951">Keywords</span></span>

#### <a name="keyword_polish_national_id_passport_number"></a><span data-ttu-id="319ad-2952">Keyword_polish_national_id_passport_number</span><span class="sxs-lookup"><span data-stu-id="319ad-2952">Keyword_polish_national_id_passport_number</span></span>

- <span data-ttu-id="319ad-2953">Dowód osobisty</span><span class="sxs-lookup"><span data-stu-id="319ad-2953">Dowód osobisty</span></span>
- <span data-ttu-id="319ad-2954">Chiffre dowodu osobistego</span><span class="sxs-lookup"><span data-stu-id="319ad-2954">Numer dowodu osobistego</span></span>
- <span data-ttu-id="319ad-2955">Nazwa i dowodu osobistego</span><span class="sxs-lookup"><span data-stu-id="319ad-2955">Nazwa i numer dowodu osobistego</span></span>
- <span data-ttu-id="319ad-2956">Nazwa i Nr dowodu osobistego</span><span class="sxs-lookup"><span data-stu-id="319ad-2956">Nazwa i nr dowodu osobistego</span></span>
- <span data-ttu-id="319ad-2957">Nazwa je nr dowodu tożsamości</span><span class="sxs-lookup"><span data-stu-id="319ad-2957">Nazwa i nr dowodu tożsamości</span></span>
- <span data-ttu-id="319ad-2958">Dowód Tożsamości</span><span class="sxs-lookup"><span data-stu-id="319ad-2958">Dowód Tożsamości</span></span>
- <span data-ttu-id="319ad-2959">Dow.</span><span class="sxs-lookup"><span data-stu-id="319ad-2959">dow.</span></span> <span data-ttu-id="319ad-2960">OS.</span><span class="sxs-lookup"><span data-stu-id="319ad-2960">os.</span></span>

   
## <a name="poland-national-id-pesel"></a><span data-ttu-id="319ad-2961">ID national polonais (PESEL)</span><span class="sxs-lookup"><span data-stu-id="319ad-2961">Poland National ID (PESEL)</span></span>

### <a name="format"></a><span data-ttu-id="319ad-2962">Format</span><span class="sxs-lookup"><span data-stu-id="319ad-2962">Format</span></span>

<span data-ttu-id="319ad-2963">11 chiffres</span><span class="sxs-lookup"><span data-stu-id="319ad-2963">11 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="319ad-2964">Modèle</span><span class="sxs-lookup"><span data-stu-id="319ad-2964">Pattern</span></span>

<span data-ttu-id="319ad-2965">11 chiffres consécutifs</span><span class="sxs-lookup"><span data-stu-id="319ad-2965">11 consecutive digits</span></span>

### <a name="checksum"></a><span data-ttu-id="319ad-2966">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="319ad-2966">Checksum</span></span>

<span data-ttu-id="319ad-2967">Oui</span><span class="sxs-lookup"><span data-stu-id="319ad-2967">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="319ad-2968">Définition</span><span class="sxs-lookup"><span data-stu-id="319ad-2968">Definition</span></span>

<span data-ttu-id="319ad-2969">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="319ad-2969">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="319ad-2970">La fonction Func_pesel_identification_number trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="319ad-2970">The function Func_pesel_identification_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="319ad-2971">Un mot clé figurant dans la liste Keyword_pesel_identification_number est trouvé.</span><span class="sxs-lookup"><span data-stu-id="319ad-2971">A keyword from Keyword_pesel_identification_number is found.</span></span>
- <span data-ttu-id="319ad-2972">La somme de contrôle est correcte.</span><span class="sxs-lookup"><span data-stu-id="319ad-2972">The checksum passes.</span></span>

```xml
<!-- Poland National ID (PESEL) -->      
<Entity id="E3AAF206-4297-412F-9E06-BA8487E22456" patternsProximity="300" recommendedConfidence="85">
      <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_pesel_identification_number" />
          <Match idRef="Keyword_pesel_identification_number" />
      </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="319ad-2973">Mots-clés</span><span class="sxs-lookup"><span data-stu-id="319ad-2973">Keywords</span></span>

#### <a name="keyword_pesel_identification_number"></a><span data-ttu-id="319ad-2974">Keyword_pesel_identification_number</span><span class="sxs-lookup"><span data-stu-id="319ad-2974">Keyword_pesel_identification_number</span></span>

- <span data-ttu-id="319ad-2975">Nr PESEL</span><span class="sxs-lookup"><span data-stu-id="319ad-2975">Nr PESEL</span></span>
- <span data-ttu-id="319ad-2976">PESEL</span><span class="sxs-lookup"><span data-stu-id="319ad-2976">PESEL</span></span>   

   
## <a name="poland-passport"></a><span data-ttu-id="319ad-2977">Passeport Pologne</span><span class="sxs-lookup"><span data-stu-id="319ad-2977">Poland Passport</span></span>

### <a name="format"></a><span data-ttu-id="319ad-2978">Format</span><span class="sxs-lookup"><span data-stu-id="319ad-2978">Format</span></span>

<span data-ttu-id="319ad-2979">Deux lettres et sept chiffres</span><span class="sxs-lookup"><span data-stu-id="319ad-2979">Two letters and seven digits</span></span>

### <a name="pattern"></a><span data-ttu-id="319ad-2980">Modèle</span><span class="sxs-lookup"><span data-stu-id="319ad-2980">Pattern</span></span>

<span data-ttu-id="319ad-2981">Deux lettres (ne respectant pas la casse) suivies de sept chiffres</span><span class="sxs-lookup"><span data-stu-id="319ad-2981">Two letters (not case sensitive) followed by seven digits</span></span>

### <a name="checksum"></a><span data-ttu-id="319ad-2982">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="319ad-2982">Checksum</span></span>

<span data-ttu-id="319ad-2983">Oui</span><span class="sxs-lookup"><span data-stu-id="319ad-2983">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="319ad-2984">Définition</span><span class="sxs-lookup"><span data-stu-id="319ad-2984">Definition</span></span>

<span data-ttu-id="319ad-2985">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="319ad-2985">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="319ad-2986">La fonction Func_polish_passport_number trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="319ad-2986">The function Func_polish_passport_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="319ad-2987">Un mot clé figurant dans la liste Keyword_polish_national_id_passport_number est trouvé.</span><span class="sxs-lookup"><span data-stu-id="319ad-2987">A keyword from Keyword_polish_national_id_passport_number is found.</span></span>
- <span data-ttu-id="319ad-2988">La somme de contrôle est correcte.</span><span class="sxs-lookup"><span data-stu-id="319ad-2988">The checksum passes.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="319ad-2989">Mots-clés</span><span class="sxs-lookup"><span data-stu-id="319ad-2989">Keywords</span></span>

#### <a name="keyword_polish_national_id_passport_number"></a><span data-ttu-id="319ad-2990">Keyword_polish_national_id_passport_number</span><span class="sxs-lookup"><span data-stu-id="319ad-2990">Keyword_polish_national_id_passport_number</span></span>

- <span data-ttu-id="319ad-2991">Numéro paszportu</span><span class="sxs-lookup"><span data-stu-id="319ad-2991">Numer paszportu</span></span>
- <span data-ttu-id="319ad-2992">Nr.</span><span class="sxs-lookup"><span data-stu-id="319ad-2992">Nr.</span></span> <span data-ttu-id="319ad-2993">Paszportu</span><span class="sxs-lookup"><span data-stu-id="319ad-2993">Paszportu</span></span>
- <span data-ttu-id="319ad-2994">Paszport</span><span class="sxs-lookup"><span data-stu-id="319ad-2994">Paszport</span></span>

   
## <a name="portugal-citizen-card-number"></a><span data-ttu-id="319ad-2995">Numéro de carte de citoyen Portugal</span><span class="sxs-lookup"><span data-stu-id="319ad-2995">Portugal Citizen Card Number</span></span>

### <a name="format"></a><span data-ttu-id="319ad-2996">Format</span><span class="sxs-lookup"><span data-stu-id="319ad-2996">Format</span></span>

<span data-ttu-id="319ad-2997">Huit chiffres</span><span class="sxs-lookup"><span data-stu-id="319ad-2997">Eight digits</span></span>

### <a name="pattern"></a><span data-ttu-id="319ad-2998">Modèle</span><span class="sxs-lookup"><span data-stu-id="319ad-2998">Pattern</span></span>

<span data-ttu-id="319ad-2999">Huit chiffres</span><span class="sxs-lookup"><span data-stu-id="319ad-2999">Eight digits</span></span>

### <a name="checksum"></a><span data-ttu-id="319ad-3000">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="319ad-3000">Checksum</span></span>

<span data-ttu-id="319ad-3001">Non</span><span class="sxs-lookup"><span data-stu-id="319ad-3001">No</span></span>

### <a name="definition"></a><span data-ttu-id="319ad-3002">Définition</span><span class="sxs-lookup"><span data-stu-id="319ad-3002">Definition</span></span>

<span data-ttu-id="319ad-3003">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="319ad-3003">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="319ad-3004">L’expression régulière Regex_portugal_citizen_card trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="319ad-3004">The regular expression Regex_portugal_citizen_card finds content that matches the pattern.</span></span>
- <span data-ttu-id="319ad-3005">Un mot clé figurant dans la liste Keyword_portugal_citizen_card est trouvé.</span><span class="sxs-lookup"><span data-stu-id="319ad-3005">A keyword from Keyword_portugal_citizen_card is found.</span></span>

```xml
<!-- Portugal Citizen Card Number -->
<Entity id="91a7ece2-add4-4986-9a15-c84544d81ecd" recommendedConfidence="85" patternsProximity="300">
  <Pattern confidenceLevel="85">
     <IdMatch idRef="Regex_portugal_citizen_card"/>
     <Match idRef="Keyword_portugal_citizen_card"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="319ad-3006">Mots-clés</span><span class="sxs-lookup"><span data-stu-id="319ad-3006">Keywords</span></span>

#### <a name="keyword_portugal_citizen_card"></a><span data-ttu-id="319ad-3007">Keyword_portugal_citizen_card</span><span class="sxs-lookup"><span data-stu-id="319ad-3007">Keyword_portugal_citizen_card</span></span>

- <span data-ttu-id="319ad-3008">Citizen Card</span><span class="sxs-lookup"><span data-stu-id="319ad-3008">Citizen Card</span></span>
- <span data-ttu-id="319ad-3009">National ID Card</span><span class="sxs-lookup"><span data-stu-id="319ad-3009">National ID Card</span></span>
- <span data-ttu-id="319ad-3010">Cc</span><span class="sxs-lookup"><span data-stu-id="319ad-3010">CC</span></span>
- <span data-ttu-id="319ad-3011">Cartão de Cidadão</span><span class="sxs-lookup"><span data-stu-id="319ad-3011">Cartão de Cidadão</span></span>
- <span data-ttu-id="319ad-3012">Bilhete de Identidade</span><span class="sxs-lookup"><span data-stu-id="319ad-3012">Bilhete de Identidade</span></span>
   
## <a name="saudi-arabia-national-id"></a><span data-ttu-id="319ad-3013">ID national Arabie saoudite</span><span class="sxs-lookup"><span data-stu-id="319ad-3013">Saudi Arabia National ID</span></span>

### <a name="format"></a><span data-ttu-id="319ad-3014">Format</span><span class="sxs-lookup"><span data-stu-id="319ad-3014">Format</span></span>

<span data-ttu-id="319ad-3015">10 chiffres</span><span class="sxs-lookup"><span data-stu-id="319ad-3015">10 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="319ad-3016">Modèle</span><span class="sxs-lookup"><span data-stu-id="319ad-3016">Pattern</span></span>

<span data-ttu-id="319ad-3017">10 chiffres consécutifs</span><span class="sxs-lookup"><span data-stu-id="319ad-3017">10 consecutive digits</span></span>

### <a name="checksum"></a><span data-ttu-id="319ad-3018">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="319ad-3018">Checksum</span></span>

<span data-ttu-id="319ad-3019">Non</span><span class="sxs-lookup"><span data-stu-id="319ad-3019">No</span></span>

### <a name="definition"></a><span data-ttu-id="319ad-3020">Définition</span><span class="sxs-lookup"><span data-stu-id="319ad-3020">Definition</span></span>

<span data-ttu-id="319ad-3021">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="319ad-3021">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="319ad-3022">L’expression régulière Regex_saudi_arabia_national_id trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="319ad-3022">The regular expression Regex_saudi_arabia_national_id finds content that matches the pattern.</span></span>
- <span data-ttu-id="319ad-3023">Un mot clé figurant dans la liste Keyword_saudi_arabia_national_id est trouvé.</span><span class="sxs-lookup"><span data-stu-id="319ad-3023">A keyword from Keyword_saudi_arabia_national_id is found.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="319ad-3024">Mots-clés</span><span class="sxs-lookup"><span data-stu-id="319ad-3024">Keywords</span></span>

#### <a name="keyword_saudi_arabia_national_id"></a><span data-ttu-id="319ad-3025">Keyword_saudi_arabia_national_id</span><span class="sxs-lookup"><span data-stu-id="319ad-3025">Keyword_saudi_arabia_national_id</span></span>

- <span data-ttu-id="319ad-3026">Carte d’identification</span><span class="sxs-lookup"><span data-stu-id="319ad-3026">Identification Card</span></span> 
- <span data-ttu-id="319ad-3027">numéro de carte d’identité</span><span class="sxs-lookup"><span data-stu-id="319ad-3027">I card number</span></span> 
- <span data-ttu-id="319ad-3028">Numéro d’identification</span><span class="sxs-lookup"><span data-stu-id="319ad-3028">ID number</span></span> 
- <span data-ttu-id="319ad-3029">الوطنية الهوية بطاقة رقم</span><span class="sxs-lookup"><span data-stu-id="319ad-3029">الوطنية الهوية بطاقة رقم</span></span> 

   
## <a name="singapore-national-registration-identity-card-nric-number"></a><span data-ttu-id="319ad-3030">Numéro de carte d’identité d’enregistrement national (NRIC) Singapour</span><span class="sxs-lookup"><span data-stu-id="319ad-3030">Singapore National Registration Identity Card (NRIC) Number</span></span>

### <a name="format"></a><span data-ttu-id="319ad-3031">Format</span><span class="sxs-lookup"><span data-stu-id="319ad-3031">Format</span></span>

<span data-ttu-id="319ad-3032">Neuf lettres et chiffres</span><span class="sxs-lookup"><span data-stu-id="319ad-3032">Nine letters and digits</span></span>

### <a name="pattern"></a><span data-ttu-id="319ad-3033">Modèle</span><span class="sxs-lookup"><span data-stu-id="319ad-3033">Pattern</span></span>

- <span data-ttu-id="319ad-3034">Neuf lettres et chiffres :</span><span class="sxs-lookup"><span data-stu-id="319ad-3034">Nine letters and digits:</span></span>
- <span data-ttu-id="319ad-3035">La lettre « F », « G », « S » ou « T » (ne respectant pas la casse) </span><span class="sxs-lookup"><span data-stu-id="319ad-3035">The letter "F", "G", "S", or "T" (not case sensitive)</span></span> 
- <span data-ttu-id="319ad-3036">Sept chiffres </span><span class="sxs-lookup"><span data-stu-id="319ad-3036">Seven digits</span></span> 
- <span data-ttu-id="319ad-3037">Un chiffre de contrôle alphabétique</span><span class="sxs-lookup"><span data-stu-id="319ad-3037">An alphabetic check digit</span></span>

### <a name="checksum"></a><span data-ttu-id="319ad-3038">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="319ad-3038">Checksum</span></span>

<span data-ttu-id="319ad-3039">Oui</span><span class="sxs-lookup"><span data-stu-id="319ad-3039">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="319ad-3040">Définition</span><span class="sxs-lookup"><span data-stu-id="319ad-3040">Definition</span></span>

<span data-ttu-id="319ad-3041">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="319ad-3041">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="319ad-3042">L’expression régulière Regex_singapore_nric trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="319ad-3042">The regular expression Regex_singapore_nric finds content that matches the pattern.</span></span>
- <span data-ttu-id="319ad-3043">Un mot clé figurant dans la liste Keyword_singapore_nric est trouvé.</span><span class="sxs-lookup"><span data-stu-id="319ad-3043">A keyword from Keyword_singapore_nric is found.</span></span>
- <span data-ttu-id="319ad-3044">La somme de contrôle est correcte.</span><span class="sxs-lookup"><span data-stu-id="319ad-3044">The checksum passes.</span></span>

<span data-ttu-id="319ad-3045">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="319ad-3045">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="319ad-3046">L’expression régulière Regex_singapore_nric trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="319ad-3046">The regular expression Regex_singapore_nric finds content that matches the pattern.</span></span>
- <span data-ttu-id="319ad-3047">La somme de contrôle est correcte.</span><span class="sxs-lookup"><span data-stu-id="319ad-3047">The checksum passes.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="319ad-3048">Mots-clés</span><span class="sxs-lookup"><span data-stu-id="319ad-3048">Keywords</span></span>
   
#### <a name="keyword_singapore_nric"></a><span data-ttu-id="319ad-3049">Keyword_singapore_nric</span><span class="sxs-lookup"><span data-stu-id="319ad-3049">Keyword_singapore_nric</span></span>

- <span data-ttu-id="319ad-3050">National Registration Identity Card</span><span class="sxs-lookup"><span data-stu-id="319ad-3050">National Registration Identity Card</span></span> 
- <span data-ttu-id="319ad-3051">Identity Card Number</span><span class="sxs-lookup"><span data-stu-id="319ad-3051">Identity Card Number</span></span> 
- <span data-ttu-id="319ad-3052">NRIC</span><span class="sxs-lookup"><span data-stu-id="319ad-3052">NRIC</span></span> 
- <span data-ttu-id="319ad-3053">COMBUSTION</span><span class="sxs-lookup"><span data-stu-id="319ad-3053">IC</span></span> 
- <span data-ttu-id="319ad-3054">Foreign Identification Number</span><span class="sxs-lookup"><span data-stu-id="319ad-3054">Foreign Identification Number</span></span> 
- <span data-ttu-id="319ad-3055">ECHERCHER</span><span class="sxs-lookup"><span data-stu-id="319ad-3055">FIN</span></span> 
- <span data-ttu-id="319ad-3056">身份证</span><span class="sxs-lookup"><span data-stu-id="319ad-3056">身份证</span></span> 
- <span data-ttu-id="319ad-3057">身份證</span><span class="sxs-lookup"><span data-stu-id="319ad-3057">身份證</span></span> 
   
## <a name="south-africa-identification-number"></a><span data-ttu-id="319ad-3058">Numéro d’identification Afrique du Sud</span><span class="sxs-lookup"><span data-stu-id="319ad-3058">South Africa Identification Number</span></span>

### <a name="format"></a><span data-ttu-id="319ad-3059">Format</span><span class="sxs-lookup"><span data-stu-id="319ad-3059">Format</span></span>

<span data-ttu-id="319ad-3060">13 chiffres pouvant contenir des espaces</span><span class="sxs-lookup"><span data-stu-id="319ad-3060">13 digits that may contain spaces</span></span>

### <a name="pattern"></a><span data-ttu-id="319ad-3061">Modèle</span><span class="sxs-lookup"><span data-stu-id="319ad-3061">Pattern</span></span>

<span data-ttu-id="319ad-3062">13 chiffres :</span><span class="sxs-lookup"><span data-stu-id="319ad-3062">13 digits:</span></span>
- <span data-ttu-id="319ad-3063">Six chiffres au format AAMMJJ correspondant à la date de naissance </span><span class="sxs-lookup"><span data-stu-id="319ad-3063">Six digits in the format YYMMDD which are the date of birth</span></span> 
- <span data-ttu-id="319ad-3064">Quatre chiffres</span><span class="sxs-lookup"><span data-stu-id="319ad-3064">Four digits</span></span> 
- <span data-ttu-id="319ad-3065">Un indicateur de citoyenneté à un chiffre </span><span class="sxs-lookup"><span data-stu-id="319ad-3065">A single-digit citizenship indicator</span></span> 
- <span data-ttu-id="319ad-3066">Le chiffre « 8 » ou « 9 » </span><span class="sxs-lookup"><span data-stu-id="319ad-3066">The digit "8" or "9"</span></span> 
- <span data-ttu-id="319ad-3067">Un chiffre pour la somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="319ad-3067">One digit which is a checksum digit</span></span>

### <a name="checksum"></a><span data-ttu-id="319ad-3068">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="319ad-3068">Checksum</span></span>

<span data-ttu-id="319ad-3069">Oui</span><span class="sxs-lookup"><span data-stu-id="319ad-3069">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="319ad-3070">Définition</span><span class="sxs-lookup"><span data-stu-id="319ad-3070">Definition</span></span>

<span data-ttu-id="319ad-3071">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="319ad-3071">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="319ad-3072">La fonction Func_south_africa_identification_number trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="319ad-3072">The function Func_south_africa_identification_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="319ad-3073">Un mot clé figurant dans la liste Keyword_south_africa_identification_number est trouvé.</span><span class="sxs-lookup"><span data-stu-id="319ad-3073">A keyword from Keyword_south_africa_identification_number is found.</span></span>
- <span data-ttu-id="319ad-3074">La somme de contrôle est correcte.</span><span class="sxs-lookup"><span data-stu-id="319ad-3074">The checksum passes.</span></span>

```xml
<!-- South Africa Identification Number -->
<Entity id="e2adf7cb-8ea6-4048-a2ed-d89eb65f2780" recommendedConfidence="85" patternsProximity="300">
  <Pattern confidenceLevel="85">
     <IdMatch idRef="Func_south_africa_identification_number"/>
     <Match idRef="Keyword_south_africa_identification_number"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="319ad-3075">Mots-clés</span><span class="sxs-lookup"><span data-stu-id="319ad-3075">Keywords</span></span>
   
#### <a name="keyword_south_africa_identification_number"></a><span data-ttu-id="319ad-3076">Keyword_south_africa_identification_number</span><span class="sxs-lookup"><span data-stu-id="319ad-3076">Keyword_south_africa_identification_number</span></span>

- <span data-ttu-id="319ad-3077">Identity card</span><span class="sxs-lookup"><span data-stu-id="319ad-3077">Identity card</span></span>
- <span data-ttu-id="319ad-3078">ID</span><span class="sxs-lookup"><span data-stu-id="319ad-3078">ID</span></span>
- <span data-ttu-id="319ad-3079">Identificateur</span><span class="sxs-lookup"><span data-stu-id="319ad-3079">Identification</span></span> 
   
## <a name="south-korea-resident-registration-number"></a><span data-ttu-id="319ad-3080">Matricule de résident Corée du Sud</span><span class="sxs-lookup"><span data-stu-id="319ad-3080">South Korea Resident Registration Number</span></span>

### <a name="format"></a><span data-ttu-id="319ad-3081">Format</span><span class="sxs-lookup"><span data-stu-id="319ad-3081">Format</span></span>

<span data-ttu-id="319ad-3082">13 chiffres contenant un trait d’union</span><span class="sxs-lookup"><span data-stu-id="319ad-3082">13 digits containing a hyphen</span></span>

### <a name="pattern"></a><span data-ttu-id="319ad-3083">Modèle</span><span class="sxs-lookup"><span data-stu-id="319ad-3083">Pattern</span></span>

<span data-ttu-id="319ad-3084">13 chiffres :</span><span class="sxs-lookup"><span data-stu-id="319ad-3084">13 digits:</span></span>
- <span data-ttu-id="319ad-3085">Six chiffres au format AAMMJJ correspondant à la date de naissance </span><span class="sxs-lookup"><span data-stu-id="319ad-3085">Six digits in the format YYMMDD which are the date of birth</span></span> 
- <span data-ttu-id="319ad-3086">Un trait d’union </span><span class="sxs-lookup"><span data-stu-id="319ad-3086">A hyphen</span></span> 
- <span data-ttu-id="319ad-3087">Un chiffre déterminé par le siècle et le sexe </span><span class="sxs-lookup"><span data-stu-id="319ad-3087">One digit determined by the century and gender</span></span> 
- <span data-ttu-id="319ad-3088">Code à quatre chiffres désignant la région de naissance </span><span class="sxs-lookup"><span data-stu-id="319ad-3088">Four-digit region-of-birth code</span></span> 
- <span data-ttu-id="319ad-3089">Un chiffre utilisé pour différencier les personnes dont les chiffres précédents sont identiques. </span><span class="sxs-lookup"><span data-stu-id="319ad-3089">One digit used to differentiate people for whom the preceding numbers are identical</span></span> 
- <span data-ttu-id="319ad-3090">Un chiffre de contrôle.</span><span class="sxs-lookup"><span data-stu-id="319ad-3090">A check digit.</span></span>

### <a name="checksum"></a><span data-ttu-id="319ad-3091">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="319ad-3091">Checksum</span></span>

<span data-ttu-id="319ad-3092">Oui</span><span class="sxs-lookup"><span data-stu-id="319ad-3092">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="319ad-3093">Définition</span><span class="sxs-lookup"><span data-stu-id="319ad-3093">Definition</span></span>

<span data-ttu-id="319ad-3094">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="319ad-3094">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="319ad-3095">La fonction Func_south_korea_resident_number trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="319ad-3095">The function Func_south_korea_resident_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="319ad-3096">Un mot clé figurant dans la liste Keyword_south_korea_resident_number est trouvé.</span><span class="sxs-lookup"><span data-stu-id="319ad-3096">A keyword from Keyword_south_korea_resident_number is found.</span></span>
- <span data-ttu-id="319ad-3097">La somme de contrôle est correcte.</span><span class="sxs-lookup"><span data-stu-id="319ad-3097">The checksum passes.</span></span>

<span data-ttu-id="319ad-3098">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="319ad-3098">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="319ad-3099">La fonction Func_south_korea_resident_number trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="319ad-3099">The function Func_south_korea_resident_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="319ad-3100">La somme de contrôle est correcte.</span><span class="sxs-lookup"><span data-stu-id="319ad-3100">The checksum passes.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="319ad-3101">Mots-clés</span><span class="sxs-lookup"><span data-stu-id="319ad-3101">Keywords</span></span>
   
#### <a name="keyword_south_korea_resident_number"></a><span data-ttu-id="319ad-3102">Keyword_south_korea_resident_number</span><span class="sxs-lookup"><span data-stu-id="319ad-3102">Keyword_south_korea_resident_number</span></span>

- <span data-ttu-id="319ad-3103">National ID card</span><span class="sxs-lookup"><span data-stu-id="319ad-3103">National ID card</span></span> 
- <span data-ttu-id="319ad-3104">Citizen’s Registration Number</span><span class="sxs-lookup"><span data-stu-id="319ad-3104">Citizen's Registration Number</span></span> 
- <span data-ttu-id="319ad-3105">Jumin deungnok beonho</span><span class="sxs-lookup"><span data-stu-id="319ad-3105">Jumin deungnok beonho</span></span> 
- <span data-ttu-id="319ad-3106">RRN</span><span class="sxs-lookup"><span data-stu-id="319ad-3106">RRN</span></span> 
- <span data-ttu-id="319ad-3107">주민등록번호</span><span class="sxs-lookup"><span data-stu-id="319ad-3107">주민등록번호</span></span>
   
## <a name="spain-social-security-number-ssn"></a><span data-ttu-id="319ad-3108">Numéro de sécurité sociale Espagne</span><span class="sxs-lookup"><span data-stu-id="319ad-3108">Spain Social Security Number (SSN)</span></span>

### <a name="format"></a><span data-ttu-id="319ad-3109">Format</span><span class="sxs-lookup"><span data-stu-id="319ad-3109">Format</span></span>

<span data-ttu-id="319ad-3110">11 à 12 chiffres</span><span class="sxs-lookup"><span data-stu-id="319ad-3110">11-12 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="319ad-3111">Modèle</span><span class="sxs-lookup"><span data-stu-id="319ad-3111">Pattern</span></span>

<span data-ttu-id="319ad-3112">11-12 chiffres :</span><span class="sxs-lookup"><span data-stu-id="319ad-3112">11-12 digits:</span></span>
- <span data-ttu-id="319ad-3113">Deux chiffres</span><span class="sxs-lookup"><span data-stu-id="319ad-3113">Two digits</span></span> 
- <span data-ttu-id="319ad-3114">Une barre oblique (facultative)</span><span class="sxs-lookup"><span data-stu-id="319ad-3114">A forward slash (optional)</span></span> 
- <span data-ttu-id="319ad-3115">7 à 8 chiffres</span><span class="sxs-lookup"><span data-stu-id="319ad-3115">7-8 digits</span></span> 
- <span data-ttu-id="319ad-3116">Une barre oblique (facultative)</span><span class="sxs-lookup"><span data-stu-id="319ad-3116">A forward slash (optional)</span></span> 
- <span data-ttu-id="319ad-3117">Deux chiffres</span><span class="sxs-lookup"><span data-stu-id="319ad-3117">Two digits</span></span>

### <a name="checksum"></a><span data-ttu-id="319ad-3118">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="319ad-3118">Checksum</span></span>

<span data-ttu-id="319ad-3119">Oui</span><span class="sxs-lookup"><span data-stu-id="319ad-3119">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="319ad-3120">Définition</span><span class="sxs-lookup"><span data-stu-id="319ad-3120">Definition</span></span>

<span data-ttu-id="319ad-3121">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="319ad-3121">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="319ad-3122">La fonction Func_spanish_social_security_number trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="319ad-3122">The function Func_spanish_social_security_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="319ad-3123">La somme de contrôle est correcte.</span><span class="sxs-lookup"><span data-stu-id="319ad-3123">The checksum passes.</span></span>

```xml
<!-- Spain SSN -->
<Entity id="5df987c0-8eae-4bce-ace7-b316347f3070" patternsProximity="300" recommendedConfidence="85">
    <Pattern confidenceLevel="85">
        <IdMatch idRef="Func_spanish_social_security_number" />
    </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="319ad-3124">Mots-clés</span><span class="sxs-lookup"><span data-stu-id="319ad-3124">Keywords</span></span>

<span data-ttu-id="319ad-3125">Aucun</span><span class="sxs-lookup"><span data-stu-id="319ad-3125">None</span></span>

## <a name="sql-server-connection-string"></a><span data-ttu-id="319ad-3126">Chaîne de connexion SQL Server</span><span class="sxs-lookup"><span data-stu-id="319ad-3126">SQL Server Connection String</span></span>

### <a name="format"></a><span data-ttu-id="319ad-3127">Format</span><span class="sxs-lookup"><span data-stu-id="319ad-3127">Format</span></span>

<span data-ttu-id="319ad-3128">La chaîne « User ID », « User ID », « UID » ou « UserId » suivi des caractères et des chaînes décrits dans le modèle ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="319ad-3128">The string "User Id", "User ID", "uid", or "UserId" followed by the characters and strings outlined in the pattern below.</span></span>

### <a name="pattern"></a><span data-ttu-id="319ad-3129">Modèle</span><span class="sxs-lookup"><span data-stu-id="319ad-3129">Pattern</span></span>

- <span data-ttu-id="319ad-3130">La chaîne « User ID », « User ID », « UID » ou « UserId »</span><span class="sxs-lookup"><span data-stu-id="319ad-3130">The string "User Id", "User ID", "uid", or "UserId"</span></span>
- <span data-ttu-id="319ad-3131">N’importe quelle combinaison entre 1-200 majuscules ou minuscules, des chiffres, des symboles, des caractères spéciaux ou des espaces</span><span class="sxs-lookup"><span data-stu-id="319ad-3131">Any combination of between 1-200 lower- or uppercase letters, digits, symbols, special characters, or spaces</span></span>
- <span data-ttu-id="319ad-3132">La chaîne "password" ou "PWD" où "PWD" n’est pas précédé d’une lettre minuscule</span><span class="sxs-lookup"><span data-stu-id="319ad-3132">The string "Password" or "pwd" where "pwd" is not preceded by a lowercase letter</span></span>
- <span data-ttu-id="319ad-3133">Signe égal (=)</span><span class="sxs-lookup"><span data-stu-id="319ad-3133">An equal sign (=)</span></span>
- <span data-ttu-id="319ad-3134">Tout caractère qui n’est pas un signe dollar ($), un symbole de pourcentage (%), un symbole supérieur à (>), un symbole (@), un guillemet ("), un point-virgule (;), une accolade ouvrante ([) ou un crochet gauche ({)</span><span class="sxs-lookup"><span data-stu-id="319ad-3134">Any character that is not a dollar sign ($), percent symbol (%), greater than symbol (>), at symbol (@), quotation mark ("), semicolon (;), left brace ([), or left bracket ({)</span></span>
- <span data-ttu-id="319ad-3135">N’importe quelle combinaison de 7-128 caractères qui ne sont pas des points-virgules (;), barre oblique (/) ou guillemets (")</span><span class="sxs-lookup"><span data-stu-id="319ad-3135">Any combination of 7-128 characters that are not a semicolon (;), forward slash (/), or quotation mark (")</span></span>
- <span data-ttu-id="319ad-3136">Un point-virgule (;) ou guillemets (")</span><span class="sxs-lookup"><span data-stu-id="319ad-3136">A semicolon (;) or quotation mark (")</span></span>

### <a name="checksum"></a><span data-ttu-id="319ad-3137">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="319ad-3137">Checksum</span></span>

<span data-ttu-id="319ad-3138">Non</span><span class="sxs-lookup"><span data-stu-id="319ad-3138">No</span></span>

### <a name="definition"></a><span data-ttu-id="319ad-3139">Définition</span><span class="sxs-lookup"><span data-stu-id="319ad-3139">Definition</span></span>

<span data-ttu-id="319ad-3140">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="319ad-3140">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="319ad-3141">L’expression régulière CEP_Regex_SQLServerConnectionString trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="319ad-3141">The regular expression CEP_Regex_SQLServerConnectionString finds content that matches the pattern.</span></span>
- <span data-ttu-id="319ad-3142">Un mot clé depuis CEP_GlobalFilter **est introuvable** .</span><span class="sxs-lookup"><span data-stu-id="319ad-3142">A keyword from CEP_GlobalFilter is **not** found.</span></span>
- <span data-ttu-id="319ad-3143">L’expression régulière CEP_PasswordPlaceHolder ne trouve **pas** le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="319ad-3143">The regular expression CEP_PasswordPlaceHolder does **not** find content that matches the pattern.</span></span>
- <span data-ttu-id="319ad-3144">L’expression régulière CEP_CommonExampleKeywords ne trouve **pas** le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="319ad-3144">The regular expression CEP_CommonExampleKeywords does **not** find content that matches the pattern.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="319ad-3145">Mots-clés</span><span class="sxs-lookup"><span data-stu-id="319ad-3145">Keywords</span></span>

#### <a name="cep_globalfilter"></a><span data-ttu-id="319ad-3146">CEP_GlobalFilter</span><span class="sxs-lookup"><span data-stu-id="319ad-3146">CEP_GlobalFilter</span></span>

- <span data-ttu-id="319ad-3147">some-password</span><span class="sxs-lookup"><span data-stu-id="319ad-3147">some-password</span></span>
- <span data-ttu-id="319ad-3148">somepassword</span><span class="sxs-lookup"><span data-stu-id="319ad-3148">somepassword</span></span>
- <span data-ttu-id="319ad-3149">secretPassword</span><span class="sxs-lookup"><span data-stu-id="319ad-3149">secretPassword</span></span>
- <span data-ttu-id="319ad-3150">échantillonnage</span><span class="sxs-lookup"><span data-stu-id="319ad-3150">sample</span></span>

#### <a name="cep_passwordplaceholder"></a><span data-ttu-id="319ad-3151">CEP_PasswordPlaceHolder</span><span class="sxs-lookup"><span data-stu-id="319ad-3151">CEP_PasswordPlaceHolder</span></span>

<span data-ttu-id="319ad-3152">(Notez que techniquement, ce type d’informations sensibles identifie ces mots clés à l’aide d’une expression régulière, et non d’une liste de mots clés.)</span><span class="sxs-lookup"><span data-stu-id="319ad-3152">(Note that technically, this sensitive information type identifies these keywords by using a regular expression, not a keyword list.)</span></span>

- <span data-ttu-id="319ad-3153">Mot de passe ou mot de passe suivi par 0-2 espaces, un signe égal (=), 0-2 espaces et un astérisque (\*)--ou--</span><span class="sxs-lookup"><span data-stu-id="319ad-3153">Password or pwd followed by 0-2 spaces, an equal sign (=), 0-2 spaces, and an asterisk (\*) --OR--</span></span>
- <span data-ttu-id="319ad-3154">Mot de passe ou mot de passe suivi par :</span><span class="sxs-lookup"><span data-stu-id="319ad-3154">Password or pwd followed by:</span></span>
    - <span data-ttu-id="319ad-3155">Signe égal (=)</span><span class="sxs-lookup"><span data-stu-id="319ad-3155">Equal sign (=)</span></span>
    - <span data-ttu-id="319ad-3156">Symbole inférieur à (<)</span><span class="sxs-lookup"><span data-stu-id="319ad-3156">Less than symbol (<)</span></span>
    - <span data-ttu-id="319ad-3157">Toute combinaison de 1-200 caractères qui sont des lettres majuscules ou minuscules, des chiffres, un astérisque (\*), un tiret (-), un trait de soulignement (_) ou un espace blanc</span><span class="sxs-lookup"><span data-stu-id="319ad-3157">Any combination of 1-200 characters that are upper- or lowercase letters, digits, an asterisk (\*), hyphen (-), underline (_), or whitespace character</span></span>
    - <span data-ttu-id="319ad-3158">Symbole supérieur à (>)</span><span class="sxs-lookup"><span data-stu-id="319ad-3158">Greater than symbol (>)</span></span>

#### <a name="cep_commonexamplekeywords"></a><span data-ttu-id="319ad-3159">CEP_CommonExampleKeywords</span><span class="sxs-lookup"><span data-stu-id="319ad-3159">CEP_CommonExampleKeywords</span></span>

<span data-ttu-id="319ad-3160">(Notez que techniquement, ce type d’informations sensibles identifie ces mots clés à l’aide d’une expression régulière, et non d’une liste de mots clés.)</span><span class="sxs-lookup"><span data-stu-id="319ad-3160">(Note that technically, this sensitive information type identifies these keywords by using a regular expression, not a keyword list.)</span></span>

- <span data-ttu-id="319ad-3161">contoso</span><span class="sxs-lookup"><span data-stu-id="319ad-3161">contoso</span></span>
- <span data-ttu-id="319ad-3162">société</span><span class="sxs-lookup"><span data-stu-id="319ad-3162">fabrikam</span></span>
- <span data-ttu-id="319ad-3163">Northwind</span><span class="sxs-lookup"><span data-stu-id="319ad-3163">northwind</span></span>
- <span data-ttu-id="319ad-3164">immédiatement</span><span class="sxs-lookup"><span data-stu-id="319ad-3164">sandbox</span></span>
- <span data-ttu-id="319ad-3165">onebox</span><span class="sxs-lookup"><span data-stu-id="319ad-3165">onebox</span></span>
- <span data-ttu-id="319ad-3166">hôte</span><span class="sxs-lookup"><span data-stu-id="319ad-3166">localhost</span></span>
- <span data-ttu-id="319ad-3167">bouclage</span><span class="sxs-lookup"><span data-stu-id="319ad-3167">127.0.0.1</span></span>
- <span data-ttu-id="319ad-3168">testacs.</span><span class="sxs-lookup"><span data-stu-id="319ad-3168">testacs.</span></span><!--no-hyperlink--><span data-ttu-id="319ad-3169">com</span><span class="sxs-lookup"><span data-stu-id="319ad-3169">com</span></span>
- <span data-ttu-id="319ad-3170">s-int.</span><span class="sxs-lookup"><span data-stu-id="319ad-3170">s-int.</span></span><!--no-hyperlink--><span data-ttu-id="319ad-3171">NET</span><span class="sxs-lookup"><span data-stu-id="319ad-3171">net</span></span>

## <a name="sweden-national-id"></a><span data-ttu-id="319ad-3172">ID national Suède</span><span class="sxs-lookup"><span data-stu-id="319ad-3172">Sweden National ID</span></span>

### <a name="format"></a><span data-ttu-id="319ad-3173">Format</span><span class="sxs-lookup"><span data-stu-id="319ad-3173">Format</span></span>

<span data-ttu-id="319ad-3174">10 ou 12 chiffres et éventuellement un délimiteur</span><span class="sxs-lookup"><span data-stu-id="319ad-3174">10 or 12 digits and an optional delimiter</span></span>

### <a name="pattern"></a><span data-ttu-id="319ad-3175">Modèle</span><span class="sxs-lookup"><span data-stu-id="319ad-3175">Pattern</span></span>

<span data-ttu-id="319ad-3176">10 ou 12 chiffres et un délimiteur facultatif :</span><span class="sxs-lookup"><span data-stu-id="319ad-3176">10 or 12 digits and an optional delimiter:</span></span>
- <span data-ttu-id="319ad-3177">2 à 4 chiffres (facultatifs)</span><span class="sxs-lookup"><span data-stu-id="319ad-3177">2-4 digits (optional)</span></span> 
- <span data-ttu-id="319ad-3178">Six chiffres au format de date AAMMJJ</span><span class="sxs-lookup"><span data-stu-id="319ad-3178">Six digits in date format YYMMDD</span></span> 
- <span data-ttu-id="319ad-3179">Séparateur de « - » ou « + » (facultatif), plus</span><span class="sxs-lookup"><span data-stu-id="319ad-3179">Delimiter of "-" or "+" (optional), plus</span></span>
- <span data-ttu-id="319ad-3180">Quatre chiffres</span><span class="sxs-lookup"><span data-stu-id="319ad-3180">Four digits</span></span>

### <a name="checksum"></a><span data-ttu-id="319ad-3181">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="319ad-3181">Checksum</span></span>

<span data-ttu-id="319ad-3182">Oui</span><span class="sxs-lookup"><span data-stu-id="319ad-3182">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="319ad-3183">Définition</span><span class="sxs-lookup"><span data-stu-id="319ad-3183">Definition</span></span>

<span data-ttu-id="319ad-3184">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="319ad-3184">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="319ad-3185">La fonction Func_swedish_national_identifier trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="319ad-3185">The function Func_swedish_national_identifier finds content that matches the pattern.</span></span>
- <span data-ttu-id="319ad-3186">La somme de contrôle est correcte.</span><span class="sxs-lookup"><span data-stu-id="319ad-3186">The checksum passes.</span></span>

```xml
<!-- Sweden National ID -->
<Entity id="f69aaf40-79be-4fac-8f05-fd1910d272c8" patternsProximity="300" recommendedConfidence="85">
    <Pattern confidenceLevel="85">
        <IdMatch idRef="Func_swedish_national_identifier" />
    </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="319ad-3187">Mots-clés</span><span class="sxs-lookup"><span data-stu-id="319ad-3187">Keywords</span></span>

<span data-ttu-id="319ad-3188">Non</span><span class="sxs-lookup"><span data-stu-id="319ad-3188">No</span></span>
   
## <a name="sweden-passport-number"></a><span data-ttu-id="319ad-3189">Numéro de passeport Suède</span><span class="sxs-lookup"><span data-stu-id="319ad-3189">Sweden Passport Number</span></span>

### <a name="format"></a><span data-ttu-id="319ad-3190">Format</span><span class="sxs-lookup"><span data-stu-id="319ad-3190">Format</span></span>

<span data-ttu-id="319ad-3191">Huit chiffres</span><span class="sxs-lookup"><span data-stu-id="319ad-3191">Eight digits</span></span>

### <a name="pattern"></a><span data-ttu-id="319ad-3192">Modèle</span><span class="sxs-lookup"><span data-stu-id="319ad-3192">Pattern</span></span>

<span data-ttu-id="319ad-3193">Huit chiffres consécutifs</span><span class="sxs-lookup"><span data-stu-id="319ad-3193">Eight consecutive digits</span></span>

### <a name="checksum"></a><span data-ttu-id="319ad-3194">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="319ad-3194">Checksum</span></span>

<span data-ttu-id="319ad-3195">Non</span><span class="sxs-lookup"><span data-stu-id="319ad-3195">No</span></span>

### <a name="definition"></a><span data-ttu-id="319ad-3196">Définition</span><span class="sxs-lookup"><span data-stu-id="319ad-3196">Definition</span></span>

<span data-ttu-id="319ad-3197">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="319ad-3197">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="319ad-3198">L’expression régulière Regex_sweden_passport_number trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="319ad-3198">The regular expression Regex_sweden_passport_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="319ad-3199">L’une des affirmations suivantes est vraie :</span><span class="sxs-lookup"><span data-stu-id="319ad-3199">One of the following is true:</span></span>
    - <span data-ttu-id="319ad-3200">Un mot clé figurant dans la liste Keyword_passport est trouvé.</span><span class="sxs-lookup"><span data-stu-id="319ad-3200">A keyword from Keyword_passport is found.</span></span>
    - <span data-ttu-id="319ad-3201">Un mot clé figurant dans la liste Keyword_sweden_passport est trouvé.</span><span class="sxs-lookup"><span data-stu-id="319ad-3201">A keyword from Keyword_sweden_passport is found.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="319ad-3202">Mots-clés</span><span class="sxs-lookup"><span data-stu-id="319ad-3202">Keywords</span></span>
   
#### <a name="keyword_sweden_passport"></a><span data-ttu-id="319ad-3203">Keyword_sweden_passport</span><span class="sxs-lookup"><span data-stu-id="319ad-3203">Keyword_sweden_passport</span></span>

- <span data-ttu-id="319ad-3204">exigences en matière de visa</span><span class="sxs-lookup"><span data-stu-id="319ad-3204">visa requirements</span></span> 
- <span data-ttu-id="319ad-3205">Carte d’enregistrement d’une personne étrangère</span><span class="sxs-lookup"><span data-stu-id="319ad-3205">Alien Registration Card</span></span> 
- <span data-ttu-id="319ad-3206">Visas Schengen</span><span class="sxs-lookup"><span data-stu-id="319ad-3206">Schengen visas</span></span> 
- <span data-ttu-id="319ad-3207">Visa Schengen</span><span class="sxs-lookup"><span data-stu-id="319ad-3207">Schengen visa</span></span> 
- <span data-ttu-id="319ad-3208">Traitement du visa</span><span class="sxs-lookup"><span data-stu-id="319ad-3208">Visa Processing</span></span> 
- <span data-ttu-id="319ad-3209">Type de visa</span><span class="sxs-lookup"><span data-stu-id="319ad-3209">Visa Type</span></span> 
- <span data-ttu-id="319ad-3210">Entrée unique</span><span class="sxs-lookup"><span data-stu-id="319ad-3210">Single Entry</span></span> 
- <span data-ttu-id="319ad-3211">Entrée multiple</span><span class="sxs-lookup"><span data-stu-id="319ad-3211">Multiple Entry</span></span> 
- <span data-ttu-id="319ad-3212">Frais de traitement G3</span><span class="sxs-lookup"><span data-stu-id="319ad-3212">G3 Processing Fees</span></span> 

#### <a name="keyword_passport"></a><span data-ttu-id="319ad-3213">Keyword_passport</span><span class="sxs-lookup"><span data-stu-id="319ad-3213">Keyword_passport</span></span>

- <span data-ttu-id="319ad-3214">Numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="319ad-3214">Passport Number</span></span> 
- <span data-ttu-id="319ad-3215">N° de passeport</span><span class="sxs-lookup"><span data-stu-id="319ad-3215">Passport No</span></span> 
- <span data-ttu-id="319ad-3216"># Passeport</span><span class="sxs-lookup"><span data-stu-id="319ad-3216">Passport #</span></span> 
- <span data-ttu-id="319ad-3217">Tel #</span><span class="sxs-lookup"><span data-stu-id="319ad-3217">Passport#</span></span> 
- <span data-ttu-id="319ad-3218">PassportID</span><span class="sxs-lookup"><span data-stu-id="319ad-3218">PassportID</span></span> 
- <span data-ttu-id="319ad-3219">N ° passeport</span><span class="sxs-lookup"><span data-stu-id="319ad-3219">Passportno</span></span> 
- <span data-ttu-id="319ad-3220">passportnumber</span><span class="sxs-lookup"><span data-stu-id="319ad-3220">passportnumber</span></span> 
- <span data-ttu-id="319ad-3221">パスポート</span><span class="sxs-lookup"><span data-stu-id="319ad-3221">パスポート</span></span> 
- <span data-ttu-id="319ad-3222">パスポート番号</span><span class="sxs-lookup"><span data-stu-id="319ad-3222">パスポート番号</span></span> 
- <span data-ttu-id="319ad-3223">パスポートのNum</span><span class="sxs-lookup"><span data-stu-id="319ad-3223">パスポートのNum</span></span> 
- <span data-ttu-id="319ad-3224">パスポート＃</span><span class="sxs-lookup"><span data-stu-id="319ad-3224">パスポート＃</span></span> 
- <span data-ttu-id="319ad-3225">Numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="319ad-3225">Numéro de passeport</span></span> 
- <span data-ttu-id="319ad-3226">Passeport n°</span><span class="sxs-lookup"><span data-stu-id="319ad-3226">Passeport n °</span></span> 
- <span data-ttu-id="319ad-3227">Passeport numéro</span><span class="sxs-lookup"><span data-stu-id="319ad-3227">Passeport Non</span></span> 
- <span data-ttu-id="319ad-3228"># Passeport</span><span class="sxs-lookup"><span data-stu-id="319ad-3228">Passeport #</span></span> 
- <span data-ttu-id="319ad-3229">Passeport #</span><span class="sxs-lookup"><span data-stu-id="319ad-3229">Passeport#</span></span> 
- <span data-ttu-id="319ad-3230">PasseportNon</span><span class="sxs-lookup"><span data-stu-id="319ad-3230">PasseportNon</span></span> 
- <span data-ttu-id="319ad-3231">Passeportn °</span><span class="sxs-lookup"><span data-stu-id="319ad-3231">Passeportn °</span></span> 
   
## <a name="swift-code"></a><span data-ttu-id="319ad-3232">Code SWIFT</span><span class="sxs-lookup"><span data-stu-id="319ad-3232">SWIFT Code</span></span>

### <a name="format"></a><span data-ttu-id="319ad-3233">Format</span><span class="sxs-lookup"><span data-stu-id="319ad-3233">Format</span></span>

<span data-ttu-id="319ad-3234">Quatre lettres suivies de 5 à 31 lettres ou chiffres</span><span class="sxs-lookup"><span data-stu-id="319ad-3234">Four letters followed by 5-31 letters or digits</span></span>

### <a name="pattern"></a><span data-ttu-id="319ad-3235">Modèle</span><span class="sxs-lookup"><span data-stu-id="319ad-3235">Pattern</span></span>

<span data-ttu-id="319ad-3236">Quatre lettres suivies de 5 à 31 lettres ou chiffres :</span><span class="sxs-lookup"><span data-stu-id="319ad-3236">Four letters followed by 5-31 letters or digits:</span></span>
- <span data-ttu-id="319ad-3237">Code bancaire à quatre lettres (ne respectent pas la casse)</span><span class="sxs-lookup"><span data-stu-id="319ad-3237">Four-letter bank code (not case sensitive)</span></span> 
- <span data-ttu-id="319ad-3238">Un espace facultatif</span><span class="sxs-lookup"><span data-stu-id="319ad-3238">An optional space</span></span> 
- <span data-ttu-id="319ad-3239">4 à 28 lettres ou chiffres (numéro de compte bancaire de base (BBAN))</span><span class="sxs-lookup"><span data-stu-id="319ad-3239">4-28 letters or digits (the Basic Bank Account Number (BBAN))</span></span> 
- <span data-ttu-id="319ad-3240">Un espace facultatif</span><span class="sxs-lookup"><span data-stu-id="319ad-3240">An optional space</span></span> 
- <span data-ttu-id="319ad-3241">1 à 3 lettres ou chiffres (reste du BBAN)</span><span class="sxs-lookup"><span data-stu-id="319ad-3241">1-3 letters or digits (remainder of the BBAN)</span></span>

### <a name="checksum"></a><span data-ttu-id="319ad-3242">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="319ad-3242">Checksum</span></span>

<span data-ttu-id="319ad-3243">Non</span><span class="sxs-lookup"><span data-stu-id="319ad-3243">No</span></span>

### <a name="definition"></a><span data-ttu-id="319ad-3244">Définition</span><span class="sxs-lookup"><span data-stu-id="319ad-3244">Definition</span></span>

<span data-ttu-id="319ad-3245">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="319ad-3245">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="319ad-3246">L’expression régulière Regex_swift trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="319ad-3246">The regular expression Regex_swift finds content that matches the pattern.</span></span>
- <span data-ttu-id="319ad-3247">Un mot clé figurant dans la liste Keyword_swift est trouvé.</span><span class="sxs-lookup"><span data-stu-id="319ad-3247">A keyword from Keyword_swift is found.</span></span>

```xml
<Entity id="cb2ab58c-9cb8-4c81-baf8-a4e106791df4" patternsProximity="300" recommendedConfidence="75">
<Pattern confidenceLevel="75">
        <IdMatch idRef="Regex_swift" />
        <Match idRef="Keyword_swift" />
    </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="319ad-3248">Mots-clés</span><span class="sxs-lookup"><span data-stu-id="319ad-3248">Keywords</span></span>
   
#### <a name="keyword_swift"></a><span data-ttu-id="319ad-3249">Keyword_swift</span><span class="sxs-lookup"><span data-stu-id="319ad-3249">Keyword_swift</span></span>

- <span data-ttu-id="319ad-3250">organisation internationale de normalisation 9362</span><span class="sxs-lookup"><span data-stu-id="319ad-3250">international organization for standardization 9362</span></span> 
- <span data-ttu-id="319ad-3251">ISO 9362</span><span class="sxs-lookup"><span data-stu-id="319ad-3251">iso 9362</span></span> 
- <span data-ttu-id="319ad-3252">iso9362</span><span class="sxs-lookup"><span data-stu-id="319ad-3252">iso9362</span></span> 
- <span data-ttu-id="319ad-3253">rapide\#</span><span class="sxs-lookup"><span data-stu-id="319ad-3253">swift\#</span></span> 
- <span data-ttu-id="319ad-3254">swiftcode</span><span class="sxs-lookup"><span data-stu-id="319ad-3254">swiftcode</span></span> 
- <span data-ttu-id="319ad-3255">swiftnumber</span><span class="sxs-lookup"><span data-stu-id="319ad-3255">swiftnumber</span></span> 
- <span data-ttu-id="319ad-3256">swiftroutingnumber</span><span class="sxs-lookup"><span data-stu-id="319ad-3256">swiftroutingnumber</span></span> 
- <span data-ttu-id="319ad-3257">code swift</span><span class="sxs-lookup"><span data-stu-id="319ad-3257">swift code</span></span> 
- <span data-ttu-id="319ad-3258"># numéro swift</span><span class="sxs-lookup"><span data-stu-id="319ad-3258">swift number #</span></span> 
- <span data-ttu-id="319ad-3259">numéro d’acheminement swift</span><span class="sxs-lookup"><span data-stu-id="319ad-3259">swift routing number</span></span> 
- <span data-ttu-id="319ad-3260">numéro BIC</span><span class="sxs-lookup"><span data-stu-id="319ad-3260">bic number</span></span> 
- <span data-ttu-id="319ad-3261">code BIC</span><span class="sxs-lookup"><span data-stu-id="319ad-3261">bic code</span></span> 
- <span data-ttu-id="319ad-3262">BIC\#</span><span class="sxs-lookup"><span data-stu-id="319ad-3262">bic \#</span></span> 
- <span data-ttu-id="319ad-3263">BIC\#</span><span class="sxs-lookup"><span data-stu-id="319ad-3263">bic\#</span></span> 
- <span data-ttu-id="319ad-3264">code d’identification bancaire</span><span class="sxs-lookup"><span data-stu-id="319ad-3264">bank identifier code</span></span> 
- <span data-ttu-id="319ad-3265">標準化 9362</span><span class="sxs-lookup"><span data-stu-id="319ad-3265">標準化9362</span></span> 
- <span data-ttu-id="319ad-3266">迅速＃</span><span class="sxs-lookup"><span data-stu-id="319ad-3266">迅速＃</span></span> 
- <span data-ttu-id="319ad-3267">SWIFTコード</span><span class="sxs-lookup"><span data-stu-id="319ad-3267">SWIFTコード</span></span> 
- <span data-ttu-id="319ad-3268">SWIFT番号</span><span class="sxs-lookup"><span data-stu-id="319ad-3268">SWIFT番号</span></span> 
- <span data-ttu-id="319ad-3269">迅速なルーティング番号</span><span class="sxs-lookup"><span data-stu-id="319ad-3269">迅速なルーティング番号</span></span> 
- <span data-ttu-id="319ad-3270">BIC番号</span><span class="sxs-lookup"><span data-stu-id="319ad-3270">BIC番号</span></span> 
- <span data-ttu-id="319ad-3271">BICコード</span><span class="sxs-lookup"><span data-stu-id="319ad-3271">BICコード</span></span> 
- <span data-ttu-id="319ad-3272">銀行識別コードのための国際組織</span><span class="sxs-lookup"><span data-stu-id="319ad-3272">銀行識別コードのための国際組織</span></span> 
- <span data-ttu-id="319ad-3273">Organisation internationale de normalisation 9362</span><span class="sxs-lookup"><span data-stu-id="319ad-3273">Organisation internationale de normalisation 9362</span></span> 
- <span data-ttu-id="319ad-3274">rapide\#</span><span class="sxs-lookup"><span data-stu-id="319ad-3274">rapide \#</span></span> 
- <span data-ttu-id="319ad-3275">code SWIFT</span><span class="sxs-lookup"><span data-stu-id="319ad-3275">code SWIFT</span></span> 
- <span data-ttu-id="319ad-3276">le numéro de swift</span><span class="sxs-lookup"><span data-stu-id="319ad-3276">le numéro de swift</span></span> 
- <span data-ttu-id="319ad-3277">swift numéro d’acheminement</span><span class="sxs-lookup"><span data-stu-id="319ad-3277">swift numéro d'acheminement</span></span> 
- <span data-ttu-id="319ad-3278">le numéro BIC</span><span class="sxs-lookup"><span data-stu-id="319ad-3278">le numéro BIC</span></span> 
- <span data-ttu-id="319ad-3279">\#BIC</span><span class="sxs-lookup"><span data-stu-id="319ad-3279">\# BIC</span></span> 
- <span data-ttu-id="319ad-3280">code identificateur de banque</span><span class="sxs-lookup"><span data-stu-id="319ad-3280">code identificateur de banque</span></span> 
   
## <a name="taiwan-national-id"></a><span data-ttu-id="319ad-3281">ID national à Taïwan</span><span class="sxs-lookup"><span data-stu-id="319ad-3281">Taiwan National ID</span></span>

### <a name="format"></a><span data-ttu-id="319ad-3282">Format</span><span class="sxs-lookup"><span data-stu-id="319ad-3282">Format</span></span>

<span data-ttu-id="319ad-3283">Une lettre  suivie de neuf chiffres</span><span class="sxs-lookup"><span data-stu-id="319ad-3283">One letter (in English) followed by nine digits</span></span>

### <a name="pattern"></a><span data-ttu-id="319ad-3284">Modèle</span><span class="sxs-lookup"><span data-stu-id="319ad-3284">Pattern</span></span>

<span data-ttu-id="319ad-3285">Une lettre suivie de neuf chiffres :</span><span class="sxs-lookup"><span data-stu-id="319ad-3285">One letter (in English) followed by nine digits:</span></span>
- <span data-ttu-id="319ad-3286">Une lettre (en anglais, ne respecte pas la casse)</span><span class="sxs-lookup"><span data-stu-id="319ad-3286">One letter (in English, not case sensitive)</span></span> 
- <span data-ttu-id="319ad-3287">Le chiffre « 1 » ou « 2 »</span><span class="sxs-lookup"><span data-stu-id="319ad-3287">The digit "1" or "2"</span></span> 
- <span data-ttu-id="319ad-3288">Huit chiffres</span><span class="sxs-lookup"><span data-stu-id="319ad-3288">Eight digits</span></span>

### <a name="checksum"></a><span data-ttu-id="319ad-3289">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="319ad-3289">Checksum</span></span>

<span data-ttu-id="319ad-3290">Oui</span><span class="sxs-lookup"><span data-stu-id="319ad-3290">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="319ad-3291">Définition</span><span class="sxs-lookup"><span data-stu-id="319ad-3291">Definition</span></span>

<span data-ttu-id="319ad-3292">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="319ad-3292">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="319ad-3293">La fonction Func_taiwanese_national_id trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="319ad-3293">The function Func_taiwanese_national_id finds content that matches the pattern.</span></span>
- <span data-ttu-id="319ad-3294">Un mot clé figurant dans la liste Keyword_taiwanese_national_id est trouvé.</span><span class="sxs-lookup"><span data-stu-id="319ad-3294">A keyword from Keyword_taiwanese_national_id is found.</span></span>
- <span data-ttu-id="319ad-3295">La somme de contrôle est correcte.</span><span class="sxs-lookup"><span data-stu-id="319ad-3295">The checksum passes.</span></span>

```xml
<!-- Taiwanese National ID -->
<Entity id="4C7BFC34-8DD1-421D-8FB7-6C6182C2AF03" patternsProximity="300" recommendedConfidence="85">
      <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_taiwanese_national_id" />
          <Match idRef="Keyword_taiwanese_national_id" />
      </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="319ad-3296">Mots-clés</span><span class="sxs-lookup"><span data-stu-id="319ad-3296">Keywords</span></span>

#### <a name="keyword_taiwanese_national_id"></a><span data-ttu-id="319ad-3297">Keyword_taiwanese_national_id</span><span class="sxs-lookup"><span data-stu-id="319ad-3297">Keyword_taiwanese_national_id</span></span>

- <span data-ttu-id="319ad-3298">身份證字號</span><span class="sxs-lookup"><span data-stu-id="319ad-3298">身份證字號</span></span> 
- <span data-ttu-id="319ad-3299">身份證</span><span class="sxs-lookup"><span data-stu-id="319ad-3299">身份證</span></span> 
- <span data-ttu-id="319ad-3300">身份證號碼</span><span class="sxs-lookup"><span data-stu-id="319ad-3300">身份證號碼</span></span> 
- <span data-ttu-id="319ad-3301">身份證號</span><span class="sxs-lookup"><span data-stu-id="319ad-3301">身份證號</span></span> 
- <span data-ttu-id="319ad-3302">身分證字號</span><span class="sxs-lookup"><span data-stu-id="319ad-3302">身分證字號</span></span> 
- <span data-ttu-id="319ad-3303">身分證</span><span class="sxs-lookup"><span data-stu-id="319ad-3303">身分證</span></span> 
- <span data-ttu-id="319ad-3304">身分證號碼</span><span class="sxs-lookup"><span data-stu-id="319ad-3304">身分證號碼</span></span> 
- <span data-ttu-id="319ad-3305">身份證號</span><span class="sxs-lookup"><span data-stu-id="319ad-3305">身份證號</span></span> 
- <span data-ttu-id="319ad-3306">身分證統一編號</span><span class="sxs-lookup"><span data-stu-id="319ad-3306">身分證統一編號</span></span> 
- <span data-ttu-id="319ad-3307">國民身分證統一編號</span><span class="sxs-lookup"><span data-stu-id="319ad-3307">國民身分證統一編號</span></span> 
- <span data-ttu-id="319ad-3308">簽名</span><span class="sxs-lookup"><span data-stu-id="319ad-3308">簽名</span></span> 
- <span data-ttu-id="319ad-3309">蓋章</span><span class="sxs-lookup"><span data-stu-id="319ad-3309">蓋章</span></span> 
- <span data-ttu-id="319ad-3310">簽名或蓋章</span><span class="sxs-lookup"><span data-stu-id="319ad-3310">簽名或蓋章</span></span> 
- <span data-ttu-id="319ad-3311">簽章</span><span class="sxs-lookup"><span data-stu-id="319ad-3311">簽章</span></span>   
   
## <a name="taiwan-passport-number"></a><span data-ttu-id="319ad-3312">	Numéro de passeport Taïwan</span><span class="sxs-lookup"><span data-stu-id="319ad-3312">Taiwan Passport Number</span></span>

### <a name="format"></a><span data-ttu-id="319ad-3313">Format</span><span class="sxs-lookup"><span data-stu-id="319ad-3313">Format</span></span>

- <span data-ttu-id="319ad-3314">Numéro de passeport biométrique : neuf chiffres</span><span class="sxs-lookup"><span data-stu-id="319ad-3314">Biometric passport number: Nine digits</span></span>
- <span data-ttu-id="319ad-3315">Numéro de passeport non biométrique : neuf chiffres</span><span class="sxs-lookup"><span data-stu-id="319ad-3315">Non-biometric passport number: Nine digits</span></span>

### <a name="pattern"></a><span data-ttu-id="319ad-3316">Modèle</span><span class="sxs-lookup"><span data-stu-id="319ad-3316">Pattern</span></span>
<span data-ttu-id="319ad-3317">Numéro de passeport biométrique :</span><span class="sxs-lookup"><span data-stu-id="319ad-3317">Biometric passport number:</span></span>
- <span data-ttu-id="319ad-3318">Le chiffre « 3 » </span><span class="sxs-lookup"><span data-stu-id="319ad-3318">The digit "3"</span></span> 
- <span data-ttu-id="319ad-3319">Huit chiffres</span><span class="sxs-lookup"><span data-stu-id="319ad-3319">Eight digits</span></span>

<span data-ttu-id="319ad-3320">Numéro de passeport non biométrique :</span><span class="sxs-lookup"><span data-stu-id="319ad-3320">Non-biometric passport number:</span></span>
- <span data-ttu-id="319ad-3321">Neuf chiffres</span><span class="sxs-lookup"><span data-stu-id="319ad-3321">Nine digits</span></span>

### <a name="checksum"></a><span data-ttu-id="319ad-3322">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="319ad-3322">Checksum</span></span>

<span data-ttu-id="319ad-3323">Non</span><span class="sxs-lookup"><span data-stu-id="319ad-3323">No</span></span>

### <a name="definition"></a><span data-ttu-id="319ad-3324">Définition</span><span class="sxs-lookup"><span data-stu-id="319ad-3324">Definition</span></span>

<span data-ttu-id="319ad-3325">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="319ad-3325">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="319ad-3326">L’expression régulière Regex_taiwan_passport trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="319ad-3326">The regular expression Regex_taiwan_passport finds content that matches the pattern.</span></span>
- <span data-ttu-id="319ad-3327">Un mot clé figurant dans la liste Keyword_taiwan_passport est trouvé.</span><span class="sxs-lookup"><span data-stu-id="319ad-3327">A keyword from Keyword_taiwan_passport is found.</span></span>

```xml
<!-- Taiwan Passport Number -->
<Entity id="e7251cb4-4c2c-41df-963e-924eb3dae04a" recommendedConfidence="75" patternsProximity="300">
  <Pattern confidenceLevel="75">
     <IdMatch idRef="Regex_taiwan_passport"/>
     <Match idRef="Keyword_taiwan_passport"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="319ad-3328">Mots-clés</span><span class="sxs-lookup"><span data-stu-id="319ad-3328">Keywords</span></span>

#### <a name="keyword_taiwan_passport"></a><span data-ttu-id="319ad-3329">Keyword_taiwan_passport</span><span class="sxs-lookup"><span data-stu-id="319ad-3329">Keyword_taiwan_passport</span></span>

- <span data-ttu-id="319ad-3330">ROC passport number</span><span class="sxs-lookup"><span data-stu-id="319ad-3330">ROC passport number</span></span> 
- <span data-ttu-id="319ad-3331">Passport number</span><span class="sxs-lookup"><span data-stu-id="319ad-3331">Passport number</span></span> 
- <span data-ttu-id="319ad-3332">Passport no</span><span class="sxs-lookup"><span data-stu-id="319ad-3332">Passport no</span></span> 
- <span data-ttu-id="319ad-3333">Passport Num</span><span class="sxs-lookup"><span data-stu-id="319ad-3333">Passport Num</span></span> 
- <span data-ttu-id="319ad-3334">Passport #</span><span class="sxs-lookup"><span data-stu-id="319ad-3334">Passport #</span></span> 
- <span data-ttu-id="319ad-3335">护照</span><span class="sxs-lookup"><span data-stu-id="319ad-3335">护照</span></span> 
- <span data-ttu-id="319ad-3336">中華民國護照</span><span class="sxs-lookup"><span data-stu-id="319ad-3336">中華民國護照</span></span> 
- <span data-ttu-id="319ad-3337">Zhōnghuá Mínguó hùzhào</span><span class="sxs-lookup"><span data-stu-id="319ad-3337">Zhōnghuá Mínguó hùzhào</span></span>
   
## <a name="taiwan-resident-certificate-arctarc-number"></a><span data-ttu-id="319ad-3338">Numéro de certificat de résident (ARC/TARC) Taïwan</span><span class="sxs-lookup"><span data-stu-id="319ad-3338">Taiwan Resident Certificate (ARC/TARC) Number</span></span>

### <a name="format"></a><span data-ttu-id="319ad-3339">Format</span><span class="sxs-lookup"><span data-stu-id="319ad-3339">Format</span></span>

<span data-ttu-id="319ad-3340">10 lettres et chiffres</span><span class="sxs-lookup"><span data-stu-id="319ad-3340">10 letters and digits</span></span>

### <a name="pattern"></a><span data-ttu-id="319ad-3341">Modèle</span><span class="sxs-lookup"><span data-stu-id="319ad-3341">Pattern</span></span>

<span data-ttu-id="319ad-3342">10 lettres et chiffres :</span><span class="sxs-lookup"><span data-stu-id="319ad-3342">10 letters and digits:</span></span>
- <span data-ttu-id="319ad-3343">Deux lettres (ne respectant pas la casse) </span><span class="sxs-lookup"><span data-stu-id="319ad-3343">Two letters (not case sensitive)</span></span> 
- <span data-ttu-id="319ad-3344">Huit chiffres</span><span class="sxs-lookup"><span data-stu-id="319ad-3344">Eight digits</span></span>

### <a name="checksum"></a><span data-ttu-id="319ad-3345">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="319ad-3345">Checksum</span></span>

<span data-ttu-id="319ad-3346">Non</span><span class="sxs-lookup"><span data-stu-id="319ad-3346">No</span></span>

### <a name="definition"></a><span data-ttu-id="319ad-3347">Définition</span><span class="sxs-lookup"><span data-stu-id="319ad-3347">Definition</span></span>

<span data-ttu-id="319ad-3348">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="319ad-3348">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="319ad-3349">L’expression régulière Regex_taiwan_resident_certificate trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="319ad-3349">The regular expression Regex_taiwan_resident_certificate finds content that matches the pattern.</span></span>
- <span data-ttu-id="319ad-3350">Un mot clé figurant dans la liste Keyword_taiwan_resident_certificate est trouvé.</span><span class="sxs-lookup"><span data-stu-id="319ad-3350">A keyword from Keyword_taiwan_resident_certificate is found.</span></span>

```xml
<!-- Taiwan Resident Certificate (ARC/TARC) -->
<Entity id="48269fec-05ea-46ea-b326-f5623a58c6e9" recommendedConfidence="75" patternsProximity="300">
  <Pattern confidenceLevel="75">
     <IdMatch idRef="Regex_taiwan_resident_certificate"/>
     <Match idRef="Keyword_taiwan_resident_certificate"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="319ad-3351">Mots-clés</span><span class="sxs-lookup"><span data-stu-id="319ad-3351">Keywords</span></span>

#### <a name="keyword_taiwan_resident_certificate"></a><span data-ttu-id="319ad-3352">Keyword_taiwan_resident_certificate</span><span class="sxs-lookup"><span data-stu-id="319ad-3352">Keyword_taiwan_resident_certificate</span></span>

- <span data-ttu-id="319ad-3353">Resident Certificate</span><span class="sxs-lookup"><span data-stu-id="319ad-3353">Resident Certificate</span></span> 
- <span data-ttu-id="319ad-3354">Resident Cert</span><span class="sxs-lookup"><span data-stu-id="319ad-3354">Resident Cert</span></span> 
- <span data-ttu-id="319ad-3355">Resident Cert.</span><span class="sxs-lookup"><span data-stu-id="319ad-3355">Resident Cert.</span></span> 
- <span data-ttu-id="319ad-3356">Identification card</span><span class="sxs-lookup"><span data-stu-id="319ad-3356">Identification card</span></span> 
- <span data-ttu-id="319ad-3357">Alien Resident Certificate</span><span class="sxs-lookup"><span data-stu-id="319ad-3357">Alien Resident Certificate</span></span> 
- <span data-ttu-id="319ad-3358">ARC</span><span class="sxs-lookup"><span data-stu-id="319ad-3358">ARC</span></span> 
- <span data-ttu-id="319ad-3359">Taiwan Area Resident Certificate</span><span class="sxs-lookup"><span data-stu-id="319ad-3359">Taiwan Area Resident Certificate</span></span> 
- <span data-ttu-id="319ad-3360">TARC</span><span class="sxs-lookup"><span data-stu-id="319ad-3360">TARC</span></span> 
- <span data-ttu-id="319ad-3361">居留證</span><span class="sxs-lookup"><span data-stu-id="319ad-3361">居留證</span></span> 
- <span data-ttu-id="319ad-3362">外僑居留證</span><span class="sxs-lookup"><span data-stu-id="319ad-3362">外僑居留證</span></span> 
- <span data-ttu-id="319ad-3363">台灣地區居留證</span><span class="sxs-lookup"><span data-stu-id="319ad-3363">台灣地區居留證</span></span> 

## <a name="thai-population-identification-code"></a><span data-ttu-id="319ad-3364">Code d’identification du remplissage thaï</span><span class="sxs-lookup"><span data-stu-id="319ad-3364">Thai Population Identification Code</span></span>

### <a name="format"></a><span data-ttu-id="319ad-3365">Format</span><span class="sxs-lookup"><span data-stu-id="319ad-3365">Format</span></span>

<span data-ttu-id="319ad-3366">13 chiffres</span><span class="sxs-lookup"><span data-stu-id="319ad-3366">13 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="319ad-3367">Modèle</span><span class="sxs-lookup"><span data-stu-id="319ad-3367">Pattern</span></span>

<span data-ttu-id="319ad-3368">13 chiffres :</span><span class="sxs-lookup"><span data-stu-id="319ad-3368">13 digits:</span></span>
- <span data-ttu-id="319ad-3369">Le premier chiffre est différent de 0 ou de 9</span><span class="sxs-lookup"><span data-stu-id="319ad-3369">First digit is not 0 or 9</span></span> 
- <span data-ttu-id="319ad-3370">12 chiffres</span><span class="sxs-lookup"><span data-stu-id="319ad-3370">12 digits</span></span>

### <a name="checksum"></a><span data-ttu-id="319ad-3371">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="319ad-3371">Checksum</span></span>

<span data-ttu-id="319ad-3372">Oui</span><span class="sxs-lookup"><span data-stu-id="319ad-3372">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="319ad-3373">Définition</span><span class="sxs-lookup"><span data-stu-id="319ad-3373">Definition</span></span>

<span data-ttu-id="319ad-3374">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="319ad-3374">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="319ad-3375">La fonction Func_Thai_Citizen_Id trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="319ad-3375">The function Func_Thai_Citizen_Id finds content that matches the pattern.</span></span>
- <span data-ttu-id="319ad-3376">Un mot clé depuis Keyword_Thai_Citizen_Id est trouvé.</span><span class="sxs-lookup"><span data-stu-id="319ad-3376">A keyword from Keyword_Thai_Citizen_Id is found.</span></span>

<span data-ttu-id="319ad-3377">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="319ad-3377">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="319ad-3378">La fonction Func_Thai_Citizen_Id trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="319ad-3378">The function Func_Thai_Citizen_Id finds content that matches the pattern.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="319ad-3379">Mots-clés</span><span class="sxs-lookup"><span data-stu-id="319ad-3379">Keywords</span></span>

#### <a name="keyword_thai_citizen_id"></a><span data-ttu-id="319ad-3380">Keyword_Thai_Citizen_Id</span><span class="sxs-lookup"><span data-stu-id="319ad-3380">Keyword_Thai_Citizen_Id</span></span>

- <span data-ttu-id="319ad-3381">ID Number</span><span class="sxs-lookup"><span data-stu-id="319ad-3381">ID Number</span></span>
- <span data-ttu-id="319ad-3382">Numéro d’identification</span><span class="sxs-lookup"><span data-stu-id="319ad-3382">Identification Number</span></span>
- <span data-ttu-id="319ad-3383">บัตรประชาชน</span><span class="sxs-lookup"><span data-stu-id="319ad-3383">บัตรประชาชน</span></span>
- <span data-ttu-id="319ad-3384">รหัสบัตรประชาชน</span><span class="sxs-lookup"><span data-stu-id="319ad-3384">รหัสบัตรประชาชน</span></span>
- <span data-ttu-id="319ad-3385">บัตรประชาชน</span><span class="sxs-lookup"><span data-stu-id="319ad-3385">บัตรประชาชน</span></span>
- <span data-ttu-id="319ad-3386">รหัสบัตรประชาชน</span><span class="sxs-lookup"><span data-stu-id="319ad-3386">รหัสบัตรประชาชน</span></span>
  
## <a name="turkish-national-identification-number"></a><span data-ttu-id="319ad-3387">Numéro d’identification national turc</span><span class="sxs-lookup"><span data-stu-id="319ad-3387">Turkish National Identification Number</span></span>

### <a name="format"></a><span data-ttu-id="319ad-3388">Format</span><span class="sxs-lookup"><span data-stu-id="319ad-3388">Format</span></span>

<span data-ttu-id="319ad-3389">11 chiffres</span><span class="sxs-lookup"><span data-stu-id="319ad-3389">11 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="319ad-3390">Modèle</span><span class="sxs-lookup"><span data-stu-id="319ad-3390">Pattern</span></span>

<span data-ttu-id="319ad-3391">11 chiffres</span><span class="sxs-lookup"><span data-stu-id="319ad-3391">11 digits</span></span>

### <a name="checksum"></a><span data-ttu-id="319ad-3392">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="319ad-3392">Checksum</span></span>

<span data-ttu-id="319ad-3393">Oui</span><span class="sxs-lookup"><span data-stu-id="319ad-3393">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="319ad-3394">Définition</span><span class="sxs-lookup"><span data-stu-id="319ad-3394">Definition</span></span>

<span data-ttu-id="319ad-3395">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="319ad-3395">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="319ad-3396">La fonction Func_Turkish_National_Id trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="319ad-3396">The function Func_Turkish_National_Id finds content that matches the pattern.</span></span>
- <span data-ttu-id="319ad-3397">Un mot clé depuis Keyword_Turkish_National_Id est trouvé.</span><span class="sxs-lookup"><span data-stu-id="319ad-3397">A keyword from Keyword_Turkish_National_Id is found.</span></span>

<span data-ttu-id="319ad-3398">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="319ad-3398">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="319ad-3399">La fonction Func_Turkish_National_Id trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="319ad-3399">The function Func_Turkish_National_Id finds content that matches the pattern.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="319ad-3400">Mots-clés</span><span class="sxs-lookup"><span data-stu-id="319ad-3400">Keywords</span></span>

#### <a name="keyword_turkish_national_id"></a><span data-ttu-id="319ad-3401">Keyword_Turkish_National_Id</span><span class="sxs-lookup"><span data-stu-id="319ad-3401">Keyword_Turkish_National_Id</span></span>

- <span data-ttu-id="319ad-3402">TC Kimlik non</span><span class="sxs-lookup"><span data-stu-id="319ad-3402">TC Kimlik No</span></span>
- <span data-ttu-id="319ad-3403">TC Kimlik numarası</span><span class="sxs-lookup"><span data-stu-id="319ad-3403">TC Kimlik numarası</span></span>
- <span data-ttu-id="319ad-3404">Vatandaşlık numarası</span><span class="sxs-lookup"><span data-stu-id="319ad-3404">Vatandaşlık numarası</span></span>
- <span data-ttu-id="319ad-3405">Vatandaşlık non</span><span class="sxs-lookup"><span data-stu-id="319ad-3405">Vatandaşlık no</span></span>

## <a name="uk-drivers-license-number"></a><span data-ttu-id="319ad-p144">Numéro de permis de conduire Royaume-Uni</span><span class="sxs-lookup"><span data-stu-id="319ad-p144">U.K. Driver's License Number</span></span>

### <a name="format"></a><span data-ttu-id="319ad-3408">Format</span><span class="sxs-lookup"><span data-stu-id="319ad-3408">Format</span></span>

<span data-ttu-id="319ad-3409">Combinaison de 18 lettres et chiffres au format spécifié</span><span class="sxs-lookup"><span data-stu-id="319ad-3409">Combination of 18 letters and digits in the specified format</span></span>

### <a name="pattern"></a><span data-ttu-id="319ad-3410">Modèle</span><span class="sxs-lookup"><span data-stu-id="319ad-3410">Pattern</span></span>

<span data-ttu-id="319ad-3411">18 lettres et chiffres</span><span class="sxs-lookup"><span data-stu-id="319ad-3411">18 letters and digits:</span></span>
- <span data-ttu-id="319ad-3412">Cinq lettres (ne respectent pas la casse) ou le chiffre « 9 » à la place d’une lettre</span><span class="sxs-lookup"><span data-stu-id="319ad-3412">Five letters (not case sensitive) or the digit "9" in place of a letter</span></span> 
- <span data-ttu-id="319ad-3413">Un chiffre</span><span class="sxs-lookup"><span data-stu-id="319ad-3413">One digit</span></span> 
- <span data-ttu-id="319ad-3414">Cinq chiffres au format de date MMDDY pour la date de naissance (7 caractères sont incrémentés de 50 si le pilote est femelle, c’est-à-dire 51 vers 62 au lieu de 01 à 12)</span><span class="sxs-lookup"><span data-stu-id="319ad-3414">Five digits in the date format MMDDY for date of birth (7th character is incremented by 50 if driver is female, i.e. 51 to 62 instead of 01 to 12)</span></span>
- <span data-ttu-id="319ad-3415">Deux lettres (ne respectent pas la casse) ou le chiffre « 9 » à la place d’une lettre</span><span class="sxs-lookup"><span data-stu-id="319ad-3415">Two letters (not case sensitive) or the digit "9" in place of a letter</span></span> 
- <span data-ttu-id="319ad-3416">Cinq chiffres</span><span class="sxs-lookup"><span data-stu-id="319ad-3416">Five digits</span></span>

### <a name="checksum"></a><span data-ttu-id="319ad-3417">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="319ad-3417">Checksum</span></span>

<span data-ttu-id="319ad-3418">Oui</span><span class="sxs-lookup"><span data-stu-id="319ad-3418">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="319ad-3419">Définition</span><span class="sxs-lookup"><span data-stu-id="319ad-3419">Definition</span></span>

<span data-ttu-id="319ad-3420">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="319ad-3420">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="319ad-3421">La fonction Func_uk_drivers_license trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="319ad-3421">The function Func_uk_drivers_license finds content that matches the pattern.</span></span>
- <span data-ttu-id="319ad-3422">Un mot clé figurant dans la liste Keyword_uk_drivers_license est trouvé.</span><span class="sxs-lookup"><span data-stu-id="319ad-3422">A keyword from Keyword_uk_drivers_license is found.</span></span>
- <span data-ttu-id="319ad-3423">La somme de contrôle est correcte.</span><span class="sxs-lookup"><span data-stu-id="319ad-3423">The checksum passes.</span></span>

```xml
<!-- U.K. Driver's License Number -->
<Entity id="f93de4be-d94c-40df-a8be-461738047551" patternsProximity="300" recommendedConfidence="75">
    <Pattern confidenceLevel="75">
        <IdMatch idRef="Func_uk_drivers_license" />
        <Match idRef="Keyword_uk_drivers_license" />
    </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="319ad-3424">Mots-clés</span><span class="sxs-lookup"><span data-stu-id="319ad-3424">Keywords</span></span>

#### <a name="keyword_uk_drivers_license"></a><span data-ttu-id="319ad-3425">Keyword_uk_drivers_license</span><span class="sxs-lookup"><span data-stu-id="319ad-3425">Keyword_uk_drivers_license</span></span>

- <span data-ttu-id="319ad-3426">DVLA</span><span class="sxs-lookup"><span data-stu-id="319ad-3426">DVLA</span></span> 
- <span data-ttu-id="319ad-3427">véhicule utilitaire léger</span><span class="sxs-lookup"><span data-stu-id="319ad-3427">light vans</span></span> 
- <span data-ttu-id="319ad-3428">quadbikes</span><span class="sxs-lookup"><span data-stu-id="319ad-3428">quadbikes</span></span> 
- <span data-ttu-id="319ad-3429">automobiles</span><span class="sxs-lookup"><span data-stu-id="319ad-3429">motor cars</span></span> 
- <span data-ttu-id="319ad-3430">125cc</span><span class="sxs-lookup"><span data-stu-id="319ad-3430">125cc</span></span> 
- <span data-ttu-id="319ad-3431">annexes</span><span class="sxs-lookup"><span data-stu-id="319ad-3431">sidecar</span></span> 
- <span data-ttu-id="319ad-3432">tricycles</span><span class="sxs-lookup"><span data-stu-id="319ad-3432">tricycles</span></span> 
- <span data-ttu-id="319ad-3433">Side</span><span class="sxs-lookup"><span data-stu-id="319ad-3433">motorcycles</span></span> 
- <span data-ttu-id="319ad-3434">permis de conduire plastifié</span><span class="sxs-lookup"><span data-stu-id="319ad-3434">photocard licence</span></span> 
- <span data-ttu-id="319ad-3435">apprentis conducteurs</span><span class="sxs-lookup"><span data-stu-id="319ad-3435">learner drivers</span></span> 
- <span data-ttu-id="319ad-3436">titulaire du permis</span><span class="sxs-lookup"><span data-stu-id="319ad-3436">licence holder</span></span> 
- <span data-ttu-id="319ad-3437">titulaires du permis</span><span class="sxs-lookup"><span data-stu-id="319ad-3437">licence holders</span></span> 
- <span data-ttu-id="319ad-3438">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="319ad-3438">driving licences</span></span> 
- <span data-ttu-id="319ad-3439">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="319ad-3439">driving licence</span></span> 
- <span data-ttu-id="319ad-3440">voiture à double commande</span><span class="sxs-lookup"><span data-stu-id="319ad-3440">dual control car</span></span> 
   
## <a name="uk-electoral-roll-number"></a><span data-ttu-id="319ad-p145">Numéro de liste électorale Royaume-Uni</span><span class="sxs-lookup"><span data-stu-id="319ad-p145">U.K. Electoral Roll Number</span></span>

### <a name="format"></a><span data-ttu-id="319ad-3443">Format</span><span class="sxs-lookup"><span data-stu-id="319ad-3443">Format</span></span>

<span data-ttu-id="319ad-3444">Deux lettres suivies de 1 à 4 chiffres</span><span class="sxs-lookup"><span data-stu-id="319ad-3444">Two letters followed by 1-4 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="319ad-3445">Modèle</span><span class="sxs-lookup"><span data-stu-id="319ad-3445">Pattern</span></span>

<span data-ttu-id="319ad-3446">Deux lettres (ne respectant pas la casse) suivies de 1 à 4 chiffres</span><span class="sxs-lookup"><span data-stu-id="319ad-3446">Two letters (not case sensitive) followed by 1-4 numbers</span></span>

### <a name="checksum"></a><span data-ttu-id="319ad-3447">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="319ad-3447">Checksum</span></span>

<span data-ttu-id="319ad-3448">Non</span><span class="sxs-lookup"><span data-stu-id="319ad-3448">No</span></span>

### <a name="definition"></a><span data-ttu-id="319ad-3449">Définition</span><span class="sxs-lookup"><span data-stu-id="319ad-3449">Definition</span></span>

<span data-ttu-id="319ad-3450">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="319ad-3450">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="319ad-3451">L’expression régulière Regex_uk_electoral trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="319ad-3451">The regular expression Regex_uk_electoral finds content that matches the pattern.</span></span>
- <span data-ttu-id="319ad-3452">Un mot clé figurant dans la liste Keyword_uk_electoral est trouvé.</span><span class="sxs-lookup"><span data-stu-id="319ad-3452">A keyword from Keyword_uk_electoral is found.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="319ad-3453">Mots-clés</span><span class="sxs-lookup"><span data-stu-id="319ad-3453">Keywords</span></span>

#### <a name="keyword_uk_electoral"></a><span data-ttu-id="319ad-3454">Keyword_uk_electoral</span><span class="sxs-lookup"><span data-stu-id="319ad-3454">Keyword_uk_electoral</span></span>

- <span data-ttu-id="319ad-3455">nomination au conseil</span><span class="sxs-lookup"><span data-stu-id="319ad-3455">council nomination</span></span> 
- <span data-ttu-id="319ad-3456">formulaire de nomination</span><span class="sxs-lookup"><span data-stu-id="319ad-3456">nomination form</span></span> 
- <span data-ttu-id="319ad-3457">registre électoral</span><span class="sxs-lookup"><span data-stu-id="319ad-3457">electoral register</span></span> 
- <span data-ttu-id="319ad-3458">liste électorale</span><span class="sxs-lookup"><span data-stu-id="319ad-3458">electoral roll</span></span>

   
## <a name="uk-national-health-service-number"></a><span data-ttu-id="319ad-p146">Numéro national des services de santé Royaume-Uni</span><span class="sxs-lookup"><span data-stu-id="319ad-p146">U.K. National Health Service Number</span></span>

### <a name="format"></a><span data-ttu-id="319ad-3461">Format</span><span class="sxs-lookup"><span data-stu-id="319ad-3461">Format</span></span>

<span data-ttu-id="319ad-3462">10 à 17 chiffres séparés par des espaces</span><span class="sxs-lookup"><span data-stu-id="319ad-3462">10-17 digits separated by spaces</span></span>

### <a name="pattern"></a><span data-ttu-id="319ad-3463">Modèle</span><span class="sxs-lookup"><span data-stu-id="319ad-3463">Pattern</span></span>

<span data-ttu-id="319ad-3464">10 à 17 chiffres :</span><span class="sxs-lookup"><span data-stu-id="319ad-3464">10-17 digits:</span></span>
- <span data-ttu-id="319ad-3465">3 ou 10 chiffres</span><span class="sxs-lookup"><span data-stu-id="319ad-3465">Either 3 or 10 digits</span></span> 
- <span data-ttu-id="319ad-3466">Un espace</span><span class="sxs-lookup"><span data-stu-id="319ad-3466">A space</span></span> 
- <span data-ttu-id="319ad-3467">Trois chiffres</span><span class="sxs-lookup"><span data-stu-id="319ad-3467">Three digits</span></span> 
- <span data-ttu-id="319ad-3468">Un espace</span><span class="sxs-lookup"><span data-stu-id="319ad-3468">A space</span></span> 
- <span data-ttu-id="319ad-3469">Quatre chiffres</span><span class="sxs-lookup"><span data-stu-id="319ad-3469">Four digits</span></span>

### <a name="checksum"></a><span data-ttu-id="319ad-3470">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="319ad-3470">Checksum</span></span>

<span data-ttu-id="319ad-3471">Oui</span><span class="sxs-lookup"><span data-stu-id="319ad-3471">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="319ad-3472">Définition</span><span class="sxs-lookup"><span data-stu-id="319ad-3472">Definition</span></span>

<span data-ttu-id="319ad-3473">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="319ad-3473">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="319ad-3474">La fonction Func_uk_nhs_number trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="319ad-3474">The function Func_uk_nhs_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="319ad-3475">L’une des affirmations suivantes est vraie :</span><span class="sxs-lookup"><span data-stu-id="319ad-3475">One of the following is true:</span></span>
    - <span data-ttu-id="319ad-3476">Un mot clé figurant dans la liste Keyword_uk_nhs_number est trouvé.</span><span class="sxs-lookup"><span data-stu-id="319ad-3476">A keyword from Keyword_uk_nhs_number is found.</span></span>
    - <span data-ttu-id="319ad-3477">Un mot clé figurant dans la liste Keyword_uk_nhs_number1 est trouvé.</span><span class="sxs-lookup"><span data-stu-id="319ad-3477">A keyword from Keyword_uk_nhs_number1 is found.</span></span>
    - <span data-ttu-id="319ad-3478">Un mot clé figurant dans la liste Keyword_uk_nhs_number_dob est trouvé.</span><span class="sxs-lookup"><span data-stu-id="319ad-3478">A keyword from Keyword_uk_nhs_number_dob is found.</span></span>
- <span data-ttu-id="319ad-3479">La somme de contrôle est correcte.</span><span class="sxs-lookup"><span data-stu-id="319ad-3479">The checksum passes.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="319ad-3480">Mots-clés</span><span class="sxs-lookup"><span data-stu-id="319ad-3480">Keywords</span></span>
   
#### <a name="keyword_uk_nhs_number"></a><span data-ttu-id="319ad-3481">Keyword_uk_nhs_number</span><span class="sxs-lookup"><span data-stu-id="319ad-3481">Keyword_uk_nhs_number</span></span>

- <span data-ttu-id="319ad-3482">service national de santé</span><span class="sxs-lookup"><span data-stu-id="319ad-3482">national health service</span></span> 
- <span data-ttu-id="319ad-3483">NHS</span><span class="sxs-lookup"><span data-stu-id="319ad-3483">nhs</span></span> 
- <span data-ttu-id="319ad-3484">administration des services de santé</span><span class="sxs-lookup"><span data-stu-id="319ad-3484">health services authority</span></span> 
- <span data-ttu-id="319ad-3485">administration de la santé</span><span class="sxs-lookup"><span data-stu-id="319ad-3485">health authority</span></span>

#### <a name="keyword_uk_nhs_number1"></a><span data-ttu-id="319ad-3486">Keyword_uk_nhs_number1</span><span class="sxs-lookup"><span data-stu-id="319ad-3486">Keyword_uk_nhs_number1</span></span>

- <span data-ttu-id="319ad-3487">id du patient</span><span class="sxs-lookup"><span data-stu-id="319ad-3487">patient id</span></span> 
- <span data-ttu-id="319ad-3488">identification du patient</span><span class="sxs-lookup"><span data-stu-id="319ad-3488">patient identification</span></span> 
- <span data-ttu-id="319ad-3489">n° patient</span><span class="sxs-lookup"><span data-stu-id="319ad-3489">patient no</span></span> 
- <span data-ttu-id="319ad-3490">numéro de patient</span><span class="sxs-lookup"><span data-stu-id="319ad-3490">patient number</span></span>

#### <a name="keyword_uk_nhs_number_dob"></a><span data-ttu-id="319ad-3491">Keyword_uk_nhs_number_dob</span><span class="sxs-lookup"><span data-stu-id="319ad-3491">Keyword_uk_nhs_number_dob</span></span>

- <span data-ttu-id="319ad-3492">GP</span><span class="sxs-lookup"><span data-stu-id="319ad-3492">GP</span></span> 
- <span data-ttu-id="319ad-3493">DOB</span><span class="sxs-lookup"><span data-stu-id="319ad-3493">DOB</span></span> 
- <span data-ttu-id="319ad-3494">D. O. B</span><span class="sxs-lookup"><span data-stu-id="319ad-3494">D.O.B</span></span> 
- <span data-ttu-id="319ad-3495">Date of Birth</span><span class="sxs-lookup"><span data-stu-id="319ad-3495">Date of Birth</span></span> 
- <span data-ttu-id="319ad-3496">Birth Date</span><span class="sxs-lookup"><span data-stu-id="319ad-3496">Birth Date</span></span> 
   
## <a name="uk-national-insurance-number-nino"></a><span data-ttu-id="319ad-p147">Numéro d'assurance nationale (NINO) Royaume-Uni</span><span class="sxs-lookup"><span data-stu-id="319ad-p147">U.K. National Insurance Number (NINO)</span></span>

### <a name="format"></a><span data-ttu-id="319ad-3499">Format</span><span class="sxs-lookup"><span data-stu-id="319ad-3499">Format</span></span>

<span data-ttu-id="319ad-3500">7 caractères ou 9 caractères séparés par des espaces ou des tirets</span><span class="sxs-lookup"><span data-stu-id="319ad-3500">7 characters or 9 characters separated by spaces or dashes</span></span>

### <a name="pattern"></a><span data-ttu-id="319ad-3501">Modèle</span><span class="sxs-lookup"><span data-stu-id="319ad-3501">Pattern</span></span>

<span data-ttu-id="319ad-3502">Deux modèles possibles :</span><span class="sxs-lookup"><span data-stu-id="319ad-3502">Two possible patterns:</span></span>

- <span data-ttu-id="319ad-3503">Deux lettres (valides NINOs Utilisez uniquement certains caractères dans ce préfixe, que ce modèle valide ; ne respecte pas la casse)</span><span class="sxs-lookup"><span data-stu-id="319ad-3503">Two letters (valid NINOs use only certain characters in this prefix, which this pattern validates; not case sensitive)</span></span>
- <span data-ttu-id="319ad-3504">Six chiffres</span><span class="sxs-lookup"><span data-stu-id="319ad-3504">Six digits</span></span>
- <span data-ttu-id="319ad-3505">« A », « B », « C » ou « d » (comme le préfixe, seuls certains caractères sont autorisés dans le suffixe ; ne respectent pas la casse)</span><span class="sxs-lookup"><span data-stu-id="319ad-3505">Either 'A', 'B', 'C', or 'D' (like the prefix, only certain characters are allowed in the suffix; not case sensitive)</span></span>

<span data-ttu-id="319ad-3506">OU</span><span class="sxs-lookup"><span data-stu-id="319ad-3506">OR</span></span>

- <span data-ttu-id="319ad-3507">Deux lettres</span><span class="sxs-lookup"><span data-stu-id="319ad-3507">Two letters</span></span>
- <span data-ttu-id="319ad-3508">Un espace ou un tiret</span><span class="sxs-lookup"><span data-stu-id="319ad-3508">A space or dash</span></span>
- <span data-ttu-id="319ad-3509">Deux chiffres</span><span class="sxs-lookup"><span data-stu-id="319ad-3509">Two digits</span></span>
- <span data-ttu-id="319ad-3510">Un espace ou un tiret</span><span class="sxs-lookup"><span data-stu-id="319ad-3510">A space or dash</span></span>
- <span data-ttu-id="319ad-3511">Deux chiffres</span><span class="sxs-lookup"><span data-stu-id="319ad-3511">Two digits</span></span>
- <span data-ttu-id="319ad-3512">Un espace ou un tiret</span><span class="sxs-lookup"><span data-stu-id="319ad-3512">A space or dash</span></span>
- <span data-ttu-id="319ad-3513">Deux chiffres</span><span class="sxs-lookup"><span data-stu-id="319ad-3513">Two digits</span></span>
- <span data-ttu-id="319ad-3514">Un espace ou un tiret</span><span class="sxs-lookup"><span data-stu-id="319ad-3514">A space or dash</span></span>
- <span data-ttu-id="319ad-3515">« A », « B », « C » ou « d »</span><span class="sxs-lookup"><span data-stu-id="319ad-3515">Either 'A', 'B', 'C', or 'D'</span></span>

### <a name="checksum"></a><span data-ttu-id="319ad-3516">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="319ad-3516">Checksum</span></span>

<span data-ttu-id="319ad-3517">Non</span><span class="sxs-lookup"><span data-stu-id="319ad-3517">No</span></span>

### <a name="definition"></a><span data-ttu-id="319ad-3518">Définition</span><span class="sxs-lookup"><span data-stu-id="319ad-3518">Definition</span></span>

<span data-ttu-id="319ad-3519">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="319ad-3519">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="319ad-3520">La fonction Func_uk_nino trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="319ad-3520">The function Func_uk_nino finds content that matches the pattern.</span></span>
- <span data-ttu-id="319ad-3521">Un mot clé figurant dans la liste Keyword_uk_nino est trouvé.</span><span class="sxs-lookup"><span data-stu-id="319ad-3521">A keyword from Keyword_uk_nino is found.</span></span>

<span data-ttu-id="319ad-3522">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="319ad-3522">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="319ad-3523">La fonction Func_uk_nino trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="319ad-3523">The function Func_uk_nino finds content that matches the pattern.</span></span>
- <span data-ttu-id="319ad-3524">Aucun mot clé figurant dans la liste Keyword_uk_nino n’est trouvé.</span><span class="sxs-lookup"><span data-stu-id="319ad-3524">No keyword from Keyword_uk_nino is found.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="319ad-3525">Mots-clés</span><span class="sxs-lookup"><span data-stu-id="319ad-3525">Keywords</span></span>

#### <a name="keyword_uk_nino"></a><span data-ttu-id="319ad-3526">Keyword_uk_nino</span><span class="sxs-lookup"><span data-stu-id="319ad-3526">Keyword_uk_nino</span></span>

- <span data-ttu-id="319ad-3527">numéro d’assurance nationale</span><span class="sxs-lookup"><span data-stu-id="319ad-3527">national insurance number</span></span> 
- <span data-ttu-id="319ad-3528">cotisations sociales</span><span class="sxs-lookup"><span data-stu-id="319ad-3528">national insurance contributions</span></span> 
- <span data-ttu-id="319ad-3529">loi sur la protection</span><span class="sxs-lookup"><span data-stu-id="319ad-3529">protection act</span></span> 
- <span data-ttu-id="319ad-3530">cotisations</span><span class="sxs-lookup"><span data-stu-id="319ad-3530">insurance</span></span> 
- <span data-ttu-id="319ad-3531">numéro de sécurité sociale</span><span class="sxs-lookup"><span data-stu-id="319ad-3531">social security number</span></span> 
- <span data-ttu-id="319ad-3532">demande d’assurance</span><span class="sxs-lookup"><span data-stu-id="319ad-3532">insurance application</span></span> 
- <span data-ttu-id="319ad-3533">demande de soins médicaux</span><span class="sxs-lookup"><span data-stu-id="319ad-3533">medical application</span></span> 
- <span data-ttu-id="319ad-3534">assurance sociale</span><span class="sxs-lookup"><span data-stu-id="319ad-3534">social insurance</span></span> 
- <span data-ttu-id="319ad-3535">soins médicaux</span><span class="sxs-lookup"><span data-stu-id="319ad-3535">medical attention</span></span> 
- <span data-ttu-id="319ad-3536">sécurité sociale</span><span class="sxs-lookup"><span data-stu-id="319ad-3536">social security</span></span> 
- <span data-ttu-id="319ad-3537">grande-bretagne</span><span class="sxs-lookup"><span data-stu-id="319ad-3537">great britain</span></span> 
- <span data-ttu-id="319ad-3538">cotisations</span><span class="sxs-lookup"><span data-stu-id="319ad-3538">insurance</span></span>    
   
## <a name="us--uk-passport-number"></a><span data-ttu-id="319ad-p148">Numéro de passeport États-Unis/Royaume-Uni</span><span class="sxs-lookup"><span data-stu-id="319ad-p148">U.S. / U.K. Passport Number</span></span>

### <a name="format"></a><span data-ttu-id="319ad-3541">Format</span><span class="sxs-lookup"><span data-stu-id="319ad-3541">Format</span></span>

<span data-ttu-id="319ad-3542">Neuf chiffres</span><span class="sxs-lookup"><span data-stu-id="319ad-3542">Nine digits</span></span>

### <a name="pattern"></a><span data-ttu-id="319ad-3543">Modèle</span><span class="sxs-lookup"><span data-stu-id="319ad-3543">Pattern</span></span>

<span data-ttu-id="319ad-3544">Neuf chiffres consécutifs</span><span class="sxs-lookup"><span data-stu-id="319ad-3544">Nine consecutive digits</span></span>

### <a name="checksum"></a><span data-ttu-id="319ad-3545">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="319ad-3545">Checksum</span></span>

<span data-ttu-id="319ad-3546">Non</span><span class="sxs-lookup"><span data-stu-id="319ad-3546">No</span></span>

### <a name="definition"></a><span data-ttu-id="319ad-3547">Définition</span><span class="sxs-lookup"><span data-stu-id="319ad-3547">Definition</span></span>

<span data-ttu-id="319ad-3548">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="319ad-3548">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="319ad-3549">La fonction Func_usa_uk_passport trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="319ad-3549">The function Func_usa_uk_passport finds content that matches the pattern.</span></span>
- <span data-ttu-id="319ad-3550">Un mot clé figurant dans la liste Keyword_passport est trouvé.</span><span class="sxs-lookup"><span data-stu-id="319ad-3550">A keyword from Keyword_passport is found.</span></span>

```xml
<Entity id="178ec42a-18b4-47cc-85c7-d62c92fd67f8" patternsProximity="300" recommendedConfidence="75">
    <Pattern confidenceLevel="75">
        <IdMatch idRef="Func_usa_uk_passport" />
        <Match idRef="Keyword_passport" />
    </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="319ad-3551">Mots-clés</span><span class="sxs-lookup"><span data-stu-id="319ad-3551">Keywords</span></span>

#### <a name="keyword_passport"></a><span data-ttu-id="319ad-3552">Keyword_passport</span><span class="sxs-lookup"><span data-stu-id="319ad-3552">Keyword_passport</span></span>

- <span data-ttu-id="319ad-3553">Numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="319ad-3553">Passport Number</span></span> 
- <span data-ttu-id="319ad-3554">N° de passeport</span><span class="sxs-lookup"><span data-stu-id="319ad-3554">Passport No</span></span> 
- <span data-ttu-id="319ad-3555"># Passeport</span><span class="sxs-lookup"><span data-stu-id="319ad-3555">Passport #</span></span> 
- <span data-ttu-id="319ad-3556">Tel #</span><span class="sxs-lookup"><span data-stu-id="319ad-3556">Passport#</span></span> 
- <span data-ttu-id="319ad-3557">PassportID</span><span class="sxs-lookup"><span data-stu-id="319ad-3557">PassportID</span></span> 
- <span data-ttu-id="319ad-3558">N ° passeport</span><span class="sxs-lookup"><span data-stu-id="319ad-3558">Passportno</span></span> 
- <span data-ttu-id="319ad-3559">passportnumber</span><span class="sxs-lookup"><span data-stu-id="319ad-3559">passportnumber</span></span> 
- <span data-ttu-id="319ad-3560">パスポート</span><span class="sxs-lookup"><span data-stu-id="319ad-3560">パスポート</span></span> 
- <span data-ttu-id="319ad-3561">パスポート番号</span><span class="sxs-lookup"><span data-stu-id="319ad-3561">パスポート番号</span></span> 
- <span data-ttu-id="319ad-3562">パスポートのNum</span><span class="sxs-lookup"><span data-stu-id="319ad-3562">パスポートのNum</span></span> 
- <span data-ttu-id="319ad-3563">パスポート＃</span><span class="sxs-lookup"><span data-stu-id="319ad-3563">パスポート＃</span></span> 
- <span data-ttu-id="319ad-3564">Numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="319ad-3564">Numéro de passeport</span></span> 
- <span data-ttu-id="319ad-3565">Passeport n°</span><span class="sxs-lookup"><span data-stu-id="319ad-3565">Passeport n °</span></span> 
- <span data-ttu-id="319ad-3566">Passeport numéro</span><span class="sxs-lookup"><span data-stu-id="319ad-3566">Passeport Non</span></span> 
- <span data-ttu-id="319ad-3567"># Passeport</span><span class="sxs-lookup"><span data-stu-id="319ad-3567">Passeport #</span></span> 
- <span data-ttu-id="319ad-3568">Passeport #</span><span class="sxs-lookup"><span data-stu-id="319ad-3568">Passeport#</span></span> 
- <span data-ttu-id="319ad-3569">PasseportNon</span><span class="sxs-lookup"><span data-stu-id="319ad-3569">PasseportNon</span></span> 
- <span data-ttu-id="319ad-3570">Passeportn °</span><span class="sxs-lookup"><span data-stu-id="319ad-3570">Passeportn °</span></span> 
   
## <a name="us-bank-account-number"></a><span data-ttu-id="319ad-3571">Numéro de compte bancaire États-Unis</span><span class="sxs-lookup"><span data-stu-id="319ad-3571">U.S. Bank Account Number</span></span>

### <a name="format"></a><span data-ttu-id="319ad-3572">Format</span><span class="sxs-lookup"><span data-stu-id="319ad-3572">Format</span></span>

<span data-ttu-id="319ad-3573">8-17 chiffres</span><span class="sxs-lookup"><span data-stu-id="319ad-3573">8-17 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="319ad-3574">Modèle</span><span class="sxs-lookup"><span data-stu-id="319ad-3574">Pattern</span></span>

<span data-ttu-id="319ad-3575">8 à 17 chiffres consécutifs</span><span class="sxs-lookup"><span data-stu-id="319ad-3575">8-17 consecutive digits</span></span>

### <a name="checksum"></a><span data-ttu-id="319ad-3576">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="319ad-3576">Checksum</span></span>

<span data-ttu-id="319ad-3577">Non</span><span class="sxs-lookup"><span data-stu-id="319ad-3577">No</span></span>

### <a name="definition"></a><span data-ttu-id="319ad-3578">Définition</span><span class="sxs-lookup"><span data-stu-id="319ad-3578">Definition</span></span>

<span data-ttu-id="319ad-3579">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="319ad-3579">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="319ad-3580">L’expression régulière Regex_usa_bank_account_number trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="319ad-3580">The regular expression Regex_usa_bank_account_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="319ad-3581">Un mot clé figurant dans la liste Keyword_usa_Bank_Account est trouvé.</span><span class="sxs-lookup"><span data-stu-id="319ad-3581">A keyword from Keyword_usa_Bank_Account is found.</span></span>

```xml
<!-- U.S. Bank Account Number -->
<Entity id="a2ce32a8-f935-4bb6-8e96-2a5157672e2c" patternsProximity="300" recommendedConfidence="75">
    <Pattern confidenceLevel="75">
        <IdMatch idRef="Regex_usa_bank_account_number" />
        <Match idRef="Keyword_usa_Bank_Account" />
    </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="319ad-3582">Mots-clés</span><span class="sxs-lookup"><span data-stu-id="319ad-3582">Keywords</span></span>

#### <a name="keyword_usa_bank_account"></a><span data-ttu-id="319ad-3583">Keyword_usa_Bank_Account</span><span class="sxs-lookup"><span data-stu-id="319ad-3583">Keyword_usa_Bank_Account</span></span>

- <span data-ttu-id="319ad-3584">Numéro de compte courant</span><span class="sxs-lookup"><span data-stu-id="319ad-3584">Checking Account Number</span></span> 
- <span data-ttu-id="319ad-3585">Compte courant</span><span class="sxs-lookup"><span data-stu-id="319ad-3585">Checking Account</span></span> 
- <span data-ttu-id="319ad-3586"># compte courant</span><span class="sxs-lookup"><span data-stu-id="319ad-3586">Checking Account #</span></span> 
- <span data-ttu-id="319ad-3587">Numéro compte courant</span><span class="sxs-lookup"><span data-stu-id="319ad-3587">Checking Acct Number</span></span> 
- <span data-ttu-id="319ad-3588"># compte courant</span><span class="sxs-lookup"><span data-stu-id="319ad-3588">Checking Acct #</span></span> 
- <span data-ttu-id="319ad-3589">N° de compte courant</span><span class="sxs-lookup"><span data-stu-id="319ad-3589">Checking Acct No.</span></span> 
- <span data-ttu-id="319ad-3590">N° de compte courant</span><span class="sxs-lookup"><span data-stu-id="319ad-3590">Checking Account No.</span></span> 
- <span data-ttu-id="319ad-3591">Numéro de compte bancaire</span><span class="sxs-lookup"><span data-stu-id="319ad-3591">Bank Account Number</span></span> 
- <span data-ttu-id="319ad-3592"># Compte bancaire</span><span class="sxs-lookup"><span data-stu-id="319ad-3592">Bank Account #</span></span> 
- <span data-ttu-id="319ad-3593">Numéro de compte bancaire</span><span class="sxs-lookup"><span data-stu-id="319ad-3593">Bank Acct Number</span></span> 
- <span data-ttu-id="319ad-3594"># Compte bancaire</span><span class="sxs-lookup"><span data-stu-id="319ad-3594">Bank Acct #</span></span> 
- <span data-ttu-id="319ad-3595">N° de compte bancaire</span><span class="sxs-lookup"><span data-stu-id="319ad-3595">Bank Acct No.</span></span> 
- <span data-ttu-id="319ad-3596">N° de compte bancaire</span><span class="sxs-lookup"><span data-stu-id="319ad-3596">Bank Account No.</span></span> 
- <span data-ttu-id="319ad-3597">Numéro de compte d’épargne</span><span class="sxs-lookup"><span data-stu-id="319ad-3597">Savings Account Number</span></span> 
- <span data-ttu-id="319ad-3598">Compte d’épargne.</span><span class="sxs-lookup"><span data-stu-id="319ad-3598">Savings Account.</span></span> 
- <span data-ttu-id="319ad-3599">N° de compte d’épargne</span><span class="sxs-lookup"><span data-stu-id="319ad-3599">Savings Account #</span></span> 
- <span data-ttu-id="319ad-3600">Numéro de compte d’épargne</span><span class="sxs-lookup"><span data-stu-id="319ad-3600">Savings Acct Number</span></span> 
- <span data-ttu-id="319ad-3601"># compte d’épargne</span><span class="sxs-lookup"><span data-stu-id="319ad-3601">Savings Acct #</span></span> 
- <span data-ttu-id="319ad-3602">N° de compte d’épargne</span><span class="sxs-lookup"><span data-stu-id="319ad-3602">Savings Acct No.</span></span> 
- <span data-ttu-id="319ad-3603">N° de compte d’épargne</span><span class="sxs-lookup"><span data-stu-id="319ad-3603">Savings Account No.</span></span> 
- <span data-ttu-id="319ad-3604">Numéro de compte de débit</span><span class="sxs-lookup"><span data-stu-id="319ad-3604">Debit Account Number</span></span> 
- <span data-ttu-id="319ad-3605">Compte de débit</span><span class="sxs-lookup"><span data-stu-id="319ad-3605">Debit Account</span></span> 
- <span data-ttu-id="319ad-3606"># Compte de débit</span><span class="sxs-lookup"><span data-stu-id="319ad-3606">Debit Account #</span></span> 
- <span data-ttu-id="319ad-3607">Numéro de compte de débit</span><span class="sxs-lookup"><span data-stu-id="319ad-3607">Debit Acct Number</span></span> 
- <span data-ttu-id="319ad-3608"># Compte de débit</span><span class="sxs-lookup"><span data-stu-id="319ad-3608">Debit Acct #</span></span> 
- <span data-ttu-id="319ad-3609">N° de compte de débit</span><span class="sxs-lookup"><span data-stu-id="319ad-3609">Debit Acct No.</span></span> 
- <span data-ttu-id="319ad-3610">N° de compte de débit</span><span class="sxs-lookup"><span data-stu-id="319ad-3610">Debit Account No.</span></span> 
   
## <a name="us-drivers-license-number"></a><span data-ttu-id="319ad-3611">Numéro de permis de conduire États-Unis</span><span class="sxs-lookup"><span data-stu-id="319ad-3611">U.S. Driver's License Number</span></span>

### <a name="format"></a><span data-ttu-id="319ad-3612">Format</span><span class="sxs-lookup"><span data-stu-id="319ad-3612">Format</span></span>

<span data-ttu-id="319ad-3613">Dépend de l’État</span><span class="sxs-lookup"><span data-stu-id="319ad-3613">Depends on the state</span></span>

### <a name="pattern"></a><span data-ttu-id="319ad-3614">Modèle</span><span class="sxs-lookup"><span data-stu-id="319ad-3614">Pattern</span></span>

<span data-ttu-id="319ad-3615">Dépend de l’État, par exemple, New York :</span><span class="sxs-lookup"><span data-stu-id="319ad-3615">Depends on the state -- for example, New York:</span></span>
- <span data-ttu-id="319ad-3616">Neuf chiffres au format DDD DDD DDD correspondront.</span><span class="sxs-lookup"><span data-stu-id="319ad-3616">Nine digits formatted like ddd ddd ddd will match.</span></span>
- <span data-ttu-id="319ad-3617">Neuf chiffres au format ddddddddd ne correspondront pas.</span><span class="sxs-lookup"><span data-stu-id="319ad-3617">Nine digits like ddddddddd will not match.</span></span>

### <a name="checksum"></a><span data-ttu-id="319ad-3618">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="319ad-3618">Checksum</span></span>

<span data-ttu-id="319ad-3619">Non</span><span class="sxs-lookup"><span data-stu-id="319ad-3619">No</span></span>

### <a name="definition"></a><span data-ttu-id="319ad-3620">Définition</span><span class="sxs-lookup"><span data-stu-id="319ad-3620">Definition</span></span>

<span data-ttu-id="319ad-3621">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="319ad-3621">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="319ad-3622">La fonction Func_new_york_drivers_license_number trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="319ad-3622">The function Func_new_york_drivers_license_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="319ad-3623">Un mot clé figurant dans la liste Keyword_[state_name]_drivers_license_name est trouvé.</span><span class="sxs-lookup"><span data-stu-id="319ad-3623">A keyword from Keyword_[state_name]_drivers_license_name is found.</span></span>
- <span data-ttu-id="319ad-3624">Un mot clé figurant dans la liste Keyword_us_drivers_license est trouvé.</span><span class="sxs-lookup"><span data-stu-id="319ad-3624">A keyword from Keyword_us_drivers_license is found.</span></span>

<span data-ttu-id="319ad-3625">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 65 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="319ad-3625">A DLP policy is 65% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="319ad-3626">La fonction Func_new_york_drivers_license_number trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="319ad-3626">The function Func_new_york_drivers_license_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="319ad-3627">Un mot clé figurant dans la liste Keyword_[state_name]_drivers_license_name est trouvé.</span><span class="sxs-lookup"><span data-stu-id="319ad-3627">A keyword from Keyword_[state_name]_drivers_license_name is found.</span></span>
- <span data-ttu-id="319ad-3628">Un mot clé figurant dans la liste Keyword_us_drivers_license_abbreviations est trouvé.</span><span class="sxs-lookup"><span data-stu-id="319ad-3628">A keyword from Keyword_us_drivers_license_abbreviations is found.</span></span>
- <span data-ttu-id="319ad-3629">Aucun mot clé figurant dans la liste Keyword_us_drivers_license n’est trouvé.</span><span class="sxs-lookup"><span data-stu-id="319ad-3629">No keyword from Keyword_us_drivers_license is found.</span></span>

```xml
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
```

### <a name="keywords"></a><span data-ttu-id="319ad-3630">Mots-clés</span><span class="sxs-lookup"><span data-stu-id="319ad-3630">Keywords</span></span>

#### <a name="keyword_us_drivers_license_abbreviations"></a><span data-ttu-id="319ad-3631">Keyword_us_drivers_license_abbreviations</span><span class="sxs-lookup"><span data-stu-id="319ad-3631">Keyword_us_drivers_license_abbreviations</span></span>

- <span data-ttu-id="319ad-3632">LD</span><span class="sxs-lookup"><span data-stu-id="319ad-3632">DL</span></span> 
- <span data-ttu-id="319ad-3633">DISTRIBUTION</span><span class="sxs-lookup"><span data-stu-id="319ad-3633">DLS</span></span> 
- <span data-ttu-id="319ad-3634">CÈDE</span><span class="sxs-lookup"><span data-stu-id="319ad-3634">CDL</span></span> 
- <span data-ttu-id="319ad-3635">CDLS</span><span class="sxs-lookup"><span data-stu-id="319ad-3635">CDLS</span></span> 
- <span data-ttu-id="319ad-3636">ID</span><span class="sxs-lookup"><span data-stu-id="319ad-3636">ID</span></span> 
- <span data-ttu-id="319ad-3637">Codes</span><span class="sxs-lookup"><span data-stu-id="319ad-3637">IDs</span></span> 
- <span data-ttu-id="319ad-3638">LD #</span><span class="sxs-lookup"><span data-stu-id="319ad-3638">DL#</span></span> 
- <span data-ttu-id="319ad-3639">DISTRIBUTION #</span><span class="sxs-lookup"><span data-stu-id="319ad-3639">DLS#</span></span> 
- <span data-ttu-id="319ad-3640">CÈDE #</span><span class="sxs-lookup"><span data-stu-id="319ad-3640">CDL#</span></span> 
- <span data-ttu-id="319ad-3641">CDLS #</span><span class="sxs-lookup"><span data-stu-id="319ad-3641">CDLS#</span></span> 
- <span data-ttu-id="319ad-3642">Réf #</span><span class="sxs-lookup"><span data-stu-id="319ad-3642">ID#</span></span>
- <span data-ttu-id="319ad-3643">Codes #</span><span class="sxs-lookup"><span data-stu-id="319ad-3643">IDs#</span></span> 
- <span data-ttu-id="319ad-3644">Numéro d’identification</span><span class="sxs-lookup"><span data-stu-id="319ad-3644">ID number</span></span> 
- <span data-ttu-id="319ad-3645">Numéros d’identification</span><span class="sxs-lookup"><span data-stu-id="319ad-3645">ID numbers</span></span> 
- <span data-ttu-id="319ad-3646">Profil</span><span class="sxs-lookup"><span data-stu-id="319ad-3646">LIC</span></span> 
- <span data-ttu-id="319ad-3647">Profil #</span><span class="sxs-lookup"><span data-stu-id="319ad-3647">LIC#</span></span> 

#### <a name="keyword_us_drivers_license"></a><span data-ttu-id="319ad-3648">Keyword_us_drivers_license</span><span class="sxs-lookup"><span data-stu-id="319ad-3648">Keyword_us_drivers_license</span></span>

- <span data-ttu-id="319ad-3649">DriverLic</span><span class="sxs-lookup"><span data-stu-id="319ad-3649">DriverLic</span></span> 
- <span data-ttu-id="319ad-3650">DriverLics</span><span class="sxs-lookup"><span data-stu-id="319ad-3650">DriverLics</span></span> 
- <span data-ttu-id="319ad-3651">DriverLicense</span><span class="sxs-lookup"><span data-stu-id="319ad-3651">DriverLicense</span></span> 
- <span data-ttu-id="319ad-3652">DriverLicenses</span><span class="sxs-lookup"><span data-stu-id="319ad-3652">DriverLicenses</span></span> 
- <span data-ttu-id="319ad-3653">Permis conduire</span><span class="sxs-lookup"><span data-stu-id="319ad-3653">Driver Lic</span></span> 
- <span data-ttu-id="319ad-3654">Permis conduire</span><span class="sxs-lookup"><span data-stu-id="319ad-3654">Driver Lics</span></span> 
- <span data-ttu-id="319ad-3655">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="319ad-3655">Driver License</span></span> 
- <span data-ttu-id="319ad-3656">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="319ad-3656">Driver Licenses</span></span> 
- <span data-ttu-id="319ad-3657">DriversLic</span><span class="sxs-lookup"><span data-stu-id="319ad-3657">DriversLic</span></span> 
- <span data-ttu-id="319ad-3658">DriversLics</span><span class="sxs-lookup"><span data-stu-id="319ad-3658">DriversLics</span></span> 
- <span data-ttu-id="319ad-3659">DriversLicense</span><span class="sxs-lookup"><span data-stu-id="319ad-3659">DriversLicense</span></span> 
- <span data-ttu-id="319ad-3660">DriversLicenses</span><span class="sxs-lookup"><span data-stu-id="319ad-3660">DriversLicenses</span></span> 
- <span data-ttu-id="319ad-3661">Permis conduire</span><span class="sxs-lookup"><span data-stu-id="319ad-3661">Drivers Lic</span></span> 
- <span data-ttu-id="319ad-3662">Permis conduire</span><span class="sxs-lookup"><span data-stu-id="319ad-3662">Drivers Lics</span></span> 
- <span data-ttu-id="319ad-3663">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="319ad-3663">Drivers License</span></span> 
- <span data-ttu-id="319ad-3664">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="319ad-3664">Drivers Licenses</span></span> 
- <span data-ttu-id="319ad-3665">Driver'Lic</span><span class="sxs-lookup"><span data-stu-id="319ad-3665">Driver'Lic</span></span> 
- <span data-ttu-id="319ad-3666">Driver'Lics</span><span class="sxs-lookup"><span data-stu-id="319ad-3666">Driver'Lics</span></span> 
- <span data-ttu-id="319ad-3667">Driver'License</span><span class="sxs-lookup"><span data-stu-id="319ad-3667">Driver'License</span></span> 
- <span data-ttu-id="319ad-3668">Driver'Licenses</span><span class="sxs-lookup"><span data-stu-id="319ad-3668">Driver'Licenses</span></span> 
- <span data-ttu-id="319ad-3669">Permis conduire</span><span class="sxs-lookup"><span data-stu-id="319ad-3669">Driver' Lic</span></span> 
- <span data-ttu-id="319ad-3670">Permis conduire</span><span class="sxs-lookup"><span data-stu-id="319ad-3670">Driver' Lics</span></span> 
- <span data-ttu-id="319ad-3671">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="319ad-3671">Driver' License</span></span> 
- <span data-ttu-id="319ad-3672">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="319ad-3672">Driver' Licenses</span></span>
- <span data-ttu-id="319ad-3673">Driver'sLic</span><span class="sxs-lookup"><span data-stu-id="319ad-3673">Driver'sLic</span></span> 
- <span data-ttu-id="319ad-3674">Driver'sLics</span><span class="sxs-lookup"><span data-stu-id="319ad-3674">Driver'sLics</span></span> 
- <span data-ttu-id="319ad-3675">Driver'sLicense</span><span class="sxs-lookup"><span data-stu-id="319ad-3675">Driver'sLicense</span></span> 
- <span data-ttu-id="319ad-3676">Driver'sLicenses</span><span class="sxs-lookup"><span data-stu-id="319ad-3676">Driver'sLicenses</span></span> 
- <span data-ttu-id="319ad-3677">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="319ad-3677">Driver's Lic</span></span> 
- <span data-ttu-id="319ad-3678">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="319ad-3678">Driver's Lics</span></span> 
- <span data-ttu-id="319ad-3679">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="319ad-3679">Driver's License</span></span> 
- <span data-ttu-id="319ad-3680">Driver’s Licenses</span><span class="sxs-lookup"><span data-stu-id="319ad-3680">Driver's Licenses</span></span> 
- <span data-ttu-id="319ad-3681">numéro d’identification</span><span class="sxs-lookup"><span data-stu-id="319ad-3681">identification number</span></span> 
- <span data-ttu-id="319ad-3682">numéros d’identification</span><span class="sxs-lookup"><span data-stu-id="319ad-3682">identification numbers</span></span> 
- <span data-ttu-id="319ad-3683"># identification</span><span class="sxs-lookup"><span data-stu-id="319ad-3683">identification #</span></span> 
- <span data-ttu-id="319ad-3684">carte d’identité</span><span class="sxs-lookup"><span data-stu-id="319ad-3684">id card</span></span> 
- <span data-ttu-id="319ad-3685">cartes d’identité</span><span class="sxs-lookup"><span data-stu-id="319ad-3685">id cards</span></span> 
- <span data-ttu-id="319ad-3686">carte d’identification</span><span class="sxs-lookup"><span data-stu-id="319ad-3686">identification card</span></span> 
- <span data-ttu-id="319ad-3687">cartes d’identification</span><span class="sxs-lookup"><span data-stu-id="319ad-3687">identification cards</span></span> 
- <span data-ttu-id="319ad-3688">DriverLic #</span><span class="sxs-lookup"><span data-stu-id="319ad-3688">DriverLic#</span></span> 
- <span data-ttu-id="319ad-3689">DriverLics #</span><span class="sxs-lookup"><span data-stu-id="319ad-3689">DriverLics#</span></span> 
- <span data-ttu-id="319ad-3690">DriverLicense #</span><span class="sxs-lookup"><span data-stu-id="319ad-3690">DriverLicense#</span></span> 
- <span data-ttu-id="319ad-3691">DriverLicenses #</span><span class="sxs-lookup"><span data-stu-id="319ad-3691">DriverLicenses#</span></span> 
- <span data-ttu-id="319ad-3692">#Permis conduire</span><span class="sxs-lookup"><span data-stu-id="319ad-3692">Driver Lic#</span></span> 
- <span data-ttu-id="319ad-3693">#Permis conduire</span><span class="sxs-lookup"><span data-stu-id="319ad-3693">Driver Lics#</span></span> 
- <span data-ttu-id="319ad-3694">#Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="319ad-3694">Driver License#</span></span> 
- <span data-ttu-id="319ad-3695">#Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="319ad-3695">Driver Licenses#</span></span> 
- <span data-ttu-id="319ad-3696">DriversLic #</span><span class="sxs-lookup"><span data-stu-id="319ad-3696">DriversLic#</span></span> 
- <span data-ttu-id="319ad-3697">DriversLics #</span><span class="sxs-lookup"><span data-stu-id="319ad-3697">DriversLics#</span></span> 
- <span data-ttu-id="319ad-3698">DriversLicense #</span><span class="sxs-lookup"><span data-stu-id="319ad-3698">DriversLicense#</span></span> 
- <span data-ttu-id="319ad-3699">DriversLicenses #</span><span class="sxs-lookup"><span data-stu-id="319ad-3699">DriversLicenses#</span></span> 
- <span data-ttu-id="319ad-3700">#Permis conduire</span><span class="sxs-lookup"><span data-stu-id="319ad-3700">Drivers Lic#</span></span> 
- <span data-ttu-id="319ad-3701">#Permis conduire</span><span class="sxs-lookup"><span data-stu-id="319ad-3701">Drivers Lics#</span></span> 
- <span data-ttu-id="319ad-3702">#Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="319ad-3702">Drivers License#</span></span> 
- <span data-ttu-id="319ad-3703">#Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="319ad-3703">Drivers Licenses#</span></span> 
- <span data-ttu-id="319ad-3704">Driver'Lic #</span><span class="sxs-lookup"><span data-stu-id="319ad-3704">Driver'Lic#</span></span> 
- <span data-ttu-id="319ad-3705">Driver'Lics #</span><span class="sxs-lookup"><span data-stu-id="319ad-3705">Driver'Lics#</span></span> 
- <span data-ttu-id="319ad-3706">Driver'License #</span><span class="sxs-lookup"><span data-stu-id="319ad-3706">Driver'License#</span></span> 
- <span data-ttu-id="319ad-3707">Driver'Licenses #</span><span class="sxs-lookup"><span data-stu-id="319ad-3707">Driver'Licenses#</span></span> 
- <span data-ttu-id="319ad-3708">#Permis conduire</span><span class="sxs-lookup"><span data-stu-id="319ad-3708">Driver' Lic#</span></span> 
- <span data-ttu-id="319ad-3709">#Permis conduire</span><span class="sxs-lookup"><span data-stu-id="319ad-3709">Driver' Lics#</span></span> 
- <span data-ttu-id="319ad-3710">#Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="319ad-3710">Driver' License#</span></span> 
- <span data-ttu-id="319ad-3711">#Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="319ad-3711">Driver' Licenses#</span></span> 
- <span data-ttu-id="319ad-3712">Driver'sLic #</span><span class="sxs-lookup"><span data-stu-id="319ad-3712">Driver'sLic#</span></span> 
- <span data-ttu-id="319ad-3713">Driver'sLics #</span><span class="sxs-lookup"><span data-stu-id="319ad-3713">Driver'sLics#</span></span> 
- <span data-ttu-id="319ad-3714">Driver'sLicense #</span><span class="sxs-lookup"><span data-stu-id="319ad-3714">Driver'sLicense#</span></span> 
- <span data-ttu-id="319ad-3715">Driver'sLicenses #</span><span class="sxs-lookup"><span data-stu-id="319ad-3715">Driver'sLicenses#</span></span> 
- <span data-ttu-id="319ad-3716">#Permisconduire</span><span class="sxs-lookup"><span data-stu-id="319ad-3716">Driver's Lic#</span></span> 
- <span data-ttu-id="319ad-3717">#Permisconduire</span><span class="sxs-lookup"><span data-stu-id="319ad-3717">Driver's Lics#</span></span> 
- <span data-ttu-id="319ad-3718">#Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="319ad-3718">Driver's License#</span></span> 
- <span data-ttu-id="319ad-3719">#Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="319ad-3719">Driver's Licenses#</span></span> 
- <span data-ttu-id="319ad-3720"># carte d’identité</span><span class="sxs-lookup"><span data-stu-id="319ad-3720">id card#</span></span> 
- <span data-ttu-id="319ad-3721"># cartes d’identité</span><span class="sxs-lookup"><span data-stu-id="319ad-3721">id cards#</span></span> 
- <span data-ttu-id="319ad-3722">#carte d’identification</span><span class="sxs-lookup"><span data-stu-id="319ad-3722">identification card#</span></span> 
- <span data-ttu-id="319ad-3723">#cartes d’identification</span><span class="sxs-lookup"><span data-stu-id="319ad-3723">identification cards#</span></span> 


#### <a name="keyword_state_name_drivers_license_name"></a><span data-ttu-id="319ad-3724">Keyword_ [state_name] _drivers_license_name</span><span class="sxs-lookup"><span data-stu-id="319ad-3724">Keyword_[state_name]_drivers_license_name</span></span>

- <span data-ttu-id="319ad-3725">Abréviation de l’État (par exemple, « NY »)</span><span class="sxs-lookup"><span data-stu-id="319ad-3725">State abbreviation (for example, "NY")</span></span> 
- <span data-ttu-id="319ad-3726">Nom de l’État (par exemple, « New York »)</span><span class="sxs-lookup"><span data-stu-id="319ad-3726">State name (for example, "New York")</span></span>    
   
## <a name="us-individual-taxpayer-identification-number-itin"></a><span data-ttu-id="319ad-3727">Numéro d’identification fiscale individuel (ITIN) États-Unis</span><span class="sxs-lookup"><span data-stu-id="319ad-3727">U.S. Individual Taxpayer Identification Number (ITIN)</span></span>

### <a name="format"></a><span data-ttu-id="319ad-3728">Format</span><span class="sxs-lookup"><span data-stu-id="319ad-3728">Format</span></span>

<span data-ttu-id="319ad-3729">Neuf chiffres, le premier étant le « 9 », le quatrième le « 7 » ou le « 8 », éventuellement mis en forme avec des espaces ou des tirets</span><span class="sxs-lookup"><span data-stu-id="319ad-3729">Nine digits that start with a "9" and contain a "7" or "8" as the fourth digit, optionally formatted with spaces or dashes</span></span>

### <a name="pattern"></a><span data-ttu-id="319ad-3730">Modèle</span><span class="sxs-lookup"><span data-stu-id="319ad-3730">Pattern</span></span>

<span data-ttu-id="319ad-3731">Avec</span><span class="sxs-lookup"><span data-stu-id="319ad-3731">Formatted:</span></span>
- <span data-ttu-id="319ad-3732">Le chiffre « 9 »</span><span class="sxs-lookup"><span data-stu-id="319ad-3732">The digit "9"</span></span> 
- <span data-ttu-id="319ad-3733">Deux chiffres</span><span class="sxs-lookup"><span data-stu-id="319ad-3733">Two digits</span></span> 
- <span data-ttu-id="319ad-3734">Un espace ou un tiret</span><span class="sxs-lookup"><span data-stu-id="319ad-3734">A space or dash</span></span> 
- <span data-ttu-id="319ad-3735">Un « 7 » ou un « 8 »</span><span class="sxs-lookup"><span data-stu-id="319ad-3735">A "7" or "8"</span></span> 
- <span data-ttu-id="319ad-3736">Un chiffre</span><span class="sxs-lookup"><span data-stu-id="319ad-3736">A digit</span></span> 
- <span data-ttu-id="319ad-3737">Un espace ou tiret</span><span class="sxs-lookup"><span data-stu-id="319ad-3737">A space, or dash</span></span> 
- <span data-ttu-id="319ad-3738">Quatre chiffres</span><span class="sxs-lookup"><span data-stu-id="319ad-3738">Four digits</span></span>

<span data-ttu-id="319ad-3739">Non</span><span class="sxs-lookup"><span data-stu-id="319ad-3739">Unformatted:</span></span>
- <span data-ttu-id="319ad-3740">Le chiffre « 9 »</span><span class="sxs-lookup"><span data-stu-id="319ad-3740">The digit "9"</span></span> 
- <span data-ttu-id="319ad-3741">Deux chiffres</span><span class="sxs-lookup"><span data-stu-id="319ad-3741">Two digits</span></span> 
- <span data-ttu-id="319ad-3742">Un « 7 » ou un « 8 »</span><span class="sxs-lookup"><span data-stu-id="319ad-3742">A "7" or "8"</span></span> 
- <span data-ttu-id="319ad-3743">Cinq chiffres</span><span class="sxs-lookup"><span data-stu-id="319ad-3743">Five digits</span></span>

### <a name="checksum"></a><span data-ttu-id="319ad-3744">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="319ad-3744">Checksum</span></span>

<span data-ttu-id="319ad-3745">Non</span><span class="sxs-lookup"><span data-stu-id="319ad-3745">No</span></span>

### <a name="definition"></a><span data-ttu-id="319ad-3746">Définition</span><span class="sxs-lookup"><span data-stu-id="319ad-3746">Definition</span></span>

<span data-ttu-id="319ad-3747">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="319ad-3747">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="319ad-3748">La fonction Func_formatted_itin trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="319ad-3748">The function Func_formatted_itin finds content that matches the pattern.</span></span>
- <span data-ttu-id="319ad-3749">Au moins une des affirmations suivantes est vraie :</span><span class="sxs-lookup"><span data-stu-id="319ad-3749">At least one of the following is true:</span></span>
    - <span data-ttu-id="319ad-3750">Un mot clé figurant dans la liste Keyword_itin est trouvé.</span><span class="sxs-lookup"><span data-stu-id="319ad-3750">A keyword from Keyword_itin is found.</span></span>
    - <span data-ttu-id="319ad-3751">La fonction Func_us_address trouve une adresse au format correct.</span><span class="sxs-lookup"><span data-stu-id="319ad-3751">The function Func_us_address finds an address in the right date format.</span></span>
    - <span data-ttu-id="319ad-3752">La fonction Func_us_date trouve une date au format correct.</span><span class="sxs-lookup"><span data-stu-id="319ad-3752">The function Func_us_date finds a date in the right date format.</span></span>
    - <span data-ttu-id="319ad-3753">Un mot clé figurant dans la liste Keyword_itin_collaborative est trouvé.</span><span class="sxs-lookup"><span data-stu-id="319ad-3753">A keyword from Keyword_itin_collaborative is found.</span></span>

<span data-ttu-id="319ad-3754">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="319ad-3754">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="319ad-3755">La fonction Func_unformatted_itin trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="319ad-3755">The function Func_unformatted_itin finds content that matches the pattern.</span></span>
- <span data-ttu-id="319ad-3756">Au moins une des affirmations suivantes est vraie :</span><span class="sxs-lookup"><span data-stu-id="319ad-3756">At least one of the following is true:</span></span>
    - <span data-ttu-id="319ad-3757">Un mot clé figurant dans la liste Keyword_itin_collaborative est trouvé.</span><span class="sxs-lookup"><span data-stu-id="319ad-3757">A keyword from Keyword_itin_collaborative is found.</span></span>
    - <span data-ttu-id="319ad-3758">La fonction Func_us_address trouve une adresse au format correct.</span><span class="sxs-lookup"><span data-stu-id="319ad-3758">The function Func_us_address finds an address in the right date format.</span></span>
    - <span data-ttu-id="319ad-3759">La fonction Func_us_date trouve une date au format correct.</span><span class="sxs-lookup"><span data-stu-id="319ad-3759">The function Func_us_date finds a date in the right date format.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="319ad-3760">Mots-clés</span><span class="sxs-lookup"><span data-stu-id="319ad-3760">Keywords</span></span>

#### <a name="keyword_itin"></a><span data-ttu-id="319ad-3761">Keyword_itin</span><span class="sxs-lookup"><span data-stu-id="319ad-3761">Keyword_itin</span></span>

- <span data-ttu-id="319ad-3762">redevable</span><span class="sxs-lookup"><span data-stu-id="319ad-3762">taxpayer</span></span> 
- <span data-ttu-id="319ad-3763">id fiscal</span><span class="sxs-lookup"><span data-stu-id="319ad-3763">tax id</span></span> 
- <span data-ttu-id="319ad-3764">identification fiscale</span><span class="sxs-lookup"><span data-stu-id="319ad-3764">tax identification</span></span> 
- <span data-ttu-id="319ad-3765">itin</span><span class="sxs-lookup"><span data-stu-id="319ad-3765">itin</span></span> 
- <span data-ttu-id="319ad-3766">SSN</span><span class="sxs-lookup"><span data-stu-id="319ad-3766">ssn</span></span> 
- <span data-ttu-id="319ad-3767">Etain</span><span class="sxs-lookup"><span data-stu-id="319ad-3767">tin</span></span> 
- <span data-ttu-id="319ad-3768">sécurité sociale</span><span class="sxs-lookup"><span data-stu-id="319ad-3768">social security</span></span> 
- <span data-ttu-id="319ad-3769">contribuable</span><span class="sxs-lookup"><span data-stu-id="319ad-3769">tax payer</span></span> 
- <span data-ttu-id="319ad-3770">itins</span><span class="sxs-lookup"><span data-stu-id="319ad-3770">itins</span></span> 
- <span data-ttu-id="319ad-3771">taxi</span><span class="sxs-lookup"><span data-stu-id="319ad-3771">taxid</span></span> 
- <span data-ttu-id="319ad-3772">contribuable individuel</span><span class="sxs-lookup"><span data-stu-id="319ad-3772">individual taxpayer</span></span> 

#### <a name="keyword_itin_collaborative"></a><span data-ttu-id="319ad-3773">Keyword_itin_collaborative</span><span class="sxs-lookup"><span data-stu-id="319ad-3773">Keyword_itin_collaborative</span></span>

- <span data-ttu-id="319ad-3774">Licence</span><span class="sxs-lookup"><span data-stu-id="319ad-3774">License</span></span> 
- <span data-ttu-id="319ad-3775">LD</span><span class="sxs-lookup"><span data-stu-id="319ad-3775">DL</span></span> 
- <span data-ttu-id="319ad-3776">DOB</span><span class="sxs-lookup"><span data-stu-id="319ad-3776">DOB</span></span> 
- <span data-ttu-id="319ad-3777">Birthdate</span><span class="sxs-lookup"><span data-stu-id="319ad-3777">Birthdate</span></span> 
- <span data-ttu-id="319ad-3778">Birthday</span><span class="sxs-lookup"><span data-stu-id="319ad-3778">Birthday</span></span> 
- <span data-ttu-id="319ad-3779">Date of Birth</span><span class="sxs-lookup"><span data-stu-id="319ad-3779">Date of Birth</span></span> 
   
## <a name="us-social-security-number-ssn"></a><span data-ttu-id="319ad-3780">Numéro de sécurité sociale (SSN) États-Unis</span><span class="sxs-lookup"><span data-stu-id="319ad-3780">U.S. Social Security Number (SSN)</span></span>

### <a name="format"></a><span data-ttu-id="319ad-3781">Format</span><span class="sxs-lookup"><span data-stu-id="319ad-3781">Format</span></span>

<span data-ttu-id="319ad-3782">9 chiffres, qui peuvent être mis en forme ou non mis en forme</span><span class="sxs-lookup"><span data-stu-id="319ad-3782">9 digits, which may be in a formatted or unformatted pattern</span></span>

> [!NOTE]
> <span data-ttu-id="319ad-3783">La mise en forme d’un numéro de sécurité sociale émis avant le milieu de l’année 2011 est fixe et certaines parties du numéro doivent se situer dans certaines plages pour qu’il soit valide (mais il n’y a pas de somme de contrôle).</span><span class="sxs-lookup"><span data-stu-id="319ad-3783">If issued before mid-2011, an SSN has strong formatting where certain parts of the number must fall within certain ranges to be valid (but there's no checksum).</span></span>

### <a name="pattern"></a><span data-ttu-id="319ad-3784">Modèle</span><span class="sxs-lookup"><span data-stu-id="319ad-3784">Pattern</span></span>

<span data-ttu-id="319ad-3785">Quatre fonctions permettent de rechercher des numéros de sécurité sociale avec quatre différents modèles :</span><span class="sxs-lookup"><span data-stu-id="319ad-3785">Four functions look for SSNs in four different patterns:</span></span>
- <span data-ttu-id="319ad-3786">Func_ssn recherche des numéros de sécurité sociale avec une mise en forme fixe d’avant l’année 2011, mis en forme avec des tirets ou des espaces (ddd-dd-dddd OU ddd dd dddd)</span><span class="sxs-lookup"><span data-stu-id="319ad-3786">Func_ssn finds SSNs with pre-2011 strong formatting that are formatted with dashes or spaces (ddd-dd-dddd OR ddd dd dddd)</span></span>
- <span data-ttu-id="319ad-3787">Func_unformatted_ssn recherche des numéros de sécurité sociale avec une mise en forme fixe d’avant l’année 2011, avec neuf chiffres consécutifs non mis en forme (ddddddddd)</span><span class="sxs-lookup"><span data-stu-id="319ad-3787">Func_unformatted_ssn finds SSNs with pre-2011 strong formatting that are unformatted as nine consecutive digits (ddddddddd)</span></span>
- <span data-ttu-id="319ad-3788">Func_randomized_formatted_ssn recherche des numéros de sécurité sociale d’après l’année 2011, mis en forme avec des tirets ou des espaces  (ddd-dd-dddd OU ddd dd dddd)</span><span class="sxs-lookup"><span data-stu-id="319ad-3788">Func_randomized_formatted_ssn finds post-2011 SSNs that are formatted with dashes or spaces (ddd-dd-dddd OR ddd dd dddd)</span></span>
- <span data-ttu-id="319ad-3789">Func_randomized_unformatted_ssn recherche des numéros de sécurité sociale d’après l’année 2011, avec neuf chiffres consécutifs non mis en forme (ddddddddd)</span><span class="sxs-lookup"><span data-stu-id="319ad-3789">Func_randomized_unformatted_ssn finds post-2011 SSNs that are unformatted as nine consecutive digits (ddddddddd)</span></span>

### <a name="checksum"></a><span data-ttu-id="319ad-3790">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="319ad-3790">Checksum</span></span>

<span data-ttu-id="319ad-3791">Non</span><span class="sxs-lookup"><span data-stu-id="319ad-3791">No</span></span>


### <a name="definition"></a><span data-ttu-id="319ad-3792">Définition</span><span class="sxs-lookup"><span data-stu-id="319ad-3792">Definition</span></span>

<span data-ttu-id="319ad-3793">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="319ad-3793">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="319ad-3794">La fonction Func_ssn trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="319ad-3794">The function Func_ssn finds content that matches the pattern.</span></span>
- <span data-ttu-id="319ad-3795">Un mot clé figurant dans la liste Keyword_ssn est trouvé.</span><span class="sxs-lookup"><span data-stu-id="319ad-3795">A keyword from Keyword_ssn is found.</span></span>

<span data-ttu-id="319ad-3796">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="319ad-3796">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="319ad-3797">La fonction Func_unformatted_ssn trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="319ad-3797">The function Func_unformatted_ssn finds content that matches the pattern.</span></span>
- <span data-ttu-id="319ad-3798">Un mot clé figurant dans la liste Keyword_ssn est trouvé.</span><span class="sxs-lookup"><span data-stu-id="319ad-3798">A keyword from Keyword_ssn is found.</span></span>

<span data-ttu-id="319ad-3799">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 65 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="319ad-3799">A DLP policy is 65% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="319ad-3800">La fonction Func_randomized_formatted_ssn trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="319ad-3800">The function Func_randomized_formatted_ssn finds content that matches the pattern.</span></span>
- <span data-ttu-id="319ad-3801">Un mot clé figurant dans la liste Keyword_ssn est trouvé.</span><span class="sxs-lookup"><span data-stu-id="319ad-3801">A keyword from Keyword_ssn is found.</span></span>

<span data-ttu-id="319ad-3802">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 55 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="319ad-3802">A DLP policy is 55% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="319ad-3803">La fonction Func_randomized_unformatted_ssn trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="319ad-3803">The function Func_randomized_unformatted_ssn finds content that matches the pattern.</span></span>
- <span data-ttu-id="319ad-3804">Un mot clé figurant dans la liste Keyword_ssn est trouvé.</span><span class="sxs-lookup"><span data-stu-id="319ad-3804">A keyword from Keyword_ssn is found.</span></span>


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

### <a name="keywords"></a><span data-ttu-id="319ad-3805">Mots-clés</span><span class="sxs-lookup"><span data-stu-id="319ad-3805">Keywords</span></span>

#### <a name="keyword_ssn"></a><span data-ttu-id="319ad-3806">Keyword_ssn</span><span class="sxs-lookup"><span data-stu-id="319ad-3806">Keyword_ssn</span></span>

- <span data-ttu-id="319ad-3807">Sécurité sociale</span><span class="sxs-lookup"><span data-stu-id="319ad-3807">Social Security</span></span> 
- <span data-ttu-id="319ad-3808"># sécurité sociale</span><span class="sxs-lookup"><span data-stu-id="319ad-3808">Social Security#</span></span> 
- <span data-ttu-id="319ad-3809">Sécu sociale</span><span class="sxs-lookup"><span data-stu-id="319ad-3809">Soc Sec</span></span> 
- <span data-ttu-id="319ad-3810">SSN</span><span class="sxs-lookup"><span data-stu-id="319ad-3810">SSN</span></span> 
- <span data-ttu-id="319ad-3811">NUMÉROS</span><span class="sxs-lookup"><span data-stu-id="319ad-3811">SSNS</span></span> 
- <span data-ttu-id="319ad-3812">SSN #</span><span class="sxs-lookup"><span data-stu-id="319ad-3812">SSN#</span></span> 
- <span data-ttu-id="319ad-3813">SOCIALE #</span><span class="sxs-lookup"><span data-stu-id="319ad-3813">SS#</span></span> 
- <span data-ttu-id="319ad-3814">Identifiant SSID</span><span class="sxs-lookup"><span data-stu-id="319ad-3814">SSID</span></span> 
   

