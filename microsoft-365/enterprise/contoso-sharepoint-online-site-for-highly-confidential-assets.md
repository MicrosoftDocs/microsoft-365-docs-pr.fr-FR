---
title: Site SharePoint Online pour les biens numériques hautement confidentiels de Contoso Corporation
ms.author: josephd
author: JoeDavies-MSFT
manager: laurawi
ms.date: 04/15/2019
audience: ITPro
ms.topic: overview
ms.service: o365-solutions
localization_priority: Normal
search.appverid:
- MET150
ms.collection: M365-security-compliance
ms.custom: Ent_Architecture
description: 'Résumé : Comment Contoso a mis en œuvre un site SharePoint Online pour les données hautement réglementées afin de faciliter la collaboration entre ses équipes de recherche.'
ms.openlocfilehash: 6c61d02c802a77afeb93a58b59114741c6630f9e
ms.sourcegitcommit: c6eab4a9f1b70e7ff0db6b2a1128a4db2591cbaf
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/02/2019
ms.locfileid: "37369525"
---
# <a name="sharepoint-online-site-for-highly-confidential-digital-assets-of-the-contoso-corporation"></a><span data-ttu-id="34d58-103">Site SharePoint Online pour les biens numériques hautement confidentiels de Contoso Corporation</span><span class="sxs-lookup"><span data-stu-id="34d58-103">SharePoint Online site for highly confidential digital assets of the Contoso Corporation</span></span>

 <span data-ttu-id="34d58-104">**Résumé :** Comment Contoso a mis en œuvre un site SharePoint Online pour les données hautement réglementées afin de faciliter la collaboration entre ses équipes de recherche.</span><span class="sxs-lookup"><span data-stu-id="34d58-104">**Summary:** How Contoso implemented a SharePoint Online site for highly regulated data for easier collaboration between its research teams.</span></span>
  
<span data-ttu-id="34d58-105">Les biens les plus précieux de Contoso sont sa propriété intellectuelle sous la forme de secrets commerciaux, tels que des techniques de fabrication propriétaires et des spécifications de conception pour les produits en cours de développement.</span><span class="sxs-lookup"><span data-stu-id="34d58-105">Contoso's most valuable assets are its intellectual property in the form of trade secrets, such as proprietary manufacturing techniques, and design specifications for products that are in development.</span></span> <span data-ttu-id="34d58-106">Ces biens sont au format numérique, stockés à l’origine en tant que fichiers sur un site SharePoint Server 2016.</span><span class="sxs-lookup"><span data-stu-id="34d58-106">These assets are in digital form, originally stored as files on a SharePoint Server 2016 site.</span></span> <span data-ttu-id="34d58-107">Lorsque Contoso a déployé Microsoft 365 Enterprise, il souhaitait faire passer ses biens numériques locaux dans le nuage pour faciliter l’accès et la collaboration ouverte entre les équipes de recherche à Paris, Moscou, New York, Pékin et Bangalore.</span><span class="sxs-lookup"><span data-stu-id="34d58-107">When Contoso deployed Microsoft 365 Enterprise, they wanted to transition their on-premises digital assets to the cloud for easier access and more open collaboration across research teams in Paris, Moscow, New York, Beijing, and Bangalore.</span></span> 
  
<span data-ttu-id="34d58-108">Toutefois, en raison de leur nature sensible, l’accès à ces fichiers doit être :</span><span class="sxs-lookup"><span data-stu-id="34d58-108">However, due to their sensitive nature, access to these files must be:</span></span>

- <span data-ttu-id="34d58-109">Limité à l’ensemble des personnes autorisées à les afficher ou à les modifier, avec des autorisations en cours pour le site administré uniquement par les administrateurs SharePoint.</span><span class="sxs-lookup"><span data-stu-id="34d58-109">Restricted to the set of people who are allowed to view or change them, with ongoing permissions for the site administered only by SharePoint admins.</span></span> 
- <span data-ttu-id="34d58-110">Protégé par la protection contre la perte de données (DLP) pour empêcher les utilisateurs de les répartir hors du site.</span><span class="sxs-lookup"><span data-stu-id="34d58-110">Protected with Data Loss Prevention (DLP) to prevent users from distributing them outside the site.</span></span>
- <span data-ttu-id="34d58-111">Chiffrés et protégés à l’aide des listes de contrôle d’accès pour empêcher les utilisateurs non autorisés d’accéder à leur contenu, même s’ils sont distribués en dehors du site.</span><span class="sxs-lookup"><span data-stu-id="34d58-111">Encrypted and protected with access control lists to prevent unauthorized users from accessing their contents, even if they are distributed outside the site.</span></span>

