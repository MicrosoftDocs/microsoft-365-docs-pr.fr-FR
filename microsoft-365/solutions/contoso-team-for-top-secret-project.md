---
title: Équipe isolée pour un projet à secret supérieur de Contoso Corporation
f1.keywords:
- NOCSH
ms.author: josephd
author: JoeDavies-MSFT
manager: laurawi
ms.date: 08/14/2020
audience: ITPro
ms.topic: overview
ms.prod: microsoft-365-enterprise
localization_priority: Normal
search.appverid:
- MET150
ms.collection:
- M365-security-compliance
ms.custom: Ent_Architecture
description: 'Résumé : Comment Contoso a utilisé une équipe avec l’isolation de sécurité pour un projet à secret principal afin de développer une nouvelle suite de produits et de services.'
ms.openlocfilehash: ba9a66d2419e81aeb1eac026b16c0475ac6d0614
ms.sourcegitcommit: 1780359234abdf081097c8064438d415da92fb85
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/17/2020
ms.locfileid: "46778583"
---
# <a name="isolated-team-for-a-top-secret-project-of-the-contoso-corporation"></a><span data-ttu-id="35f48-103">Équipe isolée pour un projet à secret supérieur de Contoso Corporation</span><span class="sxs-lookup"><span data-stu-id="35f48-103">Isolated team for a top-secret project of the Contoso Corporation</span></span>

<span data-ttu-id="35f48-104">Après un cadre hors site, le PDG de Contoso a ordonné le développement d’une nouvelle suite de produits et de services qui pourrait doubler les bénéfices de contoso au cours des cinq prochaines années.</span><span class="sxs-lookup"><span data-stu-id="35f48-104">After an executive offsite, Contoso’s CEO ordered the development of a new suite of products and services that could double Contoso’s profits in the next five years.</span></span> <span data-ttu-id="35f48-105">Le projet de secret principal pour développer l’entreprise, l’ingénierie et le plan de marché a été nommé **Project 2x** et le personnel clé de l’entreprise ont été recrutés.</span><span class="sxs-lookup"><span data-stu-id="35f48-105">The top-secret project to develop the business, engineering, and market plan was named **Project 2X** and key staff across the company were recruited.</span></span> 

<span data-ttu-id="35f48-106">Les chronologies de recherche et de développement étaient étroites, ce qui signifiait que la collaboration devait être efficace et fournir des réunions sécurisées, des conversations en cours et le stockage de fichiers.</span><span class="sxs-lookup"><span data-stu-id="35f48-106">The timelines for research and development were tight, which meant that collaboration had to be efficient and provide for secure meetings, ongoing conversations, and file storage.</span></span>

<span data-ttu-id="35f48-107">Les livrables résultants pour Project 2X étaient des offres professionnelles, des spécifications de produits et d’ingénierie, ainsi que des documents et des plans de marketing sous forme de fichiers Word, Excel et PowerPoint.</span><span class="sxs-lookup"><span data-stu-id="35f48-107">The resulting deliverables for Project 2X were business plans, product and engineering specifications, and marketing materials and schedules in the form of Word, Excel, and PowerPoint files.</span></span> 

<span data-ttu-id="35f48-108">En raison de leur nature confidentielle, l’accès à ces fichiers était :</span><span class="sxs-lookup"><span data-stu-id="35f48-108">Due to their sensitive nature, access to these files were:</span></span>

- <span data-ttu-id="35f48-109">Limité à Project 2X membres de l’équipe et leadership senior.</span><span class="sxs-lookup"><span data-stu-id="35f48-109">Restricted to Project 2X team members and senior leadership.</span></span>
- <span data-ttu-id="35f48-110">Chiffrés et protégés par des autorisations pour permettre l’accès uniquement aux membres de l’équipe Project 2X et aux dirigeants, même si les fichiers ont été distribués en dehors de leurs dossiers sécurisés.</span><span class="sxs-lookup"><span data-stu-id="35f48-110">Encrypted and protected with permissions to allow access only to Project 2X team members and senior leadership, even if the files were distributed outside of their secured folders.</span></span>

<span data-ttu-id="35f48-111">Le personnel informatique de Contoso a utilisé une [équipe avec l’isolation de sécurité](secure-teams-security-isolation.md) pour Project 2x et ces étapes.</span><span class="sxs-lookup"><span data-stu-id="35f48-111">Contoso IT staff used a [team with security isolation](secure-teams-security-isolation.md) for Project 2X and these steps.</span></span>

