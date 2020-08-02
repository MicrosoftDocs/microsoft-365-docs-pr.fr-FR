---
title: Les fonctions de protection contre la perte de données (DLP)
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
description: Découvrez les fonctions de protection contre la perte de données (DLP).
ms.openlocfilehash: ef87be7dde83b1e5ba12456e7801e0554bceb6ea
ms.sourcegitcommit: cfb0c50f1366736cdf031a75f0608246b5640d93
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/31/2020
ms.locfileid: "46536309"
---
# <a name="what-the-dlp-functions-look-for"></a><span data-ttu-id="c7160-103">Éléments recherchés par les fonctions DLP</span><span class="sxs-lookup"><span data-stu-id="c7160-103">What the DLP functions look for</span></span>

<span data-ttu-id="c7160-104">La protection contre la perte de données (DLP) inclut des types d’informations sensibles, tels que le numéro de carte de crédit et le numéro de carte de crédit intracommunautaire, qui sont prêts à être utilisés dans vos stratégies DLP.</span><span class="sxs-lookup"><span data-stu-id="c7160-104">Data loss prevention (DLP) includes sensitive information types, such as credit card Number and EU Debit card number, which are ready for you to use in your DLP policies.</span></span> <span data-ttu-id="c7160-105">Ces types d’informations sensibles recherchent un modèle spécifique et le corroborent en veillant à l’adéquation de la mise en forme, en appliquant des sommes de contrôle et en recherchant des mots clés pertinents ou d’autres informations.</span><span class="sxs-lookup"><span data-stu-id="c7160-105">These sensitive information types look for a specific pattern and corroborate it by ensuring proper formatting, enforcing checksums, and looking for relevant keywords or other information.</span></span> <span data-ttu-id="c7160-106">Certaines de ces fonctionnalités sont effectuées par des fonctions internes.</span><span class="sxs-lookup"><span data-stu-id="c7160-106">Some of this functionality is performed by internal functions.</span></span> <span data-ttu-id="c7160-107">Par exemple, le type d’informations sensibles de numéro de carte de crédit utilise une fonction pour rechercher des dates mises en forme comme une date d’expiration, pour aider à confirmer qu’un numéro est un numéro de carte de crédit.</span><span class="sxs-lookup"><span data-stu-id="c7160-107">For example, the Credit Card Number sensitive information type uses a function to look for dates formatted like an expiration date, to help corroborate that a number is a credit card number.</span></span>
  
<span data-ttu-id="c7160-108">Cet article explique ce que ces fonctions recherchent, pour vous aider à comprendre le fonctionnement des types d’informations sensibles prédéfinis.</span><span class="sxs-lookup"><span data-stu-id="c7160-108">This article explains what these functions look for, to help you understand how the predefined sensitive information types work.</span></span> <span data-ttu-id="c7160-109">Pour plus d’informations, consultez la rubrique [informations sensibles type d’entité définitions](sensitive-information-type-entity-definitions.md)</span><span class="sxs-lookup"><span data-stu-id="c7160-109">For more information, see [Sensitive information type entity definitions](sensitive-information-type-entity-definitions.md)</span></span>
  
## <a name="func_us_date"></a><span data-ttu-id="c7160-110">Func_us_date</span><span class="sxs-lookup"><span data-stu-id="c7160-110">Func_us_date</span></span>

<span data-ttu-id="c7160-111">Cette fonction recherche une date au format couramment utilisé aux États-Unis. Cela inclut les formats « mois/jour/année », « mois-jour-année » et « mois de jour du mois ».</span><span class="sxs-lookup"><span data-stu-id="c7160-111">This function looks for a date in the format commonly used in the U.S. This includes the formats "month/day/year", "month-day-year", and "month day year ".</span></span> <span data-ttu-id="c7160-112">Les noms ou les abréviations des mois ne respectent pas la casse.</span><span class="sxs-lookup"><span data-stu-id="c7160-112">The names or abbreviations of months are not case sensitive.</span></span> 
  
