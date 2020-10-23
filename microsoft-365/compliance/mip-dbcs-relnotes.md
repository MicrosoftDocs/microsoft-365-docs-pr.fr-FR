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
ms.openlocfilehash: 1c2244c49a92aa2c00fad06caa8194cf7e32220e
ms.sourcegitcommit: 554755bc9ce40228ce6e34bde6fc6e226869b6a1
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/22/2020
ms.locfileid: "48681500"
---
# <a name="support-for-double-byte-character-set-release-notes-preview"></a><span data-ttu-id="cd28c-103">Prise en charge des notes de publication des jeux de caractères à double octets (préversion)</span><span class="sxs-lookup"><span data-stu-id="cd28c-103">Support for double byte character set release notes (preview)</span></span>

 <span data-ttu-id="cd28c-104">Microsoft 365 Information Protection prend désormais en charge, en préversion, les langues de jeu de caractères à double octets pour :</span><span class="sxs-lookup"><span data-stu-id="cd28c-104">Microsoft 365 Information Protection now supports in preview double byte character set languages for:</span></span>

- <span data-ttu-id="cd28c-105">le chinois simplifié</span><span class="sxs-lookup"><span data-stu-id="cd28c-105">Chinese (simplified)</span></span>
- <span data-ttu-id="cd28c-106">Chinois (traditionnel)</span><span class="sxs-lookup"><span data-stu-id="cd28c-106">Chinese (traditional)</span></span>
- <span data-ttu-id="cd28c-107">Korean</span><span class="sxs-lookup"><span data-stu-id="cd28c-107">Korean</span></span>
- <span data-ttu-id="cd28c-108">Japanese</span><span class="sxs-lookup"><span data-stu-id="cd28c-108">Japanese</span></span>

<span data-ttu-id="cd28c-109">Cette prise en charge est disponible pour les types d’informations sensibles et les dictionnaires de mots-clés et sera affichée dans les solutions de protection contre la perte de données, de conformité des communications, Exchange Online, SharePoint Online, OneDrive Entreprise et Teams.</span><span class="sxs-lookup"><span data-stu-id="cd28c-109">This support is available for sensitive information types and keyword dictionaries and will be reflected in data loss prevention, communications compliance, Exchange Online, SharePoint Online, OneDrive for Business, and Teams solutions.</span></span>

## <a name="known-issues"></a><span data-ttu-id="cd28c-110">Problèmes connus</span><span class="sxs-lookup"><span data-stu-id="cd28c-110">Known issues</span></span>

- <span data-ttu-id="cd28c-111">Lorsqu’un fichier texte joint à un e-mail est au format UTF-8 sans indicateur d’ordre des octets (BOM), l’e-mail n’est pas détecté par la stratégie de conformité des communications.</span><span class="sxs-lookup"><span data-stu-id="cd28c-111">When a text file attached to an email is in UTF-8 format without byte order mark (BOM), the email is not detected by the Communication Compliance policy.</span></span>

- <span data-ttu-id="cd28c-112">Les stratégies de conformité des communications ne peuvent pas détecter de valeurs si une phrase est saisie pour la condition de stratégie : « Le message contient l’un de ces mots ».</span><span class="sxs-lookup"><span data-stu-id="cd28c-112">Communication Compliance policies cannot detect values if a sentence is entered for the policy condition: “Message contains any of these words”.</span></span> <span data-ttu-id="cd28c-113">Si le texte spécifié dans la stratégie est écrit sous forme de mot, il peut être détecté. Cependant, s’il est écrit au milieu d’une phrase, il ne sera pas détecté.</span><span class="sxs-lookup"><span data-stu-id="cd28c-113">If the text specified in the policy is written as a word, it can be detected; however, if it is written in the middle of a sentence, it will not be detected.</span></span>

- <span data-ttu-id="cd28c-114">Les stratégies de conformité des communications qui spécifient des dictionnaires comme informations de type ne détectent pas les discussions privées et les discussions de canal Teams.</span><span class="sxs-lookup"><span data-stu-id="cd28c-114">Communication Compliance policies that specify dictionaries as type information do not detect Teams private chats and channel chats.</span></span>

- <span data-ttu-id="cd28c-115">Les conditions suivantes ne sont pas prises en charge pour la conformité des communications à ce stade (nous prévoyons de résoudre ces problèmes à l’avenir) :</span><span class="sxs-lookup"><span data-stu-id="cd28c-115">The following conditions are not supported for Communication Compliance at this stage (we plan to fix these issues in the future):</span></span> 
  - <span data-ttu-id="cd28c-116">« Le message contient l’un de ces mots »</span><span class="sxs-lookup"><span data-stu-id="cd28c-116">“Message contains any of these words”</span></span>
  - <span data-ttu-id="cd28c-117">« Le message ne contient aucun de ces mots »</span><span class="sxs-lookup"><span data-stu-id="cd28c-117">“Message contains none of these words”</span></span>
  - <span data-ttu-id="cd28c-118">« La pièce jointe contient l’un de ces mots »</span><span class="sxs-lookup"><span data-stu-id="cd28c-118">“Attachment contains any of these words”</span></span>
  - <span data-ttu-id="cd28c-119">« La pièce jointe contient l’un de ces mots »</span><span class="sxs-lookup"><span data-stu-id="cd28c-119">“Attachment contains any of these words”</span></span>

<span data-ttu-id="cd28c-120">Nous vous recommandons plutôt de créer un type d’informations sensibles personnalisé, avec un dictionnaire de mots-clés, qui détectera les modèles dans les messages et les pièces jointes, et d’utiliser ce type d’informations sensibles personnalisé comme condition de stratégie de conformité des communications.</span><span class="sxs-lookup"><span data-stu-id="cd28c-120">Instead we recommend creating a custom Sensitive Information Type (SIT) with keyword dictionary which will detect patterns across messages and attachments, and using this custom SIT as a Communication Compliance policy condition.</span></span>
