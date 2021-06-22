---
title: 'Création de sites d’équipe : environnement de développement dans le cadre d’une campagne électorale'
f1.keywords:
- NOCSH
ms.author: josephd
author: JoeDavies-MSFT
manager: laurawi
ms.date: 05/21/2018
audience: ITPro
ms.topic: article
ms.collection:
- Ent_O365
- Strat_O365_Enterprise
localization_priority: Priority
search.appverid:
- MET150
ms.custom: seo-marvel-apr2020
ms.assetid: c2112ce8-1c4b-424f-b200-59e161db2d21
description: 'Résumé : Créez des sites d’équipe SharePoint Online publics, privés, sensibles et hautement confidentiels dans votre environnement de développement/test dans le cadre d’une campagne électorale.'
ms.technology: mdo
ms.prod: m365-security
ms.openlocfilehash: fcba6e2f3939115d6dfbaae80d322246bdeadee9
ms.sourcegitcommit: c70067b4ef9c6f8f04aca68c35bb5141857c4e4b
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/19/2021
ms.locfileid: "53029896"
---
# <a name="create-team-sites-in-a-political-campaign-devtest-environment"></a><span data-ttu-id="cf482-103">Création de sites d’équipe dans un environnement de développement/test dans le cadre d’une campagne électorale</span><span class="sxs-lookup"><span data-stu-id="cf482-103">Create team sites in a political campaign dev/test environment</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../includes/microsoft-defender-for-office.md)]

<span data-ttu-id="cf482-104">**S’applique à**</span><span class="sxs-lookup"><span data-stu-id="cf482-104">**Applies to**</span></span>

- [<span data-ttu-id="cf482-105">Microsoft Defender pour Office 365 Plan 2</span><span class="sxs-lookup"><span data-stu-id="cf482-105">Microsoft Defender for Office 365 plan 2</span></span>](defender-for-office-365.md)

 <span data-ttu-id="cf482-106">**Résumé :** Créez des sites d’équipe SharePoint Online publics, privés, sensibles et hautement confidentiels dans votre environnement de développement/test dans le cadre d’une campagne électorale.</span><span class="sxs-lookup"><span data-stu-id="cf482-106">**Summary:** Create public, private, sensitive, and highly confidential SharePoint Online team sites in your political campaign dev/test environment.</span></span>

<span data-ttu-id="cf482-p101">Utilisez les instructions fournies dans cet article pour créer un environnement de développement/test qui inclut les quatre différents types de sites d’équipe SharePoint Online pour la solution des [conseils de sécurité Microsoft pour les campagnes électorales, les organisations à but non lucratif et autres organisations souples](microsoft-security-guidance-for-political-campaigns-nonprofits-and-other-agile-o.md). Ces sites sont décrits en détail dans la Rubrique 10 intitulée **SharePoint et OneDrive Entreprise**.</span><span class="sxs-lookup"><span data-stu-id="cf482-p101">Use the instructions in this article to create a dev/test environment that includes the four different types of SharePoint Online team sites for the [Microsoft Security Guidance for Political Campaigns, Nonprofits, and Other Agile Organizations](microsoft-security-guidance-for-political-campaigns-nonprofits-and-other-agile-o.md) solution. These sites are described in detail on Topic 10, titled **SharePoint and OneDrive for Business**.</span></span>

## <a name="phase-1-create-your-political-campaign-devtest-environment"></a><span data-ttu-id="cf482-109">Phase 1 : Création d’un environnement de développement/test dans le cadre d’une campagne électorale</span><span class="sxs-lookup"><span data-stu-id="cf482-109">Phase 1: Create your political campaign dev/test environment</span></span>

<span data-ttu-id="cf482-110">Tout d’abord, suivez les instructions de [Configurer de groupes et d’utilisateurs pour un environnement de développement/test pour une campagne électorale](configure-groups-and-users-for-a-political-campaign-dev-test-environment.md) pour créer vos abonnements, utilisateurs et groupes.</span><span class="sxs-lookup"><span data-stu-id="cf482-110">First, follow the instructions in [Configure groups and users for a political campaign dev/test environment](configure-groups-and-users-for-a-political-campaign-dev-test-environment.md) to create your subscriptions, users, and groups.</span></span>

## <a name="phase-2-create-labels"></a><span data-ttu-id="cf482-111">Phase 2 : Création d’étiquettes</span><span class="sxs-lookup"><span data-stu-id="cf482-111">Phase 2: Create labels</span></span>

<span data-ttu-id="cf482-112">Dans cette phase, vous allez créer les étiquettes correspondant aux différents niveaux de sécurité pour les dossiers de document du site d’équipe SharePoint Online.</span><span class="sxs-lookup"><span data-stu-id="cf482-112">In this phase, you create the labels for the different levels of security for SharePoint Online team site document folders.</span></span>

1. <span data-ttu-id="cf482-p102">Si nécessaire, connectez-vous au centre d'administration Microsoft 365 (<https://admin.microsoft.com>) avec les informations d’identification du compte d’administrateur général de votre abonnement d’essai. Pour obtenir de l’aide, consultez [Où se connecter à Microsoft 365](https://support.microsoft.com/office/e9eb7d51-5430-4929-91ab-6157c5a050b4).</span><span class="sxs-lookup"><span data-stu-id="cf482-p102">If needed, sign in to the Microsoft 365 admin center (<https://admin.microsoft.com>) with the credentials of the global administrator account of your trial subscription. For help, see [Where to sign in to Microsoft 365](https://support.microsoft.com/office/e9eb7d51-5430-4929-91ab-6157c5a050b4).</span></span>

2. <span data-ttu-id="cf482-115">Dans la page d’**Accueil** où vous commencez, cliquez sur **Afficher tous**.</span><span class="sxs-lookup"><span data-stu-id="cf482-115">From the **Home** page where you start, click **Show all**.</span></span> <span data-ttu-id="cf482-116">Dans la section **Centres d’administration** qui s’affiche, cliquez sur **Conformité**.</span><span class="sxs-lookup"><span data-stu-id="cf482-116">In the **Admin centers** section that appears, click **Compliance**.</span></span>

3. <span data-ttu-id="cf482-117">Dans la page d’**Accueil** du Centre de conformité Microsoft 365, accédez à la section **Solutions**\> **Protection des informations**.</span><span class="sxs-lookup"><span data-stu-id="cf482-117">From the **Home** page of the Microsoft 365 compliance center, go to the **Solutions** section \> **Information protection**.</span></span> <span data-ttu-id="cf482-118">Pour accéder directement à la page **Information Protection**, utilisez <https://compliance.microsoft.com//informationprotection>.</span><span class="sxs-lookup"><span data-stu-id="cf482-118">To go directly to the **Information protection** page, use <https://compliance.microsoft.com//informationprotection>.</span></span>

4. <span data-ttu-id="cf482-119">Dans la page **Protection des informations**, vérifiez que la balise **Étiquette est sélectionnée**, puis cliquez sur ![Créer une icône d’étiquette](../../media/m365-cc-sc-create-icon.png) **Créer une étiquette**.</span><span class="sxs-lookup"><span data-stu-id="cf482-119">On the **Information protection** page, verify that the **Label** tag is selected, and then click  ![Create a label icon](../../media/m365-cc-sc-create-icon.png) **Create a label**.</span></span>

5. <span data-ttu-id="cf482-120">L’Assistant **nouvelle étiquette de confidentialité** s’ouvre.</span><span class="sxs-lookup"><span data-stu-id="cf482-120">The **New sensitivity label** wizard opens.</span></span> <span data-ttu-id="cf482-121">À l’étape **Nom et description**, entrez les valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="cf482-121">On the **Name & description** step, enter the following values:</span></span>
   - <span data-ttu-id="cf482-122">**Nom** : tapez **Interne**.</span><span class="sxs-lookup"><span data-stu-id="cf482-122">**Name**: Type **Internal**.</span></span>
   - <span data-ttu-id="cf482-123">**Nom d’affichage**</span><span class="sxs-lookup"><span data-stu-id="cf482-123">**Display name**</span></span>
   - <span data-ttu-id="cf482-124">**Description pour les utilisateurs**</span><span class="sxs-lookup"><span data-stu-id="cf482-124">**Description for users**</span></span>

   <span data-ttu-id="cf482-125">Lorsque vous avez terminé, cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="cf482-125">When you're finished, click **Next**.</span></span>

6. <span data-ttu-id="cf482-126">Dans le volet **Paramètres de l’étiquette**, cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="cf482-126">On the **Label settings** pane, click **Next**.</span></span>

