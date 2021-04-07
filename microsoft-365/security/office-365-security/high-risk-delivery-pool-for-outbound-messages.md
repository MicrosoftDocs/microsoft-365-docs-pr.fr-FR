---
title: Pools de livraison sortante
f1.keywords:
- NOCSH
ms.author: chrisda
author: chrisda
manager: dansimp
ms.date: ''
audience: ITPro
ms.topic: conceptual
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: ac11edd9-2da3-462d-8ea3-bbf9dbc6f948
ms.collection:
- M365-security-compliance
description: Découvrez comment les pools de remise sont utilisés pour protéger la réputation des serveurs de messagerie dans les centres de données Microsoft 365.
ms.technology: mdo
ms.prod: m365-security
ms.openlocfilehash: ac3469150ef5cf5c1040fcddf7f0bc95e7a18805
ms.sourcegitcommit: 7ee50882cb4ed37794a3cd82dac9b2f9e0a1f14a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/06/2021
ms.locfileid: "51599910"
---
# <a name="outbound-delivery-pools"></a><span data-ttu-id="5dc75-103">Pools de livraison sortante</span><span class="sxs-lookup"><span data-stu-id="5dc75-103">Outbound delivery pools</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../includes/microsoft-defender-for-office.md)]

<span data-ttu-id="5dc75-104">**S’applique à**</span><span class="sxs-lookup"><span data-stu-id="5dc75-104">**Applies to**</span></span>
- [<span data-ttu-id="5dc75-105">Exchange Online Protection</span><span class="sxs-lookup"><span data-stu-id="5dc75-105">Exchange Online Protection</span></span>](exchange-online-protection-overview.md)
- [<span data-ttu-id="5dc75-106">Microsoft Defender pour Office 365 : offre 1 et offre 2</span><span class="sxs-lookup"><span data-stu-id="5dc75-106">Microsoft Defender for Office 365 plan 1 and plan 2</span></span>](defender-for-office-365.md)
- [<span data-ttu-id="5dc75-107">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="5dc75-107">Microsoft 365 Defender</span></span>](../defender/microsoft-365-defender.md)

<span data-ttu-id="5dc75-108">Les serveurs de messagerie dans les centres de données Microsoft 365 peuvent ne pas pouvoir envoyer de courrier indésirable temporairement.</span><span class="sxs-lookup"><span data-stu-id="5dc75-108">Email servers in the Microsoft 365 datacenters might be temporarily guilty of sending spam.</span></span> <span data-ttu-id="5dc75-109">Par exemple, une attaque de programme malveillant ou de courrier indésirable dans une organisation de messagerie sur site qui envoie du courrier sortant via Microsoft 365 ou des comptes Microsoft 365 compromis.</span><span class="sxs-lookup"><span data-stu-id="5dc75-109">For example, a malware or malicious spam attack in an on-premises email organization that sends outbound mail through Microsoft 365, or compromised Microsoft 365 accounts.</span></span> <span data-ttu-id="5dc75-110">Les attaquants tentent également d’éviter la détection en relayant des messages via le forwarding Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="5dc75-110">Attackers also try to avoid detection by relaying messages through Microsoft 365 forwarding.</span></span>

<span data-ttu-id="5dc75-111">Ces scénarios peuvent entraîner l’apparition de l’adresse IP des serveurs de centre de données Microsoft 365 affectés sur des listes de blocage tierces.</span><span class="sxs-lookup"><span data-stu-id="5dc75-111">These scenarios can result in the IP address of the affected Microsoft 365 datacenter servers appearing on third-party blocklists.</span></span> <span data-ttu-id="5dc75-112">Les organisations de messagerie de destination qui utilisent ces listes de blocage rejetteront les messages provenant de ces sources de messages.</span><span class="sxs-lookup"><span data-stu-id="5dc75-112">Destination email organizations that use these blocklists will reject email from those messages sources.</span></span>

