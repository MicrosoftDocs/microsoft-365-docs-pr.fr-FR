---
title: Sites d’équipe SharePoint Online isolés
f1.keywords:
- NOCSH
ms.author: josephd
author: JoeDavies-MSFT
manager: laurawi
ms.date: 12/15/2017
audience: ITPro
ms.topic: overview
localization_priority: Priority
ms.collection:
- Ent_O365
- Strat_O365_Enterprise
ms.custom:
- Ent_Solutions
- seo-marvel-apr2020
ms.assetid: 71250a04-fd2d-4c3c-a32b-b8a838b19a54
description: Découvrez les sites d’équipe SharePoint Online isolés, y compris les utilisations, les exigences et les fonctionnalités compatibles.
ms.technology: mdo
ms.prod: m365-security
ms.openlocfilehash: 056c6f2a463d38dd27b26d484995280dddedf436
ms.sourcegitcommit: 786f90a163d34c02b8451d09aa1efb1e1d5f543c
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/18/2021
ms.locfileid: "50286584"
---
# <a name="isolated-sharepoint-online-team-sites"></a><span data-ttu-id="049ec-103">Sites d’équipe SharePoint Online isolés</span><span class="sxs-lookup"><span data-stu-id="049ec-103">Isolated SharePoint Online team sites</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../includes/microsoft-defender-for-office.md)]

<span data-ttu-id="049ec-104">**S’applique à**</span><span class="sxs-lookup"><span data-stu-id="049ec-104">**Applies to**</span></span>
- [<span data-ttu-id="049ec-105">Exchange Online Protection</span><span class="sxs-lookup"><span data-stu-id="049ec-105">Exchange Online Protection</span></span>](exchange-online-protection-overview.md)
- [<span data-ttu-id="049ec-106">Microsoft Defender pour Office 365 Plan 1</span><span class="sxs-lookup"><span data-stu-id="049ec-106">Microsoft Defender for Office 365 plan 1</span></span>](office-365-atp.md)
- <span data-ttu-id="049ec-107">SharePoint Online</span><span class="sxs-lookup"><span data-stu-id="049ec-107">SharePoint Online</span></span> 

 <span data-ttu-id="049ec-108">**Résumé :** Découvrez les utilisations pour les sites d'équipe SharePoint Online isolés.</span><span class="sxs-lookup"><span data-stu-id="049ec-108">**Summary:** Learn about the uses for isolated SharePoint Online team sites.</span></span>

<span data-ttu-id="049ec-p101">Les sites d'équipe SharePoint Online vous permettent de créer facilement et rapidement un espace dédié à la collaboration. Les utilisateurs peuvent collaborer sur des notes, des documents, des articles, d’un calendrier et d'autres ressources dans Microsoft Office 365. Les sites d'équipe SharePoint Online sont créés à partir d'un groupe Microsoft 365. Ils comportent un modèle d'administration simplifié pour favoriser une collaboration ouverte entre les membres d'un groupe privé ou de l'organisation tout entière. Un site d'équipe SharePoint Online par défaut permet aux membres du groupe Microsoft 365 d'inviter d'autres utilisateurs et de contrôler les paramètres d'autorisations.</span><span class="sxs-lookup"><span data-stu-id="049ec-p101">SharePoint Online team sites are an easy way to quickly create a space for collaboration. Users can work together on notes, documents, articles, a calendar, and other resources in Microsoft Office 365. SharePoint Online team sites are based on a Microsoft 365 group and have a simplified administration model to allow open collaboration with a private set of group members or the entire organization. A default SharePoint Online team site allows members of the Microsoft 365 group to invite other users and control permissions settings.</span></span>

<span data-ttu-id="049ec-113">Toutefois, vous aurez parfois besoin que l’accès au site soit contrôlé par les appartenances aux groupes et les niveaux d’autorisation SharePoint Online gérés par les administrateurs SharePoint.</span><span class="sxs-lookup"><span data-stu-id="049ec-113">However, you'll sometimes need site access to be controlled by group memberships, and SharePoint Online permission levels managed by SharePoint administrators.</span></span> <span data-ttu-id="049ec-114">C'est ce que nous appelons un site isolé, car il est réservé aux utilisateurs qui collaborent sur le site, consultent son contenu ou gèrent le site.</span><span class="sxs-lookup"><span data-stu-id="049ec-114">We call this an isolated site, which is isolated to the set of users that are either collaborating, viewing its contents, or administering the site.</span></span> <span data-ttu-id="049ec-115">Vous aurez besoin d'un site isolé pour :</span><span class="sxs-lookup"><span data-stu-id="049ec-115">You might need an isolated site for the following:</span></span>

- <span data-ttu-id="049ec-116">travailler sur un projet secret au sein de votre organisation ;</span><span class="sxs-lookup"><span data-stu-id="049ec-116">A secret project within your organization.</span></span>

- <span data-ttu-id="049ec-117">stocker des éléments de propriété intellectuelle précieux ou très sensibles pour votre organisation ;</span><span class="sxs-lookup"><span data-stu-id="049ec-117">The location for highly-sensitive or valuable intellectual property for your organization.</span></span>

- <span data-ttu-id="049ec-118">conserver les ressources destinées à une procédure judiciaire engagée par votre organisation ou à laquelle elle est soumise ;</span><span class="sxs-lookup"><span data-stu-id="049ec-118">The resources for a legal action taken by your organization or that to which it is being subjected.</span></span>

