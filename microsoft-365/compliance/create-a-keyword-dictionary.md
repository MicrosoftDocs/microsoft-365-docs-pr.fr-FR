---
title: Créer un dictionnaire de mots clés
f1.keywords:
- NOCSH
ms.author: chrfox
author: chrfox
manager: laurawi
audience: Admin
ms.topic: article
ms.service: O365-seccomp
ms.date: ''
localization_priority: Priority
ms.collection:
- M365-security-compliance
search.appverid:
- MOE150
- MET150
ms.custom:
- seo-marvel-apr2020
description: Découvrez les étapes principales de la création d’un dictionnaire de mots clés dans le Centre de sécurité et conformité Office 365.
ms.openlocfilehash: 488e39921f36a6557378a6214269fcb399114972
ms.sourcegitcommit: 7ecd10b302b3b3dfa4ba3be3a6986dd3c189fbff
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/21/2021
ms.locfileid: "49921576"
---
# <a name="create-a-keyword-dictionary"></a><span data-ttu-id="4521c-103">Créer un dictionnaire de mots clés</span><span class="sxs-lookup"><span data-stu-id="4521c-103">Create a keyword dictionary</span></span>

<span data-ttu-id="4521c-104">La protection contre la perte de données (DLP) peut identifier, surveiller et protéger vos éléments sensibles.</span><span class="sxs-lookup"><span data-stu-id="4521c-104">Data loss prevention (DLP) can identify, monitor, and protect your sensitive items.</span></span> <span data-ttu-id="4521c-105">L’identification des éléments sensibles nécessite parfois la recherche de mots clés, en particulier lors de l’identification d’un contenu générique (comme une communication liée à la santé) ou d’un langage inapproprié ou explicite.</span><span class="sxs-lookup"><span data-stu-id="4521c-105">Identifying sensitive items sometimes requires looking for keywords, particularly when identifying generic content (such as healthcare-related communication), or inappropriate or explicit language.</span></span> <span data-ttu-id="4521c-106">Bien que vous puissiez créer des listes de mots clés dans des types d’informations sensibles, ces listes sont de taille limitée et nécessitent la modification du XML pour les créer ou les modifier.</span><span class="sxs-lookup"><span data-stu-id="4521c-106">Although you can create keyword lists in sensitive information types, keyword lists are limited in size and require modifying XML to create or edit them.</span></span> <span data-ttu-id="4521c-107">Les dictionnaires de mots clés facilitent la gestion des mots clés à une échelle beaucoup plus grande, en prenant en charge jusqu’à 1Mo de termes (après la compression) dans le dictionnaire. Et ils prennent en charge toutes les langues.</span><span class="sxs-lookup"><span data-stu-id="4521c-107">Keyword dictionaries provide simpler management of keywords and at a much larger scale, supporting up to 1MB of terms (post compression) in the dictionary and support any language.</span></span> <span data-ttu-id="4521c-108">La limite du client est également de 1Mo après la compression.</span><span class="sxs-lookup"><span data-stu-id="4521c-108">The tenant limit is also 1MB after compression.</span></span> <span data-ttu-id="4521c-109">1Mo de limite après la compression signifie que tous les dictionnaires combinés dans un client peuvent avoir près 1 million de caractères.</span><span class="sxs-lookup"><span data-stu-id="4521c-109">1MB of post compression limit means that all dictionaries combined across a tenant can have close to 1 million character.</span></span>
  