7. <span data-ttu-id="cf482-127">Dans le volet **Vérifier vos paramètres**, cliquez sur **Créer cette étiquette**, puis cliquez sur **Fermer**.</span><span class="sxs-lookup"><span data-stu-id="cf482-127">On the **Review your settings** pane, click **Create this label**, and then click **Close**.</span></span>

8. <span data-ttu-id="cf482-128">Répétez les étapes 5 à 8 pour les autres étiquettes suivantes :</span><span class="sxs-lookup"><span data-stu-id="cf482-128">Repeat steps 5-8 for these additional labels:</span></span>

   - <span data-ttu-id="cf482-129">Privé</span><span class="sxs-lookup"><span data-stu-id="cf482-129">Private</span></span>
   - <span data-ttu-id="cf482-130">Sensible</span><span class="sxs-lookup"><span data-stu-id="cf482-130">Sensitive</span></span>
   - <span data-ttu-id="cf482-131">Hautement confidentiel</span><span class="sxs-lookup"><span data-stu-id="cf482-131">Highly Confidential</span></span>

9. <span data-ttu-id="cf482-132">Dans le volet **Accueil > Étiquettes**, cliquez sur **Publier des étiquettes**.</span><span class="sxs-lookup"><span data-stu-id="cf482-132">From the **Home > Labels** pane, click **Publish labels**.</span></span>

10. <span data-ttu-id="cf482-133">Dans le volet **Choisir les étiquettes à publier**, cliquez sur **Choisir les étiquettes à publier**.</span><span class="sxs-lookup"><span data-stu-id="cf482-133">On the **Choose labels to publish** pane, click **Choose labels to publish**.</span></span>

11. <span data-ttu-id="cf482-134">Dans le volet **Choisir des étiquettes**, cliquez sur **Ajouter** et sélectionnez les quatre étiquettes.</span><span class="sxs-lookup"><span data-stu-id="cf482-134">On the **Choose labels** pane, click **Add** and select all four labels.</span></span>

12. <span data-ttu-id="cf482-135">Cliquez sur **Terminé**.</span><span class="sxs-lookup"><span data-stu-id="cf482-135">Click **Done**.</span></span>

13. <span data-ttu-id="cf482-136">Dans le volet **Choisir les étiquettes à publier**, cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="cf482-136">On the **Choose labels to publish** pane, click **Next**.</span></span>

14. <span data-ttu-id="cf482-137">Dans le volet **Choisir les emplacements**, cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="cf482-137">On the **Choose locations** pane, click **Next**.</span></span>

15. <span data-ttu-id="cf482-138">Dans le volet **Nom de votre stratégie**, saisissez **Campagne** dans **Nom**, puis cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="cf482-138">On the **Name your policy** pane, type **Campaign** in **Name**, and then click **Next**.</span></span>

16. <span data-ttu-id="cf482-139">Dans le volet **Vérifier vos paramètres**, cliquez sur **Publier les étiquettes**, puis cliquez sur **Fermer**.</span><span class="sxs-lookup"><span data-stu-id="cf482-139">On the **Review your settings** pane, click **Publish labels**, and then click **Close**.</span></span>

## <a name="phase-3-create-your-sharepoint-online-team-sites"></a><span data-ttu-id="cf482-140">Phase 3 : Créer vos sites d’équipe SharePoint Online</span><span class="sxs-lookup"><span data-stu-id="cf482-140">Phase 3: Create your SharePoint Online team sites</span></span>

<span data-ttu-id="cf482-141">Lors de cette phase, vous allez créer et configurer des sites d’équipe SharePoint Online pour votre campagne électorale correspondant aux quatre types de sites d’équipe SharePoint Online.</span><span class="sxs-lookup"><span data-stu-id="cf482-141">In this phase, you create and configure SharePoint Online team sites for your political campaign corresponding to the four types of SharePoint Online team sites.</span></span>

### <a name="campaign-wide-team-site"></a><span data-ttu-id="cf482-142">Site d’équipe de la campagne</span><span class="sxs-lookup"><span data-stu-id="cf482-142">Campaign wide team site</span></span>

<span data-ttu-id="cf482-143">Pour créer une base de référence de site d’équipe SharePoint Online public, procédez comme suit :</span><span class="sxs-lookup"><span data-stu-id="cf482-143">To create a baseline public SharePoint Online team site, do the following:</span></span>

