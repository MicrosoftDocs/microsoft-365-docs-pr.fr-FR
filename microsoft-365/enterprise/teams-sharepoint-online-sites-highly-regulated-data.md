---
title: Sites SharePoint pour les données hautement réglementées
author: JoeDavies-MSFT
ms.author: josephd
manager: laurawi
ms.date: 10/21/2019
audience: ITPro
ms.topic: article
ms.service: o365-solutions
localization_priority: Priority
ms.collection:
- M365-security-compliance
- Strat_O365_Enterprise
ms.custom: ''
description: Créez un site d’équipe SharePoint sécurisé pour stocker vos fichiers les plus précieux et les plus sensibles.
ms.openlocfilehash: 7162ced48a64270713dc1eac6e73de053d24b2f4
ms.sourcegitcommit: 7ee256132358a86f8c6ad143816fcfdde011ca74
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/22/2019
ms.locfileid: "37628338"
---
# <a name="sharepoint-sites-for-highly-regulated-data"></a><span data-ttu-id="ea230-103">Sites SharePoint pour les données hautement réglementées</span><span class="sxs-lookup"><span data-stu-id="ea230-103">SharePoint sites for highly regulated data</span></span>

<span data-ttu-id="ea230-104">*Ce scénario s’applique à la fois aux versions E3 et E5 de Microsoft 365 Entreprise*</span><span class="sxs-lookup"><span data-stu-id="ea230-104">*This scenario applies to both the E3 and E5 versions of Microsoft 365 Enterprise*</span></span>

<span data-ttu-id="ea230-p101">Microsoft 365 Entreprise comprend une suite complète de services basés sur le cloud afin que vous puissiez créer, stocker, sécuriser et gérer vos données hautement réglementées, notamment les données qui sont :</span><span class="sxs-lookup"><span data-stu-id="ea230-p101">Microsoft 365 Enterprise includes a full suite of cloud-based services so that you can create, store, secure, and manage your highly regulated data stored in files. This includes data that is:</span></span>

- <span data-ttu-id="ea230-107">sujettes à des réglementations régionales ;</span><span class="sxs-lookup"><span data-stu-id="ea230-107">Subject to regional regulations.</span></span>
- <span data-ttu-id="ea230-108">les plus précieuses de votre organisation comme les secrets commerciaux, les informations sur les ressources humaines ou financières et la stratégie de l’organisation.</span><span class="sxs-lookup"><span data-stu-id="ea230-108">The most valuable data for your organization, such as trade secrets, financial or human resources information, and organization strategy.</span></span>

>[!Note]
> <span data-ttu-id="ea230-109">Un scénario similaire utilisant Microsoft Teams se trouve [ici](secure-teams-highly-regulated-data-scenario.md).</span><span class="sxs-lookup"><span data-stu-id="ea230-109">A similar scenario using Microsoft Teams is in development.</span></span>
>

<span data-ttu-id="ea230-110">Dans le cadre d’un scénario Microsoft 365 Entreprise basé sur le cloud qui répond à ce besoin métier, vous êtes tenu de suivre les instructions suivantes :</span><span class="sxs-lookup"><span data-stu-id="ea230-110">A Microsoft 365 Enterprise cloud-based scenario that meets this business need requires that you:</span></span>

- <span data-ttu-id="ea230-111">Stockez des fichiers (documents, diapositives, feuilles de calcul, etc.) dans un site d’équipe SharePoint.</span><span class="sxs-lookup"><span data-stu-id="ea230-111">Store files (documents, slide decks, spreadsheets, etc.) in a SharePoint team site.</span></span>
- <span data-ttu-id="ea230-112">Verrouillez le site pour empêcher :</span><span class="sxs-lookup"><span data-stu-id="ea230-112">Lock down the site to prevent:</span></span>
  - <span data-ttu-id="ea230-113">L’accès aux utilisateurs qui ne sont pas membres du groupe Office 365 pour le site.</span><span class="sxs-lookup"><span data-stu-id="ea230-113">Access to users who are not members of the Office 365 group for the site.</span></span>
  - <span data-ttu-id="ea230-114">les membres du site d’octroyer l’accès à d’autres personnes ;</span><span class="sxs-lookup"><span data-stu-id="ea230-114">Members of the site from granting access to others.</span></span>
  - <span data-ttu-id="ea230-115">l’accès au site par les personnes non membres.</span><span class="sxs-lookup"><span data-stu-id="ea230-115">Non-members of the site from requesting access to the site.</span></span>
- <span data-ttu-id="ea230-116">Configurez une étiquette de rétention Office 365 pour vos sites SharePoint comme moyen par défaut pour empêcher les utilisateurs d’envoyer des fichiers à l’extérieur de l’organisation.</span><span class="sxs-lookup"><span data-stu-id="ea230-116">Configure an Office 365 retention label for your SharePoint sites as a default way to block users from sending files outside the organization.</span></span>
- <span data-ttu-id="ea230-117">Chiffrer les fichiers les plus sensibles du site avec le chiffrement qui accompagne le fichier.</span><span class="sxs-lookup"><span data-stu-id="ea230-117">Encrypt the most sensitive files of the site with encryption that travels with the file.</span></span>
- <span data-ttu-id="ea230-118">Ajoutez des autorisations aux fichiers les plus sensibles de sorte que même s'ils sont partagés en dehors du site, leur ouverture nécessite toujours les informations d’identification valides d’un compte d’utilisateur autorisé.</span><span class="sxs-lookup"><span data-stu-id="ea230-118">Add permissions to the most sensitive files so that if even if they get shared outside of the site, opening the file still requires the valid credentials of a user account that has permission.</span></span>

