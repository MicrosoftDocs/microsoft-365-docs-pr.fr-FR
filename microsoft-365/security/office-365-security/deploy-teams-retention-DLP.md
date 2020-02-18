---
title: Protéger des fichiers dans Teams avec des étiquettes de rétention et la protection contre la perte de données (DLP)
f1.keywords:
- NOCSH
ms.author: josephd
author: JoeDavies-MSFT
manager: laurawi
ms.date: 10/31/2019
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Priority
search.appverid:
- MET150
ms.collection:
- Ent_O365
- Strat_O365_Enterprise
ms.custom:
- Ent_Solutions
ms.assetid: c9f837af-8d71-4df1-a285-dedb1c5618b3
description: 'Résumé : appliquez des étiquettes de rétention et des stratégies DLP à des fichiers dans Teams, avec différents niveaux de protection des informations.'
ms.openlocfilehash: 94d8a02d0ea88fa8a05cd6a2c95a2db866d72fad
ms.sourcegitcommit: 3dd9944a6070a7f35c4bc2b57df397f844c3fe79
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/15/2020
ms.locfileid: "42083395"
---
# <a name="protect-files-in-teams-with-retention-labels-and-dlp"></a><span data-ttu-id="b37e5-103">Protéger des fichiers dans Teams avec des étiquettes de rétention et la protection contre la perte de données (DLP)</span><span class="sxs-lookup"><span data-stu-id="b37e5-103">Protect files in teams with retention labels and DLP</span></span>

 
<span data-ttu-id="b37e5-104">Utilisez les étapes de cet article pour concevoir et déployer des étiquettes de rétention et des stratégies de protection contre la perte de données pour des sites d’équipe et leur site SharePoint sous-jacent de base de référence, sensibles et hautement confidentiels.</span><span class="sxs-lookup"><span data-stu-id="b37e5-104">Use the steps in this article to design and deploy retention labels and data loss prevention (DLP) policies for baseline, sensitive, and highly confidential teams and their underlying SharePoint sites.</span></span> <span data-ttu-id="b37e5-105">Pour plus d’informations sur ces trois niveaux de protection, consultez [Sécuriser des fichiers dans Microsoft Teams](secure-files-in-teams.md).</span><span class="sxs-lookup"><span data-stu-id="b37e5-105">For more information about these three tiers of protection, see [Secure files in Microsoft Teams](secure-files-in-teams.md).</span></span>
  
## <a name="how-this-works"></a><span data-ttu-id="b37e5-106">Procédure</span><span class="sxs-lookup"><span data-stu-id="b37e5-106">How this works</span></span>

1. <span data-ttu-id="b37e5-107">Créez les étiquettes de rétention de votre choix et publiez-les.</span><span class="sxs-lookup"><span data-stu-id="b37e5-107">Create the desired retention labels and publish these.</span></span> <span data-ttu-id="b37e5-108">La publication peut prendre jusqu’à 12 heures.</span><span class="sxs-lookup"><span data-stu-id="b37e5-108">It can take up to 12 hours for these to be published.</span></span>
2. <span data-ttu-id="b37e5-109">Pour les sites SharePoint sous-jacents souhaités, modifiez les paramètres de la bibliothèque de documents afin d’appliquer les étiquettes de rétention de votre choix aux éléments de la bibliothèque.</span><span class="sxs-lookup"><span data-stu-id="b37e5-109">For the desired underlying SharePoint sites, edit the document library settings to apply the desired retention labels to items in the library.</span></span>
3. <span data-ttu-id="b37e5-110">Créez des stratégies DLP pour prendre des mesures en fonction des étiquettes de rétention.</span><span class="sxs-lookup"><span data-stu-id="b37e5-110">Create DLP policies to take action based on the retention labels.</span></span>

