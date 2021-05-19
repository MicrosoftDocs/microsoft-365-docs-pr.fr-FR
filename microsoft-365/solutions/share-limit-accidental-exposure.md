---
title: Limiter l’exposition accidentelle
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
ms.custom: ''
localization_priority: Priority
f1.keywords: NOCSH
recommendations: false
description: Découvrez comment limiter l’exposition accidentelle des informations lorsque vous partagez des fichiers avec des personnes extérieures à votre organisation.
ms.openlocfilehash: aed567e503fb2c615b183c6769c69248c149742a
ms.sourcegitcommit: f780de91bc00caeb1598781e0076106c76234bad
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/19/2021
ms.locfileid: "52539046"
---
# <a name="limit-accidental-exposure-to-files-when-sharing-with-people-outside-your-organization"></a><span data-ttu-id="76550-103">Limiter l’exposition accidentelle de fichiers lors de partages avec des personnes extérieures à votre organisation</span><span class="sxs-lookup"><span data-stu-id="76550-103">Limit accidental exposure to files when sharing with people outside your organization</span></span>

<span data-ttu-id="76550-104">Lorsque vous partagez des fichiers et des dossiers avec des personnes extérieures à votre organisation, plusieurs options permettent de réduire les risques de partager accidentellement des informations sensibles.</span><span class="sxs-lookup"><span data-stu-id="76550-104">When sharing files and folders with people outside your organization, there are a variety of options to reduce the chances of accidentally sharing sensitive information.</span></span> <span data-ttu-id="76550-105">Vous pouvez choisir l’une des options de cet article pour répondre au mieux aux besoins de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="76550-105">You can choose from the options in this article to best meet the needs of your organization.</span></span>

## <a name="use-best-practices-for-anyone-links"></a><span data-ttu-id="76550-106">Utiliser les pratiques recommandées pour les liens Tout le monde</span><span class="sxs-lookup"><span data-stu-id="76550-106">Use best practices for Anyone links</span></span>

<span data-ttu-id="76550-107">Si des membres de votre organisation doivent effectuer un partage non authentifié, mais que vous êtes préoccupé par le fait que des personnes non authentifiées modifient du contenu, lisez les [meilleures pratiques relatives au partage anonyme](best-practices-anonymous-sharing.md) pour obtenir des instructions sur l’utilisation du partage non authentifié dans votre organisation.</span><span class="sxs-lookup"><span data-stu-id="76550-107">If people in your organization need to do unauthenticated sharing, but you're concerned about unauthenticated people modifying content, read [Best practices for unauthenticated sharing](best-practices-anonymous-sharing.md) for guidance on how to work with unauthenticated sharing in your organization.</span></span>

## <a name="turn-off-anyone-links"></a><span data-ttu-id="76550-108">Désactiver les liens Tout le monde</span><span class="sxs-lookup"><span data-stu-id="76550-108">Turn off Anyone links</span></span>

<span data-ttu-id="76550-109">Nous vous recommandons de laisser les liens *Tout le monde* activés pour le contenu approprié parce qu’il s’agit de la manière la plus simple de partager des documents et de réduire le risque que des utilisateurs recherchent d’autres solutions en dehors du contrôle de votre service informatique.</span><span class="sxs-lookup"><span data-stu-id="76550-109">We recommend leaving *Anyone* links enabled for appropriate content because it's the easiest way to share and can help reduce the risk of users seeking other solutions that are outside the control of your IT department.</span></span> <span data-ttu-id="76550-110">Les liens *Tout le monde* peuvent être transférés à d’autres personnes mais l’accès aux fichiers est disponible uniquement pour les personnes qui dispose du lien.</span><span class="sxs-lookup"><span data-stu-id="76550-110">*Anyone* links can be forwarded to others, but file access is only available to those who have the link.</span></span>

