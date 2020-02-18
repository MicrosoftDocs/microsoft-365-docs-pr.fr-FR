---
title: Configurer les paramètres de recherche et d’analyse
f1.keywords:
- NOCSH
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: ''
audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.collection: M365-security-compliance
search.appverid:
- MOE150
- MET150
ms.assetid: ''
description: ''
ms.openlocfilehash: bfd7c89531c2c1592f5e48f0c7656560831b392d
ms.sourcegitcommit: 3dd9944a6070a7f35c4bc2b57df397f844c3fe79
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/15/2020
ms.locfileid: "42078301"
---
# <a name="configure-search-and-analytics-settings"></a><span data-ttu-id="c6c5a-102">Configurer les paramètres de recherche et d’analyse</span><span class="sxs-lookup"><span data-stu-id="c6c5a-102">Configure search and analytics settings</span></span>

## <a name="near-duplicates-and-email-threading"></a><span data-ttu-id="c6c5a-103">Quasi-doublons et Threading de courrier électronique</span><span class="sxs-lookup"><span data-stu-id="c6c5a-103">Near duplicates and email threading</span></span>

<span data-ttu-id="c6c5a-104">Dans cette section, vous pouvez définir des paramètres pour la détection des doublons, la détection des doublons et le Threading de messagerie.</span><span class="sxs-lookup"><span data-stu-id="c6c5a-104">In this section, you can set parameters for duplicate detection, near duplicate detection, and email threading.</span></span>

- <span data-ttu-id="c6c5a-105">Activer/désactiver : inclut la détection des doublons, la détection à proximité des doublons et le Threading du courrier électronique dans le cadre du flux d’analyse s’il est activé.</span><span class="sxs-lookup"><span data-stu-id="c6c5a-105">Enable/disable: include duplicate detection, near duplicate detection, and email threading as part of analytics flow if enabled.</span></span> <span data-ttu-id="c6c5a-106">Étant donné qu’ils sont générés les uns sur les autres, vous devez tous les activer ou les désactiver tous.</span><span class="sxs-lookup"><span data-stu-id="c6c5a-106">Because they build on top of each other, you must enable all of them or disable all of them.</span></span>

- <span data-ttu-id="c6c5a-107">Seuil : si le niveau de similarité de deux documents est supérieur au seuil, ils seront placés dans le même ensemble presque en double.</span><span class="sxs-lookup"><span data-stu-id="c6c5a-107">Threshold: if the similarity level of two documents are above the threshold, they will be put in the same near duplicate set.</span></span>

- <span data-ttu-id="c6c5a-108">Masquer les doublons par défaut : si ce paramètre est activé, un filtre permettant de masquer les doublons de documents est appliqué par défaut dans le jeu de travail.</span><span class="sxs-lookup"><span data-stu-id="c6c5a-108">Hide duplicates by default: if this setting is on, a filter to hide duplicate documents will be applied in the working set by default.</span></span> <span data-ttu-id="c6c5a-109">Si nécessaire, le filtre peut être supprimé manuellement dans le jeu de travail.</span><span class="sxs-lookup"><span data-stu-id="c6c5a-109">The filter can be removed manually in the working set if necessary.</span></span>

- <span data-ttu-id="c6c5a-110">Nombre minimal/maximum de mots : les doublons et les threads de courrier électronique s’exécutent uniquement sur les documents qui contiennent au moins le nombre minimal de mots et le nombre maximal de mots.</span><span class="sxs-lookup"><span data-stu-id="c6c5a-110">Minimum/maximum number of words: near duplicates and email threading will run only on documents that have at least the minimum number of words and at most the maximum number of words.</span></span>
<span data-ttu-id="c6c5a-111">Pour plus d’informations, consultez la rubrique [near Detection Detection](near-duplicates.md) and [email Threading](email-threading.md).</span><span class="sxs-lookup"><span data-stu-id="c6c5a-111">For more information, see [Near duplicate detection](near-duplicates.md) and [Email threading](email-threading.md).</span></span>

