---
title: Différer le chargement des images et des éléments JavaScript dans SharePoint Online
ms.author: kvice
author: kelleyvice-msft
manager: laurawi
ms.date: 12/3/2019
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
ms.assetid: 74d327e5-755f-4135-b9a5-7b79578c1bf9
description: Découvrez comment réduire le temps de chargement des pages SharePoint Online à l’aide de JavaScript pour retarder le chargement des images et du JavaScript non essentiel.
ms.openlocfilehash: 86b93c4e1e102132bb0c1bfb9a413233529adecb
ms.sourcegitcommit: 27b2b2e5c41934b918cac2c171556c45e36661bf
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/19/2021
ms.locfileid: "50919163"
---
# <a name="delay-loading-images-and-javascript-in-sharepoint-online"></a><span data-ttu-id="859b1-103">Différer le chargement des images et des éléments JavaScript dans SharePoint Online</span><span class="sxs-lookup"><span data-stu-id="859b1-103">Delay loading images and JavaScript in SharePoint Online</span></span>

<span data-ttu-id="859b1-104">Cet article explique comment réduire le temps de chargement des pages SharePoint Online à l’aide de JavaScript pour retarder le chargement des images et en attendant de charger du JavaScript non essentiel jusqu’au chargement de la page.</span><span class="sxs-lookup"><span data-stu-id="859b1-104">This article describes how you can decrease the load time for SharePoint Online pages by using JavaScript to delay loading images and also by waiting to load non-essential JavaScript until after the page loads.</span></span>
  
<span data-ttu-id="859b1-105">Les images peuvent avoir une incidence négative sur les vitesses de chargement des pages sur SharePoint Online.</span><span class="sxs-lookup"><span data-stu-id="859b1-105">Images can negatively affect page load speeds on SharePoint Online.</span></span> <span data-ttu-id="859b1-106">Par défaut, la plupart des navigateurs Internet modernes pré-récupèrent les images lors du chargement d’une page HTML.</span><span class="sxs-lookup"><span data-stu-id="859b1-106">By default, most modern Internet browsers pre-fetch images when loading an HTML page.</span></span> <span data-ttu-id="859b1-107">Cela peut ralentir inutilement le chargement de la page si les images ne sont pas visibles à l’écran jusqu’à ce que l’utilisateur défile vers le bas.</span><span class="sxs-lookup"><span data-stu-id="859b1-107">This can cause the page to be unnecessarily slow to load if the images are not visible on the screen until the user scrolls down.</span></span> <span data-ttu-id="859b1-108">Les images peuvent empêcher le navigateur de charger la partie visible de la page.</span><span class="sxs-lookup"><span data-stu-id="859b1-108">The images can block the browser from loading the visible part of the page.</span></span> <span data-ttu-id="859b1-109">Pour contourner ce problème, vous pouvez utiliser JavaScript pour ignorer d’abord le chargement des images.</span><span class="sxs-lookup"><span data-stu-id="859b1-109">To work around this problem, you can use JavaScript to skip loading the images first.</span></span> <span data-ttu-id="859b1-110">En outre, le chargement de JavaScript non essentiels peut ralentir les temps de téléchargement sur SharePoint pages.</span><span class="sxs-lookup"><span data-stu-id="859b1-110">Also, loading non-essential JavaScript can slow download times on your SharePoint pages too.</span></span> <span data-ttu-id="859b1-111">Cette rubrique décrit certaines méthodes que vous pouvez utiliser pour améliorer les temps de chargement de page avec JavaScript dans SharePoint Online.</span><span class="sxs-lookup"><span data-stu-id="859b1-111">This topic describes some methods you can use to improve page load times with JavaScript in SharePoint Online.</span></span>
  
## <a name="improve-page-load-times-by-delaying-image-loading-in-sharepoint-online-pages-by-using-javascript"></a><span data-ttu-id="859b1-112">Améliorer les temps de chargement des pages en retardant le chargement des images dans SharePoint pages en ligne à l’aide de JavaScript</span><span class="sxs-lookup"><span data-stu-id="859b1-112">Improve page load times by delaying image loading in SharePoint Online pages by using JavaScript</span></span>

