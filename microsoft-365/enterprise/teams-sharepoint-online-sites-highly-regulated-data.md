---
title: Sites SharePoint pour les données hautement réglementées
author: JoeDavies-MSFT
ms.author: josephd
manager: laurawi
ms.date: 10/04/2019
audience: ITPro
ms.topic: article
ms.service: o365-solutions
localization_priority: Priority
ms.collection:
- M365-security-compliance
- Strat_O365_Enterprise
ms.custom: ''
description: Créez un site d’équipe SharePoint sécurisé pour stocker vos fichiers les plus précieux et les plus sensibles.
ms.openlocfilehash: dc604870826075cee645dd466b82f908e1571339
ms.sourcegitcommit: e1ffb98ac8159d1dc814930fe388d3e37cbdc7e2
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/05/2019
ms.locfileid: "37403179"
---
# <a name="sharepoint-sites-for-highly-regulated-data"></a><span data-ttu-id="e66eb-103">Sites SharePoint pour les données hautement réglementées</span><span class="sxs-lookup"><span data-stu-id="e66eb-103">Microsoft Teams and SharePoint Online sites for highly regulated data</span></span>

<span data-ttu-id="e66eb-104">*Ce scénario s’applique à la fois aux versions E3 et E5 de Microsoft 365 Entreprise*</span><span class="sxs-lookup"><span data-stu-id="e66eb-104">*This scenario applies to both the E3 and E5 versions of Microsoft 365 Enterprise*</span></span>

<span data-ttu-id="e66eb-p101">Microsoft 365 Entreprise comprend une suite complète de services basés sur le Cloud afin que vous puissiez créer, stocker et sécuriser vos données hautement réglementées, notamment les données qui sont :</span><span class="sxs-lookup"><span data-stu-id="e66eb-p101">Microsoft 365 Enterprise includes a full suite of cloud-based services so that you can create, store, and secure your highly regulated data. This includes data that is:</span></span>

- <span data-ttu-id="e66eb-107">sujettes à des réglementations régionales ;</span><span class="sxs-lookup"><span data-stu-id="e66eb-107">Subject to regional regulations.</span></span>
- <span data-ttu-id="e66eb-108">les plus précieuses de votre organisation comme les secrets commerciaux, les informations sur les ressources humaines ou financières et la stratégie de l’organisation.</span><span class="sxs-lookup"><span data-stu-id="e66eb-108">The most valuable data for your organization, such as trade secrets, financial or human resources information, and organization strategy.</span></span>

<span data-ttu-id="e66eb-109">Dans le cadre d’un scénario Microsoft 365 Entreprise basé sur le cloud qui répond à ce besoin métier, vous êtes tenu de suivre les instructions suivantes :</span><span class="sxs-lookup"><span data-stu-id="e66eb-109">A Microsoft 365 Enterprise cloud-based scenario that meets this business need requires that you:</span></span>

- <span data-ttu-id="e66eb-110">Stockez des fichiers (documents, diapositives, feuilles de calcul, etc.) dans un site d’équipe SharePoint.</span><span class="sxs-lookup"><span data-stu-id="e66eb-110">Store digital assets (documents, slide decks, spreadsheets, etc.) in a SharePoint Online team site or in the Files tab of a Microsoft Teams team.</span></span>
- <span data-ttu-id="e66eb-111">Verrouillez le site pour empêcher :</span><span class="sxs-lookup"><span data-stu-id="e66eb-111">Lock down the site or team to prevent:</span></span>
  - <span data-ttu-id="e66eb-112">L’accès aux utilisateurs qui ne sont pas membres du groupe Office 365 pour le site.</span><span class="sxs-lookup"><span data-stu-id="e66eb-112">Access to users who are not members of the Office 365 group for the site.</span></span>
  - <span data-ttu-id="e66eb-113">les membres du site d’octroyer l’accès à d’autres personnes ;</span><span class="sxs-lookup"><span data-stu-id="e66eb-113">Members of the site from granting access to others.</span></span>
  - <span data-ttu-id="e66eb-114">l’accès au site par les personnes non membres.</span><span class="sxs-lookup"><span data-stu-id="e66eb-114">Non-members of the site from requesting access to the site.</span></span>
- <span data-ttu-id="e66eb-115">Configurez une étiquette de rétention Office 365 pour vos sites SharePoint comme moyen par défaut pour empêcher les utilisateurs d’envoyer des fichiers à l’extérieur de l’organisation.</span><span class="sxs-lookup"><span data-stu-id="e66eb-115">Configure an Office 365 retention label for your SharePoint sites as a default way to block users from sending files outside the organization.</span></span>
- <span data-ttu-id="e66eb-116">Chiffrer les fichiers les plus sensibles du site avec le chiffrement qui accompagne le fichier.</span><span class="sxs-lookup"><span data-stu-id="e66eb-116">Encrypt the most sensitive files of the site with encryption that travels with the file.</span></span>
- <span data-ttu-id="e66eb-117">Ajoutez des autorisations aux fichiers les plus sensibles de sorte que même s'ils sont partagés en dehors du site, leur ouverture nécessite toujours les informations d’identification valides d’un compte d’utilisateur autorisé.</span><span class="sxs-lookup"><span data-stu-id="e66eb-117">Add permissions to the most sensitive digital assets so that if even if they get shared outside of the site, opening the asset still requires the valid credentials of a user account that has permission.</span></span>