> [!NOTE]
> <span data-ttu-id="4521c-110">Microsoft 365 Information Protection prend désormais en charge, en préversion, les langues de jeu de caractères à double octets pour :</span><span class="sxs-lookup"><span data-stu-id="4521c-110">Microsoft 365 Information Protection now  supports in preview double byte character set languages for:</span></span>
> - <span data-ttu-id="4521c-111">Chinois (simplifié)</span><span class="sxs-lookup"><span data-stu-id="4521c-111">Chinese (simplified)</span></span>
> - <span data-ttu-id="4521c-112">Chinois (traditionnel)</span><span class="sxs-lookup"><span data-stu-id="4521c-112">Chinese (traditional)</span></span>
> - <span data-ttu-id="4521c-113">Korean</span><span class="sxs-lookup"><span data-stu-id="4521c-113">Korean</span></span>
> - <span data-ttu-id="4521c-114">Japanese</span><span class="sxs-lookup"><span data-stu-id="4521c-114">Japanese</span></span>
>
><span data-ttu-id="4521c-115">Cette prise en charge est disponible pour les types d’informations sensibles.</span><span class="sxs-lookup"><span data-stu-id="4521c-115">This support is available for sensitive information types.</span></span> <span data-ttu-id="4521c-116">Si vous souhaitez en savoir plus, consultez l’article [Prise en charge de la protection des informations pour les jeux de caractères à double octets (préversion)](mip-dbcs-relnotes.md).</span><span class="sxs-lookup"><span data-stu-id="4521c-116">See, [Information protection support for double byte character sets release notes (preview)](mip-dbcs-relnotes.md) for more information.</span></span>

## <a name="basic-steps-to-creating-a-keyword-dictionary"></a><span data-ttu-id="4521c-117">Étapes de base de la création d’un dictionnaire de mots clés</span><span class="sxs-lookup"><span data-stu-id="4521c-117">Basic steps to creating a keyword dictionary</span></span>

<span data-ttu-id="4521c-p103">Les mots clés de votre dictionnaire peuvent provenir de diverses sources, le plus souvent d’un fichier (par exemple, une liste .csv ou .txt) importé dans le service ou par cmdlet PowerShell, d’une liste à laquelle vous accédez directement dans la cmdlet PowerShell ou d’un dictionnaire existant. Lorsque vous créez un dictionnaire de mots clés, vous suivez les mêmes étapes fondamentales :</span><span class="sxs-lookup"><span data-stu-id="4521c-p103">The keywords for your dictionary could come from a variety of sources, most commonly from a file (such as a .csv or .txt list) imported in the service or by PowerShell cmdlet, from a list you enter directly in the PowerShell cmdlet, or from an existing dictionary. When you create a keyword dictionary, you follow the same core steps:</span></span>
  
