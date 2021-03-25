---
title: Questions fréquemment posées sur les messages mis en file d'attente, différés et retournés dans EOP
f1.keywords:
- NOCSH
ms.author: chrisda
author: chrisda
manager: dansimp
ms.date: ''
audience: ITPro
ms.topic: troubleshooting
localization_priority: Normal
ms.assetid: 9d015a0d-52a0-484d-9a08-121d04f973d3
ms.custom:
- seo-marvel-apr2020
description: Trouvez des réponses aux questions les plus fréquentes sur les messages mis en file d’attente, différés ou renvoyés au cours du processus de filtrage Exchange Online Protection (EOP).
ms.technology: mdo
ms.prod: m365-security
ms.openlocfilehash: c7b5ba595e9a6401efd1b733c9e5a11c8a966037
ms.sourcegitcommit: dcb97fbfdae52960ae62b6faa707a05358193ed5
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/25/2021
ms.locfileid: "51204827"
---
# <a name="eop-queued-deferred-and-bounced-messages-faq"></a><span data-ttu-id="910ea-103">Questions fréquemment posées sur les messages mis en file d’attente, différés et retournés dans EOP</span><span class="sxs-lookup"><span data-stu-id="910ea-103">EOP queued, deferred, and bounced messages FAQ</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../includes/microsoft-defender-for-office.md)]

<span data-ttu-id="910ea-104">**S’applique à**</span><span class="sxs-lookup"><span data-stu-id="910ea-104">**Applies to**</span></span>
- [<span data-ttu-id="910ea-105">Exchange Online Protection</span><span class="sxs-lookup"><span data-stu-id="910ea-105">Exchange Online Protection</span></span>](exchange-online-protection-overview.md)
- [<span data-ttu-id="910ea-106">Microsoft Defender pour Office 365 : offre 1 et offre 2</span><span class="sxs-lookup"><span data-stu-id="910ea-106">Microsoft Defender for Office 365 plan 1 and plan 2</span></span>](defender-for-office-365.md)
- [<span data-ttu-id="910ea-107">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="910ea-107">Microsoft 365 Defender</span></span>](../defender/microsoft-365-defender.md)

<span data-ttu-id="910ea-108">Cette rubrique fournit des réponses aux questions fréquemment posées sur les messages mis en file d’attente, différés ou renvoyés pendant le processus de filtrage Exchange Online Protection (EOP).</span><span class="sxs-lookup"><span data-stu-id="910ea-108">This topic provides answers to frequently asked questions about messages that have been queued, deferred, or bounced during the Exchange Online Protection (EOP) filtering process.</span></span>

## <a name="why-is-mail-queuing"></a><span data-ttu-id="910ea-109">Pourquoi le courrier électronique est-il mis en file d’attente ?</span><span class="sxs-lookup"><span data-stu-id="910ea-109">Why is mail queuing?</span></span>

<span data-ttu-id="910ea-110">Les messages sont mis en file d'attente ou différés si le service n'est pas en mesure d'établir une connexion au serveur du destinataire en vue de la remise.</span><span class="sxs-lookup"><span data-stu-id="910ea-110">Messages are queued or deferred if the service is unable to make a connection to the recipient server for delivery.</span></span> <span data-ttu-id="910ea-111">Les messages ne sont pas différés si le réseau du destinataire renvoie une erreur de la série 500.</span><span class="sxs-lookup"><span data-stu-id="910ea-111">It will not defer messages if a 500-series error is returned from the recipient network.</span></span>

## <a name="how-does-a-message-become-deferred"></a><span data-ttu-id="910ea-112">Dans quelles circonstances un message est-il différé ?</span><span class="sxs-lookup"><span data-stu-id="910ea-112">How does a message become deferred?</span></span>

<span data-ttu-id="910ea-113">Les messages sont retenus s'il est impossible d'établir une connexion au serveur du destinataire et que celui-ci renvoie une « défaillance temporaire », comme une expiration de connexion, un refus de connexion ou une erreur de la série 400.</span><span class="sxs-lookup"><span data-stu-id="910ea-113">Messages will be held when a connection to the recipient server cannot be made and the recipient's server is returning a "temporary failure" such as a connection time-out, connection refused, or a 400-series error.</span></span> <span data-ttu-id="910ea-114">En cas de défaillance permanente, comme une erreur de la série 500, le message est renvoyé à l'expéditeur.</span><span class="sxs-lookup"><span data-stu-id="910ea-114">If there is a permanent failure, such as a 500-series error, then the message will be returned to the sender.</span></span>

## <a name="how-long-does-a-message-remain-in-deferral-and-what-is-the-retry-interval"></a><span data-ttu-id="910ea-115">Combien de temps un message reste-t-il en attente et quel est l’intervalle des nouvelles tentatives ?</span><span class="sxs-lookup"><span data-stu-id="910ea-115">How long does a message remain in deferral and what is the retry interval?</span></span>

<span data-ttu-id="910ea-116">Les messages en attente resteront dans nos files d’attente pendant 1 jour.</span><span class="sxs-lookup"><span data-stu-id="910ea-116">Messages in deferral will remain in our queues for 1 day.</span></span> <span data-ttu-id="910ea-117">Les nouvelles tentatives d'envoi de message sont basées sur les erreurs que nous recevons à partir du système de messagerie du destinataire.</span><span class="sxs-lookup"><span data-stu-id="910ea-117">Message retry attempts are based on the error we get back from the recipient's mail system.</span></span> <span data-ttu-id="910ea-118">Les premiers reports sont de 15 minutes ou moins, avec des tentatives suivantes (sur la demi-dizaine suivante) augmentant l’intervalle sur plusieurs tentatives jusqu’à un maximum de 60 minutes.</span><span class="sxs-lookup"><span data-stu-id="910ea-118">The first few deferrals are 15 minutes or less, with subsequent retries (over the next half dozen or so) increasing the interval over multiple retries to a max of 60 minutes.</span></span> <span data-ttu-id="910ea-119">L’expansion de la durée d’intervalle est dynamique, en tenant compte de plusieurs variables telles que la taille des files d’attente et la priorité des messages internes.</span><span class="sxs-lookup"><span data-stu-id="910ea-119">The interval duration expansion is dynamic, taking into consideration multiple variables like queue sizes and internal message priority.</span></span> <span data-ttu-id="910ea-120">En base, il faut 15 minutes (ou moins) pour commencer, puis développer à partir de là au cours des prochaines heures à 60 minutes max.</span><span class="sxs-lookup"><span data-stu-id="910ea-120">In basic, it's 15 minutes (or less) to start, then expanding from there over the next few hours to 60 mins max.</span></span>

## <a name="after-your-email-server-is-restored-how-are-queued-messages-distributed"></a><span data-ttu-id="910ea-121">Après la restauration du serveur de messagerie, comment les messages mis en file d’attente sont-ils distribués ?</span><span class="sxs-lookup"><span data-stu-id="910ea-121">After your email server is restored, how are queued messages distributed?</span></span>

<span data-ttu-id="910ea-122">Une fois que votre serveur de messagerie est restauré, tous les messages mis en file d'attente sont automatiquement traités dans l'ordre dans lequel ils ont été reçus et mis en file d'attente lorsque le serveur est devenu indisponible.</span><span class="sxs-lookup"><span data-stu-id="910ea-122">After your email server is restored, all queued messages are automatically processed in the order in which they were received and queued when the server became unavailable.</span></span>
