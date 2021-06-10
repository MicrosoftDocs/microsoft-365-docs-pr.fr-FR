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
ms.openlocfilehash: 4530e570f0ce593a7d2cb62acc28dfa4e1658df0
ms.sourcegitcommit: 05f40904f8278f53643efa76a907968b5c662d9a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/30/2021
ms.locfileid: "52114082"
---
# <a name="get-started-with-the-default-dlp-policy"></a><span data-ttu-id="6bf82-103">Prise en main de la stratégie DLP par défaut</span><span class="sxs-lookup"><span data-stu-id="6bf82-103">Get started with the default DLP policy</span></span>

<span data-ttu-id="6bf82-104">Avant même de créer votre première stratégie de protection contre la perte de données (DLP), la protection contre la perte de données contribue à protéger vos informations sensibles avec une stratégie par défaut.</span><span class="sxs-lookup"><span data-stu-id="6bf82-104">Before you even create your first data loss prevention (DLP) policy, DLP is helping to protect your sensitive information with a default policy.</span></span> <span data-ttu-id="6bf82-105">Cette stratégie par défaut et ses recommandations (indiquées ci-dessous) permettent de sécuriser votre contenu sensible en vous notifiant lorsque des messages électroniques ou des documents contenant un numéro de carte de crédit ont été partagés avec une personne extérieure à votre organisation.</span><span class="sxs-lookup"><span data-stu-id="6bf82-105">This default policy and its recommendation (shown below) help keep your sensitive content secure by notifying you when email or documents containing a credit card number were shared with someone outside your organization.</span></span> <span data-ttu-id="6bf82-106">Vous verrez cette recommandation sur la page **d’accueil** du Centre de conformité &amp; de la sécurité.</span><span class="sxs-lookup"><span data-stu-id="6bf82-106">You'll see this recommendation on the **Home** page of the Security &amp; Compliance Center.</span></span> 
  
<span data-ttu-id="6bf82-107">Vous pouvez utiliser ce widget pour afficher rapidement quand et combien d’informations sensibles ont été partagées, puis affiner la stratégie DLP par défaut en un ou deux clics.</span><span class="sxs-lookup"><span data-stu-id="6bf82-107">You can use this widget to quickly view when and how much sensitive information was shared, and then refine the default DLP policy in just a click or two.</span></span> <span data-ttu-id="6bf82-108">Vous pouvez également modifier la stratégie DLP par défaut à tout moment, car elle est entièrement personnalisable.</span><span class="sxs-lookup"><span data-stu-id="6bf82-108">You can also edit the default DLP policy at any time because it's fully customizable.</span></span> <span data-ttu-id="6bf82-109">Notez que si vous ne voyez pas la recommandation au début, essayez de cliquer sur **+Plus** en bas de la section **Recommandé pour vous.**</span><span class="sxs-lookup"><span data-stu-id="6bf82-109">Note that if you don't see the recommendation at first, try clicking **+More** at the bottom of the **Recommended for you** section.</span></span> 
  
![Widget nommé Protéger davantage le contenu partagé](../media/2bae6dbc-cc92-4f35-b54c-c36e60226b5b.png)
  
## <a name="view-the-report-and-refine-the-default-dlp-policy"></a><span data-ttu-id="6bf82-111">Afficher le rapport et affiner la stratégie DLP par défaut</span><span class="sxs-lookup"><span data-stu-id="6bf82-111">View the report and refine the default DLP policy</span></span>

<span data-ttu-id="6bf82-112">Lorsque le widget vous indique que les utilisateurs ont partagé des informations sensibles avec des personnes extérieures à votre organisation, choisissez Affiner la stratégie **DLP** en bas.</span><span class="sxs-lookup"><span data-stu-id="6bf82-112">When the widget shows you that users have shared sensitive information with people outside your organization, choose **Refine DLP policy** at the bottom.</span></span> 
  
<span data-ttu-id="6bf82-113">Le rapport détaillé vous indique quand et combien de contenu contenant des numéros de carte de crédit ont été partagés au cours des 30 derniers jours.</span><span class="sxs-lookup"><span data-stu-id="6bf82-113">The detailed report shows you when and how much content containing credit card numbers was shared in the past 30 days.</span></span> <span data-ttu-id="6bf82-114">Notez que l’exposition des correspondances de règles dans le widget peut prendre jusqu’à 48 heures.</span><span class="sxs-lookup"><span data-stu-id="6bf82-114">Note that rule matches can take up to 48 hours to show up in the widget.</span></span>
  
