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
- m365initiative-externalcollab
ms.custom:
- seo-marvel-apr2020
localization_priority: Priority
f1.keywords: NOCSH
recommendations: false
description: Découvrez les étapes de configuration de Microsoft 365 nécessaires pour configurer une équipe pour la collaboration entre les tâches, les conversations et la documentation avec les invités dans Teams.
ms.openlocfilehash: c17732705c1d88ff70e56f5d26d9e268e3ff7c19
ms.sourcegitcommit: f780de91bc00caeb1598781e0076106c76234bad
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/19/2021
ms.locfileid: "52539262"
---
# <a name="collaborate-with-guests-in-a-team"></a><span data-ttu-id="677b6-103">Collaborer avec des invités au sein d’une équipe</span><span class="sxs-lookup"><span data-stu-id="677b6-103">Collaborate with guests in a team</span></span>

<span data-ttu-id="677b6-104">Si vous devez collaborer avec des invités au sein de documents, de tâches et de conversations, nous vous recommandons d’utiliser Microsoft Teams.</span><span class="sxs-lookup"><span data-stu-id="677b6-104">If you need to collaborate with guests across documents, tasks, and conversations, we recommend using Microsoft Teams.</span></span> <span data-ttu-id="677b6-105">Teams fournit toutes les fonctionnalités de collaboration disponibles dans Office et SharePoint avec une conversation permanente et un ensemble personnalisable et extensible d’outils de collaboration dans une expérience utilisateur unifiée.</span><span class="sxs-lookup"><span data-stu-id="677b6-105">Teams provides all of the collaboration features available in Office and SharePoint with persistent chat and a customizable and extensible set of collaboration tools in a unified user experience.</span></span>

