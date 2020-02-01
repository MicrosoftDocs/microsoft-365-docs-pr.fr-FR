---
title: Seuils de probabilité de courrier indésirable
f1.keywords:
- NOCSH
ms.author: tracyp
author: MSFTTracyP
manager: dansimp
ms.date: 10/02/2017
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: 34681000-0022-4b92-b38a-e32b3ed96bf6
ms.collection:
- M365-security-compliance
description: Un message électronique qui passe à travers le filtrage anti-spam reçoit un score de mise en quarantaine. Ce score est mappé à une valeur de seuil de probabilité de courrier indésirable (SCL) individuelle et marqué dans un en-tête X. Le service entreprend des actions sur les messages en fonction de l'interprétation de la probabilité de courrier indésirable de la valeur SCL. Le tableau suivant indique comment sont interprétées les différentes valeurs SCL par les filtres ainsi que l'action par défaut entreprise sur les messages entrants pour chaque valeur.
ms.openlocfilehash: c40317833ea61424dab60ac858c2071f7891c4f8
ms.sourcegitcommit: 1c91b7b24537d0e54d484c3379043db53c1aea65
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/29/2020
ms.locfileid: "41598311"
---
# <a name="spam-confidence-levels"></a><span data-ttu-id="360ba-106">Seuils de probabilité de courrier indésirable</span><span class="sxs-lookup"><span data-stu-id="360ba-106">Spam confidence levels</span></span>

<span data-ttu-id="360ba-p102">Un message électronique qui passe à travers le filtrage anti-spam reçoit un score de mise en quarantaine. Ce score est mappé à une valeur de seuil de probabilité de courrier indésirable (SCL) individuelle et marqué dans un en-tête X. Le service entreprend des actions sur les messages en fonction de l'interprétation de la probabilité de courrier indésirable de la valeur SCL. Le tableau suivant indique comment sont interprétées les différentes valeurs SCL par les filtres ainsi que l'action par défaut entreprise sur les messages entrants pour chaque valeur.</span><span class="sxs-lookup"><span data-stu-id="360ba-p102">When an email message goes through spam filtering it is assigned a spam score. That score is mapped to an individual Spam Confidence Level (SCL) rating and stamped in an X-header. The service takes actions upon the messages depending upon the spam confidence interpretation of the SCL rating. The following table shows how the different SCL ratings are interpreted by the filters and the default action that is taken on inbound messages for each rating.</span></span>
  
|<span data-ttu-id="360ba-111">**Valeur SCL**</span><span class="sxs-lookup"><span data-stu-id="360ba-111">**SCL Rating**</span></span>|<span data-ttu-id="360ba-112">**Interprétation de la probabilité de courrier indésirable**</span><span class="sxs-lookup"><span data-stu-id="360ba-112">**Spam Confidence Interpretation**</span></span>|<span data-ttu-id="360ba-113">**Action par défaut**</span><span class="sxs-lookup"><span data-stu-id="360ba-113">**Default Action**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="360ba-114">-1</span><span class="sxs-lookup"><span data-stu-id="360ba-114">-1</span></span>|<span data-ttu-id="360ba-115">Non-courrier indésirable provenant d’un expéditeur approuvé, d’un destinataire approuvé ou d’une adresse IP de la zone de sécurité (partenaire approuvé).</span><span class="sxs-lookup"><span data-stu-id="360ba-115">Non-spam coming from a safe sender, safe recipient, or safe listed IP address (trusted partner).</span></span>|<span data-ttu-id="360ba-116">Le message est remis dans la boîte aux lettres des destinataires.</span><span class="sxs-lookup"><span data-stu-id="360ba-116">Deliver the message to the recipients' inbox.</span></span>|
|<span data-ttu-id="360ba-117">0, 1</span><span class="sxs-lookup"><span data-stu-id="360ba-117">0, 1</span></span>|<span data-ttu-id="360ba-118">Non-courrier indésirable, car le message a été analysé et déterminé comme étant propre.</span><span class="sxs-lookup"><span data-stu-id="360ba-118">Non-spam because the message was scanned and determined to be clean.</span></span>|<span data-ttu-id="360ba-119">Le message est remis dans la boîte aux lettres des destinataires.</span><span class="sxs-lookup"><span data-stu-id="360ba-119">Deliver the message to the recipients' inbox.</span></span>|
|<span data-ttu-id="360ba-120">5, 6</span><span class="sxs-lookup"><span data-stu-id="360ba-120">5, 6</span></span>|<span data-ttu-id="360ba-121">Courrier indésirable</span><span class="sxs-lookup"><span data-stu-id="360ba-121">Spam</span></span>|<span data-ttu-id="360ba-122">Le message est envoyé vers le dossier Courrier indésirable des destinataires.</span><span class="sxs-lookup"><span data-stu-id="360ba-122">Deliver the message to the recipients' Junk Email folder.</span></span>|
|<span data-ttu-id="360ba-123">7, 8, 9</span><span class="sxs-lookup"><span data-stu-id="360ba-123">7, 8, 9</span></span>|<span data-ttu-id="360ba-124">Courrier indésirable à probabilité élevée</span><span class="sxs-lookup"><span data-stu-id="360ba-124">High confidence spam</span></span>|<span data-ttu-id="360ba-125">Le message est envoyé vers le dossier Courrier indésirable des destinataires.</span><span class="sxs-lookup"><span data-stu-id="360ba-125">Deliver the message to the recipients' Junk Email folder.</span></span>|
   