<span data-ttu-id="c7160-113">Exemples :</span><span class="sxs-lookup"><span data-stu-id="c7160-113">Examples:</span></span>
  
- <span data-ttu-id="c7160-114">2 décembre 2016</span><span class="sxs-lookup"><span data-stu-id="c7160-114">December 2, 2016</span></span>
    
- <span data-ttu-id="c7160-115">2 décembre 2016</span><span class="sxs-lookup"><span data-stu-id="c7160-115">Dec 2, 2016</span></span>
    
- <span data-ttu-id="c7160-116">DEC 02 2016</span><span class="sxs-lookup"><span data-stu-id="c7160-116">dec 02 2016</span></span>
    
- <span data-ttu-id="c7160-117">12/2/2016</span><span class="sxs-lookup"><span data-stu-id="c7160-117">12/2/2016</span></span>
    
- <span data-ttu-id="c7160-118">12/02/16</span><span class="sxs-lookup"><span data-stu-id="c7160-118">12/02/16</span></span>
    
- <span data-ttu-id="c7160-119">Déc-2-2016</span><span class="sxs-lookup"><span data-stu-id="c7160-119">Dec-2-2016</span></span>
    
- <span data-ttu-id="c7160-120">12-2-16</span><span class="sxs-lookup"><span data-stu-id="c7160-120">12-2-16</span></span>
    
<span data-ttu-id="c7160-121">Noms de mois acceptés :</span><span class="sxs-lookup"><span data-stu-id="c7160-121">Accepted month names:</span></span>
  
- <span data-ttu-id="c7160-122">English</span><span class="sxs-lookup"><span data-stu-id="c7160-122">English</span></span>
    
  - <span data-ttu-id="c7160-123">Janvier, février, mars, avril, mai, juin, juillet, août, septembre, octobre, novembre, décembre</span><span class="sxs-lookup"><span data-stu-id="c7160-123">January, February, march, April, may, June, July, August, September, October, November, December</span></span>
    
  - <span data-ttu-id="c7160-124">Jan. fév. Mar. mai du 1er juillet aoû. septembre. Oct. nov. déc</span><span class="sxs-lookup"><span data-stu-id="c7160-124">Jan. Feb. Mar. Apr. May June July Aug. Sept. Oct. Nov. Dec.</span></span>
    
## <a name="func_eu_date"></a><span data-ttu-id="c7160-125">Func_eu_date</span><span class="sxs-lookup"><span data-stu-id="c7160-125">Func_eu_date</span></span>

<span data-ttu-id="c7160-126">Cette fonction recherche une date au format couramment utilisé dans l’Union européenne</span><span class="sxs-lookup"><span data-stu-id="c7160-126">This function looks for a date in the format commonly used in the E.U.</span></span> <span data-ttu-id="c7160-127">(et la plupart des emplacements en dehors des États-Unis), tels que « jour/mois/année », « jour-mois-année » et « jour mois année ».</span><span class="sxs-lookup"><span data-stu-id="c7160-127">(and most places outside the U.S.), such as "day/month/year", "day-month-year", and "day month year".</span></span> <span data-ttu-id="c7160-128">Les noms ou les abréviations des mois ne respectent pas la casse.</span><span class="sxs-lookup"><span data-stu-id="c7160-128">The names or abbreviations of months are not case sensitive.</span></span>
  
<span data-ttu-id="c7160-129">Exemples :</span><span class="sxs-lookup"><span data-stu-id="c7160-129">Examples:</span></span>
  
- <span data-ttu-id="c7160-130">2 déc 2016</span><span class="sxs-lookup"><span data-stu-id="c7160-130">2 Dec 2016</span></span>
    
- <span data-ttu-id="c7160-131">02 déc 2016</span><span class="sxs-lookup"><span data-stu-id="c7160-131">02 dec 2016</span></span>
    