<span data-ttu-id="677b6-106">Dans cet article, nous allons suivre les étapes de configuration de Microsoft 365 nécessaires pour configurer une équipe en collaboration avec des invités.</span><span class="sxs-lookup"><span data-stu-id="677b6-106">In this article, we'll walk through the Microsoft 365 configuration steps necessary to set up a team for collaboration with guests.</span></span> <span data-ttu-id="677b6-107">Une fois que vous avez configuré l'accès invité, vous pouvez inviter des personnes à des équipes en suivant les étapes de la section [Ajouter des invités à une équipe dans Teams](https://support.microsoft.com/office/fccb4fa6-f864-4508-bdde-256e7384a14f).</span><span class="sxs-lookup"><span data-stu-id="677b6-107">Once you have configured guest access, you can invite guests to teams by following the steps in [Add guests to a team in Teams](https://support.microsoft.com/office/fccb4fa6-f864-4508-bdde-256e7384a14f).</span></span>

## <a name="video-demonstration"></a><span data-ttu-id="677b6-108">Démonstration vidéo</span><span class="sxs-lookup"><span data-stu-id="677b6-108">Video demonstration</span></span>

<span data-ttu-id="677b6-109">Cette vidéo décrit les étapes de configuration décrites dans ce document.</span><span class="sxs-lookup"><span data-stu-id="677b6-109">This video shows the configuration steps described in this document.</span></span></br>

> [!VIDEO https://www.microsoft.com/videoplayer/embed/RE44NTr?autoplay=false]

## <a name="azure-external-collaboration-settings"></a><span data-ttu-id="677b6-110">Paramètres de collaboration externe Azure</span><span class="sxs-lookup"><span data-stu-id="677b6-110">Azure External collaboration settings</span></span>

<span data-ttu-id="677b6-111">Le partage dans Microsoft 365 est régi à son niveau le plus élevé par les [paramètres de collaboration externe B2B dans Azure Active Directory](/azure/active-directory/external-identities/delegate-invitations).</span><span class="sxs-lookup"><span data-stu-id="677b6-111">Sharing in Microsoft 365 is governed at its highest level by the [B2B external collaboration settings in Azure Active Directory](/azure/active-directory/external-identities/delegate-invitations).</span></span> <span data-ttu-id="677b6-112">Si le partage invité est désactivé ou restreint dans Azure AD, ce paramètre remplace les paramètres de partage que vous configurez dans Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="677b6-112">If guest sharing is disabled or restricted in Azure AD, this setting overrides any sharing settings that you configure in Microsoft 365.</span></span>

<span data-ttu-id="677b6-113">Vérifiez les paramètres de collaboration externe B2B pour vous assurer que le partage avec les invités n’est pas bloqué.</span><span class="sxs-lookup"><span data-stu-id="677b6-113">Check the B2B external collaboration settings settings to ensure that sharing with guests is not blocked.</span></span>

![Capture d’écran de la page des paramètres de relations organisationnelles d’Azure Active Directory](../media/azure-ad-organizational-relationships-settings.png)

<span data-ttu-id="677b6-115">Pour définir les paramètres de collaboration externe</span><span class="sxs-lookup"><span data-stu-id="677b6-115">To set external collaboration settings</span></span>

1. <span data-ttu-id="677b6-116">Connectez-vous à Azure Active Directory sur [https://aad.portal.azure.com](https://aad.portal.azure.com).</span><span class="sxs-lookup"><span data-stu-id="677b6-116">Log in to Azure Active Directory at [https://aad.portal.azure.com](https://aad.portal.azure.com).</span></span>
2. <span data-ttu-id="677b6-117">Dans le volet de navigation gauche, cliquez sur **Azure Active Directory**.</span><span class="sxs-lookup"><span data-stu-id="677b6-117">In the left navigation pane, click **Azure Active Directory**.</span></span>
3. <span data-ttu-id="677b6-118">Cliquez sur **Identités externes**.</span><span class="sxs-lookup"><span data-stu-id="677b6-118">Click **External identities**.</span></span>
4. <span data-ttu-id="677b6-119">Dans l’écran **Prise en main**, dans le volet de navigation gauche, cliquez sur **Paramètres de collaboration externe**.</span><span class="sxs-lookup"><span data-stu-id="677b6-119">On the **Get started** screen, in the left navigation pane, click **External collaboration settings**.</span></span>
5. <span data-ttu-id="677b6-120">Assurez-vous que **Les administrateurs et les utilisateurs membres du rôle Inviteur d’invités peuvent envoyer des invitations** et **Les membres peuvent inviter** sont tous deux définis sur **Oui**.</span><span class="sxs-lookup"><span data-stu-id="677b6-120">Ensure that **Admins and users in the guest inviter role can invite** and **Members can invite** are both set to **Yes**.</span></span>
6. <span data-ttu-id="677b6-121">Si vous avez effectué des modifications, cliquez sur **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="677b6-121">If you made changes, click **Save**.</span></span>

<span data-ttu-id="677b6-122">Notez les paramètres dans la section **Restrictions de collaboration**.</span><span class="sxs-lookup"><span data-stu-id="677b6-122">Note the settings in the **Collaboration restrictions** section.</span></span> <span data-ttu-id="677b6-123">Assurez-vous que les domaines des invités avec qui vous voulez collaborer ne sont pas bloqués.</span><span class="sxs-lookup"><span data-stu-id="677b6-123">Make sure that the domains of the guests that you want to collaborate with aren't blocked.</span></span>

<span data-ttu-id="677b6-124">Si vous travaillez avec des invités de plusieurs organisations, vous souhaiterez peut-être restreindre leur capacité à accéder aux données d’annuaire.</span><span class="sxs-lookup"><span data-stu-id="677b6-124">If you work with guests from multiple organizations, you may want to restrict their ability to access directory data.</span></span> <span data-ttu-id="677b6-125">Cela les empêche de voir qui d’autre est invité dans l’annuaire.</span><span class="sxs-lookup"><span data-stu-id="677b6-125">This will prevent them from seeing who else is a guest in the directory.</span></span> <span data-ttu-id="677b6-126">Pour ce faire, sous **Restrictions d’accès des utilisateurs invités**, sélectionnez **Les utilisateurs invités ont un accès limité aux propriétés et à l’appartenance aux paramètres des objets d’annuaire** ou **L’accès des utilisateurs invités est limité aux propriétés et à l’appartenance à leurs propres objets d’annuaire**.</span><span class="sxs-lookup"><span data-stu-id="677b6-126">To do this, under **Guest user access restrictions**, select **Guest users have limited access to properties and membership of directory objects settings** or **Guest user access is restricted to properties and memberships of their own directory objects**.</span></span>

## <a name="teams-guest-access-settings"></a><span data-ttu-id="677b6-127">Paramètres d’accès invité Teams, procédez comme suit :</span><span class="sxs-lookup"><span data-stu-id="677b6-127">Teams guest access settings</span></span>

<span data-ttu-id="677b6-128">Teams dispose d’un commutateur maître d’accès par invité et de divers paramètres disponibles pour contrôler ce que les invités peuvent faire dans une équipe.</span><span class="sxs-lookup"><span data-stu-id="677b6-128">Teams has a master on/off switch for guest access and a variety of settings available to control what guests can do in a team.</span></span> <span data-ttu-id="677b6-129">Le commutateur maître, **Autoriser l’accès invité dans Teams** doit être **Activé** pour que l’accès invité fonctionne dans Teams.</span><span class="sxs-lookup"><span data-stu-id="677b6-129">The master switch, **Allow guest access in Teams** must be **On** for guest access to work in Teams.</span></span>

<span data-ttu-id="677b6-p107">Vérifiez que l’accès invité est activé dans Teams et ajustez les paramètres invités en fonction des besoins de votre entreprise. N’oubliez pas que ces paramètres affectent toutes les équipes.</span><span class="sxs-lookup"><span data-stu-id="677b6-p107">Check to ensure that guest access is enabled in Teams and make any adjustment to the guest settings based on your business needs. Keep in mind that these settings affect all teams.</span></span>

![Capture d’écran du commutateur Accès invité dans Teams](../media/teams-guest-access-toggle-on.png)

<span data-ttu-id="677b6-133">Pour déterminer les paramètres d’accès invité Teams, procédez comme suit :</span><span class="sxs-lookup"><span data-stu-id="677b6-133">To set Teams guest access settings</span></span>

1. <span data-ttu-id="677b6-134">Connectez-vous au Centre d’administration Microsoft 365 sur[https://admin.microsoft.com](https://admin.microsoft.com).</span><span class="sxs-lookup"><span data-stu-id="677b6-134">Log in to the Microsoft 365 admin center at [https://admin.microsoft.com](https://admin.microsoft.com).</span></span>
2. <span data-ttu-id="677b6-135">Dans la barre de navigation de gauche, cliquez sur **Afficher tout**.</span><span class="sxs-lookup"><span data-stu-id="677b6-135">In the left navigation pane, click **Show all**.</span></span>
3. <span data-ttu-id="677b6-136">Sous **Centres d’administration**, cliquez sur **Teams**.</span><span class="sxs-lookup"><span data-stu-id="677b6-136">Under **Admin centers**, click **Teams**.</span></span>
4. <span data-ttu-id="677b6-137">Dans le Centre d’administration Teams, dans le volet de navigation gauche, développez **Paramètres à l’échelle de l’organisation**, puis cliquez sur **Accès invité**.</span><span class="sxs-lookup"><span data-stu-id="677b6-137">In the Teams admin center, in the left navigation pane, expand **Org-wide settings** and click **Guest access**.</span></span>
5. <span data-ttu-id="677b6-138">Assurez-vous que **Autoriser l’accès invité dans Teams** est défini sur **Activé**.</span><span class="sxs-lookup"><span data-stu-id="677b6-138">Ensure that **Allow guest access in Teams** is set to **On**.</span></span>
6. <span data-ttu-id="677b6-139">Apportez les modifications souhaitées aux autres paramètres invités, puis cliquez sur **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="677b6-139">Make any desired changes to the additional guest settings, and then click **Save**.</span></span>

<span data-ttu-id="677b6-140">Une fois l’accès invité Teams désactivé, vous pouvez éventuellement contrôler l’accès invité aux équipes individuelles et à leurs sites SharePoint associés à l’aide d’étiquettes de critère de critère de sécurité.</span><span class="sxs-lookup"><span data-stu-id="677b6-140">Once Teams guest access is turned on, you can optionally control guest access to individual teams and their associated SharePoint sites using sensitivity labels.</span></span> <span data-ttu-id="677b6-141">Pour plus d’informations, voir [Utiliser les étiquettes de confidentialité pour protéger le contenu dans Microsoft Teams, les groupes Office 365 et les sites SharePoint](../compliance/sensitivity-labels-teams-groups-sites.md).</span><span class="sxs-lookup"><span data-stu-id="677b6-141">For more information, see [Use sensitivity labels to protect content in Microsoft Teams, Microsoft 365 groups, and SharePoint sites](../compliance/sensitivity-labels-teams-groups-sites.md).</span></span>

> [!NOTE]
> <span data-ttu-id="677b6-142">La mise en service des paramètres invité Teams peut prendre jusqu'à vingt-quatre heures.</span><span class="sxs-lookup"><span data-stu-id="677b6-142">It may take up to twenty-four hours for the Teams guest settings to become active after you turn it on.</span></span>

## <a name="microsoft-365-groups-guest-settings"></a><span data-ttu-id="677b6-143">Paramètres invités des groupes Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="677b6-143">Microsoft 365 Groups guest settings</span></span>

<span data-ttu-id="677b6-p109">Teams utilise les groupes Microsoft 365 pour l’appartenance aux équipes. Les paramètres invités des groupes Microsoft 365 doivent être désactivés pour que l’accès invité dans Teams fonctionne.</span><span class="sxs-lookup"><span data-stu-id="677b6-p109">Teams uses Microsoft 365 Groups for team membership. The Microsoft 365 Groups guest settings must be turned on in order for guest access in Teams to work.</span></span>

![Capture d’écran des paramètres d’invité des Groupes Microsoft 365 dans le Centre d’administration Microsoft 365](../media/office-365-groups-guest-settings.png)

<span data-ttu-id="677b6-147">Pour définir les paramètres invités des groupes Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="677b6-147">To set Microsoft 365 Groups guest settings</span></span>

1. <span data-ttu-id="677b6-148">Dans le Centre d’administration Microsoft 365, dans le volet de navigation gauche, développez **Paramètres**.</span><span class="sxs-lookup"><span data-stu-id="677b6-148">In the Microsoft 365 admin center, in the left navigation pane, expand **Settings**.</span></span>
2. <span data-ttu-id="677b6-149">Cliquez sur **Paramètres de l’organisation**.</span><span class="sxs-lookup"><span data-stu-id="677b6-149">Click **Org settings**.</span></span>
3. <span data-ttu-id="677b6-150">Dans la liste, cliquez sur **Groupes Microsoft 365**.</span><span class="sxs-lookup"><span data-stu-id="677b6-150">In the list, click **Microsoft 365 Groups**.</span></span>
4. <span data-ttu-id="677b6-151">Assurez-vous que les cases à cocher **Permettre aux propriétaires de groupe d’ajouter des personnes externes à votre organisation à des groupes Microsoft 365 en tant qu'invités** et **Permettre aux membres du groupe invités d’accéder au contenu du groupe** sont cochées.</span><span class="sxs-lookup"><span data-stu-id="677b6-151">Ensure that the **Let group owners add people outside your organization to Microsoft 365 Groups as guests** and **Let guest group members access group content** check boxes are both checked.</span></span>
5. <span data-ttu-id="677b6-152">Si vous avez effectué des modifications, cliquez sur **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="677b6-152">If you made changes, click **Save changes**.</span></span>


## <a name="sharepoint-organization-level-sharing-settings"></a><span data-ttu-id="677b6-153">Paramètres de partage SharePoint au niveau de l’organisation</span><span class="sxs-lookup"><span data-stu-id="677b6-153">SharePoint organization level sharing settings</span></span>

<span data-ttu-id="677b6-154">Le contenu Teams, tel que les fichiers, dossiers et listes, est stocké dans SharePoint.</span><span class="sxs-lookup"><span data-stu-id="677b6-154">Teams content such as files, folders, and lists are all stored in SharePoint.</span></span> <span data-ttu-id="677b6-155">Pour que les invités aient accès à ces éléments dans Teams, les paramètres de partage au niveau de l'organisation SharePoint doivent permettre le partage avec les invités.</span><span class="sxs-lookup"><span data-stu-id="677b6-155">In order for guests to have access to these items in Teams, the SharePoint organization-level sharing settings must allow for sharing with guests.</span></span>

<span data-ttu-id="677b6-156">Les paramètres au niveau de l’organisation déterminent les paramètres disponibles pour les sites individuels, y compris les sites associés à des équipes.</span><span class="sxs-lookup"><span data-stu-id="677b6-156">The organization-level settings determine what settings are available for individual sites, including sites associated with teams.</span></span> <span data-ttu-id="677b6-157">Les paramètres de site ne peuvent pas être plus permissifs que les paramètres au niveau de l’organisation.</span><span class="sxs-lookup"><span data-stu-id="677b6-157">Site settings cannot be more permissive than the organization-level settings.</span></span>

<span data-ttu-id="677b6-158">Si vous voulez autoriser le partage de fichiers et de dossiers avec des personnes non authentifiés, sélectionnez **Tout le monde**.</span><span class="sxs-lookup"><span data-stu-id="677b6-158">If you want to allow file and folder sharing with unauthenticated people, choose **Anyone**.</span></span> <span data-ttu-id="677b6-159">Pour vous assurer que tous les invités doivent s’authentifier, Choisissez **Invités nouveaux et existants**.</span><span class="sxs-lookup"><span data-stu-id="677b6-159">If you want to ensure that all guests have to authenticate, choose **New and existing guests**.</span></span> <span data-ttu-id="677b6-160">Choisissez le paramètre le plus permissif qui sera nécessaire pour n’importe quel site de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="677b6-160">Choose the most permissive setting that will be needed by any site in your organization.</span></span>

![Capture d’écran des paramètres de partage SharePoint au niveau de l’organisation](../media/sharepoint-organization-external-sharing-controls.png)


<span data-ttu-id="677b6-162">Pour définir les paramètres de partage SharePoint au niveau de l’organisation</span><span class="sxs-lookup"><span data-stu-id="677b6-162">To set SharePoint organization-level sharing settings</span></span>

1. <span data-ttu-id="677b6-163">Dans le Centre d’administration Microsoft 365, dans le volet de navigation gauche, sous **Centres d’administration**, cliquez sur **SharePoint**.</span><span class="sxs-lookup"><span data-stu-id="677b6-163">In the Microsoft 365 admin center, in the left navigation pane, under **Admin centers**, click **SharePoint**.</span></span>
2. <span data-ttu-id="677b6-164">Dans le Centre d’administration SharePoint, dans le volet de navigation gauche, développez **Stratégies** puis cliquez sur **Partage**.</span><span class="sxs-lookup"><span data-stu-id="677b6-164">In the SharePoint admin center, in the left navigation pane, expand **Policies** and then click **Sharing**.</span></span>
3. <span data-ttu-id="677b6-165">Assurez-vous que le partage externe pour SharePoint est **Tout le monde** ou **Invités nouveaux et existants**.</span><span class="sxs-lookup"><span data-stu-id="677b6-165">Ensure that external sharing for SharePoint is set to **Anyone** or **New and existing guests**.</span></span>
4. <span data-ttu-id="677b6-166">Si vous avez effectué des modifications, cliquez sur **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="677b6-166">If you made changes, click **Save**.</span></span>


## <a name="sharepoint-organization-level-default-link-settings"></a><span data-ttu-id="677b6-167">Paramètres de liaison par défaut au niveau de l’organisation SharePoint</span><span class="sxs-lookup"><span data-stu-id="677b6-167">SharePoint organization-level default link settings</span></span>

<span data-ttu-id="677b6-168">Les paramètres par défaut de liaison de fichier et de dossier déterminent l’option de lien qui sera affichée par défaut aux utilisateurs lorsqu’ils partagent un fichier ou un dossier.</span><span class="sxs-lookup"><span data-stu-id="677b6-168">The default file and folder link settings determine the link option that will be shown to users by default when they share a file or folder.</span></span> <span data-ttu-id="677b6-169">Si vous le souhaitez, les utilisateurs peuvent modifier le type de lien vers l’une des autres options avant le partage.</span><span class="sxs-lookup"><span data-stu-id="677b6-169">Users can change the link type to one of the other options before sharing, if desired.</span></span>

<span data-ttu-id="677b6-170">N’oubliez pas que ce paramètre affecte toutes les équipes et les sites SharePoint dans votre organisation.</span><span class="sxs-lookup"><span data-stu-id="677b6-170">Keep in mind that this setting affects all teams and SharePoint sites in your organization.</span></span>

<span data-ttu-id="677b6-171">Choisissez l’un des types de liens suivants qui seront sélectionnés par défaut lorsque les utilisateurs partagent des fichiers et des dossiers :</span><span class="sxs-lookup"><span data-stu-id="677b6-171">Choose any one of the following link-types which will be selected by default when users share files and folders:</span></span>

- <span data-ttu-id="677b6-172">**Toute personne disposant du lien** : choisissez cette option si vous vous attendez à beaucoup de partage non authentifié de fichiers et de dossiers.</span><span class="sxs-lookup"><span data-stu-id="677b6-172">**Anyone with the link** - Choose this option if you expect to do a lot of unauthenticated sharing of files and folders.</span></span> <span data-ttu-id="677b6-173">Si vous souhaitez autoriser les liens à *Tout le monde* mais que vous craignez un partage accidentel non authentifié, envisagez l'une des autres options comme valeur par défaut.</span><span class="sxs-lookup"><span data-stu-id="677b6-173">If you want to allow *Anyone* links but are concerned about accidental unauthenticated sharing, consider one of the other options as the default.</span></span> <span data-ttu-id="677b6-174">Ce type de lien n’est disponible que si vous avez activé le partage **Tout le monde**.</span><span class="sxs-lookup"><span data-stu-id="677b6-174">This link type is only available if you've enabled **Anyone** sharing.</span></span>
- <span data-ttu-id="677b6-175">**Uniquement les personnes de votre organisation** : choisissez cette option si vous souhaitez que la plupart des partages de fichiers et de dossiers soient avec des personnes de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="677b6-175">**Only people in your organization** - Choose this option if you expect most file and folder sharing to be with people inside your organization.</span></span>
- <span data-ttu-id="677b6-176">**Personnes spécifiques** : envisagez cette option si vous prévoyez de partager beaucoup de fichiers et de dossiers avec vos invités.</span><span class="sxs-lookup"><span data-stu-id="677b6-176">**Specific people** - Consider this option if you expect to do a lot of file and folder sharing with guests.</span></span> <span data-ttu-id="677b6-177">Ce type de lien fonctionne avec les invités et exige leur authentification.</span><span class="sxs-lookup"><span data-stu-id="677b6-177">This type of link works with guests and requires them to authenticate.</span></span>
 
![Capture d’écran des paramètres de partage de fichiers et dossiers au niveau de l’organisation dans SharePoint](../media/sharepoint-organization-files-folders-sharing-settings.png)


<span data-ttu-id="677b6-179">Pour définir les paramètres de liaison par défaut au niveau de l’organisation SharePoint</span><span class="sxs-lookup"><span data-stu-id="677b6-179">To set the SharePoint organization-level default link settings</span></span>

1. <span data-ttu-id="677b6-180">Accédez à la page Partage dans le Centre d’administration SharePoint.</span><span class="sxs-lookup"><span data-stu-id="677b6-180">Navigate to the Sharing page in the SharePoint admin center.</span></span>
2. <span data-ttu-id="677b6-181">Sous **Liens des fichiers et des dossiers**, sélectionnez le lien de partage par défaut que vous voulez utiliser.</span><span class="sxs-lookup"><span data-stu-id="677b6-181">Under **File and folder links**, select the default sharing link that you want to use.</span></span>
3. <span data-ttu-id="677b6-182">Si vous avez effectué des modifications, cliquez sur **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="677b6-182">If you made changes, click **Save**.</span></span>

## <a name="create-a-team"></a><span data-ttu-id="677b6-183">Créer une équipe</span><span class="sxs-lookup"><span data-stu-id="677b6-183">Create a team</span></span>

<span data-ttu-id="677b6-184">L'étape suivante consiste à créer l'équipe que vous comptez utiliser pour collaborer avec les invités.</span><span class="sxs-lookup"><span data-stu-id="677b6-184">The next step is to create the team that you plan to use for collaborating with guests.</span></span>

<span data-ttu-id="677b6-185">Pour créer une équipe</span><span class="sxs-lookup"><span data-stu-id="677b6-185">To create a team</span></span>
1. <span data-ttu-id="677b6-186">Dans Teams, dans l’onglet **Teams** , cliquez sur **Rejoindre ou créer une équipe** en bas du volet gauche.</span><span class="sxs-lookup"><span data-stu-id="677b6-186">In Teams, on the **Teams** tab, click **Join or create a team** at the bottom of the left pane.</span></span>
2. <span data-ttu-id="677b6-187">Cliquez sur **Créer une équipe**.</span><span class="sxs-lookup"><span data-stu-id="677b6-187">Click **Create a team**.</span></span>
3. <span data-ttu-id="677b6-188">Cliquez sur **Créer une équipe à partir de zéro**.</span><span class="sxs-lookup"><span data-stu-id="677b6-188">Click **Build a team from scratch**.</span></span>
4. <span data-ttu-id="677b6-189">Sélectionnez **Privé** ou **Public**.</span><span class="sxs-lookup"><span data-stu-id="677b6-189">Choose **Private** or **Public**.</span></span>
5. <span data-ttu-id="677b6-190">Entrez le nom et une description du groupe, puis cliquez sur **Créer**.</span><span class="sxs-lookup"><span data-stu-id="677b6-190">Type a name and description for the team, and then click **Create**.</span></span>
6. <span data-ttu-id="677b6-191">Cliquez sur **Ignorer**.</span><span class="sxs-lookup"><span data-stu-id="677b6-191">Click **Skip**.</span></span>

<span data-ttu-id="677b6-p116">Nous inviterons des utilisateurs plus tard. Ensuite, il est important de vérifier les paramètres de partage au niveau du site pour le site SharePoint associé à l’équipe.</span><span class="sxs-lookup"><span data-stu-id="677b6-p116">We'll invite users later. Next, it's important to check the site-level sharing settings for the SharePoint site that is associated with the team.</span></span>

## <a name="sharepoint-site-level-sharing-settings"></a><span data-ttu-id="677b6-194">Paramètres de SharePoint au niveau du site</span><span class="sxs-lookup"><span data-stu-id="677b6-194">SharePoint site-level sharing settings</span></span>

<span data-ttu-id="677b6-195">Vérifiez les paramètres de partage au niveau du site pour vous assurer qu’ils autorisent le type d’accès voulu pour cette équipe.</span><span class="sxs-lookup"><span data-stu-id="677b6-195">Check the site-level sharing settings to make sure that they allow the type of access that you want for this team.</span></span> <span data-ttu-id="677b6-196">Par exemple, si vous définissez les paramètres au niveau de l’organisation sur **Tout le monde**, mais que vous souhaitez que tous les invités s’authentifier au niveau de cette équipe, assurez-vous que les paramètres de partage au niveau du site sont **Invités nouveaux et existants**.</span><span class="sxs-lookup"><span data-stu-id="677b6-196">For example, if you set the organization-level settings to **Anyone**, but you want all guests to authenticate for this team, then make sure the site-level sharing settings are set to **New and existing guests**.</span></span>

![Capture d’écran des paramètres de partage externe de site SharePoint](../media/sharepoint-site-external-sharing-settings.png)

<span data-ttu-id="677b6-198">Pour définir les paramètres au niveau du site</span><span class="sxs-lookup"><span data-stu-id="677b6-198">To set site-level sharing settings</span></span>
1. <span data-ttu-id="677b6-199">Dans le centre d’administration SharePoint, dans le volet de navigation de gauche, développez **Sites** et cliquez sur **Sites actifs**.</span><span class="sxs-lookup"><span data-stu-id="677b6-199">In the SharePoint admin center, in the left navigation pane, expand **Sites** and click **Active sites**.</span></span>
2. <span data-ttu-id="677b6-200">Sélectionnez le site de l’équipe que vous venez de créer.</span><span class="sxs-lookup"><span data-stu-id="677b6-200">Select the site for the team that you just created.</span></span>
3. <span data-ttu-id="677b6-201">Cliquez sur... puis sélectionnez **Partage**.</span><span class="sxs-lookup"><span data-stu-id="677b6-201">Click ... and choose **Sharing**.</span></span>
4. <span data-ttu-id="677b6-202">Assurez-vous que le partage est paramétré sur **Tout le monde** ou **Invités nouveaux et existants**.</span><span class="sxs-lookup"><span data-stu-id="677b6-202">Ensure that sharing is set to **Anyone** or **New and existing guests**.</span></span>
5. <span data-ttu-id="677b6-203">Si vous avez effectué des modifications, cliquez sur **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="677b6-203">If you made changes, click **Save**.</span></span>

## <a name="invite-users"></a><span data-ttu-id="677b6-204">Inviter des utilisateurs</span><span class="sxs-lookup"><span data-stu-id="677b6-204">Invite users</span></span>

<span data-ttu-id="677b6-205">Les paramètres de partage invité sont désormais configurés. Vous pouvez ainsi commencer à ajouter des utilisateurs internes et des invités à votre équipe.</span><span class="sxs-lookup"><span data-stu-id="677b6-205">Guest sharing settings are now configured, so you can start adding internal users and guests to your team.</span></span> 

<span data-ttu-id="677b6-206">Pour inviter des utilisateurs internes à une équipe</span><span class="sxs-lookup"><span data-stu-id="677b6-206">To invite internal users to a team</span></span>
1. <span data-ttu-id="677b6-207">Dans l’équipe, cliquez sur **Plus d'options** (**\*\*\***), puis sur **Ajouter un membre**.</span><span class="sxs-lookup"><span data-stu-id="677b6-207">In the team, click **More options** (**\*\*\***), and then click **Add member**.</span></span>
2. <span data-ttu-id="677b6-208">Tapez le nom de la personne que vous voulez inviter.</span><span class="sxs-lookup"><span data-stu-id="677b6-208">Type the name of the person who you want to invite.</span></span>
3. <span data-ttu-id="677b6-209">Cliquez sur **Ajouter**, puis sur **Fermer**.</span><span class="sxs-lookup"><span data-stu-id="677b6-209">Click **Add**, and then click **Close**.</span></span>

<span data-ttu-id="677b6-210">Pour inviter à une équipe</span><span class="sxs-lookup"><span data-stu-id="677b6-210">To invite guests to a team</span></span>
1. <span data-ttu-id="677b6-211">Dans l’équipe, cliquez sur **Plus d'options** (**\*\*\***), puis sur **Ajouter un membre**.</span><span class="sxs-lookup"><span data-stu-id="677b6-211">In the team, click **More options** (**\*\*\***), and then click **Add member**.</span></span>
2. <span data-ttu-id="677b6-212">Tapez l’adresse de courrier de la personne que vous voulez inviter.</span><span class="sxs-lookup"><span data-stu-id="677b6-212">Type the email address of the guest whom you want to invite.</span></span>
3. <span data-ttu-id="677b6-213">Cliquez sur **Modifier les informations d’un utilisateur invité**.</span><span class="sxs-lookup"><span data-stu-id="677b6-213">Click **Edit guest information**.</span></span>
4. <span data-ttu-id="677b6-214">Tapez le nom complet de l’invité, puis cliquez sur la coche.</span><span class="sxs-lookup"><span data-stu-id="677b6-214">Type the guest's full name and click the check mark.</span></span>
5. <span data-ttu-id="677b6-215">Cliquez sur **Ajouter**, puis sur **Fermer**.</span><span class="sxs-lookup"><span data-stu-id="677b6-215">Click **Add**, and then click **Close**.</span></span>

## <a name="see-also"></a><span data-ttu-id="677b6-216">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="677b6-216">See also</span></span>

[<span data-ttu-id="677b6-217">Meilleures pratiques relatives au partage de fichiers et de dossiers avec des utilisateurs non authentifiés</span><span class="sxs-lookup"><span data-stu-id="677b6-217">Best practices for sharing files and folders with unauthenticated users</span></span>](best-practices-anonymous-sharing.md)

[<span data-ttu-id="677b6-218">Limiter l’exposition accidentelle aux fichiers lors du partage avec des invités</span><span class="sxs-lookup"><span data-stu-id="677b6-218">Limit accidental exposure to files when sharing with guests</span></span>](share-limit-accidental-exposure.md)

[<span data-ttu-id="677b6-219">Créer un environnement de partage sécurisé avec des invités</span><span class="sxs-lookup"><span data-stu-id="677b6-219">Create a secure guest sharing environment</span></span>](create-secure-guest-sharing-environment.md)

[<span data-ttu-id="677b6-220">Créer un extranet B2B avec des invités gérés</span><span class="sxs-lookup"><span data-stu-id="677b6-220">Create a B2B extranet with managed guests</span></span>](b2b-extranet.md)

[<span data-ttu-id="677b6-221">Intégration de SharePoint et de OneDrive à Azure AD B2B</span><span class="sxs-lookup"><span data-stu-id="677b6-221">SharePoint and OneDrive integration with Azure AD B2B</span></span>](/sharepoint/sharepoint-azureb2b-integration-preview)

[<span data-ttu-id="677b6-222">Les options de partage sont grisées lors du partage à partir de SharePoint ou OneDrive</span><span class="sxs-lookup"><span data-stu-id="677b6-222">Sharing options are greyed out when sharing from SharePoint or OneDrive</span></span>](/sharepoint/troubleshoot/administration/sharing-options-grayed-out-when-sharing-from-sharepoint-online-or-onedrive)