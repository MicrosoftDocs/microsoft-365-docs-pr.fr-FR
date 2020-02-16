---
title: Faire équipe pour un projet top secret de Contoso Corporation
f1.keywords:
- NOCSH
ms.author: josephd
author: JoeDavies-MSFT
manager: laurawi
ms.date: 11/18/2019
audience: ITPro
ms.topic: overview
ms.service: o365-solutions
localization_priority: Normal
search.appverid:
- MET150
ms.collection: M365-security-compliance
ms.custom: Ent_Architecture
description: 'Résumé : Comment Contoso a utilisé une équipe pour les données hautement réglementées pour un projet à forte priorité afin de développer une nouvelle suite de produits et de services.'
ms.openlocfilehash: 58d381751db3e94f35a0c1b8f7a14c191918e754
ms.sourcegitcommit: 3dd9944a6070a7f35c4bc2b57df397f844c3fe79
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/15/2020
ms.locfileid: "42068024"
---
# <a name="team-for-a-top-secret-project-of-the-contoso-corporation"></a><span data-ttu-id="dadb9-103">Faire équipe pour un projet top secret de Contoso Corporation</span><span class="sxs-lookup"><span data-stu-id="dadb9-103">Team for a top-secret project of the Contoso Corporation</span></span>

<span data-ttu-id="dadb9-104">Après un cadre hors site, le PDG de Contoso a ordonné le développement d’une nouvelle suite de produits et de services qui pourrait doubler les bénéfices de contoso au cours des cinq prochaines années.</span><span class="sxs-lookup"><span data-stu-id="dadb9-104">After an executive offsite, Contoso’s CEO ordered the development of a new suite of products and services that could double Contoso’s profits in the next five years.</span></span> <span data-ttu-id="dadb9-105">Le projet de secret principal pour développer l’entreprise, l’ingénierie et le plan de marché a été nommé **Project 2x** et le personnel clé de l’entreprise ont été recrutés.</span><span class="sxs-lookup"><span data-stu-id="dadb9-105">The top-secret project to develop the business, engineering, and market plan was named **Project 2X** and key staff across the company were recruited.</span></span> 

<span data-ttu-id="dadb9-106">Les chronologies de recherche et de développement étaient étroites, ce qui signifiait que la collaboration devait être efficace et fournir des réunions sécurisées, des conversations en cours et le stockage de fichiers.</span><span class="sxs-lookup"><span data-stu-id="dadb9-106">The timelines for research and development were tight, which meant that collaboration had to be efficient and provide for secure meetings, ongoing conversations, and file storage.</span></span>

<span data-ttu-id="dadb9-107">Les livrables résultants pour Project 2X étaient des offres professionnelles, des spécifications de produits et d’ingénierie, ainsi que des documents et des plans de marketing sous forme de fichiers Word, Excel et PowerPoint.</span><span class="sxs-lookup"><span data-stu-id="dadb9-107">The resulting deliverables for Project 2X were business plans, product and engineering specifications, and marketing materials and schedules in the form of Word, Excel, and PowerPoint files.</span></span> 

<span data-ttu-id="dadb9-108">En raison de leur nature confidentielle, l’accès à ces fichiers était :</span><span class="sxs-lookup"><span data-stu-id="dadb9-108">Due to their sensitive nature, access to these files were:</span></span>

- <span data-ttu-id="dadb9-109">Limité à Project 2X membres de l’équipe.</span><span class="sxs-lookup"><span data-stu-id="dadb9-109">Restricted to Project 2X team members.</span></span>
- <span data-ttu-id="dadb9-110">Protégé par une stratégie de protection contre la perte de données (DLP) pour empêcher Project 2 membres de l’équipe de les partager en dehors de l’équipe.</span><span class="sxs-lookup"><span data-stu-id="dadb9-110">Protected with a Data Loss Prevention (DLP) policy to prevent Project 2X team members from sharing them outside the team.</span></span>
- <span data-ttu-id="dadb9-111">Chiffrés et protégés par des autorisations pour permettre l’accès uniquement aux membres de l’équipe Project 2X, même si les fichiers ont été distribués en dehors de contoso.</span><span class="sxs-lookup"><span data-stu-id="dadb9-111">Encrypted and protected with permissions to allow access only to Project 2X team members, even if the files were distributed outside of Contoso.</span></span>

<span data-ttu-id="dadb9-112">Le personnel informatique de Contoso a utilisé une [équipe pour les données hautement réglementées](secure-teams-highly-regulated-data-scenario.md) pour Project 2x et les étapes suivantes.</span><span class="sxs-lookup"><span data-stu-id="dadb9-112">Contoso IT staff used a [team for highly-regulated data](secure-teams-highly-regulated-data-scenario.md) for Project 2X and these steps.</span></span>