- <span data-ttu-id="c7160-132">2 déc 16</span><span class="sxs-lookup"><span data-stu-id="c7160-132">2 Dec 16</span></span>
    
- <span data-ttu-id="c7160-133">2/12/2016</span><span class="sxs-lookup"><span data-stu-id="c7160-133">2/12/2016</span></span>
    
- <span data-ttu-id="c7160-134">02/12/16</span><span class="sxs-lookup"><span data-stu-id="c7160-134">02/12/16</span></span>
    
- <span data-ttu-id="c7160-135">2-déc-2016</span><span class="sxs-lookup"><span data-stu-id="c7160-135">2-Dec-2016</span></span>
    
- <span data-ttu-id="c7160-136">2-12-16</span><span class="sxs-lookup"><span data-stu-id="c7160-136">2-12-16</span></span>
    
<span data-ttu-id="c7160-137">Noms de mois acceptés :</span><span class="sxs-lookup"><span data-stu-id="c7160-137">Accepted month names:</span></span>
  
- <span data-ttu-id="c7160-138">English</span><span class="sxs-lookup"><span data-stu-id="c7160-138">English</span></span>
    
  - <span data-ttu-id="c7160-139">Janvier, février, mars, avril, mai, juin, juillet, août, septembre, octobre, novembre, décembre</span><span class="sxs-lookup"><span data-stu-id="c7160-139">January, February, march, April, may, June, July, August, September, October, November, December</span></span>
    
  - <span data-ttu-id="c7160-140">Jan. fév. Mar. mai du 1er juillet aoû. septembre. Oct. nov. déc</span><span class="sxs-lookup"><span data-stu-id="c7160-140">Jan. Feb. Mar. Apr. May June July Aug. Sept. Oct. Nov. Dec.</span></span>
    
- <span data-ttu-id="c7160-141">Dutch</span><span class="sxs-lookup"><span data-stu-id="c7160-141">Dutch</span></span>
    
  - <span data-ttu-id="c7160-142">januari, februari, maart, April, mei, juni, juli, augustus, September, ocktober, October, November, December</span><span class="sxs-lookup"><span data-stu-id="c7160-142">januari, februari, maart, April, mei, juni, juli, augustus, September, ocktober, October, November, December</span></span>
    
  - <span data-ttu-id="c7160-143">Jan fév maart avr Mei Jun Jul aoû Sep sept oct OKT nov déc</span><span class="sxs-lookup"><span data-stu-id="c7160-143">jan feb maart apr mei jun jul aug sep sept oct okt nov dec</span></span>
    
- <span data-ttu-id="c7160-144">French</span><span class="sxs-lookup"><span data-stu-id="c7160-144">French</span></span>
    
  - <span data-ttu-id="c7160-145">janvier, février, mars, avril, mai, juin juillet, août, septembre, octobre, novembre, décembre</span><span class="sxs-lookup"><span data-stu-id="c7160-145">janvier, février, mars, avril, mai, juin juillet, août, septembre, octobre, novembre, décembre</span></span>
    
  - <span data-ttu-id="c7160-146">janv.</span><span class="sxs-lookup"><span data-stu-id="c7160-146">janv.</span></span> <span data-ttu-id="c7160-147">févr.</span><span class="sxs-lookup"><span data-stu-id="c7160-147">févr.</span></span> <span data-ttu-id="c7160-148">mars avril Maï juin juil.</span><span class="sxs-lookup"><span data-stu-id="c7160-148">mars avril mai juin juil.</span></span> <span data-ttu-id="c7160-149">août sept.</span><span class="sxs-lookup"><span data-stu-id="c7160-149">août sept.</span></span> <span data-ttu-id="c7160-150">OPO.</span><span class="sxs-lookup"><span data-stu-id="c7160-150">oct.</span></span> <span data-ttu-id="c7160-151">novembre.</span><span class="sxs-lookup"><span data-stu-id="c7160-151">nov.</span></span> <span data-ttu-id="c7160-152">déc.</span><span class="sxs-lookup"><span data-stu-id="c7160-152">déc.</span></span>
    
