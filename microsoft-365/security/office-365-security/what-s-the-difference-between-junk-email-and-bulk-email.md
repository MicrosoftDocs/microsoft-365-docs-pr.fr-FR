---
title: Quelle est la différence entre courrier indésirable et message électronique en masse ?
f1.keywords:
- NOCSH
ms.author: tracyp
author: MSFTTracyP
manager: dansimp
ms.date: 1/7/2015
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: 8079f193-1b40-4081-9e5d-d0e50dfbcc59
ms.collection:
- M365-security-compliance
description: Les clients askwhat parfois la différence entre le courrier indésirable et les messages électroniques en masse ? L’objectif de cette rubrique est d’expliquer la différence et de fournir des informations sur les différentes options disponibles dans Exchange Online et Exchange Online Protection (EOP).
ms.openlocfilehash: 55924ac5e83ca109fd66d1723cdb7c5f43f20df6
ms.sourcegitcommit: fce0d5cad32ea60a08ff001b228223284710e2ed
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/21/2020
ms.locfileid: "42895034"
---
# <a name="whats-the-difference-between-junk-email-and-bulk-email"></a><span data-ttu-id="b5b3f-103">Quelle est la différence entre courrier indésirable et message électronique en masse ?</span><span class="sxs-lookup"><span data-stu-id="b5b3f-103">What's the difference between junk email and bulk email?</span></span>

<span data-ttu-id="b5b3f-p101">Les clients s'interrogent parfois sur la différence entre le courrier indésirable et les messages électroniques en masse. Cette rubrique a pour but d'expliquer cette différence et de fournir des informations sur les différentes options disponibles dans Exchange Online et Exchange Online Protection (EOP).</span><span class="sxs-lookup"><span data-stu-id="b5b3f-p101">Customers sometimes ask "what's the difference between junk email and bulk email messages?" The purpose of this topic is to explain the difference and to provide information about the different options that are available for both in Exchange Online and Exchange Online Protection (EOP).</span></span>
  
 <span data-ttu-id="b5b3f-106">**Qu'est-ce que le courrier indésirable ?**</span><span class="sxs-lookup"><span data-stu-id="b5b3f-106">**What's junk email?**</span></span>
  
<span data-ttu-id="b5b3f-p102">Il s'agit de messages électroniques non sollicités (et généralement non désirés) filtrés par le service, aussi appelés « spam ». Par défaut, le service rejettera le message indésirable sur la base de la réputation de l'adresse IP d'expédition. Toutefois, s'il n'est pas détecté lors de l'inspection de l'adresse IP mais qu'il est classé comme indésirable par les filtres de contenu, le message est envoyé vers le dossier Courrier indésirable des destinataires.</span><span class="sxs-lookup"><span data-stu-id="b5b3f-p102">Junk email messages are "spam" messages, which are unsolicited (and typically unwanted) email messages that are filtered by the service. By default, the service rejects the spam message based on the reputation of the sending IP address. However, if it passes IP inspection but is classified as spam by the content filters, the message is sent to the Junk Email folder of the intended recipients.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="b5b3f-110">L’action effectuée sur les messages filtrés sur le contenu est configurable via les stratégies de filtrage de contenu dans le centre d’administration Exchange, comme décrit dans [configurer les stratégies anti-courrier indésirable dans Office 365](configure-your-spam-filter-policies.md).</span><span class="sxs-lookup"><span data-stu-id="b5b3f-110">The action performed on content-filtered messages is configurable via content filter policies in the Exchange admin center (EAC), as described in [Configure anti-spam policies in Office 365](configure-your-spam-filter-policies.md).</span></span> <span data-ttu-id="b5b3f-111">En outre, si vous estimez que le courrier indésirable n'est pas classé correctement, vous pouvez signaler les messages que vous considérez indésirables ou non à Microsoft de plusieurs façons, comme décrit dans la rubrique [Soumission des messages indésirables, légitimes ou des tentatives de hameçonnage à Microsoft pour analyse](submit-spam-non-spam-and-phishing-scam-messages-to-microsoft-for-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="b5b3f-111">Also, if you disagree with the spam classification, you can report messages that you consider to be spam or non-spam to Microsoft in several ways, as described in [Submit spam, non-spam, and phishing scam messages to Microsoft for analysis](submit-spam-non-spam-and-phishing-scam-messages-to-microsoft-for-analysis.md).</span></span> 
  
 <span data-ttu-id="b5b3f-112">**Que sont les messages électroniques en masse ?**</span><span class="sxs-lookup"><span data-stu-id="b5b3f-112">**What's bulk email?**</span></span>
  
