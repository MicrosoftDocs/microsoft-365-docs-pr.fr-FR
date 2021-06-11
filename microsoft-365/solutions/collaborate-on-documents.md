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
recommendations: false
description: Dans cet article, vous allez découvrir comment collaborer avec des invités sur un document SharePoint et OneDrive.
ms.openlocfilehash: 338c7f32944bccb766ed923c12a9fceee4d81db8
ms.sourcegitcommit: f780de91bc00caeb1598781e0076106c76234bad
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/19/2021
ms.locfileid: "52537834"
---
# <a name="collaborate-with-guests-on-a-document"></a><span data-ttu-id="ba4ef-103">Collaborer avec des invités sur un document</span><span class="sxs-lookup"><span data-stu-id="ba4ef-103">Collaborate with guests on a document</span></span>

<span data-ttu-id="ba4ef-104">Si vous devez collaborer avec des personnes extérieures à votre organisation sur des documents dans SharePoint ou OneDrive, vous pouvez leur envoyer un lien de partage vers le document.</span><span class="sxs-lookup"><span data-stu-id="ba4ef-104">If you need to collaborate with people outside your organization on documents in SharePoint or OneDrive, you can send them a sharing-link to the document.</span></span> <span data-ttu-id="ba4ef-105">Dans cet article, nous allons passer en revue les étapes de configuration Microsoft 365 nécessaires pour configurer des liens de partage pour SharePoint et OneDrive pour les besoins de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="ba4ef-105">In this article, we'll walk through the Microsoft 365 configuration steps necessary to set up sharing-links for SharePoint and OneDrive for the needs of your organization.</span></span>

## <a name="video-demonstration"></a><span data-ttu-id="ba4ef-106">Démonstration vidéo</span><span class="sxs-lookup"><span data-stu-id="ba4ef-106">Video demonstration</span></span>

<span data-ttu-id="ba4ef-107">Cette vidéo décrit les étapes de configuration décrites dans ce document.</span><span class="sxs-lookup"><span data-stu-id="ba4ef-107">This video shows the configuration steps described in this document.</span></span></br>