<span data-ttu-id="34d58-112">Les administrateurs de la sécurité et de SharePoint du service informatique de contoso ont décidé d’utiliser un [site SharePoint Online pour les données hautement réglementées](teams-sharepoint-online-sites-highly-regulated-data.md).</span><span class="sxs-lookup"><span data-stu-id="34d58-112">Security and SharePoint administrators in Contoso's IT department decided to use a [SharePoint Online site for highly regulated data](teams-sharepoint-online-sites-highly-regulated-data.md).</span></span>
  
<span data-ttu-id="34d58-113">Contoso a utilisé ces étapes pour créer et sécuriser un site d’équipe SharePoint Online pour ses équipes de recherche.</span><span class="sxs-lookup"><span data-stu-id="34d58-113">Contoso used these steps to create and secure a SharePoint Online team sites for their research teams.</span></span>

## <a name="step-1-reviewed-and-verified-the-members-of-research-team-groups"></a><span data-ttu-id="34d58-114">Étape 1 : révision et vérification des membres des groupes d’équipes de recherche</span><span class="sxs-lookup"><span data-stu-id="34d58-114">Step 1: Reviewed and verified the members of research team groups</span></span>

<span data-ttu-id="34d58-115">Les administrateurs informatiques de contoso ont effectué un examen de l’ensemble des groupes de sécurité pour leurs équipes de recherche.</span><span class="sxs-lookup"><span data-stu-id="34d58-115">Contoso IT admins performed a review of the set of security groups for their research teams.</span></span> <span data-ttu-id="34d58-116">Ils ont supprimé les personnes qui n’étaient pas chercheur ou n’ont pas besoin d’accéder aux ressources de recherche.</span><span class="sxs-lookup"><span data-stu-id="34d58-116">They removed anyone who was not a researcher or did not need access to research assets.</span></span> 

<span data-ttu-id="34d58-117">Ils ont également créé ces nouveaux groupes de sécurité et les ont créés :</span><span class="sxs-lookup"><span data-stu-id="34d58-117">They also and created these new security groups:</span></span>

- <span data-ttu-id="34d58-118">**Research-administrateurs**  Ensemble des administrateurs SharePoint qui disposent d’un contrôle total sur le site, y compris la possibilité de modifier les autorisations.</span><span class="sxs-lookup"><span data-stu-id="34d58-118">**Research-Admins**  The set of SharePoint admins that have full control over the site, including the ability to modify permissions.</span></span>
- <span data-ttu-id="34d58-119">**Research-members**  Ensemble de groupes de sécurité pour les équipes de recherche dans le monde entier.</span><span class="sxs-lookup"><span data-stu-id="34d58-119">**Research-Members**  The set of security groups for the research teams around the world.</span></span>
- <span data-ttu-id="34d58-120">**Research-visualiseurs**  Ensemble des utilisateurs de gestion, tels que les cadres de l’organisation de recherche, qui ne peuvent afficher que les biens sur le site.</span><span class="sxs-lookup"><span data-stu-id="34d58-120">**Research-Viewers**  The set of management users, such as executives in the research organization, that can only view the assets on the site.</span></span>

## <a name="step-2-created-an-isolated-sharepoint-online-team-site"></a><span data-ttu-id="34d58-121">Étape 2 : création d’un site d’équipe SharePoint Online isolé</span><span class="sxs-lookup"><span data-stu-id="34d58-121">Step 2: Created an isolated SharePoint Online team site</span></span> 

<span data-ttu-id="34d58-122">Les administrateurs SharePoint de contoso ont d’abord créé un nouveau site d’équipe nommé **Research**.</span><span class="sxs-lookup"><span data-stu-id="34d58-122">Contoso SharePoint admins first created a new team site named **Research**.</span></span> <span data-ttu-id="34d58-123">Ils sont ensuite configurés :</span><span class="sxs-lookup"><span data-stu-id="34d58-123">They then configured:</span></span>

