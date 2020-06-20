---
title: Prise en main de la stratégie DLP par défaut
f1.keywords:
- NOCSH
ms.author: chrfox
author: chrfox
manager: laurawi
ms.date: 8/10/2017
audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MOE150
- MET150
ms.assetid: e0ada764-6422-4b44-9472-513bed04837b
ms.collection:
- M365-security-compliance
ms.custom:
- seo-marvel-apr2020
description: Découvrez comment utiliser le rapport pour affiner la stratégie de protection contre la perte de données (DLP) par défaut de votre organisation.
ms.openlocfilehash: 7c8f0460f9cd02ee3d26197965f5ea74737ac833
ms.sourcegitcommit: 973f5449784cb70ce5545bc3cf57bf1ce5209218
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/19/2020
ms.locfileid: "44817613"
---
# <a name="get-started-with-the-default-dlp-policy"></a><span data-ttu-id="1334f-103">Prise en main de la stratégie DLP par défaut</span><span class="sxs-lookup"><span data-stu-id="1334f-103">Get started with the default DLP policy</span></span>

<span data-ttu-id="1334f-104">Avant de créer votre première stratégie de protection contre la perte de données (DLP), DLP contribue à protéger vos informations sensibles à l’aide d’une stratégie par défaut.</span><span class="sxs-lookup"><span data-stu-id="1334f-104">Before you even create your first data loss prevention (DLP) policy, DLP is helping to protect your sensitive information with a default policy.</span></span> <span data-ttu-id="1334f-105">Cette stratégie par défaut et ses recommandations (illustrées ci-dessous) vous permettent de sécuriser votre contenu sensible en vous avertissant que des messages ou des documents contenant un numéro de carte de crédit ont été partagés avec une personne extérieure à votre organisation.</span><span class="sxs-lookup"><span data-stu-id="1334f-105">This default policy and its recommendation (shown below) help keep your sensitive content secure by notifying you when email or documents containing a credit card number were shared with someone outside your organization.</span></span> <span data-ttu-id="1334f-106">Cette recommandation s’affiche sur la page d' **Accueil** du centre de sécurité et de &amp; conformité.</span><span class="sxs-lookup"><span data-stu-id="1334f-106">You'll see this recommendation on the **Home** page of the Security &amp; Compliance Center.</span></span> 
  
<span data-ttu-id="1334f-107">Vous pouvez utiliser ce widget pour afficher rapidement quand et comment les informations sensibles ont été partagées, puis affiner la stratégie DLP par défaut dans un ou deux.</span><span class="sxs-lookup"><span data-stu-id="1334f-107">You can use this widget to quickly view when and how much sensitive information was shared, and then refine the default DLP policy in just a click or two.</span></span> <span data-ttu-id="1334f-108">Vous pouvez également modifier la stratégie DLP par défaut à tout moment, car elle est entièrement personnalisable.</span><span class="sxs-lookup"><span data-stu-id="1334f-108">You can also edit the default DLP policy at any time because it's fully customizable.</span></span> <span data-ttu-id="1334f-109">Notez que si vous ne voyez pas la recommandation, essayez de cliquer sur **+ autres** en bas de la section **recommandé pour vous** .</span><span class="sxs-lookup"><span data-stu-id="1334f-109">Note that if you don't see the recommendation at first, try clicking **+More** at the bottom of the **Recommended for you** section.</span></span> 
  
![Widget nommé protection supplémentaire protéger le contenu partagé](../media/2bae6dbc-cc92-4f35-b54c-c36e60226b5b.png)
  
## <a name="view-the-report-and-refine-the-default-dlp-policy"></a><span data-ttu-id="1334f-111">Afficher le rapport et affiner la stratégie DLP par défaut</span><span class="sxs-lookup"><span data-stu-id="1334f-111">View the report and refine the default DLP policy</span></span>

<span data-ttu-id="1334f-112">Lorsque le widget vous montre que les utilisateurs ont partagé des informations sensibles avec des personnes extérieures à votre organisation, choisissez **affiner la stratégie DLP** en bas.</span><span class="sxs-lookup"><span data-stu-id="1334f-112">When the widget shows you that users have shared sensitive information with people outside your organization, choose **Refine DLP policy** at the bottom.</span></span> 
  
<span data-ttu-id="1334f-113">Le rapport détaillé indique quand et quelle proportion de contenu contenant des numéros de carte de crédit a été partagé au cours des 30 derniers jours.</span><span class="sxs-lookup"><span data-stu-id="1334f-113">The detailed report shows you when and how much content containing credit card numbers was shared in the past 30 days.</span></span> <span data-ttu-id="1334f-114">Notez que les correspondances de règle peuvent prendre jusqu’à 48 heures pour apparaître dans le widget.</span><span class="sxs-lookup"><span data-stu-id="1334f-114">Note that rule matches can take up to 48 hours to show up in the widget.</span></span>
  
