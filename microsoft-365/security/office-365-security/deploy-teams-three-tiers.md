---
title: Déployer des équipes pour trois niveaux de protection des fichiers
f1.keywords:
- NOCSH
ms.author: josephd
author: JoeDavies-MSFT
manager: laurawi
ms.date: 10/31/2019
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Priority
search.appverid:
- MET150
ms.collection:
- Ent_O365
- Strat_O365_Enterprise
ms.custom:
- Ent_Solutions
ms.assetid: 1e8e3cfd-b878-4088-b941-9940363a5fae
description: Créez et configurez des équipes avec Microsoft Teams pour différents niveaux de protection des informations pour les fichiers.
ms.openlocfilehash: 63a4b6763165f38e1de5331324e5a7b3573ea0f1
ms.sourcegitcommit: 3dd9944a6070a7f35c4bc2b57df397f844c3fe79
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/15/2020
ms.locfileid: "42083329"
---
# <a name="deploy-teams-for-three-tiers-of-protection-for-files"></a><span data-ttu-id="6311b-103">Déployer des équipes pour trois niveaux de protection des fichiers</span><span class="sxs-lookup"><span data-stu-id="6311b-103">Deploy teams for three tiers of protection for files</span></span>

<span data-ttu-id="6311b-104">Suivez les étapes décrites dans cet article pour créer et déployer des équipes de référence, sensibles et hautement confidentiels.</span><span class="sxs-lookup"><span data-stu-id="6311b-104">Use the steps in this article to design and deploy baseline, sensitive, and highly confidential teams.</span></span> <span data-ttu-id="6311b-105">Pour plus d’informations sur ces trois niveaux de protection, consultez [Sécuriser des fichiers dans Microsoft Teams](secure-files-in-teams.md).</span><span class="sxs-lookup"><span data-stu-id="6311b-105">For more information about these three tiers of protection, see [Secure files in Microsoft Teams](secure-files-in-teams.md).</span></span>

## <a name="baseline-teams"></a><span data-ttu-id="6311b-106">Équipes de référence</span><span class="sxs-lookup"><span data-stu-id="6311b-106">Baseline teams</span></span>

<span data-ttu-id="6311b-107">La protection Base de référence inclut les équipes publiques et privées.</span><span class="sxs-lookup"><span data-stu-id="6311b-107">Baseline protection includes both public and private teams.</span></span> <span data-ttu-id="6311b-108">Les équipes publiques peuvent être découvertes et sont accessibles par toute personne de l’organisation.</span><span class="sxs-lookup"><span data-stu-id="6311b-108">Public teams can be discovered and accessed by anybody in the organization.</span></span> <span data-ttu-id="6311b-109">Les sites privés peuvent être découverts et sont accessibles seulement par les membres du groupe Office 365 associé à l’équipe.</span><span class="sxs-lookup"><span data-stu-id="6311b-109">Private sites can only be discovered and accessed by members of the Office 365 group associated with the team.</span></span> <span data-ttu-id="6311b-110">Ces deux types d’équipes permettent aux membres de partager le site avec d’autres utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="6311b-110">Both of these types of teams allow members to share the site with others.</span></span>

### <a name="public"></a><span data-ttu-id="6311b-111">Public</span><span class="sxs-lookup"><span data-stu-id="6311b-111">Public</span></span>