- <span data-ttu-id="c7160-153">German</span><span class="sxs-lookup"><span data-stu-id="c7160-153">German</span></span>
    
  - <span data-ttu-id="c7160-154">jänuar, Februar, März, avril, mai, Juni Juli, août, septembre, oktober, novembre, Dezember</span><span class="sxs-lookup"><span data-stu-id="c7160-154">jänuar, februar, märz, April, mai, juni juli, August, September, oktober, November, dezember</span></span>
    
  - <span data-ttu-id="c7160-155">Jan./Jän.</span><span class="sxs-lookup"><span data-stu-id="c7160-155">Jan./Jän.</span></span> <span data-ttu-id="c7160-156">Fév. März avr. Maï Juni Juli aoû. sept. Okt.</span><span class="sxs-lookup"><span data-stu-id="c7160-156">Feb. März Apr. Mai Juni Juli Aug. Sept. Okt.</span></span> <span data-ttu-id="c7160-157">Nov. Dez.</span><span class="sxs-lookup"><span data-stu-id="c7160-157">Nov. Dez.</span></span>
    
- <span data-ttu-id="c7160-158">Italian</span><span class="sxs-lookup"><span data-stu-id="c7160-158">Italian</span></span>
    
  - <span data-ttu-id="c7160-159">gennaio, febbraio, marzo, aprile, maggio, giugno, luglio, agosto, settembre, ottobre, novembre, dicembre</span><span class="sxs-lookup"><span data-stu-id="c7160-159">gennaio, febbraio, marzo, aprile, maggio, giugno, luglio, agosto, settembre, ottobre, novembre, dicembre</span></span>
    
  - <span data-ttu-id="c7160-160">genn.</span><span class="sxs-lookup"><span data-stu-id="c7160-160">genn.</span></span> <span data-ttu-id="c7160-161">febbr.</span><span class="sxs-lookup"><span data-stu-id="c7160-161">febbr.</span></span> <span data-ttu-id="c7160-162">détériore.</span><span class="sxs-lookup"><span data-stu-id="c7160-162">mar.</span></span> <span data-ttu-id="c7160-163">avancé.</span><span class="sxs-lookup"><span data-stu-id="c7160-163">apr.</span></span> <span data-ttu-id="c7160-164">magg.</span><span class="sxs-lookup"><span data-stu-id="c7160-164">magg.</span></span> <span data-ttu-id="c7160-165">giugno luglio AG.</span><span class="sxs-lookup"><span data-stu-id="c7160-165">giugno luglio ag.</span></span> <span data-ttu-id="c7160-166">sett.</span><span class="sxs-lookup"><span data-stu-id="c7160-166">sett.</span></span> <span data-ttu-id="c7160-167">Verlag.</span><span class="sxs-lookup"><span data-stu-id="c7160-167">ott.</span></span> <span data-ttu-id="c7160-168">novembre.</span><span class="sxs-lookup"><span data-stu-id="c7160-168">nov.</span></span> <span data-ttu-id="c7160-169">DIC.</span><span class="sxs-lookup"><span data-stu-id="c7160-169">dic.</span></span>
    
- <span data-ttu-id="c7160-170">Portugais</span><span class="sxs-lookup"><span data-stu-id="c7160-170">Portuguese</span></span>
    
  - <span data-ttu-id="c7160-171">janeiro, fevereiro, março, marco, abril, maio, junho, julho, agosto, setembro, outubro, novembro, dezembro</span><span class="sxs-lookup"><span data-stu-id="c7160-171">janeiro, fevereiro, março, marco, abril, maio, junho, julho, agosto, setembro, outubro, novembro, dezembro</span></span>
    
  - <span data-ttu-id="c7160-172">Jan Fev Mar Abr mai Jun Jul a été défini sur le mois de novembre dez</span><span class="sxs-lookup"><span data-stu-id="c7160-172">jan fev mar abr mai jun jul ago set out nov dez</span></span>
    
