---
title: Réponse aux incidents de sécurité
f1.keywords:
- NOCSH
ms.author: chrfox
author: chrfox
manager: laurawi
ms.date: 04/27/2018
audience: ITPro
ms.topic: overview
ms.collection:
- o365_security_incident_response
- M365-security-compliance
localization_priority: Normal
search.appverid:
- MET150
description: Cette solution vous indique à quoi peuvent ressembler les attaques de cybersécurité les plus courantes dans Microsoft 365 et comment y répondre
ms.custom:
- seo-marvel-apr2020
ms.technology: mdo
ms.prod: m365-security
ms.openlocfilehash: 65ff75253f45ae2d0f051dafe73c6e665f89827a
ms.sourcegitcommit: dcb97fbfdae52960ae62b6faa707a05358193ed5
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/25/2021
ms.locfileid: "51204378"
---
# <a name="security-incident-response"></a><span data-ttu-id="2f309-103">Réponse aux incidents de sécurité</span><span class="sxs-lookup"><span data-stu-id="2f309-103">Security Incident Response</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../includes/microsoft-defender-for-office.md)]

<span data-ttu-id="2f309-104">**S’applique à**</span><span class="sxs-lookup"><span data-stu-id="2f309-104">**Applies to**</span></span>
- [<span data-ttu-id="2f309-105">Exchange Online Protection</span><span class="sxs-lookup"><span data-stu-id="2f309-105">Exchange Online Protection</span></span>](exchange-online-protection-overview.md)
- [<span data-ttu-id="2f309-106">Microsoft Defender pour Office 365 : offre 1 et offre 2</span><span class="sxs-lookup"><span data-stu-id="2f309-106">Microsoft Defender for Office 365 plan 1 and plan 2</span></span>](defender-for-office-365.md)
- [<span data-ttu-id="2f309-107">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="2f309-107">Microsoft 365 Defender</span></span>](../defender/microsoft-365-defender.md)

 <span data-ttu-id="2f309-108">**Résumé :** Cette solution vous indique quels sont les indicateurs des attaques de cybersécurité les plus courantes dans Office 365, comment confirmer les attaques données et comment y répondre.</span><span class="sxs-lookup"><span data-stu-id="2f309-108">**Summary:** This solution tells you what the indicators are for the most common cybersecurity attacks in Office 365, how to positively confirm any given attack, and how to respond to it.</span></span>

## <a name="learn-how-to-respond-to-cyberattacks"></a><span data-ttu-id="2f309-109">Découvrez comment répondre aux cyberattaques</span><span class="sxs-lookup"><span data-stu-id="2f309-109">Learn how to respond to cyberattacks</span></span>

<span data-ttu-id="2f309-110">Toutes les cyberattaques ne peuvent pas être déprécées.</span><span class="sxs-lookup"><span data-stu-id="2f309-110">Not all cyberattacks can be thwarted.</span></span> <span data-ttu-id="2f309-111">Les attaquants recherchent constamment de nouvelles faiblesses dans votre stratégie de sécurité ou exploitent des anciennes.</span><span class="sxs-lookup"><span data-stu-id="2f309-111">Attackers are constantly looking for new weaknesses in your defensive strategy or they are exploiting old ones.</span></span> <span data-ttu-id="2f309-112">Le fait de savoir reconnaître une attaque vous permet d’y répondre plus rapidement, ce qui réduit la durée de l’incident de sécurité.</span><span class="sxs-lookup"><span data-stu-id="2f309-112">Knowing how to recognize an attack allows you to respond to it faster, which shortens the duration of the security incident.</span></span>

<span data-ttu-id="2f309-113">Cette série d’articles vous aide à comprendre à quoi peut ressembler un type particulier d’attaque dans Microsoft 365 et vous donne les étapes à suivre pour y répondre.</span><span class="sxs-lookup"><span data-stu-id="2f309-113">This series of article helps you understand what a particular type of attack might look like in Microsoft 365 and gives you steps you can take to respond.</span></span> <span data-ttu-id="2f309-114">Ce sont des points d’entrée rapides pour comprendre :</span><span class="sxs-lookup"><span data-stu-id="2f309-114">They are quick entry points to understanding:</span></span>

- <span data-ttu-id="2f309-115">Qu’est-ce que l’attaque et comment elle fonctionne.</span><span class="sxs-lookup"><span data-stu-id="2f309-115">What the attack is and how it works.</span></span>

- <span data-ttu-id="2f309-116">Les signes, appelés indicateurs de compromis (IOC), à rechercher et comment les rechercher.</span><span class="sxs-lookup"><span data-stu-id="2f309-116">What signs, called indicators of compromise (IOC), to look for and how to look for them.</span></span>

- <span data-ttu-id="2f309-117">Comment confirmer l’attaque de manière positive.</span><span class="sxs-lookup"><span data-stu-id="2f309-117">How to positively confirm the attack.</span></span>

