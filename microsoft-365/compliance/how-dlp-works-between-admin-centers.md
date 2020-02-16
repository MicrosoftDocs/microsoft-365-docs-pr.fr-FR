---
title: Fonctionnement du DLP entre le Centre de sécurité et conformité et le Centre d’administration Exchange
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
description: Découvrez comment DLP dans le centre de sécurité & conformité fonctionne avec DLP et les règles de flux de messagerie (règles de transport) dans le centre d’administration Exchange.
ms.openlocfilehash: 82b3d371303b647488c08416c5392d006c81e479
ms.sourcegitcommit: 3dd9944a6070a7f35c4bc2b57df397f844c3fe79
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/15/2020
ms.locfileid: "42073064"
---
# <a name="how-dlp-works-between-the-security--compliance-center-and-exchange-admin-center"></a><span data-ttu-id="eea71-103">Fonctionnement du DLP entre le Centre de sécurité et conformité et le Centre d’administration Exchange</span><span class="sxs-lookup"><span data-stu-id="eea71-103">How DLP works between the Security & Compliance Center and Exchange admin center</span></span>

<span data-ttu-id="eea71-104">Dans Office 365, vous pouvez créer une stratégie de protection contre la perte de données (DLP) dans deux centres d’administration différents :</span><span class="sxs-lookup"><span data-stu-id="eea71-104">In Office 365, you can create a data loss prevention (DLP) policy in two different admin centers:</span></span>
  
- <span data-ttu-id="eea71-105">Dans le **Centre de sécurité & conformité**, vous pouvez créer une stratégie DLP unique pour protéger le contenu dans SharePoint, OneDrive, Exchange et Microsoft Teams.</span><span class="sxs-lookup"><span data-stu-id="eea71-105">In the **Security & Compliance Center**, you can create a single DLP policy to help protect content in SharePoint, OneDrive, Exchange, and now Microsoft Teams.</span></span> <span data-ttu-id="eea71-106">Dans la mesure du possible, nous vous recommandons de créer une stratégie DLP ici.</span><span class="sxs-lookup"><span data-stu-id="eea71-106">When possible, we recommend that you create a DLP policy here.</span></span> <span data-ttu-id="eea71-107">Pour plus d’informations, reportez-vous [à la rubrique DLP dans le centre de sécurité & conformité](data-loss-prevention-policies.md).</span><span class="sxs-lookup"><span data-stu-id="eea71-107">For more information, see [DLP in the Security & Compliance Center](data-loss-prevention-policies.md).</span></span>
    
