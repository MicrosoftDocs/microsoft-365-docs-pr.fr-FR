---
title: Supprimer un ancien employé - Vue d’ensemble
f1.keywords:
- NOCSH
ms.author: kwekua
author: kwekua
manager: scotv
audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
ms.collection:
- M365-subscription-management
- Adm_O365
- Adm_TOC
- SPO_Content
ms.custom:
- MSStore_Link
- TRN_M365B
- OKR_SMB_Videos
- AdminSurgePortfolio
search.appverid:
- BCS160
- MET150
- MOE150
description: Suivez les étapes de cette solution pour supprimer un ancien employé de Microsoft 365 et sécuriser les données de votre organisation.
ms.openlocfilehash: 4b4cf59fdce81b3098ee333095daa8e1af1cd5c5
ms.sourcegitcommit: ff20f5b4e3268c7c98a84fb1cbe7db7151596b6d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/06/2021
ms.locfileid: "52241735"
---
# <a name="overview-remove-a-former-employee-and-secure-data"></a><span data-ttu-id="b3cae-103">Vue d’ensemble : supprimer un ancien employé et sécuriser les données</span><span class="sxs-lookup"><span data-stu-id="b3cae-103">Overview: Remove a former employee and secure data</span></span>

<span data-ttu-id="b3cae-104">Nous avons souvent la question suivante : « Que dois-je faire pour sécuriser les données et protéger l’accès lorsqu’un employé quitte mon organisation ? »</span><span class="sxs-lookup"><span data-stu-id="b3cae-104">A question we often get is, "What should I do to secure data and protect access when an employee leaves my organization?"</span></span> <span data-ttu-id="b3cae-105">Cette série d’articles explique comment bloquer l’accès à Microsoft 365, les étapes à suivre pour sécuriser vos données et comment autoriser d’autres employés à accéder aux données.</span><span class="sxs-lookup"><span data-stu-id="b3cae-105">This article series explains how to block access to Microsoft 365, the steps you should take to secure your data, and how to allow other employees to access the data.</span></span>

<span data-ttu-id="b3cae-106">Regardez une courte vidéo sur la suppression d’un employé.</span><span class="sxs-lookup"><span data-stu-id="b3cae-106">Watch a short video about removing an employee.</span></span> <br><br>

