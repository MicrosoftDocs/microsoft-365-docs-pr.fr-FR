---
title: Éléments recherchés par les fonctions DLP
f1.keywords:
- NOCSH
ms.author: chrfox
author: chrfox
manager: laurawi
ms.date: 6/18/2016
audience: Admin
ms.topic: reference
ms.service: O365-seccomp
localization_priority: Normal
ms.collection:
- M365-security-compliance
search.appverid:
- MOE150
- MET150
ms.custom:
- seo-marvel-apr2020
description: Découvrez les fonctions de protection contre la perte de données (DLP), pour vous aider à comprendre le fonctionnement des types d’informations sensibles prédéfinis.
ms.openlocfilehash: 838277b2e30696cd00cfc30df49c1d5a29149d92
ms.sourcegitcommit: 973f5449784cb70ce5545bc3cf57bf1ce5209218
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/19/2020
ms.locfileid: "44819274"
---
# <a name="what-the-dlp-functions-look-for"></a><span data-ttu-id="af586-103">Éléments recherchés par les fonctions DLP</span><span class="sxs-lookup"><span data-stu-id="af586-103">What the DLP functions look for</span></span>

<span data-ttu-id="af586-p101">La protection contre la perte de données (DLP) inclut des types d’informations sensibles, tels que le numéro de carte de crédit et le numéro de carte de débit de l’Union européenne, qui sont prêts à être utilisés dans vos stratégies DLP. Ces types d’informations sensibles recherchent un modèle spécifique et le corroborent en veillant à l’adéquation de la mise en forme, en appliquant des sommes de contrôle et en recherchant des mots clés pertinents ou d’autres informations. Certaines de ces fonctionnalités sont effectuées par des fonctions internes. Par exemple, le type d’informations sensibles de numéro de carte de crédit utilise une fonction pour rechercher des dates mises en forme comme une date d’expiration, pour aider à confirmer qu’un numéro est un numéro de carte de crédit.</span><span class="sxs-lookup"><span data-stu-id="af586-p101">Data loss prevention (DLP) includes sensitive information types, such as Credit Card Number and EU Debit Card Number, which are ready for you to use in your DLP policies. These sensitive information types look for a specific pattern and corroborate it by ensuring proper formatting, enforcing checksums, and looking for relevant keywords or other information. Some of this functionality is performed by internal functions. For example, the Credit Card Number sensitive information type uses a function to look for dates formatted like an expiration date, to help corroborate that a number is a credit card number.</span></span>
  
<span data-ttu-id="af586-108">Cette rubrique explique ce que ces fonctions recherchent, pour vous aider à comprendre le fonctionnement des types d’informations sensibles prédéfinis.</span><span class="sxs-lookup"><span data-stu-id="af586-108">This topic explains what these functions look for, to help you understand how the predefined sensitive information types work.</span></span> <span data-ttu-id="af586-109">Pour plus d’informations, consultez la rubrique [informations sensibles type d’entité définitions](sensitive-information-type-entity-definitions.md)</span><span class="sxs-lookup"><span data-stu-id="af586-109">For more information, see [Sensitive information type entity definitions](sensitive-information-type-entity-definitions.md)</span></span>
  
## <a name="func_us_date"></a><span data-ttu-id="af586-110">Func_us_date</span><span class="sxs-lookup"><span data-stu-id="af586-110">Func_us_date</span></span>

<span data-ttu-id="af586-111">Cette fonction recherche une date au format couramment utilisé aux États-Unis. Cela inclut les formats « mois/jour/année », « mois-jour-année » et « mois de jour du mois ».</span><span class="sxs-lookup"><span data-stu-id="af586-111">This function looks for a date in the format commonly used in the U.S. This includes the formats "month/day/year", "month-day-year", and "month day year ".</span></span> <span data-ttu-id="af586-112">Les noms ou les abréviations des mois ne respectent pas la casse.</span><span class="sxs-lookup"><span data-stu-id="af586-112">The names or abbreviations of months are not case sensitive.</span></span> 
  
<span data-ttu-id="af586-113">Exemples :</span><span class="sxs-lookup"><span data-stu-id="af586-113">Examples:</span></span>
  
- <span data-ttu-id="af586-114">2 décembre 2016</span><span class="sxs-lookup"><span data-stu-id="af586-114">December 2, 2016</span></span>
    