- <span data-ttu-id="34d58-124">Niveau d’autorisation contrôle total permettant d’utiliser le groupe SharePoint propriétaires de recherche, dont le groupe de sécurité **administrateurs de recherche** est membre.</span><span class="sxs-lookup"><span data-stu-id="34d58-124">The Full Control permission level to use the Research Owners SharePoint group, which has the **Research-Admins** security group as a member</span></span>
- <span data-ttu-id="34d58-125">Le niveau d’autorisation Modifier pour utiliser le groupe SharePoint membres de la recherche, dont le groupe de sécurité **membres de recherche** est membre</span><span class="sxs-lookup"><span data-stu-id="34d58-125">The Edit permission level to use the Research Members SharePoint group, which has the **Research Members** security group as a member</span></span>
- <span data-ttu-id="34d58-126">Le niveau d’autorisation lecture pour utiliser le groupe SharePoint des visiteurs de la recherche, qui a le groupe de sécurité **des visionneuses de recherche** en tant que membre</span><span class="sxs-lookup"><span data-stu-id="34d58-126">The Read permission level to use the Research Visitors SharePoint group, which has the **Research-Viewers** security group as a member</span></span>

<span data-ttu-id="34d58-127">Voici les niveaux d’autorisation SharePoint qui en résultent, les groupes SharePoint et leurs membres.</span><span class="sxs-lookup"><span data-stu-id="34d58-127">Here are the resulting SharePoint permission levels, SharePoint groups, and their members.</span></span>

![Niveaux d’autorisation SharePoint, groupes SharePoint et leurs membres](./media/contoso-sharepoint-online-site-for-highly-confidential-assets/spo-permissions.png)

<span data-ttu-id="34d58-129">Ensuite, ils ont configuré des restrictions supplémentaires pour le site.</span><span class="sxs-lookup"><span data-stu-id="34d58-129">Next, they configured additional restrictions for the site.</span></span>

