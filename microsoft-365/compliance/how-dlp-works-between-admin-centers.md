---
title: Fonctionnement de DLP avec le Centre de sécurité & conformité & Exchange’administration
f1.keywords:
- NOCSH
ms.author: chrfox
author: chrfox
manager: laurawi
ms.date: ''
audience: Admin
ms.topic: conceptual
ms.service: O365-seccomp
ms.collection:
- M365-security-compliance
localization_priority: Normal
search.appverid:
- MOE150
- MET150
ms.assetid: a7e4342a-a0a1-4b43-b166-3d7eecf5d2fd
description: Découvrez comment DLP dans le Centre de sécurité et conformité & fonctionne avec DLP et les règles de flux de messagerie (règles de transport) dans le Centre d’administration Exchange de sécurité.
ms.custom: seo-marvel-apr2020
ms.openlocfilehash: a7cd4eaafbd334c8886e0e6aa72d8c0e4c53a81e
ms.sourcegitcommit: 17d82e5617f0466eb825e15ab88594afcdaf4437
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/06/2021
ms.locfileid: "53300051"
---
# <a name="how-dlp-works-between-the-microsoft-365-compliance-center-and-exchange-admin-center"></a><span data-ttu-id="967d6-103">Fonctionnement de la DLP entre le Centre Microsoft 365 conformité et Exchange’administration centrale</span><span class="sxs-lookup"><span data-stu-id="967d6-103">How DLP works between the Microsoft 365 Compliance Center and Exchange admin center</span></span>

<span data-ttu-id="967d6-104">Dans Microsoft 365, vous pouvez créer une stratégie de protection contre la perte de données (DLP) dans deux centres d’administration différents :</span><span class="sxs-lookup"><span data-stu-id="967d6-104">In Microsoft 365, you can create a data loss prevention (DLP) policy in two different admin centers:</span></span>
  
- <span data-ttu-id="967d6-105">Dans le Centre de conformité **Microsoft 365,** vous pouvez créer une stratégie DLP unique pour protéger le contenu dans les appareils SharePoint, OneDrive, Exchange, Teams et désormais les points de terminaison.</span><span class="sxs-lookup"><span data-stu-id="967d6-105">In the **Microsoft 365 Compliance Center**, you can create a single DLP policy to help protect content in SharePoint, OneDrive, Exchange, Teams, and now Endpoint Devices.</span></span> <span data-ttu-id="967d6-106">Nous vous recommandons de créer une stratégie DLP ici.</span><span class="sxs-lookup"><span data-stu-id="967d6-106">We recommend that you create a DLP policy here.</span></span> <span data-ttu-id="967d6-107">Pour plus d’informations, [voir la référence sur la protection contre la perte de données.](data-loss-prevention-policies.md)</span><span class="sxs-lookup"><span data-stu-id="967d6-107">For more information, see [Data Loss Prevention reference](data-loss-prevention-policies.md).</span></span>
    
- <span data-ttu-id="967d6-108">Dans le **Exchange d’administration,** vous pouvez créer une stratégie DLP pour protéger le contenu uniquement dans Exchange.</span><span class="sxs-lookup"><span data-stu-id="967d6-108">In the **Exchange admin center**, you can create a DLP policy to help protect content only in Exchange.</span></span> <span data-ttu-id="967d6-109">Cette stratégie peut utiliser Exchange règles de flux de messagerie (également appelées règles de transport), de sorte qu’elle dispose d’autres options spécifiques à la gestion du courrier électronique.</span><span class="sxs-lookup"><span data-stu-id="967d6-109">This policy can use Exchange mail flow rules (also known as transport rules), so it has more options specific to handling email.</span></span> <span data-ttu-id="967d6-110">Pour plus d’informations, voir [DLP dans le centre Exchange’administration.](/exchange/security-and-compliance/data-loss-prevention/data-loss-prevention)</span><span class="sxs-lookup"><span data-stu-id="967d6-110">For more information, see [DLP in the Exchange admin center](/exchange/security-and-compliance/data-loss-prevention/data-loss-prevention).</span></span>
    