- <span data-ttu-id="af586-115">2 décembre 2016</span><span class="sxs-lookup"><span data-stu-id="af586-115">Dec 2, 2016</span></span>
    
- <span data-ttu-id="af586-116">DEC 02 2016</span><span class="sxs-lookup"><span data-stu-id="af586-116">dec 02 2016</span></span>
    
- <span data-ttu-id="af586-117">12/2/2016</span><span class="sxs-lookup"><span data-stu-id="af586-117">12/2/2016</span></span>
    
- <span data-ttu-id="af586-118">12/02/16</span><span class="sxs-lookup"><span data-stu-id="af586-118">12/02/16</span></span>
    
- <span data-ttu-id="af586-119">Déc-2-2016</span><span class="sxs-lookup"><span data-stu-id="af586-119">Dec-2-2016</span></span>
    
- <span data-ttu-id="af586-120">12-2-16</span><span class="sxs-lookup"><span data-stu-id="af586-120">12-2-16</span></span>
    
<span data-ttu-id="af586-121">Noms de mois acceptés :</span><span class="sxs-lookup"><span data-stu-id="af586-121">Accepted month names:</span></span>
  
- <span data-ttu-id="af586-122">English</span><span class="sxs-lookup"><span data-stu-id="af586-122">English</span></span>
    
  - <span data-ttu-id="af586-123">Janvier, février, mars, avril, mai, juin, juillet, août, septembre, octobre, novembre, décembre</span><span class="sxs-lookup"><span data-stu-id="af586-123">January, February, march, April, may, June, July, August, September, October, November, December</span></span>
    
  - <span data-ttu-id="af586-124">Jan. fév. Mar. mai du 1er juillet aoû. septembre. Oct. nov. déc</span><span class="sxs-lookup"><span data-stu-id="af586-124">Jan. Feb. Mar. Apr. May June July Aug. Sept. Oct. Nov. Dec.</span></span>
    
## <a name="func_eu_date"></a><span data-ttu-id="af586-125">Func_eu_date</span><span class="sxs-lookup"><span data-stu-id="af586-125">Func_eu_date</span></span>

<span data-ttu-id="af586-p104">Cette fonction recherche une date au format couramment utilisé dans l’Union européenne (et la plupart des lieux, à l’exception des États-Unis). Cela inclut les formats de « jour/mois/année », « jour-mois-année » et « jour mois année ». Les noms ou les abréviations des mois ne respectent pas la casse.</span><span class="sxs-lookup"><span data-stu-id="af586-p104">This function looks for a date in the format commonly used in the E.U. (and most places outside the U.S.). This includes the formats "day/month/year", "day-month-year", and "day month year". The names or abbreviations of months are not case sensitive.</span></span>
  
<span data-ttu-id="af586-130">Exemples :</span><span class="sxs-lookup"><span data-stu-id="af586-130">Examples:</span></span>
  
- <span data-ttu-id="af586-131">2 déc 2016</span><span class="sxs-lookup"><span data-stu-id="af586-131">2 Dec 2016</span></span>
    
- <span data-ttu-id="af586-132">02 déc 2016</span><span class="sxs-lookup"><span data-stu-id="af586-132">02 dec 2016</span></span>
    
- <span data-ttu-id="af586-133">2 déc 16</span><span class="sxs-lookup"><span data-stu-id="af586-133">2 Dec 16</span></span>
    
- <span data-ttu-id="af586-134">2/12/2016</span><span class="sxs-lookup"><span data-stu-id="af586-134">2/12/2016</span></span>
    
- <span data-ttu-id="af586-135">02/12/16</span><span class="sxs-lookup"><span data-stu-id="af586-135">02/12/16</span></span>
    
- <span data-ttu-id="af586-136">2-déc-2016</span><span class="sxs-lookup"><span data-stu-id="af586-136">2-Dec-2016</span></span>
    
- <span data-ttu-id="af586-137">2-12-16</span><span class="sxs-lookup"><span data-stu-id="af586-137">2-12-16</span></span>
    
<span data-ttu-id="af586-138">Noms de mois acceptés :</span><span class="sxs-lookup"><span data-stu-id="af586-138">Accepted month names:</span></span>
  