<span data-ttu-id="76550-111">Si vous voulez toujours que les personnes extérieures à votre organisation s’authentifient lors de l’accès au contenu dans SharePoint, les groupes ou Teams, vous pouvez désactiver le partage *Tout le monde*.</span><span class="sxs-lookup"><span data-stu-id="76550-111">If you always want people outside your organization to authenticate when accessing content in SharePoint, Groups, or Teams, you can turn off *Anyone* sharing.</span></span> <span data-ttu-id="76550-112">Cela permet d’éviter que les utilisateurs ne partagent le même contenu.</span><span class="sxs-lookup"><span data-stu-id="76550-112">This will prevent users from unauthenticated sharing of content.</span></span>

<span data-ttu-id="76550-113">Si vous désactivez les liens *Tout le monde*, les utilisateurs peuvent tout de même partager facilement du contenu avec des invités à l’aide de liens *Personnes spécifiques*.</span><span class="sxs-lookup"><span data-stu-id="76550-113">If you disable *Anyone* links, users can still easily share with guests using *Specific people* links.</span></span> <span data-ttu-id="76550-114">Dans ce cas, toutes les personnes extérieures à votre organisation devront s’authentifier avant de pouvoir accéder au contenu partagé.</span><span class="sxs-lookup"><span data-stu-id="76550-114">In this case, all people outside your organization will be required to authenticate before they can access the shared content.</span></span>

<span data-ttu-id="76550-115">Selon vos besoins, vous pouvez désactiver les liens *Tout le monde* vers des sites spécifiques ou pour l’ensemble de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="76550-115">Depending on your needs, you can disable *Anyone* links for specific sites, or for your whole organization.</span></span>

<span data-ttu-id="76550-116">Pour désactiver les liens *Tout le monde* de votre organisation</span><span class="sxs-lookup"><span data-stu-id="76550-116">To turn off *Anyone* links for your organization</span></span>
1. <span data-ttu-id="76550-117">Dans le centre d’administration SharePoint, dans le volet de gauche, cliquez sur **Partage**.</span><span class="sxs-lookup"><span data-stu-id="76550-117">In the SharePoint admin center, in the left navigation, click **Sharing**.</span></span>
2. <span data-ttu-id="76550-118">Définissez les paramètres de partage externe de SharePoint sur **Invités nouveaux et existants**.</span><span class="sxs-lookup"><span data-stu-id="76550-118">Set the SharePoint external sharing settings to **New and existing guests**.</span></span>

   ![Capture d’écran des paramètres de partage externe de site SharePoint au niveau de l’organisation](../media/sharepoint-organization-external-sharing-controls-new-users.png)

3. <span data-ttu-id="76550-120">Cliquez sur **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="76550-120">Click **Save**.</span></span>

<span data-ttu-id="76550-121">Pour désactiver les liens *Tout le monde* d’un site</span><span class="sxs-lookup"><span data-stu-id="76550-121">To turn off *Anyone* links for a site</span></span>
1. <span data-ttu-id="76550-122">Dans le centre d’administration SharePoint, dans le volet de navigation de gauche, développez **Sites** et cliquez sur **Sites actifs**.</span><span class="sxs-lookup"><span data-stu-id="76550-122">In the SharePoint admin center, in the left navigation, expand **Sites** and click **Active sites**.</span></span>
2. <span data-ttu-id="76550-123">Sélectionnez sur le site à configurer.</span><span class="sxs-lookup"><span data-stu-id="76550-123">Select the site that you want to configure.</span></span>
3. <span data-ttu-id="76550-124">Dans le ruban, cliquez sur **Partage**. </span><span class="sxs-lookup"><span data-stu-id="76550-124">In the ribbon, click **Sharing**.</span></span>
4. <span data-ttu-id="76550-125">Assurez-vous que le partage est paramétré sur **Invités nouveaux et existants**.</span><span class="sxs-lookup"><span data-stu-id="76550-125">Ensure that sharing is set to **New and existing guests**.</span></span>

   ![Capture d’écran des paramètres de partage externe de site SharePoint au niveau de l’organisation](../media/sharepoint-site-external-sharing-settings.png)

