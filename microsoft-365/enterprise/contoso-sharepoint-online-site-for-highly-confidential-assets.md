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
ms.openlocfilehash: 08676f9fa89d9cbf932f9d70664ad1d17a153e3b
ms.sourcegitcommit: 80dc9ceb14e3eb3ae61b0fc2c8c3d73d564a7ef9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/21/2019
ms.locfileid: "37617252"
---
# <a name="sharepoint-site-for-highly-confidential-digital-assets-of-the-contoso-corporation"></a><span data-ttu-id="adc74-103">Site SharePoint pour les biens numériques hautement confidentiels de Contoso Corporation</span><span class="sxs-lookup"><span data-stu-id="adc74-103">SharePoint site for highly confidential digital assets of the Contoso Corporation</span></span>

 <span data-ttu-id="adc74-104">**Résumé :** Comment Contoso a mis en œuvre un site SharePoint pour les données hautement réglementées afin de faciliter la collaboration entre ses équipes de recherche.</span><span class="sxs-lookup"><span data-stu-id="adc74-104">**Summary:** How Contoso implemented a SharePoint site for highly regulated data for easier collaboration between its research teams.</span></span>
  
<span data-ttu-id="adc74-105">Les biens les plus précieux de Contoso sont sa propriété intellectuelle sous la forme de secrets commerciaux, tels que des techniques de fabrication propriétaires et des spécifications de conception pour les produits en cours de développement.</span><span class="sxs-lookup"><span data-stu-id="adc74-105">Contoso's most valuable assets are its intellectual property in the form of trade secrets, such as proprietary manufacturing techniques, and design specifications for products that are in development.</span></span> <span data-ttu-id="adc74-106">Ces biens étaient sous forme numérique, stockés à l’origine en tant que fichiers sur un site SharePoint Server 2016.</span><span class="sxs-lookup"><span data-stu-id="adc74-106">These assets were in digital form, originally stored as files on a SharePoint Server 2016 site.</span></span> <span data-ttu-id="adc74-107">Lorsque Contoso a déployé Microsoft 365 Enterprise, il souhaitait faire passer ses biens numériques locaux dans le nuage pour faciliter l’accès et la collaboration ouverte entre les équipes de recherche à Paris, Moscou, New York, Pékin et Bangalore.</span><span class="sxs-lookup"><span data-stu-id="adc74-107">When Contoso deployed Microsoft 365 Enterprise, they wanted to transition their on-premises digital assets to the cloud for easier access and more open collaboration across research teams in Paris, Moscow, New York, Beijing, and Bangalore.</span></span> 
  
<span data-ttu-id="adc74-108">Toutefois, en raison de leur nature sensible, l’accès à ces fichiers doit être :</span><span class="sxs-lookup"><span data-stu-id="adc74-108">However, due to their sensitive nature, access to these files must be:</span></span>

- <span data-ttu-id="adc74-109">Limité à l’ensemble des personnes qui sont autorisées à y accéder.</span><span class="sxs-lookup"><span data-stu-id="adc74-109">Restricted to the set of people who are allowed access them.</span></span> 
- <span data-ttu-id="adc74-110">Protégé par une stratégie de protection contre la perte de données (DLP) pour empêcher les utilisateurs de les répartir hors du site.</span><span class="sxs-lookup"><span data-stu-id="adc74-110">Protected with a Data Loss Prevention (DLP) policy to prevent users from distributing them outside the site.</span></span>
- <span data-ttu-id="adc74-111">Chiffrés et protégés par des autorisations pour empêcher les utilisateurs non autorisés d’accéder à leur contenu, même s’ils sont distribués en dehors du site.</span><span class="sxs-lookup"><span data-stu-id="adc74-111">Encrypted and protected with permissions to prevent unauthorized users from accessing their contents, even if they are distributed outside the site.</span></span>

<span data-ttu-id="adc74-112">La sécurité et les administrateurs SharePoint du service informatique de contoso ont décidé d’utiliser un [site SharePoint pour les données hautement réglementées](teams-sharepoint-online-sites-highly-regulated-data.md).</span><span class="sxs-lookup"><span data-stu-id="adc74-112">Security and SharePoint administrators in Contoso's IT department decided to use a [SharePoint site for highly regulated data](teams-sharepoint-online-sites-highly-regulated-data.md).</span></span>
  