- <span data-ttu-id="af586-139">English</span><span class="sxs-lookup"><span data-stu-id="af586-139">English</span></span>
    
  - <span data-ttu-id="af586-140">Janvier, février, mars, avril, mai, juin, juillet, août, septembre, octobre, novembre, décembre</span><span class="sxs-lookup"><span data-stu-id="af586-140">January, February, march, April, may, June, July, August, September, October, November, December</span></span>
    
  - <span data-ttu-id="af586-141">Jan. fév. Mar. mai du 1er juillet aoû. septembre. Oct. nov. déc</span><span class="sxs-lookup"><span data-stu-id="af586-141">Jan. Feb. Mar. Apr. May June July Aug. Sept. Oct. Nov. Dec.</span></span>
    
- <span data-ttu-id="af586-142">Dutch</span><span class="sxs-lookup"><span data-stu-id="af586-142">Dutch</span></span>
    
  - <span data-ttu-id="af586-143">januari, februari, maart, April, mei, juni, juli, augustus, September, ocktober, October, November, December</span><span class="sxs-lookup"><span data-stu-id="af586-143">januari, februari, maart, April, mei, juni, juli, augustus, September, ocktober, October, November, December</span></span>
    
  - <span data-ttu-id="af586-144">Jan fév maart avr Mei Jun Jul aoû Sep sept oct OKT nov déc</span><span class="sxs-lookup"><span data-stu-id="af586-144">jan feb maart apr mei jun jul aug sep sept oct okt nov dec</span></span>
    
- <span data-ttu-id="af586-145">French</span><span class="sxs-lookup"><span data-stu-id="af586-145">French</span></span>
    
  - <span data-ttu-id="af586-146">janvier, février, mars, avril, mai, juin juillet, août, septembre, octobre, novembre, décembre</span><span class="sxs-lookup"><span data-stu-id="af586-146">janvier, février, mars, avril, mai, juin juillet, août, septembre, octobre, novembre, décembre</span></span>
    
  - <span data-ttu-id="af586-147">janv.</span><span class="sxs-lookup"><span data-stu-id="af586-147">janv.</span></span> <span data-ttu-id="af586-148">févr.</span><span class="sxs-lookup"><span data-stu-id="af586-148">févr.</span></span> <span data-ttu-id="af586-149">mars avril Maï juin juil.</span><span class="sxs-lookup"><span data-stu-id="af586-149">mars avril mai juin juil.</span></span> <span data-ttu-id="af586-150">août sept.</span><span class="sxs-lookup"><span data-stu-id="af586-150">août sept.</span></span> <span data-ttu-id="af586-151">OPO.</span><span class="sxs-lookup"><span data-stu-id="af586-151">oct.</span></span> <span data-ttu-id="af586-152">novembre.</span><span class="sxs-lookup"><span data-stu-id="af586-152">nov.</span></span> <span data-ttu-id="af586-153">déc.</span><span class="sxs-lookup"><span data-stu-id="af586-153">déc.</span></span>
    
- <span data-ttu-id="af586-154">German</span><span class="sxs-lookup"><span data-stu-id="af586-154">German</span></span>
    
  - <span data-ttu-id="af586-155">jänuar, Februar, März, avril, mai, Juni Juli, août, septembre, oktober, novembre, Dezember</span><span class="sxs-lookup"><span data-stu-id="af586-155">jänuar, februar, märz, April, mai, juni juli, August, September, oktober, November, dezember</span></span>
    
  - <span data-ttu-id="af586-156">Jan./Jän.</span><span class="sxs-lookup"><span data-stu-id="af586-156">Jan./Jän.</span></span> <span data-ttu-id="af586-157">Fév. März avr. Maï Juni Juli aoû. sept. Okt.</span><span class="sxs-lookup"><span data-stu-id="af586-157">Feb. März Apr. Mai Juni Juli Aug. Sept. Okt.</span></span> <span data-ttu-id="af586-158">Nov. Dez.</span><span class="sxs-lookup"><span data-stu-id="af586-158">Nov. Dez.</span></span>
    
