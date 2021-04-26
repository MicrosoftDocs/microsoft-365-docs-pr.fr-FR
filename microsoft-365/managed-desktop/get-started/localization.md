---
title: Localiser l’expérience utilisateur
description: Comment trouver des appareils pour les utilisateurs
keywords: Bureau géré Microsoft, Microsoft 365, service, documentation
ms.service: m365-md
author: jaimeo
f1.keywords:
- NOCSH
ms.author: jaimeo
ms.localizationpriority: normal
ms.collection: M365-modern-desktop
manager: laurawi
ms.topic: article
audience: Admin
ms.openlocfilehash: 354f61284bbd95c1c7ca4cd50459a1644a89d090
ms.sourcegitcommit: 72795ec56a7c4db863dcaaff5e9f7c41c653fda8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/26/2021
ms.locfileid: "52023260"
---
# <a name="localize-the-user-experience"></a><span data-ttu-id="734e3-104">Localiser l’expérience utilisateur</span><span class="sxs-lookup"><span data-stu-id="734e3-104">Localize the user experience</span></span>

<span data-ttu-id="734e3-105">Les utilisateurs d’appareils Bureau géré Microsoft peuvent sélectionner la langue de leur choix pendant le processus de configuration (expérience « out-of-box experience ») ou par la suite.</span><span class="sxs-lookup"><span data-stu-id="734e3-105">Users of Microsoft Managed Desktop devices can select the language of their choice either during the setup process (the "out of box experience") or afterwards.</span></span>

## <a name="during-setup-the-out-of-box-experience"></a><span data-ttu-id="734e3-106">Lors de l’installation (expérience « out-of-box »)</span><span class="sxs-lookup"><span data-stu-id="734e3-106">During setup (the "out of box experience")</span></span>

<span data-ttu-id="734e3-107">Pendant le processus de configuration, les utilisateurs peuvent sélectionner la langue de leur choix.</span><span class="sxs-lookup"><span data-stu-id="734e3-107">During the process of completing setup, users can select the language of their choice.</span></span> <span data-ttu-id="734e3-108">Cette sélection affecte les attributs ci-après :</span><span class="sxs-lookup"><span data-stu-id="734e3-108">This selection affects these attributes:</span></span>

- <span data-ttu-id="734e3-109">Fonctionnalités linguistiques de Windows 10 :</span><span class="sxs-lookup"><span data-stu-id="734e3-109">Windows 10 language features:</span></span>
    - <span data-ttu-id="734e3-110">Langue d’affichage</span><span class="sxs-lookup"><span data-stu-id="734e3-110">Display language</span></span>
    - <span data-ttu-id="734e3-111">Langue du clavier</span><span class="sxs-lookup"><span data-stu-id="734e3-111">Keyboard language</span></span>
    - <span data-ttu-id="734e3-112">Fonctionnalités liées à la langue à la demande</span><span class="sxs-lookup"><span data-stu-id="734e3-112">Language-related Features on Demand</span></span>

- <span data-ttu-id="734e3-113">Fonctionnalités linguistiques de Microsoft 365 Apps for Enterprise :</span><span class="sxs-lookup"><span data-stu-id="734e3-113">Microsoft 365 Apps for Enterprise language features:</span></span>
    - <span data-ttu-id="734e3-114">Langue d’affichage</span><span class="sxs-lookup"><span data-stu-id="734e3-114">Display language</span></span>
    - <span data-ttu-id="734e3-115">Outils de preuve et de authoring</span><span class="sxs-lookup"><span data-stu-id="734e3-115">Proofing and authoring tools</span></span>

> [!NOTE]
> <span data-ttu-id="734e3-116">Les utilisateurs peuvent uniquement obtenir des fonctionnalités liées à la langue à la demande en sélectionnant la langue pendant le processus d’installation.</span><span class="sxs-lookup"><span data-stu-id="734e3-116">Users can only get language-related Features On Demand by selecting the language during the setup process.</span></span>

## <a name="after-completing-setup"></a><span data-ttu-id="734e3-117">Après avoir terminé l’installation</span><span class="sxs-lookup"><span data-stu-id="734e3-117">After completing setup</span></span>

<span data-ttu-id="734e3-118">Les utilisateurs peuvent sélectionner la langue de leur choix pour Windows 10 et Microsoft 365 Apps for Enterprise à tout moment une fois le processus d’installation terminé.</span><span class="sxs-lookup"><span data-stu-id="734e3-118">Users can select the language of their choice for Windows 10 and Microsoft 365 Apps for Enterprise anytime after the setup process is complete.</span></span> <span data-ttu-id="734e3-119">Notamment :</span><span class="sxs-lookup"><span data-stu-id="734e3-119">Specifically:</span></span>