<span data-ttu-id="b37e5-111">Lorsque des utilisateurs ajoutent un document à la bibliothèque de site SharePoint sous-jacent pour l’équipe, celui-ci reçoit par défaut l’étiquette de rétention attribuée.</span><span class="sxs-lookup"><span data-stu-id="b37e5-111">When users add a document to the underlying SharePoint site library for the team, the document will receive the assigned retention label by default.</span></span> <span data-ttu-id="b37e5-112">Si nécessaire, les utilisateurs peuvent changer l’étiquette.</span><span class="sxs-lookup"><span data-stu-id="b37e5-112">Users can change the label, if needed.</span></span> <span data-ttu-id="b37e5-113">Lorsqu’un utilisateur partage un document en dehors de l’organisation, DLP vérifie si une étiquette est attribuée et prend les mesures qui s’imposent si une stratégie DLP correspond à l’étiquette.</span><span class="sxs-lookup"><span data-stu-id="b37e5-113">When a user shares a document outside the organization, DLP will check to see if a label is assigned and take action if a DLP policy matches the label.</span></span> <span data-ttu-id="b37e5-114">DLP recherche également les correspondances liées à d’autres stratégies, comme la protection des fichiers avec des numéros de carte de crédit si ce type de stratégie est configuré.</span><span class="sxs-lookup"><span data-stu-id="b37e5-114">DLP will look for other policy matches as well, such as protecting files with credit card numbers if this type of policy is configured.</span></span> 

## <a name="retention-labels-for-your-underlying-sharepoint-sites"></a><span data-ttu-id="b37e5-115">Étiquettes de rétention pour vos sites SharePoint sous-jacents</span><span class="sxs-lookup"><span data-stu-id="b37e5-115">Retention labels for your underlying SharePoint sites</span></span>

<span data-ttu-id="b37e5-116">Trois phases s’offrent à vous pour créer et affecter des étiquettes de rétention aux sites SharePoint sous-jacents.</span><span class="sxs-lookup"><span data-stu-id="b37e5-116">There are three phases to creating and then assigning retention labels to underlying SharePoint sites.</span></span>
  
### <a name="step-1-determine-the-retention-label-names"></a><span data-ttu-id="b37e5-117">Étape 1 : Déterminer les noms des étiquettes de rétention</span><span class="sxs-lookup"><span data-stu-id="b37e5-117">Step 1: Determine the retention label names</span></span>

<span data-ttu-id="b37e5-118">Au cours de cette phase, vous déterminez les noms de vos étiquettes de rétention pour les quatre niveaux de protection des informations appliqués aux sites SharePoint sous-jacents.</span><span class="sxs-lookup"><span data-stu-id="b37e5-118">In this phase, you determine the names of your retention labels for the four levels of information protection applied to underlying SharePoint sites.</span></span> <span data-ttu-id="b37e5-119">Le tableau suivant répertorie les noms recommandés pour chaque niveau.</span><span class="sxs-lookup"><span data-stu-id="b37e5-119">The following table lists the recommended names for each level.</span></span>
  
|<span data-ttu-id="b37e5-120">**niveau de protection des sites SharePoint sous-jacents**</span><span class="sxs-lookup"><span data-stu-id="b37e5-120">**underlying SharePoint sites protection level**</span></span>|<span data-ttu-id="b37e5-121">**Nom de l’étiquette**</span><span class="sxs-lookup"><span data-stu-id="b37e5-121">**Label name**</span></span>|
|:-----|:-----|
|<span data-ttu-id="b37e5-122">Base de référence - Public</span><span class="sxs-lookup"><span data-stu-id="b37e5-122">Baseline-Public</span></span>  <br/> |<span data-ttu-id="b37e5-123">Public interne</span><span class="sxs-lookup"><span data-stu-id="b37e5-123">Internal public</span></span>  <br/> |
|<span data-ttu-id="b37e5-124">Base de référence - Privé</span><span class="sxs-lookup"><span data-stu-id="b37e5-124">Baseline-Private</span></span>  <br/> |<span data-ttu-id="b37e5-125">Private</span><span class="sxs-lookup"><span data-stu-id="b37e5-125">Private</span></span>  <br/> |
|<span data-ttu-id="b37e5-126">Sensible</span><span class="sxs-lookup"><span data-stu-id="b37e5-126">Sensitive</span></span>  <br/> |<span data-ttu-id="b37e5-127">Sensible</span><span class="sxs-lookup"><span data-stu-id="b37e5-127">Sensitive</span></span>  <br/> |
|<span data-ttu-id="b37e5-128">Hautement confidentiel</span><span class="sxs-lookup"><span data-stu-id="b37e5-128">Highly Confidential</span></span>  <br/> |<span data-ttu-id="b37e5-129">Hautement confidentiel</span><span class="sxs-lookup"><span data-stu-id="b37e5-129">Highly Confidential</span></span>  <br/> |
   
### <a name="step-2-create-the-retention-labels"></a><span data-ttu-id="b37e5-130">Étape 2 : Créer les étiquettes de rétention</span><span class="sxs-lookup"><span data-stu-id="b37e5-130">Step 2: Create the retention labels</span></span>

