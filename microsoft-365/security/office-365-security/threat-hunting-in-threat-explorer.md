---
title: Recherche de menaces dans l’Explorateur de menaces pour Microsoft Defender Office 365
f1.keywords:
- NOCSH
ms.author: dansimp
author: MSFTTracyp
manager: dansimp
audience: ITPro
ms.topic: article
ms.date: 05/05/2021
localization_priority: Normal
ms.collection:
- M365-security-compliance
- m365initiative-defender-office365
description: Utilisez l’Explorateur de menaces ou les détections en temps réel dans le Centre de conformité de sécurité pour examiner les menaces et y &amp; répondre efficacement.
ms.custom: seo-marvel-apr2020
ms.technology: mdo
ms.prod: m365-security
ms.openlocfilehash: 65fe67103d9a380c63a0362594c23290457ea3aa
ms.sourcegitcommit: de5fce90de22ba588e75e1a1d2e87e03b9e25ec7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/10/2021
ms.locfileid: "52295269"
---
# <a name="threat-hunting-in-threat-explorer-for-microsoft-defender-for-office-365"></a><span data-ttu-id="12909-103">Recherche de menaces dans l’Explorateur de menaces pour Microsoft Defender Office 365</span><span class="sxs-lookup"><span data-stu-id="12909-103">Threat hunting in Threat Explorer for Microsoft Defender for Office 365</span></span>

<span data-ttu-id="12909-104">Contenu de cet article :</span><span class="sxs-lookup"><span data-stu-id="12909-104">In this article:</span></span>

