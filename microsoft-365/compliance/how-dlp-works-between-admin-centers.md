---
title: Fonctionnement de DLP avec le Centre de sécurité & conformité & Exchange'administration
f1.keywords:
- NOCSH
ms.author: chrfox
author: chrfox
manager: laurawi
ms.date: 04/19/2019
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
description: Découvrez comment DLP dans le Centre de sécurité et conformité & fonctionne avec DLP et les règles de flux de messagerie (règles de transport) dans le Centre d'administration Exchange de sécurité.
ms.custom: seo-marvel-apr2020
ms.openlocfilehash: c5249279e1dd04447235aae813128cf458adde03
ms.sourcegitcommit: 05f40904f8278f53643efa76a907968b5c662d9a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/30/2021
ms.locfileid: "52114072"
---
# <a name="how-dlp-works-between-the-security--compliance-center-and-exchange-admin-center"></a><span data-ttu-id="f9e5b-103">Fonctionnement du DLP entre le Centre de sécurité et conformité et le Centre d’administration Exchange</span><span class="sxs-lookup"><span data-stu-id="f9e5b-103">How DLP works between the Security & Compliance Center and Exchange admin center</span></span>

<span data-ttu-id="f9e5b-104">Dans Office 365, vous pouvez créer une stratégie de protection contre la perte de données (DLP) dans deux centres d'administration différents :</span><span class="sxs-lookup"><span data-stu-id="f9e5b-104">In Office 365, you can create a data loss prevention (DLP) policy in two different admin centers:</span></span>
  
- <span data-ttu-id="f9e5b-105">Dans le Centre de sécurité **&** conformité, vous pouvez créer une stratégie DLP unique pour protéger le contenu dans SharePoint, OneDrive, Exchange et maintenant Microsoft Teams.</span><span class="sxs-lookup"><span data-stu-id="f9e5b-105">In the **Security & Compliance Center**, you can create a single DLP policy to help protect content in SharePoint, OneDrive, Exchange, and now Microsoft Teams.</span></span> <span data-ttu-id="f9e5b-106">Dans la mesure du possible, nous vous recommandons de créer une stratégie DLP ici.</span><span class="sxs-lookup"><span data-stu-id="f9e5b-106">When possible, we recommend that you create a DLP policy here.</span></span> <span data-ttu-id="f9e5b-107">Pour plus d'informations, [voir la référence sur la protection contre la perte de données.](data-loss-prevention-policies.md)</span><span class="sxs-lookup"><span data-stu-id="f9e5b-107">For more information, see [Data Loss Prevention reference](data-loss-prevention-policies.md).</span></span>
    
