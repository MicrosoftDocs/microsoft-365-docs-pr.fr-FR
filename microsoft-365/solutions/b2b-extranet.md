---
title: Créer un extranet B2B avec des invités gérés
ms.author: mikeplum
author: MikePlumleyMSFT
manager: serdars
audience: ITPro
ms.topic: article
ms.prod: microsoft-365-enterprise
ms.collection:
- SPO_Content
- M365-collaboration
- m365solution-3tiersprotection
- m365solution-securecollab
- m365initiative-externalcollab
ms.custom: ''
localization_priority: Normal
f1.keywords: NOCSH
description: Découvrez comment créer un site extranet B2B ou une équipe avec des invités gérés d’une organisation partenaire.
ms.openlocfilehash: f9b8d9326f302233ed85c9d168fdf6f343dc6cbf
ms.sourcegitcommit: 27b2b2e5c41934b918cac2c171556c45e36661bf
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/19/2021
ms.locfileid: "50904755"
---
# <a name="create-a-b2b-extranet-with-managed-guests"></a><span data-ttu-id="abb7a-103">Créer un extranet B2B avec des invités gérés</span><span class="sxs-lookup"><span data-stu-id="abb7a-103">Create a B2B extranet with managed guests</span></span>

<span data-ttu-id="abb7a-104">Vous pouvez utiliser [Azure Active Directory Entitlement Management](/azure/active-directory/governance/entitlement-management-overview) pour créer un extranet B2B afin de collaborer avec une organisation partenaire qui utilise Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="abb7a-104">You can use [Azure Active Directory Entitlement Management](/azure/active-directory/governance/entitlement-management-overview) to create a B2B extranet to collaborate with a partner organization that uses Azure Active Directory.</span></span> <span data-ttu-id="abb7a-105">Cela permet aux utilisateurs de s’inscrire eux-mêmes dans le site ou l’équipe extranet et de recevoir l’accès via un flux de travail d’approbation.</span><span class="sxs-lookup"><span data-stu-id="abb7a-105">This allows users to self-enroll in the extranet site or team and receive access via an approval workflow.</span></span>

<span data-ttu-id="abb7a-106">Grâce à cette méthode de partage de ressources pour la collaboration, l’organisation partenaire peut aider à maintenir et approuver les invités de leur côté, réduisant ainsi la charge qui pèse sur votre service informatique et permettant aux personnes les plus familiarisés avec le contrat de collaboration de gérer l’accès des utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="abb7a-106">With this method of sharing resources for collaboration, the partner organization can help maintain and approve the guests on their end, reducing the burden on your IT department and allowing those most familiar with the collaboration agreement to manage user access.</span></span>

<span data-ttu-id="abb7a-107">Cet article décrit les étapes de création d’un package de ressources (dans ce cas, un site ou une équipe) que vous pouvez partager avec une organisation partenaire via un modèle d’inscription d’accès en libre-service.</span><span class="sxs-lookup"><span data-stu-id="abb7a-107">This article walks through the steps to create a package of resources (in this case, a site or team) that you can share with a partner organization through a self-service access registration model.</span></span> 

<span data-ttu-id="abb7a-108">Avant de commencer, créez le site ou l’équipe que vous souhaitez partager avec l’organisation partenaire et activez-le pour le partage d’invités.</span><span class="sxs-lookup"><span data-stu-id="abb7a-108">Before you begin, create the site or team that you want to share with the partner organization and enable it for guest sharing.</span></span> <span data-ttu-id="abb7a-109">Pour [plus d’informations, voir](collaborate-in-site.md) Collaborer avec des invités dans un site ou collaborer avec des invités d’une équipe. [](collaborate-as-team.md)</span><span class="sxs-lookup"><span data-stu-id="abb7a-109">See [Collaborate with guests in a site](collaborate-in-site.md) or [Collaborate with guests in a team](collaborate-as-team.md) for more information.</span></span> <span data-ttu-id="abb7a-110">Nous vous recommandons [](create-secure-guest-sharing-environment.md) également de consulter Créer un environnement de partage d’invités sécurisé pour obtenir des informations sur les fonctionnalités de sécurité et de conformité que vous pouvez utiliser pour maintenir vos stratégies de gouvernance lors de la collaboration avec des invités.</span><span class="sxs-lookup"><span data-stu-id="abb7a-110">We also recommend that you review [Create a secure guest sharing environment](create-secure-guest-sharing-environment.md) for information about security and compliance features that you can use to help maintain your governance policies when collaborating with guests.</span></span>

