---
title: Sécurité Office 365
ms.author: tracyp
author: msfttracyp
manager: dansimp
ms.date: 08/13/2020
audience: Admin
ms.topic: overview
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.collection:
- microsoft-365-docs-pr
description: Sécurité dans Office 365, des plans d’EOP à ATP 1 et 2, des configurations de sécurité standard ou rigoureuses, et bien plus, afin que vous puissiez comprendre ce dont vous disposez et comment sécuriser vos propriétés.
ms.openlocfilehash: 680066f58850f59523ae6fb8a8168459dd813fc1
ms.sourcegitcommit: 888b9355ef7b933c55ca6c18639c12426ff3fbde
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/29/2020
ms.locfileid: "48304845"
---
# <a name="office-365-security-outline"></a><span data-ttu-id="1da64-103">Plan de sécurité Office 365</span><span class="sxs-lookup"><span data-stu-id="1da64-103">Office 365 Security outline</span></span>

<span data-ttu-id="1da64-104">Cet article vous présente vos nouvelles propriétés de sécurité dans le Cloud.</span><span class="sxs-lookup"><span data-stu-id="1da64-104">This article will introduce you to your new security properties in the Cloud.</span></span> <span data-ttu-id="1da64-105">Que vous soyez membre d’un centre de sécurité, vous êtes un administrateur de sécurité, ou vous souhaitez un actualisateur, commençons.</span><span class="sxs-lookup"><span data-stu-id="1da64-105">Whether you're part of a Security Operations Center, you're a Security Administrator new to the space, or you want a refresher, let's get started.</span></span>