- <span data-ttu-id="f9e5b-108">Dans le **Exchange d'administration,** vous pouvez créer une stratégie DLP pour protéger le contenu uniquement dans Exchange.</span><span class="sxs-lookup"><span data-stu-id="f9e5b-108">In the **Exchange admin center**, you can create a DLP policy to help protect content only in Exchange.</span></span> <span data-ttu-id="f9e5b-109">Cette stratégie peut utiliser Exchange règles de flux de messagerie (également appelées règles de transport), de sorte qu'elle dispose d'autres options spécifiques à la gestion du courrier électronique.</span><span class="sxs-lookup"><span data-stu-id="f9e5b-109">This policy can use Exchange mail flow rules (also known as transport rules), so it has more options specific to handling email.</span></span> <span data-ttu-id="f9e5b-110">Pour plus d'informations, voir [DLP dans le centre Exchange'administration.](/exchange/security-and-compliance/data-loss-prevention/data-loss-prevention)</span><span class="sxs-lookup"><span data-stu-id="f9e5b-110">For more information, see [DLP in the Exchange admin center](/exchange/security-and-compliance/data-loss-prevention/data-loss-prevention).</span></span>
    
<span data-ttu-id="f9e5b-111">Les polices DLP créées dans ces centres d'administration fonctionnent côte à côte : cette rubrique explique comment.</span><span class="sxs-lookup"><span data-stu-id="f9e5b-111">DLP polices created in these admin centers work side by side - this topic explains how.</span></span>
  
![Pages DLP dans le Centre de sécurité et conformité et Exchange'administration centrale](../media/d3eaa7e7-3b16-457b-bd9c-26707f7b584f.png)
  
## <a name="how-dlp-in-the-security--compliance-center-works-with-dlp-and-mail-flow-rules-in-the-exchange-admin-center"></a><span data-ttu-id="f9e5b-113">Fonctionnement de la protection contre la protection contre la protection contre la & dans le Centre de sécurité et conformité avec les règles de flux de messagerie et DLP dans le Centre d'administration Exchange de sécurité</span><span class="sxs-lookup"><span data-stu-id="f9e5b-113">How DLP in the Security & Compliance Center works with DLP and mail flow rules in the Exchange admin center</span></span>

<span data-ttu-id="f9e5b-114">Après avoir créé une stratégie DLP dans le Centre de sécurité & conformité, la stratégie est déployée sur tous les emplacements inclus dans la stratégie.</span><span class="sxs-lookup"><span data-stu-id="f9e5b-114">After you create a DLP policy in the Security & Compliance Center, the policy is deployed to all of the locations included in the policy.</span></span> <span data-ttu-id="f9e5b-115">Si la stratégie inclut Exchange Online, la stratégie y est synchronisée et appliquée exactement de la même manière qu'une stratégie DLP créée dans le centre d'administration Exchange.</span><span class="sxs-lookup"><span data-stu-id="f9e5b-115">If the policy includes Exchange Online, the policy's synced there and enforced in exactly the same way as a DLP policy created in the Exchange admin center.</span></span> 
  
<span data-ttu-id="f9e5b-116">Si vous avez créé des stratégies DLP dans le Centre d'administration Exchange, ces stratégies continueront à fonctionner côte à côte avec les stratégies de courrier électronique que vous créez dans le Centre de sécurité et conformité &.</span><span class="sxs-lookup"><span data-stu-id="f9e5b-116">If you've created DLP policies in the Exchange admin center, those policies will continue to work side by side with any policies for email that you create in the Security & Compliance Center.</span></span> <span data-ttu-id="f9e5b-117">Toutefois, notez que les règles créées dans Exchange centre d'administration sont prioritaire.</span><span class="sxs-lookup"><span data-stu-id="f9e5b-117">But note that rules created in the Exchange admin center take precedence.</span></span> <span data-ttu-id="f9e5b-118">Toutes Exchange règles de flux de messagerie sont traitées en premier, puis les règles DLP du Centre de sécurité & conformité sont traitées.</span><span class="sxs-lookup"><span data-stu-id="f9e5b-118">All Exchange mail flow rules are processed first, and then the DLP rules from the Security & Compliance Center are processed.</span></span>
  
<span data-ttu-id="f9e5b-119">Cela signifie que :</span><span class="sxs-lookup"><span data-stu-id="f9e5b-119">This means that:</span></span>
  
- <span data-ttu-id="f9e5b-120">Les messages bloqués par Exchange règles de flux de messagerie ne sont pas analysés par les règles DLP créées dans le Centre de sécurité & conformité.</span><span class="sxs-lookup"><span data-stu-id="f9e5b-120">Messages that are blocked by Exchange mail flow rules won't get scanned by DLP rules created in the Security & Compliance Center.</span></span>
    
- <span data-ttu-id="f9e5b-121">Si une règle de flux de messagerie Exchange modifie un message de manière à ce qu'il corresponde à une stratégie DLP dans le Centre de sécurité & conformité (par exemple, l'ajout d'utilisateurs externes), les règles DLP le détectent et appliquent la stratégie selon les besoins.</span><span class="sxs-lookup"><span data-stu-id="f9e5b-121">If an Exchange mail flow rule modifies a message in a way that causes it to match a DLP policy in the Security & Compliance Center - such as adding external users - then the DLP rules will detect this and enforce the policy as needed.</span></span>
    
<span data-ttu-id="f9e5b-122">Notez également que Exchange règles de flux de messagerie qui utilisent l'action « Arrêter le traitement » n'affectent pas le traitement des règles DLP dans le Centre de sécurité & conformité . Elles seront toujours traitées.</span><span class="sxs-lookup"><span data-stu-id="f9e5b-122">Also note that Exchange mail flow rules that use the "stop processing" action don't affect the processing of DLP rules in the Security & Compliance Center - they'll still be processed.</span></span>
  
## <a name="policy-tips-in-the-security--compliance-center-vs-the-exchange-admin-center"></a><span data-ttu-id="f9e5b-123">Conseils de stratégie dans le Centre de sécurité & conformité et le Centre d'administration Exchange de sécurité</span><span class="sxs-lookup"><span data-stu-id="f9e5b-123">Policy tips in the Security & Compliance Center vs. the Exchange admin center</span></span>

<span data-ttu-id="f9e5b-124">Les conseils de stratégie peuvent fonctionner avec les stratégies DLP et les règles de flux de messagerie créées dans le Centre d'administration Exchange, ou avec les stratégies DLP créées dans le Centre de sécurité et conformité &, mais pas les deux.</span><span class="sxs-lookup"><span data-stu-id="f9e5b-124">Policy tips can work either with DLP policies and mail flow rules created in the Exchange admin center, or with DLP policies created in the Security & Compliance Center, but not both.</span></span> <span data-ttu-id="f9e5b-125">En effet, ces stratégies sont stockées à différents emplacements, mais les conseils de stratégie ne peuvent dessiner qu'à partir d'un seul emplacement.</span><span class="sxs-lookup"><span data-stu-id="f9e5b-125">This is because these policies are stored in different locations, but policy tips can draw only from a single location.</span></span>
  
<span data-ttu-id="f9e5b-126">Si vous avez configuré des conseils de stratégie dans le Centre d'administration Exchange, les conseils de stratégie que vous configurez dans le Centre de sécurité & conformité n'apparaissent pas pour les utilisateurs dans Outlook sur le web et Outlook 2013 et ultérieurs tant que vous n'avez pas éteint les conseils dans le Centre d'administration Exchange.</span><span class="sxs-lookup"><span data-stu-id="f9e5b-126">If you've configured policy tips in the Exchange admin center, any policy tips that you configure in the Security & Compliance Center won't appear to users in Outlook on the web and Outlook 2013 and later until you turn off the tips in the Exchange admin center.</span></span> <span data-ttu-id="f9e5b-127">Cela garantit que vos règles de flux Exchange de messagerie continueront de fonctionner jusqu'à ce que vous choisissiez de basculer vers le Centre de sécurité & conformité.</span><span class="sxs-lookup"><span data-stu-id="f9e5b-127">This ensures that your current Exchange mail flow rules will continue to work until you choose to switch over to the Security & Compliance Center.</span></span>
  
<span data-ttu-id="f9e5b-128">Notez que bien que les conseils de stratégie ne peuvent dessiner qu'à partir d'un seul emplacement, les notifications par courrier électronique sont toujours envoyées, même si vous utilisez des stratégies DLP dans le Centre de sécurité & conformité et le Centre d'administration Exchange.</span><span class="sxs-lookup"><span data-stu-id="f9e5b-128">Note that while policy tips can draw only from a single location, email notifications are always sent, even if you're using DLP policies in both the Security & Compliance Center and the Exchange admin center.</span></span>