<span data-ttu-id="e66eb-118">Le tableau suivant mappe les conditions requises de ce scénario à une fonctionnalité de Microsoft 365 Entreprise.</span><span class="sxs-lookup"><span data-stu-id="e66eb-118">The following table maps the requirements of this scenario to a feature of Microsoft 365 Enterprise.</span></span>

|||
|:-------|:-----|
| <span data-ttu-id="e66eb-119">**Configuration requise**</span><span class="sxs-lookup"><span data-stu-id="e66eb-119">**Requirement**</span></span> | <span data-ttu-id="e66eb-120">**Fonctionnalité Microsoft 365 Entreprise**</span><span class="sxs-lookup"><span data-stu-id="e66eb-120">**Microsoft 365 Enterprise feature**</span></span> |
| <span data-ttu-id="e66eb-121">Stocker des fichiers</span><span class="sxs-lookup"><span data-stu-id="e66eb-121">Store files online</span></span> | <span data-ttu-id="e66eb-122">Sites d’équipe SharePoint</span><span class="sxs-lookup"><span data-stu-id="e66eb-122">Sensitive SharePoint Online team sites</span></span> |
| <span data-ttu-id="e66eb-123">Verrouiller le site</span><span class="sxs-lookup"><span data-stu-id="e66eb-123">Lock down the site</span></span> | <span data-ttu-id="e66eb-124">Autorisations de sites d’équipe SharePoint et de groupes Microsoft Azure Active Directory</span><span class="sxs-lookup"><span data-stu-id="e66eb-124">Azure Active Directory (Azure AD) groups and SharePoint team site permissions</span></span> |
| <span data-ttu-id="e66eb-125">Étiqueter les fichiers du site</span><span class="sxs-lookup"><span data-stu-id="e66eb-125">Label the digital assets of the site</span></span> | <span data-ttu-id="e66eb-126">Étiquettes de rétention Office 365</span><span class="sxs-lookup"><span data-stu-id="e66eb-126">Office 365 retention labels</span></span> |
| <span data-ttu-id="e66eb-127">Bloquer les utilisateurs lors de l’envoi de fichiers à l’extérieur de l’organisation</span><span class="sxs-lookup"><span data-stu-id="e66eb-127">Block users when sending files outside the organization</span></span> | <span data-ttu-id="e66eb-128">Stratégies de protection contre la perte de données (DLP) dans Office 365</span><span class="sxs-lookup"><span data-stu-id="e66eb-128">Data Loss Prevention (DLP) policies in Office 365</span></span> |
| <span data-ttu-id="e66eb-129">Chiffrer tous les fichiers du site</span><span class="sxs-lookup"><span data-stu-id="e66eb-129">Encrypt all of the digital assets of the site</span></span> | <span data-ttu-id="e66eb-130">Sous-étiquettes de sensibilité Office 365</span><span class="sxs-lookup"><span data-stu-id="e66eb-130">Office 365 sensitivity sublabels</span></span> |
| <span data-ttu-id="e66eb-131">Ajouter des autorisations aux fichiers du site</span><span class="sxs-lookup"><span data-stu-id="e66eb-131">Add permissions to the digital assets of the site</span></span> | <span data-ttu-id="e66eb-132">Sous-étiquettes de sensibilité Office 365</span><span class="sxs-lookup"><span data-stu-id="e66eb-132">Office 365 sensitivity sublabels</span></span> |
|||

<span data-ttu-id="e66eb-133">Voici la configuration d’un site SharePoint sécurisé.</span><span class="sxs-lookup"><span data-stu-id="e66eb-133">Here is the configuration for a SharePoint Online site.</span></span>

![Les sites SharePoint pour les scénarios de données hautement réglementés](./media/teams-sharepoint-online-sites-highly-regulated-data/end-to-end-configuration.png)

<span data-ttu-id="e66eb-135">Ce scénario implique que vous ayez déjà déployé les éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="e66eb-135">This scenario requires that you have already deployed:</span></span>

- <span data-ttu-id="e66eb-136">La phase [Identité](identity-infrastructure.md) et les étapes 1 et 2 de la phase [Protection des informations](infoprotect-infrastructure.md) de l’infrastructure de base.</span><span class="sxs-lookup"><span data-stu-id="e66eb-136">The [Identity](identity-infrastructure.md) phase and steps 1 and 2 of the [Information protection](infoprotect-infrastructure.md) phase of the foundation infrastructure.</span></span> 
- <span data-ttu-id="e66eb-137">[SharePoint](sharepoint-online-onedrive-workload.md).</span><span class="sxs-lookup"><span data-stu-id="e66eb-137">SharePoint</span></span>

<span data-ttu-id="e66eb-138">Les phases suivantes vous guident à travers toute la conception, la configuration et le pilotage de l'adoption des sites SharePoint pour les données hautement réglementées.</span><span class="sxs-lookup"><span data-stu-id="e66eb-138">The following phases step you through designing, configuring, and driving adoption for SharePoint Online sites and teams for highly regulated data.</span></span>