- <span data-ttu-id="af586-159">Italian</span><span class="sxs-lookup"><span data-stu-id="af586-159">Italian</span></span>
    
  - <span data-ttu-id="af586-160">gennaio, febbraio, marzo, aprile, maggio, giugno, luglio, agosto, settembre, ottobre, novembre, dicembre</span><span class="sxs-lookup"><span data-stu-id="af586-160">gennaio, febbraio, marzo, aprile, maggio, giugno, luglio, agosto, settembre, ottobre, novembre, dicembre</span></span>
    
  - <span data-ttu-id="af586-161">genn.</span><span class="sxs-lookup"><span data-stu-id="af586-161">genn.</span></span> <span data-ttu-id="af586-162">febbr.</span><span class="sxs-lookup"><span data-stu-id="af586-162">febbr.</span></span> <span data-ttu-id="af586-163">détériore.</span><span class="sxs-lookup"><span data-stu-id="af586-163">mar.</span></span> <span data-ttu-id="af586-164">avancé.</span><span class="sxs-lookup"><span data-stu-id="af586-164">apr.</span></span> <span data-ttu-id="af586-165">magg.</span><span class="sxs-lookup"><span data-stu-id="af586-165">magg.</span></span> <span data-ttu-id="af586-166">giugno luglio AG.</span><span class="sxs-lookup"><span data-stu-id="af586-166">giugno luglio ag.</span></span> <span data-ttu-id="af586-167">sett.</span><span class="sxs-lookup"><span data-stu-id="af586-167">sett.</span></span> <span data-ttu-id="af586-168">Verlag.</span><span class="sxs-lookup"><span data-stu-id="af586-168">ott.</span></span> <span data-ttu-id="af586-169">novembre.</span><span class="sxs-lookup"><span data-stu-id="af586-169">nov.</span></span> <span data-ttu-id="af586-170">DIC.</span><span class="sxs-lookup"><span data-stu-id="af586-170">dic.</span></span>
    
- <span data-ttu-id="af586-171">Portugais</span><span class="sxs-lookup"><span data-stu-id="af586-171">Portuguese</span></span>
    
  - <span data-ttu-id="af586-172">janeiro, fevereiro, março, marco, abril, maio, junho, julho, agosto, setembro, outubro, novembro, dezembro</span><span class="sxs-lookup"><span data-stu-id="af586-172">janeiro, fevereiro, março, marco, abril, maio, junho, julho, agosto, setembro, outubro, novembro, dezembro</span></span>
    
  - <span data-ttu-id="af586-173">Jan Fev Mar Abr mai Jun Jul a été défini sur le mois de novembre dez</span><span class="sxs-lookup"><span data-stu-id="af586-173">jan fev mar abr mai jun jul ago set out nov dez</span></span>
    
- <span data-ttu-id="af586-174">Spanish</span><span class="sxs-lookup"><span data-stu-id="af586-174">Spanish</span></span>
    
  - <span data-ttu-id="af586-175">enero, febrero, marzo, abril, mayo, junio, julio, agosto, septiembre, octubre, noviembre, diciembre</span><span class="sxs-lookup"><span data-stu-id="af586-175">enero, febrero, marzo, abril, mayo, junio, julio, agosto, septiembre, octubre, noviembre, diciembre</span></span>
    
  - <span data-ttu-id="af586-176">enero fév.</span><span class="sxs-lookup"><span data-stu-id="af586-176">enero feb.</span></span> <span data-ttu-id="af586-177">marzo abr.</span><span class="sxs-lookup"><span data-stu-id="af586-177">marzo abr.</span></span> <span data-ttu-id="af586-178">Mayo Jun.</span><span class="sxs-lookup"><span data-stu-id="af586-178">mayo jun.</span></span> <span data-ttu-id="af586-179">juil.</span><span class="sxs-lookup"><span data-stu-id="af586-179">jul.</span></span> <span data-ttu-id="af586-180">agosto sept./Set.</span><span class="sxs-lookup"><span data-stu-id="af586-180">agosto sept./set.</span></span> <span data-ttu-id="af586-181">OPO.</span><span class="sxs-lookup"><span data-stu-id="af586-181">oct.</span></span> <span data-ttu-id="af586-182">novembre.</span><span class="sxs-lookup"><span data-stu-id="af586-182">nov.</span></span> <span data-ttu-id="af586-183">DIC.</span><span class="sxs-lookup"><span data-stu-id="af586-183">dic.</span></span>
    
## <a name="func_eu_date1-deprecated"></a><span data-ttu-id="af586-184">Func_eu_date1 (déconseillée)</span><span class="sxs-lookup"><span data-stu-id="af586-184">Func_eu_date1 (deprecated)</span></span>

