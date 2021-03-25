---
title: Affichages dans l’Explorateur de menaces et détections en temps réel
f1.keywords:
- NOCSH
ms.author: tracyp
author: msfttracyp
manager: dansimp
ms.date: 05/15/2020
audience: ITPro
ms.topic: article
localization_priority: Normal
search.appverid: ''
ms.collection:
- M365-security-compliance
- m365initiative-defender-office365
description: Découvrez comment utiliser l’Explorateur de menaces et le rapport de détections en temps réel pour examiner les menaces et y répondre dans le Centre de sécurité & conformité.
ms.custom: seo-marvel-apr2020
ms.technology: mdo
ms.prod: m365-security
ms.openlocfilehash: 78c03b45063f4bc34b47ab003bcf00d2befab886
ms.sourcegitcommit: dcb97fbfdae52960ae62b6faa707a05358193ed5
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/25/2021
ms.locfileid: "51204605"
---
# <a name="views-in-threat-explorer-and-real-time-detections"></a><span data-ttu-id="924d7-103">Affichages dans l’Explorateur de menaces et détections en temps réel</span><span class="sxs-lookup"><span data-stu-id="924d7-103">Views in Threat Explorer and real-time detections</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../includes/microsoft-defender-for-office.md)]

<span data-ttu-id="924d7-104">**S’applique à**</span><span class="sxs-lookup"><span data-stu-id="924d7-104">**Applies to**</span></span>
- [<span data-ttu-id="924d7-105">Microsoft Defender pour Office 365 : offre 1 et offre 2</span><span class="sxs-lookup"><span data-stu-id="924d7-105">Microsoft Defender for Office 365 plan 1 and plan 2</span></span>](defender-for-office-365.md)
- [<span data-ttu-id="924d7-106">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="924d7-106">Microsoft 365 Defender</span></span>](../defender/microsoft-365-defender.md)


![Threat Explorer](../../media/ThreatExplorerFirstOpened.png)

<span data-ttu-id="924d7-108">[L’Explorateur](threat-explorer.md) de menaces (et le rapport sur les détections en temps réel) est un outil puissant, quasiment en temps réel, qui permet aux équipes des opérations de sécurité d’examiner et de répondre aux menaces dans le Centre de sécurité & conformité.</span><span class="sxs-lookup"><span data-stu-id="924d7-108">[Threat Explorer](threat-explorer.md) (and the real-time detections report) is a powerful, near real-time tool to help Security Operations teams investigate and respond to threats in the Security & Compliance Center.</span></span> <span data-ttu-id="924d7-109">L’Explorateur (et le rapport de détections en temps réel) affiche des informations sur les programmes malveillants et le hameçonnage suspectés dans le courrier électronique et les fichiers dans Office 365, ainsi que d’autres menaces et risques de sécurité pour votre organisation.</span><span class="sxs-lookup"><span data-stu-id="924d7-109">Explorer (and the real-time detections report) displays information about suspected malware and phish in email and files in Office 365, as well as other security threats and risks to your organization.</span></span>

- <span data-ttu-id="924d7-110">Si vous avez [Microsoft Defender pour Office 365](defender-for-office-365.md) Plan 2, vous avez Explorer.</span><span class="sxs-lookup"><span data-stu-id="924d7-110">If you have [Microsoft Defender for Office 365](defender-for-office-365.md) Plan 2, then you have Explorer.</span></span>
- <span data-ttu-id="924d7-111">Si vous avez Microsoft Defender pour Office 365 Plan 1, vous avez des détections en temps réel.</span><span class="sxs-lookup"><span data-stu-id="924d7-111">If you have Microsoft Defender for Office 365 Plan 1, then you have real-time detections.</span></span>

