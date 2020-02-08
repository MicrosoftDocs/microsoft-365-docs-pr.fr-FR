---
title: Comment le contenu est identifié pour consulter des recommandations de gouvernance des données
f1.keywords:
- NOCSH
ms.author: brendonb
author: cabailey
manager: laurawi
ms.date: 1/15/2019
audience: Admin
ms.topic: overview
ms.service: O365-seccomp
ms.collection:
- SPO_Content
localization_priority: Priority
search.appverid:
- MOE150
- MET150
ROBOTS: NOINDEX, NOFOLLOW
description: Le centre de Conformité et Sécurité Office 365 fournit des recommandations pour la gouvernance des données basées sur la configuration actuelle de votre organisation et vous permet de configurer certaines actions en quelques clics. Certaines de ces recommandations détectent du contenu spécifique dans votre organisation, puis actualisent les étapes recommandées pour la gestion de ce contenu. Par exemple, une recommandation peut détecter les éléments qui présentent un contenu de critique commerciale (tel qu un privilège client-avocat ou informations accord de confidentialité) et vous permet automatiquement d’appliquer une étiquette de rétention à ces éléments pour vous assurer qu’ils soient classés et conservés selon vos besoins . Cette rubrique répertorie les recommandations de gouvernance des données que vous pouvez voir et décrit quel contenu est détecté au déclenchement de chacun d’eux.
ms.openlocfilehash: af3c08f568bb0b44e8454ee345a84308b53cf01f
ms.sourcegitcommit: 1c91b7b24537d0e54d484c3379043db53c1aea65
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/29/2020
ms.locfileid: "41595431"
---
# <a name="how-content-is-identified-for-data-governance-recommendations"></a><span data-ttu-id="0d0fd-106">Comment le contenu est identifié pour consulter des recommandations de gouvernance des données</span><span class="sxs-lookup"><span data-stu-id="0d0fd-106">How content is identified for data-governance recommendations</span></span>

<span data-ttu-id="0d0fd-p102">Le centre de Conformité et Sécurité Office 365 fournit des recommandations pour la gouvernance des données basées sur la configuration actuelle de votre organisation et vous permet de configurer certaines actions en quelques clics. Certaines de ces recommandations détectent du contenu spécifique dans votre organisation, puis actualisent les étapes recommandées pour la gestion de ce contenu. Par exemple, une recommandation peut détecter les éléments qui présentent un contenu de critique commerciale (tel qu’un privilège client-avocat ou des informations relatives à un accord de confidentialité) et vous permet automatiquement d’appliquer une étiquette de rétention à ces éléments pour vous assurer qu’ils soient classés et conservés selon vos besoins. Cette rubrique répertorie les recommandations de gouvernance des données que vous pouvez voir et décrit quel contenu est détecté au déclenchement de chacun d’eux.</span><span class="sxs-lookup"><span data-stu-id="0d0fd-p102">The Office 365 Security & Compliance Center provides recommendations for data governance based on your org's current setup and lets you set things up in a couple clicks. Some of these recommendations detect specific content in your organization and then provide recommended steps for managing that content. For example, a recommendation might detect items that contain business-critical content (such as attorney-client privilege or NDA info), and then let you automatically apply a retention label to those items to ensure that they’re classified and retained as needed.</span></span>

<span data-ttu-id="0d0fd-110">Cette rubrique répertorie les recommandations de gouvernance des données que vous pouvez voir et décrit le contenu est détecté au déclenchement de chacun d’eux.</span><span class="sxs-lookup"><span data-stu-id="0d0fd-110">This topic lists the data-governance recommendations you might see and describes what content is detected to trigger each one.</span></span>

## <a name="clean-up-voicemail"></a><span data-ttu-id="0d0fd-111">Nettoyer la messagerie vocale</span><span class="sxs-lookup"><span data-stu-id="0d0fd-111">Clean up voicemail</span></span>

