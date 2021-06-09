---
title: Modifier un dictionnaire de mots clés
f1.keywords:
- NOCSH
ms.author: chrfox
author: chrfox
manager: laurawi
audience: Admin
ms.topic: article
ms.service: O365-seccomp
ms.date: ''
localization_priority: Normal
ms.collection:
- M365-security-compliance
search.appverid:
- MOE150
- MET150
ms.custom:
- seo-marvel-apr2020
description: Découvrez comment modifier un dictionnaire de mots clés dans le centre Microsoft 365 conformité.
ms.openlocfilehash: 93357d153d9c6a2a4521d1604b2a1cb8cbcec48c
ms.sourcegitcommit: a6fb731fdf726d7d9fe4232cf69510013f2b54ce
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/27/2021
ms.locfileid: "52685204"
---
# <a name="modify-a-keyword-dictionary"></a><span data-ttu-id="6a8ff-103">Modifier un dictionnaire de mots clés</span><span class="sxs-lookup"><span data-stu-id="6a8ff-103">Modify a keyword dictionary</span></span>

<span data-ttu-id="6a8ff-104">Vous devrez peut-être modifier des mots clés dans l’un de vos dictionnaires de mots clés ou modifier l’un des dictionnaires intégrés.</span><span class="sxs-lookup"><span data-stu-id="6a8ff-104">You might need to modify keywords in one of your keyword dictionaries, or modify one of the built-in dictionaries.</span></span> <span data-ttu-id="6a8ff-105">Vous pouvez le faire via PowerShell ou via le Centre de conformité.</span><span class="sxs-lookup"><span data-stu-id="6a8ff-105">You can do this through PowerShell or through the Compliance center.</span></span>

## <a name="modify-a-keyword-dictionary-in-compliance-center"></a><span data-ttu-id="6a8ff-106">Modifier un dictionnaire de mots clés dans le Centre de conformité</span><span class="sxs-lookup"><span data-stu-id="6a8ff-106">Modify a keyword dictionary in Compliance center</span></span>

<span data-ttu-id="6a8ff-107">Les dictionnaires de mots clés peuvent être utilisés en tant que modèles `Primary elements` `Supporting elements` de type d’informations sensibles (SIT).</span><span class="sxs-lookup"><span data-stu-id="6a8ff-107">Keyword dictionaries can be used as `Primary elements` or `Supporting elements` in sensitive information type (SIT) patterns.</span></span> <span data-ttu-id="6a8ff-108">Vous pouvez modifier un dictionnaire de mots clés lors de la création d’un sit ou d’un sit existant.</span><span class="sxs-lookup"><span data-stu-id="6a8ff-108">You can edit a keyword dictionary while creating a SIT or in an existing SIT.</span></span> <span data-ttu-id="6a8ff-109">Par exemple, pour modifier un dictionnaire de mots clés existant :</span><span class="sxs-lookup"><span data-stu-id="6a8ff-109">For example to edit an existing keyword dictionary:</span></span>

1. <span data-ttu-id="6a8ff-110">Ouvrez le modèle qui possède le dictionnaire de mots clés que vous souhaitez mettre à jour.</span><span class="sxs-lookup"><span data-stu-id="6a8ff-110">Open the pattern that has the keyword dictionary you want to update.</span></span>
2. <span data-ttu-id="6a8ff-111">Recherchez le dictionnaire de mots clés que vous souhaitez mettre à jour et sélectionnez Modifier.</span><span class="sxs-lookup"><span data-stu-id="6a8ff-111">Find the keyword dictionary you want to update and choose edit.</span></span> 
3.  <span data-ttu-id="6a8ff-112">A effectuer vos modifications à l’aide d’un mot clé par ligne.</span><span class="sxs-lookup"><span data-stu-id="6a8ff-112">Make your edits, using one keyword per line.</span></span>

![capture d’écran modifier les mots clés](../media/edit-keyword-dictionary.png)

4. <span data-ttu-id="6a8ff-114">Choose `Done` .</span><span class="sxs-lookup"><span data-stu-id="6a8ff-114">Choose `Done`.</span></span>

## <a name="modify-a-keyword-dictionary-using-powershell"></a><span data-ttu-id="6a8ff-115">Modifier un dictionnaire de mots clés à l’aide de PowerShell</span><span class="sxs-lookup"><span data-stu-id="6a8ff-115">Modify a keyword dictionary using PowerShell</span></span> 