<span data-ttu-id="ea230-119">Le tableau suivant mappe les conditions requises de ce scénario à une fonctionnalité de Microsoft 365 Entreprise.</span><span class="sxs-lookup"><span data-stu-id="ea230-119">The following table maps the requirements of this scenario to a feature of Microsoft 365 Enterprise.</span></span>

|||
|:-------|:-----|
| <span data-ttu-id="ea230-120">**Configuration requise**</span><span class="sxs-lookup"><span data-stu-id="ea230-120">**Requirement**</span></span> | <span data-ttu-id="ea230-121">**Fonctionnalité Microsoft 365 Entreprise**</span><span class="sxs-lookup"><span data-stu-id="ea230-121">**Microsoft 365 Enterprise feature**</span></span> |
| <span data-ttu-id="ea230-122">Stocker des fichiers</span><span class="sxs-lookup"><span data-stu-id="ea230-122">Store files</span></span> | <span data-ttu-id="ea230-123">Sites d’équipe SharePoint</span><span class="sxs-lookup"><span data-stu-id="ea230-123">SharePoint team sites</span></span> |
| <span data-ttu-id="ea230-124">Verrouiller le site</span><span class="sxs-lookup"><span data-stu-id="ea230-124">Lock down the site</span></span> | <span data-ttu-id="ea230-125">Autorisations de sites d’équipe SharePoint Online et de groupes Office 365</span><span class="sxs-lookup"><span data-stu-id="ea230-125">Office 365 groups and SharePoint team site permissions</span></span> |
| <span data-ttu-id="ea230-126">Étiqueter les fichiers du site</span><span class="sxs-lookup"><span data-stu-id="ea230-126">Label the files of the site</span></span> | <span data-ttu-id="ea230-127">Étiquettes de rétention Office 365</span><span class="sxs-lookup"><span data-stu-id="ea230-127">Office 365 retention labels</span></span> |
| <span data-ttu-id="ea230-128">Bloquer les utilisateurs lors de l’envoi de fichiers à l’extérieur de l’organisation</span><span class="sxs-lookup"><span data-stu-id="ea230-128">Block users when sending files outside the organization</span></span> | <span data-ttu-id="ea230-129">Stratégies de protection contre la perte de données (DLP) dans Office 365</span><span class="sxs-lookup"><span data-stu-id="ea230-129">Data Loss Prevention (DLP) policies in Office 365</span></span> |
| <span data-ttu-id="ea230-130">Chiffrer tous les fichiers du site</span><span class="sxs-lookup"><span data-stu-id="ea230-130">Encrypt all of the files of the site</span></span> | <span data-ttu-id="ea230-131">Sous-étiquettes ou étiquettes de confidentialité d’Office 365</span><span class="sxs-lookup"><span data-stu-id="ea230-131">Office 365 sensitivity labels or sublabels</span></span> |
| <span data-ttu-id="ea230-132">Ajouter des autorisations aux fichiers du site</span><span class="sxs-lookup"><span data-stu-id="ea230-132">Add permissions to the files of the site</span></span> | <span data-ttu-id="ea230-133">Sous-étiquettes ou étiquettes de confidentialité d’Office 365</span><span class="sxs-lookup"><span data-stu-id="ea230-133">Office 365 sensitivity labels or sublabels</span></span> |
|||

<span data-ttu-id="ea230-134">Voici un exemple de configuration d’un site SharePoint sécurisé.</span><span class="sxs-lookup"><span data-stu-id="ea230-134">Here is the configuration for a secure SharePoint site.</span></span>

![Les sites SharePoint pour les scénarios de données hautement réglementés](./media/teams-sharepoint-online-sites-highly-regulated-data/end-to-end-configuration.png)

<span data-ttu-id="ea230-136">Ce scénario implique que vous ayez déjà déployé les éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="ea230-136">This scenario requires that you have already deployed:</span></span>

- <span data-ttu-id="ea230-137">La phase [Identité](identity-infrastructure.md) et les étapes 1 et 2 de la phase [Protection des informations](infoprotect-infrastructure.md) de l’infrastructure de base.</span><span class="sxs-lookup"><span data-stu-id="ea230-137">The [Identity](identity-infrastructure.md) phase and steps 1 and 2 of the [Information protection](infoprotect-infrastructure.md) phase of the foundation infrastructure.</span></span> 
- <span data-ttu-id="ea230-138">[SharePoint](sharepoint-online-onedrive-workload.md).</span><span class="sxs-lookup"><span data-stu-id="ea230-138">[SharePoint](sharepoint-online-onedrive-workload.md).</span></span>

<span data-ttu-id="ea230-139">Les phases suivantes vous guident à travers toute la conception, la configuration et le pilotage de l'adoption des sites SharePoint pour les données hautement réglementées.</span><span class="sxs-lookup"><span data-stu-id="ea230-139">The following phases step you through designing, configuring, and driving adoption for SharePoint sites for highly regulated data.</span></span>