<span data-ttu-id="b5b3f-p104">Les messages électroniques en masse, aussi appelés « messages gris » (graymail), sont plus difficiles à classer. Tandis que le courrier indésirable constitue une menace constante, les messages électroniques en masse contiennent généralement une annonce ou un message publicitaire qui ne sera normalement pas envoyé à plusieurs reprises. Certains utilisateurs considèrent les messages électroniques en masse comme indésirables, mais d'autres les sollicitent et se sont d'ailleurs peut-être volontairement inscrits pour les recevoir. Par exemple, certains utilisateurs souhaiteront recevoir des messages publicitaires de la société Contoso ou des invitations à une conférence à venir sur la cybersécurité, tandis que d'autres considèreront ces messages comme indésirables.</span><span class="sxs-lookup"><span data-stu-id="b5b3f-p104">Bulk email, also referred to as gray mail, is a type of email message that's more difficult to classify. Whereas junk email is a constant threat, bulk email is typically comprised of an advertisement or marketing message that's not likely to get sent repeatedly. Bulk email is wanted by some users, and in fact they may have deliberately signed up to receive these messages, while other users may consider these types of messages to be spam. For example, some users want to receive advertising emails from the Contoso Corporation or invitations to an upcoming conference on cyber security, while other users consider such emails to be spam.</span></span>
  
## <a name="how-to-manage-bulk-email"></a><span data-ttu-id="b5b3f-117">Gestion des messages électroniques en masse</span><span class="sxs-lookup"><span data-stu-id="b5b3f-117">How to manage bulk email</span></span>

<span data-ttu-id="b5b3f-p105">La gestion des messages électroniques en masse n'est pas facile, car s'ils sont tous sont classés comme indésirables, les utilisateurs qui les sollicitent peuvent se plaindre et les soumettre comme des faux positif, identifiés à tort comme courrier indésirable. À l'inverse, si tous les messages électroniques en masse sont autorisés à passer, les utilisateurs qui ne les ont pas sollicités peuvent se plaindre et les soumettre comme des faux négatifs, arrivés à tort dans leur boîte de réception.</span><span class="sxs-lookup"><span data-stu-id="b5b3f-p105">How to manage bulk email isn't a clear cut decision, because if all bulk email is classified as spam, the users that want it may complain and submit it as a false positive (non-spam) message that was wrongly marked as spam. On the other hand, if all bulk email is let through, the users that don't want it may complain and submit it as a missed spam message (false negative) that wrongly arrived in their inbox.</span></span>
  
### <a name="enable-bulk-mail-sensitivity-control-in-the-content-filter-policy"></a><span data-ttu-id="b5b3f-120">Activer le contrôle de sensibilité des messages électroniques en masse dans la stratégie de filtrage de contenu</span><span class="sxs-lookup"><span data-stu-id="b5b3f-120">Enable bulk mail sensitivity control in the content filter policy</span></span>

<span data-ttu-id="b5b3f-121">En fonction de la stratégie de votre entreprise en matière de messages électroniques en nombre, les administrateurs peuvent sélectionner un seuil à attribuer aux messages électroniques en nombre.</span><span class="sxs-lookup"><span data-stu-id="b5b3f-121">Depending on your company's policy on bulk email messages, admins can select a threshold to assign the bulk email.</span></span> <span data-ttu-id="b5b3f-122">Le paramètre est configurable via stratégies de filtrage de contenu dans le centre d’administration Exchange.</span><span class="sxs-lookup"><span data-stu-id="b5b3f-122">The setting is configurable via content filter policies in the EAC.</span></span> <span data-ttu-id="b5b3f-123">Consultez [configurer les stratégies anti-courrier indésirable dans Office 365](configure-your-spam-filter-policies.md) pour les étapes.</span><span class="sxs-lookup"><span data-stu-id="b5b3f-123">Check out [Configure anti-spam policies in Office 365](configure-your-spam-filter-policies.md) for the steps.</span></span> <span data-ttu-id="b5b3f-124">Vous pouvez choisir un paramètre de seuil de 1-9, où 1 marque la plupart des messages électroniques en masse comme courrier indésirable, et 9 la plupart des messages électroniques en nombre à être remis.</span><span class="sxs-lookup"><span data-stu-id="b5b3f-124">You can choose a threshold setting from 1-9, where 1 marks most bulk email as spam, and 9 allows most bulk email to be delivered.</span></span> <span data-ttu-id="b5b3f-125">Le service effectue ensuite l'action configurée, comme par exemple l'envoi du message dans le dossier Courrier indésirable du destinataire.</span><span class="sxs-lookup"><span data-stu-id="b5b3f-125">The service then performs the configured action, such as sending the message to the recipient's Junk Email folder.</span></span> 
  

