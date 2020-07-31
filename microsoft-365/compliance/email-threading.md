---
title: 'Threading de messagerie : enquêtes sur les données'
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
ms.assetid: ''
description: Lors de la gestion d’une enquête sur les données, le Threading de messagerie analyse une conversation électronique et sépare chaque message en différentes catégories.
ms.custom: seo-marvel-mar2020
ms.openlocfilehash: 66238d87bd314f2b29e77886f33cb53f9a879aff
ms.sourcegitcommit: 6501e01a9ab131205a3eef910e6cea7f65b3f010
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/30/2020
ms.locfileid: "46527662"
---
# <a name="email-threading"></a><span data-ttu-id="6f50c-103">Threading de messagerie</span><span class="sxs-lookup"><span data-stu-id="6f50c-103">Email threading</span></span>

<span data-ttu-id="6f50c-104">Considérez une conversation par courrier électronique qui s’est en cours pendant un certain temps.</span><span class="sxs-lookup"><span data-stu-id="6f50c-104">Consider an email conversation that has been going on for a while.</span></span> <span data-ttu-id="6f50c-105">Dans la plupart des cas, le dernier courrier électronique sur le thread inclura le contenu de tous les messages électroniques précédents ; en examinant le dernier courrier électronique, vous obtiendrez un contexte complet de la conversation qui s’est produite dans le fil de discussion.</span><span class="sxs-lookup"><span data-stu-id="6f50c-105">In most cases, the last email on the thread will include the contents of all the preceding emails; reviewing the last email will give a complete context of the conversation that happened in the thread.</span></span> <span data-ttu-id="6f50c-106">Le Threading de messagerie identifie ces messages afin que les réviseurs puissent examiner une partie des documents collectés sans perdre de contexte.</span><span class="sxs-lookup"><span data-stu-id="6f50c-106">Email threading identifies such emails so that reviewers can review a fraction of collected documents without losing any context.</span></span>

## <a name="what-does-email-threading-do"></a><span data-ttu-id="6f50c-107">Qu’est-ce que le Threading du courrier électronique ?</span><span class="sxs-lookup"><span data-stu-id="6f50c-107">What does email threading do?</span></span>

<span data-ttu-id="6f50c-108">Le Threading de messagerie analyse chaque message électronique et les construit sur des messages individuels ; chaque message électronique est une chaîne de messages individuels.</span><span class="sxs-lookup"><span data-stu-id="6f50c-108">Email threading parses each email and deconstructs it to individual messages; each email is a chain of individual messages.</span></span> <span data-ttu-id="6f50c-109">Ensuite, il analyse tous les messages électroniques du jeu de travail afin de déterminer si un e-mail a un contenu unique ou si la chaîne est entièrement contenue dans un autre message électronique.</span><span class="sxs-lookup"><span data-stu-id="6f50c-109">Then, it analyzes all emails in the working set to determine whether an email has unique content or if the chain is wholly contained in a different email.</span></span> <span data-ttu-id="6f50c-110">Dans les messages électroniques finaux se répartissent en quatre catégories :</span><span class="sxs-lookup"><span data-stu-id="6f50c-110">In the end emails are divided into four categories:</span></span>

- <span data-ttu-id="6f50c-111">**Conversation complète** : le dernier message présente un contenu unique. Le courrier inclut toutes les pièces jointes ajoutées aux autres messages dont le contenu est entièrement disponible dans ce courrier.</span><span class="sxs-lookup"><span data-stu-id="6f50c-111">**Inclusive**: the last message in the email has unique content, and the email has all of the attachments that were included in other emails of which the content is wholly contained in this email.</span></span>


- <span data-ttu-id="6f50c-112">**Conversation complète moins pièce jointe** : le dernier message présente un contenu unique. Toutefois, le courrier n’inclut pas certaines pièces jointes ajoutées aux autres messages dont le contenu est entièrement disponible dans ce courrier.</span><span class="sxs-lookup"><span data-stu-id="6f50c-112">**Inclusive minus**: the last message in the email has unique content, but the email does not contain some of the attachments that were included in other emails of which the content is wholly contained in this email.</span></span>

- <span data-ttu-id="6f50c-113">**Copie complète** : copie exacte d’une conversation complète ou conversation complète moins pièce jointe.</span><span class="sxs-lookup"><span data-stu-id="6f50c-113">**Inclusive copy**: an exact copy of an inclusive/inclusive minus email</span></span>

- <span data-ttu-id="6f50c-114">**Aucune** : le contenu du message est inclus entièrement dans au moins un courrier marqué comme conversation complète ou conversation complète moins pièce jointe.</span><span class="sxs-lookup"><span data-stu-id="6f50c-114">**None**: The content of this email is wholly contained in at least one email that is marked as inclusive/inclusive minus.</span></span>

## <a name="how-is-it-different-from-conversations-in-outlook"></a><span data-ttu-id="6f50c-115">Quelle est la différence entre les conversations dans Outlook ?</span><span class="sxs-lookup"><span data-stu-id="6f50c-115">How is it different from conversations in Outlook?</span></span>
<span data-ttu-id="6f50c-116">En un clin d’œil, cela ressemble aux groupements de conversation dans Outlook.</span><span class="sxs-lookup"><span data-stu-id="6f50c-116">At a glance, this sounds similar to conversation groupings in Outlook.</span></span> <span data-ttu-id="6f50c-117">Toutefois, il existe des distinctions importantes.</span><span class="sxs-lookup"><span data-stu-id="6f50c-117">However, there are some important distinctions.</span></span> <span data-ttu-id="6f50c-118">Considérez une conversation par courrier électronique qui a été divisée en deux conversations ; par exemple, quelqu’un a répondu à un message électronique qui n’est pas le dernier de la conversation, les deux derniers messages de la conversation ont un contenu unique.</span><span class="sxs-lookup"><span data-stu-id="6f50c-118">Consider an email conversation that got forked into two conversations; for instance, someone responded to an email that is not the latest in the conversation so the last two emails in the conversation both have unique content.</span></span>

<span data-ttu-id="6f50c-119">Outlook regroupera les messages électroniques en une seule conversation ; la lecture du dernier courrier électronique ne signifie pas qu’il manque le contexte de l’avant-dernier e-mail, qui contient également du contenu unique.</span><span class="sxs-lookup"><span data-stu-id="6f50c-119">Outlook would still group the emails into a single conversation; reading only the last email would mean missing the context of the second-to-last email, which also contains unique content.</span></span> <span data-ttu-id="6f50c-120">Étant donné que le Threading de messagerie analyse chaque courrier électronique dans des composants individuels et les compare, le Threading de messagerie marque les deux derniers courriers électroniques en s’assurant que vous ne manquez pas de contexte tant que vous lisez tous les messages électroniques marqués comme inclus.</span><span class="sxs-lookup"><span data-stu-id="6f50c-120">Because email threading parses out each email into individual components and compares them, email threading would mark both of the last two emails as inclusive, ensuring that you won't miss any context as long as you read all emails marked as inclusive.</span></span>
