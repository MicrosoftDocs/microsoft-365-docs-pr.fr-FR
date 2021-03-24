---
title: Équipe isolée pour un projet top secret de Contoso Corporation
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
description: 'Résumé : Comment Contoso a utilisé une équipe avec isolation de sécurité pour un projet top secret afin de développer une nouvelle suite de produits et services.'
ms.openlocfilehash: d5ab2808251ff6a53f8975ea868431691d3301e2
ms.sourcegitcommit: 956176ed7c8b8427fdc655abcd1709d86da9447e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/23/2021
ms.locfileid: "51051005"
---
# <a name="isolated-team-for-a-top-secret-project-of-the-contoso-corporation"></a><span data-ttu-id="098e8-103">Équipe isolée pour un projet top secret de Contoso Corporation</span><span class="sxs-lookup"><span data-stu-id="098e8-103">Isolated team for a top-secret project of the Contoso Corporation</span></span>

<span data-ttu-id="098e8-104">Après un site hors site, le PDG de Contoso a commandé le développement d’une nouvelle suite de produits et services qui pourrait doubler les bénéfices de Contoso au cours des cinq prochaines années.</span><span class="sxs-lookup"><span data-stu-id="098e8-104">After an executive offsite, Contoso’s CEO ordered the development of a new suite of products and services that could double Contoso’s profits in the next five years.</span></span> <span data-ttu-id="098e8-105">Le projet top secret pour développer l’entreprise, l’ingénierie et l’offre de marché était nommé **Project 2X** et le personnel clé au sein de l’entreprise a été embauché.</span><span class="sxs-lookup"><span data-stu-id="098e8-105">The top-secret project to develop the business, engineering, and market plan was named **Project 2X** and key staff across the company were recruited.</span></span> 

<span data-ttu-id="098e8-106">La chronologie de la recherche et du développement était étroite, ce qui signifie que la collaboration devait être efficace et fournir des réunions sécurisées, des conversations en cours et un stockage de fichiers.</span><span class="sxs-lookup"><span data-stu-id="098e8-106">The timelines for research and development were tight, which meant that collaboration had to be efficient and provide for secure meetings, ongoing conversations, and file storage.</span></span>

<span data-ttu-id="098e8-107">Les livrables pour Project 2X étaient des plans d’entreprise, des spécifications de produit et d’ingénierie, ainsi que des supports et des planifications marketing sous la forme de fichiers Word, Excel et PowerPoint.</span><span class="sxs-lookup"><span data-stu-id="098e8-107">The resulting deliverables for Project 2X were business plans, product and engineering specifications, and marketing materials and schedules in the form of Word, Excel, and PowerPoint files.</span></span> 

<span data-ttu-id="098e8-108">En raison de leur nature sensible, l’accès à ces fichiers était :</span><span class="sxs-lookup"><span data-stu-id="098e8-108">Due to their sensitive nature, access to these files were:</span></span>

- <span data-ttu-id="098e8-109">Limité aux membres de l’équipe Project 2X et à la direction.</span><span class="sxs-lookup"><span data-stu-id="098e8-109">Restricted to Project 2X team members and senior leadership.</span></span>
- <span data-ttu-id="098e8-110">Chiffré et protégé par des autorisations permettant d’autoriser l’accès uniquement aux membres de l’équipe Project 2X et à la direction, même si les fichiers ont été distribués en dehors de leurs dossiers sécurisés.</span><span class="sxs-lookup"><span data-stu-id="098e8-110">Encrypted and protected with permissions to allow access only to Project 2X team members and senior leadership, even if the files were distributed outside of their secured folders.</span></span>

<span data-ttu-id="098e8-111">Le personnel informatique de Contoso a utilisé une équipe avec isolation [de la sécurité](secure-teams-security-isolation.md) pour Project 2X et ces étapes.</span><span class="sxs-lookup"><span data-stu-id="098e8-111">Contoso IT staff used a [team with security isolation](secure-teams-security-isolation.md) for Project 2X and these steps.</span></span>

## <a name="step-1-created-a-private-team"></a><span data-ttu-id="098e8-112">Étape 1 : Création d’une équipe privée</span><span class="sxs-lookup"><span data-stu-id="098e8-112">Step 1: Created a private team</span></span>