- <span data-ttu-id="734e3-120">Fonctionnalités linguistiques de Windows 10 :</span><span class="sxs-lookup"><span data-stu-id="734e3-120">Windows 10 language features:</span></span>
    - <span data-ttu-id="734e3-121">Langue d’affichage</span><span class="sxs-lookup"><span data-stu-id="734e3-121">Display language</span></span>
    - <span data-ttu-id="734e3-122">Langue du clavier</span><span class="sxs-lookup"><span data-stu-id="734e3-122">Keyboard language</span></span>

- <span data-ttu-id="734e3-123">Fonctionnalités linguistiques de Microsoft 365 Apps for Enterprise :</span><span class="sxs-lookup"><span data-stu-id="734e3-123">Microsoft 365 Apps for Enterprise language features:</span></span>
    - <span data-ttu-id="734e3-124">Langue d’affichage</span><span class="sxs-lookup"><span data-stu-id="734e3-124">Display language</span></span>
    - <span data-ttu-id="734e3-125">Outils de preuve et de authoring</span><span class="sxs-lookup"><span data-stu-id="734e3-125">Proofing and authoring tools</span></span>

<span data-ttu-id="734e3-126">Pour rendre les [langues](#supported-languages) prise en charge pour Microsoft 365 Apps for Enterprise disponibles pour que vos utilisateurs les installent, ajoutez-les au groupe Moderne **Workplace-Office-Language_Packs.**</span><span class="sxs-lookup"><span data-stu-id="734e3-126">To make the [Supported languages](#supported-languages) for Microsoft 365 Apps for Enterprise available for your users to install, add the users to the **Modern Workplace-Office-Language_Packs** group.</span></span> <span data-ttu-id="734e3-127">Les langues seront disponibles dans le portail d'entreprise Intune.</span><span class="sxs-lookup"><span data-stu-id="734e3-127">The languages will be available in the Intune Company Portal.</span></span>


## <a name="supported-languages"></a><span data-ttu-id="734e3-128">Langues prises en charge</span><span class="sxs-lookup"><span data-stu-id="734e3-128">Supported languages</span></span>

<span data-ttu-id="734e3-129">Pour les nouveaux appareils, votre fabricant doit fournir des images d'appareil qui incluent les langues dont vous avez besoin.</span><span class="sxs-lookup"><span data-stu-id="734e3-129">For new devices, your manufacturer must provide device images that include the languages you require.</span></span> <span data-ttu-id="734e3-130">Si l'image de votre fabricant inclut des langues autres que celles fournies dans la liste des langues prise en charge, elle est toujours prise en charge par le service.</span><span class="sxs-lookup"><span data-stu-id="734e3-130">If your manufacturer's image includes languages other than those provided in the supported languages list it is still supported by the service.</span></span>

<span data-ttu-id="734e3-131">Si vous réutilisez des appareils existants, vous devrez peut-être travailler avec votre représentant de compte Microsoft pour obtenir les images appropriées.</span><span class="sxs-lookup"><span data-stu-id="734e3-131">If you are reusing existing devices, you might need to work with your Microsoft account representative to obtain appropriate images.</span></span> <span data-ttu-id="734e3-132">Pour plus d'informations, voir [Images d'appareil.](../service-description/device-images.md)</span><span class="sxs-lookup"><span data-stu-id="734e3-132">For more information, see [Device images](../service-description/device-images.md).</span></span>

