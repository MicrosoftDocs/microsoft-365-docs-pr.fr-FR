---
title: Site SharePoint pour les biens numériques hautement confidentiels de Contoso Corporation
ms.author: josephd
author: JoeDavies-MSFT
manager: laurawi
ms.date: 10/04/2019
audience: ITPro
ms.topic: overview
ms.service: o365-solutions
localization_priority: Normal
search.appverid:
- MET150
ms.collection: M365-security-compliance
ms.custom: Ent_Architecture
description: 'Résumé : Comment Contoso a mis en œuvre un site SharePoint pour les données hautement réglementées afin de faciliter la collaboration entre ses équipes de recherche.'
ms.openlocfilehash: ce813407c0f4c6f7b68aa997bf5e54b86a24ff2d
ms.sourcegitcommit: 9ee873c6a2f738a0c99921e036894b646742e706
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/15/2019
ms.locfileid: "38672710"
---
# <a name="sharepoint-site-for-highly-confidential-digital-assets-of-the-contoso-corporation"></a><span data-ttu-id="abee7-103">Site SharePoint pour les biens numériques hautement confidentiels de Contoso Corporation</span><span class="sxs-lookup"><span data-stu-id="abee7-103">SharePoint site for highly confidential digital assets of the Contoso Corporation</span></span>

<span data-ttu-id="abee7-104">Les biens les plus précieux de Contoso sont sa propriété intellectuelle sous la forme de secrets commerciaux, tels que des techniques de fabrication propriétaires et des spécifications de conception pour les produits en cours de développement.</span><span class="sxs-lookup"><span data-stu-id="abee7-104">Contoso's most valuable assets are its intellectual property in the form of trade secrets, such as proprietary manufacturing techniques, and design specifications for products that are in development.</span></span> <span data-ttu-id="abee7-105">Ces biens étaient sous forme numérique, stockés à l’origine en tant que fichiers sur un site SharePoint Server 2016.</span><span class="sxs-lookup"><span data-stu-id="abee7-105">These assets were in digital form, originally stored as files on a SharePoint Server 2016 site.</span></span> <span data-ttu-id="abee7-106">Lorsque Contoso a déployé Microsoft 365 Enterprise, il souhaitait faire passer ses biens numériques locaux dans le nuage pour faciliter l’accès et la collaboration ouverte entre les équipes de recherche à Paris, Moscou, New York, Pékin et Bangalore.</span><span class="sxs-lookup"><span data-stu-id="abee7-106">When Contoso deployed Microsoft 365 Enterprise, they wanted to transition their on-premises digital assets to the cloud for easier access and more open collaboration across research teams in Paris, Moscow, New York, Beijing, and Bangalore.</span></span> 
  
<span data-ttu-id="abee7-107">Toutefois, en raison de leur nature sensible, l’accès à ces fichiers doit être :</span><span class="sxs-lookup"><span data-stu-id="abee7-107">However, due to their sensitive nature, access to these files must be:</span></span>

- <span data-ttu-id="abee7-108">Limité à l’ensemble des personnes qui sont autorisées à y accéder.</span><span class="sxs-lookup"><span data-stu-id="abee7-108">Restricted to the set of people who are allowed access them.</span></span> 
- <span data-ttu-id="abee7-109">Protégé par une stratégie de protection contre la perte de données (DLP) pour empêcher les utilisateurs de les répartir hors du site.</span><span class="sxs-lookup"><span data-stu-id="abee7-109">Protected with a Data Loss Prevention (DLP) policy to prevent users from distributing them outside the site.</span></span>
- <span data-ttu-id="abee7-110">Chiffrés et protégés par des autorisations pour empêcher les utilisateurs non autorisés d’accéder à leur contenu, même s’ils sont distribués en dehors du site.</span><span class="sxs-lookup"><span data-stu-id="abee7-110">Encrypted and protected with permissions to prevent unauthorized users from accessing their contents, even if they are distributed outside the site.</span></span>

<span data-ttu-id="abee7-111">La sécurité et les administrateurs SharePoint du service informatique de contoso ont décidé d’utiliser un [site SharePoint pour les données hautement réglementées](teams-sharepoint-online-sites-highly-regulated-data.md).</span><span class="sxs-lookup"><span data-stu-id="abee7-111">Security and SharePoint administrators in Contoso's IT department decided to use a [SharePoint site for highly regulated data](teams-sharepoint-online-sites-highly-regulated-data.md).</span></span>
  