## <a name="high-risk-delivery-pool"></a><span data-ttu-id="5dc75-113">Pool de remise à risque élevé</span><span class="sxs-lookup"><span data-stu-id="5dc75-113">High-risk delivery pool</span></span>
<span data-ttu-id="5dc75-114">Pour éviter cela, tous les messages sortants provenant de serveurs de centre de données Microsoft 365 [](configure-the-outbound-spam-policy.md) qui sont déterminés comme courrier indésirable ou qui dépassent les limites d’envoi du [service](/office365/servicedescriptions/exchange-online-service-description/exchange-online-limits#sending-limits-across-office-365-options) ou des stratégies de courrier indésirable sortant sont envoyés via le _pool_ de remise à risque élevé.</span><span class="sxs-lookup"><span data-stu-id="5dc75-114">To prevent this, all outbound messages from Microsoft 365 datacenter servers that's determined to be spam or that exceeds the sending limits of [the service](/office365/servicedescriptions/exchange-online-service-description/exchange-online-limits#sending-limits-across-office-365-options) or [outbound spam policies](configure-the-outbound-spam-policy.md) are sent through the _high-risk delivery pool_.</span></span>

<span data-ttu-id="5dc75-115">Le pool de remise à risque élevé est un pool d’adresses IP distinct pour les messages sortants qui est uniquement utilisé pour envoyer des messages de « faible qualité » (par exemple, courrier indésirable et [backscatter).](backscatter-messages-and-eop.md)</span><span class="sxs-lookup"><span data-stu-id="5dc75-115">The high risk delivery pool is a separate IP address pool for outbound email that's only used to send "low quality" messages (for example, spam and [backscatter](backscatter-messages-and-eop.md)).</span></span> <span data-ttu-id="5dc75-116">L’utilisation du pool de remise à risque élevé permet d’empêcher le pool d’adresses IP normal pour le courrier sortant d’envoyer du courrier indésirable.</span><span class="sxs-lookup"><span data-stu-id="5dc75-116">Using the high risk delivery pool helps prevent the normal IP address pool for outbound email from sending spam.</span></span> <span data-ttu-id="5dc75-117">Le pool d’adresses IP normal pour le courrier sortant conserve la réputation d’envoi de messages de « haute qualité », ce qui réduit la probabilité que ces adresses IP apparaissent sur les listes d’adresses IP bloqués.</span><span class="sxs-lookup"><span data-stu-id="5dc75-117">The normal IP address pool for outbound email maintains the reputation sending "high quality" messages, which reduces the likelihood that these IP address will appear on IP blocklists.</span></span>

<span data-ttu-id="5dc75-118">La possibilité réelle que les adresses IP du pool de remise à risque élevé soient placées sur des listes d’adresses IP bloqués demeure, mais cela est tout à fait possible.</span><span class="sxs-lookup"><span data-stu-id="5dc75-118">The very real possibility that IP addresses in the high-risk delivery pool will be placed on IP blocklists remains, but this is by design.</span></span> <span data-ttu-id="5dc75-119">La remise aux destinataires prévus n’est pas garantie, car de nombreuses organisations de messagerie n’acceptent pas les messages provenant du pool de remise à risque élevé.</span><span class="sxs-lookup"><span data-stu-id="5dc75-119">Delivery to the intended recipients isn't guaranteed, because many email organizations won't accept messages from the high risk delivery pool.</span></span>

<span data-ttu-id="5dc75-120">Pour plus d’informations, voir [Contrôler le courrier indésirable sortant.](outbound-spam-controls.md)</span><span class="sxs-lookup"><span data-stu-id="5dc75-120">For more information, see [Control outbound spam](outbound-spam-controls.md).</span></span>

> [!NOTE]
> <span data-ttu-id="5dc75-121">Les messages pour lequel le domaine de messagerie source n’a pas d’enregistrement A et aucun enregistrement MX défini dans le DNS public sont toujours acheminés via le pool de remise à risque élevé, quel que soit leur courrier indésirable ou leur disposition de limite d’envoi.</span><span class="sxs-lookup"><span data-stu-id="5dc75-121">Messages where the source email domain has no A record and no MX record defined in public DNS are always routed through the high-risk delivery pool, regardless of their spam or sending limit disposition.</span></span>

### <a name="bounce-messages"></a><span data-ttu-id="5dc75-122">Messages de non-rebond</span><span class="sxs-lookup"><span data-stu-id="5dc75-122">Bounce messages</span></span>

<span data-ttu-id="5dc75-123">Le pool de remise à haut risque sortant gère la remise de tous les rapports de non-remise (également appelés notifications de non-remise, notifications de non-remise, notifications d’état de remise ou notifications d’état de remise).</span><span class="sxs-lookup"><span data-stu-id="5dc75-123">The outbound high-risk delivery pool manages the delivery for all non-delivery reports (also known as NDRs, bounce messages, delivery status notifications, or DSNs).</span></span>

<span data-ttu-id="5dc75-124">Les causes possibles d’une augmentation des NDR sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="5dc75-124">Possible causes for a surge in NDRs include:</span></span>

- <span data-ttu-id="5dc75-125">Une campagne d’usurpation qui affecte l’un des clients qui utilisent le service.</span><span class="sxs-lookup"><span data-stu-id="5dc75-125">A spoofing campaign that affects one of the customers using the service.</span></span>
- <span data-ttu-id="5dc75-126">Une attaque de la recherche dans l’annuaire.</span><span class="sxs-lookup"><span data-stu-id="5dc75-126">A directory harvest attack.</span></span>
- <span data-ttu-id="5dc75-127">Une attaque de courrier indésirable.</span><span class="sxs-lookup"><span data-stu-id="5dc75-127">A spam attack.</span></span>
- <span data-ttu-id="5dc75-128">Un serveur de messagerie non fiable.</span><span class="sxs-lookup"><span data-stu-id="5dc75-128">A rogue email server.</span></span>

<span data-ttu-id="5dc75-129">Tous ces problèmes peuvent entraîner une augmentation soudaine du nombre de NDR traitées par le service.</span><span class="sxs-lookup"><span data-stu-id="5dc75-129">All of these issues can result in a sudden increase in the number of NDRs being processed by the service.</span></span> <span data-ttu-id="5dc75-130">De nombreuses fois, ces NDR semblent être du courrier indésirable pour d’autres serveurs et services de messagerie (également appelé _[backscatter).](backscatter-messages-and-eop.md)_</span><span class="sxs-lookup"><span data-stu-id="5dc75-130">Many times, these NDRs appear to be spam to other email servers and services (also known as _[backscatter](backscatter-messages-and-eop.md)_).</span></span>