- <span data-ttu-id="eea71-108">Dans le **Centre d’administration Exchange**, vous pouvez créer une stratégie DLP pour protéger le contenu uniquement dans Exchange.</span><span class="sxs-lookup"><span data-stu-id="eea71-108">In the **Exchange admin center**, you can create a DLP policy to help protect content only in Exchange.</span></span> <span data-ttu-id="eea71-109">Cette stratégie peut utiliser des règles de flux de messagerie Exchange (également appelées règles de transport), de sorte qu’elle dispose de plus d’options spécifiques pour gérer le courrier électronique.</span><span class="sxs-lookup"><span data-stu-id="eea71-109">This policy can use Exchange mail flow rules (also known as transport rules), so it has more options specific to handling email.</span></span> <span data-ttu-id="eea71-110">Pour plus d’informations, consultez [la rubrique DLP dans le centre d’administration Exchange](https://go.microsoft.com/fwlink/?linkid=852311).</span><span class="sxs-lookup"><span data-stu-id="eea71-110">For more information, see [DLP in the Exchange admin center](https://go.microsoft.com/fwlink/?linkid=852311).</span></span>
    
<span data-ttu-id="eea71-111">Les stratégies DLP créées dans ces centres d’administration fonctionnent côte à côte-cette rubrique explique comment procéder.</span><span class="sxs-lookup"><span data-stu-id="eea71-111">DLP polices created in these admin centers work side by side - this topic explains how.</span></span>
  
![Pages DLP dans le centre de sécurité et de conformité et centre d’administration Exchange](../media/d3eaa7e7-3b16-457b-bd9c-26707f7b584f.png)
  
## <a name="how-dlp-in-the-security--compliance-center-works-with-dlp-and-mail-flow-rules-in-the-exchange-admin-center"></a><span data-ttu-id="eea71-113">Fonctionnement de DLP dans le centre de sécurité & conformité avec DLP et les règles de flux de messagerie dans le centre d’administration Exchange</span><span class="sxs-lookup"><span data-stu-id="eea71-113">How DLP in the Security & Compliance Center works with DLP and mail flow rules in the Exchange admin center</span></span>

<span data-ttu-id="eea71-114">Une fois que vous avez créé une stratégie DLP dans le centre de sécurité & conformité, la stratégie est déployée sur tous les emplacements inclus dans la stratégie.</span><span class="sxs-lookup"><span data-stu-id="eea71-114">After you create a DLP policy in the Security & Compliance Center, the policy is deployed to all of the locations included in the policy.</span></span> <span data-ttu-id="eea71-115">Si la stratégie inclut Exchange Online, la stratégie est synchronisée et appliquée exactement de la même manière qu’une stratégie DLP créée dans le centre d’administration Exchange.</span><span class="sxs-lookup"><span data-stu-id="eea71-115">If the policy includes Exchange Online, the policy's synced there and enforced in exactly the same way as a DLP policy created in the Exchange admin center.</span></span> 
  
<span data-ttu-id="eea71-116">Si vous avez créé des stratégies DLP dans le centre d’administration Exchange, ces stratégies continueront à fonctionner côte à côte avec des stratégies pour les messages électroniques que vous créez dans le centre de sécurité & Compliance Center.</span><span class="sxs-lookup"><span data-stu-id="eea71-116">If you've created DLP policies in the Exchange admin center, those policies will continue to work side by side with any policies for email that you create in the Security & Compliance Center.</span></span> <span data-ttu-id="eea71-117">Toutefois, Notez que les règles créées dans le centre d’administration Exchange ont priorité.</span><span class="sxs-lookup"><span data-stu-id="eea71-117">But note that rules created in the Exchange admin center take precedence.</span></span> <span data-ttu-id="eea71-118">Toutes les règles de flux de messagerie Exchange sont traitées en premier, puis les règles DLP du centre de sécurité & conformité sont traitées.</span><span class="sxs-lookup"><span data-stu-id="eea71-118">All Exchange mail flow rules are processed first, and then the DLP rules from the Security & Compliance Center are processed.</span></span>
  
<span data-ttu-id="eea71-119">Cela signifie que :</span><span class="sxs-lookup"><span data-stu-id="eea71-119">This means that:</span></span>
  
- <span data-ttu-id="eea71-120">Les messages bloqués par les règles de flux de messagerie Exchange ne sont pas analysés par les règles DLP créées dans le centre de sécurité & conformité.</span><span class="sxs-lookup"><span data-stu-id="eea71-120">Messages that are blocked by Exchange mail flow rules won't get scanned by DLP rules created in the Security & Compliance Center.</span></span>
    
- <span data-ttu-id="eea71-121">Si une règle de flux de messagerie Exchange modifie un message de manière à ce qu’il corresponde à une stratégie DLP dans le centre de conformité & de sécurité, comme l’ajout d’utilisateurs externes, les règles DLP les détectent et appliquent la stratégie si nécessaire.</span><span class="sxs-lookup"><span data-stu-id="eea71-121">If an Exchange mail flow rule modifies a message in a way that causes it to match a DLP policy in the Security & Compliance Center - such as adding external users - then the DLP rules will detect this and enforce the policy as needed.</span></span>
    
<span data-ttu-id="eea71-122">Notez également que les règles de flux de messagerie Exchange qui utilisent l’action « arrêter le traitement » n’ont pas d’impact sur le traitement des règles DLP dans le centre de sécurité & conformité.</span><span class="sxs-lookup"><span data-stu-id="eea71-122">Also note that Exchange mail flow rules that use the "stop processing" action don't affect the processing of DLP rules in the Security & Compliance Center - they'll still be processed.</span></span>
  
## <a name="policy-tips-in-the-security--compliance-center-vs-the-exchange-admin-center"></a><span data-ttu-id="eea71-123">Conseils de stratégie dans le centre de sécurité & conformité et au centre d’administration Exchange</span><span class="sxs-lookup"><span data-stu-id="eea71-123">Policy tips in the Security & Compliance Center vs. the Exchange admin center</span></span>

<span data-ttu-id="eea71-124">Les conseils de stratégie peuvent fonctionner soit avec les stratégies DLP et les règles de flux de messagerie créées dans le centre d’administration Exchange, soit avec les stratégies DLP créées dans le centre de sécurité & conformité, mais pas dans les deux.</span><span class="sxs-lookup"><span data-stu-id="eea71-124">Policy tips can work either with DLP policies and mail flow rules created in the Exchange admin center, or with DLP policies created in the Security & Compliance Center, but not both.</span></span> <span data-ttu-id="eea71-125">Cela est dû au fait que ces stratégies sont stockées à des emplacements différents, mais que les conseils de stratégie ne peuvent tirer qu’à partir d’un seul emplacement.</span><span class="sxs-lookup"><span data-stu-id="eea71-125">This is because these policies are stored in different locations, but policy tips can draw only from a single location.</span></span>
  
<span data-ttu-id="eea71-126">Si vous avez configuré des conseils de stratégie dans le centre d’administration Exchange, tous les conseils de stratégie que vous configurez dans le centre de sécurité & les utilisateurs ne s’afficheront pas dans Outlook sur le Web et Outlook 2013 et les versions ultérieures jusqu’à ce que vous désactiviez les conseils dans le centre d’administration Exchange.</span><span class="sxs-lookup"><span data-stu-id="eea71-126">If you've configured policy tips in the Exchange admin center, any policy tips that you configure in the Security & Compliance Center won't appear to users in Outlook on the web and Outlook 2013 and later until you turn off the tips in the Exchange admin center.</span></span> <span data-ttu-id="eea71-127">Cela permet de s’assurer que vos règles de flux de messagerie Exchange actuelles continueront de fonctionner jusqu’à ce que vous choisissiez de basculer vers le centre de conformité & sécurité.</span><span class="sxs-lookup"><span data-stu-id="eea71-127">This ensures that your current Exchange mail flow rules will continue to work until you choose to switch over to the Security & Compliance Center.</span></span>
  
<span data-ttu-id="eea71-128">Notez que si les conseils de stratégie ne peuvent être tracés qu’à partir d’un seul emplacement, les notifications par courrier électronique sont toujours envoyées, même si vous utilisez les stratégies DLP dans le centre de sécurité & conformité et dans le centre d’administration Exchange.</span><span class="sxs-lookup"><span data-stu-id="eea71-128">Note that while policy tips can draw only from a single location, email notifications are always sent, even if you're using DLP policies in both the Security & Compliance Center and the Exchange admin center.</span></span>
  

