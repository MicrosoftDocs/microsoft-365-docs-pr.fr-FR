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
localization_priority: Normal
f1.keywords: NOCSH
description: Découvrez les étapes de configuration de Microsoft 365 nécessaires pour configurer une équipe pour la collaboration de tâches, de conversations et de documentation avec des invités dans Teams.
ms.openlocfilehash: 66c5692dd8cd233d8b3639f8ce0755ce51b60c0a
ms.sourcegitcommit: a62ac3c01ba700a51b78a647e2301f27ac437c5a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/12/2021
ms.locfileid: "50233073"
---
# <a name="collaborate-with-guests-in-a-team"></a><span data-ttu-id="3e1f4-103">Collaborer avec des invités au sein d’une équipe</span><span class="sxs-lookup"><span data-stu-id="3e1f4-103">Collaborate with guests in a team</span></span>

<span data-ttu-id="3e1f4-104">Si vous avez besoin de collaborer avec des invités dans des documents, des tâches et des conversations, nous vous recommandons d’utiliser Microsoft Teams.</span><span class="sxs-lookup"><span data-stu-id="3e1f4-104">If you need to collaborate with guests across documents, tasks, and conversations, we recommend using Microsoft Teams.</span></span> <span data-ttu-id="3e1f4-105">Teams fournit toutes les fonctionnalités de collaboration disponibles dans Office et SharePoint avec une conversation permanente et un ensemble personnalisable et extensible d’outils de collaboration dans une expérience utilisateur unifiée.</span><span class="sxs-lookup"><span data-stu-id="3e1f4-105">Teams provides all of the collaboration features available in Office and SharePoint with persistent chat and a customizable and extensible set of collaboration tools in a unified user experience.</span></span>

<span data-ttu-id="3e1f4-106">Dans cet article, nous allons passer en revue les étapes de configuration de Microsoft 365 nécessaires pour configurer une équipe pour la collaboration avec les invités.</span><span class="sxs-lookup"><span data-stu-id="3e1f4-106">In this article, we'll walk through the Microsoft 365 configuration steps necessary to set up a team for collaboration with guests.</span></span> <span data-ttu-id="3e1f4-107">Une fois que vous avez configuré l’accès invité, vous pouvez inviter des invités à des équipes en suivant les étapes de l’étape Ajouter des invités à une [équipe dans Teams.](https://support.microsoft.com/office/fccb4fa6-f864-4508-bdde-256e7384a14f)</span><span class="sxs-lookup"><span data-stu-id="3e1f4-107">Once you have configured guest access, you can invite guests to teams by following the steps in [Add guests to a team in Teams](https://support.microsoft.com/office/fccb4fa6-f864-4508-bdde-256e7384a14f).</span></span>

## <a name="video-demonstration"></a><span data-ttu-id="3e1f4-108">Démonstration vidéo</span><span class="sxs-lookup"><span data-stu-id="3e1f4-108">Video demonstration</span></span>

<span data-ttu-id="3e1f4-109">Cette vidéo montre les étapes de configuration décrites dans ce document.</span><span class="sxs-lookup"><span data-stu-id="3e1f4-109">This video shows the configuration steps described in this document.</span></span></br>

