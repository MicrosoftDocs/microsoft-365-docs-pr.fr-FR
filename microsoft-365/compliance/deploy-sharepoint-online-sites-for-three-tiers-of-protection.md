---
title: Déployer des sites SharePoint Online pour trois niveaux de protection
ms.author: josephd
author: JoeDavies-MSFT
manager: laurawi
ms.date: 03/29/2019
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
ms.assetid: 1e8e3cfd-b878-4088-b941-9940363a5fae
description: 'Résumé : Créez et configurez des sites d’équipe SharePoint Online avec différents niveaux de protection des informations.'
ms.openlocfilehash: 2ddf3de7180d384c387bdc335afda6214508e3c5
ms.sourcegitcommit: 1162d676b036449ea4220de8a6642165190e3398
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/20/2019
ms.locfileid: "37070697"
---
# <a name="deploy-sharepoint-online-sites-for-three-tiers-of-protection"></a><span data-ttu-id="6cafc-103">Déployer des sites SharePoint Online pour trois niveaux de protection</span><span class="sxs-lookup"><span data-stu-id="6cafc-103">Deploy SharePoint Online sites for three tiers of protection</span></span>

 <span data-ttu-id="6cafc-104">**Résumé :** Créez et configurez des sites d’équipe SharePoint Online avec différents niveaux de protection des informations.</span><span class="sxs-lookup"><span data-stu-id="6cafc-104">**Summary:** Create and configure SharePoint Online team sites for various levels of information protection.</span></span>
  
<span data-ttu-id="6cafc-p101">Utilisez les étapes de cet article pour concevoir et déployer des sites d’équipe SharePoint Online de base de référence, sensibles et hautement confidentiels. Pour plus d’informations sur ces trois niveaux de protection, consultez [Sécuriser des sites et des fichiers SharePoint Online](/security/office-365-security/secure-sharepoint-online-sites-and-files.md).</span><span class="sxs-lookup"><span data-stu-id="6cafc-p101">Use the steps in this article to design and deploy baseline, sensitive, and highly confidential SharePoint Online team sites. For more information about these three tiers of protection, see [Secure SharePoint Online sites and files](/security/office-365-security/secure-sharepoint-online-sites-and-files.md).</span></span>
  
## <a name="baseline-sharepoint-online-team-sites"></a><span data-ttu-id="6cafc-107">Sites d’équipe SharePoint Online de base de référence</span><span class="sxs-lookup"><span data-stu-id="6cafc-107">Baseline SharePoint Online team sites</span></span>

<span data-ttu-id="6cafc-p102">La protection Base de référence inclut les sites d’équipe publics et privés. Les sites d’équipe publics peuvent être découverts et sont accessibles par toute personne de l’organisation. Les sites privés peuvent être découverts et sont accessibles seulement par les membres du groupe Office 365 associé au site d’équipe. Ces deux types de sites d’équipe permettent aux membres de partager le site avec d’autres utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="6cafc-p102">Baseline protection includes both public and private team sites. Public team sites can be discovered and accessed by anybody in the organization. Private sites can only be discovered and accessed by members of the Office 365 group associated with the team site. Both of these types of team sites allow members to share the site with others.</span></span>
  
### <a name="public"></a><span data-ttu-id="6cafc-112">Public</span><span class="sxs-lookup"><span data-stu-id="6cafc-112">Public</span></span>

<span data-ttu-id="6cafc-113">Pour créer un site d’équipe SharePoint Online de base de référence avec un accès et des autorisations publics, procédez comme suit :</span><span class="sxs-lookup"><span data-stu-id="6cafc-113">To create a baseline SharePoint Online team site with public access and permissions, do the following:</span></span>
  
