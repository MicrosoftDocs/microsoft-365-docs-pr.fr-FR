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
- m365initiative-externalcollab
ms.custom:
- seo-marvel-apr2020
localization_priority: Normal
f1.keywords: NOCSH
recommendations: false
description: Découvrez les étapes Microsoft 365 configuration requises pour configurer un site SharePoint pour la collaboration avec des invités.
ms.openlocfilehash: f91b9c64dbdca8ed7e3ada3315cb57f1c728f838
ms.sourcegitcommit: f780de91bc00caeb1598781e0076106c76234bad
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/19/2021
ms.locfileid: "52539250"
---
# <a name="collaborate-with-guests-in-a-site"></a><span data-ttu-id="5292d-103">Collaborer avec des invités sur un site</span><span class="sxs-lookup"><span data-stu-id="5292d-103">Collaborate with guests in a site</span></span>

<span data-ttu-id="5292d-104">Si vous avez besoin de collaborer avec des invités dans des documents, des données et des listes, vous pouvez utiliser un site SharePoint web.</span><span class="sxs-lookup"><span data-stu-id="5292d-104">If you need to collaborate with guests across documents, data, and lists, you can use a SharePoint site.</span></span> <span data-ttu-id="5292d-105">Les sites SharePoint modernes sont connectés à des groupes Microsoft 365 et peuvent gérer l’appartenance au site et fournir des outils de collaboration supplémentaires tels qu’une boîte aux lettres partagée et un calendrier.</span><span class="sxs-lookup"><span data-stu-id="5292d-105">Modern SharePoint sites are connected to Microsoft 365 Groups and can manage the site membership and provide additional collaboration tools such as a shared mailbox and a calendar.</span></span>

<span data-ttu-id="5292d-106">Dans cet article, nous allons passer en revue les étapes de configuration Microsoft 365 nécessaires pour configurer un site SharePoint collaboration avec des invités.</span><span class="sxs-lookup"><span data-stu-id="5292d-106">In this article, we'll walk through the Microsoft 365 configuration steps necessary to set up a SharePoint site for collaboration with guests.</span></span>

## <a name="video-demonstration"></a><span data-ttu-id="5292d-107">Démonstration vidéo</span><span class="sxs-lookup"><span data-stu-id="5292d-107">Video demonstration</span></span>

<span data-ttu-id="5292d-108">Cette vidéo décrit les étapes de configuration décrites dans ce document.</span><span class="sxs-lookup"><span data-stu-id="5292d-108">This video shows the configuration steps described in this document.</span></span></br>