- <span data-ttu-id="049ec-119">Pour partager un abonnement Microsoft 365 avec d’autres organisations dont certaines activités se recoupent, mais qui, pour la plupart, existent en tant qu’entités distinctes.</span><span class="sxs-lookup"><span data-stu-id="049ec-119">To share a Microsoft 365 subscription between multiple organizations that have some overlap, but for the most part exist as separate business entities.</span></span>

<span data-ttu-id="049ec-120">Voici les exigences d’un site isolé :</span><span class="sxs-lookup"><span data-stu-id="049ec-120">Here are the requirements of an isolated site:</span></span>

- <span data-ttu-id="049ec-121">Seuls les administrateurs SharePoint Online peuvent gérer le site, en particulier l’accès au site par les membres du groupe et la configuration des autorisations personnalisées.</span><span class="sxs-lookup"><span data-stu-id="049ec-121">Only SharePoint Online administrators can perform site administration, which includes group membership for access to the site and configuring custom permissions.</span></span>

- <span data-ttu-id="049ec-122">Les membres du site ne peuvent pas inviter d’autres membres à accéder au site d’équipe.</span><span class="sxs-lookup"><span data-stu-id="049ec-122">Members of the site cannot invite other members to the team site.</span></span>

- <span data-ttu-id="049ec-p103">Les utilisateurs qui ne sont pas membres du site isolé ne peuvent pas demander l'accès au site. Lorsqu'ils essaieront d'accéder à une URL associée au site, ils seront redirigés vers une page web leur indiquant que l'accès a été refusé.</span><span class="sxs-lookup"><span data-stu-id="049ec-p103">Users who are not members of the isolated site cannot request access to the site. They will receive an access denied web page when they attempt to access any URL associated with the site.</span></span>

<span data-ttu-id="049ec-p104">Grâce à une gestion centralisée des accès et aux autorisations personnalisées, le site reste isolé en tout temps. Par exemple, les membres du groupe ne peuvent pas, volontairement ou accidentellement, configurer des autorisations personnalisées pour d'autres utilisateurs de l'abonnement Microsoft 365 qui ne devraient pas être membres du site ou les inviter.</span><span class="sxs-lookup"><span data-stu-id="049ec-p104">The tradeoff of requiring centralized access control and custom permissions by SharePoint Online administrators is that the site remains isolated over time. For example, current members cannot, either intentionally or accidentally, invite or configure custom permissions for other users within the Microsoft 365 subscription who should not be members of the site.</span></span>

<span data-ttu-id="049ec-127">Un site isolé peut être utilisé avec d’autres fonctionnalités, telles que :</span><span class="sxs-lookup"><span data-stu-id="049ec-127">An isolated site can be used with other features, such as:</span></span>

- <span data-ttu-id="049ec-128">la gestion des droits relatifs à l’information pour garantir que les ressources du site restent chiffrées même si elles sont téléchargées localement et chargées sur un autre site accessible à toute l’entreprise ;</span><span class="sxs-lookup"><span data-stu-id="049ec-128">Information Rights Management to ensure that the resources on the site remain encrypted, even if they are downloaded locally and uploaded to another site that is available to the entire organization.</span></span>

- <span data-ttu-id="049ec-129">la protection contre la perte de données pour empêcher les utilisateurs d’envoyer par e-mail les ressources du site, comme des fichiers.</span><span class="sxs-lookup"><span data-stu-id="049ec-129">Data loss prevention to prevent users from sending the resources of the site, such as files, in email.</span></span>

## <a name="next-steps"></a><span data-ttu-id="049ec-130">Étapes suivantes</span><span class="sxs-lookup"><span data-stu-id="049ec-130">Next steps</span></span>

<span data-ttu-id="049ec-131">Pour tester un site d'équipe SharePoint Online isolé faisant partie d'un abonnement à la version d'évaluation, consultez la rubrique [Site d'équipe SharePoint Online isolé dans votre environnement de développement/test d'Office 365](isolated-sharepoint-online-team-site-dev-test-environment.md).</span><span class="sxs-lookup"><span data-stu-id="049ec-131">To try out an isolated SharePoint Online team site in a trial subscription, see the step-by-step instructions in [Isolated SharePoint Online team site dev/test environment](isolated-sharepoint-online-team-site-dev-test-environment.md).</span></span>

<span data-ttu-id="049ec-132">Lorsque vous souhaitez déployer un site d'équipe SharePoint Online isolé en production, lisez la procédure détaillée dans la rubrique [Conception d'un site d'équipe SharePoint Online isolé](design-an-isolated-sharepoint-online-team-site.md).</span><span class="sxs-lookup"><span data-stu-id="049ec-132">When you are ready to deploy an isolated SharePoint Online team site in production, see the step-by-step design considerations in [Design an isolated SharePoint Online team site](design-an-isolated-sharepoint-online-team-site.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="049ec-133">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="049ec-133">Related topics</span></span>

[<span data-ttu-id="049ec-134">Conception d'un site d'équipe SharePoint Online isolé</span><span class="sxs-lookup"><span data-stu-id="049ec-134">Design an isolated SharePoint Online team site</span></span>](design-an-isolated-sharepoint-online-team-site.md)

[<span data-ttu-id="049ec-135">Gestion d’un site d’équipe SharePoint Online isolé</span><span class="sxs-lookup"><span data-stu-id="049ec-135">Manage an isolated SharePoint Online team site</span></span>](manage-an-isolated-sharepoint-online-team-site.md)

[<span data-ttu-id="049ec-136">Déploiement d’un site d’équipe SharePoint Online isolé</span><span class="sxs-lookup"><span data-stu-id="049ec-136">Deploy an isolated SharePoint Online team site</span></span>](deploy-an-isolated-sharepoint-online-team-site.md)
