---
title: Threads de messagerie dans Advanced eDiscovery
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
description: Lors de la conduite d’une analyse advanced eDiscovery, le thread de messagerie analyse une conversation par courrier électronique et sépare chaque message en différentes catégories.
ms.custom: seo-marvel-mar2020
ms.openlocfilehash: b087bfc84175f80daaf1c0d2f1394584a70757ac
ms.sourcegitcommit: 2160e7cf373f992dd4d11793a59cb8c44f8d587e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/26/2020
ms.locfileid: "48285560"
---
# <a name="email-threading-in-advanced-ediscovery"></a><span data-ttu-id="e9c07-103">Threads de messagerie dans Advanced eDiscovery</span><span class="sxs-lookup"><span data-stu-id="e9c07-103">Email threading in Advanced eDiscovery</span></span>

<span data-ttu-id="e9c07-104">Envisagez une conversation par courrier électronique qui se passe depuis un certain temps.</span><span class="sxs-lookup"><span data-stu-id="e9c07-104">Consider an email conversation that has been going on for a while.</span></span> <span data-ttu-id="e9c07-105">Dans la plupart des cas, le dernier e-mail sur le thread inclut le contenu de tous les e-mails précédents ; La révision du dernier e-mail donne un contexte complet de la conversation qui s’est produite dans le thread.</span><span class="sxs-lookup"><span data-stu-id="e9c07-105">In most cases, the last email on the thread will include the contents of all the preceding emails; reviewing the last email will give a complete context of the conversation that happened in the thread.</span></span> <span data-ttu-id="e9c07-106">Le thread de messagerie identifie ces e-mails afin que les réviseurs peuvent passer en revue une fraction des documents collectés sans perdre de contexte.</span><span class="sxs-lookup"><span data-stu-id="e9c07-106">Email threading identifies such emails so that reviewers can review a fraction of collected documents without losing any context.</span></span>

## <a name="what-does-email-threading-do"></a><span data-ttu-id="e9c07-107">Que fait le thread de messagerie ?</span><span class="sxs-lookup"><span data-stu-id="e9c07-107">What does email threading do?</span></span>

<span data-ttu-id="e9c07-108">Le thread de courrier électronique pare chaque e-mail et le déconstruit en messages individuels . chaque e-mail est une chaîne de messages individuels.</span><span class="sxs-lookup"><span data-stu-id="e9c07-108">Email threading parses each email and deconstructs it to individual messages; each email is a chain of individual messages.</span></span> <span data-ttu-id="e9c07-109">Ensuite, il analyse tous les e-mails du jeu à réviser pour déterminer si un e-mail a un contenu unique ou si la chaîne est entièrement contenue dans un autre e-mail.</span><span class="sxs-lookup"><span data-stu-id="e9c07-109">Then, it analyzes all emails in the review set to determine whether an email has unique content or if the chain is wholly contained in a different email.</span></span> <span data-ttu-id="e9c07-110">Au final, les courriers électroniques sont répartis en quatre catégories :</span><span class="sxs-lookup"><span data-stu-id="e9c07-110">In the end emails are divided into four categories:</span></span>

- <span data-ttu-id="e9c07-111">**Conversation complète** : le dernier message présente un contenu unique. Le courrier inclut toutes les pièces jointes ajoutées aux autres messages dont le contenu est entièrement disponible dans ce courrier.</span><span class="sxs-lookup"><span data-stu-id="e9c07-111">**Inclusive**: the last message in the email has unique content, and the email has all of the attachments that were included in other emails of which the content is wholly contained in this email.</span></span>

- <span data-ttu-id="e9c07-112">**Conversation complète moins pièce jointe** : le dernier message présente un contenu unique. Toutefois, le courrier n’inclut pas certaines pièces jointes ajoutées aux autres messages dont le contenu est entièrement disponible dans ce courrier.</span><span class="sxs-lookup"><span data-stu-id="e9c07-112">**Inclusive minus**: the last message in the email has unique content, but the email does not contain some of the attachments that were included in other emails of which the content is wholly contained in this email.</span></span>

- <span data-ttu-id="e9c07-113">**Copie complète** : copie exacte d’une conversation complète ou conversation complète moins pièce jointe.</span><span class="sxs-lookup"><span data-stu-id="e9c07-113">**Inclusive copy**: an exact copy of an inclusive/inclusive minus email</span></span>

- <span data-ttu-id="e9c07-114">**Aucune** : le contenu du message est inclus entièrement dans au moins un courrier marqué comme conversation complète ou conversation complète moins pièce jointe.</span><span class="sxs-lookup"><span data-stu-id="e9c07-114">**None**: The content of this email is wholly contained in at least one email that is marked as inclusive/inclusive minus.</span></span>

## <a name="how-is-it-different-from-conversations-in-outlook"></a><span data-ttu-id="e9c07-115">En quoi cela est-il différent des conversations dans Outlook ?</span><span class="sxs-lookup"><span data-stu-id="e9c07-115">How is it different from conversations in Outlook?</span></span>

<span data-ttu-id="e9c07-116">En un coup d’œil, cela ressemble aux regroupements de conversation dans Outlook.</span><span class="sxs-lookup"><span data-stu-id="e9c07-116">At a glance, this sounds similar to conversation groupings in Outlook.</span></span> <span data-ttu-id="e9c07-117">Toutefois, il existe certaines distinctions importantes.</span><span class="sxs-lookup"><span data-stu-id="e9c07-117">However, there are some important distinctions.</span></span> <span data-ttu-id="e9c07-118">Envisagez une conversation par courrier électronique qui a été transformée en deux conversations ; Par exemple, quelqu’un a répondu à un e-mail qui n’est pas le dernier de la conversation, de sorte que les deux derniers e-mails de la conversation ont tous deux un contenu unique.</span><span class="sxs-lookup"><span data-stu-id="e9c07-118">Consider an email conversation that got forked into two conversations; for instance, someone responded to an email that is not the latest in the conversation so the last two emails in the conversation both have unique content.</span></span>

<span data-ttu-id="e9c07-119">Outlook grouperait toujours les e-mails dans une seule conversation . Lire uniquement le dernier e-mail signifierait qu’il manque le contexte de l’avant-dernier e-mail, qui contient également un contenu unique.</span><span class="sxs-lookup"><span data-stu-id="e9c07-119">Outlook would still group the emails into a single conversation; reading only the last email would mean missing the context of the second-to-last email, which also contains unique content.</span></span> <span data-ttu-id="e9c07-120">Étant donné que le thread de courrier électronique pare chaque message électronique en composants individuels et les compare, le thread de messagerie marque les deux derniers messages comme étant inclus, ce qui garantit que vous ne manquez aucun contexte tant que vous lisez tous les messages marqués comme étant inclus.</span><span class="sxs-lookup"><span data-stu-id="e9c07-120">Because email threading parses out each email into individual components and compares them, email threading would mark both of the last two emails as inclusive, ensuring that you won't miss any context as long as you read all emails marked as inclusive.</span></span>