<span data-ttu-id="1334f-115">Pour protéger les informations sensibles, la stratégie DLP par défaut :</span><span class="sxs-lookup"><span data-stu-id="1334f-115">To help protect the sensitive information, the default DLP policy:</span></span>
  
- <span data-ttu-id="1334f-116">Détecte quand le contenu dans Exchange, SharePoint et OneDrive qui contient au moins un numéro de carte de crédit est partagé avec des personnes extérieures à votre organisation.</span><span class="sxs-lookup"><span data-stu-id="1334f-116">Detects when content in Exchange, SharePoint, and OneDrive that contains at least one credit card number is shared with people outside your organization.</span></span>
    
- <span data-ttu-id="1334f-117">Affiche un Conseil de stratégie et envoie une notification par courrier électronique aux utilisateurs lorsqu’ils essaient de partager ces informations sensibles avec des personnes extérieures à votre organisation.</span><span class="sxs-lookup"><span data-stu-id="1334f-117">Shows a policy tip and sends an email notification to users when they attempt to share this sensitive information with people outside your organization.</span></span> <span data-ttu-id="1334f-118">Pour plus d’informations sur ces options, consultez la rubrique [Envoyer des notifications par courrier électronique et afficher les conseils de stratégie pour les stratégies DLP](use-notifications-and-policy-tips.md).</span><span class="sxs-lookup"><span data-stu-id="1334f-118">For more information on these options, see [Send email notifications and show policy tips for DLP policies](use-notifications-and-policy-tips.md).</span></span>
    
- <span data-ttu-id="1334f-119">Génère des rapports d’activité détaillés pour vous permettre d’effectuer le suivi des éléments tels que le partage du contenu avec des personnes extérieures à votre organisation et à quel moment.</span><span class="sxs-lookup"><span data-stu-id="1334f-119">Generates detailed activity reports so that you can track things like who shared the content with people outside your organization and when they did it.</span></span> <span data-ttu-id="1334f-120">Vous pouvez utiliser les [données du journal d’audit](search-the-audit-log-in-security-and-compliance.md) et des [rapports DLP](view-the-dlp-reports.md) **(Where**  =  **DLP**) pour afficher ces informations.</span><span class="sxs-lookup"><span data-stu-id="1334f-120">You can use the [DLP reports](view-the-dlp-reports.md) and [audit log data](search-the-audit-log-in-security-and-compliance.md) (where **Activity** = **DLP**) to see this information.</span></span>
    
<span data-ttu-id="1334f-121">Pour affiner rapidement la stratégie DLP par défaut, vous pouvez choisir de la faire :</span><span class="sxs-lookup"><span data-stu-id="1334f-121">To quickly refine the default DLP policy, you can choose to have it:</span></span>
  
- <span data-ttu-id="1334f-122">Vous envoyer un rapport d’incident par courrier électronique lorsque les utilisateurs partagent ces informations sensibles avec des personnes extérieures à votre organisation.</span><span class="sxs-lookup"><span data-stu-id="1334f-122">Send you an incident report email when users share this sensitive information with people outside your organization.</span></span>
    
- <span data-ttu-id="1334f-123">Ajouter d’autres utilisateurs au rapport d’incident de courrier électronique.</span><span class="sxs-lookup"><span data-stu-id="1334f-123">Add other users to the email incident report.</span></span>
    
- <span data-ttu-id="1334f-124">Bloquer l’accès au contenu contenant les informations sensibles, tout en permettant à l’utilisateur de le remplacer et de le partager ou de l’envoyer si nécessaire.</span><span class="sxs-lookup"><span data-stu-id="1334f-124">Block access to the content containing the sensitive information, but allow the user to override and share or send if they need to.</span></span>
    
<span data-ttu-id="1334f-125">Pour plus d’informations sur les rapports d’incident ou la limitation de l’accès, voir [Overview of Data Loss Prevention Policies](data-loss-prevention-policies.md).</span><span class="sxs-lookup"><span data-stu-id="1334f-125">For more information on incident reports or restricting access, see [Overview of data loss prevention policies](data-loss-prevention-policies.md).</span></span>
  
<span data-ttu-id="1334f-126">Si vous souhaitez modifier ces options ultérieurement, vous pouvez modifier la stratégie DLP par défaut à tout moment-consultez la section suivante.</span><span class="sxs-lookup"><span data-stu-id="1334f-126">If you want to change these options later, you can edit the default DLP policy at any time - see the next section.</span></span>
  
