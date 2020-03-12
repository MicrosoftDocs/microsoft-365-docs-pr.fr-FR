---
title: Collaborer avec des invités au sein d’une équipe
ms.author: mikeplum
author: MikePlumleyMSFT
manager: pamgreen
audience: ITPro
ms.topic: article
ms.service: sharepoint-online
ms.collection: SPO_Content
localization_priority: Normal
f1.keywords: NOCSH
description: Découvrez comment collaborer avec des invités dans Teams.
ms.openlocfilehash: 54bf52eebc77e1cce8e1c05a708572d7d1e7fdae
ms.sourcegitcommit: 21338a9287017a66298e0ff557e80051946ebf13
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/11/2020
ms.locfileid: "42604523"
---
# <a name="collaborate-with-guests-in-a-team"></a><span data-ttu-id="f31ba-103">Collaborer avec des invités au sein d’une équipe</span><span class="sxs-lookup"><span data-stu-id="f31ba-103">Collaborate with guests in a team</span></span>

<span data-ttu-id="f31ba-104">Si vous avez besoin de collaborer avec des invités dans des documents, des tâches et des conversations, nous vous recommandons d’utiliser Microsoft Teams.</span><span class="sxs-lookup"><span data-stu-id="f31ba-104">If you need to collaborate with guests across documents, tasks, and conversations, we recommend using Microsoft Teams.</span></span> <span data-ttu-id="f31ba-105">Teams fournit toutes les fonctionnalités de collaboration disponibles dans Office et SharePoint avec conversation permanente et un ensemble d’outils de collaboration personnalisable et extensible dans une expérience utilisateur unifiée.</span><span class="sxs-lookup"><span data-stu-id="f31ba-105">Teams provides all of the collaboration features available in Office and SharePoint with persistent chat and a customizable and extensible set of collaboration tools in a unified user experience.</span></span>

<span data-ttu-id="f31ba-106">Dans cet article, nous allons passer en revue les étapes de configuration de Microsoft 365 nécessaires pour configurer une équipe de collaboration avec des invités.</span><span class="sxs-lookup"><span data-stu-id="f31ba-106">In this article, we'll walk through the Microsoft 365 configuration steps necessary to set up a team for collaboration with guests.</span></span>

## <a name="video-demonstration"></a><span data-ttu-id="f31ba-107">Démonstration vidéo</span><span class="sxs-lookup"><span data-stu-id="f31ba-107">Video demonstration</span></span>

<span data-ttu-id="f31ba-108">Cette vidéo présente les étapes de configuration décrites dans ce document.</span><span class="sxs-lookup"><span data-stu-id="f31ba-108">This video shows the configuration steps described in this document.</span></span></br>

