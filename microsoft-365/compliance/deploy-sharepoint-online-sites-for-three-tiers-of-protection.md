---
title: Déployer des sites SharePoint Online pour trois niveaux de protection
ms.author: josephd
author: JoeDavies-MSFT
manager: laurawi
ms.date: 11/27/2019
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Priority
search.appverid:
- MET150
ms.collection:
- Ent_O365
- Strat_O365_Enterprise
- SPO_Content
ms.custom:
- Ent_Solutions
ms.assetid: 1e8e3cfd-b878-4088-b941-9940363a5fae
description: 'Résumé : Créez et configurez des sites d’équipe SharePoint Online avec différents niveaux de protection des informations.'
ms.openlocfilehash: 1396a45103bfbaf6ea2de6c5ba6c4b086da344ec
ms.sourcegitcommit: 58a7bd70a4bcf52530baf5f82507fd5dc4455fd9
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/03/2019
ms.locfileid: "39668862"
---
# <a name="deploy-sharepoint-online-sites-for-three-tiers-of-protection"></a><span data-ttu-id="ae081-103">Déployer des sites SharePoint Online pour trois niveaux de protection</span><span class="sxs-lookup"><span data-stu-id="ae081-103">Deploy SharePoint Online sites for three tiers of protection</span></span>

<span data-ttu-id="ae081-p101">Utilisez les étapes de cet article pour concevoir et déployer des sites d’équipe SharePoint Online de base de référence, sensibles et hautement confidentiels. Pour plus d’informations sur ces trois niveaux de protection, consultez [Sécuriser des sites et des fichiers SharePoint Online](../security/office-365-security/secure-sharepoint-online-sites-and-files.md).</span><span class="sxs-lookup"><span data-stu-id="ae081-p101">Use the steps in this article to design and deploy baseline, sensitive, and highly confidential SharePoint Online team sites. For more information about these three tiers of protection, see [Secure SharePoint Online sites and files](../security/office-365-security/secure-sharepoint-online-sites-and-files.md).</span></span>
  
## <a name="baseline-sharepoint-online-team-sites"></a><span data-ttu-id="ae081-106">Sites d’équipe SharePoint Online de base de référence</span><span class="sxs-lookup"><span data-stu-id="ae081-106">Baseline SharePoint Online team sites</span></span>

<span data-ttu-id="ae081-p102">La protection Base de référence inclut les sites d’équipe publics et privés. Les sites d’équipe publics peuvent être découverts et sont accessibles par toute personne de l’organisation. Les sites privés peuvent être découverts et sont accessibles seulement par les membres du groupe Office 365 associé au site d’équipe. Ces deux types de sites d’équipe permettent aux membres de partager le site avec d’autres utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="ae081-p102">Baseline protection includes both public and private team sites. Public team sites can be discovered and accessed by anybody in the organization. Private sites can only be discovered and accessed by members of the Office 365 group associated with the team site. Both of these types of team sites allow members to share the site with others.</span></span>
  
### <a name="public"></a><span data-ttu-id="ae081-111">Public</span><span class="sxs-lookup"><span data-stu-id="ae081-111">Public</span></span>

