---
title: Teams pour les données hautement réglementées
author: JoeDavies-MSFT
ms.author: josephd
manager: laurawi
ms.date: 10/21/2019
audience: ITPro
ms.topic: article
ms.service: o365-solutions
localization_priority: Priority
ms.collection:
- M365-subscription-management
- Strat_O365_Enterprise
ms.custom: ''
description: Créez une équipe sécurisée pour stocker vos fichiers les plus précieux et les plus sensibles.
ms.openlocfilehash: d917e14719744dad8a681e15a8547655c3a0457f
ms.sourcegitcommit: d95aab99d7827dbb9248280044748ca05ebec786
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/24/2019
ms.locfileid: "37657801"
---
# <a name="teams-for-highly-regulated-data"></a><span data-ttu-id="ade02-103">Teams pour les données hautement réglementées</span><span class="sxs-lookup"><span data-stu-id="ade02-103">Teams for highly regulated data</span></span>

<span data-ttu-id="ade02-104">Cet article décrit les recommandations et les étapes à suivre pour configurer une équipe privée dans Microsoft Teams, qui donne l’accès aux fonctionnalités de Teams, telles que les conversations, réunions et fichiers, uniquement aux membres et aux propriétaires du groupe Office 365 pour l’équipe.</span><span class="sxs-lookup"><span data-stu-id="ade02-104">This article provides you with recommendations and steps to configure a private team in Microsoft Teams that locks down access to Teams features—such as chats, meetings, and files—to only members and owners of the Office 365 group for the team.</span></span> 

<span data-ttu-id="ade02-105">Au-delà de l’accès privé sur la base du groupe Office 365, cet article décrit comment configurer le site d’équipe SharePoint privé sous-jacent, auquel vous pouvez accéder à partir de la section **Fichiers** d’un canal d’équipe, afin de renforcer la sécurité nécessaire pour stocker les données hautement réglementées.</span><span class="sxs-lookup"><span data-stu-id="ade02-105">Beyond the private access based on the Office 365 group, this article describes how to configure the underlying private SharePoint team site, which you can access from the **Files** section of a team channel, for the additional security needed to store highly regulated data.</span></span> <span data-ttu-id="ade02-106">Sur ce site d’équipe SharePoint, vous pouvez stocker et collaborer sur des fichiers, des pages, un calendrier partagé, des tâches, un bloc-notes et des listes.</span><span class="sxs-lookup"><span data-stu-id="ade02-106">On this SharePoint team site, you can store and collaborate on files, pages, a shared calendar, tasks, a notebook, and lists.</span></span>

<span data-ttu-id="ade02-107">Les éléments de configuration d’une équipe pour les données hautement réglementées sont les suivants :</span><span class="sxs-lookup"><span data-stu-id="ade02-107">The elements of configuration for a team for highly regulated data are:</span></span>

- <span data-ttu-id="ade02-108">Une équipe privée avec un groupe Office 365 associé qui dispose de comptes propriétaire et utilisateur.</span><span class="sxs-lookup"><span data-stu-id="ade02-108">A private team with a corresponding Office 365 group that has owner and member user accounts.</span></span>
- <span data-ttu-id="ade02-109">Une sécurité supplémentaire sur le site SharePoint sous-jacent pour l’équipe qui :</span><span class="sxs-lookup"><span data-stu-id="ade02-109">Additional security on the underlying SharePoint site for the team that:</span></span>
  - <span data-ttu-id="ade02-110">Empêche les membres du site d’octroyer l’accès à d’autres personnes.</span><span class="sxs-lookup"><span data-stu-id="ade02-110">Prevents members of the site from granting access to others.</span></span>
  - <span data-ttu-id="ade02-111">Empêche les non-membres du site de demander l’accès au site.</span><span class="sxs-lookup"><span data-stu-id="ade02-111">Prevents non-members of the site from requesting access to the site.</span></span>
- <span data-ttu-id="ade02-112">Une étiquette de rétention Office 365 pour le site SharePoint sous-jacent qui est automatiquement appliquée aux nouveaux fichiers sur le site comme moyen par défaut pour définir les stratégies de rétention.</span><span class="sxs-lookup"><span data-stu-id="ade02-112">An Office 365 retention label for the underlying SharePoint site that is automatically applied to new files on the site as a default way to define retention policies.</span></span>
- <span data-ttu-id="ade02-113">Une stratégie de prévention contre la perte de données (DLP) qui utilise l’étiquette de rétention et empêche les utilisateurs de partager ou d’envoyer des fichiers en dehors de l’organisation.</span><span class="sxs-lookup"><span data-stu-id="ade02-113">A Data Loss Prevention (DLP) policy that uses the retention label and blocks users from sharing or sending files outside the organization.</span></span>
- <span data-ttu-id="ade02-114">Une étiquette de confidentialité Office 365 ou sous-étiquette d’une étiquette hautement réglementée avec le chiffrement activé et les autorisations de co-édition pour le groupe Office 365 de l’équipe.</span><span class="sxs-lookup"><span data-stu-id="ade02-114">An Office 365 sensitivity label or a sublabel of a highly regulated label that has encryption enabled and Co-Author permissions for the Office 365 group of the team.</span></span> <span data-ttu-id="ade02-115">Les utilisateurs appliquent les étiquettes ou sous-étiquettes aux fichiers stockés dans la section **Fichiers** de l’équipe à partir de l’option de la barre de menus Confidentialité dans Word, Excel et PowerPoint.</span><span class="sxs-lookup"><span data-stu-id="ade02-115">Users apply the label or sublabel to files stored in **Files** section of the team from the Sensitivity menu bar option in Word, Excel, and PowerPoint.</span></span>