<span data-ttu-id="924d7-112">Lorsque vous ouvrez l’Explorateur pour la première fois (ou le rapport de détections en temps réel), l’affichage par défaut affiche les détections de programmes malveillants de messagerie électronique au cours des 7 derniers jours.</span><span class="sxs-lookup"><span data-stu-id="924d7-112">When you first open Explorer (or the real-time detections report), the default view shows email malware detections for the past 7 days.</span></span> <span data-ttu-id="924d7-113">Ce rapport peut également afficher les détections de Microsoft Defender pour Office 365, telles que les URL malveillantes détectées par les liens fiables [et](safe-links.md)les fichiers malveillants détectés par les pièces [jointes fiables.](safe-attachments.md)</span><span class="sxs-lookup"><span data-stu-id="924d7-113">This report can also show Microsoft Defender for Office 365 detections, such as malicious URLs detected by [Safe Links](safe-links.md), and malicious files detected by [Safe Attachments](safe-attachments.md).</span></span> <span data-ttu-id="924d7-114">Ce rapport peut être modifié pour afficher les données des 30 derniers jours (avec un abonnement Payant Microsoft Defender pour Office 365 P2).</span><span class="sxs-lookup"><span data-stu-id="924d7-114">This report can be modified to show data for the past 30 days (with a Microsoft Defender for Office 365 P2 paid subscription).</span></span> <span data-ttu-id="924d7-115">Les abonnements à la version d’essai incluent uniquement les données des sept derniers jours.</span><span class="sxs-lookup"><span data-stu-id="924d7-115">Trial subscriptions will include data for the past seven days only.</span></span>

****

|<span data-ttu-id="924d7-116">Abonnement</span><span class="sxs-lookup"><span data-stu-id="924d7-116">Subscription</span></span>|<span data-ttu-id="924d7-117">Utilitaire</span><span class="sxs-lookup"><span data-stu-id="924d7-117">Utility</span></span>|<span data-ttu-id="924d7-118">Jours de données</span><span class="sxs-lookup"><span data-stu-id="924d7-118">Days of Data</span></span>|
|---|---|---|
|<span data-ttu-id="924d7-119">Version d’essai de Microsoft Defender pour Office 365 P1</span><span class="sxs-lookup"><span data-stu-id="924d7-119">Microsoft Defender for Office 365 P1 trial</span></span>|<span data-ttu-id="924d7-120">Détections en temps réel</span><span class="sxs-lookup"><span data-stu-id="924d7-120">Real-time detections</span></span>|<span data-ttu-id="924d7-121">7 </span><span class="sxs-lookup"><span data-stu-id="924d7-121">7</span></span>|
|<span data-ttu-id="924d7-122">Microsoft Defender pour Office 365 P1 payant</span><span class="sxs-lookup"><span data-stu-id="924d7-122">Microsoft Defender for Office 365 P1 paid</span></span>|<span data-ttu-id="924d7-123">Détections en temps réel</span><span class="sxs-lookup"><span data-stu-id="924d7-123">Real-time detections</span></span>|<span data-ttu-id="924d7-124">30</span><span class="sxs-lookup"><span data-stu-id="924d7-124">30</span></span>|
|<span data-ttu-id="924d7-125">Essai payant de Microsoft Defender pour Office 365 P1 pour Office 365 P2</span><span class="sxs-lookup"><span data-stu-id="924d7-125">Microsoft Defender for Office 365 P1 paid testing Defender for Office 365 P2 trial</span></span>|<span data-ttu-id="924d7-126">Threat Explorer</span><span class="sxs-lookup"><span data-stu-id="924d7-126">Threat Explorer</span></span>|<span data-ttu-id="924d7-127">7 </span><span class="sxs-lookup"><span data-stu-id="924d7-127">7</span></span>|
|<span data-ttu-id="924d7-128">Version d’essai de Microsoft Defender pour Office 365 P2</span><span class="sxs-lookup"><span data-stu-id="924d7-128">Microsoft Defender for Office 365 P2 trial</span></span>|<span data-ttu-id="924d7-129">Threat Explorer</span><span class="sxs-lookup"><span data-stu-id="924d7-129">Threat Explorer</span></span>|<span data-ttu-id="924d7-130">7 </span><span class="sxs-lookup"><span data-stu-id="924d7-130">7</span></span>|
|<span data-ttu-id="924d7-131">Microsoft Defender pour Office 365 P2 payant</span><span class="sxs-lookup"><span data-stu-id="924d7-131">Microsoft Defender for Office 365 P2 paid</span></span>|<span data-ttu-id="924d7-132">Threat Explorer</span><span class="sxs-lookup"><span data-stu-id="924d7-132">Threat Explorer</span></span>|<span data-ttu-id="924d7-133">30</span><span class="sxs-lookup"><span data-stu-id="924d7-133">30</span></span>|
|

