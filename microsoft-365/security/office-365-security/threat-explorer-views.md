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
ms.service: O365-seccomp
localization_priority: Normal
search.appverid: ''
ms.collection:
- M365-security-compliance
- m365initiative-defender-office365
description: Découvrez comment utiliser l’Explorateur de menaces et le rapport de détection en temps réel pour examiner les menaces et y répondre dans le &amp; Centre de sécurité conformité.
ms.custom: seo-marvel-apr2020
ms.openlocfilehash: 75286b3fa8319afc9baadbc7ed349e8fe689d11c
ms.sourcegitcommit: 9a764c2aed7338c37f6e92f5fb487f02b3c4dfa1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/13/2020
ms.locfileid: "48447130"
---
# <a name="views-in-threat-explorer-and-real-time-detections"></a><span data-ttu-id="63970-103">Affichages dans l’Explorateur de menaces et détections en temps réel</span><span class="sxs-lookup"><span data-stu-id="63970-103">Views in Threat Explorer and real-time detections</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../includes/microsoft-defender-for-office.md)]


![Threat Explorer](../../media/ThreatExplorerFirstOpened.png)

<span data-ttu-id="63970-105">L' [Explorateur de menaces](threat-explorer.md) (et le rapport de détections en temps réel) est un outil puissant, en temps réel, qui permet aux équipes des opérations de sécurité d’examiner et de répondre aux menaces dans le centre de sécurité &amp; conformité.</span><span class="sxs-lookup"><span data-stu-id="63970-105">[Threat Explorer](threat-explorer.md) (and the real-time detections report) is a powerful, near real-time tool to help Security Operations teams investigate and respond to threats in the Security &amp; Compliance Center.</span></span> <span data-ttu-id="63970-106">Explorer (et le rapport de détections en temps réel) affiche des informations sur les programmes malveillants et les messages hameçons suspects dans des e-mails et des fichiers dans Office 365, ainsi que d’autres menaces et risques de sécurité pour votre organisation.</span><span class="sxs-lookup"><span data-stu-id="63970-106">Explorer (and the real-time detections report) displays information about suspected malware and phish in email and files in Office 365, as well as other security threats and risks to your organization.</span></span>

- <span data-ttu-id="63970-107">Si vous disposez d' [Office 365 Advanced Threat Protection](office-365-atp.md) (ATP) plan 2, vous disposez de l’Explorateur.</span><span class="sxs-lookup"><span data-stu-id="63970-107">If you have [Office 365 Advanced Threat Protection](office-365-atp.md) (ATP) Plan 2, then you have Explorer.</span></span>
- <span data-ttu-id="63970-108">Si vous disposez d’Office 365 DAV plan 1, vous disposez de détections en temps réel.</span><span class="sxs-lookup"><span data-stu-id="63970-108">If you have Office 365 ATP Plan 1, then you have real-time detections.</span></span>

<span data-ttu-id="63970-109">Lorsque vous ouvrez l’Explorateur (ou le rapport de détection en temps réel) pour la première fois, la vue par défaut affiche les détections de programmes malveillants de messagerie pour les 7 derniers jours.</span><span class="sxs-lookup"><span data-stu-id="63970-109">When you first open Explorer (or the real-time detections report), the default view shows email malware detections for the past 7 days.</span></span> <span data-ttu-id="63970-110">Ce rapport peut également afficher des détections ATP, telles que les URL malveillantes détectées par les [liens fiables](atp-safe-links.md)et les fichiers malveillants détectés par des [pièces jointes fiables](atp-safe-attachments.md).</span><span class="sxs-lookup"><span data-stu-id="63970-110">This report can also show ATP detections, such as malicious URLs detected by [Safe Links](atp-safe-links.md), and malicious files detected by [Safe Attachments](atp-safe-attachments.md).</span></span> <span data-ttu-id="63970-111">Ce rapport peut être modifié pour afficher les données des 30 derniers jours (avec un abonnement payant P2 ATP).</span><span class="sxs-lookup"><span data-stu-id="63970-111">This report can be modified to show data for the past 30 days (with an ATP P2 paid subscription).</span></span> <span data-ttu-id="63970-112">Les abonnements à la version d’évaluation incluent des données pour les sept derniers jours.</span><span class="sxs-lookup"><span data-stu-id="63970-112">Trial subscriptions will include data for the past seven days only.</span></span>