<span data-ttu-id="ae081-112">Pour créer un site d’équipe SharePoint Online de base de référence avec un accès et des autorisations publics, suivez [ces instructions](https://support.office.com/article/create-a-team-site-in-sharepoint-ef10c1e7-15f3-42a3-98aa-b5972711777d).</span><span class="sxs-lookup"><span data-stu-id="ae081-112">To create a baseline SharePoint Online team site with public access and permissions, do the following:</span></span>

<span data-ttu-id="ae081-113">Voici la configuration finale.</span><span class="sxs-lookup"><span data-stu-id="ae081-113">Here is your resulting configuration.</span></span>
  
![Protection de base pour un site d’équipe SharePoint Online public.](media/bcd46b8d-3f89-4398-80ce-4da17ee85e03.png)
  
### <a name="private"></a><span data-ttu-id="ae081-115">Privé</span><span class="sxs-lookup"><span data-stu-id="ae081-115">Private</span></span>

<span data-ttu-id="ae081-116">Pour créer un site d’équipe SharePoint Online de base de référence avec un accès et des autorisations privés, suivez [ces instructions](https://support.office.com/article/create-a-team-site-in-sharepoint-ef10c1e7-15f3-42a3-98aa-b5972711777d).</span><span class="sxs-lookup"><span data-stu-id="ae081-116">To create a baseline SharePoint Online team site with private access and permissions, do the following:</span></span>
  
<span data-ttu-id="ae081-117">Voici la configuration finale.</span><span class="sxs-lookup"><span data-stu-id="ae081-117">Here is your resulting configuration.</span></span>
  
![Protection de base pour le site d’équipe SharePoint Online privé.](media/91769026-37e3-4383-ac3c-dbf7aca98e41.png)
  
## <a name="sensitive-sharepoint-online-team-sites"></a><span data-ttu-id="ae081-119">Sites d’équipe SharePoint Online sensibles</span><span class="sxs-lookup"><span data-stu-id="ae081-119">Sensitive SharePoint Online team sites</span></span>

<span data-ttu-id="ae081-120">Un site d’équipe SharePoint Online sensible démarre en tant que site d’équipe privé.</span><span class="sxs-lookup"><span data-stu-id="ae081-120">A sensitive SharePoint Online team site starts as a private team site.</span></span>
  
<span data-ttu-id="ae081-121">Commencez par créer le site d’équipe privé SharePoint Online en suivant [ces instructions](https://support.office.com/article/create-a-team-site-in-sharepoint-ef10c1e7-15f3-42a3-98aa-b5972711777d).</span><span class="sxs-lookup"><span data-stu-id="ae081-121">First, create the SharePoint Online team site with these steps.</span></span>

<span data-ttu-id="ae081-122">Ensuite, dans le nouveau site d’équipe SharePoint Online, configurez d’autres paramètres autorisations en suivant ces étapes.</span><span class="sxs-lookup"><span data-stu-id="ae081-122">Next, from the new SharePoint Online team site, configure permissions with these steps.</span></span>

1.  <span data-ttu-id="ae081-123">Dans la barre d’outils du site d’équipe SharePoint, cliquez sur l’icône Paramètres, puis cliquez sur **Autorisations du site**.</span><span class="sxs-lookup"><span data-stu-id="ae081-123">In the tool bar of the SharePoint team site, click the settings icon, and then click **Site permissions**.</span></span>
2.  <span data-ttu-id="ae081-124">Dans le volet **Autorisations de site**, sous **Paramètres de partage**, cliquez sur **Modifier les paramètres de partage**.</span><span class="sxs-lookup"><span data-stu-id="ae081-124">In the **Site permissions** pane, under **Sharing Settings**, click **Change sharing settings**.</span></span>
3.  <span data-ttu-id="ae081-125">Sous **Autorisations de partage**, sélectionnez **Seuls les propriétaires du site peuvent partager des fichiers, des dossiers et le site**, puis cliquez sur **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="ae081-125">Under **Sharing permissions**, choose **Only site owners can share files, folders, and the site**, and then click **Save**.</span></span>

<span data-ttu-id="ae081-126">Voici les résultats que vous devez escompter :</span><span class="sxs-lookup"><span data-stu-id="ae081-126">The results of these permission settings are:</span></span>

- <span data-ttu-id="ae081-127">La possibilité pour les membres de partager avec d’autres membres est désactivée.</span><span class="sxs-lookup"><span data-stu-id="ae081-127">The ability for members to invite other members is disabled.</span></span>
- <span data-ttu-id="ae081-128">La possibilité pour les non-membres de demander l’accès est activée.</span><span class="sxs-lookup"><span data-stu-id="ae081-128">The ability for non-members to request access is enabled.</span></span>

<span data-ttu-id="ae081-129">Voici la configuration finale.</span><span class="sxs-lookup"><span data-stu-id="ae081-129">Here is your resulting configuration.</span></span>
  
![Protection des données sensibles d’un site d’équipe SharePoint Online isolé.](media/7a6ab9c6-560a-4674-ac39-8175644dbe6f.png)
  
<span data-ttu-id="ae081-131">Les membres du site, via l’appartenance à un des groupes d’accès, peuvent désormais collaborer sur les ressources du site de façon sécurisée.</span><span class="sxs-lookup"><span data-stu-id="ae081-131">The members of the site, through group membership in one of the access groups, can now securely collaborate on the resources of the site.</span></span>
  
## <a name="highly-confidential-sharepoint-online-team-sites"></a><span data-ttu-id="ae081-132">Sites d’équipe SharePoint Online hautement confidentiels</span><span class="sxs-lookup"><span data-stu-id="ae081-132">Highly confidential SharePoint Online team sites</span></span>

<span data-ttu-id="ae081-133">Un site d’équipe SharePoint Online hautement confidentiel est un site d’équipe privé avec des paramètres d’autorisations supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="ae081-133">A highly confidential SharePoint Online team site is a private team site with additional permissions settings.</span></span>

<span data-ttu-id="ae081-134">Commencez par créer le site d’équipe privé SharePoint Online en suivant [ces instructions](https://support.office.com/article/create-a-team-site-in-sharepoint-ef10c1e7-15f3-42a3-98aa-b5972711777d).</span><span class="sxs-lookup"><span data-stu-id="ae081-134">First, create the SharePoint Online team site with these steps.</span></span>

<span data-ttu-id="ae081-135">Ensuite, dans le nouveau site d’équipe SharePoint Online, configurez d’autres paramètres autorisations en suivant ces étapes.</span><span class="sxs-lookup"><span data-stu-id="ae081-135">Next, from the new SharePoint Online team site, configure permissions with these steps.</span></span>

1.  <span data-ttu-id="ae081-136">Dans la barre d’outils du site d’équipe SharePoint, cliquez sur l’icône Paramètres, puis cliquez sur **Autorisations du site**.</span><span class="sxs-lookup"><span data-stu-id="ae081-136">In the tool bar of the SharePoint team site, click the settings icon, and then click **Site permissions**.</span></span>
2.  <span data-ttu-id="ae081-137">Dans le volet **Autorisations de site**, sous **Paramètres de partage**, cliquez sur **Modifier les paramètres de partage**.</span><span class="sxs-lookup"><span data-stu-id="ae081-137">In the **Site permissions** pane, under **Sharing Settings**, click **Change sharing settings**.</span></span>
3.  <span data-ttu-id="ae081-138">Sous **Autorisations de partage**, sélectionnez **Seuls les propriétaires du site peuvent partager des fichiers, des dossiers et le site**.</span><span class="sxs-lookup"><span data-stu-id="ae081-138">Under **Sharing permissions**, choose **Only site owners can share files, folders, and the site**.</span></span>
4. <span data-ttu-id="ae081-139">Désactivez **Autoriser les demandes d’accès**, puis cliquez sur **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="ae081-139">Turn off **Allow access requests**, and then click **Save**.</span></span>

<span data-ttu-id="ae081-140">Voici les résultats que vous devez escompter :</span><span class="sxs-lookup"><span data-stu-id="ae081-140">The results of these permission settings are:</span></span>

- <span data-ttu-id="ae081-141">La possibilité pour les membres de partager avec d’autres membres est désactivée.</span><span class="sxs-lookup"><span data-stu-id="ae081-141">The ability for members to invite other members is disabled.</span></span>
- <span data-ttu-id="ae081-142">La possibilité pour les non-membres de demander l’accès est désactivée.</span><span class="sxs-lookup"><span data-stu-id="ae081-142">The ability for non-members to request access is disabled.</span></span>

<span data-ttu-id="ae081-143">Voici la configuration finale.</span><span class="sxs-lookup"><span data-stu-id="ae081-143">Here is your resulting configuration.</span></span>
  
![Protection avec un niveau de confidentialité élevé pour un site d’équipe SharePoint Online isolé.](media/196359ab-d7ed-4fcf-97b4-61820a74aca4.png)
  
<span data-ttu-id="ae081-145">Les membres du site, via l’appartenance à un des groupes d’accès, peuvent désormais collaborer sur les ressources du site de façon sécurisée.</span><span class="sxs-lookup"><span data-stu-id="ae081-145">The members of the site, through group membership in one of the access groups, can now securely collaborate on the resources of the site.</span></span>
  
## <a name="next-step"></a><span data-ttu-id="ae081-146">Étape suivante</span><span class="sxs-lookup"><span data-stu-id="ae081-146">Next step</span></span>

[<span data-ttu-id="ae081-147">Protéger les fichiers SharePoint Online avec des étiquettes Office 365 et la protection contre la perte de données</span><span class="sxs-lookup"><span data-stu-id="ae081-147">Protect SharePoint Online files with Office 365 labels and DLP</span></span>](protect-sharepoint-online-files-with-office-365-labels-and-dlp.md)

## <a name="see-also"></a><span data-ttu-id="ae081-148">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ae081-148">See also</span></span>

[<span data-ttu-id="ae081-149">Sécuriser les fichiers et sites SharePoint Online</span><span class="sxs-lookup"><span data-stu-id="ae081-149">Secure SharePoint Online sites and files</span></span>](../security/office-365-security/secure-sharepoint-online-sites-and-files.md)
  
[<span data-ttu-id="ae081-150">Conseils de sécurité Microsoft pour les campagnes électorales, les organisations à but non lucratif et d’autres organisations flexibles</span><span class="sxs-lookup"><span data-stu-id="ae081-150">Microsoft Security Guidance for Political Campaigns, Nonprofits, and Other Agile Organizations</span></span>](/security/office-365-security/microsoft-security-guidance-for-political-campaigns-nonprofits-and-other-agile-o.md)
  
[<span data-ttu-id="ae081-151">Adoption du cloud et solutions hybrides</span><span class="sxs-lookup"><span data-stu-id="ae081-151">Cloud adoption and hybrid solutions</span></span>](https://docs.microsoft.com/office365/enterprise/cloud-adoption-and-hybrid-solutions)