<span data-ttu-id="6bf82-115">Pour protéger les informations sensibles, la stratégie DLP par défaut :</span><span class="sxs-lookup"><span data-stu-id="6bf82-115">To help protect the sensitive information, the default DLP policy:</span></span>
  
- <span data-ttu-id="6bf82-116">Détecte le moment où le contenu des Exchange, SharePoint et OneDrive contenant au moins un numéro de carte de crédit est partagé avec des personnes extérieures à votre organisation.</span><span class="sxs-lookup"><span data-stu-id="6bf82-116">Detects when content in Exchange, SharePoint, and OneDrive that contains at least one credit card number is shared with people outside your organization.</span></span>
    
- <span data-ttu-id="6bf82-117">Affiche un conseil de stratégie et envoie une notification par courrier électronique aux utilisateurs lorsqu’ils tentent de partager ces informations sensibles avec des personnes extérieures à votre organisation.</span><span class="sxs-lookup"><span data-stu-id="6bf82-117">Shows a policy tip and sends an email notification to users when they attempt to share this sensitive information with people outside your organization.</span></span> <span data-ttu-id="6bf82-118">Pour plus d’informations sur ces options, voir Envoyer des notifications par courrier électronique et afficher des conseils de stratégie [pour les stratégies DLP.](use-notifications-and-policy-tips.md)</span><span class="sxs-lookup"><span data-stu-id="6bf82-118">For more information on these options, see [Send email notifications and show policy tips for DLP policies](use-notifications-and-policy-tips.md).</span></span>
    
- <span data-ttu-id="6bf82-119">Génère des rapports d’activité détaillés afin que vous pouvez suivre des éléments tels que les personnes qui ont partagé le contenu avec des personnes extérieures à votre organisation et quand elles l’ont fait.</span><span class="sxs-lookup"><span data-stu-id="6bf82-119">Generates detailed activity reports so that you can track things like who shared the content with people outside your organization and when they did it.</span></span> <span data-ttu-id="6bf82-120">Vous pouvez utiliser les rapports [DLP](view-the-dlp-reports.md) et les données du journal [d’audit](search-the-audit-log-in-security-and-compliance.md) (où **Activité**  =  **DLP**) pour voir ces informations.</span><span class="sxs-lookup"><span data-stu-id="6bf82-120">You can use the [DLP reports](view-the-dlp-reports.md) and [audit log data](search-the-audit-log-in-security-and-compliance.md) (where **Activity** = **DLP**) to see this information.</span></span>
    
<span data-ttu-id="6bf82-121">Pour affiner rapidement la stratégie DLP par défaut, vous pouvez choisir de l’utiliser :</span><span class="sxs-lookup"><span data-stu-id="6bf82-121">To quickly refine the default DLP policy, you can choose to have it:</span></span>
  
- <span data-ttu-id="6bf82-122">Envoyez-vous un e-mail de rapport d’incident lorsque les utilisateurs partagent ces informations sensibles avec des personnes extérieures à votre organisation.</span><span class="sxs-lookup"><span data-stu-id="6bf82-122">Send you an incident report email when users share this sensitive information with people outside your organization.</span></span>
    
- <span data-ttu-id="6bf82-123">Ajoutez d’autres utilisateurs au rapport d’incident de courrier électronique.</span><span class="sxs-lookup"><span data-stu-id="6bf82-123">Add other users to the email incident report.</span></span>
    
- <span data-ttu-id="6bf82-124">Bloquez l’accès au contenu contenant les informations sensibles, mais autorisez l’utilisateur à remplacer, partager ou envoyer s’il le faut.</span><span class="sxs-lookup"><span data-stu-id="6bf82-124">Block access to the content containing the sensitive information, but allow the user to override and share or send if they need to.</span></span>
    
<span data-ttu-id="6bf82-125">Pour plus d’informations sur les rapports d’incident ou la restriction de l’accès, consultez la référence [de protection contre la perte de données.](data-loss-prevention-policies.md)</span><span class="sxs-lookup"><span data-stu-id="6bf82-125">For more information on incident reports or restricting access, see [Data loss prevention reference](data-loss-prevention-policies.md).</span></span>
  
<span data-ttu-id="6bf82-126">Si vous souhaitez modifier ces options ultérieurement, vous pouvez modifier la stratégie DLP par défaut à tout moment (voir la section suivante).</span><span class="sxs-lookup"><span data-stu-id="6bf82-126">If you want to change these options later, you can edit the default DLP policy at any time - see the next section.</span></span>
  