5. <span data-ttu-id="76550-127">Si vous avez effectué des modifications, cliquez sur **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="76550-127">If you made changes, click **Save**.</span></span>

## <a name="domain-filtering"></a><span data-ttu-id="76550-128">Filtrage de domaines</span><span class="sxs-lookup"><span data-stu-id="76550-128">Domain filtering</span></span>

<span data-ttu-id="76550-129">Vous pouvez utiliser des listes d’autorisation ou de refus de domaine pour spécifier les domaines que vos utilisateurs peuvent utiliser lors d’un partage avec des personnes extérieures à votre organisation.</span><span class="sxs-lookup"><span data-stu-id="76550-129">You can use domain allow or deny lists to specify which domains your users can use when sharing with people outside your organization.</span></span>

<span data-ttu-id="76550-130">Avec une liste d’autorisation, vous pouvez spécifier une liste de domaines sur lesquels les utilisateurs de votre organisation peuvent partager avec des personnes extérieures à votre organisation.</span><span class="sxs-lookup"><span data-stu-id="76550-130">With an allow list, you can specify a list of domains where users in your organization can share with people outside your organization.</span></span> <span data-ttu-id="76550-131">Le partage sur d’autres domaines est bloqué.</span><span class="sxs-lookup"><span data-stu-id="76550-131">Sharing with to other domains is blocked.</span></span> <span data-ttu-id="76550-132">Si votre organisation collabore avec des personnes uniquement à partir d’une liste de domaines spécifiques, vous pouvez utiliser cette fonctionnalité pour empêcher le partage avec d’autres domaines.</span><span class="sxs-lookup"><span data-stu-id="76550-132">If your organization only collaborates with people from a list of specific domains, you can use this feature to prevent sharing with other domains.</span></span>

<span data-ttu-id="76550-133">Avec une liste d’exclusion, vous pouvez spécifier une liste de domaines à partir desquels les utilisateurs de votre organisation ne peuvent pas partager avec des personnes extérieures à votre organisation.</span><span class="sxs-lookup"><span data-stu-id="76550-133">With a deny list, you can specify a list of domains from which users in your organization cannot share with people outside your organization.</span></span> <span data-ttu-id="76550-134">Le partage avec ces domaines listés est bloqué.</span><span class="sxs-lookup"><span data-stu-id="76550-134">Sharing with the listed domains is blocked.</span></span> <span data-ttu-id="76550-135">Cela peut s’avérer utile si vous avez des concurrents, par exemple, à qui vous souhaitez empêcher d’accéder à du contenu au sein de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="76550-135">This can be useful if you have competitors, for example, who you want to prevent from accessing content in your organization.</span></span>

<span data-ttu-id="76550-136">Les listes d’autorisation et de refus n’affectent que le partage avec des invités.</span><span class="sxs-lookup"><span data-stu-id="76550-136">The allow and deny lists only affect sharing with guests.</span></span> <span data-ttu-id="76550-137">Les utilisateurs peuvent toujours partager du contenu avec des personnes de domaines interdits en utilisant les liens *Tout le monde* si vous ne les avez pas désactivés.</span><span class="sxs-lookup"><span data-stu-id="76550-137">Users can still share with people from prohibited domains by using *Anyone* links if you haven't disabled them.</span></span> <span data-ttu-id="76550-138">Pour des résultats optimaux avec les listes d’autorisation et de refus de domaine, prévoyez de désactiver les liens *Tout le monde*, comme décrit ci-dessus.</span><span class="sxs-lookup"><span data-stu-id="76550-138">For best results with domain allow and deny lists, consider disabling *Anyone* links as described above.</span></span>

