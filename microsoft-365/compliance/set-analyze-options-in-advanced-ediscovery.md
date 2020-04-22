---
title: Définir les options d’analyse dans Advanced eDiscovery
f1.keywords:
- NOCSH
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
ms.assetid: f6cd6588-f6b6-424a-a9ab-3782b842faee
description: 'Passez en revue les étapes de configuration des options pour le processus d’analyse dans Advanced eDiscovery, y compris les thèmes de quasi-duplication, les threads de messagerie et les thèmes.  '
ms.openlocfilehash: 5f50e2863398679d1381c66009ff1daec40623f9
ms.sourcegitcommit: 2614f8b81b332f8dab461f4f64f3adaa6703e0d6
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/21/2020
ms.locfileid: "43631261"
---
# <a name="set-analyze-options-in-advanced-ediscovery-classic"></a><span data-ttu-id="2a232-103">Définir les options d’analyse dans Advanced eDiscovery (classique)</span><span class="sxs-lookup"><span data-stu-id="2a232-103">Set Analyze options in Advanced eDiscovery (classic)</span></span>

> [!NOTE]
> <span data-ttu-id="2a232-p101">Pour utiliser Advanced eDiscovery, votre organisation doit souscrire un abonnement Office 365 E3 avec le module complémentaire Conformité avancée ou un abonnement E5. Si vous ne disposez pas d’un abonnement et que vous souhaitez essayer Advanced eDiscovery, vous pouvez vous [inscrire pour utiliser une version d’évaluation d’Office 365 Entreprise E5](https://go.microsoft.com/fwlink/p/?LinkID=698279).</span><span class="sxs-lookup"><span data-stu-id="2a232-p101">Advanced eDiscovery requires an Office 365 E3 with the Advanced Compliance add-on or an E5 subscription for your organization. If you don't have that plan and want to try Advanced eDiscovery, you can [sign up for a trial of Office 365 Enterprise E5](https://go.microsoft.com/fwlink/p/?LinkID=698279).</span></span> 
  
<span data-ttu-id="2a232-106">Dans Advanced eDiscovery, définissez les options d’analyse avant d’exécuter Analyze.</span><span class="sxs-lookup"><span data-stu-id="2a232-106">In Advanced eDiscovery, set the Analyze options prior to running Analyze.</span></span>
  
## <a name="set-analyze-options"></a><span data-ttu-id="2a232-107">Définir les options d’analyse</span><span class="sxs-lookup"><span data-stu-id="2a232-107">Set Analyze options</span></span>

<span data-ttu-id="2a232-108">Ouvrez \*\*Prepare prepare prepare \> \*\* \> **Setup**.</span><span class="sxs-lookup"><span data-stu-id="2a232-108">Open **Prepare \> Analyze** \> **Setup**.</span></span> <span data-ttu-id="2a232-109">La fenêtre suivante s’affiche.</span><span class="sxs-lookup"><span data-stu-id="2a232-109">The following window is displayed.</span></span>
  
![Options Définir l’analyse](../media/c3ec7a92-8484-4812-b98c-aa3eb740e5b7.png)
  
 <span data-ttu-id="2a232-111">**Quasi-doublons et threads de messagerie** Activez cette case à cocher si vous souhaitez exécuter l’analyse.</span><span class="sxs-lookup"><span data-stu-id="2a232-111">**Near-duplicates and email threads** Check this box if you want to run the analysis.</span></span> <span data-ttu-id="2a232-112">Elle est sélectionnée par défaut.</span><span class="sxs-lookup"><span data-stu-id="2a232-112">It is selected by default.</span></span> 
  
 <span data-ttu-id="2a232-113">**Similarité des documents** Entrez la valeur de seuil des quasi-doublons ou acceptez la valeur par défaut de 65%.</span><span class="sxs-lookup"><span data-stu-id="2a232-113">**Document similarity** Enter the Near-duplicates threshold value or accept the default of 65%.</span></span> 
  
 <span data-ttu-id="2a232-114">**Thèmes** Activez cette case à cocher pour traiter tous les fichiers et leur affecter des thèmes.</span><span class="sxs-lookup"><span data-stu-id="2a232-114">**Themes**Check this box to process all files and assign themes to them.</span></span> <span data-ttu-id="2a232-115">Par défaut, cette case à cocher n’est pas activée.</span><span class="sxs-lookup"><span data-stu-id="2a232-115">By default, this check box is not selected.</span></span> <span data-ttu-id="2a232-116">Entrez les options suivantes si vous souhaitez effectuer le traitement des thèmes.</span><span class="sxs-lookup"><span data-stu-id="2a232-116">Enter the following options if you want to perform Themes processing.</span></span>
  
- <span data-ttu-id="2a232-117">**Nombre maximal de thèmes** Entrez ou sélectionnez une valeur pour le nombre de thèmes à créer.</span><span class="sxs-lookup"><span data-stu-id="2a232-117">**Max number of themes**Enter or select a value for the number of themes to create.</span></span> <span data-ttu-id="2a232-118">La valeur par défaut est 200.</span><span class="sxs-lookup"><span data-stu-id="2a232-118">The default is 200.</span></span> 
    
    > [!NOTE]
    > <span data-ttu-id="2a232-119">L’augmentation du nombre de thèmes a une incidence sur les performances, ainsi que sur la capacité d’un thème à généraliser.</span><span class="sxs-lookup"><span data-stu-id="2a232-119">Increasing the number of themes affects performance, as well as the ability of a theme to generalize.</span></span> <span data-ttu-id="2a232-120">Plus le nombre de thèmes est élevé, plus il est granulaire.</span><span class="sxs-lookup"><span data-stu-id="2a232-120">The higher the number of themes, the more granular they are.</span></span> <span data-ttu-id="2a232-121">Par exemple, si un jeu de thèmes 50 inclut un thème tel que « basket-ball, Spurs, détoureurs, Lakers »; 300 les thèmes peuvent inclure des thèmes distincts : « Spurs », « Clipper », « Lakers ».</span><span class="sxs-lookup"><span data-stu-id="2a232-121">For example, if a set of 50 themes include a theme such as "Basketball, Spurs, Clippers, Lakers"; 300 themes may include separate themes: "Spurs", "Clippers", "Lakers".</span></span> <span data-ttu-id="2a232-122">Si vous n’avez pas conscience du thème « basket » et si vous utilisez cette fonctionnalité pour ECA, voir le thème « basket » peut être utile.</span><span class="sxs-lookup"><span data-stu-id="2a232-122">If you had no awareness of the theme "Basketball" and use this feature for ECA, seeing the theme "Basketball" could be useful.</span></span> <span data-ttu-id="2a232-123">Toutefois, si le traitement avait trop de thèmes, il se peut que vous ne trouviez jamais le mot « basket-ball » et que des Spurs et des découpages soient des thèmes de basket-ball intéressants à consulter, plutôt que des éléments qui se trouvent sur les bottes et utilisés pour les cheveux.</span><span class="sxs-lookup"><span data-stu-id="2a232-123">But, if the processing had too many themes, you may never see the word "Basketball" and may not know that Spurs and Clippers are good Basketball themes to review, rather than items that go on boots and used for hair.</span></span> 
  
- <span data-ttu-id="2a232-124">**Thèmes suggérés** Vous pouvez suggérer des mots de thème pour contrôler le traitement des thèmes.</span><span class="sxs-lookup"><span data-stu-id="2a232-124">**Suggested themes** You can suggest theme words to control Themes processing.</span></span> <span data-ttu-id="2a232-125">Advanced eDiscovery se concentrera sur ces suggestions de mots et tentera de créer un ou plusieurs thèmes pertinents, en fonction des paramètres « nombre maximal de thèmes ».</span><span class="sxs-lookup"><span data-stu-id="2a232-125">Advanced eDiscovery will focus on these suggested words and try to create one or more relevant themes, based on the "Max number of themes" settings.</span></span> 
    
    <span data-ttu-id="2a232-126">Par exemple, si le mot suggéré est « ordinateur » et que vous avez spécifié « 2 » comme « nombre maximal de thèmes », Advanced eDiscovery essaiera de générer deux thèmes liés au mot « ordinateur ».</span><span class="sxs-lookup"><span data-stu-id="2a232-126">For example, if the suggested word is "computer", and you specified "2" as the "Max number of Themes", Advanced eDiscovery will try to generate two themes that relate to the word "computer".</span></span> <span data-ttu-id="2a232-127">Les deux thèmes peuvent être « logiciels informatiques » et « matériel informatique », par exemple.</span><span class="sxs-lookup"><span data-stu-id="2a232-127">The two themes might be "computer software" and "computer hardware", for example.</span></span> 
    
    ![Ajouter une suggestion de thème](../media/06e9ffd3-a76c-423b-b450-9e465eb9a02f.png)
  
1. <span data-ttu-id="2a232-129">Pour afficher, ajouter ou modifier des thèmes suggérés, cliquez sur **modifier**.</span><span class="sxs-lookup"><span data-stu-id="2a232-129">To view, add, or edit suggested themes, click **Modify**.</span></span>
    
2. <span data-ttu-id="2a232-130">Dans le **panneau thèmes suggérés** , cliquez sur l’icône](../media/c2dd8b3a-5a22-412c-a7fa-143f5b2b5612.png) **Ajouter** ![une icône Ajouter pour ajouter un thème.</span><span class="sxs-lookup"><span data-stu-id="2a232-130">In the **Suggested themes** panel, click the **Add** ![add icon](../media/c2dd8b3a-5a22-412c-a7fa-143f5b2b5612.png) icon to add a theme.</span></span> <span data-ttu-id="2a232-131">Dans le panneau **Ajouter un thème suggéré** , ajoutez les mots, séparés par des virgules.</span><span class="sxs-lookup"><span data-stu-id="2a232-131">In the **Add suggested theme** panel, add the words, separated by commas.</span></span> 
    
3. <span data-ttu-id="2a232-132">Dans **nombre de thèmes**, sélectionnez une valeur pour déterminer le nombre de thèmes que la fonctionnalité eDiscovery avancée essaiera de générer pour ces mots (la valeur par défaut est 1 thème).</span><span class="sxs-lookup"><span data-stu-id="2a232-132">In **Number of themes**, select a value to determine the number of themes Advanced eDiscovery will try to generate for these words (default is 1 theme).</span></span>
    
4. <span data-ttu-id="2a232-133">Cliquez sur **Enregistrer** , puis fermez la boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="2a232-133">Click **Save** and then close the dialogue.</span></span> 
    
    > [!NOTE]
    > <span data-ttu-id="2a232-134">Le nombre total de thèmes inclut les thèmes suggérés.</span><span class="sxs-lookup"><span data-stu-id="2a232-134">The total number of themes includes Suggested Themes.</span></span> <span data-ttu-id="2a232-135">Le total des thèmes suggérés ne peut pas dépasser le nombre total de thèmes.</span><span class="sxs-lookup"><span data-stu-id="2a232-135">The total Suggested Themes cannot exceed the total themes.</span></span> <span data-ttu-id="2a232-136">S’il existe de nombreux thèmes suggérés par rapport au nombre total de thèmes, seuls quelques « nouveaux » thèmes seront détectés par le système, car la plupart des thèmes seront dédiés aux thèmes suggérés.</span><span class="sxs-lookup"><span data-stu-id="2a232-136">If there are many Suggested Themes relative to the total themes, only a few "novel" themes will be detected by the system because most of the themes will be dedicated to Suggested Themes.</span></span> 
  
- <span data-ttu-id="2a232-137">**Mode** Dans la liste déroulante, sélectionnez une option de **thèmes** :</span><span class="sxs-lookup"><span data-stu-id="2a232-137">**Mode** From the drop-down list, select a **Themes** option:</span></span> 
    
  - <span data-ttu-id="2a232-138">**Créer et appliquer un modèle**: calcule les thèmes par modèles à partir d’un segment des fichiers, puis distribue les fichiers entre eux.</span><span class="sxs-lookup"><span data-stu-id="2a232-138">**Create and apply model**: Calculates themes by models from a segment of the files and then distributes files among them.</span></span>
    
  - <span data-ttu-id="2a232-139">**Créer un modèle**: calcule un modèle de thèmes à partir d’un segment des fichiers.</span><span class="sxs-lookup"><span data-stu-id="2a232-139">**Create model**: Calculates a themes model from a segment of the files.</span></span> <span data-ttu-id="2a232-140">Le processus d’application de la Division des fichiers est réalisé séparément à un autre moment.</span><span class="sxs-lookup"><span data-stu-id="2a232-140">The Apply process of dividing files is done separately at another time.</span></span>
    
  - <span data-ttu-id="2a232-141">**Appliquer le modèle**: cette option n’est visible que si un modèle a été créé précédemment et n’a pas encore été appliqué.</span><span class="sxs-lookup"><span data-stu-id="2a232-141">**Apply model**: This option is only shown if a model was created previously and not yet applied.</span></span> <span data-ttu-id="2a232-142">Cela permet de diviser les fichiers en fonction des thèmes.</span><span class="sxs-lookup"><span data-stu-id="2a232-142">This will divide the files based on the themes.</span></span>
    
<span data-ttu-id="2a232-143">Vous pouvez également [définir ignorer le texte](set-ignore-text-in-advanced-ediscovery.md) et [définir les paramètres avancés](set-analyze-advanced-settings-in-advanced-ediscovery.md) d’analyse pour l’analyse.</span><span class="sxs-lookup"><span data-stu-id="2a232-143">You can also [set ignore text](set-ignore-text-in-advanced-ediscovery.md) and [set Analyze advanced settings](set-analyze-advanced-settings-in-advanced-ediscovery.md) for Analyze.</span></span> 
  
<span data-ttu-id="2a232-144">Après avoir défini ces options, cliquez sur **analyser** pour exécuter.</span><span class="sxs-lookup"><span data-stu-id="2a232-144">After you've set these options, click **Analyze** to run.</span></span> <span data-ttu-id="2a232-145">[Afficher les résultats](view-analyze-results-in-advanced-ediscovery.md) de l’analyse sont affichés.</span><span class="sxs-lookup"><span data-stu-id="2a232-145">[View Analyze results](view-analyze-results-in-advanced-ediscovery.md) are displayed.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="2a232-146">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2a232-146">See also</span></span>

[<span data-ttu-id="2a232-147">Advanced eDiscovery (classique)</span><span class="sxs-lookup"><span data-stu-id="2a232-147">Advanced eDiscovery (classic)</span></span>](office-365-advanced-ediscovery.md)
  
[<span data-ttu-id="2a232-148">Présentation de la similarité des documents</span><span class="sxs-lookup"><span data-stu-id="2a232-148">Understanding document similarity</span></span>](understand-document-similarity-in-advanced-ediscovery.md)
  
[<span data-ttu-id="2a232-149">Définir le texte ignoré</span><span class="sxs-lookup"><span data-stu-id="2a232-149">Set Ignore text </span></span>](set-ignore-text-in-advanced-ediscovery.md)
  
[<span data-ttu-id="2a232-150">Paramètres avancés Définir l’analyse</span><span class="sxs-lookup"><span data-stu-id="2a232-150">Set Analyze advanced settings</span></span>](set-analyze-advanced-settings-in-advanced-ediscovery.md)
  
[<span data-ttu-id="2a232-151">Afficher les résultats de l’analyse</span><span class="sxs-lookup"><span data-stu-id="2a232-151">View Analyze results</span></span>](view-analyze-results-in-advanced-ediscovery.md)

