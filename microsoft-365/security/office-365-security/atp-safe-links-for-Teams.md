---
title: Liens fiables ATP pour Teams, safelinks, liens fiables, bloquer les liens malveillants, Office 365 ATP, liens approuvés de teams, empêcher les utilisateurs de cliquer sur les liens incorrects, liens malveillants
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
ms.openlocfilehash: 362fb37b352a77aea07b899b707dbf4ac3d440d5
ms.sourcegitcommit: c083602dda3cdcb5b58cb8aa070d77019075f765
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/22/2020
ms.locfileid: "48198750"
---
<!--06/21/2019-->

# <a name="safe-links-in-teams"></a><span data-ttu-id="17c0d-104">Liens fiables dans Teams</span><span class="sxs-lookup"><span data-stu-id="17c0d-104">Safe Links in Teams</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../includes/microsoft-defender-for-office.md)]


> [!IMPORTANT]
> <span data-ttu-id="17c0d-105">Cette fonctionnalité est en préversion **publique** pour les clients du programme d’adoption de la technologie Microsoft Teams (TAP) du 28 février 2020.</span><span class="sxs-lookup"><span data-stu-id="17c0d-105">This feature is in **Public Preview** for customers in the Microsoft Teams Technology Adoption Program (TAP) as of Feb 28, 2020.</span></span> <span data-ttu-id="17c0d-106">Cette note sera supprimée de l’article lorsque les liens fiables de teams sont plus largement disponibles.</span><span class="sxs-lookup"><span data-stu-id="17c0d-106">This note will be removed from the article when Safe Links for Teams is more widely available.</span></span>

<span data-ttu-id="17c0d-107">Microsoft Teams, une application Microsoft Cloud pour la gestion de votre travail, utilise déjà des pièces jointes fiables (pour Office 365), mais il aura maintenant accès à des liens fiables au moment de votre clic.</span><span class="sxs-lookup"><span data-stu-id="17c0d-107">Microsoft Teams, a Microsoft cloud-based application for managing your work, already uses Safe Attachments (for Office 365), but it will now have access to Safe Links at the time of your click.</span></span> <span data-ttu-id="17c0d-108">Que vous utilisiez des conversations, des conversations de groupe, des canaux ou des onglets, si vous disposez d’un abonnement à la protection avancée contre les menaces Office 365, vous pouvez activer et utiliser cette mesure de sécurité.</span><span class="sxs-lookup"><span data-stu-id="17c0d-108">Whether you're using Chats, Group Chats, Channels, or Tabs, if you have a subscription to Office 365 ATP, you will have the ability to enable and use this safety measure.</span></span> <span data-ttu-id="17c0d-109">Pour en savoir plus sur les conditions d’octroi de licences, consultez [Conseils sur la gestion des licences des services de niveau client de Microsoft 365](https://docs.microsoft.com/office365/servicedescriptions/microsoft-365-service-descriptions/microsoft-365-tenantlevel-services-licensing-guidance/microsoft-365-security-compliance-licensing-guidance).</span><span class="sxs-lookup"><span data-stu-id="17c0d-109">To learn more about licensing requirements, see [Microsoft 365 Tenant-Level Services Licensing Guidance](https://docs.microsoft.com/office365/servicedescriptions/microsoft-365-service-descriptions/microsoft-365-tenantlevel-services-licensing-guidance/microsoft-365-security-compliance-licensing-guidance).</span></span>

<span data-ttu-id="17c0d-110">Voici le principe de fonctionnement :</span><span class="sxs-lookup"><span data-stu-id="17c0d-110">Here's how it works:</span></span>

1. <span data-ttu-id="17c0d-111">Lorsque vous démarrez l’application Teams, Microsoft 365 vérifie que l’utilisateur appartient à une organisation disposant d’Office 365 ATP et que l’utilisateur fait partie d’une stratégie de liens approuvés active avec sa protection activée pour Microsoft Teams.</span><span class="sxs-lookup"><span data-stu-id="17c0d-111">When you start the Teams application, Microsoft 365 will check to make sure the user belongs to an organization that has Office 365 ATP, and that the user is part of an active safe links policy with its protection enabled for Microsoft Teams.</span></span>

2. <span data-ttu-id="17c0d-112">Si les éléments ci-dessus sont vrais, les URL seront validées au moment du clic dans les conversations, les conversations de groupe, les canaux et dans les onglets pour cet utilisateur.</span><span class="sxs-lookup"><span data-stu-id="17c0d-112">If the above are true, then URLs will be validated at the time of click in Chats, Group Chats, Channels, and in Tabs for that user.</span></span>