1. <span data-ttu-id="cf482-144">Si nécessaire, utilisez un navigateur de votre ordinateur local et connectez-vous au centre d’administration (<https://admin.microsoft.com>) à l’aide de votre compte d’administrateur général.</span><span class="sxs-lookup"><span data-stu-id="cf482-144">If needed, use a browser on your local computer and sign in to the admin center (<https://admin.microsoft.com>) using your global administrator account.</span></span>

2. <span data-ttu-id="cf482-145">Dans la liste des vignettes, cliquez sur **SharePoint**.</span><span class="sxs-lookup"><span data-stu-id="cf482-145">In the list of tiles, click **SharePoint**.</span></span>

3. <span data-ttu-id="cf482-146">Sous le nouvel onglet **SharePoint** de votre navigateur, cliquez sur **+ Créer un site**.</span><span class="sxs-lookup"><span data-stu-id="cf482-146">On the new **SharePoint** tab in your browser, click **+ Create site**.</span></span>

4. <span data-ttu-id="cf482-147">Dans la page **Créer un site**, cliquez sur **Site d’équipe**.</span><span class="sxs-lookup"><span data-stu-id="cf482-147">On the **Create a site** page, click **Team site**.</span></span>

5. <span data-ttu-id="cf482-148">Dans **Nom du site**, saisissez **Campagne**.</span><span class="sxs-lookup"><span data-stu-id="cf482-148">In **Site name**, type **Campaign wide**.</span></span>

6. <span data-ttu-id="cf482-149">Dans **Description du site d’équipe**, saisissez **Site SharePoint pour l’ensemble de la campagne**.</span><span class="sxs-lookup"><span data-stu-id="cf482-149">In **Team site description**, type **SharePoint site for the entire campaign**.</span></span>

7. <span data-ttu-id="cf482-150">Dans **Paramètres de confidentialité**, sélectionnez **Public - tout le monde dans l’organisation peut accéder à ce site**, puis cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="cf482-150">In **Privacy settings**, select **Public - anyone in the organization can access this site**, and then click **Next**.</span></span>

8. <span data-ttu-id="cf482-151">Dans le volet **Qui voulez-vous ajouter ?**, cliquez sur **Terminer**.</span><span class="sxs-lookup"><span data-stu-id="cf482-151">On the **Who do you want to add?** pane, click **Finish**.</span></span>

<span data-ttu-id="cf482-152">Ensuite, configurez le dossier de documents du site d’équipe de la campagne pour l’étiquette Interne.</span><span class="sxs-lookup"><span data-stu-id="cf482-152">Next, configure the documents folder of the Campaign wide team site for the Internal label.</span></span>

1. <span data-ttu-id="cf482-153">Dans l’onglet **Campagne - Accueil** de votre navigateur, cliquez sur **Documents**.</span><span class="sxs-lookup"><span data-stu-id="cf482-153">In the **Campaign wide-Home** tab of your browser, click **Documents**.</span></span>

2. <span data-ttu-id="cf482-154">Cliquez sur l’icône des paramètres, puis cliquez sur **Paramètres de la bibliothèque**.</span><span class="sxs-lookup"><span data-stu-id="cf482-154">Click the settings icon, and then click **Library settings**.</span></span>

3. <span data-ttu-id="cf482-155">Sous **Autorisations et gestion**, cliquez sur **Appliquer l’étiquette aux éléments de cette bibliothèque**.</span><span class="sxs-lookup"><span data-stu-id="cf482-155">Under **Permissions and Management**, click **Apply label to items in this library**.</span></span>

4. <span data-ttu-id="cf482-156">Dans **Paramètres - Appliquer l’étiquette**, sélectionnez **Interne**, puis cliquez sur **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="cf482-156">In **Settings-Apply Label**, select **Internal**, and then click **Save**.</span></span>

### <a name="campaign-project-1-team-site"></a><span data-ttu-id="cf482-157">Site d’équipe 1 du projet Campagne</span><span class="sxs-lookup"><span data-stu-id="cf482-157">Campaign project 1 team site</span></span>

<span data-ttu-id="cf482-158">Pour créer un site d’équipe SharePoint Online privé de référence pour un projet dans la campagne, procédez comme suit :</span><span class="sxs-lookup"><span data-stu-id="cf482-158">To create a baseline private SharePoint Online team site for a project within the campaign, do the following:</span></span>

1. <span data-ttu-id="cf482-159">Si nécessaire, utilisez un navigateur de votre ordinateur local et connectez-vous au centre d’administration (<https://admin.microsoft.com>) à l’aide de votre compte d’administrateur général.</span><span class="sxs-lookup"><span data-stu-id="cf482-159">If needed, use a browser on your local computer and sign in to the admin center (<https://admin.microsoft.com>) using your global administrator account.</span></span>

2. <span data-ttu-id="cf482-160">Dans la liste des vignettes, cliquez sur **SharePoint**.</span><span class="sxs-lookup"><span data-stu-id="cf482-160">In the list of tiles, click **SharePoint**.</span></span>

3. <span data-ttu-id="cf482-161">Sous le nouvel onglet **SharePoint** de votre navigateur, cliquez sur **+ Créer un site**.</span><span class="sxs-lookup"><span data-stu-id="cf482-161">On the new **SharePoint** tab in your browser, click **+ Create site**.</span></span>

4. <span data-ttu-id="cf482-162">Dans la page **Créer un site**, cliquez sur **Site d’équipe**.</span><span class="sxs-lookup"><span data-stu-id="cf482-162">On the **Create a site** page, click **Team site**.</span></span>

5. <span data-ttu-id="cf482-163">Dans **Nom du site**, saisissez **Projet de campagne 1**.</span><span class="sxs-lookup"><span data-stu-id="cf482-163">In **Site name**, type **Campaign project 1**.</span></span>

6. <span data-ttu-id="cf482-164">Dans **Description du site d’équipe**, saisissez **Site SharePoint pour le projet de campagne 1**.</span><span class="sxs-lookup"><span data-stu-id="cf482-164">In **Team site description,** type **SharePoint site for Campaign project 1**.</span></span>

7. <span data-ttu-id="cf482-165">Dans **Paramètres de confidentialité**, sélectionnez **Privé - Seuls les membres peuvent accéder à ce site**, puis cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="cf482-165">In **Privacy settings**, select **Private - only members can access this site**, and then click **Next**.</span></span>

8. <span data-ttu-id="cf482-166">Dans le volet **Qui voulez-vous ajouter ?**, cliquez sur **Terminer**.</span><span class="sxs-lookup"><span data-stu-id="cf482-166">On the **Who do you want to add?** pane, click **Finish**.</span></span>

<span data-ttu-id="cf482-167">Ensuite, configurez le dossier de documents du site d’équipe Projet Campagne 1 pour l’étiquette Privé.</span><span class="sxs-lookup"><span data-stu-id="cf482-167">Next, configure the documents folder of the Campaign project 1 team site for the Private label.</span></span>

1. <span data-ttu-id="cf482-168">Dans l’onglet **Projet Campagne 1 - Accueil** de votre navigateur, cliquez sur **Documents**.</span><span class="sxs-lookup"><span data-stu-id="cf482-168">In the **Campaign project 1-Home** tab of your browser, click **Documents**.</span></span>

2. <span data-ttu-id="cf482-169">Cliquez sur l’icône des paramètres, puis cliquez sur **Paramètres de la bibliothèque**.</span><span class="sxs-lookup"><span data-stu-id="cf482-169">Click the settings icon, and then click **Library settings**.</span></span>

3. <span data-ttu-id="cf482-170">Sous **Autorisations et gestion**, cliquez sur **Appliquer l’étiquette aux éléments de cette bibliothèque**.</span><span class="sxs-lookup"><span data-stu-id="cf482-170">Under **Permissions and Management**, click **Apply label to items in this library**.</span></span>

4. <span data-ttu-id="cf482-171">Dans **Paramètres - Appliquer l’étiquette**, sélectionnez **Privé**, puis cliquez sur **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="cf482-171">In **Settings-Apply Label**, select **Private**, and then click **Save**.</span></span>

### <a name="campaign-marketing-team-site"></a><span data-ttu-id="cf482-172">Site d’équipe marketing de campagne</span><span class="sxs-lookup"><span data-stu-id="cf482-172">Campaign marketing team site</span></span>

<span data-ttu-id="cf482-173">Pour créer un site d’équipe SharePoint Online isolé pour les données sensibles des ressources marketing de la campagne, procédez comme suit :</span><span class="sxs-lookup"><span data-stu-id="cf482-173">To create a sensitive-level isolated SharePoint Online team site for campaign marketing resources, do the following:</span></span>

1. <span data-ttu-id="cf482-174">Utilisez un navigateur de votre ordinateur local et connectez-vous au centre d’administration (<https://admin.microsoft.com>) à l’aide de votre compte d’administrateur général.</span><span class="sxs-lookup"><span data-stu-id="cf482-174">Using a browser on your local computer, sign in to the admin center (<https://admin.microsoft.com>) using your global administrator account.</span></span>

2. <span data-ttu-id="cf482-175">Dans la liste des vignettes, cliquez sur **SharePoint**.</span><span class="sxs-lookup"><span data-stu-id="cf482-175">In the list of tiles, click **SharePoint**.</span></span>

3. <span data-ttu-id="cf482-176">Sous le nouvel onglet **SharePoint** de votre navigateur, cliquez sur **+ Créer un site**.</span><span class="sxs-lookup"><span data-stu-id="cf482-176">On the new **SharePoint** tab in your browser, click **+ Create site**.</span></span>

4. <span data-ttu-id="cf482-177">Dans la page **Créer un site**, cliquez sur **Site d’équipe**.</span><span class="sxs-lookup"><span data-stu-id="cf482-177">On the **Create a site** page, click **Team site**.</span></span>

5. <span data-ttu-id="cf482-178">Dans **Nom du site d’équipe**, saisissez **Ressources marketing de la campagne**.</span><span class="sxs-lookup"><span data-stu-id="cf482-178">In **Team site name**, type **Campaign marketing**.</span></span>

6. <span data-ttu-id="cf482-179">Dans **Description du site d’équipe**, saisissez **Site SharePoint pour les ressources marketing de la campagne (données sensibles)**.</span><span class="sxs-lookup"><span data-stu-id="cf482-179">In **Team site description**, type **SharePoint site for campaign marketing (sensitive)**.</span></span>

7. <span data-ttu-id="cf482-180">Dans **Paramètres de confidentialité**, sélectionnez **Privé - Seuls les membres peuvent accéder à ce site**, puis cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="cf482-180">In **Privacy settings**, select **Private - only members can access this site**, and then click **Next**.</span></span>

8. <span data-ttu-id="cf482-181">Dans le volet **Qui voulez-vous ajouter ?**, cliquez sur **Terminer**.</span><span class="sxs-lookup"><span data-stu-id="cf482-181">On the **Who do you want to add?** pane, click **Finish**.</span></span>

9. <span data-ttu-id="cf482-182">Dans le nouvel onglet **Marketing campagne** de votre navigateur, cliquez sur l’icône des paramètres dans la barre d’outils, puis sur **Autorisations du site**.</span><span class="sxs-lookup"><span data-stu-id="cf482-182">On the new **Campaign marketing** tab in your browser, in the tool bar, click the settings icon, and then click **Site permissions**.</span></span>

10. <span data-ttu-id="cf482-183">Dans le volet **Autorisations du site**, cliquez sur **Paramètres d’autorisations avancés**.</span><span class="sxs-lookup"><span data-stu-id="cf482-183">In the **Site permissions** pane, click **Advanced permissions settings**.</span></span>

11. <span data-ttu-id="cf482-184">Sous le nouvel onglet **Autorisations** dans votre navigateur, cliquez sur **Paramètres des demandes d’accès**.</span><span class="sxs-lookup"><span data-stu-id="cf482-184">In the new **Permissions** tab in your browser, click **Access Request Settings**.</span></span>

12. <span data-ttu-id="cf482-185">Dans la boîte de dialogue **Paramètres de demande d’accès**, désactivez les cases à cocher **Autoriser les membres à partager le site, ainsi que des fichiers et dossiers individuels** et **Autoriser les membres à inviter d’autres personnes sur le groupe de membres du site**, saisissez **ITAdmin1@**\<your organization name\> **.onmicrosoft.com** dans le champ **Envoyer toutes les demandes d’accès à**, puis cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="cf482-185">In the **Access Request Settings** dialog box, clear the **Allow members to share the site and individual files and folders** and **Allow members to invite others to the site members group** check boxes, type **ITAdmin1@**\<your organization name\>**.onmicrosoft.com** in **Send all requests for access**, and then click **OK**.</span></span>

13. <span data-ttu-id="cf482-186">Cliquez sur les **membres de l’équipe marketing de la campagne** dans la liste.</span><span class="sxs-lookup"><span data-stu-id="cf482-186">Click **Campaign marketing Members** in the list.</span></span>

14. <span data-ttu-id="cf482-187">Dans la page **Personnes et groupes**, cliquez sur **Nouveau**.</span><span class="sxs-lookup"><span data-stu-id="cf482-187">On the **People and Groups** page, click **New**.</span></span>

15. <span data-ttu-id="cf482-188">Dans la boîte de dialogue **Partager**, saisissez **Personnel senior et stratégique**, sélectionnez-le, puis cliquez sur **Partager**.</span><span class="sxs-lookup"><span data-stu-id="cf482-188">In the **Share** dialog box, type **Senior and strategic staff**, select it, and then click **Share**.</span></span>

16. <span data-ttu-id="cf482-189">Répétez les étapes 14 et 15 pour le groupe **Analytics staff** et le compte d’utilisateur **Standard1**.</span><span class="sxs-lookup"><span data-stu-id="cf482-189">Repeat steps 14 and 15 for the **Analytics staff** group and the **Regular1** user account.</span></span>

17. <span data-ttu-id="cf482-190">Cliquez sur le bouton de retour de votre navigateur.</span><span class="sxs-lookup"><span data-stu-id="cf482-190">Click the back button on your browser.</span></span>

18. <span data-ttu-id="cf482-191">Cliquez sur **Marketing campagne - Propriétaires** dans la liste.</span><span class="sxs-lookup"><span data-stu-id="cf482-191">Click **Campaign marketing Owners** in the list.</span></span>

19. <span data-ttu-id="cf482-192">Dans la page **Personnes et groupes**, cliquez sur **Nouveau**.</span><span class="sxs-lookup"><span data-stu-id="cf482-192">On the **People and Groups** page, click **New**.</span></span>

20. <span data-ttu-id="cf482-193">Dans la boîte de dialogue **Partager**, saisissez **Équipe informatique**, sélectionnez-la, puis cliquez sur **Partager**.</span><span class="sxs-lookup"><span data-stu-id="cf482-193">In the **Share** dialog box, type **IT staff**, select it, and then click **Share**.</span></span>

21. <span data-ttu-id="cf482-194">Cliquez sur le bouton de retour de votre navigateur.</span><span class="sxs-lookup"><span data-stu-id="cf482-194">Click the back button on your browser.</span></span>

22. <span data-ttu-id="cf482-195">Fermez l’onglet **Personnes et groupes** de votre navigateur, cliquez sur l’onglet **Marketing campagne - Accueil** de votre navigateur, puis fermez le volet **Autorisations du site**.</span><span class="sxs-lookup"><span data-stu-id="cf482-195">Close the **People and Groups** tab in your browser, click the **Campaign marketing-Home** tab in your browser, and then close the **Site permissions** pane.</span></span>

<span data-ttu-id="cf482-196">Voici les résultats de la configuration des autorisations :</span><span class="sxs-lookup"><span data-stu-id="cf482-196">Here are the results of configuring permissions:</span></span>

- <span data-ttu-id="cf482-197">Le groupe SharePoint **Marketing campagne - Membres** contient uniquement le groupe **Senior and strategic staff** (qui contient les comptes d’utilisateurs Candidate, ChiefOfStaff et Strategic1), le groupe **Marketing campagne** (qui contient le compte d’administrateur général), le groupe **Analytics staff** (qui contient le compte d’utilisateur DataScientist1) et le compte d’utilisateur **Regular1**.</span><span class="sxs-lookup"><span data-stu-id="cf482-197">The **Campaign marketing-Members** SharePoint group contains only the **Senior and strategic staff** group (which contains the Candidate, ChiefOfStaff, and Strategic1 user accounts), the **Campaign marketing** group (which contains the global administrator user account), the **Analytics staff** group (which contains the DataScientist1 user account), and the **Regular1** user account.</span></span>

- <span data-ttu-id="cf482-198">Le groupe SharePoint **Marketing campagne - Propriétaires** contient uniquement le groupe **Équipe informatique** (qui contient uniquement les comptes d’utilisateurs ITAdmin1 et ITAdmin2).</span><span class="sxs-lookup"><span data-stu-id="cf482-198">The **Campaign marketing-Owners** SharePoint group contains only the **IT staff** group (which contains only the ITAdmin1 and ITAdmin2 user accounts).</span></span>

- <span data-ttu-id="cf482-199">Le groupe SharePoint **Marketing campagne - Visiteurs** ne contient aucun groupe ou compte d’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="cf482-199">The **Campaign marketing-Visitors** SharePoint group contains no groups or user accounts.</span></span>

- <span data-ttu-id="cf482-200">Les membres ne peuvent pas modifier les autorisations au niveau du site (cette opération peut être uniquement effectuée par les membres du groupe **Marketing campagne - Propriétaires**).</span><span class="sxs-lookup"><span data-stu-id="cf482-200">Members cannot modify site-level permissions (this can only be done by members of the **Campaign marketing-Owners** group).</span></span>

- <span data-ttu-id="cf482-201">Les autres comptes d’utilisateurs ne peuvent pas accéder au site ni à ses ressources, mais peuvent demander d’avoir accès au site. Un courrier électronique sera envoyé à la boîte aux lettres du compte d’utilisateur ITAdmin1.</span><span class="sxs-lookup"><span data-stu-id="cf482-201">Other user accounts cannot access the site or its resources, but can request access to the site, which will send an email to the ITAdmin1 user account mailbox.</span></span>

<span data-ttu-id="cf482-202">Ensuite, configurez le dossier de documents du site d’équipe Marketing campagne pour l’étiquette Sensible.</span><span class="sxs-lookup"><span data-stu-id="cf482-202">Next, configure the documents folder of the Campaign marketing team site for the Sensitive label.</span></span>

1. <span data-ttu-id="cf482-203">Dans l’onglet **Marketing campagne - Accueil** de votre navigateur, cliquez sur **Documents**.</span><span class="sxs-lookup"><span data-stu-id="cf482-203">In the **Campaign marketing-Home** tab of your browser, click **Documents**.</span></span>

2. <span data-ttu-id="cf482-204">Cliquez sur l’icône des paramètres, puis cliquez sur **Paramètres de la bibliothèque**.</span><span class="sxs-lookup"><span data-stu-id="cf482-204">Click the settings icon, and then click **Library settings**.</span></span>

3. <span data-ttu-id="cf482-205">Sous **Autorisations et gestion**, cliquez sur **Appliquer l’étiquette aux éléments de cette bibliothèque**.</span><span class="sxs-lookup"><span data-stu-id="cf482-205">Under **Permissions and Management**, click **Apply label to items in this library**.</span></span>

4. <span data-ttu-id="cf482-206">Dans **Paramètres - Appliquer l’étiquette**, sélectionnez **Sensible**, puis cliquez sur **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="cf482-206">In **Settings-Apply Label**, select **Sensitive**, and then click **Save**.</span></span>

<span data-ttu-id="cf482-p106">Ensuite, configurez une stratégie de protection contre la perte de données qui avertit les utilisateurs quand ils partagent un document sur un site d’équipe SharePoint Online avec l’étiquette Sensible à l’extérieur de l’organisation. Cette stratégie DLP s’applique aux ressources du site Marketing campagne.</span><span class="sxs-lookup"><span data-stu-id="cf482-p106">Next, configure a data loss prevention (DLP) policy that notifies users when they share a document on a SharePoint Online team site with the Sensitive label outside the organization. This DLP policy will apply to resources in the Campaign marketing site.</span></span>

1. <span data-ttu-id="cf482-209">Sous l’onglet **Accueil Microsoft Office** de votre navigateur, cliquez sur la vignette **Sécurité et conformité**.</span><span class="sxs-lookup"><span data-stu-id="cf482-209">From the **Microsoft Office Home** tab in your browser, click the **Security & Compliance** tile.</span></span>

2. <span data-ttu-id="cf482-210">Sous le nouvel onglet **Sécurité et conformité** de votre navigateur, cliquez sur **Protection contre la perte de données > Stratégie**.</span><span class="sxs-lookup"><span data-stu-id="cf482-210">On the new **Security & Compliance** tab in your browser, click **Data loss prevention > Policy**.</span></span>

3. <span data-ttu-id="cf482-211">Dans le volet **Protection contre la perte de données**, cliquez sur **+ Créer une stratégie**.</span><span class="sxs-lookup"><span data-stu-id="cf482-211">In the **Data loss prevention** pane, click **+ Create a policy**.</span></span>

4. <span data-ttu-id="cf482-212">Dans le volet **Utiliser un modèle ou créer une stratégie personnalisée**, cliquez sur **Personnalisé**, puis sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="cf482-212">In the **Start with a template or create a custom policy** pane, click **Custom**, and then click **Next**.</span></span>

5. <span data-ttu-id="cf482-213">Dans le volet **Nom de votre stratégie**, saisissez les **sites d’équipe SharePoint Online avec étiquette Sensible** sous **Nom**, puis cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="cf482-213">In the **Name your policy** pane, type **Sensitive label SharePoint Online team sites** in **Name**, and then click **Next**.</span></span>

6. <span data-ttu-id="cf482-214">Dans le volet **Choisir des emplacements**, cliquez sur **Me laisser choisir des emplacements spécifiques**, puis cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="cf482-214">In the **Choose locations** pane, click **Let me choose specific locations**, and then click **Next**.</span></span>

7. <span data-ttu-id="cf482-215">Dans la liste des emplacements, désactivez les emplacements **Messagerie Exchange** et **Comptes OneDrive**, puis cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="cf482-215">In the list of locations, disable the **Exchange email** and **OneDrive accounts** locations, and then click **Next**.</span></span>

8. <span data-ttu-id="cf482-216">Dans le volet **Personnaliser les types d’informations sensibles que vous voulez protéger**, cliquez sur **Modifier**.</span><span class="sxs-lookup"><span data-stu-id="cf482-216">In the **Customize the types of sensitive info you want to protect** pane, click **Edit**.</span></span>

9. <span data-ttu-id="cf482-217">Dans le volet **Choisir les types de contenu à protéger**, cliquez sur **Ajouter** dans la zone de liste déroulante, puis cliquez sur **Étiquettes**.</span><span class="sxs-lookup"><span data-stu-id="cf482-217">In the **Choose the types of content to protect** pane, click **Add** in the drop-down box, and then click **Labels**.</span></span>

10. <span data-ttu-id="cf482-218">Dans le volet **Étiquettes**, cliquez sur **+ Ajouter**, sélectionnez l’étiquette **Sensible**, cliquez sur **Ajouter**, puis sur **Terminé**.</span><span class="sxs-lookup"><span data-stu-id="cf482-218">In the **Labels** pane, click **+ Add**, select the **Sensitive** label, click **Add**, and then click **Done**.</span></span>

11. <span data-ttu-id="cf482-219">Dans le volet **Choisir les types de contenu à protéger**, cliquez sur **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="cf482-219">In the **Choose the types of content to protect** pane, click **Save**.</span></span>

12. <span data-ttu-id="cf482-220">Dans le volet **Personnaliser les types d’informations sensibles que vous voulez protéger**, cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="cf482-220">In the **Customize the types of sensitive info you want to protect** pane, click **Next**.</span></span>

13. <span data-ttu-id="cf482-221">Dans le volet **Que voulez-vous faire si nous détectons des informations confidentielles ?**, cliquez sur **Personnaliser l’info-bulle et la messagerie électronique**.</span><span class="sxs-lookup"><span data-stu-id="cf482-221">In the **What do you want to do if we detect sensitive info?** pane, click **Customize the tip and email**.</span></span>

14. <span data-ttu-id="cf482-222">Dans le volet **Personnaliser les conseils et les notifications par e-mail de la stratégie**, cliquez sur **Personnaliser le texte de l’info-bulle de la stratégie**.</span><span class="sxs-lookup"><span data-stu-id="cf482-222">In the **Customize policy tips and email notifications** pane, click **Customize the policy tip text**.</span></span>

15. <span data-ttu-id="cf482-223">Dans la zone de texte, tapez ou collez ce qui suit :</span><span class="sxs-lookup"><span data-stu-id="cf482-223">In the text box, type or paste in the following:</span></span>

    - <span data-ttu-id="cf482-p107">Pour partager un fichier avec un utilisateur extérieur à l’organisation, téléchargez-le et ouvrez-le. Cliquez sur Fichier > Protéger le document > Chiffrer avec mot de passe, puis indiquez un mot de passe fort. Envoyez le mot de passe par e-mail ou un autre moyen de communication.</span><span class="sxs-lookup"><span data-stu-id="cf482-p107">To share with a user outside the organization, download the file and then open it. Click File, then Protect Document, and then Encrypt with Password, and then specify a strong password. Send the password in a separate email or other means of communication.</span></span>

16. <span data-ttu-id="cf482-227">Cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="cf482-227">Click **OK**.</span></span>

17. <span data-ttu-id="cf482-228">Dans le volet **Que faire en cas de détection d’informations sensibles ?**, désélectionnez la case **Empêcher les utilisateurs de partager un fichier et restreindre l’accès au contenu partagé**, puis cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="cf482-228">In the **What do you want to do if we detect sensitive info?** pane, clear the **Block people from sharing, and restrict access to shared content** check box, and then click **Next**.</span></span>

18. <span data-ttu-id="cf482-229">Dans le volet **Voulez-vous activer la stratégie ou d’abord effectuer des tests ?**, cliquez sur **Oui, l’activer maintenant**, puis cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="cf482-229">In the **Do you want to turn on the policy or test things out first?** pane, click **Yes, turn it on right away**, and then click **Next**.</span></span>

19. <span data-ttu-id="cf482-230">Dans le volet **Vérifier vos paramètres**, cliquez sur **Créer**, puis cliquez sur **Fermer**.</span><span class="sxs-lookup"><span data-stu-id="cf482-230">In the **Review your settings** pane, click **Create**, and then click **Close**.</span></span>

### <a name="campaign-strategy-team-site"></a><span data-ttu-id="cf482-231">Site d’équipe Stratégie de campagne</span><span class="sxs-lookup"><span data-stu-id="cf482-231">Campaign strategy team site</span></span>

<span data-ttu-id="cf482-232">Pour créer un site d’équipe SharePoint Online isolé hautement confidentiel pour les ressources de stratégie de campagne, procédez comme suit :</span><span class="sxs-lookup"><span data-stu-id="cf482-232">To create an isolated SharePoint Online team site at the highly confidential level for campaign strategy resources, do the following:</span></span>

1. <span data-ttu-id="cf482-233">Si nécessaire, utilisez un navigateur de votre ordinateur local et connectez-vous au centre d’administration (<https://admin.microsoft.com>) à l’aide de votre compte d’administrateur général.</span><span class="sxs-lookup"><span data-stu-id="cf482-233">If needed, use a browser on your local computer and sign in to the admin center (<https://admin.microsoft.com>) using your global administrator account.</span></span>

2. <span data-ttu-id="cf482-234">Dans la liste des vignettes, cliquez sur **SharePoint**.</span><span class="sxs-lookup"><span data-stu-id="cf482-234">In the list of tiles, click **SharePoint**.</span></span>

3. <span data-ttu-id="cf482-235">Sous le nouvel onglet **SharePoint** de votre navigateur, cliquez sur **+ Créer un site**.</span><span class="sxs-lookup"><span data-stu-id="cf482-235">On the new **SharePoint** tab in your browser, click **+ Create site**.</span></span>

4. <span data-ttu-id="cf482-236">Dans la page **Créer un site**, cliquez sur **Site d’équipe**.</span><span class="sxs-lookup"><span data-stu-id="cf482-236">On the **Create a site** page, click **Team site**.</span></span>

5. <span data-ttu-id="cf482-237">Dans **Nom du site d’équipe**, saisissez **Stratégie de campagne**.</span><span class="sxs-lookup"><span data-stu-id="cf482-237">In **Team site name**, type **Campaign strategy**.</span></span>

6. <span data-ttu-id="cf482-238">Dans **Description du site d’équipe** saisissez **Site SharePoint pour la stratégie de campagne (hautement confidentiel)**.</span><span class="sxs-lookup"><span data-stu-id="cf482-238">In **Team site description**, type **SharePoint site for campaign strategy (highly confidential)**.</span></span>

7. <span data-ttu-id="cf482-239">Dans **Paramètres de confidentialité**, sélectionnez **Privé - Seuls les membres peuvent accéder à ce site**, puis cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="cf482-239">In **Privacy settings**, select **Private - only members can access this site**, and then click **Next**.</span></span>

8. <span data-ttu-id="cf482-240">Dans le volet **Qui voulez-vous ajouter ?**, cliquez sur **Terminer**.</span><span class="sxs-lookup"><span data-stu-id="cf482-240">On the **Who do you want to add?** pane, click **Finish**.</span></span>

9. <span data-ttu-id="cf482-241">Dans le nouvel onglet **Stratégie de campagne** de votre navigateur, cliquez sur l’icône des paramètres dans la barre d’outils, puis sur **Autorisations du site**.</span><span class="sxs-lookup"><span data-stu-id="cf482-241">On the new **Campaign strategy** tab in your browser, in the tool bar, click the settings icon, and then click **Site permissions**.</span></span>

10. <span data-ttu-id="cf482-242">Dans le volet **Autorisations du site**, cliquez sur **Paramètres d’autorisations avancés**.</span><span class="sxs-lookup"><span data-stu-id="cf482-242">In the **Site permissions** pane, click **Advanced permissions settings**.</span></span>

11. <span data-ttu-id="cf482-243">Sous le nouvel onglet **Autorisations** dans votre navigateur, cliquez sur **Paramètres des demandes d’accès**.</span><span class="sxs-lookup"><span data-stu-id="cf482-243">In the new **Permissions** tab in your browser, click **Access Request Settings**.</span></span>

12. <span data-ttu-id="cf482-244">Dans la boîte de dialogue **Paramètres de demande d’accès**, désactivez les cases à cocher **Autoriser les membres à partager le site et les fichiers et dossiers individuels** et **Autoriser les membres à inviter d’autres personnes sur le groupe de membres du site** (afin que les trois cases à cocher soient désactivées), puis cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="cf482-244">In the **Access Request Settings** dialog box, clear **Allow members to share the site and individual files and folders** and **Allow members to invite others to the site members group** (so that all three check boxes are cleared), and then click **OK**.</span></span>

13. <span data-ttu-id="cf482-245">Cliquez sur les **membres de l’équipe Stratégie de campagne** dans la liste.</span><span class="sxs-lookup"><span data-stu-id="cf482-245">Click **Campaign strategy Members** in the list.</span></span>

14. <span data-ttu-id="cf482-246">Dans la page **Personnes et groupes**, cliquez sur **Nouveau**.</span><span class="sxs-lookup"><span data-stu-id="cf482-246">On the **People and Groups** page, click **New**.</span></span>

15. <span data-ttu-id="cf482-247">Dans la boîte de dialogue **Partager**, saisissez **Personnel senior et stratégique**, sélectionnez-le, puis cliquez sur **Partager**.</span><span class="sxs-lookup"><span data-stu-id="cf482-247">In the **Share** dialog box, type **Senior and strategic staff**, select it, and then click **Share**.</span></span>

16. <span data-ttu-id="cf482-248">Cliquez sur les **propriétaires de la stratégie de campagne** dans la liste.</span><span class="sxs-lookup"><span data-stu-id="cf482-248">Click **Campaign strategy Owners** in the list.</span></span>

17. <span data-ttu-id="cf482-249">Dans la page **Personnes et groupes**, cliquez sur **Nouveau**.</span><span class="sxs-lookup"><span data-stu-id="cf482-249">On the **People and Groups** page, click **New**.</span></span>

18. <span data-ttu-id="cf482-250">Dans la boîte de dialogue **Partager**, saisissez **Équipe informatique**, sélectionnez-la, puis cliquez sur **Partager**.</span><span class="sxs-lookup"><span data-stu-id="cf482-250">In the **Share** dialog box, type **IT staff**, select it, and then click **Share**.</span></span>

19. <span data-ttu-id="cf482-251">Cliquez sur le bouton de retour de votre navigateur.</span><span class="sxs-lookup"><span data-stu-id="cf482-251">Click the back button on your browser.</span></span>

20. <span data-ttu-id="cf482-252">Fermez l’onglet **Personnes et groupes** de votre navigateur, cliquez sur l’onglet **Stratégie de campagne - Accueil** de votre navigateur, puis fermez le volet **Autorisations du site**.</span><span class="sxs-lookup"><span data-stu-id="cf482-252">Close the **People and Groups** tab in your browser, click the **Campaign strategy-Home** tab in your browser, and then close the **Site permissions** pane.</span></span>

<span data-ttu-id="cf482-253">Voici les résultats de la configuration des autorisations :</span><span class="sxs-lookup"><span data-stu-id="cf482-253">Here are the results of configuring permissions:</span></span>

- <span data-ttu-id="cf482-254">Le groupe SharePoint **Stratégie de campagne - Membres** contient uniquement le groupe **Senior and strategic staff** (qui contient uniquement les comptes d’utilisateurs Candidate, ChiefOfStaff et Strategic1) et le groupe **Stratégie de campagne** (qui contient uniquement le compte d’administrateur général).
</span><span class="sxs-lookup"><span data-stu-id="cf482-254">The **Campaign strategy-Members** SharePoint group contains only the **Senior and strategic staff** group (which contains only the Candidate, ChiefOfStaff, and Strategic1 user accounts) and the **Campaign strategy** group (which contains only the global administrator user account).</span></span>

- <span data-ttu-id="cf482-255">Le groupe SharePoint **Stratégie de campagne - Propriétaires** contient uniquement le groupe **Équipe informatique** (qui contient uniquement les comptes d’utilisateurs ITAdmin1 et ITAdmin2).</span><span class="sxs-lookup"><span data-stu-id="cf482-255">The **Campaign strategy-Owners** SharePoint group contains only the **IT staff** group (which contains only the ITAdmin1 and ITAdmin2 user accounts).</span></span>

- <span data-ttu-id="cf482-256">Le groupe SharePoint **Stratégie de campagne - Visiteurs** ne contient aucun groupe ou compte d’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="cf482-256">The **Campaign strategy-Visitors** SharePoint group contains no groups or user accounts.</span></span>

- <span data-ttu-id="cf482-257">Les membres ne peuvent pas modifier les autorisations au niveau du site (cette opération peut être uniquement effectuée par les membres du groupe **Stratégie de campagne - Propriétaires**).</span><span class="sxs-lookup"><span data-stu-id="cf482-257">Members cannot modify site-level permissions (this can only be done by members of the **Campaign strategy-Owners** group).</span></span>

- <span data-ttu-id="cf482-p108">Les autres comptes d’utilisateurs ne peuvent pas accéder au site ni à ses ressources, ni demander l’accès au site. Les autorisations supplémentaires doivent être accordées par l’administrateur général ou par un membre du groupe **Stratégie de campagne - Propriétaires**.</span><span class="sxs-lookup"><span data-stu-id="cf482-p108">Other user accounts cannot access the site or its resources or request access to the site. Additional permissions to the site must be done by the global administrator or by a member of the **Campaign strategy-Owners** group.</span></span>

<span data-ttu-id="cf482-260">Ensuite, configurez le dossier de documents du site d’équipe Stratégie de campagne pour l’étiquette Hautement confidentiel.</span><span class="sxs-lookup"><span data-stu-id="cf482-260">Next, configure the documents folder of the Campaign strategy team site for the Highly Confidential label.</span></span>

1. <span data-ttu-id="cf482-261">Dans l’onglet **Stratégie de campagne - Accueil** de votre navigateur, cliquez sur **Documents**.</span><span class="sxs-lookup"><span data-stu-id="cf482-261">In the **Campaign strategy-Home** tab of your browser, click **Documents**.</span></span>

2. <span data-ttu-id="cf482-262">Cliquez sur l’icône des paramètres, puis cliquez sur **Paramètres de la bibliothèque**.</span><span class="sxs-lookup"><span data-stu-id="cf482-262">Click the settings icon, and then click **Library settings**.</span></span>

3. <span data-ttu-id="cf482-263">Sous **Autorisations et gestion**, cliquez sur **Appliquer l’étiquette aux éléments de cette bibliothèque**.</span><span class="sxs-lookup"><span data-stu-id="cf482-263">Under **Permissions and Management**, click **Apply label to items in this library**.</span></span>

4. <span data-ttu-id="cf482-264">Dans **Paramètres - Appliquer une étiquette**, sélectionnez **Hautement confidentiel**, puis cliquez sur **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="cf482-264">In **Settings-Apply Label**, select **Highly Confidential**, and then click **Save**.</span></span>

<span data-ttu-id="cf482-p109">Ensuite, configurez une stratégie DLP qui bloque les utilisateurs quand ils partagent un document à l’extérieur de l’organisation sur un site d’équipe SharePoint Online avec l’étiquette Hautement confidentiel. Cette stratégie DLP s’applique aux ressources du site Stratégie de campagne.</span><span class="sxs-lookup"><span data-stu-id="cf482-p109">Next, configure a DLP policy that blocks users when they share a document on a SharePoint Online team site with the Highly Confidential label outside the organization. This DLP policy will apply to resources in the Campaign strategy site.</span></span>

1. <span data-ttu-id="cf482-267">Si nécessaire, utilisez un navigateur de votre ordinateur local et connectez-vous au centre d’administration (<https://admin.microsoft.com>) à l’aide d’un compte disposant du rôle Administrateur de la sécurité ou Administrateur de la société.</span><span class="sxs-lookup"><span data-stu-id="cf482-267">If needed, use a browser on your local computer and sign in to the admin center (<https://admin.microsoft.com>) with an account that has the Security Administrator or Company Administrator role.</span></span>

2. <span data-ttu-id="cf482-268">Sous l’onglet **Accueil Microsoft Office** de votre navigateur, cliquez sur la vignette **Sécurité et conformité**.</span><span class="sxs-lookup"><span data-stu-id="cf482-268">From the **Microsoft Office Home** tab in your browser, click the **Security & Compliance** tile.</span></span>

3. <span data-ttu-id="cf482-269">Sous le nouvel onglet **Sécurité et conformité** de votre navigateur, cliquez sur **Protection contre la perte de données > Stratégie**.</span><span class="sxs-lookup"><span data-stu-id="cf482-269">On the new **Security & Compliance** tab in your browser, click **Data loss prevention > Policy**.</span></span>

4. <span data-ttu-id="cf482-270">Dans le volet **Protection contre la perte de données**, cliquez sur **+ Créer une stratégie**.</span><span class="sxs-lookup"><span data-stu-id="cf482-270">In the **Data loss prevention** pane, click **+ Create a policy**.</span></span>

5. <span data-ttu-id="cf482-271">Dans le volet **Utiliser un modèle ou créer une stratégie personnalisée**, cliquez sur **Personnalisé**, puis sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="cf482-271">In the **Start with a template or create a custom policy** pane, click **Custom**, and then click **Next**.</span></span>

6. <span data-ttu-id="cf482-272">Dans le volet **Nom de votre stratégie**, saisissez les **sites d’équipe SharePoint Online avec étiquette Hautement confidentiel** sous **Nom**, puis cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="cf482-272">In the **Name your policy** pane, type **Highly Confidential label SharePoint Online team sites** in **Name**, and then click **Next**.</span></span>

7. <span data-ttu-id="cf482-273">Dans le volet **Choisir des emplacements**, cliquez sur **Me laisser choisir des emplacements spécifiques**, puis cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="cf482-273">In the **Choose locations** pane, click **Let me choose specific locations**, and then click **Next**.</span></span>

8. <span data-ttu-id="cf482-274">Dans la liste des emplacements, désactivez les emplacements **Messagerie Exchange** et **Comptes OneDrive**, puis cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="cf482-274">In the list of locations, disable the **Exchange email** and **OneDrive accounts** locations, and then click **Next**.</span></span>

9. <span data-ttu-id="cf482-275">Dans le volet **Personnaliser les types d’informations sensibles que vous voulez protéger**, cliquez sur **Modifier**.</span><span class="sxs-lookup"><span data-stu-id="cf482-275">In the **Customize the types of sensitive info you want to protect** pane, click **Edit**.</span></span>

10. <span data-ttu-id="cf482-276">Dans le volet **Choisir les types de contenu à protéger**, cliquez sur **Ajouter** dans la zone de liste déroulante, puis cliquez sur **Étiquettes**.</span><span class="sxs-lookup"><span data-stu-id="cf482-276">In the **Choose the types of content to protect** pane, click **Add** in the drop-down box, and then click **Labels**.</span></span>

11. <span data-ttu-id="cf482-277">Dans le volet **Étiquettes**, cliquez sur **+ Ajouter**, sélectionnez l’étiquette **Hautement confidentiel**, cliquez sur **Ajouter**, puis sur **Terminé**.</span><span class="sxs-lookup"><span data-stu-id="cf482-277">In the **Labels** pane, click **+ Add**, select the **Highly Confidential** label, click **Add**, and then click **Done**.</span></span>

12. <span data-ttu-id="cf482-278">Dans le volet **Choisir les types de contenu à protéger**, cliquez sur **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="cf482-278">In the **Choose the types of content to protect** pane, click **Save**.</span></span>

13. <span data-ttu-id="cf482-279">Dans le volet **Personnaliser les types d’informations sensibles que vous voulez protéger**, cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="cf482-279">In the **Customize the types of sensitive info you want to protect** pane, click **Next**.</span></span>

14. <span data-ttu-id="cf482-280">Dans le volet **Que voulez-vous faire si nous détectons des informations confidentielles ?**, cliquez sur **Personnaliser l’info-bulle et la messagerie électronique**.</span><span class="sxs-lookup"><span data-stu-id="cf482-280">In the **What do you want to do if we detect sensitive info?** pane, click **Customize the tip and email**.</span></span>

15. <span data-ttu-id="cf482-281">Dans le volet **Personnaliser les conseils et les notifications par e-mail de la stratégie**, cliquez sur **Personnaliser le texte de l’info-bulle de la stratégie**.</span><span class="sxs-lookup"><span data-stu-id="cf482-281">In the **Customize policy tips and email notifications** pane, click **Customize the policy tip text**.</span></span>

16. <span data-ttu-id="cf482-282">Dans la zone de texte, tapez ou collez ce qui suit :</span><span class="sxs-lookup"><span data-stu-id="cf482-282">In the text box, type or paste in the following:</span></span>

    - <span data-ttu-id="cf482-p110">Pour partager un fichier avec un utilisateur extérieur à l’organisation, téléchargez-le et ouvrez-le. Cliquez sur Fichier > Protéger le document > Chiffrer avec mot de passe, puis indiquez un mot de passe fort. Envoyez le mot de passe par e-mail ou un autre moyen de communication.</span><span class="sxs-lookup"><span data-stu-id="cf482-p110">To share with a user outside the organization, download the file and then open it. Click File, then Protect Document, and then Encrypt with Password, and then specify a strong password. Send the password in a separate email or other means of communication.</span></span>

17. <span data-ttu-id="cf482-286">Cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="cf482-286">Click **OK**.</span></span>

18. <span data-ttu-id="cf482-287">Dans le volet **Que faire en cas de détection d’informations sensibles ?**, sélectionnez **Exiger une justification professionnelle pour le remplacement**, puis cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="cf482-287">In the **What do you want to do if we detect sensitive info?** pane, select **Require a business justification to override**, and then click **Next**.</span></span>

19. <span data-ttu-id="cf482-288">Dans le volet **Voulez-vous activer la stratégie ou d’abord effectuer des tests ?**, cliquez sur **Oui, l’activer maintenant**, puis cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="cf482-288">In the **Do you want to turn on the policy or test things out first?** pane, click **Yes, turn it on right away**, and then click **Next**.</span></span>

20. <span data-ttu-id="cf482-289">Dans le volet **Vérifier vos paramètres**, cliquez sur **Créer**, puis sur **Fermer**.</span><span class="sxs-lookup"><span data-stu-id="cf482-289">In the **Review your settings** pane, click **Create**, and then click **Close**.</span></span>

<span data-ttu-id="cf482-290">Utilisez les instructions de [Comment activer Azure Rights Management à partir du Centre d’administration Microsoft 365](/information-protection/deploy-use/activate-office365).</span><span class="sxs-lookup"><span data-stu-id="cf482-290">Use the instructions in [Activate Azure RMS with the Microsoft 365 admin center](/information-protection/deploy-use/activate-office365).</span></span>

<span data-ttu-id="cf482-291">Ensuite, configurez Azure Information Protection avec une nouvelle stratégie délimitée et une sous-étiquette pour la protection et les autorisations en suivant ces étapes :</span><span class="sxs-lookup"><span data-stu-id="cf482-291">Next, configure Azure Information Protection with a new scoped policy and sub-label for protection and permissions with the following steps:</span></span>

1. <span data-ttu-id="cf482-p111">Connectez-vous au centre d'administration avec un compte disposant du rôle Administrateur de sécurité ou Administrateur d’entreprise. Pour obtenir de l’aide, consultez la rubrique [Se connecter à Office 365](https://support.microsoft.com/office/e9eb7d51-5430-4929-91ab-6157c5a050b4).</span><span class="sxs-lookup"><span data-stu-id="cf482-p111">Sign in to the admin center with an account that has the Security Administrator or Company Administrator role. For help, see [Where to sign in to Office 365](https://support.microsoft.com/office/e9eb7d51-5430-4929-91ab-6157c5a050b4).</span></span>

2. <span data-ttu-id="cf482-294">Dans un nouvel onglet de votre navigateur, accédez au portail Azure (<https://portal.azure.com>).</span><span class="sxs-lookup"><span data-stu-id="cf482-294">In a separate tab of your browser, go to the Azure portal (<https://portal.azure.com>).</span></span>

3. <span data-ttu-id="cf482-295">Dans le volet Rechercher, tapez **information**, puis cliquez **Azure Information Protection**.</span><span class="sxs-lookup"><span data-stu-id="cf482-295">In the search pane, type **information**, and then click **Azure Information Protection**.</span></span>

4. <span data-ttu-id="cf482-296">Cliquez sur **Étiquettes**.</span><span class="sxs-lookup"><span data-stu-id="cf482-296">Click **Labels**.</span></span>

5. <span data-ttu-id="cf482-297">Cliquez avec le bouton droit de la souris sur l’étiquette **Hautement confidentiel**, puis sur **Ajouter une sous-étiquette**.</span><span class="sxs-lookup"><span data-stu-id="cf482-297">Right-click the **Highly Confidential** label, and then click **Add a sub-label**.</span></span>

6. <span data-ttu-id="cf482-298">Saisissez **CampaignStrategy** dans **Nom** et **Étiquette pour les documents dans le site d’équipe Stratégie de campagne** dans **Description**.</span><span class="sxs-lookup"><span data-stu-id="cf482-298">Type **CampaignStrategy** in **Name** and **Label for documents in the Campaign strategy team site** in **Description**.</span></span>

7. <span data-ttu-id="cf482-299">Dans **Définir les autorisations pour les documents et les e-mails contenant cette étiquette**, cliquez sur **Protéger**.</span><span class="sxs-lookup"><span data-stu-id="cf482-299">In **Set permissions for documents and emails containing this label**, click **Protect**.</span></span>

8. <span data-ttu-id="cf482-300">Dans la section **Protection**, cliquez sur **Azure (clé cloud)**.</span><span class="sxs-lookup"><span data-stu-id="cf482-300">In the **Protection** section, click **Azure (cloud key)**.</span></span>

9. <span data-ttu-id="cf482-301">Dans le panneau **Protection**, sous **Paramètres de protection**, cliquez sur **+ Ajouter des autorisations**.</span><span class="sxs-lookup"><span data-stu-id="cf482-301">On the **Protection** blade, under **Protection settings**, click **+ Add permissions**.</span></span>

10. <span data-ttu-id="cf482-302">Dans le panneau **Ajouter des autorisations**, sous **Spécifier les utilisateurs et les groupes**, cliquez sur **+ Parcourir le répertoire**.</span><span class="sxs-lookup"><span data-stu-id="cf482-302">On the **Add permissions** blade, under **Specify users and groups**, click **+ Browse directory**.</span></span>

11. <span data-ttu-id="cf482-303">Dans le volet **Utilisateurs et groupes AAD**, sélectionnez **Personnel senior et stratégique**, puis cliquez sur **Sélectionner**.</span><span class="sxs-lookup"><span data-stu-id="cf482-303">On the **AAD Users and Groups** pane, select **Senior and strategic staff**, and then click **Select**.</span></span>

12. <span data-ttu-id="cf482-304">sSous **Choisir les autorisations parmi les autorisations personnalisées prédéfinies ou définies**, cliquez sur **Personnalisé**, puis sur les cases à cocher **Afficher les droits**, **Modifier le contenu**, **Enregistrer**, **Répondre** et **Répondre à tous**.</span><span class="sxs-lookup"><span data-stu-id="cf482-304">Under **Choose permissions from the preset or set custom**, click **Custom**, and then click the **View Rights**, **Edit Content**, **Save**, **Reply**, and **Reply all** check boxes.</span></span>

13. <span data-ttu-id="cf482-305">Cliquez deux fois sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="cf482-305">Click **OK** twice.</span></span>

14. <span data-ttu-id="cf482-306">Dans le panneau **Sous-étiquette**, cliquez sur **Enregistrer**, puis sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="cf482-306">On the **Sub-label** blade, click **Save**, and then click **OK**.</span></span>

15. <span data-ttu-id="cf482-307">Dans le panneau **Azure Information Protection**, cliquez sur **Stratégies > + Ajouter une nouvelle stratégie**.</span><span class="sxs-lookup"><span data-stu-id="cf482-307">On the **Azure Information protection** blade, click **Policies > + Add a new policy**.</span></span>

16. <span data-ttu-id="cf482-308">Saisissez **CampaignStrategy** dans **Nom** et **Documents dans le site d’équipe Stratégie de campagne** dans **Description**.</span><span class="sxs-lookup"><span data-stu-id="cf482-308">Type **CampaignStrategy** in **Name** and **Documents in the Campaign strategy team site** in **Description**.</span></span>

17. <span data-ttu-id="cf482-309">Cliquez sur **Sélectionner les utilisateurs ou groupes devant recevoir cette stratégie > Utilisateurs/Groupes**, puis sélectionnez **Personnel senior et stratégique**.</span><span class="sxs-lookup"><span data-stu-id="cf482-309">Click **Select which users or groups get this policy > User/Groups**, and then select **Senior and strategic staff**.</span></span>

18. <span data-ttu-id="cf482-310">Cliquez sur **Sélectionner \> OK**.</span><span class="sxs-lookup"><span data-stu-id="cf482-310">Click **Select \> OK**.</span></span>

19. <span data-ttu-id="cf482-p112">Cliquez sur **Ajouter ou supprimer des étiquettes**. Dans le volet **Stratégie : Ajouter ou supprimer des étiquettes**, cliquez sur **CampaignStrategy**, puis sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="cf482-p112">Click **Add or remove labels**. In the **Policy: Add or remove labels** pane, click **CampaignStrategy**, and then click **OK**.</span></span>

20. <span data-ttu-id="cf482-313">Cliquez sur **Enregistrer**, puis sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="cf482-313">Click **Save**, and then click **OK**.</span></span>

<span data-ttu-id="cf482-314">Vous êtes désormais prêt à créer des documents dans ces quatre sites et à tester l’accès à ces sites avec divers comptes d’utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="cf482-314">You are now ready to begin creating documents in these four sites and test access to them with various user accounts.</span></span>

<span data-ttu-id="cf482-315">Pour protéger un document avec Azure Information Protection et cette nouvelle étiquette, vous devez [installer le client Azure Information Protection](/information-protection/rms-client/install-client-app) sur une machine de test, installer Office à partir du centre d’administration, puis vous connecter à partir de Microsoft Word avec un compte du groupe **Personnel senior et stratégique** de votre abonnement d’essai.</span><span class="sxs-lookup"><span data-stu-id="cf482-315">To protect a document with Azure Information Protection and this new label, you must [install the Azure Information Protection client](/information-protection/rms-client/install-client-app) on a test machine, install Office from the admin center, and then sign in from Microsoft Word with an account in the **Senior and strategic staff** group of your trial subscription.</span></span>

## <a name="see-also"></a><span data-ttu-id="cf482-316">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="cf482-316">See Also</span></span>

[<span data-ttu-id="cf482-317">Conseils de sécurité Microsoft pour les campagnes électorales, les organisations à but non lucratif et d’autres organisations flexibles</span><span class="sxs-lookup"><span data-stu-id="cf482-317">Microsoft Security Guidance for Political Campaigns, Nonprofits, and Other Agile Organizations</span></span>](microsoft-security-guidance-for-political-campaigns-nonprofits-and-other-agile-o.md)

[<span data-ttu-id="cf482-318">Configuration de groupes et d’utilisateurs pour un environnement de développement/test pour une campagne électorale</span><span class="sxs-lookup"><span data-stu-id="cf482-318">Configure groups and users for a political campaign dev/test environment</span></span>](configure-groups-and-users-for-a-political-campaign-dev-test-environment.md)

[<span data-ttu-id="cf482-319">Guides de laboratoire de test d’adoption cloud</span><span class="sxs-lookup"><span data-stu-id="cf482-319">Cloud adoption Test Lab Guides (TLGs)</span></span>](../../enterprise/cloud-adoption-test-lab-guides-tlgs.md)

[<span data-ttu-id="cf482-320">Centre de solutions et d'architecture Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="cf482-320">Microsoft 365 solution and architecture center</span></span>](../../solutions/index.yml)