## <a name="step-1-created-a-private-team-and-locked-down-the-underlying-sharepoint-site"></a><span data-ttu-id="dadb9-113">Étape 1 : création d’une équipe privée et verrouillage du site SharePoint sous-jacent</span><span class="sxs-lookup"><span data-stu-id="dadb9-113">Step 1: Created a private team and locked down the underlying SharePoint site</span></span>

<span data-ttu-id="dadb9-114">Pour protéger l’accès au site SharePoint sous-jacent pour l’équipe, les administrateurs informatiques de contoso ont configuré les [stratégies d’accès SharePoint recommandées](sharepoint-file-access-policies.md).</span><span class="sxs-lookup"><span data-stu-id="dadb9-114">To protect access to the underlying SharePoint site for the team, Contoso IT administrators configured the [recommended SharePoint access policies](sharepoint-file-access-policies.md).</span></span>

<span data-ttu-id="dadb9-115">Ensuite, un administrateur informatique de Contoso a créé une nouvelle équipe privée appelée Project 2X et a ajouté les comptes d’utilisateur de Project 2X personnel en tant que membres.</span><span class="sxs-lookup"><span data-stu-id="dadb9-115">Next, a Contoso IT administrator created a new private team named Project 2X and added the user accounts of Project 2X staff as members.</span></span>

<span data-ttu-id="dadb9-116">Ensuite, ils ont configuré des paramètres d’autorisation supplémentaires pour le site afin d’empêcher Project 2X de partager l’accès au site et d’empêcher d’autres personnes de demander l’accès au site.</span><span class="sxs-lookup"><span data-stu-id="dadb9-116">Next, they configured additional permission settings for the site to prevent Project 2X from sharing access to the site and to prevent other from requesting access to the site.</span></span>