<span data-ttu-id="859b1-113">Vous pouvez utiliser JavaScript pour empêcher un navigateur web de pré-récupérer des images.</span><span class="sxs-lookup"><span data-stu-id="859b1-113">You can use JavaScript to prevent a web browser from pre-fetching images.</span></span> <span data-ttu-id="859b1-114">Cela accélère le rendu global du document.</span><span class="sxs-lookup"><span data-stu-id="859b1-114">This speeds up overall document rendering.</span></span> <span data-ttu-id="859b1-115">Pour ce faire, vous supprimez la valeur de l’attribut src de la balise et remplacez-la par le chemin d’accès à un fichier dans un attribut de données tel que \<img\> : data-src.</span><span class="sxs-lookup"><span data-stu-id="859b1-115">To do this you remove the value of the src attribute from the \<img\> tag and replace it with the path to a file in a data attribute such as: data-src.</span></span> <span data-ttu-id="859b1-116">Par exemple :</span><span class="sxs-lookup"><span data-stu-id="859b1-116">For example:</span></span>
  
```html
<img src="" data-src="/sites/NavigationBySearch/_catalogs/masterpage/media/microsoft-white-8.jpg" />
```

<span data-ttu-id="859b1-117">À l’aide de cette méthode, le navigateur ne télécharge pas immédiatement les images.</span><span class="sxs-lookup"><span data-stu-id="859b1-117">By using this method, the browser doesn't download the images immediately.</span></span> <span data-ttu-id="859b1-118">Si l’image se trouve déjà dans la fenêtre d’affichage, JavaScript indique au navigateur de récupérer l’URL de l’attribut de données et de l’insérer en tant que valeur pour l’attribut src.</span><span class="sxs-lookup"><span data-stu-id="859b1-118">If the image is already in the viewport, JavaScript tells the browser to retrieve the URL from the data attribute and insert it as the value for the src attribute.</span></span> <span data-ttu-id="859b1-119">L’image se charge uniquement à mesure que l’utilisateur défile et qu’elle s’affiche.</span><span class="sxs-lookup"><span data-stu-id="859b1-119">The image only loads as the user scrolls and it comes into view.</span></span>
  
<span data-ttu-id="859b1-120">Pour que tout cela se produise, vous devez utiliser JavaScript.</span><span class="sxs-lookup"><span data-stu-id="859b1-120">To make all of this happen, you'll need to use JavaScript.</span></span>
  
<span data-ttu-id="859b1-121">Dans un fichier texte, définissez la fonction **isElementInViewport()** pour vérifier si un élément se trouve dans la partie du navigateur visible par l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="859b1-121">In a text file, define the **isElementInViewport()** function to check whether or not an element is in the part of the browser that is visible to the user.</span></span>
  
```javascript
function isElementInViewport(el) {
  if (!el)
    return false;
  var rect = el.getBoundingClientRect();
  return (
    rect.top >= 0 &amp;&amp;
    rect.left >= 0 &amp;&amp;
    rect.bottom <= (window.innerHeight || document.documentElement.clientHeight) &amp;&amp;
    rect.right <= (window.innerWidth || document.documentElement.clientWidth)
  );
}
```

<span data-ttu-id="859b1-122">Ensuite, utilisez **isElementInViewport()** dans la **fonction loadItemsInView().**</span><span class="sxs-lookup"><span data-stu-id="859b1-122">Next, use **isElementInViewport()** in the **loadItemsInView()** function.</span></span> <span data-ttu-id="859b1-123">La **fonction loadItemsInView()** charge toutes les images qui ont une valeur pour l’attribut data-src s’ils se trouve dans la partie du navigateur visible par l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="859b1-123">The **loadItemsInView()** function will load all images that have a value for the data-src attribute if they are in the part of the browser that is visible to the user.</span></span> <span data-ttu-id="859b1-124">Ajoutez la fonction suivante au fichier texte :</span><span class="sxs-lookup"><span data-stu-id="859b1-124">Add the following function to the text file:</span></span>
  
```javascript
function loadItemsInView() {
  //Select elements by the row id.
  $("#row [data-src]").each(function () {
      var isVisible = isElementInViewport(this);
      if (isVisible) {
          if ($(this).attr("src") == undefined) {
              $(this).attr("src", $(this).data("src"));
          }
      }
  });
}
```

<span data-ttu-id="859b1-125">Enfin, **appelez loadItemsInView()** à partir de **window.onscroll()** comme illustré dans l’exemple suivant.</span><span class="sxs-lookup"><span data-stu-id="859b1-125">Finally, call **loadItemsInView()** from within **window.onscroll()** as shown in the following example.</span></span> <span data-ttu-id="859b1-126">Cela garantit que toutes les images qui se trouveraient dans laport d’affichage sont chargées en tant que l’utilisateur en a besoin, mais pas avant.</span><span class="sxs-lookup"><span data-stu-id="859b1-126">This ensures that any images that are in the viewport are loaded as the user needs them, but not before.</span></span> <span data-ttu-id="859b1-127">Ajoutez ce qui suit au fichier texte :</span><span class="sxs-lookup"><span data-stu-id="859b1-127">Add the following to the text file:</span></span>
  
