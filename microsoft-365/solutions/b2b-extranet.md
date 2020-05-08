---
title: Créer un extranet B2B avec des invités gérés
ms.author: mikeplum
author: MikePlumleyMSFT
manager: pamgreen
audience: ITPro
ms.topic: article
ms.prod: microsoft-365-enterprise
ms.collection:
- SPO_Content
- M365-collaboration
- M365solutions
ms.custom: ''
localization_priority: Normal
f1.keywords: NOCSH
description: Découvrez comment créer un site extranet B2B ou une équipe avec des utilisateurs d’invités gérés à partir d’une organisation partenaire.
ms.openlocfilehash: 1b7542dd2fcd5fa28afc013f83da713c37e1187b
ms.sourcegitcommit: 46644f9778bc70ab6d62783e0a1e60ba2eccc27f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/08/2020
ms.locfileid: "44166148"
---
# <a name="create-a-b2b-extranet-with-managed-guests"></a><span data-ttu-id="13d28-103">Créer un extranet B2B avec des invités gérés</span><span class="sxs-lookup"><span data-stu-id="13d28-103">Create a B2B extranet with managed guests</span></span>

<span data-ttu-id="13d28-104">Vous pouvez utiliser la [gestion des droits Azure Active Directory](https://docs.microsoft.com/azure/active-directory/governance/entitlement-management-overview) pour créer un extranet B2B afin de collaborer avec une organisation partenaire qui utilise Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="13d28-104">You can use [Azure Active Directory Entitlement Management](https://docs.microsoft.com/azure/active-directory/governance/entitlement-management-overview) to create a B2B extranet to collaborate with a partner organization that uses Azure Active Directory.</span></span> <span data-ttu-id="13d28-105">Cela permet aux utilisateurs de s’inscrire automatiquement sur le site extranet ou l’équipe et de recevoir un accès via un flux de travail d’approbation.</span><span class="sxs-lookup"><span data-stu-id="13d28-105">This allows users to self-enroll in the extranet site or team and receive access via an approval workflow.</span></span>

<span data-ttu-id="13d28-106">Avec cette méthode de partage des ressources pour la collaboration, l’organisation partenaire peut vous aider à gérer et à approuver les utilisateurs invités à la fin de celle-ci, en réduisant la charge pesant sur votre service informatique et en permettant aux personnes les plus familières de l’accord de collaboration de gérer l’accès des utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="13d28-106">With this method of sharing resources for collaboration, the partner organization can help maintain and approve the guest users on their end, reducing the burden on your IT department and allowing those most familiar with the collaboration agreement to manage user access.</span></span>

<span data-ttu-id="13d28-107">Cet article décrit les étapes à suivre pour créer un package de ressources (dans ce cas, un site ou une équipe) que vous pouvez partager avec une organisation partenaire par le biais d’un modèle d’enregistrement d’accès libre-service.</span><span class="sxs-lookup"><span data-stu-id="13d28-107">This article walks through the steps to create a package of resources (in this case, a site or team) that you can share with a partner organization through a self-service access registration model.</span></span> 

<span data-ttu-id="13d28-108">Avant de commencer, créez le site ou l’équipe que vous souhaitez partager avec l’organisation partenaire et activez-le pour le partage d’invité.</span><span class="sxs-lookup"><span data-stu-id="13d28-108">Before you begin, create the site or team that you want to share with the partner organization and enable it for guest sharing.</span></span> <span data-ttu-id="13d28-109">Pour plus d’informations, consultez la rubrique [collaborer avec des invités dans un site](collaborate-in-site.md) ou [collaborer avec des invités dans une équipe](collaborate-as-team.md) .</span><span class="sxs-lookup"><span data-stu-id="13d28-109">See [Collaborate with guests in a site](collaborate-in-site.md) or [Collaborate with guests in a team](collaborate-as-team.md) for more information.</span></span> <span data-ttu-id="13d28-110">Nous vous recommandons également de consulter la rubrique [Create a Secure Guest Sharing Environment](create-secure-guest-sharing-environment.md) pour obtenir des informations sur les fonctionnalités de sécurité et de conformité que vous pouvez utiliser pour gérer vos stratégies de gouvernance lors de la collaboration avec des invités.</span><span class="sxs-lookup"><span data-stu-id="13d28-110">We also recommend that you review [Create a secure guest sharing environment](create-secure-guest-sharing-environment.md) for information about security and compliance features that you can use to help maintain your governance policies when collaborating with guests.</span></span>

## <a name="connect-the-partner-organization"></a><span data-ttu-id="13d28-111">Connecter l’organisation partenaire</span><span class="sxs-lookup"><span data-stu-id="13d28-111">Connect the partner organization</span></span>

<span data-ttu-id="13d28-112">Pour inviter des invités à partir d’une organisation partenaire, vous devez ajouter le domaine du partenaire en tant qu’organisation connectée dans Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="13d28-112">In order to invite guests from a partner organization, you need to add the partner's domain as a connected organization in Azure Active Directory.</span></span>

<span data-ttu-id="13d28-113">Pour ajouter une organisation connectée</span><span class="sxs-lookup"><span data-stu-id="13d28-113">To add a connected organization</span></span>
1. <span data-ttu-id="13d28-114">Dans [Azure Active Directory](https://aad.portal.azure.com), cliquez sur **gouvernance des identités**.</span><span class="sxs-lookup"><span data-stu-id="13d28-114">In [Azure Active Directory](https://aad.portal.azure.com), click **Identity Governance**.</span></span>
2. <span data-ttu-id="13d28-115">Cliquez sur **organisations connectées**.</span><span class="sxs-lookup"><span data-stu-id="13d28-115">Click **Connected organizations**.</span></span>
4. <span data-ttu-id="13d28-116">Cliquez sur **Ajouter une organisation connectée**.</span><span class="sxs-lookup"><span data-stu-id="13d28-116">Click **Add connected organization**.</span></span>
5. <span data-ttu-id="13d28-117">Tapez un nom et une description pour l’organisation, puis cliquez sur **suivant : répertoire + domaine**.</span><span class="sxs-lookup"><span data-stu-id="13d28-117">Type a name and description for the organization, and then click **Next: Directory + domain**.</span></span>
6. <span data-ttu-id="13d28-118">Cliquez sur **Ajouter un répertoire + domaine**.</span><span class="sxs-lookup"><span data-stu-id="13d28-118">Click **Add directory + domain**.</span></span>
7. <span data-ttu-id="13d28-119">Tapez le domaine de l’organisation à laquelle vous souhaitez vous connecter, puis cliquez sur **Ajouter**.</span><span class="sxs-lookup"><span data-stu-id="13d28-119">Type the domain for the organization that you want to connect, and then click **Add**.</span></span>
8. <span data-ttu-id="13d28-120">Cliquez sur **se connecter**, puis sur **suivant : organisateurs**.</span><span class="sxs-lookup"><span data-stu-id="13d28-120">Click **Connect**, and then click **Next: Sponsors**.</span></span>
9. <span data-ttu-id="13d28-121">Ajoutez des personnes de votre organisation ou de l’organisation à laquelle vous vous connectez, auxquelles vous souhaitez approuver l’accès des utilisateurs invités.</span><span class="sxs-lookup"><span data-stu-id="13d28-121">Add people from your organization or the organization that you're connecting to who you want to approve access for guest users.</span></span>
10. <span data-ttu-id="13d28-122">Cliquez sur **suivant : examiner + créer**.</span><span class="sxs-lookup"><span data-stu-id="13d28-122">Click **Next: Review + Create**.</span></span>
11. <span data-ttu-id="13d28-123">Passez en revue les paramètres que vous avez choisis, puis cliquez sur **créer**.</span><span class="sxs-lookup"><span data-stu-id="13d28-123">Review the settings that you've chosen and then click **Create**.</span></span>

    ![Capture d’écran de la page organisations connectées dans Azure Active Directory](../media/identity-governance-connected-organizations.png)

## <a name="choose-the-resources-to-share"></a><span data-ttu-id="13d28-125">Choisir les ressources à partager</span><span class="sxs-lookup"><span data-stu-id="13d28-125">Choose the resources to share</span></span>

<span data-ttu-id="13d28-126">La première étape de sélection des ressources à partager avec une organisation partenaire consiste à créer un catalogue pour les contenir.</span><span class="sxs-lookup"><span data-stu-id="13d28-126">The first step in selecting resources to share with a partner organization is to create a catalog to contain them.</span></span>

<span data-ttu-id="13d28-127">Pour créer un catalogue</span><span class="sxs-lookup"><span data-stu-id="13d28-127">To create a catalog</span></span>
1. <span data-ttu-id="13d28-128">Dans [Azure Active Directory](https://aad.portal.azure.com), cliquez sur **gouvernance des identités**.</span><span class="sxs-lookup"><span data-stu-id="13d28-128">In [Azure Active Directory](https://aad.portal.azure.com), click **Identity Governance**.</span></span>
2. <span data-ttu-id="13d28-129">Cliquez sur **catalogues**.</span><span class="sxs-lookup"><span data-stu-id="13d28-129">Click **Catalogs**.</span></span>
3. <span data-ttu-id="13d28-130">Cliquez sur **nouveau catalogue**.</span><span class="sxs-lookup"><span data-stu-id="13d28-130">Click **New catalog**.</span></span>
4. <span data-ttu-id="13d28-131">Tapez un nom et une description pour le catalogue et assurez-vous que **activé** et **activé pour les utilisateurs externes** sont définis sur **Oui**.</span><span class="sxs-lookup"><span data-stu-id="13d28-131">Type a name and description for the catalog and ensure that **Enabled** and **Enabled for external users** are both set to **Yes**.</span></span>
5. <span data-ttu-id="13d28-132">Cliquez sur **Créer**.</span><span class="sxs-lookup"><span data-stu-id="13d28-132">Click **Create**.</span></span>

   ![Capture d’écran de la page de catalogues dans Azure Active Directory Identity Governance](../media/identity-governance-catalogs.png)

<span data-ttu-id="13d28-134">Une fois le catalogue créé, vous ajoutez le site ou l’équipe SharePoint que vous souhaitez partager avec l’organisation partenaire.</span><span class="sxs-lookup"><span data-stu-id="13d28-134">Once the catalog has been created, you add the SharePoint site or team that you want to share with the partner organization.</span></span>

<span data-ttu-id="13d28-135">Pour ajouter des ressources à un catalogue</span><span class="sxs-lookup"><span data-stu-id="13d28-135">To add resources to a catalog</span></span>
1. <span data-ttu-id="13d28-136">Dans Azure AD Identity Government, cliquez sur **catalogues**, puis cliquez sur le catalogue dans lequel vous souhaitez ajouter des ressources.</span><span class="sxs-lookup"><span data-stu-id="13d28-136">In Azure AD Identity Governance, click **Catalogs**, and then click the catalog where you want to add resources.</span></span>
2. <span data-ttu-id="13d28-137">Cliquez sur **ressources** , puis sur **Ajouter des ressources**.</span><span class="sxs-lookup"><span data-stu-id="13d28-137">Click **Resources** and then click **Add resources**.</span></span>
3. <span data-ttu-id="13d28-138">Sélectionnez les équipes ou les sites SharePoint que vous souhaitez inclure dans votre extranet, puis cliquez sur **Ajouter**.</span><span class="sxs-lookup"><span data-stu-id="13d28-138">Select the teams or SharePoint sites that you want to include in your extranet, and then click **Add**.</span></span>

   ![Capture d’écran de la page de ressources de catalogue dans Azure Active Directory Identity Governance](../media/identity-governance-catalog-resource.png)

<span data-ttu-id="13d28-140">Une fois que vous avez défini les ressources que vous souhaitez partager, l’étape suivante consiste à créer un package Access, qui définit le type d’accès accordé aux utilisateurs partenaires et le processus d’approbation des nouveaux utilisateurs partenaires qui demandent l’accès.</span><span class="sxs-lookup"><span data-stu-id="13d28-140">Once you've defined the resources that you want to share, the next step is to create an access package, which defines the type of access that partner users are granted and the approval process for new partner users requesting access.</span></span>

<span data-ttu-id="13d28-141">Pour créer un package Access</span><span class="sxs-lookup"><span data-stu-id="13d28-141">To create an access package</span></span>
1. <span data-ttu-id="13d28-142">Dans Azure AD Identity Government, cliquez sur **catalogues**, puis cliquez sur le catalogue dans lequel vous souhaitez créer un package Access.</span><span class="sxs-lookup"><span data-stu-id="13d28-142">In Azure AD Identity Governance, click **Catalogs**, and then click the catalog where you want to create an access package.</span></span>
2. <span data-ttu-id="13d28-143">Cliquez sur **packages d’accès**, puis sur **nouveau package Access**.</span><span class="sxs-lookup"><span data-stu-id="13d28-143">Click **Access packages**, and then click **New access package**.</span></span>
3. <span data-ttu-id="13d28-144">Tapez un nom et une description pour le package d’accès, puis cliquez sur **suivant : rôles de ressource**.</span><span class="sxs-lookup"><span data-stu-id="13d28-144">Type a name and description for the access package, and then click **Next: Resource roles**.</span></span>
4. <span data-ttu-id="13d28-145">Choisissez les ressources du catalogue que vous souhaitez utiliser pour votre extranet.</span><span class="sxs-lookup"><span data-stu-id="13d28-145">Choose the resources from the catalog that you want to use for your extranet.</span></span>
5. <span data-ttu-id="13d28-146">Pour chaque ressource, dans la colonne **rôle** , choisissez le rôle d’utilisateur que vous souhaitez accorder aux utilisateurs invités qui utilisent l’extranet.</span><span class="sxs-lookup"><span data-stu-id="13d28-146">For each resource, in the **Role** column, choose the user role you want to grant to the guest users who use the extranet.</span></span>
6. <span data-ttu-id="13d28-147">Cliquez sur **suivant : demandes**.</span><span class="sxs-lookup"><span data-stu-id="13d28-147">Click **Next: Requests**.</span></span>
7. <span data-ttu-id="13d28-148">Sous **utilisateurs pouvant demander l’accès**, choisissez **pour les utilisateurs qui ne se trouvent pas dans votre répertoire**.</span><span class="sxs-lookup"><span data-stu-id="13d28-148">Under **Users who can request access**, choose **For users not in your directory**.</span></span>
8. <span data-ttu-id="13d28-149">Assurez-vous que l’option **organisations connectées spécifique** est sélectionnée, puis cliquez sur **Ajouter des répertoires**.</span><span class="sxs-lookup"><span data-stu-id="13d28-149">Ensure that the **Specific connected organizations** option is selected, and then click **Add directories**.</span></span>
9. <span data-ttu-id="13d28-150">Choisissez l’organisation connectée que vous avez ajoutée précédemment, puis cliquez sur **Sélectionner** .</span><span class="sxs-lookup"><span data-stu-id="13d28-150">Choose the connected organization that you add earlier, and then click **Select**</span></span>
10. <span data-ttu-id="13d28-151">Sous **approbation**, sélectionnez **Oui** pour **demander une approbation**.</span><span class="sxs-lookup"><span data-stu-id="13d28-151">Under **Approval**, choose **Yes** for **Require approval**.</span></span>
11. <span data-ttu-id="13d28-152">Sous **premier approbateur**, sélectionnez l’un des organisateurs ajoutés précédemment ou choisissez un utilisateur spécifique.</span><span class="sxs-lookup"><span data-stu-id="13d28-152">Under **First approver**, choose one of the sponsors that you added earlier or choose a specific user.</span></span>
12. <span data-ttu-id="13d28-153">Cliquez sur **Ajouter un secours** et sélectionnez un approbateur de secours.</span><span class="sxs-lookup"><span data-stu-id="13d28-153">Click **Add fallback** and select a fallback approver.</span></span>
13. <span data-ttu-id="13d28-154">Sous **activer**, sélectionnez **Oui**.</span><span class="sxs-lookup"><span data-stu-id="13d28-154">Under **Enable**, choose **Yes**.</span></span>
14. <span data-ttu-id="13d28-155">Cliquez sur **suivant : cycle de vie**.</span><span class="sxs-lookup"><span data-stu-id="13d28-155">Click **Next: Lifecycle**.</span></span>
15. <span data-ttu-id="13d28-156">Choisissez les paramètres d’expiration et de révision d’accès que vous souhaitez utiliser, puis cliquez sur **suivant : examiner + créer**.</span><span class="sxs-lookup"><span data-stu-id="13d28-156">Choose the expiration and access review settings that you want to use, and then click **Next: Review + Create**.</span></span>
16. <span data-ttu-id="13d28-157">Vérifiez vos paramètres, puis cliquez sur **créer**.</span><span class="sxs-lookup"><span data-stu-id="13d28-157">Review your settings, and then click **Create**.</span></span>

    ![Capture d’écran de l’écran des packages d’accès dans Azure Active Directory Identity Governance](../media/identity-governance-access-packages.png)

<span data-ttu-id="13d28-159">Si vous êtes un partenaire d’une grande organisation, vous souhaiterez peut-être masquer le package d’accès.</span><span class="sxs-lookup"><span data-stu-id="13d28-159">If you're partnering with a large organization, you may want to hide the access package.</span></span> <span data-ttu-id="13d28-160">Si le package est masqué, les utilisateurs de l’organisation partenaire ne verront pas le package sur leur portail d' *accès My* .</span><span class="sxs-lookup"><span data-stu-id="13d28-160">If the package is hidden, then users in the partner organization will not see the package on their *My Access* portal.</span></span> <span data-ttu-id="13d28-161">Au lieu de cela, ils doivent recevoir un lien direct pour s’inscrire au package.</span><span class="sxs-lookup"><span data-stu-id="13d28-161">Instead, they must be sent a direct link to sign up for the package.</span></span> <span data-ttu-id="13d28-162">Le fait de masquer le package Access peut réduire le nombre de demandes d’accès inappropriées et permettre de conserver les packages d’accès disponibles organisés sur le portail de l’organisation partenaire.</span><span class="sxs-lookup"><span data-stu-id="13d28-162">Hiding the access package can reduce the number of inappropriate access requests and can also help keep available access packages organized in the partner organization's portal.</span></span>

<span data-ttu-id="13d28-163">Pour définir le masquage d’un package Access</span><span class="sxs-lookup"><span data-stu-id="13d28-163">To set an access package to hidden</span></span>
1. <span data-ttu-id="13d28-164">Dans Azure AD Identity Government, cliquez sur **packages d’accès**, puis sur votre package d’accès.</span><span class="sxs-lookup"><span data-stu-id="13d28-164">In Azure AD Identity Governance, click **Access packages**, and then click your access package.</span></span>
2. <span data-ttu-id="13d28-165">Sur la page **vue d’ensemble** , cliquez sur **modifier**.</span><span class="sxs-lookup"><span data-stu-id="13d28-165">On the **Overview** page, click **Edit**.</span></span>
3. <span data-ttu-id="13d28-166">Sous **Propriétés**, choisissez **Oui** pour **Masquer**, puis cliquez sur **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="13d28-166">Under **Properties**, choose **Yes** for **Hidden**, and then click **Save**.</span></span>

   ![Capture d’écran d’un écran modifier les propriétés du package d’accès](../media/identity-governance-access-package-hidden.png)

## <a name="invite-partner-users"></a><span data-ttu-id="13d28-168">Inviter des utilisateurs partenaires</span><span class="sxs-lookup"><span data-stu-id="13d28-168">Invite partner users</span></span>

<span data-ttu-id="13d28-169">Si vous définissez le package Access sur masqué, vous devez envoyer un lien direct à l’organisation partenaire afin qu’il puisse demander l’accès à votre site ou équipe.</span><span class="sxs-lookup"><span data-stu-id="13d28-169">If you set the access package to hidden, you need to send a direct link to the partner organization so that they can request access to your site or team.</span></span>

<span data-ttu-id="13d28-170">Pour trouver le lien portail d’accès</span><span class="sxs-lookup"><span data-stu-id="13d28-170">To find the access portal link</span></span>
1. <span data-ttu-id="13d28-171">Dans Azure AD Identity Government, cliquez sur **packages d’accès**, puis sur votre package d’accès.</span><span class="sxs-lookup"><span data-stu-id="13d28-171">In Azure AD Identity Governance, click **Access packages**, and then click your access package.</span></span>
2. <span data-ttu-id="13d28-172">Sur la page **vue d’ensemble** , cliquez sur **copier dans le presse-papiers** pour le **lien mon portail d’accès**.</span><span class="sxs-lookup"><span data-stu-id="13d28-172">On the **Overview** page, click **Copy to clipboard** link for the **My Access portal link**.</span></span>

   ![Capture d’écran des propriétés de package Access avec le lien du portail Access](../media/identity-governance-access-portal-link.png)

<span data-ttu-id="13d28-174">Une fois que vous avez copié le lien, vous pouvez le partager avec votre contact auprès de l’organisation partenaire et l’envoyer aux utilisateurs de son équipe de collaboration.</span><span class="sxs-lookup"><span data-stu-id="13d28-174">Once you have copied the link, you can share it with your contact at the partner organization and they can send it to the users on their collaboration team.</span></span>

## <a name="see-also"></a><span data-ttu-id="13d28-175">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="13d28-175">See Also</span></span>

[<span data-ttu-id="13d28-176">Créer un environnement de partage sécurisé avec des invités</span><span class="sxs-lookup"><span data-stu-id="13d28-176">Create a secure guest sharing environment</span></span>](create-secure-guest-sharing-environment.md)