<span data-ttu-id="76550-139">Pour configurer une liste d’autorisation ou de refus de domaine</span><span class="sxs-lookup"><span data-stu-id="76550-139">To set up a domain allow or deny list</span></span>
1. <span data-ttu-id="76550-140">Dans le centre d’administration SharePoint, dans le volet de gauche, cliquez sur **Partage**.</span><span class="sxs-lookup"><span data-stu-id="76550-140">In the SharePoint admin center, in the left navigation, click **Sharing**.</span></span>
2. <span data-ttu-id="76550-141">Sous **Paramètres avancés pour le partage externe**, cochez la case **Limiter le partage externe par domaine**.</span><span class="sxs-lookup"><span data-stu-id="76550-141">Under **Advanced settings for external sharing**, select the **Limit external sharing by domain** check box.</span></span>
3. <span data-ttu-id="76550-142">Cliquez sur **Ajouter des domaines**.</span><span class="sxs-lookup"><span data-stu-id="76550-142">Click **Add domains**.</span></span>
4. <span data-ttu-id="76550-143">Choisissez si vous voulez bloquer des domaines, indiquez les domaines, puis cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="76550-143">Select whether you want to block domains, type the domains, and click **OK**.</span></span>

   ![Capture d’écran du paramètre Limiter le partage externe de SharePoint](../media/sharepoint-sharing-block-domain.png)

5. <span data-ttu-id="76550-145">Cliquez sur **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="76550-145">Click **Save**.</span></span>

<span data-ttu-id="76550-146">Si vous voulez limiter le partage par domaine à un niveau plus élevé que SharePoint et OneDrive, vous pouvez [autoriser ou bloquer les invitations à des utilisateurs B2B d’organisations spécifiques](/azure/active-directory/b2b/allow-deny-list) dans Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="76550-146">If you want to limit sharing by domain at a higher level than SharePoint and OneDrive, you can [allow or block invitations to B2B users from specific organizations](/azure/active-directory/b2b/allow-deny-list) in Azure Active Directory.</span></span> <span data-ttu-id="76550-147">(Vous devez configurer [l’intégration de SharePoint et OneDrive avec Azure AD B2B (préversion)](/sharepoint/sharepoint-azureb2b-integration-preview) pour que ces paramètres affectent SharePoint et OneDrive.)</span><span class="sxs-lookup"><span data-stu-id="76550-147">(You must configure the [SharePoint and OneDrive integration with Azure AD B2B Preview](/sharepoint/sharepoint-azureb2b-integration-preview) for these settings to affect SharePoint and OneDrive.)</span></span>

## <a name="limit-sharing-of-files-folders-and-sites-with-people-outside-your-organization-to-specified-security-groups"></a><span data-ttu-id="76550-148">Limiter le partage de fichiers, de dossiers et de sites avec des personnes extérieures à votre organisation à des groupes de sécurité spécifiés</span><span class="sxs-lookup"><span data-stu-id="76550-148">Limit sharing of files, folders, and sites with people outside your organization to specified security groups</span></span>

<span data-ttu-id="76550-149">Vous pouvez limiter le partage de fichiers, de dossiers et de sites avec des personnes extérieures à votre organisation à des membres d’un groupe de sécurité spécifique.</span><span class="sxs-lookup"><span data-stu-id="76550-149">You can restrict sharing of files, folders, and sites with people outside your organization to members of a specific security group.</span></span> <span data-ttu-id="76550-150">Cette fonction est utile si vous voulez activer le partage externe, mais avec un flux de travail d’approbation ou un processus de demande.</span><span class="sxs-lookup"><span data-stu-id="76550-150">This is useful if you want to enable external sharing, but with an approval workflow or request process.</span></span> <span data-ttu-id="76550-151">Vous pouvez également demander à vos utilisateurs de suivre une formation avant d’être ajoutés au groupe de sécurité et d’être autorisés à partager en externe.</span><span class="sxs-lookup"><span data-stu-id="76550-151">Alternatively, you might require your users to complete a training course before they're added to the security group and are allowed to share externally.</span></span>