<span data-ttu-id="ade02-116">Voici la configuration obtenue avec une étiquette de confidentialité.</span><span class="sxs-lookup"><span data-stu-id="ade02-116">Here is the resulting configuration with a sensitivity label.</span></span>

![Configuration du scénario d’équipe sécurisée](./media/secure-teams-highly-regulated-data-scenario/secure-team-final.png)
 
## <a name="phase-1-configure-a-team-for-highly-regulated-data"></a><span data-ttu-id="ade02-118">Phase 1 : configurer une équipe pour les données hautement réglementées</span><span class="sxs-lookup"><span data-stu-id="ade02-118">Phase 1: Configure a team for highly regulated data</span></span>

<span data-ttu-id="ade02-119">La configuration de bout en bout comprend les étapes suivantes :</span><span class="sxs-lookup"><span data-stu-id="ade02-119">The end-to-end configuration consists of these steps:</span></span>

1. <span data-ttu-id="ade02-120">Configuration des accès aux identités et appareils.</span><span class="sxs-lookup"><span data-stu-id="ade02-120">Configure identity and device access.</span></span>
2. <span data-ttu-id="ade02-121">Création d’une équipe privée.</span><span class="sxs-lookup"><span data-stu-id="ade02-121">Create a private team.</span></span>
3. <span data-ttu-id="ade02-122">Configuration du site SharePoint sous-jacent pour une sécurité supplémentaire.</span><span class="sxs-lookup"><span data-stu-id="ade02-122">Configure the underlying SharePoint site for additional security.</span></span>
4. <span data-ttu-id="ade02-123">Création d’une étiquette de rétention et d’une stratégie DLP.</span><span class="sxs-lookup"><span data-stu-id="ade02-123">Create a retention label and DLP policy.</span></span>
5. <span data-ttu-id="ade02-124">Création de l’étiquette ou de la sous-étiquette de l’étiquette très réglementée.</span><span class="sxs-lookup"><span data-stu-id="ade02-124">Create the label or sublabel of the highly regulated label.</span></span>

### <a name="step-1-configure-identity-and-device-access"></a><span data-ttu-id="ade02-125">Etape 1 : configuration des accès aux identités et appareils</span><span class="sxs-lookup"><span data-stu-id="ade02-125">Step 1: Configure identity and device access</span></span>