<span data-ttu-id="6311b-112">Utilisez les instructions de [cet article](https://support.office.com/article/174adf5f-846b-4780-b765-de1a0a737e2b) pour créer une équipe de référence avec accès et autorisations publics.</span><span class="sxs-lookup"><span data-stu-id="6311b-112">Follow the instructions in [this article](https://support.office.com/article/174adf5f-846b-4780-b765-de1a0a737e2b) to create a baseline Team with public access and permissions.</span></span>

<span data-ttu-id="6311b-113">Voici la configuration finale.</span><span class="sxs-lookup"><span data-stu-id="6311b-113">Here is your resulting configuration.</span></span>

![Protection de niveau de référence pour une équipe publique.](../../media/baseline-public-team.png)

### <a name="private"></a><span data-ttu-id="6311b-115">Privé</span><span class="sxs-lookup"><span data-stu-id="6311b-115">Private</span></span>

<span data-ttu-id="6311b-116">Utilisez les instructions de [cet article](https://support.office.com/article/174adf5f-846b-4780-b765-de1a0a737e2b) pour créer une équipe de référence avec accès et autorisations privés.</span><span class="sxs-lookup"><span data-stu-id="6311b-116">Follow the instructions in [this article](https://support.office.com/article/174adf5f-846b-4780-b765-de1a0a737e2b) to create a baseline Team with private access and permissions.</span></span>

<span data-ttu-id="6311b-117">Voici la configuration finale.</span><span class="sxs-lookup"><span data-stu-id="6311b-117">Here is your resulting configuration.</span></span>

![Protection de niveau de référence pour une équipe privée.](../../media/baseline-private-team.png)

## <a name="sensitive-teams"></a><span data-ttu-id="6311b-119">Équipes sensibles</span><span class="sxs-lookup"><span data-stu-id="6311b-119">Sensitive teams</span></span>

<span data-ttu-id="6311b-120">Pour une équipe sensible, vous commencez par [créer une équipe privée](https://support.office.com/article/174adf5f-846b-4780-b765-de1a0a737e2b).</span><span class="sxs-lookup"><span data-stu-id="6311b-120">For a sensitive team, you start by [creating a private team](https://support.office.com/article/174adf5f-846b-4780-b765-de1a0a737e2b).</span></span>

<span data-ttu-id="6311b-121">Vous configurez ensuite le site SharePoint sous-jacent pour empêcher le partage par les membres de l'équipe.</span><span class="sxs-lookup"><span data-stu-id="6311b-121">Next, you configure the underlying SharePoint site to prevent sharing by team members.</span></span>

1. <span data-ttu-id="6311b-122">Dans la barre d’outils de l’équipe, cliquez sur **Fichiers**.</span><span class="sxs-lookup"><span data-stu-id="6311b-122">In the tool bar for the team, click **Files**.</span></span>

2. <span data-ttu-id="6311b-123">Cliquez sur les points de suspension, puis sur **Ouvrir dans SharePoint**.</span><span class="sxs-lookup"><span data-stu-id="6311b-123">Click the ellipsis, and then click **Open in SharePoint**.</span></span>

3. <span data-ttu-id="6311b-124">Dans la barre d’outils du site SharePoint sous-jacent, cliquez sur l’icône Paramètres, puis cliquez sur **Autorisations du site**.</span><span class="sxs-lookup"><span data-stu-id="6311b-124">In the tool bar of the underlying SharePoint site, click the settings icon, and then click **Site permissions**.</span></span>

4. <span data-ttu-id="6311b-125">Dans le volet **Autorisations de site**, sous **Paramètres de partage**, cliquez sur **Modifier les paramètres de partage**.</span><span class="sxs-lookup"><span data-stu-id="6311b-125">In the **Site permissions** pane, under **Sharing Settings**, click **Change sharing settings**.</span></span>

5. <span data-ttu-id="6311b-126">Sous **Autorisations de partage**, sélectionnez **Seuls les propriétaires du site peuvent partager des fichiers, des dossiers et le site**, puis cliquez sur **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="6311b-126">Under **Sharing permissions**, choose **Only site owners can share files, folders, and the site**, and then click **Save**.</span></span>

<span data-ttu-id="6311b-127">Voici la configuration finale.</span><span class="sxs-lookup"><span data-stu-id="6311b-127">Here is your resulting configuration.</span></span>

![Protection sensible pour les membres d’une équipe.](../../media/sensitive-team.png)

## <a name="highly-confidential-teams"></a><span data-ttu-id="6311b-129">Équipe hautement confidentielles</span><span class="sxs-lookup"><span data-stu-id="6311b-129">Highly confidential teams</span></span>

<span data-ttu-id="6311b-130">Avec une équipe hautement confidentielle, vous commencez par [créer une équipe privée](https://support.office.com/article/174adf5f-846b-4780-b765-de1a0a737e2b).</span><span class="sxs-lookup"><span data-stu-id="6311b-130">With a highly confidential team, you start by [creating a private team](https://support.office.com/article/174adf5f-846b-4780-b765-de1a0a737e2b).</span></span>

<span data-ttu-id="6311b-131">Vous configurez ensuite le site SharePoint sous-jacent pour empêcher le partage par les membres de l'équipe et la demande d’accès par des non-membre de l’équipe.</span><span class="sxs-lookup"><span data-stu-id="6311b-131">Next, you configure the underlying SharePoint site to prevent sharing by team members and the requesting of access by non-members of the team.</span></span>

1. <span data-ttu-id="6311b-132">Dans la barre d’outils de l’équipe, cliquez sur **Fichiers**.</span><span class="sxs-lookup"><span data-stu-id="6311b-132">In the tool bar for the team, click **Files**.</span></span>

2. <span data-ttu-id="6311b-133">Cliquez sur les points de suspension, puis sur **Ouvrir dans SharePoint**.</span><span class="sxs-lookup"><span data-stu-id="6311b-133">Click the ellipsis, and then click **Open in SharePoint**.</span></span>

3. <span data-ttu-id="6311b-134">Dans la barre d’outils du site SharePoint sous-jacent, cliquez sur l’icône Paramètres, puis cliquez sur **Autorisations du site**.</span><span class="sxs-lookup"><span data-stu-id="6311b-134">In the tool bar of the underlying SharePoint site, click the settings icon, and then click **Site permissions**.</span></span>

4. <span data-ttu-id="6311b-135">Dans le volet **Autorisations de site**, sous **Paramètres de partage**, cliquez sur **Modifier les paramètres de partage**.</span><span class="sxs-lookup"><span data-stu-id="6311b-135">In the **Site permissions** pane, under **Sharing Settings**, click **Change sharing settings**.</span></span>

5. <span data-ttu-id="6311b-136">Sous **Autorisations de partage**, sélectionnez **Seuls les propriétaires du site peuvent partager des fichiers, des dossiers et le site**.</span><span class="sxs-lookup"><span data-stu-id="6311b-136">Under **Sharing permissions**, choose **Only site owners can share files, folders, and the site**.</span></span>

6. <span data-ttu-id="6311b-137">Désactivez **Autoriser les demandes d’accès**, puis cliquez sur **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="6311b-137">Turn off **Allow access requests**, and then click **Save**.</span></span>

<span data-ttu-id="6311b-138">Voici la configuration finale.</span><span class="sxs-lookup"><span data-stu-id="6311b-138">Here is your resulting configuration.</span></span>

![Protection hautement confidentielle pour les membres d’une équipe.](../../media/highly-confidential-team.png)

## <a name="next-step"></a><span data-ttu-id="6311b-140">Étape suivante</span><span class="sxs-lookup"><span data-stu-id="6311b-140">Next step</span></span>

[<span data-ttu-id="6311b-141">Protéger des fichiers dans Teams avec des étiquettes de rétention et la protection contre la perte de données (DLP)</span><span class="sxs-lookup"><span data-stu-id="6311b-141">Protect files in teams with retention labels and DLP</span></span>](deploy-teams-retention-DLP.md)

## <a name="see-also"></a><span data-ttu-id="6311b-142">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6311b-142">See also</span></span>

[<span data-ttu-id="6311b-143">Sécuriser des fichiers dans Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="6311b-143">Secure files in Microsoft Teams</span></span>](secure-files-in-teams.md)

[<span data-ttu-id="6311b-144">Adoption du cloud et solutions hybrides</span><span class="sxs-lookup"><span data-stu-id="6311b-144">Cloud adoption and hybrid solutions</span></span>](https://docs.microsoft.com/office365/enterprise/cloud-adoption-and-hybrid-solutions)