![Paramètres widget nommé Protéger davantage le contenu partagé](../media/dad30a84-2715-4c0a-a5c5-44d85492363e.png)
  
## <a name="edit-the-default-dlp-policy"></a><span data-ttu-id="6bf82-128">Modifier la stratégie DLP par défaut</span><span class="sxs-lookup"><span data-stu-id="6bf82-128">Edit the default DLP policy</span></span>

<span data-ttu-id="6bf82-129">Cette stratégie est nommée **Stratégie DLP par défaut** et apparaît sous Protection contre la perte de données dans la page Stratégie du Centre de conformité de   &amp; sécurité.</span><span class="sxs-lookup"><span data-stu-id="6bf82-129">This policy is named **Default DLP policy** and appears under **Data loss prevention** on the **Policy** page of the Security &amp; Compliance Center.</span></span> 
  
<span data-ttu-id="6bf82-130">Cette stratégie est entièrement personnalisable, comme toute stratégie DLP que vous créez vous-même à partir de zéro.</span><span class="sxs-lookup"><span data-stu-id="6bf82-130">This policy is fully customizable, the same as any DLP policy that you create yourself from scratch.</span></span> <span data-ttu-id="6bf82-131">Vous pouvez également désactiver ou supprimer la stratégie afin que vos utilisateurs ne reçoivent plus de conseils de stratégie ou de notifications par courrier électronique.</span><span class="sxs-lookup"><span data-stu-id="6bf82-131">You can also turn off or delete the policy, so that your users no longer receive policy tips or email notifications.</span></span>
  
![Stratégie DLP nommée Stratégie DLP par défaut](../media/260731e8-4d57-4c98-abec-07b052ec48d5.png)
  
## <a name="when-the-widget-does-and-does-not-appear"></a><span data-ttu-id="6bf82-133">Lorsque le widget s’affiche et n’apparaît pas</span><span class="sxs-lookup"><span data-stu-id="6bf82-133">When the widget does and does not appear</span></span>

<span data-ttu-id="6bf82-134">Le widget nommé **Protéger davantage le** contenu partagé apparaît dans la section Recommandé pour vous de la page **d’accueil** du Centre de conformité de la  &amp; sécurité.</span><span class="sxs-lookup"><span data-stu-id="6bf82-134">The widget named **Further protect shared content** appears in the **Recommended for you** section of the **Home** page of the Security &amp; Compliance Center.</span></span> 
  
<span data-ttu-id="6bf82-135">Ce widget apparaît uniquement lorsque :</span><span class="sxs-lookup"><span data-stu-id="6bf82-135">This widget appears only when:</span></span>
  
- <span data-ttu-id="6bf82-136">Il n’existe aucune stratégie de protection contre la perte de données dans le Centre de conformité de sécurité &amp; Exchange centre d’administration.</span><span class="sxs-lookup"><span data-stu-id="6bf82-136">There are no data loss prevention policies in the Security &amp; Compliance Center or Exchange admin center.</span></span> <span data-ttu-id="6bf82-137">Ce widget est destiné à vous aider à démarrer avec DLP, afin qu’il n’apparaisse pas si vous avez déjà des stratégies DLP.</span><span class="sxs-lookup"><span data-stu-id="6bf82-137">This widget is intended to help you get started with DLP, so it doesn't appear if you already have DLP policies.</span></span>
    
- <span data-ttu-id="6bf82-138">Le contenu contenant au moins une carte de crédit a été partagé avec une personne extérieure à votre organisation au cours des 30 derniers jours.</span><span class="sxs-lookup"><span data-stu-id="6bf82-138">Content containing least one credit card has been shared with someone outside your organization in the past 30 days.</span></span>
    
<span data-ttu-id="6bf82-139">Notez que les correspondances de règles peuvent prendre jusqu’à 48 heures pour être disponibles pour le widget. Ainsi, une fois que des informations sensibles partagées en externe sont détectées, la recommandation peut prendre jusqu’à deux jours.</span><span class="sxs-lookup"><span data-stu-id="6bf82-139">Note that rule matches can take up to 48 hours to be available to the widget, so after sensitive information shared externally is detected, it may take up to two days for the recommendation to appear.</span></span>
  
<span data-ttu-id="6bf82-140">Enfin, une fois que vous avez utilisé le widget pour affiner la stratégie DLP par défaut, le widget disparaît de la page **d’accueil.**</span><span class="sxs-lookup"><span data-stu-id="6bf82-140">Finally, after you use the widget to refine the default DLP policy, the widget disappears from the **Home** page.</span></span> 
  