> [!VIDEO https://www.microsoft.com/videoplayer/embed/RE44Llg?autoplay=false]

## <a name="azure-external-collaboration-settings"></a><span data-ttu-id="5292d-109">Paramètres de collaboration externe Azure</span><span class="sxs-lookup"><span data-stu-id="5292d-109">Azure external collaboration settings</span></span>

<span data-ttu-id="5292d-110">Le partage dans Microsoft 365 est régi à son niveau le plus élevé par les [paramètres de collaboration externe B2B dans Azure Active Directory](/azure/active-directory/external-identities/delegate-invitations).</span><span class="sxs-lookup"><span data-stu-id="5292d-110">Sharing in Microsoft 365 is governed at its highest level by the [B2B external collaboration settings in Azure Active Directory](/azure/active-directory/external-identities/delegate-invitations).</span></span> <span data-ttu-id="5292d-111">Si le partage invité est désactivé ou restreint dans Azure AD, ce paramètre remplace les paramètres de partage que vous configurez dans Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="5292d-111">If guest sharing is disabled or restricted in Azure AD, this setting overrides any sharing settings that you configure in Microsoft 365.</span></span>

<span data-ttu-id="5292d-112">Vérifiez les paramètres de collaboration externe B2B pour vous assurer que le partage avec des invités n’est pas bloqué.</span><span class="sxs-lookup"><span data-stu-id="5292d-112">Check the B2B external collaboration settings to ensure that sharing with guests is not blocked.</span></span>

![Capture d’écran Azure Active Directory page Paramètres collaboration externe](../media/azure-ad-organizational-relationships-settings.png)

<span data-ttu-id="5292d-114">Pour définir les paramètres de collaboration externe</span><span class="sxs-lookup"><span data-stu-id="5292d-114">To set external collaboration settings</span></span>

1. <span data-ttu-id="5292d-115">Connectez-vous à Azure Active Directory sur [https://aad.portal.azure.com](https://aad.portal.azure.com).</span><span class="sxs-lookup"><span data-stu-id="5292d-115">Log in to Azure Active Directory at [https://aad.portal.azure.com](https://aad.portal.azure.com).</span></span>
2. <span data-ttu-id="5292d-116">Dans le volet de navigation gauche, cliquez sur **Azure Active Directory**.</span><span class="sxs-lookup"><span data-stu-id="5292d-116">In the left navigation pane, click **Azure Active Directory**.</span></span>
3. <span data-ttu-id="5292d-117">Cliquez sur **Identités externes**.</span><span class="sxs-lookup"><span data-stu-id="5292d-117">Click **External identities**.</span></span>
4. <span data-ttu-id="5292d-118">Dans l’écran **Prise en main**, dans le volet de navigation gauche, cliquez sur **Paramètres de collaboration externe**.</span><span class="sxs-lookup"><span data-stu-id="5292d-118">On the **Get started** screen, in the left navigation pane, click **External collaboration settings**.</span></span>
5. <span data-ttu-id="5292d-119">Assurez-vous que **Les administrateurs et les utilisateurs membres du rôle Inviteur d’invités peuvent envoyer des invitations** et **Les membres peuvent inviter** sont tous deux définis sur **Oui**.</span><span class="sxs-lookup"><span data-stu-id="5292d-119">Ensure that **Admins and users in the guest inviter role can invite** and **Members can invite** are both set to **Yes**.</span></span>
6. <span data-ttu-id="5292d-120">Si vous avez effectué des modifications, cliquez sur **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="5292d-120">If you made changes, click **Save**.</span></span>

<span data-ttu-id="5292d-121">Notez les paramètres dans la section **Restrictions de collaboration**.</span><span class="sxs-lookup"><span data-stu-id="5292d-121">Note the settings in the **Collaboration restrictions** section.</span></span> <span data-ttu-id="5292d-122">Assurez-vous que les domaines des invités avec qui vous voulez collaborer ne sont pas bloqués.</span><span class="sxs-lookup"><span data-stu-id="5292d-122">Make sure that the domains of the guests that you want to collaborate with aren't blocked.</span></span>

<span data-ttu-id="5292d-123">Si vous travaillez avec des invités de plusieurs organisations, vous souhaiterez peut-être restreindre leur capacité à accéder aux données d’annuaire.</span><span class="sxs-lookup"><span data-stu-id="5292d-123">If you work with guests from multiple organizations, you may want to restrict their ability to access directory data.</span></span> <span data-ttu-id="5292d-124">Cela les empêche de voir qui d’autre est invité dans l’annuaire.</span><span class="sxs-lookup"><span data-stu-id="5292d-124">This will prevent them from seeing who else is a guest in the directory.</span></span> <span data-ttu-id="5292d-125">Pour ce faire, sous **Restrictions d’accès des utilisateurs invités**, sélectionnez **Les utilisateurs invités ont un accès limité aux propriétés et à l’appartenance aux paramètres des objets d’annuaire** ou **L’accès des utilisateurs invités est limité aux propriétés et à l’appartenance à leurs propres objets d’annuaire**.</span><span class="sxs-lookup"><span data-stu-id="5292d-125">To do this, under **Guest user access restrictions**, select **Guest users have limited access to properties and membership of directory objects settings** or **Guest user access is restricted to properties and memberships of their own directory objects**.</span></span>

## <a name="microsoft-365-groups-guest-settings"></a><span data-ttu-id="5292d-126">Paramètres invités des groupes Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="5292d-126">Microsoft 365 Groups guest settings</span></span>

<span data-ttu-id="5292d-127">Les sites SharePoint modernes utilisent Microsoft 365 groupes pour contrôler l’accès au site.</span><span class="sxs-lookup"><span data-stu-id="5292d-127">Modern SharePoint sites use Microsoft 365 Groups to control site access.</span></span> <span data-ttu-id="5292d-128">Les paramètres Microsoft 365 groupes d’invités doivent être allumés pour que l’accès invité SharePoint sites fonctionne.</span><span class="sxs-lookup"><span data-stu-id="5292d-128">The Microsoft 365 Groups guest settings must be turned on in order for guest access in SharePoint sites to work.</span></span>

![Capture d’écran des paramètres d’invité des Groupes Microsoft 365 dans le Centre d’administration Microsoft 365](../media/office-365-groups-guest-settings.png)

<span data-ttu-id="5292d-130">Pour définir les paramètres invités des groupes Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="5292d-130">To set Microsoft 365 Groups guest settings</span></span>

1. <span data-ttu-id="5292d-131">Dans le Centre d’administration Microsoft 365, dans le volet de navigation gauche, développez **Paramètres**.</span><span class="sxs-lookup"><span data-stu-id="5292d-131">In the Microsoft 365 admin center, in the left navigation pane, expand **Settings**.</span></span>
2. <span data-ttu-id="5292d-132">Cliquez sur **Paramètres de l’organisation**.</span><span class="sxs-lookup"><span data-stu-id="5292d-132">Click **Org settings**.</span></span>
3. <span data-ttu-id="5292d-133">Dans la liste, cliquez sur **Groupes Microsoft 365**.</span><span class="sxs-lookup"><span data-stu-id="5292d-133">In the list, click **Microsoft 365 Groups**.</span></span>
4. <span data-ttu-id="5292d-134">Assurez-vous que les cases à cocher **Permettre aux propriétaires de groupe d’ajouter des personnes externes à votre organisation à des groupes Microsoft 365 en tant qu'invités** et **Permettre aux membres du groupe invités d’accéder au contenu du groupe** sont cochées.</span><span class="sxs-lookup"><span data-stu-id="5292d-134">Ensure that the **Let group owners add people outside your organization to Microsoft 365 Groups as guests** and **Let guest group members access group content** check boxes are both checked.</span></span>
5. <span data-ttu-id="5292d-135">Si vous avez effectué des modifications, cliquez sur **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="5292d-135">If you made changes, click **Save changes**.</span></span>

## <a name="sharepoint-organization-level-sharing-settings"></a><span data-ttu-id="5292d-136">SharePoint de partage au niveau de l’organisation</span><span class="sxs-lookup"><span data-stu-id="5292d-136">SharePoint organization-level sharing settings</span></span>

<span data-ttu-id="5292d-137">Pour que les invités ont accès à SharePoint sites web, les paramètres SharePoint de partage au niveau de l’organisation doivent autoriser le partage avec des invités.</span><span class="sxs-lookup"><span data-stu-id="5292d-137">In order for guests to have access to SharePoint sites, the SharePoint organization-level sharing settings must allow for sharing with guests.</span></span>

<span data-ttu-id="5292d-138">Les paramètres au niveau de l’organisation déterminent les paramètres qui seront disponibles pour les sites individuels.</span><span class="sxs-lookup"><span data-stu-id="5292d-138">The organization-level settings determine the settings that will be available for individual sites.</span></span> <span data-ttu-id="5292d-139">Les paramètres de site ne peuvent pas être plus permissifs que les paramètres au niveau de l’organisation.</span><span class="sxs-lookup"><span data-stu-id="5292d-139">Site settings cannot be more permissive than the organization-level settings.</span></span>

<span data-ttu-id="5292d-140">Si vous souhaitez autoriser le partage de fichiers et de dossiers non authentifiés, choisissez **Tout le monde.**</span><span class="sxs-lookup"><span data-stu-id="5292d-140">If you want to allow unauthenticated file and folder sharing, choose **Anyone**.</span></span> <span data-ttu-id="5292d-141">Si vous souhaitez vous assurer que toutes les personnes extérieures à votre organisation doivent s’authentifier, choisissez Invités nouveaux **et existants.**</span><span class="sxs-lookup"><span data-stu-id="5292d-141">If you want to ensure that all people outside your organization have to authenticate, choose **New and existing guests**.</span></span> <span data-ttu-id="5292d-142">Choisissez le paramètre le plus permissif qui sera nécessaire pour n’importe quel site de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="5292d-142">Choose the most permissive setting that will be needed by any site in your organization.</span></span>

![Capture d’écran des paramètres de partage SharePoint au niveau de l’organisation](../media/sharepoint-organization-external-sharing-controls.png)


<span data-ttu-id="5292d-144">Pour définir les paramètres de partage SharePoint au niveau de l’organisation</span><span class="sxs-lookup"><span data-stu-id="5292d-144">To set SharePoint organization-level sharing settings</span></span>

1. <span data-ttu-id="5292d-145">Dans le Centre d’administration Microsoft 365, dans le volet de navigation gauche, sous **Centres d’administration**, cliquez sur **SharePoint**.</span><span class="sxs-lookup"><span data-stu-id="5292d-145">In the Microsoft 365 admin center, in the left navigation pane, under **Admin centers**, click **SharePoint**.</span></span>
2. <span data-ttu-id="5292d-146">Dans le SharePoint d’administration, dans le volet de navigation de gauche, sous **Stratégies,** cliquez sur **Partage.**</span><span class="sxs-lookup"><span data-stu-id="5292d-146">In the SharePoint admin center, in the left navigation pane, under **Policies**, click **Sharing**.</span></span>
3. <span data-ttu-id="5292d-147">Assurez-vous que le partage externe pour SharePoint est **Tout le monde** ou **Invités nouveaux et existants**.</span><span class="sxs-lookup"><span data-stu-id="5292d-147">Ensure that external sharing for SharePoint is set to **Anyone** or **New and existing guests**.</span></span>
4. <span data-ttu-id="5292d-148">Si vous avez effectué des modifications, cliquez sur **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="5292d-148">If you made changes, click **Save**.</span></span>

## <a name="create-a-site"></a><span data-ttu-id="5292d-149">Créer un site</span><span class="sxs-lookup"><span data-stu-id="5292d-149">Create a site</span></span>

<span data-ttu-id="5292d-150">L’étape suivante consiste à créer le site que vous prévoyez d’utiliser pour collaborer avec des invités.</span><span class="sxs-lookup"><span data-stu-id="5292d-150">The next step is to create the site that you plan to use for collaborating with guests.</span></span>

<span data-ttu-id="5292d-151">Pour créer un site</span><span class="sxs-lookup"><span data-stu-id="5292d-151">To create a site</span></span>
1. <span data-ttu-id="5292d-152">Dans le Centre d’administration SharePoint, sous **Sites**, cliquez sur **Sites actifs**.</span><span class="sxs-lookup"><span data-stu-id="5292d-152">In the SharePoint admin center, under **Sites**, click **Active sites**.</span></span>
2. <span data-ttu-id="5292d-153">Cliquez sur **Créer**.</span><span class="sxs-lookup"><span data-stu-id="5292d-153">Click **Create**.</span></span>
3. <span data-ttu-id="5292d-154">Cliquez **sur Site d’équipe.**</span><span class="sxs-lookup"><span data-stu-id="5292d-154">Click **Team site**.</span></span>
4. <span data-ttu-id="5292d-155">Tapez un nom de site et entrez un nom pour le propriétaire du groupe (propriétaire du site).</span><span class="sxs-lookup"><span data-stu-id="5292d-155">Type a site name and enter a name for the Group owner (site owner).</span></span>
5. <span data-ttu-id="5292d-156">Sous **Paramètres avancés,** choisissez si vous souhaitez que ce site soit public ou privé.</span><span class="sxs-lookup"><span data-stu-id="5292d-156">Under **Advanced settings**, choose if you want this site to be a public or private one.</span></span>
6. <span data-ttu-id="5292d-157">Cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="5292d-157">Click **Next**.</span></span>
7. <span data-ttu-id="5292d-158">Cliquez sur **Terminer**.</span><span class="sxs-lookup"><span data-stu-id="5292d-158">Click **Finish**.</span></span>

<span data-ttu-id="5292d-159">Nous inviterons des utilisateurs plus tard.</span><span class="sxs-lookup"><span data-stu-id="5292d-159">We'll invite users later.</span></span> <span data-ttu-id="5292d-160">Ensuite, il est important de vérifier les paramètres de partage au niveau du site pour ce site.</span><span class="sxs-lookup"><span data-stu-id="5292d-160">Next, it's important to check the site-level sharing settings for this site.</span></span>

## <a name="sharepoint-site-level-sharing-settings"></a><span data-ttu-id="5292d-161">Paramètres de SharePoint au niveau du site</span><span class="sxs-lookup"><span data-stu-id="5292d-161">SharePoint site-level sharing settings</span></span>

<span data-ttu-id="5292d-162">Vérifiez les paramètres de partage au niveau du site pour vous assurer qu’ils autorisent le type d’accès que vous souhaitez pour ce site.</span><span class="sxs-lookup"><span data-stu-id="5292d-162">Check the site-level sharing settings to make sure that they allow the type of access that you want for this site.</span></span> <span data-ttu-id="5292d-163">Par exemple, si vous définissez les paramètres au niveau de l’organisation sur Tout le **monde,** mais que vous souhaitez que tous les invités s’authentifier pour ce site, assurez-vous que les paramètres de partage au niveau du site sont les invités nouveaux et existants. </span><span class="sxs-lookup"><span data-stu-id="5292d-163">For example, if you set the organization-level settings to **Anyone**, but you want all guests to authenticate for this site, then make sure the site-level sharing settings are set to **New and existing guests**.</span></span>

<span data-ttu-id="5292d-164">Notez que le site ne peut pas être partagé avec des personnes non authentifiés **(paramètre** Tout le monde), mais que des fichiers et dossiers individuels le peuvent.</span><span class="sxs-lookup"><span data-stu-id="5292d-164">Note that the site cannot be shared with unauthenticated people (**Anyone** setting), but individual files and folders can.</span></span>

<span data-ttu-id="5292d-165">Vous pouvez également utiliser des [étiquettes de sensibilité pour contrôler les paramètres](../compliance/sensitivity-labels-teams-groups-sites.md)de partage externe pour SharePoint sites.</span><span class="sxs-lookup"><span data-stu-id="5292d-165">You can also use [sensitivity labels to control external sharing settings for SharePoint sites](../compliance/sensitivity-labels-teams-groups-sites.md).</span></span>

![Capture d’écran des paramètres de partage externe de site SharePoint](../media/sharepoint-site-external-sharing-settings.png)

<span data-ttu-id="5292d-167">Pour définir les paramètres au niveau du site</span><span class="sxs-lookup"><span data-stu-id="5292d-167">To set site-level sharing settings</span></span>
1. <span data-ttu-id="5292d-168">Dans le centre d’administration SharePoint, dans le volet de navigation de gauche, développez **Sites** et cliquez sur **Sites actifs**.</span><span class="sxs-lookup"><span data-stu-id="5292d-168">In the SharePoint admin center, in the left navigation, expand **Sites** and click **Active sites**.</span></span>
2. <span data-ttu-id="5292d-169">Sélectionnez le site que vous souhaitez partager.</span><span class="sxs-lookup"><span data-stu-id="5292d-169">Select the site that you want to share.</span></span>
3. <span data-ttu-id="5292d-170">Cliquez sur ..., puis sur **Partage.**</span><span class="sxs-lookup"><span data-stu-id="5292d-170">Click ..., and click **Sharing**.</span></span>
4. <span data-ttu-id="5292d-171">Assurez-vous que le partage est paramétré sur **Tout le monde** ou **Invités nouveaux et existants**.</span><span class="sxs-lookup"><span data-stu-id="5292d-171">Ensure that sharing is set to **Anyone** or **New and existing guests**.</span></span>
5. <span data-ttu-id="5292d-172">Si vous avez effectué des modifications, cliquez sur **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="5292d-172">If you made changes, click **Save**.</span></span>

## <a name="invite-users"></a><span data-ttu-id="5292d-173">Inviter des utilisateurs</span><span class="sxs-lookup"><span data-stu-id="5292d-173">Invite users</span></span>

<span data-ttu-id="5292d-174">Les paramètres de partage d’invités sont désormais configurés, afin que vous pouvez commencer à ajouter des utilisateurs internes et des invités à votre site.</span><span class="sxs-lookup"><span data-stu-id="5292d-174">Guest sharing settings are now configured, so you can start adding internal users and guests to your site.</span></span> <span data-ttu-id="5292d-175">L’accès au site est contrôlé par le groupe Microsoft 365 associé, donc nous y ajouterons des utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="5292d-175">Site access is controlled through the associated Microsoft 365 Group, so we'll be adding users there.</span></span>

<span data-ttu-id="5292d-176">Pour inviter des utilisateurs internes à un groupe</span><span class="sxs-lookup"><span data-stu-id="5292d-176">To invite internal users to a group</span></span>
1. <span data-ttu-id="5292d-177">Accédez au site où vous souhaitez ajouter des utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="5292d-177">Navigate to the site where you want to add users.</span></span>
2. <span data-ttu-id="5292d-178">Cliquez **sur Lien** Membres dans le coin supérieur droit qui indique le nombre de membres.</span><span class="sxs-lookup"><span data-stu-id="5292d-178">Click **Members** link in the upper right which denotes the member count.</span></span>
3. <span data-ttu-id="5292d-179">Cliquez sur **Ajouter des membres**.</span><span class="sxs-lookup"><span data-stu-id="5292d-179">Click **Add members**.</span></span>
4. <span data-ttu-id="5292d-180">Tapez les noms ou adresses e-mail des utilisateurs que vous souhaitez inviter sur le site, puis cliquez sur **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="5292d-180">Type the names or email addresses of the users that you want to invite to the site, and then click **Save**.</span></span>

<span data-ttu-id="5292d-181">Les invités ne peuvent pas être ajoutés à partir du site.</span><span class="sxs-lookup"><span data-stu-id="5292d-181">Guests can't be added from the site.</span></span> <span data-ttu-id="5292d-182">Vous devez les ajouter à l’aide Outlook sur le web.</span><span class="sxs-lookup"><span data-stu-id="5292d-182">You need to add them using Outlook on the web.</span></span> <span data-ttu-id="5292d-183">Par conséquent, comme condition préalable pour ajouter et inviter des invités à un groupe, cliquez sur l’URL du site dans la colonne **URL**  pour accéder à la page spécifique au site.</span><span class="sxs-lookup"><span data-stu-id="5292d-183">Therefore, as a prerequisite to add and invite guests to a group, click the URL of the site in the **URL**  column to navigate to the site-specific page.</span></span> <span data-ttu-id="5292d-184">Dans cette page, cliquez sur **l’icône du lanceur** d’applications et **sélectionnez Outlook**.</span><span class="sxs-lookup"><span data-stu-id="5292d-184">From this page, click the **App launcher** icon and select **Outlook**.</span></span> <span data-ttu-id="5292d-185">Il s’agit de l’écran à partir duquel vous pouvez inviter des invités dans un groupe, pour lequel la procédure est décrite ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="5292d-185">This is the screen from which you can invite guests into a group, for which procedure is described below.</span></span>

<span data-ttu-id="5292d-186">Pour inviter des invités à un groupe</span><span class="sxs-lookup"><span data-stu-id="5292d-186">To invite guests to a group</span></span>
1. <span data-ttu-id="5292d-187">Sous **Groupes,** cliquez sur le groupe auquel vous souhaitez inviter des invités.</span><span class="sxs-lookup"><span data-stu-id="5292d-187">Under **Groups**, click the group to which you want to invite guests.</span></span>
2. <span data-ttu-id="5292d-188">Ouvrez la carte de visite du groupe, cliquez sur **Le** lien Membres dans le coin supérieur droit (lien qui indique le nombre de membres).</span><span class="sxs-lookup"><span data-stu-id="5292d-188">Open the group contact card, click **Members** link in the upper right (the link which denotes the member count).</span></span>
3. <span data-ttu-id="5292d-189">cliquez **sur Ajouter des membres.**</span><span class="sxs-lookup"><span data-stu-id="5292d-189">click **Add members**.</span></span>
4. <span data-ttu-id="5292d-190">Tapez les adresses de messagerie des invités que vous souhaitez inviter, puis cliquez sur **Ajouter.**</span><span class="sxs-lookup"><span data-stu-id="5292d-190">Type the email addresses of the guests that you want to invite, and then click **Add**.</span></span>
5. <span data-ttu-id="5292d-191">Cliquez sur **Fermer**.</span><span class="sxs-lookup"><span data-stu-id="5292d-191">Click **Close**.</span></span>
<span data-ttu-id="5292d-192">Notez que vous devez cliquer sur **Fermer** uniquement si vous n’êtes pas le propriétaire du groupe et, par conséquent, vous n’êtes pas autorisé à ajouter l’invité au groupe.</span><span class="sxs-lookup"><span data-stu-id="5292d-192">Note that you need to click **Close** only if you are not the owner of the group and as a result, you are not allowed to add the guest into the group.</span></span> <span data-ttu-id="5292d-193">Dans ce cas, la demande d’ajout de l’invité au groupe est transférée au propriétaire du groupe pour approbation.</span><span class="sxs-lookup"><span data-stu-id="5292d-193">In such cases, the request to add the guest into the group is transferred to the group owner for approval.</span></span>

## <a name="see-also"></a><span data-ttu-id="5292d-194">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5292d-194">See also</span></span>

[<span data-ttu-id="5292d-195">Meilleures pratiques relatives au partage de fichiers et de dossiers avec des utilisateurs non authentifiés</span><span class="sxs-lookup"><span data-stu-id="5292d-195">Best practices for sharing files and folders with unauthenticated users</span></span>](best-practices-anonymous-sharing.md)

[<span data-ttu-id="5292d-196">Limiter l’exposition accidentelle aux fichiers lors du partage avec des invités</span><span class="sxs-lookup"><span data-stu-id="5292d-196">Limit accidental exposure to files when sharing with guests</span></span>](share-limit-accidental-exposure.md)

[<span data-ttu-id="5292d-197">Créer un environnement de partage sécurisé avec des invités</span><span class="sxs-lookup"><span data-stu-id="5292d-197">Create a secure guest sharing environment</span></span>](create-secure-guest-sharing-environment.md)

[<span data-ttu-id="5292d-198">Créer un extranet B2B avec des invités gérés</span><span class="sxs-lookup"><span data-stu-id="5292d-198">Create a B2B extranet with managed guests</span></span>](b2b-extranet.md)

[<span data-ttu-id="5292d-199">Intégration de SharePoint et de OneDrive à Azure AD B2B</span><span class="sxs-lookup"><span data-stu-id="5292d-199">SharePoint and OneDrive integration with Azure AD B2B</span></span>](/sharepoint/sharepoint-azureb2b-integration-preview)