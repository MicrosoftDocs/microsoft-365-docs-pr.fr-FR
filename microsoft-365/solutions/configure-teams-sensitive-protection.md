---
title: Configurer les équipes avec la protection des données sensibles
f1.keywords: NOCSH
ms.author: mikeplum
author: MikePlumleyMSFT
manager: serdars
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Priority
search.appverid:
- MET150
ms.collection:
- Ent_O365
- Strat_O365_Enterprise
- m365solution-3tiersprotection
- m365solution-securecollab
ms.custom:
- Ent_Solutions
recommendations: false
description: Découvrez comment déployer des équipes avec la protection des données sensibles.
ms.openlocfilehash: a3f715cb05ad1d5acf3c93c58959f12ebec46978
ms.sourcegitcommit: b09aee96a1e2266b33ba81dfe497f24c5300bb56
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/06/2021
ms.locfileid: "52788341"
---
# <a name="configure-teams-with-protection-for-sensitive-data"></a><span data-ttu-id="93c2b-103">Configurer les équipes avec la protection des données sensibles</span><span class="sxs-lookup"><span data-stu-id="93c2b-103">Configure teams with protection for sensitive data</span></span>

<span data-ttu-id="93c2b-104">Dans cet article, nous étudions la configuration d’une équipe pour un niveau de protection sensible.</span><span class="sxs-lookup"><span data-stu-id="93c2b-104">In this article, we look at setting up a team for a sensitive level of protection.</span></span> <span data-ttu-id="93c2b-105">Assurez-vous d’avoir effectué les étapes décrites dans [Déployer des équipes avec une protection de base de référence](configure-teams-baseline-protection.md) avant de suivre les étapes décrites dans cet article.</span><span class="sxs-lookup"><span data-stu-id="93c2b-105">Be sure you've completed the steps in [Deploy teams with baseline protection](configure-teams-baseline-protection.md) before following the steps in this article.</span></span> <span data-ttu-id="93c2b-106">Le niveau sensible offre les protections supplémentaires suivantes sur le niveau de référence :</span><span class="sxs-lookup"><span data-stu-id="93c2b-106">The sensitive tier offers the following additional protections over the baseline tier:</span></span>

- <span data-ttu-id="93c2b-p102">Une étiquette de sensibilité pour l'équipe qui vous permet d'activer ou de désactiver le partage des invités et de limiter l'accès au contenu SharePoint au web uniquement pour les appareils non gérés. Cette étiquette peut également être utilisée pour classer les fichiers.</span><span class="sxs-lookup"><span data-stu-id="93c2b-p102">A sensitivity label for the team that allows you to turn guest sharing on or off and limits access to SharePoint content to web-only for unmanaged devices. This label can also be used to classify files.</span></span>
- <span data-ttu-id="93c2b-109">Type de lien de partage par défaut plus restrictif</span><span class="sxs-lookup"><span data-stu-id="93c2b-109">A more restrictive default sharing link type</span></span>
- <span data-ttu-id="93c2b-110">Seuls les propriétaires d’équipe peuvent créer des canaux privés.</span><span class="sxs-lookup"><span data-stu-id="93c2b-110">Only team owners can create private channels.</span></span>

## <a name="video-demonstration"></a><span data-ttu-id="93c2b-111">Démonstration vidéo</span><span class="sxs-lookup"><span data-stu-id="93c2b-111">Video demonstration</span></span>

