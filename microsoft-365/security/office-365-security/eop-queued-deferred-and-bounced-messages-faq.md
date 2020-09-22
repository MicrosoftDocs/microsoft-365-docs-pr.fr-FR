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
ms.service: O365-seccomp
localization_priority: Normal
ms.assetid: 9d015a0d-52a0-484d-9a08-121d04f973d3
ms.custom:
- seo-marvel-apr2020
description: Trouvez des réponses aux questions les plus fréquentes sur les messages qui ont été mis en file d’attente, différés ou retournés lors du processus de filtrage Exchange Online Protection (EOP).
ms.openlocfilehash: 4ae38e871c0d6e4321bd7586c5cfd0bea3aeef81
ms.sourcegitcommit: c083602dda3cdcb5b58cb8aa070d77019075f765
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/22/2020
ms.locfileid: "48202938"
---
# <a name="eop-queued-deferred-and-bounced-messages-faq"></a><span data-ttu-id="a088a-103">Questions fréquemment posées sur les messages mis en file d’attente, différés et retournés dans EOP</span><span class="sxs-lookup"><span data-stu-id="a088a-103">EOP queued, deferred, and bounced messages FAQ</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../includes/microsoft-defender-for-office.md)]


<span data-ttu-id="a088a-104">Cette rubrique fournit des réponses aux questions fréquemment posées sur les messages mis en file d’attente, différés ou retournés lors du processus de filtrage Exchange Online Protection (EOP).</span><span class="sxs-lookup"><span data-stu-id="a088a-104">This topic provides answers to frequently asked questions about messages that have been queued, deferred, or bounced during the Exchange Online Protection (EOP) filtering process.</span></span>

## <a name="why-is-mail-queuing"></a><span data-ttu-id="a088a-105">Pourquoi le courrier électronique est-il mis en file d’attente ?</span><span class="sxs-lookup"><span data-stu-id="a088a-105">Why is mail queuing?</span></span>

<span data-ttu-id="a088a-106">Les messages sont mis en file d'attente ou différés si le service n'est pas en mesure d'établir une connexion au serveur du destinataire en vue de la remise.</span><span class="sxs-lookup"><span data-stu-id="a088a-106">Messages are queued or deferred if the service is unable to make a connection to the recipient server for delivery.</span></span> <span data-ttu-id="a088a-107">Les messages ne sont pas différés si le réseau du destinataire renvoie une erreur de la série 500.</span><span class="sxs-lookup"><span data-stu-id="a088a-107">It will not defer messages if a 500-series error is returned from the recipient network.</span></span>

## <a name="how-does-a-message-become-deferred"></a><span data-ttu-id="a088a-108">Dans quelles circonstances un message est-il différé ?</span><span class="sxs-lookup"><span data-stu-id="a088a-108">How does a message become deferred?</span></span>

<span data-ttu-id="a088a-109">Les messages sont retenus s'il est impossible d'établir une connexion au serveur du destinataire et que celui-ci renvoie une « défaillance temporaire », comme une expiration de connexion, un refus de connexion ou une erreur de la série 400.</span><span class="sxs-lookup"><span data-stu-id="a088a-109">Messages will be held when a connection to the recipient server cannot be made and the recipient's server is returning a "temporary failure" such as a connection time-out, connection refused, or a 400-series error.</span></span> <span data-ttu-id="a088a-110">En cas de défaillance permanente, comme une erreur de la série 500, le message est renvoyé à l'expéditeur.</span><span class="sxs-lookup"><span data-stu-id="a088a-110">If there is a permanent failure, such as a 500-series error, then the message will be returned to the sender.</span></span>

## <a name="how-long-does-a-message-remain-in-deferral-and-what-is-the-retry-interval"></a><span data-ttu-id="a088a-111">Combien de temps un message reste-t-il en attente et quel est l’intervalle des nouvelles tentatives ?</span><span class="sxs-lookup"><span data-stu-id="a088a-111">How long does a message remain in deferral and what is the retry interval?</span></span>

<span data-ttu-id="a088a-112">Les messages en différé resteront dans nos files d’attente pendant 1 jour.</span><span class="sxs-lookup"><span data-stu-id="a088a-112">Messages in deferral will remain in our queues for 1 day.</span></span> <span data-ttu-id="a088a-113">Les nouvelles tentatives d'envoi de message sont basées sur les erreurs que nous recevons à partir du système de messagerie du destinataire.</span><span class="sxs-lookup"><span data-stu-id="a088a-113">Message retry attempts are based on the error we get back from the recipient's mail system.</span></span> <span data-ttu-id="a088a-114">Les premiers nombre de retards sont 15 minutes ou moins, avec les nouvelles tentatives suivantes (au cours d’une demi-douzaine ou par conséquent), ce qui augmente l’intervalle entre plusieurs tentatives et une durée maximale de 60 minutes.</span><span class="sxs-lookup"><span data-stu-id="a088a-114">The first few deferrals are 15 minutes or less, with subsequent retries (over the next half dozen or so) increasing the interval over multiple retries to a max of 60 minutes.</span></span> <span data-ttu-id="a088a-115">L’expansion de la durée de l’intervalle est dynamique, en prenant en compte plusieurs variables telles que les tailles de file d’attente et la priorité des messages internes.</span><span class="sxs-lookup"><span data-stu-id="a088a-115">The interval duration expansion is dynamic, taking into consideration multiple variables like queue sizes and internal message priority.</span></span> <span data-ttu-id="a088a-116">En standard, il faut 15 minutes (ou moins) pour commencer, puis les prochaines heures à 60 mins max.</span><span class="sxs-lookup"><span data-stu-id="a088a-116">In basic, it's 15 minutes (or less) to start, then expanding from there over the next few hours to 60 mins max.</span></span>

## <a name="after-your-email-server-is-restored-how-are-queued-messages-distributed"></a><span data-ttu-id="a088a-117">Après la restauration du serveur de messagerie, comment les messages mis en file d’attente sont-ils distribués ?</span><span class="sxs-lookup"><span data-stu-id="a088a-117">After your email server is restored, how are queued messages distributed?</span></span>

<span data-ttu-id="a088a-118">Une fois que votre serveur de messagerie est restauré, tous les messages mis en file d'attente sont automatiquement traités dans l'ordre dans lequel ils ont été reçus et mis en file d'attente lorsque le serveur est devenu indisponible.</span><span class="sxs-lookup"><span data-stu-id="a088a-118">After your email server is restored, all queued messages are automatically processed in the order in which they were received and queued when the server became unavailable.</span></span>