```javascript
//Example of calling loadItemsInView() from within window.onscroll()
$(window).on("scroll", function () {
    loadItemsInView();
});

```

<span data-ttu-id="859b1-128">Pour SharePoint Online, vous devez attacher la fonction suivante à l’événement de défilement sur la balise #s4-workspace. \<div\></span><span class="sxs-lookup"><span data-stu-id="859b1-128">For SharePoint Online, you need to attach the following function to the scroll event on the #s4-workspace \<div\> tag.</span></span> <span data-ttu-id="859b1-129">Cela est dû au fait que les événements de fenêtre sont surchargés afin de s’assurer que le ruban reste attaché au haut de la page.</span><span class="sxs-lookup"><span data-stu-id="859b1-129">This is because the window events are overridden in order to ensure the ribbon remains attached to the top of the page.</span></span>
  
```javascript
//Keep the ribbon at the top of the page
$('#s4-workspace').on("scroll", function () {
    loadItemsInView();
});
```

<span data-ttu-id="859b1-130">Enregistrez le fichier texte en tant que fichier JavaScript avec l’extension .js, par exemple delayLoadImages.js.</span><span class="sxs-lookup"><span data-stu-id="859b1-130">Save the text file as a JavaScript file with the extension .js, for example delayLoadImages.js.</span></span>
  
<span data-ttu-id="859b1-131">Une fois que vous avez terminé delayLoadImages.js, vous pouvez ajouter le contenu du fichier à une page maître dans SharePoint Online.</span><span class="sxs-lookup"><span data-stu-id="859b1-131">Once you've finished writing delayLoadImages.js, you can add the contents of the file to a master page in SharePoint Online.</span></span> <span data-ttu-id="859b1-132">Pour ce faire, ajoutez un lien de script à l’en-tête de la page maître.</span><span class="sxs-lookup"><span data-stu-id="859b1-132">You do this by adding a script link to the header in the master page.</span></span> <span data-ttu-id="859b1-133">Une fois qu’il est dans une page maître, le JavaScript est appliqué à toutes les pages de votre site SharePoint Online qui utilisent cette mise en page maître.</span><span class="sxs-lookup"><span data-stu-id="859b1-133">Once it's in a master page, the JavaScript will be applied to all pages in your SharePoint Online site that use that master page layout.</span></span> <span data-ttu-id="859b1-134">Sinon, si vous avez l’intention de l’utiliser uniquement sur une page de votre site, utilisez le script éditeur de web part pour incorporer le JavaScript dans la page.</span><span class="sxs-lookup"><span data-stu-id="859b1-134">Alternatively, if you intend to only use this on one page of your site, use the script editor Web Part to embed the JavaScript into the page.</span></span> <span data-ttu-id="859b1-135">Pour plus d’informations, consultez ces rubriques :</span><span class="sxs-lookup"><span data-stu-id="859b1-135">See these topics for more information:</span></span>
  
- [<span data-ttu-id="859b1-136">Comment appliquer une page maître à un site dans SharePoint 2013</span><span class="sxs-lookup"><span data-stu-id="859b1-136">How to: Apply a master page to a site in SharePoint 2013</span></span>](/sharepoint/dev/general-development/how-to-apply-a-master-page-to-a-site-in-sharepoint)

- [<span data-ttu-id="859b1-137">Procédure : Créer une mise en page dans SharePoint 2013</span><span class="sxs-lookup"><span data-stu-id="859b1-137">How to: Create a page layout in SharePoint 2013</span></span>](/sharepoint/dev/general-development/how-to-create-a-page-layout-in-sharepoint)

### <a name="example-referencing-the-javascript-delayloadimagesjs-file-from-a-master-page-in-sharepoint-online"></a><span data-ttu-id="859b1-138">Exemple : référencement du fichier delayLoadImages.js JavaScript à partir d’une page maître dans SharePoint Online</span><span class="sxs-lookup"><span data-stu-id="859b1-138">Example: Referencing the JavaScript delayLoadImages.js file from a master page in SharePoint Online</span></span>
  
<span data-ttu-id="859b1-139">Pour que cela fonctionne, vous devez également référencer jQuery dans la page maître.</span><span class="sxs-lookup"><span data-stu-id="859b1-139">In order for this to work, you also need to reference jQuery in the master page.</span></span> <span data-ttu-id="859b1-140">Dans l’exemple suivant, vous pouvez voir dans le chargement initial de la page qu’une seule image est chargée, mais qu’il en existe plusieurs autres sur la page.</span><span class="sxs-lookup"><span data-stu-id="859b1-140">In the following example, you can see in the initial page load that there is only one image loaded but there are several more on the page.</span></span>
  