> [!NOTE]
> <span data-ttu-id="924d7-134">Nous étendons bientôt la limite de rétention et de recherche des données de l’Explorateur (et des détections en temps réel) pour les clients d’essai de 7 à 30 jours.</span><span class="sxs-lookup"><span data-stu-id="924d7-134">We will soon be extending the Explorer (and Real-time detections) data retention and search limit for trial tenants from 7 to 30 days.</span></span> <span data-ttu-id="924d7-135">Cette modification est en cours de suivi dans le cadre de l’élément de feuille de route n. 70544 et est actuellement en phase de déploiement.</span><span class="sxs-lookup"><span data-stu-id="924d7-135">This change is being tracked as part of roadmap item no. 70544, and is currently in a roll-out phase.</span></span>

<span data-ttu-id="924d7-136">Utilisez le menu **Affichage** pour modifier les informations affichées.</span><span class="sxs-lookup"><span data-stu-id="924d7-136">Use the **View** menu to change what information is displayed.</span></span> <span data-ttu-id="924d7-137">Les bulles vous aident à déterminer l’affichage à utiliser.</span><span class="sxs-lookup"><span data-stu-id="924d7-137">Tooltips help you determine which view to use.</span></span>

![Menu Affichage de l’Explorateur de menaces](../../media/ThreatExplorerViewMenu.png)

<span data-ttu-id="924d7-139">Une fois que vous avez sélectionné un affichage, vous pouvez appliquer des filtres et configurer des requêtes pour effectuer une analyse plus approfondie.</span><span class="sxs-lookup"><span data-stu-id="924d7-139">Once you have selected a view, you can apply filters and set up queries to conduct further analysis.</span></span> <span data-ttu-id="924d7-140">Les sections suivantes fournissent une brève vue d’ensemble des différents affichages disponibles dans l’Explorateur (ou détections en temps réel).</span><span class="sxs-lookup"><span data-stu-id="924d7-140">The following sections provide a brief overview of the various views available in Explorer (or real-time detections).</span></span>

## <a name="email--malware"></a><span data-ttu-id="924d7-141">Courrier électronique > programmes malveillants</span><span class="sxs-lookup"><span data-stu-id="924d7-141">Email > Malware</span></span>

<span data-ttu-id="924d7-142">Pour afficher ce rapport, dans l’Explorateur (ou détections en temps réel), choisissez **Afficher les** programmes malveillants \> **de** \> **messagerie.**</span><span class="sxs-lookup"><span data-stu-id="924d7-142">To view this report, in Explorer (or real-time detections), choose **View** \> **Email** \> **Malware**.</span></span> <span data-ttu-id="924d7-143">Cet affichage affiche des informations sur les messages électroniques identifiés comme contenant des programmes malveillants.</span><span class="sxs-lookup"><span data-stu-id="924d7-143">This view shows information about email messages that were identified as containing malware.</span></span>

![Afficher les données relatives aux e-mails identifiés comme programmes malveillants](../../media/ExplorerEmailMalwareMenu.png)

<span data-ttu-id="924d7-145">Cliquez **sur Expéditeur** pour ouvrir votre liste d’options d’affichage.</span><span class="sxs-lookup"><span data-stu-id="924d7-145">Click **Sender** to open your list of viewing options.</span></span> <span data-ttu-id="924d7-146">Cette liste permet d’afficher les données par expéditeur, destinataire, domaine de l’expéditeur, objet, technologie de détection, état de protection, etc.</span><span class="sxs-lookup"><span data-stu-id="924d7-146">Use this list to view data by sender, recipients, sender domain, subject, detection technology, protection status, and more.</span></span>

<span data-ttu-id="924d7-147">Par exemple, pour voir les actions qui ont été prises sur les messages électroniques détectés, choisissez **l’état protection** dans la liste.</span><span class="sxs-lookup"><span data-stu-id="924d7-147">For example, to see what actions were taken on detected email messages, choose **Protection status** in the list.</span></span> <span data-ttu-id="924d7-148">Sélectionnez une option, puis cliquez sur le bouton Actualiser pour appliquer ce filtre à votre rapport.</span><span class="sxs-lookup"><span data-stu-id="924d7-148">Select an option, and then click the Refresh button to apply that filter to your report.</span></span>

![Options d’état de la protection contre les menaces pour l’Explorateur de menaces](../../media/ThreatExplorerProtectionStatusOptions.png)