> [!VIDEO https://www.microsoft.com/videoplayer/embed/RE44NTr?autoplay=false]

## <a name="azure-organizational-relationships-settings"></a><span data-ttu-id="f31ba-109">Paramètres Azure de relations organisationnelles</span><span class="sxs-lookup"><span data-stu-id="f31ba-109">Azure Organizational relationships settings</span></span>

<span data-ttu-id="f31ba-110">Le partage dans Microsoft 365 est régi par les paramètres de relations organisationnelles dans Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="f31ba-110">Sharing in Microsoft 365 is governed at its highest level by the organizational relationships settings in Azure Active Directory.</span></span> <span data-ttu-id="f31ba-111">Si le partage d’invités est désactivé ou restreint dans Azure AD, cela remplace tous les paramètres de partage que vous configurez dans Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="f31ba-111">If guest sharing is disabled or restricted in Azure AD, this will override any sharing settings that you configure in Microsoft 365.</span></span>

<span data-ttu-id="f31ba-112">Vérifiez les paramètres de relations organisationnelles pour vous assurer que le partage avec des invités n’est pas bloqué.</span><span class="sxs-lookup"><span data-stu-id="f31ba-112">Check the organizational relationships settings to ensure that sharing with guests is not blocked.</span></span>

![Capture d’écran de la page des paramètres de relations organisationnelles d’Azure Active Directory](../media/azure-ad-organizational-relationships-settings.png)

<span data-ttu-id="f31ba-114">Pour définir les paramètres de relation organisationnelle</span><span class="sxs-lookup"><span data-stu-id="f31ba-114">To set organizational relationship settings</span></span>

1. <span data-ttu-id="f31ba-115">Connectez-vous à Microsoft Azure [https://portal.azure.com](https://portal.azure.com)à l’adresse.</span><span class="sxs-lookup"><span data-stu-id="f31ba-115">Log in to Microsoft Azure at [https://portal.azure.com](https://portal.azure.com).</span></span>
2. <span data-ttu-id="f31ba-116">Dans le volet de navigation de gauche, cliquez sur **Azure Active Directory**.</span><span class="sxs-lookup"><span data-stu-id="f31ba-116">In the left navigation, click **Azure Active Directory**.</span></span>
3. <span data-ttu-id="f31ba-117">Dans le volet de **vue d’ensemble** , cliquez sur **relations organisationnelles**.</span><span class="sxs-lookup"><span data-stu-id="f31ba-117">In the **Overview** pane, click **Organizational relationships**.</span></span>
4. <span data-ttu-id="f31ba-118">Dans le volet **relations organisationnelles** , cliquez sur **paramètres**.</span><span class="sxs-lookup"><span data-stu-id="f31ba-118">In the **Organizational relationships** pane, click **Settings**.</span></span>
5. <span data-ttu-id="f31ba-119">Assurez-vous que les **administrateurs et les utilisateurs du rôle d’invité invité peuvent inviter** et que les **membres peuvent inviter** sont tous deux la valeur **Oui**.</span><span class="sxs-lookup"><span data-stu-id="f31ba-119">Ensure that **Admins and users in the guest inviter role can invite** and **Members can invite** are both set to **Yes**.</span></span>
6. <span data-ttu-id="f31ba-120">Si vous avez effectué des modifications, cliquez sur **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="f31ba-120">If you made changes, click **Save**.</span></span>

<span data-ttu-id="f31ba-121">Notez les paramètres dans la section **restrictions de collaboration** .</span><span class="sxs-lookup"><span data-stu-id="f31ba-121">Note the settings in the **Collaboration restrictions** section.</span></span> <span data-ttu-id="f31ba-122">Assurez-vous que les domaines des invités avec lesquels vous souhaitez collaborer ne sont pas bloqués.</span><span class="sxs-lookup"><span data-stu-id="f31ba-122">Make sure that the domains of the guests that you want to collaborate with aren't blocked.</span></span>

## <a name="teams-guest-access-settings"></a><span data-ttu-id="f31ba-123">Paramètres d’accès invité de teams</span><span class="sxs-lookup"><span data-stu-id="f31ba-123">Teams guest access settings</span></span>

<span data-ttu-id="f31ba-124">Teams dispose d’un commutateur maître/inactif pour l’accès invité et de divers paramètres permettant de contrôler ce que les invités peuvent faire dans une équipe.</span><span class="sxs-lookup"><span data-stu-id="f31ba-124">Teams has a master on/off switch for guest access and a variety of settings available to control what guests can do in a team.</span></span> <span data-ttu-id="f31ba-125">Le commutateur maître, **autoriser l’accès invité dans teams** doit être **activé** pour que l’accès invité fonctionne dans Teams.</span><span class="sxs-lookup"><span data-stu-id="f31ba-125">The master switch, **Allow guest access in Teams** must be **On** for guest access to work in Teams.</span></span>

<span data-ttu-id="f31ba-126">Vérifiez que l’accès invité est activé dans teams et effectuez les ajustements nécessaires aux paramètres invités en fonction des besoins de votre entreprise.</span><span class="sxs-lookup"><span data-stu-id="f31ba-126">Check to ensure that guest access is enabled in Teams and make any adjustment to the guest settings based on your business needs.</span></span> <span data-ttu-id="f31ba-127">N’oubliez pas que ces paramètres affectent toutes les équipes.</span><span class="sxs-lookup"><span data-stu-id="f31ba-127">Keep in mind that these settings affect all teams.</span></span>

![Capture d’écran du commutateur Accès invité dans Teams](../media/teams-guest-access-toggle-on.png)

<span data-ttu-id="f31ba-129">Pour définir les paramètres d’accès invité aux équipes</span><span class="sxs-lookup"><span data-stu-id="f31ba-129">To set Teams guest access settings</span></span>

1. <span data-ttu-id="f31ba-130">Connectez-vous au centre d’administration Microsoft 365 [https://admin.microsoft.com](https://admin.microsoft.com)à l’adresse.</span><span class="sxs-lookup"><span data-stu-id="f31ba-130">Log in to the Microsoft 365 admin center at [https://admin.microsoft.com](https://admin.microsoft.com).</span></span>
2. <span data-ttu-id="f31ba-131">Dans le volet de navigation de gauche, cliquez sur **Afficher tout**.</span><span class="sxs-lookup"><span data-stu-id="f31ba-131">In the left navigation, click **Show all**.</span></span>
3. <span data-ttu-id="f31ba-132">Sous **centres d’administration**, cliquez sur **équipes**.</span><span class="sxs-lookup"><span data-stu-id="f31ba-132">Under **Admin centers**, click **Teams**.</span></span>
4. <span data-ttu-id="f31ba-133">Dans le centre d’administration Teams, dans le volet de navigation de gauche, développez Paramètres à l’échelle de l' **organisation** , puis cliquez sur **accès invité**.</span><span class="sxs-lookup"><span data-stu-id="f31ba-133">In the Teams admin center, in the left navigation, expand **Org-wide settings** and click **Guest access**.</span></span>
5. <span data-ttu-id="f31ba-134">Assurez-vous que **l’autorisation autoriser l’accès invité dans teams** est **activée.**</span><span class="sxs-lookup"><span data-stu-id="f31ba-134">Ensure that **Allow guest access in Teams** is set to **On**.</span></span>
6. <span data-ttu-id="f31ba-135">Effectuez toutes les modifications souhaitées dans les paramètres d’invité supplémentaires, puis cliquez sur **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="f31ba-135">Make any desired changes to the additional guest settings, and then click **Save**.</span></span>

> [!NOTE]
> <span data-ttu-id="f31ba-136">Le paramètre invité de teams peut prendre jusqu’à vingt-quatre heures après son activation.</span><span class="sxs-lookup"><span data-stu-id="f31ba-136">It may take up to twenty-four hours for the Teams guest setting to become active after you turn it on.</span></span>

## <a name="office-365-groups-guest-settings"></a><span data-ttu-id="f31ba-137">Les paramètres invités des groupes Office 365</span><span class="sxs-lookup"><span data-stu-id="f31ba-137">Office 365 Groups guest settings</span></span>

<span data-ttu-id="f31ba-138">Teams utilise les groupes Office 365 pour les membres de l’équipe.</span><span class="sxs-lookup"><span data-stu-id="f31ba-138">Teams uses Office 365 Groups for team membership.</span></span> <span data-ttu-id="f31ba-139">Les paramètres invités des groupes Office 365 doivent être activés pour que l’accès invité dans teams puisse fonctionner.</span><span class="sxs-lookup"><span data-stu-id="f31ba-139">The Office 365 Groups guest settings must be turned on in order for guest access in Teams to work.</span></span>

![Capture d’écran des paramètres d’invité des Groupes Office 365 dans le Centre d’administration Microsoft 365](../media/office-365-groups-guest-settings.png)

<span data-ttu-id="f31ba-141">Pour définir les paramètres invités des groupes Office 365</span><span class="sxs-lookup"><span data-stu-id="f31ba-141">To set Office 365 Groups guest settings</span></span>

1. <span data-ttu-id="f31ba-142">Dans le centre d’administration Microsoft 365, dans le volet de navigation de gauche, développez **paramètres**.</span><span class="sxs-lookup"><span data-stu-id="f31ba-142">In the Microsoft 365 admin center, in the left navigation, expand **Settings**.</span></span>
2. <span data-ttu-id="f31ba-143">Cliquez sur **Services & compléments**.</span><span class="sxs-lookup"><span data-stu-id="f31ba-143">Click **Services & add-ins**.</span></span>
3. <span data-ttu-id="f31ba-144">Dans la liste, cliquez sur **groupes Office 365**.</span><span class="sxs-lookup"><span data-stu-id="f31ba-144">In the list, click **Office 365 Groups**.</span></span>
4. <span data-ttu-id="f31ba-145">Assurez-vous que les **membres de groupe Let en dehors de votre organisation accèdent au contenu de groupe** et que les **propriétaires de groupes ajoutent des personnes en dehors de votre organisation aux** cases à cocher sont activées.</span><span class="sxs-lookup"><span data-stu-id="f31ba-145">Ensure that the **Let group members outside your organization access group content** and **Let group owners add people outside your organization to groups** check boxes are both checked.</span></span>
5. <span data-ttu-id="f31ba-146">Si vous avez apporté des modifications, cliquez sur **enregistrer les modifications**.</span><span class="sxs-lookup"><span data-stu-id="f31ba-146">If you made changes, click **Save changes**.</span></span>


## <a name="sharepoint-organization-level-sharing-settings"></a><span data-ttu-id="f31ba-147">Paramètres de partage au niveau de l’organisation SharePoint</span><span class="sxs-lookup"><span data-stu-id="f31ba-147">SharePoint organization level sharing settings</span></span>

<span data-ttu-id="f31ba-148">Le contenu de teams, tel que des fichiers, des dossiers et des listes, est tous stockés dans SharePoint.</span><span class="sxs-lookup"><span data-stu-id="f31ba-148">Teams content such as files, folders, and lists are all stored in SharePoint.</span></span> <span data-ttu-id="f31ba-149">Pour que les invités aient accès à ces éléments dans Teams, les paramètres de partage au niveau de l’organisation SharePoint doivent autoriser le partage avec des invités.</span><span class="sxs-lookup"><span data-stu-id="f31ba-149">In order for guests to have access to these items in Teams, the SharePoint organization-level sharing settings must allow for sharing with guests.</span></span>

<span data-ttu-id="f31ba-150">Les paramètres au niveau de l’organisation déterminent les paramètres disponibles pour des sites individuels, y compris les sites associés à Teams.</span><span class="sxs-lookup"><span data-stu-id="f31ba-150">The organization-level settings determine what settings are available for individual sites, including sites associated with teams.</span></span> <span data-ttu-id="f31ba-151">Les paramètres de site ne peuvent pas être plus permissants que les paramètres au niveau de l’organisation.</span><span class="sxs-lookup"><span data-stu-id="f31ba-151">Site settings cannot be more permissive than the organization-level settings.</span></span>

<span data-ttu-id="f31ba-152">Si vous souhaitez autoriser le partage de fichiers et de dossiers avec des personnes non authentifiées, sélectionnez **tout le monde**.</span><span class="sxs-lookup"><span data-stu-id="f31ba-152">If you want to allow file and folder sharing with unauthenticated people, choose **Anyone**.</span></span> <span data-ttu-id="f31ba-153">Si vous souhaitez vous assurer que tous les invités doivent s’authentifier, choisissez **nouveau et invités existants**.</span><span class="sxs-lookup"><span data-stu-id="f31ba-153">If you want to ensure that all guests have to authenticate, choose **New and existing guests**.</span></span> <span data-ttu-id="f31ba-154">Choisissez le paramètre le plus permissif qui sera nécessaire pour tous les sites de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="f31ba-154">Choose the most permissive setting that will be needed by any site in your organization.</span></span>

![Capture d’écran des paramètres de partage SharePoint au niveau de l’organisation](../media/sharepoint-organization-external-sharing-controls.png)


<span data-ttu-id="f31ba-156">Pour définir les paramètres de partage au niveau de l’organisation SharePoint</span><span class="sxs-lookup"><span data-stu-id="f31ba-156">To set SharePoint organization level sharing settings</span></span>

1. <span data-ttu-id="f31ba-157">Dans le centre d’administration 365 de Microsoft, dans le volet de navigation de gauche, sous **centres d’administration**, cliquez sur **SharePoint**.</span><span class="sxs-lookup"><span data-stu-id="f31ba-157">In the Microsoft 365 admin center, in the left navigation, under **Admin centers**, click **SharePoint**.</span></span>
2. <span data-ttu-id="f31ba-158">Dans le centre d’administration SharePoint, dans le volet de gauche, cliquez sur **Partage**.</span><span class="sxs-lookup"><span data-stu-id="f31ba-158">In the SharePoint admin center, in the left navigation, click **Sharing**.</span></span>
3. <span data-ttu-id="f31ba-159">Assurez-vous que le partage externe pour SharePoint est défini sur **tout le monde** ou sur **des invités nouveaux et existants**.</span><span class="sxs-lookup"><span data-stu-id="f31ba-159">Ensure that external sharing for SharePoint is set to **Anyone** or **New and existing guests**.</span></span>
4. <span data-ttu-id="f31ba-160">Si vous avez effectué des modifications, cliquez sur **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="f31ba-160">If you made changes, click **Save**.</span></span>


## <a name="sharepoint-organization-level-default-link-settings"></a><span data-ttu-id="f31ba-161">Paramètres de lien par défaut au niveau de l’organisation SharePoint</span><span class="sxs-lookup"><span data-stu-id="f31ba-161">SharePoint organization level default link settings</span></span>

<span data-ttu-id="f31ba-162">Les paramètres de lien de fichier et de dossier par défaut déterminent l’option de lien qui est présentée par défaut à l’utilisateur lorsqu’il partage un fichier ou un dossier.</span><span class="sxs-lookup"><span data-stu-id="f31ba-162">The default file and folder link settings determine which link option is shown to the user by default when they share a file or folder.</span></span> <span data-ttu-id="f31ba-163">Les utilisateurs peuvent remplacer le type de lien par l’une des autres options avant de procéder au partage si vous le souhaitez.</span><span class="sxs-lookup"><span data-stu-id="f31ba-163">Users can change the link type to one of the other options before sharing if desired.</span></span>

<span data-ttu-id="f31ba-164">N’oubliez pas que ce paramètre affecte toutes les équipes et tous les sites SharePoint de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="f31ba-164">Keep in mind that this setting affects all teams and SharePoint sites in your organization.</span></span>

<span data-ttu-id="f31ba-165">Choisissez le type de lien sélectionné par défaut lorsque les utilisateurs partagent des fichiers et des dossiers :</span><span class="sxs-lookup"><span data-stu-id="f31ba-165">Choose the type of link that's selected by default when users share files and folders:</span></span>

- <span data-ttu-id="f31ba-166">**Toute personne disposant du lien** : choisissez cette option si vous envisagez d’effectuer beaucoup de partage non authentifié de fichiers et de dossiers.</span><span class="sxs-lookup"><span data-stu-id="f31ba-166">**Anyone with the link** - Choose this option if you expect to do a lot of unauthenticated sharing of files and folders.</span></span> <span data-ttu-id="f31ba-167">Si vous souhaitez autoriser *tout le monde* à se lier, mais que vous êtes préoccupé par le partage non authentifié accidentel, envisagez l’une des autres options par défaut.</span><span class="sxs-lookup"><span data-stu-id="f31ba-167">If you want to allow *Anyone* links but are concerned about accidental unauthenticated sharing, consider one of the other options as the default.</span></span> <span data-ttu-id="f31ba-168">Ce type de lien n’est disponible que si vous avez activé le partage d’un **utilisateur** .</span><span class="sxs-lookup"><span data-stu-id="f31ba-168">This link type is only available if you've enabled **Anyone** sharing.</span></span>
- <span data-ttu-id="f31ba-169">**Uniquement les personnes de votre organisation** : choisissez cette option si vous pensez que le partage de fichiers et de dossiers doit être associé à des personnes au sein de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="f31ba-169">**Only people in your organization** - Choose this option if you expect most file and folder sharing to be with people inside your organization.</span></span>
- <span data-ttu-id="f31ba-170">**Personnes spécifiques** : envisagez cette option si vous envisagez de faire beaucoup de partage de fichiers et de dossiers avec des invités.</span><span class="sxs-lookup"><span data-stu-id="f31ba-170">**Specific people** - Consider this option if you expect to do a lot of file and folder sharing with guests.</span></span> <span data-ttu-id="f31ba-171">Ce type de lien fonctionne avec les invités et les requiert pour s’authentifier.</span><span class="sxs-lookup"><span data-stu-id="f31ba-171">This type of link works with guests and requires them to authenticate.</span></span>
 
![Capture d’écran des paramètres de partage de fichiers et dossiers au niveau de l’organisation dans SharePoint](../media/sharepoint-organization-files-folders-sharing-settings.png)


<span data-ttu-id="f31ba-173">Pour définir les paramètres de liaison par défaut au niveau de l’organisation SharePoint</span><span class="sxs-lookup"><span data-stu-id="f31ba-173">To set the SharePoint organization level default link settings</span></span>

1. <span data-ttu-id="f31ba-174">Accédez à la page de partage dans le centre d’administration SharePoint.</span><span class="sxs-lookup"><span data-stu-id="f31ba-174">Navigate to the Sharing page in the SharePoint admin center.</span></span>
2. <span data-ttu-id="f31ba-175">Sous **liens de fichiers et de dossiers**, sélectionnez le lien de partage par défaut à utiliser.</span><span class="sxs-lookup"><span data-stu-id="f31ba-175">Under **File and folder links**, select the default sharing link that you want to use.</span></span>
3. <span data-ttu-id="f31ba-176">Si vous avez effectué des modifications, cliquez sur **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="f31ba-176">If you made changes, click **Save**.</span></span>

## <a name="create-a-team"></a><span data-ttu-id="f31ba-177">Créer une équipe</span><span class="sxs-lookup"><span data-stu-id="f31ba-177">Create a team</span></span>

<span data-ttu-id="f31ba-178">L’étape suivante consiste à créer l’équipe que vous envisagez d’utiliser pour collaborer avec des invités.</span><span class="sxs-lookup"><span data-stu-id="f31ba-178">The next step is to create the team that you plan to use for collaborating with guests.</span></span>

<span data-ttu-id="f31ba-179">Pour créer une équipe</span><span class="sxs-lookup"><span data-stu-id="f31ba-179">To create a team</span></span>
1. <span data-ttu-id="f31ba-180">Dans Teams, sous l’onglet **teams** , cliquez sur **rejoindre ou créer une équipe** en bas du volet de gauche.</span><span class="sxs-lookup"><span data-stu-id="f31ba-180">In Teams, on the **Teams** tab, click **Join or create a team** at the bottom of the left pane.</span></span>
2. <span data-ttu-id="f31ba-181">Cliquez sur **créer une équipe**.</span><span class="sxs-lookup"><span data-stu-id="f31ba-181">Click **Create a team**.</span></span>
3. <span data-ttu-id="f31ba-182">Cliquez sur **créer une équipe de toutes pièces**.</span><span class="sxs-lookup"><span data-stu-id="f31ba-182">Click **Build a team from scratch**.</span></span>
4. <span data-ttu-id="f31ba-183">Choisissez **privé** ou **public**.</span><span class="sxs-lookup"><span data-stu-id="f31ba-183">Choose **Private** or **Public**.</span></span>
5. <span data-ttu-id="f31ba-184">Tapez un nom et une description pour l’équipe, puis cliquez sur **créer**.</span><span class="sxs-lookup"><span data-stu-id="f31ba-184">Type a name and description for the team, and then click **Create**.</span></span>
6. <span data-ttu-id="f31ba-185">Cliquez sur **Ignorer**.</span><span class="sxs-lookup"><span data-stu-id="f31ba-185">Click **Skip**.</span></span>

<span data-ttu-id="f31ba-186">Nous allons inviter les utilisateurs ultérieurement.</span><span class="sxs-lookup"><span data-stu-id="f31ba-186">We'll invite users later.</span></span> <span data-ttu-id="f31ba-187">Ensuite, il est important de vérifier les paramètres de partage au niveau du site pour le site SharePoint qui est associé à l’équipe.</span><span class="sxs-lookup"><span data-stu-id="f31ba-187">Next, it's important to check the site-level sharing settings for the SharePoint site that is associated with the team.</span></span>

## <a name="sharepoint-site-level-sharing-settings"></a><span data-ttu-id="f31ba-188">Paramètres de partage au niveau du site SharePoint</span><span class="sxs-lookup"><span data-stu-id="f31ba-188">SharePoint site level sharing settings</span></span>

<span data-ttu-id="f31ba-189">Vérifiez les paramètres de partage au niveau du site pour vous assurer qu’ils autorisent le type d’accès que vous souhaitez pour cette équipe.</span><span class="sxs-lookup"><span data-stu-id="f31ba-189">Check the site-level sharing settings to make sure that they allow the type of access that you want for this team.</span></span> <span data-ttu-id="f31ba-190">Par exemple, si vous définissez les paramètres au niveau de l’organisation sur tous les **utilisateurs**, mais que vous souhaitez que tous les invités s’authentifient pour cette équipe, assurez-vous que les paramètres de partage au niveau du site sont définis sur **nouveaux et invités existants**.</span><span class="sxs-lookup"><span data-stu-id="f31ba-190">For example, if you set the organization-level settings to **Anyone**, but you want all guests to authenticate for this team, then make sure the site-level sharing settings are set to **New and existing guests**.</span></span>

![Capture d’écran des paramètres de partage externe de site SharePoint](../media/sharepoint-site-external-sharing-settings.png)


<span data-ttu-id="f31ba-192">Pour définir les paramètres de partage au niveau du site</span><span class="sxs-lookup"><span data-stu-id="f31ba-192">To set site-level sharing settings</span></span>
1. <span data-ttu-id="f31ba-193">Dans le centre d’administration SharePoint, dans le volet de navigation de gauche, développez **Sites** et cliquez sur **Sites actifs**.</span><span class="sxs-lookup"><span data-stu-id="f31ba-193">In the SharePoint admin center, in the left navigation, expand **Sites** and click **Active sites**.</span></span>
2. <span data-ttu-id="f31ba-194">Sélectionnez le site de l’équipe que vous venez de créer.</span><span class="sxs-lookup"><span data-stu-id="f31ba-194">Select the site for the team that you just created.</span></span>
3. <span data-ttu-id="f31ba-195">Dans le ruban, cliquez sur **Partage**. </span><span class="sxs-lookup"><span data-stu-id="f31ba-195">In the ribbon, click **Sharing**.</span></span>
4. <span data-ttu-id="f31ba-196">Assurez-vous que le partage est défini sur **tout le monde** ou sur **des invités nouveaux et existants**.</span><span class="sxs-lookup"><span data-stu-id="f31ba-196">Ensure that sharing is set to **Anyone** or **New and existing guests**.</span></span>
5. <span data-ttu-id="f31ba-197">Si vous avez effectué des modifications, cliquez sur **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="f31ba-197">If you made changes, click **Save**.</span></span>

## <a name="invite-users"></a><span data-ttu-id="f31ba-198">Inviter des utilisateurs</span><span class="sxs-lookup"><span data-stu-id="f31ba-198">Invite users</span></span>

<span data-ttu-id="f31ba-199">Les paramètres de partage des invités sont désormais configurés, de sorte que vous pouvez commencer à ajouter des utilisateurs et des invités internes à votre équipe.</span><span class="sxs-lookup"><span data-stu-id="f31ba-199">Guest sharing settings are now configured, so you can start adding internal users and guests to your team.</span></span> 

<span data-ttu-id="f31ba-200">Pour inviter des utilisateurs internes à une équipe</span><span class="sxs-lookup"><span data-stu-id="f31ba-200">To invite internal users to a team</span></span>
1. <span data-ttu-id="f31ba-201">Dans l’équipe, cliquez sur plus d'**\*\*** **options** (), puis sur **Ajouter un membre**.</span><span class="sxs-lookup"><span data-stu-id="f31ba-201">In the team, click **More options** (**\*\*\***), and then click **Add member**.</span></span>
2. <span data-ttu-id="f31ba-202">Tapez le nom de la personne que vous souhaitez inviter.</span><span class="sxs-lookup"><span data-stu-id="f31ba-202">Type the name of the person who you want to invite.</span></span>
3. <span data-ttu-id="f31ba-203">Cliquez sur **Ajouter**, puis sur **Fermer**.</span><span class="sxs-lookup"><span data-stu-id="f31ba-203">Click **Add**, and then click **Close**.</span></span>

<span data-ttu-id="f31ba-204">Pour inviter des invités à une équipe</span><span class="sxs-lookup"><span data-stu-id="f31ba-204">To invite guests to a team</span></span>
1. <span data-ttu-id="f31ba-205">Dans l’équipe, cliquez sur plus d'**\*\*** **options** (), puis sur **Ajouter un membre**.</span><span class="sxs-lookup"><span data-stu-id="f31ba-205">In the team, click **More options** (**\*\*\***), and then click **Add member**.</span></span>
2. <span data-ttu-id="f31ba-206">Tapez l’adresse de messagerie de l’invité que vous souhaitez inviter.</span><span class="sxs-lookup"><span data-stu-id="f31ba-206">Type the email address of the guest who you want to invite.</span></span>
3. <span data-ttu-id="f31ba-207">Cliquez sur **modifier les informations invité**.</span><span class="sxs-lookup"><span data-stu-id="f31ba-207">Click **Edit guest information**.</span></span>
4. <span data-ttu-id="f31ba-208">Tapez le nom complet de l’invité et cliquez sur la coche.</span><span class="sxs-lookup"><span data-stu-id="f31ba-208">Type the guest's full name and click the check mark.</span></span>
5. <span data-ttu-id="f31ba-209">Cliquez sur **Ajouter**, puis sur **Fermer**.</span><span class="sxs-lookup"><span data-stu-id="f31ba-209">Click **Add**, and then click **Close**.</span></span>

## <a name="see-also"></a><span data-ttu-id="f31ba-210">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f31ba-210">See Also</span></span>

[<span data-ttu-id="f31ba-211">Meilleures pratiques relatives au partage de fichiers et de dossiers avec des utilisateurs non authentifiés</span><span class="sxs-lookup"><span data-stu-id="f31ba-211">Best practices for sharing files and folders with unauthenticated users</span></span>](best-practices-anonymous-sharing.md)

[<span data-ttu-id="f31ba-212">Limiter l’exposition accidentelle aux fichiers lors du partage avec des invités</span><span class="sxs-lookup"><span data-stu-id="f31ba-212">Limit accidental exposure to files when sharing with guests</span></span>](share-limit-accidental-exposure.md)

[<span data-ttu-id="f31ba-213">Créer un environnement de partage sécurisé avec des invités</span><span class="sxs-lookup"><span data-stu-id="f31ba-213">Create a secure guest sharing environment</span></span>](create-secure-guest-sharing-environment.md)

[<span data-ttu-id="f31ba-214">Créer un extranet B2B avec des invités gérés</span><span class="sxs-lookup"><span data-stu-id="f31ba-214">Create a B2B extranet with managed guests</span></span>](b2b-extranet.md)
