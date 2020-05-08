---
title: Équipe isolée pour un projet à secret supérieur de Contoso Corporation
f1.keywords:
- NOCSH
ms.author: josephd
author: JoeDavies-MSFT
manager: laurawi
ms.date: 05/01/2020
audience: ITPro
ms.topic: overview
ms.prod: microsoft-365-enterprise
localization_priority: Normal
search.appverid:
- MET150
ms.collection:
- M365-security-compliance
- M365solutions
ms.custom: Ent_Architecture
description: 'Résumé : Comment Contoso a utilisé une équipe avec l’isolation de sécurité pour un projet à secret principal afin de développer une nouvelle suite de produits et de services.'
ms.openlocfilehash: 1083c9d3db3be9ca528b2eee40f072aa17c7431e
ms.sourcegitcommit: 9c828bc27cd73a1bb85e9fe38d818190025ebb3f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/07/2020
ms.locfileid: "44159454"
---
# <a name="isolated-team-for-a-top-secret-project-of-the-contoso-corporation"></a><span data-ttu-id="15ec8-103">Équipe isolée pour un projet à secret supérieur de Contoso Corporation</span><span class="sxs-lookup"><span data-stu-id="15ec8-103">Isolated team for a top-secret project of the Contoso Corporation</span></span>

<span data-ttu-id="15ec8-104">Après un cadre hors site, le PDG de Contoso a ordonné le développement d’une nouvelle suite de produits et de services qui pourrait doubler les bénéfices de contoso au cours des cinq prochaines années.</span><span class="sxs-lookup"><span data-stu-id="15ec8-104">After an executive offsite, Contoso’s CEO ordered the development of a new suite of products and services that could double Contoso’s profits in the next five years.</span></span> <span data-ttu-id="15ec8-105">Le projet de secret principal pour développer l’entreprise, l’ingénierie et le plan de marché a été nommé **Project 2x** et le personnel clé de l’entreprise ont été recrutés.</span><span class="sxs-lookup"><span data-stu-id="15ec8-105">The top-secret project to develop the business, engineering, and market plan was named **Project 2X** and key staff across the company were recruited.</span></span> 

<span data-ttu-id="15ec8-106">Les chronologies de recherche et de développement étaient étroites, ce qui signifiait que la collaboration devait être efficace et fournir des réunions sécurisées, des conversations en cours et le stockage de fichiers.</span><span class="sxs-lookup"><span data-stu-id="15ec8-106">The timelines for research and development were tight, which meant that collaboration had to be efficient and provide for secure meetings, ongoing conversations, and file storage.</span></span>

<span data-ttu-id="15ec8-107">Les livrables résultants pour Project 2X étaient des offres professionnelles, des spécifications de produits et d’ingénierie, ainsi que des documents et des plans de marketing sous forme de fichiers Word, Excel et PowerPoint.</span><span class="sxs-lookup"><span data-stu-id="15ec8-107">The resulting deliverables for Project 2X were business plans, product and engineering specifications, and marketing materials and schedules in the form of Word, Excel, and PowerPoint files.</span></span> 

<span data-ttu-id="15ec8-108">En raison de leur nature confidentielle, l’accès à ces fichiers était :</span><span class="sxs-lookup"><span data-stu-id="15ec8-108">Due to their sensitive nature, access to these files were:</span></span>

- <span data-ttu-id="15ec8-109">Limité à Project 2X membres de l’équipe.</span><span class="sxs-lookup"><span data-stu-id="15ec8-109">Restricted to Project 2X team members.</span></span>
- <span data-ttu-id="15ec8-110">Chiffrés et protégés par des autorisations pour permettre l’accès uniquement aux membres de l’équipe Project 2X, même si les fichiers ont été distribués en dehors de leurs dossiers sécurisés.</span><span class="sxs-lookup"><span data-stu-id="15ec8-110">Encrypted and protected with permissions to allow access only to Project 2X team members, even if the files were distributed outside of their secured folders.</span></span>