<span data-ttu-id="ea230-140">Pour découvrir comment Contoso Corporation, une organisation multinationale fictive mais représentative, a conçu un site SharePoint pour ses équipes de recherche, consultez cette [configuration exemple](contoso-sharepoint-online-site-for-highly-confidential-assets.md).</span><span class="sxs-lookup"><span data-stu-id="ea230-140">To see how the Contoso Corporation, a fictional but representative multi-national organization, designed a SharePoint site for its research teams, see this [example configuration](contoso-sharepoint-online-site-for-highly-confidential-assets.md).</span></span>

## <a name="identity-and-device-access-prerequisites"></a><span data-ttu-id="ea230-141">Conditions préalables pour les identités et l’accès aux appareils</span><span class="sxs-lookup"><span data-stu-id="ea230-141">Identity and device access prerequisites</span></span>

<span data-ttu-id="ea230-142">Pour protéger l’accès aux sites SharePoint, vérifiez que vous avez configuré les [stratégies pour les identités et l’accès aux appareils](identity-access-policies.md) et les [stratégies d’accès à SharePoint recommandées](sharepoint-file-access-policies.md).</span><span class="sxs-lookup"><span data-stu-id="ea230-142">To protect access to the SharePoint site, ensure that you have configured [identity and device access policies](identity-access-policies.md) and the [recommended SharePoint access policies](sharepoint-file-access-policies.md).</span></span>

## <a name="phase-1-design"></a><span data-ttu-id="ea230-143">Phase 1 : conception</span><span class="sxs-lookup"><span data-stu-id="ea230-143">Phase 1: Design</span></span>

<span data-ttu-id="ea230-144">Pour créer un site SharePoint pour les données hautement réglementées, vous devez commencer par identifier son objet.</span><span class="sxs-lookup"><span data-stu-id="ea230-144">To create a SharePoint site for highly regulated data, you must first identify its purpose.</span></span> <span data-ttu-id="ea230-145">Par exemple, le département recherche et développement d’une organisation de production a besoin d’un site SharePoint pour stocker les spécifications de conception actuelles des produits existants et un emplacement pour collaborer à de nouveaux produits.</span><span class="sxs-lookup"><span data-stu-id="ea230-145">For example, the research and development department of a manufacturing organization needs a SharePoint site to store current design specifications for existing products and a place to collaborate on new products.</span></span> <span data-ttu-id="ea230-146">Seuls les membres du service recherche et développement et des responsables sélectionnés peuvent accéder au site.</span><span class="sxs-lookup"><span data-stu-id="ea230-146">Only members of the Research & Development department and selected executives will be allowed to access the site.</span></span>

<span data-ttu-id="ea230-147">Cet objectif va permettre de déterminer les éléments de configuration essentiels, tels que les éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="ea230-147">That purpose will drive the determination of essential configuration items such as:</span></span>

- <span data-ttu-id="ea230-148">L'étiquette de rétention Office 365 à attribuer à la partie Documents du site et les stratégies DLP liées à l'étiquette</span><span class="sxs-lookup"><span data-stu-id="ea230-148">The Office 365 retention label to assign to the Documents portion of the site and DLP policies for the label</span></span>
- <span data-ttu-id="ea230-149">Les paramètres d’une sous-étiquette de sensibilité Office 365 que les utilisateurs appliquent aux fichiers hautement sensibles stockés sur le site</span><span class="sxs-lookup"><span data-stu-id="ea230-149">The settings of an Office 365 sensitivity sublabel that users apply to highly sensitive files stored in the site</span></span>

<span data-ttu-id="ea230-150">Une fois ces paramètres déterminés, utilisez-les pour configurer le site à la phase 2.</span><span class="sxs-lookup"><span data-stu-id="ea230-150">Once determined, you use these settings to configure the site in Phase 2.</span></span> 

### <a name="step-1-office-365-retention-labels-and-dlp-policies"></a><span data-ttu-id="ea230-151">Étape 1 : étiquettes de rétention Office 365 et stratégies DLP</span><span class="sxs-lookup"><span data-stu-id="ea230-151">Step 1 Office 365 retention labels and DLP policies</span></span>

<span data-ttu-id="ea230-152">Lorsqu’elles sont appliquées à la partie Documents du site d’équipe SharePoint, les étiquettes de rétention Office 365 fournissent une méthode par défaut de classification de toutes les fichiers stockées sur le site.</span><span class="sxs-lookup"><span data-stu-id="ea230-152">When applied to the Documents portion of a SharePoint team site, Office 365 retention labels provide a default method of classifying all files stored on the site.</span></span>
 
<span data-ttu-id="ea230-153">En ce qui concerne les sites SharePoint pour les données hautement réglementées, vous devez déterminer les étiquettes de rétention Office 365 à utiliser.</span><span class="sxs-lookup"><span data-stu-id="ea230-153">For SharePoint sites for highly regulated data, you need to determine which Office 365 retention label to use.</span></span>