1. <span data-ttu-id="4521c-120">Utilisez le **Centre de sécurité et de conformité** ([https://protection.office.com](https://protection.office.com)) ou connectez-vous au **Centre de sécurité &amp; de conformité PowerShell**.</span><span class="sxs-lookup"><span data-stu-id="4521c-120">Use the **Security & Compliance Center** ([https://protection.office.com](https://protection.office.com)) or connect to  **Security &amp; Compliance Center PowerShell**.</span></span>
    
2. <span data-ttu-id="4521c-121">**Définissez ou chargez vos mots clés à partir de la source souhaitée**.</span><span class="sxs-lookup"><span data-stu-id="4521c-121">**Define or load your keywords from your intended source**.</span></span> <span data-ttu-id="4521c-122">L’Assistant et le cmdlet acceptent une liste de mots clés séparés par des virgules pour la création d’un dictionnaire de mots clés personnalisé. Cette étape varie légèrement en fonction de l’origine de vos mots clés.</span><span class="sxs-lookup"><span data-stu-id="4521c-122">The wizard and the cmdlet both accept a comma-separated list of keywords to create a custom keyword dictionary, so this step will vary slightly depending on where your keywords come from.</span></span> <span data-ttu-id="4521c-123">Une fois chargés, les mots clés sont encodés et convertis en un tableau d’octets avant d’être importés.</span><span class="sxs-lookup"><span data-stu-id="4521c-123">Once loaded, they're encoded and converted to a byte array before they're imported.</span></span>
    
3. <span data-ttu-id="4521c-124">**Créez le dictionnaire**.</span><span class="sxs-lookup"><span data-stu-id="4521c-124">**Create your dictionary**.</span></span> <span data-ttu-id="4521c-125">Choisissez un nom et une description, puis créez votre dictionnaire.</span><span class="sxs-lookup"><span data-stu-id="4521c-125">Choose a name and description and create your dictionary.</span></span>

## <a name="create-a-keyword-dictionary-using-the-security--compliance-center"></a><span data-ttu-id="4521c-126">Créer un dictionnaire de mots clés avec le Centre de sécurité et de conformité</span><span class="sxs-lookup"><span data-stu-id="4521c-126">Create a keyword dictionary using the Security & Compliance Center</span></span>

<span data-ttu-id="4521c-127">Procédez comme suit pour créer et importer des mots clés pour un dictionnaire personnalisé :</span><span class="sxs-lookup"><span data-stu-id="4521c-127">Use the following steps to create and import keywords for a custom dictionary:</span></span>

1. <span data-ttu-id="4521c-128">Connectez-vous au Centre de sécurité et de conformité([https://protection.office.com](https://protection.office.com)).</span><span class="sxs-lookup"><span data-stu-id="4521c-128">Connect to the Security & Compliance Center ([https://protection.office.com](https://protection.office.com)).</span></span>

2. <span data-ttu-id="4521c-129">Accédez à **Classifications > Types d’informations sensibles**.</span><span class="sxs-lookup"><span data-stu-id="4521c-129">Navigate to **Classifications > Sensitive info types**.</span></span>

3. <span data-ttu-id="4521c-130">Sélectionnez **Créer** et entrez un **Nom** et une **Description** pour votre type d’informations sensibles, puis sélectionnez **Suivant**</span><span class="sxs-lookup"><span data-stu-id="4521c-130">Select **Create** and enter a **Name** and **Description** for your sensitive info type, then select **Next**</span></span>

4. <span data-ttu-id="4521c-131">Sélectionnez **Ajouter un élément**, puis sélectionnez **Dictionnaire (grands mots clés)** dans la liste déroulante **Détecter le contenu contenant**.</span><span class="sxs-lookup"><span data-stu-id="4521c-131">Select **Add an element**, then select **Dictionary (Large keywords)** in the **Detect content containing** drop-down list.</span></span>

5. <span data-ttu-id="4521c-132">Sélectionnez **Ajouter un dictionnaire**</span><span class="sxs-lookup"><span data-stu-id="4521c-132">Select **Add a dictionary**</span></span>

6. <span data-ttu-id="4521c-133">Sous le Contrôle de recherche, sélectionnez **Vous pouvez créer de nouveaux dictionnaires de mots clés ici**.</span><span class="sxs-lookup"><span data-stu-id="4521c-133">Under the Search control, select **You can create new keyword dictionaries here**.</span></span>

7. <span data-ttu-id="4521c-134">Entrez un **Nom** pour votre dictionnaire personnalisé.</span><span class="sxs-lookup"><span data-stu-id="4521c-134">Enter a **Name** for your custom dictionary.</span></span>

8. <span data-ttu-id="4521c-135">Sélectionnez **Importer**, puis sélectionnez **À partir d’un fichier texte** ou **À partir d’un fichier CSV** selon votre type de fichier de mots clés.</span><span class="sxs-lookup"><span data-stu-id="4521c-135">Select **Import**, and select either **From text** or **From csv** depending on your keyword file type.</span></span>

9. <span data-ttu-id="4521c-136">Dans la boîte de dialogue du fichier, sélectionnez le fichier de mots clés sur votre PC local ou sur votre partage de fichiers réseau, puis sélectionnez **Ouvrir**.</span><span class="sxs-lookup"><span data-stu-id="4521c-136">In the file dialog, select the keyword file from your local PC or network file share, then select **Open**.</span></span>

10. <span data-ttu-id="4521c-137">Sélectionnez **Enregistrer**, puis sélectionnez votre dictionnaire personnalisé dans la liste **Dictionnaires de mots clés**.</span><span class="sxs-lookup"><span data-stu-id="4521c-137">Select **Save**, then select your custom dictionary from the **Keyword dictionaries** list.</span></span>

11. <span data-ttu-id="4521c-138">Sélectionnez **Ajouter**, puis **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="4521c-138">Select **Add**, then select **Next**.</span></span>

12. <span data-ttu-id="4521c-139">Passez en revue et finalisez vos sélections de type d’informations sensibles, puis sélectionnez **Terminer**.</span><span class="sxs-lookup"><span data-stu-id="4521c-139">Review and finalize your sensitive info type selections, then select **Finish**.</span></span>
    
## <a name="create-a-keyword-dictionary-from-a-file-using-powershell"></a><span data-ttu-id="4521c-140">Création d’un dictionnaire de mots clés à partir d’un fichier avec PowerShell</span><span class="sxs-lookup"><span data-stu-id="4521c-140">Create a keyword dictionary from a file using PowerShell</span></span>

<span data-ttu-id="4521c-141">Lorsque vous devez créer un dictionnaire volumineux, c’est souvent pour utiliser les mots clés d’un fichier ou d’une liste exportée à partir d’une autre source.</span><span class="sxs-lookup"><span data-stu-id="4521c-141">Often when you need to create a large dictionary, it's to use keywords from a file or a list exported from some other source.</span></span> <span data-ttu-id="4521c-142">Dans cet exemple, vous allez créer un dictionnaire de mots clés, contenant une liste de langages inappropriés à filtrer dans un courrier électronique externe.</span><span class="sxs-lookup"><span data-stu-id="4521c-142">In this case, you'll create a keyword dictionary containing a list of inappropriate language to screen in external email.</span></span> <span data-ttu-id="4521c-143">Vous devez d’abord [vous connecter au Centre de sécurité &amp; de conformité PowerShell](https://docs.microsoft.com/powershell/exchange/connect-to-scc-powershell).</span><span class="sxs-lookup"><span data-stu-id="4521c-143">You must first [connect to Security &amp; Compliance Center PowerShell](https://docs.microsoft.com/powershell/exchange/connect-to-scc-powershell).</span></span>
  
1. <span data-ttu-id="4521c-144">Copiez les mots clés dans un fichier texte et assurez-vous que chaque mot clé est sur une ligne distincte.</span><span class="sxs-lookup"><span data-stu-id="4521c-144">Copy the keywords into a text file and make sure that each keyword is on a separate line.</span></span>
    
2. <span data-ttu-id="4521c-p107">Enregistrez le fichier texte avec le codage Unicode. Dans le Bloc-notes \> **Enregistrer sous** \> **Codage** \> **Unicode**.</span><span class="sxs-lookup"><span data-stu-id="4521c-p107">Save the text file with Unicode encoding. In Notepad \> **Save As** \> **Encoding** \> **Unicode**.</span></span>
    
3. <span data-ttu-id="4521c-147">Lisez le fichier dans une variable en exécutant la cmdlet suivante :</span><span class="sxs-lookup"><span data-stu-id="4521c-147">Read the file into a variable by running this cmdlet:</span></span>
    
    ```powershell
    $fileData = Get-Content <filename> -Encoding Byte -ReadCount 0
    ```

4. <span data-ttu-id="4521c-148">Créez le dictionnaire en exécutant la cmdlet suivante :</span><span class="sxs-lookup"><span data-stu-id="4521c-148">Create the dictionary by running this cmdlet:</span></span>
    
    ```powershell
    New-DlpKeywordDictionary -Name <name> -Description <description> -FileData $fileData
    ```

## <a name="modifying-an-existing-keyword-dictionary"></a><span data-ttu-id="4521c-149">Modification d’un dictionnaire de mots clés existant</span><span class="sxs-lookup"><span data-stu-id="4521c-149">Modifying an existing keyword dictionary</span></span>

<span data-ttu-id="4521c-150">Vous devrez peut-être modifier des mots clés dans l’un de vos dictionnaires de mots clés ou modifier l’un des dictionnaires intégrés.</span><span class="sxs-lookup"><span data-stu-id="4521c-150">You might need to modify keywords in one of your keyword dictionaries, or modify one of the built-in dictionaries.</span></span> <span data-ttu-id="4521c-151">Pour l’instant, vous ne pouvez mettre à jour qu’un dictionnaire de mots clés personnalisé avec PowerShell.</span><span class="sxs-lookup"><span data-stu-id="4521c-151">Currently, your can only update a custom keyword dictionary using PowerShell.</span></span> 

<span data-ttu-id="4521c-152">Par exemple, nous allons modifier certains termes dans PowerShell, les enregistrer localement pour qu’ils puissent être modifiés dans un éditeur, puis mettre à jour les termes précédemment intégrés.</span><span class="sxs-lookup"><span data-stu-id="4521c-152">For example, we'll modify some terms in PowerShell, save the terms locally where you can modify them in an editor, and then update the previous terms in place.</span></span> 

<span data-ttu-id="4521c-153">Tout d’abord, récupérez l’objet dictionnaire :</span><span class="sxs-lookup"><span data-stu-id="4521c-153">First, retrieve the dictionary object:</span></span>
  
```powershell
$dict = Get-DlpKeywordDictionary -Name "Diseases"
```

<span data-ttu-id="4521c-154">L’impression  `$dict` affichera les différentes variables.</span><span class="sxs-lookup"><span data-stu-id="4521c-154">Printing  `$dict` will show the various variables.</span></span> <span data-ttu-id="4521c-155">Les mots clés eux-mêmes sont stockés dans un objet sur le serveur principal, mais  `$dict.KeywordDictionary` contient une représentation de ceux-ci sous forme de chaîne, que vous utiliserez pour modifier le dictionnaire.</span><span class="sxs-lookup"><span data-stu-id="4521c-155">The keywords themselves are stored in an object on the backend, but  `$dict.KeywordDictionary` contains a string representation of them, which you'll use to modify the dictionary.</span></span> 

<span data-ttu-id="4521c-156">Avant de modifier le dictionnaire, vous devez reconvertir la chaîne de termes en un tableau à l’aide de la méthode  `.split(',')`.</span><span class="sxs-lookup"><span data-stu-id="4521c-156">Before you modify the dictionary, you need to turn the string of terms back into an array using the  `.split(',')` method.</span></span> <span data-ttu-id="4521c-157">Ensuite, vous nettoierez les espaces indésirables entre les mots clés avec la méthode  `.trim()`, en ne laissant que les mots clés que vous souhaitez utiliser.</span><span class="sxs-lookup"><span data-stu-id="4521c-157">Then you'll clean up the unwanted spaces between the keywords with the  `.trim()` method, leaving just the keywords to work with.</span></span> 
  
```powershell
$terms = $dict.KeywordDictionary.split(',').trim()
```

<span data-ttu-id="4521c-p111">Vous allez maintenant supprimer certains termes du dictionnaire. Étant donné que l’exemple de dictionnaire ne contient que quelques mots clés, vous pourriez simplement passer directement à l’exportation et à la modification du dictionnaire dans le Bloc-notes, mais les dictionnaires contiennent généralement une grande quantité de texte. Vous allez donc découvrir d’abord cette méthode pour les modifier facilement dans PowerShell.</span><span class="sxs-lookup"><span data-stu-id="4521c-p111">Now you'll remove some terms from the dictionary. Because the example dictionary has only a few keywords, you could just as easily skip to exporting the dictionary and editing it in Notepad, but dictionaries generally contain a large amount of text, so you'll first learn this way to edit them easily in PowerShell.</span></span>
  
<span data-ttu-id="4521c-p112">Dans la dernière étape, vous avez enregistré les mots clés dans un tableau. Il existe plusieurs façons de [supprimer des éléments dans un tableau](https://docs.microsoft.com/previous-versions/windows/it-pro/windows-powershell-1.0/ee692802(v=technet.10)), mais une approche simple consiste à créer un tableau des termes à supprimer du dictionnaire et à copier uniquement les termes dans celui-ci de dictionnaire qui ne figurent pas dans la liste des termes à supprimer.</span><span class="sxs-lookup"><span data-stu-id="4521c-p112">In the last step, you saved the keywords to an array. There are several ways to [remove items from an array](https://docs.microsoft.com/previous-versions/windows/it-pro/windows-powershell-1.0/ee692802(v=technet.10)), but as a straightforward approach, you'll create an array of the terms you want to remove from the dictionary, and then copy only the dictionary terms to it that aren't in the list of terms to remove.</span></span>
  
<span data-ttu-id="4521c-p113">Exécutez la commande `$terms` pour afficher la liste actuelle des termes. La sortie de la commande se présente comme suit :</span><span class="sxs-lookup"><span data-stu-id="4521c-p113">Run the command  `$terms` to show the current list of terms. The output of the command looks like this:</span></span> 
  
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

<span data-ttu-id="4521c-164">Exécutez cette commande pour spécifier les termes à supprimer :</span><span class="sxs-lookup"><span data-stu-id="4521c-164">Run this command to specify the terms that you want to remove:</span></span>
  
```powershell
$termsToRemove = @('abandonment', 'ablatio')
```

<span data-ttu-id="4521c-165">Exécutez cette commande pour supprimer réellement les termes de la liste :</span><span class="sxs-lookup"><span data-stu-id="4521c-165">Run this command to actually remove the terms from the list:</span></span>
  
```powershell
$updatedTerms = $terms | Where-Object{ $_ -notin $termsToRemove }
```

<span data-ttu-id="4521c-p114">Exécutez la commande `$updatedTerms` pour afficher la liste mise à jour des termes. La sortie de la commande se présente comme suit (les termes spécifiés ont été supprimés) :</span><span class="sxs-lookup"><span data-stu-id="4521c-p114">Run the command  `$updatedTerms` to show the updated list of terms. The output of the command looks like this (the specified terms have been removed):</span></span> 
  
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

<span data-ttu-id="4521c-p115">À présent, ouvrez simplement le fichier, ajoutez les termes supplémentaires et enregistrez-le avec le codage Unicode (UTF-16). Chargez ensuite les termes mis à jour et mettez à jour le dictionnaire en place.</span><span class="sxs-lookup"><span data-stu-id="4521c-p115">Now simply open the file, add your additional terms, and save with Unicode encoding (UTF-16). Now you'll upload the updated terms and update the dictionary in place.</span></span>
  
```powershell
PS> Set-DlpKeywordDictionary -Identity "Diseases" -FileData (Get-Content -Path "C:myPath\terms.txt" -Encoding Byte -ReadCount 0)
```

<span data-ttu-id="4521c-p116">Le dictionnaire a été mis à jour. Notez que le champ `Identity` prend le nom du dictionnaire. Si vous vouliez également modifier le nom de votre dictionnaire à l’aide la cmdlet `set-`, vous n’aviez qu’à ajouter le paramètre `-Name` au-dessus avec le nouveau nom de votre dictionnaire.</span><span class="sxs-lookup"><span data-stu-id="4521c-p116">Now the dictionary has been updated in place. Note that the  `Identity` field takes the name of the dictionary. If you wanted to also change the name of your dictionary using the  `set-` cmdlet, you would just need to add the  `-Name` parameter to what's above with your new dictionary name.</span></span> 
  
## <a name="using-keyword-dictionaries-in-custom-sensitive-information-types-and-dlp-policies"></a><span data-ttu-id="4521c-173">Utilisation des dictionnaires de mots clés dans les types d’informations sensibles personnalisés et les stratégies DLP</span><span class="sxs-lookup"><span data-stu-id="4521c-173">Using keyword dictionaries in custom sensitive information types and DLP policies</span></span>

<span data-ttu-id="4521c-174">Les dictionnaires de mots clés peuvent être utilisés dans le cadre des exigences de correspondance pour un type d’information sensible personnalisé ou comme type d’information sensible eux-mêmes.</span><span class="sxs-lookup"><span data-stu-id="4521c-174">Keyword dictionaries can be used as part of the match requirements for a custom sensitive information type, or as a sensitive information type themselves.</span></span> <span data-ttu-id="4521c-175">Dans les deux cas, la création d’un [type d’informations sensibles personnalisé](create-a-custom-sensitive-information-type-in-scc-powershell.md) est requise.</span><span class="sxs-lookup"><span data-stu-id="4521c-175">Both require you to create a [custom sensitive information type](create-a-custom-sensitive-information-type-in-scc-powershell.md).</span></span> <span data-ttu-id="4521c-176">Suivez les instructions de l’article lié pour créer un type d’informations sensibles.</span><span class="sxs-lookup"><span data-stu-id="4521c-176">Follow the instructions in the linked article to create a sensitive information type.</span></span> <span data-ttu-id="4521c-177">Une fois que vous avez le XML, vous aurez besoin de l’identificateur GUID que le dictionnaire utilise.</span><span class="sxs-lookup"><span data-stu-id="4521c-177">Once you have the XML, you'll need the GUID identifier for the dictionary to use it.</span></span>
  
```xml
<Entity id="9e5382d0-1b6a-42fd-820e-44e0d3b15b6e" patternsProximity="300" recommendedConfidence="75">
    <Pattern confidenceLevel="75">
        <IdMatch idRef=". . ."/>
    </Pattern>
</Entity>
```

<span data-ttu-id="4521c-178">Pour obtenir l’identité de votre dictionnaire, exécutez la commande suivante et copiez la valeur de la propriété **Identité** :</span><span class="sxs-lookup"><span data-stu-id="4521c-178">To get the identity of your dictionary, run this command and copy the **Identity** property value:</span></span> 
  
```powershell
Get-DlpKeywordDictionary -Name "Diseases"
```

<span data-ttu-id="4521c-179">Le résultat de la commande ressemble à ceci :</span><span class="sxs-lookup"><span data-stu-id="4521c-179">The output of the command looks like this:</span></span>
  
<span data-ttu-id="4521c-180">`RunspaceId        : 138e55e7-ea1e-4f7a-b824-79f2c4252255`
`Identity          : 8d2d44b0-91f4-41f2-94e0-21c1c5b5fc9f`
`Name              : Diseases`
`Description       : Names of diseases and injuries from ICD-10-CM lexicon`
`KeywordDictionary : aarskog's syndrome, abandonment, abasia, abderhalden-kaufmann-lignac, abdominalgia, abduction contracture, abetalipo` `proteinemia, abiotrophy, ablatio, ablation, ablepharia, abocclusion, abolition, aborter, abortion, abortus, aboulomania,`</span><span class="sxs-lookup"><span data-stu-id="4521c-180">`RunspaceId        : 138e55e7-ea1e-4f7a-b824-79f2c4252255`
`Identity          : 8d2d44b0-91f4-41f2-94e0-21c1c5b5fc9f`
`Name              : Diseases`
`Description       : Names of diseases and injuries from ICD-10-CM lexicon`
`KeywordDictionary : aarskog's syndrome, abandonment, abasia, abderhalden-kaufmann-lignac, abdominalgia, abduction contracture, abetalipo` `proteinemia, abiotrophy, ablatio, ablation, ablepharia, abocclusion, abolition, aborter, abortion, abortus, aboulomania,`</span></span>
                    `abrami's disease, abramo`
`IsValid           : True`
`ObjectState       : Unchanged`


<span data-ttu-id="4521c-p118">Collez l’identité dans le code XML de votre type personnalisé d’informations sensibles et chargez-le. Votre dictionnaire s’affiche désormais dans votre liste de types d’informations sensibles et vous pouvez l’utiliser directement dans votre stratégie en indiquant le nombre de mots clés qui doivent correspondre.</span><span class="sxs-lookup"><span data-stu-id="4521c-p118">Paste the identity into your custom sensitive information type's XML and upload it. Now your dictionary will appear in your list of sensitive information types and you can use it right in your policy, specifying how many keywords are required to match.</span></span>
  
```xml
<Entity id="d333c6c2-5f4c-4131-9433-db3ef72a89e8" patternsProximity="300" recommendedConfidence="85">
      <Pattern confidenceLevel="85">
        <IdMatch idRef="8d2d44b0-91f4-41f2-94e0-21c1c5b5fc9f" />
      </Pattern>
    </Entity>
    <LocalizedStrings>
      <Resource idRef="d333c6c2-5f4c-4131-9433-db3ef72a89e8">
        <Name default="true" langcode="en-us">Diseases</Name>
        <Description default="true" langcode="en-us">Detects various diseases</Description>
      </Resource>
    </LocalizedStrings>
```
