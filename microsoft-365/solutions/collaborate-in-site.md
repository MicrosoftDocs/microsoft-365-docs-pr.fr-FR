---
title: Collaborer avec des invités sur un site
ms.author: mikeplum
author: MikePlumleyMSFT
manager: pamgreen
audience: ITPro
ms.topic: article
ms.prod: microsoft-365-enterprise
ms.collection:
- SPO_Content
- M365-collaboration
- m365solution-3tiersprotection
- m365solution-securecollab
ms.custom:
- seo-marvel-apr2020
localization_priority: Normal
f1.keywords: NOCSH
description: Découvrez les étapes de configuration de Microsoft 365 nécessaires pour configurer un site SharePoint en vue de la collaboration avec des invités.
ms.openlocfilehash: dbbf84539c1bef239abc76e142922976902a01ed
ms.sourcegitcommit: ae3aa7f29be16d08950cf23cad489bc069aa8617
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/09/2020
ms.locfileid: "48409035"
---
# <a name="collaborate-with-guests-in-a-site"></a><span data-ttu-id="409e5-103">Collaborer avec des invités sur un site</span><span class="sxs-lookup"><span data-stu-id="409e5-103">Collaborate with guests in a site</span></span>

<span data-ttu-id="409e5-104">Si vous avez besoin de collaborer avec des invités dans des documents, des données et des listes, vous pouvez utiliser un site SharePoint.</span><span class="sxs-lookup"><span data-stu-id="409e5-104">If you need to collaborate with guests across documents, data, and lists, you can use a SharePoint site.</span></span> <span data-ttu-id="409e5-105">Les sites SharePoint modernes sont connectés aux groupes Microsoft 365 et peuvent gérer l’appartenance à un site et fournir des outils de collaboration supplémentaires tels qu’une boîte aux lettres partagée et un calendrier.</span><span class="sxs-lookup"><span data-stu-id="409e5-105">Modern SharePoint sites are connected to Microsoft 365 Groups and can manage the site membership and provide additional collaboration tools such as a shared mailbox and a calendar.</span></span>

<span data-ttu-id="409e5-106">Dans cet article, nous allons passer en revue les étapes de configuration de Microsoft 365 nécessaires pour configurer un site SharePoint en vue de la collaboration avec des invités.</span><span class="sxs-lookup"><span data-stu-id="409e5-106">In this article, we'll walk through the Microsoft 365 configuration steps necessary to set up a SharePoint site for collaboration with guests.</span></span>

## <a name="video-demonstration"></a><span data-ttu-id="409e5-107">Démonstration vidéo</span><span class="sxs-lookup"><span data-stu-id="409e5-107">Video demonstration</span></span>

<span data-ttu-id="409e5-108">Cette vidéo présente les étapes de configuration décrites dans ce document.</span><span class="sxs-lookup"><span data-stu-id="409e5-108">This video shows the configuration steps described in this document.</span></span></br>

