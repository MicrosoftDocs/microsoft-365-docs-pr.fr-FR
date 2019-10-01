---
title: Protéger les fichiers SharePoint Online avec des étiquettes de rétention et la protection contre la perte de données (DLP)
ms.author: josephd
author: JoeDavies-MSFT
manager: laurawi
ms.date: 06/18/2019
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
description: 'Résumé : appliquez des étiquettes de rétention et des stratégies DLP à des sites d’équipe SharePoint Online, avec différents niveaux de protection des informations.'
ms.openlocfilehash: 77da4ec44e31fae8db2c37ebc39233f76c5e4dd3
ms.sourcegitcommit: 8e5b799efd3ddd0eae9dd2835c3783103817fb4b
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/30/2019
ms.locfileid: "37317606"
---
# <a name="protect-sharepoint-online-files-with-retention-labels-and-dlp"></a><span data-ttu-id="90255-103">Protéger les fichiers SharePoint Online avec des étiquettes de rétention et la protection contre la perte de données (DLP)</span><span class="sxs-lookup"><span data-stu-id="90255-103">Protect SharePoint Online files with retention labels and DLP</span></span>

 <span data-ttu-id="90255-104">**Résumé :** appliquez des étiquettes de rétention et des stratégies DLP à des sites d’équipe SharePoint Online, avec différents niveaux de protection des informations.</span><span class="sxs-lookup"><span data-stu-id="90255-104">**Summary:** Apply retention labels and data loss prevention (DLP) policies for SharePoint Online team sites with various levels of information protection.</span></span>
  
<span data-ttu-id="90255-105">Suivez les étapes décrites dans cet article afin de créer et de déployer des étiquettes de rétention et des stratégies DLP pour des sites d’équipe SharePoint Online de base, sensibles et hautement confidentiels.</span><span class="sxs-lookup"><span data-stu-id="90255-105">Use the steps in this article to design and deploy retention labels and DLP policies for baseline, sensitive, and highly confidential SharePoint Online team sites.</span></span> <span data-ttu-id="90255-106">Pour plus d’informations sur ces trois niveaux de protection, consultez [Sécuriser des sites et des fichiers SharePoint Online](/security/office-365-security/secure-sharepoint-online-sites-and-files.md).</span><span class="sxs-lookup"><span data-stu-id="90255-106">For more information about these three tiers of protection, see [Secure SharePoint Online sites and files](/security/office-365-security/secure-sharepoint-online-sites-and-files.md).</span></span>
  
## <a name="how-this-works"></a><span data-ttu-id="90255-107">Procédure</span><span class="sxs-lookup"><span data-stu-id="90255-107">How this works</span></span>

1. <span data-ttu-id="90255-108">Créez les étiquettes de rétention de votre choix et publiez-les.</span><span class="sxs-lookup"><span data-stu-id="90255-108">Create the desired retention labels and publish these.</span></span> <span data-ttu-id="90255-109">La publication peut prendre jusqu’à 12 heures.</span><span class="sxs-lookup"><span data-stu-id="90255-109">It can take up to 12 hours for these to be published.</span></span>
2. <span data-ttu-id="90255-110">Pour les sites SharePoint souhaités, modifiez les paramètres de la bibliothèque de documents afin d’appliquer les étiquettes de rétention de votre choix aux éléments de la bibliothèque.</span><span class="sxs-lookup"><span data-stu-id="90255-110">For the desired SharePoint sites, edit the document library settings to apply the desired retention labels to items in the library.</span></span>
3. <span data-ttu-id="90255-111">Créez des stratégies DLP pour prendre des mesures en fonction des étiquettes de rétention.</span><span class="sxs-lookup"><span data-stu-id="90255-111">Create DLP policies to take action based on the retention labels.</span></span>

<span data-ttu-id="90255-112">Lorsque des utilisateurs ajoutent un document à la bibliothèque, celui-ci reçoit par défaut l’étiquette de rétention attribuée.</span><span class="sxs-lookup"><span data-stu-id="90255-112">When users add a document to the library, the document will receive the assigned retention label by default.</span></span> <span data-ttu-id="90255-113">Si nécessaire, les utilisateurs peuvent changer l’étiquette.</span><span class="sxs-lookup"><span data-stu-id="90255-113">Users can change the label, if needed.</span></span> <span data-ttu-id="90255-114">Lorsqu’un utilisateur partage un document en dehors de l’organisation, DLP vérifie si une étiquette est attribuée et prend les mesures qui s’imposent si une stratégie DLP correspond à l’étiquette.</span><span class="sxs-lookup"><span data-stu-id="90255-114">When a user shares a document outside the organization, DLP will check to see if a label is assigned and take action if a DLP policy matches the label.</span></span> <span data-ttu-id="90255-115">DLP recherche également les correspondances liées à d’autres stratégies, comme la protection des fichiers avec des numéros de carte de crédit si ce type de stratégie est configuré.</span><span class="sxs-lookup"><span data-stu-id="90255-115">DLP will look for other policy matches as well, such as protecting files with credit card numbers if this type of policy is configured.</span></span> 