## <a name="themes"></a><span data-ttu-id="c6c5a-112">Thèmes</span><span class="sxs-lookup"><span data-stu-id="c6c5a-112">Themes</span></span>

<span data-ttu-id="c6c5a-113">Dans cette section, vous pouvez définir des paramètres pour les thèmes.</span><span class="sxs-lookup"><span data-stu-id="c6c5a-113">In this section, you can set parameters for themes.</span></span>

- <span data-ttu-id="c6c5a-114">Activer/désactiver : inclut le clustering thèmes dans le cadre du flux d’analyse s’il est activé.</span><span class="sxs-lookup"><span data-stu-id="c6c5a-114">Enable/disable: include themes clustering as part of analytics flow if enabled.</span></span>
- <span data-ttu-id="c6c5a-115">Ajustez dynamiquement le nombre maximal de thèmes de façon dynamique : dans certains cas, il n’y a pas assez de documents pour produire le nombre souhaité de thèmes.</span><span class="sxs-lookup"><span data-stu-id="c6c5a-115">Adjust maximum number of themes dynamically dynamically: in certain cases, there are not enough documents to produce the desired number of themes.</span></span> <span data-ttu-id="c6c5a-116">Si ce paramètre est activé, au lieu d’essayer de forcer le nombre maximal de thèmes souhaités, le système ajuste le nombre maximal de thèmes de manière dynamique.</span><span class="sxs-lookup"><span data-stu-id="c6c5a-116">If this setting is turned on, then rather than trying to force the desired maximum number of themes, the system adjusts maximum number of themes dynamically.</span></span>
- <span data-ttu-id="c6c5a-117">Nombre maximal de thèmes : nombre souhaité de thèmes</span><span class="sxs-lookup"><span data-stu-id="c6c5a-117">Maximum number of themes: desired number of themes</span></span>
- <span data-ttu-id="c6c5a-118">Inclure les numéros dans les thèmes : lorsque ce dernier est activé, il inclut des numéros dans lors de la génération de thèmes.</span><span class="sxs-lookup"><span data-stu-id="c6c5a-118">Include numbers in themes: When enabled, it will include numbers in when generating themes.</span></span>  

## <a name="optical-character-recognition-ocr"></a><span data-ttu-id="c6c5a-119">Reconnaissance optique de caractères (OCR)</span><span class="sxs-lookup"><span data-stu-id="c6c5a-119">Optical character recognition (OCR)</span></span>

<span data-ttu-id="c6c5a-120">Lorsque ce paramètre est activé, la reconnaissance optique de caractères est exécutée sur les images qui sont ingérées dans les jeux de travail afin qu’ils puissent être recherchés.</span><span class="sxs-lookup"><span data-stu-id="c6c5a-120">When this setting is turned on, OCR will be run on images that are ingested into working sets so that they can be searchable.</span></span>

## <a name="ignore-text"></a><span data-ttu-id="c6c5a-121">Ignorer le texte</span><span class="sxs-lookup"><span data-stu-id="c6c5a-121">Ignore text</span></span>

<span data-ttu-id="c6c5a-122">Il existe des situations dans lesquelles certains textes réduisent la qualité de l’analyse, tels que des clauses de responsabilité longues qui sont ajoutées à certains courriers électroniques indépendamment du contenu du message.</span><span class="sxs-lookup"><span data-stu-id="c6c5a-122">There are instances where certain texts will diminish the quality of analytics, such as lengthy disclaimers that get added to certain emails regardless of the content of the email.</span></span> <span data-ttu-id="c6c5a-123">Si vous avez conscience de ces cas, vous pouvez exclure ce texte de l’analyse en spécifiant le texte (RegEx est pris en charge) et les modules pour lesquels le texte doit être exclu.</span><span class="sxs-lookup"><span data-stu-id="c6c5a-123">If you are aware of such cases, you can exclude this text from analytics by specifying the text (RegEx is supported) and which modules that text should be excluded for.</span></span>