<span data-ttu-id="6a8ff-116">Par exemple, nous allons modifier certains termes dans PowerShell, les enregistrer localement pour qu’ils puissent être modifiés dans un éditeur, puis mettre à jour les termes précédemment intégrés.</span><span class="sxs-lookup"><span data-stu-id="6a8ff-116">For example, we'll modify some terms in PowerShell, save the terms locally where you can modify them in an editor, and then update the previous terms in place.</span></span> 

<span data-ttu-id="6a8ff-117">Tout d’abord, récupérez l’objet dictionnaire :</span><span class="sxs-lookup"><span data-stu-id="6a8ff-117">First, retrieve the dictionary object:</span></span>
  
```powershell
$dict = Get-DlpKeywordDictionary -Name "Diseases"
```

<span data-ttu-id="6a8ff-118">L’impression  `$dict` affichera les différentes variables.</span><span class="sxs-lookup"><span data-stu-id="6a8ff-118">Printing  `$dict` will show the various variables.</span></span> <span data-ttu-id="6a8ff-119">Les mots clés eux-mêmes sont stockés dans un objet sur le serveur principal, mais  `$dict.KeywordDictionary` contient une représentation de ceux-ci sous forme de chaîne, que vous utiliserez pour modifier le dictionnaire.</span><span class="sxs-lookup"><span data-stu-id="6a8ff-119">The keywords themselves are stored in an object on the backend, but  `$dict.KeywordDictionary` contains a string representation of them, which you'll use to modify the dictionary.</span></span> 

<span data-ttu-id="6a8ff-120">Avant de modifier le dictionnaire, vous devez reconvertir la chaîne de termes en un tableau à l’aide de la méthode  `.split(',')`.</span><span class="sxs-lookup"><span data-stu-id="6a8ff-120">Before you modify the dictionary, you need to turn the string of terms back into an array using the  `.split(',')` method.</span></span> <span data-ttu-id="6a8ff-121">Ensuite, vous nettoierez les espaces indésirables entre les mots clés avec la méthode  `.trim()`, en ne laissant que les mots clés que vous souhaitez utiliser.</span><span class="sxs-lookup"><span data-stu-id="6a8ff-121">Then you'll clean up the unwanted spaces between the keywords with the  `.trim()` method, leaving just the keywords to work with.</span></span> 
  
```powershell
$terms = $dict.KeywordDictionary.split(',').trim()
```

<span data-ttu-id="6a8ff-p105">Vous allez maintenant supprimer certains termes du dictionnaire. Étant donné que l’exemple de dictionnaire ne contient que quelques mots clés, vous pourriez simplement passer directement à l’exportation et à la modification du dictionnaire dans le Bloc-notes, mais les dictionnaires contiennent généralement une grande quantité de texte. Vous allez donc d’abord découvrir la méthode qui permet de les modifier facilement dans PowerShell.</span><span class="sxs-lookup"><span data-stu-id="6a8ff-p105">Now you'll remove some terms from the dictionary. Because the example dictionary has only a few keywords, you could as easily skip to exporting the dictionary and editing it in Notepad, but dictionaries generally contain a large amount of text, so you'll first learn this way to edit them easily in PowerShell.</span></span>
  
<span data-ttu-id="6a8ff-p106">Dans la dernière étape, vous avez enregistré les mots clés dans un tableau. Il existe plusieurs façons de [supprimer des éléments dans un tableau](/previous-versions/windows/it-pro/windows-powershell-1.0/ee692802(v=technet.10)), mais une approche simple consiste à créer un tableau des termes à supprimer du dictionnaire et à copier uniquement les termes dans celui-ci de dictionnaire qui ne figurent pas dans la liste des termes à supprimer.</span><span class="sxs-lookup"><span data-stu-id="6a8ff-p106">In the last step, you saved the keywords to an array. There are several ways to [remove items from an array](/previous-versions/windows/it-pro/windows-powershell-1.0/ee692802(v=technet.10)), but as a straightforward approach, you'll create an array of the terms you want to remove from the dictionary, and then copy only the dictionary terms to it that aren't in the list of terms to remove.</span></span>
  
<span data-ttu-id="6a8ff-p107">Exécutez la commande `$terms` pour afficher la liste actuelle des termes. La sortie de la commande se présente comme suit :</span><span class="sxs-lookup"><span data-stu-id="6a8ff-p107">Run the command  `$terms` to show the current list of terms. The output of the command looks like this:</span></span> 
  