<span data-ttu-id="adc74-113">Contoso a utilisé ces étapes pour créer et sécuriser un site d’équipe SharePoint pour ses équipes de recherche.</span><span class="sxs-lookup"><span data-stu-id="adc74-113">Contoso used these steps to create and secure a SharePoint team sites for their research teams.</span></span>

## <a name="step-1-created-a-private-sharepoint-team-site"></a><span data-ttu-id="adc74-114">Étape 1 : création d’un site d’équipe SharePoint privé</span><span class="sxs-lookup"><span data-stu-id="adc74-114">Step 1: Created a private SharePoint team site</span></span>

<span data-ttu-id="adc74-115">Pour protéger l’accès au site SharePoint, contoso IT a configuré les [stratégies d’accès SharePoint recommandées](sharepoint-file-access-policies.md).</span><span class="sxs-lookup"><span data-stu-id="adc74-115">To protect access to the SharePoint site, Contoso IT configured the [recommended SharePoint access policies](sharepoint-file-access-policies.md).</span></span>

<span data-ttu-id="adc74-116">Ensuite, les administrateurs informatiques de contoso ont compilé une liste des comptes d’utilisateurs pour les chercheurs de Paris, Moscou, New York, Pékin et Bangalore.</span><span class="sxs-lookup"><span data-stu-id="adc74-116">Next, Contoso IT admins compiled a list of the user accounts for the researchers in their Paris, Moscow, New York, Beijing, and Bangalore offices.</span></span> 

<span data-ttu-id="adc74-117">Ensuite, un administrateur informatique de Contoso a créé un nouveau site d’équipe privé nommé **Research** et ajouté tous les comptes d’utilisateurs pour ses chercheurs.</span><span class="sxs-lookup"><span data-stu-id="adc74-117">Next, a Contoso IT admin created a new private team site named **Research** and added all of the user accounts for its researchers.</span></span>

<span data-ttu-id="adc74-118">Ils ont ensuite configuré des paramètres d’autorisation supplémentaires pour le site afin d’empêcher les chercheurs de partager l’accès au site et d’empêcher les non-chercheurs de demander l’accès au site.</span><span class="sxs-lookup"><span data-stu-id="adc74-118">Then they configured additional permission settings for the site to prevent researchers from sharing access to the site and to prevent non-researchers from requesting access to the site.</span></span>

## <a name="step-2-configured-the-site-for-a-restrictive-dlp-policy"></a><span data-ttu-id="adc74-119">Étape 2 : configuration du site pour une stratégie DLP restrictive</span><span class="sxs-lookup"><span data-stu-id="adc74-119">Step 2: Configured the site for a restrictive DLP policy</span></span>

<span data-ttu-id="adc74-120">Tout d’abord, les administrateurs de contoso ont appliqué l’étiquette de rétention Office 365 **hautement confidentiel** existante au dossier documents du site de **recherche** .</span><span class="sxs-lookup"><span data-stu-id="adc74-120">First, Contoso admins applied the existing **Highly Confidential** Office 365 retention label to the Documents folder of the **Research** site.</span></span>

<span data-ttu-id="adc74-121">Ensuite, ils ont créé une nouvelle stratégie DLP Office 365 nommée **Research** qui :</span><span class="sxs-lookup"><span data-stu-id="adc74-121">Next, they created a new Office 365 DLP policy named **Research** that:</span></span>

- <span data-ttu-id="adc74-122">Utilise l’étiquette de rétention Office 365 **hautement confidentiel** .</span><span class="sxs-lookup"><span data-stu-id="adc74-122">Uses the **Highly Confidential** Office 365 retention label.</span></span> 
- <span data-ttu-id="adc74-123">Bloque les utilisateurs lorsqu’ils tentent de partager une ressource numérique sur le site de **recherche** en dehors de contoso.</span><span class="sxs-lookup"><span data-stu-id="adc74-123">Blocks users when they attempt to share a digital asset on the **Research** site outside of Contoso.</span></span>