<span data-ttu-id="15ec8-111">Le personnel informatique de Contoso a utilisé une [équipe avec l’isolation de sécurité](secure-teams-security-isolation.md) pour Project 2x et ces étapes.</span><span class="sxs-lookup"><span data-stu-id="15ec8-111">Contoso IT staff used a [team with security isolation](secure-teams-security-isolation.md) for Project 2X and these steps.</span></span>

## <a name="step-1-created-a-private-team"></a><span data-ttu-id="15ec8-112">Étape 1 : création d’une équipe privée</span><span class="sxs-lookup"><span data-stu-id="15ec8-112">Step 1: Created a private team</span></span>

<span data-ttu-id="15ec8-113">Tout d’abord, pour protéger l’accès au site SharePoint sous-jacent pour l’équipe, les administrateurs informatiques de contoso ont configuré les [stratégies d’accès SharePoint recommandées](../enterprise/sharepoint-file-access-policies.md).</span><span class="sxs-lookup"><span data-stu-id="15ec8-113">First, to protect access to the underlying SharePoint site for the team, Contoso IT administrators configured the [recommended SharePoint access policies](../enterprise/sharepoint-file-access-policies.md).</span></span>

<span data-ttu-id="15ec8-114">Ensuite, un administrateur informatique de Contoso a créé une nouvelle équipe privée appelée Project 2X et a ajouté les comptes d’utilisateur de Project 2X personnel en tant que membres.</span><span class="sxs-lookup"><span data-stu-id="15ec8-114">Next, a Contoso IT administrator created a new private team named Project 2X and added the user accounts of Project 2X staff as members.</span></span>