## <a name="step-1-created-a-private-team"></a><span data-ttu-id="35f48-112">Étape 1 : création d’une équipe privée</span><span class="sxs-lookup"><span data-stu-id="35f48-112">Step 1: Created a private team</span></span>

<span data-ttu-id="35f48-113">Tout d’abord, pour protéger l’accès au site SharePoint sous-jacent pour l’équipe, les administrateurs informatiques de contoso ont configuré les [stratégies d’accès SharePoint recommandées](../enterprise/sharepoint-file-access-policies.md).</span><span class="sxs-lookup"><span data-stu-id="35f48-113">First, to protect access to the underlying SharePoint site for the team, Contoso IT administrators configured the [recommended SharePoint access policies](../enterprise/sharepoint-file-access-policies.md).</span></span>

<span data-ttu-id="35f48-114">Ensuite, un administrateur informatique de Contoso a créé une nouvelle équipe privée appelée Project 2X et a ajouté les comptes d’utilisateur de Project 2X personnel en tant que membres.</span><span class="sxs-lookup"><span data-stu-id="35f48-114">Next, a Contoso IT administrator created a new private team named Project 2X and added the user accounts of Project 2X staff as members.</span></span> <span data-ttu-id="35f48-115">Ils ont également configuré l’équipe de sorte que seuls les propriétaires d’équipe Project 2X puissent créer des canaux privés.</span><span class="sxs-lookup"><span data-stu-id="35f48-115">They also configured the team so that only Project 2X team owners can create private channels.</span></span>