> [!TIP]
> <span data-ttu-id="360ba-126">Les valeurs SCL de 2, 3, 4, 7 et 8 ne sont pas définies par le service.</span><span class="sxs-lookup"><span data-stu-id="360ba-126">SCL ratings of 2, 3, 4, 7, and 8 are not set by the service.</span></span> <span data-ttu-id="360ba-127">Une valeur SCL de 5 ou 6 indique une suspicion de courrier indésirable, ce qui est moins probable qu'une valeur SCL de 9, qui indique que le message est certainement du courrier indésirable.</span><span class="sxs-lookup"><span data-stu-id="360ba-127">An SCL rating of 5 or 6 is considered suspected spam, which is less certain to be spam than an SCL rating of 9, which is considered certain spam.</span></span> <span data-ttu-id="360ba-128">Vous pouvez configurer différentes actions pour le courrier indésirable et le courrier indésirable à niveau de confiance élevé à l'aide de vos stratégies de filtrage de contenu dans le Centre d'administration Exchange.</span><span class="sxs-lookup"><span data-stu-id="360ba-128">Different actions for spam and high confidence spam can be configured via your content filter policies in the Exchange admin center.</span></span> <span data-ttu-id="360ba-129">Pour plus d'informations, consultez la rubrique [Configuration de vos stratégies de filtrage du courrier indésirable](configure-your-spam-filter-policies.md).</span><span class="sxs-lookup"><span data-stu-id="360ba-129">For more information, see [Configure your spam filter policies](configure-your-spam-filter-policies.md).</span></span> <span data-ttu-id="360ba-130">Vous pouvez également définir la valeur de contrôle d’accès SCL pour les messages qui correspondent à des conditions spécifiques à l’aide de règles de flux de messagerie (également appelées règles de transport), comme décrit dans [utiliser des règles de flux de messagerie pour définir le seuil de probabilité de courrier indésirable (SCL) dans les messages](use-mail-flow-rules-to-set-the-spam-confidence-level-scl-in-messages.md).</span><span class="sxs-lookup"><span data-stu-id="360ba-130">You can also set the SCL rating for messages that match specific conditions by using mail flow rules (also known as transport rules), as described in [Use mail flow rules to set the spam confidence level (SCL) in messages](use-mail-flow-rules-to-set-the-spam-confidence-level-scl-in-messages.md).</span></span> <span data-ttu-id="360ba-131">Si vous utilisez une règle de flux de messagerie pour définir la valeur SCL de 7, 8 ou 9, le message sera traité comme du courrier indésirable à niveau de confiance élevé.</span><span class="sxs-lookup"><span data-stu-id="360ba-131">If you use a mail flow rule to set SCL of 7, 8, or 9 the message will be treated as high confidence spam.</span></span> 
  
||
|:-----|
|<span data-ttu-id="360ba-p104">![Icône rapide pour LinkedIn Learning](../media/eac8a413-9498-4220-8544-1e37d1aaea13.png) **Vous débutez avec Office 365 ?**         Découvrez les cours vidéo gratuits pour **Office 365 admins and IT pros** proposés par LinkedIn Learning.</span><span class="sxs-lookup"><span data-stu-id="360ba-p104">![The short icon for LinkedIn Learning](../media/eac8a413-9498-4220-8544-1e37d1aaea13.png) **New to Office 365?**         Discover free video courses for **Office 365 admins and IT pros**, brought to you by LinkedIn Learning.</span></span>|
   