<span data-ttu-id="abee7-112">Contoso a utilisé ces étapes pour créer et sécuriser un site d’équipe SharePoint pour ses équipes de recherche.</span><span class="sxs-lookup"><span data-stu-id="abee7-112">Contoso used these steps to create and secure a SharePoint team sites for their research teams.</span></span>

## <a name="step-1-created-a-private-sharepoint-team-site"></a><span data-ttu-id="abee7-113">Étape 1 : création d’un site d’équipe SharePoint privé</span><span class="sxs-lookup"><span data-stu-id="abee7-113">Step 1: Created a private SharePoint team site</span></span>

<span data-ttu-id="abee7-114">Pour protéger l’accès au site SharePoint, contoso IT a configuré les [stratégies d’accès SharePoint recommandées](sharepoint-file-access-policies.md).</span><span class="sxs-lookup"><span data-stu-id="abee7-114">To protect access to the SharePoint site, Contoso IT configured the [recommended SharePoint access policies](sharepoint-file-access-policies.md).</span></span>

<span data-ttu-id="abee7-115">Ensuite, les administrateurs informatiques de contoso ont compilé une liste des comptes d’utilisateurs pour les chercheurs de Paris, Moscou, New York, Pékin et Bangalore.</span><span class="sxs-lookup"><span data-stu-id="abee7-115">Next, Contoso IT admins compiled a list of the user accounts for the researchers in their Paris, Moscow, New York, Beijing, and Bangalore offices.</span></span> 

<span data-ttu-id="abee7-116">Ensuite, un administrateur informatique de Contoso a créé un nouveau site d’équipe privé nommé **Research** et ajouté tous les comptes d’utilisateurs pour ses chercheurs.</span><span class="sxs-lookup"><span data-stu-id="abee7-116">Next, a Contoso IT admin created a new private team site named **Research** and added all of the user accounts for its researchers.</span></span>

<span data-ttu-id="abee7-117">Ils ont ensuite configuré des paramètres d’autorisation supplémentaires pour le site afin d’empêcher les chercheurs de partager l’accès au site et d’empêcher les non-chercheurs de demander l’accès au site.</span><span class="sxs-lookup"><span data-stu-id="abee7-117">Then they configured additional permission settings for the site to prevent researchers from sharing access to the site and to prevent non-researchers from requesting access to the site.</span></span>

## <a name="step-2-configured-the-site-for-a-restrictive-dlp-policy"></a><span data-ttu-id="abee7-118">Étape 2 : configuration du site pour une stratégie DLP restrictive</span><span class="sxs-lookup"><span data-stu-id="abee7-118">Step 2: Configured the site for a restrictive DLP policy</span></span>

<span data-ttu-id="abee7-119">Tout d’abord, les administrateurs de contoso ont appliqué l’étiquette de rétention Office 365 **hautement confidentiel** existante au dossier documents du site de **recherche** .</span><span class="sxs-lookup"><span data-stu-id="abee7-119">First, Contoso admins applied the existing **Highly Confidential** Office 365 retention label to the Documents folder of the **Research** site.</span></span>

<span data-ttu-id="abee7-120">Ensuite, ils ont créé une nouvelle stratégie DLP Office 365 nommée **Research** qui :</span><span class="sxs-lookup"><span data-stu-id="abee7-120">Next, they created a new Office 365 DLP policy named **Research** that:</span></span>

- <span data-ttu-id="abee7-121">Utilise l’étiquette de rétention Office 365 **hautement confidentiel** .</span><span class="sxs-lookup"><span data-stu-id="abee7-121">Uses the **Highly Confidential** Office 365 retention label.</span></span> 
- <span data-ttu-id="abee7-122">Bloque les utilisateurs lorsqu’ils tentent de partager une ressource numérique sur le site de **recherche** en dehors de contoso.</span><span class="sxs-lookup"><span data-stu-id="abee7-122">Blocks users when they attempt to share a digital asset on the **Research** site outside of Contoso.</span></span>