> [!VIDEO https://www.microsoft.com/videoplayer/embed/RE1FOfR] 

<span data-ttu-id="b3cae-107">Si vous avez trouvé cette vidéo utile, consultez les [séries de formations complètes pour les petites entreprises et les nouveaux utilisateurs de Microsoft 365](../../business-video/index.yml).</span><span class="sxs-lookup"><span data-stu-id="b3cae-107">If you found this video helpful, check out the [complete training series for small businesses and those new to Microsoft 365](../../business-video/index.yml).</span></span>

<span data-ttu-id="b3cae-108">Pour empêcher un employé de se connecter :</span><span class="sxs-lookup"><span data-stu-id="b3cae-108">To prevent an employee from logging in:</span></span>

1. <span data-ttu-id="b3cae-109">Dans le Centre d’administration, accédez à la page **Utilisateurs** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=834822" target="_blank">Utilisateurs actifs</a>.</span><span class="sxs-lookup"><span data-stu-id="b3cae-109">In the admin center, go to the **Users** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=834822" target="_blank">Active users</a> page.</span></span>
2. <span data-ttu-id="b3cae-110">Sélectionnez la case à côté du nom de l’utilisateur, puis sélectionnez **Réinitialiser le mot de passe.**</span><span class="sxs-lookup"><span data-stu-id="b3cae-110">Select the box next to the user's name, and then select **Reset password**.</span></span>
3. <span data-ttu-id="b3cae-111">Entrez un nouveau mot de passe, puis sélectionnez **Réinitialiser.**</span><span class="sxs-lookup"><span data-stu-id="b3cae-111">Enter a new password, and then select **Reset**.</span></span> <span data-ttu-id="b3cae-112">(Ne leur envoyez pas de message.)</span><span class="sxs-lookup"><span data-stu-id="b3cae-112">(Don't send it to them.)</span></span>
4. <span data-ttu-id="b3cae-113">Sélectionnez le nom de l’utilisateur pour aller  dans le volet de propriétés, puis sous l’onglet Compte, sélectionnez Lancer **la signature.**</span><span class="sxs-lookup"><span data-stu-id="b3cae-113">Select the user's name to go to their properties pane, and on the **Account** tab, select **Initiate sign-out**.</span></span>

> [!NOTE]
> <span data-ttu-id="b3cae-114">Vous devez être un administrateur général pour lancer la signature.</span><span class="sxs-lookup"><span data-stu-id="b3cae-114">You need to be a global administrator to initiate sign-out.</span></span>

<span data-ttu-id="b3cae-115">Dans l’heure qui s’affiche( ou après avoir quitté la page de Microsoft 365 en cours), ils sont invités à se ré-inscrire.</span><span class="sxs-lookup"><span data-stu-id="b3cae-115">Within an hour - or after they leave the current Microsoft 365 page they are on - they're prompted to sign in again.</span></span> <span data-ttu-id="b3cae-116">Un jeton d’accès est bon pendant une heure, donc la chronologie dépend du temps qui reste sur ce jeton et de la façon dont il quitte la page web actuelle.</span><span class="sxs-lookup"><span data-stu-id="b3cae-116">An access token is good for an hour, so the timeline depends on how much time is left on that token, and whether they navigate out of their current webpage.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="b3cae-117">Même si nous avons numéroé les étapes de cette solution et que vous n’avez pas besoin d’effectuer la solution dans l’ordre exact, nous vous recommandons d’effectuer les étapes de cette façon.</span><span class="sxs-lookup"><span data-stu-id="b3cae-117">Although we've numbered the steps in this solution and you don't have to complete the solution using the exact order, we do recommend doing the steps this way.</span></span>

## <a name="before-you-begin"></a><span data-ttu-id="b3cae-118">Avant de commencer</span><span class="sxs-lookup"><span data-stu-id="b3cae-118">Before you begin</span></span>

<span data-ttu-id="b3cae-119">Vous devez être administrateur général pour effectuer les étapes de cette solution.</span><span class="sxs-lookup"><span data-stu-id="b3cae-119">You need to be a global administrator to complete the steps in this solution.</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="b3cae-120">**Étape**</span><span class="sxs-lookup"><span data-stu-id="b3cae-120">**Step**</span></span> <br/> |<span data-ttu-id="b3cae-121">**Raison**</span><span class="sxs-lookup"><span data-stu-id="b3cae-121">**Why do this**</span></span> <br/> |
|[<span data-ttu-id="b3cae-122">Étape 1 : empêcher un ancien employé de se connecter et bloquer l’accès Microsoft 365 services</span><span class="sxs-lookup"><span data-stu-id="b3cae-122">Step 1 - Prevent a former employee from logging in and block access to Microsoft 365 services</span></span>](remove-former-employee-step-1.md) <br/> |<span data-ttu-id="b3cae-123">Cela empêche votre ancien employé de se connecter à Microsoft 365 et empêche la personne d’accéder Microsoft 365 services.</span><span class="sxs-lookup"><span data-stu-id="b3cae-123">This blocks your former employee from logging in to Microsoft 365 and prevents the person from accessing Microsoft 365 services.</span></span> <br/> |
|[<span data-ttu-id="b3cae-124">Étape 2 : enregistrer le contenu de la boîte aux lettres d’un ancien employé</span><span class="sxs-lookup"><span data-stu-id="b3cae-124">Step 2 - Save the contents of a former employee's mailbox</span></span>](remove-former-employee-step-2.md) <br/> |<span data-ttu-id="b3cae-125">Cela est utile pour la personne qui va reprendre le travail de l’employé, ou en cas de litige.</span><span class="sxs-lookup"><span data-stu-id="b3cae-125">This is useful for the person who is going to take over the employee's work, or if there is litigation.</span></span> <br/> |
|[<span data-ttu-id="b3cae-126">Étape 3 : Forward a former employee’s email to another employee or convert to a shared mailbox</span><span class="sxs-lookup"><span data-stu-id="b3cae-126">Step 3 - Forward a former employee's email to another employee or convert to a shared mailbox</span></span>](remove-former-employee-step-3.md) <br/> |<span data-ttu-id="b3cae-p104">Cette étape vous permet de conserver l'adresse e-mail de l'ancien employé. Si certains de vos clients ou partenaires continuent d'envoyer du courrier à l'adresse de l'ancien employé, celui-ci est reçu par son remplaçant.</span><span class="sxs-lookup"><span data-stu-id="b3cae-p104">This lets you keep the former employee's email address active. If you have customers or partners still sending email to the former employee's address, this gets them to the person taking over the work.</span></span> <br/> |
|[<span data-ttu-id="b3cae-129">Étape 4 : donner à un autre employé l’accès OneDrive données Outlook données</span><span class="sxs-lookup"><span data-stu-id="b3cae-129">Step 4 - Give another employee access to OneDrive and Outlook data</span></span>](remove-former-employee-step-6.md) <br/> |<span data-ttu-id="b3cae-130">Si vous supprimez uniquement la licence d'un utilisateur, mais pas le compte, vous pouvez toujours accéder au contenu enregistré dans l'espace OneDrive de l'utilisateur même après 30 jours.</span><span class="sxs-lookup"><span data-stu-id="b3cae-130">If you only remove a user's license but don't delete the account, the content in the user's OneDrive will remain accessible to you even after 30 days.</span></span> <br/><br/> <span data-ttu-id="b3cae-131">Avant de supprimer le compte, vous devez accorder l’accès à ses OneDrive et Outlook à un autre utilisateur.</span><span class="sxs-lookup"><span data-stu-id="b3cae-131">Before you delete the account, you should give access of their OneDrive and Outlook to another user.</span></span> <span data-ttu-id="b3cae-132">Après avoir supprimé le compte d’un employé, le contenu de ses OneDrive et Outlook est conservé **pendant 30** jours.</span><span class="sxs-lookup"><span data-stu-id="b3cae-132">After you delete an employee's account, the content in their OneDrive and Outlook is retained for **30** days.</span></span> <span data-ttu-id="b3cae-133">Toutefois, pendant ces 30 jours, vous pouvez restaurer le compte de l’utilisateur et accéder à son contenu.</span><span class="sxs-lookup"><span data-stu-id="b3cae-133">During that 30 days, however, you can restore the user's account, and gain access to their content.</span></span> <span data-ttu-id="b3cae-134">Si vous restituer le compte de l’utilisateur, les OneDrive et Outlook restent accessibles même après 30 jours.</span><span class="sxs-lookup"><span data-stu-id="b3cae-134">If you restore the user's account, the OneDrive and Outlook content will remain accessible to you even after 30 days.</span></span> <br/> |
|[<span data-ttu-id="b3cae-135">Étape 5 : effacer et bloquer l’appareil mobile d’un ancien employé</span><span class="sxs-lookup"><span data-stu-id="b3cae-135">Step 5 - Wipe and block a former employee's mobile device</span></span>](remove-former-employee-step-4.md) <br/> |<span data-ttu-id="b3cae-136">Cette étape supprime vos données professionnelles du téléphone ou de la tablette.</span><span class="sxs-lookup"><span data-stu-id="b3cae-136">Removes your business data from the phone or tablet.</span></span>  <br/> |
|[<span data-ttu-id="b3cae-137">Étape 6 : Supprimer et supprimer la licence Microsoft 365 d’un ancien employé</span><span class="sxs-lookup"><span data-stu-id="b3cae-137">Step 6 - Remove and delete the Microsoft 365 license from a former employee</span></span>](remove-former-employee-step-7.md) <br/> |<span data-ttu-id="b3cae-p106">Si vous retirez une licence, vous pouvez l'affecter à quelqu'un d'autre. Vous pouvez également supprimer la licence pour ne plus payer pour celle-ci jusqu'à ce que vous embauchiez une autre personne.  </span><span class="sxs-lookup"><span data-stu-id="b3cae-p106">When you remove a license, you can assign it to someone else. Or, you can delete the license so you don't pay for it until you hire another person. </span></span><br/><br/> <span data-ttu-id="b3cae-p107">Lorsque vous retirez ou supprimez une licence, les anciens courriers, les contacts et le calendrier de l'utilisateur sont conservés pendant **30 jours** avant d'être supprimés définitivement. Si vous retirez ou supprimez une licence, mais pas le compte, vous pouvez toujours accéder au contenu enregistré dans l'espace OneDrive de l'utilisateur même après 30 jours.  </span><span class="sxs-lookup"><span data-stu-id="b3cae-p107">When you remove or delete a license, the user's old email, contacts, and calendar are retained for **30 days**, then permanently deleted. If you remove or delete a license but don't delete the account, the content in the user's OneDrive will remain accessible to you even after 30 days.  </span></span><br/> |
|[<span data-ttu-id="b3cae-142">Étape 7 : supprimer le compte d’utilisateur d’un ancien employé</span><span class="sxs-lookup"><span data-stu-id="b3cae-142">Step 7 - Delete a former employee's user account</span></span>](remove-former-employee-step-7.md) <br/> |<span data-ttu-id="b3cae-143">Cela supprime le compte de votre centre d’administration.</span><span class="sxs-lookup"><span data-stu-id="b3cae-143">This removes the account from your admin center.</span></span> <span data-ttu-id="b3cae-144">Ainsi, les choses restent claires et bien organisées.</span><span class="sxs-lookup"><span data-stu-id="b3cae-144">Keeps things clean.</span></span> <br/> |

## <a name="related-articles"></a><span data-ttu-id="b3cae-145">Articles connexes</span><span class="sxs-lookup"><span data-stu-id="b3cae-145">Related articles</span></span>

[<span data-ttu-id="b3cae-146">Restaurer un utilisateur</span><span class="sxs-lookup"><span data-stu-id="b3cae-146">Restore a user</span></span>](restore-user.md)