> [!NOTE]
> <span data-ttu-id="af586-185">Cette fonction est déconseillée, car elle prend en charge uniquement les noms de mois portugais, qui sont désormais inclus dans la `Func_eu_date` fonction ci-dessus.</span><span class="sxs-lookup"><span data-stu-id="af586-185">This function is deprecated because it supports only Portuguese month names, which are now included in the  `Func_eu_date` function above.</span></span> 
  
<span data-ttu-id="af586-186">Cette fonction recherche une date au format couramment utilisé en portugais.</span><span class="sxs-lookup"><span data-stu-id="af586-186">This function looks for a date in the format commonly used in Portuguese.</span></span> <span data-ttu-id="af586-187">Le format de cette fonction est le même que `Func_eu_date` , qui diffère uniquement dans la langue utilisée.</span><span class="sxs-lookup"><span data-stu-id="af586-187">The format for this function is the same as  `Func_eu_date`, differing only in the language used.</span></span>
  
<span data-ttu-id="af586-188">Exemples :</span><span class="sxs-lookup"><span data-stu-id="af586-188">Examples:</span></span>
  
- <span data-ttu-id="af586-189">2 dez 2016</span><span class="sxs-lookup"><span data-stu-id="af586-189">2 Dez 2016</span></span>
    
- <span data-ttu-id="af586-190">02 dez 2016</span><span class="sxs-lookup"><span data-stu-id="af586-190">02 dez 2016</span></span>
    
- <span data-ttu-id="af586-191">2 dez 16</span><span class="sxs-lookup"><span data-stu-id="af586-191">2 Dez 16</span></span>
    
- <span data-ttu-id="af586-192">2/12/2016</span><span class="sxs-lookup"><span data-stu-id="af586-192">2/12/2016</span></span>
    
- <span data-ttu-id="af586-193">02/12/16</span><span class="sxs-lookup"><span data-stu-id="af586-193">02/12/16</span></span>
    
- <span data-ttu-id="af586-194">2-dez-2016</span><span class="sxs-lookup"><span data-stu-id="af586-194">2-Dez-2016</span></span>
    
- <span data-ttu-id="af586-195">2-12-16</span><span class="sxs-lookup"><span data-stu-id="af586-195">2-12-16</span></span>
    
<span data-ttu-id="af586-196">Noms de mois acceptés :</span><span class="sxs-lookup"><span data-stu-id="af586-196">Accepted month names:</span></span>
  
- <span data-ttu-id="af586-197">Portugais</span><span class="sxs-lookup"><span data-stu-id="af586-197">Portuguese</span></span>
    
  - <span data-ttu-id="af586-198">janeiro, fevereiro, março, marco, abril, maio, junho, julho, agosto, setembro, outubro, novembro, dezembro</span><span class="sxs-lookup"><span data-stu-id="af586-198">janeiro, fevereiro, março, marco, abril, maio, junho, julho, agosto, setembro, outubro, novembro, dezembro</span></span>
    
  - <span data-ttu-id="af586-199">Jan Fev Mar Abr mai Jun Jul a été défini sur le mois de novembre dez</span><span class="sxs-lookup"><span data-stu-id="af586-199">jan fev mar abr mai jun jul ago set out nov dez</span></span>
    
## <a name="func_eu_date2-deprecated"></a><span data-ttu-id="af586-200">Func_eu_date2 (déconseillée)</span><span class="sxs-lookup"><span data-stu-id="af586-200">Func_eu_date2 (deprecated)</span></span>

> [!NOTE]
> <span data-ttu-id="af586-201">Cette fonction est déconseillée, car elle prend en charge uniquement les noms de mois néerlandais, qui sont désormais inclus dans la `Func_eu_date` fonction ci-dessus.</span><span class="sxs-lookup"><span data-stu-id="af586-201">This function is deprecated because it supports only Dutch month names, which are now included in the  `Func_eu_date` function above.</span></span> 
  
<span data-ttu-id="af586-202">Cette fonction recherche une date au format couramment utilisé en néerlandais.</span><span class="sxs-lookup"><span data-stu-id="af586-202">This function looks for a date in the format commonly used in Dutch.</span></span> <span data-ttu-id="af586-203">Le format de cette fonction est le même que `Func_eu_date` , qui diffère uniquement dans la langue utilisée.</span><span class="sxs-lookup"><span data-stu-id="af586-203">The format for this function is the same as  `Func_eu_date`, differing only in the language used.</span></span>
  