## <a name="retention-labels-for-your-sharepoint-online-sites"></a><span data-ttu-id="90255-116">Étiquettes de rétention pour vos sites SharePoint Online</span><span class="sxs-lookup"><span data-stu-id="90255-116">Retention labels for your SharePoint Online sites</span></span>

<span data-ttu-id="90255-117">La création, puis l’attribution d’étiquettes de rétention à des sites d’équipe SharePoint Online se déroulent en trois phases.</span><span class="sxs-lookup"><span data-stu-id="90255-117">There are three phases to creating and then assigning retention labels to SharePoint Online team sites.</span></span>
  
### <a name="phase-1-determine-the-retention-label-names"></a><span data-ttu-id="90255-118">Phase 1 : Déterminer les noms des étiquettes de rétention</span><span class="sxs-lookup"><span data-stu-id="90255-118">Phase 1: Determine the retention label names</span></span>

<span data-ttu-id="90255-119">Au cours de cette phase, vous déterminez les noms de vos étiquettes de rétention pour les quatre niveaux de protection des informations appliqués aux sites d’équipe SharePoint Online.</span><span class="sxs-lookup"><span data-stu-id="90255-119">In this phase, you determine the names of your retention labels for the four levels of information protection applied to SharePoint Online team sites.</span></span> <span data-ttu-id="90255-120">Le tableau suivant répertorie les noms recommandés pour chaque niveau.</span><span class="sxs-lookup"><span data-stu-id="90255-120">The following table lists the recommended names for each level.</span></span>
  
|<span data-ttu-id="90255-121">**Niveau de protection du site d’équipe SharePoint Online**</span><span class="sxs-lookup"><span data-stu-id="90255-121">**SharePoint Online team site protection level**</span></span>|<span data-ttu-id="90255-122">**Nom de l’étiquette**</span><span class="sxs-lookup"><span data-stu-id="90255-122">**Label name**</span></span>|
|:-----|:-----|
|<span data-ttu-id="90255-123">Base de référence - Public</span><span class="sxs-lookup"><span data-stu-id="90255-123">Baseline-Public</span></span>  <br/> |<span data-ttu-id="90255-124">Public interne</span><span class="sxs-lookup"><span data-stu-id="90255-124">Internal public</span></span>  <br/> |
|<span data-ttu-id="90255-125">Base de référence - Privé</span><span class="sxs-lookup"><span data-stu-id="90255-125">Baseline-Private</span></span>  <br/> |<span data-ttu-id="90255-126">Private</span><span class="sxs-lookup"><span data-stu-id="90255-126">Private</span></span>  <br/> |
|<span data-ttu-id="90255-127">Sensible</span><span class="sxs-lookup"><span data-stu-id="90255-127">Sensitive</span></span>  <br/> |<span data-ttu-id="90255-128">Sensible</span><span class="sxs-lookup"><span data-stu-id="90255-128">Sensitive</span></span>  <br/> |
|<span data-ttu-id="90255-129">Hautement confidentiel</span><span class="sxs-lookup"><span data-stu-id="90255-129">Highly Confidential</span></span>  <br/> |<span data-ttu-id="90255-130">Hautement confidentiel</span><span class="sxs-lookup"><span data-stu-id="90255-130">Highly Confidential</span></span>  <br/> |
   
### <a name="phase-2-create-the-retention-labels"></a><span data-ttu-id="90255-131">Phase 2 : Créer les étiquettes de rétention</span><span class="sxs-lookup"><span data-stu-id="90255-131">Phase 2: Create the retention labels</span></span>

<span data-ttu-id="90255-132">Au cours de cette phase, vous créez puis vous publiez les étiquettes que vous avez déterminées pour les différents niveaux de protection des informations.</span><span class="sxs-lookup"><span data-stu-id="90255-132">In this phase, you create and then publish your determined labels for the different levels of information protection.</span></span>
  