<span data-ttu-id="b37e5-131">Au cours de cette phase, vous créez puis vous publiez les étiquettes que vous avez déterminées pour les différents niveaux de protection des informations.</span><span class="sxs-lookup"><span data-stu-id="b37e5-131">In this phase, you create and then publish your determined labels for the different levels of information protection.</span></span>
  
1. <span data-ttu-id="b37e5-132">Connectez-vous au [portail de conformité Microsoft 365](https://compliance.microsoft.com) avec un compte disposant du rôle Administrateur de la sécurité ou Administrateur de la société.</span><span class="sxs-lookup"><span data-stu-id="b37e5-132">Sign in to the [Microsoft 365 compliance portal](https://compliance.microsoft.com) with an account that has the Security Administrator or Company Administrator role.</span></span>
    
2. <span data-ttu-id="b37e5-133">Sous l’onglet **Accueil - Conformité Microsoft 365** de votre navigateur, cliquez sur **Classifications > Étiquettes**.</span><span class="sxs-lookup"><span data-stu-id="b37e5-133">From the **Home - Microsoft 365 compliance** tab of your browser, click **Classifications > Labels**.</span></span>
    
3. <span data-ttu-id="b37e5-134">Cliquez sur **Étiquettes de rétention > Créer une étiquette**.</span><span class="sxs-lookup"><span data-stu-id="b37e5-134">Click **Retention labels > Create a label**.</span></span>
    
4. <span data-ttu-id="b37e5-135">Dans le volet **Nommer l’étiquette**, entrez le nom de l’étiquette ainsi qu’une description destinée aux administrateurs et aux utilisateurs, puis cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="b37e5-135">On the **Name your label** pane, type the name of the label and a description for admins and users, and then click **Next**.</span></span>

5. <span data-ttu-id="b37e5-136">Dans le volet **Descripteurs de plan de gestion de fichiers**, complétez les champs requis, puis cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="b37e5-136">On the **File plan descriptors** pane, fill in as needed, and then click **Next**.</span></span>
    
6. <span data-ttu-id="b37e5-137">Dans le volet **Paramètres d’étiquette**, si nécessaire, définissez **Rétention** sur **Activé** et configurez les paramètres de rétention.</span><span class="sxs-lookup"><span data-stu-id="b37e5-137">On the **Label settings** pane, if needed, set **Retention** to **On** and configure retention settings.</span></span> <span data-ttu-id="b37e5-138">Cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="b37e5-138">Click **Next**.</span></span>
    
7. <span data-ttu-id="b37e5-139">Dans le volet **Vérifier vos paramètres**, cliquez sur **Créer l’étiquette**.</span><span class="sxs-lookup"><span data-stu-id="b37e5-139">On the **Review your settings** pane, click **Create the label**.</span></span>
    
8. <span data-ttu-id="b37e5-140">Pour vos autres étiquettes, cliquez sur **Créer une étiquette** puis, si nécessaire, répétez les étapes 3 à 7.</span><span class="sxs-lookup"><span data-stu-id="b37e5-140">For your additional labels, click **Create a label**, and then repeat steps 3-7 in this procedure as needed.</span></span>
    

### <a name="publish-your-new-labels"></a><span data-ttu-id="b37e5-141">Publier vos nouvelles étiquettes</span><span class="sxs-lookup"><span data-stu-id="b37e5-141">Publish your new labels</span></span>

<span data-ttu-id="b37e5-142">Procédez comme suit pour publier les nouvelles étiquettes de rétention.</span><span class="sxs-lookup"><span data-stu-id="b37e5-142">Next, use these steps to publish the new retention labels.</span></span>
  
1. <span data-ttu-id="b37e5-143">Depuis le volet **Étiquettes**, cliquez sur l’onglet **Étiquettes de rétention**, puis sur **Publier les étiquettes**.</span><span class="sxs-lookup"><span data-stu-id="b37e5-143">From the **Labels** pane, click the **Retention labels** tab, and then click **Publish labels**.</span></span>
    
2. <span data-ttu-id="b37e5-144">Dans le volet **Choisir les étiquettes à publier**, cliquez sur **Choisir les étiquettes à publier**.</span><span class="sxs-lookup"><span data-stu-id="b37e5-144">On the **Choose labels to publish** pane, click **Choose labels to publish**.</span></span>
    
3. <span data-ttu-id="b37e5-145">Dans le volet **Choisir des étiquettes**, cliquez sur **Ajouter**, sélectionnez les quatre étiquettes, puis cliquez à nouveau sur **Ajouter**.</span><span class="sxs-lookup"><span data-stu-id="b37e5-145">On the **Choose labels** pane, click **Add**, select all four labels, click **Add**.</span></span>
    
4. <span data-ttu-id="b37e5-146">Cliquez sur **Terminé**.</span><span class="sxs-lookup"><span data-stu-id="b37e5-146">Click **Done**.</span></span>
    
5. <span data-ttu-id="b37e5-147">Dans le volet **Choisir les étiquettes à publier**, cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="b37e5-147">On the **Choose labels to publish** pane, click **Next**.</span></span>
    
6. <span data-ttu-id="b37e5-148">Dans le volet **Choisir les emplacements**, cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="b37e5-148">On the **Choose locations** pane, click **Next**.</span></span>
    
7. <span data-ttu-id="b37e5-149">Dans le volet **Nom de votre stratégie**, entrez un nom pour désigner l’ensemble des étiquettes dans **Nom**, puis cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="b37e5-149">On the **Name your policy** pane, type a name for your set of labels in **Name**, and then click **Next**.</span></span>
    
8. <span data-ttu-id="b37e5-150">Dans le volet **Vérifier vos paramètres**, cliquez sur **Publier les étiquettes**, puis sur **Fermer**.</span><span class="sxs-lookup"><span data-stu-id="b37e5-150">On the **Review your settings** pane, click **Publish labels**, and then click **Close**.</span></span>

    
### <a name="step-3-apply-the-retention-labels-to-your-underlying-sharepoint-sites"></a><span data-ttu-id="b37e5-151">Étape 3 : appliquer les étiquettes de rétention à vos sites SharePoint sous-jacents</span><span class="sxs-lookup"><span data-stu-id="b37e5-151">Step 3: Apply the retention labels to your underlying SharePoint sites</span></span>

<span data-ttu-id="b37e5-152">Utilisez ces étapes pour appliquer les étiquettes de rétention aux dossiers de documents de vos sites SharePoint sous-jacents.</span><span class="sxs-lookup"><span data-stu-id="b37e5-152">Use these steps to apply the retention labels to the documents folders of your underlying SharePoint sites.</span></span>
  
1.  <span data-ttu-id="b37e5-153">À partir de l’équipe, cliquez sur **Fichiers**, puis cliquez sur **Ouvrir dans SharePoint**.</span><span class="sxs-lookup"><span data-stu-id="b37e5-153">From the team, click **Files**, and then click **Open in SharePoint**.</span></span>

2. <span data-ttu-id="b37e5-154">Sous le nouvel onglet du Site SharePoint de votre navigateur, cliquez sur **Documents**.</span><span class="sxs-lookup"><span data-stu-id="b37e5-154">In the new SharePoint site tab of your browser, click **Documents**.</span></span>
    
3. <span data-ttu-id="b37e5-155">Cliquez sur l’icône des paramètres, puis cliquez sur **Paramètres de la bibliothèque**.</span><span class="sxs-lookup"><span data-stu-id="b37e5-155">Click the settings icon, and then click **Library settings**.</span></span>
    
4. <span data-ttu-id="b37e5-156">Sous **Autorisations et gestion**, cliquez sur **Appliquer l’étiquette aux éléments de cette bibliothèque**.</span><span class="sxs-lookup"><span data-stu-id="b37e5-156">Under **Permissions and Management**, click **Apply label to items in this library**.</span></span>
    
5. <span data-ttu-id="b37e5-157">Dans **Paramètres-Appliquer une étiquette**, sélectionnez l’étiquette de rétention qui convient, puis cliquez sur **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="b37e5-157">In **Settings-Apply Label**, select the appropriate retention label, and then click **Save**.</span></span>
    
6. <span data-ttu-id="b37e5-158">Fermez l’onglet du site SharePoint.</span><span class="sxs-lookup"><span data-stu-id="b37e5-158">Close the tab for the SharePoint site.</span></span>
    
7. <span data-ttu-id="b37e5-159">Répétez les étapes 1 à 6 pour attribuer des étiquettes de rétention à vos autres sites SharePoint sous-jacents.</span><span class="sxs-lookup"><span data-stu-id="b37e5-159">Repeat steps 1-6 to assign retention labels to your additional underlying SharePoint sites.</span></span>
    
<span data-ttu-id="b37e5-160">Voici la configuration finale.</span><span class="sxs-lookup"><span data-stu-id="b37e5-160">Here is your resulting configuration.</span></span>
  
![Étiquettes de rétention des quatre types de sites SharePoint sous-jacents.](../../media/retention-labels.png)
  
## <a name="dlp-policies-for-your-underlying-sharepoint-sites"></a><span data-ttu-id="b37e5-162">Stratégies DLP pour vos sites SharePoint sous-jacents</span><span class="sxs-lookup"><span data-stu-id="b37e5-162">DLP policies for your underlying SharePoint sites</span></span>

<span data-ttu-id="b37e5-163">Suivez ces étapes pour configurer une stratégie DLP qui avertit les utilisateurs lorsqu’ils partagent un document sur un site SharePoint sous-jacent externe à l’organisation.</span><span class="sxs-lookup"><span data-stu-id="b37e5-163">Use these steps to configure a DLP policy that notifies users when they share a document on an underlying SharePoint site outside the organization.</span></span>

1. <span data-ttu-id="b37e5-164">Connectez-vous au [Centre de conformité Microsoft 365](https://compliance.microsoft.com/) avec un compte disposant du rôle Administrateur de la sécurité ou Administrateur de la société.</span><span class="sxs-lookup"><span data-stu-id="b37e5-164">Sign in to the [Microsoft 365 compliance portal](https://compliance.microsoft.com/) with an account that has the Security Administrator or Company Administrator role.</span></span>
    
2. <span data-ttu-id="b37e5-165">Sous le nouvel onglet **Conformité Microsoft 365** de votre navigateur, cliquez sur **Stratégie > Protection contre la perte de données**.</span><span class="sxs-lookup"><span data-stu-id="b37e5-165">On the new **Microsoft 365 compliance** tab in your browser, click **Policies > Data loss prevention**.</span></span>
    
3. <span data-ttu-id="b37e5-166">Dans le volet **Accueil > Protection contre la perte de données**, cliquez sur **Créer une stratégie**.</span><span class="sxs-lookup"><span data-stu-id="b37e5-166">In the **Home > Data loss prevention** pane, click **Create a policy**.</span></span>
    
4. <span data-ttu-id="b37e5-167">Dans le volet **Commencez en utilisant un modèle ou créez une stratégie personnalisée**, cliquez sur **Personnalisé**, puis sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="b37e5-167">In the **Start with a template or create a custom policy** pane, click **Custom**, and then click **Next**.</span></span>
    
5. <span data-ttu-id="b37e5-168">Dans le volet **Nom de votre stratégie**, entrez le nom de la stratégie DLP sensible dans **Nom**, puis cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="b37e5-168">In the **Name your policy** pane, type the name for the sensitive level DLP policy in **Name**, and then click **Next**.</span></span>
    
6. <span data-ttu-id="b37e5-169">Dans le volet **Choisir les emplacements**, cliquez sur **Me laisser choisir des emplacements spécifiques**, puis sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="b37e5-169">In the **Choose locations** pane, click **Let me choose specific locations**, and then click **Next**.</span></span>
    
7. <span data-ttu-id="b37e5-170">Dans la liste des emplacements, désactivez les emplacements **Courrier Exchange**, **Comptes OneDrive** et **Messages de conversations et de canaux Teams**, puis cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="b37e5-170">In the list of locations, disable the **Exchange email**, **OneDrive accounts**, and **Teams chat and channel messages** locations, and then click **Next**.</span></span>
    
8. <span data-ttu-id="b37e5-171">Dans le volet **Personnalisez le type de contenu que vous voulez protéger**, cliquez sur **Modifier**.</span><span class="sxs-lookup"><span data-stu-id="b37e5-171">In the **Customize the type of content you want to protect** pane, click **Edit**.</span></span>
    
9. <span data-ttu-id="b37e5-172">Dans le volet **Choisissez les types de contenu à protéger**, cliquez sur **Ajouter** dans la zone déroulante, puis sélectionnez **Étiquettes de rétention**.</span><span class="sxs-lookup"><span data-stu-id="b37e5-172">In the **Choose the types of content to protect** pane, click **Add** in the drop-down box, and then click **Retention labels**.</span></span>
    
10. <span data-ttu-id="b37e5-173">Dans le volet **Étiquettes de rétention**, cliquez sur **Ajouter**, sélectionnez l’étiquette **Sensible**, puis cliquez sur **Ajouter** et sur **Terminé**.</span><span class="sxs-lookup"><span data-stu-id="b37e5-173">In the **Retention labels** pane, click **Add**, select the **Sensitive** label, click **Add**, and then click **Done**.</span></span>
    
11. <span data-ttu-id="b37e5-174">Dans le volet **Choisir les types de contenu à protéger**, cliquez sur **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="b37e5-174">In the **Choose the types of content to protect** pane, click **Save**.</span></span>
    
12. <span data-ttu-id="b37e5-175">Dans le volet **Personnaliser les types d’informations sensibles que vous souhaitez protéger**, cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="b37e5-175">In the **Customize the type of content you want to protect** pane, click **Next**.</span></span>

13. <span data-ttu-id="b37e5-176">Dans le volet **Que faire en cas de détection d’informations sensibles ?**, cliquez sur **Personnaliser l’info-bulle et l’e-mail**.</span><span class="sxs-lookup"><span data-stu-id="b37e5-176">In the **What do you want to do if we detect sensitive info?** pane, click **Customize the tip and email**.</span></span>
    
14. <span data-ttu-id="b37e5-177">Dans le volet **Personnaliser les conseils et les notifications par e-mail de la stratégie**, cliquez sur **Personnaliser le texte de l’info-bulle de la stratégie**.</span><span class="sxs-lookup"><span data-stu-id="b37e5-177">In the **Customize policy tips and email notifications** pane, click **Customize the policy tip text**.</span></span>
    
15. <span data-ttu-id="b37e5-178">Dans la zone de texte, tapez ou collez l’une des astuces suivantes :</span><span class="sxs-lookup"><span data-stu-id="b37e5-178">In the text box, type or paste in one of the following tips:</span></span>
    
  - <span data-ttu-id="b37e5-p106">Pour partager un fichier avec un utilisateur extérieur à l’organisation, téléchargez-le et ouvrez-le. Cliquez sur Fichier > Protéger le document > Chiffrer avec mot de passe, puis indiquez un mot de passe fort. Envoyez le mot de passe par e-mail ou un autre moyen de communication.</span><span class="sxs-lookup"><span data-stu-id="b37e5-p106">To share with a user outside the organization, download the file and then open it. Click File, then Protect Document, and then Encrypt with Password, and then specify a strong password. Send the password in a separate email or other means of communication.</span></span>
  - <span data-ttu-id="b37e5-p107">Les fichiers hautement confidentiels sont protégés par chiffrement. Seuls les utilisateurs externes qui y ont été autorisés par votre service informatique peuvent lire ces fichiers.</span><span class="sxs-lookup"><span data-stu-id="b37e5-p107">Highly confidential files are protected with encryption. Only external users who are granted permissions to these files by your IT department can read them.</span></span>
    
    <span data-ttu-id="b37e5-184">Vous pouvez également saisir ou coller votre propre conseil de stratégie pour expliquer aux utilisateurs comment partager un fichier en dehors de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="b37e5-184">Alternately, type or paste in your own policy tip that instructs users on how to share a file outside your organization.</span></span>
    
16. <span data-ttu-id="b37e5-185">Cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="b37e5-185">Click **OK**.</span></span>
    
17. <span data-ttu-id="b37e5-186">Dans le volet Office **Que faire en cas de détection d’informations sensibles ?**, cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="b37e5-186">In the **What do you want to do if we detect sensitive info?** pane, click **Next**.</span></span>
    
18. <span data-ttu-id="b37e5-187">Dans le volet **Voulez-vous activer la stratégie ou d’abord effectuer des tests ?**, cliquez sur **Oui, l’activer maintenant**, puis cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="b37e5-187">In the **Do you want to turn on the policy or test things out first?** pane, click **Yes, turn it on right away**, and then click **Next**.</span></span>
    
19. <span data-ttu-id="b37e5-188">Dans le volet **Vérifier vos paramètres**, cliquez sur **Créer**, puis sur **Fermer**.</span><span class="sxs-lookup"><span data-stu-id="b37e5-188">In the **Review your settings** pane, click **Create**, and then click **Close**.</span></span>
    
<span data-ttu-id="b37e5-189">Voici le résultat de votre configuration pour les équipes sensibles.</span><span class="sxs-lookup"><span data-stu-id="b37e5-189">Here is your resulting configuration for sensitive teams.</span></span>
  
![Stratégie DLP pour équipe sensible utilisant l’étiquette de rétention Sensible](../../media/retention-labels-sensitive-dlp.png)
  
<span data-ttu-id="b37e5-191">Ensuite, suivez ces étapes pour configurer une stratégie DLP qui bloque les utilisateurs lorsqu’ils partagent un document sur un site SharePoint sous-jacent externe à l’organisation.</span><span class="sxs-lookup"><span data-stu-id="b37e5-191">Next, use these steps to configure a DLP policy that blocks users when they share a document on an underlying SharePoint site outside the organization.</span></span>
  
1. <span data-ttu-id="b37e5-192">Sous le nouvel onglet **Conformité Microsoft 365** de votre navigateur, cliquez sur **Stratégie > Protection contre la perte de données**.</span><span class="sxs-lookup"><span data-stu-id="b37e5-192">On the new **Microsoft 365 compliance** tab in your browser, click **Policies > Data loss prevention**.</span></span>
    
2. <span data-ttu-id="b37e5-193">Dans le volet **Protection contre la perte de données**, cliquez sur **Créer une stratégie**.</span><span class="sxs-lookup"><span data-stu-id="b37e5-193">In the **Data loss prevention** pane, click **Create a policy**.</span></span>
    
3. <span data-ttu-id="b37e5-194">Dans le volet **Utiliser un modèle ou créer une stratégie personnalisée**, cliquez sur **Personnalisé**, puis sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="b37e5-194">In the **Start with a template or create a custom policy** pane, click **Custom**, and then click **Next**.</span></span>
    
4. <span data-ttu-id="b37e5-195">Dans le volet **Nom de votre stratégie**, entrez le nom de la stratégie DLP hautement sensible dans **Nom**, puis cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="b37e5-195">In the **Name your policy** pane, type the name for the highly sensitive level DLP policy in **Name**, and then click **Next**.</span></span>
    
5. <span data-ttu-id="b37e5-196">Dans le volet **Choisir des emplacements**, cliquez sur **Me laisser choisir des emplacements spécifiques**, puis cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="b37e5-196">In the **Choose locations** pane, click **Let me choose specific locations**, and then click **Next**.</span></span>
    
6. <span data-ttu-id="b37e5-197">Dans la liste des emplacements, désactivez les emplacements **Courrier Exchange**, **Comptes OneDrive** et **Messages de conversations et de canaux Teams**, puis cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="b37e5-197">In the list of locations, disable the **Exchange email**, **OneDrive accounts**, and **Teams chat and channel messages** locations, and then click **Next**.</span></span>
    
7. <span data-ttu-id="b37e5-198">Dans le volet **Personnalisez les types d’informations sensibles que vous voulez protéger**, cliquez sur **Modifier**.</span><span class="sxs-lookup"><span data-stu-id="b37e5-198">In the **Customize the types of sensitive info you want to protect** pane, click **Edit**.</span></span>
    
8. <span data-ttu-id="b37e5-199">Dans le volet **Choisissez les types de contenu à protéger**, cliquez sur **Ajouter** dans la zone déroulante, puis sélectionnez **Étiquettes de rétention**.</span><span class="sxs-lookup"><span data-stu-id="b37e5-199">In the **Choose the types of content to protect** pane, click **Add** in the drop-down box, and then click **Retention labels**.</span></span>
    
9. <span data-ttu-id="b37e5-200">Dans le volet **Étiquettes de rétention**, cliquez sur **Ajouter**, sélectionnez l’étiquette **Hautement confidentiel**, puis cliquez sur **Ajouter** et sur **Terminé**.</span><span class="sxs-lookup"><span data-stu-id="b37e5-200">In the **Retention labels** pane, click **Add**, select the **Highly Confidential** label, click **Add**, and then click **Done**.</span></span>
    
10. <span data-ttu-id="b37e5-201">Dans le volet **Choisir les types de contenu à protéger**, cliquez sur **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="b37e5-201">In the **Choose the types of content to protect** pane, click **Save**.</span></span>
    
12. <span data-ttu-id="b37e5-202">Dans le volet **Personnaliser les types d’informations sensibles que vous voulez protéger**, cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="b37e5-202">In the **Customize the types of sensitive info you want to protect** pane, click **Next**.</span></span>
    
13. <span data-ttu-id="b37e5-203">Dans le volet **Que voulez-vous faire si nous détectons des informations confidentielles ?**, cliquez sur **Personnaliser l’info-bulle et la messagerie électronique**.</span><span class="sxs-lookup"><span data-stu-id="b37e5-203">In the **What do you want to do if we detect sensitive info?** pane, click **Customize the tip and email**.</span></span>
    
14. <span data-ttu-id="b37e5-204">Dans le volet **Personnaliser les conseils et les notifications par e-mail de la stratégie**, cliquez sur **Personnaliser le texte de l’info-bulle de la stratégie**.</span><span class="sxs-lookup"><span data-stu-id="b37e5-204">In the **Customize policy tips and email notifications** pane, click **Customize the policy tip text**.</span></span>
    
15. <span data-ttu-id="b37e5-205">Dans la zone de texte, tapez ou collez ce qui suit :</span><span class="sxs-lookup"><span data-stu-id="b37e5-205">In the text box, type or paste in the following:</span></span>
    
  - <span data-ttu-id="b37e5-p108">Pour partager un fichier avec un utilisateur extérieur à l’organisation, téléchargez-le et ouvrez-le. Cliquez sur Fichier > Protéger le document > Chiffrer avec mot de passe, puis indiquez un mot de passe fort. Envoyez le mot de passe par e-mail ou un autre moyen de communication.</span><span class="sxs-lookup"><span data-stu-id="b37e5-p108">To share with a user outside the organization, download the file and then open it. Click File, then Protect Document, and then Encrypt with Password, and then specify a strong password. Send the password in a separate email or other means of communication.</span></span>
    
    <span data-ttu-id="b37e5-209">Vous pouvez également saisir ou coller votre propre conseil de stratégie pour expliquer aux utilisateurs comment partager un fichier en dehors de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="b37e5-209">Alternately, type or paste in your own policy tip that instructs users on how to share a file outside your organization.</span></span>
    
16. <span data-ttu-id="b37e5-210">Cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="b37e5-210">Click **OK**.</span></span>
    
17. <span data-ttu-id="b37e5-211">Dans le volet **Que faire en cas de détection d’informations sensibles ?**, sous **Détecter les cas où une quantité spécifique d’informations sensibles sont partagées en même temps**, cliquez sur **Restreindre l’accès ou chiffrer le contenu**, puis cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="b37e5-211">In the **What do you want to do if we detect sensitive info?** pane, under **Detect when a specific amount of sensitive info is being shared at one time**, click **Restrict access or encrypt the content**, and then click **Next**.</span></span>
    
18. <span data-ttu-id="b37e5-212">Dans le volet **Voulez-vous activer la stratégie ou d’abord effectuer des tests ?**, cliquez sur **Oui, l’activer maintenant**, puis cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="b37e5-212">In the **Do you want to turn on the policy or test things out first?** pane, click **Yes, turn it on right away**, and then click **Next**.</span></span>
    
19. <span data-ttu-id="b37e5-213">Dans le volet **Vérifier vos paramètres**, cliquez sur **Créer**, puis sur **Fermer**.</span><span class="sxs-lookup"><span data-stu-id="b37e5-213">In the **Review your settings** pane, click **Create**, and then click **Close**.</span></span>
    
<span data-ttu-id="b37e5-214">Voici le résultat de votre configuration pour les équipes Hautement confidentielles.</span><span class="sxs-lookup"><span data-stu-id="b37e5-214">Here is your resulting configuration for high confidentiality team.</span></span>
  
![Stratégie DLP pour une équipe de haute confidentialité utilisant l’étiquette de rétention Hautement confidentiel](../../media/retention-labels-highly-confidential-dlp.png)
  
## <a name="next-step"></a><span data-ttu-id="b37e5-216">Étape suivante</span><span class="sxs-lookup"><span data-stu-id="b37e5-216">Next step</span></span>

[<span data-ttu-id="b37e5-217">Protéger des fichiers dans Teams avec des étiquettes de confidentialité</span><span class="sxs-lookup"><span data-stu-id="b37e5-217">Protect files in teams with sensitivity labels</span></span>](deploy-teams-sensitivity-labels.md)
    
## <a name="see-also"></a><span data-ttu-id="b37e5-218">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b37e5-218">See Also</span></span>

[<span data-ttu-id="b37e5-219">Sécuriser des fichiers dans Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="b37e5-219">Secure files in Microsoft Teams</span></span>](secure-files-in-teams.md)
  
[<span data-ttu-id="b37e5-220">Adoption du cloud et solutions hybrides</span><span class="sxs-lookup"><span data-stu-id="b37e5-220">Cloud adoption and hybrid solutions</span></span>](https://docs.microsoft.com/office365/enterprise/cloud-adoption-and-hybrid-solutions)


