---
title: Minimisation et regroupement dans SharePoint Online
ms.author: kvice
author: kelleyvice-msft
manager: laurawi
ms.date: 3/1/2017
audience: Admin
ms.topic: troubleshooting
ms.service: o365-administration
localization_priority: Normal
ms.collection:
- Ent_O365
- SPO_Content
f1.keywords:
- CSH
ms.custom:
- Adm_O365
- seo-marvel-apr2020
search.appverid:
- SPO160
- MET150
ms.assetid: 87a52468-994e-43a2-b155-7229ed659291
description: Découvrez comment utiliser les techniques de réduction et de regroupement avec Web Essentials pour réduire les demandes HTTP et le temps nécessaire au chargement des pages dans SharePoint Online.
ms.openlocfilehash: 2e2ff7b9d36a6c28ca3840304d896782e1096e85
ms.sourcegitcommit: 79065e72c0799064e9055022393113dfcf40eb4b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/14/2020
ms.locfileid: "46689655"
---
# <a name="minification-and-bundling-in-sharepoint-online"></a><span data-ttu-id="ccc3e-103">Minimisation et regroupement dans SharePoint Online</span><span class="sxs-lookup"><span data-stu-id="ccc3e-103">Minification and bundling in SharePoint Online</span></span>

<span data-ttu-id="ccc3e-104">Cet article explique comment utiliser les techniques de réduction et de regroupement avec Web Essentials pour réduire le nombre de demandes HTTP et réduire le temps nécessaire au chargement des pages dans SharePoint Online.</span><span class="sxs-lookup"><span data-stu-id="ccc3e-104">This article describes how to use minification and bundling techniques with Web Essentials to reduce the number of HTTP requests and to reduce the time it takes to load pages in SharePoint Online.</span></span>
  
<span data-ttu-id="ccc3e-105">Lorsque vous personnalisez votre site web, vous pouvez ajouter un grand nombre de fichiers supplémentaires au serveur pour prendre en charge la personnalisation.</span><span class="sxs-lookup"><span data-stu-id="ccc3e-105">When you customize your website you can end up adding a large number of extra files to the server to support the customization.</span></span> <span data-ttu-id="ccc3e-106">L’ajout de JavaScript, de CSS et d’images supplémentaires augmente le nombre de requêtes HTTP sur le serveur, ce qui augmente le temps d’affichage d’une page web.</span><span class="sxs-lookup"><span data-stu-id="ccc3e-106">Adding extra JavaScript, CSS, and images increases the number of HTTP requests to the server which in turn increases the time it takes to display a web page.</span></span> <span data-ttu-id="ccc3e-107">Si vous avez plusieurs fichiers du même type, vous pouvez regrouper ces fichiers pour accélérer le téléchargement de ces fichiers.</span><span class="sxs-lookup"><span data-stu-id="ccc3e-107">If you have multiple files of the same type, you can bundle these files to make downloading these files faster.</span></span>
  
<span data-ttu-id="ccc3e-108">Pour les fichiers JavaScript et CSS, vous pouvez également utiliser une approche appelée réduction, dans laquelle vous réduisez la taille totale des fichiers en supprimant les espaces et autres caractères qui ne sont pas nécessaires.</span><span class="sxs-lookup"><span data-stu-id="ccc3e-108">For JavaScript and CSS files, you can also use an approach called minification, where you reduce the total size of files by removing whitespace and other characters that aren't necessary.</span></span>
  
## <a name="minification-and-bundling-javascript-and-css-files-with-web-essentials"></a><span data-ttu-id="ccc3e-109">Minification et regroupement de fichiers JavaScript et CSS avec Web Essentials</span><span class="sxs-lookup"><span data-stu-id="ccc3e-109">Minification and bundling JavaScript and CSS files with Web Essentials</span></span>

<span data-ttu-id="ccc3e-110">Vous pouvez utiliser des logiciels tiers tels que Web Essentials pour regrouper les fichiers CSS et JavaScript.</span><span class="sxs-lookup"><span data-stu-id="ccc3e-110">You can use third-party software such as Web Essentials to bundle CSS and JavaScript files.</span></span>
  