- [<span data-ttu-id="12909-105">Exploration pas à pas de l’Explorateur de menaces</span><span class="sxs-lookup"><span data-stu-id="12909-105">Threat Explorer walk-through</span></span>](#threat-explorer-walk-through)
- [<span data-ttu-id="12909-106">Examen par courrier électronique</span><span class="sxs-lookup"><span data-stu-id="12909-106">Email investigation</span></span>](#email-investigation)
- [<span data-ttu-id="12909-107">Correction de courrier électronique</span><span class="sxs-lookup"><span data-stu-id="12909-107">Email remediation</span></span>](#email-remediation)
- [<span data-ttu-id="12909-108">Améliorations de l’expérience de recherche de menaces</span><span class="sxs-lookup"><span data-stu-id="12909-108">Improvements to threat hunting experience</span></span>](#improvements-to-threat-hunting-experience)

> [!NOTE]
> <span data-ttu-id="12909-109">Cela fait partie d’une série de **3** articles sur l’Explorateur de menaces **,** la sécurité du courrier électronique et les bases de détection **en** temps réel et de l’Explorateur (telles que les différences entre les outils et les autorisations nécessaires pour les utiliser).</span><span class="sxs-lookup"><span data-stu-id="12909-109">This is part of a **3-article series** on **Threat Explorer (Explorer)**, **email security**, and **Explorer and Real-time detections basics** (such as differences between the tools, and permissions needed to operate them).</span></span> <span data-ttu-id="12909-110">Les deux autres articles de cette série sont la sécurité de la messagerie avec [l’Explorateur](email-security-in-microsoft-defender.md) de menaces et l’Explorateur de menaces et les informations de base sur les [détections en temps réel.](real-time-detections.md)</span><span class="sxs-lookup"><span data-stu-id="12909-110">The other two articles in this series are [Email security with Threat Explorer](email-security-in-microsoft-defender.md) and [Threat Explorer and Real-time detections basics](real-time-detections.md).</span></span>


<span data-ttu-id="12909-111">**S’applique à**</span><span class="sxs-lookup"><span data-stu-id="12909-111">**Applies to**</span></span>
- [<span data-ttu-id="12909-112">Microsoft Defender pour Office 365 : offre 1 et offre 2</span><span class="sxs-lookup"><span data-stu-id="12909-112">Microsoft Defender for Office 365 plan 1 and plan 2</span></span>](defender-for-office-365.md)
- [<span data-ttu-id="12909-113">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="12909-113">Microsoft 365 Defender</span></span>](../defender/microsoft-365-defender.md)

<span data-ttu-id="12909-114">Si votre organisation dispose de [Microsoft Defender pour Office 365](defender-for-office-365.md)et que vous disposez des [autorisations,](#required-licenses-and-permissions)vous pouvez utiliser l’Explorateur ou les  **détections** en temps réel pour détecter et corriger les menaces.</span><span class="sxs-lookup"><span data-stu-id="12909-114">If your organization has [Microsoft Defender for Office 365](defender-for-office-365.md), and you have the [permissions](#required-licenses-and-permissions), you can use **Explorer** or **Real-time detections** to detect and remediate threats.</span></span> 

<span data-ttu-id="12909-115">Dans le Centre de sécurité &  **conformité,** sélectionnez Gestion des menaces, puis sélectionnez **Explorer**  ou **Détections en temps réel.**</span><span class="sxs-lookup"><span data-stu-id="12909-115">In the **Security & Compliance Center**, go to **Threat management**, and then choose **Explorer** _or_ **Real-time detections**.</span></span>

<br>

****

|<span data-ttu-id="12909-116">Avec Microsoft Defender pour Office 365 Plan 2, vous pouvez voir :</span><span class="sxs-lookup"><span data-stu-id="12909-116">With Microsoft Defender for Office 365 Plan 2, you see:</span></span>|<span data-ttu-id="12909-117">Avec Microsoft Defender pour Office 365 Plan 1, vous pouvez voir :</span><span class="sxs-lookup"><span data-stu-id="12909-117">With Microsoft Defender for Office 365 Plan 1, you see:</span></span>|
|---|---|
|![Explorateur de menaces](../../media/threatmgmt-explorer.png)|![Détections en temps réel](../../media/threatmgmt-realtimedetections.png)|
|

<span data-ttu-id="12909-120">Avec ces outils, vous pouvez :</span><span class="sxs-lookup"><span data-stu-id="12909-120">With these tools, you can:</span></span>

- <span data-ttu-id="12909-121">Consulter les programmes malveillants détectés par les fonctionnalités Microsoft 365 sécurité</span><span class="sxs-lookup"><span data-stu-id="12909-121">See malware detected by Microsoft 365 security features</span></span>
- <span data-ttu-id="12909-122">Afficher l’URL de hameçonnage et cliquer sur les données de verdict</span><span class="sxs-lookup"><span data-stu-id="12909-122">View phishing URL and click verdict data</span></span>
- <span data-ttu-id="12909-123">Démarrer un processus d’examen et de réponse automatisé à partir d’un affichage dans l’Explorateur</span><span class="sxs-lookup"><span data-stu-id="12909-123">Start an automated investigation and response process from a view in Explorer</span></span>
- <span data-ttu-id="12909-124">Examiner les e-mails malveillants, et bien plus encore</span><span class="sxs-lookup"><span data-stu-id="12909-124">Investigate malicious email, and more</span></span>

<span data-ttu-id="12909-125">Pour plus d’informations, [voir Sécurité du courrier électronique avec l’Explorateur de menaces.](email-security-in-microsoft-defender.md)</span><span class="sxs-lookup"><span data-stu-id="12909-125">For more information, see [Email security with Threat Explorer](email-security-in-microsoft-defender.md).</span></span> 

## <a name="threat-explorer-walk-through"></a><span data-ttu-id="12909-126">Exploration pas à pas de l’Explorateur de menaces</span><span class="sxs-lookup"><span data-stu-id="12909-126">Threat Explorer walk-through</span></span>

<span data-ttu-id="12909-127">Dans Microsoft Defender pour Office 365, il existe deux plans d’abonnement : Plan 1 et Plan 2.</span><span class="sxs-lookup"><span data-stu-id="12909-127">In Microsoft Defender for Office 365, there are two subscription plans—Plan 1 and Plan 2.</span></span> <span data-ttu-id="12909-128">Les outils de recherche de menaces gérés manuellement existent dans les deux plans, sous des noms différents et avec des fonctionnalités différentes.</span><span class="sxs-lookup"><span data-stu-id="12909-128">Manually operated Threat hunting tools exist in both plans, under different names and with different capabilities.</span></span>

<span data-ttu-id="12909-129">Defender pour Office 365 Plan 1 utilise les détections en temps réel, qui est un *sous-ensemble* de l’outil de repérage de l’Explorateur de menaces *(également* appelé *Explorateur)* dans le Plan 2.</span><span class="sxs-lookup"><span data-stu-id="12909-129">Defender for Office 365 Plan 1 uses *Real-time detections*, which is a subset of the *Threat Explorer* (also called *Explorer*) hunting tool in Plan 2.</span></span> <span data-ttu-id="12909-130">Dans cette série d’articles, la plupart des exemples ont été créés à l’aide de l’Explorateur de menaces complet.</span><span class="sxs-lookup"><span data-stu-id="12909-130">In this series of articles, most of the examples were created using the full Threat Explorer.</span></span> <span data-ttu-id="12909-131">Les administrateurs doivent tester les étapes des détections en temps réel pour voir où elles s’appliquent.</span><span class="sxs-lookup"><span data-stu-id="12909-131">Admins should test any steps in Real-time detections to see where they apply.</span></span>

<span data-ttu-id="12909-132">Pour ouvrir l’outil Explorer, go to **Security & Compliance Center** Threat  >  **management**  >  **Explorer** (or **Real-time detections**).</span><span class="sxs-lookup"><span data-stu-id="12909-132">To open the Explorer tool, go to **Security & Compliance Center** > **Threat management** > **Explorer** (or **Real-time detections**).</span></span> <span data-ttu-id="12909-133">Par défaut, vous arrivez sur la **page** Programmes malveillants, mais utilisez la vue du bas pour vous familiariser avec vos options. </span><span class="sxs-lookup"><span data-stu-id="12909-133">By default, you’ll arrive on the **Malware** page, but use the **View** drop down to get familiar with your options.</span></span> <span data-ttu-id="12909-134">Si vous recherchez du hameçonnage ou si vous êtes en train d’entrer dans une campagne contre les menaces, choisissez ces affichages.</span><span class="sxs-lookup"><span data-stu-id="12909-134">If you’re hunting Phish, or digging into a threat campaign, choose those views.</span></span>

> [!div class="mx-imgBorder"]
> <span data-ttu-id="12909-135">![Afficher la vue dans l’Explorateur de menaces](../../media/threat-explorer-view-drop-down.png)</span><span class="sxs-lookup"><span data-stu-id="12909-135">![View drop down in Threat Explorer](../../media/threat-explorer-view-drop-down.png)</span></span>

<span data-ttu-id="12909-136">Une fois qu’une personne des opérations de sécurité (Sec Ops) sélectionne les données qu’elle souhaite voir, si  l’étendue est un affichage étroit comme les **soumissions** utilisateur ou une vue plus large, comme Tous les e-mails, elle peut utiliser le bouton Expéditeur pour filtrer davantage.</span><span class="sxs-lookup"><span data-stu-id="12909-136">Once a security operations (Sec Ops) person selects the data they want to see, whether the scope is narrow view like user **Submissions**, or a wider view, like **All email**, they can use the **Sender** button to further filter.</span></span> <span data-ttu-id="12909-137">N’oubliez pas de sélectionner Actualiser pour terminer vos actions de filtrage.</span><span class="sxs-lookup"><span data-stu-id="12909-137">Remember to select Refresh to complete your filtering actions.</span></span>

> [!div class="mx-imgBorder"]
> <span data-ttu-id="12909-138">![Bouton Expéditeur dans l’Explorateur de menaces](../../media/threat-explorer-sender-button.png)</span><span class="sxs-lookup"><span data-stu-id="12909-138">![Sender button in Threat Explorer](../../media/threat-explorer-sender-button.png)</span></span>

<span data-ttu-id="12909-139">L’affinage du focus dans l’Explorateur ou la détection en temps réel peut être pensé en couches.</span><span class="sxs-lookup"><span data-stu-id="12909-139">Refining focus in Explorer or Real-time detection can be thought of in layers.</span></span> <span data-ttu-id="12909-140">Le premier est **View**.</span><span class="sxs-lookup"><span data-stu-id="12909-140">The first is **View**.</span></span> <span data-ttu-id="12909-141">Le second peut être pensé comme un focus *filtré.*</span><span class="sxs-lookup"><span data-stu-id="12909-141">The second can be thought of as a *filtered focus*.</span></span> <span data-ttu-id="12909-142">Par exemple, vous pouvez revenir sur les étapes que vous avez prises pour rechercher une menace en enregistrant vos décisions comme celle-ci : Pour trouver le problème dans l’Explorateur, j’ai choisi l’affichage programmes malveillants avec le focus filtre **destinataire.**</span><span class="sxs-lookup"><span data-stu-id="12909-142">For example, you can retrace the steps you took in finding a threat by recording your decisions like this: To find the issue in Explorer, **I chose the Malware View with a Recipient filter focus**.</span></span> <span data-ttu-id="12909-143">Cela facilite le retracage de vos étapes.</span><span class="sxs-lookup"><span data-stu-id="12909-143">This makes retracing your steps easier.</span></span>

> [!TIP]
> <span data-ttu-id="12909-144">Si Sec Ops utilise des balises pour marquer les comptes qu’ils considèrent comme cibles à valeur élevée, ils peuvent effectuer des sélections telles que l’affichage d’hameçonnage avec un focus de filtre *Tags (inclure* une plage de dates si elle est utilisée). </span><span class="sxs-lookup"><span data-stu-id="12909-144">If Sec Ops uses **Tags** to mark accounts they consider high valued targets, they can make selections like *Phish View with a Tags filter focus (include a date range if used)*.</span></span> <span data-ttu-id="12909-145">Cela leur montrera toutes les tentatives de hameçonnage dirigées vers leurs cibles utilisateur à valeur élevée pendant une période de temps (par exemple, les dates où certaines attaques par hameçonnage se produisent beaucoup pour leur secteur d’activité).</span><span class="sxs-lookup"><span data-stu-id="12909-145">This will show them any phishing attempts directed at their high value user targets during a time-range (like dates when certain phishing attacks are happening a lot for their industry).</span></span> 

<span data-ttu-id="12909-146">Les affinements peuvent être effectués sur des plages de dates à l’aide des contrôles de plage de dates.</span><span class="sxs-lookup"><span data-stu-id="12909-146">Refinements can be made on date ranges by using the date range controls.</span></span> <span data-ttu-id="12909-147">Ici, vous pouvez voir l’Explorateur en affichage **Programmes** malveillants, avec le focus du filtre **Technologie** de détection.</span><span class="sxs-lookup"><span data-stu-id="12909-147">Here you can see Explorer in **Malware** view, with a **Detection Technology** filter focus.</span></span> <span data-ttu-id="12909-148">Mais c’est le **bouton Filtre avancé** qui permet aux équipes Sec Ops d’être approfondies.</span><span class="sxs-lookup"><span data-stu-id="12909-148">But it’s the **Advanced filter** button that lets Sec Ops teams dig deep.</span></span> 

> [!div class="mx-imgBorder"]
> <span data-ttu-id="12909-149">![Filtre avancé dans l’Explorateur de menaces](../../media/threat-explorer-advanced-filter.png)</span><span class="sxs-lookup"><span data-stu-id="12909-149">![Advanced filter in Threat Explorer](../../media/threat-explorer-advanced-filter.png)</span></span>

<span data-ttu-id="12909-150">Le fait **de** cliquer sur le filtre avancé fait apparaître un panneau qui permet aux chercheurs sec Ops de créer eux-mêmes des requêtes, ce qui leur permet d’inclure ou d’exclure les informations dont ils ont besoin.</span><span class="sxs-lookup"><span data-stu-id="12909-150">Clicking the **Advanced filter** pops a panel that will let Sec Ops hunters build queries themselves, letting them include or exclude the information they need to see.</span></span> <span data-ttu-id="12909-151">Le graphique et le tableau de la page Explorateur reflètent leurs résultats.</span><span class="sxs-lookup"><span data-stu-id="12909-151">Both the chart and table on the Explorer page will reflect their results.</span></span> 

> [!div class="mx-imgBorder"]
> <span data-ttu-id="12909-152">![Résultats d’une requête](../../media/threat-explorer-chart-table.png)</span><span class="sxs-lookup"><span data-stu-id="12909-152">![Results from a query](../../media/threat-explorer-chart-table.png)</span></span>

<span data-ttu-id="12909-153">Utilisez le **bouton Options** de colonne pour obtenir le type d’informations sur le tableau qui serait le plus utile :</span><span class="sxs-lookup"><span data-stu-id="12909-153">Use the **Column options** button to get the kind of information on the table that would be most helpful:</span></span> 

> [!div class="mx-imgBorder"]
> <span data-ttu-id="12909-154">![Bouton Options de colonne mis en surbrill](../../media/threat-explorer-column-options.png)</span><span class="sxs-lookup"><span data-stu-id="12909-154">![Column options button highlighted](../../media/threat-explorer-column-options.png)</span></span>

> [!div class="mx-imgBorder"]
> <span data-ttu-id="12909-155">![Options disponibles dans colonnes](../../media/threat-explorer-column-options-details.png)</span><span class="sxs-lookup"><span data-stu-id="12909-155">![Available options in Columns](../../media/threat-explorer-column-options-details.png)</span></span>

<span data-ttu-id="12909-156">Dans la même façon, veillez à tester vos options d’affichage.</span><span class="sxs-lookup"><span data-stu-id="12909-156">In the same mien, make sure to test your display options.</span></span> <span data-ttu-id="12909-157">Différents publics réagissent bien aux différentes présentations des mêmes données.</span><span class="sxs-lookup"><span data-stu-id="12909-157">Different audiences will react well to different presentations of the same data.</span></span> <span data-ttu-id="12909-158">Pour certains visiteurs, **la** carte Origines du courrier électronique peut montrer qu’une menace est répandue ou discrète plus rapidement que l’option  d’affichage Campagne juste à côté.</span><span class="sxs-lookup"><span data-stu-id="12909-158">For some viewers, the **Email Origins** map can show that a threat is widespread or discreet more quickly than the **Campaign display** option right next to it.</span></span> <span data-ttu-id="12909-159">Sec Ops peut utiliser ces affichages pour mieux faire ressortir la nécessité d’une sécurité et d’une protection, ou pour une comparaison ultérieure, afin de démontrer l’efficacité de leurs actions.</span><span class="sxs-lookup"><span data-stu-id="12909-159">Sec Ops can make use of these displays to best make points that underscore the need for security and protection, or for later comparison, to demonstrate the effectiveness of their actions.</span></span> 

> [!div class="mx-imgBorder"]
> <span data-ttu-id="12909-160">![Carte des origines du courrier électronique](../../media/threat-explorer-email-origin-map.png)</span><span class="sxs-lookup"><span data-stu-id="12909-160">![Email Origins map](../../media/threat-explorer-email-origin-map.png)</span></span>

> [!div class="mx-imgBorder"]
> <span data-ttu-id="12909-161">![Options d’affichage de campagne](../../media/threat-explorer-campaign-display.png)</span><span class="sxs-lookup"><span data-stu-id="12909-161">![Campaign display options](../../media/threat-explorer-campaign-display.png)</span></span>

### <a name="email-investigation"></a><span data-ttu-id="12909-162">Examen par courrier électronique</span><span class="sxs-lookup"><span data-stu-id="12909-162">Email investigation</span></span>

<span data-ttu-id="12909-163">Lorsque vous voyez un e-mail suspect, cliquez sur le nom pour développer le volant sur la droite.</span><span class="sxs-lookup"><span data-stu-id="12909-163">When you see a suspicious email, click the name to expand the flyout on the right.</span></span> <span data-ttu-id="12909-164">Ici, la bannière qui permet à Sec Ops de voir la [page d’entité de](mdo-email-entity-page.md) messagerie est disponible.</span><span class="sxs-lookup"><span data-stu-id="12909-164">Here, the banner that lets Sec Ops see the [email entity page](mdo-email-entity-page.md) is available.</span></span>

<span data-ttu-id="12909-165">La page d’entité de messagerie regroupe le contenu qui se trouve sous **Détails,** **Pièces jointes,** **Appareils,** mais inclut des données plus organisées.</span><span class="sxs-lookup"><span data-stu-id="12909-165">The email entity page pulls together contents that can be found under **Details**, **Attachments**, **Devices**, but includes more organized data.</span></span> <span data-ttu-id="12909-166">Cela inclut des éléments tels que les résultats DMARC, l’affichage en texte simple de l’en-tête de l’e-mail avec une option de copie, les informations de verdict sur les pièces jointes qui ont été détonées en toute sécurité et les fichiers supprimés (il peut s’agir d’adresses IP contactées et de captures d’écran de pages ou de fichiers).</span><span class="sxs-lookup"><span data-stu-id="12909-166">This includes things like DMARC results, plain text display of the email header with a copy option, verdict information on attachments that were securely detonated, and files those detonations dropped (can include IP addresses that were contacted and screenshots of pages or files).</span></span> <span data-ttu-id="12909-167">Les URL et leurs verdicts sont également répertoriés avec des détails similaires signalés.</span><span class="sxs-lookup"><span data-stu-id="12909-167">URLs and their verdicts are also listed with similar details reported.</span></span> 

<span data-ttu-id="12909-168">Lorsque vous arrivez à cette étape, la page d’entité de messagerie sera essentielle à l’étape finale , à savoir la *correction.*</span><span class="sxs-lookup"><span data-stu-id="12909-168">When you reach this stage, the email entity page will be critical to the final step—*remediation*.</span></span> 

> [!div class="mx-imgBorder"]
> <span data-ttu-id="12909-169">![Page de l’entité de messagerie](../../media/threat-explorer-email-entity-page.png)</span><span class="sxs-lookup"><span data-stu-id="12909-169">![The email entity page](../../media/threat-explorer-email-entity-page.png)</span></span>

> [!TIP]
> <span data-ttu-id="12909-170">Pour en savoir plus sur la page d’entité de messagerie enrichie (voir ci-dessous sous l’onglet Analyse), y compris les résultats des pièces jointes détonées, les résultats pour les URL incluses et l’aperçu de courrier électronique sécurisé, cliquez [ici.](mdo-email-entity-page.md) </span><span class="sxs-lookup"><span data-stu-id="12909-170">To learn more about the rich email entity page (seen below on the **Analysis** tab), including the results of detonated Attachments, findings for included URLs, and safe Email preview, click [here](mdo-email-entity-page.md).</span></span>

> [!div class="mx-imgBorder"]
> <span data-ttu-id="12909-171">![Onglet Analyse de la page d’entité de messagerie](../../media/threat-explorer-analysis-tab.png)</span><span class="sxs-lookup"><span data-stu-id="12909-171">![Analysis tab of the email entity page](../../media/threat-explorer-analysis-tab.png)</span></span>

### <a name="email-remediation"></a><span data-ttu-id="12909-172">Correction de courrier électronique</span><span class="sxs-lookup"><span data-stu-id="12909-172">Email remediation</span></span>

<span data-ttu-id="12909-173">Une fois qu’une personne Sec Ops détermine qu’un e-mail est une menace, l’étape suivante de détection de l’Explorateur ou en temps réel traite la menace et la remédie.</span><span class="sxs-lookup"><span data-stu-id="12909-173">Once a Sec Ops person determines that an email is a threat, the next Explorer or Real-time detection step is dealing with the threat and remediating it.</span></span> <span data-ttu-id="12909-174">Pour ce faire, vous pouvez revenir à l’Explorateur de menaces, cocher la case du message électronique à l’aide du problème et utiliser le bouton **Actions.**</span><span class="sxs-lookup"><span data-stu-id="12909-174">This can be done by returning to Threat Explorer, selecting the checkbox for the problem email, and using the **Actions** button.</span></span>

> [!div class="mx-imgBorder"]
> <span data-ttu-id="12909-175">![Bouton Actions dans l’Explorateur de menaces](../../media/threat-explorer-email-actions-button.png)</span><span class="sxs-lookup"><span data-stu-id="12909-175">![Actions button in Threat Explorer](../../media/threat-explorer-email-actions-button.png)</span></span>

<span data-ttu-id="12909-176">Ici, l’analyste peut prendre des mesures telles que signaler le courrier comme courrier indésirable, hameçonnage ou programme malveillant, contacter des destinataires ou d’autres enquêtes qui peuvent inclure le déclenchement de manuels d’investigation et de réponse automatisées (ou AIR) (si vous avez l’offre 2).</span><span class="sxs-lookup"><span data-stu-id="12909-176">Here, the analyst can take actions like reporting the mail as Spam, Phishing, or Malware, contacting recipients, or further investigations that can include triggering Automated Investigation and Response (or AIR) playbooks (if you have Plan 2).</span></span> <span data-ttu-id="12909-177">Sinon, le courrier peut également être signalé comme étant propre.</span><span class="sxs-lookup"><span data-stu-id="12909-177">Or, the mail can also be reported as clean.</span></span>

> [!div class="mx-imgBorder"]
> <span data-ttu-id="12909-178">![Le drop down Actions](../../media/threat-explorer-email-actions-drop-down.png)</span><span class="sxs-lookup"><span data-stu-id="12909-178">![The Actions drop down](../../media/threat-explorer-email-actions-drop-down.png)</span></span>

## <a name="improvements-to-threat-hunting-experience"></a><span data-ttu-id="12909-179">Améliorations de l’expérience de recherche de menaces</span><span class="sxs-lookup"><span data-stu-id="12909-179">Improvements to threat hunting experience</span></span>

### <a name="alert-id"></a><span data-ttu-id="12909-180">ID d’alerte</span><span class="sxs-lookup"><span data-stu-id="12909-180">Alert ID</span></span>

<span data-ttu-id="12909-181">Lors de la navigation à partir  d’une alerte dans l’Explorateur de menaces, l’affichage est filtré par **L’ID d’alerte**.</span><span class="sxs-lookup"><span data-stu-id="12909-181">When navigating from an alert into Threat Explorer, the **View** will be filtered by **Alert ID**.</span></span> <span data-ttu-id="12909-182">Cela s’applique également dans la détection en temps réel.</span><span class="sxs-lookup"><span data-stu-id="12909-182">This also applies in Real-time detection.</span></span> <span data-ttu-id="12909-183">Les messages pertinents pour l’alerte spécifique, ainsi qu’un total de messages électroniques (un nombre) sont affichés.</span><span class="sxs-lookup"><span data-stu-id="12909-183">Messages relevant to the specific alert, and an email total (a count) are shown.</span></span> <span data-ttu-id="12909-184">Vous pourrez voir si un message faisait partie d’une alerte, ainsi que naviguer de ce message vers l’alerte associée.</span><span class="sxs-lookup"><span data-stu-id="12909-184">You will be able to see if a message was part of an alert, as well as navigate from that message to the related alert.</span></span>

<span data-ttu-id="12909-185">Enfin, l’ID d’alerte est inclus dans l’URL, par exemple : `https://protection.office.com/viewalerts?id=372c9b5b-a6c3-5847-fa00-08d8abb04ef1`</span><span class="sxs-lookup"><span data-stu-id="12909-185">Finally, alert ID is included in the URL, for example: `https://protection.office.com/viewalerts?id=372c9b5b-a6c3-5847-fa00-08d8abb04ef1`</span></span>

> [!div class="mx-imgBorder"]
> <span data-ttu-id="12909-186">![Filtrage de l’ID d’alerte](../../media/AlertID-Filter.png)</span><span class="sxs-lookup"><span data-stu-id="12909-186">![Filtering for Alert ID](../../media/AlertID-Filter.png)</span></span>

> [!div class="mx-imgBorder"]
> <span data-ttu-id="12909-187">![ID d’alerte dans le volant de détails](../../media/AlertID-DetailsFlyout.png)</span><span class="sxs-lookup"><span data-stu-id="12909-187">![Alert ID in details flyout](../../media/AlertID-DetailsFlyout.png)</span></span>

### <a name="extending-explorer-and-real-time-detections-data-retention-and-search-limit-for-trial-tenants"></a><span data-ttu-id="12909-188">Extension de la rétention et de la limite de recherche des données de l’Explorateur (et détections en temps réel) pour les clients d’essai</span><span class="sxs-lookup"><span data-stu-id="12909-188">Extending Explorer (and Real-time detections) data retention and search limit for trial tenants</span></span> 

<span data-ttu-id="12909-189">Dans le cadre de cette modification, les analystes pourront rechercher et filtrer les données de courrier électronique sur une période de 30 jours (plus de sept jours) dans l’Explorateur de menaces et les détections en temps réel pour Defender pour les clients d’essai Office P1 et P2.</span><span class="sxs-lookup"><span data-stu-id="12909-189">As part of this change, analysts will be able to search for, and filter email data across 30 days (increased from seven days) in Threat Explorer and Real-time detections for both Defender for Office P1 and P2 trial tenants.</span></span> <span data-ttu-id="12909-190">Cela n’a aucune incidence sur les clients de production pour les clients P1 et P2 E5, où la valeur par défaut de rétention est déjà de 30 jours.</span><span class="sxs-lookup"><span data-stu-id="12909-190">This doesn’t impact any production tenants for both P1 and P2 E5 customers, where the retention default is already 30 days.</span></span>

### <a name="updated-export-limit"></a><span data-ttu-id="12909-191">Limite d’exportation mise à jour</span><span class="sxs-lookup"><span data-stu-id="12909-191">Updated Export limit</span></span> 

<span data-ttu-id="12909-192">Le nombre d’enregistrements d’e-mails qui peuvent être exportés à partir de l’Explorateur de menaces est désormais de 200 000 (9 990).</span><span class="sxs-lookup"><span data-stu-id="12909-192">The number of Emails records that can be exported from Threat Explorer is now 200,000 (was 9990).</span></span> <span data-ttu-id="12909-193">L’ensemble des colonnes qui peuvent être exportées reste inchangé.</span><span class="sxs-lookup"><span data-stu-id="12909-193">The set of columns that can be exported is unchanged.</span></span> 

### <a name="tags-in-threat-explorer"></a><span data-ttu-id="12909-194">Balises dans l’Explorateur de menaces</span><span class="sxs-lookup"><span data-stu-id="12909-194">Tags in Threat Explorer</span></span>

> [!NOTE]
> <span data-ttu-id="12909-195">La fonctionnalité de balises utilisateur est en prévisualisation et n’est peut-être pas disponible pour tout le monde.</span><span class="sxs-lookup"><span data-stu-id="12909-195">The user tags feature is in Preview and may not be available to everyone.</span></span> <span data-ttu-id="12909-196">En outre, les aperçus sont sujets à modification.</span><span class="sxs-lookup"><span data-stu-id="12909-196">Also, Previews are subject to change.</span></span> <span data-ttu-id="12909-197">Pour plus d’informations sur la planification de publication, consultez la feuille de Microsoft 365 de publication.</span><span class="sxs-lookup"><span data-stu-id="12909-197">For information about the release schedule, check out the Microsoft 365 roadmap.</span></span>

<span data-ttu-id="12909-198">Les balises utilisateur identifient des groupes spécifiques d’utilisateurs dans Microsoft Defender Office 365.</span><span class="sxs-lookup"><span data-stu-id="12909-198">User tags identify specific groups of users in Microsoft Defender for Office 365.</span></span> <span data-ttu-id="12909-199">Pour plus d’informations sur les balises, notamment la gestion des licences et la configuration, voir [Balises utilisateur.](user-tags.md)</span><span class="sxs-lookup"><span data-stu-id="12909-199">For more information about tags, including licensing and configuration, see [User tags](user-tags.md).</span></span>

<span data-ttu-id="12909-200">Dans l’Explorateur de menaces, vous pouvez voir les informations sur les balises utilisateur dans les expériences suivantes.</span><span class="sxs-lookup"><span data-stu-id="12909-200">In Threat Explorer, you can see information about user tags in the following experiences.</span></span>

#### <a name="email-grid-view"></a><span data-ttu-id="12909-201">Affichage Grille du courrier électronique</span><span class="sxs-lookup"><span data-stu-id="12909-201">Email grid view</span></span>

<span data-ttu-id="12909-202">Lorsque les analystes voient la colonne **Balises** dans la grille de courrier, ils voient toutes les balises qui ont été appliquées aux boîtes aux lettres de l’expéditeur ou du destinataire.</span><span class="sxs-lookup"><span data-stu-id="12909-202">When analysts look at the **Tags** column the email grid, they are seeing all tags that have been applied to sender or recipient mailboxes.</span></span> <span data-ttu-id="12909-203">Par défaut, les balises système *telles que les comptes* de priorité sont affichées en premier.</span><span class="sxs-lookup"><span data-stu-id="12909-203">By default, system tags like *priority accounts* are shown first.</span></span>

> [!div class="mx-imgBorder"]
> <span data-ttu-id="12909-204">![Filtrer les balises dans l’affichage Grille du courrier électronique](../../media/tags-grid.png)</span><span class="sxs-lookup"><span data-stu-id="12909-204">![Filter tags in email grid view](../../media/tags-grid.png)</span></span>

#### <a name="filtering"></a><span data-ttu-id="12909-205">Filtrage</span><span class="sxs-lookup"><span data-stu-id="12909-205">Filtering</span></span>

<span data-ttu-id="12909-206">Les balises peuvent être utilisées comme filtres.</span><span class="sxs-lookup"><span data-stu-id="12909-206">Tags can be used as filters.</span></span> <span data-ttu-id="12909-207">Recherchez parmi les comptes prioritaires uniquement ou utilisez des scénarios de balises utilisateur spécifiques de cette façon.</span><span class="sxs-lookup"><span data-stu-id="12909-207">Hunt among priority accounts only, or use specific user tags scenarios this way.</span></span> <span data-ttu-id="12909-208">Vous pouvez également exclure les résultats qui ont certaines balises.</span><span class="sxs-lookup"><span data-stu-id="12909-208">You can also exclude results that have certain tags.</span></span> <span data-ttu-id="12909-209">Combinez les balises avec d’autres filtres et plages de dates pour affiner votre portée d’examen.</span><span class="sxs-lookup"><span data-stu-id="12909-209">Combine Tags with other filters and date ranges to narrow your scope of investigation.</span></span> 

<span data-ttu-id="12909-210">[![Balises de filtre](../../media/tags-filter-normal.png)](../../media/tags-filter-normal.png#lightbox)</span><span class="sxs-lookup"><span data-stu-id="12909-210">[![Filter tags](../../media/tags-filter-normal.png)](../../media/tags-filter-normal.png#lightbox)</span></span>

> [!div class="mx-imgBorder"]
> <span data-ttu-id="12909-211">![Ne pas filtrer les balises](../../media/tags-filter-not.png)</span><span class="sxs-lookup"><span data-stu-id="12909-211">![Not filter tags](../../media/tags-filter-not.png)</span></span>

#### <a name="email-detail-flyout"></a><span data-ttu-id="12909-212">Flyout des détails des e-mails</span><span class="sxs-lookup"><span data-stu-id="12909-212">Email detail flyout</span></span>

<span data-ttu-id="12909-213">Pour afficher les balises individuelles de l’expéditeur et du destinataire, sélectionnez un e-mail pour ouvrir le volant des détails du message.</span><span class="sxs-lookup"><span data-stu-id="12909-213">To view the individual tags for sender and recipient, select an email to open the message details flyout.</span></span> <span data-ttu-id="12909-214">Sous **l’onglet Résumé,** les balises de l’expéditeur et du destinataire sont affichées séparément.</span><span class="sxs-lookup"><span data-stu-id="12909-214">On the **Summary** tab, the sender and recipient tags are shown separately.</span></span> <span data-ttu-id="12909-215">Les informations relatives aux balises individuelles de l’expéditeur et du destinataire peuvent être exportées en tant que données CSV.</span><span class="sxs-lookup"><span data-stu-id="12909-215">The information about individual tags for sender and recipient can be exported as CSV data.</span></span> 

> [!div class="mx-imgBorder"]
> <span data-ttu-id="12909-216">![Balises de détails du courrier électronique](../../media/tags-flyout.png)</span><span class="sxs-lookup"><span data-stu-id="12909-216">![Email Details tags](../../media/tags-flyout.png)</span></span>

<span data-ttu-id="12909-217">Les informations sur les balises sont également affichées dans le volant des clics d’URL.</span><span class="sxs-lookup"><span data-stu-id="12909-217">Tags information is also shown in the URL clicks flyout.</span></span> <span data-ttu-id="12909-218">Pour le voir, consultez l’affichage Hameçonnage ou Tous les messages > **URL** ou **l’onglet Clics d’URL.** Sélectionnez un volant d’URL individuel pour afficher des détails supplémentaires sur les clics pour cette URL, y compris les balises associées à ce clic.</span><span class="sxs-lookup"><span data-stu-id="12909-218">To see it, go to Phish or All Email view > **URLs** or **URL Clicks** tab. Select an individual URL flyout to see additional details about clicks for that URL, including any Tags associated with that click.</span></span>

### <a name="updated-timeline-view"></a><span data-ttu-id="12909-219">Affichage de chronologie mis à jour</span><span class="sxs-lookup"><span data-stu-id="12909-219">Updated Timeline View</span></span>

> [!div class="mx-imgBorder"]
> <span data-ttu-id="12909-220">![Balises d’URL](../../media/tags-urls.png)</span><span class="sxs-lookup"><span data-stu-id="12909-220">![URL tags](../../media/tags-urls.png)</span></span>
>
<span data-ttu-id="12909-221">Pour en savoir plus, regardez [cette vidéo](https://www.youtube.com/watch?v=UoVzN0lYbfY&list=PL3ZTgFEc7LystRja2GnDeUFqk44k7-KXf&index=4).</span><span class="sxs-lookup"><span data-stu-id="12909-221">Learn more by watching [this video](https://www.youtube.com/watch?v=UoVzN0lYbfY&list=PL3ZTgFEc7LystRja2GnDeUFqk44k7-KXf&index=4).</span></span>

## <a name="extended-capabilities"></a><span data-ttu-id="12909-222">Fonctionnalités étendues</span><span class="sxs-lookup"><span data-stu-id="12909-222">Extended capabilities</span></span>

### <a name="top-targeted-users"></a><span data-ttu-id="12909-223">Utilisateurs les plus ciblés</span><span class="sxs-lookup"><span data-stu-id="12909-223">Top targeted users</span></span>

<span data-ttu-id="12909-224">Les principales familles de programmes malveillants **indiquent les utilisateurs les plus ciblés** dans la section Programmes malveillants.</span><span class="sxs-lookup"><span data-stu-id="12909-224">Top Malware Families shows the **top targeted users** in the Malware section.</span></span> <span data-ttu-id="12909-225">Les utilisateurs les plus ciblés seront également étendus via les affichages Hameçonnage et Tous les e-mails.</span><span class="sxs-lookup"><span data-stu-id="12909-225">Top targeted users will be extended through Phish and All Email views too.</span></span> <span data-ttu-id="12909-226">Les analystes pourront voir les cinq premiers utilisateurs ciblés, ainsi que le nombre de tentatives pour chaque utilisateur dans chaque affichage.</span><span class="sxs-lookup"><span data-stu-id="12909-226">Analysts will be able to see the top-five targeted users, along with the number of attempts for each user in each view.</span></span> 

<span data-ttu-id="12909-227">Les opérations de sécurité peuvent exporter la liste des utilisateurs ciblés, jusqu’à une limite de 3 000, ainsi que le nombre de tentatives réalisées, pour l’analyse hors connexion pour chaque affichage de courrier électronique.</span><span class="sxs-lookup"><span data-stu-id="12909-227">Security operations people be able to export the list of targeted users, up to a limit of 3,000, along with the number of attempts made, for offline analysis for each email view.</span></span> <span data-ttu-id="12909-228">En outre, la sélection du nombre de tentatives (par exemple, 13 tentatives dans l’image ci-dessous) ouvre une vue filtrée dans l’Explorateur de menaces, afin que vous pouvez voir plus de détails sur les messages électroniques et les menaces pour cet utilisateur.</span><span class="sxs-lookup"><span data-stu-id="12909-228">Also, selecting the number of attempts (for example, 13 attempts in the image below) will open a filtered view in Threat Explorer, so you can see more details across emails, and threats for that user.</span></span>  

> [!div class="mx-imgBorder"]
> <span data-ttu-id="12909-229">![Utilisateurs les plus ciblés](../../media/Top_Targeted_Users.png)</span><span class="sxs-lookup"><span data-stu-id="12909-229">![Top targeted users](../../media/Top_Targeted_Users.png)</span></span>

### <a name="exchange-transport-rules"></a><span data-ttu-id="12909-230">Exchange transport</span><span class="sxs-lookup"><span data-stu-id="12909-230">Exchange transport rules</span></span>

<span data-ttu-id="12909-231">L’équipe des opérations de sécurité pourra voir toutes les règles de transport Exchange (ou règles de flux de messagerie) appliquées à un message, dans l’affichage Grille de messagerie.</span><span class="sxs-lookup"><span data-stu-id="12909-231">The security operations team will be able to see all the Exchange transport rules (or Mail flow rules) applied to a message, in the Email grid view.</span></span> <span data-ttu-id="12909-232">Sélectionnez **les options Colonne** dans la grille, puis Exchange règle de transport **à** partir des options de colonne.</span><span class="sxs-lookup"><span data-stu-id="12909-232">Select **Column options** in the grid and then **Add Exchange Transport Rule** from the column options.</span></span> <span data-ttu-id="12909-233">L Exchange des règles de transport est également visible dans le volant **Détails** de l’e-mail.</span><span class="sxs-lookup"><span data-stu-id="12909-233">The Exchange transport rules option is also visible on the **Details** flyout in the email.</span></span> 

<span data-ttu-id="12909-234">Les noms et les GUID des règles de transport appliquées au message s’affichent.</span><span class="sxs-lookup"><span data-stu-id="12909-234">Names and GUIDs of the transport rules applied to the message appear.</span></span> <span data-ttu-id="12909-235">Les analystes pourront rechercher des messages à l’aide du nom de la règle de transport.</span><span class="sxs-lookup"><span data-stu-id="12909-235">Analysts will be able to search for messages by using the name of the transport rule.</span></span> <span data-ttu-id="12909-236">Il s’agit d’une recherche CONTAINS, ce qui signifie que vous pouvez également effectuer des recherches partielles.</span><span class="sxs-lookup"><span data-stu-id="12909-236">This is a CONTAINS search, which means you can do partial searches as well.</span></span> 

> [!IMPORTANT]
> <span data-ttu-id="12909-237">Exchange recherche de règle de transport et la disponibilité du nom dépendent du rôle spécifique qui vous est attribué.</span><span class="sxs-lookup"><span data-stu-id="12909-237">Exchange transport rule search and name availability depend on the specific role assigned to you.</span></span> <span data-ttu-id="12909-238">Vous devez avoir l’un des rôles ou autorisations suivants pour afficher les noms des règles de transport et la recherche.</span><span class="sxs-lookup"><span data-stu-id="12909-238">You need to have one of the following roles or permissions to view the transport rule names and search.</span></span> <span data-ttu-id="12909-239">Toutefois, même sans les rôles ou autorisations ci-dessous, un analyste peut voir l’étiquette de règle de transport et les informations de GUID dans les détails de l’e-mail.</span><span class="sxs-lookup"><span data-stu-id="12909-239">However, even without the roles or permissions below, an analyst may see the transport rule label and GUID information in the Email Details.</span></span> <span data-ttu-id="12909-240">Les autres expériences d’affichage d’enregistrement dans les grilles de courrier électronique, les volants de courrier électronique, les filtres et l’exportation ne sont pas affectées.</span><span class="sxs-lookup"><span data-stu-id="12909-240">Other record-viewing experiences in Email Grids, Email flyouts, Filters, and Export are not affected.</span></span>
>
> - <span data-ttu-id="12909-241">Exchange Online Uniquement - Protection contre la perte de données : tous</span><span class="sxs-lookup"><span data-stu-id="12909-241">Exchange Online Only - Data Loss Prevention: All</span></span>
> - <span data-ttu-id="12909-242">Exchange Online Uniquement - O365SupportViewConfig : Tous</span><span class="sxs-lookup"><span data-stu-id="12909-242">Exchange Online Only - O365SupportViewConfig: All</span></span>
> - <span data-ttu-id="12909-243">Microsoft Azure Active Directory ou Exchange Online - Administrateur de sécurité : Tous</span><span class="sxs-lookup"><span data-stu-id="12909-243">Microsoft Azure Active Directory or Exchange Online - Security Admin: All</span></span>
> - <span data-ttu-id="12909-244">Azure Active Directory ou Exchange Online - Lecteur sécurité : Tous</span><span class="sxs-lookup"><span data-stu-id="12909-244">Azure Active Directory or Exchange Online - Security Reader: All</span></span>
> - <span data-ttu-id="12909-245">Exchange Online Uniquement - Règles de transport : tous</span><span class="sxs-lookup"><span data-stu-id="12909-245">Exchange Online Only - Transport Rules: All</span></span>
> - <span data-ttu-id="12909-246">Exchange Online Uniquement - View-Only configuration : Tous</span><span class="sxs-lookup"><span data-stu-id="12909-246">Exchange Online Only - View-Only Configuration: All</span></span>
>
> <span data-ttu-id="12909-247">Dans la grille de courrier électronique, le volant Détails et le CSV exporté, les ETR sont présentés avec un nom/GUID, comme illustré ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="12909-247">Within the email grid, Details flyout, and Exported CSV, the ETRs are presented with a Name/GUID as shown below.</span></span>
>
> > [!div class="mx-imgBorder"]
> > <span data-ttu-id="12909-248">![Exchange Règles de transport](../../media/ETR_Details.png)</span><span class="sxs-lookup"><span data-stu-id="12909-248">![Exchange Transport Rules](../../media/ETR_Details.png)</span></span>

### <a name="inbound-connectors"></a><span data-ttu-id="12909-249">Connecteurs entrants</span><span class="sxs-lookup"><span data-stu-id="12909-249">Inbound connectors</span></span>

<span data-ttu-id="12909-250">Les connecteurs sont un ensemble d’instructions qui personnalisent la façon dont vos messages électroniques circulent vers et depuis Microsoft 365 ou Office 365 organisation.</span><span class="sxs-lookup"><span data-stu-id="12909-250">Connectors are a collection of instructions that customize how your email flows to and from your Microsoft 365 or Office 365 organization.</span></span> <span data-ttu-id="12909-251">Elles vous permettent d’appliquer des restrictions ou contrôles de sécurité.</span><span class="sxs-lookup"><span data-stu-id="12909-251">They enable you to apply any security restrictions or controls.</span></span> <span data-ttu-id="12909-252">Dans l’Explorateur de menaces, vous pouvez afficher les connecteurs associés à un courrier électronique et rechercher des messages électroniques à l’aide de noms de connecteur.</span><span class="sxs-lookup"><span data-stu-id="12909-252">In Threat Explorer, you can view the connectors that are related to an email and search for emails using connector names.</span></span> 

<span data-ttu-id="12909-253">La recherche de connecteurs est une requête CONTAINS, ce qui signifie que les recherches partielles par mot clé peuvent fonctionner :</span><span class="sxs-lookup"><span data-stu-id="12909-253">The search for connectors is a CONTAINS query, which means partial keyword searches can work:</span></span> 

> [!div class="mx-imgBorder"]
> <span data-ttu-id="12909-254">![Détails du connecteur](../../media/Connector_Details.png)</span><span class="sxs-lookup"><span data-stu-id="12909-254">![Connector details](../../media/Connector_Details.png)</span></span>

## <a name="required-licenses-and-permissions"></a><span data-ttu-id="12909-255">Licences et autorisations requises</span><span class="sxs-lookup"><span data-stu-id="12909-255">Required licenses and permissions</span></span>

<span data-ttu-id="12909-256">Vous devez avoir [Microsoft Defender pour que Office 365](defender-for-office-365.md) utiliser les détections d’explorateur ou en temps réel.</span><span class="sxs-lookup"><span data-stu-id="12909-256">You must have [Microsoft Defender for Office 365](defender-for-office-365.md) to use Explorer or Real-time detections.</span></span>

- <span data-ttu-id="12909-257">L’Explorateur est inclus dans Defender pour Office 365 Plan 2.</span><span class="sxs-lookup"><span data-stu-id="12909-257">Explorer is included in Defender for Office 365 Plan 2.</span></span>
- <span data-ttu-id="12909-258">Le rapport détections en temps réel est inclus dans Defender pour Office 365 Plan 1.</span><span class="sxs-lookup"><span data-stu-id="12909-258">The Real-time detections report is included in Defender for Office 365 Plan 1.</span></span>
- <span data-ttu-id="12909-259">Prévoyez d’attribuer des licences à tous les utilisateurs qui doivent être protégés par Defender Office 365.</span><span class="sxs-lookup"><span data-stu-id="12909-259">Plan to assign licenses for all users who should be protected by Defender for Office 365.</span></span> <span data-ttu-id="12909-260">Les détections d’explorateur et en temps réel montrent les données de détection pour les utilisateurs sous licence.</span><span class="sxs-lookup"><span data-stu-id="12909-260">Explorer and Real-time detections show detection data for licensed users.</span></span>

<span data-ttu-id="12909-261">Pour afficher et utiliser les détections de l’Explorateur ou en temps réel, vous devez avoir les valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="12909-261">To view and use Explorer or Real-time detections, you must have the following:</span></span>

- <span data-ttu-id="12909-262">Pour le Centre de sécurité & conformité :</span><span class="sxs-lookup"><span data-stu-id="12909-262">For the Security & Compliance Center:</span></span>

  - <span data-ttu-id="12909-263">Gestion de l’organisation</span><span class="sxs-lookup"><span data-stu-id="12909-263">Organization Management</span></span>
  - <span data-ttu-id="12909-264">Administrateur de sécurité (peut être affecté dans le centre d’administration Azure Active Directory de sécurité ( <https://aad.portal.azure.com> )</span><span class="sxs-lookup"><span data-stu-id="12909-264">Security Administrator (this can be assigned in the Azure Active Directory admin center (<https://aad.portal.azure.com>)</span></span>
  - <span data-ttu-id="12909-265">Lecteur de sécurité</span><span class="sxs-lookup"><span data-stu-id="12909-265">Security Reader</span></span>

- <span data-ttu-id="12909-266">Pour Exchange Online :</span><span class="sxs-lookup"><span data-stu-id="12909-266">For Exchange Online:</span></span>

  - <span data-ttu-id="12909-267">Gestion de l’organisation</span><span class="sxs-lookup"><span data-stu-id="12909-267">Organization Management</span></span>
  - <span data-ttu-id="12909-268">Afficher uniquement la gestion de l’organisation</span><span class="sxs-lookup"><span data-stu-id="12909-268">View-Only Organization Management</span></span>
  - <span data-ttu-id="12909-269">Afficher uniquement les destinataires</span><span class="sxs-lookup"><span data-stu-id="12909-269">View-Only Recipients</span></span>
  - <span data-ttu-id="12909-270">Gestion de la conformité</span><span class="sxs-lookup"><span data-stu-id="12909-270">Compliance Management</span></span>

<span data-ttu-id="12909-271">Pour en savoir plus sur les rôles et les autorisations, consultez les ressources suivantes :</span><span class="sxs-lookup"><span data-stu-id="12909-271">To learn more about roles and permissions, see the following resources:</span></span>

- [<span data-ttu-id="12909-272">Autorisations dans le centre de conformité et de sécurité</span><span class="sxs-lookup"><span data-stu-id="12909-272">Permissions in the Security & Compliance Center</span></span>](permissions-in-the-security-and-compliance-center.md)
- [<span data-ttu-id="12909-273">Autorisations des fonctionnalités dans Exchange Online</span><span class="sxs-lookup"><span data-stu-id="12909-273">Feature permissions in Exchange Online</span></span>](/exchange/permissions-exo/feature-permissions)
- [<span data-ttu-id="12909-274">Exchange Online PowerShell</span><span class="sxs-lookup"><span data-stu-id="12909-274">Exchange Online PowerShell</span></span>](/powershell/exchange/exchange-online-powershell)

## <a name="more-information"></a><span data-ttu-id="12909-275">Plus d’informations</span><span class="sxs-lookup"><span data-stu-id="12909-275">More information</span></span>

- [<span data-ttu-id="12909-276">Rechercher et d’examiner l’e-mail malveillant qui a été distribué</span><span class="sxs-lookup"><span data-stu-id="12909-276">Find and investigate malicious email that was delivered</span></span>](investigate-malicious-email-that-was-delivered.md) 
- [<span data-ttu-id="12909-277">Afficher les fichiers malveillants détectés dans SharePoint Online, OneDrive et Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="12909-277">View malicious files detected in SharePoint Online, OneDrive, and Microsoft Teams</span></span>](mdo-for-spo-odb-and-teams.md) 
- [<span data-ttu-id="12909-278">Obtenir une vue d’ensemble des affichages dans l’Explorateur de menaces (et détections en temps réel)</span><span class="sxs-lookup"><span data-stu-id="12909-278">Get an overview of the views in Threat Explorer (and Real-time detections)</span></span>](threat-explorer-views.md) 
- [<span data-ttu-id="12909-279">Rapport sur l’état de la protection contre les menaces</span><span class="sxs-lookup"><span data-stu-id="12909-279">Threat protection status report</span></span>](view-email-security-reports.md#threat-protection-status-report) 
- [<span data-ttu-id="12909-280">Examen et réponses automatisés dans Protection Microsoft contre les menaces</span><span class="sxs-lookup"><span data-stu-id="12909-280">Automated investigation and response in Microsoft Threat Protection</span></span>](automated-investigation-response-office.md) 
- [<span data-ttu-id="12909-281">Examiner les e-mails avec la page Entité de messagerie</span><span class="sxs-lookup"><span data-stu-id="12909-281">Investigate emails with the Email Entity Page</span></span>](mdo-email-entity-page.md)