## <a name="license-requirements"></a><span data-ttu-id="abb7a-111">Critères de licence</span><span class="sxs-lookup"><span data-stu-id="abb7a-111">License requirements</span></span>

<span data-ttu-id="abb7a-112">L’utilisation de cette fonctionnalité nécessite une licence Azure AD Premium P2.</span><span class="sxs-lookup"><span data-stu-id="abb7a-112">Using this feature requires an Azure AD Premium P2 license.</span></span> 

<span data-ttu-id="abb7a-113">Les clouds spécialisés, tels qu’Azure Allemagne et Azure China 21Vianet, ne sont actuellement pas disponibles.</span><span class="sxs-lookup"><span data-stu-id="abb7a-113">Specialized clouds, such as Azure Germany and Azure China 21Vianet, are not currently available for use.</span></span>

## <a name="video-demonstration"></a><span data-ttu-id="abb7a-114">Démonstration vidéo</span><span class="sxs-lookup"><span data-stu-id="abb7a-114">Video demonstration</span></span>

<span data-ttu-id="abb7a-115">Cette vidéo illustre les procédures couvertes dans cet article.</span><span class="sxs-lookup"><span data-stu-id="abb7a-115">This video demonstrates the procedures covered in this article.</span></span>

> [!VIDEO https://www.microsoft.com/videoplayer/embed/RE4wKUj?autoplay=false]

## <a name="connect-the-partner-organization"></a><span data-ttu-id="abb7a-116">Connecter l’organisation partenaire</span><span class="sxs-lookup"><span data-stu-id="abb7a-116">Connect the partner organization</span></span>

<span data-ttu-id="abb7a-117">Pour inviter des invités d’une organisation partenaire, vous devez ajouter le domaine du partenaire en tant qu’organisation connectée dans Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="abb7a-117">In order to invite guests from a partner organization, you need to add the partner's domain as a connected organization in Azure Active Directory.</span></span>

<span data-ttu-id="abb7a-118">Pour ajouter une organisation connectée</span><span class="sxs-lookup"><span data-stu-id="abb7a-118">To add a connected organization</span></span>
1. <span data-ttu-id="abb7a-119">Dans [Azure Active Directory,](https://aad.portal.azure.com)cliquez **sur Gouvernance des identités.**</span><span class="sxs-lookup"><span data-stu-id="abb7a-119">In [Azure Active Directory](https://aad.portal.azure.com), click **Identity Governance**.</span></span>
2. <span data-ttu-id="abb7a-120">Cliquez **sur Organisations connectées.**</span><span class="sxs-lookup"><span data-stu-id="abb7a-120">Click **Connected organizations**.</span></span>
4. <span data-ttu-id="abb7a-121">Cliquez **sur Ajouter une organisation connectée.**</span><span class="sxs-lookup"><span data-stu-id="abb7a-121">Click **Add connected organization**.</span></span>
5. <span data-ttu-id="abb7a-122">Tapez un nom et une description pour l’organisation, puis cliquez sur **Suivant : Répertoire + domaine.**</span><span class="sxs-lookup"><span data-stu-id="abb7a-122">Type a name and description for the organization, and then click **Next: Directory + domain**.</span></span>
6. <span data-ttu-id="abb7a-123">Cliquez **sur Ajouter un répertoire + domaine.**</span><span class="sxs-lookup"><span data-stu-id="abb7a-123">Click **Add directory + domain**.</span></span>
7. <span data-ttu-id="abb7a-124">Tapez le domaine de l’organisation à connecter, puis cliquez sur **Ajouter.**</span><span class="sxs-lookup"><span data-stu-id="abb7a-124">Type the domain for the organization that you want to connect, and then click **Add**.</span></span>
8. <span data-ttu-id="abb7a-125">Cliquez **sur** Se connecter, puis sur **Suivant : Sponsors**.</span><span class="sxs-lookup"><span data-stu-id="abb7a-125">Click **Connect**, and then click **Next: Sponsors**.</span></span>
9. <span data-ttu-id="abb7a-126">Ajoutez des personnes de votre organisation ou de l’organisation à qui vous voulez approuver l’accès pour les invités.</span><span class="sxs-lookup"><span data-stu-id="abb7a-126">Add people from your organization or the organization that you're connecting to who you want to approve access for guests.</span></span>
10. <span data-ttu-id="abb7a-127">Cliquez sur **Suivant : Révision + Créer**.</span><span class="sxs-lookup"><span data-stu-id="abb7a-127">Click **Next: Review + Create**.</span></span>
11. <span data-ttu-id="abb7a-128">Examinez les paramètres que vous avez choisis, puis cliquez sur **Créer.**</span><span class="sxs-lookup"><span data-stu-id="abb7a-128">Review the settings that you've chosen and then click **Create**.</span></span>

    ![Capture d’écran de la page des organisations connectées dans Azure Active Directory](../media/identity-governance-connected-organizations.png)

## <a name="choose-the-resources-to-share"></a><span data-ttu-id="abb7a-130">Choisir les ressources à partager</span><span class="sxs-lookup"><span data-stu-id="abb7a-130">Choose the resources to share</span></span>

<span data-ttu-id="abb7a-131">La première étape de la sélection des ressources à partager avec une organisation partenaire consiste à créer un catalogue pour les contenir.</span><span class="sxs-lookup"><span data-stu-id="abb7a-131">The first step in selecting resources to share with a partner organization is to create a catalog to contain them.</span></span>

<span data-ttu-id="abb7a-132">Pour créer un catalogue</span><span class="sxs-lookup"><span data-stu-id="abb7a-132">To create a catalog</span></span>
1. <span data-ttu-id="abb7a-133">Dans [Azure Active Directory,](https://aad.portal.azure.com)cliquez **sur Gouvernance des identités.**</span><span class="sxs-lookup"><span data-stu-id="abb7a-133">In [Azure Active Directory](https://aad.portal.azure.com), click **Identity Governance**.</span></span>
2. <span data-ttu-id="abb7a-134">Cliquez **sur Catalogues.**</span><span class="sxs-lookup"><span data-stu-id="abb7a-134">Click **Catalogs**.</span></span>
3. <span data-ttu-id="abb7a-135">Cliquez **sur Nouveau catalogue.**</span><span class="sxs-lookup"><span data-stu-id="abb7a-135">Click **New catalog**.</span></span>
4. <span data-ttu-id="abb7a-136">Tapez un nom et une  description pour  le catalogue et assurez-vous que activés et activés pour les utilisateurs externes sont tous deux définies sur **Oui**.</span><span class="sxs-lookup"><span data-stu-id="abb7a-136">Type a name and description for the catalog and ensure that **Enabled** and **Enabled for external users** are both set to **Yes**.</span></span>
5. <span data-ttu-id="abb7a-137">Cliquez sur **Créer**.</span><span class="sxs-lookup"><span data-stu-id="abb7a-137">Click **Create**.</span></span>

   ![Capture d’écran de la page catalogues dans Azure Active Directory Identity Governance](../media/identity-governance-catalogs.png)

<span data-ttu-id="abb7a-139">Une fois le catalogue créé, vous ajoutez le site SharePoint ou l’équipe que vous souhaitez partager avec l’organisation partenaire.</span><span class="sxs-lookup"><span data-stu-id="abb7a-139">Once the catalog has been created, you add the SharePoint site or team that you want to share with the partner organization.</span></span>

<span data-ttu-id="abb7a-140">Pour ajouter des ressources à un catalogue</span><span class="sxs-lookup"><span data-stu-id="abb7a-140">To add resources to a catalog</span></span>
1. <span data-ttu-id="abb7a-141">Dans Azure AD Identity Governance, cliquez sur **Catalogues,** puis cliquez sur le catalogue dans lequel vous souhaitez ajouter des ressources.</span><span class="sxs-lookup"><span data-stu-id="abb7a-141">In Azure AD Identity Governance, click **Catalogs**, and then click the catalog where you want to add resources.</span></span>
2. <span data-ttu-id="abb7a-142">Cliquez **sur Ressources,** puis sur **Ajouter des ressources.**</span><span class="sxs-lookup"><span data-stu-id="abb7a-142">Click **Resources** and then click **Add resources**.</span></span>
3. <span data-ttu-id="abb7a-143">Sélectionnez les équipes ou les sites SharePoint que vous souhaitez inclure dans votre extranet, puis cliquez sur **Ajouter**.</span><span class="sxs-lookup"><span data-stu-id="abb7a-143">Select the teams or SharePoint sites that you want to include in your extranet, and then click **Add**.</span></span>

   ![Capture d’écran de la page ressources du catalogue dans Azure Active Directory Identity Governance](../media/identity-governance-catalog-resource.png)

<span data-ttu-id="abb7a-145">Une fois que vous avez défini les ressources que vous souhaitez partager, l’étape suivante consiste à créer un package d’accès, qui définit le type d’accès accordé aux utilisateurs partenaires et le processus d’approbation pour les nouveaux utilisateurs partenaires demandant l’accès.</span><span class="sxs-lookup"><span data-stu-id="abb7a-145">Once you've defined the resources that you want to share, the next step is to create an access package, which defines the type of access that partner users are granted and the approval process for new partner users requesting access.</span></span>

<span data-ttu-id="abb7a-146">Pour créer un package d’accès</span><span class="sxs-lookup"><span data-stu-id="abb7a-146">To create an access package</span></span>
1. <span data-ttu-id="abb7a-147">Dans La gouvernance des identités Azure AD, cliquez sur **Catalogues,** puis cliquez sur le catalogue dans lequel vous souhaitez créer un package d’accès.</span><span class="sxs-lookup"><span data-stu-id="abb7a-147">In Azure AD Identity Governance, click **Catalogs**, and then click the catalog where you want to create an access package.</span></span>
2. <span data-ttu-id="abb7a-148">Cliquez **sur Packages Access,** puis sur **Nouveau package d’accès.**</span><span class="sxs-lookup"><span data-stu-id="abb7a-148">Click **Access packages**, and then click **New access package**.</span></span>
3. <span data-ttu-id="abb7a-149">Tapez un nom et une description pour le package d’accès, puis cliquez sur **Suivant : Rôles de ressource.**</span><span class="sxs-lookup"><span data-stu-id="abb7a-149">Type a name and description for the access package, and then click **Next: Resource roles**.</span></span>
4. <span data-ttu-id="abb7a-150">Choisissez les ressources du catalogue que vous souhaitez utiliser pour votre extranet.</span><span class="sxs-lookup"><span data-stu-id="abb7a-150">Choose the resources from the catalog that you want to use for your extranet.</span></span>
5. <span data-ttu-id="abb7a-151">Pour chaque ressource, dans la colonne **Rôle,** choisissez le rôle d’utilisateur que vous souhaitez accorder aux invités qui utilisent l’extranet.</span><span class="sxs-lookup"><span data-stu-id="abb7a-151">For each resource, in the **Role** column, choose the user role you want to grant to the guests who use the extranet.</span></span>
6. <span data-ttu-id="abb7a-152">Cliquez **sur Suivant : Demandes**.</span><span class="sxs-lookup"><span data-stu-id="abb7a-152">Click **Next: Requests**.</span></span>
7. <span data-ttu-id="abb7a-153">Under **Users who can request access**, choose For users not in your **directory**.</span><span class="sxs-lookup"><span data-stu-id="abb7a-153">Under **Users who can request access**, choose **For users not in your directory**.</span></span>
8. <span data-ttu-id="abb7a-154">Assurez-vous que **l’option Organisations connectées** spécifiques est sélectionnée, puis cliquez sur **Ajouter des répertoires.**</span><span class="sxs-lookup"><span data-stu-id="abb7a-154">Ensure that the **Specific connected organizations** option is selected, and then click **Add directories**.</span></span>
9. <span data-ttu-id="abb7a-155">Choisissez l’organisation connectée que vous ajoutez précédemment, puis cliquez sur **Sélectionner**</span><span class="sxs-lookup"><span data-stu-id="abb7a-155">Choose the connected organization that you add earlier, and then click **Select**</span></span>
10. <span data-ttu-id="abb7a-156">Sous **Approbation,** **sélectionnez Oui** pour **Exiger l’approbation.**</span><span class="sxs-lookup"><span data-stu-id="abb7a-156">Under **Approval**, choose **Yes** for **Require approval**.</span></span>
11. <span data-ttu-id="abb7a-157">Sous **Premier approuveur,** choisissez l’un des sponsors que vous avez ajoutés précédemment ou choisissez un utilisateur spécifique.</span><span class="sxs-lookup"><span data-stu-id="abb7a-157">Under **First approver**, choose one of the sponsors that you added earlier or choose a specific user.</span></span>
12. <span data-ttu-id="abb7a-158">Cliquez **sur Ajouter un secours** et sélectionnez un approuveur de secours.</span><span class="sxs-lookup"><span data-stu-id="abb7a-158">Click **Add fallback** and select a fallback approver.</span></span>
13. <span data-ttu-id="abb7a-159">Sous **Activer,** sélectionnez **Oui.**</span><span class="sxs-lookup"><span data-stu-id="abb7a-159">Under **Enable**, choose **Yes**.</span></span>
14. <span data-ttu-id="abb7a-160">Cliquez **sur Suivant : Cycle de vie.**</span><span class="sxs-lookup"><span data-stu-id="abb7a-160">Click **Next: Lifecycle**.</span></span>
15. <span data-ttu-id="abb7a-161">Choisissez les paramètres d’expiration et de révision d’accès que vous souhaitez utiliser, puis cliquez sur **Suivant : Révision + Créer.**</span><span class="sxs-lookup"><span data-stu-id="abb7a-161">Choose the expiration and access review settings that you want to use, and then click **Next: Review + Create**.</span></span>
16. <span data-ttu-id="abb7a-162">Examinez vos paramètres, puis cliquez sur **Créer.**</span><span class="sxs-lookup"><span data-stu-id="abb7a-162">Review your settings, and then click **Create**.</span></span>

    ![Capture d’écran de l’écran packages d’accès dans Azure Active Directory Identity Governance](../media/identity-governance-access-packages.png)

<span data-ttu-id="abb7a-164">Si vous êtes partenaire d’une grande organisation, vous pouvez masquer le package d’accès.</span><span class="sxs-lookup"><span data-stu-id="abb7a-164">If you're partnering with a large organization, you may want to hide the access package.</span></span> <span data-ttu-id="abb7a-165">Si le package est masqué, les utilisateurs de l’organisation partenaire ne voient pas le package sur leur *portail My Access.*</span><span class="sxs-lookup"><span data-stu-id="abb7a-165">If the package is hidden, then users in the partner organization will not see the package on their *My Access* portal.</span></span> <span data-ttu-id="abb7a-166">Au lieu de cela, un lien direct doit leur être envoyé pour s’inscrire au package.</span><span class="sxs-lookup"><span data-stu-id="abb7a-166">Instead, they must be sent a direct link to sign up for the package.</span></span> <span data-ttu-id="abb7a-167">Le masquage du package d’accès peut réduire le nombre de demandes d’accès inappropriés et peut également aider à maintenir les packages d’accès disponibles organisés dans le portail de l’organisation partenaire.</span><span class="sxs-lookup"><span data-stu-id="abb7a-167">Hiding the access package can reduce the number of inappropriate access requests and can also help keep available access packages organized in the partner organization's portal.</span></span>

<span data-ttu-id="abb7a-168">Pour définir un package d’accès sur masqué</span><span class="sxs-lookup"><span data-stu-id="abb7a-168">To set an access package to hidden</span></span>
1. <span data-ttu-id="abb7a-169">Dans Azure AD Identity Governance, cliquez **sur Packages Access,** puis cliquez sur votre package d’accès.</span><span class="sxs-lookup"><span data-stu-id="abb7a-169">In Azure AD Identity Governance, click **Access packages**, and then click your access package.</span></span>
2. <span data-ttu-id="abb7a-170">Dans la page **Vue d’ensemble,** cliquez sur **Modifier.**</span><span class="sxs-lookup"><span data-stu-id="abb7a-170">On the **Overview** page, click **Edit**.</span></span>
3. <span data-ttu-id="abb7a-171">Sous **Propriétés,** **sélectionnez Oui** pour **Masqué,** puis cliquez sur **Enregistrer.**</span><span class="sxs-lookup"><span data-stu-id="abb7a-171">Under **Properties**, choose **Yes** for **Hidden**, and then click **Save**.</span></span>

   ![Capture d’écran d’un écran modifier les propriétés du package d’accès](../media/identity-governance-access-package-hidden.png)

## <a name="invite-partner-users"></a><span data-ttu-id="abb7a-173">Inviter des utilisateurs partenaires</span><span class="sxs-lookup"><span data-stu-id="abb7a-173">Invite partner users</span></span>

<span data-ttu-id="abb7a-174">Si vous définissez le package d’accès sur masqué, vous devez envoyer un lien direct à l’organisation partenaire afin qu’elle puisse demander l’accès à votre site ou à votre équipe.</span><span class="sxs-lookup"><span data-stu-id="abb7a-174">If you set the access package to hidden, you need to send a direct link to the partner organization so that they can request access to your site or team.</span></span>

<span data-ttu-id="abb7a-175">Pour trouver le lien du portail d’accès</span><span class="sxs-lookup"><span data-stu-id="abb7a-175">To find the access portal link</span></span>
1. <span data-ttu-id="abb7a-176">Dans Azure AD Identity Governance, cliquez **sur Packages Access,** puis cliquez sur votre package d’accès.</span><span class="sxs-lookup"><span data-stu-id="abb7a-176">In Azure AD Identity Governance, click **Access packages**, and then click your access package.</span></span>
2. <span data-ttu-id="abb7a-177">Dans la page **Vue d’ensemble,** cliquez **sur Copier dans le Presse-papiers** pour le lien **portail Mon accès.**</span><span class="sxs-lookup"><span data-stu-id="abb7a-177">On the **Overview** page, click **Copy to clipboard** link for the **My Access portal link**.</span></span>

   ![Capture d’écran des propriétés du package d’accès avec lien du portail d’accès](../media/identity-governance-access-portal-link.png)

<span data-ttu-id="abb7a-179">Une fois que vous avez copié le lien, vous pouvez le partager avec votre contact au niveau de l’organisation partenaire et l’envoyer aux utilisateurs de son équipe de collaboration.</span><span class="sxs-lookup"><span data-stu-id="abb7a-179">Once you have copied the link, you can share it with your contact at the partner organization and they can send it to the users on their collaboration team.</span></span>

## <a name="see-also"></a><span data-ttu-id="abb7a-180">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="abb7a-180">See Also</span></span>

[<span data-ttu-id="abb7a-181">Créer un environnement de partage sécurisé avec des invités</span><span class="sxs-lookup"><span data-stu-id="abb7a-181">Create a secure guest sharing environment</span></span>](create-secure-guest-sharing-environment.md)