- <span data-ttu-id="c7160-173">Spanish</span><span class="sxs-lookup"><span data-stu-id="c7160-173">Spanish</span></span>
    
  - <span data-ttu-id="c7160-174">enero, febrero, marzo, abril, mayo, junio, julio, agosto, septiembre, octubre, noviembre, diciembre</span><span class="sxs-lookup"><span data-stu-id="c7160-174">enero, febrero, marzo, abril, mayo, junio, julio, agosto, septiembre, octubre, noviembre, diciembre</span></span>
    
  - <span data-ttu-id="c7160-175">enero fév.</span><span class="sxs-lookup"><span data-stu-id="c7160-175">enero feb.</span></span> <span data-ttu-id="c7160-176">marzo abr.</span><span class="sxs-lookup"><span data-stu-id="c7160-176">marzo abr.</span></span> <span data-ttu-id="c7160-177">Mayo Jun.</span><span class="sxs-lookup"><span data-stu-id="c7160-177">mayo jun.</span></span> <span data-ttu-id="c7160-178">juil.</span><span class="sxs-lookup"><span data-stu-id="c7160-178">jul.</span></span> <span data-ttu-id="c7160-179">agosto sept./Set.</span><span class="sxs-lookup"><span data-stu-id="c7160-179">agosto sept./set.</span></span> <span data-ttu-id="c7160-180">OPO.</span><span class="sxs-lookup"><span data-stu-id="c7160-180">oct.</span></span> <span data-ttu-id="c7160-181">novembre.</span><span class="sxs-lookup"><span data-stu-id="c7160-181">nov.</span></span> <span data-ttu-id="c7160-182">DIC.</span><span class="sxs-lookup"><span data-stu-id="c7160-182">dic.</span></span>
    
## <a name="func_eu_date1-deprecated"></a><span data-ttu-id="c7160-183">Func_eu_date1 (déconseillée)</span><span class="sxs-lookup"><span data-stu-id="c7160-183">Func_eu_date1 (deprecated)</span></span>

> [!NOTE]
> <span data-ttu-id="c7160-184">Cette fonction est déconseillée, car elle prend en charge uniquement les noms de mois portugais, qui sont désormais inclus dans la `Func_eu_date` fonction ci-dessus.</span><span class="sxs-lookup"><span data-stu-id="c7160-184">This function is deprecated because it supports only Portuguese month names, which are now included in the  `Func_eu_date` function above.</span></span> 
  
<span data-ttu-id="c7160-185">Cette fonction recherche une date au format couramment utilisé en portugais.</span><span class="sxs-lookup"><span data-stu-id="c7160-185">This function looks for a date in the format commonly used in Portuguese.</span></span> <span data-ttu-id="c7160-186">Le format de cette fonction est le même que `Func_eu_date` , qui diffère uniquement dans la langue utilisée.</span><span class="sxs-lookup"><span data-stu-id="c7160-186">The format for this function is the same as  `Func_eu_date`, differing only in the language used.</span></span>
  
<span data-ttu-id="c7160-187">Exemples :</span><span class="sxs-lookup"><span data-stu-id="c7160-187">Examples:</span></span>
  
- <span data-ttu-id="c7160-188">2 dez 2016</span><span class="sxs-lookup"><span data-stu-id="c7160-188">2 Dez 2016</span></span>
    
- <span data-ttu-id="c7160-189">02 dez 2016</span><span class="sxs-lookup"><span data-stu-id="c7160-189">02 dez 2016</span></span>
    
- <span data-ttu-id="c7160-190">2 dez 16</span><span class="sxs-lookup"><span data-stu-id="c7160-190">2 Dez 16</span></span>
    
- <span data-ttu-id="c7160-191">2/12/2016</span><span class="sxs-lookup"><span data-stu-id="c7160-191">2/12/2016</span></span>
    
- <span data-ttu-id="c7160-192">02/12/16</span><span class="sxs-lookup"><span data-stu-id="c7160-192">02/12/16</span></span>
    
