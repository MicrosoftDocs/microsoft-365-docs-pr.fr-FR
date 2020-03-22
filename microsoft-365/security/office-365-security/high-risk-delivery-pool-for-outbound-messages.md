---
title: Pool de remise à risque élevé pour les messages sortants
f1.keywords:
- NOCSH
ms.author: chrisda
author: chrisda
manager: dansimp
ms.date: ''
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: ac11edd9-2da3-462d-8ea3-bbf9dbc6f948
ms.collection:
- M365-security-compliance
description: Découvrez comment le pool de remise à haut risque est utilisé pour protéger la réputation des serveurs de messagerie dans les centres de ressources Office 365.
ms.openlocfilehash: 5d1bd2b14eb17ed74ee1cf1e44967f660f4595b8
ms.sourcegitcommit: fce0d5cad32ea60a08ff001b228223284710e2ed
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/21/2020
ms.locfileid: "42895358"
---
# <a name="high-risk-delivery-pool-for-outbound-messages-in-office-365"></a><span data-ttu-id="a5e83-103">Pool de remise à haut risque pour les messages sortants dans Office 365</span><span class="sxs-lookup"><span data-stu-id="a5e83-103">High-risk delivery pool for outbound messages in Office 365</span></span>

<span data-ttu-id="a5e83-104">Les serveurs de messagerie dans les centres de 365 Office peuvent être temporairement coupable d’envoyer du courrier indésirable.</span><span class="sxs-lookup"><span data-stu-id="a5e83-104">Email servers in the Office 365 datacenters might be temporarily guilty of sending spam.</span></span> <span data-ttu-id="a5e83-105">Par exemple, un programme malveillant ou une attaque de courrier indésirable malveillant dans une organisation de messagerie locale qui envoie des messages sortants via Office 365 ou des comptes Office 365 compromis.</span><span class="sxs-lookup"><span data-stu-id="a5e83-105">For example, a malware or malicious spam attack in an on-premises email organization that sends outbound mail through Office 365, or compromised Office 365 accounts.</span></span> <span data-ttu-id="a5e83-106">Ces scénarios peuvent entraîner l’affichage de l’adresse IP des serveurs Office 365 Datacenter concernés qui apparaissent sur des listes rouges tierces.</span><span class="sxs-lookup"><span data-stu-id="a5e83-106">These scenarios can result in the IP address of the affected Office 365 datacenter servers appearing on third-party block lists.</span></span> <span data-ttu-id="a5e83-107">Les organisations de messagerie de destination qui utilisent ces listes rouges rejettent les messages provenant de ces sources de messages.</span><span class="sxs-lookup"><span data-stu-id="a5e83-107">Destination email organizations that use these block lists will reject email from those messages sources.</span></span>