<span data-ttu-id="734e3-133">[L'image universelle](../service-description/device-images.md#universal-image) fournie par Bureau géré Microsoft inclut les langues suivantes et pour Windows 10 :</span><span class="sxs-lookup"><span data-stu-id="734e3-133">The [universal image](../service-description/device-images.md#universal-image) provided by Microsoft Managed Desktop includes these languages and for Windows 10:</span></span>

- <span data-ttu-id="734e3-134">Arabe</span><span class="sxs-lookup"><span data-stu-id="734e3-134">Arabic</span></span>
- <span data-ttu-id="734e3-135">Bulgare</span><span class="sxs-lookup"><span data-stu-id="734e3-135">Bulgarian</span></span>
- <span data-ttu-id="734e3-136">Chinois simplifié</span><span class="sxs-lookup"><span data-stu-id="734e3-136">Chinese Simplified</span></span>
- <span data-ttu-id="734e3-137">Chinois traditionnel</span><span class="sxs-lookup"><span data-stu-id="734e3-137">Chinese Traditional</span></span>
- <span data-ttu-id="734e3-138">Croate</span><span class="sxs-lookup"><span data-stu-id="734e3-138">Croatian</span></span>
- <span data-ttu-id="734e3-139">Tchèque</span><span class="sxs-lookup"><span data-stu-id="734e3-139">Czech</span></span>
- <span data-ttu-id="734e3-140">Danois</span><span class="sxs-lookup"><span data-stu-id="734e3-140">Danish</span></span>  
- <span data-ttu-id="734e3-141">Néerlandais</span><span class="sxs-lookup"><span data-stu-id="734e3-141">Dutch</span></span>  
- <span data-ttu-id="734e3-142">Anglais (États-Unis, GB, AU, CA, IN)</span><span class="sxs-lookup"><span data-stu-id="734e3-142">English (US, GB, AU, CA, IN)</span></span>
- <span data-ttu-id="734e3-143">Estonien</span><span class="sxs-lookup"><span data-stu-id="734e3-143">Estonian</span></span>
- <span data-ttu-id="734e3-144">Finnois</span><span class="sxs-lookup"><span data-stu-id="734e3-144">Finnish</span></span> 
- <span data-ttu-id="734e3-145">Français (France, Canada)</span><span class="sxs-lookup"><span data-stu-id="734e3-145">French (France, Canada)</span></span>
- <span data-ttu-id="734e3-146">Allemand</span><span class="sxs-lookup"><span data-stu-id="734e3-146">German</span></span>
- <span data-ttu-id="734e3-147">Grec</span><span class="sxs-lookup"><span data-stu-id="734e3-147">Greek</span></span>
- <span data-ttu-id="734e3-148">Hébreu</span><span class="sxs-lookup"><span data-stu-id="734e3-148">Hebrew</span></span>
- <span data-ttu-id="734e3-149">Hongrois</span><span class="sxs-lookup"><span data-stu-id="734e3-149">Hungarian</span></span>
- <span data-ttu-id="734e3-150">Indonésien</span><span class="sxs-lookup"><span data-stu-id="734e3-150">Indonesian</span></span>
- <span data-ttu-id="734e3-151">Italien</span><span class="sxs-lookup"><span data-stu-id="734e3-151">Italian</span></span>
- <span data-ttu-id="734e3-152">Japonais</span><span class="sxs-lookup"><span data-stu-id="734e3-152">Japanese</span></span>
- <span data-ttu-id="734e3-153">Coréen</span><span class="sxs-lookup"><span data-stu-id="734e3-153">Korean</span></span>
- <span data-ttu-id="734e3-154">Letton</span><span class="sxs-lookup"><span data-stu-id="734e3-154">Latvian</span></span>
- <span data-ttu-id="734e3-155">Lituanien</span><span class="sxs-lookup"><span data-stu-id="734e3-155">Lithuanian</span></span>
- <span data-ttu-id="734e3-156">Norvégien (Bokmål)</span><span class="sxs-lookup"><span data-stu-id="734e3-156">Norwegian (Bokmål)</span></span>
- <span data-ttu-id="734e3-157">Polonais</span><span class="sxs-lookup"><span data-stu-id="734e3-157">Polish</span></span>
- <span data-ttu-id="734e3-158">Portugais (Brésil)</span><span class="sxs-lookup"><span data-stu-id="734e3-158">Portuguese (Brazil)</span></span>
- <span data-ttu-id="734e3-159">Portugais (Portugal)</span><span class="sxs-lookup"><span data-stu-id="734e3-159">Portuguese (Portugal)</span></span>
- <span data-ttu-id="734e3-160">Roumain</span><span class="sxs-lookup"><span data-stu-id="734e3-160">Romanian</span></span>
- <span data-ttu-id="734e3-161">Russe</span><span class="sxs-lookup"><span data-stu-id="734e3-161">Russian</span></span> 
- <span data-ttu-id="734e3-162">Serbe (alphabet latin)</span><span class="sxs-lookup"><span data-stu-id="734e3-162">Serbian (Latin alphabet)</span></span>
- <span data-ttu-id="734e3-163">Slovaque</span><span class="sxs-lookup"><span data-stu-id="734e3-163">Slovak</span></span>
- <span data-ttu-id="734e3-164">Slovène</span><span class="sxs-lookup"><span data-stu-id="734e3-164">Slovenian</span></span>
- <span data-ttu-id="734e3-165">Espagnol (Espagne, Mexique)</span><span class="sxs-lookup"><span data-stu-id="734e3-165">Spanish (Spain, Mexico)</span></span>
- <span data-ttu-id="734e3-166">Suédois</span><span class="sxs-lookup"><span data-stu-id="734e3-166">Swedish</span></span>
- <span data-ttu-id="734e3-167">Thaï</span><span class="sxs-lookup"><span data-stu-id="734e3-167">Thai</span></span>
- <span data-ttu-id="734e3-168">Turc</span><span class="sxs-lookup"><span data-stu-id="734e3-168">Turkish</span></span>
- <span data-ttu-id="734e3-169">Ukrainien</span><span class="sxs-lookup"><span data-stu-id="734e3-169">Ukrainian</span></span>
- <span data-ttu-id="734e3-170">Vietnamien</span><span class="sxs-lookup"><span data-stu-id="734e3-170">Vietnamese</span></span>

<span data-ttu-id="734e3-171">Microsoft 365 Apps for Enterprise peut avoir une liste légèrement différente.</span><span class="sxs-lookup"><span data-stu-id="734e3-171">Microsoft 365 Apps for Enterprise might support a slightly different list.</span></span>

<span data-ttu-id="734e3-172">Si vos utilisateurs ont besoin d'une langue autre que celle répertoriée ici, déposez une demande de [support](../working-with-managed-desktop/admin-support.md) à l'aide du [portail d'administration.](access-admin-portal.md)</span><span class="sxs-lookup"><span data-stu-id="734e3-172">If your users need a language other than the ones listed here, file a [support request](../working-with-managed-desktop/admin-support.md) by using the [Admin portal](access-admin-portal.md).</span></span>

## <a name="languages-for-support-and-operations"></a><span data-ttu-id="734e3-173">Langues pour la prise en charge et les opérations</span><span class="sxs-lookup"><span data-stu-id="734e3-173">Languages for support and operations</span></span>

### <a name="user-support"></a><span data-ttu-id="734e3-174">Support pour les utilisateurs</span><span class="sxs-lookup"><span data-stu-id="734e3-174">User support</span></span>
<span data-ttu-id="734e3-175">Bureau géré Microsoft fournit une prise en charge uniquement en anglais.</span><span class="sxs-lookup"><span data-stu-id="734e3-175">Microsoft Managed Desktop provides support only in English.</span></span> <span data-ttu-id="734e3-176">Si les utilisateurs choisissent une autre langue dans l'application Obtenir de l'aide, ils obtiennent le support des canaux de support microsoft généraux, plutôt que le support directement à partir du Bureau géré Microsoft.</span><span class="sxs-lookup"><span data-stu-id="734e3-176">If users choose another language in the Get Help app, they will get support from the general Microsoft support channels, rather than support directly from Microsoft Managed Desktop.</span></span> <span data-ttu-id="734e3-177">Pour plus d'informations, voir [Obtenir de l'aide pour les utilisateurs.](../working-with-managed-desktop/end-user-support.md)</span><span class="sxs-lookup"><span data-stu-id="734e3-177">For more information, see [Getting help for users](../working-with-managed-desktop/end-user-support.md).</span></span>

<span data-ttu-id="734e3-178">Si vos utilisateurs ont besoin d'une prise en charge dans d'autres langues, vous devrez le fournir via des sources de support non-Microsoft ou à partir de votre propre organisation.</span><span class="sxs-lookup"><span data-stu-id="734e3-178">If your users need support in other languages, you'll have to provide that through non-Microsoft support sources or from your own organization.</span></span>

### <a name="admin-support-and-operations"></a><span data-ttu-id="734e3-179">Support et opérations de l'administrateur</span><span class="sxs-lookup"><span data-stu-id="734e3-179">Admin support and operations</span></span>
<span data-ttu-id="734e3-180">Bureau géré Microsoft fournit une prise en charge administrateur uniquement en anglais.</span><span class="sxs-lookup"><span data-stu-id="734e3-180">Microsoft Managed Desktop provides admin support only in English.</span></span> <span data-ttu-id="734e3-181">Cela inclut le portail d’administration et toutes les communications avec les opérations Bureau géré Microsoft.</span><span class="sxs-lookup"><span data-stu-id="734e3-181">This includes the Admin portal and all communications with Microsoft Managed Desktop Operations.</span></span> <span data-ttu-id="734e3-182">Vous devez supposer que toutes les interactions et interfaces liées à l’administrateur seront en anglais, sauf indication contraire.</span><span class="sxs-lookup"><span data-stu-id="734e3-182">You should assume that all admin-related interactions and interfaces will be in English, unless specified otherwise.</span></span>


