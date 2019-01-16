---
title: Site SharePoint Online pour les biens numériques hautement confidentielles de la société Contoso
ms.author: josephd
author: JoeDavies-MSFT
manager: laurawi
ms.date: 11/01/2018
ms.audience: ITPro
ms.topic: overview
ms.service: o365-solutions
localization_priority: Normal
search.appverid:
- MET150
ms.collection: Ent_O365
ms.custom: Ent_Architecture
description: 'Résumé : Comment Contoso implémenté un site SharePoint Online pour hautement régulées données pour faciliter la collaboration entre ses recherches équipes.'
ms.openlocfilehash: 697ddb27b56fd529e9c73b89d9f07b8731ad76c3
ms.sourcegitcommit: e491c4713115610cbe13d2fbd0d65e1a41c34d62
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/16/2019
ms.locfileid: "26867430"
---
# <a name="sharepoint-online-site-for-highly-confidential-digital-assets-of-the-contoso-corporation"></a><span data-ttu-id="301a2-103">Site SharePoint Online pour les biens numériques hautement confidentielles de la société Contoso</span><span class="sxs-lookup"><span data-stu-id="301a2-103">SharePoint Online site for highly confidential digital assets of the Contoso Corporation</span></span>

 <span data-ttu-id="301a2-104">**Résumé :** Comment Contoso implémenté un site SharePoint Online pour les données hautement régulés pour faciliter la collaboration entre des équipes de recherche.</span><span class="sxs-lookup"><span data-stu-id="301a2-104">**Summary:** How Contoso implemented a SharePoint Online site for highly regulated data for easier collaboration between its research teams.</span></span>
  
<span data-ttu-id="301a2-p101">Actifs les plus importants de Contoso sont la propriété intellectuelle sous la forme de secrets commerciaux, tels que des techniques de fabrication propriétaires et les spécifications pour les produits qui se trouvent dans le développement de conception. Ces ressources sont au format numérique, à l’origine stockée en tant que fichiers sur un site SharePoint Server 2016. Lorsque Contoso déployé Microsoft 365 pour entreprises, qu’ils veulent effectuer la transition entre les équipes de recherche dans Paris, Moscou, New York, Pékin et Bangalore leurs ressources numériques locaux vers le nuage pour faciliter l’accès et de collaboration plus ouverte.</span><span class="sxs-lookup"><span data-stu-id="301a2-p101">Contoso's most valuable assets are its intellectual property in the form of trade secrets, such as proprietary manufacturing techniques, and design specifications for products that are in development. These assets are in digital form, originally stored as files on a SharePoint Server 2016 site. When Contoso deployed Microsoft 365 Enterprise, they wanted to transition their on-premises digital assets to the cloud for easier access and more open collaboration across research teams in Paris, Moscow, New York, Beijing, and Bangalore.</span></span> 
  
<span data-ttu-id="301a2-108">Toutefois, en raison de leur nature confidentielle, accès à ces fichiers doit être :</span><span class="sxs-lookup"><span data-stu-id="301a2-108">However, due to their sensitive nature, access to these files must be:</span></span>

- <span data-ttu-id="301a2-109">Limitée à l’ensemble des personnes qui sont autorisés à afficher ou modifier les, avec des autorisations en cours pour le site gérée uniquement par les administrateurs SharePoint.</span><span class="sxs-lookup"><span data-stu-id="301a2-109">Restricted to the set of people who are allowed to view or change them, with ongoing permissions for the site administered only by SharePoint admins.</span></span> 
- <span data-ttu-id="301a2-110">Protégé avec Data Loss Prevention (DLP) pour empêcher les utilisateurs de les distribuer en dehors du site.</span><span class="sxs-lookup"><span data-stu-id="301a2-110">Protected with Data Loss Prevention (DLP) to prevent users from distributing them outside the site.</span></span>
- <span data-ttu-id="301a2-111">Pour empêcher les utilisateurs non autorisés d’accéder à leur contenu, même s’ils sont en dehors du site, les listes de contrôle d’accès chiffré et protégé avec.</span><span class="sxs-lookup"><span data-stu-id="301a2-111">Encrypted and protected with access control lists to prevent unauthorized users from accessing their contents, even if they are distributed outside the site.</span></span>