![Paramètres du widget nommé protection supplémentaire protéger le contenu partagé](../media/dad30a84-2715-4c0a-a5c5-44d85492363e.png)
  
## <a name="edit-the-default-dlp-policy"></a><span data-ttu-id="1334f-128">Modifier la stratégie DLP par défaut</span><span class="sxs-lookup"><span data-stu-id="1334f-128">Edit the default DLP policy</span></span>

<span data-ttu-id="1334f-129">Cette stratégie est nommée **stratégie DLP par défaut** et apparaît sous **protection contre la perte de données** dans la page **stratégie** du centre de sécurité et de &amp; conformité.</span><span class="sxs-lookup"><span data-stu-id="1334f-129">This policy is named **Default DLP policy** and appears under **Data loss prevention** on the **Policy** page of the Security &amp; Compliance Center.</span></span> 
  
<span data-ttu-id="1334f-130">Cette stratégie est entièrement personnalisable, comme n’importe quelle stratégie DLP que vous créez vous-même de toutes pièces.</span><span class="sxs-lookup"><span data-stu-id="1334f-130">This policy is fully customizable, the same as any DLP policy that you create yourself from scratch.</span></span> <span data-ttu-id="1334f-131">Vous pouvez également désactiver ou supprimer la stratégie, afin que vos utilisateurs ne reçoivent plus de conseils de stratégie ou de notifications par courrier électronique.</span><span class="sxs-lookup"><span data-stu-id="1334f-131">You can also turn off or delete the policy, so that your users no longer receive policy tips or email notifications.</span></span>
  
![Stratégie DLP nommée Stratégie DLP par défaut](../media/260731e8-4d57-4c98-abec-07b052ec48d5.png)
  
## <a name="when-the-widget-does-and-does-not-appear"></a><span data-ttu-id="1334f-133">Lorsque le widget n’apparaît pas</span><span class="sxs-lookup"><span data-stu-id="1334f-133">When the widget does and does not appear</span></span>

<span data-ttu-id="1334f-134">Le widget nommé **protection supplémentaire protéger le contenu partagé** apparaît dans la section **recommandé pour vous** de la page d' **Accueil** du centre de sécurité et de &amp; conformité.</span><span class="sxs-lookup"><span data-stu-id="1334f-134">The widget named **Further protect shared content** appears in the **Recommended for you** section of the **Home** page of the Security &amp; Compliance Center.</span></span> 
  
<span data-ttu-id="1334f-135">Ce widget apparaît uniquement dans les cas suivants :</span><span class="sxs-lookup"><span data-stu-id="1334f-135">This widget appears only when:</span></span>
  
- <span data-ttu-id="1334f-136">Il n’existe aucune stratégie de protection contre la perte de données dans le &amp; Centre d’administration et de sécurité.</span><span class="sxs-lookup"><span data-stu-id="1334f-136">There are no data loss prevention policies in the Security &amp; Compliance Center or Exchange admin center.</span></span> <span data-ttu-id="1334f-137">Ce widget est conçu pour vous aider à commencer à utiliser DLP, il n’apparaît donc pas si vous avez déjà des stratégies DLP.</span><span class="sxs-lookup"><span data-stu-id="1334f-137">This widget is intended to help you get started with DLP, so it doesn't appear if you already have DLP policies.</span></span>
    
- <span data-ttu-id="1334f-138">Le contenu contenant moins une carte de crédit a été partagé avec une personne extérieure à votre organisation au cours des 30 derniers jours.</span><span class="sxs-lookup"><span data-stu-id="1334f-138">Content containing least one credit card has been shared with someone outside your organization in the past 30 days.</span></span>
    
<span data-ttu-id="1334f-139">Notez que les correspondances de règle peuvent prendre jusqu’à 48 heures pour être disponibles pour le widget, ainsi une fois que les informations sensibles partagées en externe sont détectées, il peut falloir jusqu’à deux jours pour que la recommandation s’affiche.</span><span class="sxs-lookup"><span data-stu-id="1334f-139">Note that rule matches can take up to 48 hours to be available to the widget, so after sensitive information shared externally is detected, it may take up to two days for the recommendation to appear.</span></span>
  
<span data-ttu-id="1334f-140">Enfin, une fois que vous avez utilisé le widget pour affiner la stratégie DLP par défaut, le widget disparaît de la page d' **Accueil** .</span><span class="sxs-lookup"><span data-stu-id="1334f-140">Finally, after you use the widget to refine the default DLP policy, the widget disappears from the **Home** page.</span></span> 
  