<span data-ttu-id="76550-152">Limiter le partage externe aux membres d’un groupe de sécurité</span><span class="sxs-lookup"><span data-stu-id="76550-152">To limit external sharing to members of a security group</span></span>
1. <span data-ttu-id="76550-153">Dans le [Centre d’administration SharePoint](https://admin.microsoft.com/sharepoint), dans le volet de gauche, sous **Stratégies**, cliquez sur **Partage**.</span><span class="sxs-lookup"><span data-stu-id="76550-153">In the [SharePoint admin center](https://admin.microsoft.com/sharepoint), in the left navigation, under **Policies**, click **Sharing**.</span></span>
2. <span data-ttu-id="76550-154">Sous **Partage externe**, développez **Autres paramètres de partage externe**.</span><span class="sxs-lookup"><span data-stu-id="76550-154">Under **External sharing**, expand **More external sharing settings**.</span></span>

3. <span data-ttu-id="76550-155">Sélectionnez **Autoriser uniquement les utilisateurs de groupes de sécurité spécifiques à partager en externe**, puis sélectionnez **Gérer les groupes de sécurité**.</span><span class="sxs-lookup"><span data-stu-id="76550-155">Select **Allow only users in specific security groups to share externally**, and then select **Manage security groups**.</span></span>

    ![Capture d’écran du volet Gérer les groupes de sécurité](/sharepoint/sharepointonline/media/manage-security-groups.png)

4. <span data-ttu-id="76550-157">Dans la zone **Ajouter un groupe de sécurité** , entrez un nom pour un groupe de sécurité.</span><span class="sxs-lookup"><span data-stu-id="76550-157">In the **Add a security group** box, enter a name for a security group.</span></span> <span data-ttu-id="76550-158">La boîte de dialogue du groupe de sécurité s’affiche.</span><span class="sxs-lookup"><span data-stu-id="76550-158">The security group box appears.</span></span>

5. <span data-ttu-id="76550-159">En regard du nom du groupe de sécurité, dans le menu déroulant **Peut partager avec**, sélectionnez l’une des options suivantes :</span><span class="sxs-lookup"><span data-stu-id="76550-159">Next to the security group name, from the **Can share with** dropdown, select either:</span></span>

    - <span data-ttu-id="76550-160">**Invités authentifiés uniquement** (par défaut)</span><span class="sxs-lookup"><span data-stu-id="76550-160">**Authenticated guests only** (default)</span></span>
    - <span data-ttu-id="76550-161">**Tout le monde**</span><span class="sxs-lookup"><span data-stu-id="76550-161">**Anyone**</span></span>

6. <span data-ttu-id="76550-162">Sélectionnez **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="76550-162">Select **Save**.</span></span>

<span data-ttu-id="76550-163">Notez que cela affecte les fichiers, dossiers et sites, mais pas les groupes Microsoft 365 ou Teams.</span><span class="sxs-lookup"><span data-stu-id="76550-163">Note that this affects files, folders, and sites, but not Microsoft 365 groups or Teams.</span></span> <span data-ttu-id="76550-164">Lorsque les membres acceptent des invités dans un groupe Microsoft 365 privé ou une équipe privée dans Microsoft Teams, l’invitation est envoyée au groupe ou au propriétaire de l’équipe pour approbation.</span><span class="sxs-lookup"><span data-stu-id="76550-164">When members invite guests to a private Microsoft 365 group or a private team in Microsoft Teams, the invitation is sent to the group or team owner for approval.</span></span>

## <a name="see-also"></a><span data-ttu-id="76550-165">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="76550-165">See Also</span></span>

[<span data-ttu-id="76550-166">Créer un environnement de partage sécurisé avec des invités</span><span class="sxs-lookup"><span data-stu-id="76550-166">Create a secure guest sharing environment</span></span>](create-secure-guest-sharing-environment.md)

[<span data-ttu-id="76550-167">Meilleures pratiques relatives au partage de fichiers et de dossiers avec des utilisateurs anonymes</span><span class="sxs-lookup"><span data-stu-id="76550-167">Best practices for sharing files and folders with anonymous users</span></span>](best-practices-anonymous-sharing.md)