<span data-ttu-id="301a2-112">Sécurité et SharePoint des administrateurs de Contoso de l’informatique a décidé d’utiliser un [site SharePoint Online pour régulé hautement des données](teams-sharepoint-online-sites-highly-regulated-data.md).</span><span class="sxs-lookup"><span data-stu-id="301a2-112">Security and SharePoint administrators in Contoso's IT department decided to use a [SharePoint Online site for highly regulated data](teams-sharepoint-online-sites-highly-regulated-data.md).</span></span>
  
<span data-ttu-id="301a2-113">Contoso a utilisé ces étapes pour créer et sécuriser un sites d’équipe SharePoint Online pour leurs équipes de recherche.</span><span class="sxs-lookup"><span data-stu-id="301a2-113">Contoso used these steps to create and secure a SharePoint Online team sites for their research teams.</span></span>

## <a name="step-1-reviewed-and-verified-the-members-of-research-team-groups"></a><span data-ttu-id="301a2-114">Étape 1 : Révisé et vérifié les membres des groupes de l’équipe de recherche</span><span class="sxs-lookup"><span data-stu-id="301a2-114">Step 1: Reviewed and verified the members of research team groups</span></span>

<span data-ttu-id="301a2-p102">Les administrateurs informatiques de Contoso effectuée un examen de l’ensemble des groupes de sécurité pour leurs équipes de recherche. Supprimés, toute personne qui n’a pas un enquêteur ou n’était pas nécessaire de l’accès aux ressources de recherche.</span><span class="sxs-lookup"><span data-stu-id="301a2-p102">Contoso IT admins performed a review of the set of security groups for their research teams. They removed anyone who was not a researcher or did not need access to research assets.</span></span> 

<span data-ttu-id="301a2-117">Ils également et créé ces nouveaux groupes de sécurité :</span><span class="sxs-lookup"><span data-stu-id="301a2-117">They also and created these new security groups:</span></span>

- <span data-ttu-id="301a2-118">**Administrateurs de la recherche**  L’ensemble du groupe Administrateurs SharePoint qui ont un contrôle total sur le site, notamment la possibilité de modifier les autorisations.</span><span class="sxs-lookup"><span data-stu-id="301a2-118">**Research-Admins**  The set of SharePoint admins that have full control over the site, including the ability to modify permissions.</span></span>
- <span data-ttu-id="301a2-119">**Membres de la recherche**  L’ensemble des groupes de sécurité pour les équipes de recherche dans le monde entier.</span><span class="sxs-lookup"><span data-stu-id="301a2-119">**Research Members**  The set of security groups for the research teams around the world.</span></span>
- <span data-ttu-id="301a2-120">**Visionneuses de la recherche**  L’ensemble de la gestion des utilisateurs, telles que les dirigeants de l’entreprise de recherche, qui peut afficher les biens sur le site.</span><span class="sxs-lookup"><span data-stu-id="301a2-120">**Research-Viewers**  The set of management users, such as executives in the research organization, that can view the assets on the site.</span></span>

## <a name="step-2-created-an-isolated-sharepoint-online-team-site"></a><span data-ttu-id="301a2-121">Étape 2 : Création d’un site d’équipe SharePoint Online isolé</span><span class="sxs-lookup"><span data-stu-id="301a2-121">Step 2: Created an isolated SharePoint Online team site</span></span> 

<span data-ttu-id="301a2-p103">Les administrateurs Contoso SharePoint tout d’abord créés un nouveau site d’équipe nommé **recherche**. Ils configurés, puis :</span><span class="sxs-lookup"><span data-stu-id="301a2-p103">Contoso SharePoint admins first created a new team site named **Research**. They then configured:</span></span>

