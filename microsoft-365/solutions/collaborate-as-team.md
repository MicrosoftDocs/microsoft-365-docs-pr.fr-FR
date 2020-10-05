---
title: Collaborer avec des invités au sein d’une équipe
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
ms.custom:
- seo-marvel-apr2020
localization_priority: Normal
f1.keywords: NOCSH
description: Découvrez les étapes de configuration de Microsoft 365 nécessaires pour configurer une équipe de collaboration avec des invités dans Teams.
ms.openlocfilehash: e92397c7b8d4a4192fb36a52a76679269be53b3b
ms.sourcegitcommit: 8589323c1b4ab43aab30597ee66303b0a0eb71ed
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/05/2020
ms.locfileid: "48357793"
---
# <a name="collaborate-with-guests-in-a-team"></a><span data-ttu-id="cda91-103">Collaborer avec des invités au sein d’une équipe</span><span class="sxs-lookup"><span data-stu-id="cda91-103">Collaborate with guests in a team</span></span>

<span data-ttu-id="cda91-104">Si vous avez besoin de collaborer avec des invités dans des documents, des tâches et des conversations, nous vous recommandons d’utiliser Microsoft Teams.</span><span class="sxs-lookup"><span data-stu-id="cda91-104">If you need to collaborate with guests across documents, tasks, and conversations, we recommend using Microsoft Teams.</span></span> <span data-ttu-id="cda91-105">Teams fournit toutes les fonctionnalités de collaboration disponibles dans Office et SharePoint avec conversation permanente et un ensemble d’outils de collaboration personnalisable et extensible dans une expérience utilisateur unifiée.</span><span class="sxs-lookup"><span data-stu-id="cda91-105">Teams provides all of the collaboration features available in Office and SharePoint with persistent chat and a customizable and extensible set of collaboration tools in a unified user experience.</span></span>

<span data-ttu-id="cda91-106">Dans cet article, nous allons passer en revue les étapes de configuration de Microsoft 365 nécessaires pour configurer une équipe de collaboration avec des invités.</span><span class="sxs-lookup"><span data-stu-id="cda91-106">In this article, we'll walk through the Microsoft 365 configuration steps necessary to set up a team for collaboration with guests.</span></span>

## <a name="video-demonstration"></a><span data-ttu-id="cda91-107">Démonstration vidéo</span><span class="sxs-lookup"><span data-stu-id="cda91-107">Video demonstration</span></span>

<span data-ttu-id="cda91-108">Cette vidéo présente les étapes de configuration décrites dans ce document.</span><span class="sxs-lookup"><span data-stu-id="cda91-108">This video shows the configuration steps described in this document.</span></span></br>

