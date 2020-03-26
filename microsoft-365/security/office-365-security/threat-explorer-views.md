---
title: Affichages dans l’Explorateur de menaces et détections en temps réel
f1.keywords:
- NOCSH
ms.author: tracyp
author: msfttracyp
manager: dansimp
ms.date: 08/07/2019
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid: ''
ms.collection:
- M365-security-compliance
description: Découvrez les différents types d’affichage disponibles dans l’Explorateur de menaces et les détections en temps réel.
ms.openlocfilehash: 7b05ec1346df3bfa428c384a4236a8758e22da28
ms.sourcegitcommit: 58c1b4208a5e231463091573e40696d08fc39b8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/25/2020
ms.locfileid: "42955638"
---
# <a name="views-in-threat-explorer-and-real-time-detections"></a><span data-ttu-id="c1594-103">Affichages dans l’Explorateur de menaces et détections en temps réel</span><span class="sxs-lookup"><span data-stu-id="c1594-103">Views in Threat Explorer and real-time detections</span></span>

![Threat Explorer](../../media/ThreatExplorerFirstOpened.png)

<span data-ttu-id="c1594-105">L' [Explorateur de menaces](threat-explorer.md) (et le rapport de détections en temps réel) est un outil puissant, en temps réel, qui permet aux équipes des opérations de sécurité d’examiner &amp; et de répondre aux menaces dans le centre de sécurité conformité.</span><span class="sxs-lookup"><span data-stu-id="c1594-105">[Threat Explorer](threat-explorer.md) (and the real-time detections report) is a powerful, near real-time tool to help Security Operations teams investigate and respond to threats in the Security &amp; Compliance Center.</span></span> <span data-ttu-id="c1594-106">Explorer (et le rapport de détections en temps réel) affiche des informations sur les programmes malveillants et les messages hameçons suspects dans des e-mails et des fichiers dans Office 365, ainsi que d’autres menaces et risques de sécurité pour votre organisation.</span><span class="sxs-lookup"><span data-stu-id="c1594-106">Explorer (and the real-time detections report) displays information about suspected malware and phish in email and files in Office 365, as well as other security threats and risks to your organization.</span></span> 

- <span data-ttu-id="c1594-107">Si vous disposez d' [Office 365 Advanced Threat Protection](office-365-atp.md) (ATP) plan 2, vous disposez de l’Explorateur.</span><span class="sxs-lookup"><span data-stu-id="c1594-107">If you have [Office 365 Advanced Threat Protection](office-365-atp.md) (ATP) Plan 2, then you have Explorer.</span></span>
- <span data-ttu-id="c1594-108">Si vous disposez d’Office 365 DAV plan 1, vous disposez de détections en temps réel.</span><span class="sxs-lookup"><span data-stu-id="c1594-108">If you have Office 365 ATP Plan 1, then you have real-time detections.</span></span>

<span data-ttu-id="c1594-109">Lorsque vous ouvrez l’Explorateur (ou le rapport de détection en temps réel) pour la première fois, la vue par défaut affiche les détections de programmes malveillants de messagerie pour les 7 derniers jours.</span><span class="sxs-lookup"><span data-stu-id="c1594-109">When you first open Explorer (or the real-time detections report), the default view shows email malware detections for the past 7 days.</span></span> <span data-ttu-id="c1594-110">Ce rapport peut également afficher des détections ATP, telles que les URL malveillantes détectées par les [liens fiables](atp-safe-links.md)et les fichiers malveillants détectés par des [pièces jointes fiables](atp-safe-attachments.md).</span><span class="sxs-lookup"><span data-stu-id="c1594-110">This report can also show ATP detections, such as malicious URLs detected by [Safe Links](atp-safe-links.md), and malicious files detected by [Safe Attachments](atp-safe-attachments.md).</span></span> <span data-ttu-id="c1594-111">Ce rapport peut être modifié pour afficher les données des 30 derniers jours (sauf si vous utilisez un abonnement à la version d’évaluation).</span><span class="sxs-lookup"><span data-stu-id="c1594-111">This report can be modified to show data for the past 30 days (unless you are using a trial subscription).</span></span> <span data-ttu-id="c1594-112">Les abonnements à la version d’évaluation incluent des données pour les sept derniers jours.</span><span class="sxs-lookup"><span data-stu-id="c1594-112">Trial subscriptions will include data for the past seven days only.</span></span>