<span data-ttu-id="098e8-113">Tout d’abord, pour protéger l’accès au site SharePoint sous-jacent pour l’équipe, les administrateurs informatiques de Contoso ont configuré les stratégies d’accès [SharePoint recommandées.](../security/defender-365-security/sharepoint-file-access-policies.md)</span><span class="sxs-lookup"><span data-stu-id="098e8-113">First, to protect access to the underlying SharePoint site for the team, Contoso IT administrators configured the [recommended SharePoint access policies](../security/defender-365-security/sharepoint-file-access-policies.md).</span></span>

<span data-ttu-id="098e8-114">Ensuite, un administrateur informatique de Contoso a créé une équipe privée nommée Project 2X et ajouté les comptes d’utilisateur du personnel Project 2X en tant que membres.</span><span class="sxs-lookup"><span data-stu-id="098e8-114">Next, a Contoso IT administrator created a new private team named Project 2X and added the user accounts of Project 2X staff as members.</span></span> <span data-ttu-id="098e8-115">Ils ont également configuré l’équipe de sorte que seuls les propriétaires d’équipe Project 2X peuvent créer des canaux privés.</span><span class="sxs-lookup"><span data-stu-id="098e8-115">They also configured the team so that only Project 2X team owners can create private channels.</span></span>

<span data-ttu-id="098e8-116">Pour plus d’informations sur la configuration, voir [Créer une équipe privée.](secure-teams-security-isolation.md#create-a-private-team)</span><span class="sxs-lookup"><span data-stu-id="098e8-116">For the configuration details, see [Create a private team](secure-teams-security-isolation.md#create-a-private-team).</span></span>

## <a name="step-2-created-a-sensitivity-label-for-the-project-2x-team"></a><span data-ttu-id="098e8-117">Étape 2 : Création d’une étiquette de niveau de sensibilité pour l’équipe Project 2X</span><span class="sxs-lookup"><span data-stu-id="098e8-117">Step 2: Created a sensitivity label for the Project 2X team</span></span>

<span data-ttu-id="098e8-118">Les administrateurs Contoso ont créé une étiquette de sensibilité **nommée Project 2X** qui :</span><span class="sxs-lookup"><span data-stu-id="098e8-118">Contoso admins created a new sensitivity label named **Project 2X** that:</span></span>

- <span data-ttu-id="098e8-119">Chiffrement activé.</span><span class="sxs-lookup"><span data-stu-id="098e8-119">Enabled encryption.</span></span>
- <span data-ttu-id="098e8-120">Autorisations Co-Author autorisations pour le groupe Microsoft 2X Project 365.</span><span class="sxs-lookup"><span data-stu-id="098e8-120">Allowed Co-Author permissions for the Project 2X Microsoft 365 group.</span></span>
- <span data-ttu-id="098e8-121">Autorisations de visionneuse autorisées pour le groupe Senior Leadership.</span><span class="sxs-lookup"><span data-stu-id="098e8-121">Allowed Viewer permissions for the Senior Leadership group.</span></span>
- <span data-ttu-id="098e8-122">Accès bloqué aux appareils non utilisés.</span><span class="sxs-lookup"><span data-stu-id="098e8-122">Blocked access to unmanaged devices.</span></span>

<span data-ttu-id="098e8-123">Les fichiers de la section **Documents** du site SharePoint Project 2X sous-jacent étaient protégés par :</span><span class="sxs-lookup"><span data-stu-id="098e8-123">Files in the **Documents** section of the underlying Project 2X SharePoint site were protected by:</span></span>

- <span data-ttu-id="098e8-124">Autorisations de site, qui autorisent uniquement les autorisations complètes pour les membres du groupe Project 2X Microsoft 365 et les autorisations de lecture pour le groupe Senior Leadership.</span><span class="sxs-lookup"><span data-stu-id="098e8-124">The site permissions, which only allow full permissions to members of the Project 2X Microsoft 365 group and read permissions to the Senior Leadership group.</span></span>
- <span data-ttu-id="098e8-125">Étiquette de sensibilité Project 2X, avec chiffrement et autorisations qui se déplacent avec le fichier s’il est déplacé ou copié à partir du site.</span><span class="sxs-lookup"><span data-stu-id="098e8-125">The Project 2X sensitivity label, with encryption and permissions that travel with the file if it is moved or copied from the site.</span></span>

<span data-ttu-id="098e8-126">Pour plus d’informations sur la configuration, voir [Créer une étiquette de sensibilité.](secure-teams-security-isolation.md#create-a-sensitivity-label)</span><span class="sxs-lookup"><span data-stu-id="098e8-126">For the configuration details, see [Create a sensitivity label](secure-teams-security-isolation.md#create-a-sensitivity-label).</span></span>

## <a name="step-3-configured-the-underlying-sharepoint-site"></a><span data-ttu-id="098e8-127">Étape 3 : Configuration du site SharePoint sous-jacent</span><span class="sxs-lookup"><span data-stu-id="098e8-127">Step 3: Configured the underlying SharePoint site</span></span>

<span data-ttu-id="098e8-128">Tout d’abord, pour protéger l’accès au site SharePoint sous-jacent pour l’équipe, les administrateurs informatiques de Contoso ont configuré les stratégies d’accès [SharePoint recommandées.](../security/defender-365-security/sharepoint-file-access-policies.md)</span><span class="sxs-lookup"><span data-stu-id="098e8-128">First, to protect access to the underlying SharePoint site for the team, Contoso IT administrators configured the [recommended SharePoint access policies](../security/defender-365-security/sharepoint-file-access-policies.md).</span></span>

<span data-ttu-id="098e8-129">Ensuite, ils ont configuré des paramètres d’autorisation supplémentaires pour le site :</span><span class="sxs-lookup"><span data-stu-id="098e8-129">Next, they configured additional permission settings for the site:</span></span>

- <span data-ttu-id="098e8-130">Pour empêcher les membres du groupe Project 2X de partager l’accès au site.</span><span class="sxs-lookup"><span data-stu-id="098e8-130">To prevent Project 2X group members from sharing access to the site.</span></span> <span data-ttu-id="098e8-131">Pour plus d’informations sur la configuration, voir [paramètres SharePoint](secure-teams-security-isolation.md#sharepoint-settings)pour une équipe avec isolation de sécurité.</span><span class="sxs-lookup"><span data-stu-id="098e8-131">For the configuration details, see [SharePoint settings for a team with security isolation](secure-teams-security-isolation.md#sharepoint-settings).</span></span>
- <span data-ttu-id="098e8-132">Pour les autorisations de lecture pour le groupe Senior Leadership.</span><span class="sxs-lookup"><span data-stu-id="098e8-132">For Read permissions for the Senior Leadership group.</span></span>

<span data-ttu-id="098e8-133">Ensuite, ils ont configuré des paramètres d’autorisation supplémentaires pour le site afin d’empêcher les membres du groupe Project 2X de partager l’accès au site.</span><span class="sxs-lookup"><span data-stu-id="098e8-133">Next, they configured additional permission settings for the site to prevent Project 2X group members from sharing access to the site.</span></span> 

<span data-ttu-id="098e8-134">À mesure que des canaux privés pour Project 2X ont été créés, le propriétaire du groupe a désactivé le partage d’invités et définissez le lien de partage par défaut sur la valeur Personnes **spécifiques.**</span><span class="sxs-lookup"><span data-stu-id="098e8-134">As private channels for the Project 2X were created, the group owner disabled guest sharing and set the default sharing link to the **Specific people** value.</span></span>

<span data-ttu-id="098e8-135">Voici la configuration résultante de l’équipe Project 2X avec isolation de sécurité.</span><span class="sxs-lookup"><span data-stu-id="098e8-135">Here is the resulting configuration of the Project 2X team with security isolation.</span></span>

![Configuration résultante de l’équipe Project 2X](../media/contoso-team-for-top-secret-project.png)

 ## <a name="step-4-trained-project-2x-team-members"></a><span data-ttu-id="098e8-137">Étape 4 : Membres d’équipe Project 2X formés</span><span class="sxs-lookup"><span data-stu-id="098e8-137">Step 4: Trained Project 2X team members</span></span>

<span data-ttu-id="098e8-138">Le personnel de sécurité de Contoso a formé les membres de l’équipe Project 2X dans un cours obligatoire qui les a formés à :</span><span class="sxs-lookup"><span data-stu-id="098e8-138">Contoso security staff trained the Project 2X team members in a mandatory course that stepped them through:</span></span>

- <span data-ttu-id="098e8-139">Comment accéder à la nouvelle équipe Project 2X, utiliser des réunions et des conversations, et comment collaborer sur des fichiers d’équipe.</span><span class="sxs-lookup"><span data-stu-id="098e8-139">How to access the new Project 2X team, use meetings and chats, and how to collaborate on team files.</span></span>
- <span data-ttu-id="098e8-140">Comment créer des fichiers dans l’équipe et télécharger de nouveaux fichiers créés localement.</span><span class="sxs-lookup"><span data-stu-id="098e8-140">How to create new files in the team and upload new files created locally.</span></span>
- <span data-ttu-id="098e8-141">Comment étiqueter des fichiers avec l’étiquette de sensibilité Project 2X.</span><span class="sxs-lookup"><span data-stu-id="098e8-141">How to label files with the Project 2X sensitivity label.</span></span>
- <span data-ttu-id="098e8-142">Démonstration de la façon dont l’étiquette Project 2X protège un fichier même lorsqu’il quitte l’équipe.</span><span class="sxs-lookup"><span data-stu-id="098e8-142">A demonstration of how the Project 2X  label protects a file even when it leaves the team.</span></span>

<span data-ttu-id="098e8-143">Le résultat final est un environnement sécurisé dans lequel les membres de l’équipe Project 2X ont travaillé dans un environnement sécurisé pour les conversations, les réunions et les fichiers.</span><span class="sxs-lookup"><span data-stu-id="098e8-143">The end result was a secure environment in which Project 2X team members collaborated in a secure environment for chats, meetings, and files.</span></span>

<span data-ttu-id="098e8-144">Voici un exemple de fichier stocké dans le site Project 2X sous-jacent avec l’étiquette de sensibilité Project 2X attribuée.</span><span class="sxs-lookup"><span data-stu-id="098e8-144">Here is an example of a file stored in the underlying Project 2X site with the Project 2X sensitivity label assigned.</span></span>

![Exemple de fichier stocké dans le site Project 2X sous-jacent](../media/contoso-team-for-top-secret-project-example.png)

<span data-ttu-id="098e8-146">Dans deux cas, les membres de l’équipe Project 2X ont téléchargé des fichiers protégés par l’étiquette Project 2X sur un lecteur local pour le travail hors connexion.</span><span class="sxs-lookup"><span data-stu-id="098e8-146">In a couple of instances, Project 2X team members downloaded files protected by the Project 2X label to a local drive for offline work.</span></span> 

<span data-ttu-id="098e8-147">Toutefois, après avoir été invité à obtenir des informations d’identification lors de leur ouverture, ils ont réalisé leur erreur et les ont supprimés.</span><span class="sxs-lookup"><span data-stu-id="098e8-147">However, after being prompted for credentials when opening them, they realized their mistake and deleted them.</span></span>

<span data-ttu-id="098e8-148">En raison de l’environnement de collaboration de Teams et des fonctionnalités de sécurité de Microsoft 365, les détails de Project 2X ont été conservés secrètes pendant toute la durée du projet.</span><span class="sxs-lookup"><span data-stu-id="098e8-148">Because of the collaboration environment of Teams and the security features of Microsoft 365, the details of Project 2X were kept secret for the duration of the project.</span></span> <span data-ttu-id="098e8-149">Contoso a annoncé ses plans et est en train de déployer les nouveaux produits et services pour le plus grand plaisir de ses clients, de ses investisseurs et de ses concurrents.</span><span class="sxs-lookup"><span data-stu-id="098e8-149">Contoso announced its plans and is in the process of rolling out the new products and services to the delight of its customers and investors and the chagrin of its competitors.</span></span>

## <a name="next-step"></a><span data-ttu-id="098e8-150">Étape suivante</span><span class="sxs-lookup"><span data-stu-id="098e8-150">Next step</span></span>

<span data-ttu-id="098e8-151">[Déployez une équipe avec isolation de la sécurité](secure-teams-security-isolation.md) dans votre organisation.</span><span class="sxs-lookup"><span data-stu-id="098e8-151">[Deploy a team with security isolation](secure-teams-security-isolation.md) in your organization.</span></span>