<span data-ttu-id="93c2b-112">Regardez cette vidéo pour une explication pas à pas des procédures décrites dans cet article.</span><span class="sxs-lookup"><span data-stu-id="93c2b-112">Watch this video for a walkthrough of the procedures described in this article.</span></span>
<br>
<br>
> [!VIDEO https://www.microsoft.com/videoplayer/embed/RE4NMS6]

## <a name="guest-sharing"></a><span data-ttu-id="93c2b-113">Partage d’invités</span><span class="sxs-lookup"><span data-stu-id="93c2b-113">Guest sharing</span></span>

<span data-ttu-id="93c2b-114">Selon la nature de votre entreprise, il est possible que vous souhaitiez ou non activer le partage d’invités pour les équipes qui contiennent des données sensibles.</span><span class="sxs-lookup"><span data-stu-id="93c2b-114">Depending on the nature of your business, you may or may not want to enable guest sharing for teams that contain sensitive data.</span></span> <span data-ttu-id="93c2b-115">Si vous envisagez de collaborer avec des personnes extérieures à votre organisation, nous vous recommandons d’activer le partage d’invités.</span><span class="sxs-lookup"><span data-stu-id="93c2b-115">If you do plan to collaborate with people outside your organization in the team, we recommend enabling guest sharing.</span></span> <span data-ttu-id="93c2b-116">Microsoft 365 inclut de nombreuses fonctionnalités de sécurité et conformité qui vous permettent de partager du contenu sensible de façon sécurisée.</span><span class="sxs-lookup"><span data-stu-id="93c2b-116">Microsoft 365 includes a variety of security and compliance features to help you share sensitive content securely.</span></span> <span data-ttu-id="93c2b-117">Il s’agit généralement d’une option plus sécurisée que la messagerie électronique de contenu directement pour les personnes extérieures à votre organisation.</span><span class="sxs-lookup"><span data-stu-id="93c2b-117">This is generally a more secure option than emailing content directly to people outside your organization.</span></span>

<span data-ttu-id="93c2b-118">Pour plus d’informations sur le partage sécurisé avec des invités, consultez les ressources suivantes :</span><span class="sxs-lookup"><span data-stu-id="93c2b-118">For details about sharing with guests securely, see the following resources:</span></span>

- [<span data-ttu-id="93c2b-119">Limiter l’exposition accidentelle de fichiers lors de partages avec des personnes extérieures à votre organisation</span><span class="sxs-lookup"><span data-stu-id="93c2b-119">Limit accidental exposure to files when sharing with people outside your organization</span></span>](./share-limit-accidental-exposure.md)
- [<span data-ttu-id="93c2b-120">Créer un environnement de partage sécurisé avec des invités</span><span class="sxs-lookup"><span data-stu-id="93c2b-120">Create a secure guest sharing environment</span></span>](./create-secure-guest-sharing-environment.md)

<span data-ttu-id="93c2b-121">Pour autoriser ou bloquer le partage d’invités, nous utilisons une combinaison d’une étiquette de confidentialité pour les contrôles de partage au niveau du site et des équipes pour le site SharePoint associé, les deux décrites ultérieurement.</span><span class="sxs-lookup"><span data-stu-id="93c2b-121">To allow or block guest sharing, we use a combination of a sensitivity label for the team and site-level sharing controls for the associated SharePoint site, both discussed later.</span></span>

## <a name="sensitivity-labels"></a><span data-ttu-id="93c2b-122">Étiquettes de confidentialité</span><span class="sxs-lookup"><span data-stu-id="93c2b-122">Sensitivity labels</span></span>

<span data-ttu-id="93c2b-123">Pour le niveau de protection sensible, nous allons utiliser une étiquette de confidentialité pour classer l’équipe.</span><span class="sxs-lookup"><span data-stu-id="93c2b-123">For the sensitive level of protection, we'll be using a sensitivity label to classify the team.</span></span> <span data-ttu-id="93c2b-124">Cette étiquette peut également être utilisée pour classifier des fichiers individuels dans ce ou d’autres équipes, ou dans d’autres emplacements de fichier tels que SharePoint ou OneDrive.</span><span class="sxs-lookup"><span data-stu-id="93c2b-124">This label can also be used to classify individual files in this or other teams, or in other file locations such as SharePoint or OneDrive.</span></span> 

<span data-ttu-id="93c2b-125">Pour commencer, vous devez activer les étiquettes de confidentialité pour Teams.</span><span class="sxs-lookup"><span data-stu-id="93c2b-125">As a first step, you must enable sensitivity labels for Teams.</span></span> <span data-ttu-id="93c2b-126">Pour plus d’informations, consultez [Utiliser les étiquettes de confidentialité pour protéger le contenu dans Microsoft Teams, les groupes Office 365 et les sites SharePoint](../compliance/sensitivity-labels-teams-groups-sites.md).</span><span class="sxs-lookup"><span data-stu-id="93c2b-126">See [Use sensitivity labels to protect content in Microsoft Teams, Office 365 groups, and SharePoint sites](../compliance/sensitivity-labels-teams-groups-sites.md) for details.</span></span>

<span data-ttu-id="93c2b-127">Si vous avez déjà déployé des étiquettes de confidentialité au sein de votre organisation, réfléchissez à la façon dont cette étiquette correspond à votre stratégie d’étiquette globale.</span><span class="sxs-lookup"><span data-stu-id="93c2b-127">If you already have sensitivity labels deployed in your organization, consider how this label fits with your overall label strategy.</span></span> <span data-ttu-id="93c2b-128">Vous pouvez modifier le nom ou les paramètres si nécessaire pour répondre aux besoins de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="93c2b-128">You can change the name or settings if needed to meet the needs of your organization.</span></span>

<span data-ttu-id="93c2b-129">Une fois que vous avez activé les étiquettes de confidentialité pour Teams, l’étape suivante consiste à créer l’étiquette.</span><span class="sxs-lookup"><span data-stu-id="93c2b-129">Once you have enabled sensitivity labels for Teams, the next step is to create the label.</span></span>

<span data-ttu-id="93c2b-130">Pour créer une étiquette de confidentialité</span><span class="sxs-lookup"><span data-stu-id="93c2b-130">To create a sensitivity label</span></span>
1. <span data-ttu-id="93c2b-131">Ouvrez [Centre de conformité Microsoft 365](https://compliance.microsoft.com).</span><span class="sxs-lookup"><span data-stu-id="93c2b-131">Open the [Microsoft 365 compliance center](https://compliance.microsoft.com).</span></span>
2. <span data-ttu-id="93c2b-132">Sous **Solutions**, cliquez sur **Protection des informations**.</span><span class="sxs-lookup"><span data-stu-id="93c2b-132">Under **Solutions**, click **Information protection**.</span></span>
3. <span data-ttu-id="93c2b-133">Cliquez sur **Créer une étiquette**.</span><span class="sxs-lookup"><span data-stu-id="93c2b-133">Click **Create a label**.</span></span>
4. <span data-ttu-id="93c2b-134">Donnez un nom à l’étiquette.</span><span class="sxs-lookup"><span data-stu-id="93c2b-134">Give the label a name.</span></span> <span data-ttu-id="93c2b-135">Nous vous suggérons le terme **Sensible**, mais vous pouvez choisir un autre nom si celui-ci est déjà utilisé.</span><span class="sxs-lookup"><span data-stu-id="93c2b-135">We suggest **Sensitive**, but you can choose a different name if that one is already in use.</span></span>
5. <span data-ttu-id="93c2b-136">Tapez un nom et une description, puis cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="93c2b-136">Add a display name and description, and then click **Next**.</span></span>
6. <span data-ttu-id="93c2b-137">Dans la page **Définir l’étendue de cette page d’étiquettes**, sélectionnez **Fichiers et courriers électroniques** et **Groupes et sites**, puis cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="93c2b-137">On the **Define the scope for this label page**, select **Files & emails** and **Groups & sites** and click **Next**.</span></span>
7. <span data-ttu-id="93c2b-138">Dans la page **Sélectionner les paramètres de protection pour les fichiers et les messages électroniques**, cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="93c2b-138">On the **Choose protection settings for files and emails** page, click **Next**.</span></span>
8. <span data-ttu-id="93c2b-139">Dans la page \*Étiquetage automatique des fichiers et messages électroniques\*\*, cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="93c2b-139">On the *Auto-labeling for files and emails*\* page, click **Next**.</span></span>
9. <span data-ttu-id="93c2b-140">Dans la page **Définir les paramètres de protection pour les groupes et sites**, sélectionnez **Paramètres de confidentialité et d’accès des utilisateurs externes**, et **Accès appareil et paramètres de partage externe**, puis cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="93c2b-140">On the **Define protection settings for groups and sites** page, select **Privacy and external user access settings** and **Device access and external sharing settings** and click **Next**.</span></span>
10. <span data-ttu-id="93c2b-141">Dans la page **Définir les paramètres de confidentialité et d’accès des utilisateurs externes**, sous **Confidentialité**, sélectionnez l’option **Privé** .</span><span class="sxs-lookup"><span data-stu-id="93c2b-141">On the **Define privacy and external user access settings** page, under **Privacy**, select the **Private** option.</span></span>
11. <span data-ttu-id="93c2b-142">Si vous souhaitez autoriser l’accès invité, sous **Accès des utilisateurs externes**, sélectionnez **Autoriser les propriétaires de groupe Microsoft 365 à ajouter des personnes externes à votre organisation au groupe comme invités**.</span><span class="sxs-lookup"><span data-stu-id="93c2b-142">If you want to allow guest access, under **External user access**, select **Let Microsoft 365 Group owners add people outside your organization to the group as guests**.</span></span>
12. <span data-ttu-id="93c2b-143">Cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="93c2b-143">Click **Next**.</span></span>
13. <span data-ttu-id="93c2b-144">Dans la page **Définir les paramètres de partage externe et d’accès aux appareils**, sélectionnez **Contrôler le partage externe dans les sites étiquetés SharePoint**.</span><span class="sxs-lookup"><span data-stu-id="93c2b-144">On the **Define external sharing and device access settings** page, select **Control external sharing from labeled SharePoint sites**.</span></span>
14. <span data-ttu-id="93c2b-145">Sous **Le contenu peut être partagé avec**, sélectionnez **Invités nouveaux et existants** si vous autorisez l’accès invité ou **Uniquement les membres de votre organisation** si ce n’est pas le cas.</span><span class="sxs-lookup"><span data-stu-id="93c2b-145">Under **Content can be shared with**, choose **New and existing guests** if you're allowing guest access or **Only people in your organization** if not.</span></span>
15. <span data-ttu-id="93c2b-146">Sous **Accès à partir d’appareils non gérés**, sélectionnez **Autoriser l’accès limité au Web uniquement**.</span><span class="sxs-lookup"><span data-stu-id="93c2b-146">Under **Access from unmanaged devices**, choose **Allow limited, web-only access**.</span></span>
16. <span data-ttu-id="93c2b-147">Cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="93c2b-147">Click **Next**.</span></span>
17. <span data-ttu-id="93c2b-148">Dans la page **Étiquetage automatique pour les colonnes de base de données** , cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="93c2b-148">On the **Auto-labeling for database columns** page, click **Next**.</span></span>
18. <span data-ttu-id="93c2b-149">Cliquez sur **Créer une étiquette**, puis sur **Terminé**.</span><span class="sxs-lookup"><span data-stu-id="93c2b-149">Click **Create label**, and then click **Done**.</span></span>

<span data-ttu-id="93c2b-150">Une fois que vous avez créé l’étiquette, vous devez la publier aux utilisateurs qui l’utiliseront.</span><span class="sxs-lookup"><span data-stu-id="93c2b-150">Once you've created the label, you need to publish it to the users who will use it.</span></span> <span data-ttu-id="93c2b-151">Pour une protection sensible, nous allons mettre l’étiquette à la disposition de tous les utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="93c2b-151">For sensitive protection, we'll make the label available to all users.</span></span> <span data-ttu-id="93c2b-152">Vous publiez l’étiquette dans le Centre de conformité Microsoft 365, sur l’onglet **Stratégies d’étiquette** de la page **Protection des informations**.</span><span class="sxs-lookup"><span data-stu-id="93c2b-152">You publish the label in the Microsoft 365 compliance center, on the **Label policies** tab of the **Information protection** page.</span></span> <span data-ttu-id="93c2b-153">Si vous avez une stratégie existante qui s’applique à tous les utilisateurs, ajoutez cette étiquette à cette stratégie.</span><span class="sxs-lookup"><span data-stu-id="93c2b-153">If you have an existing policy that applies to all users, add this label to that policy.</span></span> <span data-ttu-id="93c2b-154">Si vous avez besoin de créer une stratégie, consultez [Publier des étiquettes de confidentialité en créant une stratégie d’étiquette](../compliance/create-sensitivity-labels.md#publish-sensitivity-labels-by-creating-a-label-policy).</span><span class="sxs-lookup"><span data-stu-id="93c2b-154">If you need to create a new policy, see [Publish sensitivity labels by creating a label policy](../compliance/create-sensitivity-labels.md#publish-sensitivity-labels-by-creating-a-label-policy).</span></span>

## <a name="create-a-team"></a><span data-ttu-id="93c2b-155">Créer une équipe</span><span class="sxs-lookup"><span data-stu-id="93c2b-155">Create a team</span></span>

<span data-ttu-id="93c2b-156">La configuration supplémentaire du scénario sensible est effectuée sur le site SharePoint associé à l’équipe. L’étape suivante consiste à créer une équipe.</span><span class="sxs-lookup"><span data-stu-id="93c2b-156">Further configuration of the sensitive scenario is done in the SharePoint site associated with the team, so the next step is to create a team.</span></span>

<span data-ttu-id="93c2b-157">Pour créer une équipe pour les informations sensibles</span><span class="sxs-lookup"><span data-stu-id="93c2b-157">To create a team for sensitive information</span></span>
1. <span data-ttu-id="93c2b-158">Dans Teams, cliquez sur **Teams** sur le côté gauche de l’application, puis cliquez sur **Rejoindre ou créer une équipe** en bas de la liste des équipes.</span><span class="sxs-lookup"><span data-stu-id="93c2b-158">In Teams, click **Teams** on the left side of the app, then click **Join or create a team** at the bottom of the teams list.</span></span>
2. <span data-ttu-id="93c2b-159">Cliquez sur **Créer une équipe** (première carte, coin supérieur gauche).</span><span class="sxs-lookup"><span data-stu-id="93c2b-159">Click **Create team** (first card, top left corner).</span></span>
3. <span data-ttu-id="93c2b-160">Sélectionnez **Créer une équipe à partir de zéro**.</span><span class="sxs-lookup"><span data-stu-id="93c2b-160">Choose **Build a team from scratch**.</span></span>
4. <span data-ttu-id="93c2b-161">Dans la liste **Sensibilité**, sélectionnez l’étiquette **sensible** que vous venez de créer.</span><span class="sxs-lookup"><span data-stu-id="93c2b-161">In the **Sensitivity** list, choose the **sensitive** label that you just created.</span></span>
5. <span data-ttu-id="93c2b-162">Sous **Confidentialité**, cliquez sur **Privée**.</span><span class="sxs-lookup"><span data-stu-id="93c2b-162">Under **Privacy**, click **Private**.</span></span>
6. <span data-ttu-id="93c2b-163">Tapez un nom pour l’équipe, puis cliquez sur **Créer**.</span><span class="sxs-lookup"><span data-stu-id="93c2b-163">Type a name for the team, and then click **Create**.</span></span>
7. <span data-ttu-id="93c2b-164">Ajoutez des utilisateurs à l’équipe, puis cliquez sur **Fermer**.</span><span class="sxs-lookup"><span data-stu-id="93c2b-164">Add users to the team, and then click **Close**.</span></span>

## <a name="private-channel-settings"></a><span data-ttu-id="93c2b-165">Paramètres du canal privé</span><span class="sxs-lookup"><span data-stu-id="93c2b-165">Private channel settings</span></span>

<span data-ttu-id="93c2b-166">À ce niveau, nous limitons la création de canaux privés aux propriétaires d'équipe.</span><span class="sxs-lookup"><span data-stu-id="93c2b-166">In this tier, we restrict creating private channels to team owners.</span></span>

<span data-ttu-id="93c2b-167">Pour restreindre la création d’un canal privé</span><span class="sxs-lookup"><span data-stu-id="93c2b-167">To restrict private channel creation</span></span>
1. <span data-ttu-id="93c2b-168">Dans l’équipe, cliquez sur **Autres options**, puis cliquez sur **Gérer l’équipe**.</span><span class="sxs-lookup"><span data-stu-id="93c2b-168">In the team, click **More options**, and then click **Manage team**.</span></span>
2. <span data-ttu-id="93c2b-169">Sous l’onglet **Paramètres**, développez **Autorisations de membre**.</span><span class="sxs-lookup"><span data-stu-id="93c2b-169">On the **Settings** tab, expand **Member permissions**.</span></span>
3. <span data-ttu-id="93c2b-170">Désactivez la case à cocher **Autoriser les membres à créer des canaux privés**.</span><span class="sxs-lookup"><span data-stu-id="93c2b-170">Clear the **Allow members to create private channels** check box.</span></span>

<span data-ttu-id="93c2b-171">Vous pouvez également utiliser les [stratégies d’équipes](/MicrosoftTeams/teams-policies) pour contrôler qui peut créer des canaux privés.</span><span class="sxs-lookup"><span data-stu-id="93c2b-171">You can also use [teams policies](/MicrosoftTeams/teams-policies) to control who can create private channels.</span></span>

## <a name="sharepoint-settings"></a><span data-ttu-id="93c2b-172">Paramètres de SharePoint</span><span class="sxs-lookup"><span data-stu-id="93c2b-172">SharePoint settings</span></span>

<span data-ttu-id="93c2b-173">Chaque fois que vous créez une équipe avec une étiquette de confidentialité, vous devez procéder de deux étapes dans SharePoint :</span><span class="sxs-lookup"><span data-stu-id="93c2b-173">Each time you create a new team with the sensitive label, there are two steps to do in SharePoint:</span></span>

- <span data-ttu-id="93c2b-174">Mettez à jour les paramètres de partage d’invités pour le site dans le Centre d’administration SharePoint, afin qu’ils mettent à jour le lien de partage par défaut vers *Personnes spécifiques*.</span><span class="sxs-lookup"><span data-stu-id="93c2b-174">Update the guest sharing settings for the site in the SharePoint admin center to update the default sharing link to *Specific people*.</span></span>
- <span data-ttu-id="93c2b-175">Mettez à jour les paramètres de partage du site lui-même pour empêcher les membres de partager le site.</span><span class="sxs-lookup"><span data-stu-id="93c2b-175">Update the site sharing settings in the site itself to prevent members from sharing the site.</span></span>

### <a name="site-default-sharing-link-settings"></a><span data-ttu-id="93c2b-176">Paramètres de lien de partage par défaut du site</span><span class="sxs-lookup"><span data-stu-id="93c2b-176">Site default sharing link settings</span></span>

<span data-ttu-id="93c2b-177">Pour mettre à jour le type de lien de partage par défaut du site</span><span class="sxs-lookup"><span data-stu-id="93c2b-177">To update the site default sharing link type</span></span>

1. <span data-ttu-id="93c2b-178">Ouvrez le [Centre d’administration SharePoint](https://admin.microsoft.com/sharepoint).</span><span class="sxs-lookup"><span data-stu-id="93c2b-178">Open the [SharePoint admin center](https://admin.microsoft.com/sharepoint).</span></span>
2. <span data-ttu-id="93c2b-179">Sous **Sites**, cliquez sur **Sites actifs**.</span><span class="sxs-lookup"><span data-stu-id="93c2b-179">Under **Sites**, click **Active sites**.</span></span>
3. <span data-ttu-id="93c2b-180">Cliquez sur le site associé à l’équipe.</span><span class="sxs-lookup"><span data-stu-id="93c2b-180">Click the site that is associated with team.</span></span>
4. <span data-ttu-id="93c2b-181">Sous l’onglet **Stratégies**, sous **Partage externe**, cliquez sur **Modifier**.</span><span class="sxs-lookup"><span data-stu-id="93c2b-181">On the **Policies** tab, under **External sharing**, click **Edit**.</span></span>
5. <span data-ttu-id="93c2b-182">Sous Type de lien de partage par défaut, désactivez la case à cocher **Identique au paramètre de niveau organisation**, puis sélectionnez **Personnes spécifiques (uniquement les membres spécifiés par l’utilisateur)**.</span><span class="sxs-lookup"><span data-stu-id="93c2b-182">Under Default sharing link type, clear the **Same as organization-level setting** check box, and select **Specific people (only the people the user specifies)**.</span></span>
6. <span data-ttu-id="93c2b-183">Cliquez sur **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="93c2b-183">Click **Save**.</span></span>

<span data-ttu-id="93c2b-184">Si vous voulez créer un script dans le cadre de votre processus de création d’équipe, vous pouvez utiliser [Set-SPOSite](/powershell/module/sharepoint-online/set-sposite) avec les paramètre `-DefaultSharingLinkType Direct` pour modifier le lien de partage par défaut pour *Personnes spécifiques*.</span><span class="sxs-lookup"><span data-stu-id="93c2b-184">If you want to script this as part of your team creation process, you can use [Set-SPOSite](/powershell/module/sharepoint-online/set-sposite) with the `-DefaultSharingLinkType Direct` parameter to change the default sharing link to *Specific people*.</span></span>

#### <a name="private-channels"></a><span data-ttu-id="93c2b-185">Canaux privés</span><span class="sxs-lookup"><span data-stu-id="93c2b-185">Private channels</span></span>

<span data-ttu-id="93c2b-186">Si vous ajoutez des canaux privés à l’équipe, chaque canal privé crée un site SharePoint avec les paramètres de partage par défaut.</span><span class="sxs-lookup"><span data-stu-id="93c2b-186">If you add private channels to the team, each private channel creates a new SharePoint site with the default sharing settings.</span></span> <span data-ttu-id="93c2b-187">Ces sites ne sont pas visibles dans le Centre d’administration SharePoint. vous devez donc utiliser l’applet de commande PowerShell SPOSite pour mettre à jour les paramètres de partage d’invités.</span><span class="sxs-lookup"><span data-stu-id="93c2b-187">These sites are not visible in the SharePoint admin center, so you must use the Set-SPOSite PowerShell cmdlet to update the guest sharing settings.</span></span>

### <a name="site-sharing-settings"></a><span data-ttu-id="93c2b-188">Paramètres de partage de site</span><span class="sxs-lookup"><span data-stu-id="93c2b-188">Site sharing settings</span></span>

<span data-ttu-id="93c2b-189">Pour vous assurer que le site SharePoint ne soit pas partagé avec des personnes qui ne sont pas membres de l’équipe, nous limitons ce partage aux propriétaires.</span><span class="sxs-lookup"><span data-stu-id="93c2b-189">To help ensure that the SharePoint site does not get shared with people who are not members of the team, we limit such sharing to owners.</span></span>

<span data-ttu-id="93c2b-190">Pour configurer le partage de sites propriétaires uniquement</span><span class="sxs-lookup"><span data-stu-id="93c2b-190">To configure owners-only site sharing</span></span>
1. <span data-ttu-id="93c2b-191">Dans Teams, accédez à l’onglet **Général** de l’équipe que vous voulez mettre à jour.</span><span class="sxs-lookup"><span data-stu-id="93c2b-191">In Teams, navigate to the **General** tab of the team you want to update.</span></span>
2. <span data-ttu-id="93c2b-192">Dans la barre d’outils de l’équipe, cliquez sur **Fichiers**.</span><span class="sxs-lookup"><span data-stu-id="93c2b-192">In the tool bar for the team, click **Files**.</span></span>
3. <span data-ttu-id="93c2b-193">Cliquez sur les points de suspension, puis sur **Ouvrir dans SharePoint**.</span><span class="sxs-lookup"><span data-stu-id="93c2b-193">Click the ellipsis, and then click **Open in SharePoint**.</span></span>
4. <span data-ttu-id="93c2b-194">Dans la barre d’outils du site SharePoint sous-jacent, cliquez sur l’icône Paramètres, puis cliquez sur **Autorisations du site**.</span><span class="sxs-lookup"><span data-stu-id="93c2b-194">In the tool bar of the underlying SharePoint site, click the settings icon, and then click **Site permissions**.</span></span>
5. <span data-ttu-id="93c2b-195">Dans le volet **Autorisations de site**, sous **Partage de site**, cliquez sur **Modifier les modalités de partage par les membres**.</span><span class="sxs-lookup"><span data-stu-id="93c2b-195">In the **Site permissions** pane, under **Site sharing**, click **Change how members can share**.</span></span>
6. <span data-ttu-id="93c2b-196">Sous **Autorisations de partage**, sélectionnez **Propriétaires et membres du site. les personnes disposant des autorisations de modification peuvent partager des fichiers et des dossiers, mais seuls les propriétaires de site peuvent partager le site**, puis cliquer sur **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="93c2b-196">Under **Sharing permissions**, choose **Site owners and members, and people with Edit permissions can share files and folders, but only site owners can share the site**, and then click **Save**.</span></span>


## <a name="see-also"></a><span data-ttu-id="93c2b-197">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="93c2b-197">See Also</span></span>

[<span data-ttu-id="93c2b-198">Créer et configurer des étiquettes de confidentialité ainsi que leurs stratégies</span><span class="sxs-lookup"><span data-stu-id="93c2b-198">Create and configure sensitivity labels and their policies</span></span>](../compliance/create-sensitivity-labels.md)