<span data-ttu-id="abee7-123">Pour plus d’informations sur la configuration, consultez la rubrique [protéger les fichiers SharePoint avec les étiquettes de rétention et DLP](https://docs.microsoft.com/office365/enterprise/protect-sharepoint-online-files-with-office-365-labels-and-dlp).</span><span class="sxs-lookup"><span data-stu-id="abee7-123">For the configuration details, see [Protect SharePoint files with retention labels and DLP](https://docs.microsoft.com/office365/enterprise/protect-sharepoint-online-files-with-office-365-labels-and-dlp).</span></span>

## <a name="step-4-created-an-office-365-sensitivity-sublabel-for-the-site"></a><span data-ttu-id="abee7-124">Étape 4 : création d’une sous-étiquette de confidentialité Office 365 pour le site</span><span class="sxs-lookup"><span data-stu-id="abee7-124">Step 4: Created an Office 365 sensitivity sublabel for the site</span></span>

<span data-ttu-id="abee7-125">Les administrateurs contoso ont créé une nouvelle sous-étiquette de confidentialité Office 365 nommée « **teams** » de l’étiquette **hautement confidentiel** qui :</span><span class="sxs-lookup"><span data-stu-id="abee7-125">Contoso admins created a new Office 365 sensitivity sublabel named **Research Teams** of the **Highly Confidential** label that:</span></span>

- <span data-ttu-id="abee7-126">Nécessite le chiffrement.</span><span class="sxs-lookup"><span data-stu-id="abee7-126">Requires encryption.</span></span>
- <span data-ttu-id="abee7-127">Autorise les autorisations de co-auteur pour le groupe de **recherche 365 Research** Office</span><span class="sxs-lookup"><span data-stu-id="abee7-127">Allows Co-Author permissions for the **Research** Office 365 group</span></span>
- <span data-ttu-id="abee7-128">S’applique au groupe Office **Research** Office 365</span><span class="sxs-lookup"><span data-stu-id="abee7-128">Applies to the **Research** Office 365 group</span></span>

<span data-ttu-id="abee7-129">Voici la configuration obtenue du site d’équipe de **recherche** pour les ressources hautement confidentielles.</span><span class="sxs-lookup"><span data-stu-id="abee7-129">Here is the resulting configuration of the **Research** team site for highly confidential assets.</span></span>

![La configuration obtenue du site d’équipe de recherche pour les ressources hautement confidentielles](./media/contoso-sharepoint-online-site-for-highly-confidential-assets/final-config.png)

<span data-ttu-id="abee7-131">Les fichiers dans les dossiers du site de **recherche** sont protégés par :</span><span class="sxs-lookup"><span data-stu-id="abee7-131">Files in folders of the **Research** site are protected by:</span></span>

- <span data-ttu-id="abee7-132">Les autorisations de site, qui autorisent uniquement l’accès aux membres du groupe Office **Research** Office 365.</span><span class="sxs-lookup"><span data-stu-id="abee7-132">The site permissions, which only allow access to members of the **Research** Office 365 group.</span></span>
- <span data-ttu-id="abee7-133">La stratégie DLP de **recherche** , qui utilise l’étiquette de rétention **hautement confidentielle** et les paramètres qui empêchent le partage du fichier avec des utilisateurs externes.</span><span class="sxs-lookup"><span data-stu-id="abee7-133">The **Research** DLP policy, which uses the **Highly Confidential** retention label and settings that prevent the file from being shared with external users.</span></span>
- <span data-ttu-id="abee7-134">Sous-étiquette de sensibilité des **équipes de recherche** , avec le chiffrement et les autorisations qui voyagent avec le fichier s’il est déplacé ou copié à partir du site de **recherche** .</span><span class="sxs-lookup"><span data-stu-id="abee7-134">The **Research Teams** sensitivity sublabel, with encryption and permissions that travel with the file if it is moved or copied from the **Research** site.</span></span>

<span data-ttu-id="abee7-135">Voici un exemple de fichier stocké sur le site de **recherche** avec la sous-étiquette de sensibilité **teams de recherche** affectée.</span><span class="sxs-lookup"><span data-stu-id="abee7-135">Here is an example of a file stored in the **Research** site with the **Research Teams** sensitivity sublabel assigned.</span></span>

![La configuration obtenue du site d’équipe de recherche pour les ressources hautement confidentielles](./media/contoso-sharepoint-online-site-for-highly-confidential-assets/final-config-example-file.png)


## <a name="step-5-migrated-the-on-premises-sharepoint-research-data"></a><span data-ttu-id="abee7-137">Étape 5 : migration des données de recherche SharePoint locales</span><span class="sxs-lookup"><span data-stu-id="abee7-137">Step 5: Migrated the on-premises SharePoint research data</span></span>

<span data-ttu-id="abee7-138">Les administrateurs de contoso ont déplacé tous les fichiers de recherche sur site du site SharePoint Server 2016 local vers des dossiers dans le nouveau site SharePoint de **recherche** .</span><span class="sxs-lookup"><span data-stu-id="abee7-138">Contoso admins moved all of the on-premises research files in the on-premises SharePoint Server 2016 site to folders in the new **Research** SharePoint site.</span></span>

## <a name="step-6-trained-their-researchers"></a><span data-ttu-id="abee7-139">Étape 6 : formation de leurs chercheurs</span><span class="sxs-lookup"><span data-stu-id="abee7-139">Step 6: Trained their researchers</span></span>

<span data-ttu-id="abee7-140">Le personnel de sécurité de Contoso a formé les membres du groupe **Research** Office 365 dans un cours obligatoire qui les a exécutées par les utilisateurs :</span><span class="sxs-lookup"><span data-stu-id="abee7-140">Contoso security staff trained the members of the **Research** Office 365 group in a mandatory course that stepped them through:</span></span>

- <span data-ttu-id="abee7-141">Comment accéder au nouveau site de **recherche** et à ses fichiers existants.</span><span class="sxs-lookup"><span data-stu-id="abee7-141">How to access the new **Research** site and its existing files.</span></span>
- <span data-ttu-id="abee7-142">Création de nouveaux fichiers sur le site et chargement de nouveaux fichiers stockés localement.</span><span class="sxs-lookup"><span data-stu-id="abee7-142">How to create new files on the site and upload new files stored locally.</span></span>
- <span data-ttu-id="abee7-143">Démonstration de la façon dont la stratégie DLP de **recherche** empêche les fichiers d’être partagés en externe.</span><span class="sxs-lookup"><span data-stu-id="abee7-143">A demonstration of how the **Research** DLP policy blocks files from being shared externally.</span></span>
- <span data-ttu-id="abee7-144">Comment étiqueter les fichiers avec la sous-étiquette de sensibilité des **équipes de recherche** .</span><span class="sxs-lookup"><span data-stu-id="abee7-144">How to label files with the **Research Teams** sensitivity sublabel.</span></span>
- <span data-ttu-id="abee7-145">Démonstration de la façon dont la sous-étiquette **Research teams** protège un fichier même lorsqu’il est divulgué à partir du site.</span><span class="sxs-lookup"><span data-stu-id="abee7-145">A demonstration of how the **Research Teams** sub-label protects a file even when it is leaked from the site.</span></span>

<span data-ttu-id="abee7-146">Le résultat final est un environnement sécurisé dans lequel les chercheurs peuvent collaborer entre Contoso dans un environnement sécurisé sur des fichiers contenant des informations de recherche.</span><span class="sxs-lookup"><span data-stu-id="abee7-146">The end result is a secure environment in which the researchers can collaborate across Contoso in a secure environment on files containing research information.</span></span> 

<span data-ttu-id="abee7-147">Si un document de recherche avec la sous-étiquette **Research teams** quitte le site de **recherche** , il est chiffré et accessible uniquement aux membres du groupe **Research** Office 365 avec des informations d’identification de compte d’utilisateur valides.</span><span class="sxs-lookup"><span data-stu-id="abee7-147">If a research document with the **Research Teams** sublabel leaves the **Research** site, it is encrypted and accessible only to members of the **Research** Office 365 group with valid user account credentials.</span></span>

## <a name="next-step"></a><span data-ttu-id="abee7-148">Étape suivante</span><span class="sxs-lookup"><span data-stu-id="abee7-148">Next step</span></span>

<span data-ttu-id="abee7-149">[Déployer](deploy-microsoft-365-enterprise.md) Microsoft 365 entreprise dans votre organisation.</span><span class="sxs-lookup"><span data-stu-id="abee7-149">[Deploy](deploy-microsoft-365-enterprise.md) Microsoft 365 Enterprise in your organization.</span></span>

## <a name="see-also"></a><span data-ttu-id="abee7-150">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="abee7-150">See also</span></span>

<span data-ttu-id="abee7-151">[Bibliothèque de productivité Microsoft 365](https://aka.ms/productivitylibrary)https://aka.ms/productivitylibrary)</span><span class="sxs-lookup"><span data-stu-id="abee7-151">[Microsoft 365 Productivity Library](https://aka.ms/productivitylibrary) (https://aka.ms/productivitylibrary)</span></span>