<span data-ttu-id="ea230-154">Concernant les considérations relatives à la conception d’étiquettes Office 365, consultez la rubrique [Classification et étiquettes Office 365](https://docs.microsoft.com/office365/securitycompliance/secure-sharepoint-online-sites-and-files#office-365-retention-labels).</span><span class="sxs-lookup"><span data-stu-id="ea230-154">For the design considerations of Office 365 labels, see [Office 365 classification and labels](https://docs.microsoft.com/office365/securitycompliance/secure-sharepoint-online-sites-and-files#office-365-retention-labels).</span></span>

<span data-ttu-id="ea230-p103">Pour protéger les informations sensibles et empêcher leur divulgation accidentelle ou intentionnelle, vous pouvez utiliser des stratégies DLP. Pour obtenir plus d’informations, consultez cette [vue d’ensemble](https://docs.microsoft.com/office365/securitycompliance/data-loss-prevention-policies).</span><span class="sxs-lookup"><span data-stu-id="ea230-p103">To protect sensitive information and prevent its accidental or intentional disclosure, you use DLP policies. For more information, see this [overview](https://docs.microsoft.com/office365/securitycompliance/data-loss-prevention-policies).</span></span>

<span data-ttu-id="ea230-157">En ce qui concerne les sites SharePoint, vous devez configurer une stratégie DLP pour l’étiquette de rétention Office 365 attribuée au site afin de bloquer les utilisateurs lorsqu’ils essaient de partager des fichiers avec des utilisateurs externes.</span><span class="sxs-lookup"><span data-stu-id="ea230-157">For SharePoint sites, you must configure a DLP policy for the Office 365 retention label assigned to the site to block users when they attempt to share files with external users.</span></span> 

### <a name="step-2-your-office-365-sensitivity-sublabel"></a><span data-ttu-id="ea230-158">Étape 2 : sous-étiquette de sensibilité Office 365</span><span class="sxs-lookup"><span data-stu-id="ea230-158">Step 2: Your Office 365 sensitivity sublabel</span></span>

<span data-ttu-id="ea230-159">Pour fournir un chiffrement et un ensemble d’autorisations à vos fichiers les plus sensibles, les utilisateurs doivent appliquer une sous-étiquette ou une étiquette de sensibilité Office 365.</span><span class="sxs-lookup"><span data-stu-id="ea230-159">To provide encryption and a set of permissions to your most sensitive files, users must apply an Office 365 sensitivity sublabel.</span></span> <span data-ttu-id="ea230-160">Une sous-étiquette se trouve sous une étiquette existante.</span><span class="sxs-lookup"><span data-stu-id="ea230-160">A sublabel exists under an existing label.</span></span> 

<span data-ttu-id="ea230-161">Utilisez une étiquette de confidentialité lorsque vous avez besoin d’un petit nombre d’étiquettes pour un usage à la fois global et pour des équipes privées individuelles.</span><span class="sxs-lookup"><span data-stu-id="ea230-161">Use a sensitivity label when you need is a small number of labels for both global use and individual private teams.</span></span> <span data-ttu-id="ea230-162">Utilisez une sous-étiquette de confidentialité lorsque vous avez un grand nombre d’étiquettes ou si vous souhaitez organiser les étiquettes pour les sites sécurisés sous l’étiquette hautement réglementée.</span><span class="sxs-lookup"><span data-stu-id="ea230-162">Use a sensitivity sublabel when you have a large number of labels or want to organize labels for secure sites the under your highly regulated label.</span></span> 

<span data-ttu-id="ea230-163">Les paramètres de la sous-étiquette ou de l’étiquette appliquée accompagnent le fichier.</span><span class="sxs-lookup"><span data-stu-id="ea230-163">The settings of the applied sublabel travel with the file.</span></span> <span data-ttu-id="ea230-164">Même si elle est divulguée en dehors du site, seuls les comptes d’utilisateurs authentifiés disposant des autorisations appropriées peuvent l’ouvrir.</span><span class="sxs-lookup"><span data-stu-id="ea230-164">Even if it is leaked outside the site, only authenticated user accounts that have permissions can open it.</span></span>

### <a name="design-results"></a><span data-ttu-id="ea230-165">Résultats de conception</span><span class="sxs-lookup"><span data-stu-id="ea230-165">Design results</span></span>

<span data-ttu-id="ea230-166">Vous avez déterminé les éléments suivants:</span><span class="sxs-lookup"><span data-stu-id="ea230-166">You have determined the following:</span></span>

- <span data-ttu-id="ea230-167">L’étiquette de rétention Office 365 appropriée et la stratégie DLP associée à l’étiquette</span><span class="sxs-lookup"><span data-stu-id="ea230-167">The appropriate Office 365 retention label and the DLP policy that is associated with the label</span></span>
- <span data-ttu-id="ea230-168">Les paramètres de la sous-étiquette Office 365 comprenant le chiffrement et les autorisations</span><span class="sxs-lookup"><span data-stu-id="ea230-168">The settings of the Office 365 sensitivity sublabel that include encryption and permissions</span></span>

## <a name="phase-2-configure"></a><span data-ttu-id="ea230-169">Phase 2 : configuration</span><span class="sxs-lookup"><span data-stu-id="ea230-169">Phase 2: Configure</span></span>

<span data-ttu-id="ea230-170">Dans cette phase, vous prenez les paramètres déterminés à la phase 1 et les implémentez pour créer un site SharePoint pour les données hautement réglementées.</span><span class="sxs-lookup"><span data-stu-id="ea230-170">In this phase, you take the settings determined in Phase 1 and implement them to create a SharePoint site for highly regulated data.</span></span>

### <a name="step-1-create-a-private-sharepoint-team-site-with-owners-and-members-of-the-corresponding-office-365-group"></a><span data-ttu-id="ea230-171">Étape 1 : créer un site d’équipe SharePoint privé avec les propriétaires et les membres du groupe Office 365 correspondant</span><span class="sxs-lookup"><span data-stu-id="ea230-171">Step 1: Create a private SharePoint team site with owners and members of the corresponding Office 365 group</span></span>

<span data-ttu-id="ea230-172">Suivez [ces instructions]( https://support.office.com/article/create-a-site-in-sharepoint-online-4d1e11bf-8ddc-499d-b889-2b48d10b1ce8) pour créer un site d’équipe SharePoint privé.</span><span class="sxs-lookup"><span data-stu-id="ea230-172">Follow [these instructions]( https://support.office.com/article/create-a-site-in-sharepoint-online-4d1e11bf-8ddc-499d-b889-2b48d10b1ce8) to create a private SharePoint team site.</span></span>

### <a name="step-2-configure-additional-permissions-settings-for-the-sharepoint-team-site"></a><span data-ttu-id="ea230-173">Étape 2 : configurer les paramètres d’autorisations supplémentaires pour le site d’équipe SharePoint</span><span class="sxs-lookup"><span data-stu-id="ea230-173">Step 2: Configure additional permissions settings for the SharePoint team site</span></span>

<span data-ttu-id="ea230-174">À partir du site SharePoint, configurez ces paramètres d’autorisation.</span><span class="sxs-lookup"><span data-stu-id="ea230-174">From the SharePoint site, configure these permission settings.</span></span>

1. <span data-ttu-id="ea230-175">Dans la barre d’outils, cliquez sur l’icône Paramètres, puis cliquez sur **Paramètres du site**.</span><span class="sxs-lookup"><span data-stu-id="ea230-175">In the tool bar, click the settings icon, and then click **Site permissions**.</span></span>
2. <span data-ttu-id="ea230-176">Dans le volet **Autorisations de site**, sous **Paramètres de partage**, cliquez sur **Modifier les paramètres de partage**.</span><span class="sxs-lookup"><span data-stu-id="ea230-176">In the **Site permissions** pane, under **Sharing Settings**, click **Change sharing settings**.</span></span>
3. <span data-ttu-id="ea230-177">Sous **Autorisations de partage**, sélectionnez **Seuls les propriétaires du site peuvent partager des fichiers, des dossiers et le site**.</span><span class="sxs-lookup"><span data-stu-id="ea230-177">Under **Sharing permissions**, choose **Only site owners can share files, folders, and the site**.</span></span>
4. <span data-ttu-id="ea230-178">Désactivez **Autoriser les demandes d’accès**, puis cliquez sur **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="ea230-178">Turn off **Allow access requests**, and then click **Save**.</span></span>

<span data-ttu-id="ea230-179">Avec ces paramètres, la possibilité pour les membres du groupe de sites de partager le site avec d’autres membres ou pour les non-membres afin de demander l’accès au site est désactivée.</span><span class="sxs-lookup"><span data-stu-id="ea230-179">With these settings, the ability for site group members to share the site with other members or for non-members to request access to the site is disabled.</span></span>

### <a name="step-3-configure-the-site-for-an-office-365-retention-label"></a><span data-ttu-id="ea230-180">Étape 3 : configurer le site pour une étiquette de rétention Office 365</span><span class="sxs-lookup"><span data-stu-id="ea230-180">Step 3: Configure the site for an Office 365 retention label</span></span>

<span data-ttu-id="ea230-181">Suivez les instructions mentionnées dans [Protéger les fichiers SharePoint avec les étiquettes Office 365 et la protection contre la perte de données (DLP)](https://docs.microsoft.com/office365/enterprise/protect-sharepoint-online-files-with-office-365-labels-and-dlp) pour :</span><span class="sxs-lookup"><span data-stu-id="ea230-181">Use the instructions in [Protect SharePoint files with Office 365 labels and DLP](https://docs.microsoft.com/office365/enterprise/protect-sharepoint-online-files-with-office-365-labels-and-dlp) to:</span></span>

1. <span data-ttu-id="ea230-182">Créer et publier une étiquette de rétention pour les données hautement réglementées (le cas échéant).</span><span class="sxs-lookup"><span data-stu-id="ea230-182">Create and publish a retention label for highly regulated data (if needed).</span></span>
2. <span data-ttu-id="ea230-183">Configurez le site pour l’étiquette de rétention créée à l’étape 1.</span><span class="sxs-lookup"><span data-stu-id="ea230-183">Configure the site for the retention label created in step 1.</span></span>
3. <span data-ttu-id="ea230-184">Créez une stratégie DLP pour les données hautement réglementées qui utilise l’étiquette de rétention créée à l’étape 2 et qui empêche les utilisateurs d’envoyer des fichiers à l’extérieur de l’Organisation</span><span class="sxs-lookup"><span data-stu-id="ea230-184">Create a DLP policy for highly regulated data that uses the retention label created in step 2 and blocks users from sending files outside the organization</span></span>

#### <a name="step-4-create-an-office-365-sensitivity-sublabel-for-the-site"></a><span data-ttu-id="ea230-185">Étape 4 : créer une sous-étiquette de sensibilité dans Office 365 pour le site</span><span class="sxs-lookup"><span data-stu-id="ea230-185">Step 4: Create an Office 365 sensitivity sublabel for the site</span></span>

<span data-ttu-id="ea230-186">Contrairement à une étiquette de sensibilité pour les données hautement réglementées qu’une personne peut appliquer à n’importe quel fichier, un site sécurisé nécessite sa propre sous-étiquette de sorte que les fichiers auxquels la sous-étiquette est attribuée :</span><span class="sxs-lookup"><span data-stu-id="ea230-186">Unlike a sensitivity label for highly regulated data that anyone can apply to any file, a secure site needs its own sublabel so that files with the sublabel assigned:</span></span>

- <span data-ttu-id="ea230-187">Sont chiffrés et le chiffrement est acheminé avec le fichier.</span><span class="sxs-lookup"><span data-stu-id="ea230-187">Are encrypted and the encryption travels with the file.</span></span>
- <span data-ttu-id="ea230-188">Contiennent des autorisations personnalisées de sorte que seuls les membres du groupe de sites puissent l’ouvrir.</span><span class="sxs-lookup"><span data-stu-id="ea230-188">Contain custom permissions so that only members of the site group can open it.</span></span>

<span data-ttu-id="ea230-189">Pour atteindre ce niveau de sécurité supplémentaire pour les fichiers stockés sur le site, vous devez configurer une nouvelle étiquette de sensibilité ou une sous-étiquette de l’étiquette général pour les fichiers hautement réglementés.</span><span class="sxs-lookup"><span data-stu-id="ea230-189">To accomplish this additional level of security for files stored in the site, you must configure a new sensitivity label that is a sublabel of the general label for highly regulated files.</span></span> <span data-ttu-id="ea230-190">Seuls les membres du groupe pour le site peuvent le voir dans la liste des sous-étiquettes pour l’étiquette hautement réglementée.</span><span class="sxs-lookup"><span data-stu-id="ea230-190">Only group members for the site will see it in the list of sublabels for the highly regulated label.</span></span>

<span data-ttu-id="ea230-191">Utilisez les instructions [ici](https://docs.microsoft.com/microsoft-365/compliance/encryption-sensitivity-labels) pour configurer une sous-étiquette ou une étiquette que vous utilisez pour les fichiers hautement réglementés avec les paramètres suivants :</span><span class="sxs-lookup"><span data-stu-id="ea230-191">Use the instructions [here](https://docs.microsoft.com/microsoft-365/compliance/encryption-sensitivity-labels) to configure a sublabel of the label you are using for highly regulated files with the following settings:</span></span>

- <span data-ttu-id="ea230-192">Le nom de l’étiquette ou de la sous-étiquette contient le nom du site pour simplifier l’association lors de l’attribution de l’étiquette ou de la sous-étiquette à un fichier.</span><span class="sxs-lookup"><span data-stu-id="ea230-192">The name of the sublabel contains the name of the site for easy association when assign the sublabel to a file.</span></span>
- <span data-ttu-id="ea230-193">Le chiffrement est activé.</span><span class="sxs-lookup"><span data-stu-id="ea230-193">Encryption is enabled.</span></span>
- <span data-ttu-id="ea230-194">Le groupe de sites possède des autorisations de co-création.</span><span class="sxs-lookup"><span data-stu-id="ea230-194">The site group has Co-Author permissions.</span></span>

### <a name="configuration-results"></a><span data-ttu-id="ea230-195">Résultats de la configuration</span><span class="sxs-lookup"><span data-stu-id="ea230-195">Configuration results</span></span>

<span data-ttu-id="ea230-196">Vous avez configuré les éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="ea230-196">You have configured the following:</span></span>

- <span data-ttu-id="ea230-197">Paramètres d’autorisation plus restrictifs sur le site SharePoint</span><span class="sxs-lookup"><span data-stu-id="ea230-197">More restrictive permission settings on the SharePoint site</span></span>
- <span data-ttu-id="ea230-198">Une étiquette de rétention Office 365 attribuée à la partie Documents du site SharePoint</span><span class="sxs-lookup"><span data-stu-id="ea230-198">An Office 365 retention label assigned to the Documents portion of the SharePoint site</span></span>
- <span data-ttu-id="ea230-199">Une stratégie DLP pour l’étiquette de rétention Office 365</span><span class="sxs-lookup"><span data-stu-id="ea230-199">A DLP policy for the Office 365 retention label</span></span>
- <span data-ttu-id="ea230-200">Une sous-étiquette de sensibilité Office 365 que les utilisateurs peuvent appliquer aux fichiers les plus sensibles stockés sur le site, qui chiffre le fichier et autorise uniquement l’accès de co-création pour les membres du groupe de site d’équipe</span><span class="sxs-lookup"><span data-stu-id="ea230-200">An Office 365 sensitivity sublabel that users can apply to the most sensitive files stored in the site that encrypts the file and only allows Co-Author access for members of the team site group</span></span> 

<span data-ttu-id="ea230-201">Voici la configuration obtenue qui utilise une sous-étiquette de l’étiquette hautement réglementée.</span><span class="sxs-lookup"><span data-stu-id="ea230-201">Here is the resulting configuration that uses a sublabel of the Highly regulated label.</span></span>

![Les sites SharePoint pour les scénarios de données hautement réglementés](./media/teams-sharepoint-online-sites-highly-regulated-data/end-to-end-configuration.png)

<span data-ttu-id="ea230-203">Voici un exemple d’utilisateur ayant appliqué la sous-étiquette à un fichier stocké sur le site.</span><span class="sxs-lookup"><span data-stu-id="ea230-203">Here is an example of a user that has applied the sensitivity sublabel to a file stored in the site.</span></span>

![Les sites SharePoint pour les scénarios de données hautement réglementés](./media/teams-sharepoint-online-sites-highly-regulated-data/end-to-end-configuration-example-file.png)


## <a name="phase-3-drive-user-adoption"></a><span data-ttu-id="ea230-205">Étape 3 : favoriser l’adoption utilisateur</span><span class="sxs-lookup"><span data-stu-id="ea230-205">Phase 3: Drive user adoption</span></span>

<span data-ttu-id="ea230-206">Un site SharePoint pour les données hautement réglementées ne peut protéger ces données que s’il est utilisé de façon cohérente pour le stockage et l’accès aux fichiers sensibles.</span><span class="sxs-lookup"><span data-stu-id="ea230-206">A SharePoint site for highly regulated data can only protect that data if it is consistently used for storage and access of sensitive files.</span></span> <span data-ttu-id="ea230-207">Il s’agit de la phase la plus difficile, car elle s’appuie sur les utilisateurs qui modifient leurs habitudes et leurs préférences.</span><span class="sxs-lookup"><span data-stu-id="ea230-207">This is the hardest phase because it relies on users changing their habits and preferences.</span></span> 

<span data-ttu-id="ea230-208">Par exemple, les employés habitués à stocker des fichiers sensibles sur des lecteurs USB ou des solutions de stockage personnelles basées sur le Cloud devront désormais les stocker exclusivement sur un site SharePoint pour les données hautement réglementées.</span><span class="sxs-lookup"><span data-stu-id="ea230-208">For example, employees that are used to storing sensitive files on USB drives or on personal cloud-based storage solutions will now have to store them exclusively in a SharePoint site for highly regulated data.</span></span>

### <a name="step-1-train-your-users"></a><span data-ttu-id="ea230-209">Étape 1 : former vos utilisateurs</span><span class="sxs-lookup"><span data-stu-id="ea230-209">Step 1: Train your users</span></span>

<span data-ttu-id="ea230-210">Après avoir effectué votre configuration, formez l’ensemble des utilisateurs qui sont membres du site :</span><span class="sxs-lookup"><span data-stu-id="ea230-210">After completing your configuration, train the set of users who are members of the site access groups:</span></span>

- <span data-ttu-id="ea230-211">Sur l’importance de l’utilisation du nouveau site pour protéger les fichiers précieux et les conséquences de la fuite de données hautement réglementées, telles que des conséquences juridiques, des amendes réglementaires, des logiciels rançonneurs ou la perte de l’avantage concurrentiel.</span><span class="sxs-lookup"><span data-stu-id="ea230-211">On the importance of using the new site to protect valuable files and the consequences of a highly regulated data leak, such as legal ramifications, regulatory fines, ransomware, or loss of competitive advantage.</span></span>
- <span data-ttu-id="ea230-212">Accès au site et aux fichiers.</span><span class="sxs-lookup"><span data-stu-id="ea230-212">How to access the site and its files.</span></span>
- <span data-ttu-id="ea230-213">Création de nouveaux fichiers sur le site et chargement de nouveaux fichiers stockés localement.</span><span class="sxs-lookup"><span data-stu-id="ea230-213">How to create new files on the site and upload new files stored locally.</span></span>
- <span data-ttu-id="ea230-214">Blocage du partage des fichiers en externe par la stratégie DLP.</span><span class="sxs-lookup"><span data-stu-id="ea230-214">How the DLP policy blocks them from sharing files externally.</span></span>
- <span data-ttu-id="ea230-215">Comment étiqueter les fichiers les plus sensibles avec l’étiquette ou la sous-étiquette du site.</span><span class="sxs-lookup"><span data-stu-id="ea230-215">How to label the most sensitive files with the sublabel for the site.</span></span>
- <span data-ttu-id="ea230-216">Comment l’étiquette ou la sous-étiquette protège un fichier même lorsque celui-ci a été divulgué hors du site.</span><span class="sxs-lookup"><span data-stu-id="ea230-216">How the sublabel protects a file even when it is leaked off the site.</span></span>

<span data-ttu-id="ea230-217">Cette formation doit inclure des exercices pratiques pour que les utilisateurs puissent effectuer ces opérations et observer leurs résultats.</span><span class="sxs-lookup"><span data-stu-id="ea230-217">This training should include hands-on exercises so that the users can experience these operations and their results.</span></span>

### <a name="step-2-conduct-periodic-reviews-of-usage-and-files"></a><span data-ttu-id="ea230-218">Étape 2 : conduire des vérifications périodiques de l’utilisation et des fichiers</span><span class="sxs-lookup"><span data-stu-id="ea230-218">Step 2: Conduct periodic reviews of usage and files</span></span>

<span data-ttu-id="ea230-219">Au cours des semaines après la formation, l’Administrateur de services SharePoint du site SharePoint peut effectuer les actions suivantes :</span><span class="sxs-lookup"><span data-stu-id="ea230-219">In the weeks after training, the SharePoint administrator for the SharePoint site can:</span></span>

- <span data-ttu-id="ea230-220">Analyser l’utilisation du site et les comparer avec les attentes de l’utilisation.</span><span class="sxs-lookup"><span data-stu-id="ea230-220">Analyze usage for the site and compare it with usage expectations.</span></span>
- <span data-ttu-id="ea230-221">Vérifier que les fichiers hautement sensibles ont été correctement étiquetés avec l’étiquette ou la sous-étiquette de sensibilité.</span><span class="sxs-lookup"><span data-stu-id="ea230-221">Verify that highly sensitive files have been properly labeled with the sensitivity sublabel.</span></span>

  <span data-ttu-id="ea230-222">Vous pouvez voir quels fichiers disposent d'une étiquette attribuée en affichant un dossier dans SharePoint Online et en ajoutant la colonne **Confidentialité** via l'option **Afficher/masquer les colonnes** de **Ajouter un colonne**.</span><span class="sxs-lookup"><span data-stu-id="ea230-222">You can see which files have a label assigned by viewing a folder in SharePoint and adding the **Sensitivity** column through the **Show/hide columns** option of **Add column**.</span></span>


<span data-ttu-id="ea230-223">Former à nouveau vos utilisateurs, le cas échéant.</span><span class="sxs-lookup"><span data-stu-id="ea230-223">Retrain your users as needed.</span></span>

### <a name="user-adoption-results"></a><span data-ttu-id="ea230-224">Résultats de l’adoption par les utilisateurs</span><span class="sxs-lookup"><span data-stu-id="ea230-224">User adoption results</span></span>

<span data-ttu-id="ea230-225">Les fichiers hautement réglementés sont stockés exclusivement sur des sites SharePoint pour des données hautement réglementées, et les fichiers les plus sensibles ont une étiquette ou une sous-étiquette de sensibilité pour le site appliqué.</span><span class="sxs-lookup"><span data-stu-id="ea230-225">Highly regulated files are stored exclusively on SharePoint sites for highly regulated data and the most sensitive files have the sensitivity sublabel for the site applied.</span></span>

## <a name="how-the-contoso-corporation-deployed-microsoft-365-enterprise"></a><span data-ttu-id="ea230-226">Comment Contoso Corporation a déployé Microsoft 365 Entreprise</span><span class="sxs-lookup"><span data-stu-id="ea230-226">How the Contoso Corporation deployed Microsoft 365 Enterprise</span></span>

<span data-ttu-id="ea230-227">Contoso Corporation est un conglomérat de fabricants international fictif mais représentatif.</span><span class="sxs-lookup"><span data-stu-id="ea230-227">The Contoso Corporation is a fictional but representative global manufacturing conglomerate with its headquarters in Paris, France.</span></span> <span data-ttu-id="ea230-228">Découvrez comment Contoso a conçu, configuré, puis piloté l’adoption d’un [site SharePoint sécurisé](contoso-sharepoint-online-site-for-highly-confidential-assets.md) pour ses équipes de recherche basées à Paris, Moscou, New York, Beijing et Bengaluru.</span><span class="sxs-lookup"><span data-stu-id="ea230-228">See how Contoso designed, configured, and then drove the adoption of a [secure SharePoint site](contoso-sharepoint-online-site-for-highly-confidential-assets.md) for their research teams in Paris, Moscow, New York, Beijing, and Bangalore.</span></span> 

## <a name="see-also"></a><span data-ttu-id="ea230-229">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ea230-229">See also</span></span>

[<span data-ttu-id="ea230-230">Microsoft Teams pour les données hautement réglementées</span><span class="sxs-lookup"><span data-stu-id="ea230-230">Microsoft Teams for highly regulated data</span></span>](secure-teams-highly-regulated-data-scenario.md)

[<span data-ttu-id="ea230-231">Scénarios et charges de travail Microsoft 365 Entreprise</span><span class="sxs-lookup"><span data-stu-id="ea230-231">Microsoft 365 Enterprise workloads and scenarios</span></span>](deploy-workloads.md)

<span data-ttu-id="ea230-232">[Bibliothèque de productivité Microsoft 365](https://aka.ms/productivitylibrary)https://aka.ms/productivitylibrary)</span><span class="sxs-lookup"><span data-stu-id="ea230-232">[Microsoft 365 Productivity Library](https://aka.ms/productivitylibrary) (https://aka.ms/productivitylibrary)</span></span>

[<span data-ttu-id="ea230-233">Guide de déploiement</span><span class="sxs-lookup"><span data-stu-id="ea230-233">Deployment guide</span></span>](deploy-microsoft-365-enterprise.md)