> [!VIDEO https://www.microsoft.com/videoplayer/embed/RE44Llg?autoplay=false]

## <a name="azure-external-collaboration-settings"></a><span data-ttu-id="409e5-109">Paramètres de collaboration externe Azure</span><span class="sxs-lookup"><span data-stu-id="409e5-109">Azure external collaboration settings</span></span>

<span data-ttu-id="409e5-110">Le partage dans Microsoft 365 est régi par les [paramètres de relations organisationnelles dans Azure Active Directory](https://docs.microsoft.com/azure/active-directory/external-identities/delegate-invitations).</span><span class="sxs-lookup"><span data-stu-id="409e5-110">Sharing in Microsoft 365 is governed at its highest level by the [organizational relationships settings in Azure Active Directory](https://docs.microsoft.com/azure/active-directory/external-identities/delegate-invitations).</span></span> <span data-ttu-id="409e5-111">Si le partage d’invités est désactivé ou restreint dans Azure AD, ce paramètre remplace tous les paramètres de partage que vous configurez dans Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="409e5-111">If guest sharing is disabled or restricted in Azure AD, this setting overrides any sharing settings that you configure in Microsoft 365.</span></span>

<span data-ttu-id="409e5-112">Vérifiez les paramètres de collaboration externe pour vous assurer que le partage avec des invités n’est pas bloqué.</span><span class="sxs-lookup"><span data-stu-id="409e5-112">Check the external collaboration settings to ensure that sharing with guests is not blocked.</span></span>

![Capture d’écran de la page des paramètres de collaboration externe Azure Active Directory](../media/azure-ad-organizational-relationships-settings.png)

<span data-ttu-id="409e5-114">Pour définir les paramètres de collaboration externe</span><span class="sxs-lookup"><span data-stu-id="409e5-114">To set external collaboration settings</span></span>

1. <span data-ttu-id="409e5-115">Connectez-vous à Azure Active Directory à l’adresse [https://aad.portal.azure.com](https://aad.portal.azure.com) .</span><span class="sxs-lookup"><span data-stu-id="409e5-115">Log in to Azure Active Directory at [https://aad.portal.azure.com](https://aad.portal.azure.com).</span></span>
2. <span data-ttu-id="409e5-116">Dans le volet de navigation de gauche, cliquez sur **Azure Active Directory**.</span><span class="sxs-lookup"><span data-stu-id="409e5-116">In the left navigation pane, click **Azure Active Directory**.</span></span>
3. <span data-ttu-id="409e5-117">Cliquez sur **identités externes**.</span><span class="sxs-lookup"><span data-stu-id="409e5-117">Click **External identities**.</span></span>
4. <span data-ttu-id="409e5-118">Sur l’écran de **prise en main** , dans le volet de navigation de gauche, cliquez sur **paramètres de collaboration externe**.</span><span class="sxs-lookup"><span data-stu-id="409e5-118">On the **Get started** screen, in the left navigation pane, click **External collaboration settings**.</span></span>
5. <span data-ttu-id="409e5-119">Assurez-vous que les **administrateurs et les utilisateurs du rôle d’invité invité peuvent inviter** et que les **membres peuvent inviter** sont tous deux la valeur **Oui**.</span><span class="sxs-lookup"><span data-stu-id="409e5-119">Ensure that **Admins and users in the guest inviter role can invite** and **Members can invite** are both set to **Yes**.</span></span>
6. <span data-ttu-id="409e5-120">Si vous avez effectué des modifications, cliquez sur **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="409e5-120">If you made changes, click **Save**.</span></span>

<span data-ttu-id="409e5-121">Notez les paramètres dans la section **restrictions de collaboration** .</span><span class="sxs-lookup"><span data-stu-id="409e5-121">Note the settings in the **Collaboration restrictions** section.</span></span> <span data-ttu-id="409e5-122">Assurez-vous que les domaines des invités avec lesquels vous souhaitez collaborer ne sont pas bloqués.</span><span class="sxs-lookup"><span data-stu-id="409e5-122">Make sure that the domains of the guests that you want to collaborate with aren't blocked.</span></span>

<span data-ttu-id="409e5-123">Si vous travaillez avec des invités de plusieurs organisations, vous souhaiterez peut-être limiter leur capacité à accéder aux données d’annuaire.</span><span class="sxs-lookup"><span data-stu-id="409e5-123">If you work with guests from multiple organizations, you may want to restrict their ability to access directory data.</span></span> <span data-ttu-id="409e5-124">Cela les empêchera de voir qui d’autre est un invité dans l’annuaire.</span><span class="sxs-lookup"><span data-stu-id="409e5-124">This will prevent them from seeing who else is a guest in the directory.</span></span> <span data-ttu-id="409e5-125">Pour ce faire, sous **restrictions d’accès des utilisateurs invités**, sélectionnez **les utilisateurs invités ont un accès limité aux propriétés et l’appartenance aux paramètres d’objets d’annuaire** ou **l’accès des utilisateurs invités est limité aux propriétés et aux appartenances de leurs propres objets d’annuaire**.</span><span class="sxs-lookup"><span data-stu-id="409e5-125">To do this, under **Guest user access restrictions**, select **Guest users have limited access to properties and membership of directory objects settings** or **Guest user access is restricted to properties and memberships of their own directory objects**.</span></span>

## <a name="microsoft-365-groups-guest-settings"></a><span data-ttu-id="409e5-126">Paramètres invités des groupes Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="409e5-126">Microsoft 365 Groups guest settings</span></span>

<span data-ttu-id="409e5-127">Les sites SharePoint modernes utilisent les groupes Microsoft 365 pour contrôler l’accès au site.</span><span class="sxs-lookup"><span data-stu-id="409e5-127">Modern SharePoint sites use Microsoft 365 Groups to control site access.</span></span> <span data-ttu-id="409e5-128">Les paramètres invités des groupes Microsoft 365 doivent être activés pour que l’accès invité dans les sites SharePoint fonctionne.</span><span class="sxs-lookup"><span data-stu-id="409e5-128">The Microsoft 365 Groups guest settings must be turned on in order for guest access in SharePoint sites to work.</span></span>

![Capture d’écran des paramètres d’invité des Groupes Microsoft 365 dans le Centre d’administration Microsoft 365](../media/office-365-groups-guest-settings.png)

<span data-ttu-id="409e5-130">Pour définir les paramètres invités des groupes Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="409e5-130">To set Microsoft 365 Groups guest settings</span></span>

1. <span data-ttu-id="409e5-131">Dans le centre d’administration Microsoft 365, dans le volet de navigation de gauche, développez **paramètres**.</span><span class="sxs-lookup"><span data-stu-id="409e5-131">In the Microsoft 365 admin center, in the left navigation pane, expand **Settings**.</span></span>
2. <span data-ttu-id="409e5-132">Cliquez sur paramètres de l' **organisation**.</span><span class="sxs-lookup"><span data-stu-id="409e5-132">Click **Org settings**.</span></span>
3. <span data-ttu-id="409e5-133">Dans la liste, cliquez sur **groupes Microsoft 365**.</span><span class="sxs-lookup"><span data-stu-id="409e5-133">In the list, click **Microsoft 365 Groups**.</span></span>
4. <span data-ttu-id="409e5-134">Assurez-vous que les **propriétaires de groupe Let ajoutent des personnes extérieures à votre organisation aux groupes Microsoft 365 en tant qu’invités** et laissez les cases à cocher le **contenu des membres du groupe invité** sont tous deux activés.</span><span class="sxs-lookup"><span data-stu-id="409e5-134">Ensure that the **Let group owners add people outside your organization to Microsoft 365 Groups as guests** and **Let guest group members access group content** check boxes are both checked.</span></span>
5. <span data-ttu-id="409e5-135">Si vous avez apporté des modifications, cliquez sur **enregistrer les modifications**.</span><span class="sxs-lookup"><span data-stu-id="409e5-135">If you made changes, click **Save changes**.</span></span>

## <a name="sharepoint-organization-level-sharing-settings"></a><span data-ttu-id="409e5-136">Paramètres de partage au niveau de l’organisation SharePoint</span><span class="sxs-lookup"><span data-stu-id="409e5-136">SharePoint organization-level sharing settings</span></span>

<span data-ttu-id="409e5-137">Pour que les invités aient accès aux sites SharePoint, les paramètres de partage au niveau de l’organisation SharePoint doivent autoriser le partage avec des invités.</span><span class="sxs-lookup"><span data-stu-id="409e5-137">In order for guests to have access to SharePoint sites, the SharePoint organization-level sharing settings must allow for sharing with guests.</span></span>

<span data-ttu-id="409e5-138">Les paramètres au niveau de l’organisation déterminent les paramètres qui seront disponibles pour des sites individuels.</span><span class="sxs-lookup"><span data-stu-id="409e5-138">The organization-level settings determine the settings that will be available for individual sites.</span></span> <span data-ttu-id="409e5-139">Les paramètres de site ne peuvent pas être plus permissants que les paramètres au niveau de l’organisation.</span><span class="sxs-lookup"><span data-stu-id="409e5-139">Site settings cannot be more permissive than the organization-level settings.</span></span>

<span data-ttu-id="409e5-140">Si vous souhaitez autoriser le partage de fichiers et de dossiers non authentifié, sélectionnez **tout le monde**.</span><span class="sxs-lookup"><span data-stu-id="409e5-140">If you want to allow unauthenticated file and folder sharing, choose **Anyone**.</span></span> <span data-ttu-id="409e5-141">Si vous souhaitez vous assurer que toutes les personnes extérieures à votre organisation doivent s’authentifier, choisissez **nouveau et invités existants**.</span><span class="sxs-lookup"><span data-stu-id="409e5-141">If you want to ensure that all people outside your organization have to authenticate, choose **New and existing guests**.</span></span> <span data-ttu-id="409e5-142">Choisissez le paramètre le plus permissif qui sera nécessaire pour tous les sites de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="409e5-142">Choose the most permissive setting that will be needed by any site in your organization.</span></span>

![Capture d’écran des paramètres de partage SharePoint au niveau de l’organisation](../media/sharepoint-organization-external-sharing-controls.png)


<span data-ttu-id="409e5-144">Pour définir les paramètres de partage au niveau de l’organisation SharePoint</span><span class="sxs-lookup"><span data-stu-id="409e5-144">To set SharePoint organization-level sharing settings</span></span>

1. <span data-ttu-id="409e5-145">Dans le centre d’administration 365 de Microsoft, dans le volet de navigation de gauche, sous **centres d’administration**, cliquez sur **SharePoint**.</span><span class="sxs-lookup"><span data-stu-id="409e5-145">In the Microsoft 365 admin center, in the left navigation pane, under **Admin centers**, click **SharePoint**.</span></span>
2. <span data-ttu-id="409e5-146">Dans le centre d’administration SharePoint, dans le volet de navigation de gauche, sous **stratégies**, cliquez sur **partage**.</span><span class="sxs-lookup"><span data-stu-id="409e5-146">In the SharePoint admin center, in the left navigation pane, under **Policies**, click **Sharing**.</span></span>
3. <span data-ttu-id="409e5-147">Assurez-vous que le partage externe pour SharePoint est défini sur **tout le monde** ou sur **des invités nouveaux et existants**.</span><span class="sxs-lookup"><span data-stu-id="409e5-147">Ensure that external sharing for SharePoint is set to **Anyone** or **New and existing guests**.</span></span>
4. <span data-ttu-id="409e5-148">Si vous avez effectué des modifications, cliquez sur **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="409e5-148">If you made changes, click **Save**.</span></span>

## <a name="create-a-site"></a><span data-ttu-id="409e5-149">Créer un site</span><span class="sxs-lookup"><span data-stu-id="409e5-149">Create a site</span></span>

<span data-ttu-id="409e5-150">L’étape suivante consiste à créer le site que vous envisagez d’utiliser pour collaborer avec des invités.</span><span class="sxs-lookup"><span data-stu-id="409e5-150">The next step is to create the site that you plan to use for collaborating with guests.</span></span>

<span data-ttu-id="409e5-151">Pour créer un site</span><span class="sxs-lookup"><span data-stu-id="409e5-151">To create a site</span></span>
1. <span data-ttu-id="409e5-152">Dans le Centre d’administration SharePoint, sous **Sites**, cliquez sur **Sites actifs**.</span><span class="sxs-lookup"><span data-stu-id="409e5-152">In the SharePoint admin center, under **Sites**, click **Active sites**.</span></span>
2. <span data-ttu-id="409e5-153">Cliquez sur **Créer**.</span><span class="sxs-lookup"><span data-stu-id="409e5-153">Click **Create**.</span></span>
3. <span data-ttu-id="409e5-154">Cliquez sur **site d’équipe**.</span><span class="sxs-lookup"><span data-stu-id="409e5-154">Click **Team site**.</span></span>
4. <span data-ttu-id="409e5-155">Tapez un nom de site et entrez un nom pour le propriétaire du groupe (propriétaire du site).</span><span class="sxs-lookup"><span data-stu-id="409e5-155">Type a site name and enter a name for the Group owner (site owner).</span></span>
5. <span data-ttu-id="409e5-156">Sous **Paramètres avancés**, choisissez si vous souhaitez que ce site soit public ou privé.</span><span class="sxs-lookup"><span data-stu-id="409e5-156">Under **Advanced settings**, choose if you want this site to be a public or private one.</span></span>
6. <span data-ttu-id="409e5-157">Cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="409e5-157">Click **Next**.</span></span>
7. <span data-ttu-id="409e5-158">Cliquez sur **Terminer**.</span><span class="sxs-lookup"><span data-stu-id="409e5-158">Click **Finish**.</span></span>

<span data-ttu-id="409e5-159">Nous allons inviter les utilisateurs ultérieurement.</span><span class="sxs-lookup"><span data-stu-id="409e5-159">We'll invite users later.</span></span> <span data-ttu-id="409e5-160">Ensuite, il est important de vérifier les paramètres de partage au niveau du site pour ce site.</span><span class="sxs-lookup"><span data-stu-id="409e5-160">Next, it's important to check the site-level sharing settings for this site.</span></span>

## <a name="sharepoint-site-level-sharing-settings"></a><span data-ttu-id="409e5-161">Paramètres de partage au niveau du site SharePoint</span><span class="sxs-lookup"><span data-stu-id="409e5-161">SharePoint site-level sharing settings</span></span>

<span data-ttu-id="409e5-162">Vérifiez les paramètres de partage au niveau du site pour vous assurer qu’ils autorisent le type d’accès souhaité pour ce site.</span><span class="sxs-lookup"><span data-stu-id="409e5-162">Check the site-level sharing settings to make sure that they allow the type of access that you want for this site.</span></span> <span data-ttu-id="409e5-163">Par exemple, si vous définissez les paramètres au niveau de l’organisation sur tous les **utilisateurs**, mais que vous souhaitez que tous les invités s’authentifient pour ce site, assurez-vous que les paramètres de partage au niveau du site sont définis sur **nouveaux et invités existants**.</span><span class="sxs-lookup"><span data-stu-id="409e5-163">For example, if you set the organization-level settings to **Anyone**, but you want all guests to authenticate for this site, then make sure the site-level sharing settings are set to **New and existing guests**.</span></span>

<span data-ttu-id="409e5-164">Notez que le site ne peut pas être partagé avec des personnes non authentifiées (paramètre**tout le monde** ), mais avec des fichiers et dossiers individuels.</span><span class="sxs-lookup"><span data-stu-id="409e5-164">Note that the site cannot be shared with unauthenticated people (**Anyone** setting), but individual files and folders can.</span></span>

![Capture d’écran des paramètres de partage externe de site SharePoint](../media/sharepoint-site-external-sharing-settings.png)

<span data-ttu-id="409e5-166">Pour définir les paramètres de partage au niveau du site</span><span class="sxs-lookup"><span data-stu-id="409e5-166">To set site-level sharing settings</span></span>
1. <span data-ttu-id="409e5-167">Dans le centre d’administration SharePoint, dans le volet de navigation de gauche, développez **Sites** et cliquez sur **Sites actifs**.</span><span class="sxs-lookup"><span data-stu-id="409e5-167">In the SharePoint admin center, in the left navigation, expand **Sites** and click **Active sites**.</span></span>
2. <span data-ttu-id="409e5-168">Sélectionnez le site que vous souhaitez partager.</span><span class="sxs-lookup"><span data-stu-id="409e5-168">Select the site that you want to share.</span></span>
3. <span data-ttu-id="409e5-169">Cliquez sur..., puis sur **partage**.</span><span class="sxs-lookup"><span data-stu-id="409e5-169">Click ..., and click **Sharing**.</span></span>
4. <span data-ttu-id="409e5-170">Assurez-vous que le partage est défini sur **tout le monde** ou sur **des invités nouveaux et existants**.</span><span class="sxs-lookup"><span data-stu-id="409e5-170">Ensure that sharing is set to **Anyone** or **New and existing guests**.</span></span>
5. <span data-ttu-id="409e5-171">Si vous avez effectué des modifications, cliquez sur **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="409e5-171">If you made changes, click **Save**.</span></span>

## <a name="invite-users"></a><span data-ttu-id="409e5-172">Inviter des utilisateurs</span><span class="sxs-lookup"><span data-stu-id="409e5-172">Invite users</span></span>

<span data-ttu-id="409e5-173">Les paramètres de partage des invités sont désormais configurés, de sorte que vous pouvez commencer à ajouter des utilisateurs et des invités internes à votre site.</span><span class="sxs-lookup"><span data-stu-id="409e5-173">Guest sharing settings are now configured, so you can start adding internal users and guests to your site.</span></span> <span data-ttu-id="409e5-174">L’accès au site est contrôlé par le biais du groupe Microsoft 365 associé, c’est pourquoi nous allons y ajouter des utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="409e5-174">Site access is controlled through the associated Microsoft 365 Group, so we'll be adding users there.</span></span>

<span data-ttu-id="409e5-175">Pour inviter des utilisateurs internes à un groupe</span><span class="sxs-lookup"><span data-stu-id="409e5-175">To invite internal users to a group</span></span>
1. <span data-ttu-id="409e5-176">Accédez au site où vous souhaitez ajouter des utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="409e5-176">Navigate to the site where you want to add users.</span></span>
2. <span data-ttu-id="409e5-177">Cliquez sur le lien **membres** dans le coin supérieur droit, qui indique le nombre de membres.</span><span class="sxs-lookup"><span data-stu-id="409e5-177">Click **Members** link in the upper right which denotes the member count.</span></span>
3. <span data-ttu-id="409e5-178">Cliquez sur **Ajouter des membres**.</span><span class="sxs-lookup"><span data-stu-id="409e5-178">Click **Add members**.</span></span>
4. <span data-ttu-id="409e5-179">Tapez les noms ou les adresses de messagerie des utilisateurs que vous souhaitez inviter sur le site, puis cliquez sur **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="409e5-179">Type the names or email addresses of the users that you want to invite to the site, and then click **Save**.</span></span>

<span data-ttu-id="409e5-180">Les utilisateurs invités ne peuvent pas être ajoutés à partir du site.</span><span class="sxs-lookup"><span data-stu-id="409e5-180">Guest users can't be added from the site.</span></span> <span data-ttu-id="409e5-181">Vous devez les ajouter à l’aide d’Outlook sur le Web.</span><span class="sxs-lookup"><span data-stu-id="409e5-181">You need to add them using Outlook on the web.</span></span> <span data-ttu-id="409e5-182">Par conséquent, en tant que prérequis pour ajouter et inviter des invités à un groupe, cliquez sur l’URL du site dans la colonne **URL**  pour accéder à la page propre au site.</span><span class="sxs-lookup"><span data-stu-id="409e5-182">Therefore, as a prerequisite to add and invite guests to a group, click the URL of the site in the **URL**  column to navigate to the site-specific page.</span></span> <span data-ttu-id="409e5-183">À partir de cette page, cliquez sur l’icône du **lanceur d’applications** et sélectionnez **Outlook**.</span><span class="sxs-lookup"><span data-stu-id="409e5-183">From this page, click the **App launcher** icon and select **Outlook**.</span></span> <span data-ttu-id="409e5-184">Il s’agit de l’écran à partir duquel vous pouvez inviter des invités à un groupe, pour lequel la procédure est décrite ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="409e5-184">This is the screen from which you can invite guests into a group, for which procedure is described below.</span></span>

<span data-ttu-id="409e5-185">Pour inviter des invités à un groupe</span><span class="sxs-lookup"><span data-stu-id="409e5-185">To invite guests to a group</span></span>
1. <span data-ttu-id="409e5-186">Sous **groupes**, cliquez sur le groupe auquel vous souhaitez inviter des invités.</span><span class="sxs-lookup"><span data-stu-id="409e5-186">Under **Groups**, click the group to which you want to invite guests.</span></span>
2. <span data-ttu-id="409e5-187">Ouvrez la carte de visite de groupe, cliquez sur le lien **membres** dans le coin supérieur droit (le lien qui indique le nombre de membres).</span><span class="sxs-lookup"><span data-stu-id="409e5-187">Open the group contact card, click **Members** link in the upper right (the link which denotes the member count).</span></span>
3. <span data-ttu-id="409e5-188">Cliquez sur **Ajouter des membres**.</span><span class="sxs-lookup"><span data-stu-id="409e5-188">click **Add members**.</span></span>
4. <span data-ttu-id="409e5-189">Tapez les adresses de messagerie des invités que vous souhaitez inviter, puis cliquez sur **Ajouter**.</span><span class="sxs-lookup"><span data-stu-id="409e5-189">Type the email addresses of the guests that you want to invite, and then click **Add**.</span></span>
5. <span data-ttu-id="409e5-190">Cliquez sur **Fermer**.</span><span class="sxs-lookup"><span data-stu-id="409e5-190">Click **Close**.</span></span>
<span data-ttu-id="409e5-191">Notez que vous devez cliquer sur **Fermer** uniquement si vous n’êtes pas le propriétaire du groupe et, par conséquent, si vous n’êtes pas autorisé à ajouter l’invité dans le groupe.</span><span class="sxs-lookup"><span data-stu-id="409e5-191">Note that you need to click **Close** only if you are not the owner of the group and as a result, you are not allowed to add the guest into the group.</span></span> <span data-ttu-id="409e5-192">Dans ce cas, la demande d’ajout de l’invité au groupe est transférée au propriétaire du groupe pour approbation.</span><span class="sxs-lookup"><span data-stu-id="409e5-192">In such cases, the request to add the guest into the group is transferred to the group owner for approval.</span></span>

## <a name="see-also"></a><span data-ttu-id="409e5-193">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="409e5-193">See also</span></span>

[<span data-ttu-id="409e5-194">Meilleures pratiques relatives au partage de fichiers et de dossiers avec des utilisateurs non authentifiés</span><span class="sxs-lookup"><span data-stu-id="409e5-194">Best practices for sharing files and folders with unauthenticated users</span></span>](best-practices-anonymous-sharing.md)

[<span data-ttu-id="409e5-195">Limiter l’exposition accidentelle aux fichiers lors du partage avec des invités</span><span class="sxs-lookup"><span data-stu-id="409e5-195">Limit accidental exposure to files when sharing with guests</span></span>](share-limit-accidental-exposure.md)

[<span data-ttu-id="409e5-196">Créer un environnement de partage sécurisé avec des invités</span><span class="sxs-lookup"><span data-stu-id="409e5-196">Create a secure guest sharing environment</span></span>](create-secure-guest-sharing-environment.md)

[<span data-ttu-id="409e5-197">Créer un extranet B2B avec des invités gérés</span><span class="sxs-lookup"><span data-stu-id="409e5-197">Create a B2B extranet with managed guests</span></span>](b2b-extranet.md)

[<span data-ttu-id="409e5-198">Intégration de SharePoint et de OneDrive avec Azure AD B2B</span><span class="sxs-lookup"><span data-stu-id="409e5-198">SharePoint and OneDrive integration with Azure AD B2B</span></span>](https://docs.microsoft.com/sharepoint/sharepoint-azureb2b-integration-preview)