<span data-ttu-id="e66eb-139">Pour découvrir comment Contoso Corporation, une organisation multinationale fictive mais représentative, a conçu un site SharePoint pour ses équipes de recherche, consultez cette [configuration exemple](contoso-sharepoint-online-site-for-highly-confidential-assets.md).</span><span class="sxs-lookup"><span data-stu-id="e66eb-139">To see how the Contoso Corporation, a fictional but representative multi-national organization, designed a SharePoint Online site for its research teams, see this [example configuration](contoso-sharepoint-online-site-for-highly-confidential-assets.md).</span></span>

## <a name="identity-and-device-access-prerequisites"></a><span data-ttu-id="e66eb-140">Conditions préalables pour les identités et l’accès aux appareils</span><span class="sxs-lookup"><span data-stu-id="e66eb-140">Identity and device access prerequisites</span></span>

<span data-ttu-id="e66eb-141">Pour protéger l’accès aux sites SharePoint, vérifiez que vous avez configuré les [stratégies pour les identités et l’accès aux appareils](identity-access-policies.md) et les [stratégies d’accès à SharePoint recommandées](sharepoint-file-access-policies.md).</span><span class="sxs-lookup"><span data-stu-id="e66eb-141">To protect access to the team or SharePoint Online site, ensure that you have configured [identity and device access policies](identity-access-policies.md) and the [recommended SharePoint Online access policies](sharepoint-file-access-policies.md).</span></span>

## <a name="phase-1-design"></a><span data-ttu-id="e66eb-142">Phase 1 : conception</span><span class="sxs-lookup"><span data-stu-id="e66eb-142">Phase 1: Design</span></span>

<span data-ttu-id="e66eb-143">Pour créer un site SharePoint pour les données hautement réglementées, vous devez commencer par identifier son objet.</span><span class="sxs-lookup"><span data-stu-id="e66eb-143">To create a SharePoint site for highly regulated data, you must first identify its purpose.</span></span> <span data-ttu-id="e66eb-144">Par exemple, le département recherche et développement d’une organisation de production a besoin d’un site SharePoint pour stocker les spécifications de conception actuelles des produits existants et un emplacement pour collaborer à de nouveaux produits.</span><span class="sxs-lookup"><span data-stu-id="e66eb-144">To create a SharePoint Online site or team for highly regulated data, you must first identify its purpose. For example, the research and development department of a manufacturing organization needs a SharePoint Online site to store current design specifications for existing products and a place to collaborate on new products. Only members of the Research & Development department and selected executives will be allowed to access the site.</span></span> <span data-ttu-id="e66eb-145">Seuls les membres du service recherche et développement et des responsables sélectionnés peuvent accéder au site.</span><span class="sxs-lookup"><span data-stu-id="e66eb-145">Only members of the Research & Development department and selected executives will be allowed to access the site.</span></span>

<span data-ttu-id="e66eb-146">Cet objectif va permettre de déterminer les éléments de configuration essentiels, tels que les éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="e66eb-146">That purpose will drive the determination of essential configuration items such as:</span></span>

- <span data-ttu-id="e66eb-147">L'étiquette de rétention Office 365 à attribuer à la partie Documents du site et les stratégies DLP liées à l'étiquette</span><span class="sxs-lookup"><span data-stu-id="e66eb-147">The Office 365 retention label to assign to the site and the set of DLP policies for the label</span></span>
- <span data-ttu-id="e66eb-148">Les paramètres d’une sous-étiquette de sensibilité Office 365 que les utilisateurs appliquent aux fichiers hautement sensibles stockés sur le site</span><span class="sxs-lookup"><span data-stu-id="e66eb-148">The settings of an Office 365 sensitivity sublabel that users apply to highly sensitive files stored in the site</span></span>

<span data-ttu-id="e66eb-149">Une fois ces paramètres déterminés, utilisez-les pour configurer le site à la phase 2.</span><span class="sxs-lookup"><span data-stu-id="e66eb-149">Once determined, you use these settings to configure the site in Phase 2.</span></span> 

### <a name="step-1-office-365-retention-labels-and-dlp-policies"></a><span data-ttu-id="e66eb-150">Étape 1 : étiquettes de rétention Office 365 et stratégies DLP</span><span class="sxs-lookup"><span data-stu-id="e66eb-150">Step 2: Office 365 retention labels and DLP policies</span></span>

<span data-ttu-id="e66eb-151">Lorsqu’elles sont appliquées à la partie Documents du site d’équipe SharePoint, les étiquettes de rétention Office 365 fournissent une méthode par défaut de classification de toutes les fichiers stockées sur le site.</span><span class="sxs-lookup"><span data-stu-id="e66eb-151">When applied to a SharePoint Online team site, Office 365 retention labels provide a default method of classifying all digital assets stored on the site.</span></span>
 
<span data-ttu-id="e66eb-152">En ce qui concerne les sites SharePoint pour les données hautement réglementées, vous devez déterminer les étiquettes de rétention Office 365 à utiliser.</span><span class="sxs-lookup"><span data-stu-id="e66eb-152">For SharePoint Online sites for highly regulated data, you need to determine which Office 365 retention label to use.</span></span>