## <a name="what-will-users-experience"></a><span data-ttu-id="17c0d-113">Qu’est-ce que les utilisateurs peuvent expérimenter ?</span><span class="sxs-lookup"><span data-stu-id="17c0d-113">What will users experience?</span></span>

<span data-ttu-id="17c0d-114">Tous les utilisateurs protégés bénéficieront de cette expérience avec des URL dangereuses :</span><span class="sxs-lookup"><span data-stu-id="17c0d-114">All protected users will have this experience with hazardous URLs:</span></span>

- <span data-ttu-id="17c0d-115">Si vous avez cliqué sur le lien d’une conversation Teams, d’une conversation de groupe ou de canaux, une page s’affiche dans le navigateur par défaut.</span><span class="sxs-lookup"><span data-stu-id="17c0d-115">If the link was clicked from a Teams conversation, group chat, or from channels, a page will render in the default browser.</span></span> <span data-ttu-id="17c0d-116">Si vous avez cliqué sur le lien à partir d’un onglet épinglé, la page s’affiche dans l’interface utilisateur de teams sous cet onglet, et l’option d’ouverture dans le navigateur est désactivée pour des raisons de sécurité.</span><span class="sxs-lookup"><span data-stu-id="17c0d-116">If the link was clicked from a pinned tab, the page will appear in the Teams GUI within that tab, and the option to open in browser will be disabled for security purposes.</span></span>

- <span data-ttu-id="17c0d-117">Cet utilisateur ne pourra pas continuer à passer sur le site de l’URL.</span><span class="sxs-lookup"><span data-stu-id="17c0d-117">This user will be blocked from proceeding to the URL's site.</span></span>

<span data-ttu-id="17c0d-118">Si l’utilisateur qui a envoyé le lien n’est pas protégé par la protection avancée contre les menaces d’Office 365, il est libre de cliquer sur l’URL sur son ordinateur et de résoudre le problème.</span><span class="sxs-lookup"><span data-stu-id="17c0d-118">If the user who sent the link isn't protected by Office 365 ATP, he or she is free to click the URL on his or her machine and resolve the problem site.</span></span> <span data-ttu-id="17c0d-119">Il est ainsi doublement important que les administrateurs soient conscients de l’identité de leurs utilisateurs protégés.</span><span class="sxs-lookup"><span data-stu-id="17c0d-119">This makes it doubly important for administrators to be aware of who their protected users are and should be.</span></span>

![Une page de liens fiables pour les équipes qui signalent un lien malveillant et bloque le transit vers la page.](/microsoft-365/media/TP_SafelinksForTeams_Malicious.png)

<span data-ttu-id="17c0d-121">Le fait de cliquer sur *le bouton de retour de* cette page dans teams le ferme (ou peut entraîner la fermeture d’une page vierge par les utilisateurs).</span><span class="sxs-lookup"><span data-stu-id="17c0d-121">Clicking the *Go Back* button on this page in Teams will close it out (or may result in a blank page users  can close out).</span></span> <span data-ttu-id="17c0d-122">Toutefois, le fait de cliquer à nouveau sur le lien entraînera une nouvelle évaluation de la réputation du site afin de réafficher cette page.</span><span class="sxs-lookup"><span data-stu-id="17c0d-122">However, clicking on the link again will result in reassessment of the reputation of the site so that this page reappears.</span></span>

> [!NOTE]
> <span data-ttu-id="17c0d-123">Certains administrateurs de Microsoft 365 vont activer le message **continuer quand même** sur la page de blocage.</span><span class="sxs-lookup"><span data-stu-id="17c0d-123">Some Microsoft 365 admins will enable the **Continue Anyway** message on the blocking page.</span></span> <span data-ttu-id="17c0d-124">Toutefois, si les liens fiables mesurent la réputation d’un site et le trouvent manquant, aucune autre opération de clic ne doit être effectuée.</span><span class="sxs-lookup"><span data-stu-id="17c0d-124">However, if Safe Links measures the reputation of a site and finds it lacking, no further click-through should be undertaken.</span></span> <span data-ttu-id="17c0d-125">Il n’est pas recommandé que les utilisateurs contournent les mesures de sécurité.</span><span class="sxs-lookup"><span data-stu-id="17c0d-125">It is not recommended that users bypass safety measures.</span></span> <span data-ttu-id="17c0d-126">N’hésitez pas à évaluer ces éléments avant d’activer la fonctionnalité continuer.</span><span class="sxs-lookup"><span data-stu-id="17c0d-126">Please weigh this into your considerations before enabling Continue Anyway.</span></span>