![Capture d’écran montrant une seule image chargée sur une page](../media/3d177ddb-67e5-43a7-b327-c9f9566ca937.png)
  
<span data-ttu-id="859b1-142">La capture d’écran suivante montre le reste des images qui sont téléchargées après leur défilement vers l’affichage.</span><span class="sxs-lookup"><span data-stu-id="859b1-142">The following screenshot shows the rest of the images that are downloaded after they scroll into view.</span></span>
  
![Capture d’écran montrant plusieurs images chargées sur une page](../media/95eb2b14-f6a1-4eac-a5cb-96097e49514c.png)
  
<span data-ttu-id="859b1-144">Retarder le chargement de l’image à l’aide de JavaScript peut être une technique efficace pour augmenter les performances . toutefois, si la technique est appliquée sur un site web public, les moteurs de recherche ne sont pas en mesure d’analyser les images de la même façon qu’ils analysent une image formée régulièrement.</span><span class="sxs-lookup"><span data-stu-id="859b1-144">Delaying image loading by using JavaScript can be an effective technique in increasing performance; however, if the technique is applied on a public website then search engines are not able to crawl the images in the same way they would crawl a regularly formed image.</span></span> <span data-ttu-id="859b1-145">Cela peut affecter les classements sur les moteurs de recherche, car les métadonnées sur l’image elle-même ne sont pas réellement présentes tant que la page n’est pas en cours de chargement.</span><span class="sxs-lookup"><span data-stu-id="859b1-145">This can affect rankings on search engines because metadata on the image itself is not really there until the page loads.</span></span> <span data-ttu-id="859b1-146">Les robot d’un moteur de recherche lisent uniquement le code HTML et, par conséquent, ne voient pas les images en tant que contenu sur la page.</span><span class="sxs-lookup"><span data-stu-id="859b1-146">Search engine crawlers only read the HTML and therefore will not see the images as content on the page.</span></span> <span data-ttu-id="859b1-147">Les images sont l’un des facteurs utilisés pour classer les pages dans les résultats de la recherche.</span><span class="sxs-lookup"><span data-stu-id="859b1-147">Images are one of the factors used to rank pages in search results.</span></span> <span data-ttu-id="859b1-148">L’une des façons de contourner ce besoin consiste à utiliser du texte d’introduction pour vos images.</span><span class="sxs-lookup"><span data-stu-id="859b1-148">One way to work around this is to use introductory text for your images.</span></span>
  
## <a name="github-code-sample-injecting-javascript-to-improve-performance"></a><span data-ttu-id="859b1-149">GitHub code : injection de JavaScript pour améliorer les performances</span><span class="sxs-lookup"><span data-stu-id="859b1-149">GitHub code sample: Injecting JavaScript to improve performance</span></span>

<span data-ttu-id="859b1-150">Ne manquez pas l’article et l’exemple de code sur [l’injection JavaScript](https://go.microsoft.com/fwlink/p/?LinkId=524759) fournis GitHub.</span><span class="sxs-lookup"><span data-stu-id="859b1-150">Don't miss the article and code sample on [JavaScript injection](https://go.microsoft.com/fwlink/p/?LinkId=524759) provided on GitHub.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="859b1-151">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="859b1-151">See also</span></span>

[<span data-ttu-id="859b1-152">Navigateurs pris en charge dans Office 2013 et Applications Microsoft 365 pour les grandes entreprises</span><span class="sxs-lookup"><span data-stu-id="859b1-152">Supported browsers in Office 2013 and Microsoft 365 Apps for enterprise</span></span>](https://support.office.com/article/57342811-0dc4-4316-b773-20082ced8a82)
  
[<span data-ttu-id="859b1-153">Comment appliquer une page maître à un site dans SharePoint 2013</span><span class="sxs-lookup"><span data-stu-id="859b1-153">How to: Apply a master page to a site in SharePoint 2013</span></span>](/sharepoint/dev/general-development/how-to-apply-a-master-page-to-a-site-in-sharepoint)
  
[<span data-ttu-id="859b1-154">Procédure : Créer une mise en page dans SharePoint 2013</span><span class="sxs-lookup"><span data-stu-id="859b1-154">How to: Create a page layout in SharePoint 2013</span></span>](/sharepoint/dev/general-development/how-to-create-a-page-layout-in-sharepoint)