> [!CAUTION]
> <span data-ttu-id="1da64-106">Salut.</span><span class="sxs-lookup"><span data-stu-id="1da64-106">Hi.</span></span> <span data-ttu-id="1da64-107">Si vous utilisez **Outlook.com**, la **famille Microsoft 365**ou **Microsoft 365 personnel**, et que vous avez besoin de *liens fiables* ou d’informations de *pièces jointes fiables* , ***cliquez sur ce lien***: [sécurité avancée Outlook.com pour les abonnés de Microsoft 365](https://support.microsoft.com/office/advanced-outlook-com-security-for-office-365-subscribers-882d2243-eab9-4545-a58a-b36fee4a46e2).</span><span class="sxs-lookup"><span data-stu-id="1da64-107">If you're using **Outlook.com**, **Microsoft 365 Family**, or **Microsoft 365 Personal**, and need *Safe Links* or *Safe Attachments* info, ***click this link***: [Advanced Outlook.com security for Microsoft 365 subscribers](https://support.microsoft.com/office/advanced-outlook-com-security-for-office-365-subscribers-882d2243-eab9-4545-a58a-b36fee4a46e2).</span></span> <span data-ttu-id="1da64-108">Nos!</span><span class="sxs-lookup"><span data-stu-id="1da64-108">Thanks!</span></span>

## <a name="office-365-security-spelled-out"></a><span data-ttu-id="1da64-109">Sécurité Office 365</span><span class="sxs-lookup"><span data-stu-id="1da64-109">Office 365 security spelled out</span></span>

<span data-ttu-id="1da64-110">Chaque abonnement Office 365 est fourni avec des fonctionnalités de sécurité.</span><span class="sxs-lookup"><span data-stu-id="1da64-110">Every Office 365 subscription comes with security capabilities.</span></span> <span data-ttu-id="1da64-111">Les objectifs et les actions que vous pouvez effectuer dépendent de l’intérêt de ces différents abonnements.</span><span class="sxs-lookup"><span data-stu-id="1da64-111">The goals and actions that you can take depend on the focus of these different subscriptions.</span></span> <span data-ttu-id="1da64-112">Dans la sécurité Office 365, trois services de sécurité (ou produits) principaux sont liés à votre type d’abonnement :</span><span class="sxs-lookup"><span data-stu-id="1da64-112">In Office 365 security, there are three main security services (or products) tied to your subscription type:</span></span>

1. <span data-ttu-id="1da64-113">Exchange Online Protection (EOP)</span><span class="sxs-lookup"><span data-stu-id="1da64-113">Exchange Online Protection (EOP)</span></span>
1. <span data-ttu-id="1da64-114">Protection avancée contre les menaces, plan 1 (ATP P1)</span><span class="sxs-lookup"><span data-stu-id="1da64-114">Advanced Threat Protection, Plan 1 (ATP P1)</span></span>
1. <span data-ttu-id="1da64-115">Protection avancée contre les menaces, plan 2 (ATP P2)</span><span class="sxs-lookup"><span data-stu-id="1da64-115">Advanced Threat Protection, Plan 2 (ATP P2)</span></span>

> [!NOTE]
> <span data-ttu-id="1da64-116">Si vous avez acheté votre abonnement et que vous avez besoin de déployer des fonctionnalités de sécurité *dès à présent*, passez aux étapes décrites dans l’article se [protéger contre les menaces](https://docs.microsoft.com/microsoft-365/security/office-365-security/protect-against-threats?view=o365-worldwide) .</span><span class="sxs-lookup"><span data-stu-id="1da64-116">If you bought your subscription and need to roll out security features *right now*, skip to the steps in the [Protect Against Threats](https://docs.microsoft.com/microsoft-365/security/office-365-security/protect-against-threats?view=o365-worldwide) article.</span></span> <span data-ttu-id="1da64-117">Si vous débutez avec votre abonnement et que vous aimeriez en obtenir la licence avant de commencer, parcourez la > facturation vos produits dans le [Centre d’administration Microsoft 365](https://admin.microsoft.com/AdminPortal/#/homepage).</span><span class="sxs-lookup"><span data-stu-id="1da64-117">If you're new to your subscription and would like to know your license before you begin, browse Billing > Your Products in the [Microsoft 365 admin center](https://admin.microsoft.com/AdminPortal/#/homepage).</span></span>

<span data-ttu-id="1da64-118">La sécurité Office 365 s’appuie sur les protections principales proposées par EOP.</span><span class="sxs-lookup"><span data-stu-id="1da64-118">Office 365 security builds on the core protections offered by EOP.</span></span> <span data-ttu-id="1da64-119">EOP est présent dans tout abonnement où se trouvent des boîtes aux lettres Exchange Online (n’oubliez pas que tous les produits de sécurité présentés ici sont basés sur le Cloud).</span><span class="sxs-lookup"><span data-stu-id="1da64-119">EOP is present in any subscription where Exchange Online mailboxes can be found (remember, all the security products discussed here are Cloud-based).</span></span>

<span data-ttu-id="1da64-120">Vous pouvez être habitué à voir ces trois composants présentés de la manière suivante :</span><span class="sxs-lookup"><span data-stu-id="1da64-120">You may be accustomed to seeing these three components discussed in this way:</span></span>

|<span data-ttu-id="1da64-121">Exchange Online Protection</span><span class="sxs-lookup"><span data-stu-id="1da64-121">EOP</span></span>  | <span data-ttu-id="1da64-122">ATP P1</span><span class="sxs-lookup"><span data-stu-id="1da64-122">ATP P1</span></span> | <span data-ttu-id="1da64-123">ATP P2</span><span class="sxs-lookup"><span data-stu-id="1da64-123">ATP P2</span></span>  |
|---------|---------|---------|
|<span data-ttu-id="1da64-124">Empêche les attaques connues basées sur un volume et de grandes quantités.</span><span class="sxs-lookup"><span data-stu-id="1da64-124">Prevents broad, volume-based, known attacks.</span></span>    |  <span data-ttu-id="1da64-125">Protège le courrier électronique et la collaboration contre les programmes malveillants, les hameçons et les messages électroniques de jour.</span><span class="sxs-lookup"><span data-stu-id="1da64-125">Protects email and collaboration from zero-day malware, phish, and business email compromise.</span></span>       | <span data-ttu-id="1da64-126">Ajoute une enquête après effraction, une chasse et une réponse, ainsi qu’une automatisation et une simulation (pour la formation).</span><span class="sxs-lookup"><span data-stu-id="1da64-126">Adds post-breach investigation, hunting, and response, as well as automation, and simulation (for training).</span></span>         |

<span data-ttu-id="1da64-127">Toutefois, en ce qui concerne l’architecture, nous allons commencer par réfléchir à chaque partie en tant que couches de sécurité cumulatives, chacune avec une mise en évidence de la sécurité.</span><span class="sxs-lookup"><span data-stu-id="1da64-127">But in terms of architecture, let's start by thinking of each piece as cumulative layers of security, each with a security emphasis.</span></span> <span data-ttu-id="1da64-128">Plus comme ceci :</span><span class="sxs-lookup"><span data-stu-id="1da64-128">More like this:</span></span>

<!--:::image type="content" source="../../media/tp-EOPATPStack.PNG" alt-text="Placeholder graphic":::-->

:::image type="content" source="../../media/tp_EOPandATPGraphic.png" alt-text="Placeholder graphic":::

<span data-ttu-id="1da64-130">Bien que chacun de ces services mette en évidence un objectif spécifique parmi les objectifs de la protection, de la détection, de l’examen et de la réponse, ***tous*** les services peuvent ***effectuer les objectifs*** de protection, de détection, d’analyse et de réponse.</span><span class="sxs-lookup"><span data-stu-id="1da64-130">Though each of these services emphasizes a specific goal from among Protect, Detect, Investigate, and Respond, ***all*** the services can carry out ***any*** of the goals of protecting, detecting, investigating, and responding.</span></span>

<span data-ttu-id="1da64-131">Le cœur de la sécurité Office 365 est la protection EOP.</span><span class="sxs-lookup"><span data-stu-id="1da64-131">The core of Office 365 security is EOP protection.</span></span> <span data-ttu-id="1da64-132">ATP P1 contient EOP.</span><span class="sxs-lookup"><span data-stu-id="1da64-132">ATP P1 contains EOP in it.</span></span> <span data-ttu-id="1da64-133">ATP P2 contient P1 et EOP.</span><span class="sxs-lookup"><span data-stu-id="1da64-133">ATP P2 contains P1 and EOP.</span></span> <span data-ttu-id="1da64-134">La structure est cumulative.</span><span class="sxs-lookup"><span data-stu-id="1da64-134">The structure is cumulative.</span></span> <span data-ttu-id="1da64-135">C’est pourquoi, lors de la configuration de la protection avancée contre les menaces, commencez par EOP et utilisez les couches.</span><span class="sxs-lookup"><span data-stu-id="1da64-135">That's why, when configuring ATP, you should start with EOP and work up through the layers.</span></span>

<span data-ttu-id="1da64-136">Bien que la configuration de l’authentification de messagerie ait lieu dans le DNS public, il est important de configurer cette fonctionnalité pour la protéger contre l’usurpation d’identité.</span><span class="sxs-lookup"><span data-stu-id="1da64-136">Though email authentication configuration takes place in public DNS, it's important to configure this feature to help defend against spoofing.</span></span> <span data-ttu-id="1da64-137">*Si vous disposez d’EOP,* ***vous devez [configurer l’authentification de messagerie](https://docs.microsoft.com/microsoft-365/security/office-365-security/email-validation-and-authentication?view=o365-worldwide)***.</span><span class="sxs-lookup"><span data-stu-id="1da64-137">*If you have EOP,* ***you should [configure email authentication](https://docs.microsoft.com/microsoft-365/security/office-365-security/email-validation-and-authentication?view=o365-worldwide)***.</span></span>

<span data-ttu-id="1da64-138">Si vous avez un Office 365 E3 ou une version inférieure, vous disposez d’EOP, mais avec la possibilité d’acheter une solution de protection avancée contre les menaces P1 via la mise à niveau.</span><span class="sxs-lookup"><span data-stu-id="1da64-138">If you have an Office 365 E3, or below, you have EOP, but with the option to buy standalone ATP P1 through upgrade.</span></span> <span data-ttu-id="1da64-139">Si vous disposez d’Office 365 E5, vous avez déjà ATP P2.</span><span class="sxs-lookup"><span data-stu-id="1da64-139">If you have Office 365 E5, you already have ATP P2.</span></span>

> [!TIP]
> <span data-ttu-id="1da64-140">Si votre abonnement n’est ni Office 365 E3 ni E5, vous pouvez toujours vérifier si vous avez la possibilité de procéder à une mise à niveau vers la protection avancée contre les menaces.</span><span class="sxs-lookup"><span data-stu-id="1da64-140">If your subscription is neither Office 365 E3 or E5, you can still check to see if you have the option to upgrade to ATP P1.</span></span> <span data-ttu-id="1da64-141">Si vous êtes intéressé, [cette page Web](https://www.microsoft.com/microsoft-365/exchange/advance-threat-protection#coreui-contentrichblock-x07wids) répertorie les abonnements éligibles pour la mise à niveau de la protection avancée contre les menaces (à la fin de la page).</span><span class="sxs-lookup"><span data-stu-id="1da64-141">If you're interested, [this webpage](https://www.microsoft.com/microsoft-365/exchange/advance-threat-protection#coreui-contentrichblock-x07wids) lists subscriptions eligible for the ATP P1 upgrade (check the end of the page for the fine-print).</span></span>

## <a name="the-office-365-security-ladder-from-eop-to-atp"></a><span data-ttu-id="1da64-142">Échelle de sécurité Office 365 de EOP à la protection avancée contre les menaces</span><span class="sxs-lookup"><span data-stu-id="1da64-142">The Office 365 security ladder from EOP to ATP</span></span>

:::image type="content" source="../../media/tp_EOPATPEmailAuth4.gif" alt-text="Placeholder graphic":::

> [!IMPORTANT]
> <span data-ttu-id="1da64-144">Découvrez les détails de ces pages : [Exchange Online Protection](https://docs.microsoft.com/microsoft-365/security/office-365-security/exchange-online-protection-overview?view=o365-worldwide)et [Advanced Threat Protection](https://docs.microsoft.com/microsoft-365/security/office-365-security/office-365-atp?view=o365-worldwide).</span><span class="sxs-lookup"><span data-stu-id="1da64-144">Learn the details on these pages: [Exchange Online Protection](https://docs.microsoft.com/microsoft-365/security/office-365-security/exchange-online-protection-overview?view=o365-worldwide), and [Advanced Threat Protection](https://docs.microsoft.com/microsoft-365/security/office-365-security/office-365-atp?view=o365-worldwide).</span></span>

<span data-ttu-id="1da64-145">Les avantages de l’ajout de plans ATP à la gestion des menaces EOP pures peuvent être difficiles à déterminer à première vue.</span><span class="sxs-lookup"><span data-stu-id="1da64-145">What makes adding ATP plans an advantage to pure EOP threat management can be difficult to tell at first glance.</span></span> <span data-ttu-id="1da64-146">Pour vous aider à déterminer si un chemin de mise à niveau est approprié pour votre organisation, examinons les fonctionnalités de chaque produit lors de la réalisation des opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="1da64-146">To help sort out if an upgrade path is right for your organization, let's look at the capabilities of each product when it comes to:</span></span>

 - <span data-ttu-id="1da64-147">prévention et détection des menaces</span><span class="sxs-lookup"><span data-stu-id="1da64-147">preventing and detecting threats</span></span>
 - <span data-ttu-id="1da64-148">examen en cours</span><span class="sxs-lookup"><span data-stu-id="1da64-148">investigating</span></span>
 - <span data-ttu-id="1da64-149">face</span><span class="sxs-lookup"><span data-stu-id="1da64-149">responding</span></span>

<span data-ttu-id="1da64-150">à partir d' **Exchange Online Protection**:</span><span class="sxs-lookup"><span data-stu-id="1da64-150">starting with **Exchange Online Protection**:</span></span>
<p>

|<span data-ttu-id="1da64-151">Empêcher/détecter</span><span class="sxs-lookup"><span data-stu-id="1da64-151">Prevent/Detect</span></span>  |<span data-ttu-id="1da64-152">Examiner</span><span class="sxs-lookup"><span data-stu-id="1da64-152">Investigate</span></span>  |<span data-ttu-id="1da64-153">Répondre</span><span class="sxs-lookup"><span data-stu-id="1da64-153">Respond</span></span>  |
|---------|---------|---------|
| <span data-ttu-id="1da64-154">Les technologies sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="1da64-154">Technologies include:</span></span><ul><li><span data-ttu-id="1da64-155">courrier indésirable</span><span class="sxs-lookup"><span data-stu-id="1da64-155">spam</span></span></li><li><span data-ttu-id="1da64-156">jouer</span><span class="sxs-lookup"><span data-stu-id="1da64-156">phish</span></span></li><li><span data-ttu-id="1da64-157">programmes malveillants</span><span class="sxs-lookup"><span data-stu-id="1da64-157">malware</span></span></li><li><span data-ttu-id="1da64-158">courrier en nombre</span><span class="sxs-lookup"><span data-stu-id="1da64-158">bulk mail</span></span></li><li><span data-ttu-id="1da64-159">aide à l’usurpation d’identité</span><span class="sxs-lookup"><span data-stu-id="1da64-159">spoof intelligence</span></span></li><li><span data-ttu-id="1da64-160">détection de l’emprunt d’identité</span><span class="sxs-lookup"><span data-stu-id="1da64-160">impersonation detection</span></span></li><li><span data-ttu-id="1da64-161">Mise en quarantaine de l’administrateur</span><span class="sxs-lookup"><span data-stu-id="1da64-161">Admin Quarantine</span></span></li><li><span data-ttu-id="1da64-162">Soumissions d’administrateurs et d’utilisateurs de faux positifs et faux négatifs</span><span class="sxs-lookup"><span data-stu-id="1da64-162">Admin and user submissions of False Positives and False Negatives</span></span></li><li><span data-ttu-id="1da64-163">Autoriser/bloquer pour les URL et les fichiers</span><span class="sxs-lookup"><span data-stu-id="1da64-163">Allow/Block for URLs and Files</span></span></li><li><span data-ttu-id="1da64-164">Rapports</span><span class="sxs-lookup"><span data-stu-id="1da64-164">Reports</span></span></li></u1>|<li><span data-ttu-id="1da64-165">Recherche de journal d’audit</span><span class="sxs-lookup"><span data-stu-id="1da64-165">Audit log search</span></span></li><li><span data-ttu-id="1da64-166">Suivi des messages</span><span class="sxs-lookup"><span data-stu-id="1da64-166">Message Trace</span></span></li>|<li><span data-ttu-id="1da64-167">Purge automatique avec zéro heure (ZAP)</span><span class="sxs-lookup"><span data-stu-id="1da64-167">Zero-hour Auto-Purge (ZAP)</span></span></li><li><span data-ttu-id="1da64-168">Perfectionnement et test des listes verte et rouge</span><span class="sxs-lookup"><span data-stu-id="1da64-168">Refinement and testing of Allow and Block lists</span></span></li>|

<span data-ttu-id="1da64-169">Si vous souhaitez aller plus loin dans EOP, **[accédez à cet article](https://review.docs.microsoft.com/microsoft-365/security/office-365-security/exchange-online-protection-overview?view=o365-21vianet&branch=tp_EOPOverview)**.</span><span class="sxs-lookup"><span data-stu-id="1da64-169">If you want to dig in to EOP, **[jump to this article](https://review.docs.microsoft.com/microsoft-365/security/office-365-security/exchange-online-protection-overview?view=o365-21vianet&branch=tp_EOPOverview)**.</span></span>

<span data-ttu-id="1da64-170">Étant donné que ces produits sont cumulatifs, si vous évaluez la protection avancée contre les menaces et décidez de s’y abonner, vous ajouterez ces capacités.</span><span class="sxs-lookup"><span data-stu-id="1da64-170">Because these products are cumulative, if you evaluate ATP P1 and decide to subscribe to it, you'll add these abilities.</span></span>

<span data-ttu-id="1da64-171">Améliorations apportées par la **protection avancée contre les menaces, plan 1** (à ce jour) :</span><span class="sxs-lookup"><span data-stu-id="1da64-171">Gains with **Advanced Threat Protection, Plan 1** (to date):</span></span>
<p>

|<span data-ttu-id="1da64-172">Empêcher/détecter</span><span class="sxs-lookup"><span data-stu-id="1da64-172">Prevent/Detect</span></span>  |<span data-ttu-id="1da64-173">Examiner</span><span class="sxs-lookup"><span data-stu-id="1da64-173">Investigate</span></span>  |<span data-ttu-id="1da64-174">Répondre</span><span class="sxs-lookup"><span data-stu-id="1da64-174">Respond</span></span>  |
|---------|---------|---------|
| <span data-ttu-id="1da64-175">Les technologies incluent tous les éléments dans EOP plus :<u1></span><span class="sxs-lookup"><span data-stu-id="1da64-175">Technologies include everything in EOP plus:<u1></span></span><li><span data-ttu-id="1da64-176">Pièces jointes fiables</span><span class="sxs-lookup"><span data-stu-id="1da64-176">Safe attachments</span></span></li><li><span data-ttu-id="1da64-177">Liens fiables</span><span class="sxs-lookup"><span data-stu-id="1da64-177">Safe links</span></span><li><span data-ttu-id="1da64-178">Protection contre les charges de travail ATP (ex.</span><span class="sxs-lookup"><span data-stu-id="1da64-178">ATP protection for workloads (ex.</span></span> <span data-ttu-id="1da64-179">SharePoint Online, teams, OneDrive entreprise)</span><span class="sxs-lookup"><span data-stu-id="1da64-179">SharePoint Online, Teams, OneDrive for Business)</span></span></li><li><span data-ttu-id="1da64-180">Protection du temps de clic dans les e-mails, les clients Office et les équipes</span><span class="sxs-lookup"><span data-stu-id="1da64-180">Time-of-click protection in email, Office clients, and Teams</span></span></li><li><span data-ttu-id="1da64-181">Protection contre le hameçonnage (ATP)</span><span class="sxs-lookup"><span data-stu-id="1da64-181">ATP anti-phishing</span></span></li><li><span data-ttu-id="1da64-182">Protection contre l’usurpation d’identité d’utilisateur et de domaine</span><span class="sxs-lookup"><span data-stu-id="1da64-182">User and domain impersonation protection</span></span></li><li><span data-ttu-id="1da64-183">Alertes et API d’intégration SIEM pour les alertes</span><span class="sxs-lookup"><span data-stu-id="1da64-183">Alerts, and SIEM integration API for alerts</span></span></li>|<li><span data-ttu-id="1da64-184">API d’intégration SIEM pour les détections</span><span class="sxs-lookup"><span data-stu-id="1da64-184">SIEM integration API for detections</span></span></li><li><span data-ttu-id="1da64-185">**Outil de détection en temps réel**</span><span class="sxs-lookup"><span data-stu-id="1da64-185">**Real-time detections tool**</span></span></li><li><span data-ttu-id="1da64-186">Suivi d’URL</span><span class="sxs-lookup"><span data-stu-id="1da64-186">URL trace</span></span></li>|<li><span data-ttu-id="1da64-187">Identique</span><span class="sxs-lookup"><span data-stu-id="1da64-187">Same</span></span></li></u1>

<span data-ttu-id="1da64-188">Par conséquent, ATP P1 s’étend sur le côté de la ***protection*** de la maison et ajoute des formes de ***détection***supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="1da64-188">So, ATP P1 expands on the ***prevention*** side of the house, and adds extra forms of ***detection***.</span></span>

<span data-ttu-id="1da64-189">ATP P1 ajoute également des **détections en temps réel** pour les enquêtes.</span><span class="sxs-lookup"><span data-stu-id="1da64-189">ATP P1 also adds **Real-time detections** for investigations.</span></span> <span data-ttu-id="1da64-190">Ce nom d’outil de sélection de menace est en gras, car il est clair pour *savoir* si vous avez un service ATP P1.</span><span class="sxs-lookup"><span data-stu-id="1da64-190">This threat hunting tool's name is in bold because having it is clear means of *knowing* you have ATP P1.</span></span> <span data-ttu-id="1da64-191">Elle n’apparaît pas dans le service ATP P2.</span><span class="sxs-lookup"><span data-stu-id="1da64-191">It doesn't appear in ATP P2.</span></span>

<span data-ttu-id="1da64-192">Améliorations apportées par la **protection avancée contre les menaces, plan 2** (à ce jour) :</span><span class="sxs-lookup"><span data-stu-id="1da64-192">Gains with **Advanced Threat Protection, Plan 2** (to date):</span></span>
<p>

|<span data-ttu-id="1da64-193">Empêcher/détecter</span><span class="sxs-lookup"><span data-stu-id="1da64-193">Prevent/Detect</span></span>  |<span data-ttu-id="1da64-194">Examiner</span><span class="sxs-lookup"><span data-stu-id="1da64-194">Investigate</span></span>  |<span data-ttu-id="1da64-195">Répondre</span><span class="sxs-lookup"><span data-stu-id="1da64-195">Respond</span></span>  |
|---------|---------|---------|
| <span data-ttu-id="1da64-196">Les technologies incluent tous les éléments d’EOP et de l’ATP P1 plus :<u1></span><span class="sxs-lookup"><span data-stu-id="1da64-196">Technologies include everything in EOP, and ATP P1 plus:<u1></span></span><li><span data-ttu-id="1da64-197">Identique</span><span class="sxs-lookup"><span data-stu-id="1da64-197">Same</span></span></li>|<li><span data-ttu-id="1da64-198">**Threat Explorer**</span><span class="sxs-lookup"><span data-stu-id="1da64-198">**Threat Explorer**</span></span></li><li><span data-ttu-id="1da64-199">Suivi des menaces</span><span class="sxs-lookup"><span data-stu-id="1da64-199">Threat Trackers</span></span></li><li><span data-ttu-id="1da64-200">Vues de campagne</span><span class="sxs-lookup"><span data-stu-id="1da64-200">Campaign views</span></span></li>|<li><span data-ttu-id="1da64-201">Examen et réponse automatisés (AIR)</span><span class="sxs-lookup"><span data-stu-id="1da64-201">Automated Investigation and Response (AIR)</span></span></li><li><span data-ttu-id="1da64-202">AIR de l’Explorateur de menaces</span><span class="sxs-lookup"><span data-stu-id="1da64-202">AIR from Threat Explorer</span></span></li><li><span data-ttu-id="1da64-203">AIR pour les utilisateurs compromis</span><span class="sxs-lookup"><span data-stu-id="1da64-203">AIR for compromised users</span></span></li><li><span data-ttu-id="1da64-204">API d’intégration SIEM pour les enquêtes automatisées</span><span class="sxs-lookup"><span data-stu-id="1da64-204">SIEM Integration API for Automated Investigations</span></span></li>

<span data-ttu-id="1da64-205">Ainsi, ATP P2 s’étend sur le côté de l' ***enquête et*** de la réponse de la maison, et ajoute un nouveau dosage de la chasse.</span><span class="sxs-lookup"><span data-stu-id="1da64-205">So, ATP P2 expands on the ***investigation and response*** side of the house, and adds a new hunting strength.</span></span> <span data-ttu-id="1da64-206">Traitement.</span><span class="sxs-lookup"><span data-stu-id="1da64-206">Automation.</span></span>

<span data-ttu-id="1da64-207">Dans le service ATP P2, l’outil de chasse principal est appelé « **Explorateur de menaces** » plutôt que des détections en temps réel.</span><span class="sxs-lookup"><span data-stu-id="1da64-207">In ATP P2, the primary hunting tool is called **Threat Explorer** rather than Real-time detections.</span></span> <span data-ttu-id="1da64-208">Si vous voyez l’Explorateur de menaces lorsque vous accédez au centre de sécurité, c’est que vous êtes dans l’ATP P2.</span><span class="sxs-lookup"><span data-stu-id="1da64-208">If you see Threat Explorer when you navigate to the Security center, you're in ATP P2.</span></span>

<span data-ttu-id="1da64-209">Pour obtenir des informations détaillées sur les P1 et P2, **[accédez à cet article](https://docs.microsoft.com/microsoft-365/security/office-365-security/office-365-atp?view=o365-worldwide)**.</span><span class="sxs-lookup"><span data-stu-id="1da64-209">To get into the details of ATP P1 and P2, **[jump to this article](https://docs.microsoft.com/microsoft-365/security/office-365-security/office-365-atp?view=o365-worldwide)**.</span></span>

> [!TIP]
> <span data-ttu-id="1da64-210">EOP et ATP sont également différents en ce qui concerne les utilisateurs finaux.</span><span class="sxs-lookup"><span data-stu-id="1da64-210">EOP and ATP are also different when it comes to end-users.</span></span> <span data-ttu-id="1da64-211">Dans EOP et ATP, le focus est *conscient*, de sorte que ces deux services incluent le *complément Outlook message de rapport* afin que les utilisateurs puissent signaler les courriers électroniques qu’ils détectent comme suspects, pour une analyse plus poussée.</span><span class="sxs-lookup"><span data-stu-id="1da64-211">In EOP and ATP P1, the focus is *awareness*, and so those two services include the *Report message Outlook add-in* so users can report emails they find suspicious, for further analysis.</span></span> <p> <span data-ttu-id="1da64-212">Dans le service ATP P2 (qui contient tous les éléments d’EOP et de P1), l’objectif est de suivre une *formation supplémentaire* pour les utilisateurs finals, et le centre d’exploitation de sécurité a accès à un puissant outil *simulateur de menace* , ainsi qu’aux mesures de l’utilisateur final qu’il fournit.</span><span class="sxs-lookup"><span data-stu-id="1da64-212">In ATP P2 (which contains everything in EOP and P1), the focus shifts to *further training* for end-users, and so the Security Operations Center has access to a powerful *Threat Simulator* tool, and the end-user metrics it provides.</span></span>

## <a name="office-365-atp-plan-1-vs-plan-2-cheat-sheet"></a><span data-ttu-id="1da64-213">Feuille de triche Office 365 DAV plan 1 vs.</span><span class="sxs-lookup"><span data-stu-id="1da64-213">Office 365 ATP Plan 1 vs. Plan 2 cheat sheet</span></span>

<span data-ttu-id="1da64-214">Ce guide de référence rapide vous aidera à comprendre les fonctionnalités fournies avec chaque abonnement ATP.</span><span class="sxs-lookup"><span data-stu-id="1da64-214">This quick-reference will help you understand what capabilities come with each ATP subscription.</span></span> <span data-ttu-id="1da64-215">Lorsqu’il est associé à votre connaissance des fonctionnalités EOP, il peut aider les décideurs à déterminer la solution disponible à la décision la plus adaptée à leurs besoins.</span><span class="sxs-lookup"><span data-stu-id="1da64-215">When combined with your knowledge of EOP features, it can help business decision makers determine what ATP is best for their needs.</span></span>

|<span data-ttu-id="1da64-216">Office 365 – Protection avancée contre les menaces (Plan 1)</span><span class="sxs-lookup"><span data-stu-id="1da64-216">Office 365 ATP Plan 1</span></span>|<span data-ttu-id="1da64-217">Office 365 – Protection avancée contre les menaces (Plan 2)</span><span class="sxs-lookup"><span data-stu-id="1da64-217">Office 365 ATP Plan 2</span></span>|
|---|---|
|<br/><span data-ttu-id="1da64-218">Fonctionnalités de configuration, de protection et de détection :</span><span class="sxs-lookup"><span data-stu-id="1da64-218">Configuration, protection, and detection capabilities:</span></span> <ul><li>[<span data-ttu-id="1da64-219">Pièces jointes fiables</span><span class="sxs-lookup"><span data-stu-id="1da64-219">Safe Attachments</span></span>](atp-safe-attachments.md)</li><li>[<span data-ttu-id="1da64-220">Liens fiables</span><span class="sxs-lookup"><span data-stu-id="1da64-220">Safe Links</span></span>](atp-safe-links.md)</li><li>[<span data-ttu-id="1da64-221">ATP pour SharePoint, OneDrive et Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="1da64-221">ATP for SharePoint, OneDrive, and Microsoft Teams</span></span>](atp-for-spo-odb-and-teams.md)</li><li>[<span data-ttu-id="1da64-222">ATP Protection anti-hameçonnage</span><span class="sxs-lookup"><span data-stu-id="1da64-222">ATP anti-phishing protection</span></span>](set-up-anti-phishing-policies.md#exclusive-settings-in-atp-anti-phishing-policies)</li><li>[<span data-ttu-id="1da64-223">Détections en temps réel</span><span class="sxs-lookup"><span data-stu-id="1da64-223">Real-time detections</span></span>](threat-explorer.md)</li></ul>|<span data-ttu-id="1da64-224">Fonctionnalités de l’offre Office 365 - Protection avancée contre les menaces (plan 1)</span><span class="sxs-lookup"><span data-stu-id="1da64-224">Office 365 ATP Plan 1 capabilities</span></span><br/><span data-ttu-id="1da64-225">--- plus ---</span><span class="sxs-lookup"><span data-stu-id="1da64-225">--- plus ---</span></span><br/><span data-ttu-id="1da64-226">Fonctionnalités d’automatisation, d’examen, de correction et de formation :</span><span class="sxs-lookup"><span data-stu-id="1da64-226">Automation, investigation, remediation, and education capabilities:</span></span></li><li>[<span data-ttu-id="1da64-227">Suivi des menaces</span><span class="sxs-lookup"><span data-stu-id="1da64-227">Threat Trackers</span></span>](threat-trackers.md)</li><li>[<span data-ttu-id="1da64-228">Threat Explorer</span><span class="sxs-lookup"><span data-stu-id="1da64-228">Threat Explorer</span></span>](threat-explorer.md)</li><li>[<span data-ttu-id="1da64-229">Examen et réponse automatisés</span><span class="sxs-lookup"><span data-stu-id="1da64-229">Automated investigation and response</span></span>](https://docs.microsoft.com/microsoft-365/security/office-365-security/office-365-air)</li><li>[<span data-ttu-id="1da64-230">Simulateur d’attaques</span><span class="sxs-lookup"><span data-stu-id="1da64-230">Attack Simulator</span></span>](attack-simulator.md)</li></ul>|
|

- <span data-ttu-id="1da64-231">Office 365 – Protection avancée contre les menaces (Plan 2) est inclus dans Office 365 E5, Office 365 a5 et Microsoft 365 E5.</span><span class="sxs-lookup"><span data-stu-id="1da64-231">Office 365 ATP Plan 2 is included in Office 365 E5, Office 365 A5, and Microsoft 365 E5.</span></span>

- <span data-ttu-id="1da64-232">Le plan 1 Office 365 ATP est incluse dans Microsoft 365 Business Premium.</span><span class="sxs-lookup"><span data-stu-id="1da64-232">Office 365 ATP Plan 1 is included in Microsoft 365 Business Premium.</span></span>

- <span data-ttu-id="1da64-233">Le plan 1 Office 365 ATP et le Plan 2 Office 365 ATP sont, pour certains abonnements, disponibles sous forme de complément.</span><span class="sxs-lookup"><span data-stu-id="1da64-233">Office 365 ATP Plan 1 and Office 365 ATP Plan 2 are each available as an add-on for certain subscriptions.</span></span> <span data-ttu-id="1da64-234">Pour en savoir plus, voici une autre [fonctionnalité de liaison disponible pour tous les plans ATP](https://docs.microsoft.com/office365/servicedescriptions/office-365-advanced-threat-protection-service-description#feature-availability-across-advanced-threat-protection-atp-plans).</span><span class="sxs-lookup"><span data-stu-id="1da64-234">To learn more, here's another link [Feature availability across ATP plans](https://docs.microsoft.com/office365/servicedescriptions/office-365-advanced-threat-protection-service-description#feature-availability-across-advanced-threat-protection-atp-plans).</span></span>

- <span data-ttu-id="1da64-235">La fonctionnalité [Documents sécurisés](safe-docs.md) est uniquement disponible pour les utilisateurs ayant des licences Microsoft 365 E5 ou Microsoft 365 E5 Sécurité (non inclus dans les plans Office 365 ATP)</span><span class="sxs-lookup"><span data-stu-id="1da64-235">The [Safe Documents](safe-docs.md) feature is only available to users with the Microsoft 365 E5 or Microsoft 365 E5 Security licenses (not included in Office 365 ATP plans).</span></span>

- <span data-ttu-id="1da64-236">Si votre abonnement actuel n’inclut pas Office 365 ATP et que vous le souhaitez, [contactez sales pour commencer une version d’évaluation](https://go.microsoft.com/fwlink/p/?LinkId=518644)et découvrez le fonctionnement de l’ATP pour votre organisation.</span><span class="sxs-lookup"><span data-stu-id="1da64-236">If your current subscription doesn't include Office 365 ATP and you want it, [contact sales to start a trial](https://go.microsoft.com/fwlink/p/?LinkId=518644), and find out how ATP can work for in your organization.</span></span>

> [!TIP]
> <span data-ttu-id="1da64-237">***Conseil Insider***.</span><span class="sxs-lookup"><span data-stu-id="1da64-237">***Insider tip***.</span></span> <span data-ttu-id="1da64-238">Vous pouvez utiliser la table des matières docs.microsoft.com pour en savoir plus sur EOP et la protection avancée contre les menaces.</span><span class="sxs-lookup"><span data-stu-id="1da64-238">You can use the docs.microsoft.com table of contents to learn about EOP and ATP.</span></span> <span data-ttu-id="1da64-239">Accédez aux articles sur la [sécurité d’Office 365](https://docs.microsoft.com/microsoft-365/security/office-365-security/security-roadmap?view=o365-worldwide) et vous remarquerez que l’organisation de la table des matières commence par l’évaluation et le déploiement (y compris la migration), puis continue à la prévention, la détection, l’enquête et la réponse.</span><span class="sxs-lookup"><span data-stu-id="1da64-239">Navigate to [Office 365 Security](https://docs.microsoft.com/microsoft-365/security/office-365-security/security-roadmap?view=o365-worldwide) articles, and you'll notice that table of contents organization begins with Evaluation and Deployment (including migration) and then continues into prevention, detection, investigation, and response.</span></span> <p> <span data-ttu-id="1da64-240">Cette structure est divisée de manière à ce que les rubriques relatives à l’administration de la **sécurité** soient suivies par les rubriques **opérations de sécurité** .</span><span class="sxs-lookup"><span data-stu-id="1da64-240">This structure is divided so that **Security Administration** topics are followed by **Security Operations** topics.</span></span> <span data-ttu-id="1da64-241">Si vous êtes un nouveau membre de l’un des rôles de travail, utilisez le lien de ce Conseil et vos connaissances de la table des matières pour en savoir plus sur l’espace.</span><span class="sxs-lookup"><span data-stu-id="1da64-241">If you're a new member of either job role, use the link in this tip, and your knowledge of the table of contents, to help learn the space.</span></span> <span data-ttu-id="1da64-242">N’oubliez pas d’utiliser les *liens de commentaires* et les *Articles de taux* au fur et à mesure.</span><span class="sxs-lookup"><span data-stu-id="1da64-242">Remember to use *feedback links* and *rate articles* as you go.</span></span> <span data-ttu-id="1da64-243">Les commentaires nous permettent d’améliorer votre offre.</span><span class="sxs-lookup"><span data-stu-id="1da64-243">Feedback helps us improve what we offer you.</span></span>