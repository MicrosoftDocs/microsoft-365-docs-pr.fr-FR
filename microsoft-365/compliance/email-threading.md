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
ms.openlocfilehash: 6cc466bf89187f292acd454fd8ca6efb05958d2b
ms.sourcegitcommit: a45cf8b887587a1810caf9afa354638e68ec5243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/05/2020
ms.locfileid: "44035656"
---
# <a name="email-threading"></a><span data-ttu-id="b1b58-103">Threading de messagerie</span><span class="sxs-lookup"><span data-stu-id="b1b58-103">Email threading</span></span>

<span data-ttu-id="b1b58-104">Considérez une conversation par courrier électronique qui s’est en cours pendant un certain temps.</span><span class="sxs-lookup"><span data-stu-id="b1b58-104">Consider an email conversation that has been going on for a while.</span></span> <span data-ttu-id="b1b58-105">Dans la plupart des cas, le dernier courrier électronique sur le thread inclura le contenu de tous les messages électroniques précédents ; en examinant le dernier courrier électronique, vous obtiendrez un contexte complet de la conversation qui s’est produite dans le fil de discussion.</span><span class="sxs-lookup"><span data-stu-id="b1b58-105">In most cases, the last email on the thread will include the contents of all the preceding emails; reviewing the last email will give a complete context of the conversation that happened in the thread.</span></span> <span data-ttu-id="b1b58-106">Le Threading de messagerie identifie ces messages afin que les réviseurs puissent examiner une partie des documents collectés sans perdre de contexte.</span><span class="sxs-lookup"><span data-stu-id="b1b58-106">Email threading identifies such emails so that reviewers can review a fraction of collected documents without losing any context.</span></span>

## <a name="what-does-email-threading-do"></a><span data-ttu-id="b1b58-107">Qu’est-ce que le Threading du courrier électronique ?</span><span class="sxs-lookup"><span data-stu-id="b1b58-107">What does email threading do?</span></span>

<span data-ttu-id="b1b58-108">Le Threading de messagerie analyse chaque message électronique et les desconstructs à des messages individuels ; chaque message électronique est une chaîne de messages individuels.</span><span class="sxs-lookup"><span data-stu-id="b1b58-108">Email threading parses each email and desconstructs it to individual messages; each email is a chain of individual messages.</span></span> <span data-ttu-id="b1b58-109">Ensuite, il analyse tous les messages électroniques du jeu de travail afin de déterminer si un e-mail a un contenu unique ou si la chaîne est entièrement contenue dans un autre message électronique.</span><span class="sxs-lookup"><span data-stu-id="b1b58-109">Then, it analyzes all emails in the working set to determine whether an email has unique content or if the chain is wholly contained in a different email.</span></span> <span data-ttu-id="b1b58-110">Dans les messages électroniques finaux se répartissent en quatre catégories :</span><span class="sxs-lookup"><span data-stu-id="b1b58-110">In the end emails are divided into four categories:</span></span>

- <span data-ttu-id="b1b58-111">**Inclus**: le dernier message de l’e-mail a un contenu unique, et le courrier électronique contient toutes les pièces jointes incluses dans d’autres messages électroniques dont le contenu est entièrement contenu dans cet e-mail.</span><span class="sxs-lookup"><span data-stu-id="b1b58-111">**Inclusive**: the last message in the email has unique content, and the email has all of the attachments that were included in other emails of which the content is wholly contained in this email.</span></span>


- <span data-ttu-id="b1b58-112">**Inclusif**: le dernier message de l’e-mail a un contenu unique, mais le courrier électronique ne contient pas certaines pièces jointes incluses dans d’autres messages électroniques dont le contenu est entièrement contenu dans ce message électronique.</span><span class="sxs-lookup"><span data-stu-id="b1b58-112">**Inclusive minus**: the last message in the email has unique content, but the email does not contain some of the attachments that were included in other emails of which the content is wholly contained in this email.</span></span>

- <span data-ttu-id="b1b58-113">**Copie inclusive**: une copie exacte d’un message électronique inclusif/inclusif</span><span class="sxs-lookup"><span data-stu-id="b1b58-113">**Inclusive copy**: an exact copy of an inclusive/inclusive minus email</span></span>

- <span data-ttu-id="b1b58-114">**None**: le contenu de ce message électronique est entièrement contenu dans au moins un e-mail marqué comme inclusif/inclusif.</span><span class="sxs-lookup"><span data-stu-id="b1b58-114">**None**: The content of this email is wholly contained in at least one email that is marked as inclusive/inclusive minus.</span></span>

## <a name="how-is-it-different-from-conversations-in-outlook"></a><span data-ttu-id="b1b58-115">Quelle est la différence entre les conversations dans Outlook ?</span><span class="sxs-lookup"><span data-stu-id="b1b58-115">How is it different from conversations in Outlook?</span></span>
<span data-ttu-id="b1b58-116">En un clin d’œil, cela semble très semblable aux groupements de conversation dans Outlook.</span><span class="sxs-lookup"><span data-stu-id="b1b58-116">At a glance, this sounds very similar to conversation groupings in Outlook.</span></span> <span data-ttu-id="b1b58-117">Toutefois, il existe des distinctions importantes.</span><span class="sxs-lookup"><span data-stu-id="b1b58-117">However, there are some important distinctions.</span></span> <span data-ttu-id="b1b58-118">Considérez une conversation par courrier électronique qui a été divisée en deux conversations ; par exemple, quelqu’un a répondu à un message électronique qui n’est pas le dernier de la conversation, les deux derniers messages de la conversation ont un contenu unique.</span><span class="sxs-lookup"><span data-stu-id="b1b58-118">Consider an email conversation that got forked into two conversation; for instance, someone responded to an email that is not the latest in the conversation so the last two emails in the conversation both have unique content.</span></span>

<span data-ttu-id="b1b58-119">Outlook regroupera les messages électroniques en une seule conversation ; la lecture du dernier courrier électronique ne signifie pas qu’il manque le contexte de l’avant-dernier e-mail, qui contient également du contenu unique.</span><span class="sxs-lookup"><span data-stu-id="b1b58-119">Outlook would still group the emails into a single conversation; reading only the last email would mean missing the context of the second-to-last email, which also contains unique content.</span></span> <span data-ttu-id="b1b58-120">Étant donné que le Threading de messagerie analyse chaque courrier électronique dans des composants individuels et les compare, le Threading de courrier électronique marque les deux derniers courriers électroniques comme étant inclusifs, ce qui vous permettra de ne pas manquer de contexte tant que vous lisez tous les messages électroniques marqués comme inclus.</span><span class="sxs-lookup"><span data-stu-id="b1b58-120">Because email threading parses out each email into individual components and compares them, email threading would mark both of the last two emails as inclusives, ensuring that you won't miss any context as long as you read all emails marked as inclusive.</span></span>
