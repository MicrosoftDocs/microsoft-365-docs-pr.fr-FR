---
title: Diagnostic des problèmes de performances avec SharePoint Online
ms.author: kvice
author: kelleyvice-msft
manager: laurawi
ms.date: 7/9/2019
audience: Admin
ms.topic: troubleshooting
ms.service: o365-administration
localization_priority: Normal
ms.collection:
- Ent_O365
- SPO_Content
f1.keywords:
- CSH
ms.custom: Adm_O365
search.appverid:
- SPO160
- MET150
ms.assetid: 3c364f9e-b9f6-4da4-a792-c8e8c8cd2e86
description: Cet article vous explique comment diagnostiquer des problèmes courants avec votre site SharePoint Online à l’aide des outils de développement Internet Explorer.
ms.openlocfilehash: a8a79afd860006a16874370b1124696550dab029
ms.sourcegitcommit: 79065e72c0799064e9055022393113dfcf40eb4b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/14/2020
ms.locfileid: "46689846"
---
# <a name="diagnosing-performance-issues-with-sharepoint-online"></a><span data-ttu-id="eedf7-103">Diagnostic des problèmes de performances avec SharePoint Online</span><span class="sxs-lookup"><span data-stu-id="eedf7-103">Diagnosing performance issues with SharePoint Online</span></span>

<span data-ttu-id="eedf7-104">Cet article vous explique comment diagnostiquer des problèmes courants avec votre site SharePoint Online à l’aide des outils de développement Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="eedf7-104">This article shows you how you can diagnose common issues with your SharePoint Online site using Internet Explorer developer tools.</span></span>
  
<span data-ttu-id="eedf7-105">Il existe trois façons différentes d’identifier qu’une page sur un site SharePoint Online présente un problème de performances avec les personnalisations.</span><span class="sxs-lookup"><span data-stu-id="eedf7-105">There are three different ways that you can identify that a page on a SharePoint Online site has a performance problem with the customizations.</span></span>
  
- <span data-ttu-id="eedf7-106">Moniteur réseau de la barre d’outils F12</span><span class="sxs-lookup"><span data-stu-id="eedf7-106">The F12 tool bar network monitor</span></span>

- <span data-ttu-id="eedf7-107">Comparaison à une ligne de base non personnalisée</span><span class="sxs-lookup"><span data-stu-id="eedf7-107">Comparison to a non-customized baseline</span></span>

- <span data-ttu-id="eedf7-108">Mesures d’en-tête de réponse SharePoint Online</span><span class="sxs-lookup"><span data-stu-id="eedf7-108">SharePoint Online response header metrics</span></span>

<span data-ttu-id="eedf7-109">Cette rubrique décrit comment utiliser chacune de ces méthodes pour diagnostiquer les problèmes de performances.</span><span class="sxs-lookup"><span data-stu-id="eedf7-109">This topic describes how to use each of these methods to diagnose performance issues.</span></span> <span data-ttu-id="eedf7-110">Une fois que vous avez compris la cause du problème, vous pouvez travailler à une solution à l’aide des articles sur l’amélioration des performances SharePoint que vous pouvez trouver sur https://aka.ms/tune .</span><span class="sxs-lookup"><span data-stu-id="eedf7-110">Once you've figured out the cause of the problem, you can work toward a solution using the articles about improving SharePoint performance that you can find on https://aka.ms/tune.</span></span>
  
## <a name="using-the-f12-tool-bar-to-diagnose-performance-in-sharepoint-online"></a><span data-ttu-id="eedf7-111">Utilisation de la barre d’outils F12 pour diagnostiquer les performances dans SharePoint Online</span><span class="sxs-lookup"><span data-stu-id="eedf7-111">Using the F12 tool bar to diagnose performance in SharePoint Online</span></span>
<span data-ttu-id="eedf7-112"><a name="F12ToolInfo"> </a></span><span class="sxs-lookup"><span data-stu-id="eedf7-112"><a name="F12ToolInfo"> </a></span></span>

<span data-ttu-id="eedf7-113">Dans cet article, nous utilisons Internet Explorer 11.</span><span class="sxs-lookup"><span data-stu-id="eedf7-113">In this article we use Internet Explorer 11.</span></span> <span data-ttu-id="eedf7-114">Les versions des outils de développement F12 sur d’autres navigateurs ont des fonctionnalités similaires, bien qu’elles semblent légèrement différentes.</span><span class="sxs-lookup"><span data-stu-id="eedf7-114">Versions of the F12 developer tools on other browsers have similar features though they may look slightly different.</span></span> <span data-ttu-id="eedf7-115">Pour plus d’informations sur les outils de développement F12, voir :</span><span class="sxs-lookup"><span data-stu-id="eedf7-115">For information on the F12 developer tools, see:</span></span>
  