- <span data-ttu-id="c7160-193">2-dez-2016</span><span class="sxs-lookup"><span data-stu-id="c7160-193">2-Dez-2016</span></span>
    
- <span data-ttu-id="c7160-194">2-12-16</span><span class="sxs-lookup"><span data-stu-id="c7160-194">2-12-16</span></span>
    
<span data-ttu-id="c7160-195">Noms de mois acceptés :</span><span class="sxs-lookup"><span data-stu-id="c7160-195">Accepted month names:</span></span>
  
- <span data-ttu-id="c7160-196">Portugais</span><span class="sxs-lookup"><span data-stu-id="c7160-196">Portuguese</span></span>
    
  - <span data-ttu-id="c7160-197">janeiro, fevereiro, março, marco, abril, maio, junho, julho, agosto, setembro, outubro, novembro, dezembro</span><span class="sxs-lookup"><span data-stu-id="c7160-197">janeiro, fevereiro, março, marco, abril, maio, junho, julho, agosto, setembro, outubro, novembro, dezembro</span></span>
    
  - <span data-ttu-id="c7160-198">Jan Fev Mar Abr mai Jun Jul a été défini sur le mois de novembre dez</span><span class="sxs-lookup"><span data-stu-id="c7160-198">jan fev mar abr mai jun jul ago set out nov dez</span></span>
    
## <a name="func_eu_date2-deprecated"></a><span data-ttu-id="c7160-199">Func_eu_date2 (déconseillée)</span><span class="sxs-lookup"><span data-stu-id="c7160-199">Func_eu_date2 (deprecated)</span></span>

> [!NOTE]
> <span data-ttu-id="c7160-200">Cette fonction est déconseillée, car elle prend en charge uniquement les noms de mois néerlandais, qui sont désormais inclus dans la `Func_eu_date` fonction ci-dessus.</span><span class="sxs-lookup"><span data-stu-id="c7160-200">This function is deprecated because it supports only Dutch month names, which are now included in the  `Func_eu_date` function above.</span></span> 
  
<span data-ttu-id="c7160-201">Cette fonction recherche une date au format couramment utilisé en néerlandais.</span><span class="sxs-lookup"><span data-stu-id="c7160-201">This function looks for a date in the format commonly used in Dutch.</span></span> <span data-ttu-id="c7160-202">Le format de cette fonction est le même que `Func_eu_date` , qui diffère uniquement dans la langue utilisée.</span><span class="sxs-lookup"><span data-stu-id="c7160-202">The format for this function is the same as  `Func_eu_date`, differing only in the language used.</span></span>
  
<span data-ttu-id="c7160-203">Exemples :</span><span class="sxs-lookup"><span data-stu-id="c7160-203">Examples:</span></span>
  
- <span data-ttu-id="c7160-204">2 Mei 2016</span><span class="sxs-lookup"><span data-stu-id="c7160-204">2 Mei 2016</span></span>
    
- <span data-ttu-id="c7160-205">02 Mei 2016</span><span class="sxs-lookup"><span data-stu-id="c7160-205">02 mei 2016</span></span>
    
- <span data-ttu-id="c7160-206">2 Mei 16</span><span class="sxs-lookup"><span data-stu-id="c7160-206">2 Mei 16</span></span>
    
- <span data-ttu-id="c7160-207">2/12/2016</span><span class="sxs-lookup"><span data-stu-id="c7160-207">2/12/2016</span></span>
    
- <span data-ttu-id="c7160-208">02/12/16</span><span class="sxs-lookup"><span data-stu-id="c7160-208">02/12/16</span></span>
    
- <span data-ttu-id="c7160-209">2-Mei-2016</span><span class="sxs-lookup"><span data-stu-id="c7160-209">2-Mei-2016</span></span>
    
- <span data-ttu-id="c7160-210">2-12-16</span><span class="sxs-lookup"><span data-stu-id="c7160-210">2-12-16</span></span>
    