<span data-ttu-id="924d7-150">Sous le graphique, affichez plus de détails sur des messages spécifiques.</span><span class="sxs-lookup"><span data-stu-id="924d7-150">Below the chart, view more details about specific messages.</span></span> <span data-ttu-id="924d7-151">Lorsque vous sélectionnez un élément dans la liste, un volet volant s’ouvre, où vous pouvez en savoir plus sur l’élément que vous avez sélectionné.</span><span class="sxs-lookup"><span data-stu-id="924d7-151">When you select an item in the list, a fly-out pane opens, where you can learn more about the item you selected.</span></span>

![Explorateur de menaces avec le flyout ouvert](../../media/ThreatExplorerMalwareItemSelectedFlyout.png)

## <a name="email--phish"></a><span data-ttu-id="924d7-153">Hameçonnage > courrier électronique</span><span class="sxs-lookup"><span data-stu-id="924d7-153">Email > Phish</span></span>

<span data-ttu-id="924d7-154">Pour afficher ce rapport, dans l’Explorateur (ou détections en temps réel), choisissez **Afficher le** \> **hameçonnage de** \> **messagerie.**</span><span class="sxs-lookup"><span data-stu-id="924d7-154">To view this report, in Explorer (or real-time detections), choose **View** \> **Email** \> **Phish**.</span></span> <span data-ttu-id="924d7-155">Cet affichage affiche les messages électroniques identifiés comme tentatives de hameçonnage.</span><span class="sxs-lookup"><span data-stu-id="924d7-155">This view shows email messages identified as phishing attempts.</span></span>

![Afficher les données relatives aux e-mails identifiés comme tentatives d’hameçonnage](../../media/ThreatExplorerEmailPhish.png)

<span data-ttu-id="924d7-157">Cliquez **sur Expéditeur** pour ouvrir votre liste d’options d’affichage.</span><span class="sxs-lookup"><span data-stu-id="924d7-157">Click **Sender** to open your list of viewing options.</span></span> <span data-ttu-id="924d7-158">Cette liste permet d’afficher les données par expéditeur, destinataire, domaine de l’expéditeur, adresse IP de l’expéditeur, domaine d’URL, verdict de clic, etc.</span><span class="sxs-lookup"><span data-stu-id="924d7-158">Use this list to view data by sender, recipients, sender domain, sender IP, URL domain, click verdict, and more.</span></span>

<span data-ttu-id="924d7-159">Par exemple, pour voir les actions qui ont été entreprises lorsque des utilisateurs  ont cliqué sur des URL identifiées comme tentatives d’hameçonnage, choisissez Verdict de clic dans la liste, sélectionnez une ou plusieurs options, puis cliquez sur le bouton Actualiser.</span><span class="sxs-lookup"><span data-stu-id="924d7-159">For example, to see what actions were taken when people clicked on URLs that were identified as phishing attempts, choose **Click verdict** in the list, select one or more options, and then click the Refresh button.</span></span>

![Cliquez sur options de verdict pour le rapport d’hameçonnage](../../media/ThreatExplorerEmailPhishClickVerdictOptions.png)

<span data-ttu-id="924d7-161">Sous le graphique, affichez plus de détails sur des messages spécifiques, des clics d’URL, des URL et l’origine du courrier électronique.</span><span class="sxs-lookup"><span data-stu-id="924d7-161">Below the chart, view more details about specific messages, URL clicks, URLs, and email origin.</span></span>

![URL détectées comme hameçonnage dans les messages électroniques](../../media/ThreatExplorerEmailPhishURLs.png)

<span data-ttu-id="924d7-163">Lorsque vous sélectionnez un élément dans la liste, tel qu’une URL détectée, un volet volant s’ouvre, où vous pouvez en savoir plus sur l’élément que vous avez sélectionné.</span><span class="sxs-lookup"><span data-stu-id="924d7-163">When you select an item in the list, such as a URL that was detected, a fly-out pane opens, where you can learn more about the item you selected.</span></span>

![Détails sur une URL détectée](../../media/ThreatExplorerEmailPhishURLDetails.png)

## <a name="email--submissions"></a><span data-ttu-id="924d7-165">Envois > courrier électronique</span><span class="sxs-lookup"><span data-stu-id="924d7-165">Email > Submissions</span></span>

<span data-ttu-id="924d7-166">Pour afficher ce rapport, dans l’Explorateur (ou détections en temps réel), choisissez **Afficher les** \>  \> **envois de courrier électronique.**</span><span class="sxs-lookup"><span data-stu-id="924d7-166">To view this report, in Explorer (or real-time detections), choose **View** \> **Email** \> **Submissions**.</span></span> <span data-ttu-id="924d7-167">Cette vue affiche les messages électroniques que les utilisateurs ont signalés comme courrier indésirable, non indésirable ou hameçonnage.</span><span class="sxs-lookup"><span data-stu-id="924d7-167">This view shows email that users have reported as junk, not junk, or phishing email.</span></span>

