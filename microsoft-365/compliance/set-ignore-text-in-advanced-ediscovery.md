---
title: Définir l’option ignorer le texte pour l’analyse dans Office 365 Advanced eDiscovery
ms.author: chrfox
author: chrfox
manager: laurawi
titleSuffix: Office 365
ms.date: 9/14/2017
audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MOE150
- MET150
ms.assetid: 44055727-56e8-42d7-9dc3-fb942f3901cc
description: 'Découvrez comment définir la règle pour ignorer le texte spécifique lors de l’utilisation des modules Analyze et process dans Office 365 Advanced eDiscovery.  '
ms.openlocfilehash: cb010c1929241720a69bdc906eda4788786adda2
ms.sourcegitcommit: 0ad0092d9c5cb2d69fc70c990a9b7cc03140611b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/19/2019
ms.locfileid: "40802717"
---
# <a name="set-ignore-text-option-for-analyze-in-office-365-advanced-ediscovery"></a><span data-ttu-id="5cffd-103">Définir l’option ignorer le texte pour l’analyse dans Office 365 Advanced eDiscovery</span><span class="sxs-lookup"><span data-stu-id="5cffd-103">Set Ignore Text option for Analyze in Office 365 Advanced eDiscovery</span></span>

> [!NOTE]
> <span data-ttu-id="5cffd-p101">Pour utiliser Advanced eDiscovery, votre organisation doit souscrire un abonnement Office 365 E3 avec le module complémentaire Conformité avancée ou un abonnement E5. Si vous ne disposez pas d’un abonnement et que vous souhaitez essayer Advanced eDiscovery, vous pouvez vous [inscrire pour utiliser une version d’évaluation d’Office 365 Entreprise E5](https://go.microsoft.com/fwlink/p/?LinkID=698279).</span><span class="sxs-lookup"><span data-stu-id="5cffd-p101">Advanced eDiscovery requires an Office 365 E3 with the Advanced Compliance add-on or an E5 subscription for your organization. If you don't have that plan and want to try Advanced eDiscovery, you can [sign up for a trial of Office 365 Enterprise E5](https://go.microsoft.com/fwlink/p/?LinkID=698279).</span></span> 
  
<span data-ttu-id="5cffd-106">La fonctionnalité ignorer le texte peut être appliquée à tout ou partie des modules avancés eDiscovery suivants : Analyze (Near-Duplicates, threads de messagerie, thèmes) et pertinence.</span><span class="sxs-lookup"><span data-stu-id="5cffd-106">The Ignore Text feature can be applied to all or any of the following Advanced eDiscovery modules: Analyze (Near-duplicates, Email Threads, Themes) and Relevance.</span></span> <span data-ttu-id="5cffd-107">Le texte ignoré n’apparaît pas dans les fichiers affichés par pertinence, et l’analyse/les calculs ignorent le texte ignoré.</span><span class="sxs-lookup"><span data-stu-id="5cffd-107">Ignored text will not appear in files displayed in Relevance, and the analysis/calculations will discard the ignored text.</span></span>
  
<span data-ttu-id="5cffd-108">Si la fonctionnalité ignorer le texte a été précédemment définie pour les modules qui ont déjà été exécutés, le paramètre ignorer le texte est maintenant protégé de la modification.</span><span class="sxs-lookup"><span data-stu-id="5cffd-108">If the Ignore Text feature was previously defined for modules that have already run, the Ignore Text setting will now be protected from being modified.</span></span> <span data-ttu-id="5cffd-109">Toutefois, la fonctionnalité ignorer le texte pour le module de pertinence peut toujours être modifiée à tout moment.</span><span class="sxs-lookup"><span data-stu-id="5cffd-109">However, the Ignore Text feature for the Relevance module can still be changed at any time.</span></span>
  
## <a name="how-ignore-text-filters-are-applied"></a><span data-ttu-id="5cffd-110">Procédure d’application des filtres de texte</span><span class="sxs-lookup"><span data-stu-id="5cffd-110">How Ignore Text filters are applied</span></span>

<span data-ttu-id="5cffd-111">Les filtres de texte ignoré multiples sont appliqués dans l’ordre dans lequel ils ont été entrés.</span><span class="sxs-lookup"><span data-stu-id="5cffd-111">Multiple Ignore Text filters are applied in the order that they were entered.</span></span> <span data-ttu-id="5cffd-112">Pour modifier l’ordre dans lequel ils sont appliqués, vous devez les supprimer et les saisir à nouveau dans l’ordre souhaité.</span><span class="sxs-lookup"><span data-stu-id="5cffd-112">To change the order in which they are applied, they must be deleted and re-entered in the desired order.</span></span>
  
<span data-ttu-id="5cffd-113">Par exemple, si le contenu de texte est : « DAVE BOB ALICE CAROL veille », Voici des exemples d’entrées de texte ignorées et des résultats :</span><span class="sxs-lookup"><span data-stu-id="5cffd-113">For example, if the text content is: "DAVE BOB ALICE CAROL EVE", the following are samples of Ignore Text entries and the results:</span></span>
  
||||
|:-----|:-----|:-----|
|<span data-ttu-id="5cffd-114">**Ignorer les entrées de texte**</span><span class="sxs-lookup"><span data-stu-id="5cffd-114">**Ignore Text entries**</span></span> <br/> |**==\>** <br/> |<span data-ttu-id="5cffd-115">**Results**</span><span class="sxs-lookup"><span data-stu-id="5cffd-115">**Results**</span></span> <br/> |
|<span data-ttu-id="5cffd-116">« ALICE », « BOB CAROL »</span><span class="sxs-lookup"><span data-stu-id="5cffd-116">"ALICE", "BOB CAROL"</span></span>  <br/> |==\>  <br/> |<span data-ttu-id="5cffd-117">« DAVID RÉVEILLON »</span><span class="sxs-lookup"><span data-stu-id="5cffd-117">"DAVE EVE"</span></span>  <br/> |
|<span data-ttu-id="5cffd-118">« ALICE », « BOB ALICE CAROL »</span><span class="sxs-lookup"><span data-stu-id="5cffd-118">"ALICE", "BOB ALICE CAROL"</span></span>  <br/> |==\>  <br/> |<span data-ttu-id="5cffd-119">« DAVE BOB CAROL VEILLE »</span><span class="sxs-lookup"><span data-stu-id="5cffd-119">"DAVE BOB CAROL EVE"</span></span>  <br/> |
   
<span data-ttu-id="5cffd-120">La seconde entrée de texte ignorer n’est pas implémentée car la chaîne est introuvable comme telle après l’application du premier texte d’ignorer.</span><span class="sxs-lookup"><span data-stu-id="5cffd-120">The second Ignore Text entry is not implemented because the string is not found as such AFTER the first Ignore Text has been applied.</span></span>
  
## <a name="use-regular-expressions-when-defining-ignore-text"></a><span data-ttu-id="5cffd-121">Utiliser des expressions régulières lors de la définition d’un texte ignoré</span><span class="sxs-lookup"><span data-stu-id="5cffd-121">Use regular expressions when defining Ignore Text</span></span>

<span data-ttu-id="5cffd-122">Les expressions régulières sont prises en charge pour une utilisation lors de la définition d’un texte ignoré.</span><span class="sxs-lookup"><span data-stu-id="5cffd-122">Regular expressions are supported for use when defining Ignore Text.</span></span> <span data-ttu-id="5cffd-123">Voici des exemples de syntaxe et d’utilisation des expressions régulières :</span><span class="sxs-lookup"><span data-stu-id="5cffd-123">The following are examples of regular expression syntax and usage:</span></span>
  
- <span data-ttu-id="5cffd-124">Pour supprimer (ignorer) le texte début jusqu’à la fin d’une ligne :</span><span class="sxs-lookup"><span data-stu-id="5cffd-124">To remove (ignore) text from Begin until the end of a line:</span></span>
    
     `Begin(.*)$`
    
    <span data-ttu-id="5cffd-125">où « Begin » est l’occurrence initiale de cette chaîne dans la ligne.</span><span class="sxs-lookup"><span data-stu-id="5cffd-125">where "Begin" is the initial occurrence of this string in the line.</span></span>
    
    <span data-ttu-id="5cffd-126">Par exemple, pour le texte suivant :</span><span class="sxs-lookup"><span data-stu-id="5cffd-126">For example, for the following text:</span></span>
    
    <span data-ttu-id="5cffd-127">**«Il s’agit de la première phrase et de la première ligne**</span><span class="sxs-lookup"><span data-stu-id="5cffd-127">**"This is first sentence and first line**</span></span>
    
    <span data-ttu-id="5cffd-128">**Il s’agit de la deuxième phrase et de la deuxième ligne»**</span><span class="sxs-lookup"><span data-stu-id="5cffd-128">**This is second sentence and second line"**</span></span>
    
    <span data-ttu-id="5cffd-129">première expression régulière (.\*) $ entraînera :</span><span class="sxs-lookup"><span data-stu-id="5cffd-129">the Regular Expression first(.\*)$ will result in:</span></span>
    
    <span data-ttu-id="5cffd-130">**"Ceci est**</span><span class="sxs-lookup"><span data-stu-id="5cffd-130">**"This is**</span></span>
    
    <span data-ttu-id="5cffd-131">**Il s’agit de la deuxième phrase et de la deuxième ligne»**</span><span class="sxs-lookup"><span data-stu-id="5cffd-131">**This is second sentence and second line"**</span></span>
    
- <span data-ttu-id="5cffd-132">Pour supprimer les clauses d’exclusion de responsabilité et les instructions légales insérées automatiquement à la fin des threads de messagerie :</span><span class="sxs-lookup"><span data-stu-id="5cffd-132">To remove disclaimers and legal statements automatically inserted at the end of email threads:</span></span>
    
     `Begin(.|\s)*End`
    
    <span data-ttu-id="5cffd-133">où « Begin » et « end » sont des chaînes uniques au début et à la fin d’un paragraphe de texte renvoyé à la page.</span><span class="sxs-lookup"><span data-stu-id="5cffd-133">where "Begin" and "End" are unique strings at the beginning and end of a wrapped text paragraph.</span></span> 
    
    <span data-ttu-id="5cffd-134">Par exemple, l’expression régulière suivante supprime les clauses d’exclusion de responsabilité et les instructions légales qui se trouvaient dans le fil de messagerie entre les chaînes de début et de fin :</span><span class="sxs-lookup"><span data-stu-id="5cffd-134">For example, the following regular expression will remove disclaimers and legal statements that were in the email thread between the Begin and End strings:</span></span>
    
    <span data-ttu-id="5cffd-135">**Ce message contient des informations confidentielles (. | \s)\*si la vérification est requise, demandez une version de copie papier.**</span><span class="sxs-lookup"><span data-stu-id="5cffd-135">**This message contains confidential information (.|\s)\*If verification is required please request a hard-copy version**</span></span>
    
- <span data-ttu-id="5cffd-136">Pour supprimer une clause d’exclusion de responsabilité (y compris des caractères spéciaux) :</span><span class="sxs-lookup"><span data-stu-id="5cffd-136">To remove a disclaimer (including special characters):</span></span> 
    
    <span data-ttu-id="5cffd-137">Par exemple, pour le texte suivant (avec la clause d’exclusion de responsabilité représentée par x) :</span><span class="sxs-lookup"><span data-stu-id="5cffd-137">For example, for the following text (with the disclaimer represented here by x's):</span></span> 
    
    <span data-ttu-id="5cffd-138">**/\*\ Ce message contient des informations confidentielles. xxxx xxxx**</span><span class="sxs-lookup"><span data-stu-id="5cffd-138">**/\*\ This message contains confidential information. xxxx xxxx**</span></span>
    
    <span data-ttu-id="5cffd-139">**xxxx xxxx xxxx xxxx xxxx xxxx xxxx**</span><span class="sxs-lookup"><span data-stu-id="5cffd-139">**xxxx xxxx xxxx xxxx xxxx xxxx xxxx**</span></span>
    
    <span data-ttu-id="5cffd-140">\**xxxx xxxx si la vérification est requise, demandez une version en copie papier. /\*\**</span><span class="sxs-lookup"><span data-stu-id="5cffd-140">\**xxxx xxxx If verification is required, please request a hard-copy version. /\*\**</span></span>
    
    <span data-ttu-id="5cffd-141">l’expression régulière permettant de supprimer la clause d’exclusion de responsabilité ci-dessus doit être :</span><span class="sxs-lookup"><span data-stu-id="5cffd-141">the regular expression to remove the above disclaimer should be:</span></span> 
    
    <span data-ttu-id="5cffd-142">**\/\\*\\Ce message contient des informations\.confidentielles (. | \s)\* si la vérification est requise, demandez une version\. de copie papier.\/\\*\\**</span><span class="sxs-lookup"><span data-stu-id="5cffd-142">**\/\\*\\ This message contains confidential information\.(.|\s)\* If verification is required please request a hard-copy version\. \/\\*\\**</span></span>
    
- <span data-ttu-id="5cffd-143">Règles d’expression régulière :</span><span class="sxs-lookup"><span data-stu-id="5cffd-143">Regular expression rules:</span></span>
    
  - <span data-ttu-id="5cffd-144">Tous les caractères qui ne font pas partie de l’alphabet, à l’exception de l’espace (s), « _ » et « - »\", doivent être précédés de «.</span><span class="sxs-lookup"><span data-stu-id="5cffd-144">Any characters that are not part of the alphabet except for space(s), "_" and "-" must be preceded by "\".</span></span>
    
  - <span data-ttu-id="5cffd-145">Le champ eExpression normal peut avoir une longueur illimitée.</span><span class="sxs-lookup"><span data-stu-id="5cffd-145">The regular eExpression field can be unlimited length.</span></span>
    
> [!TIP]
> <span data-ttu-id="5cffd-146">Pour obtenir une explication et la syntaxe détaillée des expressions régulières, voir : [Regular Expression Language-aide-mémoire](https://msdn.microsoft.com/library/az24scfc%28v=vs.110%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="5cffd-146">For an explanation and detailed syntax of regular expressions, see: [Regular Expression Language - Quick Reference](https://msdn.microsoft.com/library/az24scfc%28v=vs.110%29.aspx).</span></span> 
  
## <a name="define-ignore-text-rule"></a><span data-ttu-id="5cffd-147">Définir la règle de texte ignorer</span><span class="sxs-lookup"><span data-stu-id="5cffd-147">Define Ignore Text rule</span></span>

1. <span data-ttu-id="5cffd-148">Dans l' \*\*onglet \> gérer \> \*\* l’analyse et les options, dans la section **Ignorer** le texte **+** , cliquez sur l’icône pour ajouter une règle.</span><span class="sxs-lookup"><span data-stu-id="5cffd-148">In the **Manage \> Analyze \> Analyze options** tab, in the **Ignore Text** section, click the **+** icon to add a rule.</span></span> 
    
2. <span data-ttu-id="5cffd-149">Dans la boîte de dialogue **Ajouter le texte ignorer** , dans le champ **nom** , tapez un nom pour la règle ignorer le texte.</span><span class="sxs-lookup"><span data-stu-id="5cffd-149">In the **Add Ignore Text** dialog, in the **Name** field, type a name for the Ignore Text rule.</span></span> 
    
    ![Ajouter le texte ignoré](media/98e5129b-2667-4692-86fa-2d0117187a7f.png)
  
3. <span data-ttu-id="5cffd-151">Dans la zone de **texte** , tapez le texte à ignorer.</span><span class="sxs-lookup"><span data-stu-id="5cffd-151">In the **Text** box, type the text to be ignored.</span></span> <span data-ttu-id="5cffd-152">Le champ de texte autorise un nombre illimité de caractères.</span><span class="sxs-lookup"><span data-stu-id="5cffd-152">The text field allows an unlimited number of characters.</span></span> 
    
    > [!TIP]
    > <span data-ttu-id="5cffd-153">Comme indiqué dans la fenêtre ci-dessus, cliquez sur **ampoule** pour afficher les instructions de syntaxe courantes pour la règle ignorer le texte.</span><span class="sxs-lookup"><span data-stu-id="5cffd-153">As shown in the window above, click **light bulb** to see common syntax guidelines for the Ignore Text rule.</span></span> 
  
4. <span data-ttu-id="5cffd-154">Activez la case à cocher **respecter la casse** , si vous le souhaitez.</span><span class="sxs-lookup"><span data-stu-id="5cffd-154">Select the **Case sensitive** check box, if desired.</span></span> 
    
5. <span data-ttu-id="5cffd-155">Dans la liste **appliquer à** , sélectionnez les modules avancés eDiscovery dans lesquels appliquer la définition.</span><span class="sxs-lookup"><span data-stu-id="5cffd-155">In the **Apply to** list, select the Advanced eDiscovery modules in which to apply the definition.</span></span> 
    
6. <span data-ttu-id="5cffd-156">Si vous souhaitez une série de tests sur un exemple de texte, tapez exemple de texte dans la zone de texte de **saisie** , puis cliquez sur **test**.</span><span class="sxs-lookup"><span data-stu-id="5cffd-156">If you want a test run on sample text, type sample text in the **Input** text box and click **Test**.</span></span> <span data-ttu-id="5cffd-157">Les résultats s’affichent dans la zone de texte de **sortie** .</span><span class="sxs-lookup"><span data-stu-id="5cffd-157">The results are displayed in the **Output** text box.</span></span> 
    
7. <span data-ttu-id="5cffd-158">Cliquez sur **OK** pour enregistrer la règle ignorer le texte.</span><span class="sxs-lookup"><span data-stu-id="5cffd-158">Click **OK** to save the Ignore Text rule.</span></span> <span data-ttu-id="5cffd-159">La règle de texte ignorer est affichée.</span><span class="sxs-lookup"><span data-stu-id="5cffd-159">The defined Ignore Text rule is displayed.</span></span> 
    
    ![Définir le nom du texte ignoré](media/3a788ac3-4a1c-46c9-89bd-7ff32d68ce23.png)
  
## <a name="see-also"></a><span data-ttu-id="5cffd-161">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5cffd-161">See also</span></span>

[<span data-ttu-id="5cffd-162">Office 365 Advanced eDiscovery</span><span class="sxs-lookup"><span data-stu-id="5cffd-162">Office 365 Advanced eDiscovery</span></span>](office-365-advanced-ediscovery.md)
  
[<span data-ttu-id="5cffd-163">Présentation de la similarité des documents</span><span class="sxs-lookup"><span data-stu-id="5cffd-163">Understanding document similarity</span></span>](understand-document-similarity-in-advanced-ediscovery.md)
  
[<span data-ttu-id="5cffd-164">Définition des options d’analyse</span><span class="sxs-lookup"><span data-stu-id="5cffd-164">Setting Analyze options</span></span>](set-analyze-options-in-advanced-ediscovery.md)
  
[<span data-ttu-id="5cffd-165">Définition des paramètres avancés d’analyse</span><span class="sxs-lookup"><span data-stu-id="5cffd-165">Setting Analyze advanced settings</span></span>](set-analyze-advanced-settings-in-advanced-ediscovery.md)
  
[<span data-ttu-id="5cffd-166">Affichage des résultats de l’analyse</span><span class="sxs-lookup"><span data-stu-id="5cffd-166">Viewing Analyze results</span></span>](view-analyze-results-in-advanced-ediscovery.md)

