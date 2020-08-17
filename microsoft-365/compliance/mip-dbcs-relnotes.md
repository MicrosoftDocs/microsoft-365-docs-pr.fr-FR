---
title: Prise en charge de la conformité Microsoft 365 pour les notes de publication des jeux de caractères à double octets (préversion)
ms.author: chrfox
author: chrfox
manager: laurawi
ms.date: ''
audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Priority
ms.collection:
- M365-security-compliance
search.appverid:
- MOE150
- MET150
description: Notes de publication pour la prise en charge des jeux de caractères à double octets.
ms.openlocfilehash: 13bac873f2ba18bc166451ea73ec0d569fb30f68
ms.sourcegitcommit: 79065e72c0799064e9055022393113dfcf40eb4b
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/14/2020
ms.locfileid: "46695245"
---
# <a name="support-for-double-byte-character-set-release-notes-preview"></a><span data-ttu-id="c5001-103">Prise en charge des notes de publication des jeux de caractères à double octets (préversion)</span><span class="sxs-lookup"><span data-stu-id="c5001-103">Support for double byte character set release notes (preview)</span></span>

 <span data-ttu-id="c5001-104">Microsoft 365 Information Protection prend désormais en charge, en préversion, les langues de jeu de caractères à double octets pour :</span><span class="sxs-lookup"><span data-stu-id="c5001-104">Microsoft 365 Information Protection now supports in preview double byte character set languages for:</span></span>

- <span data-ttu-id="c5001-105">le chinois simplifié</span><span class="sxs-lookup"><span data-stu-id="c5001-105">Chinese (simplified)</span></span>
- <span data-ttu-id="c5001-106">le chinois traditionnel</span><span class="sxs-lookup"><span data-stu-id="c5001-106">Chinese (traditional)</span></span>
- <span data-ttu-id="c5001-107">le coréen</span><span class="sxs-lookup"><span data-stu-id="c5001-107">Korean</span></span>
- <span data-ttu-id="c5001-108">le japonais</span><span class="sxs-lookup"><span data-stu-id="c5001-108">Japanese</span></span>

<span data-ttu-id="c5001-109">Cette préversion est uniquement disponible dans le cloud commercial et le déploiement est limité aux pays suivants :</span><span class="sxs-lookup"><span data-stu-id="c5001-109">This preview is only in the commercial cloud and the rollout is limited to:</span></span>

- <span data-ttu-id="c5001-110">Japon</span><span class="sxs-lookup"><span data-stu-id="c5001-110">Japan</span></span>
- <span data-ttu-id="c5001-111">Corée</span><span class="sxs-lookup"><span data-stu-id="c5001-111">Korea</span></span>
- <span data-ttu-id="c5001-112">Chine</span><span class="sxs-lookup"><span data-stu-id="c5001-112">China</span></span>
- <span data-ttu-id="c5001-113">Hong Kong (R.A.S.)</span><span class="sxs-lookup"><span data-stu-id="c5001-113">Hong Kong</span></span>
- <span data-ttu-id="c5001-114">Macao R.A.S</span><span class="sxs-lookup"><span data-stu-id="c5001-114">Macau</span></span>
- <span data-ttu-id="c5001-115">Taïwan</span><span class="sxs-lookup"><span data-stu-id="c5001-115">Taiwan</span></span>

<span data-ttu-id="c5001-116">Cette prise en charge est disponible pour les types d’informations sensibles et les dictionnaires de mots-clés et sera affichée dans les solutions de protection contre la perte de données, de conformité des communications, Exchange Online, SharePoint Online, OneDrive Entreprise et Teams.</span><span class="sxs-lookup"><span data-stu-id="c5001-116">This support is available for sensitive information types and keyword dictionaries and will be reflected in data loss prevention, communications compliance, Exchange Online, SharePoint Online, OneDrive for Business, and Teams solutions.</span></span>

## <a name="known-issues"></a><span data-ttu-id="c5001-117">Problèmes connus</span><span class="sxs-lookup"><span data-stu-id="c5001-117">Known issues</span></span>

- <span data-ttu-id="c5001-118">Lorsqu’un fichier texte joint à un e-mail est au format UTF-8 sans indicateur d’ordre des octets (BOM), l’e-mail n’est pas détecté par la stratégie de conformité des communications.</span><span class="sxs-lookup"><span data-stu-id="c5001-118">When a text file attached to an email is in UTF-8 format without byte order mark (BOM), the email is not detected by the Communication Compliance policy.</span></span>

- <span data-ttu-id="c5001-119">Les stratégies de conformité des communications ne peuvent pas détecter de valeurs si une phrase est saisie pour la condition de stratégie : « Le message contient l’un de ces mots ».</span><span class="sxs-lookup"><span data-stu-id="c5001-119">Communication Compliance policies cannot detect values if a sentence is entered for the policy condition: “Message contains any of these words”.</span></span> <span data-ttu-id="c5001-120">Si le texte spécifié dans la stratégie est écrit sous forme de mot, il peut être détecté. Cependant, s’il est écrit au milieu d’une phrase, il ne sera pas détecté.</span><span class="sxs-lookup"><span data-stu-id="c5001-120">If the text specified in the policy is written as a word, it can be detected; however, if it is written in the middle of a sentence, it will not be detected.</span></span>

- <span data-ttu-id="c5001-121">Les stratégies de conformité des communications qui spécifient des dictionnaires comme informations de type ne détectent pas les discussions privées et les discussions de canal Teams.</span><span class="sxs-lookup"><span data-stu-id="c5001-121">Communication Compliance policies that specify dictionaries as type information do not detect Teams private chats and channel chats.</span></span>

- <span data-ttu-id="c5001-122">Les conditions suivantes ne sont pas prises en charge pour la conformité des communications à ce stade (nous prévoyons de résoudre ces problèmes à l’avenir) :</span><span class="sxs-lookup"><span data-stu-id="c5001-122">The following conditions are not supported for Communication Compliance at this stage (we plan to fix these issues in the future):</span></span> 
  - <span data-ttu-id="c5001-123">« Le message contient l’un de ces mots »</span><span class="sxs-lookup"><span data-stu-id="c5001-123">“Message contains any of these words”</span></span>
  - <span data-ttu-id="c5001-124">« Le message ne contient aucun de ces mots »</span><span class="sxs-lookup"><span data-stu-id="c5001-124">“Message contains none of these words”</span></span>
  - <span data-ttu-id="c5001-125">« La pièce jointe contient l’un de ces mots »</span><span class="sxs-lookup"><span data-stu-id="c5001-125">“Attachment contains any of these words”</span></span>
  - <span data-ttu-id="c5001-126">« La pièce jointe contient l’un de ces mots »</span><span class="sxs-lookup"><span data-stu-id="c5001-126">“Attachment contains any of these words”</span></span>

<span data-ttu-id="c5001-127">Nous vous recommandons plutôt de créer un type d’informations sensibles personnalisé, avec un dictionnaire de mots-clés, qui détectera les modèles dans les messages et les pièces jointes, et d’utiliser ce type d’informations sensibles personnalisé comme condition de stratégie de conformité des communications.</span><span class="sxs-lookup"><span data-stu-id="c5001-127">Instead we recommend creating a custom Sensitive Information Type (SIT) with keyword dictionary which will detect patterns across messages and attachments, and using this custom SIT as a Communication Compliance policy condition.</span></span>
