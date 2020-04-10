---
title: Liens fiables Office 365 ATP pour Teams, safelinks, les liens fiables, bloquer les liens malveillants, Office 365 ATP, teams de liens approuvés, empêcher les utilisateurs de cliquer sur liens incorrects, liens malveillants
ms.author: tracyp
author: MSFTTracyP
manager: dansimp
audience: Admin
ms.date: 02/28/2020
ms.topic: overview
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.collection:
- M365-security-compliance
description: Les équipes auront désormais accès à des liens fiables au moment de votre clic. Que vous utilisiez des conversations de conversation 1-on-1, entre des groupes ou des canaux, et des onglets, si vous disposez d’un abonnement à la protection avancée contre les menaces pour Office 365, vous pouvez activer et utiliser cette fonctionnalité de sécurité.
ms.openlocfilehash: 49a49bd41e71daf0afc9e7a24e79898ff98ad798
ms.sourcegitcommit: 4a34b48584071e0c43c920bb35025e34cb4f5d15
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/09/2020
ms.locfileid: "43212544"
---
<!--06/21/2019-->

# <a name="office-365-safe-links-in-teams"></a><span data-ttu-id="e4c85-104">Liens approuvés Office 365 dans teams</span><span class="sxs-lookup"><span data-stu-id="e4c85-104">Office 365 Safe Links in Teams</span></span>

> [!IMPORTANT]
> <span data-ttu-id="e4c85-105">Cette fonctionnalité est en préversion **publique** pour les clients du programme d’adoption de la technologie Microsoft Teams (TAP) du 28 février 2020.</span><span class="sxs-lookup"><span data-stu-id="e4c85-105">This feature is in **Public Preview** for customers in the Microsoft Teams Technology Adoption Program (TAP) as of Feb 28, 2020.</span></span> <span data-ttu-id="e4c85-106">Cette note sera supprimée de l’article lorsque les liens fiables de teams sont plus largement disponibles.</span><span class="sxs-lookup"><span data-stu-id="e4c85-106">This note will be removed from the article when Safe Links for Teams is more widely available.</span></span>

<span data-ttu-id="e4c85-107">Microsoft Teams, une application Cloud Office 365 pour la gestion de votre travail, utilise déjà des pièces jointes fiables (pour Office 365), mais il aura maintenant accès à des liens fiables au moment de votre clic.</span><span class="sxs-lookup"><span data-stu-id="e4c85-107">Microsoft Teams, an Office 365 Cloud-based application for managing your work, already uses safe attachments (for Office 365), but it will now have access to safe links at the time of your click.</span></span> <span data-ttu-id="e4c85-108">Que vous utilisiez des conversations de conversation 1-on-1, entre des groupes ou des canaux, et des onglets, si vous disposez d’un abonnement à la protection avancée contre les menaces pour Office 365, vous pouvez activer et utiliser cette mesure de sécurité.</span><span class="sxs-lookup"><span data-stu-id="e4c85-108">Whether you're using chats 1-on-1 Chats, between Groups, or in Channels, and Tabs, if you have a subscription to Office 365 ATP, you will have the ability to enable and use this safety measure.</span></span>

<span data-ttu-id="e4c85-109">Voici le principe de fonctionnement :</span><span class="sxs-lookup"><span data-stu-id="e4c85-109">Here's how it works:</span></span> 

1. <span data-ttu-id="e4c85-110">Lorsque vous démarrez l’application Teams, Office 365 vérifie que l’utilisateur appartient à une organisation disposant d’Office 365 ATP et que l’utilisateur fait partie d’une stratégie de liens approuvés active avec sa protection activée pour Microsoft Teams.</span><span class="sxs-lookup"><span data-stu-id="e4c85-110">When you start the Teams application, Office 365 will check to make sure the user belongs to an organization that has Office 365 ATP, and that the user is part of an active safe links policy with its protection enabled for Microsoft Teams.</span></span>

2. <span data-ttu-id="e4c85-111">Si les éléments ci-dessus sont vrais, les URL seront validées au moment du clic dans les conversations, les conversations de groupe, les canaux et dans les onglets pour cet utilisateur.</span><span class="sxs-lookup"><span data-stu-id="e4c85-111">If the above are true, then URLs will be validated at the time of click in Chats, Group Chats, Channels, and in Tabs for that user.</span></span>

> [!NOTE]
> <span data-ttu-id="e4c85-112">Les liens fiables protègent les utilisateurs des liens envoyés par des utilisateurs invités, des utilisateurs fédérés, des utilisateurs clients.</span><span class="sxs-lookup"><span data-stu-id="e4c85-112">Safe links safeguards users from links sent by Guest users, Federated users, tenant users.</span></span> <span data-ttu-id="e4c85-113">Si l’utilisateur connecté dispose de liens fiables pour les équipes activées, les protections de liens fiables s’appliquent.</span><span class="sxs-lookup"><span data-stu-id="e4c85-113">If the user logged in has safe links for Teams enabled, then safe links protections will apply.</span></span>
 