1. <span data-ttu-id="90255-133">Connectez-vous au [portail de conformité Microsoft 365](https://compliance.microsoft.com) avec un compte disposant du rôle Administrateur de la sécurité ou Administrateur de la société.</span><span class="sxs-lookup"><span data-stu-id="90255-133">Sign in to the [Microsoft 365 compliance portal](https://compliance.microsoft.com) with an account that has the Security Administrator or Company Administrator role.</span></span>
    
2. <span data-ttu-id="90255-134">Sous l’onglet **Accueil - Conformité Microsoft 365** de votre navigateur, cliquez sur **Classifications > Étiquettes**.</span><span class="sxs-lookup"><span data-stu-id="90255-134">From the **Home - Microsoft 365 compliance** tab of your browser, click **Classifications > Labels**.</span></span>
    
3. <span data-ttu-id="90255-135">Cliquez sur **Étiquettes de rétention > Créer une étiquette**.</span><span class="sxs-lookup"><span data-stu-id="90255-135">Click **Retention labels > Create a label**.</span></span>
    
4. <span data-ttu-id="90255-136">Dans le volet **Nommer l’étiquette**, entrez le nom de l’étiquette ainsi qu’une description destinée aux administrateurs et aux utilisateurs, puis cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="90255-136">On the **Name your label** pane, type the name of the label and a description for admins and users, and then click **Next**.</span></span>

5. <span data-ttu-id="90255-137">Dans le volet **Descripteurs de plan de gestion de fichiers**, complétez les champs requis, puis cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="90255-137">On the **File plan descriptors** pane, fill in as needed, and then click **Next**.</span></span>
    
6. <span data-ttu-id="90255-138">Dans le volet **Paramètres d’étiquette**, si nécessaire, définissez **Rétention** sur **Activé** et configurez les paramètres de rétention.</span><span class="sxs-lookup"><span data-stu-id="90255-138">On the **Label settings** pane, if needed, set **Retention** to **On** and configure retention settings.</span></span> <span data-ttu-id="90255-139">Cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="90255-139">Click **Next**.</span></span>
    
7. <span data-ttu-id="90255-140">Dans le volet **Vérifier vos paramètres**, cliquez sur **Créer l’étiquette**.</span><span class="sxs-lookup"><span data-stu-id="90255-140">On the **Review your settings** pane, click **Create the label**.</span></span>
    
8. <span data-ttu-id="90255-141">Pour vos autres étiquettes, cliquez sur **Créer une étiquette** puis, si nécessaire, répétez les étapes 3 à 7.</span><span class="sxs-lookup"><span data-stu-id="90255-141">For your additional labels, click **Create a label**, and then repeat steps 3-7 as needed.</span></span>
    

### <a name="publish-your-new-labels"></a><span data-ttu-id="90255-142">Publier vos nouvelles étiquettes</span><span class="sxs-lookup"><span data-stu-id="90255-142">Publish your new labels</span></span>

<span data-ttu-id="90255-143">Procédez comme suit pour publier les nouvelles étiquettes de rétention.</span><span class="sxs-lookup"><span data-stu-id="90255-143">Next, use these steps to publish the new retention labels.</span></span>
  
1. <span data-ttu-id="90255-144">Depuis le volet **Étiquettes**, cliquez sur l’onglet **Étiquettes de rétention**, puis sur **Publier les étiquettes**.</span><span class="sxs-lookup"><span data-stu-id="90255-144">From the **Labels** pane, click the **Retention labels** tab, and then click **Publish labels**.</span></span>
    
2. <span data-ttu-id="90255-145">Dans le volet **Choisir les étiquettes à publier**, cliquez sur **Choisir les étiquettes à publier**.</span><span class="sxs-lookup"><span data-stu-id="90255-145">On the **Choose labels to publish** pane, click **Choose labels to publish**.</span></span>
    
3. <span data-ttu-id="90255-146">Dans le volet **Choisir des étiquettes**, cliquez sur **Ajouter**, sélectionnez les quatre étiquettes, puis cliquez à nouveau sur **Ajouter**.</span><span class="sxs-lookup"><span data-stu-id="90255-146">On the **Choose labels** pane, click **Add**, select all four labels, click **Add**.</span></span>
    
4. <span data-ttu-id="90255-147">Cliquez sur **Terminé**.</span><span class="sxs-lookup"><span data-stu-id="90255-147">Click **Done**.</span></span>
    
5. <span data-ttu-id="90255-148">Dans le volet **Choisir les étiquettes à publier**, cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="90255-148">On the **Choose labels to publish** pane, click **Next**.</span></span>
    
6. <span data-ttu-id="90255-149">Dans le volet **Choisir les emplacements**, cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="90255-149">On the **Choose locations** pane, click **Next**.</span></span>
    
7. <span data-ttu-id="90255-150">Dans le volet **Nom de votre stratégie**, entrez un nom pour désigner l’ensemble des étiquettes dans **Nom**, puis cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="90255-150">On the **Name your policy** pane, type a name for your set of labels in **Name**, and then click **Next**.</span></span>
    
8. <span data-ttu-id="90255-151">Dans le volet **Vérifier vos paramètres**, cliquez sur **Publier les étiquettes**, puis sur **Fermer**.</span><span class="sxs-lookup"><span data-stu-id="90255-151">On the **Review your settings** pane, click **Publish labels**, and then click **Close**.</span></span>

    
### <a name="phase-3-apply-the-retention-labels-to-your-sharepoint-online-sites"></a><span data-ttu-id="90255-152">Phase 3 : Appliquer les étiquettes de rétention à vos sites SharePoint Online</span><span class="sxs-lookup"><span data-stu-id="90255-152">Phase 3: Apply the retention labels to your SharePoint Online sites</span></span>

<span data-ttu-id="90255-153">Procédez comme suit pour appliquer les étiquettes de rétention aux dossiers de documents de vos sites d’équipe SharePoint Online.</span><span class="sxs-lookup"><span data-stu-id="90255-153">Use these steps to apply the retention labels to the documents folders of your SharePoint Online team sites.</span></span>
  
1. <span data-ttu-id="90255-154">Connectez-vous au [portail Office 365](https://www.office.com) et cliquez sur l’application **SharePoint**.</span><span class="sxs-lookup"><span data-stu-id="90255-154">Sign in to the [Office 365 portal](https://www.office.com), click the **SharePoint** app.</span></span>
    
2. <span data-ttu-id="90255-155">Sous le nouvel onglet **SharePoint** de votre navigateur, cliquez sur un site auquel vous devez attribuer une étiquette de rétention.</span><span class="sxs-lookup"><span data-stu-id="90255-155">On the new **SharePoint** tab in your browser, click a site that needs a retention label assigned.</span></span>
    
3. <span data-ttu-id="90255-156">Sous le nouvel onglet du Site SharePoint de votre navigateur, cliquez sur **Documents**.</span><span class="sxs-lookup"><span data-stu-id="90255-156">In the new SharePoint site tab of your browser, click **Documents**.</span></span>
    
4. <span data-ttu-id="90255-157">Cliquez sur l’icône des paramètres, puis cliquez sur **Paramètres de la bibliothèque**.</span><span class="sxs-lookup"><span data-stu-id="90255-157">Click the settings icon, and then click **Library settings**.</span></span>
    
5. <span data-ttu-id="90255-158">Sous **Autorisations et gestion**, cliquez sur **Appliquer l’étiquette aux éléments de cette bibliothèque**.</span><span class="sxs-lookup"><span data-stu-id="90255-158">Under **Permissions and Management**, click **Apply label to items in this library**.</span></span>
    
6. <span data-ttu-id="90255-159">Dans **Paramètres-Appliquer une étiquette**, sélectionnez l’étiquette de rétention qui convient, puis cliquez sur **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="90255-159">In **Settings-Apply Label**, select the appropriate retention label, and then click **Save**.</span></span>
    
7. <span data-ttu-id="90255-160">Fermez l’onglet du site SharePoint Online.</span><span class="sxs-lookup"><span data-stu-id="90255-160">Close the tab for the SharePoint Online site.</span></span>
    
8. <span data-ttu-id="90255-161">Répétez les étapes 2 à 8 pour attribuer des étiquettes de rétention à vos autres sites SharePoint Online.</span><span class="sxs-lookup"><span data-stu-id="90255-161">Repeat steps 2-8 to assign retention labels to your additional SharePoint Online sites.</span></span>
    
<span data-ttu-id="90255-162">Voici la configuration finale.</span><span class="sxs-lookup"><span data-stu-id="90255-162">Here is your resulting configuration.</span></span>
  
![Étiquettes de rétention des quatre types de sites d’équipe SharePoint Online.](media/e0a4fdd2-1c30-4d93-8af4-a6f0c6c29966.png)
  
## <a name="dlp-policies-for-your-sharepoint-online-sites"></a><span data-ttu-id="90255-164">Stratégies de protection contre la perte de données pour vos sites SharePoint Online</span><span class="sxs-lookup"><span data-stu-id="90255-164">DLP policies for your SharePoint Online sites</span></span>

<span data-ttu-id="90255-165">Suivez ces étapes pour configurer une stratégie DLP qui avertit les utilisateurs lorsqu’ils partagent un document sur un site d’équipe sensible SharePoint Online externe à l’organisation.</span><span class="sxs-lookup"><span data-stu-id="90255-165">Use these steps to configure a DLP policy that notifies users when they share a document on a SharePoint Online sensitive team site outside the organization.</span></span>

1. <span data-ttu-id="90255-166">Connectez-vous au [portail de conformité Microsoft 365](https://compliance.microsoft.com/) avec un compte disposant du rôle Administrateur de la sécurité ou Administrateur de la société.</span><span class="sxs-lookup"><span data-stu-id="90255-166">Sign in to the [Microsoft 365 compliance portal](https://compliance.microsoft.com/) with an account that has the Security Administrator or Company Administrator role.</span></span>
    
2. <span data-ttu-id="90255-167">Sous le nouvel onglet **Conformité Microsoft 365** de votre navigateur, cliquez sur **Stratégie > Protection contre la perte de données**.</span><span class="sxs-lookup"><span data-stu-id="90255-167">On the new **Microsoft 365 compliance** tab in your browser, click **Policies > Data loss prevention**.</span></span>
    
3. <span data-ttu-id="90255-168">Dans le volet **Accueil > Protection contre la perte de données**, cliquez sur **Créer une stratégie**.</span><span class="sxs-lookup"><span data-stu-id="90255-168">In the **Home > Data loss prevention** pane, click **Create a policy**.</span></span>
    
4. <span data-ttu-id="90255-169">Dans le volet **Commencez en utilisant un modèle ou créez une stratégie personnalisée**, cliquez sur **Personnalisé**, puis sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="90255-169">In the **Start with a template or create a custom policy** pane, click **Custom**, and then click **Next**.</span></span>
    
5. <span data-ttu-id="90255-170">Dans le volet **Nom de votre stratégie**, entrez le nom de la stratégie DLP sensible dans **Nom**, puis cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="90255-170">In the **Name your policy** pane, type the name for the sensitive level DLP policy in **Name**, and then click **Next**.</span></span>
    
6. <span data-ttu-id="90255-171">Dans le volet **Choisir les emplacements**, cliquez sur **Me laisser choisir des emplacements spécifiques**, puis sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="90255-171">In the **Choose locations** pane, click **Let me choose specific locations**, and then click **Next**.</span></span>
    
7. <span data-ttu-id="90255-172">Dans la liste des emplacements, désactivez les emplacements **Courrier Exchange**, **Comptes OneDrive** et **Messages de conversations et de canaux Teams**, puis cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="90255-172">In the list of locations, disable the **Exchange email**, **OneDrive accounts**, and **Teams chat and channel messages** locations, and then click **Next**.</span></span>
    
8. <span data-ttu-id="90255-173">Dans le volet **Personnalisez le type de contenu que vous voulez protéger**, cliquez sur **Modifier**.</span><span class="sxs-lookup"><span data-stu-id="90255-173">In the **Customize the type of content you want to protect** pane, click **Edit**.</span></span>
    
9. <span data-ttu-id="90255-174">Dans le volet **Choisissez les types de contenu à protéger**, cliquez sur **Ajouter** dans la zone déroulante, puis sélectionnez **Étiquettes de rétention**.</span><span class="sxs-lookup"><span data-stu-id="90255-174">In the **Choose the types of content to protect** pane, click **Add** in the drop-down box, and then click **Retention labels**.</span></span>
    
10. <span data-ttu-id="90255-175">Dans le volet **Étiquettes de rétention**, cliquez sur **Ajouter**, sélectionnez l’étiquette **Sensible**, puis cliquez sur **Ajouter** et sur **Terminé**.</span><span class="sxs-lookup"><span data-stu-id="90255-175">In the **Retention labels** pane, click **Add**, select the **Sensitive** label, click **Add**, and then click **Done**.</span></span>
    
11. <span data-ttu-id="90255-176">Dans le volet **Choisir les types de contenu à protéger**, cliquez sur **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="90255-176">In the **Choose the types of content to protect** pane, click **Save**.</span></span>
    
12. <span data-ttu-id="90255-177">Dans le volet **Personnaliser les types d’informations sensibles que vous souhaitez protéger**, cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="90255-177">In the **Customize the type of content you want to protect** pane, click **Next**.</span></span>

13. <span data-ttu-id="90255-178">Dans le volet **Que faire en cas de détection d’informations sensibles ?**, cliquez sur **Personnaliser l’info-bulle et l’e-mail**.</span><span class="sxs-lookup"><span data-stu-id="90255-178">In the **What do you want to do if we detect sensitive info?** pane, click **Customize the tip and email**.</span></span>
    
14. <span data-ttu-id="90255-179">Dans le volet **Personnaliser les conseils et les notifications par e-mail de la stratégie**, cliquez sur **Personnaliser le texte de l’info-bulle de la stratégie**.</span><span class="sxs-lookup"><span data-stu-id="90255-179">In the **Customize policy tips and email notifications** pane, click **Customize the policy tip text**.</span></span>
    
15. <span data-ttu-id="90255-180">Dans la zone de texte, saisissez ou collez l’un des conseils suivants, selon si vous avez implémenté Azure Information Protection pour protéger les fichiers hautement confidentiels :</span><span class="sxs-lookup"><span data-stu-id="90255-180">In the text box, type or paste in one of the following tips, depending on if you implemented Azure Information Protection to protect highly confidential files:</span></span>
    
  - <span data-ttu-id="90255-p106">Pour partager un fichier avec un utilisateur extérieur à l’organisation, téléchargez-le et ouvrez-le. Cliquez sur Fichier > Protéger le document > Chiffrer avec mot de passe, puis indiquez un mot de passe fort. Envoyez le mot de passe par e-mail ou un autre moyen de communication.</span><span class="sxs-lookup"><span data-stu-id="90255-p106">To share with a user outside the organization, download the file and then open it. Click File, then Protect Document, and then Encrypt with Password, and then specify a strong password. Send the password in a separate email or other means of communication.</span></span>
  - <span data-ttu-id="90255-p107">Les fichiers hautement confidentiels sont protégés par chiffrement. Seuls les utilisateurs externes qui y ont été autorisés par votre service informatique peuvent lire ces fichiers.</span><span class="sxs-lookup"><span data-stu-id="90255-p107">Highly confidential files are protected with encryption. Only external users who are granted permissions to these files by your IT department can read them.</span></span>
    
    <span data-ttu-id="90255-186">Vous pouvez également saisir ou coller votre propre conseil de stratégie pour expliquer aux utilisateurs comment partager un fichier en dehors de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="90255-186">Alternately, type or paste in your own policy tip that instructs users on how to share a file outside your organization.</span></span>
    
16. <span data-ttu-id="90255-187">Cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="90255-187">Click **OK**.</span></span>
    
17. <span data-ttu-id="90255-188">Dans le volet Office **Que faire en cas de détection d’informations sensibles ?**, cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="90255-188">In the **What do you want to do if we detect sensitive info?** pane, click **Next**.</span></span>
    
18. <span data-ttu-id="90255-189">Dans le volet **Voulez-vous activer la stratégie ou d’abord effectuer des tests ?**, cliquez sur **Oui, l’activer maintenant**, puis cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="90255-189">In the **Do you want to turn on the policy or test things out first?** pane, click **Yes, turn it on right away**, and then click **Next**.</span></span>
    
19. <span data-ttu-id="90255-190">Dans le volet **Vérifier vos paramètres**, cliquez sur **Créer**, puis sur **Fermer**.</span><span class="sxs-lookup"><span data-stu-id="90255-190">In the **Review your settings** pane, click **Create**, and then click **Close**.</span></span>
    
<span data-ttu-id="90255-191">Voici le résultat de votre configuration pour les sites d’équipe SharePoint Online sensibles.</span><span class="sxs-lookup"><span data-stu-id="90255-191">Here is your resulting configuration for sensitive SharePoint Online team sites.</span></span>
  
![Stratégie DLP pour un site d’équipe SharePoint Online isolé utilisant l’étiquette de rétention Sensible](media/2ff4cc53-87a8-43e3-b637-3068d88409f3.png)
  
<span data-ttu-id="90255-193">Utilisez ces étapes pour configurer une stratégie de protection contre la perte de données qui bloque les utilisateurs quand ils partagent un document sur un site d’équipe SharePoint Online hautement confidentiel à l’extérieur de l’organisation.</span><span class="sxs-lookup"><span data-stu-id="90255-193">Next, use these steps to configure a DLP policy that blocks users when they share a document on a SharePoint Online highly confidential team site outside the organization.</span></span>
  
1. <span data-ttu-id="90255-194">Sous le nouvel onglet **Conformité Microsoft 365** de votre navigateur, cliquez sur **Stratégie > Protection contre la perte de données**.</span><span class="sxs-lookup"><span data-stu-id="90255-194">On the new **Microsoft 365 compliance** tab in your browser, click **Policies > Data loss prevention**.</span></span>
    
2. <span data-ttu-id="90255-195">Dans le volet **Protection contre la perte de données**, cliquez sur **Créer une stratégie**.</span><span class="sxs-lookup"><span data-stu-id="90255-195">In the **Data loss prevention** pane, click **Create a policy**.</span></span>
    
3. <span data-ttu-id="90255-196">Dans le volet **Utiliser un modèle ou créer une stratégie personnalisée**, cliquez sur **Personnalisé**, puis sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="90255-196">In the **Start with a template or create a custom policy** pane, click **Custom**, and then click **Next**.</span></span>
    
4. <span data-ttu-id="90255-197">Dans le volet **Nom de votre stratégie**, entrez le nom de la stratégie DLP hautement sensible dans **Nom**, puis cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="90255-197">In the **Name your policy** pane, type the name for the highly sensitive level DLP policy in **Name**, and then click **Next**.</span></span>
    
5. <span data-ttu-id="90255-198">Dans le volet **Choisir des emplacements**, cliquez sur **Me laisser choisir des emplacements spécifiques**, puis cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="90255-198">In the **Choose locations** pane, click **Let me choose specific locations**, and then click **Next**.</span></span>
    
6. <span data-ttu-id="90255-199">Dans la liste des emplacements, désactivez les emplacements **Courrier Exchange**, **Comptes OneDrive** et **Messages de conversations et de canaux Teams**, puis cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="90255-199">In the list of locations, disable the **Exchange email**, **OneDrive accounts**, and **Teams chat and channel messages** locations, and then click **Next**.</span></span>
    
7. <span data-ttu-id="90255-200">Dans le volet **Personnalisez les types d’informations sensibles que vous voulez protéger**, cliquez sur **Modifier**.</span><span class="sxs-lookup"><span data-stu-id="90255-200">In the **Customize the types of sensitive info you want to protect** pane, click **Edit**.</span></span>
    
8. <span data-ttu-id="90255-201">Dans le volet **Choisissez les types de contenu à protéger**, cliquez sur **Ajouter** dans la zone déroulante, puis sélectionnez **Étiquettes de rétention**.</span><span class="sxs-lookup"><span data-stu-id="90255-201">In the **Choose the types of content to protect** pane, click **Add** in the drop-down box, and then click **Retention labels**.</span></span>
    
9. <span data-ttu-id="90255-202">Dans le volet **Étiquettes de rétention**, cliquez sur **Ajouter**, sélectionnez l’étiquette **Hautement confidentiel**, puis cliquez sur **Ajouter** et sur **Terminé**.</span><span class="sxs-lookup"><span data-stu-id="90255-202">In the **Retention labels** pane, click **Add**, select the **Highly Confidential** label, click **Add**, and then click **Done**.</span></span>
    
10. <span data-ttu-id="90255-203">Dans le volet **Choisir les types de contenu à protéger**, cliquez sur **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="90255-203">In the **Choose the types of content to protect** pane, click **Save**.</span></span>
    
12. <span data-ttu-id="90255-204">Dans le volet **Personnaliser les types d’informations sensibles que vous voulez protéger**, cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="90255-204">In the **Customize the types of sensitive info you want to protect** pane, click **Next**.</span></span>
    
13. <span data-ttu-id="90255-205">Dans le volet **Que voulez-vous faire si nous détectons des informations confidentielles ?**, cliquez sur **Personnaliser l’info-bulle et la messagerie électronique**.</span><span class="sxs-lookup"><span data-stu-id="90255-205">In the **What do you want to do if we detect sensitive info?** pane, click **Customize the tip and email**.</span></span>
    
14. <span data-ttu-id="90255-206">Dans le volet **Personnaliser les conseils et les notifications par e-mail de la stratégie**, cliquez sur **Personnaliser le texte de l’info-bulle de la stratégie**.</span><span class="sxs-lookup"><span data-stu-id="90255-206">In the **Customize policy tips and email notifications** pane, click **Customize the policy tip text**.</span></span>
    
15. <span data-ttu-id="90255-207">Dans la zone de texte, tapez ou collez ce qui suit :</span><span class="sxs-lookup"><span data-stu-id="90255-207">In the text box, type or paste in the following:</span></span>
    
  - <span data-ttu-id="90255-p108">Pour partager un fichier avec un utilisateur extérieur à l’organisation, téléchargez-le et ouvrez-le. Cliquez sur Fichier > Protéger le document > Chiffrer avec mot de passe, puis indiquez un mot de passe fort. Envoyez le mot de passe par e-mail ou un autre moyen de communication.</span><span class="sxs-lookup"><span data-stu-id="90255-p108">To share with a user outside the organization, download the file and then open it. Click File, then Protect Document, and then Encrypt with Password, and then specify a strong password. Send the password in a separate email or other means of communication.</span></span>
    
    <span data-ttu-id="90255-211">Vous pouvez également saisir ou coller votre propre conseil de stratégie pour expliquer aux utilisateurs comment partager un fichier en dehors de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="90255-211">Alternately, type or paste in your own policy tip that instructs users on how to share a file outside your organization.</span></span>
    
16. <span data-ttu-id="90255-212">Cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="90255-212">Click **OK**.</span></span>
    
17. <span data-ttu-id="90255-213">Dans le volet **Que faire en cas de détection d’informations sensibles ?**, sous **Détecter les cas où une quantité spécifique d’informations sensibles sont partagées en même temps**, cliquez sur **Restreindre l’accès ou chiffrer le contenu**, puis cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="90255-213">In the **What do you want to do if we detect sensitive info?** pane, under **Detect when a specific amount of sensitive info is being shared at one time**, click **Restrict access or encrypt the content**, and then click **Next**.</span></span>
    
18. <span data-ttu-id="90255-214">Dans le volet **Voulez-vous activer la stratégie ou d’abord effectuer des tests ?**, cliquez sur **Oui, l’activer maintenant**, puis cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="90255-214">In the **Do you want to turn on the policy or test things out first?** pane, click **Yes, turn it on right away**, and then click **Next**.</span></span>
    
19. <span data-ttu-id="90255-215">Dans le volet **Vérifier vos paramètres**, cliquez sur **Créer**, puis sur **Fermer**.</span><span class="sxs-lookup"><span data-stu-id="90255-215">In the **Review your settings** pane, click **Create**, and then click **Close**.</span></span>
    
<span data-ttu-id="90255-216">Voici le résultat de votre configuration pour les sites d’équipe SharePoint Online hautement confidentiels.</span><span class="sxs-lookup"><span data-stu-id="90255-216">Here is your resulting configuration for high confidentiality SharePoint Online team sites.</span></span>
  
![Stratégie DLP pour un site d’équipe SharePoint Online isolé utilisant l’étiquette de rétention Hautement confidentiel](media/f705d3d0-23c9-4333-8b70-ad3b91f835ea.png)
  
## <a name="next-step"></a><span data-ttu-id="90255-218">Étape suivante</span><span class="sxs-lookup"><span data-stu-id="90255-218">Next step</span></span>

[<span data-ttu-id="90255-219">Protéger les fichiers SharePoint Online avec Azure Information Protection</span><span class="sxs-lookup"><span data-stu-id="90255-219">Protect SharePoint Online files with Azure Information Protection</span></span>](protect-sharepoint-online-files-with-azure-information-protection.md)
    
## <a name="see-also"></a><span data-ttu-id="90255-220">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="90255-220">See Also</span></span>

[<span data-ttu-id="90255-221">Sécuriser les fichiers et sites SharePoint Online</span><span class="sxs-lookup"><span data-stu-id="90255-221">Secure SharePoint Online sites and files</span></span>](../security/office-365-security/secure-sharepoint-online-sites-and-files.md)
  
[<span data-ttu-id="90255-222">Conseils de sécurité Microsoft pour les campagnes électorales, les organisations à but non lucratif et d’autres organisations flexibles</span><span class="sxs-lookup"><span data-stu-id="90255-222">Microsoft Security Guidance for Political Campaigns, Nonprofits, and Other Agile Organizations</span></span>](../security/office-365-security/microsoft-security-guidance-for-political-campaigns-nonprofits-and-other-agile-o.md)
  
[<span data-ttu-id="90255-223">Adoption du cloud et solutions hybrides</span><span class="sxs-lookup"><span data-stu-id="90255-223">Cloud adoption and hybrid solutions</span></span>](https://docs.microsoft.com/office365/enterprise/cloud-adoption-and-hybrid-solutions)


