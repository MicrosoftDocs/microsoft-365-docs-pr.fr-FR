---
title: Collaborer avec des invités sur un document
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
description: Dans cet article, vous allez apprendre à collaborer avec des invités sur un document dans SharePoint et OneDrive.
ms.openlocfilehash: 1b2fe003902b69e4c0c58852af67862ce6f2eb34
ms.sourcegitcommit: 47de4402174c263ae8d70c910ca068a7581d04ae
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "49663510"
---
# <a name="collaborate-with-guests-on-a-document"></a><span data-ttu-id="ee0d1-103">Collaborer avec des invités sur un document</span><span class="sxs-lookup"><span data-stu-id="ee0d1-103">Collaborate with guests on a document</span></span>

<span data-ttu-id="ee0d1-104">Si vous devez collaborer avec des personnes extérieures à votre organisation sur des documents dans SharePoint ou OneDrive, vous pouvez leur envoyer un lien de partage vers le document.</span><span class="sxs-lookup"><span data-stu-id="ee0d1-104">If you need to collaborate with people outside your organization on documents in SharePoint or OneDrive, you can send them a sharing-link to the document.</span></span> <span data-ttu-id="ee0d1-105">Dans cet article, nous allons passer en revue les étapes de configuration de Microsoft 365 requises pour configurer des liens de partage pour SharePoint et OneDrive pour les besoins de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="ee0d1-105">In this article, we'll walk through the Microsoft 365 configuration steps necessary to set up sharing-links for SharePoint and OneDrive for the needs of your organization.</span></span>

## <a name="video-demonstration"></a><span data-ttu-id="ee0d1-106">Démonstration vidéo</span><span class="sxs-lookup"><span data-stu-id="ee0d1-106">Video demonstration</span></span>

<span data-ttu-id="ee0d1-107">Cette vidéo présente les étapes de configuration décrites dans ce document.</span><span class="sxs-lookup"><span data-stu-id="ee0d1-107">This video shows the configuration steps described in this document.</span></span></br>