> [!VIDEO https://www.microsoft.com/videoplayer/embed/RE450Vt?autoplay=false]

## <a name="azure-external-collaboration-settings"></a><span data-ttu-id="ba4ef-108">Paramètres de collaboration externe Azure</span><span class="sxs-lookup"><span data-stu-id="ba4ef-108">Azure external collaboration settings</span></span>

<span data-ttu-id="ba4ef-109">Le partage dans Microsoft 365 est régi à son niveau le plus élevé par les [paramètres de collaboration externe B2B dans Azure Active Directory](/azure/active-directory/external-identities/delegate-invitations).</span><span class="sxs-lookup"><span data-stu-id="ba4ef-109">Sharing in Microsoft 365 is governed at its highest level by the [B2B external collaboration settings in Azure Active Directory](/azure/active-directory/external-identities/delegate-invitations).</span></span> <span data-ttu-id="ba4ef-110">Si le partage d’invités est désactivé ou restreint dans Azure AD, ce paramètre remplace tous les paramètres de partage que vous configurez dans Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="ba4ef-110">If guest-sharing is disabled or restricted in Azure AD, this setting overrides any sharing settings that you configure in Microsoft 365.</span></span>

<span data-ttu-id="ba4ef-111">Vérifiez les paramètres de collaboration externe B2B pour vous assurer que le partage avec des invités n’est pas bloqué.</span><span class="sxs-lookup"><span data-stu-id="ba4ef-111">Check the B2B external collaboration settings to ensure that sharing with guests is not blocked.</span></span>

![Capture d’écran de la page des paramètres de relations organisationnelles d’Azure Active Directory](../media/azure-ad-organizational-relationships-settings.png)

<span data-ttu-id="ba4ef-113">Pour définir les paramètres de collaboration externe</span><span class="sxs-lookup"><span data-stu-id="ba4ef-113">To set external collaboration settings</span></span>

1. <span data-ttu-id="ba4ef-114">Connectez-vous à Azure Active Directory sur [https://aad.portal.azure.com](https://aad.portal.azure.com).</span><span class="sxs-lookup"><span data-stu-id="ba4ef-114">Log in to Azure Active Directory at [https://aad.portal.azure.com](https://aad.portal.azure.com).</span></span>
2. <span data-ttu-id="ba4ef-115">Dans le volet de navigation gauche, cliquez sur **Azure Active Directory**.</span><span class="sxs-lookup"><span data-stu-id="ba4ef-115">In the left navigation pane, click **Azure Active Directory**.</span></span>
3. <span data-ttu-id="ba4ef-116">Cliquez sur **Identités externes**.</span><span class="sxs-lookup"><span data-stu-id="ba4ef-116">Click **External identities**.</span></span>
4. <span data-ttu-id="ba4ef-117">Dans l’écran **Prise en main**, dans le volet de navigation gauche, cliquez sur **Paramètres de collaboration externe**.</span><span class="sxs-lookup"><span data-stu-id="ba4ef-117">On the **Get started** screen, in the left navigation pane, click **External collaboration settings**.</span></span>
5. <span data-ttu-id="ba4ef-118">Assurez-vous que **Les administrateurs et les utilisateurs membres du rôle Inviteur d’invités peuvent envoyer des invitations** et **Les membres peuvent inviter** sont tous deux définis sur **Oui**.</span><span class="sxs-lookup"><span data-stu-id="ba4ef-118">Ensure that **Admins and users in the guest inviter role can invite** and **Members can invite** are both set to **Yes**.</span></span>
6. <span data-ttu-id="ba4ef-119">Si vous avez effectué des modifications, cliquez sur **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="ba4ef-119">If you made changes, click **Save**.</span></span>

<span data-ttu-id="ba4ef-120">Notez les paramètres dans la section **Restrictions de collaboration**.</span><span class="sxs-lookup"><span data-stu-id="ba4ef-120">Note the settings in the **Collaboration restrictions** section.</span></span> <span data-ttu-id="ba4ef-121">Assurez-vous que les domaines des invités avec qui vous voulez collaborer ne sont pas bloqués.</span><span class="sxs-lookup"><span data-stu-id="ba4ef-121">Make sure that the domains of the guests that you want to collaborate with aren't blocked.</span></span>

<span data-ttu-id="ba4ef-122">Si vous travaillez avec des invités de plusieurs organisations, vous souhaiterez peut-être restreindre leur capacité à accéder aux données d’annuaire.</span><span class="sxs-lookup"><span data-stu-id="ba4ef-122">If you work with guests from multiple organizations, you may want to restrict their ability to access directory data.</span></span> <span data-ttu-id="ba4ef-123">Cela les empêche de voir qui d’autre est invité dans l’annuaire.</span><span class="sxs-lookup"><span data-stu-id="ba4ef-123">This will prevent them from seeing who else is a guest in the directory.</span></span> <span data-ttu-id="ba4ef-124">Pour ce faire, sous **Restrictions d’accès des utilisateurs invités**, sélectionnez **Les utilisateurs invités ont un accès limité aux propriétés et à l’appartenance aux paramètres des objets d’annuaire** ou **L’accès des utilisateurs invités est limité aux propriétés et à l’appartenance à leurs propres objets d’annuaire**.</span><span class="sxs-lookup"><span data-stu-id="ba4ef-124">To do this, under **Guest user access restrictions**, select **Guest users have limited access to properties and membership of directory objects settings** or **Guest user access is restricted to properties and memberships of their own directory objects**.</span></span>

## <a name="sharepoint-organization-level-sharing-settings"></a><span data-ttu-id="ba4ef-125">SharePoint de partage au niveau de l’organisation</span><span class="sxs-lookup"><span data-stu-id="ba4ef-125">SharePoint organization-level sharing settings</span></span>

<span data-ttu-id="ba4ef-126">Pour que les personnes extérieures à votre organisation ont accès à un document en SharePoint ou OneDrive, les paramètres de partage au niveau de l’organisation SharePoint et OneDrive doivent autoriser le partage avec des personnes extérieures à votre organisation.</span><span class="sxs-lookup"><span data-stu-id="ba4ef-126">In order for people outside your organization to have access to a document in SharePoint or OneDrive, the SharePoint and OneDrive organization-level sharing settings must allow for sharing with people outside your organization.</span></span>

<span data-ttu-id="ba4ef-127">Les paramètres au niveau de l’SharePoint déterminent les paramètres qui seront disponibles pour les sites SharePoint individuels.</span><span class="sxs-lookup"><span data-stu-id="ba4ef-127">The organization-level settings for SharePoint determine the settings that will be available for individual SharePoint sites.</span></span> <span data-ttu-id="ba4ef-128">Les paramètres de site ne peuvent pas être plus permissifs que les paramètres au niveau de l’organisation.</span><span class="sxs-lookup"><span data-stu-id="ba4ef-128">Site settings cannot be more permissive than the organization-level settings.</span></span> <span data-ttu-id="ba4ef-129">Le paramètre au niveau de l’OneDrive détermine le niveau de partage qui sera disponible dans les bibliothèques OneDrive utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="ba4ef-129">The organization-level setting for OneDrive determines the level of sharing that will be available in users' OneDrive libraries.</span></span>

<span data-ttu-id="ba4ef-130">Pour SharePoint et OneDrive, si vous souhaitez autoriser le partage de fichiers et de dossiers non authentifiés, choisissez Tout le **monde.**</span><span class="sxs-lookup"><span data-stu-id="ba4ef-130">For SharePoint and OneDrive, if you want to allow unauthenticated file and folder sharing, choose **Anyone**.</span></span> <span data-ttu-id="ba4ef-131">Si vous souhaitez vous assurer que les personnes extérieures à votre organisation doivent s’authentifier, choisissez Invités nouveaux **et existants.**</span><span class="sxs-lookup"><span data-stu-id="ba4ef-131">If you want to ensure that people outside your organization have to authenticate, choose **New and existing guests**.</span></span> <span data-ttu-id="ba4ef-132">*Les* liens tout le monde sont le moyen le plus simple de partager : les personnes extérieures à votre organisation peuvent ouvrir le lien sans authentification et sont libres de le transmettre à d’autres personnes.</span><span class="sxs-lookup"><span data-stu-id="ba4ef-132">*Anyone* links is the easiest way to share: people outside your organization can open the link without authentication and are free to pass it on to others.</span></span>

<span data-ttu-id="ba4ef-133">Pour SharePoint, choisissez le paramètre le plus permissif qui sera nécessaire à n’importe quel site de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="ba4ef-133">For SharePoint, choose the most permissive setting that will be needed by any site in your organization.</span></span>

![Capture d’écran des paramètres de partage SharePoint au niveau de l’organisation](../media/sharepoint-organization-external-sharing-controls.png)


<span data-ttu-id="ba4ef-135">Pour définir les paramètres de partage SharePoint au niveau de l’organisation</span><span class="sxs-lookup"><span data-stu-id="ba4ef-135">To set SharePoint organization-level sharing settings</span></span>

1. <span data-ttu-id="ba4ef-136">Dans le Centre d’administration Microsoft 365, dans le volet de navigation gauche, sous **Centres d’administration**, cliquez sur **SharePoint**.</span><span class="sxs-lookup"><span data-stu-id="ba4ef-136">In the Microsoft 365 admin center, in the left navigation pane, under **Admin centers**, click **SharePoint**.</span></span>
2. <span data-ttu-id="ba4ef-137">Dans le SharePoint d’administration, dans le volet de navigation de gauche, sous **Stratégies,** cliquez sur **Partage.**</span><span class="sxs-lookup"><span data-stu-id="ba4ef-137">In the SharePoint admin center, in the left navigation pane, under **Policies**, click **Sharing**.</span></span>
3. <span data-ttu-id="ba4ef-138">Assurez-vous que le partage externe pour SharePoint ou OneDrive est définie sur **Tout** le monde ou Nouveau **et les invités existants.**</span><span class="sxs-lookup"><span data-stu-id="ba4ef-138">Ensure that external sharing for SharePoint or OneDrive is set to **Anyone** or **New and existing guests**.</span></span> <span data-ttu-id="ba4ef-139">(Notez que le paramètre OneDrive ne peut pas être plus permissif que le SharePoint paramètre.)</span><span class="sxs-lookup"><span data-stu-id="ba4ef-139">(Note that the OneDrive setting cannot be more permissive than the SharePoint setting.)</span></span>
4. <span data-ttu-id="ba4ef-140">Si vous avez effectué des modifications, cliquez sur **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="ba4ef-140">If you made changes, click **Save**.</span></span>

## <a name="sharepoint-organization-level-default-link-settings"></a><span data-ttu-id="ba4ef-141">Paramètres de liaison par défaut au niveau de l’organisation SharePoint</span><span class="sxs-lookup"><span data-stu-id="ba4ef-141">SharePoint organization-level default link settings</span></span>

<span data-ttu-id="ba4ef-142">Les paramètres par défaut de liaison de fichier et de dossier déterminent l’option de lien qui sera affichée par défaut aux utilisateurs lorsqu’ils partagent un fichier ou un dossier.</span><span class="sxs-lookup"><span data-stu-id="ba4ef-142">The default file and folder link settings determine the link option that will be shown to users by default when they share a file or folder.</span></span> <span data-ttu-id="ba4ef-143">Si vous le souhaitez, les utilisateurs peuvent modifier le type de lien vers l’une des autres options avant le partage.</span><span class="sxs-lookup"><span data-stu-id="ba4ef-143">Users can change the link type to one of the other options before sharing, if desired.</span></span>

<span data-ttu-id="ba4ef-144">N’oubliez pas que ce paramètre affecte SharePoint sites de votre organisation, ainsi que les OneDrive.</span><span class="sxs-lookup"><span data-stu-id="ba4ef-144">Keep in mind that this setting affects SharePoint sites in your organization, as well as OneDrive.</span></span>

<span data-ttu-id="ba4ef-145">Choisissez un lien parmi les types suivants, qui est ensuite sélectionné par défaut lorsque les utilisateurs partagent des fichiers et des dossiers :</span><span class="sxs-lookup"><span data-stu-id="ba4ef-145">Choose a link from any of the following types which is then selected by default when users share files and folders:</span></span>

- <span data-ttu-id="ba4ef-146">**Toute personne partageant le lien** : choisissez cette option si vous prévoyez d’avoir un grand nombre de partages de fichiers et de dossiers non authentifiés.</span><span class="sxs-lookup"><span data-stu-id="ba4ef-146">**Anyone with the link** - Choose this option if you expect to do a lot of unauthenticated file and folder sharing.</span></span> <span data-ttu-id="ba4ef-147">Si vous souhaitez autoriser les liens à *Tout le monde* mais que vous craignez un partage accidentel non authentifié, envisagez l'une des autres options comme valeur par défaut.</span><span class="sxs-lookup"><span data-stu-id="ba4ef-147">If you want to allow *Anyone* links but are concerned about accidental unauthenticated sharing, consider one of the other options as the default.</span></span> <span data-ttu-id="ba4ef-148">Ce type de lien n’est disponible que si vous avez activé le partage **Tout le monde**.</span><span class="sxs-lookup"><span data-stu-id="ba4ef-148">This link type is only available if you've enabled **Anyone** sharing.</span></span>
- <span data-ttu-id="ba4ef-149">**Uniquement les personnes de votre organisation** : choisissez cette option si vous souhaitez que la plupart des partages de fichiers et de dossiers soient avec des personnes de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="ba4ef-149">**Only people in your organization** - Choose this option if you expect most file and folder sharing to be with people inside your organization.</span></span>
- <span data-ttu-id="ba4ef-150">**Personnes spécifiques** : envisagez cette option si vous prévoyez de partager beaucoup de fichiers et de dossiers avec vos invités.</span><span class="sxs-lookup"><span data-stu-id="ba4ef-150">**Specific people** - Consider this option if you expect to do a lot of file and folder sharing with guests.</span></span> <span data-ttu-id="ba4ef-151">Ce type de lien fonctionne avec les invités et exige leur authentification.</span><span class="sxs-lookup"><span data-stu-id="ba4ef-151">This type of link works with guests and requires them to authenticate.</span></span>
 
![Capture d’écran des paramètres de partage de fichiers et dossiers au niveau de l’organisation dans SharePoint](../media/sharepoint-organization-files-folders-sharing-settings.png)


<span data-ttu-id="ba4ef-153">Pour définir les paramètres SharePoint et OneDrive paramètres de lien par défaut au niveau de l’organisation</span><span class="sxs-lookup"><span data-stu-id="ba4ef-153">To set the SharePoint and OneDrive organization-level default link settings</span></span>

1. <span data-ttu-id="ba4ef-154">Accédez à la page Partage dans le Centre d’administration SharePoint.</span><span class="sxs-lookup"><span data-stu-id="ba4ef-154">Navigate to the Sharing page in the SharePoint admin center.</span></span>
2. <span data-ttu-id="ba4ef-155">Sous **Liens des fichiers et des dossiers**, sélectionnez le lien de partage par défaut que vous voulez utiliser.</span><span class="sxs-lookup"><span data-stu-id="ba4ef-155">Under **File and folder links**, select the default sharing link that you want to use.</span></span>
3. <span data-ttu-id="ba4ef-156">Si vous avez effectué des modifications, cliquez sur **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="ba4ef-156">If you made changes, click **Save**.</span></span>

<span data-ttu-id="ba4ef-157">Pour définir l’autorisation pour le lien de partage, sous **Choisir l’autorisation** sélectionnée par défaut pour le partage de liens.</span><span class="sxs-lookup"><span data-stu-id="ba4ef-157">To set the permission for the sharing link, under **Choose the permission that's selected by default for sharing links.**</span></span>

1. <span data-ttu-id="ba4ef-158">Sélectionnez **Afficher** si vous ne souhaitez pas que les utilisateurs non authentifiés modifient les fichiers et dossiers.</span><span class="sxs-lookup"><span data-stu-id="ba4ef-158">Select **View** if you do not want unauthenticated users to make changes to the files and folders.</span></span>
2. <span data-ttu-id="ba4ef-159">Sélectionnez **Modifier** si vous souhaitez autoriser les utilisateurs non authentifiés à apporter des modifications aux fichiers et dossiers.</span><span class="sxs-lookup"><span data-stu-id="ba4ef-159">Select **Edit** if you want to allow unauthenticated users to make changes to the files and folders.</span></span>

<span data-ttu-id="ba4ef-160">Notez que les deux options de prémission ci-dessus peuvent être appliquées non seulement pour les invités/utilisateurs externes, mais également pour les utilisateurs internes.</span><span class="sxs-lookup"><span data-stu-id="ba4ef-160">Note that the above two premission-options can be applied not only for guests/external users but also for internal users.</span></span> <span data-ttu-id="ba4ef-161">L’option d’autorisation que vous choisissez est déterminée par la discrétion.</span><span class="sxs-lookup"><span data-stu-id="ba4ef-161">The permission-option you choose is determined by self-discretion.</span></span>

<span data-ttu-id="ba4ef-162">Pour définir des autorisations pour les liens qui autorisent le partage avec tout le monde</span><span class="sxs-lookup"><span data-stu-id="ba4ef-162">To set permissions for links that allow sharing with anyone</span></span>

1. <span data-ttu-id="ba4ef-163">Sous ces **liens, vous pouvez accorder ces autorisations :** sous-volet,</span><span class="sxs-lookup"><span data-stu-id="ba4ef-163">Under the **These links can give these permissions:** sub-pane,</span></span> 
    1. <span data-ttu-id="ba4ef-164">À partir **de la** liste de listes de listes</span><span class="sxs-lookup"><span data-stu-id="ba4ef-164">From the **Files** drop-down list,</span></span> 
        - <span data-ttu-id="ba4ef-165">Sélectionnez **Afficher et modifier** si vous souhaitez autoriser les utilisateurs non authentifiés à apporter des modifications aux fichiers.</span><span class="sxs-lookup"><span data-stu-id="ba4ef-165">Select **View and edit** if you want to allow unauthenticated users to make changes to the files.</span></span>
        - <span data-ttu-id="ba4ef-166">Sélectionnez **Afficher** si vous ne souhaitez pas que les utilisateurs non authentifiés modifient les fichiers.</span><span class="sxs-lookup"><span data-stu-id="ba4ef-166">Select **View** if you do not want unauthenticated users to make changes to the files.</span></span>
    2. <span data-ttu-id="ba4ef-167">À partir de la liste de listes de **dossiers,**</span><span class="sxs-lookup"><span data-stu-id="ba4ef-167">From the **Folders** drop-down list,</span></span>
        - <span data-ttu-id="ba4ef-168">Sélectionnez **Afficher, modifier et charger** si vous souhaitez autoriser les utilisateurs non authentifiés à apporter des modifications aux dossiers.</span><span class="sxs-lookup"><span data-stu-id="ba4ef-168">Select **View, edit, and upload** if you want to allow unauthenticated users to make changes to the folders.</span></span>
        - <span data-ttu-id="ba4ef-169">Sélectionnez **Afficher** si vous ne souhaitez pas que les utilisateurs non authentifiés modifient les dossiers.</span><span class="sxs-lookup"><span data-stu-id="ba4ef-169">Select **View** if you do not want unauthenticated users to make changes to the folders.</span></span>

## <a name="sharepoint-site-level-sharing-settings"></a><span data-ttu-id="ba4ef-170">Paramètres de SharePoint au niveau du site</span><span class="sxs-lookup"><span data-stu-id="ba4ef-170">SharePoint site-level sharing settings</span></span>

<span data-ttu-id="ba4ef-171">Si vous partagez des fichiers et des dossiers situés dans un site SharePoint, vous devez également vérifier les paramètres de partage au niveau du site pour ce site.</span><span class="sxs-lookup"><span data-stu-id="ba4ef-171">If you're sharing files and folders that are in a SharePoint site, you also need to check the site-level sharing settings for that site.</span></span>

![Capture d’écran des paramètres de partage externe de site SharePoint](../media/sharepoint-site-external-sharing-settings.png)

<span data-ttu-id="ba4ef-173">Pour définir les paramètres au niveau du site</span><span class="sxs-lookup"><span data-stu-id="ba4ef-173">To set site-level sharing settings</span></span>

1. <span data-ttu-id="ba4ef-174">Dans le centre d’administration SharePoint, dans le volet de navigation de gauche, développez **Sites** et cliquez sur **Sites actifs**.</span><span class="sxs-lookup"><span data-stu-id="ba4ef-174">In the SharePoint admin center, in the left navigation pane, expand **Sites** and click **Active sites**.</span></span>
2. <span data-ttu-id="ba4ef-175">Sélectionnez le site sur lequel vous souhaitez partager des fichiers et des dossiers avec des invités.</span><span class="sxs-lookup"><span data-stu-id="ba4ef-175">Select the site on which you want to share files and folders with guests.</span></span>
3. <span data-ttu-id="ba4ef-176">Faites défiler vers la droite la ligne (dans laquelle le site sélectionné est présent) et cliquez n’importe où dans la **colonne de partage** externe.</span><span class="sxs-lookup"><span data-stu-id="ba4ef-176">Scroll right across the row (in which the selected site is present) and click anywhere in the **External sharing** column.</span></span>
4. <span data-ttu-id="ba4ef-177">Dans la page qui s’insérait, cliquez sur **l’onglet Stratégies.**</span><span class="sxs-lookup"><span data-stu-id="ba4ef-177">From the page that pops up, click **Policies** tab.</span></span>
5. <span data-ttu-id="ba4ef-178">Sous le **volet de partage** externe, cliquez sur **Modifier.**</span><span class="sxs-lookup"><span data-stu-id="ba4ef-178">Under the **External sharing** pane, click **Edit**.</span></span>
6. <span data-ttu-id="ba4ef-179">Assurez-vous que le partage est paramétré sur **Tout le monde** ou **Invités nouveaux et existants**.</span><span class="sxs-lookup"><span data-stu-id="ba4ef-179">Ensure that sharing is set to **Anyone** or **New and existing guests**.</span></span>
7. <span data-ttu-id="ba4ef-180">Si vous avez effectué des modifications, cliquez sur **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="ba4ef-180">If you made changes, click **Save**.</span></span>

## <a name="invite-users"></a><span data-ttu-id="ba4ef-181">Inviter des utilisateurs</span><span class="sxs-lookup"><span data-stu-id="ba4ef-181">Invite users</span></span>

<span data-ttu-id="ba4ef-182">Les paramètres de partage d’invités sont désormais configurés ; afin que les utilisateurs peuvent désormais partager des fichiers et des dossiers avec des personnes extérieures à votre organisation.</span><span class="sxs-lookup"><span data-stu-id="ba4ef-182">Guest-sharing settings are now configured; so users can now share files and folders with people outside your organization.</span></span> <span data-ttu-id="ba4ef-183">Pour [plus d OneDrive,](https://support.office.com/article/9fcc2f7d-de0c-4cec-93b0-a82024800c07) voir Partager des fichiers et des dossiers et Partager SharePoint fichiers ou [dossiers.](https://support.office.com/article/1fe37332-0f9a-4719-970e-d2578da4941c)</span><span class="sxs-lookup"><span data-stu-id="ba4ef-183">See [Share OneDrive files and folders](https://support.office.com/article/9fcc2f7d-de0c-4cec-93b0-a82024800c07) and [Share SharePoint files or folders](https://support.office.com/article/1fe37332-0f9a-4719-970e-d2578da4941c) for more information.</span></span>

## <a name="see-also"></a><span data-ttu-id="ba4ef-184">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ba4ef-184">See also</span></span>

[<span data-ttu-id="ba4ef-185">Meilleures pratiques relatives au partage de fichiers et de dossiers avec des utilisateurs non authentifiés</span><span class="sxs-lookup"><span data-stu-id="ba4ef-185">Best practices for sharing files and folders with unauthenticated users</span></span>](best-practices-anonymous-sharing.md)

[<span data-ttu-id="ba4ef-186">Limiter l’exposition accidentelle aux fichiers lors du partage avec des invités</span><span class="sxs-lookup"><span data-stu-id="ba4ef-186">Limit accidental exposure to files when sharing with guests</span></span>](share-limit-accidental-exposure.md)

[<span data-ttu-id="ba4ef-187">Intégration de SharePoint et de OneDrive à Azure AD B2B</span><span class="sxs-lookup"><span data-stu-id="ba4ef-187">SharePoint and OneDrive integration with Azure AD B2B</span></span>](/sharepoint/sharepoint-azureb2b-integration-preview)