****

|<span data-ttu-id="63970-113">Abonnement</span><span class="sxs-lookup"><span data-stu-id="63970-113">Subscription</span></span>|<span data-ttu-id="63970-114">Utilitaire</span><span class="sxs-lookup"><span data-stu-id="63970-114">Utility</span></span>|<span data-ttu-id="63970-115">Jours de données</span><span class="sxs-lookup"><span data-stu-id="63970-115">Days of Data</span></span>|
|---|---|---|
|<span data-ttu-id="63970-116">Version d’évaluation de l’ATP P1</span><span class="sxs-lookup"><span data-stu-id="63970-116">ATP P1 trial</span></span>|<span data-ttu-id="63970-117">Détections en temps réel</span><span class="sxs-lookup"><span data-stu-id="63970-117">Real-time detections</span></span>|<span data-ttu-id="63970-118">7 </span><span class="sxs-lookup"><span data-stu-id="63970-118">7</span></span>|
|<span data-ttu-id="63970-119">ATP P1 payé</span><span class="sxs-lookup"><span data-stu-id="63970-119">ATP P1 paid</span></span>|<span data-ttu-id="63970-120">Détections en temps réel</span><span class="sxs-lookup"><span data-stu-id="63970-120">Real-time detections</span></span>|<span data-ttu-id="63970-121">0,30</span><span class="sxs-lookup"><span data-stu-id="63970-121">30</span></span>|
|<span data-ttu-id="63970-122">Version d’évaluation de l’ATP P2, tests sponsorisés P1</span><span class="sxs-lookup"><span data-stu-id="63970-122">ATP P1 paid testing ATP P2 trial</span></span>|<span data-ttu-id="63970-123">Threat Explorer</span><span class="sxs-lookup"><span data-stu-id="63970-123">Threat Explorer</span></span>|<span data-ttu-id="63970-124">7 </span><span class="sxs-lookup"><span data-stu-id="63970-124">7</span></span>|
|<span data-ttu-id="63970-125">Version d’évaluation de l’ATP P2</span><span class="sxs-lookup"><span data-stu-id="63970-125">ATP P2 trial</span></span>|<span data-ttu-id="63970-126">Threat Explorer</span><span class="sxs-lookup"><span data-stu-id="63970-126">Threat Explorer</span></span>|<span data-ttu-id="63970-127">7 </span><span class="sxs-lookup"><span data-stu-id="63970-127">7</span></span>|
|<span data-ttu-id="63970-128">ATP P2 payé</span><span class="sxs-lookup"><span data-stu-id="63970-128">ATP P2 paid</span></span>|<span data-ttu-id="63970-129">Threat Explorer</span><span class="sxs-lookup"><span data-stu-id="63970-129">Threat Explorer</span></span>|<span data-ttu-id="63970-130">0,30</span><span class="sxs-lookup"><span data-stu-id="63970-130">30</span></span>|
|

<span data-ttu-id="63970-131">Utilisez le menu **affichage** pour modifier les informations affichées.</span><span class="sxs-lookup"><span data-stu-id="63970-131">Use the **View** menu to change what information is displayed.</span></span> <span data-ttu-id="63970-132">Les info-bulles vous aident à déterminer l’affichage à utiliser.</span><span class="sxs-lookup"><span data-stu-id="63970-132">Tooltips help you determine which view to use.</span></span>

![Menu Affichage de l’Explorateur de menaces](../../media/ThreatExplorerViewMenu.png)

<span data-ttu-id="63970-134">Une fois que vous avez sélectionné un affichage, vous pouvez appliquer des filtres et configurer des requêtes pour effectuer une analyse plus poussée.</span><span class="sxs-lookup"><span data-stu-id="63970-134">Once you have selected a view, you can apply filters and set up queries to conduct further analysis.</span></span> <span data-ttu-id="63970-135">Les sections suivantes fournissent un bref aperçu des différentes vues disponibles dans l’Explorateur (ou les détections en temps réel).</span><span class="sxs-lookup"><span data-stu-id="63970-135">The following sections provide a brief overview of the various views available in Explorer (or real-time detections).</span></span>

