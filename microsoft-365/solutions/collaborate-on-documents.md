---
title: Collaborer avec des invités sur un document
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
description: Dans cet article, vous allez apprendre à collaborer avec des invités sur un document dans SharePoint et OneDrive.
ms.openlocfilehash: 98eea8fe9c613aef3e24f9e4bb6746ddc9a527ab
ms.sourcegitcommit: 445b249a6f0420b32e49742fd7744006c7090b2b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/18/2020
ms.locfileid: "46798269"
---
# <a name="collaborate-with-guests-on-a-document"></a><span data-ttu-id="89164-103">Collaborer avec des invités sur un document</span><span class="sxs-lookup"><span data-stu-id="89164-103">Collaborate with guests on a document</span></span>

<span data-ttu-id="89164-104">Si vous devez collaborer avec des personnes extérieures à votre organisation sur des documents dans SharePoint ou OneDrive, vous pouvez leur envoyer un lien de partage vers le document.</span><span class="sxs-lookup"><span data-stu-id="89164-104">If you need to collaborate with people outside your organization on documents in SharePoint or OneDrive, you can send them a sharing link to the document.</span></span> <span data-ttu-id="89164-105">Dans cet article, nous allons passer en revue les étapes de configuration de Microsoft 365 requises pour configurer des liens de partage pour SharePoint et OneDrive pour les besoins de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="89164-105">In this article, we'll walk through the Microsoft 365 configuration steps necessary to set up sharing links for SharePoint and OneDrive for the needs of your organization.</span></span>

## <a name="video-demonstration"></a><span data-ttu-id="89164-106">Démonstration vidéo</span><span class="sxs-lookup"><span data-stu-id="89164-106">Video demonstration</span></span>

<span data-ttu-id="89164-107">Cette vidéo présente les étapes de configuration décrites dans ce document.</span><span class="sxs-lookup"><span data-stu-id="89164-107">This video shows the configuration steps described in this document.</span></span></br>