- <span data-ttu-id="301a2-124">Le niveau d’autorisation contrôle total à utiliser le groupe SharePoint propriétaires de recherche, qui est le groupe de sécurité **Administrateurs de la recherche** en tant que membre</span><span class="sxs-lookup"><span data-stu-id="301a2-124">The Full Control permission level to use the Research Owners SharePoint group, which has the **Research-Admins** security group as a member</span></span>
- <span data-ttu-id="301a2-125">Le niveau d’autorisation Modifier pour utiliser le groupe SharePoint des membres de recherche, dont le groupe de sécurité **Membres de recherche** en tant que membre</span><span class="sxs-lookup"><span data-stu-id="301a2-125">The Edit permission level to use the Research Members SharePoint group, which has the **Research Members** security group as a member</span></span>
- <span data-ttu-id="301a2-126">Le niveau d’autorisation en lecture à utiliser le groupe SharePoint visiteurs de recherche, qui est le groupe de sécurité des **Visionneuses de la recherche** en tant que membre</span><span class="sxs-lookup"><span data-stu-id="301a2-126">The Read permission level to use the Research Visitors SharePoint group, which has the **Research-Viewers** security group as a member</span></span>

<span data-ttu-id="301a2-127">Voici les niveaux d’autorisation SharePoint qui en résulte, les groupes SharePoint et leurs membres.</span><span class="sxs-lookup"><span data-stu-id="301a2-127">Here are the resulting SharePoint permission levels, SharePoint groups, and their members.</span></span>

![](./media/contoso-sharepoint-online-site-for-highly-confidential-assets/spo-permissions.png)

<span data-ttu-id="301a2-128">Ensuite, ils configuré des restrictions supplémentaires pour le site.</span><span class="sxs-lookup"><span data-stu-id="301a2-128">Next, they configured additional restrictions for the site.</span></span>