## <a name="email--malware"></a><span data-ttu-id="63970-136">Courrier électronique > programme malveillant</span><span class="sxs-lookup"><span data-stu-id="63970-136">Email > Malware</span></span>

<span data-ttu-id="63970-137">Pour afficher ce rapport, dans l’Explorateur (ou les détections en temps réel), sélectionnez **Afficher**les  >  **Email**  >  **programmes malveillants**de messagerie.</span><span class="sxs-lookup"><span data-stu-id="63970-137">To view this report, in Explorer (or real-time detections), choose **View** > **Email** > **Malware**.</span></span> <span data-ttu-id="63970-138">Cette vue affiche des informations sur les messages électroniques identifiés comme contenant des programmes malveillants.</span><span class="sxs-lookup"><span data-stu-id="63970-138">This view shows information about email messages that were identified as containing malware.</span></span>

![Afficher les données sur le courrier électronique identifié comme programme malveillant](../../media/ExplorerEmailMalwareMenu.png)

<span data-ttu-id="63970-140">Cliquez sur **expéditeur** pour ouvrir votre liste d’options d’affichage.</span><span class="sxs-lookup"><span data-stu-id="63970-140">Click **Sender** to open your list of viewing options.</span></span> <span data-ttu-id="63970-141">Utilisez cette liste pour afficher les données par expéditeur, destinataires, domaine de l’expéditeur, objet, technologie de détection, état de protection, etc.</span><span class="sxs-lookup"><span data-stu-id="63970-141">Use this list to view data by sender, recipients, sender domain, subject, detection technology, protection status, and more.</span></span>

<span data-ttu-id="63970-142">Par exemple, pour voir les actions qui ont été effectuées sur les messages électroniques détectés, choisissez **État de protection** dans la liste.</span><span class="sxs-lookup"><span data-stu-id="63970-142">For example, to see what actions were taken on detected email messages, choose **Protection status** in the list.</span></span> <span data-ttu-id="63970-143">Sélectionnez une option, puis cliquez sur le bouton Actualiser pour appliquer ce filtre à votre rapport.</span><span class="sxs-lookup"><span data-stu-id="63970-143">Select an option, and then click the Refresh button to apply that filter to your report.</span></span>

![Options d’état de protection contre les menaces pour l’Explorateur de menaces](../../media/ThreatExplorerProtectionStatusOptions.png)

<span data-ttu-id="63970-145">Sous le graphique, affichez plus de détails sur des messages spécifiques.</span><span class="sxs-lookup"><span data-stu-id="63970-145">Below the chart, view more details about specific messages.</span></span> <span data-ttu-id="63970-146">Lorsque vous sélectionnez un élément dans la liste, un volet de survol s’ouvre, dans lequel vous pouvez en savoir plus sur l’élément que vous avez sélectionné.</span><span class="sxs-lookup"><span data-stu-id="63970-146">When you select an item in the list, a fly-out pane opens, where you can learn more about the item you selected.</span></span>

![Explorateur de menaces avec le lanceur ouvert](../../media/ThreatExplorerMalwareItemSelectedFlyout.png)

## <a name="email--phish"></a><span data-ttu-id="63970-148">Courrier électronique > hameçonnage</span><span class="sxs-lookup"><span data-stu-id="63970-148">Email > Phish</span></span>

<span data-ttu-id="63970-149">Pour afficher ce rapport, dans l’Explorateur (ou les détections en temps réel), sélectionnez **Afficher**le  >  **hameçonnage par courrier électronique**  >  **Phish**.</span><span class="sxs-lookup"><span data-stu-id="63970-149">To view this report, in Explorer (or real-time detections), choose **View** > **Email** > **Phish**.</span></span> <span data-ttu-id="63970-150">Cet affichage montre les messages électroniques identifiés comme des tentatives de hameçonnage.</span><span class="sxs-lookup"><span data-stu-id="63970-150">This view shows email messages identified as phishing attempts.</span></span>