<span data-ttu-id="c7160-211">Noms de mois acceptés :</span><span class="sxs-lookup"><span data-stu-id="c7160-211">Accepted month names:</span></span>
  
- <span data-ttu-id="c7160-212">Dutch</span><span class="sxs-lookup"><span data-stu-id="c7160-212">Dutch</span></span>
    
  - <span data-ttu-id="c7160-213">januari, februari, maart, April, mei, juni, juli, augustus, September, ocktober, October, November, December</span><span class="sxs-lookup"><span data-stu-id="c7160-213">januari, februari, maart, April, mei, juni, juli, augustus, September, ocktober, October, November, December</span></span>
    
  - <span data-ttu-id="c7160-214">Jan fév maart avr Mei Jun Jul aoû Sep sept parti OKT nov déc</span><span class="sxs-lookup"><span data-stu-id="c7160-214">jan feb maart apr mei jun jul aug sep sept out okt nov dec</span></span>
    
## <a name="func_expiration_date"></a><span data-ttu-id="c7160-215">Func_expiration_date</span><span class="sxs-lookup"><span data-stu-id="c7160-215">Func_expiration_date</span></span>

<span data-ttu-id="c7160-216">Cette fonction recherche une date dans les formats couramment utilisés par les cartes de crédit et de débit, qui excluent les jours au profit des mois.</span><span class="sxs-lookup"><span data-stu-id="c7160-216">This function looks for a date in the formats commonly used by credit and debit cards, which exclude days in favor of months.</span></span> <span data-ttu-id="c7160-217">Cette fonction correspond aux dates au format « mois/année », « mois-année », « [nom du mois] année » et « [abréviation mois-année] ».</span><span class="sxs-lookup"><span data-stu-id="c7160-217">This function will match dates in format of "month/year", "month-year", "[month name] year", and "[month abbreviation] year".</span></span> <span data-ttu-id="c7160-218">Les noms ou les abréviations des mois ne respectent pas la casse.</span><span class="sxs-lookup"><span data-stu-id="c7160-218">The names or abbreviations of months are not case sensitive.</span></span>
  
<span data-ttu-id="c7160-219">Exemples :</span><span class="sxs-lookup"><span data-stu-id="c7160-219">Examples:</span></span>
  
- <span data-ttu-id="c7160-220">MM/AA, par exemple, 01/11 ou 1/11</span><span class="sxs-lookup"><span data-stu-id="c7160-220">MM/YY -- for example, 01/11 or 1/11</span></span>
    
- <span data-ttu-id="c7160-221">MM/AAAA, par exemple, 01/2011 ou 1/2011</span><span class="sxs-lookup"><span data-stu-id="c7160-221">MM/YYYY -- for example, 01/2011 or 1/2011</span></span>
    
- <span data-ttu-id="c7160-222">MM-AA, par exemple, 01-22 ou 1-11</span><span class="sxs-lookup"><span data-stu-id="c7160-222">MM-YY -- for example, 01-22 or 1-11</span></span>
    
- <span data-ttu-id="c7160-223">MM-AAAA, par exemple, 01-2000 ou 1-2000</span><span class="sxs-lookup"><span data-stu-id="c7160-223">MM-YYYY -- for example, 01-2000 or 1-2000</span></span>
    
<span data-ttu-id="c7160-224">Les formats suivants prennent en charge AA ou AAAA :</span><span class="sxs-lookup"><span data-stu-id="c7160-224">The following formats support YY or YYYY:</span></span>
  
- <span data-ttu-id="c7160-225">Mois-aaaa--par exemple, Jan-2010, janvier-2010 ou Jan-10 ou janvier-10</span><span class="sxs-lookup"><span data-stu-id="c7160-225">Month-YYYY -- for example Jan-2010 or january-2010 or Jan-10 or january-10</span></span>
    