## <a name="what-will-users-experience"></a><span data-ttu-id="e4c85-114">Qu’est-ce que les utilisateurs peuvent expérimenter ?</span><span class="sxs-lookup"><span data-stu-id="e4c85-114">What will users experience?</span></span> 

<span data-ttu-id="e4c85-115">Tous les utilisateurs protégés bénéficieront de cette expérience avec des URL dangereuses :</span><span class="sxs-lookup"><span data-stu-id="e4c85-115">All protected users will have this experience with hazardous URLs:</span></span> 

- <span data-ttu-id="e4c85-116">Si vous avez cliqué sur le lien d’une conversation Teams, d’une conversation de groupe ou de canaux, une page s’affiche dans le navigateur par défaut.</span><span class="sxs-lookup"><span data-stu-id="e4c85-116">If the link was clicked from a Teams conversation, group chat, or from channels, a page will render in the default browser.</span></span> <span data-ttu-id="e4c85-117">Si vous avez cliqué sur le lien à partir d’un onglet épinglé, la page s’affiche dans l’interface utilisateur de teams sous cet onglet, et l’option d’ouverture dans le navigateur est désactivée pour des raisons de sécurité.</span><span class="sxs-lookup"><span data-stu-id="e4c85-117">If the link was clicked from a pinned tab, the page will appear in the Teams GUI within that tab, and the option to open in browser will be disabled for security purposes.</span></span>

- <span data-ttu-id="e4c85-118">Cet utilisateur ne pourra pas continuer à passer sur le site de l’URL.</span><span class="sxs-lookup"><span data-stu-id="e4c85-118">This user will be blocked from proceeding to the URL's site.</span></span>

<span data-ttu-id="e4c85-119">Si l’utilisateur qui a envoyé le lien n’est pas protégé par la protection avancée contre les menaces d’Office 365, il est libre de cliquer sur l’URL sur son ordinateur et de résoudre le problème.</span><span class="sxs-lookup"><span data-stu-id="e4c85-119">If the user who sent the link isn't protected by Office 365 ATP, he or she is free to click the URL on his or her machine and resolve the problem site.</span></span> <span data-ttu-id="e4c85-120">Il est ainsi doublement important pour les administrateurs d’Office 365 de connaître l’identité de leurs utilisateurs protégés.</span><span class="sxs-lookup"><span data-stu-id="e4c85-120">This makes it doubly important for Office 365 Administrators to be aware of who their protected users are and should be.</span></span>

![Une page de liens fiables pour les équipes qui signalent un lien malveillant et bloque le transit vers la page.](/microsoft-365/media/TP_SafelinksForTeams_Malicious.png)

<span data-ttu-id="e4c85-122">Le fait de cliquer sur *le bouton de retour de* cette page dans teams le ferme (ou peut entraîner la fermeture d’une page vierge par les utilisateurs).</span><span class="sxs-lookup"><span data-stu-id="e4c85-122">Clicking the *Go Back* button on this page in Teams will close it out (or may result in a blank page users  can close out).</span></span> <span data-ttu-id="e4c85-123">Toutefois, le fait de cliquer à nouveau sur le lien entraînera une nouvelle évaluation de la réputation du site afin de réafficher cette page.</span><span class="sxs-lookup"><span data-stu-id="e4c85-123">However, clicking on the link again will result in reassessment of the reputation of the site so that this page reappears.</span></span>

> [!NOTE]
><span data-ttu-id="e4c85-124">Certains administrateurs Office 365 vont activer le message **continuer quand même** sur la page de blocage.</span><span class="sxs-lookup"><span data-stu-id="e4c85-124">Some Office 365 Admins will enable the **Continue Anyway** message on the blocking page.</span></span> <span data-ttu-id="e4c85-125">Toutefois, si les liens fiables mesurent la réputation d’un site et le trouvent manquant, aucune autre opération de clic ne doit être effectuée.</span><span class="sxs-lookup"><span data-stu-id="e4c85-125">However, if safe links measures the reputation of a site and finds it lacking, no further click-through should be undertaken.</span></span> <span data-ttu-id="e4c85-126">Il n’est pas recommandé que les utilisateurs contournent les mesures de sécurité.</span><span class="sxs-lookup"><span data-stu-id="e4c85-126">It is not recommended that users bypass safety measures.</span></span> <span data-ttu-id="e4c85-127">N’hésitez pas à évaluer ces éléments avant d’activer la fonctionnalité continuer.</span><span class="sxs-lookup"><span data-stu-id="e4c85-127">Please weigh this into your considerations before enabling Continue Anyway.</span></span> 