`aarskog's syndrome`
`abandonment`
`abasia`
`abderhalden-kaufmann-lignac`
`abdominalgia`
`abduction contracture`
`abetalipoproteinemia`
`abiotrophy`
`ablatio`
`ablation`
`ablepharia`
`abocclusion`
`abolition`
`aborter`
`abortion`
`abortus`
`aboulomania`
`abrami's disease`

<span data-ttu-id="6a8ff-128">Exécutez cette commande pour spécifier les termes à supprimer :</span><span class="sxs-lookup"><span data-stu-id="6a8ff-128">Run this command to specify the terms that you want to remove:</span></span>
  
```powershell
$termsToRemove = @('abandonment', 'ablatio')
```

<span data-ttu-id="6a8ff-129">Exécutez cette commande pour supprimer réellement les termes de la liste :</span><span class="sxs-lookup"><span data-stu-id="6a8ff-129">Run this command to actually remove the terms from the list:</span></span>
  
```powershell
$updatedTerms = $terms | Where-Object{ $_ -notin $termsToRemove }
```

<span data-ttu-id="6a8ff-p108">Exécutez la commande `$updatedTerms` pour afficher la liste mise à jour des termes. La sortie de la commande se présente comme suit (les termes spécifiés ont été supprimés) :</span><span class="sxs-lookup"><span data-stu-id="6a8ff-p108">Run the command  `$updatedTerms` to show the updated list of terms. The output of the command looks like this (the specified terms have been removed):</span></span> 
  
`aarskog's syndrome`
`abasia`
`abderhalden-kaufmann-lignac`
`abdominalgia`
`abduction contracture`
`abetalipo proteinemia`
`abiotrophy`
`ablation`
`ablepharia`
`abocclusion`
`abolition`
`aborter`
`abortion`
`abortus`
`aboulomania`
`abrami's disease`
```

Now save the dictionary locally and add a few more terms. You could add the terms right here in PowerShell, but you'll still need to export the file locally to ensure it's saved with Unicode encoding and contains the BOM.
  
Save the dictionary locally by running the following:
  
```powershell
Set-Content $updatedTerms -Path "C:\myPath\terms.txt"
```

<span data-ttu-id="6a8ff-p109">À présent, ouvrez simplement le fichier, ajoutez les autres termes et enregistrez-le avec le codage Unicode (UTF-16). Chargez ensuite les termes mis à jour et mettez à jour le dictionnaire sur place.</span><span class="sxs-lookup"><span data-stu-id="6a8ff-p109">Now open the file, add your other terms, and save with Unicode encoding (UTF-16). Now you'll upload the updated terms and update the dictionary in place.</span></span>
  
```powershell
PS> Set-DlpKeywordDictionary -Identity "Diseases" -FileData (Get-Content -Path "C:myPath\terms.txt" -Encoding Byte -ReadCount 0)
```

<span data-ttu-id="6a8ff-134">Le dictionnaire a maintenant été mis à jour sur place.</span><span class="sxs-lookup"><span data-stu-id="6a8ff-134">Now the dictionary has been updated in place.</span></span> <span data-ttu-id="6a8ff-135">Le champ `Identity` prend le nom du dictionnaire.</span><span class="sxs-lookup"><span data-stu-id="6a8ff-135">The  `Identity` field takes the name of the dictionary.</span></span> <span data-ttu-id="6a8ff-136">Si vous souhaitez également modifier le nom de votre dictionnaire à l’aide de la cmdlet `set-`, vous n’avez qu’à ajouter le paramètre `-Name` à ce qui précède avec le nouveau nom de votre dictionnaire.</span><span class="sxs-lookup"><span data-stu-id="6a8ff-136">If you wanted to also change the name of your dictionary using the  `set-` cmdlet, you would just need to add the  `-Name` parameter to what's above with your new dictionary name.</span></span> 

<span data-ttu-id="6a8ff-137">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6a8ff-137">See Also</span></span>
- [<span data-ttu-id="6a8ff-138">Créer un dictionnaire de mots clés</span><span class="sxs-lookup"><span data-stu-id="6a8ff-138">Create a keyword dictionary</span></span>](create-a-keyword-dictionary.md)
- [<span data-ttu-id="6a8ff-139">Créer un type d’informations sensibles personnalisé</span><span class="sxs-lookup"><span data-stu-id="6a8ff-139">Create a custom sensitive information type</span></span>](create-a-custom-sensitive-information-type.md)