<span data-ttu-id="15ec8-115">Pour plus d’informations sur la configuration, consultez la rubrique [Create a private Team](secure-teams-security-isolation.md#create-a-private-team).</span><span class="sxs-lookup"><span data-stu-id="15ec8-115">For the configuration details, see [Create a private team](secure-teams-security-isolation.md#create-a-private-team).</span></span>

## <a name="step-2-created-a-sensitivity-label-for-the-project-2x-team"></a><span data-ttu-id="15ec8-116">Étape 2 : création d’une étiquette de critère de diffusion pour l’équipe Project 2X</span><span class="sxs-lookup"><span data-stu-id="15ec8-116">Step 2: Created a sensitivity label for the Project 2X team</span></span>

<span data-ttu-id="15ec8-117">Les administrateurs contoso ont créé une étiquette de sensibilité nommée **Project 2x** qui :</span><span class="sxs-lookup"><span data-stu-id="15ec8-117">Contoso admins created a new sensitivity label named **Project 2X** that:</span></span>

- <span data-ttu-id="15ec8-118">Nécessite le chiffrement.</span><span class="sxs-lookup"><span data-stu-id="15ec8-118">Requires encryption.</span></span>
- <span data-ttu-id="15ec8-119">Autorise les autorisations de co-auteur pour le projet 2X groupe Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="15ec8-119">Allows Co-Author permissions for the Project 2X Microsoft 365 group.</span></span>

<span data-ttu-id="15ec8-120">Les fichiers de la section **documents** du projet sous-jacent 2 SharePoint ont été protégés par :</span><span class="sxs-lookup"><span data-stu-id="15ec8-120">Files in the **Documents** section of the underlying Project 2X SharePoint site were protected by:</span></span>

- <span data-ttu-id="15ec8-121">Les autorisations de site, qui autorisent uniquement l’accès aux membres du projet 2X groupe Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="15ec8-121">The site permissions, which only allow access to members of the Project 2X Microsoft 365 group.</span></span>
- <span data-ttu-id="15ec8-122">L’étiquette de sensibilité Project 2X, avec le chiffrement et les autorisations qui transitent avec le fichier s’il est déplacé ou copié à partir du site.</span><span class="sxs-lookup"><span data-stu-id="15ec8-122">The Project 2X sensitivity label, with encryption and permissions that travel with the file if it is moved or copied from the site.</span></span>

<span data-ttu-id="15ec8-123">Pour plus d’informations sur la configuration, consultez la rubrique [Create a Sensitivity label](secure-teams-security-isolation.md#create-a-sensitivity-label).</span><span class="sxs-lookup"><span data-stu-id="15ec8-123">For the configuration details, see [Create a sensitivity label](secure-teams-security-isolation.md#create-a-sensitivity-label).</span></span>

## <a name="step-3-configured-the-underlying-sharepoint-site"></a><span data-ttu-id="15ec8-124">Étape 3 : configuration du site SharePoint sous-jacent</span><span class="sxs-lookup"><span data-stu-id="15ec8-124">Step 3: Configured the underlying SharePoint site</span></span>

<span data-ttu-id="15ec8-125">Tout d’abord, pour protéger l’accès au site SharePoint sous-jacent pour l’équipe, les administrateurs informatiques de contoso ont configuré les [stratégies d’accès SharePoint recommandées](../enterprise/sharepoint-file-access-policies.md).</span><span class="sxs-lookup"><span data-stu-id="15ec8-125">First, to protect access to the underlying SharePoint site for the team, Contoso IT administrators configured the [recommended SharePoint access policies](../enterprise/sharepoint-file-access-policies.md).</span></span>

<span data-ttu-id="15ec8-126">Ensuite, ils ont configuré des paramètres d’autorisation supplémentaires pour le site afin d’empêcher Project 2X de partager l’accès au site.</span><span class="sxs-lookup"><span data-stu-id="15ec8-126">Next, they configured additional permission settings for the site to prevent Project 2X from sharing access to the site.</span></span> <span data-ttu-id="15ec8-127">Pour plus d’informations sur la configuration, consultez la rubrique [paramètres SharePoint pour une équipe avec isolation de sécurité](secure-teams-security-isolation.md#sharepoint-settings).</span><span class="sxs-lookup"><span data-stu-id="15ec8-127">For the configuration details, see [SharePoint settings for a team with security isolation](secure-teams-security-isolation.md#sharepoint-settings).</span></span>

<span data-ttu-id="15ec8-128">Voici la configuration obtenue de l’équipe Project 2X.</span><span class="sxs-lookup"><span data-stu-id="15ec8-128">Here is the resulting configuration of the Project 2X team.</span></span>

![La configuration obtenue de l’équipe Project 2X](../media/contoso-team-for-top-secret-project/contoso-team-for-top-secret-project.png)

 ## <a name="step-4-trained-project-2x-team-members"></a><span data-ttu-id="15ec8-130">Étape 4 : projet formé 2X membres de l’équipe</span><span class="sxs-lookup"><span data-stu-id="15ec8-130">Step 4: Trained Project 2X team members</span></span>

<span data-ttu-id="15ec8-131">Le personnel de sécurité de Contoso a formé le projet 2 membres d’équipe dans un cours obligatoire qui les a exécutés par les utilisateurs :</span><span class="sxs-lookup"><span data-stu-id="15ec8-131">Contoso security staff trained the Project 2X team members in a mandatory course that stepped them through:</span></span>

- <span data-ttu-id="15ec8-132">Comment accéder au nouveau projet 2 équipe, utiliser des réunions et des conversations et collaborer sur des fichiers d’équipe.</span><span class="sxs-lookup"><span data-stu-id="15ec8-132">How to access the new Project 2X team, use meetings and chats, and how to collaborate on team files.</span></span>
- <span data-ttu-id="15ec8-133">Comment créer des fichiers dans l’équipe et télécharger de nouveaux fichiers créés localement.</span><span class="sxs-lookup"><span data-stu-id="15ec8-133">How to create new files in the team and upload new files created locally.</span></span>
- <span data-ttu-id="15ec8-134">Démonstration de la façon dont la stratégie DLP empêche les fichiers d’être partagés en externe.</span><span class="sxs-lookup"><span data-stu-id="15ec8-134">A demonstration of how the DLP policy blocks files from being shared externally.</span></span>
- <span data-ttu-id="15ec8-135">Comment étiqueter les fichiers avec l’étiquette de sensibilité Project 2X.</span><span class="sxs-lookup"><span data-stu-id="15ec8-135">How to label files with the Project 2X sensitivity label.</span></span>
- <span data-ttu-id="15ec8-136">Démonstration de la façon dont l’étiquette Project 2X protège un fichier même lorsqu’il quitte l’équipe.</span><span class="sxs-lookup"><span data-stu-id="15ec8-136">A demonstration of how the Project 2X  label protects a file even when it leaves the team.</span></span>

<span data-ttu-id="15ec8-137">Le résultat final était un environnement sécurisé dans lequel Project 2 membres de l’équipe ont collaboré dans un environnement sécurisé pour les conversations, les réunions et les fichiers.</span><span class="sxs-lookup"><span data-stu-id="15ec8-137">The end result was a secure environment in which Project 2X team members collaborated in a secure environment for chats, meetings, and files.</span></span>

<span data-ttu-id="15ec8-138">Voici un exemple de fichier stocké dans le site du projet 2 sous-jacent avec l’étiquette de sensibilité de projet 2 affectée.</span><span class="sxs-lookup"><span data-stu-id="15ec8-138">Here is an example of a file stored in the underlying Project 2X site with the Project 2X sensitivity label assigned.</span></span>

![Exemple de fichier stocké dans le site du projet 2 sous-jacent](../media/contoso-team-for-top-secret-project/contoso-team-for-top-secret-project-example.png)

<span data-ttu-id="15ec8-140">Dans quelques exemples, Project 2X les membres de l’équipe ont téléchargé des fichiers protégés par l’étiquette Project 2X sur un lecteur local pour le travail hors connexion.</span><span class="sxs-lookup"><span data-stu-id="15ec8-140">In a couple of instances, Project 2X team members downloaded files protected by the Project 2X label to a local drive for offline work.</span></span> <span data-ttu-id="15ec8-141">Toutefois, une fois que vous êtes invité à entrer les informations d’identification lors de leur ouverture, elles ont fait l’erreur et les ont supprimées.</span><span class="sxs-lookup"><span data-stu-id="15ec8-141">However, after being prompted for credentials when opening them, they realized their mistake and deleted them.</span></span>

<span data-ttu-id="15ec8-142">En raison de l’environnement de collaboration de teams et des fonctionnalités de sécurité de Microsoft 365, les détails du projet 2X étaient secrets pendant toute la durée du projet.</span><span class="sxs-lookup"><span data-stu-id="15ec8-142">Because of the collaboration environment of Teams and the security features of Microsoft 365, the details of Project 2X were kept secret for the duration of the project.</span></span> <span data-ttu-id="15ec8-143">Contoso a annoncé ses plans et est en train de déployer les nouveaux produits et services à l’esprit de ses clients et investisseurs, ainsi que les chagrin de ses concurrents.</span><span class="sxs-lookup"><span data-stu-id="15ec8-143">Contoso announced its plans and is in the process of rolling out the new products and services to the delight of its customers and investors and the chagrin of its competitors.</span></span>

## <a name="next-step"></a><span data-ttu-id="15ec8-144">Étape suivante</span><span class="sxs-lookup"><span data-stu-id="15ec8-144">Next step</span></span>

<span data-ttu-id="15ec8-145">[Déployer une équipe avec l’isolation de sécurité](secure-teams-security-isolation.md) dans votre organisation.</span><span class="sxs-lookup"><span data-stu-id="15ec8-145">[Deploy a team with security isolation](secure-teams-security-isolation.md) in your organization.</span></span>