![Afficher les données sur l’e-mail identifiées comme tentatives de hameçonnage](../../media/ThreatExplorerEmailPhish.png)

<span data-ttu-id="63970-152">Cliquez sur **expéditeur** pour ouvrir votre liste d’options d’affichage.</span><span class="sxs-lookup"><span data-stu-id="63970-152">Click **Sender** to open your list of viewing options.</span></span> <span data-ttu-id="63970-153">Utilisez cette liste pour afficher les données par expéditeur, destinataires, domaine de l’expéditeur, adresse IP de l’expéditeur, domaine de l’URL, cliquez sur verdict, etc.</span><span class="sxs-lookup"><span data-stu-id="63970-153">Use this list to view data by sender, recipients, sender domain, sender IP, URL domain, click verdict, and more.</span></span>

<span data-ttu-id="63970-154">Par exemple, pour voir les actions qui ont été effectuées lorsque des utilisateurs cliquaient sur des URL identifiées comme tentatives de hameçonnage, choisissez **cliquer sur verdict** dans la liste, sélectionnez une ou plusieurs options, puis cliquez sur le bouton Actualiser.</span><span class="sxs-lookup"><span data-stu-id="63970-154">For example, to see what actions were taken when people clicked on URLs that were identified as phishing attempts, choose **Click verdict** in the list, select one or more options, and then click the Refresh button.</span></span>

![Cliquez sur options de verdict pour le rapport de hameçonnage.](../../media/ThreatExplorerEmailPhishClickVerdictOptions.png)

<span data-ttu-id="63970-156">Sous le graphique, affichez plus de détails sur des messages spécifiques, des clics d’URL, des URL et de l’origine du courrier électronique.</span><span class="sxs-lookup"><span data-stu-id="63970-156">Below the chart, view more details about specific messages, URL clicks, URLs, and email origin.</span></span>

![URL détectées comme hameçonnage dans les messages électroniques](../../media/ThreatExplorerEmailPhishURLs.png)

<span data-ttu-id="63970-158">Lorsque vous sélectionnez un élément dans la liste, tel qu’une URL qui a été détectée, un volet de survol s’ouvre, dans lequel vous pouvez en savoir plus sur l’élément que vous avez sélectionné.</span><span class="sxs-lookup"><span data-stu-id="63970-158">When you select an item in the list, such as a URL that was detected, a fly-out pane opens, where you can learn more about the item you selected.</span></span>

![Détails sur une URL détectée](../../media/ThreatExplorerEmailPhishURLDetails.png)

## <a name="email--submissions"></a><span data-ttu-id="63970-160">Envois de > de messagerie</span><span class="sxs-lookup"><span data-stu-id="63970-160">Email > Submissions</span></span>

<span data-ttu-id="63970-161">Pour afficher ce rapport, dans l’Explorateur (ou les détections en temps réel), sélectionnez **Afficher**les  >  **Email**  >  **envois**de courrier.</span><span class="sxs-lookup"><span data-stu-id="63970-161">To view this report, in Explorer (or real-time detections), choose **View** > **Email** > **Submissions**.</span></span> <span data-ttu-id="63970-162">Cet affichage montre le courrier électronique que les utilisateurs ont signalés comme courrier indésirable, non légitime ou courrier électronique de hameçonnage.</span><span class="sxs-lookup"><span data-stu-id="63970-162">This view shows email that users have reported as junk, not junk, or phishing email.</span></span>

![Messages électroniques signalés par les utilisateurs](../../media/ThreatExplorerEmailUserReportedViewOptions.png)