<span data-ttu-id="dadb9-117">Pour plus d’informations sur la configuration, consultez la rubrique [paramètres SharePoint d’une équipe hautement réglementée](https://docs.microsoft.com/microsoft-365/security/office-365-security/deploy-teams-three-tiers#highly-confidential-teams).</span><span class="sxs-lookup"><span data-stu-id="dadb9-117">For the configuration details, see [SharePoint settings for a highly regulated team](https://docs.microsoft.com/microsoft-365/security/office-365-security/deploy-teams-three-tiers#highly-confidential-teams).</span></span>

## <a name="step-2-configured-a-dlp-policy-and-the-underlying-site-for-a-retention-label"></a><span data-ttu-id="dadb9-118">Étape 2 : configuration d’une stratégie DLP et du site sous-jacent pour une étiquette de rétention</span><span class="sxs-lookup"><span data-stu-id="dadb9-118">Step 2: Configured a DLP policy and the underlying site for a retention label</span></span> 

<span data-ttu-id="dadb9-119">Tout d’abord, contoso admins a appliqué l’étiquette de rétention Office 365 **hautement confidentiel** existante à la section **documents** du site SharePoint sous-jacent de l’équipe Project 2x.</span><span class="sxs-lookup"><span data-stu-id="dadb9-119">First, Contoso admins applied the existing **Highly Confidential** Office 365 retention label to the **Documents** section of the underlying SharePoint site of the Project 2X team.</span></span>

<span data-ttu-id="dadb9-120">Ensuite, ils ont créé une nouvelle stratégie DLP Office 365 nommée **Project 2x** qui :</span><span class="sxs-lookup"><span data-stu-id="dadb9-120">Next, they created a new Office 365 DLP policy named **Project 2X** that:</span></span>

- <span data-ttu-id="dadb9-121">Utilise l’étiquette de rétention Office 365 hautement confidentiel.</span><span class="sxs-lookup"><span data-stu-id="dadb9-121">Uses the Highly Confidential Office 365 retention label.</span></span>
- <span data-ttu-id="dadb9-122">Bloque les utilisateurs lorsqu’ils tentent de partager un fichier dans l’équipe Project 2X en dehors de contoso.</span><span class="sxs-lookup"><span data-stu-id="dadb9-122">Blocks users when they attempt to share a file in the Project 2X team outside of Contoso.</span></span>

<span data-ttu-id="dadb9-123">Pour plus d’informations sur la configuration, consultez la rubrique [protéger les fichiers dans teams avec les étiquettes de rétention et DLP](https://docs.microsoft.com/microsoft-365/security/office-365-security/deploy-teams-retention-dlp).</span><span class="sxs-lookup"><span data-stu-id="dadb9-123">For the configuration details, see [Protect files in teams with retention labels and DLP](https://docs.microsoft.com/microsoft-365/security/office-365-security/deploy-teams-retention-dlp).</span></span>

## <a name="step-3-created-an-office-365-sensitivity-label-for-the-project-2x-team"></a><span data-ttu-id="dadb9-124">Étape 3 : création d’une étiquette de confidentialité Office 365 pour l’équipe Project 2X</span><span class="sxs-lookup"><span data-stu-id="dadb9-124">Step 3: Created an Office 365 sensitivity label for the Project 2X team</span></span>

<span data-ttu-id="dadb9-125">Les administrateurs contoso ont créé une étiquette de confidentialité Office 365 nommée **Project 2x** qui :</span><span class="sxs-lookup"><span data-stu-id="dadb9-125">Contoso admins created a new Office 365 sensitivity label named **Project 2X** that:</span></span>

- <span data-ttu-id="dadb9-126">Nécessite le chiffrement.</span><span class="sxs-lookup"><span data-stu-id="dadb9-126">Requires encryption.</span></span>
- <span data-ttu-id="dadb9-127">Autorise les autorisations de co-auteur pour le groupe 2 d’Office 365.</span><span class="sxs-lookup"><span data-stu-id="dadb9-127">Allows Co-Author permissions for the Project 2X Office 365 group.</span></span>

<span data-ttu-id="dadb9-128">Voici la configuration obtenue de l’équipe Project 2X.</span><span class="sxs-lookup"><span data-stu-id="dadb9-128">Here is the resulting configuration of the Project 2X team.</span></span>

![La configuration obtenue de l’équipe Project 2X](../media/contoso-team-for-highly-confidential-assets/final-config.png)
 
<span data-ttu-id="dadb9-130">Les fichiers de la section documents du projet sous-jacent 2 SharePoint ont été protégés par :</span><span class="sxs-lookup"><span data-stu-id="dadb9-130">Files in the Documents section of the underlying Project 2X SharePoint site were protected by:</span></span>

- <span data-ttu-id="dadb9-131">Les autorisations de site, qui autorisent uniquement l’accès aux membres du groupe 2 d’Office 365.</span><span class="sxs-lookup"><span data-stu-id="dadb9-131">The site permissions, which only allow access to members of the Project 2X Office 365 group.</span></span>
- <span data-ttu-id="dadb9-132">Étiquette de rétention hautement confidentielle, automatiquement affectée aux nouveaux fichiers.</span><span class="sxs-lookup"><span data-stu-id="dadb9-132">The  Highly Confidential retention label, which is automatically assigned to new files.</span></span>
- <span data-ttu-id="dadb9-133">Stratégie DLP qui utilise l’étiquette de rétention hautement confidentielle et les paramètres qui empêchent le partage du fichier avec les utilisateurs externes.</span><span class="sxs-lookup"><span data-stu-id="dadb9-133">A DLP policy that uses the Highly Confidential retention label and settings that block the file from being shared with external users.</span></span>
- <span data-ttu-id="dadb9-134">L’étiquette de sensibilité Project 2X, avec le chiffrement et les autorisations qui transitent avec le fichier s’il est déplacé ou copié à partir du site.</span><span class="sxs-lookup"><span data-stu-id="dadb9-134">The Project 2X sensitivity label, with encryption and permissions that travel with the file if it is moved or copied from the site.</span></span>

<span data-ttu-id="dadb9-135">Voici un exemple de fichier stocké dans le site Project 2X sous-jacent avec l’étiquette de rétention hautement réglementée et l’étiquette de sensibilité du projet 2X attribuée.</span><span class="sxs-lookup"><span data-stu-id="dadb9-135">Here is an example of a file stored in the underlying Project 2X site with the Highly Regulated retention label and the Project 2X sensitivity label assigned.</span></span>

![Exemple de fichier stocké dans le site du projet 2 sous-jacent](../media/contoso-team-for-highly-confidential-assets/final-config-example-file.png)
 
## <a name="step-4-trained-project-2x-team-members"></a><span data-ttu-id="dadb9-137">Étape 4 : projet formé 2X membres de l’équipe</span><span class="sxs-lookup"><span data-stu-id="dadb9-137">Step 4: Trained Project 2X team members</span></span>

<span data-ttu-id="dadb9-138">Le personnel de sécurité de Contoso a formé le projet 2 membres d’équipe dans un cours obligatoire qui les a exécutés par les utilisateurs :</span><span class="sxs-lookup"><span data-stu-id="dadb9-138">Contoso security staff trained the Project 2X team members in a mandatory course that stepped them through:</span></span>

- <span data-ttu-id="dadb9-139">Comment accéder au nouveau projet 2 équipe, utiliser des réunions et des conversations et collaborer sur des fichiers d’équipe.</span><span class="sxs-lookup"><span data-stu-id="dadb9-139">How to access the new Project 2X team, use meetings and chats, and how to collaborate on team files.</span></span>
- <span data-ttu-id="dadb9-140">Comment créer des fichiers dans l’équipe et télécharger de nouveaux fichiers créés localement.</span><span class="sxs-lookup"><span data-stu-id="dadb9-140">How to create new files in the team and upload new files created locally.</span></span>
- <span data-ttu-id="dadb9-141">Démonstration de la façon dont la stratégie DLP empêche les fichiers d’être partagés en externe.</span><span class="sxs-lookup"><span data-stu-id="dadb9-141">A demonstration of how the DLP policy blocks files from being shared externally.</span></span>
- <span data-ttu-id="dadb9-142">Comment étiqueter les fichiers avec l’étiquette de sensibilité Project 2X.</span><span class="sxs-lookup"><span data-stu-id="dadb9-142">How to label files with the Project 2X sensitivity label.</span></span>
- <span data-ttu-id="dadb9-143">Démonstration de la façon dont l’étiquette Project 2X protège un fichier même lorsqu’il quitte l’équipe.</span><span class="sxs-lookup"><span data-stu-id="dadb9-143">A demonstration of how the Project 2X  label protects a file even when it leaves the team.</span></span>

<span data-ttu-id="dadb9-144">Le résultat final était un environnement sécurisé dans lequel Project 2 membres de l’équipe ont collaboré dans un environnement sécurisé pour les conversations, les réunions et les fichiers.</span><span class="sxs-lookup"><span data-stu-id="dadb9-144">The end result was a secure environment in which Project 2X team members collaborated in a secure environment for chats, meetings, and files.</span></span>

<span data-ttu-id="dadb9-145">Dans quelques exemples, Project 2X les membres de l’équipe ont téléchargé des fichiers protégés par l’étiquette Project 2X sur un lecteur local pour le travail hors connexion.</span><span class="sxs-lookup"><span data-stu-id="dadb9-145">In a couple of instances, Project 2X team members downloaded files protected by the Project 2X label to a local drive for offline work.</span></span> <span data-ttu-id="dadb9-146">Toutefois, une fois que vous êtes invité à entrer les informations d’identification lors de leur ouverture, elles ont fait l’erreur et les ont supprimées.</span><span class="sxs-lookup"><span data-stu-id="dadb9-146">However, after being prompted for credentials when opening them, they realized their mistake and deleted them.</span></span>

<span data-ttu-id="dadb9-147">En raison de l’environnement de collaboration de teams et des fonctionnalités de sécurité de Microsoft 365, les détails du projet 2X étaient secrets pendant toute la durée du projet.</span><span class="sxs-lookup"><span data-stu-id="dadb9-147">Because of the collaboration environment of Teams and the security features of Microsoft 365, the details of Project 2X were kept secret for the duration of the project.</span></span> <span data-ttu-id="dadb9-148">Contoso a annoncé ses plans et est en train de déployer les nouveaux produits et services à l’esprit de ses clients et investisseurs, ainsi que les chagrin de ses concurrents.</span><span class="sxs-lookup"><span data-stu-id="dadb9-148">Contoso announced its plans and is in the process of rolling out the new products and services to the delight of its customers and investors and the chagrin of its competitors.</span></span>

## <a name="next-step"></a><span data-ttu-id="dadb9-149">Étape suivante</span><span class="sxs-lookup"><span data-stu-id="dadb9-149">Next step</span></span>

<span data-ttu-id="dadb9-150">[Déployer](deploy-microsoft-365-enterprise.md) Microsoft 365 entreprise dans votre organisation.</span><span class="sxs-lookup"><span data-stu-id="dadb9-150">[Deploy](deploy-microsoft-365-enterprise.md) Microsoft 365 Enterprise in your organization.</span></span>

## <a name="see-also"></a><span data-ttu-id="dadb9-151">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="dadb9-151">See also</span></span>

<span data-ttu-id="dadb9-152">[Bibliothèque de productivité Microsoft 365](https://aka.ms/productivitylibrary)https://aka.ms/productivitylibrary)</span><span class="sxs-lookup"><span data-stu-id="dadb9-152">[Microsoft 365 Productivity Library](https://aka.ms/productivitylibrary) (https://aka.ms/productivitylibrary)</span></span>