<span data-ttu-id="a5e83-108">Pour éviter ce problème, tous les messages sortants provenant de serveurs Office 365 Datacenter qui sont considérés comme des courriers indésirables ou qui dépassent les limites d’envoi du [service](https://docs.microsoft.com/office365/servicedescriptions/exchange-online-service-description/exchange-online-limits#sending-limits-across-office-365-options) ou les [stratégies de courrier indésirable sortant](configure-the-outbound-spam-policy.md) sont envoyés via le _pool de remise à haut risque_.</span><span class="sxs-lookup"><span data-stu-id="a5e83-108">To prevent this, all outbound messages from Office 365 datacenter servers that's determined to be spam or that exceeds the sending limits of [the service](https://docs.microsoft.com/office365/servicedescriptions/exchange-online-service-description/exchange-online-limits#sending-limits-across-office-365-options) or [outbound spam policies](configure-the-outbound-spam-policy.md) are sent through the _high-risk delivery pool_.</span></span>

<span data-ttu-id="a5e83-109">Le pool de remise à haut risque est un pool d’adresses IP secondaire pour le courrier électronique sortant, qui sert uniquement à envoyer des messages « de faible qualité » (par exemple, le courrier indésirable et [rétrodiffusion](backscatter-messages-and-eop.md)).</span><span class="sxs-lookup"><span data-stu-id="a5e83-109">The high risk delivery pool is a secondary IP address pool for outbound email that's only used to send "low quality" messages (for example, spam and [backscatter](backscatter-messages-and-eop.md)).</span></span> <span data-ttu-id="a5e83-110">Le pool de remise à haut risque empêche le pool d’adresses IP normal pour le courrier électronique sortant d’envoyer du courrier indésirable.</span><span class="sxs-lookup"><span data-stu-id="a5e83-110">Using the high risk delivery pool helps prevent the normal IP address pool for outbound email from sending spam.</span></span> <span data-ttu-id="a5e83-111">Le pool d’adresses IP normales pour le courrier électronique sortant maintient la réputation envoyant des messages « de qualité supérieure », ce qui réduit la probabilité que ces adresses IP apparaissent sur les listes d’adresses IP bloquées.</span><span class="sxs-lookup"><span data-stu-id="a5e83-111">The normal IP address pool for outbound email maintains the reputation sending "high quality" messages, which reduces the likelihood that these IP address will appear on IP block lists.</span></span>

<span data-ttu-id="a5e83-112">La probabilité très réelle que les adresses IP dans le pool de remise à haut risque soient placées sur les listes d’adresses IP bloquées reste, mais cela est dû à la conception.</span><span class="sxs-lookup"><span data-stu-id="a5e83-112">The very real possibility that IP addresses in the high-risk delivery pool will be placed on IP block lists remains, but this is by design.</span></span> <span data-ttu-id="a5e83-113">La remise aux destinataires prévus n’est pas garantie, car de nombreuses organisations de messagerie n’acceptent pas les messages du pool de remise à haut risque.</span><span class="sxs-lookup"><span data-stu-id="a5e83-113">Delivery to the intended recipients isn't guaranteed, because many email organizations won't accept messages from the high risk delivery pool.</span></span>

<span data-ttu-id="a5e83-114">Pour plus d’informations, consultez la rubrique [contrôler le courrier indésirable sortant dans Office 365](outbound-spam-controls.md).</span><span class="sxs-lookup"><span data-stu-id="a5e83-114">For more information, see [Control outbound spam in Office 365](outbound-spam-controls.md).</span></span>

> [!NOTE]
> <span data-ttu-id="a5e83-115">Messages dans lesquels le domaine de messagerie source n’a pas d’enregistrement a et aucun enregistrement MX défini dans DNS public n’est toujours routé via le pool de remise à haut risque, indépendamment de la disposition des limites d’envoi ou de courrier indésirable.</span><span class="sxs-lookup"><span data-stu-id="a5e83-115">Messages where the source email domain has no A record and no MX record defined in public DNS are always routed through the high-risk delivery pool, regardless of their spam or sending limit disposition.</span></span>

## <a name="bounce-messages"></a><span data-ttu-id="a5e83-116">Messages de retour</span><span class="sxs-lookup"><span data-stu-id="a5e83-116">Bounce messages</span></span>

<span data-ttu-id="a5e83-117">Le pool de remise à haut risque sortant gère la remise de tous les rapports de non-remise (également appelés notifications d’échec de remise, messages de retransmission, notifications d’état de remise ou notifications d’échec de remise).</span><span class="sxs-lookup"><span data-stu-id="a5e83-117">The outbound high-risk delivery pool manages the delivery for all non-delivery reports (also known as NDRs, bounce messages, delivery status notifications, or DSNs).</span></span>

<span data-ttu-id="a5e83-118">Voici les causes possibles d’une augmentation des notifications d’échec de remise :</span><span class="sxs-lookup"><span data-stu-id="a5e83-118">Possible causes for a surge in NDRs include:</span></span>

- <span data-ttu-id="a5e83-119">Une campagne d’usurpation d’identité qui affecte l’un des clients utilisant le service.</span><span class="sxs-lookup"><span data-stu-id="a5e83-119">A spoofing campaign that affects one of the customers using the service.</span></span>

- <span data-ttu-id="a5e83-120">Une attaque par extraction d’annuaire.</span><span class="sxs-lookup"><span data-stu-id="a5e83-120">A directory harvest attack.</span></span>

- <span data-ttu-id="a5e83-121">Une attaque de courrier indésirable.</span><span class="sxs-lookup"><span data-stu-id="a5e83-121">A spam attack.</span></span>

- <span data-ttu-id="a5e83-122">Un serveur de messagerie non autorisé.</span><span class="sxs-lookup"><span data-stu-id="a5e83-122">A rogue email server.</span></span>

<span data-ttu-id="a5e83-123">Tous ces problèmes peuvent entraîner une augmentation soudaine du nombre de notifications d’échec de remise traitées par le service.</span><span class="sxs-lookup"><span data-stu-id="a5e83-123">All of these issues can result in a sudden increase in the number of NDRs being processed by the service.</span></span> <span data-ttu-id="a5e83-124">Bien souvent, ces notifications d’échec de remise semblent être du courrier indésirable pour les autres serveurs et services de messagerie (également appelés _[rétrodiffusion](backscatter-messages-and-eop.md)_).</span><span class="sxs-lookup"><span data-stu-id="a5e83-124">Many times, these NDRs appear to be spam to other email servers and services (also known as _[backscatter](backscatter-messages-and-eop.md)_).</span></span>