<span data-ttu-id="34d58-130">Pour plus d’informations sur la configuration, consultez la rubrique [deploy an Isolated SharePoint Online Team site](https://docs.microsoft.com/office365/enterprise/deploy-an-isolated-sharepoint-online-team-site).</span><span class="sxs-lookup"><span data-stu-id="34d58-130">For the configuration details, see [Deploy an isolated SharePoint Online team site](https://docs.microsoft.com/office365/enterprise/deploy-an-isolated-sharepoint-online-team-site).</span></span>

## <a name="step-3-configured-the-site-for-a-restrictive-dlp-policy"></a><span data-ttu-id="34d58-131">Étape 3 : configuration du site pour une stratégie DLP restrictive</span><span class="sxs-lookup"><span data-stu-id="34d58-131">Step 3: Configured the site for a restrictive DLP policy</span></span>

<span data-ttu-id="34d58-132">Tout d’abord, les administrateurs de contoso ont appliqué l’étiquette de rétention Office 365 **hautement confidentiel** au site de **recherche** .</span><span class="sxs-lookup"><span data-stu-id="34d58-132">First, Contoso admins applied the **Highly Confidential** Office 365 retention label to the **Research** site.</span></span>

<span data-ttu-id="34d58-133">Ensuite, ils ont créé une nouvelle stratégie DLP Office 365 nommée **Research** qui :</span><span class="sxs-lookup"><span data-stu-id="34d58-133">Next, they created a new Office 365 DLP policy named **Research** that:</span></span>

- <span data-ttu-id="34d58-134">Utilise l’étiquette de rétention Office 365 **hautement confidentiel** .</span><span class="sxs-lookup"><span data-stu-id="34d58-134">Uses the **Highly Confidential** Office 365 retention label.</span></span> 
- <span data-ttu-id="34d58-135">Est appliqué au site de **recherche** .</span><span class="sxs-lookup"><span data-stu-id="34d58-135">Is applied to the **Research** site.</span></span>
- <span data-ttu-id="34d58-136">Bloque les utilisateurs lorsqu’ils tentent de partager une ressource numérique sur le site de **recherche** en dehors de contoso.</span><span class="sxs-lookup"><span data-stu-id="34d58-136">Blocks users when they attempt to share a digital asset on the **Research** site outside of Contoso.</span></span>

<span data-ttu-id="34d58-137">Pour plus d’informations sur la configuration, consultez la rubrique [protéger des fichiers SharePoint Online avec des étiquettes de rétention et DLP](https://docs.microsoft.com/office365/enterprise/protect-sharepoint-online-files-with-office-365-labels-and-dlp).</span><span class="sxs-lookup"><span data-stu-id="34d58-137">For the configuration details, see [Protect SharePoint Online files with retention labels and DLP](https://docs.microsoft.com/office365/enterprise/protect-sharepoint-online-files-with-office-365-labels-and-dlp).</span></span>

## <a name="step-4-created-an-azure-information-protection-sub-label-for-the-site"></a><span data-ttu-id="34d58-138">Étape 4 : création d’une sous-étiquette Azure information protection pour le site</span><span class="sxs-lookup"><span data-stu-id="34d58-138">Step 4: Created an Azure Information Protection sub-label for the site</span></span>

<span data-ttu-id="34d58-139">Les administrateurs contoso ont créé une nouvelle sous-étiquette Azure information protection nommée **Research** de l’étiquette **hautement confidentiel** par défaut dans une stratégie délimitée :</span><span class="sxs-lookup"><span data-stu-id="34d58-139">Contoso admins created a new Azure Information Protection sub-label named **Research** of the default **Highly Confidential** label in a scoped policy that:</span></span>

- <span data-ttu-id="34d58-140">Nécessite le chiffrement.</span><span class="sxs-lookup"><span data-stu-id="34d58-140">Requires encryption.</span></span>
- <span data-ttu-id="34d58-141">Permet un accès total par les membres du groupe de sécurité des membres de la **recherche** .</span><span class="sxs-lookup"><span data-stu-id="34d58-141">Allows full access by members of the **Research-Members** security group.</span></span>
- <span data-ttu-id="34d58-142">Autorise l’accès en lecture par les membres du groupe de sécurité **Research-visualisers** .</span><span class="sxs-lookup"><span data-stu-id="34d58-142">Allows read access by members of the **Research-Viewers** security group.</span></span>

<span data-ttu-id="34d58-143">Ensuite, ils ont déployé le client Azure information protection sur les appareils des membres de l’équipe de recherche.</span><span class="sxs-lookup"><span data-stu-id="34d58-143">Next, they deployed the Azure Information Protection client to the devices of research team members.</span></span>

<span data-ttu-id="34d58-144">Pour plus d’informations sur la configuration, consultez la rubrique [protéger les fichiers SharePoint Online avec Azure information protection](https://docs.microsoft.com/office365/enterprise/protect-sharepoint-online-files-with-azure-information-protection).</span><span class="sxs-lookup"><span data-stu-id="34d58-144">For the configuration details, see [Protect SharePoint Online files with Azure Information Protection](https://docs.microsoft.com/office365/enterprise/protect-sharepoint-online-files-with-azure-information-protection).</span></span> 

<span data-ttu-id="34d58-145">Voici la configuration obtenue du site de **recherche** pour les ressources hautement confidentielles.</span><span class="sxs-lookup"><span data-stu-id="34d58-145">Here is the resulting configuration of the **Research** site for highly confidential assets.</span></span>

![La configuration obtenue du site \* \* Research \* \* pour les ressources hautement confidentielles](./media/contoso-sharepoint-online-site-for-highly-confidential-assets/final-config.png)

<span data-ttu-id="34d58-147">Les fichiers dans les dossiers du site de **recherche** sont protégés par :</span><span class="sxs-lookup"><span data-stu-id="34d58-147">Files in folders of the **Research** site are protected by:</span></span>

- <span data-ttu-id="34d58-148">Sous-étiquette **Research** Azure information protection, qui applique le chiffrement et permssions à chaque fichier qui voyage avec le fichier lorsqu’il est déplacé ou copié à partir du site de **recherche** .</span><span class="sxs-lookup"><span data-stu-id="34d58-148">The **Research** Azure Information Protection sublabel, which applies encryption and permssions to each file that travel with the file when it is moved or copied from the **Research** site.</span></span>
- <span data-ttu-id="34d58-149">La stratégie DLP de **recherche** , qui utilise l’étiquette de rétention **hautement sensible** et les paramètres qui empêchent le partage du fichier avec des utilisateurs externes.</span><span class="sxs-lookup"><span data-stu-id="34d58-149">The **Research** DLP policy, which uses the **Highly Sensitive** retention label and settings that prevent the file from being shared with external users.</span></span>
- <span data-ttu-id="34d58-150">Ensemble des autorisations de site, qui autorisent uniquement l’accès aux membres des groupes de sécurité et de l’administration des **membres** de la recherche et des **visionneuses de recherche** par les membres du groupe de sécurité **Research-admins** .</span><span class="sxs-lookup"><span data-stu-id="34d58-150">The set of site permissions, which only allow access to members of the **Research-Members** and **Research-Viewers** security groups and administration by members of the **Research-Admins** security group.</span></span>

## <a name="step-5-migrated-the-on-premises-sharepoint-research-data"></a><span data-ttu-id="34d58-151">Étape 5 : migration des données de recherche SharePoint locales</span><span class="sxs-lookup"><span data-stu-id="34d58-151">Step 5: Migrated the on-premises SharePoint research data</span></span>

<span data-ttu-id="34d58-152">Les administrateurs de contoso ont déplacé tous les fichiers de recherche sur site du site SharePoint Server 2016 local vers des dossiers dans le nouveau site SharePoint Online de **recherche** .</span><span class="sxs-lookup"><span data-stu-id="34d58-152">Contoso admins moved all of the on-premises research files in the on-premises SharePoint Server 2016 site to folders in the new **Research** SharePoint Online site.</span></span>

## <a name="step-6-trained-their-users"></a><span data-ttu-id="34d58-153">Étape 6 : apprentissage de leurs utilisateurs</span><span class="sxs-lookup"><span data-stu-id="34d58-153">Step 6: Trained their users</span></span> 

<span data-ttu-id="34d58-154">Le personnel de sécurité de Contoso a formé les équipes de recherche dans un cours obligatoire qui les a exécutées par les utilisateurs :</span><span class="sxs-lookup"><span data-stu-id="34d58-154">Contoso security staff trained the research teams in a mandatory course that stepped them through:</span></span>

- <span data-ttu-id="34d58-155">Comment accéder au nouveau site SharePoint Online de **recherche** et à ses fichiers existants.</span><span class="sxs-lookup"><span data-stu-id="34d58-155">How to access the new **Research** SharePoint Online site and its existing files.</span></span>
- <span data-ttu-id="34d58-156">Création de nouveaux fichiers sur le site et chargement de nouveaux fichiers stockés localement.</span><span class="sxs-lookup"><span data-stu-id="34d58-156">How to create new files on the site and upload new files stored locally.</span></span>
- <span data-ttu-id="34d58-157">Démonstration de la façon dont la stratégie DLP empêche les fichiers d’être partagés en externe.</span><span class="sxs-lookup"><span data-stu-id="34d58-157">A demonstration of how the DLP policy blocks files from being shared externally.</span></span>
- <span data-ttu-id="34d58-158">Comment utiliser le client Azure information protection pour étiqueter les fichiers de recherche avec la sous-étiquette **Research** .</span><span class="sxs-lookup"><span data-stu-id="34d58-158">How to use the Azure Information Protection client to label research files with the **Research** sub-label.</span></span>
- <span data-ttu-id="34d58-159">Démonstration de la façon dont la sous-étiquette de **recherche** protège un fichier même lorsqu’il est divulgué à partir du site.</span><span class="sxs-lookup"><span data-stu-id="34d58-159">A demonstration of how the **Research** sub-label protects a file even when it is leaked from the site.</span></span>

<span data-ttu-id="34d58-160">Le résultat final est un environnement sécurisé dans lequel les chercheurs peuvent collaborer au sein de l’organisation dans un environnement sécurisé.</span><span class="sxs-lookup"><span data-stu-id="34d58-160">The end result is a secure environment in which the researchers can collaborate across the organization in a secure environment.</span></span> 

<span data-ttu-id="34d58-161">Si un document de recherche avec la sous-étiquette **Research** est divulgué à partir du site de **recherche** , il est chiffré et accessible uniquement aux membres des groupes de sécurité **Research-members** et **Research-visualisables** avec des informations d’identification valides.</span><span class="sxs-lookup"><span data-stu-id="34d58-161">If a research document with the **Research** sub-label is leaked from the **Research** site, it is encrypted and accessible only to members of the **Research-Members** and **Research-Viewers** security groups with valid credentials.</span></span>

## <a name="next-step"></a><span data-ttu-id="34d58-162">Étape suivante</span><span class="sxs-lookup"><span data-stu-id="34d58-162">Next step</span></span>

<span data-ttu-id="34d58-163">[Déployer](deploy-microsoft-365-enterprise.md) Microsoft 365 entreprise dans votre organisation.</span><span class="sxs-lookup"><span data-stu-id="34d58-163">[Deploy](deploy-microsoft-365-enterprise.md) Microsoft 365 Enterprise in your organization.</span></span>