<span data-ttu-id="af586-204">Exemples :</span><span class="sxs-lookup"><span data-stu-id="af586-204">Examples:</span></span>
  
- <span data-ttu-id="af586-205">2 Mei 2016</span><span class="sxs-lookup"><span data-stu-id="af586-205">2 Mei 2016</span></span>
    
- <span data-ttu-id="af586-206">02 Mei 2016</span><span class="sxs-lookup"><span data-stu-id="af586-206">02 mei 2016</span></span>
    
- <span data-ttu-id="af586-207">2 Mei 16</span><span class="sxs-lookup"><span data-stu-id="af586-207">2 Mei 16</span></span>
    
- <span data-ttu-id="af586-208">2/12/2016</span><span class="sxs-lookup"><span data-stu-id="af586-208">2/12/2016</span></span>
    
- <span data-ttu-id="af586-209">02/12/16</span><span class="sxs-lookup"><span data-stu-id="af586-209">02/12/16</span></span>
    
- <span data-ttu-id="af586-210">2-Mei-2016</span><span class="sxs-lookup"><span data-stu-id="af586-210">2-Mei-2016</span></span>
    
- <span data-ttu-id="af586-211">2-12-16</span><span class="sxs-lookup"><span data-stu-id="af586-211">2-12-16</span></span>
    
<span data-ttu-id="af586-212">Noms de mois acceptés :</span><span class="sxs-lookup"><span data-stu-id="af586-212">Accepted month names:</span></span>
  
- <span data-ttu-id="af586-213">Dutch</span><span class="sxs-lookup"><span data-stu-id="af586-213">Dutch</span></span>
    
  - <span data-ttu-id="af586-214">januari, februari, maart, April, mei, juni, juli, augustus, September, ocktober, October, November, December</span><span class="sxs-lookup"><span data-stu-id="af586-214">januari, februari, maart, April, mei, juni, juli, augustus, September, ocktober, October, November, December</span></span>
    
  - <span data-ttu-id="af586-215">Jan fév maart avr Mei Jun Jul aoû Sep sept oct OKT nov déc</span><span class="sxs-lookup"><span data-stu-id="af586-215">jan feb maart apr mei jun jul aug sep sept oct okt nov dec</span></span>
    
## <a name="func_expiration_date"></a><span data-ttu-id="af586-216">Func_expiration_date</span><span class="sxs-lookup"><span data-stu-id="af586-216">Func_expiration_date</span></span>

<span data-ttu-id="af586-217">Cette fonction recherche une date dans les formats couramment utilisés par les cartes de crédit et de débit, qui excluent les jours au profit des mois.</span><span class="sxs-lookup"><span data-stu-id="af586-217">This function looks for a date in the formats commonly used by credit and debit cards, which exclude days in favor of months.</span></span> <span data-ttu-id="af586-218">Cette fonction correspond aux dates au format « mois/année », « mois-année », « [nom du mois] année » et « [abréviation mois-année] ».</span><span class="sxs-lookup"><span data-stu-id="af586-218">This function will match dates in format of "month/year", "month-year", "[month name] year", and "[month abbreviation] year".</span></span> <span data-ttu-id="af586-219">Les noms ou les abréviations des mois ne respectent pas la casse.</span><span class="sxs-lookup"><span data-stu-id="af586-219">The names or abbreviations of months are not case sensitive.</span></span>
  
<span data-ttu-id="af586-220">Exemples :</span><span class="sxs-lookup"><span data-stu-id="af586-220">Examples:</span></span>
  
- <span data-ttu-id="af586-221">MM/AA, par exemple, 01/11 ou 1/11</span><span class="sxs-lookup"><span data-stu-id="af586-221">MM/YY -- for example, 01/11 or 1/11</span></span>
    
- <span data-ttu-id="af586-222">MM/AAAA, par exemple, 01/2011 ou 1/2011</span><span class="sxs-lookup"><span data-stu-id="af586-222">MM/YYYY -- for example, 01/2011 or 1/2011</span></span>
    
- <span data-ttu-id="af586-223">MM-AA, par exemple, 01-22 ou 1-11</span><span class="sxs-lookup"><span data-stu-id="af586-223">MM-YY -- for example, 01-22 or 1-11</span></span>
    
- <span data-ttu-id="af586-224">MM-AAAA, par exemple, 01-2000 ou 1-2000</span><span class="sxs-lookup"><span data-stu-id="af586-224">MM-YYYY -- for example, 01-2000 or 1-2000</span></span>
    