<span data-ttu-id="967d6-111">Les polices DLP créées dans ces centres d’administration fonctionnent côte à côte : cette rubrique explique comment.</span><span class="sxs-lookup"><span data-stu-id="967d6-111">DLP polices created in these admin centers work side by side - this topic explains how.</span></span>
  
![Pages DLP dans le Centre de sécurité et conformité et Exchange’administration centrale](../media/d3eaa7e7-3b16-457b-bd9c-26707f7b584f.png)
  
## <a name="how-dlp-in-the-security--compliance-center-works-with-dlp-and-mail-flow-rules-in-the-exchange-admin-center"></a><span data-ttu-id="967d6-113">Fonctionnement de la protection contre la protection contre la protection contre la & dans le Centre de sécurité et conformité avec les règles de flux de messagerie et DLP dans Exchange’administration centrale</span><span class="sxs-lookup"><span data-stu-id="967d6-113">How DLP in the Security & Compliance Center works with DLP and mail flow rules in the Exchange admin center</span></span>

<span data-ttu-id="967d6-114">Après avoir créé une stratégie DLP dans le Centre de sécurité & conformité, la stratégie est déployée sur tous les emplacements inclus dans la stratégie.</span><span class="sxs-lookup"><span data-stu-id="967d6-114">After you create a DLP policy in the Security & Compliance Center, the policy is deployed to all of the locations included in the policy.</span></span> <span data-ttu-id="967d6-115">Si la stratégie inclut Exchange Online, la stratégie y est synchronisée et appliquée exactement de la même manière qu’une stratégie DLP créée dans le Centre d’administration Exchange.</span><span class="sxs-lookup"><span data-stu-id="967d6-115">If the policy includes Exchange Online, the policy's synced there and enforced in exactly the same way as a DLP policy created in the Exchange admin center.</span></span> 
  
<span data-ttu-id="967d6-116">Si vous avez créé des stratégies DLP dans le Centre d’administration Exchange, ces stratégies continueront à fonctionner côte à côte avec les stratégies de courrier électronique que vous créez dans le Centre de sécurité et conformité &.</span><span class="sxs-lookup"><span data-stu-id="967d6-116">If you've created DLP policies in the Exchange admin center, those policies will continue to work side by side with any policies for email that you create in the Security & Compliance Center.</span></span> <span data-ttu-id="967d6-117">Toutefois, notez que les règles créées dans Exchange centre d’administration sont prioritaire.</span><span class="sxs-lookup"><span data-stu-id="967d6-117">But note that rules created in the Exchange admin center take precedence.</span></span> <span data-ttu-id="967d6-118">Toutes Exchange règles de flux de messagerie sont traitées en premier, puis les règles DLP du Centre de sécurité & conformité sont traitées.</span><span class="sxs-lookup"><span data-stu-id="967d6-118">All Exchange mail flow rules are processed first, and then the DLP rules from the Security & Compliance Center are processed.</span></span>
  
<span data-ttu-id="967d6-119">Cela signifie que :</span><span class="sxs-lookup"><span data-stu-id="967d6-119">This means that:</span></span>
  
- <span data-ttu-id="967d6-120">Les messages bloqués par Exchange règles de flux de messagerie ne sont pas analysés par les règles DLP créées dans le Centre de sécurité & conformité.</span><span class="sxs-lookup"><span data-stu-id="967d6-120">Messages that are blocked by Exchange mail flow rules won't get scanned by DLP rules created in the Security & Compliance Center.</span></span>

- <span data-ttu-id="967d6-121">Les messages mis en quarantaine par Exchange règles de flux de messagerie ou tout autre filtre exécuté avant la DLP ne seront pas analysés par DLP.</span><span class="sxs-lookup"><span data-stu-id="967d6-121">Messages that are quarantined by Exchange mail flow rules or any other filters run before DLP will not be scanned by DLP.</span></span>
    