<span data-ttu-id="35f48-116">Pour plus d’informations sur la configuration, consultez la rubrique [Create a private Team](secure-teams-security-isolation.md#create-a-private-team).</span><span class="sxs-lookup"><span data-stu-id="35f48-116">For the configuration details, see [Create a private team](secure-teams-security-isolation.md#create-a-private-team).</span></span>

## <a name="step-2-created-a-sensitivity-label-for-the-project-2x-team"></a><span data-ttu-id="35f48-117">Étape 2 : création d’une étiquette de critère de diffusion pour l’équipe Project 2X</span><span class="sxs-lookup"><span data-stu-id="35f48-117">Step 2: Created a sensitivity label for the Project 2X team</span></span>

<span data-ttu-id="35f48-118">Les administrateurs contoso ont créé une étiquette de sensibilité nommée **Project 2x** qui :</span><span class="sxs-lookup"><span data-stu-id="35f48-118">Contoso admins created a new sensitivity label named **Project 2X** that:</span></span>

- <span data-ttu-id="35f48-119">Chiffrement activé.</span><span class="sxs-lookup"><span data-stu-id="35f48-119">Enabled encryption.</span></span>
- <span data-ttu-id="35f48-120">Autorisation de co-auteur autorisée pour le projet 2X groupe Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="35f48-120">Allowed Co-Author permissions for the Project 2X Microsoft 365 group.</span></span>
- <span data-ttu-id="35f48-121">Autorisations de la visionneuse autorisées pour le groupe de leadership senior.</span><span class="sxs-lookup"><span data-stu-id="35f48-121">Allowed Viewer permissions for the Senior Leadership group.</span></span>
- <span data-ttu-id="35f48-122">Blocage de l’accès aux appareils non gérés.</span><span class="sxs-lookup"><span data-stu-id="35f48-122">Blocked access to unmanaged devices.</span></span>

<span data-ttu-id="35f48-123">Les fichiers de la section **documents** du projet sous-jacent 2 SharePoint ont été protégés par :</span><span class="sxs-lookup"><span data-stu-id="35f48-123">Files in the **Documents** section of the underlying Project 2X SharePoint site were protected by:</span></span>

- <span data-ttu-id="35f48-124">Les autorisations de site, qui autorisent uniquement les autorisations maximales pour les membres du projet 2X groupe Microsoft 365 et les autorisations de lecture sur le groupe de leadership senior.</span><span class="sxs-lookup"><span data-stu-id="35f48-124">The site permissions, which only allow full permissions to members of the Project 2X Microsoft 365 group and read permissions to the Senior Leadership group.</span></span>
- <span data-ttu-id="35f48-125">L’étiquette de sensibilité Project 2X, avec le chiffrement et les autorisations qui transitent avec le fichier s’il est déplacé ou copié à partir du site.</span><span class="sxs-lookup"><span data-stu-id="35f48-125">The Project 2X sensitivity label, with encryption and permissions that travel with the file if it is moved or copied from the site.</span></span>

<span data-ttu-id="35f48-126">Pour plus d’informations sur la configuration, consultez la rubrique [Create a Sensitivity label](secure-teams-security-isolation.md#create-a-sensitivity-label).</span><span class="sxs-lookup"><span data-stu-id="35f48-126">For the configuration details, see [Create a sensitivity label](secure-teams-security-isolation.md#create-a-sensitivity-label).</span></span>

## <a name="step-3-configured-the-underlying-sharepoint-site"></a><span data-ttu-id="35f48-127">Étape 3 : configuration du site SharePoint sous-jacent</span><span class="sxs-lookup"><span data-stu-id="35f48-127">Step 3: Configured the underlying SharePoint site</span></span>

<span data-ttu-id="35f48-128">Tout d’abord, pour protéger l’accès au site SharePoint sous-jacent pour l’équipe, les administrateurs informatiques de contoso ont configuré les [stratégies d’accès SharePoint recommandées](../enterprise/sharepoint-file-access-policies.md).</span><span class="sxs-lookup"><span data-stu-id="35f48-128">First, to protect access to the underlying SharePoint site for the team, Contoso IT administrators configured the [recommended SharePoint access policies](../enterprise/sharepoint-file-access-policies.md).</span></span>

<span data-ttu-id="35f48-129">Ensuite, ils ont configuré des paramètres d’autorisation supplémentaires pour le site :</span><span class="sxs-lookup"><span data-stu-id="35f48-129">Next, they configured additional permission settings for the site:</span></span>

- <span data-ttu-id="35f48-130">Pour empêcher Project 2X membres du groupe de partager l’accès au site.</span><span class="sxs-lookup"><span data-stu-id="35f48-130">To prevent Project 2X group members from sharing access to the site.</span></span> <span data-ttu-id="35f48-131">Pour plus d’informations sur la configuration, consultez la rubrique [paramètres SharePoint pour une équipe avec isolation de sécurité](secure-teams-security-isolation.md#sharepoint-settings).</span><span class="sxs-lookup"><span data-stu-id="35f48-131">For the configuration details, see [SharePoint settings for a team with security isolation](secure-teams-security-isolation.md#sharepoint-settings).</span></span>
- <span data-ttu-id="35f48-132">Pour les autorisations de lecture pour le groupe de leadership senior.</span><span class="sxs-lookup"><span data-stu-id="35f48-132">For Read permissions for the Senior Leadership group.</span></span>

<span data-ttu-id="35f48-133">Ensuite, ils ont configuré des paramètres d’autorisation supplémentaires pour le site afin d’empêcher Project 2X membres du groupe de partager l’accès au site.</span><span class="sxs-lookup"><span data-stu-id="35f48-133">Next, they configured additional permission settings for the site to prevent Project 2X group members from sharing access to the site.</span></span> 

<span data-ttu-id="35f48-134">Comme les canaux privés pour le projet 2X ont été créés, le propriétaire du groupe a désactivé le partage d’invité et définit le lien de partage par défaut sur la valeur de **personnes spécifiques** .</span><span class="sxs-lookup"><span data-stu-id="35f48-134">As private channels for the Project 2X were created, the group owner disabled guest sharing and set the default sharing link to the **Specific people** value.</span></span>

<span data-ttu-id="35f48-135">Voici la configuration obtenue de l’équipe Project 2X avec l’isolation de sécurité.</span><span class="sxs-lookup"><span data-stu-id="35f48-135">Here is the resulting configuration of the Project 2X team with security isolation.</span></span>

![La configuration obtenue de l’équipe Project 2X](../media/contoso-team-for-top-secret-project/contoso-team-for-top-secret-project.png)

 ## <a name="step-4-trained-project-2x-team-members"></a><span data-ttu-id="35f48-137">Étape 4 : projet formé 2X membres de l’équipe</span><span class="sxs-lookup"><span data-stu-id="35f48-137">Step 4: Trained Project 2X team members</span></span>

<span data-ttu-id="35f48-138">Le personnel de sécurité de Contoso a formé le projet 2 membres d’équipe dans un cours obligatoire qui les a exécutés par les utilisateurs :</span><span class="sxs-lookup"><span data-stu-id="35f48-138">Contoso security staff trained the Project 2X team members in a mandatory course that stepped them through:</span></span>

- <span data-ttu-id="35f48-139">Comment accéder au nouveau projet 2 équipe, utiliser des réunions et des conversations et collaborer sur des fichiers d’équipe.</span><span class="sxs-lookup"><span data-stu-id="35f48-139">How to access the new Project 2X team, use meetings and chats, and how to collaborate on team files.</span></span>
- <span data-ttu-id="35f48-140">Comment créer des fichiers dans l’équipe et télécharger de nouveaux fichiers créés localement.</span><span class="sxs-lookup"><span data-stu-id="35f48-140">How to create new files in the team and upload new files created locally.</span></span>
- <span data-ttu-id="35f48-141">Comment étiqueter les fichiers avec l’étiquette de sensibilité Project 2X.</span><span class="sxs-lookup"><span data-stu-id="35f48-141">How to label files with the Project 2X sensitivity label.</span></span>
- <span data-ttu-id="35f48-142">Démonstration de la façon dont l’étiquette Project 2X protège un fichier même lorsqu’il quitte l’équipe.</span><span class="sxs-lookup"><span data-stu-id="35f48-142">A demonstration of how the Project 2X  label protects a file even when it leaves the team.</span></span>

<span data-ttu-id="35f48-143">Le résultat final était un environnement sécurisé dans lequel Project 2 membres de l’équipe ont collaboré dans un environnement sécurisé pour les conversations, les réunions et les fichiers.</span><span class="sxs-lookup"><span data-stu-id="35f48-143">The end result was a secure environment in which Project 2X team members collaborated in a secure environment for chats, meetings, and files.</span></span>

<span data-ttu-id="35f48-144">Voici un exemple de fichier stocké dans le site du projet 2 sous-jacent avec l’étiquette de sensibilité de projet 2 affectée.</span><span class="sxs-lookup"><span data-stu-id="35f48-144">Here is an example of a file stored in the underlying Project 2X site with the Project 2X sensitivity label assigned.</span></span>

![Exemple de fichier stocké dans le site du projet 2 sous-jacent](../media/contoso-team-for-top-secret-project/contoso-team-for-top-secret-project-example.png)

<span data-ttu-id="35f48-146">Dans quelques exemples, Project 2X les membres de l’équipe ont téléchargé des fichiers protégés par l’étiquette Project 2X sur un lecteur local pour le travail hors connexion.</span><span class="sxs-lookup"><span data-stu-id="35f48-146">In a couple of instances, Project 2X team members downloaded files protected by the Project 2X label to a local drive for offline work.</span></span> 

<span data-ttu-id="35f48-147">Toutefois, une fois que vous êtes invité à entrer les informations d’identification lors de leur ouverture, elles ont fait l’erreur et les ont supprimées.</span><span class="sxs-lookup"><span data-stu-id="35f48-147">However, after being prompted for credentials when opening them, they realized their mistake and deleted them.</span></span>

<span data-ttu-id="35f48-148">En raison de l’environnement de collaboration de teams et des fonctionnalités de sécurité de Microsoft 365, les détails du projet 2X étaient secrets pendant toute la durée du projet.</span><span class="sxs-lookup"><span data-stu-id="35f48-148">Because of the collaboration environment of Teams and the security features of Microsoft 365, the details of Project 2X were kept secret for the duration of the project.</span></span> <span data-ttu-id="35f48-149">Contoso a annoncé ses plans et est en train de déployer les nouveaux produits et services à l’esprit de ses clients et investisseurs, ainsi que les chagrin de ses concurrents.</span><span class="sxs-lookup"><span data-stu-id="35f48-149">Contoso announced its plans and is in the process of rolling out the new products and services to the delight of its customers and investors and the chagrin of its competitors.</span></span>

## <a name="next-step"></a><span data-ttu-id="35f48-150">Étape suivante</span><span class="sxs-lookup"><span data-stu-id="35f48-150">Next step</span></span>

<span data-ttu-id="35f48-151">[Déployer une équipe avec l’isolation de sécurité](secure-teams-security-isolation.md) dans votre organisation.</span><span class="sxs-lookup"><span data-stu-id="35f48-151">[Deploy a team with security isolation](secure-teams-security-isolation.md) in your organization.</span></span>