- <span data-ttu-id="2f309-118">Étapes à suivre pour réduire l’attaque et mieux protéger votre organisation à l’avenir.</span><span class="sxs-lookup"><span data-stu-id="2f309-118">Steps to take to cut off the attack and better protect your organization in the future.</span></span>

- <span data-ttu-id="2f309-119">Liens vers des informations détaillées sur chaque type d’attaque.</span><span class="sxs-lookup"><span data-stu-id="2f309-119">Links to in-depth information on each attack type.</span></span>

<span data-ttu-id="2f309-120">Consultez cet article tous les mois, car d’autres articles seront ajoutés au fil du temps.</span><span class="sxs-lookup"><span data-stu-id="2f309-120">Check back here monthly as more articles will be added over time.</span></span>

## <a name="detect-and-remediate-articles"></a><span data-ttu-id="2f309-121">Détecter et corriger les articles</span><span class="sxs-lookup"><span data-stu-id="2f309-121">Detect and remediate articles</span></span>

- [<span data-ttu-id="2f309-122">Détecter et résoudre les problèmes d’octroi illégal de consentement dans Office 365</span><span class="sxs-lookup"><span data-stu-id="2f309-122">Detect and Remediate Illicit Consent Grants in Office 365</span></span>](detect-and-remediate-illicit-consent-grants.md)

- [<span data-ttu-id="2f309-123">Détecter et résoudre les attaques par injections sur les règles d’Outlook et les formulaires personnalisés dans Office 365</span><span class="sxs-lookup"><span data-stu-id="2f309-123">Detect and Remediate Outlook Rules and Custom Forms Injections Attacks in Office 365</span></span>](detect-and-remediate-outlook-rules-forms-attack.md)

## <a name="incident-response-articles"></a><span data-ttu-id="2f309-124">Articles sur la réponse aux incidents</span><span class="sxs-lookup"><span data-stu-id="2f309-124">Incident response articles</span></span>

- [<span data-ttu-id="2f309-125">Réponse à un compte de messagerie compromis dans Office 365</span><span class="sxs-lookup"><span data-stu-id="2f309-125">Responding to a Compromised Email Account in Office 365</span></span>](responding-to-a-compromised-email-account.md)

## <a name="secure-microsoft-365-like-a-cybersecurity-pro"></a><span data-ttu-id="2f309-126">Sécuriser Microsoft 365 comme un pro de la cyber-sécurité</span><span class="sxs-lookup"><span data-stu-id="2f309-126">Secure Microsoft 365 like a cybersecurity pro</span></span>

<span data-ttu-id="2f309-127">Votre abonnement Microsoft 365 inclut un ensemble puissant de fonctionnalités de sécurité que vous pouvez utiliser pour protéger vos données et vos utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="2f309-127">Your Microsoft 365 subscription comes with a powerful set of security capabilities that you can use to protect your data and your users.</span></span>  <span data-ttu-id="2f309-128">Utilisez la feuille de route de sécurité Microsoft 365 - Principales priorités pour les [30 premiers jours, 90](security-roadmap.md) jours et au-delà pour implémenter les meilleures pratiques recommandées par Microsoft pour sécuriser votre organisation Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="2f309-128">Use the [Microsoft 365 security roadmap - Top priorities for the first 30 days, 90 days, and beyond](security-roadmap.md) to implement Microsoft recommended best practices for securing your Microsoft 365 organization.</span></span>

- <span data-ttu-id="2f309-129">Tâches à effectuer lors des 30 premiers jours.</span><span class="sxs-lookup"><span data-stu-id="2f309-129">Tasks to accomplish in the first 30 days.</span></span>  <span data-ttu-id="2f309-130">Elle ont un effet immédiat et n’ont qu’un faible impact négatif sur vos utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="2f309-130">These have immediate affect and are low-impact to your users.</span></span>

- <span data-ttu-id="2f309-131">Tâches à accomplir dans les 90 premiers jours.</span><span class="sxs-lookup"><span data-stu-id="2f309-131">Tasks to accomplish in 90 days.</span></span> <span data-ttu-id="2f309-132">La planifier et l’implémenter prennent un peu plus de temps, mais améliorent considérablement votre posture de sécurité.</span><span class="sxs-lookup"><span data-stu-id="2f309-132">These take a bit more time to plan and implement but greatly improve your security posture</span></span>

- <span data-ttu-id="2f309-133">Au-delà de 90 jours.</span><span class="sxs-lookup"><span data-stu-id="2f309-133">Beyond 90 days.</span></span> <span data-ttu-id="2f309-134">Ces améliorations sont à mettre en place pendant les 90 premiers jours.</span><span class="sxs-lookup"><span data-stu-id="2f309-134">These enhancements build in your first 90 days work.</span></span>