1. <span data-ttu-id="6cafc-114">Connectez-vous au centre d’administration avec un compte qui servira également à gérer le site d’équipe SharePoint Online (par un administrateur SharePoint Online).</span><span class="sxs-lookup"><span data-stu-id="6cafc-114">Sign in to the admin center with an account that will also be used to administer the SharePoint Online team site (a SharePoint Online administrator).</span></span> <span data-ttu-id="6cafc-115">Pour obtenir de l’aide, consultez [Où se connecter à Office 365](https://support.office.com/Article/Where-to-sign-in-to-Office-365-e9eb7d51-5430-4929-91ab-6157c5a050b4).</span><span class="sxs-lookup"><span data-stu-id="6cafc-115">For help, see [Where to sign in to Office 365](https://support.office.com/Article/Where-to-sign-in-to-Office-365-e9eb7d51-5430-4929-91ab-6157c5a050b4).</span></span>
    
2. <span data-ttu-id="6cafc-116">Dans la liste des vignettes, cliquez sur **SharePoint**.</span><span class="sxs-lookup"><span data-stu-id="6cafc-116">In the list of tiles, click **SharePoint**.</span></span>
    
3. <span data-ttu-id="6cafc-117">Sous le nouvel onglet **SharePoint** de votre navigateur, cliquez sur **+ Créer un site**.</span><span class="sxs-lookup"><span data-stu-id="6cafc-117">On the new **SharePoint** tab in your browser, click **+ Create site**.</span></span>
    
4. <span data-ttu-id="6cafc-118">Dans la page **Créer un site**, cliquez sur **Site d’équipe**.</span><span class="sxs-lookup"><span data-stu-id="6cafc-118">On the **Create a site** page, click **Team site**.</span></span>
    
5. <span data-ttu-id="6cafc-119">Dans **Nom du Site**, tapez un nom pour le site d’équipe public.</span><span class="sxs-lookup"><span data-stu-id="6cafc-119">In **Site name**, type a name for the public team site.</span></span> 
    
6. <span data-ttu-id="6cafc-120">Dans **Description du site d’équipe**, tapez une description de l’objectif du site.</span><span class="sxs-lookup"><span data-stu-id="6cafc-120">In **Team site description**, type a description of the purpose of the site.</span></span>
    
7. <span data-ttu-id="6cafc-121">Dans **Paramètres de confidentialité**, sélectionnez **Public - tout le monde dans l’organisation peut accéder à ce site**, puis cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="6cafc-121">In **Privacy settings**, select **Public - anyone in the organization can access this site**, and then click **Next**.</span></span>
    
8. <span data-ttu-id="6cafc-122">Dans le volet **Qui voulez-vous ajouter ?**, cliquez sur **Terminer**.</span><span class="sxs-lookup"><span data-stu-id="6cafc-122">On the **Who do you want to add?** pane, click **Finish**.</span></span>
    
<span data-ttu-id="6cafc-123">Voici la configuration finale.</span><span class="sxs-lookup"><span data-stu-id="6cafc-123">Here is your resulting configuration.</span></span>
  
![Protection de base pour un site d’équipe SharePoint Online public.](media/bcd46b8d-3f89-4398-80ce-4da17ee85e03.png)
  
### <a name="private"></a><span data-ttu-id="6cafc-125">Private</span><span class="sxs-lookup"><span data-stu-id="6cafc-125">Private</span></span>

<span data-ttu-id="6cafc-126">Pour créer un site d’équipe SharePoint Online de base de référence avec un accès et des autorisations privés, procédez comme suit :</span><span class="sxs-lookup"><span data-stu-id="6cafc-126">To create a baseline SharePoint Online team site with private access and permissions, do the following:</span></span>
  
1. <span data-ttu-id="6cafc-127">Connectez-vous au centre d’administration avec un compte qui servira également à gérer le site d’équipe SharePoint Online (par un administrateur SharePoint Online).</span><span class="sxs-lookup"><span data-stu-id="6cafc-127">Sign in to the admin center with an account that will also be used to administer the SharePoint Online team site (a SharePoint Online administrator).</span></span> <span data-ttu-id="6cafc-128">Pour obtenir de l’aide, consultez [Où se connecter à Office 365](https://support.office.com/Article/Where-to-sign-in-to-Office-365-e9eb7d51-5430-4929-91ab-6157c5a050b4).</span><span class="sxs-lookup"><span data-stu-id="6cafc-128">For help, see [Where to sign in to Office 365](https://support.office.com/Article/Where-to-sign-in-to-Office-365-e9eb7d51-5430-4929-91ab-6157c5a050b4).</span></span>
    
2. <span data-ttu-id="6cafc-129">Dans la liste des vignettes, cliquez sur **SharePoint**.</span><span class="sxs-lookup"><span data-stu-id="6cafc-129">In the list of tiles, click **SharePoint**.</span></span>
    
3. <span data-ttu-id="6cafc-130">Sous le nouvel onglet **SharePoint** de votre navigateur, cliquez sur **+ Créer un site**.</span><span class="sxs-lookup"><span data-stu-id="6cafc-130">On the new **SharePoint** tab in your browser, click **+ Create site**.</span></span>
    
4. <span data-ttu-id="6cafc-131">Dans la page **Créer un site**, cliquez sur **Site d’équipe**.</span><span class="sxs-lookup"><span data-stu-id="6cafc-131">On the **Create a site** page, click **Team site**.</span></span>
    
5. <span data-ttu-id="6cafc-132">Dans **Nom du site**, tapez un nom pour le site d’équipe privé.</span><span class="sxs-lookup"><span data-stu-id="6cafc-132">In **Site name**, type a name for the private team site.</span></span> 
    
6. <span data-ttu-id="6cafc-133">Dans **Description du site d’équipe**, tapez une description de l’objectif du site.</span><span class="sxs-lookup"><span data-stu-id="6cafc-133">In **Team site description,** type a description of the purpose of the site.</span></span>
    
7. <span data-ttu-id="6cafc-134">Dans **Paramètres de confidentialité**, sélectionnez **Privé - Seuls les membres peuvent accéder à ce site**, puis cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="6cafc-134">In **Privacy settings**, select **Private - only members can access this site**, and then click **Next**.</span></span>
    
8. <span data-ttu-id="6cafc-135">Dans le volet **Qui voulez-vous ajouter ?**, dans **Ajouter des membres**, tapez les noms des comptes d’utilisateurs qui ont accès à ce site d’équipe privé.</span><span class="sxs-lookup"><span data-stu-id="6cafc-135">On the **Who do you want to add?** pane, in **Add members**, type the names of user accounts that have access to this private team site.</span></span>
    
9. <span data-ttu-id="6cafc-136">Quand vous avez fini d’ajouter l’ensemble initial des membres au site, cliquez sur **Terminer**.</span><span class="sxs-lookup"><span data-stu-id="6cafc-136">When you are done adding the initial set of members to the site, click **Finish**</span></span>
    
<span data-ttu-id="6cafc-137">Voici la configuration finale.</span><span class="sxs-lookup"><span data-stu-id="6cafc-137">Here is your resulting configuration.</span></span>
  
![Protection de base pour le site d’équipe SharePoint Online privé.](media/91769026-37e3-4383-ac3c-dbf7aca98e41.png)
  
## <a name="sensitive-sharepoint-online-team-sites"></a><span data-ttu-id="6cafc-139">Sites d’équipe SharePoint Online sensibles</span><span class="sxs-lookup"><span data-stu-id="6cafc-139">Sensitive SharePoint Online team sites</span></span>

<span data-ttu-id="6cafc-140">Un site d’équipe SharePoint Online sensible est un site d’équipe isolé. En d’autres termes, les autorisations sont contrôlées selon l’appartenance de l’utilisateur à des groupes SharePoint, et non selon son appartenance au groupe Office 365 associé au site d’équipe.</span><span class="sxs-lookup"><span data-stu-id="6cafc-140">A sensitive SharePoint Online team site is an isolated team site, which means that permissions are controlled through membership in SharePoint groups instead of membership in the Office 365 group associated with the team site.</span></span>
  
<span data-ttu-id="6cafc-141">La création d’un site d’équipe isolé se déroule en deux étapes.</span><span class="sxs-lookup"><span data-stu-id="6cafc-141">To create an isolated team site, there are two main steps.</span></span>
  
### <a name="step-1-design-your-isolated-site"></a><span data-ttu-id="6cafc-142">Étape 1 : Concevoir votre site isolé</span><span class="sxs-lookup"><span data-stu-id="6cafc-142">Step 1: Design your isolated site</span></span>

<span data-ttu-id="6cafc-143">Pour concevoir votre site d’équipe isolé, vous devez déterminer :</span><span class="sxs-lookup"><span data-stu-id="6cafc-143">To design your isolated team site, you need to determine:</span></span>
  
- <span data-ttu-id="6cafc-144">Vos groupes et vos niveaux d’autorisation SharePoint.</span><span class="sxs-lookup"><span data-stu-id="6cafc-144">Your SharePoint groups and permission levels.</span></span>
    
- <span data-ttu-id="6cafc-145">L’ensemble de groupes d’accès qui seront membres de vos groupes SharePoint.</span><span class="sxs-lookup"><span data-stu-id="6cafc-145">The set of access groups that will be members of your SharePoint groups.</span></span>
    
     <span data-ttu-id="6cafc-146">L’ensemble de groupes d’accès recommandé est le suivant : un pour les membres du site, un pour les personnes consultant le site et un pour les administrateurs du site.</span><span class="sxs-lookup"><span data-stu-id="6cafc-146">The recommended set of access groups is one for site members, one for site viewers, and one for site administrators.</span></span>
    
- <span data-ttu-id="6cafc-147">Si vous utilisez des groupes imbriqués au sein de vos groupes d’accès.</span><span class="sxs-lookup"><span data-stu-id="6cafc-147">Whether you will use nested groups within your access groups.</span></span>
    
<span data-ttu-id="6cafc-148">Par exemple, la structure des groupes et les niveaux d’autorisations recommandés se présentent comme ceci :</span><span class="sxs-lookup"><span data-stu-id="6cafc-148">For example, the recommended group structure and permission levels look like this:</span></span>
  
|<span data-ttu-id="6cafc-149">**Groupe SharePoint**</span><span class="sxs-lookup"><span data-stu-id="6cafc-149">**SharePoint group**</span></span>|<span data-ttu-id="6cafc-150">**Niveau d’autorisation**</span><span class="sxs-lookup"><span data-stu-id="6cafc-150">**Permission level**</span></span>|<span data-ttu-id="6cafc-151">**Groupe d’accès (exemples)**</span><span class="sxs-lookup"><span data-stu-id="6cafc-151">**Access group (examples)**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="6cafc-152">Membres de [nom du site]</span><span class="sxs-lookup"><span data-stu-id="6cafc-152">[site name] Members</span></span>  <br/> |<span data-ttu-id="6cafc-153">Éditer</span><span class="sxs-lookup"><span data-stu-id="6cafc-153">Edit</span></span>  <br/> |<span data-ttu-id="6cafc-154">Membres de [nom du site]</span><span class="sxs-lookup"><span data-stu-id="6cafc-154">[site name] Members</span></span>  <br/> |
|<span data-ttu-id="6cafc-155">Visiteurs de [nom du site]</span><span class="sxs-lookup"><span data-stu-id="6cafc-155">[site name] Visitors</span></span>  <br/> |<span data-ttu-id="6cafc-156">Lire</span><span class="sxs-lookup"><span data-stu-id="6cafc-156">Read</span></span>  <br/> |<span data-ttu-id="6cafc-157">Personnes consultant [nom du site]</span><span class="sxs-lookup"><span data-stu-id="6cafc-157">[site name] Viewers</span></span>  <br/> |
|<span data-ttu-id="6cafc-158">Propriétaires de [nom du site]</span><span class="sxs-lookup"><span data-stu-id="6cafc-158">[site name] Owners</span></span>  <br/> |<span data-ttu-id="6cafc-159">Contrôle total</span><span class="sxs-lookup"><span data-stu-id="6cafc-159">Full control</span></span>  <br/> |<span data-ttu-id="6cafc-160">Administrateurs de [nom du site]</span><span class="sxs-lookup"><span data-stu-id="6cafc-160">[site name] Admins</span></span>  <br/> |
   
<span data-ttu-id="6cafc-p105">Les groupes et les niveaux d’autorisation SharePoint sont créés par défaut pour un site d’équipe. Vous devez déterminer les noms de vos groupes d’accès.</span><span class="sxs-lookup"><span data-stu-id="6cafc-p105">The SharePoint groups and permission levels are created by default for a team site. You need to determine the names of your access groups.</span></span>
  
<span data-ttu-id="6cafc-163">Pour plus d’informations sur le processus de conception, consultez [Concevoir un site d’équipe SharePoint Online isolé](/security/office-365-security/design-an-isolated-sharepoint-online-team-site.md).</span><span class="sxs-lookup"><span data-stu-id="6cafc-163">For the details of the design process, see [Design an isolated SharePoint Online team site](/security/office-365-security/design-an-isolated-sharepoint-online-team-site.md).</span></span>
  
### <a name="step-2-deploy-your-isolated-site"></a><span data-ttu-id="6cafc-164">Étape 2 : Déployer votre site isolé</span><span class="sxs-lookup"><span data-stu-id="6cafc-164">Step 2: Deploy your isolated site</span></span>

<span data-ttu-id="6cafc-165">Pour déployer votre site isolé, vous devez d’abord :</span><span class="sxs-lookup"><span data-stu-id="6cafc-165">To deploy your isolated site, you first need to:</span></span>
  
- <span data-ttu-id="6cafc-166">Déterminer les comptes d’utilisateur et les groupes à ajouter à chacun de vos groupes d’accès.</span><span class="sxs-lookup"><span data-stu-id="6cafc-166">Determine the user accounts and groups to add to each of your access groups.</span></span>
    
- <span data-ttu-id="6cafc-167">Créer les groupes d’accès, et ajouter les utilisateurs et les groupes membres.</span><span class="sxs-lookup"><span data-stu-id="6cafc-167">Create the access groups and add the user and group members.</span></span>
    
<span data-ttu-id="6cafc-168">Pour la procédure détaillée, consultez la **phase 1** de [Déployer un site d’équipe SharePoint Online isolé](/security/office-365-security/design-an-isolated-sharepoint-online-team-site.md).</span><span class="sxs-lookup"><span data-stu-id="6cafc-168">For the detailed steps, see **Phase 1** of [Deploy an isolated SharePoint Online team site](/security/office-365-security/design-an-isolated-sharepoint-online-team-site.md).</span></span>
  
<span data-ttu-id="6cafc-169">Ensuite, vous devez créer le site d’équipe SharePoint Online en suivant ces étapes.</span><span class="sxs-lookup"><span data-stu-id="6cafc-169">Next, you create the SharePoint Online team site with these steps.</span></span>
  
1. <span data-ttu-id="6cafc-170">Connectez-vous au centre d’administration avec un compte qui servira également à gérer le site d’équipe SharePoint Online (par un administrateur SharePoint Online).</span><span class="sxs-lookup"><span data-stu-id="6cafc-170">Sign in to the admin center with an account that will also be used to administer the SharePoint Online team site (a SharePoint Online administrator).</span></span> <span data-ttu-id="6cafc-171">Pour obtenir de l’aide, consultez [Où se connecter à Office 365](https://support.office.com/Article/Where-to-sign-in-to-Office-365-e9eb7d51-5430-4929-91ab-6157c5a050b4).</span><span class="sxs-lookup"><span data-stu-id="6cafc-171">For help, see [Where to sign in to Office 365](https://support.office.com/Article/Where-to-sign-in-to-Office-365-e9eb7d51-5430-4929-91ab-6157c5a050b4).</span></span>
    
2. <span data-ttu-id="6cafc-172">Dans la liste des vignettes, cliquez sur **SharePoint**.</span><span class="sxs-lookup"><span data-stu-id="6cafc-172">In the list of tiles, click **SharePoint**.</span></span>
    
3. <span data-ttu-id="6cafc-173">Sous le nouvel onglet **SharePoint** de votre navigateur, cliquez sur **+ Créer un site**.</span><span class="sxs-lookup"><span data-stu-id="6cafc-173">In the new **SharePoint** tab of your browser, click **+ Create site**.</span></span>
    
4. <span data-ttu-id="6cafc-174">Dans la page **Créer un site**, cliquez sur **Site d’équipe**.</span><span class="sxs-lookup"><span data-stu-id="6cafc-174">On the **Create a site** page, click **Team site**.</span></span>
    
5. <span data-ttu-id="6cafc-175">Dans **Nom du site**, tapez un nom pour le site d’équipe privé.</span><span class="sxs-lookup"><span data-stu-id="6cafc-175">In **Site name**, type a name for the private team site.</span></span>
    
6. <span data-ttu-id="6cafc-176">Dans **Description du site d’équipe**, tapez une description facultative.</span><span class="sxs-lookup"><span data-stu-id="6cafc-176">In **Team site description**, type an optional description.</span></span>
    
7. <span data-ttu-id="6cafc-177">Dans **Paramètres de confidentialité**, sélectionnez **Privé - Seuls les membres peuvent accéder à ce site**, puis cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="6cafc-177">In **Privacy settings**, select **Private - only members can access this site**, and then click **Next**.</span></span>
    
8. <span data-ttu-id="6cafc-178">Dans le volet **Qui voulez-vous ajouter ?**, cliquez sur **Terminer**.</span><span class="sxs-lookup"><span data-stu-id="6cafc-178">On the **Who do you want to add?** pane, click **Finish**.</span></span>
    
<span data-ttu-id="6cafc-179">Ensuite, dans le nouveau site d’équipe SharePoint Online, configurez les autorisations en suivant ces étapes.</span><span class="sxs-lookup"><span data-stu-id="6cafc-179">Next, from the new SharePoint Online team site, configure permissions with these steps.</span></span>
  
1. <span data-ttu-id="6cafc-180">Choisissez le Nom d’utilisateur principal (UPN) de l’administrateur informatique ou d’une autre personne qui sera chargée de répondre aux demandes d’accès au site (belindan@contoso.com est un exemple d’UPN).</span><span class="sxs-lookup"><span data-stu-id="6cafc-180">Determine the User Principal Name (UPN) of the IT administrator or other person who will be responsible for responding to and addressing requests for access to the site (belindan@contoso.com is an example of a UPN).</span></span> 
    
2. <span data-ttu-id="6cafc-181">Dans la barre d’outils, cliquez sur l’icône Paramètres, puis cliquez sur **Paramètres du site**.</span><span class="sxs-lookup"><span data-stu-id="6cafc-181">In the tool bar, click the settings icon, and then click **Site permissions**.</span></span>
    
3. <span data-ttu-id="6cafc-182">Dans le volet **Autorisations du site**, cliquez sur **Paramètres d’autorisations avancés**.</span><span class="sxs-lookup"><span data-stu-id="6cafc-182">In the **Site permissions** pane, click **Advanced permissions settings**.</span></span>
    
4. <span data-ttu-id="6cafc-183">Sous le nouvel onglet **Autorisations** dans votre navigateur, cliquez sur **Paramètres des demandes d’accès**.</span><span class="sxs-lookup"><span data-stu-id="6cafc-183">On the new **Permissions** tab of your browser, click **Access Request Settings**.</span></span>
    
5. <span data-ttu-id="6cafc-184">Dans la boîte de dialogue **Paramètres des demandes d’accès** :</span><span class="sxs-lookup"><span data-stu-id="6cafc-184">In the **Access Requests Settings** dialog box:</span></span>
    
  - <span data-ttu-id="6cafc-185">Décochez les cases **Autoriser les membres à partager le site, ainsi que des fichiers et dossiers individuels** et **Autoriser les membres à inviter d’autres personnes sur le groupe de membres du site**.</span><span class="sxs-lookup"><span data-stu-id="6cafc-185">Clear the **Allow members to share the site and individual files and folders** and **Allow members to invite others to the site members group** check boxes.</span></span>
    
  - <span data-ttu-id="6cafc-186">Tapez le nom d’utilisateur principal de votre administrateur informatique de l’étape 1 dans **Envoyer toutes les demandes d’accès**.</span><span class="sxs-lookup"><span data-stu-id="6cafc-186">Type the UPN of your IT administrator from step 1 in **Send all requests for access**.</span></span>
    
  - <span data-ttu-id="6cafc-187">Cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="6cafc-187">Click **OK**.</span></span>
    
6. <span data-ttu-id="6cafc-188">Sous l’onglet **Autorisations** de votre navigateur, cliquez sur **Membres de [nom du site]** dans la liste.</span><span class="sxs-lookup"><span data-stu-id="6cafc-188">On the **Permissions** tab of your browser, click **[site name] Members** in the list.</span></span>
    
7. <span data-ttu-id="6cafc-189">Dans **Personnes et groupes**, cliquez sur **Nouveau**.</span><span class="sxs-lookup"><span data-stu-id="6cafc-189">In **People and Groups**, click **New**.</span></span>
    
8. <span data-ttu-id="6cafc-190">Dans la boîte de dialogue **Partager**, tapez le nom du groupe d’accès des membres de site pour ce site, sélectionnez-le, puis cliquez sur **Partager**.</span><span class="sxs-lookup"><span data-stu-id="6cafc-190">In the **Share** dialog box, type the name of your site members access group for this site, select it, and then click **Share**.</span></span>
    
9. <span data-ttu-id="6cafc-191">Cliquez sur le bouton de retour de votre navigateur.</span><span class="sxs-lookup"><span data-stu-id="6cafc-191">Click the back button on your browser.</span></span>
    
10. <span data-ttu-id="6cafc-192">Cliquez sur **Propriétaires de [nom du site]** dans la liste.</span><span class="sxs-lookup"><span data-stu-id="6cafc-192">Click **[site name] Owners** in the list.</span></span>
    
11. <span data-ttu-id="6cafc-193">Dans **Personnes et groupes**, cliquez sur **Nouveau**.</span><span class="sxs-lookup"><span data-stu-id="6cafc-193">In **People and Groups**, click **New**.</span></span>
    
12. <span data-ttu-id="6cafc-194">Dans la boîte de dialogue **Partager**, tapez le nom du groupe d’accès des administrateurs de site pour ce site, sélectionnez-le, puis cliquez sur **Partager**.</span><span class="sxs-lookup"><span data-stu-id="6cafc-194">In the **Share** dialog box, type the name of the site administrators access group for this site, select it, and then click **Share**.</span></span>
    
13. <span data-ttu-id="6cafc-195">Cliquez sur le bouton de retour de votre navigateur.</span><span class="sxs-lookup"><span data-stu-id="6cafc-195">Click the back button on your browser.</span></span>
    
14. <span data-ttu-id="6cafc-196">Cliquez sur **Visiteurs de [nom du site]** dans la liste.</span><span class="sxs-lookup"><span data-stu-id="6cafc-196">Click **[site name] Visitors** in the list.</span></span>
    
15. <span data-ttu-id="6cafc-197">Dans **Personnes et groupes**, cliquez sur **Nouveau**.</span><span class="sxs-lookup"><span data-stu-id="6cafc-197">In **People and Groups**, click **New**.</span></span>
    
16. <span data-ttu-id="6cafc-198">Dans la boîte de dialogue **Partager**, tapez le nom du groupe d’accès des personnes consultant ce site, sélectionnez-le, puis cliquez sur **Partager**.</span><span class="sxs-lookup"><span data-stu-id="6cafc-198">In the **Share** dialog box, type the name of the site viewers access group for this site, select it, and then click **Share**.</span></span>
    
17. <span data-ttu-id="6cafc-199">Fermez l’onglet **Autorisations** de votre navigateur.</span><span class="sxs-lookup"><span data-stu-id="6cafc-199">Close the **Permissions** tab of your browser.</span></span>
    
<span data-ttu-id="6cafc-200">Voici les résultats que vous devez escompter :</span><span class="sxs-lookup"><span data-stu-id="6cafc-200">The results of these permission settings are:</span></span>
  
- <span data-ttu-id="6cafc-201">Le groupe SharePoint **Propriétaires de [nom du site]** contient le groupe d’accès Administrateurs du site, dans lequel tous les membres ont le niveau d’autorisation **Contrôle total**.</span><span class="sxs-lookup"><span data-stu-id="6cafc-201">The **[site name] Owners** SharePoint group contains the site administrators access group, in which all the members have the **Full control** permission level.</span></span>
    
- <span data-ttu-id="6cafc-202">Le groupe SharePoint **Membres de [nom du site]** contient le groupe d’accès Membres du site, dans lequel tous les membres ont le niveau d’autorisation **Modifier**.</span><span class="sxs-lookup"><span data-stu-id="6cafc-202">The **[site name] Members** SharePoint group contains the site members access group, in which all the members have the **Edit** permission level.</span></span>
    
- <span data-ttu-id="6cafc-203">Le groupe SharePoint **Visiteurs de [nom du site]** contient le groupe d’accès Visiteurs du site, dans lequel tous les membres ont le niveau d’autorisation **Lire**.</span><span class="sxs-lookup"><span data-stu-id="6cafc-203">The **[site name] Visitors** SharePoint group contains the site viewers access group, in which all the members have the **Read** permission level.</span></span>
    
- <span data-ttu-id="6cafc-204">La possibilité pour les membres d’inviter d’autres membres est désactivée.</span><span class="sxs-lookup"><span data-stu-id="6cafc-204">The ability for members to invite other members is disabled.</span></span>
    
- <span data-ttu-id="6cafc-205">La possibilité pour les non-membres de demander l’accès est activée.</span><span class="sxs-lookup"><span data-stu-id="6cafc-205">The ability for non-members to request access is enabled.</span></span>
    
<span data-ttu-id="6cafc-206">Voici la configuration finale.</span><span class="sxs-lookup"><span data-stu-id="6cafc-206">Here is your resulting configuration.</span></span>
  
![Protection des données sensibles d’un site d’équipe SharePoint Online isolé.](media/7a6ab9c6-560a-4674-ac39-8175644dbe6f.png)
  
<span data-ttu-id="6cafc-208">Les membres du site, via l’appartenance à un des groupes d’accès, peuvent désormais collaborer sur les ressources du site de façon sécurisée.</span><span class="sxs-lookup"><span data-stu-id="6cafc-208">The members of the site, through group membership in one of the access groups, can now securely collaborate on the resources of the site.</span></span>
  
## <a name="highly-confidential-sharepoint-online-team-sites"></a><span data-ttu-id="6cafc-209">Sites d’équipe SharePoint Online hautement confidentiels</span><span class="sxs-lookup"><span data-stu-id="6cafc-209">Highly confidential SharePoint Online team sites</span></span>

<span data-ttu-id="6cafc-210">Un site d’équipe SharePoint Online hautement confidentiel est un site d’équipe isolé, ce qui signifie que les autorisations sont contrôlées via l’appartenance à des groupes SharePoint, au lieu de l’appartenance au groupe Office 365 associé au site d’équipe.</span><span class="sxs-lookup"><span data-stu-id="6cafc-210">A highly confidential SharePoint Online team site is an isolated team site, which means that permissions are controlled through membership in SharePoint groups instead of membership in the Office 365 group associated with the team site.</span></span>
  
<span data-ttu-id="6cafc-211">Pour créer un site d’équipe isolé pour des informations et une collaboration hautement confidentielles, vous devez procéder en deux étapes principales.</span><span class="sxs-lookup"><span data-stu-id="6cafc-211">To create an isolated team site for highly confidential information and collaboration, there are two main steps.</span></span>
  
### <a name="step-1-design-your-isolated-site"></a><span data-ttu-id="6cafc-212">Étape 1 : Concevoir votre site isolé</span><span class="sxs-lookup"><span data-stu-id="6cafc-212">Step 1: Design your isolated site</span></span>

<span data-ttu-id="6cafc-213">Pour concevoir votre site d’équipe isolé, vous devez déterminer :</span><span class="sxs-lookup"><span data-stu-id="6cafc-213">To design your isolated team site, you need to determine:</span></span>
  
- <span data-ttu-id="6cafc-214">Vos groupes et vos niveaux d’autorisation SharePoint.</span><span class="sxs-lookup"><span data-stu-id="6cafc-214">Your SharePoint groups and permission levels.</span></span>
    
- <span data-ttu-id="6cafc-215">L’ensemble de groupes d’accès qui seront membres de vos groupes SharePoint.</span><span class="sxs-lookup"><span data-stu-id="6cafc-215">The set of access groups that will be members of your SharePoint groups.</span></span>
    
     <span data-ttu-id="6cafc-216">L’ensemble de groupes d’accès recommandé est le suivant : un pour les membres du site, un pour les personnes consultant le site et un pour les administrateurs du site.</span><span class="sxs-lookup"><span data-stu-id="6cafc-216">The recommended set of access groups is one for site members, one for site viewers, and one for site administrators.</span></span>
    
- <span data-ttu-id="6cafc-217">Si vous utilisez des groupes imbriqués au sein de vos groupes d’accès.</span><span class="sxs-lookup"><span data-stu-id="6cafc-217">Whether you will use nested groups within your access groups.</span></span>
    
<span data-ttu-id="6cafc-218">Par exemple, la structure des groupes et les niveaux d’autorisations recommandés se présentent comme ceci :</span><span class="sxs-lookup"><span data-stu-id="6cafc-218">For example, the recommended group structure and permission levels look like this:</span></span>
  
|<span data-ttu-id="6cafc-219">**Groupe SharePoint**</span><span class="sxs-lookup"><span data-stu-id="6cafc-219">**SharePoint group**</span></span>|<span data-ttu-id="6cafc-220">**Niveau d’autorisation**</span><span class="sxs-lookup"><span data-stu-id="6cafc-220">**Permission level**</span></span>|<span data-ttu-id="6cafc-221">**Groupe d’accès (exemples)**</span><span class="sxs-lookup"><span data-stu-id="6cafc-221">**Access group (examples)**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="6cafc-222">Membres de [nom du site]</span><span class="sxs-lookup"><span data-stu-id="6cafc-222">[site name] Members</span></span>  <br/> |<span data-ttu-id="6cafc-223">Éditer</span><span class="sxs-lookup"><span data-stu-id="6cafc-223">Edit</span></span>  <br/> |<span data-ttu-id="6cafc-224">Membres de [nom du site]</span><span class="sxs-lookup"><span data-stu-id="6cafc-224">[site name] Members</span></span>  <br/> |
|<span data-ttu-id="6cafc-225">Visiteurs de [nom du site]</span><span class="sxs-lookup"><span data-stu-id="6cafc-225">[site name] Visitors</span></span>  <br/> |<span data-ttu-id="6cafc-226">Lire</span><span class="sxs-lookup"><span data-stu-id="6cafc-226">Read</span></span>  <br/> |<span data-ttu-id="6cafc-227">Personnes consultant [nom du site]</span><span class="sxs-lookup"><span data-stu-id="6cafc-227">[site name] Viewers</span></span>  <br/> |
|<span data-ttu-id="6cafc-228">Propriétaires de [nom du site]</span><span class="sxs-lookup"><span data-stu-id="6cafc-228">[site name] Owners</span></span>  <br/> |<span data-ttu-id="6cafc-229">Contrôle total</span><span class="sxs-lookup"><span data-stu-id="6cafc-229">Full control</span></span>  <br/> |<span data-ttu-id="6cafc-230">Administrateurs de [nom du site]</span><span class="sxs-lookup"><span data-stu-id="6cafc-230">[site name] Admins</span></span>  <br/> |
   
<span data-ttu-id="6cafc-p107">Les groupes et les niveaux d’autorisation SharePoint sont créés par défaut pour un site d’équipe. Vous devez déterminer les noms de vos groupes d’accès.</span><span class="sxs-lookup"><span data-stu-id="6cafc-p107">The SharePoint groups and permission levels are created by default for a team site. You need to determine the names of your access groups.</span></span>
  
<span data-ttu-id="6cafc-233">Pour plus d’informations sur le processus de conception, consultez [Concevoir un site d’équipe SharePoint Online isolé](/security/office-365-security/design-an-isolated-sharepoint-online-team-site.md).</span><span class="sxs-lookup"><span data-stu-id="6cafc-233">For the details of the design process, see [Design an isolated SharePoint Online team site](/security/office-365-security/design-an-isolated-sharepoint-online-team-site.md).</span></span>
  
### <a name="step-2-deploy-your-isolated-site"></a><span data-ttu-id="6cafc-234">Étape 2 : Déployer votre site isolé</span><span class="sxs-lookup"><span data-stu-id="6cafc-234">Step 2: Deploy your isolated site</span></span>

<span data-ttu-id="6cafc-235">Pour déployer votre site isolé, vous devez d’abord :</span><span class="sxs-lookup"><span data-stu-id="6cafc-235">To deploy your isolated site, you first need to:</span></span>
  
- <span data-ttu-id="6cafc-236">déterminer les utilisateurs et les membres du groupe de chacun de vos groupes d’accès ;</span><span class="sxs-lookup"><span data-stu-id="6cafc-236">Determine the user and group members of each of your access groups</span></span>
    
- <span data-ttu-id="6cafc-237">créer les groupes d’accès et ajouter les utilisateurs et les membres du groupe ;</span><span class="sxs-lookup"><span data-stu-id="6cafc-237">Create the access groups and add the user and group members</span></span>
    
- <span data-ttu-id="6cafc-238">créer un site d’équipe isolé qui utilise vos groupes d’accès.</span><span class="sxs-lookup"><span data-stu-id="6cafc-238">Create an isolated team site that uses your access groups</span></span>
    
<span data-ttu-id="6cafc-239">Pour la procédure détaillée, consultez [Déployer un site d’équipe SharePoint Online isolé](/security/office-365-security/design-an-isolated-sharepoint-online-team-site.md).</span><span class="sxs-lookup"><span data-stu-id="6cafc-239">For the detailed steps, see [Deploy an isolated SharePoint Online team site](/security/office-365-security/design-an-isolated-sharepoint-online-team-site.md).</span></span>
  
<span data-ttu-id="6cafc-240">Voici les résultats que vous devez escompter :</span><span class="sxs-lookup"><span data-stu-id="6cafc-240">The results of the permission settings are:</span></span>
  
- <span data-ttu-id="6cafc-241">Le groupe SharePoint **Propriétaires de [nom du site]** contient le groupe d’accès Administrateurs du site, dans lequel tous les membres ont le niveau d’autorisation **Contrôle total**.</span><span class="sxs-lookup"><span data-stu-id="6cafc-241">The **[site name] Owners** SharePoint group contains the site administrators access group, in which all the members have the **Full control** permission level.</span></span>
    
- <span data-ttu-id="6cafc-242">Le groupe SharePoint **Membres de [nom du site]** contient le groupe d’accès Membres du site, dans lequel tous les membres ont le niveau d’autorisation **Modifier**.</span><span class="sxs-lookup"><span data-stu-id="6cafc-242">The **[site name] Members** SharePoint group contains the site members access group, in which all the members have the **Edit** permission level.</span></span>
    
- <span data-ttu-id="6cafc-243">Le groupe SharePoint **Visiteurs de [nom du site]** contient le groupe d’accès Visiteurs du site, dans lequel tous les membres ont le niveau d’autorisation **Lire**.</span><span class="sxs-lookup"><span data-stu-id="6cafc-243">The **[site name] Visitors** SharePoint group contains the site viewers access group, in which all the members have the **Read** permission level.</span></span>
    
- <span data-ttu-id="6cafc-244">La possibilité pour les membres d’inviter d’autres membres est désactivée.</span><span class="sxs-lookup"><span data-stu-id="6cafc-244">The ability for members to invite other members is disabled.</span></span>
    
- <span data-ttu-id="6cafc-245">La possibilité pour les non-membres de demander l’accès est désactivée.</span><span class="sxs-lookup"><span data-stu-id="6cafc-245">The ability for non-members to request access is disabled.</span></span>
    
<span data-ttu-id="6cafc-246">Voici la configuration finale.</span><span class="sxs-lookup"><span data-stu-id="6cafc-246">Here is your resulting configuration.</span></span>
  
![Protection avec un niveau de confidentialité élevé pour un site d’équipe SharePoint Online isolé.](media/196359ab-d7ed-4fcf-97b4-61820a74aca4.png)
  
<span data-ttu-id="6cafc-248">Les membres du site, via l’appartenance à un des groupes d’accès, peuvent désormais collaborer sur les ressources du site de façon sécurisée.</span><span class="sxs-lookup"><span data-stu-id="6cafc-248">The members of the site, through group membership in one of the access groups, can now securely collaborate on the resources of the site.</span></span>
  
## <a name="next-step"></a><span data-ttu-id="6cafc-249">Étape suivante</span><span class="sxs-lookup"><span data-stu-id="6cafc-249">Next step</span></span>

[<span data-ttu-id="6cafc-250">Protéger les fichiers SharePoint Online avec des étiquettes Office 365 et la protection contre la perte de données</span><span class="sxs-lookup"><span data-stu-id="6cafc-250">Protect SharePoint Online files with Office 365 labels and DLP</span></span>](protect-sharepoint-online-files-with-office-365-labels-and-dlp.md)

## <a name="see-also"></a><span data-ttu-id="6cafc-251">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6cafc-251">See also</span></span>

[<span data-ttu-id="6cafc-252">Sécuriser les fichiers et sites SharePoint Online</span><span class="sxs-lookup"><span data-stu-id="6cafc-252">Secure SharePoint Online sites and files</span></span>](/security/office-365-security/secure-sharepoint-online-sites-and-files.md)
  
[<span data-ttu-id="6cafc-253">Conseils de sécurité Microsoft pour les campagnes électorales, les organisations à but non lucratif et d’autres organisations flexibles</span><span class="sxs-lookup"><span data-stu-id="6cafc-253">Microsoft Security Guidance for Political Campaigns, Nonprofits, and Other Agile Organizations</span></span>](/security/office-365-security/microsoft-security-guidance-for-political-campaigns-nonprofits-and-other-agile-o.md)
  
[<span data-ttu-id="6cafc-254">Adoption du cloud et solutions hybrides</span><span class="sxs-lookup"><span data-stu-id="6cafc-254">Cloud adoption and hybrid solutions</span></span>](https://docs.microsoft.com/office365/enterprise/cloud-adoption-and-hybrid-solutions)