- [<span data-ttu-id="eedf7-116">Nouveautés des outils F12</span><span class="sxs-lookup"><span data-stu-id="eedf7-116">What's new in F12 Tools</span></span>](https://go.microsoft.com/fwlink/p/?LinkId=522545)

- [<span data-ttu-id="eedf7-117">Utilisation des outils de développement F12</span><span class="sxs-lookup"><span data-stu-id="eedf7-117">Using the F12 developer tools</span></span>](https://go.microsoft.com/fwlink/p/?LinkId=522546)

<span data-ttu-id="eedf7-118">Pour faire monter les outils de développement, appuyez **sur F12,** puis cliquez sur Wi-Fi icône :</span><span class="sxs-lookup"><span data-stu-id="eedf7-118">To bring up the developer tools press **F12** and then click the Wi-Fi icon:</span></span>
  
![Capture d’écran de l’icône Wi-Fi des outils de développement F12](../media/27acacbb-5688-459a-aa2f-5c8c5f17b76e.png)
  
<span data-ttu-id="eedf7-120">Sous **l’onglet** Réseau, appuyez sur le bouton vert pour charger une page.</span><span class="sxs-lookup"><span data-stu-id="eedf7-120">On the **Network** tab, press the green play button to load a page.</span></span> <span data-ttu-id="eedf7-121">L’outil renvoie tous les fichiers demandés par le navigateur afin d’obtenir la page que vous avez demandé.</span><span class="sxs-lookup"><span data-stu-id="eedf7-121">The tool returns all of the files that the browser requests in order to get the page you asked for.</span></span> <span data-ttu-id="eedf7-122">La capture d’écran suivante montre une liste de ce type.</span><span class="sxs-lookup"><span data-stu-id="eedf7-122">The following screen shot shows one such list.</span></span>
  
![Capture d’écran de la liste de fichiers renvoyés avec une demande de page.](../media/247a9422-76da-4b0c-bed3-ce77b05e4560.png)
  
<span data-ttu-id="eedf7-124">Vous pouvez également voir les heures de téléchargement des fichiers sur le côté droit, comme illustré dans cette capture d’écran.</span><span class="sxs-lookup"><span data-stu-id="eedf7-124">You can also see the download times of the files on the right side as shown in this screen shot.</span></span>
  
![Diagramme montrant le temps nécessaire pour charger les pages demandées à partir de SharePoint](../media/d71ad1fa-9018-4fae-82eb-c1838e7db0ff.png)
  
<span data-ttu-id="eedf7-126">Cela vous donne une représentation visuelle de la durée de chargement du fichier.</span><span class="sxs-lookup"><span data-stu-id="eedf7-126">This gives you a visual representation of how long the file took to load.</span></span> <span data-ttu-id="eedf7-127">La ligne verte représente le moment où la page est prête à être rendue par le navigateur.</span><span class="sxs-lookup"><span data-stu-id="eedf7-127">The green line represents when the page is ready to be rendered by the browser.</span></span> <span data-ttu-id="eedf7-128">Cela peut vous donner un aperçu rapide des différents fichiers qui peuvent être à l’origine de chargements de page lents sur votre site.</span><span class="sxs-lookup"><span data-stu-id="eedf7-128">This can give you a quick view of the different files that might be causing slow page loads on your site.</span></span>
  
## <a name="setting-up-a-non-customized-baseline-for-sharepoint-online"></a><span data-ttu-id="eedf7-129">Configuration d’une ligne de base non personnalisée pour SharePoint Online</span><span class="sxs-lookup"><span data-stu-id="eedf7-129">Setting up a non-customized baseline for SharePoint Online</span></span>
<span data-ttu-id="eedf7-130"><a name="F12ToolInfo"> </a></span><span class="sxs-lookup"><span data-stu-id="eedf7-130"><a name="F12ToolInfo"> </a></span></span>

<span data-ttu-id="eedf7-131">La meilleure façon de déterminer les points faibles en terme de performances de votre site consiste à configurer une collection de sites totalement pré-prêt à l’utilisation dans SharePoint Online.</span><span class="sxs-lookup"><span data-stu-id="eedf7-131">The best way to determine your site's performance weak points is to set up a completely out-of-the-box site collection in SharePoint Online.</span></span> <span data-ttu-id="eedf7-132">Ainsi, vous pouvez comparer tous les différents aspects de votre site avec ce que vous obtenez sans personnalisation sur la page.</span><span class="sxs-lookup"><span data-stu-id="eedf7-132">This way you can compare all the various aspects of your site with what you would get with no customization on the page.</span></span> <span data-ttu-id="eedf7-133">La page d’accueil OneDrive Entreprise est un bon exemple d’une collection de sites distincte qui n’a probablement pas de personnalisations.</span><span class="sxs-lookup"><span data-stu-id="eedf7-133">The OneDrive for Business home page is a good example of a separate site collection that is unlikely to have any customizations.</span></span>
  
## <a name="viewing-sharepoint-response-header-information"></a><span data-ttu-id="eedf7-134">Affichage des informations d’en-tête de réponse SharePoint</span><span class="sxs-lookup"><span data-stu-id="eedf7-134">Viewing SharePoint response header information</span></span>
<span data-ttu-id="eedf7-135"><a name="F12ToolInfo"> </a></span><span class="sxs-lookup"><span data-stu-id="eedf7-135"><a name="F12ToolInfo"> </a></span></span>

<span data-ttu-id="eedf7-136">Dans SharePoint Online, vous pouvez accéder aux informations renvoyées au navigateur dans l’en-tête de réponse pour chaque fichier.</span><span class="sxs-lookup"><span data-stu-id="eedf7-136">In SharePoint Online, you can access the information that is sent back to the browser in the response header for each file.</span></span> <span data-ttu-id="eedf7-137">La valeur la plus utile pour diagnostiquer les problèmes de performances est **SPRequestDuration**, qui affiche la durée de traitement de la demande sur le serveur.</span><span class="sxs-lookup"><span data-stu-id="eedf7-137">The most useful value for diagnosing performance issues is **SPRequestDuration**, which displays the amount of time that the request took on the server to be processed.</span></span> <span data-ttu-id="eedf7-138">Cela peut aider à déterminer si la demande est très lourde et demande beaucoup de ressources.</span><span class="sxs-lookup"><span data-stu-id="eedf7-138">This can help determine if the request is very heavy and resource intensive.</span></span> <span data-ttu-id="eedf7-139">Il s’agit de la meilleure information que vous avez sur la quantité de travail que le serveur fait pour servir la page.</span><span class="sxs-lookup"><span data-stu-id="eedf7-139">This is the best insight you have into how much work the server is doing to serve the page.</span></span>

### <a name="to-view-sharepoint-response-header-information"></a><span data-ttu-id="eedf7-140">Pour afficher les informations d’en-tête de réponse SharePoint</span><span class="sxs-lookup"><span data-stu-id="eedf7-140">To view SharePoint response header information</span></span>
  
1. <span data-ttu-id="eedf7-141">Assurez-vous que les outils F12 sont installés.</span><span class="sxs-lookup"><span data-stu-id="eedf7-141">Ensure that you have the F12 tools installed.</span></span> <span data-ttu-id="eedf7-142">Pour plus d’informations sur le téléchargement et l’installation de ces outils, voir Nouveautés [des outils F12.](https://go.microsoft.com/fwlink/p/?LinkId=522545)</span><span class="sxs-lookup"><span data-stu-id="eedf7-142">For more information on downloading and installing these tools, see [What's new in F12 tools](https://go.microsoft.com/fwlink/p/?LinkId=522545).</span></span>

2. <span data-ttu-id="eedf7-143">Dans les outils F12, sous **l’onglet** Réseau, appuyez sur le bouton vert pour charger une page.</span><span class="sxs-lookup"><span data-stu-id="eedf7-143">In the F12 tools, on the **Network** tab, press the green play button to load a page.</span></span>

3. <span data-ttu-id="eedf7-144">Cliquez sur l’un des fichiers .aspx renvoyés par l’outil, puis cliquez sur **DÉTAILS.**</span><span class="sxs-lookup"><span data-stu-id="eedf7-144">Click one of the .aspx files returned by the tool and then click **DETAILS**.</span></span>

    ![Affiche les détails de l’en-tête de réponse](../media/1f8a044a-caf8-4613-be2b-7e064141ac8a.png)
  
4. <span data-ttu-id="eedf7-146">Cliquez **sur En-têtes de réponse.**</span><span class="sxs-lookup"><span data-stu-id="eedf7-146">Click **Response headers**.</span></span>

    ![Diagramme présentant l’URL de l’en-tête de réponse](../media/efc7076e-447e-447e-882a-ae3aa721e2c3.png)
  
## <a name="whats-causing-performance-issues-in-sharepoint-online"></a><span data-ttu-id="eedf7-148">Qu’est-ce qui provoque des problèmes de performances dans SharePoint Online ?</span><span class="sxs-lookup"><span data-stu-id="eedf7-148">What's causing performance issues in SharePoint Online?</span></span>
<span data-ttu-id="eedf7-149"><a name="F12ToolInfo"> </a></span><span class="sxs-lookup"><span data-stu-id="eedf7-149"><a name="F12ToolInfo"> </a></span></span>

<span data-ttu-id="eedf7-150">L’article Options de navigation pour [SharePoint Online](navigation-options-for-sharepoint-online.md) montre un exemple d’utilisation de la valeur SPRequestDuration pour déterminer que la navigation structurelle compliquée a provoqué le traitement de la page sur le serveur.</span><span class="sxs-lookup"><span data-stu-id="eedf7-150">The article [Navigation options for SharePoint Online](navigation-options-for-sharepoint-online.md) shows an example of using the SPRequestDuration value to determine that the complicated structural navigation was causing the page to take a long time to process on the server.</span></span> <span data-ttu-id="eedf7-151">En prenant une valeur pour un site de référence (sans personnalisation), il est possible de déterminer si le chargement d’un fichier donné prend beaucoup de temps.</span><span class="sxs-lookup"><span data-stu-id="eedf7-151">By taking a value for a baseline site (without customization), it is possible to determine if any given file is taking a long time to load.</span></span> <span data-ttu-id="eedf7-152">L’exemple utilisé dans [les options de navigation pour SharePoint Online](navigation-options-for-sharepoint-online.md) est le fichier .aspx principal.</span><span class="sxs-lookup"><span data-stu-id="eedf7-152">The example used in [Navigation options for SharePoint Online](navigation-options-for-sharepoint-online.md) is the main .aspx file.</span></span> <span data-ttu-id="eedf7-153">Ce fichier contient la plupart du code ASP.NET qui s’exécute pour le chargement de votre page.</span><span class="sxs-lookup"><span data-stu-id="eedf7-153">That file contains most of the ASP.NET code that runs for your page load.</span></span> <span data-ttu-id="eedf7-154">Selon le modèle de site que vous utilisez, il peut s’agit de start.aspx, home.aspx, default.aspx ou d’un autre nom si vous personnalisez la page d’accueil.</span><span class="sxs-lookup"><span data-stu-id="eedf7-154">Depending on the site template you use, this could be start.aspx, home.aspx, default.aspx, or another name if you customize the home page.</span></span> <span data-ttu-id="eedf7-155">Si ce nombre est beaucoup plus élevé que votre site de référence, cela indique qu’un problème de performances est à l’origine d’un problème dans votre page.</span><span class="sxs-lookup"><span data-stu-id="eedf7-155">If this number is considerably higher than your baseline site, then it's a good indication that there is something complex going on in your page that is causing performance issues.</span></span>
  
<span data-ttu-id="eedf7-156">Une fois que vous avez identifié qu’un problème spécifique à votre site est identifié, la meilleure façon de déterminer ce qui provoque des performances médiocres consiste à éliminer toutes les causes possibles, telles que les personnalisations de page, puis à les rajouter au site une par une.</span><span class="sxs-lookup"><span data-stu-id="eedf7-156">Once you have identified that an issue specific to your site, the recommended way to figure out what is causing poor performance is to eliminate all of the possible causes, like page customizations, and then add them back to the site one by one.</span></span> <span data-ttu-id="eedf7-157">Une fois que vous avez supprimé suffisamment de personnalisations pour que la page s’exécute bien, vous pouvez rajouter des personnalisations spécifiques une par une.</span><span class="sxs-lookup"><span data-stu-id="eedf7-157">Once you have removed enough customizations that the page is performing well, you can then add back specific customizations one by one.</span></span>
  
<span data-ttu-id="eedf7-158">Par exemple, si vous avez une navigation très complexe, essayez de modifier la navigation pour ne pas afficher les sous-sites, puis vérifiez les outils de développement pour voir si cela fait une différence.</span><span class="sxs-lookup"><span data-stu-id="eedf7-158">For example, if you have a very complex navigation try changing the navigation to not show sub-sites then check the developer tools to see if this makes a difference.</span></span> <span data-ttu-id="eedf7-159">Ou si vous avez une grande quantité de roll-ups de contenu, essayez de les supprimer de votre page et de voir si cela améliore les choses.</span><span class="sxs-lookup"><span data-stu-id="eedf7-159">Or if you have a large amount of content roll-ups try removing them from your page and see if this improves things.</span></span> <span data-ttu-id="eedf7-160">Si vous éliminez toutes les causes possibles et que vous les ajoutez une par une, vous pouvez facilement identifier les fonctionnalités qui sont le problème le plus important, puis travailler à une solution.</span><span class="sxs-lookup"><span data-stu-id="eedf7-160">If you eliminate all of the possible causes and add them back in one at a time, you can easily identify which features are the biggest problem and then work towards a solution.</span></span>