<span data-ttu-id="ade02-126">Pour protéger l’accès à l’équipe et au site SharePoint sous-jacent, vérifiez que vous avez configuré les [stratégies pour les identités et l’accès aux appareils](https://docs.microsoft.com/microsoft-365/enterprise/identity-access-policies) et les [stratégies d’accès à SharePoint Online](https://docs.microsoft.com/microsoft-365/enterprise/sharepoint-file-access-policies) recommandées.</span><span class="sxs-lookup"><span data-stu-id="ade02-126">To protect access to the team and its underlying SharePoint site, ensure that you have configured [identity and device access policies](https://docs.microsoft.com/microsoft-365/enterprise/identity-access-policies) and the recommended [SharePoint Online access policies](https://docs.microsoft.com/microsoft-365/enterprise/sharepoint-file-access-policies).</span></span>

### <a name="step-2-create-a-private-team"></a><span data-ttu-id="ade02-127">Etape 2 : création d’une équipe privée</span><span class="sxs-lookup"><span data-stu-id="ade02-127">Step 2: Create a private team</span></span>

<span data-ttu-id="ade02-128">Suivez [ces instructions](https://support.office.com/article/create-a-team-from-scratch-174adf5f-846b-4780-b765-de1a0a737e2b) pour créer une équipe privée.</span><span class="sxs-lookup"><span data-stu-id="ade02-128">Use [these instructions](https://support.office.com/article/create-a-team-from-scratch-174adf5f-846b-4780-b765-de1a0a737e2b) to create a private team.</span></span>

<span data-ttu-id="ade02-129">Lorsque vous créez une équipe privée, voici les autorisations par défaut :</span><span class="sxs-lookup"><span data-stu-id="ade02-129">When you create a private team, here are the default permissions:</span></span>

- <span data-ttu-id="ade02-130">Le groupe Office 365 pour l’équipe (le groupe d’équipe) est constitué de propriétaires du groupe et de membres du groupe</span><span class="sxs-lookup"><span data-stu-id="ade02-130">The Office 365 group for the team (the Team Group) has group owners and group members</span></span>
- <span data-ttu-id="ade02-131">Pour le site SharePoint sous-jacent pour l’équipe (le site d’équipe) :</span><span class="sxs-lookup"><span data-stu-id="ade02-131">For the underlying SharePoint site for the team (the Team Site):</span></span>
  - <span data-ttu-id="ade02-132">Les administrateurs de collection de sites sont configurés pour les propriétaires du groupe d’équipe</span><span class="sxs-lookup"><span data-stu-id="ade02-132">The Site Collection Administrators is configured for the Team Group owners</span></span>
  - <span data-ttu-id="ade02-133">Pour le site d’équipe :</span><span class="sxs-lookup"><span data-stu-id="ade02-133">For the Team Site:</span></span> 
    - <span data-ttu-id="ade02-134">Le groupe SharePoint des propriétaires du site d’équipe, avec le niveau d’autorisation contrôle total, est relié aux propriétaires du groupe d’équipe</span><span class="sxs-lookup"><span data-stu-id="ade02-134">The Team Site Owners SharePoint group—with the Full Control permission level—is set to the Team Group owners</span></span>
    - <span data-ttu-id="ade02-135">Le groupe SharePoint des membres du site d’équipe, avec le niveau d’autorisation modification, est relié aux membres du groupe d’équipe</span><span class="sxs-lookup"><span data-stu-id="ade02-135">The Team Site Members SharePoint group—with the Edit permission level—is set to the Team Group members</span></span>
    - <span data-ttu-id="ade02-136">Le groupe SharePoint des visiteurs du site d’équipe, avec le niveau d’autorisation lecture, ne possède pas de groupe ou de comptes d’utilisateur</span><span class="sxs-lookup"><span data-stu-id="ade02-136">The Team Site Visitors SharePoint group—with the Read permission level—has no groups or user accounts</span></span>

<span data-ttu-id="ade02-137">Voici les autorisations par défaut pour le site d’équipe.</span><span class="sxs-lookup"><span data-stu-id="ade02-137">Here are the default permissions for the Team Site.</span></span>

![Autorisations par défaut d’un site d’équipe](./media/secure-teams-highly-regulated-data-scenario/secure-team-default-site-permissions.png)
 
>[!Note]
><span data-ttu-id="ade02-139">Si vous consultez le groupe SharePoint des propriétaires de \<nom de l’équipe> pour le niveau d’autorisation modification, celui-ci n’affiche pas les propriétaires de \<nom de l’équipe>.</span><span class="sxs-lookup"><span data-stu-id="ade02-139">If you view the \<team name> Owners SharePoint group for the Edit permission level, it does not display \<team name> Owners.</span></span>
>

<span data-ttu-id="ade02-140">Les autorisations obtenues permettent :</span><span class="sxs-lookup"><span data-stu-id="ade02-140">The resulting permissions allow:</span></span>

- <span data-ttu-id="ade02-141">Aux propriétaires du groupe d’équipe de gérer le site et de disposer d’un contrôle total sur son contenu.</span><span class="sxs-lookup"><span data-stu-id="ade02-141">Team Group owners to administer the site and have full control over the site contents.</span></span>
- <span data-ttu-id="ade02-142">Aux membres d’un groupe d’équipe de créer et modifier des fichiers sur le site.</span><span class="sxs-lookup"><span data-stu-id="ade02-142">Team Group members to create and edit files on the site.</span></span> 

<span data-ttu-id="ade02-143">La maintenance des autorisations est identique à la maintenance des membres d’équipe et des propriétaires.</span><span class="sxs-lookup"><span data-stu-id="ade02-143">Permissions maintenance is the same as team member and owner maintenance.</span></span>

<span data-ttu-id="ade02-144">Voici la configuration obtenue pour l’instant.</span><span class="sxs-lookup"><span data-stu-id="ade02-144">Here’s the resulting configuration so far.</span></span>

![Etape 2 de la configuration du scénario d’équipe sécurisée](./media/secure-teams-highly-regulated-data-scenario/secure-team-step2.png)
 
### <a name="step-3-configure-the-underlying-sharepoint-site-for-additional-security"></a><span data-ttu-id="ade02-146">Etape 3 : configuration du site SharePoint sous-jacent pour une sécurité supplémentaire</span><span class="sxs-lookup"><span data-stu-id="ade02-146">Step 3: Configure the underlying SharePoint site for additional security</span></span>

<span data-ttu-id="ade02-147">À partir du site d’équipe, configurez ces paramètres d’autorisation.</span><span class="sxs-lookup"><span data-stu-id="ade02-147">From the Team Site, configure these permission settings.</span></span>

1. <span data-ttu-id="ade02-148">Dans la barre d’outils, cliquez sur l’icône Paramètres, puis cliquez sur **Autorisations du site**.</span><span class="sxs-lookup"><span data-stu-id="ade02-148">In the tool bar, click the settings icon, and then click **Site permissions**.</span></span>
2. <span data-ttu-id="ade02-149">Dans le volet **Autorisations de site**, sous **Paramètres de partage**, cliquez sur **Modifier les paramètres de partage**.</span><span class="sxs-lookup"><span data-stu-id="ade02-149">In the **Site permissions** pane, under **Sharing Settings**, click **Change sharing settings**.</span></span>
3. <span data-ttu-id="ade02-150">Sous **Autorisations de partage**, sélectionnez **Seuls les propriétaires du site peuvent partager des fichiers, des dossiers et le site**.</span><span class="sxs-lookup"><span data-stu-id="ade02-150">Under **Sharing permissions**, choose **Only site owners can share files, folders, and the site**.</span></span>
4. <span data-ttu-id="ade02-151">Désactivez **Autoriser les demandes d’accès**, puis cliquez sur **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="ade02-151">Turn off **Allow access requests**, and then click **Save**.</span></span>

<span data-ttu-id="ade02-152">Avec ces paramètres, la possibilité pour les membres du groupe d’équipe de partager le site d’équipe avec d’autres membres ou pour les non-membres de demander l’accès au site d’équipe est désactivée.</span><span class="sxs-lookup"><span data-stu-id="ade02-152">With these settings, the ability for Team Group members to share the Team Site with other members or for non-members to request access to the Team Site is disabled.</span></span>

<span data-ttu-id="ade02-153">Voici la configuration obtenue pour l’instant.</span><span class="sxs-lookup"><span data-stu-id="ade02-153">Here’s the resulting configuration so far.</span></span>

![Etape 3 de la configuration du scénario d’équipe sécurisée](./media/secure-teams-highly-regulated-data-scenario/secure-team-step3.png)

 
### <a name="step-4-create-a-retention-label-and-dlp-policy"></a><span data-ttu-id="ade02-155">Etape 4 : création d’une étiquette de rétention et d’une stratégie DLP</span><span class="sxs-lookup"><span data-stu-id="ade02-155">Step 4: Create a retention label and DLP policy</span></span>

<span data-ttu-id="ade02-156">Utilisez [ces instructions](https://docs.microsoft.com/microsoft-365/compliance/protect-sharepoint-online-files-with-office-365-labels-and-dlp) pour :</span><span class="sxs-lookup"><span data-stu-id="ade02-156">Use [these instructions](https://docs.microsoft.com/microsoft-365/compliance/protect-sharepoint-online-files-with-office-365-labels-and-dlp) to:</span></span>

1. <span data-ttu-id="ade02-157">Créer et publier une étiquette de rétention pour les données hautement réglementées (le cas échéant).</span><span class="sxs-lookup"><span data-stu-id="ade02-157">Create and publish a retention label for highly regulated data (if needed).</span></span>
2. <span data-ttu-id="ade02-158">Configurer le site d’équipe pour l’étiquette de rétention créée à l’étape 1.</span><span class="sxs-lookup"><span data-stu-id="ade02-158">Configure the Team Site for the retention label created in step 1.</span></span>
3. <span data-ttu-id="ade02-159">Créer une stratégie DLP pour les données hautement réglementées qui utilise l’étiquette de rétention créée à l’étape 2 et qui empêche les utilisateurs d’envoyer des fichiers à l’extérieur de l’organisation.</span><span class="sxs-lookup"><span data-stu-id="ade02-159">Create a DLP policy for highly regulated data that uses the retention label created in step 2 and blocks users from sending files outside the organization.</span></span> <span data-ttu-id="ade02-160">Vous pouvez également configurer la stratégie pour définir des exigences supplémentaires, telles que celles correspondant aux réglementations sectorielles sur la santé et la finance, sur la base des [modèles de stratégie de DLP](https://docs.microsoft.com/microsoft-365/compliance/data-loss-prevention-policies#dlp-policy-templates).</span><span class="sxs-lookup"><span data-stu-id="ade02-160">You can also configure the policy for additional requirements, such as those for health and financial industry regulations, based on [DLP policy templates](https://docs.microsoft.com/microsoft-365/compliance/data-loss-prevention-policies#dlp-policy-templates).</span></span>

<span data-ttu-id="ade02-161">Voici la configuration obtenue pour l’instant.</span><span class="sxs-lookup"><span data-stu-id="ade02-161">Here’s the resulting configuration so far.</span></span>

![Etape 4 de la configuration du scénario d’équipe sécurisée](./media/secure-teams-highly-regulated-data-scenario/secure-team-step4.png)
 
### <a name="step-5-create-the-label-or-a-sublabel-of-the-highly-regulated-label"></a><span data-ttu-id="ade02-163">Etape 5 : création de l’étiquette ou d’une sous-étiquette de l’étiquette très réglementée</span><span class="sxs-lookup"><span data-stu-id="ade02-163">Step 5: Create the label or a sublabel of the highly regulated label</span></span>

<span data-ttu-id="ade02-164">Contrairement à une étiquette de sensibilité pour les données hautement réglementées qu’une personne peut appliquer à n’importe quel fichier, une équipe sécurisée doit avoir sa propre étiquette ou sous-étiquette de sorte que les fichiers auxquels elle est attribuée :</span><span class="sxs-lookup"><span data-stu-id="ade02-164">Unlike a sensitivity label for highly regulated data that anyone can apply to any file, a secure team needs its own label or sublabel so that assigned files:</span></span>

- <span data-ttu-id="ade02-165">Soient chiffrés et que le chiffrement soit acheminé avec le fichier.</span><span class="sxs-lookup"><span data-stu-id="ade02-165">Are encrypted and the encryption travels with the file.</span></span>
- <span data-ttu-id="ade02-166">Contiennent des autorisations personnalisées de sorte que seuls les membres du groupe d’équipe puissent l’ouvrir.</span><span class="sxs-lookup"><span data-stu-id="ade02-166">Contain custom permissions so that only members of the Team Group can open it.</span></span>

<span data-ttu-id="ade02-167">Pour atteindre ce niveau de sécurité supplémentaire pour les fichiers stockés sur le site d’équipe, vous devez configurer une nouvelle étiquette de sensibilité qui est soit sa propre étiquette, soit une sous-étiquette de l’étiquette générale pour les fichiers hautement réglementés.</span><span class="sxs-lookup"><span data-stu-id="ade02-167">To accomplish this additional level of security for files stored in the Team Site, you must configure a new sensitivity label that is either its own label a sublabel of the general label for highly regulated files.</span></span> <span data-ttu-id="ade02-168">Seuls les membres du groupe d’équipe la verront dans leur liste d’étiquettes.</span><span class="sxs-lookup"><span data-stu-id="ade02-168">Only Team Group members will see it in their list of labels.</span></span>

<span data-ttu-id="ade02-169">Utilisez une étiquette de confidentialité lorsque vous avez besoin d’un petit nombre d’étiquettes à la fois pour un usage global et pour des équipes privées individuelles.</span><span class="sxs-lookup"><span data-stu-id="ade02-169">Use a sensitivity label when you need a small number of labels for both global use and individual private teams.</span></span> <span data-ttu-id="ade02-170">Utilisez une sous-étiquette de confidentialité lorsque vous avez un grand nombre d’étiquettes ou si vous souhaitez organiser les étiquettes pour les équipes privées sous l’étiquette hautement réglementée.</span><span class="sxs-lookup"><span data-stu-id="ade02-170">Use a sensitivity sublabel when you have a large number of labels or want to organize labels for private teams the under the highly regulated label.</span></span>

<span data-ttu-id="ade02-171">[Suivez ces instructions](https://docs.microsoft.com/microsoft-365/compliance/encryption-sensitivity-labels) pour configurer une étiquette distincte ou une sous-étiquette avec les paramètres suivants :</span><span class="sxs-lookup"><span data-stu-id="ade02-171">[Use these instructions](https://docs.microsoft.com/microsoft-365/compliance/encryption-sensitivity-labels) to configure a separate label or a sublabel with the following settings:</span></span>

- <span data-ttu-id="ade02-172">Le nom de l’étiquette contient le nom de l’équipe</span><span class="sxs-lookup"><span data-stu-id="ade02-172">The name of the label contains the name of the team</span></span>
- <span data-ttu-id="ade02-173">Le chiffrement est activé</span><span class="sxs-lookup"><span data-stu-id="ade02-173">Encryption is enabled</span></span>
- <span data-ttu-id="ade02-174">Le groupe d’équipe possède des autorisations de co-création</span><span class="sxs-lookup"><span data-stu-id="ade02-174">The Team Group has Co-Author permissions</span></span>

<span data-ttu-id="ade02-175">Voici la configuration obtenue avec la nouvelle étiquette.</span><span class="sxs-lookup"><span data-stu-id="ade02-175">Here’s the resulting configuration with the new label.</span></span>

![Etape 5 de la configuration du scénario d’équipe sécurisée](./media/secure-teams-highly-regulated-data-scenario/secure-team-final.png)

<span data-ttu-id="ade02-177">Voici la relation entre l’étiquette de confidentialité et le groupe d’équipe.</span><span class="sxs-lookup"><span data-stu-id="ade02-177">Here’s the relationship between the sensitivity label and the Team Group.</span></span>

![Relation entre le groupe d’équipe et les autorisations d’étiquette](./media/secure-teams-highly-regulated-data-scenario/secure-team-label-permissions.png)


>[!Note]
><span data-ttu-id="ade02-179">Si vous configurez l’étiquette de confidentialité ou la sous-étiquette pour les autorisations définies par l’utilisateur ou avec une date d’expiration, vous ne pouvez pas ouvrir le fichier à partir de Teams ou de SharePoint.</span><span class="sxs-lookup"><span data-stu-id="ade02-179">If you configure the sensitivity label or sublabel for user-defined permissions or with an expiration date, you cannot open the file from Teams or SharePoint.</span></span> <span data-ttu-id="ade02-180">Vous devez utiliser une application Office.</span><span class="sxs-lookup"><span data-stu-id="ade02-180">You must use an Office app.</span></span>
>

### <a name="custom-permissions"></a><span data-ttu-id="ade02-181">Autorisations personnalisées</span><span class="sxs-lookup"><span data-stu-id="ade02-181">Custom permissions</span></span>

<span data-ttu-id="ade02-182">Vous pouvez également configurer les autorisations des sites SharePoint personnalisés pour le site d’équipe et, si nécessaire, l’étiquette de confidentialité correspondante.</span><span class="sxs-lookup"><span data-stu-id="ade02-182">You can also configure custom SharePoint site permissions for the Team Site and, if needed, its corresponding sensitivity label.</span></span> <span data-ttu-id="ade02-183">Voici deux exemples.</span><span class="sxs-lookup"><span data-stu-id="ade02-183">Here are two examples.</span></span>

#### <a name="example-1-delegating-sharepoint-site-administration"></a><span data-ttu-id="ade02-184">Exemple 1 : délégation de l’administration d’un site SharePoint</span><span class="sxs-lookup"><span data-stu-id="ade02-184">Example 1: Delegating SharePoint site administration</span></span>

<span data-ttu-id="ade02-185">Si le propriétaire de l’équipe ne dispose pas d’une expérience d’administration de SharePoint ou souhaite déléguer l’administration du site d’équipe, il peut ajouter le compte d’utilisateur d’un administrateur de services SharePoint à la liste des propriétaires d’équipe.</span><span class="sxs-lookup"><span data-stu-id="ade02-185">If the team owner does not have SharePoint administration experience or wants to delegate administration of the Team Site, they could add the user account of a SharePoint administrator to the list of team owners.</span></span> <span data-ttu-id="ade02-186">L’administrateur de services SharePoint dispose alors d’un accès total à l’équipe et à toutes ses ressources et peut ouvrir un fichier avec l’étiquette de confidentialité appliquée.</span><span class="sxs-lookup"><span data-stu-id="ade02-186">But then the SharePoint administrator would have full access to the team and all its resources and would be able to open a file with the sensitivity label applied.</span></span> 

<span data-ttu-id="ade02-187">Pour empêcher l’octroi de trop grands privilèges, ajoutez le compte d’utilisateur de l’administrateur de services SharePoint au groupe SharePoint propriétaires du site d’équipe dans les paramètres d’autorisations avancés du site.</span><span class="sxs-lookup"><span data-stu-id="ade02-187">To prevent this over-granting of privileges, add the user account of the SharePoint administrator to the Team Site Owners SharePoint group in the advanced permissions settings of the site.</span></span> <span data-ttu-id="ade02-188">L’administrateur de services SharePoint peut gérer le site, mais ne peut pas accéder à l’équipe et à ses ressources, ni ouvrir les fichiers avec l’étiquette de confidentialité attribuée.</span><span class="sxs-lookup"><span data-stu-id="ade02-188">The SharePoint administrator can administer the site but will not be able to access the team and any of its resources or open the files with the sensitivity label assigned.</span></span>

#### <a name="example-2-allowing-view-only-access-to-labeled-files"></a><span data-ttu-id="ade02-189">Exemple 2 : autoriser l’accès en affichage seul aux fichiers étiquetés</span><span class="sxs-lookup"><span data-stu-id="ade02-189">Example 2: Allowing view-only access to labeled files</span></span>

<span data-ttu-id="ade02-190">Si certains membres du personnel doivent seulement consulter le contenu des fichiers étiquetés du site d’équipe, ajoutez leurs comptes d’utilisateur individuels au :</span><span class="sxs-lookup"><span data-stu-id="ade02-190">If some staff only need to view the contents of labeled files in the Team Site, add their individual user accounts to the:</span></span>

- <span data-ttu-id="ade02-191">groupe SharePoint visiteurs \<nom de l’équipe >, qui par défaut dispose du niveau d’autorisation lecture.</span><span class="sxs-lookup"><span data-stu-id="ade02-191">\<team name> Visitors SharePoint group, which by default has the Read permission level.</span></span> 
- <span data-ttu-id="ade02-192">Étiquette de confidentialité avec autorisations d’affichage.</span><span class="sxs-lookup"><span data-stu-id="ade02-192">The sensitivity label with the Viewer permissions.</span></span>

<span data-ttu-id="ade02-193">Voici les autorisations obtenues sur l’étiquette.</span><span class="sxs-lookup"><span data-stu-id="ade02-193">Here are the resulting permissions on the label.</span></span>

![Exemple d’autorisations personnalisées pour l’affichage des fichiers étiquetés](./media/secure-teams-highly-regulated-data-scenario/secure-team-custom-view-permissions.png)
 
<span data-ttu-id="ade02-195">Les visiteurs du site pourront accéder directement au site d’équipe et afficher le contenu des fichiers sur lesquels la sous-étiquette est appliquée.</span><span class="sxs-lookup"><span data-stu-id="ade02-195">The site visitors will be able to access the Team Site directly and view the contents of files that have the sublabel applied.</span></span> <span data-ttu-id="ade02-196">Mais, étant donné qu’ils ne sont pas membres du groupe d’équipe, ils ne pourront accéder ni à l’équipe, ni à aucune de ses ressources.</span><span class="sxs-lookup"><span data-stu-id="ade02-196">But because they are not members of the Team Group, they will not be able to access the team or any of its resources.</span></span>


## <a name="phase-2-drive-user-adoption-for-team-members"></a><span data-ttu-id="ade02-197">Phase 2 : favoriser l’adoption par les utilisateurs pour les membres de l’équipe</span><span class="sxs-lookup"><span data-stu-id="ade02-197">Phase 2: Drive user adoption for team members</span></span>

<span data-ttu-id="ade02-198">Une fois l’équipe en place, il est temps de stimuler l’adoption de cette équipe et de sa sécurité supplémentaire pour les membres de l’équipe.</span><span class="sxs-lookup"><span data-stu-id="ade02-198">With the team in place, it’s time to drive the adoption of this team and its additional security to team members.</span></span>

### <a name="step-1-train-your-users"></a><span data-ttu-id="ade02-199">Étape 1 : former vos utilisateurs</span><span class="sxs-lookup"><span data-stu-id="ade02-199">Step 1: Train your users</span></span>

<span data-ttu-id="ade02-200">Les membres du groupe d’équipe peuvent accéder à l’équipe et à toutes ses ressources, y compris aux conversations, réunions et autres applications.</span><span class="sxs-lookup"><span data-stu-id="ade02-200">Members of the Team Group can access the team and all of its resources, including chats, meetings, and other apps.</span></span> <span data-ttu-id="ade02-201">Lorsque vous travaillez avec des fichiers de la section **Fichiers** d’un canal, les membres du groupe d’équipe doivent affecter l’étiquette ou la sous-étiquette de confidentialité aux fichiers créés pour l’équipe sécurisée.</span><span class="sxs-lookup"><span data-stu-id="ade02-201">When working with files from the **Files** section of a channel, members of the Team Group must assign the sensitivity label or sublabel to files created for the secure team.</span></span> <span data-ttu-id="ade02-202">Voici un exemple.</span><span class="sxs-lookup"><span data-stu-id="ade02-202">Here’s an example.</span></span>

![Exemple d’étiquette appliquée à un fichier dans une équipe sécurisée](./media/secure-teams-highly-regulated-data-scenario/secure-team-label-applied.png)
 
<span data-ttu-id="ade02-204">Lorsque l’étiquette est appliquée au fichier, celui-ci devient sécurisé.</span><span class="sxs-lookup"><span data-stu-id="ade02-204">When the label gets applied to the file it is secured.</span></span> <span data-ttu-id="ade02-205">Les membres du groupe d’équipe peuvent l’ouvrir dans Teams et collaborer en temps réel.</span><span class="sxs-lookup"><span data-stu-id="ade02-205">Members of the Team Group can open it in Teams and collaborate in real time.</span></span> <span data-ttu-id="ade02-206">Il est chiffré et inclut les autorisations de co-édition définies pour les membres du groupe d’équipe.</span><span class="sxs-lookup"><span data-stu-id="ade02-206">It is encrypted and includes the Co-Author permissions set to the Team Group members.</span></span> <span data-ttu-id="ade02-207">Si le fichier quitte le site et est transmis à un utilisateur malveillant, celui-ci devra fournir les informations d’identification d’un compte d’utilisateur membre du groupe d’équipe pour ouvrir le fichier et afficher son contenu.</span><span class="sxs-lookup"><span data-stu-id="ade02-207">If the file leaves the site and gets forwarded to a malicious user, they will have to supply credentials of a user account that is member of the Team Group to open the file and view its contents.</span></span> 

<span data-ttu-id="ade02-208">Formez les membres de votre équipe :</span><span class="sxs-lookup"><span data-stu-id="ade02-208">Train your team members:</span></span>

- <span data-ttu-id="ade02-209">Sur l’importance de l’utilisation de la nouvelle équipe pour les conversations, les réunions, les fichiers et les autres ressources du site de l’équipe, et les conséquences d’une fuite de données hautement réglementées, telles que des conséquences juridiques, des amendes réglementaires, des rançongiciels ou la perte de l’avantage concurrentiel.</span><span class="sxs-lookup"><span data-stu-id="ade02-209">On the importance of using the new team for chats, meetings, files, and the other resources of the Team Site and the consequences of a highly regulated data leak, such as legal ramifications, regulatory fines, ransomware, or loss of competitive advantage.</span></span>
- <span data-ttu-id="ade02-210">Accès à l’équipe.</span><span class="sxs-lookup"><span data-stu-id="ade02-210">How to access the team.</span></span>
- <span data-ttu-id="ade02-211">Création de nouveaux fichiers sur le site et chargement de nouveaux fichiers stockés localement.</span><span class="sxs-lookup"><span data-stu-id="ade02-211">How to create new files on the site and upload new files stored locally.</span></span>
- <span data-ttu-id="ade02-212">Blocage du partage des fichiers en externe par la stratégie DLP.</span><span class="sxs-lookup"><span data-stu-id="ade02-212">How the DLP policy blocks them from sharing files externally.</span></span>
- <span data-ttu-id="ade02-213">Mode d’étiquetage de fichiers à l’aide de l’étiquette ou de la sous-étiquette personnalisée pour l’équipe.</span><span class="sxs-lookup"><span data-stu-id="ade02-213">How to label files with the custom label or sublabel for the team.</span></span>
- <span data-ttu-id="ade02-214">Comment l’étiquette ou la sous-étiquette protège des fichiers même lorsque ceux-ci ont été divulgués hors du site.</span><span class="sxs-lookup"><span data-stu-id="ade02-214">How the label or sublabel protects files even when they are leaked off the site.</span></span>

<span data-ttu-id="ade02-215">Cette formation doit inclure des exercices pratiques pour que les membres de votre équipe puissent se familiariser avec ces fonctionnalités et leurs résultats.</span><span class="sxs-lookup"><span data-stu-id="ade02-215">This training should include hands-on exercises so that your team members can experience these capabilities and their results.</span></span>

### <a name="step-2-conduct-periodic-reviews-of-usage-and-address-team-member-feedback"></a><span data-ttu-id="ade02-216">Étape 2 : conduire des vérifications périodiques de l’utilisation et donner suite aux commentaires des membres de l’équipe</span><span class="sxs-lookup"><span data-stu-id="ade02-216">Step 2: Conduct periodic reviews of usage and address team member feedback</span></span>

<span data-ttu-id="ade02-217">Dans les semaines suivant la formation :</span><span class="sxs-lookup"><span data-stu-id="ade02-217">In the weeks after training:</span></span>

- <span data-ttu-id="ade02-218">Traitez rapidement les commentaires des membres de l’équipe et affinez les stratégies et les configurations.</span><span class="sxs-lookup"><span data-stu-id="ade02-218">Quickly address team member feedback and fine tune polices and configurations.</span></span>
- <span data-ttu-id="ade02-219">Analysez l’utilisation pour l’équipe et comparez-la avec les attentes en matière d’utilisation.</span><span class="sxs-lookup"><span data-stu-id="ade02-219">Analyze usage for the team and compare it with usage expectations.</span></span>
- <span data-ttu-id="ade02-220">Vérifiez que les fichiers hautement réglementés ont été correctement étiquetés avec l’étiquette ou la sous-étiquette de sensibilité personnalisée.</span><span class="sxs-lookup"><span data-stu-id="ade02-220">Verify that highly regulated files have been properly labeled with the custom sensitivity label or sublabel.</span></span>

  <span data-ttu-id="ade02-221">Vous pouvez voir quels fichiers disposent d'une étiquette attribuée en affichant un dossier dans SharePoint Online et en ajoutant la colonne **Confidentialité** via l'option **Afficher/masquer les colonnes** de la fonction **Ajouter une colonne**.</span><span class="sxs-lookup"><span data-stu-id="ade02-221">You can see which files have a label assigned by viewing a folder in SharePoint and adding the **Sensitivity** column through the **Show/hide columns** option of **Add column**.</span></span>

<span data-ttu-id="ade02-222">Formez à nouveau vos utilisateurs, le cas échéant.</span><span class="sxs-lookup"><span data-stu-id="ade02-222">Retrain your users as needed.</span></span>

## <a name="see-also"></a><span data-ttu-id="ade02-223">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ade02-223">See also</span></span>

[<span data-ttu-id="ade02-224">Sites SharePoint pour les données hautement réglementées</span><span class="sxs-lookup"><span data-stu-id="ade02-224">SharePoint sites for highly regulated data</span></span>](teams-sharepoint-online-sites-highly-regulated-data.md)

[<span data-ttu-id="ade02-225">Scénarios et charges de travail Microsoft 365 Entreprise</span><span class="sxs-lookup"><span data-stu-id="ade02-225">Microsoft 365 Enterprise workloads and scenarios</span></span>](deploy-workloads.md)

<span data-ttu-id="ade02-226">[Bibliothèque de productivité Microsoft 365](https://aka.ms/productivitylibrary)https://aka.ms/productivitylibrary)</span><span class="sxs-lookup"><span data-stu-id="ade02-226">[Microsoft 365 Productivity Library](https://aka.ms/productivitylibrary) (https://aka.ms/productivitylibrary)</span></span>

[<span data-ttu-id="ade02-227">Guide de déploiement</span><span class="sxs-lookup"><span data-stu-id="ade02-227">Deployment guide</span></span>](deploy-microsoft-365-enterprise.md)
