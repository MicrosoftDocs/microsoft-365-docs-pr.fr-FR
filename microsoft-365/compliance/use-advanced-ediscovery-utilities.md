---
title: Utiliser les utilitaires eDiscovery avancés d’Office 365
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
ms.assetid: 66ca9993-75f4-4724-aea2-5a0719b660c1
description: 'Découvrez les utilitaires d’Office 365 Advanced eDiscovery, notamment le journal des cas, les données claires, les erreurs de processus, la pertinence et l’analyse de la transparence.  '
ms.openlocfilehash: fd7ed1afe4b9204665e58b393c79bbb47b7598e3
ms.sourcegitcommit: 0ad0092d9c5cb2d69fc70c990a9b7cc03140611b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/19/2019
ms.locfileid: "40802329"
---
# <a name="use-office-365-advanced-ediscovery-utilities"></a><span data-ttu-id="1d83b-103">Utiliser les utilitaires eDiscovery avancés d’Office 365</span><span class="sxs-lookup"><span data-stu-id="1d83b-103">Use Office 365 Advanced eDiscovery utilities</span></span>

> [!NOTE]
> <span data-ttu-id="1d83b-p101">Pour utiliser Advanced eDiscovery, votre organisation doit souscrire un abonnement Office 365 E3 avec le module complémentaire Conformité avancée ou un abonnement E5. Si vous ne disposez pas d’un abonnement et que vous souhaitez essayer Advanced eDiscovery, vous pouvez vous [inscrire pour utiliser une version d’évaluation d’Office 365 Entreprise E5](https://go.microsoft.com/fwlink/p/?LinkID=698279).</span><span class="sxs-lookup"><span data-stu-id="1d83b-p101">Advanced eDiscovery requires an Office 365 E3 with the Advanced Compliance add-on or an E5 subscription for your organization. If you don't have that plan and want to try Advanced eDiscovery, you can [sign up for a trial of Office 365 Enterprise E5](https://go.microsoft.com/fwlink/p/?LinkID=698279).</span></span> 
  
<span data-ttu-id="1d83b-106">Les utilitaires affichés et disponibles dans Advanced eDiscovery dépendent des rôles de contexte et d’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="1d83b-106">The utilities that are displayed and available in Advanced eDiscovery depend on context and user roles.</span></span>
  
## <a name="case-log"></a><span data-ttu-id="1d83b-107">Journal des cas</span><span class="sxs-lookup"><span data-stu-id="1d83b-107">Case log</span></span>

<span data-ttu-id="1d83b-108">Le journal des cas fournit une liste détaillée des activités de traitement des applications, qui peuvent être utilisées pour le suivi, la résolution des problèmes et la résolution des erreurs et des avertissements.</span><span class="sxs-lookup"><span data-stu-id="1d83b-108">The Case log provides a detailed list of application processing activities, which can be used for tracking, troubleshooting, and for addressing errors and warnings.</span></span> <span data-ttu-id="1d83b-109">Le journal peut être généré et stocké localement sur l’hôte ou le serveur, ou envoyé directement à une adresse de messagerie.</span><span class="sxs-lookup"><span data-stu-id="1d83b-109">The log can be generated and stored locally on the host or server, or sent directly to an email address.</span></span>
  
<span data-ttu-id="1d83b-110">Le fichier journal peut également être téléchargé sur l’ordinateur du client.</span><span class="sxs-lookup"><span data-stu-id="1d83b-110">The log file can also be downloaded to the client's computer.</span></span> <span data-ttu-id="1d83b-111">L’option de téléchargement de client peut être activée ou désactivée en fonction de la configuration et du rôle d’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="1d83b-111">The client download option may be enabled or disabled according to configuration and user role.</span></span>
  
1. <span data-ttu-id="1d83b-112">Dans la barre de menus, cliquez sur l’icône **cogwheel** .</span><span class="sxs-lookup"><span data-stu-id="1d83b-112">In the menu bar, click the **Cogwheel** icon.</span></span> 
    
2. <span data-ttu-id="1d83b-113">Dans l’onglet \*\*paramètres et \> \*\* utilitaires, sélectionnez **configuration du journal \> des incidents**.</span><span class="sxs-lookup"><span data-stu-id="1d83b-113">In the **Settings and utilities \> Utilities** tab, select **Case log \> Setup**.</span></span>
    
3. <span data-ttu-id="1d83b-114">Sélectionnez le **niveau de journalisation** comme suit :</span><span class="sxs-lookup"><span data-stu-id="1d83b-114">Select the **Log level** as follows:</span></span> 
    
  - <span data-ttu-id="1d83b-115">**Standard**: inclut les données de journal de base.</span><span class="sxs-lookup"><span data-stu-id="1d83b-115">**Standard**: Includes the basic log data.</span></span> <span data-ttu-id="1d83b-116">Cette option est généralement nécessaire pour la surveillance et doit être utilisée sauf indication contraire.</span><span class="sxs-lookup"><span data-stu-id="1d83b-116">This option is usually necessary for monitoring, and should be used unless recommended otherwise.</span></span>
    
  - <span data-ttu-id="1d83b-117">**Minimal**: utilisé pour les très grandes situations et renvoie uniquement les données les plus récentes.</span><span class="sxs-lookup"><span data-stu-id="1d83b-117">**Minimal**: Used for very large cases, and returns only the latest data.</span></span>
    
4. <span data-ttu-id="1d83b-118">Cliquez sur **exécuter le journal des cas**.</span><span class="sxs-lookup"><span data-stu-id="1d83b-118">Click **Run Case log**.</span></span> <span data-ttu-id="1d83b-119">Le journal est généré et le chemin d’accès est affiché.</span><span class="sxs-lookup"><span data-stu-id="1d83b-119">The log is generated and path is displayed.</span></span> <span data-ttu-id="1d83b-120">Les informations d’avancement de la tâche pour les tâches en cours et dernière sont affichées dans le volet État de la tâche.</span><span class="sxs-lookup"><span data-stu-id="1d83b-120">The task progress information for the current and last task is displayed in the Task status pane.</span></span>
    
## <a name="clear-data"></a><span data-ttu-id="1d83b-121">Effacer les données</span><span class="sxs-lookup"><span data-stu-id="1d83b-121">Clear data</span></span>

<span data-ttu-id="1d83b-122">S’il est nécessaire de supprimer ou de réinitialiser les données de cas, l’instance de base de données doit être initialisée.</span><span class="sxs-lookup"><span data-stu-id="1d83b-122">If it is necessary to delete or reinitialize case data, the database instance must be initialized.</span></span> <span data-ttu-id="1d83b-123">L’utilitaire effacer les données supprime toutes les entrées spécifiées de la base de données de cas, des fichiers texte, du dossier case et des résultats accumulés.</span><span class="sxs-lookup"><span data-stu-id="1d83b-123">The Clear data utility deletes all specified entries from the case database, text files, case folder, and accumulated results.</span></span> <span data-ttu-id="1d83b-124">La fonction peut uniquement être effectuée par un administrateur.</span><span class="sxs-lookup"><span data-stu-id="1d83b-124">The function can only be performed by an administrator.</span></span>
  
> [!IMPORTANT]
> <span data-ttu-id="1d83b-125">Cette action n’est pas réversible et efface toutes les balises et les analyses de pertinence effectuées par l’expert.</span><span class="sxs-lookup"><span data-stu-id="1d83b-125">This action is not reversible and will clear all Relevance tagging and analysis performed by the expert.</span></span> <span data-ttu-id="1d83b-126">Enregistrer une sauvegarde des données, si nécessaire.</span><span class="sxs-lookup"><span data-stu-id="1d83b-126">Save a backup of data, if necessary.</span></span> <span data-ttu-id="1d83b-127">Utilisez cette option avec une extrême précaution.</span><span class="sxs-lookup"><span data-stu-id="1d83b-127">Use this option with extreme care.</span></span> <span data-ttu-id="1d83b-128">La suppression des fichiers balisés et classés peut avoir un impact sur les résultats de pertinence.</span><span class="sxs-lookup"><span data-stu-id="1d83b-128">Deleting tagged and ranked files can impact the Relevance results.</span></span> 
  
1. <span data-ttu-id="1d83b-129">Dans la barre de menus, cliquez sur l’icône **cogwheel** .</span><span class="sxs-lookup"><span data-stu-id="1d83b-129">In the menu bar, click the **Cogwheel** icon.</span></span> 
    
2. <span data-ttu-id="1d83b-130">Dans l’onglet \*\*paramètres et \> \*\* utilitaires, sélectionnez **effacer la configuration \> des données**.</span><span class="sxs-lookup"><span data-stu-id="1d83b-130">In the **Settings and utilities \> Utilities** tab, select **Clear data \> Setup**.</span></span>
    
3. <span data-ttu-id="1d83b-131">Sélectionnez une option pour l’initialisation des informations :</span><span class="sxs-lookup"><span data-stu-id="1d83b-131">Select an option for the information to initialize:</span></span>
    
  - <span data-ttu-id="1d83b-132">**Pertinence**: supprime tout le travail réalisé en matière de pertinence, y compris la définition des charges et des associations de fichiers à charger.</span><span class="sxs-lookup"><span data-stu-id="1d83b-132">**Relevance**: Deletes all work done in Relevance, including definition of loads and association of files to loads.</span></span> <span data-ttu-id="1d83b-133">Il supprime tous les exemples et balisage.</span><span class="sxs-lookup"><span data-stu-id="1d83b-133">It deletes all samples and tagging.</span></span>
    
  - <span data-ttu-id="1d83b-134">**Near-Duplicates et threads de messagerie**: supprime toutes les informations d’analyse des liens de proximité et des fils de messagerie.</span><span class="sxs-lookup"><span data-stu-id="1d83b-134">**Near-duplicates and email threads**: Deletes all analysis information of near-duplicates and email threads.</span></span>
    
  - <span data-ttu-id="1d83b-135">**Themes**: supprime les données liées aux thèmes.</span><span class="sxs-lookup"><span data-stu-id="1d83b-135">**Themes**: Deletes themes-related data.</span></span>
    
  - <span data-ttu-id="1d83b-136">**Historique des exportations**: supprime les informations d’historique des lots d’exportation.</span><span class="sxs-lookup"><span data-stu-id="1d83b-136">**Export history**: Deletes history information of Export batches.</span></span>
    
4. <span data-ttu-id="1d83b-137">Cliquez sur **effacer les données**.</span><span class="sxs-lookup"><span data-stu-id="1d83b-137">Click **Clear data**.</span></span> <span data-ttu-id="1d83b-138">Les données de cas sont effacées.</span><span class="sxs-lookup"><span data-stu-id="1d83b-138">The case data is cleared.</span></span> <span data-ttu-id="1d83b-139">Les informations d’avancement de la tâche pour les tâches en cours et dernière sont affichées dans le volet État de la **tâche** .</span><span class="sxs-lookup"><span data-stu-id="1d83b-139">The task progress information for the current and last task is displayed in the **Task status** pane.</span></span> 
    
## <a name="modify-relevance"></a><span data-ttu-id="1d83b-140">Modifier la pertinence</span><span class="sxs-lookup"><span data-stu-id="1d83b-140">Modify Relevance</span></span>

<span data-ttu-id="1d83b-141">Cette section décrit comment ignorer ou restaurer un exemple de pertinence.</span><span class="sxs-lookup"><span data-stu-id="1d83b-141">This section describes how to skip or roll back a Relevance sample.</span></span>
  
1. <span data-ttu-id="1d83b-142">Dans la barre de menus, cliquez sur l’icône **cogwheel** .</span><span class="sxs-lookup"><span data-stu-id="1d83b-142">In the menu bar, click the **Cogwheel** icon.</span></span> 
    
2. <span data-ttu-id="1d83b-143">Dans l’onglet \*\*paramètres et \> \*\* utilitaires, sélectionnez **modifier la pertinence**.</span><span class="sxs-lookup"><span data-stu-id="1d83b-143">In the **Settings and utilities \> Utilities** tab, select **Modify relevance**.</span></span>
    
3. <span data-ttu-id="1d83b-144">Sélectionnez l’une des options suivantes :</span><span class="sxs-lookup"><span data-stu-id="1d83b-144">Select from the options:</span></span> 
    
  - <span data-ttu-id="1d83b-145">**Ignorer l’exemple actuel : pour l’utilisateur actuel**: cette balise, sous la forme **Ignorer**, tous les fichiers non balisés dans l’exemple de cas d’ouverture de l’utilisateur qui exécute l’utilitaire.</span><span class="sxs-lookup"><span data-stu-id="1d83b-145">**Skip current sample - for current user**: This will tag, as **Skip**, all untagged files in the open case sample of the user running the utility.</span></span> <span data-ttu-id="1d83b-146">Le traitement de pertinence ne sera pas effectué sur les fichiers marqués comme **Skip**.</span><span class="sxs-lookup"><span data-stu-id="1d83b-146">Relevance processing will not be performed on files tagged as **Skip**.</span></span>
    
  - <span data-ttu-id="1d83b-147">**Ignorer l’exemple actuel-tous les exemples ouverts**: cette balise, sous la forme **Ignorer**, tous les fichiers non balisés de tous les exemples ouverts pour tous les utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="1d83b-147">**Skip current sample - all open samples**: This will tag, as **Skip**, all untagged files in all open samples for all users.</span></span> <span data-ttu-id="1d83b-148">Cette option n’est pas recommandée si les utilisateurs sont actuellement en train de baliser des exemples.</span><span class="sxs-lookup"><span data-stu-id="1d83b-148">This option is not recommended if users are currently tagging samples.</span></span>
    
  - <span data-ttu-id="1d83b-149">**Restaurer le dernier exemple**: le dernier exemple de formation à la pertinence terminé sera annulé, qu’il soit ou non avant ou après le processus de « calcul ».</span><span class="sxs-lookup"><span data-stu-id="1d83b-149">**Roll back last sample**: The last completed Relevance training sample will be rolled back, regardless of whether it is before or after the "Calculate" process.</span></span> <span data-ttu-id="1d83b-150">La restauration d’un exemple de rattrapage n’est pas autorisée.</span><span class="sxs-lookup"><span data-stu-id="1d83b-150">Rollback of a catch-up sample is not allowed.</span></span>
    
4. <span data-ttu-id="1d83b-151">Cliquez sur **exécuter** pour exécuter.</span><span class="sxs-lookup"><span data-stu-id="1d83b-151">Click **Execute** to run.</span></span> 
    
## <a name="transparency-analysis"></a><span data-ttu-id="1d83b-152">Analyse de la transparence</span><span class="sxs-lookup"><span data-stu-id="1d83b-152">Transparency analysis</span></span>

<span data-ttu-id="1d83b-153">L’utilitaire d’analyse de transparence active une vue détaillée des fichiers et le score de pertinence qui leur est attribué.</span><span class="sxs-lookup"><span data-stu-id="1d83b-153">The Transparency analysis utility enables a detailed view of files and their assigned Relevance score.</span></span> <span data-ttu-id="1d83b-154">Le rapport peut être utilisé en tant que contrôle de validité ou comparer la pertinence d’un fichier défini par un réviseur humain par rapport à la pertinence attribuée par Advanced eDiscovery.</span><span class="sxs-lookup"><span data-stu-id="1d83b-154">The report can be used as a sanity check or to compare the relevance of a file defined by a human reviewer as compared to the relevance assigned by Advanced eDiscovery.</span></span> 
  
<span data-ttu-id="1d83b-155">Outre les scores de pertinence, la découverte électronique avancée calcule et affecte des pondérations de mots clés qui envisagent le contexte de mot clé.</span><span class="sxs-lookup"><span data-stu-id="1d83b-155">In addition to Relevance scores, Advanced eDiscovery calculates and assigns keyword weights that consider the keyword context.</span></span> <span data-ttu-id="1d83b-156">Le même mot dans un fichier peut se voir attribuer différents poids, selon le contexte et l’emplacement.</span><span class="sxs-lookup"><span data-stu-id="1d83b-156">The same word in a file can be assigned different weights, depending on context and location.</span></span> <span data-ttu-id="1d83b-157">Chaque mot clé est marqué à l’aide d’une échelle croissante d’intensité de couleur allant de jaune à orange foncé et de différentes nuances de gris.</span><span class="sxs-lookup"><span data-stu-id="1d83b-157">Each keyword is marked using an increasing scale of color intensity ranging from yellow to dark orange and varying shades of gray.</span></span> <span data-ttu-id="1d83b-158">Le codage en couleurs permet d’indiquer visuellement la contribution positive ou négative du mot au score de pertinence.</span><span class="sxs-lookup"><span data-stu-id="1d83b-158">Color coding is used to visually indicate the word's relative positive or negative contribution to the Relevance score.</span></span> 
  
<span data-ttu-id="1d83b-159">Dans un scénario de cas à plusieurs problèmes, un rapport d’analyse de transparence peut être généré pour chaque problème.</span><span class="sxs-lookup"><span data-stu-id="1d83b-159">In a multiple-issue case scenario, a Transparency analysis report can be generated for each issue.</span></span>
  
1. <span data-ttu-id="1d83b-160">Dans la barre de menus, cliquez sur l’icône **cogwheel** .</span><span class="sxs-lookup"><span data-stu-id="1d83b-160">In the menu bar, click the **Cogwheel** icon.</span></span> 
    
2. <span data-ttu-id="1d83b-161">Dans l’onglet \*\*paramètres et \> \*\* utilitaires, sélectionnez Configuration de l' **analyse \> de transparence**.</span><span class="sxs-lookup"><span data-stu-id="1d83b-161">In the **Settings and utilities \> Utilities** tab, select **Transparency analysis \> Setup**.</span></span>
    
3. <span data-ttu-id="1d83b-162">Dans \* \* ID de fichier \* \*, entrez l’ID de fichier du fichier à traiter.</span><span class="sxs-lookup"><span data-stu-id="1d83b-162">In \*\* File ID \*\*, enter the file ID of the file to process.</span></span>
    
4. <span data-ttu-id="1d83b-163">Dans la liste **problème** , sélectionnez le problème pertinent.</span><span class="sxs-lookup"><span data-stu-id="1d83b-163">In the **Issue** list, select the pertinent issue.</span></span> 
    
5. <span data-ttu-id="1d83b-164">Cliquez sur **analyse de transparence**.</span><span class="sxs-lookup"><span data-stu-id="1d83b-164">Click **Transparency analysis**.</span></span> <span data-ttu-id="1d83b-165">Une fois l’opération terminée, le rapport d’analyse de transparence du fichier s’affiche, qui montre comment les couleurs de mots clés marquées correspondent au score global de pertinence.</span><span class="sxs-lookup"><span data-stu-id="1d83b-165">Upon completion, the Transparency analysis report for the file is displayed, which shows how the marked keyword colors correlate to the overall Relevance score.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="1d83b-166">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1d83b-166">See also</span></span>

[<span data-ttu-id="1d83b-167">Office 365 Advanced eDiscovery</span><span class="sxs-lookup"><span data-stu-id="1d83b-167">Office 365 Advanced eDiscovery</span></span>](office-365-advanced-ediscovery.md)
  
[<span data-ttu-id="1d83b-168">Définition des paramètres de cas et de client</span><span class="sxs-lookup"><span data-stu-id="1d83b-168">Defining case and tenant settings</span></span>](define-case-and-tenant-settings-in-advanced-ediscovery.md)