<span data-ttu-id="c1594-113">Utilisez le menu **affichage** pour modifier les informations affichées.</span><span class="sxs-lookup"><span data-stu-id="c1594-113">Use the **View** menu to change what information is displayed.</span></span> <span data-ttu-id="c1594-114">Les info-bulles vous aident à déterminer l’affichage à utiliser.</span><span class="sxs-lookup"><span data-stu-id="c1594-114">Tooltips help you determine which view to use.</span></span>
  
![Menu Affichage de l’Explorateur de menaces](../../media/ThreatExplorerViewMenu.png)

<span data-ttu-id="c1594-116">Une fois que vous avez sélectionné un affichage, vous pouvez appliquer des filtres et configurer des requêtes pour effectuer une analyse plus poussée.</span><span class="sxs-lookup"><span data-stu-id="c1594-116">Once you have selected a view, you can apply filters and set up queries to conduct further analysis.</span></span> <span data-ttu-id="c1594-117">Les sections suivantes fournissent un bref aperçu des différentes vues disponibles dans l’Explorateur (ou les détections en temps réel).</span><span class="sxs-lookup"><span data-stu-id="c1594-117">The following sections provide a brief overview of the various views available in Explorer (or real-time detections).</span></span>  

## <a name="email--malware"></a><span data-ttu-id="c1594-118">Courrier électronique > programme malveillant</span><span class="sxs-lookup"><span data-stu-id="c1594-118">Email > Malware</span></span>

<span data-ttu-id="c1594-119">Pour afficher ce rapport, dans l’Explorateur (ou les détections en temps réel), sélectionnez **Afficher** > les**programmes malveillants**de**messagerie** > .</span><span class="sxs-lookup"><span data-stu-id="c1594-119">To view this report, in Explorer (or real-time detections), choose **View** > **Email** > **Malware**.</span></span> <span data-ttu-id="c1594-120">Cette vue affiche des informations sur les messages électroniques identifiés comme contenant des programmes malveillants.</span><span class="sxs-lookup"><span data-stu-id="c1594-120">This view shows information about email messages that were identified as containing malware.</span></span>  

![Afficher les données sur le courrier électronique identifié comme programme malveillant](../../media/ExplorerEmailMalwareMenu.png) 

<span data-ttu-id="c1594-122">Cliquez sur **expéditeur** pour ouvrir votre liste d’options d’affichage.</span><span class="sxs-lookup"><span data-stu-id="c1594-122">Click **Sender** to open your list of viewing options.</span></span> <span data-ttu-id="c1594-123">Utilisez cette liste pour afficher les données par expéditeur, destinataires, domaine de l’expéditeur, objet, technologie de détection, état de protection, etc.</span><span class="sxs-lookup"><span data-stu-id="c1594-123">Use this list to view data by sender, recipients, sender domain, subject, detection technology, protection status, and more.</span></span> 

<span data-ttu-id="c1594-124">Par exemple, pour voir les actions qui ont été effectuées sur les messages électroniques détectés, choisissez **État de protection** dans la liste.</span><span class="sxs-lookup"><span data-stu-id="c1594-124">For example, to see what actions were taken on detected email messages, choose **Protection status** in the list.</span></span> <span data-ttu-id="c1594-125">Sélectionnez une option, puis cliquez sur le bouton Actualiser pour appliquer ce filtre à votre rapport.</span><span class="sxs-lookup"><span data-stu-id="c1594-125">Select an option, and then click the Refresh button to apply that filter to your report.</span></span>

![Options d’état de protection contre les menaces pour l’Explorateur de menaces](../../media/ThreatExplorerProtectionStatusOptions.png)

<span data-ttu-id="c1594-127">Sous le graphique, affichez plus de détails sur des messages spécifiques.</span><span class="sxs-lookup"><span data-stu-id="c1594-127">Below the chart, view more details about specific messages.</span></span> <span data-ttu-id="c1594-128">Lorsque vous sélectionnez un élément dans la liste, un volet de survol s’ouvre, dans lequel vous pouvez en savoir plus sur l’élément que vous avez sélectionné.</span><span class="sxs-lookup"><span data-stu-id="c1594-128">When you select an item in the list, a fly-out pane opens, where you can learn more about the item you selected.</span></span> 

![Explorateur de menaces avec le lanceur ouvert](../../media/ThreatExplorerMalwareItemSelectedFlyout.png)