<span data-ttu-id="af586-225">Les formats suivants prennent en charge AA ou AAAA :</span><span class="sxs-lookup"><span data-stu-id="af586-225">The following formats support YY or YYYY:</span></span>
  
- <span data-ttu-id="af586-226">Mois-AAAA, par exemple, jan-2010, janvier-2010, jan-10 ou janvier-10</span><span class="sxs-lookup"><span data-stu-id="af586-226">Month-YYYY -- for example, .Jan-2010 or january-2010 or Jan-10 or january-10</span></span>
    
- <span data-ttu-id="af586-227">Mois AAAA, par exemple, « janvier 2010 », « jan 2010 », « janvier 10 » ou « jan 10 »</span><span class="sxs-lookup"><span data-stu-id="af586-227">Month YYYY -- for example, 'january 2010' or 'Jan 2010' or 'january 10' or 'Jan 10'</span></span>
    
- <span data-ttu-id="af586-228">MoisAAAA, par exemple, « janvier2010 », « jan2010 », « janvier10 » ou « jan10 »</span><span class="sxs-lookup"><span data-stu-id="af586-228">MonthYYYY -- for example, 'january2010' or 'Jan2010' or 'january10' or 'Jan10'</span></span>
    
- <span data-ttu-id="af586-229">Mois/aaaa--par exemple, « janvier/2010 » ou « Jan/2010 », « janvier/10 » ou « Jan/10 »</span><span class="sxs-lookup"><span data-stu-id="af586-229">Month/YYYY -- for example, 'january/2010' or 'Jan/2010' or 'january/10' or 'Jan/10'</span></span>
    
<span data-ttu-id="af586-230">Noms de mois acceptés :</span><span class="sxs-lookup"><span data-stu-id="af586-230">Accepted month names:</span></span>
  
- <span data-ttu-id="af586-231">English</span><span class="sxs-lookup"><span data-stu-id="af586-231">English</span></span>
    
  - <span data-ttu-id="af586-232">Janvier, février, mars, avril, mai, juin, juillet, août, septembre, octobre, novembre, décembre</span><span class="sxs-lookup"><span data-stu-id="af586-232">January, February, march, April, may, June, July, August, September, October, November, December</span></span>
    
  - <span data-ttu-id="af586-233">Jan Fév Mar Avr mai juin septembre sept octobre déc</span><span class="sxs-lookup"><span data-stu-id="af586-233">Jan Feb Mar Apr May June July Aug Sept Oct Nov Dec</span></span>
    
## <a name="func_us_address"></a><span data-ttu-id="af586-234">Func_us_address</span><span class="sxs-lookup"><span data-stu-id="af586-234">Func_us_address</span></span>

<span data-ttu-id="af586-p112">Cette fonction recherche un nom d’état américain ou son abréviation postale, suivi d’un code postal valide, au format utilisé dans les adresses postales. Le code postal doit être l’un des codes postaux corrects qui sont associés au nom de l’état américain ou à son abréviation. Le nom de l’état américain et le code postal ne doivent pas être séparés par des signes de ponctuation ou des lettres.</span><span class="sxs-lookup"><span data-stu-id="af586-p112">This function looks for a U.S. state name or postal abbreviation followed by a valid zip code, just as they are used in postal addresses. The zip code must be one of the correct zip codes associated with the U.S. state name or abbreviation. The U.S. state name and zip code cannot be separated by punctuation or letters.</span></span>
  
<span data-ttu-id="af586-238">Exemples :</span><span class="sxs-lookup"><span data-stu-id="af586-238">Examples:</span></span>
  
- <span data-ttu-id="af586-239">Washington 98052</span><span class="sxs-lookup"><span data-stu-id="af586-239">Washington 98052</span></span>
    
- <span data-ttu-id="af586-240">Washington 98052-9998</span><span class="sxs-lookup"><span data-stu-id="af586-240">Washington 98052-9998</span></span>
    
- <span data-ttu-id="af586-241">WA 98052</span><span class="sxs-lookup"><span data-stu-id="af586-241">WA 98052</span></span>
    
- <span data-ttu-id="af586-242">WA 98052-9998</span><span class="sxs-lookup"><span data-stu-id="af586-242">WA 98052-9998</span></span>
    