<span data-ttu-id="e66eb-153">Concernant les considérations relatives à la conception d’étiquettes Office 365, consultez la rubrique [Classification et étiquettes Office 365](https://docs.microsoft.com/office365/securitycompliance/secure-sharepoint-online-sites-and-files#office-365-retention-labels).</span><span class="sxs-lookup"><span data-stu-id="e66eb-153">For the design considerations of Office 365 labels, see [Office 365 classification and labels](https://docs.microsoft.com/office365/securitycompliance/secure-sharepoint-online-sites-and-files#office-365-retention-labels).</span></span>

<span data-ttu-id="e66eb-p103">Pour protéger les informations sensibles et empêcher leur divulgation accidentelle ou intentionnelle, vous pouvez utiliser des stratégies DLP. Pour obtenir plus d’informations, consultez cette [vue d’ensemble](https://docs.microsoft.com/office365/securitycompliance/data-loss-prevention-policies).</span><span class="sxs-lookup"><span data-stu-id="e66eb-p103">To protect sensitive information and prevent its accidental or intentional disclosure, you use DLP policies. For more information, see this [overview](https://docs.microsoft.com/office365/securitycompliance/data-loss-prevention-policies).</span></span>

<span data-ttu-id="e66eb-156">En ce qui concerne les sites SharePoint, vous devez configurer une stratégie DLP pour l’étiquette de rétention Office 365 attribuée au site afin de bloquer les utilisateurs lorsqu’ils essaient de partager des fichiers avec des utilisateurs externes.</span><span class="sxs-lookup"><span data-stu-id="e66eb-156">For SharePoint Online sites for highly regulated data, you must configure a DLP policy for the Office 365 retention label assigned to the site to block users when they attempt to share digital assets with external users.</span></span> 

### <a name="step-2-your-office-365-sensitivity-sublabel"></a><span data-ttu-id="e66eb-157">Étape 2 : sous-étiquette de sensibilité Office 365</span><span class="sxs-lookup"><span data-stu-id="e66eb-157">Step 2: Your Office 365 sensitivity sublabel</span></span>

<span data-ttu-id="e66eb-158">Pour fournir un chiffrement et un ensemble d’autorisations à vos fichiers les plus sensibles, les utilisateurs doivent appliquer une sous-étiquette de sensibilité Office 365.</span><span class="sxs-lookup"><span data-stu-id="e66eb-158">To provide encryption and a set of permissions to your most sensitive files, users must apply an Office 365 sensitivity sublabel.</span></span>

<span data-ttu-id="e66eb-159">Une sous-étiquette se trouve sous une étiquette existante.</span><span class="sxs-lookup"><span data-stu-id="e66eb-159">A sublabel exists under an existing label.</span></span> <span data-ttu-id="e66eb-160">Par exemple, vous pouvez créer une sous-étiquette de recherche et développement sous l’étiquette hautement réglementée.</span><span class="sxs-lookup"><span data-stu-id="e66eb-160">For example, you can create a Research & Development sublabel under the Highly Regulated label.</span></span> <span data-ttu-id="e66eb-161">Pour les sites SharePoint pour les données hautement réglementées, vous configurez les autorisations de sorte que seuls les membres du site puissent ouvrir et modifier le fichier auquel la sous-étiquette est jointe.</span><span class="sxs-lookup"><span data-stu-id="e66eb-161">For SharePoint sites for highly regulated data, you configure the permissions so that only site members can open and change the file to which the sublabel is attached.</span></span>

<span data-ttu-id="e66eb-162">Les paramètres de la sous-étiquette appliquée accompagnent le fichier.</span><span class="sxs-lookup"><span data-stu-id="e66eb-162">The settings of the applied sublabel travel with the file.</span></span> <span data-ttu-id="e66eb-163">Même si elle est divulguée en dehors du site, seuls les comptes d’utilisateurs authentifiés disposant des autorisations appropriées peuvent l’ouvrir.</span><span class="sxs-lookup"><span data-stu-id="e66eb-163">The settings of the applied sub-label travel with the asset. Even if it is downloaded and shared outside the site, only authenticated user accounts that have permissions can open it.</span></span>


### <a name="design-results"></a><span data-ttu-id="e66eb-164">Résultats de conception</span><span class="sxs-lookup"><span data-stu-id="e66eb-164">Design results</span></span>

<span data-ttu-id="e66eb-165">Vous avez déterminé les éléments suivants:</span><span class="sxs-lookup"><span data-stu-id="e66eb-165">You have determined the following:</span></span>

- <span data-ttu-id="e66eb-166">L’étiquette de rétention Office 365 appropriée et la stratégie DLP associée à l’étiquette</span><span class="sxs-lookup"><span data-stu-id="e66eb-166">The appropriate Office 365 retention label and the DLP policy that is associated with the label</span></span>
- <span data-ttu-id="e66eb-167">Les paramètres de la sous-étiquette Office 365 comprenant le chiffrement et les autorisations</span><span class="sxs-lookup"><span data-stu-id="e66eb-167">The settings of the Office 365 sensitivity sublabel that include encryption and permissions</span></span>

## <a name="phase-2-configure"></a><span data-ttu-id="e66eb-168">Phase 2 : configuration</span><span class="sxs-lookup"><span data-stu-id="e66eb-168">Phase 2: Configure</span></span>

<span data-ttu-id="e66eb-169">Dans cette phase, vous prenez les paramètres déterminés à la phase 1 et les implémentez pour créer un site SharePoint pour les données hautement réglementées.</span><span class="sxs-lookup"><span data-stu-id="e66eb-169">In this phase, you take the settings determined in Phase 1 and implement them to create a SharePoint Online site for highly regulated data.</span></span>

### <a name="step-1-create-a-private-sharepoint-team-site-with-owners-and-members-of-the-corresponding-office-365-group"></a><span data-ttu-id="e66eb-170">Étape 1 : créer un site d’équipe SharePoint privé avec les propriétaires et les membres du groupe Office 365 correspondant</span><span class="sxs-lookup"><span data-stu-id="e66eb-170">Step 1: Create a private SharePoint team site with owners and members of the corresponding Office 365 group</span></span>

<span data-ttu-id="e66eb-171">Suivez [ces instructions]( https://support.office.com/article/create-a-site-in-sharepoint-online-4d1e11bf-8ddc-499d-b889-2b48d10b1ce8) pour créer un site d’équipe SharePoint privé.</span><span class="sxs-lookup"><span data-stu-id="e66eb-171">Follow [these instructions]( https://support.office.com/article/create-a-site-in-sharepoint-online-4d1e11bf-8ddc-499d-b889-2b48d10b1ce8) to create a private SharePoint team site.</span></span>

### <a name="step-2-configure-additional-permissions-settings-for-the-sharepoint-team-site"></a><span data-ttu-id="e66eb-172">Étape 2 : configurer les paramètres d’autorisations supplémentaires pour le site d’équipe SharePoint</span><span class="sxs-lookup"><span data-stu-id="e66eb-172">Step 2: Configure additional permissions settings for the SharePoint team site</span></span>

<span data-ttu-id="e66eb-173">À partir du site SharePoint, configurez ces paramètres d’autorisation.</span><span class="sxs-lookup"><span data-stu-id="e66eb-173">From the SharePoint site, configure these permission settings.</span></span>

1.  <span data-ttu-id="e66eb-174">Dans la barre d’outils, cliquez sur l’icône Paramètres, puis cliquez sur **Paramètres du site**.</span><span class="sxs-lookup"><span data-stu-id="e66eb-174">In the tool bar, click the settings icon, and then click **Site permissions**.</span></span>
2.  <span data-ttu-id="e66eb-175">Dans le volet **Autorisations du site**, cliquez sur **Paramètres d’autorisations avancés**.</span><span class="sxs-lookup"><span data-stu-id="e66eb-175">In the **Site permissions** pane, click **Advanced permissions settings**.</span></span>
3.  <span data-ttu-id="e66eb-176">Sous le nouvel onglet **Autorisations** dans votre navigateur, cliquez sur **Paramètres des demandes d’accès**.</span><span class="sxs-lookup"><span data-stu-id="e66eb-176">On the new **Permissions** tab of your browser, click **Access Request Settings**.</span></span>
4.  <span data-ttu-id="e66eb-177">Dans la boîte de dialogue **Paramètres de demande d’accès**, désélectionnez les cases **Autoriser les membres à partager le site et les fichiers et dossiers individuels** et **Autoriser les demandes d’accès** (les trois cases doivent être décochées), puis cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="e66eb-177">In the **Access Requests Settings** dialog box, clear **Allow member to share the site and individual files and folders** and \*\*Allow access requests \*\*(so that all three check boxes are cleared), and then click **OK**.</span></span>

<span data-ttu-id="e66eb-178">Avec ces paramètres, la possibilité pour les membres du groupe de sites de partager le site avec d’autres membres ou pour les non-membres afin de demander l’accès au site est désactivée.</span><span class="sxs-lookup"><span data-stu-id="e66eb-178">With these settings, the ability for site group members to share the site with other members or for non-members to request access to the site is disabled.</span></span>

### <a name="step-3-configure-the-site-for-an-office-365-retention-label"></a><span data-ttu-id="e66eb-179">Étape 3 : configurer le site pour une étiquette de rétention Office 365</span><span class="sxs-lookup"><span data-stu-id="e66eb-179">Step 2: Configure the site for an Office 365 retention label</span></span>

<span data-ttu-id="e66eb-180">Suivez les instructions mentionnées dans [Protéger les fichiers SharePoint avec les étiquettes Office 365 et la protection contre la perte de données (DLP)](https://docs.microsoft.com/office365/enterprise/protect-sharepoint-online-files-with-office-365-labels-and-dlp) pour :</span><span class="sxs-lookup"><span data-stu-id="e66eb-180">Use the instructions in [Protect SharePoint Online files with Office 365 labels and DLP](https://docs.microsoft.com/office365/enterprise/protect-sharepoint-online-files-with-office-365-labels-and-dlp) to:</span></span>

1. <span data-ttu-id="e66eb-181">Créer et publier une étiquette de rétention pour les données hautement réglementées (le cas échéant).</span><span class="sxs-lookup"><span data-stu-id="e66eb-181">Create and publish a retention label for highly regulated data (if needed).</span></span>
2. <span data-ttu-id="e66eb-182">Configurez le site pour l’étiquette de rétention créée à l’étape 1.</span><span class="sxs-lookup"><span data-stu-id="e66eb-182">Configure the site for the retention label created in step 1.</span></span>
3. <span data-ttu-id="e66eb-183">Créez une stratégie DLP pour les données hautement réglementées qui utilise l’étiquette de rétention créée à l’étape 2 et qui empêche les utilisateurs d’envoyer des fichiers à l’extérieur de l’Organisation</span><span class="sxs-lookup"><span data-stu-id="e66eb-183">Create a DLP policy for highly regulated data that uses the retention label created in step 2 and blocks users from sending files outside the organization</span></span>

#### <a name="step-4-create-an-office-365-sensitivity-sublabel-for-the-site"></a><span data-ttu-id="e66eb-184">Étape 4 : créer une sous-étiquette de sensibilité dans Office 365 pour le site</span><span class="sxs-lookup"><span data-stu-id="e66eb-184">Step 4: Create an Office 365 sensitivity sublabel for the site</span></span>

<span data-ttu-id="e66eb-185">Contrairement à une étiquette de sensibilité pour les données hautement réglementées qu’une personne peut appliquer à n’importe quel fichier, un site sécurisé nécessite sa propre sous-étiquette de sorte que les fichiers auxquels la sous-étiquette est attribuée :</span><span class="sxs-lookup"><span data-stu-id="e66eb-185">Unlike a sensitivity label for highly regulated data that anyone can apply to any file, a secure site needs its own sublabel so that files with the sublabel assigned:</span></span>

- <span data-ttu-id="e66eb-186">Sont chiffrés et le chiffrement est acheminé avec le fichier.</span><span class="sxs-lookup"><span data-stu-id="e66eb-186">Are encrypted and the encryption travels with the file.</span></span>
-   <span data-ttu-id="e66eb-187">Contiennent des autorisations personnalisées de sorte que seuls les membres du groupe de sites puissent l’ouvrir.</span><span class="sxs-lookup"><span data-stu-id="e66eb-187">Contain custom permissions so that only members of the site group can open it.</span></span>

<span data-ttu-id="e66eb-188">Pour atteindre ce niveau de sécurité supplémentaire pour les fichiers stockés sur le site, vous devez configurer une nouvelle étiquette de sensibilité qui est une sous-étiquette de l’étiquette général pour les fichiers hautement réglementés.</span><span class="sxs-lookup"><span data-stu-id="e66eb-188">To accomplish this additional level of security for files stored in the site, you must configure a new sensitivity label that is a sublabel of the general label for highly regulated files.</span></span> <span data-ttu-id="e66eb-189">Seuls les membres du groupe pour le site peuvent le voir dans la liste des sous-étiquettes pour l’étiquette hautement réglementée.</span><span class="sxs-lookup"><span data-stu-id="e66eb-189">Only group members for the site will see it in the list of sublabels for the highly regulated label.</span></span>

<span data-ttu-id="e66eb-190">Utilisez les instructions [ici](https://docs.microsoft.com/microsoft-365/compliance/encryption-sensitivity-labels) pour configurer une sous-étiquette de l’étiquette que vous utilisez pour les fichiers hautement réglementés avec les paramètres suivants :</span><span class="sxs-lookup"><span data-stu-id="e66eb-190">Use the instructions [here](https://docs.microsoft.com/microsoft-365/compliance/encryption-sensitivity-labels) to configure a sublabel of the label you are using for highly regulated files with the following settings:</span></span>

- <span data-ttu-id="e66eb-191">Le nom de la sous-étiquette contient le nom du site pour simplifier l’association lors de l’attribution de la sous-étiquette à un fichier.</span><span class="sxs-lookup"><span data-stu-id="e66eb-191">The name of the sublabel contains the name of the site for easy association when assign the sublabel to a file.</span></span>
- <span data-ttu-id="e66eb-192">Le chiffrement est activé.</span><span class="sxs-lookup"><span data-stu-id="e66eb-192">Encryption is enabled.</span></span>
- <span data-ttu-id="e66eb-193">Le groupe de sites possède des autorisations de co-création.</span><span class="sxs-lookup"><span data-stu-id="e66eb-193">The site group has Co-Author permissions.</span></span>

### <a name="configuration-results"></a><span data-ttu-id="e66eb-194">Résultats de la configuration</span><span class="sxs-lookup"><span data-stu-id="e66eb-194">Configuration results</span></span>

<span data-ttu-id="e66eb-195">Vous avez configuré les éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="e66eb-195">You have configured the following:</span></span>

- <span data-ttu-id="e66eb-196">Paramètres d’autorisation plus restrictifs sur le site SharePoint</span><span class="sxs-lookup"><span data-stu-id="e66eb-196">More restrictive permission settings on the SharePoint site</span></span>
- <span data-ttu-id="e66eb-197">Une étiquette de rétention Office 365 attribuée à la partie Documents du site SharePoint</span><span class="sxs-lookup"><span data-stu-id="e66eb-197">An Office 365 retention label assigned to the SharePoint Online isolated site</span></span>
- <span data-ttu-id="e66eb-198">Une stratégie DLP pour l’étiquette de rétention Office 365</span><span class="sxs-lookup"><span data-stu-id="e66eb-198">A DLP policy for the Office 365 retention label</span></span>
- <span data-ttu-id="e66eb-199">Une sous-étiquette de sensibilité Office 365 que les utilisateurs peuvent appliquer aux fichiers les plus sensibles stockés dans le site qui chiffre le fichier et autorise uniquement l’accès de co-création pour les membres du groupe de site d’équipe</span><span class="sxs-lookup"><span data-stu-id="e66eb-199">An Office 365 sensitivity sublabel that users can apply to the most sensitive files stored in the site that encrypts the file and only allows Co-Author access for members of the team site group</span></span> 

<span data-ttu-id="e66eb-200">Voici la configuration obtenue.</span><span class="sxs-lookup"><span data-stu-id="e66eb-200">Here is the resulting configuration.</span></span>

![Les sites SharePoint pour les scénarios de données hautement réglementés](./media/teams-sharepoint-online-sites-highly-regulated-data/end-to-end-configuration.png)


<span data-ttu-id="e66eb-202">Voici un exemple d’utilisateur ayant appliqué la sous-étiquette de sensibilité à un fichier stocké sur le site.</span><span class="sxs-lookup"><span data-stu-id="e66eb-202">Here is an example of a user that has applied the sensitivity sublabel to a file stored in the site.</span></span>

![Les sites SharePoint pour les scénarios de données hautement réglementés](./media/teams-sharepoint-online-sites-highly-regulated-data/end-to-end-configuration-example-file.png)


## <a name="phase-3-drive-user-adoption"></a><span data-ttu-id="e66eb-204">Étape 3 : favoriser l’adoption utilisateur</span><span class="sxs-lookup"><span data-stu-id="e66eb-204">Phase 3: Drive user adoption</span></span>

<span data-ttu-id="e66eb-205">Un site SharePoint pour les données hautement réglementées ne peut protéger ces données que s’il est utilisé de façon cohérente pour le stockage et l’accès aux fichiers sensibles.</span><span class="sxs-lookup"><span data-stu-id="e66eb-205">A SharePoint Online site or team for highly regulated data can only protect that data if it is consistently used for storage and access of sensitive digital assets. This is the hardest phase because it relies on users changing their ways.</span></span> <span data-ttu-id="e66eb-206">Il s’agit de la phase la plus difficile, car elle s’appuie sur les utilisateurs qui modifient leurs habitudes et leurs préférences.</span><span class="sxs-lookup"><span data-stu-id="e66eb-206">This is the hardest phase because it relies on users changing their habits and preferences.</span></span> 

<span data-ttu-id="e66eb-207">Par exemple, les employés habitués à stocker des fichiers sensibles sur des lecteurs USB ou des solutions de stockage personnelles basées sur le Cloud devront désormais les stocker exclusivement sur un site SharePoint pour les données hautement réglementées.</span><span class="sxs-lookup"><span data-stu-id="e66eb-207">For example, executives that are used to storing sensitive files on USB drives or on personal cloud-based storage solutions will now have to store them exclusively in a SharePoint Online site or team for highly regulated data.</span></span>

### <a name="step-1-train-your-users"></a><span data-ttu-id="e66eb-208">Étape 1 : former vos utilisateurs</span><span class="sxs-lookup"><span data-stu-id="e66eb-208">Step 1: Train your users</span></span>

<span data-ttu-id="e66eb-209">Après avoir effectué votre configuration, formez l’ensemble des utilisateurs membres des groupes d’accès au site aux sujets suivants :</span><span class="sxs-lookup"><span data-stu-id="e66eb-209">After completing your configuration, train the set of users who are members of the site access groups:</span></span>

- <span data-ttu-id="e66eb-210">Sur l’importance de l’utilisation du nouveau site pour protéger les fichiers précieux et les conséquences de la fuite de données hautement réglementées, telles que des conséquences juridiques, des amendes réglementaires, des logiciels rançonneurs ou la perte de l’avantage concurrentiel.</span><span class="sxs-lookup"><span data-stu-id="e66eb-210">On the importance of using the new site or team to protect valuable assets and the consequences of a highly regulated data leak, such as legal ramifications, regulatory fines, ransomware, or loss of competitive advantage.</span></span>
- <span data-ttu-id="e66eb-211">Accès au site et aux fichiers.</span><span class="sxs-lookup"><span data-stu-id="e66eb-211">How to access the site and its assets.</span></span>
- <span data-ttu-id="e66eb-212">Création de nouveaux fichiers sur le site et chargement de nouveaux fichiers stockés localement.</span><span class="sxs-lookup"><span data-stu-id="e66eb-212">How to create new files on the site and upload new files stored locally.</span></span>
- <span data-ttu-id="e66eb-213">Blocage du partage des fichiers en externe par la stratégie DLP.</span><span class="sxs-lookup"><span data-stu-id="e66eb-213">How the DLP policy blocks them from sharing files externally.</span></span>
- <span data-ttu-id="e66eb-214">Comment étiqueter les fichiers les plus sensibles avec la sous-étiquette du site.</span><span class="sxs-lookup"><span data-stu-id="e66eb-214">How to label the most sensitive files with the sublabel for the site.</span></span>
- <span data-ttu-id="e66eb-215">Comment la sous-étiquette protège un fichier même lorsque celui-ci a été divulgué hors du site.</span><span class="sxs-lookup"><span data-stu-id="e66eb-215">How the sublabel protects a file even when it is leaked off the site.</span></span>

<span data-ttu-id="e66eb-216">Cette formation doit inclure des exercices pratiques pour que les utilisateurs puissent effectuer ces opérations et observer leurs résultats.</span><span class="sxs-lookup"><span data-stu-id="e66eb-216">This training should include hands-on exercises so that the users can experience these operations and their results.</span></span>

### <a name="step-2-conduct-periodic-reviews-of-usage-and-files"></a><span data-ttu-id="e66eb-217">Étape 2 : conduire des vérifications périodiques de l’utilisation et des fichiers</span><span class="sxs-lookup"><span data-stu-id="e66eb-217">Step 2: Conduct periodic reviews of usage and files</span></span>

<span data-ttu-id="e66eb-218">Au cours des semaines après la formation, l’Administrateur de services SharePoint du site SharePoint peut effectuer les actions suivantes :</span><span class="sxs-lookup"><span data-stu-id="e66eb-218">In the weeks after training, the SharePoint administrator for the SharePoint Online site or team can:</span></span>

- <span data-ttu-id="e66eb-219">Analyser l’utilisation du site et les comparer avec les attentes de l’utilisation.</span><span class="sxs-lookup"><span data-stu-id="e66eb-219">Analyze usage for the site or team and compare it with usage expectations.</span></span>
- <span data-ttu-id="e66eb-220">Vérifier que les fichiers hautement sensibles ont été correctement étiquetés avec la sous-étiquette de sensibilité.</span><span class="sxs-lookup"><span data-stu-id="e66eb-220">Verify that sensitive or highly regulated files have been properly labeled with the appropriate sensitivity label.</span></span>

<span data-ttu-id="e66eb-221">Former à nouveau vos utilisateurs, le cas échéant.</span><span class="sxs-lookup"><span data-stu-id="e66eb-221">Retrain your users as needed.</span></span>

### <a name="user-adoption-results"></a><span data-ttu-id="e66eb-222">Résultats de l’adoption par les utilisateurs</span><span class="sxs-lookup"><span data-stu-id="e66eb-222">User adoption results</span></span>

<span data-ttu-id="e66eb-223">Les fichiers hautement réglementés sont stockés exclusivement sur des sites SharePoint pour des données hautement réglementées, et les fichiers les plus sensibles ont une sous-étiquette de sensibilité pour le site appliqué.</span><span class="sxs-lookup"><span data-stu-id="e66eb-223">Highly regulated files are stored exclusively on SharePoint sites for highly regulated data and the most sensitive files have the sensitivity sublabel for the site applied.</span></span>

## <a name="how-the-contoso-corporation-deployed-microsoft-365-enterprise"></a><span data-ttu-id="e66eb-224">Comment Contoso Corporation a déployé Microsoft 365 Entreprise</span><span class="sxs-lookup"><span data-stu-id="e66eb-224">How the Contoso Corporation deployed Microsoft 365 Enterprise</span></span>

<span data-ttu-id="e66eb-225">Contoso Corporation est un conglomérat de fabricants international fictif mais représentatif avec son siège à Paris en France.</span><span class="sxs-lookup"><span data-stu-id="e66eb-225">The Contoso Corporation is a fictional but representative global manufacturing conglomerate with its headquarters in Paris, France.</span></span> <span data-ttu-id="e66eb-226">Découvrez comment Contoso a conçu, configuré, puis piloté l’adoption d’un [site SharePoint sécurisé](contoso-sharepoint-online-site-for-highly-confidential-assets.md) pour ses équipes de recherche basées à Paris, Moscou, New York, Beijing et Bengaluru.</span><span class="sxs-lookup"><span data-stu-id="e66eb-226">See how Contoso designed, configured, and then drove the adoption of a [secure SharePoint Online site](contoso-sharepoint-online-site-for-highly-confidential-assets.md) for their research teams in Paris, Moscow, New York, Beijing, and Bangalore.</span></span> 

## <a name="see-also"></a><span data-ttu-id="e66eb-227">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e66eb-227">See also</span></span>

[<span data-ttu-id="e66eb-228">Guide de déploiement</span><span class="sxs-lookup"><span data-stu-id="e66eb-228">Deployment guide</span></span>](deploy-microsoft-365-enterprise.md)

[<span data-ttu-id="e66eb-229">Guides de laboratoire de test</span><span class="sxs-lookup"><span data-stu-id="e66eb-229">Test lab guides</span></span>](m365-enterprise-test-lab-guides.md)

