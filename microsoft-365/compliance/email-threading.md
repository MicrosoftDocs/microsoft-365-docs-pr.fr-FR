---
title: Threading de messagerie
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
description: ''
ms.openlocfilehash: 423b3a4ebb00473a45122cf89d2810e6d7c1fc2d
ms.sourcegitcommit: 3dd9944a6070a7f35c4bc2b57df397f844c3fe79
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/15/2020
ms.locfileid: "42074701"
---
# <a name="email-threading"></a><span data-ttu-id="cc391-102">Threading de messagerie</span><span class="sxs-lookup"><span data-stu-id="cc391-102">Email threading</span></span>

<span data-ttu-id="cc391-103">Considérez une conversation par courrier électronique qui s’est en cours pendant un certain temps.</span><span class="sxs-lookup"><span data-stu-id="cc391-103">Consider an email conversation that has been going on for a while.</span></span> <span data-ttu-id="cc391-104">Dans la plupart des cas, le dernier courrier électronique sur le thread inclura le contenu de tous les messages électroniques précédents ; en examinant le dernier courrier électronique, vous obtiendrez un contexte complet de la conversation qui s’est produite dans le fil de discussion.</span><span class="sxs-lookup"><span data-stu-id="cc391-104">In most cases, the last email on the thread will include the contents of all the preceding emails; reviewing the last email will give a complete context of the conversation that happened in the thread.</span></span> <span data-ttu-id="cc391-105">Le Threading de messagerie identifie ces messages afin que les réviseurs puissent examiner une partie des documents collectés sans perdre de contexte.</span><span class="sxs-lookup"><span data-stu-id="cc391-105">Email threading identifies such emails so that reviewers can review a fraction of collected documents without losing any context.</span></span>

## <a name="what-does-email-threading-do"></a><span data-ttu-id="cc391-106">Qu’est-ce que le Threading du courrier électronique ?</span><span class="sxs-lookup"><span data-stu-id="cc391-106">What does email threading do?</span></span>

<span data-ttu-id="cc391-107">Le Threading de messagerie analyse chaque message électronique et les desconstructs à des messages individuels ; chaque message électronique est une chaîne de messages individuels.</span><span class="sxs-lookup"><span data-stu-id="cc391-107">Email threading parses each email and desconstructs it to individual messages; each email is a chain of individual messages.</span></span> <span data-ttu-id="cc391-108">Ensuite, il analyse tous les messages électroniques du jeu de travail afin de déterminer si un e-mail a un contenu unique ou si la chaîne est entièrement contenue dans un autre message électronique.</span><span class="sxs-lookup"><span data-stu-id="cc391-108">Then, it analyzes all emails in the working set to determine whether an email has unique content or if the chain is wholly contained in a different email.</span></span> <span data-ttu-id="cc391-109">Dans les messages électroniques finaux se répartissent en quatre catégories :</span><span class="sxs-lookup"><span data-stu-id="cc391-109">In the end emails are divided into four categories:</span></span>

- <span data-ttu-id="cc391-110">**Inclus**: le dernier message de l’e-mail a un contenu unique, et le courrier électronique contient toutes les pièces jointes incluses dans d’autres messages électroniques dont le contenu est entièrement contenu dans cet e-mail.</span><span class="sxs-lookup"><span data-stu-id="cc391-110">**Inclusive**: the last message in the email has unique content, and the email has all of the attachments that were included in other emails of which the content is wholly contained in this email.</span></span>


- <span data-ttu-id="cc391-111">**Inclusif**: le dernier message de l’e-mail a un contenu unique, mais le courrier électronique ne contient pas certaines pièces jointes incluses dans d’autres messages électroniques dont le contenu est entièrement contenu dans ce message électronique.</span><span class="sxs-lookup"><span data-stu-id="cc391-111">**Inclusive minus**: the last message in the email has unique content, but the email does not contain some of the attachments that were included in other emails of which the content is wholly contained in this email.</span></span>

- <span data-ttu-id="cc391-112">**Copie inclusive**: une copie exacte d’un message électronique inclusif/inclusif</span><span class="sxs-lookup"><span data-stu-id="cc391-112">**Inclusive copy**: an exact copy of an inclusive/inclusive minus email</span></span>

- <span data-ttu-id="cc391-113">**None**: le contenu de ce message électronique est entièrement contenu dans au moins un e-mail marqué comme inclusif/inclusif.</span><span class="sxs-lookup"><span data-stu-id="cc391-113">**None**: The content of this email is wholly contained in at least one email that is marked as inclusive/inclusive minus.</span></span>

## <a name="how-is-it-different-from-conversations-in-outlook"></a><span data-ttu-id="cc391-114">Quelle est la différence entre les conversations dans Outlook ?</span><span class="sxs-lookup"><span data-stu-id="cc391-114">How is it different from conversations in Outlook?</span></span>
<span data-ttu-id="cc391-115">En un clin d’œil, cela semble très semblable aux groupements de conversation dans Outlook.</span><span class="sxs-lookup"><span data-stu-id="cc391-115">At a glance, this sounds very similar to conversation groupings in Outlook.</span></span> <span data-ttu-id="cc391-116">Toutefois, il existe des distinctions importantes.</span><span class="sxs-lookup"><span data-stu-id="cc391-116">However, there are some important distinctions.</span></span> <span data-ttu-id="cc391-117">Considérez une conversation par courrier électronique qui a été divisée en deux conversations ; par exemple, quelqu’un a répondu à un message électronique qui n’est pas le dernier de la conversation, les deux derniers messages de la conversation ont un contenu unique.</span><span class="sxs-lookup"><span data-stu-id="cc391-117">Consider an email conversation that got forked into two conversation; for instance, someone responded to an email that is not the latest in the conversation so the last two emails in the conversation both have unique content.</span></span>

<span data-ttu-id="cc391-118">Outlook regroupera les messages électroniques en une seule conversation ; la lecture du dernier courrier électronique ne signifie pas qu’il manque le contexte de l’avant-dernier e-mail, qui contient également du contenu unique.</span><span class="sxs-lookup"><span data-stu-id="cc391-118">Outlook would still group the emails into a single conversation; reading only the last email would mean missing the context of the second-to-last email, which also contains unique content.</span></span> <span data-ttu-id="cc391-119">Étant donné que le Threading de messagerie analyse chaque courrier électronique dans des composants individuels et les compare, le Threading de courrier électronique marque les deux derniers courriers électroniques comme étant inclusifs, ce qui vous permettra de ne pas manquer de contexte tant que vous lisez tous les messages électroniques marqués comme inclus.</span><span class="sxs-lookup"><span data-stu-id="cc391-119">Because email threading parses out each email into individual components and compares them, email threading would mark both of the last two emails as inclusives, ensuring that you won't miss any context as long as you read all emails marked as inclusive.</span></span>