> [!VIDEO https://www.microsoft.com/videoplayer/embed/RE44NTr?autoplay=false]

## <a name="azure-organizational-relationships-settings"></a><span data-ttu-id="cda91-109">Paramètres Azure de relations organisationnelles</span><span class="sxs-lookup"><span data-stu-id="cda91-109">Azure Organizational relationships settings</span></span>

<span data-ttu-id="cda91-110">Le partage dans Microsoft 365 est régi par les [paramètres de relations organisationnelles dans Azure Active Directory](https://docs.microsoft.com/azure/active-directory/external-identities/delegate-invitations).</span><span class="sxs-lookup"><span data-stu-id="cda91-110">Sharing in Microsoft 365 is governed at its highest level by the [organizational relationships settings in Azure Active Directory](https://docs.microsoft.com/azure/active-directory/external-identities/delegate-invitations).</span></span> <span data-ttu-id="cda91-111">Si le partage d’invités est désactivé ou restreint dans Azure AD, cela remplace tous les paramètres de partage que vous configurez dans Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="cda91-111">If guest sharing is disabled or restricted in Azure AD, this will override any sharing settings that you configure in Microsoft 365.</span></span>

<span data-ttu-id="cda91-112">Vérifiez les paramètres de relations organisationnelles pour vous assurer que le partage avec des invités n’est pas bloqué.</span><span class="sxs-lookup"><span data-stu-id="cda91-112">Check the organizational relationships settings to ensure that sharing with guests is not blocked.</span></span>

![Capture d’écran de la page des paramètres de relations organisationnelles d’Azure Active Directory](../media/azure-ad-organizational-relationships-settings.png)

<span data-ttu-id="cda91-114">Pour définir les paramètres de relation organisationnelle</span><span class="sxs-lookup"><span data-stu-id="cda91-114">To set organizational relationship settings</span></span>

1. <span data-ttu-id="cda91-115">Connectez-vous à Microsoft Azure à l’adresse [https://portal.azure.com](https://portal.azure.com) .</span><span class="sxs-lookup"><span data-stu-id="cda91-115">Log in to Microsoft Azure at [https://portal.azure.com](https://portal.azure.com).</span></span>
2. <span data-ttu-id="cda91-116">Dans le volet de navigation de gauche, cliquez sur **Azure Active Directory**.</span><span class="sxs-lookup"><span data-stu-id="cda91-116">In the left navigation, click **Azure Active Directory**.</span></span>
3. <span data-ttu-id="cda91-117">Dans le volet **Vue d’ensemble** , cliquez sur **Identités externes**.</span><span class="sxs-lookup"><span data-stu-id="cda91-117">In the **Overview** pane, click **External identities**.</span></span>
4. <span data-ttu-id="cda91-118">Dans le volet **identités organisationnelles** , cliquez sur **paramètres de collaboration externe**.</span><span class="sxs-lookup"><span data-stu-id="cda91-118">In the **Organizational identities** pane, click **External collaboration settings**.</span></span>
5. <span data-ttu-id="cda91-119">Assurez-vous que les **administrateurs et les utilisateurs du rôle d’invité invité peuvent inviter** et que les **membres peuvent inviter** sont tous deux la valeur **Oui**.</span><span class="sxs-lookup"><span data-stu-id="cda91-119">Ensure that **Admins and users in the guest inviter role can invite** and **Members can invite** are both set to **Yes**.</span></span>
6. <span data-ttu-id="cda91-120">Si vous avez effectué des modifications, cliquez sur **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="cda91-120">If you made changes, click **Save**.</span></span>

<span data-ttu-id="cda91-121">Notez les paramètres dans la section **restrictions de collaboration** .</span><span class="sxs-lookup"><span data-stu-id="cda91-121">Note the settings in the **Collaboration restrictions** section.</span></span> <span data-ttu-id="cda91-122">Assurez-vous que les domaines des invités avec lesquels vous souhaitez collaborer ne sont pas bloqués.</span><span class="sxs-lookup"><span data-stu-id="cda91-122">Make sure that the domains of the guests that you want to collaborate with aren't blocked.</span></span>

<span data-ttu-id="cda91-123">Si vous travaillez avec des invités de plusieurs organisations, vous souhaiterez peut-être limiter leur capacité à accéder aux données d’annuaire.</span><span class="sxs-lookup"><span data-stu-id="cda91-123">If you work with guests from multiple organizations, you may want to restrict their ability to access directory data.</span></span> <span data-ttu-id="cda91-124">Cela les empêchera de voir qui d’autre est un invité dans l’annuaire.</span><span class="sxs-lookup"><span data-stu-id="cda91-124">This will prevent them from seeing who else is a guest in the directory.</span></span> <span data-ttu-id="cda91-125">Pour ce faire, sous **restrictions d’accès des utilisateurs invités**, sélectionnez **les utilisateurs invités ont un accès limité aux propriétés et l’appartenance aux paramètres d’objets d’annuaire** ou **l’accès des utilisateurs invités est limité aux propriétés et aux appartenances de leurs propres objets d’annuaire**.</span><span class="sxs-lookup"><span data-stu-id="cda91-125">To do this, under **Guest user access restrictions**, select **Guest users have limited access to properties and membership of directory objects settings** or **Guest user access is restricted to properties and memberships of their own directory objects**.</span></span>

## <a name="teams-guest-access-settings"></a><span data-ttu-id="cda91-126">Paramètres d’accès invité de teams</span><span class="sxs-lookup"><span data-stu-id="cda91-126">Teams guest access settings</span></span>

<span data-ttu-id="cda91-127">Teams dispose d’un commutateur maître/inactif pour l’accès invité et de divers paramètres permettant de contrôler ce que les invités peuvent faire dans une équipe.</span><span class="sxs-lookup"><span data-stu-id="cda91-127">Teams has a master on/off switch for guest access and a variety of settings available to control what guests can do in a team.</span></span> <span data-ttu-id="cda91-128">Le commutateur maître, **autoriser l’accès invité dans teams** doit être **activé** pour que l’accès invité fonctionne dans Teams.</span><span class="sxs-lookup"><span data-stu-id="cda91-128">The master switch, **Allow guest access in Teams** must be **On** for guest access to work in Teams.</span></span>

<span data-ttu-id="cda91-129">Vérifiez que l’accès invité est activé dans teams et effectuez les ajustements nécessaires aux paramètres invités en fonction des besoins de votre entreprise.</span><span class="sxs-lookup"><span data-stu-id="cda91-129">Check to ensure that guest access is enabled in Teams and make any adjustment to the guest settings based on your business needs.</span></span> <span data-ttu-id="cda91-130">N’oubliez pas que ces paramètres affectent toutes les équipes.</span><span class="sxs-lookup"><span data-stu-id="cda91-130">Keep in mind that these settings affect all teams.</span></span>

![Capture d’écran du commutateur Accès invité dans Teams](../media/teams-guest-access-toggle-on.png)

<span data-ttu-id="cda91-132">Pour déterminer les paramètres d’accès invité Teams, procédez comme suit :</span><span class="sxs-lookup"><span data-stu-id="cda91-132">To set Teams guest access settings</span></span>

1. <span data-ttu-id="cda91-133">Connectez-vous au Centre d’administration Microsoft 365 sur[https://admin.microsoft.com](https://admin.microsoft.com).</span><span class="sxs-lookup"><span data-stu-id="cda91-133">Log in to the Microsoft 365 admin center at [https://admin.microsoft.com](https://admin.microsoft.com).</span></span>
2. <span data-ttu-id="cda91-134">Dans la barre de navigation de gauche, cliquez sur **Afficher tout**.</span><span class="sxs-lookup"><span data-stu-id="cda91-134">In the left navigation, click **Show all**.</span></span>
3. <span data-ttu-id="cda91-135">Sous **Centres d’administration**, cliquez sur **Teams**.</span><span class="sxs-lookup"><span data-stu-id="cda91-135">Under **Admin centers**, click **Teams**.</span></span>
4. <span data-ttu-id="cda91-136">Dans le Centre d’administration Teams, dans le volet de navigation gauche, développez **Paramètres à l’échelle de l’organisation**, puis cliquez sur **Accès invité**.</span><span class="sxs-lookup"><span data-stu-id="cda91-136">In the Teams admin center, in the left navigation, expand **Org-wide settings** and click **Guest access**.</span></span>
5. <span data-ttu-id="cda91-137">Assurez-vous que **Autoriser l’accès invité dans Teams** est défini sur **Activé**.</span><span class="sxs-lookup"><span data-stu-id="cda91-137">Ensure that **Allow guest access in Teams** is set to **On**.</span></span>
6. <span data-ttu-id="cda91-138">Apportez les modifications souhaitées aux autres paramètres invités, puis cliquez sur **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="cda91-138">Make any desired changes to the additional guest settings, and then click **Save**.</span></span>

> [!NOTE]
> <span data-ttu-id="cda91-139">La mise en service du paramètre invité Teams peut prendre jusqu'à vingt-quatre heures.</span><span class="sxs-lookup"><span data-stu-id="cda91-139">It may take up to twenty-four hours for the Teams guest setting to become active after you turn it on.</span></span>

## <a name="microsoft-365-groups-guest-settings"></a><span data-ttu-id="cda91-140">Paramètres invités des groupes Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="cda91-140">Microsoft 365 Groups guest settings</span></span>

<span data-ttu-id="cda91-141">Teams utilise les groupes Microsoft 365 pour les membres de l’équipe.</span><span class="sxs-lookup"><span data-stu-id="cda91-141">Teams uses Microsoft 365 Groups for team membership.</span></span> <span data-ttu-id="cda91-142">Les paramètres invités des groupes Microsoft 365 doivent être activés pour que l’accès invité dans teams puisse fonctionner.</span><span class="sxs-lookup"><span data-stu-id="cda91-142">The Microsoft 365 Groups guest settings must be turned on in order for guest access in Teams to work.</span></span>

![Capture d’écran des paramètres d’invité des Groupes Microsoft 365 dans le Centre d’administration Microsoft 365](../media/office-365-groups-guest-settings.png)

<span data-ttu-id="cda91-144">Pour définir les paramètres invités des groupes Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="cda91-144">To set Microsoft 365 Groups guest settings</span></span>

1. <span data-ttu-id="cda91-145">Dans le centre d’administration Microsoft 365, dans le volet de navigation de gauche, développez **paramètres**.</span><span class="sxs-lookup"><span data-stu-id="cda91-145">In the Microsoft 365 admin center, in the left navigation, expand **Settings**.</span></span>
2. <span data-ttu-id="cda91-146">Cliquez sur paramètres de l' **organisation**.</span><span class="sxs-lookup"><span data-stu-id="cda91-146">Click **Org settings**.</span></span>
3. <span data-ttu-id="cda91-147">Dans la liste, cliquez sur **groupes Microsoft 365**.</span><span class="sxs-lookup"><span data-stu-id="cda91-147">In the list, click **Microsoft 365 Groups**.</span></span>
4. <span data-ttu-id="cda91-148">Assurez-vous que les **membres de groupe Let en dehors de votre organisation accèdent au contenu de groupe** et que les **propriétaires de groupes ajoutent des personnes en dehors de votre organisation aux** cases à cocher sont activées.</span><span class="sxs-lookup"><span data-stu-id="cda91-148">Ensure that the **Let group members outside your organization access group content** and **Let group owners add people outside your organization to groups** check boxes are both checked.</span></span>
5. <span data-ttu-id="cda91-149">Si vous avez apporté des modifications, cliquez sur **enregistrer les modifications**.</span><span class="sxs-lookup"><span data-stu-id="cda91-149">If you made changes, click **Save changes**.</span></span>


## <a name="sharepoint-organization-level-sharing-settings"></a><span data-ttu-id="cda91-150">Paramètres de partage au niveau de l’organisation SharePoint</span><span class="sxs-lookup"><span data-stu-id="cda91-150">SharePoint organization level sharing settings</span></span>

<span data-ttu-id="cda91-151">Le contenu de teams, tel que des fichiers, des dossiers et des listes, est tous stockés dans SharePoint.</span><span class="sxs-lookup"><span data-stu-id="cda91-151">Teams content such as files, folders, and lists are all stored in SharePoint.</span></span> <span data-ttu-id="cda91-152">Pour que les invités aient accès à ces éléments dans Teams, les paramètres de partage au niveau de l’organisation SharePoint doivent autoriser le partage avec des invités.</span><span class="sxs-lookup"><span data-stu-id="cda91-152">In order for guests to have access to these items in Teams, the SharePoint organization-level sharing settings must allow for sharing with guests.</span></span>

<span data-ttu-id="cda91-153">Les paramètres au niveau de l’organisation déterminent les paramètres disponibles pour des sites individuels, y compris les sites associés à Teams.</span><span class="sxs-lookup"><span data-stu-id="cda91-153">The organization-level settings determine what settings are available for individual sites, including sites associated with teams.</span></span> <span data-ttu-id="cda91-154">Les paramètres de site ne peuvent pas être plus permissants que les paramètres au niveau de l’organisation.</span><span class="sxs-lookup"><span data-stu-id="cda91-154">Site settings cannot be more permissive than the organization-level settings.</span></span>

<span data-ttu-id="cda91-155">Si vous souhaitez autoriser le partage de fichiers et de dossiers avec des personnes non authentifiées, sélectionnez **tout le monde**.</span><span class="sxs-lookup"><span data-stu-id="cda91-155">If you want to allow file and folder sharing with unauthenticated people, choose **Anyone**.</span></span> <span data-ttu-id="cda91-156">Si vous souhaitez vous assurer que tous les invités doivent s’authentifier, choisissez **nouveau et invités existants**.</span><span class="sxs-lookup"><span data-stu-id="cda91-156">If you want to ensure that all guests have to authenticate, choose **New and existing guests**.</span></span> <span data-ttu-id="cda91-157">Choisissez le paramètre le plus permissif qui sera nécessaire pour tous les sites de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="cda91-157">Choose the most permissive setting that will be needed by any site in your organization.</span></span>

![Capture d’écran des paramètres de partage SharePoint au niveau de l’organisation](../media/sharepoint-organization-external-sharing-controls.png)


<span data-ttu-id="cda91-159">Pour définir les paramètres de partage au niveau de l’organisation SharePoint</span><span class="sxs-lookup"><span data-stu-id="cda91-159">To set SharePoint organization level sharing settings</span></span>

1. <span data-ttu-id="cda91-160">Dans le centre d’administration 365 de Microsoft, dans le volet de navigation de gauche, sous **centres d’administration**, cliquez sur **SharePoint**.</span><span class="sxs-lookup"><span data-stu-id="cda91-160">In the Microsoft 365 admin center, in the left navigation, under **Admin centers**, click **SharePoint**.</span></span>
2. <span data-ttu-id="cda91-161">Dans le centre d’administration SharePoint, dans le volet de navigation de gauche, développez **stratégies** , puis cliquez sur **partage**.</span><span class="sxs-lookup"><span data-stu-id="cda91-161">In the SharePoint admin center, in the left navigation, expand **Policies** and then click **Sharing**.</span></span>
3. <span data-ttu-id="cda91-162">Assurez-vous que le partage externe pour SharePoint est défini sur **tout le monde** ou sur **des invités nouveaux et existants**.</span><span class="sxs-lookup"><span data-stu-id="cda91-162">Ensure that external sharing for SharePoint is set to **Anyone** or **New and existing guests**.</span></span>
4. <span data-ttu-id="cda91-163">Si vous avez effectué des modifications, cliquez sur **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="cda91-163">If you made changes, click **Save**.</span></span>


## <a name="sharepoint-organization-level-default-link-settings"></a><span data-ttu-id="cda91-164">Paramètres de lien par défaut au niveau de l’organisation SharePoint</span><span class="sxs-lookup"><span data-stu-id="cda91-164">SharePoint organization level default link settings</span></span>

<span data-ttu-id="cda91-165">Les paramètres de lien de fichier et de dossier par défaut déterminent l’option de lien qui est présentée par défaut à l’utilisateur lorsqu’il partage un fichier ou un dossier.</span><span class="sxs-lookup"><span data-stu-id="cda91-165">The default file and folder link settings determine which link option is shown to the user by default when they share a file or folder.</span></span> <span data-ttu-id="cda91-166">Les utilisateurs peuvent remplacer le type de lien par l’une des autres options avant de procéder au partage si vous le souhaitez.</span><span class="sxs-lookup"><span data-stu-id="cda91-166">Users can change the link type to one of the other options before sharing if desired.</span></span>

<span data-ttu-id="cda91-167">N’oubliez pas que ce paramètre affecte toutes les équipes et tous les sites SharePoint de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="cda91-167">Keep in mind that this setting affects all teams and SharePoint sites in your organization.</span></span>

<span data-ttu-id="cda91-168">Choisissez le type de lien sélectionné par défaut lorsque les utilisateurs partagent des fichiers et des dossiers :</span><span class="sxs-lookup"><span data-stu-id="cda91-168">Choose the type of link that's selected by default when users share files and folders:</span></span>

- <span data-ttu-id="cda91-169">**Toute personne disposant du lien** : choisissez cette option si vous envisagez d’effectuer beaucoup de partage non authentifié de fichiers et de dossiers.</span><span class="sxs-lookup"><span data-stu-id="cda91-169">**Anyone with the link** - Choose this option if you expect to do a lot of unauthenticated sharing of files and folders.</span></span> <span data-ttu-id="cda91-170">Si vous souhaitez autoriser *tout le monde* à se lier, mais que vous êtes préoccupé par le partage non authentifié accidentel, envisagez l’une des autres options par défaut.</span><span class="sxs-lookup"><span data-stu-id="cda91-170">If you want to allow *Anyone* links but are concerned about accidental unauthenticated sharing, consider one of the other options as the default.</span></span> <span data-ttu-id="cda91-171">Ce type de lien n’est disponible que si vous avez activé le partage d’un **utilisateur** .</span><span class="sxs-lookup"><span data-stu-id="cda91-171">This link type is only available if you've enabled **Anyone** sharing.</span></span>
- <span data-ttu-id="cda91-172">**Uniquement les personnes de votre organisation** : choisissez cette option si vous pensez que le partage de fichiers et de dossiers doit être associé à des personnes au sein de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="cda91-172">**Only people in your organization** - Choose this option if you expect most file and folder sharing to be with people inside your organization.</span></span>
- <span data-ttu-id="cda91-173">**Personnes spécifiques** : envisagez cette option si vous envisagez de faire beaucoup de partage de fichiers et de dossiers avec des invités.</span><span class="sxs-lookup"><span data-stu-id="cda91-173">**Specific people** - Consider this option if you expect to do a lot of file and folder sharing with guests.</span></span> <span data-ttu-id="cda91-174">Ce type de lien fonctionne avec les invités et les requiert pour s’authentifier.</span><span class="sxs-lookup"><span data-stu-id="cda91-174">This type of link works with guests and requires them to authenticate.</span></span>
 
![Capture d’écran des paramètres de partage de fichiers et dossiers au niveau de l’organisation dans SharePoint](../media/sharepoint-organization-files-folders-sharing-settings.png)


<span data-ttu-id="cda91-176">Pour définir les paramètres de liaison par défaut au niveau de l’organisation SharePoint</span><span class="sxs-lookup"><span data-stu-id="cda91-176">To set the SharePoint organization level default link settings</span></span>

1. <span data-ttu-id="cda91-177">Accédez à la page de partage dans le centre d’administration SharePoint.</span><span class="sxs-lookup"><span data-stu-id="cda91-177">Navigate to the Sharing page in the SharePoint admin center.</span></span>
2. <span data-ttu-id="cda91-178">Sous **liens de fichiers et de dossiers**, sélectionnez le lien de partage par défaut à utiliser.</span><span class="sxs-lookup"><span data-stu-id="cda91-178">Under **File and folder links**, select the default sharing link that you want to use.</span></span>
3. <span data-ttu-id="cda91-179">Si vous avez effectué des modifications, cliquez sur **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="cda91-179">If you made changes, click **Save**.</span></span>

## <a name="create-a-team"></a><span data-ttu-id="cda91-180">Créer une équipe</span><span class="sxs-lookup"><span data-stu-id="cda91-180">Create a team</span></span>

<span data-ttu-id="cda91-181">L’étape suivante consiste à créer l’équipe que vous envisagez d’utiliser pour collaborer avec des invités.</span><span class="sxs-lookup"><span data-stu-id="cda91-181">The next step is to create the team that you plan to use for collaborating with guests.</span></span>

<span data-ttu-id="cda91-182">Pour créer une équipe</span><span class="sxs-lookup"><span data-stu-id="cda91-182">To create a team</span></span>
1. <span data-ttu-id="cda91-183">Dans Teams, sous l’onglet **teams** , cliquez sur **rejoindre ou créer une équipe** en bas du volet de gauche.</span><span class="sxs-lookup"><span data-stu-id="cda91-183">In Teams, on the **Teams** tab, click **Join or create a team** at the bottom of the left pane.</span></span>
2. <span data-ttu-id="cda91-184">Cliquez sur **créer une équipe**.</span><span class="sxs-lookup"><span data-stu-id="cda91-184">Click **Create a team**.</span></span>
3. <span data-ttu-id="cda91-185">Cliquez sur **créer une équipe de toutes pièces**.</span><span class="sxs-lookup"><span data-stu-id="cda91-185">Click **Build a team from scratch**.</span></span>
4. <span data-ttu-id="cda91-186">Choisissez **privé** ou **public**.</span><span class="sxs-lookup"><span data-stu-id="cda91-186">Choose **Private** or **Public**.</span></span>
5. <span data-ttu-id="cda91-187">Tapez un nom et une description pour l’équipe, puis cliquez sur **créer**.</span><span class="sxs-lookup"><span data-stu-id="cda91-187">Type a name and description for the team, and then click **Create**.</span></span>
6. <span data-ttu-id="cda91-188">Cliquez sur **Ignorer**.</span><span class="sxs-lookup"><span data-stu-id="cda91-188">Click **Skip**.</span></span>

<span data-ttu-id="cda91-189">Nous allons inviter les utilisateurs ultérieurement.</span><span class="sxs-lookup"><span data-stu-id="cda91-189">We'll invite users later.</span></span> <span data-ttu-id="cda91-190">Ensuite, il est important de vérifier les paramètres de partage au niveau du site pour le site SharePoint qui est associé à l’équipe.</span><span class="sxs-lookup"><span data-stu-id="cda91-190">Next, it's important to check the site-level sharing settings for the SharePoint site that is associated with the team.</span></span>

## <a name="sharepoint-site-level-sharing-settings"></a><span data-ttu-id="cda91-191">Paramètres de partage au niveau du site SharePoint</span><span class="sxs-lookup"><span data-stu-id="cda91-191">SharePoint site level sharing settings</span></span>

<span data-ttu-id="cda91-192">Vérifiez les paramètres de partage au niveau du site pour vous assurer qu’ils autorisent le type d’accès que vous souhaitez pour cette équipe.</span><span class="sxs-lookup"><span data-stu-id="cda91-192">Check the site-level sharing settings to make sure that they allow the type of access that you want for this team.</span></span> <span data-ttu-id="cda91-193">Par exemple, si vous définissez les paramètres au niveau de l’organisation sur tous les **utilisateurs**, mais que vous souhaitez que tous les invités s’authentifient pour cette équipe, assurez-vous que les paramètres de partage au niveau du site sont définis sur **nouveaux et invités existants**.</span><span class="sxs-lookup"><span data-stu-id="cda91-193">For example, if you set the organization-level settings to **Anyone**, but you want all guests to authenticate for this team, then make sure the site-level sharing settings are set to **New and existing guests**.</span></span>

![Capture d’écran des paramètres de partage externe de site SharePoint](../media/sharepoint-site-external-sharing-settings.png)


<span data-ttu-id="cda91-195">Pour définir les paramètres de partage au niveau du site</span><span class="sxs-lookup"><span data-stu-id="cda91-195">To set site-level sharing settings</span></span>
1. <span data-ttu-id="cda91-196">Dans le centre d’administration SharePoint, dans le volet de navigation de gauche, développez **Sites** et cliquez sur **Sites actifs**.</span><span class="sxs-lookup"><span data-stu-id="cda91-196">In the SharePoint admin center, in the left navigation, expand **Sites** and click **Active sites**.</span></span>
2. <span data-ttu-id="cda91-197">Sélectionnez le site de l’équipe que vous venez de créer.</span><span class="sxs-lookup"><span data-stu-id="cda91-197">Select the site for the team that you just created.</span></span>
3. <span data-ttu-id="cda91-198">Dans le ruban, cliquez sur **Partage**. </span><span class="sxs-lookup"><span data-stu-id="cda91-198">In the ribbon, click **Sharing**.</span></span>
4. <span data-ttu-id="cda91-199">Assurez-vous que le partage est défini sur **tout le monde** ou sur **des invités nouveaux et existants**.</span><span class="sxs-lookup"><span data-stu-id="cda91-199">Ensure that sharing is set to **Anyone** or **New and existing guests**.</span></span>
5. <span data-ttu-id="cda91-200">Si vous avez effectué des modifications, cliquez sur **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="cda91-200">If you made changes, click **Save**.</span></span>

## <a name="invite-users"></a><span data-ttu-id="cda91-201">Inviter des utilisateurs</span><span class="sxs-lookup"><span data-stu-id="cda91-201">Invite users</span></span>

<span data-ttu-id="cda91-202">Les paramètres de partage des invités sont désormais configurés, de sorte que vous pouvez commencer à ajouter des utilisateurs et des invités internes à votre équipe.</span><span class="sxs-lookup"><span data-stu-id="cda91-202">Guest sharing settings are now configured, so you can start adding internal users and guests to your team.</span></span> 

<span data-ttu-id="cda91-203">Pour inviter des utilisateurs internes à une équipe</span><span class="sxs-lookup"><span data-stu-id="cda91-203">To invite internal users to a team</span></span>
1. <span data-ttu-id="cda91-204">Dans l’équipe, cliquez sur **plus d’options** ( **\*\*\*** ), puis sur **Ajouter un membre**.</span><span class="sxs-lookup"><span data-stu-id="cda91-204">In the team, click **More options** (**\*\*\***), and then click **Add member**.</span></span>
2. <span data-ttu-id="cda91-205">Tapez le nom de la personne que vous souhaitez inviter.</span><span class="sxs-lookup"><span data-stu-id="cda91-205">Type the name of the person who you want to invite.</span></span>
3. <span data-ttu-id="cda91-206">Cliquez sur **Ajouter**, puis sur **Fermer**.</span><span class="sxs-lookup"><span data-stu-id="cda91-206">Click **Add**, and then click **Close**.</span></span>

<span data-ttu-id="cda91-207">Pour inviter des invités à une équipe</span><span class="sxs-lookup"><span data-stu-id="cda91-207">To invite guests to a team</span></span>
1. <span data-ttu-id="cda91-208">Dans l’équipe, cliquez sur **plus d’options** ( **\*\*\*** ), puis sur **Ajouter un membre**.</span><span class="sxs-lookup"><span data-stu-id="cda91-208">In the team, click **More options** (**\*\*\***), and then click **Add member**.</span></span>
2. <span data-ttu-id="cda91-209">Tapez l’adresse de messagerie de l’invité que vous souhaitez inviter.</span><span class="sxs-lookup"><span data-stu-id="cda91-209">Type the email address of the guest who you want to invite.</span></span>
3. <span data-ttu-id="cda91-210">Cliquez sur **modifier les informations invité**.</span><span class="sxs-lookup"><span data-stu-id="cda91-210">Click **Edit guest information**.</span></span>
4. <span data-ttu-id="cda91-211">Tapez le nom complet de l’invité et cliquez sur la coche.</span><span class="sxs-lookup"><span data-stu-id="cda91-211">Type the guest's full name and click the check mark.</span></span>
5. <span data-ttu-id="cda91-212">Cliquez sur **Ajouter**, puis sur **Fermer**.</span><span class="sxs-lookup"><span data-stu-id="cda91-212">Click **Add**, and then click **Close**.</span></span>

## <a name="see-also"></a><span data-ttu-id="cda91-213">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="cda91-213">See Also</span></span>

[<span data-ttu-id="cda91-214">Meilleures pratiques relatives au partage de fichiers et de dossiers avec des utilisateurs non authentifiés</span><span class="sxs-lookup"><span data-stu-id="cda91-214">Best practices for sharing files and folders with unauthenticated users</span></span>](best-practices-anonymous-sharing.md)

[<span data-ttu-id="cda91-215">Limiter l’exposition accidentelle aux fichiers lors du partage avec des invités</span><span class="sxs-lookup"><span data-stu-id="cda91-215">Limit accidental exposure to files when sharing with guests</span></span>](share-limit-accidental-exposure.md)

[<span data-ttu-id="cda91-216">Créer un environnement de partage sécurisé avec des invités</span><span class="sxs-lookup"><span data-stu-id="cda91-216">Create a secure guest sharing environment</span></span>](create-secure-guest-sharing-environment.md)

[<span data-ttu-id="cda91-217">Créer un extranet B2B avec des invités gérés</span><span class="sxs-lookup"><span data-stu-id="cda91-217">Create a B2B extranet with managed guests</span></span>](b2b-extranet.md)

[<span data-ttu-id="cda91-218">Intégration de SharePoint et de OneDrive avec Azure AD B2B</span><span class="sxs-lookup"><span data-stu-id="cda91-218">SharePoint and OneDrive integration with Azure AD B2B</span></span>](https://docs.microsoft.com/sharepoint/sharepoint-azureb2b-integration-preview)