- <span data-ttu-id="c7160-226">Mois AAAA, par exemple, « janvier 2010 », « jan 2010 », « janvier 10 » ou « jan 10 »</span><span class="sxs-lookup"><span data-stu-id="c7160-226">Month YYYY -- for example, 'january 2010' or 'Jan 2010' or 'january 10' or 'Jan 10'</span></span>
    
- <span data-ttu-id="c7160-227">MoisAAAA, par exemple, « janvier2010 », « jan2010 », « janvier10 » ou « jan10 »</span><span class="sxs-lookup"><span data-stu-id="c7160-227">MonthYYYY -- for example, 'january2010' or 'Jan2010' or 'january10' or 'Jan10'</span></span>
    
- <span data-ttu-id="c7160-228">Mois/aaaa--par exemple, « janvier/2010 » ou « Jan/2010 », « janvier/10 » ou « Jan/10 »</span><span class="sxs-lookup"><span data-stu-id="c7160-228">Month/YYYY -- for example, 'january/2010' or 'Jan/2010' or 'january/10' or 'Jan/10'</span></span>
    
<span data-ttu-id="c7160-229">Noms de mois acceptés :</span><span class="sxs-lookup"><span data-stu-id="c7160-229">Accepted month names:</span></span>
  
- <span data-ttu-id="c7160-230">English</span><span class="sxs-lookup"><span data-stu-id="c7160-230">English</span></span>
    
  - <span data-ttu-id="c7160-231">Janvier, février, mars, avril, mai, juin, juillet, août, septembre, octobre, novembre, décembre</span><span class="sxs-lookup"><span data-stu-id="c7160-231">January, February, march, April, may, June, July, August, September, October, November, December</span></span>
    
  - <span data-ttu-id="c7160-232">Jan Fév Mar Avr mai juin septembre sept octobre déc</span><span class="sxs-lookup"><span data-stu-id="c7160-232">Jan Feb Mar Apr May June July Aug Sept Oct Nov Dec</span></span>
    
## <a name="func_us_address"></a><span data-ttu-id="c7160-233">Func_us_address</span><span class="sxs-lookup"><span data-stu-id="c7160-233">Func_us_address</span></span>

<span data-ttu-id="c7160-234">Cette fonction recherche un nom d’État américain ou une abréviation postale suivie d’un code postal valide, tout comme ils sont utilisés dans des adresses postales.</span><span class="sxs-lookup"><span data-stu-id="c7160-234">This function looks for a U.S. state name or postal abbreviation followed by a valid zip code, just as they're used in postal addresses.</span></span> <span data-ttu-id="c7160-235">Le code postal doit être l’un des codes postaux corrects qui sont associés au nom de l’état américain ou à son abréviation.</span><span class="sxs-lookup"><span data-stu-id="c7160-235">The zip code must be one of the correct zip codes associated with the U.S. state name or abbreviation.</span></span> <span data-ttu-id="c7160-236">Le nom de l’état américain et le code postal ne doivent pas être séparés par des signes de ponctuation ou des lettres.</span><span class="sxs-lookup"><span data-stu-id="c7160-236">The U.S. state name and zip code cannot be separated by punctuation or letters.</span></span>
  
<span data-ttu-id="c7160-237">Exemples :</span><span class="sxs-lookup"><span data-stu-id="c7160-237">Examples:</span></span>
  
- <span data-ttu-id="c7160-238">Washington 98052</span><span class="sxs-lookup"><span data-stu-id="c7160-238">Washington 98052</span></span>
    
- <span data-ttu-id="c7160-239">Washington 98052-9998</span><span class="sxs-lookup"><span data-stu-id="c7160-239">Washington 98052-9998</span></span>
    
- <span data-ttu-id="c7160-240">WA 98052</span><span class="sxs-lookup"><span data-stu-id="c7160-240">WA 98052</span></span>
    
- <span data-ttu-id="c7160-241">WA 98052-9998</span><span class="sxs-lookup"><span data-stu-id="c7160-241">WA 98052-9998</span></span>
    