> [!IMPORTANT]
> <span data-ttu-id="ccc3e-111">Web Essentials est un projet communautaire tiers, open source.</span><span class="sxs-lookup"><span data-stu-id="ccc3e-111">Web Essentials is a third-party, open-source, community-based project.</span></span> <span data-ttu-id="ccc3e-112">Le logiciel est une extension de Visual Studio 2012 et Visual Studio 2013 et n’est pas pris en charge par Microsoft.</span><span class="sxs-lookup"><span data-stu-id="ccc3e-112">The software is an extension to Visual Studio 2012 and Visual Studio 2013 and is not supported by Microsoft.</span></span> <span data-ttu-id="ccc3e-113">Pour télécharger Web Essentials, visitez le site web à [https://vswebessentials.com/download](https://go.microsoft.com/fwlink/p/?LinkId=525629) l’adresse .</span><span class="sxs-lookup"><span data-stu-id="ccc3e-113">To download Web Essentials, visit the website at [https://vswebessentials.com/download](https://go.microsoft.com/fwlink/p/?LinkId=525629).</span></span> 
  
<span data-ttu-id="ccc3e-114">Web Essentials offre deux formes de regroupement :</span><span class="sxs-lookup"><span data-stu-id="ccc3e-114">Web Essentials offers two forms of bundling:</span></span>
  
- <span data-ttu-id="ccc3e-115">.bundle : pour les fichiers CSS et JavaScript</span><span class="sxs-lookup"><span data-stu-id="ccc3e-115">.bundle: for CSS and JavaScript files</span></span>
    
- <span data-ttu-id="ccc3e-116">.sprite : pour les images (disponible uniquement dans Visual Studio 2013)</span><span class="sxs-lookup"><span data-stu-id="ccc3e-116">.sprite: for images (only available in Visual Studio 2013)</span></span>
    
<span data-ttu-id="ccc3e-117">Vous pouvez utiliser Web Essentials si vous disposez d’une fonctionnalité existante avec certains éléments de personnalisation référencés dans une page maître personnalisée, telles que :</span><span class="sxs-lookup"><span data-stu-id="ccc3e-117">You can use Web Essentials if you have an existing feature with some branding elements that are referenced inside a custom master page, such as:</span></span>
  
![Capture d’écran de l’élément de marque sur la page maître personnalisée](../media/3a6eba36-973d-482b-8556-a9394b8ba19f.png)
  
 <span data-ttu-id="ccc3e-119">**Pour créer un ensemble TE000127218 et CSS dans Web Essentials**</span><span class="sxs-lookup"><span data-stu-id="ccc3e-119">**To create a TE000127218 and CSS bundle in Web Essentials**</span></span>
  
1. <span data-ttu-id="ccc3e-120">Dans Visual Studio, dans l’Explorateur de solutions, sélectionnez les fichiers que vous souhaitez inclure dans le fichier groupé.</span><span class="sxs-lookup"><span data-stu-id="ccc3e-120">In Visual Studio, in Solution Explorer, select the files that you want to include in the bundle.</span></span>
    
2. <span data-ttu-id="ccc3e-121">Cliquez avec le bouton droit sur les fichiers sélectionnés, puis sélectionnez **Web Essentials** Créer un fichier groupé \> **JavaScript** dans le menu contextif.</span><span class="sxs-lookup"><span data-stu-id="ccc3e-121">Right-click the selected files and then select **Web Essentials** \> **Create JavaScript bundle file** from the context menu.</span></span> <span data-ttu-id="ccc3e-122">Par exemple :</span><span class="sxs-lookup"><span data-stu-id="ccc3e-122">For example:</span></span> 
    
    ![Capture d’écran montrant les options de menu Web Essentials](../media/41aac84c-4538-4f78-b454-46e651f868a3.png)
  
## <a name="viewing-the-results-of-bundling-javascript-and-css-files"></a><span data-ttu-id="ccc3e-124">Affichage des résultats du regroupement de fichiers JavaScript et CSS</span><span class="sxs-lookup"><span data-stu-id="ccc3e-124">Viewing the results of bundling JavaScript and CSS files</span></span>

<span data-ttu-id="ccc3e-125">Lorsque vous créez un fichier groupé JavaScript et CSS, Web Essentials crée un fichier XML appelé fichier de recette qui identifie les fichiers JavaScript et CSS, ainsi que d’autres informations de configuration :</span><span class="sxs-lookup"><span data-stu-id="ccc3e-125">When you create a JavaScript and CSS bundle, Web Essentials creates an XML file called a recipe file that identifies the JavaScript and CSS files as well as some other configuration information:</span></span> 
  
![Capture d’écran du fichier de recette CSS et JavaScript](../media/7ba891f8-52d8-467b-a0f6-b062dd1137a4.png)
  
<span data-ttu-id="ccc3e-127">En outre, si l’indicateur de réduction est définie sur true dans la recette de regroupement, les fichiers sont réduits en taille et regroupés.</span><span class="sxs-lookup"><span data-stu-id="ccc3e-127">In addition, if the minify flag is set to true in the bundling recipe the files are reduced in size as well as bundled together.</span></span> <span data-ttu-id="ccc3e-128">Cela signifie que de nouvelles versions minifiées des fichiers JavaScript ont été créées que vous pouvez référencer dans votre page maître.</span><span class="sxs-lookup"><span data-stu-id="ccc3e-128">This means that new, minified versions of the JavaScript files were created that you can reference in your master page.</span></span>
  
![Capture d’écran de l’indicateur minify défini sur True](../media/50523af2-6412-4117-ac3d-5bd26f6d562e.png)
  
<span data-ttu-id="ccc3e-130">Lorsque vous chargez une page à partir de votre site web, vous pouvez utiliser les outils de développement de votre navigateur web, tels qu’Internet Explorer 11, pour voir le nombre de demandes envoyées au serveur et la durée de chargement de chaque fichier.</span><span class="sxs-lookup"><span data-stu-id="ccc3e-130">When you load a page from your web site, you can use the developer tools from your web browser, such as Internet Explorer 11, to see the number of requests sent to the server and how long each file took to load.</span></span>
  
<span data-ttu-id="ccc3e-131">La figure suivante est le résultat du chargement des fichiers JavaScript et CSS avant la minification.</span><span class="sxs-lookup"><span data-stu-id="ccc3e-131">The following figure is the result of loading the JavaScript and CSS files before minification.</span></span>
  
![Capture d’écran montrant 80 éléments en cours de téléchargement](../media/e2df3912-1923-46e6-8cf2-3015a31554e1.png)
  
<span data-ttu-id="ccc3e-133">Après avoir groupé les fichiers CSS et JavaScript, le nombre de demandes abandonnées à 74 et chaque fichier n’a pris que légèrement plus de temps que les fichiers d’origine à télécharger individuellement :</span><span class="sxs-lookup"><span data-stu-id="ccc3e-133">After bundling the CSS and JavaScript files together, the number of requests dropped to 74 and each file took only slightly longer than the original files to download individually:</span></span>
  
![Capture d’écran montrant 74 éléments en cours de téléchargement](../media/686c4387-70e8-4a74-9d45-059f33a91184.png)
  
<span data-ttu-id="ccc3e-135">Après le regroupement, le fichier groupé JavaScript est considérablement réduit de 815 000 à 365 000 000 :</span><span class="sxs-lookup"><span data-stu-id="ccc3e-135">After bundling, the JavaScript bundle file is reduced significantly from 815KB to 365KB:</span></span>
  
![Capture d’écran montrant une taille de téléchargement réduite](../media/5e7dbd98-faff-4f68-b320-108fb252e395.png)
  
## <a name="bundling-images-by-creating-an-image-sprite"></a><span data-ttu-id="ccc3e-137">Regroupement d’images en créant un sprite d’image</span><span class="sxs-lookup"><span data-stu-id="ccc3e-137">Bundling images by creating an image sprite</span></span>

<span data-ttu-id="ccc3e-138">À l’image de la façon dont vous regroupez des fichiers JavaScript et CSS, vous pouvez combiner de nombreuses petites icônes et autres images communes dans une feuille de sprite plus grande, puis utiliser CSS pour révéler les images individuelles.</span><span class="sxs-lookup"><span data-stu-id="ccc3e-138">Similar to how you bundle JavaScript and CSS files, you can combine many small icons and other common images into a larger sprite sheet and then use CSS to reveal the individual images.</span></span> <span data-ttu-id="ccc3e-139">Au lieu de télécharger chaque image individuelle, le navigateur web de l’utilisateur télécharge une seule fois la feuille de sprite, puis la met en cache sur l’ordinateur local.</span><span class="sxs-lookup"><span data-stu-id="ccc3e-139">Instead of downloading each individual image, the user's web browser downloads the sprite sheet once and then caches it on the local computer.</span></span> <span data-ttu-id="ccc3e-140">Cela améliore les performances de chargement des pages en réduisant le nombre de téléchargements et d’allers-retours vers le serveur web.</span><span class="sxs-lookup"><span data-stu-id="ccc3e-140">This improves page load performance by cutting down on the number of downloads and round trips to the web server.</span></span>
  
 <span data-ttu-id="ccc3e-141">**Pour créer un sprite d’image dans Web Essentials**</span><span class="sxs-lookup"><span data-stu-id="ccc3e-141">**To create an image sprite in Web Essentials**</span></span>
  
1. <span data-ttu-id="ccc3e-142">Dans Visual Studio, dans l’Explorateur de solutions, sélectionnez les fichiers que vous souhaitez inclure dans le fichier groupé.</span><span class="sxs-lookup"><span data-stu-id="ccc3e-142">In Visual Studio, in Solution Explorer, select the files that you want to include in the bundle.</span></span>
    
2. <span data-ttu-id="ccc3e-143">Cliquez avec le bouton droit sur les fichiers sélectionnés, puis sélectionnez **Web Essentials** Créer un \> **sprite d’image** dans le menu contextiqué.</span><span class="sxs-lookup"><span data-stu-id="ccc3e-143">Right-click the selected files and then select **Web Essentials** \> **Create image sprite** from the context menu.</span></span> <span data-ttu-id="ccc3e-144">Par exemple :</span><span class="sxs-lookup"><span data-stu-id="ccc3e-144">For example:</span></span> 
    
    ![Capture d’écran montrant comment créer une image-objet](../media/de0fe741-4ef7-4e3b-bafa-ef9f4822dac6.png)
  
3. <span data-ttu-id="ccc3e-146">Choisissez un emplacement pour enregistrer le fichier sprite.</span><span class="sxs-lookup"><span data-stu-id="ccc3e-146">Choose a location to save the sprite file.</span></span> <span data-ttu-id="ccc3e-147">Le fichier .sprite est un fichier XML qui décrit les paramètres et les fichiers du sprite.</span><span class="sxs-lookup"><span data-stu-id="ccc3e-147">The .sprite file is an XML file that describes the settings and files in the sprite.</span></span> <span data-ttu-id="ccc3e-148">Les figures suivantes illustrent un fichier PNG sprite et son fichier XML .sprite correspondant.</span><span class="sxs-lookup"><span data-stu-id="ccc3e-148">The following figures show an example of a sprite PNG file and its corresponding .sprite XML file.</span></span>
    
    ![Capture d’écran d’un fichier d’image-objet](../media/0876bb2a-d1b9-4169-8e95-9c290d628d90.png)
  
    ![Capture d’écran d’un fichier XML d’image-objet](../media/d1f94776-280d-4d56-abb5-384f145d9989.png)
  

