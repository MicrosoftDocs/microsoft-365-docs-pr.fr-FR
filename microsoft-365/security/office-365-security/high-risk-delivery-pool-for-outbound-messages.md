---
title: Pool de remise à risque élevé pour les messages sortants
ms.author: tracyp
author: MSFTTracyP
manager: dansimp
ms.date: 8/24/2016
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: ac11edd9-2da3-462d-8ea3-bbf9dbc6f948
ms.collection:
- M365-security-compliance
description: Lorsque le système de courrier d’un client a été compromis par un programme malveillant ou une attaque de courrier indésirable malveillant, et qu’il envoie du courrier indésirable sortant via le service de filtrage hébergé, les adresses IP des serveurs du centre de données Office 365 sont peut-être référencées dans un bloc tiers. établit.
ms.openlocfilehash: 5b9241dead5b40e9f216ecd3023d6f8b86fb0205
ms.sourcegitcommit: 1162d676b036449ea4220de8a6642165190e3398
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/20/2019
ms.locfileid: "37079052"
---
# <a name="high-risk-delivery-pool-for-outbound-messages"></a><span data-ttu-id="61578-103">Pool de remise à risque élevé pour les messages sortants</span><span class="sxs-lookup"><span data-stu-id="61578-103">High-risk delivery pool for outbound messages</span></span>

<span data-ttu-id="61578-p101">Quand l'intégrité du système de messagerie d'un client a été compromise par un programme malveillant ou une attaque malveillante de courriers indésirables, et que ce système envoie du courrier indésirable via le service de filtrage hébergé, les adresses IP des serveurs du centre de données Office 365 peuvent alors être répertoriées sur des listes rouges tierces. Les serveurs de destination qui utilisent ces listes rouges à la place du service de filtrage hébergé rejettent tous les messages électroniques envoyés à partir des adresses IP de filtrage hébergées qui ont été ajoutées à ces listes. Pour éviter cela, tous les messages sortants qui dépassent le seuil de courrier indésirable sont envoyés via un pool de remise à risque élevé. Ce pool de messages électroniques sortants secondaire est utilisé uniquement pour envoyer des messages pouvant être de qualité médiocre, ce qui permet ainsi de protéger le reste du réseau contre l'envoi de messages plus susceptibles d'entraîner le blocage de l'adresse IP d'expédition.</span><span class="sxs-lookup"><span data-stu-id="61578-p101">When a customer's email system has been compromised by malware or a malicious spam attack, and it's sending outbound spam through the hosted filtering service, this can result in the IP addresses of the Office 365 data center servers being listed on third-party block lists. Destination servers that do not use the hosted filtering service, but do use these block lists, reject all email sent from any of the hosted filtering IP addresses that have been added to those lists. To prevent this, all outbound messages that exceed the spam threshold are sent through a high-risk delivery pool. This secondary outbound email pool is only used to send messages that may be of low quality. This helps to protect the rest of the network from sending messages that are more likely to result in the sending IP address being blocked.</span></span>
  
<span data-ttu-id="61578-p102">L'utilisation d'un pool de remise à risque élevé dédié permet de garantir que le pool sortant normal n'envoie que des messages réputés de bonne qualité. Ce pool d'adresses IP secondaire permet de réduire la probabilité que le pool d'adresses IP sortantes normal soit ajouté à une liste rouge. La possibilité qu'un pool de remise à risque élevé soit placé sur une liste rouge est toujours présente. Il s'agit du comportement par défaut.</span><span class="sxs-lookup"><span data-stu-id="61578-p102">The use of a dedicated high-risk delivery pool helps ensure that the normal outbound pool is only sending messages that are known to be of a high-quality. Using this secondary IP pool helps to reduce the probability of the normal outbound-IP pool being added to a blocked list. The possibility of the high-risk delivery pool being placed on a blocked list remains a risk. This is by design.</span></span>
  
<span data-ttu-id="61578-113">Les messages pour lesquels le domaine d'envoi n'a ni enregistrement d'adresse (enregistrement A), qui vous permet de récupérer l'adresse IP du domaine, ni enregistrement MX, qui permet de diriger le message électronique vers les serveurs censés recevoir le message pour un domaine particulier dans le DNS, sont toujours acheminés via le pool de remise à risque élevé qu'elle que soit leur inclination à être du courrier indésirable.</span><span class="sxs-lookup"><span data-stu-id="61578-113">Messages where the sending domain has no address record (A record), which gives you the IP address of the domain, and no MX record, which helps direct mail to the servers that should receive the mail for a particular domain in the DNS, are always routed through the high-risk delivery pool regardless of their spam disposition.</span></span>
  
## <a name="understanding-delivery-status-notification-dsn-messages"></a><span data-ttu-id="61578-114">Présentation des messages de notification d'état de remise (DSN)</span><span class="sxs-lookup"><span data-stu-id="61578-114">Understanding Delivery Status Notification (DSN) messages</span></span>

<span data-ttu-id="61578-115">Le pool de remise à risque élevé sortant gère la remise de tous les messages de notification d'état de remise (DSN) « rejetés » ou « en échec ».</span><span class="sxs-lookup"><span data-stu-id="61578-115">The outbound high-risk delivery pool manages the delivery for all "bounced" or "failed" (DSN) messages.</span></span>
  
<span data-ttu-id="61578-116">Voici quelques causes possibles à une augmentation subite du nombre de messages DSN :</span><span class="sxs-lookup"><span data-stu-id="61578-116">Possible causes for a surge in DSN messages include the following:</span></span>
  
- <span data-ttu-id="61578-117">Une campagne de falsification affectant l'un des clients qui utilisent le service.</span><span class="sxs-lookup"><span data-stu-id="61578-117">A spoofing campaign affecting one of the customers using the service</span></span>
    
- <span data-ttu-id="61578-118">Une attaque DHA (Directory Harvest Attack).</span><span class="sxs-lookup"><span data-stu-id="61578-118">A directory harvest attack</span></span>
    
- <span data-ttu-id="61578-119">Une attaque par courrier indésirable.</span><span class="sxs-lookup"><span data-stu-id="61578-119">A spam attack</span></span>
    
- <span data-ttu-id="61578-120">Un serveur SMTP non autorisé.</span><span class="sxs-lookup"><span data-stu-id="61578-120">A rogue SMTP server</span></span>
    
<span data-ttu-id="61578-p103">Tous ces problèmes peuvent entraîner une augmentation subite du nombre de messages DSN traités par le service. Souvent, ces messages DSN sont considérés comme des courriers indésirables auprès des autres serveurs de messagerie et services.</span><span class="sxs-lookup"><span data-stu-id="61578-p103">All of these issues can result in a sudden increase in the number of DSN messages being processed by the service. Many times, these DSN messages appear to be spam to other email servers and services.</span></span>
  
## <a name="for-more-information"></a><span data-ttu-id="61578-123">Pour plus d'informations</span><span class="sxs-lookup"><span data-stu-id="61578-123">For more information</span></span>

[<span data-ttu-id="61578-124">Configurer la stratégie anti-courrier indésirable sortant</span><span class="sxs-lookup"><span data-stu-id="61578-124">Configure the outbound spam policy</span></span>](configure-the-outbound-spam-policy.md)
  
[<span data-ttu-id="61578-125">FAQ sur la protection contre le courrier indésirable</span><span class="sxs-lookup"><span data-stu-id="61578-125">Anti-spam protection FAQ</span></span>](anti-spam-protection-faq.md)
  