<span data-ttu-id="301a2-129">Pour les détails de configuration, voir [déploiement d’un site d’équipe SharePoint Online isolé](https://docs.microsoft.com/office365/enterprise/deploy-an-isolated-sharepoint-online-team-site).</span><span class="sxs-lookup"><span data-stu-id="301a2-129">For the configuration details, see [Deploy an isolated SharePoint Online team site](https://docs.microsoft.com/office365/enterprise/deploy-an-isolated-sharepoint-online-team-site).</span></span>

## <a name="step-3-configured-the-site-for-a-restrictive-office-365-label-dlp-policy"></a><span data-ttu-id="301a2-130">Étape 3 : Configurer le site d’une étiquette d’Office 365 restrictif stratégie DLP</span><span class="sxs-lookup"><span data-stu-id="301a2-130">Step 3: Configured the site for a restrictive Office 365 label DLP policy</span></span>

<span data-ttu-id="301a2-131">Tout d’abord, les administrateurs Contoso appliqué l’étiquette de Office 365 **Hautement confidentielles** sur le site de **recherche** .</span><span class="sxs-lookup"><span data-stu-id="301a2-131">First, Contoso admins applied the **Highly Confidential** Office 365 label to the **Research** site.</span></span>

<span data-ttu-id="301a2-132">Ensuite, ils créé une nouvelle stratégie Office 365 DLP nommé **recherche** qui :</span><span class="sxs-lookup"><span data-stu-id="301a2-132">Next, they created a new Office 365 DLP policy named **Research** that:</span></span>

- <span data-ttu-id="301a2-133">Utilise l’étiquette d’Office 365 **Hautement confidentielles** .</span><span class="sxs-lookup"><span data-stu-id="301a2-133">Uses the **Highly Confidential** Office 365 label.</span></span> 
- <span data-ttu-id="301a2-134">Est appliquée au site de **recherche** .</span><span class="sxs-lookup"><span data-stu-id="301a2-134">Is applied to the **Research** site.</span></span>
- <span data-ttu-id="301a2-135">Empêche les utilisateurs de partager des documents.</span><span class="sxs-lookup"><span data-stu-id="301a2-135">Prevents users from sharing documents.</span></span>

<span data-ttu-id="301a2-136">Pour les détails de configuration, voir [fichiers protéger SharePoint Online avec Office 365 étiquettes et DLP](https://docs.microsoft.com/office365/enterprise/protect-sharepoint-online-files-with-office-365-labels-and-dlp).</span><span class="sxs-lookup"><span data-stu-id="301a2-136">For the configuration details, see [Protect SharePoint Online files with Office 365 labels and DLP](https://docs.microsoft.com/office365/enterprise/protect-sharepoint-online-files-with-office-365-labels-and-dlp).</span></span>

## <a name="step-4-created-an-azure-information-protection-sub-label-for-the-site"></a><span data-ttu-id="301a2-137">Étape 4 : Créé une étiquette sous-sites Azure la Protection des informations pour le site</span><span class="sxs-lookup"><span data-stu-id="301a2-137">Step 4: Created an Azure Information Protection sub-label for the site</span></span>

<span data-ttu-id="301a2-138">Les administrateurs Contoso créés une nouvelle étiquette de sous-sites Azure Information Protection nommé **recherche** de l’étiquette **Hautement confidentielles** par défaut d’une stratégie sur lesquelles porte qui :</span><span class="sxs-lookup"><span data-stu-id="301a2-138">Contoso admins created a new Azure Information Protection sub-label named **Research** of the default **Highly Confidential** label in a scoped policy that:</span></span>

- <span data-ttu-id="301a2-139">Nécessite un chiffrement.</span><span class="sxs-lookup"><span data-stu-id="301a2-139">Requires encryption.</span></span>
- <span data-ttu-id="301a2-140">Autorise l’accès complet par les membres du groupe de sécurité **Membres de la recherche** .</span><span class="sxs-lookup"><span data-stu-id="301a2-140">Allows full access by members of the **Research Members** security group.</span></span>
- <span data-ttu-id="301a2-141">Permet un accès en lecture par les membres du groupe de sécurité **Des visionneuses de recherche** .</span><span class="sxs-lookup"><span data-stu-id="301a2-141">Allows read access by members of the **Research Viewers** security group.</span></span>

<span data-ttu-id="301a2-142">Ensuite, ils déploiement le client Azure la Protection des informations sur les périphériques de membres de l’équipe.</span><span class="sxs-lookup"><span data-stu-id="301a2-142">Next, they deployed the Azure Information Protection client to the devices of research team members.</span></span>

<span data-ttu-id="301a2-143">Pour les détails de configuration, voir [fichiers protéger SharePoint Online avec Azure la Protection des informations](https://docs.microsoft.com/office365/enterprise/protect-sharepoint-online-files-with-azure-information-protection).</span><span class="sxs-lookup"><span data-stu-id="301a2-143">For the configuration details, see [Protect SharePoint Online files with Azure Information Protection](https://docs.microsoft.com/office365/enterprise/protect-sharepoint-online-files-with-azure-information-protection).</span></span> 

<span data-ttu-id="301a2-144">Voici la configuration du site de **recherche** pour les biens hautement confidentielles qui en résulte.</span><span class="sxs-lookup"><span data-stu-id="301a2-144">Here is the resulting configuration of the **Research** site for highly confidential assets.</span></span>

![](./media/contoso-sharepoint-online-site-for-highly-confidential-assets/final-config.png)

## <a name="step-5-migrated-the-on-premises-sharepoint-research-data"></a><span data-ttu-id="301a2-145">Étape 5 : Migrer les données de recherche SharePoint local</span><span class="sxs-lookup"><span data-stu-id="301a2-145">Step 5: Migrated the on-premises SharePoint research data</span></span>

<span data-ttu-id="301a2-146">Les administrateurs de Contoso déplacement que tous les locaux de recherche les fichiers dans le site de SharePoint Server 2016 locale aux dossiers dans le nouveau site SharePoint Online **Research** .</span><span class="sxs-lookup"><span data-stu-id="301a2-146">Contoso admins moved all of the on-premises research files in the on-premises SharePoint Server 2016 site to folders in the new **Research** SharePoint Online site.</span></span>

## <a name="step-6-trained-their-users"></a><span data-ttu-id="301a2-147">Étape 6 : Former les utilisateurs</span><span class="sxs-lookup"><span data-stu-id="301a2-147">Step 6: Trained their users</span></span> 

<span data-ttu-id="301a2-148">Le personnel de sécurité Contoso formé les équipes de recherche dans un cours obligatoire qui les pas à pas :</span><span class="sxs-lookup"><span data-stu-id="301a2-148">Contoso security staff trained the research teams in a mandatory course that stepped them through:</span></span>

- <span data-ttu-id="301a2-149">Comment accéder à nouveau site SharePoint Online **Research** et ses fichiers existants.</span><span class="sxs-lookup"><span data-stu-id="301a2-149">How to access the new **Research** SharePoint Online site and its existing files.</span></span>
- <span data-ttu-id="301a2-150">Création de nouveaux fichiers sur le site et chargement de nouveaux fichiers stockés localement.</span><span class="sxs-lookup"><span data-stu-id="301a2-150">How to create new files on the site and upload new files stored locally.</span></span>
- <span data-ttu-id="301a2-151">Une démonstration de la stratégie DLP empêche les fichiers partagés en externe.</span><span class="sxs-lookup"><span data-stu-id="301a2-151">A demonstration of how the DLP policy blocks files from being shared externally.</span></span>
- <span data-ttu-id="301a2-152">Découvrez comment utiliser le client de la Protection des informations Azure pour étiqueter les fichiers de recherche avec l’étiquette d’une **recherche** .</span><span class="sxs-lookup"><span data-stu-id="301a2-152">How to use the Azure Information Protection client to label research files with the **Research** sub-label.</span></span>
- <span data-ttu-id="301a2-153">Une démonstration de l’étiquette de sous-sites de **recherche** protège un fichier même si elle est une fuite d’à partir du site.</span><span class="sxs-lookup"><span data-stu-id="301a2-153">A demonstration of how the **Research** sub-label protects a file even when it is leaked from the site.</span></span>

<span data-ttu-id="301a2-154">Le résultat final est un environnement sécurisé dans lequel les chercheurs peuvent collaborer au sein de l’organisation dans un environnement sécurisé.</span><span class="sxs-lookup"><span data-stu-id="301a2-154">The end result is a secure environment in which the researchers can collaborate across the organization in a secure environment.</span></span> 

<span data-ttu-id="301a2-155">Si un document de recherche avec l’étiquette de sous-sites de **recherche** est perdue à partir du site de **recherche** , il est chiffré et accessibles uniquement aux membres des groupes de sécurité **Membres de recherche** et les **Visionneuses de recherche** avec les informations d’identification valides.</span><span class="sxs-lookup"><span data-stu-id="301a2-155">If a research document with the **Research** sub-label is leaked from the **Research** site, it is encrypted and accessible only to members of the **Research Members** and **Research Viewers** security groups with valid credentials.</span></span>

## <a name="next-step"></a><span data-ttu-id="301a2-156">Étape suivante</span><span class="sxs-lookup"><span data-stu-id="301a2-156">Next step</span></span>

<span data-ttu-id="301a2-157">[Déployez](deploy-microsoft-365-enterprise.md) Microsoft 365 Entreprise dans votre organisation.</span><span class="sxs-lookup"><span data-stu-id="301a2-157">[Deploy](deploy-microsoft-365-enterprise.md) Microsoft 365 Enterprise in your organization.</span></span>