<span data-ttu-id="adc74-124">Pour plus d’informations sur la configuration, consultez la rubrique [protéger les fichiers SharePoint avec les étiquettes de rétention et DLP](https://docs.microsoft.com/office365/enterprise/protect-sharepoint-online-files-with-office-365-labels-and-dlp).</span><span class="sxs-lookup"><span data-stu-id="adc74-124">For the configuration details, see [Protect SharePoint files with retention labels and DLP](https://docs.microsoft.com/office365/enterprise/protect-sharepoint-online-files-with-office-365-labels-and-dlp).</span></span>

## <a name="step-4-created-an-office-365-sensitivity-sublabel-for-the-site"></a><span data-ttu-id="adc74-125">Étape 4 : création d’une sous-étiquette de confidentialité Office 365 pour le site</span><span class="sxs-lookup"><span data-stu-id="adc74-125">Step 4: Created an Office 365 sensitivity sublabel for the site</span></span>

<span data-ttu-id="adc74-126">Les administrateurs contoso ont créé une nouvelle sous-étiquette de confidentialité Office 365 nommée « **teams** » de l’étiquette **hautement confidentiel** qui :</span><span class="sxs-lookup"><span data-stu-id="adc74-126">Contoso admins created a new Office 365 sensitivity sublabel named **Research Teams** of the **Highly Confidential** label that:</span></span>

- <span data-ttu-id="adc74-127">Nécessite le chiffrement.</span><span class="sxs-lookup"><span data-stu-id="adc74-127">Requires encryption.</span></span>
- <span data-ttu-id="adc74-128">Autorise les autorisations de co-auteur pour le groupe de **recherche 365 Research** Office</span><span class="sxs-lookup"><span data-stu-id="adc74-128">Allows Co-Author permissions for the **Research** Office 365 group</span></span>
- <span data-ttu-id="adc74-129">S’applique au groupe Office **Research** Office 365</span><span class="sxs-lookup"><span data-stu-id="adc74-129">Applies to the **Research** Office 365 group</span></span>

<span data-ttu-id="adc74-130">Voici la configuration obtenue du site d’équipe de **recherche** pour les ressources hautement confidentielles.</span><span class="sxs-lookup"><span data-stu-id="adc74-130">Here is the resulting configuration of the **Research** team site for highly confidential assets.</span></span>

![La configuration obtenue du site d’équipe de recherche pour les ressources hautement confidentielles](./media/contoso-sharepoint-online-site-for-highly-confidential-assets/final-config.png)

<span data-ttu-id="adc74-132">Les fichiers dans les dossiers du site de **recherche** sont protégés par :</span><span class="sxs-lookup"><span data-stu-id="adc74-132">Files in folders of the **Research** site are protected by:</span></span>

- <span data-ttu-id="adc74-133">Les autorisations de site, qui autorisent uniquement l’accès aux membres du groupe Office **Research** Office 365.</span><span class="sxs-lookup"><span data-stu-id="adc74-133">The site permissions, which only allow access to members of the **Research** Office 365 group.</span></span>
- <span data-ttu-id="adc74-134">La stratégie DLP de **recherche** , qui utilise l’étiquette de rétention **hautement confidentielle** et les paramètres qui empêchent le partage du fichier avec des utilisateurs externes.</span><span class="sxs-lookup"><span data-stu-id="adc74-134">The **Research** DLP policy, which uses the **Highly Confidential** retention label and settings that prevent the file from being shared with external users.</span></span>
- <span data-ttu-id="adc74-135">Sous-étiquette de sensibilité des **équipes de recherche** , avec le chiffrement et les autorisations qui voyagent avec le fichier s’il est déplacé ou copié à partir du site de **recherche** .</span><span class="sxs-lookup"><span data-stu-id="adc74-135">The **Research Teams** sensitivity sublabel, with encryption and permissions that travel with the file if it is moved or copied from the **Research** site.</span></span>

<span data-ttu-id="adc74-136">Voici un exemple de fichier stocké sur le site de **recherche** avec la sous-étiquette de sensibilité **teams de recherche** affectée.</span><span class="sxs-lookup"><span data-stu-id="adc74-136">Here is an example of a file stored in the **Research** site with the **Research Teams** sensitivity sublabel assigned.</span></span>

![La configuration obtenue du site d’équipe de recherche pour les ressources hautement confidentielles](./media/contoso-sharepoint-online-site-for-highly-confidential-assets/final-config-example-file.png)


## <a name="step-5-migrated-the-on-premises-sharepoint-research-data"></a><span data-ttu-id="adc74-138">Étape 5 : migration des données de recherche SharePoint locales</span><span class="sxs-lookup"><span data-stu-id="adc74-138">Step 5: Migrated the on-premises SharePoint research data</span></span>

<span data-ttu-id="adc74-139">Les administrateurs de contoso ont déplacé tous les fichiers de recherche sur site du site SharePoint Server 2016 local vers des dossiers dans le nouveau site SharePoint de **recherche** .</span><span class="sxs-lookup"><span data-stu-id="adc74-139">Contoso admins moved all of the on-premises research files in the on-premises SharePoint Server 2016 site to folders in the new **Research** SharePoint site.</span></span>

## <a name="step-6-trained-their-researchers"></a><span data-ttu-id="adc74-140">Étape 6 : formation de leurs chercheurs</span><span class="sxs-lookup"><span data-stu-id="adc74-140">Step 6: Trained their researchers</span></span>

<span data-ttu-id="adc74-141">Le personnel de sécurité de Contoso a formé les membres du groupe **Research** Office 365 dans un cours obligatoire qui les a exécutées par les utilisateurs :</span><span class="sxs-lookup"><span data-stu-id="adc74-141">Contoso security staff trained the members of the **Research** Office 365 group in a mandatory course that stepped them through:</span></span>

- <span data-ttu-id="adc74-142">Comment accéder au nouveau site de **recherche** et à ses fichiers existants.</span><span class="sxs-lookup"><span data-stu-id="adc74-142">How to access the new **Research** site and its existing files.</span></span>
- <span data-ttu-id="adc74-143">Création de nouveaux fichiers sur le site et chargement de nouveaux fichiers stockés localement.</span><span class="sxs-lookup"><span data-stu-id="adc74-143">How to create new files on the site and upload new files stored locally.</span></span>
- <span data-ttu-id="adc74-144">Démonstration de la façon dont la stratégie DLP de **recherche** empêche les fichiers d’être partagés en externe.</span><span class="sxs-lookup"><span data-stu-id="adc74-144">A demonstration of how the **Research** DLP policy blocks files from being shared externally.</span></span>
- <span data-ttu-id="adc74-145">Comment étiqueter les fichiers avec la sous-étiquette de sensibilité des **équipes de recherche** .</span><span class="sxs-lookup"><span data-stu-id="adc74-145">How to label files with the **Research Teams** sensitivity sublabel.</span></span>
- <span data-ttu-id="adc74-146">Démonstration de la façon dont la sous-étiquette **Research teams** protège un fichier même lorsqu’il est divulgué à partir du site.</span><span class="sxs-lookup"><span data-stu-id="adc74-146">A demonstration of how the **Research Teams** sub-label protects a file even when it is leaked from the site.</span></span>

<span data-ttu-id="adc74-147">Le résultat final est un environnement sécurisé dans lequel les chercheurs peuvent collaborer entre Contoso dans un environnement sécurisé sur des fichiers contenant des informations de recherche.</span><span class="sxs-lookup"><span data-stu-id="adc74-147">The end result is a secure environment in which the researchers can collaborate across Contoso in a secure environment on files containing research information.</span></span> 

<span data-ttu-id="adc74-148">Si un document de recherche avec la sous-étiquette **Research teams** quitte le site de **recherche** , il est chiffré et accessible uniquement aux membres du groupe **Research** Office 365 avec des informations d’identification de compte d’utilisateur valides.</span><span class="sxs-lookup"><span data-stu-id="adc74-148">If a research document with the **Research Teams** sublabel leaves the **Research** site, it is encrypted and accessible only to members of the **Research** Office 365 group with valid user account credentials.</span></span>

## <a name="next-step"></a><span data-ttu-id="adc74-149">Étape suivante</span><span class="sxs-lookup"><span data-stu-id="adc74-149">Next step</span></span>

<span data-ttu-id="adc74-150">[Déployer](deploy-microsoft-365-enterprise.md) Microsoft 365 entreprise dans votre organisation.</span><span class="sxs-lookup"><span data-stu-id="adc74-150">[Deploy](deploy-microsoft-365-enterprise.md) Microsoft 365 Enterprise in your organization.</span></span>

## <a name="see-also"></a><span data-ttu-id="adc74-151">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="adc74-151">See also</span></span>

<span data-ttu-id="adc74-152">[Bibliothèque de productivité Microsoft 365](https://aka.ms/productivitylibrary)https://aka.ms/productivitylibrary)</span><span class="sxs-lookup"><span data-stu-id="adc74-152">[Microsoft 365 Productivity Library](https://aka.ms/productivitylibrary) (https://aka.ms/productivitylibrary)</span></span>