- <span data-ttu-id="967d6-122">Si une règle de flux de messagerie Exchange modifie un message de manière à ce qu’il corresponde à une stratégie DLP dans le Centre de sécurité & conformité (par exemple, l’ajout d’utilisateurs externes), les règles DLP le détectent et appliquent la stratégie selon les besoins.</span><span class="sxs-lookup"><span data-stu-id="967d6-122">If an Exchange mail flow rule modifies a message in a way that causes it to match a DLP policy in the Security & Compliance Center - such as adding external users - then the DLP rules will detect this and enforce the policy as needed.</span></span>
    
<span data-ttu-id="967d6-123">Notez également que Exchange règles de flux de messagerie qui utilisent l’action « Arrêter le traitement » n’affectent pas le traitement des règles DLP dans le Centre de sécurité & conformité . Elles seront toujours traitées.</span><span class="sxs-lookup"><span data-stu-id="967d6-123">Also note that Exchange mail flow rules that use the "stop processing" action don't affect the processing of DLP rules in the Security & Compliance Center - they'll still be processed.</span></span>
  
## <a name="policy-tips-in-the-security--compliance-center-vs-the-exchange-admin-center"></a><span data-ttu-id="967d6-124">Conseils de stratégie dans le Centre de sécurité & conformité et le Centre d’administration Exchange de sécurité</span><span class="sxs-lookup"><span data-stu-id="967d6-124">Policy tips in the Security & Compliance Center vs. the Exchange admin center</span></span>

<span data-ttu-id="967d6-125">Les conseils de stratégie peuvent fonctionner avec les stratégies DLP et les règles de flux de messagerie créées dans le Centre d’administration Exchange, ou avec les stratégies DLP créées dans le Centre de sécurité et conformité &, mais pas les deux.</span><span class="sxs-lookup"><span data-stu-id="967d6-125">Policy tips can work either with DLP policies and mail flow rules created in the Exchange admin center, or with DLP policies created in the Security & Compliance Center, but not both.</span></span> <span data-ttu-id="967d6-126">En effet, ces stratégies sont stockées à différents emplacements, mais les conseils de stratégie ne peuvent dessiner qu’à partir d’un seul emplacement.</span><span class="sxs-lookup"><span data-stu-id="967d6-126">This is because these policies are stored in different locations, but policy tips can draw only from a single location.</span></span>
  
<span data-ttu-id="967d6-127">Si vous avez configuré des conseils de stratégie dans le Centre d’administration Exchange, les conseils de stratégie que vous configurez dans le Centre de sécurité & conformité n’apparaîtront pas pour les utilisateurs dans Outlook sur le web et Outlook 2013 et les ultérieures tant que vous n’avez pas éteint les conseils du Centre d’administration Exchange.</span><span class="sxs-lookup"><span data-stu-id="967d6-127">If you've configured policy tips in the Exchange admin center, any policy tips that you configure in the Security & Compliance Center won't appear to users in Outlook on the web and Outlook 2013 and later until you turn off the tips in the Exchange admin center.</span></span> <span data-ttu-id="967d6-128">Cela garantit que vos règles de flux Exchange de messagerie continueront de fonctionner jusqu’à ce que vous choisissiez de basculer vers le Centre de sécurité & conformité.</span><span class="sxs-lookup"><span data-stu-id="967d6-128">This ensures that your current Exchange mail flow rules will continue to work until you choose to switch over to the Security & Compliance Center.</span></span>
  
<span data-ttu-id="967d6-129">Notez que bien que les conseils de stratégie ne peuvent dessiner qu’à partir d’un seul emplacement, les notifications par courrier électronique sont toujours envoyées, même si vous utilisez des stratégies DLP dans le Centre de sécurité & conformité et le Centre d’administration Exchange.</span><span class="sxs-lookup"><span data-stu-id="967d6-129">Note that while policy tips can draw only from a single location, email notifications are always sent, even if you're using DLP policies in both the Security & Compliance Center and the Exchange admin center.</span></span>