## <a name="email--phish"></a><span data-ttu-id="c1594-130">Courrier électronique > hameçonnage</span><span class="sxs-lookup"><span data-stu-id="c1594-130">Email > Phish</span></span>

<span data-ttu-id="c1594-131">Pour afficher ce rapport, dans l’Explorateur (ou les détections en temps réel), sélectionnez **Afficher** > le**hameçonnage\*\*\*\*par courrier électronique** > .</span><span class="sxs-lookup"><span data-stu-id="c1594-131">To view this report, in Explorer (or real-time detections), choose **View** > **Email** > **Phish**.</span></span> <span data-ttu-id="c1594-132">Cet affichage montre les messages électroniques identifiés comme des tentatives de hameçonnage.</span><span class="sxs-lookup"><span data-stu-id="c1594-132">This view shows email messages identified as phishing attempts.</span></span>  

![Afficher les données sur l’e-mail identifiées comme tentatives de hameçonnage](../../media/ThreatExplorerEmailPhish.png) 

<span data-ttu-id="c1594-134">Cliquez sur **expéditeur** pour ouvrir votre liste d’options d’affichage.</span><span class="sxs-lookup"><span data-stu-id="c1594-134">Click **Sender** to open your list of viewing options.</span></span> <span data-ttu-id="c1594-135">Utilisez cette liste pour afficher les données par expéditeur, destinataires, domaine de l’expéditeur, adresse IP de l’expéditeur, domaine de l’URL, cliquez sur verdict, etc.</span><span class="sxs-lookup"><span data-stu-id="c1594-135">Use this list to view data by sender, recipients, sender domain, sender IP, URL domain, click verdict, and more.</span></span> 

<span data-ttu-id="c1594-136">Par exemple, pour voir les actions qui ont été effectuées lorsque des utilisateurs cliquaient sur des URL identifiées comme tentatives de hameçonnage, choisissez **cliquer sur verdict** dans la liste, sélectionnez une ou plusieurs options, puis cliquez sur le bouton Actualiser.</span><span class="sxs-lookup"><span data-stu-id="c1594-136">For example, to see what actions were taken when people clicked on URLs that were identified as phishing attempts, choose **Click verdict** in the list, select one or more options, and then click the Refresh button.</span></span>

![Cliquez sur options de verdict pour le rapport de hameçonnage.](../../media/ThreatExplorerEmailPhishClickVerdictOptions.png)

<span data-ttu-id="c1594-138">Sous le graphique, affichez plus de détails sur des messages spécifiques, des clics d’URL, des URL et de l’origine du courrier électronique.</span><span class="sxs-lookup"><span data-stu-id="c1594-138">Below the chart, view more details about specific messages, URL clicks, URLs, and email origin.</span></span> 

![URL détectées comme hameçonnage dans les messages électroniques](../../media/ThreatExplorerEmailPhishURLs.png)

<span data-ttu-id="c1594-140">Lorsque vous sélectionnez un élément dans la liste, tel qu’une URL qui a été détectée, un volet de survol s’ouvre, dans lequel vous pouvez en savoir plus sur l’élément que vous avez sélectionné.</span><span class="sxs-lookup"><span data-stu-id="c1594-140">When you select an item in the list, such as a URL that was detected, a fly-out pane opens, where you can learn more about the item you selected.</span></span> 

![Détails sur une URL détectée](../../media/ThreatExplorerEmailPhishURLDetails.png)

## <a name="email--submissions"></a><span data-ttu-id="c1594-142">Envois de > de messagerie</span><span class="sxs-lookup"><span data-stu-id="c1594-142">Email > Submissions</span></span>

<span data-ttu-id="c1594-143">Pour afficher ce rapport, dans l’Explorateur (ou les détections en temps réel), sélectionnez **Afficher** > les**envois**de**courrier** > .</span><span class="sxs-lookup"><span data-stu-id="c1594-143">To view this report, in Explorer (or real-time detections), choose **View** > **Email** > **Submissions**.</span></span> <span data-ttu-id="c1594-144">Cet affichage montre le courrier électronique que les utilisateurs ont signalés comme courrier indésirable, non légitime ou courrier électronique de hameçonnage.</span><span class="sxs-lookup"><span data-stu-id="c1594-144">This view shows email that users have reported as junk, not junk, or phishing email.</span></span> 

![Messages électroniques signalés par les utilisateurs](../../media/ThreatExplorerEmailUserReportedViewOptions.png) 

