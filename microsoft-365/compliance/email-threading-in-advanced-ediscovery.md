---
title: Threading de courrier électronique dans Advanced eDiscovery
f1.keywords:
- NOCSH
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: ''
audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.collection: M365-security-compliance
search.appverid:
- MOE150
- MET150
description: Lors de la réalisation d’une analyse eDiscovery avancée, le Threading de messagerie analyse une conversation électronique et sépare chaque message en différentes catégories.
ms.custom: seo-marvel-mar2020
ms.openlocfilehash: b087bfc84175f80daaf1c0d2f1394584a70757ac
ms.sourcegitcommit: 2160e7cf373f992dd4d11793a59cb8c44f8d587e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/26/2020
ms.locfileid: "48285560"
---
# <a name="email-threading-in-advanced-ediscovery"></a><span data-ttu-id="d84d2-103">Threading de courrier électronique dans Advanced eDiscovery</span><span class="sxs-lookup"><span data-stu-id="d84d2-103">Email threading in Advanced eDiscovery</span></span>

<span data-ttu-id="d84d2-104">Considérez une conversation par courrier électronique qui s’est en cours pendant un certain temps.</span><span class="sxs-lookup"><span data-stu-id="d84d2-104">Consider an email conversation that has been going on for a while.</span></span> <span data-ttu-id="d84d2-105">Dans la plupart des cas, le dernier courrier électronique sur le thread inclura le contenu de tous les messages électroniques précédents ; en examinant le dernier courrier électronique, vous obtiendrez un contexte complet de la conversation qui s’est produite dans le fil de discussion.</span><span class="sxs-lookup"><span data-stu-id="d84d2-105">In most cases, the last email on the thread will include the contents of all the preceding emails; reviewing the last email will give a complete context of the conversation that happened in the thread.</span></span> <span data-ttu-id="d84d2-106">Le Threading de messagerie identifie ces messages afin que les réviseurs puissent examiner une partie des documents collectés sans perdre de contexte.</span><span class="sxs-lookup"><span data-stu-id="d84d2-106">Email threading identifies such emails so that reviewers can review a fraction of collected documents without losing any context.</span></span>

## <a name="what-does-email-threading-do"></a><span data-ttu-id="d84d2-107">Qu’est-ce que le Threading du courrier électronique ?</span><span class="sxs-lookup"><span data-stu-id="d84d2-107">What does email threading do?</span></span>

<span data-ttu-id="d84d2-108">Le Threading de messagerie analyse chaque message électronique et les construit sur des messages individuels ; chaque message électronique est une chaîne de messages individuels.</span><span class="sxs-lookup"><span data-stu-id="d84d2-108">Email threading parses each email and deconstructs it to individual messages; each email is a chain of individual messages.</span></span> <span data-ttu-id="d84d2-109">Ensuite, il analyse tous les messages électroniques de l’ensemble de vérification pour déterminer si un e-mail a un contenu unique ou si la chaîne est entièrement contenue dans un autre message électronique.</span><span class="sxs-lookup"><span data-stu-id="d84d2-109">Then, it analyzes all emails in the review set to determine whether an email has unique content or if the chain is wholly contained in a different email.</span></span> <span data-ttu-id="d84d2-110">Dans les messages électroniques finaux se répartissent en quatre catégories :</span><span class="sxs-lookup"><span data-stu-id="d84d2-110">In the end emails are divided into four categories:</span></span>

- <span data-ttu-id="d84d2-111">**Conversation complète** : le dernier message présente un contenu unique. Le courrier inclut toutes les pièces jointes ajoutées aux autres messages dont le contenu est entièrement disponible dans ce courrier.</span><span class="sxs-lookup"><span data-stu-id="d84d2-111">**Inclusive**: the last message in the email has unique content, and the email has all of the attachments that were included in other emails of which the content is wholly contained in this email.</span></span>

- <span data-ttu-id="d84d2-112">**Conversation complète moins pièce jointe** : le dernier message présente un contenu unique. Toutefois, le courrier n’inclut pas certaines pièces jointes ajoutées aux autres messages dont le contenu est entièrement disponible dans ce courrier.</span><span class="sxs-lookup"><span data-stu-id="d84d2-112">**Inclusive minus**: the last message in the email has unique content, but the email does not contain some of the attachments that were included in other emails of which the content is wholly contained in this email.</span></span>

- <span data-ttu-id="d84d2-113">**Copie complète** : copie exacte d’une conversation complète ou conversation complète moins pièce jointe.</span><span class="sxs-lookup"><span data-stu-id="d84d2-113">**Inclusive copy**: an exact copy of an inclusive/inclusive minus email</span></span>

- <span data-ttu-id="d84d2-114">**Aucune** : le contenu du message est inclus entièrement dans au moins un courrier marqué comme conversation complète ou conversation complète moins pièce jointe.</span><span class="sxs-lookup"><span data-stu-id="d84d2-114">**None**: The content of this email is wholly contained in at least one email that is marked as inclusive/inclusive minus.</span></span>

## <a name="how-is-it-different-from-conversations-in-outlook"></a><span data-ttu-id="d84d2-115">Quelle est la différence entre les conversations dans Outlook ?</span><span class="sxs-lookup"><span data-stu-id="d84d2-115">How is it different from conversations in Outlook?</span></span>

<span data-ttu-id="d84d2-116">En un clin d’œil, cela ressemble aux groupements de conversation dans Outlook.</span><span class="sxs-lookup"><span data-stu-id="d84d2-116">At a glance, this sounds similar to conversation groupings in Outlook.</span></span> <span data-ttu-id="d84d2-117">Toutefois, il existe des distinctions importantes.</span><span class="sxs-lookup"><span data-stu-id="d84d2-117">However, there are some important distinctions.</span></span> <span data-ttu-id="d84d2-118">Considérez une conversation par courrier électronique qui a été divisée en deux conversations ; par exemple, quelqu’un a répondu à un message électronique qui n’est pas le dernier de la conversation, les deux derniers messages de la conversation ont un contenu unique.</span><span class="sxs-lookup"><span data-stu-id="d84d2-118">Consider an email conversation that got forked into two conversations; for instance, someone responded to an email that is not the latest in the conversation so the last two emails in the conversation both have unique content.</span></span>

<span data-ttu-id="d84d2-119">Outlook regroupera les messages électroniques en une seule conversation ; la lecture du dernier courrier électronique ne signifie pas qu’il manque le contexte de l’avant-dernier e-mail, qui contient également du contenu unique.</span><span class="sxs-lookup"><span data-stu-id="d84d2-119">Outlook would still group the emails into a single conversation; reading only the last email would mean missing the context of the second-to-last email, which also contains unique content.</span></span> <span data-ttu-id="d84d2-120">Étant donné que le Threading de messagerie analyse chaque courrier électronique dans des composants individuels et les compare, le Threading de messagerie marque les deux derniers courriers électroniques en s’assurant que vous ne manquez pas de contexte tant que vous lisez tous les messages électroniques marqués comme inclus.</span><span class="sxs-lookup"><span data-stu-id="d84d2-120">Because email threading parses out each email into individual components and compares them, email threading would mark both of the last two emails as inclusive, ensuring that you won't miss any context as long as you read all emails marked as inclusive.</span></span>