> [!VIDEO https://www.microsoft.com/videoplayer/embed/RE450Vt?autoplay=false]

## <a name="azure-organizational-relationships-settings"></a><span data-ttu-id="89164-108">Paramètres Azure de relations organisationnelles</span><span class="sxs-lookup"><span data-stu-id="89164-108">Azure Organizational relationships settings</span></span>

<span data-ttu-id="89164-109">Le partage dans Microsoft 365 est régi par les [paramètres de relations organisationnelles dans Azure Active Directory](https://docs.microsoft.com/azure/active-directory/external-identities/delegate-invitations).</span><span class="sxs-lookup"><span data-stu-id="89164-109">Sharing in Microsoft 365 is governed at its highest level by the [organizational relationships settings in Azure Active Directory](https://docs.microsoft.com/azure/active-directory/external-identities/delegate-invitations).</span></span> <span data-ttu-id="89164-110">Si le partage d’invités est désactivé ou restreint dans Azure AD, cela remplace tous les paramètres de partage que vous configurez dans Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="89164-110">If guest sharing is disabled or restricted in Azure AD, this will override any sharing settings that you configure in Microsoft 365.</span></span>

<span data-ttu-id="89164-111">Vérifiez les paramètres de relations organisationnelles pour vous assurer que le partage avec des invités n’est pas bloqué.</span><span class="sxs-lookup"><span data-stu-id="89164-111">Check the organizational relationships settings to ensure that sharing with guests is not blocked.</span></span>

![Capture d’écran de la page des paramètres de relations organisationnelles d’Azure Active Directory](../media/azure-ad-organizational-relationships-settings.png)

<span data-ttu-id="89164-113">Pour définir les paramètres de relation organisationnelle</span><span class="sxs-lookup"><span data-stu-id="89164-113">To set organizational relationship settings</span></span>

1. <span data-ttu-id="89164-114">Connectez-vous à Microsoft Azure à l’adresse [https://portal.azure.com](https://portal.azure.com) .</span><span class="sxs-lookup"><span data-stu-id="89164-114">Log in to Microsoft Azure at [https://portal.azure.com](https://portal.azure.com).</span></span>
2. <span data-ttu-id="89164-115">Dans le volet de navigation de gauche, cliquez sur **Azure Active Directory**.</span><span class="sxs-lookup"><span data-stu-id="89164-115">In the left navigation, click **Azure Active Directory**.</span></span>
3. <span data-ttu-id="89164-116">Dans le volet de **vue d’ensemble** , cliquez sur **relations organisationnelles**.</span><span class="sxs-lookup"><span data-stu-id="89164-116">In the **Overview** pane, click **Organizational relationships**.</span></span>
4. <span data-ttu-id="89164-117">Dans le volet **relations organisationnelles** , cliquez sur **paramètres**.</span><span class="sxs-lookup"><span data-stu-id="89164-117">In the **Organizational relationships** pane, click **Settings**.</span></span>
5. <span data-ttu-id="89164-118">Assurez-vous que les **administrateurs et les utilisateurs du rôle d’invité invité peuvent inviter** et que les **membres peuvent inviter** sont tous deux la valeur **Oui**.</span><span class="sxs-lookup"><span data-stu-id="89164-118">Ensure that **Admins and users in the guest inviter role can invite** and **Members can invite** are both set to **Yes**.</span></span>
6. <span data-ttu-id="89164-119">Si vous avez effectué des modifications, cliquez sur **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="89164-119">If you made changes, click **Save**.</span></span>

<span data-ttu-id="89164-120">Notez les paramètres dans la section **restrictions de collaboration** .</span><span class="sxs-lookup"><span data-stu-id="89164-120">Note the settings in the **Collaboration restrictions** section.</span></span> <span data-ttu-id="89164-121">Assurez-vous que les domaines des invités avec lesquels vous souhaitez collaborer ne sont pas bloqués.</span><span class="sxs-lookup"><span data-stu-id="89164-121">Make sure that the domains of the guests that you want to collaborate with aren't blocked.</span></span>

<span data-ttu-id="89164-122">Si vous travaillez avec des invités de plusieurs organisations, vous souhaiterez peut-être limiter leur capacité à accéder aux données d’annuaire.</span><span class="sxs-lookup"><span data-stu-id="89164-122">If you work with guests from multiple organizations, you may want to restrict their ability to access directory data.</span></span> <span data-ttu-id="89164-123">Cela les empêchera de voir qui d’autre est un invité dans l’annuaire.</span><span class="sxs-lookup"><span data-stu-id="89164-123">This will prevent them from seeing who else is a guest in the directory.</span></span> <span data-ttu-id="89164-124">Pour ce faire, sous **restrictions d’accès des utilisateurs invités**, sélectionnez **les utilisateurs invités ont un accès limité aux propriétés et l’appartenance aux paramètres d’objets d’annuaire** ou **l’accès des utilisateurs invités est limité aux propriétés et aux appartenances de leurs propres objets d’annuaire**.</span><span class="sxs-lookup"><span data-stu-id="89164-124">To do this, under **Guest user access restrictions**, select **Guest users have limited access to properties and membership of directory objects settings** or **Guest user access is restricted to properties and memberships of their own directory objects**.</span></span>

## <a name="sharepoint-organization-level-sharing-settings"></a><span data-ttu-id="89164-125">Paramètres de partage au niveau de l’organisation SharePoint</span><span class="sxs-lookup"><span data-stu-id="89164-125">SharePoint organization level sharing settings</span></span>

<span data-ttu-id="89164-126">Pour que les personnes extérieures à votre organisation aient accès à un document dans SharePoint ou OneDrive, les paramètres de partage au niveau de l’organisation SharePoint et OneDrive doivent autoriser le partage avec des personnes extérieures à votre organisation.</span><span class="sxs-lookup"><span data-stu-id="89164-126">In order for people outside your organization to have access to a document in SharePoint or OneDrive, the SharePoint and OneDrive organization-level sharing settings must allow for sharing with people outside your organization.</span></span>

<span data-ttu-id="89164-127">Les paramètres au niveau de l’Organisation pour SharePoint déterminent les paramètres disponibles pour les sites SharePoint individuels.</span><span class="sxs-lookup"><span data-stu-id="89164-127">The organization-level settings for SharePoint determine what settings are available for individual SharePoint sites.</span></span> <span data-ttu-id="89164-128">Les paramètres de site ne peuvent pas être plus permissants que les paramètres au niveau de l’organisation.</span><span class="sxs-lookup"><span data-stu-id="89164-128">Site settings cannot be more permissive than the organization-level settings.</span></span> <span data-ttu-id="89164-129">Le paramètre au niveau de l’Organisation pour OneDrive détermine quel niveau de partage est disponible dans les bibliothèques OneDrive des utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="89164-129">The organization-level setting for OneDrive determines what level of sharing is available in users' OneDrive libraries.</span></span>

<span data-ttu-id="89164-130">Pour SharePoint et OneDrive, si vous voulez autoriser le partage de fichiers et de dossiers non authentifié, sélectionnez **tout le monde**.</span><span class="sxs-lookup"><span data-stu-id="89164-130">For SharePoint and OneDrive, if you want to allow unauthenticated file and folder sharing, choose **Anyone**.</span></span> <span data-ttu-id="89164-131">Si vous souhaitez vous assurer que les personnes extérieures à votre organisation doivent s’authentifier, choisissez **nouveau et invités existants**.</span><span class="sxs-lookup"><span data-stu-id="89164-131">If you want to ensure that people outside your organization have to authenticate, choose **New and existing guests**.</span></span> <span data-ttu-id="89164-132">Les liens *tout le monde* sont le moyen le plus simple de partager : les personnes extérieures à votre organisation peuvent ouvrir le lien sans authentification et être libres de le transmettre à d’autres personnes.</span><span class="sxs-lookup"><span data-stu-id="89164-132">*Anyone* links are the easiest way to share: people outside your organization can open the link without authentication and are free to pass it on to others.</span></span>

<span data-ttu-id="89164-133">Pour SharePoint, choisissez le paramètre le plus permissif qui sera nécessaire pour tous les sites de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="89164-133">For SharePoint, choose the most permissive setting that will be needed by any site in your organization.</span></span>

![Capture d’écran des paramètres de partage SharePoint au niveau de l’organisation](../media/sharepoint-organization-external-sharing-controls.png)


<span data-ttu-id="89164-135">Pour définir les paramètres de partage au niveau de l’organisation SharePoint</span><span class="sxs-lookup"><span data-stu-id="89164-135">To set SharePoint organization level sharing settings</span></span>

1. <span data-ttu-id="89164-136">Dans le centre d’administration 365 de Microsoft, dans le volet de navigation de gauche, sous **centres d’administration**, cliquez sur **SharePoint**.</span><span class="sxs-lookup"><span data-stu-id="89164-136">In the Microsoft 365 admin center, in the left navigation, under **Admin centers**, click **SharePoint**.</span></span>
2. <span data-ttu-id="89164-137">Dans le centre d’administration SharePoint, dans le volet de gauche, cliquez sur **Partage**.</span><span class="sxs-lookup"><span data-stu-id="89164-137">In the SharePoint admin center, in the left navigation, click **Sharing**.</span></span>
3. <span data-ttu-id="89164-138">Assurez-vous que le partage externe pour SharePoint ou OneDrive est défini sur **tout le monde** ou sur **des invités nouveaux et existants**.</span><span class="sxs-lookup"><span data-stu-id="89164-138">Ensure that external sharing for SharePoint or OneDrive is set to **Anyone** or **New and existing guests**.</span></span> <span data-ttu-id="89164-139">(Notez que le paramètre OneDrive ne peut pas être plus permissif que le paramètre SharePoint.)</span><span class="sxs-lookup"><span data-stu-id="89164-139">(Note that the OneDrive setting cannot be more permissive than the SharePoint setting.)</span></span>
4. <span data-ttu-id="89164-140">Si vous avez effectué des modifications, cliquez sur **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="89164-140">If you made changes, click **Save**.</span></span>

## <a name="sharepoint-organization-level-default-link-settings"></a><span data-ttu-id="89164-141">Paramètres de lien par défaut au niveau de l’organisation SharePoint</span><span class="sxs-lookup"><span data-stu-id="89164-141">SharePoint organization level default link settings</span></span>

<span data-ttu-id="89164-142">Les paramètres de lien de fichier et de dossier par défaut déterminent l’option de lien qui est présentée par défaut à l’utilisateur lorsqu’il partage un fichier ou un dossier.</span><span class="sxs-lookup"><span data-stu-id="89164-142">The default file and folder link settings determine which link option is shown to the user by default when they share a file or folder.</span></span> <span data-ttu-id="89164-143">Les utilisateurs peuvent remplacer le type de lien par l’une des autres options avant de procéder au partage si vous le souhaitez.</span><span class="sxs-lookup"><span data-stu-id="89164-143">Users can change the link type to one of the other options before sharing if desired.</span></span>

<span data-ttu-id="89164-144">N’oubliez pas que ce paramètre affecte les sites SharePoint de votre organisation, ainsi que OneDrive.</span><span class="sxs-lookup"><span data-stu-id="89164-144">Keep in mind that this setting affects SharePoint sites in your organization, as well as OneDrive.</span></span>

<span data-ttu-id="89164-145">Choisissez le type de lien sélectionné par défaut lorsque les utilisateurs partagent des fichiers et des dossiers :</span><span class="sxs-lookup"><span data-stu-id="89164-145">Choose the type of link that's selected by default when users share files and folders:</span></span>

- <span data-ttu-id="89164-146">**Toute personne disposant du lien** : choisissez cette option si vous envisagez d’effectuer beaucoup de partage de fichiers et de dossiers non authentifiés.</span><span class="sxs-lookup"><span data-stu-id="89164-146">**Anyone with the link** - Choose this option if you expect to do a lot of unauthenticated file and folder sharing.</span></span> <span data-ttu-id="89164-147">Si vous souhaitez autoriser *tout le monde* à se lier, mais que vous êtes préoccupé par le partage non authentifié accidentel, envisagez l’une des autres options par défaut.</span><span class="sxs-lookup"><span data-stu-id="89164-147">If you want to allow *Anyone* links but are concerned about accidental unauthenticated sharing, consider one of the other options as the default.</span></span> <span data-ttu-id="89164-148">Ce type de lien n’est disponible que si vous avez activé le partage d’un **utilisateur** .</span><span class="sxs-lookup"><span data-stu-id="89164-148">This link type is only available if you've enabled **Anyone** sharing.</span></span>
- <span data-ttu-id="89164-149">**Uniquement les personnes de votre organisation** : choisissez cette option si vous pensez que le partage de fichiers et de dossiers doit être associé à des personnes au sein de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="89164-149">**Only people in your organization** - Choose this option if you expect most file and folder sharing to be with people inside your organization.</span></span>
- <span data-ttu-id="89164-150">**Personnes spécifiques** : envisagez cette option si vous envisagez de faire beaucoup de partage de fichiers et de dossiers avec des invités.</span><span class="sxs-lookup"><span data-stu-id="89164-150">**Specific people** - Consider this option if you expect to do a lot of file and folder sharing with guests.</span></span> <span data-ttu-id="89164-151">Ce type de lien fonctionne avec les invités et les requiert pour s’authentifier.</span><span class="sxs-lookup"><span data-stu-id="89164-151">This type of link works with guests and requires them to authenticate.</span></span>
 
![Capture d’écran des paramètres de partage de fichiers et dossiers au niveau de l’organisation dans SharePoint](../media/sharepoint-organization-files-folders-sharing-settings.png)


<span data-ttu-id="89164-153">Pour définir les paramètres de lien par défaut de l’organisation OneDrive et SharePoint</span><span class="sxs-lookup"><span data-stu-id="89164-153">To set the SharePoint and OneDrive organization level default link settings</span></span>

1. <span data-ttu-id="89164-154">Accédez à la page de partage dans le centre d’administration SharePoint.</span><span class="sxs-lookup"><span data-stu-id="89164-154">Navigate to the Sharing page in the SharePoint admin center.</span></span>
2. <span data-ttu-id="89164-155">Sous **liens de fichiers et de dossiers**, sélectionnez le lien de partage par défaut à utiliser.</span><span class="sxs-lookup"><span data-stu-id="89164-155">Under **File and folder links**, select the default sharing link that you want to use.</span></span>
3. <span data-ttu-id="89164-156">Si vous avez effectué des modifications, cliquez sur **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="89164-156">If you made changes, click **Save**.</span></span>

## <a name="sharepoint-site-level-sharing-settings"></a><span data-ttu-id="89164-157">Paramètres de partage au niveau du site SharePoint</span><span class="sxs-lookup"><span data-stu-id="89164-157">SharePoint site level sharing settings</span></span>

<span data-ttu-id="89164-158">Si vous partagez des fichiers et des dossiers qui se trouvent dans un site SharePoint, vous devez également vérifier les paramètres de partage au niveau du site pour ce site.</span><span class="sxs-lookup"><span data-stu-id="89164-158">If you're sharing files and folders that are in a SharePoint site, you also need to check the site-level sharing settings for that site.</span></span>

![Capture d’écran des paramètres de partage externe de site SharePoint](../media/sharepoint-site-external-sharing-settings.png)

<span data-ttu-id="89164-160">Pour définir les paramètres de partage au niveau du site</span><span class="sxs-lookup"><span data-stu-id="89164-160">To set site-level sharing settings</span></span>
1. <span data-ttu-id="89164-161">Dans le centre d’administration SharePoint, dans le volet de navigation de gauche, développez **Sites** et cliquez sur **Sites actifs**.</span><span class="sxs-lookup"><span data-stu-id="89164-161">In the SharePoint admin center, in the left navigation, expand **Sites** and click **Active sites**.</span></span>
2. <span data-ttu-id="89164-162">Sélectionnez le site que vous venez de créer.</span><span class="sxs-lookup"><span data-stu-id="89164-162">Select the site that you just created.</span></span>
3. <span data-ttu-id="89164-163">Dans le ruban, cliquez sur **Partage**. </span><span class="sxs-lookup"><span data-stu-id="89164-163">In the ribbon, click **Sharing**.</span></span>
4. <span data-ttu-id="89164-164">Assurez-vous que le partage est défini sur **tout le monde** ou sur **des invités nouveaux et existants**.</span><span class="sxs-lookup"><span data-stu-id="89164-164">Ensure that sharing is set to **Anyone** or **New and existing guests**.</span></span>
5. <span data-ttu-id="89164-165">Si vous avez effectué des modifications, cliquez sur **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="89164-165">If you made changes, click **Save**.</span></span>

## <a name="invite-users"></a><span data-ttu-id="89164-166">Inviter des utilisateurs</span><span class="sxs-lookup"><span data-stu-id="89164-166">Invite users</span></span>

<span data-ttu-id="89164-167">Les paramètres de partage des invités sont désormais configurés, de sorte que les utilisateurs peuvent désormais partager des fichiers et des dossiers avec des personnes extérieures à votre organisation.</span><span class="sxs-lookup"><span data-stu-id="89164-167">Guest sharing settings are now configured, so users can now share files and folders with people outside your organization.</span></span> <span data-ttu-id="89164-168">Pour plus d’informations, voir [partager des fichiers et des dossiers OneDrive](https://support.office.com/article/9fcc2f7d-de0c-4cec-93b0-a82024800c07) et [partager des fichiers ou des dossiers SharePoint](https://support.office.com/article/1fe37332-0f9a-4719-970e-d2578da4941c) .</span><span class="sxs-lookup"><span data-stu-id="89164-168">See [Share OneDrive files and folders](https://support.office.com/article/9fcc2f7d-de0c-4cec-93b0-a82024800c07) and [Share SharePoint files or folders](https://support.office.com/article/1fe37332-0f9a-4719-970e-d2578da4941c) for more information.</span></span>

## <a name="see-also"></a><span data-ttu-id="89164-169">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="89164-169">See Also</span></span>

[<span data-ttu-id="89164-170">Meilleures pratiques relatives au partage de fichiers et de dossiers avec des utilisateurs non authentifiés</span><span class="sxs-lookup"><span data-stu-id="89164-170">Best practices for sharing files and folders with unauthenticated users</span></span>](best-practices-anonymous-sharing.md)

[<span data-ttu-id="89164-171">Limiter l’exposition accidentelle aux fichiers lors du partage avec des invités</span><span class="sxs-lookup"><span data-stu-id="89164-171">Limit accidental exposure to files when sharing with guests</span></span>](share-limit-accidental-exposure.md)