<span data-ttu-id="c1594-146">Cliquez sur **expéditeur** pour ouvrir votre liste d’options d’affichage.</span><span class="sxs-lookup"><span data-stu-id="c1594-146">Click **Sender** to open your list of viewing options.</span></span> <span data-ttu-id="c1594-147">Cette liste permet d’afficher des informations par expéditeur, destinataires, type de rapport (l’utilisateur a déterminé que le courrier électronique a été légitime, non légitime ou hameçon), et bien plus encore.</span><span class="sxs-lookup"><span data-stu-id="c1594-147">Use this list to view information by sender, recipients, report type (the user's determination that the email was junk, not junk, or phish), and more.</span></span> 

<span data-ttu-id="c1594-148">Par exemple, pour afficher les informations sur les messages électroniques qui ont été signalés en tant que tentatives de hameçonnage, cliquez sur**type de rapport**de l' **expéditeur** > , sélectionnez **hameçonnage**, puis cliquez sur le bouton Actualiser.</span><span class="sxs-lookup"><span data-stu-id="c1594-148">For example, to view information about email messages that were reported as phishing attempts, click **Sender** > **Report type**, select **Phish**, and then click the Refresh button.</span></span>

![Hameçonnage sélectionné pour le filtre de type de rapport](../../media/ThreatExplorerEmailUserReportedPhishSelected.png)

<span data-ttu-id="c1594-150">Sous le graphique, affichez plus de détails sur des messages électroniques spécifiques, tels que la ligne d’objet, l’adresse IP de l’expéditeur, l’utilisateur qui a signalé le message comme courrier indésirable, légitime, ou hameçon, et bien plus encore.</span><span class="sxs-lookup"><span data-stu-id="c1594-150">Below the chart, view more details about specific email messages, such as subject line, the sender's IP address, the user that reported the message as junk, not junk, or phish, and more.</span></span> 

![Messages qui ont été signalés en tant que tentatives de hameçonnage](../../media/ThreatExplorerEmailPhishUserReportedPhishDetails.png)

<span data-ttu-id="c1594-152">Sélectionnez un élément dans la liste pour afficher des détails supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="c1594-152">Select an item in the list to view additional details.</span></span>

## <a name="email--all-email"></a><span data-ttu-id="c1594-153">Courrier électronique > tous les messages électroniques</span><span class="sxs-lookup"><span data-stu-id="c1594-153">Email > All email</span></span>

<span data-ttu-id="c1594-154">Pour afficher ce rapport, dans l’Explorateur, sélectionnez **Afficher** > le courrier**électronique** > de**tous les messages**.</span><span class="sxs-lookup"><span data-stu-id="c1594-154">To view this report, in Explorer, choose **View** > **Email** > **All mail**.</span></span> <span data-ttu-id="c1594-155">Cette vue affiche une vue d’ensemble de l’activité de messagerie, y compris le courrier électronique identifié comme malveillant en raison d’un hameçonnage ou d’un programme malveillant, ainsi que tous les messages non malveillants (e-mail normal, courrier indésirable et courrier en nombre).</span><span class="sxs-lookup"><span data-stu-id="c1594-155">This views shows an all-up view of email activity, including email identified as malicious due to phishing or malware, as well all non-malicious mail (normal email, spam, and bulk mail).</span></span> 

> [!NOTE]
> <span data-ttu-id="c1594-156">Si vous obtenez une erreur indiquant un **trop grand nombre de données à afficher**, ajoutez un filtre et, si nécessaire, Affinez la plage de dates que vous visualisez.</span><span class="sxs-lookup"><span data-stu-id="c1594-156">If you get an error that reads **Too much data to display**, add a filter and, if necessary, narrow the date range you're viewing.</span></span> 

<span data-ttu-id="c1594-157">Pour appliquer un filtre, choisissez **expéditeur**, sélectionnez un élément dans la liste, puis cliquez sur le bouton Actualiser.</span><span class="sxs-lookup"><span data-stu-id="c1594-157">To apply a filter, choose **Sender**, select an item in the list, and then click the Refresh button.</span></span> <span data-ttu-id="c1594-158">Dans notre exemple, nous avons utilisé la **technologie de détection** en tant que filtre (plusieurs options sont disponibles).</span><span class="sxs-lookup"><span data-stu-id="c1594-158">In our example, we used **Detection technology** as a filter (there are several options available).</span></span> <span data-ttu-id="c1594-159">Afficher les informations de l’expéditeur, du domaine de l’expéditeur, des destinataires, de l’objet, du nom de fichier de la pièce jointe, de la famille de programmes malveillants, du statut de protection (actions effectuées par vos stratégies et fonctionnalités de protection contre les menaces dans Office 365), de la technologie de détection (comment le programme malveillant a été détecté) et plus d'.</span><span class="sxs-lookup"><span data-stu-id="c1594-159">View information by sender, sender's domain, recipients, subject, attachment filename, malware family, protection status (actions taken by your threat protection features and policies in Office 365), detection technology (how the malware was detected), and more.</span></span> 

![Afficher les données sur les messages détectés par la technologie de détection](../../media/0c032eb3-6021-4174-9f06-ff8f30c245ca.png) 

<span data-ttu-id="c1594-161">Sous le graphique, affichez plus de détails sur des messages électroniques spécifiques, tels que la ligne d’objet, le destinataire, l’expéditeur, l’État, etc.</span><span class="sxs-lookup"><span data-stu-id="c1594-161">Below the chart, view more details about specific email messages, such as subject line, recipient, sender, status, and so on.</span></span> 

## <a name="content--malware"></a><span data-ttu-id="c1594-162">Contenu > programme malveillant</span><span class="sxs-lookup"><span data-stu-id="c1594-162">Content > Malware</span></span>

<span data-ttu-id="c1594-163">Pour afficher ce rapport, dans l’Explorateur (ou les détections en temps réel), sélectionnez **Afficher** > **le contenu** > **malveillant**.</span><span class="sxs-lookup"><span data-stu-id="c1594-163">To view this report, in Explorer (or real-time detections), choose **View** > **Content** > **Malware**.</span></span> <span data-ttu-id="c1594-164">Cet affichage montre les fichiers identifiés comme étant malveillants par [Office 365 protection avancée contre les menaces dans SharePoint Online, OneDrive entreprise et Microsoft teams](atp-for-spo-odb-and-teams.md).</span><span class="sxs-lookup"><span data-stu-id="c1594-164">This view shows files that were identified as malicious by [Office 365 Advanced Threat Protection in SharePoint Online, OneDrive for Business, and Microsoft Teams](atp-for-spo-odb-and-teams.md).</span></span>

<span data-ttu-id="c1594-165">Afficher des informations par famille de programmes malveillants, technologie de détection (comment le programme malveillant a été détecté) et charge de travail (OneDrive, SharePoint ou Teams).</span><span class="sxs-lookup"><span data-stu-id="c1594-165">View information by malware family, detection technology (how the malware was detected), and workload (OneDrive, SharePoint, or Teams).</span></span> 

![Afficher les données sur les programmes malveillants détectés](../../media/d11dc568-b091-4159-b261-df13d76b520b.png)  

<span data-ttu-id="c1594-167">Sous le graphique, affichez plus de détails sur des fichiers spécifiques, tels que le nom de fichier de la pièce jointe, la charge de travail, la taille du fichier, la dernière personne qui a modifié le fichier, etc.</span><span class="sxs-lookup"><span data-stu-id="c1594-167">Below the chart, view more details about specific files, such as attachment filename, workload, file size, who last modified the file, and more.</span></span> 
  
## <a name="click-to-filter-capabilities"></a><span data-ttu-id="c1594-168">Fonctionnalités de cliquer-filtrer</span><span class="sxs-lookup"><span data-stu-id="c1594-168">Click-to-filter capabilities</span></span>

<span data-ttu-id="c1594-169">Avec l’Explorateur (et les détections en temps réel), vous pouvez appliquer un filtre dans un clic.</span><span class="sxs-lookup"><span data-stu-id="c1594-169">With Explorer (and real-time detections), you can apply a filter in a click.</span></span> <span data-ttu-id="c1594-170">Cliquez sur un élément dans la légende, et cet élément devient un filtre pour le rapport.</span><span class="sxs-lookup"><span data-stu-id="c1594-170">Click an item in the legend, and that item becomes a filter for the report.</span></span> <span data-ttu-id="c1594-171">Par exemple, supposons que nous examinons l’affichage programmes malveillants dans l’Explorateur :</span><span class="sxs-lookup"><span data-stu-id="c1594-171">For example, suppose we are looking at the Malware view in Explorer:</span></span>
  
![Accéder à l’Explorateur \> de gestion des menaces](../../media/cab32fa2-66f1-4ad5-bc1d-2bac4dbeb48c.png)
  
<span data-ttu-id="c1594-173">Si vous cliquez sur **détonation** de la protection avancée contre les menaces dans ce graphique, les résultats sont les suivants :</span><span class="sxs-lookup"><span data-stu-id="c1594-173">Clicking **ATP Detonation** in this chart results in a view like this:</span></span> 
  
![Explorateur filtré pour afficher uniquement les résultats de la détonation ATP](../../media/7241d7dd-27bc-467d-9db8-6e806c49df14.png)
  
<span data-ttu-id="c1594-175">Dans cet affichage, nous examinons à présent les données des fichiers qui ont été détonants par [les pièces jointes approuvées par Office 365 ATP](atp-safe-attachments.md).</span><span class="sxs-lookup"><span data-stu-id="c1594-175">In this view, we are now looking at data for files that were detonated by [Office 365 ATP Safe Attachments](atp-safe-attachments.md).</span></span> <span data-ttu-id="c1594-176">Sous le graphique, nous pouvons voir des détails sur des messages électroniques spécifiques qui avaient des pièces jointes détectées par des pièces jointes sûres ATP.</span><span class="sxs-lookup"><span data-stu-id="c1594-176">Below the chart, we can see details about specific email messages that had attachments that were detected by ATP Safe Attachments.</span></span>
  
![Détails spécifiques sur les messages électroniques avec des pièces jointes détectées](../../media/c91fb05c-d1d4-4085-acc6-f7008a415c2a.png)
  
<span data-ttu-id="c1594-178">La sélection d’un ou de plusieurs éléments active le menu **actions** , qui offre plusieurs choix parmi lesquels choisir pour les éléments sélectionnés.</span><span class="sxs-lookup"><span data-stu-id="c1594-178">Selecting one or more items activates the **Actions** menu, which offers several choices from which to choose for the selected item(s).</span></span> 
  
![La sélection d’un élément active le menu actions](../../media/95f127a4-1b2a-4a76-88b9-096e3ba27d1b.png)
  
<span data-ttu-id="c1594-180">La possibilité de filtrer un clic et d’accéder à des détails spécifiques peut vous faire gagner du temps lors de l’enquête sur les menaces.</span><span class="sxs-lookup"><span data-stu-id="c1594-180">The ability to filter in a click and navigate to specific details can save you a lot of time in investigating threats.</span></span>

## <a name="queries-and-filters"></a><span data-ttu-id="c1594-181">Requêtes et filtres</span><span class="sxs-lookup"><span data-stu-id="c1594-181">Queries and filters</span></span>

<span data-ttu-id="c1594-182">L’Explorateur (ainsi que le rapport de détections en temps réel) dispose de plusieurs filtres et fonctionnalités d’interrogation puissants qui vous permettent d’explorer les détails, tels que les principaux utilisateurs ciblés, les principales familles de logiciels malveillants, la technologie de détection et bien plus encore.</span><span class="sxs-lookup"><span data-stu-id="c1594-182">Explorer (as well as the real-time detections report) has several powerful filters and querying capabilities that enable you to drill into details, such as top targeted users, top malware families, detection technology and more.</span></span> <span data-ttu-id="c1594-183">Chaque type de rapport offre plusieurs façons d’afficher et d’explorer les données.</span><span class="sxs-lookup"><span data-stu-id="c1594-183">Each kind of report offers a variety of ways to view and explore data.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="c1594-184">N’utilisez pas de caractères génériques, tels qu’un astérisque ou un point d’interrogation, dans la barre de requête pour l’Explorateur (ou les détections en temps réel).</span><span class="sxs-lookup"><span data-stu-id="c1594-184">Do not use wildcard characters, such as an asterisk or a question mark, in the query bar for Explorer (or real-time detections).</span></span> <span data-ttu-id="c1594-185">Lorsque vous effectuez une recherche dans le **champ Subject** pour les messages électroniques, l’Explorateur (ou les détections en temps réel) effectue une correspondance partielle et génère des résultats similaires à une recherche par caractères génériques.</span><span class="sxs-lookup"><span data-stu-id="c1594-185">When you search on the **Subject field** for email messages, Explorer (or real-time detections) will perform partial matching and yield results similar to a wildcard search.</span></span>