<span data-ttu-id="63970-164">Cliquez sur **expéditeur** pour ouvrir votre liste d’options d’affichage.</span><span class="sxs-lookup"><span data-stu-id="63970-164">Click **Sender** to open your list of viewing options.</span></span> <span data-ttu-id="63970-165">Cette liste permet d’afficher des informations par expéditeur, destinataires, type de rapport (l’utilisateur a déterminé que le courrier électronique a été légitime, non légitime ou hameçon), et bien plus encore.</span><span class="sxs-lookup"><span data-stu-id="63970-165">Use this list to view information by sender, recipients, report type (the user's determination that the email was junk, not junk, or phish), and more.</span></span>

<span data-ttu-id="63970-166">Par exemple, pour afficher les informations sur les messages électroniques qui ont été signalés en tant **Sender**que tentatives de hameçonnage, cliquez sur  >  **type de rapport**de l’expéditeur, sélectionnez **hameçonnage**, puis cliquez sur le bouton Actualiser.</span><span class="sxs-lookup"><span data-stu-id="63970-166">For example, to view information about email messages that were reported as phishing attempts, click **Sender** > **Report type**, select **Phish**, and then click the Refresh button.</span></span>

![Hameçonnage sélectionné pour le filtre de type de rapport](../../media/ThreatExplorerEmailUserReportedPhishSelected.png)

<span data-ttu-id="63970-168">Sous le graphique, affichez plus de détails sur des messages électroniques spécifiques, tels que la ligne d’objet, l’adresse IP de l’expéditeur, l’utilisateur qui a signalé le message comme courrier indésirable, légitime, ou hameçon, et bien plus encore.</span><span class="sxs-lookup"><span data-stu-id="63970-168">Below the chart, view more details about specific email messages, such as subject line, the sender's IP address, the user that reported the message as junk, not junk, or phish, and more.</span></span>

![Messages qui ont été signalés en tant que tentatives de hameçonnage](../../media/ThreatExplorerEmailPhishUserReportedPhishDetails.png)

<span data-ttu-id="63970-170">Sélectionnez un élément dans la liste pour afficher des détails supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="63970-170">Select an item in the list to view additional details.</span></span>

## <a name="email--all-email"></a><span data-ttu-id="63970-171">Courrier électronique > tous les messages électroniques</span><span class="sxs-lookup"><span data-stu-id="63970-171">Email > All email</span></span>

<span data-ttu-id="63970-172">Pour afficher ce rapport, dans l’Explorateur, sélectionnez **Afficher**le courrier  >  **électronique**de  >  **tous les messages**.</span><span class="sxs-lookup"><span data-stu-id="63970-172">To view this report, in Explorer, choose **View** > **Email** > **All mail**.</span></span> <span data-ttu-id="63970-173">Cette vue affiche une vue d’ensemble de l’activité de messagerie, y compris le courrier électronique identifié comme malveillant en raison d’un hameçonnage ou d’un programme malveillant, ainsi que tous les messages non malveillants (e-mail normal, courrier indésirable et courrier en nombre).</span><span class="sxs-lookup"><span data-stu-id="63970-173">This views shows an all-up view of email activity, including email identified as malicious due to phishing or malware, as well all non-malicious mail (normal email, spam, and bulk mail).</span></span>

> [!NOTE]
> <span data-ttu-id="63970-174">Si vous obtenez une erreur indiquant un **trop grand nombre de données à afficher**, ajoutez un filtre et, si nécessaire, Affinez la plage de dates que vous visualisez.</span><span class="sxs-lookup"><span data-stu-id="63970-174">If you get an error that reads **Too much data to display**, add a filter and, if necessary, narrow the date range you're viewing.</span></span>

<span data-ttu-id="63970-175">Pour appliquer un filtre, choisissez **expéditeur**, sélectionnez un élément dans la liste, puis cliquez sur le bouton Actualiser.</span><span class="sxs-lookup"><span data-stu-id="63970-175">To apply a filter, choose **Sender**, select an item in the list, and then click the Refresh button.</span></span> <span data-ttu-id="63970-176">Dans notre exemple, nous avons utilisé la **technologie de détection** en tant que filtre (plusieurs options sont disponibles).</span><span class="sxs-lookup"><span data-stu-id="63970-176">In our example, we used **Detection technology** as a filter (there are several options available).</span></span> <span data-ttu-id="63970-177">Afficher les informations par expéditeur, domaine de l’expéditeur, destinataires, objet, nom de fichier de la pièce jointe, famille de programmes malveillants, statut de protection (actions effectuées par vos stratégies et fonctionnalités de protection contre les menaces dans Office 365), technologie de détection (comment le programme malveillant a été détecté), et plus encore.</span><span class="sxs-lookup"><span data-stu-id="63970-177">View information by sender, sender's domain, recipients, subject, attachment filename, malware family, protection status (actions taken by your threat protection features and policies in Office 365), detection technology (how the malware was detected), and more.</span></span>

![Afficher les données sur les messages détectés par la technologie de détection](../../media/0c032eb3-6021-4174-9f06-ff8f30c245ca.png)

<span data-ttu-id="63970-179">Sous le graphique, affichez plus de détails sur des messages électroniques spécifiques, tels que la ligne d’objet, le destinataire, l’expéditeur, l’État, etc.</span><span class="sxs-lookup"><span data-stu-id="63970-179">Below the chart, view more details about specific email messages, such as subject line, recipient, sender, status, and so on.</span></span>

## <a name="content--malware"></a><span data-ttu-id="63970-180">Contenu > programme malveillant</span><span class="sxs-lookup"><span data-stu-id="63970-180">Content > Malware</span></span>

<span data-ttu-id="63970-181">Pour afficher ce rapport, dans l’Explorateur (ou les détections en temps réel), sélectionnez **Afficher**le  >  **contenu**  >  **malveillant**.</span><span class="sxs-lookup"><span data-stu-id="63970-181">To view this report, in Explorer (or real-time detections), choose **View** > **Content** > **Malware**.</span></span> <span data-ttu-id="63970-182">Cet affichage montre les fichiers identifiés comme étant malveillants par [Office 365 protection avancée contre les menaces dans SharePoint Online, OneDrive entreprise et Microsoft teams](atp-for-spo-odb-and-teams.md).</span><span class="sxs-lookup"><span data-stu-id="63970-182">This view shows files that were identified as malicious by [Office 365 Advanced Threat Protection in SharePoint Online, OneDrive for Business, and Microsoft Teams](atp-for-spo-odb-and-teams.md).</span></span>

<span data-ttu-id="63970-183">Afficher des informations par famille de programmes malveillants, technologie de détection (comment le programme malveillant a été détecté) et charge de travail (OneDrive, SharePoint ou Teams).</span><span class="sxs-lookup"><span data-stu-id="63970-183">View information by malware family, detection technology (how the malware was detected), and workload (OneDrive, SharePoint, or Teams).</span></span>

![Afficher les données sur les programmes malveillants détectés](../../media/d11dc568-b091-4159-b261-df13d76b520b.png)

<span data-ttu-id="63970-185">Sous le graphique, affichez plus de détails sur des fichiers spécifiques, tels que le nom de fichier de la pièce jointe, la charge de travail, la taille du fichier, la dernière personne qui a modifié le fichier, etc.</span><span class="sxs-lookup"><span data-stu-id="63970-185">Below the chart, view more details about specific files, such as attachment filename, workload, file size, who last modified the file, and more.</span></span>

## <a name="click-to-filter-capabilities"></a><span data-ttu-id="63970-186">Fonctionnalités de cliquer-filtrer</span><span class="sxs-lookup"><span data-stu-id="63970-186">Click-to-filter capabilities</span></span>

<span data-ttu-id="63970-187">Avec l’Explorateur (et les détections en temps réel), vous pouvez appliquer un filtre dans un clic.</span><span class="sxs-lookup"><span data-stu-id="63970-187">With Explorer (and real-time detections), you can apply a filter in a click.</span></span> <span data-ttu-id="63970-188">Cliquez sur un élément dans la légende, et cet élément devient un filtre pour le rapport.</span><span class="sxs-lookup"><span data-stu-id="63970-188">Click an item in the legend, and that item becomes a filter for the report.</span></span> <span data-ttu-id="63970-189">Par exemple, supposons que nous examinons l’affichage programmes malveillants dans l’Explorateur :</span><span class="sxs-lookup"><span data-stu-id="63970-189">For example, suppose we are looking at the Malware view in Explorer:</span></span>

![Accéder à l’Explorateur de gestion des menaces \>](../../media/cab32fa2-66f1-4ad5-bc1d-2bac4dbeb48c.png)

<span data-ttu-id="63970-191">Si vous cliquez sur **détonation** de la protection avancée contre les menaces dans ce graphique, les résultats sont les suivants :</span><span class="sxs-lookup"><span data-stu-id="63970-191">Clicking **ATP Detonation** in this chart results in a view like this:</span></span>

![Explorateur filtré pour afficher uniquement les résultats de la détonation ATP](../../media/7241d7dd-27bc-467d-9db8-6e806c49df14.png)

<span data-ttu-id="63970-193">Dans cet affichage, nous examinons à présent les données des fichiers qui ont été détonants par des [pièces jointes fiables](atp-safe-attachments.md).</span><span class="sxs-lookup"><span data-stu-id="63970-193">In this view, we are now looking at data for files that were detonated by [Safe Attachments](atp-safe-attachments.md).</span></span> <span data-ttu-id="63970-194">Sous le graphique, nous pouvons voir des détails sur des messages électroniques spécifiques qui avaient des pièces jointes détectées par des pièces jointes fiables.</span><span class="sxs-lookup"><span data-stu-id="63970-194">Below the chart, we can see details about specific email messages that had attachments that were detected by Safe Attachments.</span></span>

![Détails spécifiques sur les messages électroniques avec des pièces jointes détectées](../../media/c91fb05c-d1d4-4085-acc6-f7008a415c2a.png)

<span data-ttu-id="63970-196">La sélection d’un ou de plusieurs éléments active le menu **actions** , qui offre plusieurs choix parmi lesquels choisir pour les éléments sélectionnés.</span><span class="sxs-lookup"><span data-stu-id="63970-196">Selecting one or more items activates the **Actions** menu, which offers several choices from which to choose for the selected item(s).</span></span>

![La sélection d’un élément active le menu actions](../../media/95f127a4-1b2a-4a76-88b9-096e3ba27d1b.png)

<span data-ttu-id="63970-198">La possibilité de filtrer un clic et d’accéder à des détails spécifiques peut vous faire gagner du temps lors de l’enquête sur les menaces.</span><span class="sxs-lookup"><span data-stu-id="63970-198">The ability to filter in a click and navigate to specific details can save you a lot of time in investigating threats.</span></span>

## <a name="queries-and-filters"></a><span data-ttu-id="63970-199">Requêtes et filtres</span><span class="sxs-lookup"><span data-stu-id="63970-199">Queries and filters</span></span>

<span data-ttu-id="63970-200">L’Explorateur (ainsi que le rapport de détections en temps réel) dispose de plusieurs filtres et fonctionnalités d’interrogation puissants qui vous permettent d’explorer les détails, tels que les principaux utilisateurs ciblés, les principales familles de logiciels malveillants, la technologie de détection et bien plus encore.</span><span class="sxs-lookup"><span data-stu-id="63970-200">Explorer (as well as the real-time detections report) has several powerful filters and querying capabilities that enable you to drill into details, such as top targeted users, top malware families, detection technology and more.</span></span> <span data-ttu-id="63970-201">Chaque type de rapport offre plusieurs façons d’afficher et d’explorer les données.</span><span class="sxs-lookup"><span data-stu-id="63970-201">Each kind of report offers a variety of ways to view and explore data.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="63970-202">N’utilisez pas de caractères génériques, tels qu’un astérisque ou un point d’interrogation, dans la barre de requête pour l’Explorateur (ou les détections en temps réel).</span><span class="sxs-lookup"><span data-stu-id="63970-202">Do not use wildcard characters, such as an asterisk or a question mark, in the query bar for Explorer (or real-time detections).</span></span> <span data-ttu-id="63970-203">Lorsque vous effectuez une recherche dans le **champ Subject** pour les messages électroniques, l’Explorateur (ou les détections en temps réel) effectue une correspondance partielle et génère des résultats similaires à une recherche par caractères génériques.</span><span class="sxs-lookup"><span data-stu-id="63970-203">When you search on the **Subject field** for email messages, Explorer (or real-time detections) will perform partial matching and yield results similar to a wildcard search.</span></span>