> [!VIDEO https://www.microsoft.com/videoplayer/embed/RE450Vt?autoplay=false]

## <a name="azure-external-collaboration-settings"></a><span data-ttu-id="ee0d1-108">Paramètres de collaboration externe Azure</span><span class="sxs-lookup"><span data-stu-id="ee0d1-108">Azure external collaboration settings</span></span>

<span data-ttu-id="ee0d1-109">Le partage dans Microsoft 365 est régi au niveau le plus élevé par les [paramètres de collaboration externe B2B dans Azure Active Directory](https://docs.microsoft.com/azure/active-directory/external-identities/delegate-invitations).</span><span class="sxs-lookup"><span data-stu-id="ee0d1-109">Sharing in Microsoft 365 is governed at its highest level by the [B2B external collaboration settings in Azure Active Directory](https://docs.microsoft.com/azure/active-directory/external-identities/delegate-invitations).</span></span> <span data-ttu-id="ee0d1-110">Si le partage d’invités est désactivé ou restreint dans Azure AD, ce paramètre remplace tous les paramètres de partage que vous configurez dans Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="ee0d1-110">If guest-sharing is disabled or restricted in Azure AD, this setting overrides any sharing settings that you configure in Microsoft 365.</span></span>

<span data-ttu-id="ee0d1-111">Vérifiez les paramètres de collaboration externe B2B pour vous assurer que le partage avec des invités n’est pas bloqué.</span><span class="sxs-lookup"><span data-stu-id="ee0d1-111">Check the B2B external collaboration settings to ensure that sharing with guests is not blocked.</span></span>

![Capture d’écran de la page des paramètres de relations organisationnelles d’Azure Active Directory](../media/azure-ad-organizational-relationships-settings.png)

<span data-ttu-id="ee0d1-113">Pour définir les paramètres de collaboration externe</span><span class="sxs-lookup"><span data-stu-id="ee0d1-113">To set external collaboration settings</span></span>

1. <span data-ttu-id="ee0d1-114">Connectez-vous à Azure Active Directory à l’adresse [https://aad.portal.azure.com](https://aad.portal.azure.com) .</span><span class="sxs-lookup"><span data-stu-id="ee0d1-114">Log in to Azure Active Directory at [https://aad.portal.azure.com](https://aad.portal.azure.com).</span></span>
2. <span data-ttu-id="ee0d1-115">Dans le volet de navigation de gauche, cliquez sur **Azure Active Directory**.</span><span class="sxs-lookup"><span data-stu-id="ee0d1-115">In the left navigation pane, click **Azure Active Directory**.</span></span>
3. <span data-ttu-id="ee0d1-116">Cliquez sur **identités externes**.</span><span class="sxs-lookup"><span data-stu-id="ee0d1-116">Click **External identities**.</span></span>
4. <span data-ttu-id="ee0d1-117">Sur l’écran de **prise en main** , dans le volet de navigation de gauche, cliquez sur **paramètres de collaboration externe**.</span><span class="sxs-lookup"><span data-stu-id="ee0d1-117">On the **Get started** screen, in the left navigation pane, click **External collaboration settings**.</span></span>
5. <span data-ttu-id="ee0d1-118">Assurez-vous que les **administrateurs et les utilisateurs du rôle d’invité invité peuvent inviter** et que les **membres peuvent inviter** sont tous deux la valeur **Oui**.</span><span class="sxs-lookup"><span data-stu-id="ee0d1-118">Ensure that **Admins and users in the guest inviter role can invite** and **Members can invite** are both set to **Yes**.</span></span>
6. <span data-ttu-id="ee0d1-119">Si vous avez effectué des modifications, cliquez sur **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="ee0d1-119">If you made changes, click **Save**.</span></span>

<span data-ttu-id="ee0d1-120">Notez les paramètres dans la section **restrictions de collaboration** .</span><span class="sxs-lookup"><span data-stu-id="ee0d1-120">Note the settings in the **Collaboration restrictions** section.</span></span> <span data-ttu-id="ee0d1-121">Assurez-vous que les domaines des invités avec lesquels vous souhaitez collaborer ne sont pas bloqués.</span><span class="sxs-lookup"><span data-stu-id="ee0d1-121">Make sure that the domains of the guests that you want to collaborate with aren't blocked.</span></span>

<span data-ttu-id="ee0d1-122">Si vous travaillez avec des invités de plusieurs organisations, vous souhaiterez peut-être limiter leur capacité à accéder aux données d’annuaire.</span><span class="sxs-lookup"><span data-stu-id="ee0d1-122">If you work with guests from multiple organizations, you may want to restrict their ability to access directory data.</span></span> <span data-ttu-id="ee0d1-123">Cela les empêchera de voir qui d’autre est un invité dans l’annuaire.</span><span class="sxs-lookup"><span data-stu-id="ee0d1-123">This will prevent them from seeing who else is a guest in the directory.</span></span> <span data-ttu-id="ee0d1-124">Pour ce faire, sous **restrictions d’accès des utilisateurs invités**, sélectionnez **les utilisateurs invités ont un accès limité aux propriétés et l’appartenance aux paramètres d’objets d’annuaire** ou **l’accès des utilisateurs invités est limité aux propriétés et aux appartenances de leurs propres objets d’annuaire**.</span><span class="sxs-lookup"><span data-stu-id="ee0d1-124">To do this, under **Guest user access restrictions**, select **Guest users have limited access to properties and membership of directory objects settings** or **Guest user access is restricted to properties and memberships of their own directory objects**.</span></span>

## <a name="sharepoint-organization-level-sharing-settings"></a><span data-ttu-id="ee0d1-125">Paramètres de partage au niveau de l’organisation SharePoint</span><span class="sxs-lookup"><span data-stu-id="ee0d1-125">SharePoint organization-level sharing settings</span></span>

<span data-ttu-id="ee0d1-126">Pour que les personnes extérieures à votre organisation aient accès à un document dans SharePoint ou OneDrive, les paramètres de partage au niveau de l’organisation SharePoint et OneDrive doivent autoriser le partage avec des personnes extérieures à votre organisation.</span><span class="sxs-lookup"><span data-stu-id="ee0d1-126">In order for people outside your organization to have access to a document in SharePoint or OneDrive, the SharePoint and OneDrive organization-level sharing settings must allow for sharing with people outside your organization.</span></span>

<span data-ttu-id="ee0d1-127">Les paramètres au niveau de l’Organisation pour SharePoint déterminent les paramètres qui seront disponibles pour les sites SharePoint individuels.</span><span class="sxs-lookup"><span data-stu-id="ee0d1-127">The organization-level settings for SharePoint determine the settings that will be available for individual SharePoint sites.</span></span> <span data-ttu-id="ee0d1-128">Les paramètres de site ne peuvent pas être plus permissants que les paramètres au niveau de l’organisation.</span><span class="sxs-lookup"><span data-stu-id="ee0d1-128">Site settings cannot be more permissive than the organization-level settings.</span></span> <span data-ttu-id="ee0d1-129">Le paramètre au niveau de l’Organisation pour OneDrive détermine le niveau de partage qui sera disponible dans les bibliothèques OneDrive des utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="ee0d1-129">The organization-level setting for OneDrive determines the level of sharing that will be available in users' OneDrive libraries.</span></span>

<span data-ttu-id="ee0d1-130">Pour SharePoint et OneDrive, si vous voulez autoriser le partage de fichiers et de dossiers non authentifié, sélectionnez **tout le monde**.</span><span class="sxs-lookup"><span data-stu-id="ee0d1-130">For SharePoint and OneDrive, if you want to allow unauthenticated file and folder sharing, choose **Anyone**.</span></span> <span data-ttu-id="ee0d1-131">Si vous souhaitez vous assurer que les personnes extérieures à votre organisation doivent s’authentifier, choisissez **nouveau et invités existants**.</span><span class="sxs-lookup"><span data-stu-id="ee0d1-131">If you want to ensure that people outside your organization have to authenticate, choose **New and existing guests**.</span></span> <span data-ttu-id="ee0d1-132">Les liens *tout le monde* constituent le moyen le plus simple de partager : les personnes extérieures à votre organisation peuvent ouvrir le lien sans authentification et être libres de le transmettre à d’autres personnes.</span><span class="sxs-lookup"><span data-stu-id="ee0d1-132">*Anyone* links is the easiest way to share: people outside your organization can open the link without authentication and are free to pass it on to others.</span></span>

<span data-ttu-id="ee0d1-133">Pour SharePoint, choisissez le paramètre le plus permissif qui sera nécessaire pour tous les sites de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="ee0d1-133">For SharePoint, choose the most permissive setting that will be needed by any site in your organization.</span></span>

![Capture d’écran des paramètres de partage SharePoint au niveau de l’organisation](../media/sharepoint-organization-external-sharing-controls.png)


<span data-ttu-id="ee0d1-135">Pour définir les paramètres de partage au niveau de l’organisation SharePoint</span><span class="sxs-lookup"><span data-stu-id="ee0d1-135">To set SharePoint organization-level sharing settings</span></span>

1. <span data-ttu-id="ee0d1-136">Dans le centre d’administration 365 de Microsoft, dans le volet de navigation de gauche, sous **centres d’administration**, cliquez sur **SharePoint**.</span><span class="sxs-lookup"><span data-stu-id="ee0d1-136">In the Microsoft 365 admin center, in the left navigation pane, under **Admin centers**, click **SharePoint**.</span></span>
2. <span data-ttu-id="ee0d1-137">Dans le centre d’administration SharePoint, dans le volet de navigation de gauche, sous **stratégies**, cliquez sur **partage**.</span><span class="sxs-lookup"><span data-stu-id="ee0d1-137">In the SharePoint admin center, in the left navigation pane, under **Policies**, click **Sharing**.</span></span>
3. <span data-ttu-id="ee0d1-138">Assurez-vous que le partage externe pour SharePoint ou OneDrive est défini sur **tout le monde** ou sur **des invités nouveaux et existants**.</span><span class="sxs-lookup"><span data-stu-id="ee0d1-138">Ensure that external sharing for SharePoint or OneDrive is set to **Anyone** or **New and existing guests**.</span></span> <span data-ttu-id="ee0d1-139">(Notez que le paramètre OneDrive ne peut pas être plus permissif que le paramètre SharePoint.)</span><span class="sxs-lookup"><span data-stu-id="ee0d1-139">(Note that the OneDrive setting cannot be more permissive than the SharePoint setting.)</span></span>
4. <span data-ttu-id="ee0d1-140">Si vous avez effectué des modifications, cliquez sur **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="ee0d1-140">If you made changes, click **Save**.</span></span>

## <a name="sharepoint-organization-level-default-link-settings"></a><span data-ttu-id="ee0d1-141">Paramètres de lien par défaut au niveau de l’organisation SharePoint</span><span class="sxs-lookup"><span data-stu-id="ee0d1-141">SharePoint organization-level default link settings</span></span>

<span data-ttu-id="ee0d1-142">Les paramètres de lien de fichier et de dossier par défaut déterminent l’option de lien qui apparaîtra par défaut aux utilisateurs lorsqu’ils partageront un fichier ou un dossier.</span><span class="sxs-lookup"><span data-stu-id="ee0d1-142">The default file and folder link settings determine the link option that will be shown to users by default when they share a file or folder.</span></span> <span data-ttu-id="ee0d1-143">Les utilisateurs peuvent remplacer le type de lien par l’une des autres options avant le partage, si vous le souhaitez.</span><span class="sxs-lookup"><span data-stu-id="ee0d1-143">Users can change the link type to one of the other options before sharing, if desired.</span></span>

<span data-ttu-id="ee0d1-144">N’oubliez pas que ce paramètre affecte les sites SharePoint de votre organisation, ainsi que OneDrive.</span><span class="sxs-lookup"><span data-stu-id="ee0d1-144">Keep in mind that this setting affects SharePoint sites in your organization, as well as OneDrive.</span></span>

<span data-ttu-id="ee0d1-145">Choisissez un lien de l’un des types suivants, qui est ensuite sélectionné par défaut lorsque les utilisateurs partagent des fichiers et des dossiers :</span><span class="sxs-lookup"><span data-stu-id="ee0d1-145">Choose a link from any of the following types which is then selected by default when users share files and folders:</span></span>

- <span data-ttu-id="ee0d1-146">**Toute personne disposant du lien** : choisissez cette option si vous envisagez d’effectuer beaucoup de partage de fichiers et de dossiers non authentifiés.</span><span class="sxs-lookup"><span data-stu-id="ee0d1-146">**Anyone with the link** - Choose this option if you expect to do a lot of unauthenticated file and folder sharing.</span></span> <span data-ttu-id="ee0d1-147">Si vous souhaitez autoriser *tout le monde* à se lier, mais que vous êtes préoccupé par le partage non authentifié accidentel, envisagez l’une des autres options par défaut.</span><span class="sxs-lookup"><span data-stu-id="ee0d1-147">If you want to allow *Anyone* links but are concerned about accidental unauthenticated sharing, consider one of the other options as the default.</span></span> <span data-ttu-id="ee0d1-148">Ce type de lien n’est disponible que si vous avez activé le partage d’un **utilisateur** .</span><span class="sxs-lookup"><span data-stu-id="ee0d1-148">This link type is only available if you've enabled **Anyone** sharing.</span></span>
- <span data-ttu-id="ee0d1-149">**Uniquement les personnes de votre organisation** : choisissez cette option si vous pensez que le partage de fichiers et de dossiers doit être associé à des personnes au sein de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="ee0d1-149">**Only people in your organization** - Choose this option if you expect most file and folder sharing to be with people inside your organization.</span></span>
- <span data-ttu-id="ee0d1-150">**Personnes spécifiques** : envisagez cette option si vous envisagez de faire beaucoup de partage de fichiers et de dossiers avec des invités.</span><span class="sxs-lookup"><span data-stu-id="ee0d1-150">**Specific people** - Consider this option if you expect to do a lot of file and folder sharing with guests.</span></span> <span data-ttu-id="ee0d1-151">Ce type de lien fonctionne avec les invités et les requiert pour s’authentifier.</span><span class="sxs-lookup"><span data-stu-id="ee0d1-151">This type of link works with guests and requires them to authenticate.</span></span>
 
![Capture d’écran des paramètres de partage de fichiers et dossiers au niveau de l’organisation dans SharePoint](../media/sharepoint-organization-files-folders-sharing-settings.png)


<span data-ttu-id="ee0d1-153">Pour définir les paramètres de lien par défaut au niveau de l’organisation SharePoint et OneDrive</span><span class="sxs-lookup"><span data-stu-id="ee0d1-153">To set the SharePoint and OneDrive organization-level default link settings</span></span>

1. <span data-ttu-id="ee0d1-154">Accédez à la page de partage dans le centre d’administration SharePoint.</span><span class="sxs-lookup"><span data-stu-id="ee0d1-154">Navigate to the Sharing page in the SharePoint admin center.</span></span>
2. <span data-ttu-id="ee0d1-155">Sous **liens de fichiers et de dossiers**, sélectionnez le lien de partage par défaut à utiliser.</span><span class="sxs-lookup"><span data-stu-id="ee0d1-155">Under **File and folder links**, select the default sharing link that you want to use.</span></span>
3. <span data-ttu-id="ee0d1-156">Si vous avez effectué des modifications, cliquez sur **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="ee0d1-156">If you made changes, click **Save**.</span></span>

<span data-ttu-id="ee0d1-157">Pour définir les autorisations pour le lien de partage, sous **Choisissez l’autorisation sélectionnée par défaut pour les liens de partage.**</span><span class="sxs-lookup"><span data-stu-id="ee0d1-157">To set the permission for the sharing link, under **Choose the permission that's selected by default for sharing links.**</span></span>

1. <span data-ttu-id="ee0d1-158">Sélectionnez **affichage** si vous ne souhaitez pas que les utilisateurs non authentifiés puissent modifier les fichiers et les dossiers.</span><span class="sxs-lookup"><span data-stu-id="ee0d1-158">Select **View** if you do not want unauthenticated users to make changes to the files and folders.</span></span>
2. <span data-ttu-id="ee0d1-159">Sélectionnez **modifier** si vous souhaitez autoriser les utilisateurs non authentifiés à apporter des modifications aux fichiers et aux dossiers.</span><span class="sxs-lookup"><span data-stu-id="ee0d1-159">Select **Edit** if you want to allow unauthenticated users to make changes to the files and folders.</span></span>

<span data-ttu-id="ee0d1-160">Notez que les deux options de prémission-ci-dessus peuvent être appliquées non seulement pour les utilisateurs invités/externes, mais aussi pour les utilisateurs internes.</span><span class="sxs-lookup"><span data-stu-id="ee0d1-160">Note that the above two premission-options can be applied not only for guests/external users but also for internal users.</span></span> <span data-ttu-id="ee0d1-161">L’option d’autorisation que vous choisissez est déterminée par auto-discrétion.</span><span class="sxs-lookup"><span data-stu-id="ee0d1-161">The permission-option you choose is determined by self-discretion.</span></span>

<span data-ttu-id="ee0d1-162">Pour définir des autorisations pour les liens qui permettent le partage avec d’autres personnes</span><span class="sxs-lookup"><span data-stu-id="ee0d1-162">To set permissions for links that allow sharing with anyone</span></span>

1. <span data-ttu-id="ee0d1-163">Sous le **lien ces liens peuvent donner les autorisations suivantes :** sous-volet,</span><span class="sxs-lookup"><span data-stu-id="ee0d1-163">Under the **These links can give these permissions:** sub-pane,</span></span> 
    1. <span data-ttu-id="ee0d1-164">Dans la liste déroulante **fichiers** ,</span><span class="sxs-lookup"><span data-stu-id="ee0d1-164">From the **Files** drop-down list,</span></span> 
        - <span data-ttu-id="ee0d1-165">Sélectionnez **afficher et modifier** si vous souhaitez autoriser les utilisateurs non authentifiés à apporter des modifications aux fichiers.</span><span class="sxs-lookup"><span data-stu-id="ee0d1-165">Select **View and edit** if you want to allow unauthenticated users to make changes to the files.</span></span>
        - <span data-ttu-id="ee0d1-166">Sélectionnez **affichage** si vous ne souhaitez pas que les utilisateurs non authentifiés puissent modifier les fichiers.</span><span class="sxs-lookup"><span data-stu-id="ee0d1-166">Select **View** if you do not want unauthenticated users to make changes to the files.</span></span>
    2. <span data-ttu-id="ee0d1-167">Dans la liste déroulante **dossiers** ,</span><span class="sxs-lookup"><span data-stu-id="ee0d1-167">From the **Folders** drop-down list,</span></span>
        - <span data-ttu-id="ee0d1-168">Sélectionnez **afficher, modifier et charger** si vous voulez autoriser les utilisateurs non authentifiés à apporter des modifications aux dossiers.</span><span class="sxs-lookup"><span data-stu-id="ee0d1-168">Select **View, edit, and upload** if you want to allow unauthenticated users to make changes to the folders.</span></span>
        - <span data-ttu-id="ee0d1-169">Sélectionnez **affichage** si vous ne souhaitez pas que les utilisateurs non authentifiés puissent modifier les dossiers.</span><span class="sxs-lookup"><span data-stu-id="ee0d1-169">Select **View** if you do not want unauthenticated users to make changes to the folders.</span></span>

## <a name="sharepoint-site-level-sharing-settings"></a><span data-ttu-id="ee0d1-170">Paramètres de partage au niveau du site SharePoint</span><span class="sxs-lookup"><span data-stu-id="ee0d1-170">SharePoint site-level sharing settings</span></span>

<span data-ttu-id="ee0d1-171">Si vous partagez des fichiers et des dossiers qui se trouvent dans un site SharePoint, vous devez également vérifier les paramètres de partage au niveau du site pour ce site.</span><span class="sxs-lookup"><span data-stu-id="ee0d1-171">If you're sharing files and folders that are in a SharePoint site, you also need to check the site-level sharing settings for that site.</span></span>

![Capture d’écran des paramètres de partage externe de site SharePoint](../media/sharepoint-site-external-sharing-settings.png)

<span data-ttu-id="ee0d1-173">Pour définir les paramètres de partage au niveau du site</span><span class="sxs-lookup"><span data-stu-id="ee0d1-173">To set site-level sharing settings</span></span>

1. <span data-ttu-id="ee0d1-174">Dans le centre d’administration SharePoint, dans le volet de navigation de gauche, développez **sites** , puis cliquez sur **sites actifs**.</span><span class="sxs-lookup"><span data-stu-id="ee0d1-174">In the SharePoint admin center, in the left navigation pane, expand **Sites** and click **Active sites**.</span></span>
2. <span data-ttu-id="ee0d1-175">Sélectionnez le site sur lequel vous souhaitez partager des fichiers et des dossiers avec des invités.</span><span class="sxs-lookup"><span data-stu-id="ee0d1-175">Select the site on which you want to share files and folders with guests.</span></span>
3. <span data-ttu-id="ee0d1-176">Faites défiler vers la droite sur la ligne (dans laquelle se trouve le site sélectionné), puis cliquez n’importe où dans la colonne de **partage externe** .</span><span class="sxs-lookup"><span data-stu-id="ee0d1-176">Scroll right across the row (in which the selected site is present) and click anywhere in the **External sharing** column.</span></span>
4. <span data-ttu-id="ee0d1-177">Dans la page qui s’affiche, cliquez sur l’onglet **stratégies** .</span><span class="sxs-lookup"><span data-stu-id="ee0d1-177">From the page that pops up, click **Policies** tab.</span></span>
5. <span data-ttu-id="ee0d1-178">Dans le volet **partage externe** , cliquez sur **modifier**.</span><span class="sxs-lookup"><span data-stu-id="ee0d1-178">Under the **External sharing** pane, click **Edit**.</span></span>
6. <span data-ttu-id="ee0d1-179">Assurez-vous que le partage est défini sur **tout le monde** ou sur **des invités nouveaux et existants**.</span><span class="sxs-lookup"><span data-stu-id="ee0d1-179">Ensure that sharing is set to **Anyone** or **New and existing guests**.</span></span>
7. <span data-ttu-id="ee0d1-180">Si vous avez effectué des modifications, cliquez sur **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="ee0d1-180">If you made changes, click **Save**.</span></span>

## <a name="invite-users"></a><span data-ttu-id="ee0d1-181">Inviter des utilisateurs</span><span class="sxs-lookup"><span data-stu-id="ee0d1-181">Invite users</span></span>

<span data-ttu-id="ee0d1-182">Les paramètres de partage d’invité sont désormais configurés ; les utilisateurs peuvent désormais partager des fichiers et des dossiers avec des personnes extérieures à votre organisation.</span><span class="sxs-lookup"><span data-stu-id="ee0d1-182">Guest-sharing settings are now configured; so users can now share files and folders with people outside your organization.</span></span> <span data-ttu-id="ee0d1-183">Pour plus d’informations, voir [partager des fichiers et des dossiers OneDrive](https://support.office.com/article/9fcc2f7d-de0c-4cec-93b0-a82024800c07) et [partager des fichiers ou des dossiers SharePoint](https://support.office.com/article/1fe37332-0f9a-4719-970e-d2578da4941c) .</span><span class="sxs-lookup"><span data-stu-id="ee0d1-183">See [Share OneDrive files and folders](https://support.office.com/article/9fcc2f7d-de0c-4cec-93b0-a82024800c07) and [Share SharePoint files or folders](https://support.office.com/article/1fe37332-0f9a-4719-970e-d2578da4941c) for more information.</span></span>

## <a name="see-also"></a><span data-ttu-id="ee0d1-184">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ee0d1-184">See also</span></span>

[<span data-ttu-id="ee0d1-185">Meilleures pratiques relatives au partage de fichiers et de dossiers avec des utilisateurs non authentifiés</span><span class="sxs-lookup"><span data-stu-id="ee0d1-185">Best practices for sharing files and folders with unauthenticated users</span></span>](best-practices-anonymous-sharing.md)

[<span data-ttu-id="ee0d1-186">Limiter l’exposition accidentelle aux fichiers lors du partage avec des invités</span><span class="sxs-lookup"><span data-stu-id="ee0d1-186">Limit accidental exposure to files when sharing with guests</span></span>](share-limit-accidental-exposure.md)

[<span data-ttu-id="ee0d1-187">Intégration de SharePoint et de OneDrive avec Azure AD B2B</span><span class="sxs-lookup"><span data-stu-id="ee0d1-187">SharePoint and OneDrive integration with Azure AD B2B</span></span>](https://docs.microsoft.com/sharepoint/sharepoint-azureb2b-integration-preview)