<span data-ttu-id="0d0fd-p103">Cette recommandation s’affiche lorsque les messages électroniques identifiés comme message de type « messagerie vocale » sont détectés dans les boîtes aux lettres des utilisateurs. En savoir plus sur [propriétés dans Exchange de message](https://docs.microsoft.com/exchange/policy-and-compliance/ediscovery/message-properties-and-search-operators?view=exchserver-2019#searchable-properties-in-exchange).</span><span class="sxs-lookup"><span data-stu-id="0d0fd-p103">This recommendation appears when email messages identified as the message type ‘voicemail’ are detected in users’ mailboxes. Learn more about [message properties in Exchange](https://docs.microsoft.com/exchange/policy-and-compliance/ediscovery/message-properties-and-search-operators?view=exchserver-2019#searchable-properties-in-exchange).</span></span>

## <a name="label-attorney-client-privilege-content"></a><span data-ttu-id="0d0fd-114">Étiquette du contenu client avocat privilège élevé</span><span class="sxs-lookup"><span data-stu-id="0d0fd-114">Label attorney-client privilege content</span></span> 

<span data-ttu-id="0d0fd-115">Cette recommandation s’affiche lorsqu’un des critères suivants est rempli.</span><span class="sxs-lookup"><span data-stu-id="0d0fd-115">This recommendation appears when either of the following criteria are met.</span></span>

- <span data-ttu-id="0d0fd-116">Une combinaison de ces mots clés est détectée dans le corps du message électronique:</span><span class="sxs-lookup"><span data-stu-id="0d0fd-116">Any of combination of these keywords is detected in the body of an email message:</span></span>
    - <span data-ttu-id="0d0fd-117">ACP</span><span class="sxs-lookup"><span data-stu-id="0d0fd-117">ACP</span></span>
    - <span data-ttu-id="0d0fd-118">Privilège Client Avocat  </span><span class="sxs-lookup"><span data-stu-id="0d0fd-118">Attorney Client Privilege</span></span>
    - <span data-ttu-id="0d0fd-119">Privilège Client-Avocat  </span><span class="sxs-lookup"><span data-stu-id="0d0fd-119">Attorney-Client Privilege</span></span>
    - <span data-ttu-id="0d0fd-120">Privilège de Client/Avocat (A/C Privilégié)</span><span class="sxs-lookup"><span data-stu-id="0d0fd-120">Attorney-Client Privileged</span></span>

- <span data-ttu-id="0d0fd-121">N’importe quelle combinaison de ces mots clés est détectée dans les fichiers SharePoint ou OneDrive:</span><span class="sxs-lookup"><span data-stu-id="0d0fd-121">Any combination of these keywords are detected in SharePoint or OneDrive files:</span></span>
    - <span data-ttu-id="0d0fd-122">ACP</span><span class="sxs-lookup"><span data-stu-id="0d0fd-122">ACP</span></span>
    - <span data-ttu-id="0d0fd-123">Privilège Client Avocat\*</span><span class="sxs-lookup"><span data-stu-id="0d0fd-123">Attorney Client Privilege\*</span></span>
    - <span data-ttu-id="0d0fd-124">Privilège AC</span><span class="sxs-lookup"><span data-stu-id="0d0fd-124">AC Privilege</span></span>

## <a name="retain-audio-files"></a><span data-ttu-id="0d0fd-125">Conservation des fichiers audio</span><span class="sxs-lookup"><span data-stu-id="0d0fd-125">Retain audio files</span></span>

<span data-ttu-id="0d0fd-126">Cette recommandation s’affiche lorsque les types de fichiers suivants sont détectés dans SharePoint ou OneDrive.</span><span class="sxs-lookup"><span data-stu-id="0d0fd-126">This recommendation appears when any of the following file types are detected in SharePoint or OneDrive.</span></span>

- <span data-ttu-id="0d0fd-127">.MP3</span><span class="sxs-lookup"><span data-stu-id="0d0fd-127">.MP3</span></span>
- <span data-ttu-id="0d0fd-128">.WMA</span><span class="sxs-lookup"><span data-stu-id="0d0fd-128">.WMA</span></span>
- <span data-ttu-id="0d0fd-129">.WAV</span><span class="sxs-lookup"><span data-stu-id="0d0fd-129">.WAV</span></span>
- <span data-ttu-id="0d0fd-130">.RA</span><span class="sxs-lookup"><span data-stu-id="0d0fd-130">.RA</span></span>
- <span data-ttu-id="0d0fd-131">.RAM</span><span class="sxs-lookup"><span data-stu-id="0d0fd-131">.RAM</span></span>
- <span data-ttu-id="0d0fd-132">.RM</span><span class="sxs-lookup"><span data-stu-id="0d0fd-132">.RM</span></span>
- <span data-ttu-id="0d0fd-133">.MID</span><span class="sxs-lookup"><span data-stu-id="0d0fd-133">.MID</span></span>
- <span data-ttu-id="0d0fd-134">.OGG</span><span class="sxs-lookup"><span data-stu-id="0d0fd-134">.OGG</span></span>
- <span data-ttu-id="0d0fd-135">.AIFF</span><span class="sxs-lookup"><span data-stu-id="0d0fd-135">.AIFF</span></span>
- <span data-ttu-id="0d0fd-136">.PCM</span><span class="sxs-lookup"><span data-stu-id="0d0fd-136">.PCM</span></span>
- <span data-ttu-id="0d0fd-137">.AAC</span><span class="sxs-lookup"><span data-stu-id="0d0fd-137">.AAC</span></span>
- <span data-ttu-id="0d0fd-138">.FLAC</span><span class="sxs-lookup"><span data-stu-id="0d0fd-138">.FLAC</span></span>
- <span data-ttu-id="0d0fd-139">. ALAC</span><span class="sxs-lookup"><span data-stu-id="0d0fd-139">.ALAC</span></span>

## <a name="retain-cad-files"></a><span data-ttu-id="0d0fd-140">Conservation des fichiers de CAD</span><span class="sxs-lookup"><span data-stu-id="0d0fd-140">Retain CAD files</span></span>

<span data-ttu-id="0d0fd-141">Cette recommandation s’affiche lorsque les types de fichiers suivants sont détectés dans SharePoint ou OneDrive.</span><span class="sxs-lookup"><span data-stu-id="0d0fd-141">This recommendation appears when any of the following file types are detected in SharePoint or OneDrive.</span></span>

- <span data-ttu-id="0d0fd-142">.3DXML</span><span class="sxs-lookup"><span data-stu-id="0d0fd-142">.3DXML</span></span>
- <span data-ttu-id="0d0fd-143">. ACIS</span><span class="sxs-lookup"><span data-stu-id="0d0fd-143">.ACIS</span></span>
- <span data-ttu-id="0d0fd-144">.ARC
</span><span class="sxs-lookup"><span data-stu-id="0d0fd-144">.ARC</span></span>
- <span data-ttu-id="0d0fd-145">.ASM</span><span class="sxs-lookup"><span data-stu-id="0d0fd-145">.ASM</span></span>
- <span data-ttu-id="0d0fd-146">.CAT\*</span><span class="sxs-lookup"><span data-stu-id="0d0fd-146">.CAT\*</span></span>
- <span data-ttu-id="0d0fd-147">. CGR</span><span class="sxs-lookup"><span data-stu-id="0d0fd-147">.CGR</span></span>
- <span data-ttu-id="0d0fd-148">.DW\*</span><span class="sxs-lookup"><span data-stu-id="0d0fd-148">.DW\*</span></span>
- <span data-ttu-id="0d0fd-149">.DX\*</span><span class="sxs-lookup"><span data-stu-id="0d0fd-149">.DX\*</span></span>
- <span data-ttu-id="0d0fd-150">.EDRW</span><span class="sxs-lookup"><span data-stu-id="0d0fd-150">.EDRW</span></span>
- <span data-ttu-id="0d0fd-151">.IAM</span><span class="sxs-lookup"><span data-stu-id="0d0fd-151">.IAM</span></span>
- <span data-ttu-id="0d0fd-152">.IGES</span><span class="sxs-lookup"><span data-stu-id="0d0fd-152">.IGES</span></span>
- <span data-ttu-id="0d0fd-153">. IGS</span><span class="sxs-lookup"><span data-stu-id="0d0fd-153">.IGS</span></span>
- <span data-ttu-id="0d0fd-154">.IPT</span><span class="sxs-lookup"><span data-stu-id="0d0fd-154">.IPT</span></span>
- <span data-ttu-id="0d0fd-155">.JT</span><span class="sxs-lookup"><span data-stu-id="0d0fd-155">.JT</span></span>
- <span data-ttu-id="0d0fd-156">.MF1</span><span class="sxs-lookup"><span data-stu-id="0d0fd-156">.MF1</span></span>
- <span data-ttu-id="0d0fd-157">. NEU</span><span class="sxs-lookup"><span data-stu-id="0d0fd-157">.NEU</span></span>
- <span data-ttu-id="0d0fd-158">.PAR</span><span class="sxs-lookup"><span data-stu-id="0d0fd-158">.PAR</span></span>
- <span data-ttu-id="0d0fd-159">.PKG</span><span class="sxs-lookup"><span data-stu-id="0d0fd-159">.PKG</span></span>
- <span data-ttu-id="0d0fd-160">.PRC
</span><span class="sxs-lookup"><span data-stu-id="0d0fd-160">.PRC</span></span>
- <span data-ttu-id="0d0fd-161">.PRT</span><span class="sxs-lookup"><span data-stu-id="0d0fd-161">.PRT</span></span>
- <span data-ttu-id="0d0fd-162">.PSM</span><span class="sxs-lookup"><span data-stu-id="0d0fd-162">.PSM</span></span>
- <span data-ttu-id="0d0fd-163">.PWD</span><span class="sxs-lookup"><span data-stu-id="0d0fd-163">.PWD</span></span>
- <span data-ttu-id="0d0fd-164">. SLD \*</span><span class="sxs-lookup"><span data-stu-id="0d0fd-164">.SLD\*</span></span>
- <span data-ttu-id="0d0fd-165">.STEP</span><span class="sxs-lookup"><span data-stu-id="0d0fd-165">.STEP</span></span>
- <span data-ttu-id="0d0fd-166">. STL</span><span class="sxs-lookup"><span data-stu-id="0d0fd-166">.STL</span></span>
- <span data-ttu-id="0d0fd-167">.STP</span><span class="sxs-lookup"><span data-stu-id="0d0fd-167">.STP</span></span>
- <span data-ttu-id="0d0fd-168">.U3D</span><span class="sxs-lookup"><span data-stu-id="0d0fd-168">.U3D</span></span>
- <span data-ttu-id="0d0fd-169">. UNV</span><span class="sxs-lookup"><span data-stu-id="0d0fd-169">.UNV</span></span>
- <span data-ttu-id="0d0fd-170">. VRML</span><span class="sxs-lookup"><span data-stu-id="0d0fd-170">.VRML</span></span>
- <span data-ttu-id="0d0fd-171">. WRL</span><span class="sxs-lookup"><span data-stu-id="0d0fd-171">.WRL</span></span>
- <span data-ttu-id="0d0fd-172">.X_\*</span><span class="sxs-lookup"><span data-stu-id="0d0fd-172">.X_\*</span></span>
- <span data-ttu-id="0d0fd-173">.XAS</span><span class="sxs-lookup"><span data-stu-id="0d0fd-173">.XAS</span></span>
- <span data-ttu-id="0d0fd-174">.XMT\*</span><span class="sxs-lookup"><span data-stu-id="0d0fd-174">.XMT\*</span></span>
- <span data-ttu-id="0d0fd-175">.XPR</span><span class="sxs-lookup"><span data-stu-id="0d0fd-175">.XPR</span></span>

## <a name="retain-image-files"></a><span data-ttu-id="0d0fd-176">Conservation de fichiers image</span><span class="sxs-lookup"><span data-stu-id="0d0fd-176">Retain image files</span></span>

<span data-ttu-id="0d0fd-177">Cette recommandation s’affiche lorsque les types de fichiers suivants sont détectés dans SharePoint ou OneDrive.</span><span class="sxs-lookup"><span data-stu-id="0d0fd-177">This recommendation appears when any of the following file types are detected in SharePoint or OneDrive.</span></span>

- <span data-ttu-id="0d0fd-178">.JPEG</span><span class="sxs-lookup"><span data-stu-id="0d0fd-178">.JPEG</span></span>
- <span data-ttu-id="0d0fd-179">.GIF</span><span class="sxs-lookup"><span data-stu-id="0d0fd-179">.GIF</span></span>
- <span data-ttu-id="0d0fd-180">.TIF\*</span><span class="sxs-lookup"><span data-stu-id="0d0fd-180">.TIF\*</span></span>
- <span data-ttu-id="0d0fd-181">.BMP</span><span class="sxs-lookup"><span data-stu-id="0d0fd-181">.BMP</span></span>
- <span data-ttu-id="0d0fd-182">.PNG</span><span class="sxs-lookup"><span data-stu-id="0d0fd-182">.PNG</span></span>
- <span data-ttu-id="0d0fd-183">.RAW</span><span class="sxs-lookup"><span data-stu-id="0d0fd-183">.RAW</span></span>
- <span data-ttu-id="0d0fd-184">.PSD</span><span class="sxs-lookup"><span data-stu-id="0d0fd-184">.PSD</span></span>
- <span data-ttu-id="0d0fd-185">.PSP
</span><span class="sxs-lookup"><span data-stu-id="0d0fd-185">.PSP</span></span>
- <span data-ttu-id="0d0fd-186">.JPG</span><span class="sxs-lookup"><span data-stu-id="0d0fd-186">.JPG</span></span>
- <span data-ttu-id="0d0fd-187">.EXIF</span><span class="sxs-lookup"><span data-stu-id="0d0fd-187">.EXIF</span></span>
- <span data-ttu-id="0d0fd-188">.PPM</span><span class="sxs-lookup"><span data-stu-id="0d0fd-188">.PPM</span></span>
- <span data-ttu-id="0d0fd-189">.PGM</span><span class="sxs-lookup"><span data-stu-id="0d0fd-189">.PGM</span></span>
- <span data-ttu-id="0d0fd-190">.PBM</span><span class="sxs-lookup"><span data-stu-id="0d0fd-190">.PBM</span></span>
- <span data-ttu-id="0d0fd-191">.PNM</span><span class="sxs-lookup"><span data-stu-id="0d0fd-191">.PNM</span></span>
- <span data-ttu-id="0d0fd-192">.WEBP</span><span class="sxs-lookup"><span data-stu-id="0d0fd-192">.WEBP</span></span>

## <a name="retain-nda-content"></a><span data-ttu-id="0d0fd-193">Conserver le contenu de l’accord de confidentialité</span><span class="sxs-lookup"><span data-stu-id="0d0fd-193">Retain NDA content</span></span> 

<span data-ttu-id="0d0fd-194">Cette recommandation s’affiche lorsqu’un des critères suivants est rempli.</span><span class="sxs-lookup"><span data-stu-id="0d0fd-194">This recommendation appears when either of the following criteria are met.</span></span>

- <span data-ttu-id="0d0fd-195">Une combinaison de ces mots clés est détectée dans le corps du message électronique:</span><span class="sxs-lookup"><span data-stu-id="0d0fd-195">Any of combination of these keywords is detected in the body of an email message:</span></span>
    - <span data-ttu-id="0d0fd-196">ACCORD DE CONFIDENTIALITÉ</span><span class="sxs-lookup"><span data-stu-id="0d0fd-196">NDA</span></span>
    - <span data-ttu-id="0d0fd-197">« Accord de Non-Divulgation »</span><span class="sxs-lookup"><span data-stu-id="0d0fd-197">“Non-Disclosure Agreement”</span></span>
    - <span data-ttu-id="0d0fd-198">« Accord de Non Divulgation »</span><span class="sxs-lookup"><span data-stu-id="0d0fd-198">“Non Disclosure Agreement”</span></span>

- <span data-ttu-id="0d0fd-199">N’importe quelle combinaison de ces mots clés est détectée en .PDF ou .DOC dans les fichiers SharePoint ou OneDrive:</span><span class="sxs-lookup"><span data-stu-id="0d0fd-199">Any combination of these keywords are detected in .PDF or .DOC files in SharePoint or OneDrive:</span></span>
    - <span data-ttu-id="0d0fd-200">ACCORD DE CONFIDENTIALITÉ</span><span class="sxs-lookup"><span data-stu-id="0d0fd-200">NDA</span></span>
    - <span data-ttu-id="0d0fd-201">Accord de Non Divulgation</span><span class="sxs-lookup"><span data-stu-id="0d0fd-201">Non Disclosure Agreement</span></span>

## <a name="retain-software-development-files"></a><span data-ttu-id="0d0fd-202">Conservation des fichiers de développement de logiciel</span><span class="sxs-lookup"><span data-stu-id="0d0fd-202">Retain software development files</span></span>

<span data-ttu-id="0d0fd-203">Cette recommandation s’affiche lorsque les types de fichiers suivants sont détectés dans SharePoint ou OneDrive.</span><span class="sxs-lookup"><span data-stu-id="0d0fd-203">This recommendation appears when any of the following file types are detected in SharePoint or OneDrive.</span></span>

- <span data-ttu-id="0d0fd-204">.ASAX</span><span class="sxs-lookup"><span data-stu-id="0d0fd-204">.ASAX</span></span>
- <span data-ttu-id="0d0fd-205">.ASM</span><span class="sxs-lookup"><span data-stu-id="0d0fd-205">.ASM</span></span>
- <span data-ttu-id="0d0fd-206">.ASP\*</span><span class="sxs-lookup"><span data-stu-id="0d0fd-206">.ASP\*</span></span>
- <span data-ttu-id="0d0fd-207">.BAT</span><span class="sxs-lookup"><span data-stu-id="0d0fd-207">.BAT</span></span>
- <span data-ttu-id="0d0fd-208">.CONFIG</span><span class="sxs-lookup"><span data-stu-id="0d0fd-208">.CONFIG</span></span>
- <span data-ttu-id="0d0fd-209">.CS</span><span class="sxs-lookup"><span data-stu-id="0d0fd-209">.CS</span></span>
- <span data-ttu-id="0d0fd-210">.CSS</span><span class="sxs-lookup"><span data-stu-id="0d0fd-210">.CSS</span></span>
- <span data-ttu-id="0d0fd-211">.DISCO</span><span class="sxs-lookup"><span data-stu-id="0d0fd-211">.DISCO</span></span>
- <span data-ttu-id="0d0fd-212">.HTM\*</span><span class="sxs-lookup"><span data-stu-id="0d0fd-212">.HTM\*</span></span>
- <span data-ttu-id="0d0fd-213">.INC</span><span class="sxs-lookup"><span data-stu-id="0d0fd-213">.INC</span></span>
- <span data-ttu-id="0d0fd-214">.JAD</span><span class="sxs-lookup"><span data-stu-id="0d0fd-214">.JAD</span></span>
- <span data-ttu-id="0d0fd-215">.JAVA</span><span class="sxs-lookup"><span data-stu-id="0d0fd-215">.JAVA</span></span>
- <span data-ttu-id="0d0fd-216">.JS\*</span><span class="sxs-lookup"><span data-stu-id="0d0fd-216">.JS\*</span></span>
- <span data-ttu-id="0d0fd-217">.LIB</span><span class="sxs-lookup"><span data-stu-id="0d0fd-217">.LIB</span></span>
- <span data-ttu-id="0d0fd-218">.O</span><span class="sxs-lookup"><span data-stu-id="0d0fd-218">.O</span></span>
- <span data-ttu-id="0d0fd-219">.PHP</span><span class="sxs-lookup"><span data-stu-id="0d0fd-219">.PHP</span></span>
- <span data-ttu-id="0d0fd-220">.RC</span><span class="sxs-lookup"><span data-stu-id="0d0fd-220">.RC</span></span>
- <span data-ttu-id="0d0fd-221">.RESX</span><span class="sxs-lookup"><span data-stu-id="0d0fd-221">.RESX</span></span>
- <span data-ttu-id="0d0fd-222">. RPT</span><span class="sxs-lookup"><span data-stu-id="0d0fd-222">.RPT</span></span>
- <span data-ttu-id="0d0fd-223">.RSS</span><span class="sxs-lookup"><span data-stu-id="0d0fd-223">.RSS</span></span>
- <span data-ttu-id="0d0fd-224">.SCPT</span><span class="sxs-lookup"><span data-stu-id="0d0fd-224">.SCPT</span></span>
- <span data-ttu-id="0d0fd-225">.SRC</span><span class="sxs-lookup"><span data-stu-id="0d0fd-225">.SRC</span></span>
- <span data-ttu-id="0d0fd-226">.VB\*</span><span class="sxs-lookup"><span data-stu-id="0d0fd-226">.VB\*</span></span>
- <span data-ttu-id="0d0fd-227">.WSF</span><span class="sxs-lookup"><span data-stu-id="0d0fd-227">.WSF</span></span>
- <span data-ttu-id="0d0fd-228">.XCODEPROJ</span><span class="sxs-lookup"><span data-stu-id="0d0fd-228">.XCODEPROJ</span></span>
- <span data-ttu-id="0d0fd-229">.XML</span><span class="sxs-lookup"><span data-stu-id="0d0fd-229">.XML</span></span>
- <span data-ttu-id="0d0fd-230">.XSD</span><span class="sxs-lookup"><span data-stu-id="0d0fd-230">.XSD</span></span>
- <span data-ttu-id="0d0fd-231">.XSL\*</span><span class="sxs-lookup"><span data-stu-id="0d0fd-231">.XSL\*</span></span>

## <a name="retain-video-files"></a><span data-ttu-id="0d0fd-232">Conservation des fichiers vidéo</span><span class="sxs-lookup"><span data-stu-id="0d0fd-232">Retain video files</span></span>

<span data-ttu-id="0d0fd-233">Cette recommandation s’affiche lorsque les types de fichiers suivants sont détectés dans SharePoint ou OneDrive.</span><span class="sxs-lookup"><span data-stu-id="0d0fd-233">This recommendation appears when any of the following file types are detected in SharePoint or OneDrive.</span></span>

- <span data-ttu-id="0d0fd-234">.AVCHD</span><span class="sxs-lookup"><span data-stu-id="0d0fd-234">.AVCHD</span></span>
- <span data-ttu-id="0d0fd-235">.AVI</span><span class="sxs-lookup"><span data-stu-id="0d0fd-235">.AVI</span></span>
- <span data-ttu-id="0d0fd-236">.FLV</span><span class="sxs-lookup"><span data-stu-id="0d0fd-236">.FLV</span></span>
- <span data-ttu-id="0d0fd-237">.MOV</span><span class="sxs-lookup"><span data-stu-id="0d0fd-237">.MOV</span></span>
- <span data-ttu-id="0d0fd-238">.MP2V</span><span class="sxs-lookup"><span data-stu-id="0d0fd-238">.MP2V</span></span>
- <span data-ttu-id="0d0fd-239">.MP4</span><span class="sxs-lookup"><span data-stu-id="0d0fd-239">.MP4</span></span>
- <span data-ttu-id="0d0fd-240">.MP4V</span><span class="sxs-lookup"><span data-stu-id="0d0fd-240">.MP4V</span></span>
- <span data-ttu-id="0d0fd-241">.MPE</span><span class="sxs-lookup"><span data-stu-id="0d0fd-241">.MPE</span></span>
- <span data-ttu-id="0d0fd-242">MPEG</span><span class="sxs-lookup"><span data-stu-id="0d0fd-242">.MPEG</span></span>
- <span data-ttu-id="0d0fd-243">.MPEG1</span><span class="sxs-lookup"><span data-stu-id="0d0fd-243">.MPEG1</span></span>
- <span data-ttu-id="0d0fd-244">.MPEG2</span><span class="sxs-lookup"><span data-stu-id="0d0fd-244">.MPEG2</span></span>
- <span data-ttu-id="0d0fd-245">.MPEG4</span><span class="sxs-lookup"><span data-stu-id="0d0fd-245">.MPEG4</span></span>
- <span data-ttu-id="0d0fd-246">.MPG</span><span class="sxs-lookup"><span data-stu-id="0d0fd-246">.MPG</span></span>
- <span data-ttu-id="0d0fd-247">.MPG2</span><span class="sxs-lookup"><span data-stu-id="0d0fd-247">.MPG2</span></span>
- <span data-ttu-id="0d0fd-248">.MPG4</span><span class="sxs-lookup"><span data-stu-id="0d0fd-248">.MPG4</span></span>
- <span data-ttu-id="0d0fd-249">.WMV</span><span class="sxs-lookup"><span data-stu-id="0d0fd-249">.WMV</span></span>
- <span data-ttu-id="0d0fd-250">.XMV</span><span class="sxs-lookup"><span data-stu-id="0d0fd-250">.XMV</span></span>