![Messages électroniques signalés par les utilisateurs](../../media/ThreatExplorerEmailUserReportedViewOptions.png)

<span data-ttu-id="924d7-169">Cliquez **sur Expéditeur** pour ouvrir votre liste d’options d’affichage.</span><span class="sxs-lookup"><span data-stu-id="924d7-169">Click **Sender** to open your list of viewing options.</span></span> <span data-ttu-id="924d7-170">Cette liste permet d’afficher des informations par expéditeur, destinataire, type de rapport (la détermination de l’utilisateur que le courrier était indésirable, non indésirable ou hameçonnage), et bien plus encore.</span><span class="sxs-lookup"><span data-stu-id="924d7-170">Use this list to view information by sender, recipients, report type (the user's determination that the email was junk, not junk, or phish), and more.</span></span>

<span data-ttu-id="924d7-171">Par exemple, pour afficher des informations sur les messages  électroniques signalés comme tentatives d’hameçonnage, cliquez sur Type de rapport de l’expéditeur, sélectionnez Hameçonnage, puis cliquez sur le \> bouton Actualiser. </span><span class="sxs-lookup"><span data-stu-id="924d7-171">For example, to view information about email messages that were reported as phishing attempts, click **Sender** \> **Report type**, select **Phish**, and then click the Refresh button.</span></span>

![Hameçonnage sélectionné pour le filtre Type de rapport](../../media/ThreatExplorerEmailUserReportedPhishSelected.png)

<span data-ttu-id="924d7-173">Sous le graphique, affichez plus de détails sur des messages électroniques spécifiques, tels que la ligne d’objet, l’adresse IP de l’expéditeur, l’utilisateur qui a signalé le message comme courrier indésirable, non indésirable ou hameçonnage, etc.</span><span class="sxs-lookup"><span data-stu-id="924d7-173">Below the chart, view more details about specific email messages, such as subject line, the sender's IP address, the user that reported the message as junk, not junk, or phish, and more.</span></span>

![Messages signalés comme tentatives de hameçonnage](../../media/ThreatExplorerEmailPhishUserReportedPhishDetails.png)

<span data-ttu-id="924d7-175">Sélectionnez un élément dans la liste pour afficher des détails supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="924d7-175">Select an item in the list to view additional details.</span></span>

## <a name="email--all-email"></a><span data-ttu-id="924d7-176">Courrier électronique > tous les messages électroniques</span><span class="sxs-lookup"><span data-stu-id="924d7-176">Email > All email</span></span>

<span data-ttu-id="924d7-177">Pour afficher ce rapport, dans l’Explorateur, choisissez **Afficher tous** \> **les messages** \> **électroniques.**</span><span class="sxs-lookup"><span data-stu-id="924d7-177">To view this report, in Explorer, choose **View** \> **Email** \> **All mail**.</span></span> <span data-ttu-id="924d7-178">Cette vue présente une vue d’ensemble de l’activité de messagerie, y compris les e-mails identifiés comme malveillants en raison de l’hameçonnage ou des programmes malveillants, ainsi que tous les messages non malveillants (courrier électronique normal, courrier indésirable et courrier en nombre).</span><span class="sxs-lookup"><span data-stu-id="924d7-178">This views shows an all-up view of email activity, including email identified as malicious due to phishing or malware, as well all non-malicious mail (normal email, spam, and bulk mail).</span></span>

> [!NOTE]
> <span data-ttu-id="924d7-179">Si vous obtenez une erreur qui lit trop de données à **afficher,** ajoutez un filtre et, si nécessaire, réduisez la plage de dates que vous affichez.</span><span class="sxs-lookup"><span data-stu-id="924d7-179">If you get an error that reads **Too much data to display**, add a filter and, if necessary, narrow the date range you're viewing.</span></span>

<span data-ttu-id="924d7-180">Pour appliquer un filtre, choisissez **Expéditeur,** sélectionnez un élément dans la liste, puis cliquez sur le bouton Actualiser.</span><span class="sxs-lookup"><span data-stu-id="924d7-180">To apply a filter, choose **Sender**, select an item in the list, and then click the Refresh button.</span></span> <span data-ttu-id="924d7-181">Dans notre exemple, nous avons utilisé **la technologie De détection** comme filtre (plusieurs options sont disponibles).</span><span class="sxs-lookup"><span data-stu-id="924d7-181">In our example, we used **Detection technology** as a filter (there are several options available).</span></span> <span data-ttu-id="924d7-182">Afficher les informations par expéditeur, domaine de l’expéditeur, destinataires, objet, nom de fichier de pièce jointe, famille de programmes malveillants, état de protection (actions prises par vos fonctionnalités et stratégies de protection contre les menaces dans Office 365), technologie de détection (détection des programmes malveillants) et bien plus encore.</span><span class="sxs-lookup"><span data-stu-id="924d7-182">View information by sender, sender's domain, recipients, subject, attachment filename, malware family, protection status (actions taken by your threat protection features and policies in Office 365), detection technology (how the malware was detected), and more.</span></span>

![Afficher les données sur le courrier électronique détecté par la technologie de détection](../../media/0c032eb3-6021-4174-9f06-ff8f30c245ca.png)

<span data-ttu-id="924d7-184">Sous le graphique, affichez plus de détails sur des messages électroniques spécifiques, tels que la ligne d’objet, le destinataire, l’expéditeur, l’état, etc.</span><span class="sxs-lookup"><span data-stu-id="924d7-184">Below the chart, view more details about specific email messages, such as subject line, recipient, sender, status, and so on.</span></span>

## <a name="content--malware"></a><span data-ttu-id="924d7-185">Programme malveillant > contenu</span><span class="sxs-lookup"><span data-stu-id="924d7-185">Content > Malware</span></span>

<span data-ttu-id="924d7-186">Pour afficher ce rapport, dans l’Explorateur (ou détections en temps réel), choisissez **Afficher les** programmes \> **malveillants de** \> **contenu.**</span><span class="sxs-lookup"><span data-stu-id="924d7-186">To view this report, in Explorer (or real-time detections), choose **View** \> **Content** \> **Malware**.</span></span> <span data-ttu-id="924d7-187">Cette vue affiche les fichiers identifiés comme malveillants par Microsoft Defender pour [Office 365 dans SharePoint Online, OneDrive](mdo-for-spo-odb-and-teams.md)Entreprise et Microsoft Teams.</span><span class="sxs-lookup"><span data-stu-id="924d7-187">This view shows files that were identified as malicious by [Microsoft Defender for Office 365 in SharePoint Online, OneDrive for Business, and Microsoft Teams](mdo-for-spo-odb-and-teams.md).</span></span>

<span data-ttu-id="924d7-188">Afficher les informations par famille de programmes malveillants, technologie de détection (détection des programmes malveillants) et charge de travail (OneDrive, SharePoint ou Teams).</span><span class="sxs-lookup"><span data-stu-id="924d7-188">View information by malware family, detection technology (how the malware was detected), and workload (OneDrive, SharePoint, or Teams).</span></span>

![Afficher les données sur les programmes malveillants détectés](../../media/d11dc568-b091-4159-b261-df13d76b520b.png)

<span data-ttu-id="924d7-190">Sous le graphique, affichez plus de détails sur des fichiers spécifiques, tels que le nom de fichier de pièce jointe, la charge de travail, la taille du fichier, qui a modifié le fichier en dernier, et bien plus encore.</span><span class="sxs-lookup"><span data-stu-id="924d7-190">Below the chart, view more details about specific files, such as attachment filename, workload, file size, who last modified the file, and more.</span></span>

## <a name="click-to-filter-capabilities"></a><span data-ttu-id="924d7-191">Fonctionnalités « Cliquer pour filtrer »</span><span class="sxs-lookup"><span data-stu-id="924d7-191">Click-to-filter capabilities</span></span>

<span data-ttu-id="924d7-192">Avec l’Explorateur (et les détections en temps réel), vous pouvez appliquer un filtre en un clic.</span><span class="sxs-lookup"><span data-stu-id="924d7-192">With Explorer (and real-time detections), you can apply a filter in a click.</span></span> <span data-ttu-id="924d7-193">Cliquez sur un élément dans la légende et cet élément devient un filtre pour le rapport.</span><span class="sxs-lookup"><span data-stu-id="924d7-193">Click an item in the legend, and that item becomes a filter for the report.</span></span> <span data-ttu-id="924d7-194">Par exemple, supposons que nous regardions la vue Programmes malveillants dans l’Explorateur :</span><span class="sxs-lookup"><span data-stu-id="924d7-194">For example, suppose we are looking at the Malware view in Explorer:</span></span>

![Accès à l’Explorateur de gestion des \> menaces](../../media/cab32fa2-66f1-4ad5-bc1d-2bac4dbeb48c.png)

<span data-ttu-id="924d7-196">Le fait de **cliquer sur la déstonation atp** dans ce graphique entraîne une vue comme celle-ci :</span><span class="sxs-lookup"><span data-stu-id="924d7-196">Clicking **ATP Detonation** in this chart results in a view like this:</span></span>

![Explorateur filtré pour afficher uniquement les résultats de la détonation de Defender pour Office 365](../../media/7241d7dd-27bc-467d-9db8-6e806c49df14.png)

<span data-ttu-id="924d7-198">Dans cette vue, nous regardons maintenant les données des fichiers qui ont été détonés par des [pièces jointes sécurisées.](safe-attachments.md)</span><span class="sxs-lookup"><span data-stu-id="924d7-198">In this view, we are now looking at data for files that were detonated by [Safe Attachments](safe-attachments.md).</span></span> <span data-ttu-id="924d7-199">Sous le graphique, nous pouvons voir des détails sur des messages électroniques spécifiques dont les pièces jointes ont été détectées par des pièces jointes sécurisées.</span><span class="sxs-lookup"><span data-stu-id="924d7-199">Below the chart, we can see details about specific email messages that had attachments that were detected by Safe Attachments.</span></span>

![Détails spécifiques sur les messages électroniques avec pièces jointes détectées](../../media/c91fb05c-d1d4-4085-acc6-f7008a415c2a.png)

<span data-ttu-id="924d7-201">La sélection d’un ou de plusieurs éléments active le menu **Actions,** qui propose plusieurs choix parmi lesquels choisir les éléments sélectionnés.</span><span class="sxs-lookup"><span data-stu-id="924d7-201">Selecting one or more items activates the **Actions** menu, which offers several choices from which to choose for the selected item(s).</span></span>

![La sélection d’un élément active le menu Actions](../../media/95f127a4-1b2a-4a76-88b9-096e3ba27d1b.png)

<span data-ttu-id="924d7-203">La possibilité de filtrer en un clic et d’accéder à des détails spécifiques peut vous faire gagner beaucoup de temps pour examiner les menaces.</span><span class="sxs-lookup"><span data-stu-id="924d7-203">The ability to filter in a click and navigate to specific details can save you a lot of time in investigating threats.</span></span>

## <a name="queries-and-filters"></a><span data-ttu-id="924d7-204">Requêtes et filtres</span><span class="sxs-lookup"><span data-stu-id="924d7-204">Queries and filters</span></span>

<span data-ttu-id="924d7-205">L’Explorateur (ainsi que le rapport de détections en temps réel) dispose de plusieurs filtres et fonctionnalités d’interrogation puissants qui vous permettent d’explorer des détails, tels que les utilisateurs les plus ciblés, les principales familles de programmes malveillants, la technologie de détection et bien plus encore.</span><span class="sxs-lookup"><span data-stu-id="924d7-205">Explorer (as well as the real-time detections report) has several powerful filters and querying capabilities that enable you to drill into details, such as top targeted users, top malware families, detection technology and more.</span></span> <span data-ttu-id="924d7-206">Chaque type de rapport offre de nombreuses façons d’afficher et d’explorer des données.</span><span class="sxs-lookup"><span data-stu-id="924d7-206">Each kind of report offers a variety of ways to view and explore data.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="924d7-207">N’utilisez pas de caractères génériques, tels qu’un astérisque ou un point d’interrogation, dans la barre de requête de l’Explorateur (ou détections en temps réel).</span><span class="sxs-lookup"><span data-stu-id="924d7-207">Do not use wildcard characters, such as an asterisk or a question mark, in the query bar for Explorer (or real-time detections).</span></span> <span data-ttu-id="924d7-208">Lorsque vous recherchez des messages électroniques dans le champ Objet, l’Explorateur (ou détections en temps réel) effectue une correspondance partielle et produit des résultats semblables à une recherche par caractères génériques. </span><span class="sxs-lookup"><span data-stu-id="924d7-208">When you search on the **Subject field** for email messages, Explorer (or real-time detections) will perform partial matching and yield results similar to a wildcard search.</span></span>