> [!VIDEO https://www.microsoft.com/videoplayer/embed/RE44NTr?autoplay=false]

## <a name="azure-external-collaboration-settings"></a><span data-ttu-id="3e1f4-110">Paramètres de collaboration externe Azure</span><span class="sxs-lookup"><span data-stu-id="3e1f4-110">Azure External collaboration settings</span></span>

<span data-ttu-id="3e1f4-111">Le partage dans Microsoft 365 est régi à son niveau le plus élevé par les [paramètres de collaboration externe B2B dans Azure Active Directory.](https://docs.microsoft.com/azure/active-directory/external-identities/delegate-invitations)</span><span class="sxs-lookup"><span data-stu-id="3e1f4-111">Sharing in Microsoft 365 is governed at its highest level by the [B2B external collaboration settings in Azure Active Directory](https://docs.microsoft.com/azure/active-directory/external-identities/delegate-invitations).</span></span> <span data-ttu-id="3e1f4-112">Si le partage d’invités est désactivé ou restreint dans Azure AD, ce paramètre remplace tous les paramètres de partage que vous configurez dans Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="3e1f4-112">If guest sharing is disabled or restricted in Azure AD, this setting overrides any sharing settings that you configure in Microsoft 365.</span></span>

<span data-ttu-id="3e1f4-113">Vérifiez les paramètres de collaboration externe B2B pour vous assurer que le partage avec des invités n’est pas bloqué.</span><span class="sxs-lookup"><span data-stu-id="3e1f4-113">Check the B2B external collaboration settings settings to ensure that sharing with guests is not blocked.</span></span>

![Capture d’écran de la page des paramètres de relations organisationnelles d’Azure Active Directory](../media/azure-ad-organizational-relationships-settings.png)

<span data-ttu-id="3e1f4-115">Pour définir des paramètres de collaboration externe</span><span class="sxs-lookup"><span data-stu-id="3e1f4-115">To set external collaboration settings</span></span>

1. <span data-ttu-id="3e1f4-116">Connectez-vous à Azure Active Directory sur [https://aad.portal.azure.com](https://aad.portal.azure.com) .</span><span class="sxs-lookup"><span data-stu-id="3e1f4-116">Log in to Azure Active Directory at [https://aad.portal.azure.com](https://aad.portal.azure.com).</span></span>
2. <span data-ttu-id="3e1f4-117">Dans le volet de navigation de gauche, cliquez **sur Azure Active Directory.**</span><span class="sxs-lookup"><span data-stu-id="3e1f4-117">In the left navigation pane, click **Azure Active Directory**.</span></span>
3. <span data-ttu-id="3e1f4-118">Cliquez **sur Identités externes.**</span><span class="sxs-lookup"><span data-stu-id="3e1f4-118">Click **External identities**.</span></span>
4. <span data-ttu-id="3e1f4-119">Dans **l’écran De mise en** main, dans le volet de navigation de gauche, cliquez sur **Paramètres de collaboration externe.**</span><span class="sxs-lookup"><span data-stu-id="3e1f4-119">On the **Get started** screen, in the left navigation pane, click **External collaboration settings**.</span></span>
5. <span data-ttu-id="3e1f4-120">**Assurez-vous que les administrateurs et les utilisateurs** du rôle d’invite d’invités peuvent inviter et que les membres peuvent **inviter** sont tous les deux définies sur **Oui**.</span><span class="sxs-lookup"><span data-stu-id="3e1f4-120">Ensure that **Admins and users in the guest inviter role can invite** and **Members can invite** are both set to **Yes**.</span></span>
6. <span data-ttu-id="3e1f4-121">Si vous avez effectué des modifications, cliquez sur **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="3e1f4-121">If you made changes, click **Save**.</span></span>

<span data-ttu-id="3e1f4-122">Notez les paramètres de la section **Restrictions de** collaboration.</span><span class="sxs-lookup"><span data-stu-id="3e1f4-122">Note the settings in the **Collaboration restrictions** section.</span></span> <span data-ttu-id="3e1f4-123">Assurez-vous que les domaines des invités avec qui vous souhaitez collaborer ne sont pas bloqués.</span><span class="sxs-lookup"><span data-stu-id="3e1f4-123">Make sure that the domains of the guests that you want to collaborate with aren't blocked.</span></span>

<span data-ttu-id="3e1f4-124">Si vous travaillez avec des invités de plusieurs organisations, vous pouvez restreindre leur capacité à accéder aux données d’annuaire.</span><span class="sxs-lookup"><span data-stu-id="3e1f4-124">If you work with guests from multiple organizations, you may want to restrict their ability to access directory data.</span></span> <span data-ttu-id="3e1f4-125">Cela les empêche de voir qui d’autre est un invité dans l’annuaire.</span><span class="sxs-lookup"><span data-stu-id="3e1f4-125">This will prevent them from seeing who else is a guest in the directory.</span></span> <span data-ttu-id="3e1f4-126">Pour ce faire, sous les restrictions d’accès des **utilisateurs invités,** sélectionnez Les utilisateurs invités ont un accès limité aux propriétés et à l’appartenance aux paramètres des objets d’annuaire ou l’accès des **utilisateurs** invités est limité aux propriétés et aux **appartenances** de leurs propres objets d’annuaire.</span><span class="sxs-lookup"><span data-stu-id="3e1f4-126">To do this, under **Guest user access restrictions**, select **Guest users have limited access to properties and membership of directory objects settings** or **Guest user access is restricted to properties and memberships of their own directory objects**.</span></span>

## <a name="teams-guest-access-settings"></a><span data-ttu-id="3e1f4-127">Paramètres d’accès invité Teams</span><span class="sxs-lookup"><span data-stu-id="3e1f4-127">Teams guest access settings</span></span>

<span data-ttu-id="3e1f4-128">Teams dispose d’un commutateur master on/off pour l’accès invité et de divers paramètres disponibles pour contrôler ce que les invités peuvent faire dans une équipe.</span><span class="sxs-lookup"><span data-stu-id="3e1f4-128">Teams has a master on/off switch for guest access and a variety of settings available to control what guests can do in a team.</span></span> <span data-ttu-id="3e1f4-129">Le commutateur maître, **Autoriser l’accès invité dans Teams,** doit être **en** cours pour que l’accès invité fonctionne dans Teams.</span><span class="sxs-lookup"><span data-stu-id="3e1f4-129">The master switch, **Allow guest access in Teams** must be **On** for guest access to work in Teams.</span></span>

<span data-ttu-id="3e1f4-130">Vérifiez que l’accès invité est activé dans Teams et ajustez les paramètres invité en fonction des besoins de votre entreprise.</span><span class="sxs-lookup"><span data-stu-id="3e1f4-130">Check to ensure that guest access is enabled in Teams and make any adjustment to the guest settings based on your business needs.</span></span> <span data-ttu-id="3e1f4-131">Gardez à l’esprit que ces paramètres affectent toutes les équipes.</span><span class="sxs-lookup"><span data-stu-id="3e1f4-131">Keep in mind that these settings affect all teams.</span></span>

![Capture d’écran du commutateur Accès invité dans Teams](../media/teams-guest-access-toggle-on.png)

<span data-ttu-id="3e1f4-133">Pour déterminer les paramètres d’accès invité Teams, procédez comme suit :</span><span class="sxs-lookup"><span data-stu-id="3e1f4-133">To set Teams guest access settings</span></span>

1. <span data-ttu-id="3e1f4-134">Connectez-vous au Centre d’administration Microsoft 365 sur[https://admin.microsoft.com](https://admin.microsoft.com).</span><span class="sxs-lookup"><span data-stu-id="3e1f4-134">Log in to the Microsoft 365 admin center at [https://admin.microsoft.com](https://admin.microsoft.com).</span></span>
2. <span data-ttu-id="3e1f4-135">Dans le volet de navigation de gauche, cliquez **sur Afficher tout.**</span><span class="sxs-lookup"><span data-stu-id="3e1f4-135">In the left navigation pane, click **Show all**.</span></span>
3. <span data-ttu-id="3e1f4-136">Sous **Centres d’administration**, cliquez sur **Teams**.</span><span class="sxs-lookup"><span data-stu-id="3e1f4-136">Under **Admin centers**, click **Teams**.</span></span>
4. <span data-ttu-id="3e1f4-137">Dans le centre d’administration Teams, dans le volet de navigation de gauche, développez les **paramètres** à l’échelle de l’organisation et cliquez sur **Accès invité.**</span><span class="sxs-lookup"><span data-stu-id="3e1f4-137">In the Teams admin center, in the left navigation pane, expand **Org-wide settings** and click **Guest access**.</span></span>
5. <span data-ttu-id="3e1f4-138">Assurez-vous que **Autoriser l’accès invité dans Teams** est défini sur **Activé**.</span><span class="sxs-lookup"><span data-stu-id="3e1f4-138">Ensure that **Allow guest access in Teams** is set to **On**.</span></span>
6. <span data-ttu-id="3e1f4-139">Apportez les modifications souhaitées aux autres paramètres invités, puis cliquez sur **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="3e1f4-139">Make any desired changes to the additional guest settings, and then click **Save**.</span></span>

<span data-ttu-id="3e1f4-140">Une fois l’accès invité Teams est désactivé, vous pouvez éventuellement contrôler l’accès invité à des équipes individuelles et à leurs sites SharePoint associés à l’aide d’étiquettes de sensibilité.</span><span class="sxs-lookup"><span data-stu-id="3e1f4-140">Once Teams guest access is turned on, you can optionally control guest access to individual teams and their associated SharePoint sites using sensitivity labels.</span></span> <span data-ttu-id="3e1f4-141">Pour plus d’informations, voir [Utiliser les étiquettes de confidentialité pour protéger le contenu dans Microsoft Teams, les groupes Office 365 et les sites SharePoint](https://docs.microsoft.com/microsoft-365/compliance/sensitivity-labels-teams-groups-sites).</span><span class="sxs-lookup"><span data-stu-id="3e1f4-141">For more information, see [Use sensitivity labels to protect content in Microsoft Teams, Microsoft 365 groups, and SharePoint sites](https://docs.microsoft.com/microsoft-365/compliance/sensitivity-labels-teams-groups-sites).</span></span>

> [!NOTE]
> <span data-ttu-id="3e1f4-142">L’activité des paramètres invités teams peut prendre jusqu’à 24 heures une fois que vous l’avez active.</span><span class="sxs-lookup"><span data-stu-id="3e1f4-142">It may take up to twenty-four hours for the Teams guest settings to become active after you turn it on.</span></span>

## <a name="microsoft-365-groups-guest-settings"></a><span data-ttu-id="3e1f4-143">Paramètres invités des groupes Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="3e1f4-143">Microsoft 365 Groups guest settings</span></span>

<span data-ttu-id="3e1f4-144">Teams utilise les groupes Microsoft 365 pour l’appartenance à une équipe.</span><span class="sxs-lookup"><span data-stu-id="3e1f4-144">Teams uses Microsoft 365 Groups for team membership.</span></span> <span data-ttu-id="3e1f4-145">Les paramètres invités des groupes Microsoft 365 doivent être allumés pour que l’accès invité dans Teams fonctionne.</span><span class="sxs-lookup"><span data-stu-id="3e1f4-145">The Microsoft 365 Groups guest settings must be turned on in order for guest access in Teams to work.</span></span>

![Capture d’écran des paramètres d’invité des Groupes Microsoft 365 dans le Centre d’administration Microsoft 365](../media/office-365-groups-guest-settings.png)

<span data-ttu-id="3e1f4-147">Pour définir les paramètres invités des groupes Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="3e1f4-147">To set Microsoft 365 Groups guest settings</span></span>

1. <span data-ttu-id="3e1f4-148">Dans le Centre d’administration Microsoft 365, dans le volet de navigation de gauche, développez **Paramètres.**</span><span class="sxs-lookup"><span data-stu-id="3e1f4-148">In the Microsoft 365 admin center, in the left navigation pane, expand **Settings**.</span></span>
2. <span data-ttu-id="3e1f4-149">Cliquez **sur Paramètres de l’organisation.**</span><span class="sxs-lookup"><span data-stu-id="3e1f4-149">Click **Org settings**.</span></span>
3. <span data-ttu-id="3e1f4-150">Dans la liste, cliquez **sur Groupes Microsoft 365.**</span><span class="sxs-lookup"><span data-stu-id="3e1f4-150">In the list, click **Microsoft 365 Groups**.</span></span>
4. <span data-ttu-id="3e1f4-151">Assurez-vous que les propriétaires du groupe Permettre aux propriétaires d’ajouter des personnes extérieures à votre organisation aux groupes **Microsoft 365** en tant qu’invités et permettre aux membres du groupe invité d’accéder aux cases à cocher de contenu du groupe sont cochées. </span><span class="sxs-lookup"><span data-stu-id="3e1f4-151">Ensure that the **Let group owners add people outside your organization to Microsoft 365 Groups as guests** and **Let guest group members access group content** check boxes are both checked.</span></span>
5. <span data-ttu-id="3e1f4-152">Si vous avez apporté des modifications, cliquez **sur Enregistrer les modifications.**</span><span class="sxs-lookup"><span data-stu-id="3e1f4-152">If you made changes, click **Save changes**.</span></span>


## <a name="sharepoint-organization-level-sharing-settings"></a><span data-ttu-id="3e1f4-153">Paramètres de partage au niveau de l’organisation SharePoint</span><span class="sxs-lookup"><span data-stu-id="3e1f4-153">SharePoint organization level sharing settings</span></span>

<span data-ttu-id="3e1f4-154">Le contenu Teams, tel que les fichiers, les dossiers et les listes, est stocké dans SharePoint.</span><span class="sxs-lookup"><span data-stu-id="3e1f4-154">Teams content such as files, folders, and lists are all stored in SharePoint.</span></span> <span data-ttu-id="3e1f4-155">Pour que les invités ont accès à ces éléments dans Teams, les paramètres de partage au niveau de l’organisation SharePoint doivent autoriser le partage avec des invités.</span><span class="sxs-lookup"><span data-stu-id="3e1f4-155">In order for guests to have access to these items in Teams, the SharePoint organization-level sharing settings must allow for sharing with guests.</span></span>

<span data-ttu-id="3e1f4-156">Les paramètres au niveau de l’organisation déterminent les paramètres disponibles pour les sites individuels, y compris les sites associés à des équipes.</span><span class="sxs-lookup"><span data-stu-id="3e1f4-156">The organization-level settings determine what settings are available for individual sites, including sites associated with teams.</span></span> <span data-ttu-id="3e1f4-157">Les paramètres de site ne peuvent pas être plus permissifs que les paramètres au niveau de l’organisation.</span><span class="sxs-lookup"><span data-stu-id="3e1f4-157">Site settings cannot be more permissive than the organization-level settings.</span></span>

<span data-ttu-id="3e1f4-158">Si vous souhaitez autoriser le partage de fichiers et de dossiers avec des personnes non authentifiés, choisissez **Tout le monde.**</span><span class="sxs-lookup"><span data-stu-id="3e1f4-158">If you want to allow file and folder sharing with unauthenticated people, choose **Anyone**.</span></span> <span data-ttu-id="3e1f4-159">Si vous souhaitez vous assurer que tous les invités doivent s’authentifier, choisissez **Invités nouveaux et existants.**</span><span class="sxs-lookup"><span data-stu-id="3e1f4-159">If you want to ensure that all guests have to authenticate, choose **New and existing guests**.</span></span> <span data-ttu-id="3e1f4-160">Choisissez le paramètre le plus permissif qui sera nécessaire à n’importe quel site de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="3e1f4-160">Choose the most permissive setting that will be needed by any site in your organization.</span></span>

![Capture d’écran des paramètres de partage SharePoint au niveau de l’organisation](../media/sharepoint-organization-external-sharing-controls.png)


<span data-ttu-id="3e1f4-162">Pour définir les paramètres de partage au niveau de l’organisation SharePoint</span><span class="sxs-lookup"><span data-stu-id="3e1f4-162">To set SharePoint organization-level sharing settings</span></span>

1. <span data-ttu-id="3e1f4-163">Dans le Centre d’administration Microsoft 365, dans le volet de navigation de gauche, sous Centres d’administration, cliquez **sur SharePoint**.</span><span class="sxs-lookup"><span data-stu-id="3e1f4-163">In the Microsoft 365 admin center, in the left navigation pane, under **Admin centers**, click **SharePoint**.</span></span>
2. <span data-ttu-id="3e1f4-164">Dans le Centre d’administration SharePoint, dans le volet de navigation de gauche, développez **Stratégies,** puis cliquez sur **Partage.**</span><span class="sxs-lookup"><span data-stu-id="3e1f4-164">In the SharePoint admin center, in the left navigation pane, expand **Policies** and then click **Sharing**.</span></span>
3. <span data-ttu-id="3e1f4-165">Assurez-vous que le partage externe pour SharePoint est définie sur **Tout** le monde ou **Nouveau et les invités existants.**</span><span class="sxs-lookup"><span data-stu-id="3e1f4-165">Ensure that external sharing for SharePoint is set to **Anyone** or **New and existing guests**.</span></span>
4. <span data-ttu-id="3e1f4-166">Si vous avez effectué des modifications, cliquez sur **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="3e1f4-166">If you made changes, click **Save**.</span></span>


## <a name="sharepoint-organization-level-default-link-settings"></a><span data-ttu-id="3e1f4-167">Paramètres de lien par défaut au niveau de l’organisation SharePoint</span><span class="sxs-lookup"><span data-stu-id="3e1f4-167">SharePoint organization-level default link settings</span></span>

<span data-ttu-id="3e1f4-168">Les paramètres de lien de fichiers et de dossiers par défaut déterminent l’option de lien qui sera affichée par défaut aux utilisateurs lorsqu’ils partagent un fichier ou un dossier.</span><span class="sxs-lookup"><span data-stu-id="3e1f4-168">The default file and folder link settings determine the link option that will be shown to users by default when they share a file or folder.</span></span> <span data-ttu-id="3e1f4-169">Les utilisateurs peuvent modifier le type de lien en l’une des autres options avant le partage, si vous le souhaitez.</span><span class="sxs-lookup"><span data-stu-id="3e1f4-169">Users can change the link type to one of the other options before sharing, if desired.</span></span>

<span data-ttu-id="3e1f4-170">N’oubliez pas que ce paramètre affecte toutes les équipes et les sites SharePoint de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="3e1f4-170">Keep in mind that this setting affects all teams and SharePoint sites in your organization.</span></span>

<span data-ttu-id="3e1f4-171">Choisissez l’un des types de liens suivants qui sera sélectionné par défaut lorsque les utilisateurs partagent des fichiers et des dossiers :</span><span class="sxs-lookup"><span data-stu-id="3e1f4-171">Choose any one of the following link-types which will be selected by default when users share files and folders:</span></span>

- <span data-ttu-id="3e1f4-172">**Toute personne partageant le** lien : choisissez cette option si vous prévoyez d’avoir un grand nombre de partages non authentifiés de fichiers et de dossiers.</span><span class="sxs-lookup"><span data-stu-id="3e1f4-172">**Anyone with the link** - Choose this option if you expect to do a lot of unauthenticated sharing of files and folders.</span></span> <span data-ttu-id="3e1f4-173">Si vous souhaitez autoriser les liens *Tout* le monde mais que vous êtes préoccupé par le partage non authentifié accidentel, envisagez l’une des autres options par défaut.</span><span class="sxs-lookup"><span data-stu-id="3e1f4-173">If you want to allow *Anyone* links but are concerned about accidental unauthenticated sharing, consider one of the other options as the default.</span></span> <span data-ttu-id="3e1f4-174">Ce type de lien est disponible uniquement si vous avez activé le partage **tout le** monde.</span><span class="sxs-lookup"><span data-stu-id="3e1f4-174">This link type is only available if you've enabled **Anyone** sharing.</span></span>
- <span data-ttu-id="3e1f4-175">**Seules les personnes de votre organisation** : choisissez cette option si vous pensez que la plupart des partages de fichiers et de dossiers seront partagés avec des personnes au sein de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="3e1f4-175">**Only people in your organization** - Choose this option if you expect most file and folder sharing to be with people inside your organization.</span></span>
- <span data-ttu-id="3e1f4-176">**Personnes spécifiques** : envisagez cette option si vous comptez faire beaucoup de partage de fichiers et de dossiers avec des invités.</span><span class="sxs-lookup"><span data-stu-id="3e1f4-176">**Specific people** - Consider this option if you expect to do a lot of file and folder sharing with guests.</span></span> <span data-ttu-id="3e1f4-177">Ce type de lien fonctionne avec les invités et les oblige à s’authentifier.</span><span class="sxs-lookup"><span data-stu-id="3e1f4-177">This type of link works with guests and requires them to authenticate.</span></span>
 
![Capture d’écran des paramètres de partage de fichiers et dossiers au niveau de l’organisation dans SharePoint](../media/sharepoint-organization-files-folders-sharing-settings.png)


<span data-ttu-id="3e1f4-179">Pour définir les paramètres de lien par défaut au niveau de l’organisation SharePoint</span><span class="sxs-lookup"><span data-stu-id="3e1f4-179">To set the SharePoint organization-level default link settings</span></span>

1. <span data-ttu-id="3e1f4-180">Accédez à la page Partage dans le Centre d’administration SharePoint.</span><span class="sxs-lookup"><span data-stu-id="3e1f4-180">Navigate to the Sharing page in the SharePoint admin center.</span></span>
2. <span data-ttu-id="3e1f4-181">Sous **Liens de fichiers et de dossiers,** sélectionnez le lien de partage par défaut que vous souhaitez utiliser.</span><span class="sxs-lookup"><span data-stu-id="3e1f4-181">Under **File and folder links**, select the default sharing link that you want to use.</span></span>
3. <span data-ttu-id="3e1f4-182">Si vous avez effectué des modifications, cliquez sur **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="3e1f4-182">If you made changes, click **Save**.</span></span>

## <a name="create-a-team"></a><span data-ttu-id="3e1f4-183">Créer une équipe</span><span class="sxs-lookup"><span data-stu-id="3e1f4-183">Create a team</span></span>

<span data-ttu-id="3e1f4-184">L’étape suivante consiste à créer l’équipe que vous prévoyez d’utiliser pour collaborer avec des invités.</span><span class="sxs-lookup"><span data-stu-id="3e1f4-184">The next step is to create the team that you plan to use for collaborating with guests.</span></span>

<span data-ttu-id="3e1f4-185">Pour créer une équipe</span><span class="sxs-lookup"><span data-stu-id="3e1f4-185">To create a team</span></span>
1. <span data-ttu-id="3e1f4-186">Dans Teams, sous l’onglet **Teams,** cliquez sur **Rejoindre** ou créer une équipe en bas du volet gauche.</span><span class="sxs-lookup"><span data-stu-id="3e1f4-186">In Teams, on the **Teams** tab, click **Join or create a team** at the bottom of the left pane.</span></span>
2. <span data-ttu-id="3e1f4-187">Cliquez **sur Créer une équipe.**</span><span class="sxs-lookup"><span data-stu-id="3e1f4-187">Click **Create a team**.</span></span>
3. <span data-ttu-id="3e1f4-188">Cliquez **sur Créer une équipe à partir de zéro.**</span><span class="sxs-lookup"><span data-stu-id="3e1f4-188">Click **Build a team from scratch**.</span></span>
4. <span data-ttu-id="3e1f4-189">Choisissez **Privé** ou **Public.**</span><span class="sxs-lookup"><span data-stu-id="3e1f4-189">Choose **Private** or **Public**.</span></span>
5. <span data-ttu-id="3e1f4-190">Tapez un nom et une description pour l’équipe, puis cliquez sur **Créer.**</span><span class="sxs-lookup"><span data-stu-id="3e1f4-190">Type a name and description for the team, and then click **Create**.</span></span>
6. <span data-ttu-id="3e1f4-191">Cliquez **sur Ignorer.**</span><span class="sxs-lookup"><span data-stu-id="3e1f4-191">Click **Skip**.</span></span>

<span data-ttu-id="3e1f4-192">Nous inviterons les utilisateurs ultérieurement.</span><span class="sxs-lookup"><span data-stu-id="3e1f4-192">We'll invite users later.</span></span> <span data-ttu-id="3e1f4-193">Ensuite, il est important de vérifier les paramètres de partage au niveau du site pour le site SharePoint associé à l’équipe.</span><span class="sxs-lookup"><span data-stu-id="3e1f4-193">Next, it's important to check the site-level sharing settings for the SharePoint site that is associated with the team.</span></span>

## <a name="sharepoint-site-level-sharing-settings"></a><span data-ttu-id="3e1f4-194">Paramètres de partage au niveau du site SharePoint</span><span class="sxs-lookup"><span data-stu-id="3e1f4-194">SharePoint site-level sharing settings</span></span>

<span data-ttu-id="3e1f4-195">Vérifiez les paramètres de partage au niveau du site pour vous assurer qu’ils autorisent le type d’accès que vous souhaitez pour cette équipe.</span><span class="sxs-lookup"><span data-stu-id="3e1f4-195">Check the site-level sharing settings to make sure that they allow the type of access that you want for this team.</span></span> <span data-ttu-id="3e1f4-196">Par exemple, si vous définissez les paramètres au niveau de l’organisation sur Tout le **monde,** mais que vous souhaitez que tous les invités s’authentifier pour cette équipe, assurez-vous que les paramètres de partage au niveau du site sont les invités nouveaux et existants. </span><span class="sxs-lookup"><span data-stu-id="3e1f4-196">For example, if you set the organization-level settings to **Anyone**, but you want all guests to authenticate for this team, then make sure the site-level sharing settings are set to **New and existing guests**.</span></span>

![Capture d’écran des paramètres de partage externe de site SharePoint](../media/sharepoint-site-external-sharing-settings.png)

<span data-ttu-id="3e1f4-198">Pour définir les paramètres de partage au niveau du site</span><span class="sxs-lookup"><span data-stu-id="3e1f4-198">To set site-level sharing settings</span></span>
1. <span data-ttu-id="3e1f4-199">Dans le Centre d’administration SharePoint, dans le volet de navigation de gauche, développez **Sites** et cliquez **sur Sites actifs.**</span><span class="sxs-lookup"><span data-stu-id="3e1f4-199">In the SharePoint admin center, in the left navigation pane, expand **Sites** and click **Active sites**.</span></span>
2. <span data-ttu-id="3e1f4-200">Sélectionnez le site de l’équipe que vous venez de créer.</span><span class="sxs-lookup"><span data-stu-id="3e1f4-200">Select the site for the team that you just created.</span></span>
3. <span data-ttu-id="3e1f4-201">Cliquez sur ... et choisissez **Partage.**</span><span class="sxs-lookup"><span data-stu-id="3e1f4-201">Click ... and choose **Sharing**.</span></span>
4. <span data-ttu-id="3e1f4-202">Assurez-vous que le partage est définie sur **Tout** le monde ou **Nouveau et sur les invités existants.**</span><span class="sxs-lookup"><span data-stu-id="3e1f4-202">Ensure that sharing is set to **Anyone** or **New and existing guests**.</span></span>
5. <span data-ttu-id="3e1f4-203">Si vous avez effectué des modifications, cliquez sur **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="3e1f4-203">If you made changes, click **Save**.</span></span>

## <a name="invite-users"></a><span data-ttu-id="3e1f4-204">Inviter des utilisateurs</span><span class="sxs-lookup"><span data-stu-id="3e1f4-204">Invite users</span></span>

<span data-ttu-id="3e1f4-205">Les paramètres de partage d’invités sont désormais configurés, afin que vous pouvez commencer à ajouter des utilisateurs internes et des invités à votre équipe.</span><span class="sxs-lookup"><span data-stu-id="3e1f4-205">Guest sharing settings are now configured, so you can start adding internal users and guests to your team.</span></span> 

<span data-ttu-id="3e1f4-206">Pour inviter des utilisateurs internes à une équipe</span><span class="sxs-lookup"><span data-stu-id="3e1f4-206">To invite internal users to a team</span></span>
1. <span data-ttu-id="3e1f4-207">Dans l’équipe, cliquez **sur Plus d’options** ( **\*\*\*** ), puis cliquez sur Ajouter un **membre.**</span><span class="sxs-lookup"><span data-stu-id="3e1f4-207">In the team, click **More options** (**\*\*\***), and then click **Add member**.</span></span>
2. <span data-ttu-id="3e1f4-208">Tapez le nom de la personne que vous voulez inviter.</span><span class="sxs-lookup"><span data-stu-id="3e1f4-208">Type the name of the person who you want to invite.</span></span>
3. <span data-ttu-id="3e1f4-209">Cliquez **sur** Ajouter, puis sur **Fermer.**</span><span class="sxs-lookup"><span data-stu-id="3e1f4-209">Click **Add**, and then click **Close**.</span></span>

<span data-ttu-id="3e1f4-210">Pour inviter des invités à une équipe</span><span class="sxs-lookup"><span data-stu-id="3e1f4-210">To invite guests to a team</span></span>
1. <span data-ttu-id="3e1f4-211">Dans l’équipe, cliquez **sur Plus d’options** ( **\*\*\*** ), puis cliquez sur Ajouter un **membre.**</span><span class="sxs-lookup"><span data-stu-id="3e1f4-211">In the team, click **More options** (**\*\*\***), and then click **Add member**.</span></span>
2. <span data-ttu-id="3e1f4-212">Tapez l’adresse e-mail de l’invité que vous voulez inviter.</span><span class="sxs-lookup"><span data-stu-id="3e1f4-212">Type the email address of the guest whom you want to invite.</span></span>
3. <span data-ttu-id="3e1f4-213">Cliquez sur **Modifier les informations d’invité.**</span><span class="sxs-lookup"><span data-stu-id="3e1f4-213">Click **Edit guest information**.</span></span>
4. <span data-ttu-id="3e1f4-214">Tapez le nom complet de l’invité et cliquez sur la coche.</span><span class="sxs-lookup"><span data-stu-id="3e1f4-214">Type the guest's full name and click the check mark.</span></span>
5. <span data-ttu-id="3e1f4-215">Cliquez **sur** Ajouter, puis sur **Fermer.**</span><span class="sxs-lookup"><span data-stu-id="3e1f4-215">Click **Add**, and then click **Close**.</span></span>

## <a name="see-also"></a><span data-ttu-id="3e1f4-216">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3e1f4-216">See also</span></span>

[<span data-ttu-id="3e1f4-217">Meilleures pratiques relatives au partage de fichiers et de dossiers avec des utilisateurs non authentifiés</span><span class="sxs-lookup"><span data-stu-id="3e1f4-217">Best practices for sharing files and folders with unauthenticated users</span></span>](best-practices-anonymous-sharing.md)

[<span data-ttu-id="3e1f4-218">Limiter l’exposition accidentelle aux fichiers lors du partage avec des invités</span><span class="sxs-lookup"><span data-stu-id="3e1f4-218">Limit accidental exposure to files when sharing with guests</span></span>](share-limit-accidental-exposure.md)

[<span data-ttu-id="3e1f4-219">Créer un environnement de partage sécurisé avec des invités</span><span class="sxs-lookup"><span data-stu-id="3e1f4-219">Create a secure guest sharing environment</span></span>](create-secure-guest-sharing-environment.md)

[<span data-ttu-id="3e1f4-220">Créer un extranet B2B avec des invités gérés</span><span class="sxs-lookup"><span data-stu-id="3e1f4-220">Create a B2B extranet with managed guests</span></span>](b2b-extranet.md)

[<span data-ttu-id="3e1f4-221">Intégration de SharePoint et de OneDrive à Azure AD B2B</span><span class="sxs-lookup"><span data-stu-id="3e1f4-221">SharePoint and OneDrive integration with Azure AD B2B</span></span>](https://docs.microsoft.com/sharepoint/sharepoint-azureb2b-integration-preview)

[<span data-ttu-id="3e1f4-222">Les options de partage sont grisées lors du partage à partir de SharePoint ou OneDrive</span><span class="sxs-lookup"><span data-stu-id="3e1f4-222">Sharing options are greyed out when sharing from SharePoint or OneDrive</span></span>](https://docs.microsoft.com/sharepoint/troubleshoot/administration/sharing-options-grayed-out-when-sharing-from-sharepoint-online-or-onedrive)
