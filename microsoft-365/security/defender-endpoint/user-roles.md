---
title: Créer et gérer des rôles pour le contrôle d’accès basé sur un rôle
description: Créer des rôles et définir les autorisations attribuées au rôle dans le cadre de l’implémentation du contrôle d’accès basé sur un rôle dans le Centre de sécurité Microsoft Defender
keywords: rôles utilisateur, rôles, accès rbac
search.product: eADQiWindows 10XVcnh
search.appverid: met150
ms.prod: m365-security
ms.mktglfcycl: deploy
ms.sitesec: library
ms.pagetype: security
ms.author: macapara
author: mjcaparas
localization_priority: Normal
manager: dansimp
audience: ITPro
ms.collection: M365-security-compliance
ms.topic: article
ms.technology: mde
ms.openlocfilehash: 932fd6ecd7dca66f4cb587b226474109c788c341
ms.sourcegitcommit: 956176ed7c8b8427fdc655abcd1709d86da9447e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/23/2021
ms.locfileid: "51065950"
---
# <a name="create-and-manage-roles-for-role-based-access-control"></a><span data-ttu-id="4fe80-104">Créer et gérer des rôles pour le contrôle d’accès basé sur un rôle</span><span class="sxs-lookup"><span data-stu-id="4fe80-104">Create and manage roles for role-based access control</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../../includes/microsoft-defender.md)]

<span data-ttu-id="4fe80-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="4fe80-105">**Applies to:**</span></span>
- [<span data-ttu-id="4fe80-106">Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="4fe80-106">Microsoft Defender for Endpoint</span></span>](https://go.microsoft.com/fwlink/?linkid=2154037)
- [<span data-ttu-id="4fe80-107">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="4fe80-107">Microsoft 365 Defender</span></span>](https://go.microsoft.com/fwlink/?linkid=2118804)

><span data-ttu-id="4fe80-108">Vous souhaitez découvrir Microsoft Defender pour le point de terminaison ?</span><span class="sxs-lookup"><span data-stu-id="4fe80-108">Want to experience Microsoft Defender for Endpoint?</span></span> [<span data-ttu-id="4fe80-109">Inscrivez-vous à un essai gratuit.</span><span class="sxs-lookup"><span data-stu-id="4fe80-109">Sign up for a free trial.</span></span>](https://www.microsoft.com/microsoft-365/windows/microsoft-defender-atp?ocid=docs-wdatp-roles-abovefoldlink)

[!include[Prerelease information](../../includes/prerelease.md)]

## <a name="create-roles-and-assign-the-role-to-an-azure-active-directory-group"></a><span data-ttu-id="4fe80-110">Créer des rôles et attribuer le rôle à un groupe Azure Active Directory de gestion</span><span class="sxs-lookup"><span data-stu-id="4fe80-110">Create roles and assign the role to an Azure Active Directory group</span></span>

<span data-ttu-id="4fe80-111">Les étapes suivantes vous guident sur la création de rôles dans Centre de sécurité Microsoft Defender.</span><span class="sxs-lookup"><span data-stu-id="4fe80-111">The following steps guide you on how to create roles in Microsoft Defender Security Center.</span></span> <span data-ttu-id="4fe80-112">Il part du principe que vous avez déjà créé Azure Active Directory groupes d’utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="4fe80-112">It assumes that you have already created Azure Active Directory user groups.</span></span>

1. <span data-ttu-id="4fe80-113">Connectez-vous [Centre de sécurité Microsoft Defender](https://securitycenter.windows.com/) compte avec un rôle d’administrateur de sécurité ou d’administrateur général attribué.</span><span class="sxs-lookup"><span data-stu-id="4fe80-113">Log in to [Microsoft Defender Security Center](https://securitycenter.windows.com/) using account with a Security administrator or Global administrator role assigned.</span></span>

2. <span data-ttu-id="4fe80-114">Dans le volet de navigation, sélectionnez **Paramètres > rôles.**</span><span class="sxs-lookup"><span data-stu-id="4fe80-114">In the navigation pane, select **Settings > Roles**.</span></span>

3. <span data-ttu-id="4fe80-115">Sélectionnez **Ajouter un élément.**</span><span class="sxs-lookup"><span data-stu-id="4fe80-115">Select **Add item**.</span></span>

4. <span data-ttu-id="4fe80-116">Entrez le nom de rôle, la description et les autorisations que vous souhaitez attribuer au rôle.</span><span class="sxs-lookup"><span data-stu-id="4fe80-116">Enter the role name, description, and permissions you'd like to assign to the role.</span></span>

5. <span data-ttu-id="4fe80-117">Sélectionnez **Suivant** pour attribuer le rôle à un groupe de sécurité Azure AD.</span><span class="sxs-lookup"><span data-stu-id="4fe80-117">Select **Next** to assign the role to an Azure AD Security group.</span></span>

6. <span data-ttu-id="4fe80-118">Utilisez le filtre pour sélectionner le groupe Azure AD à ajouter à ce rôle.</span><span class="sxs-lookup"><span data-stu-id="4fe80-118">Use the filter to select the Azure AD group that you'd like to add to this role to.</span></span>

7. <span data-ttu-id="4fe80-119">**Enregistrez et fermez.**</span><span class="sxs-lookup"><span data-stu-id="4fe80-119">**Save and close**.</span></span>

8. <span data-ttu-id="4fe80-120">Appliquez les paramètres de configuration.</span><span class="sxs-lookup"><span data-stu-id="4fe80-120">Apply the configuration settings.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="4fe80-121">Après avoir créé des rôles, vous devez créer un groupe d’appareils et fournir l’accès au groupe d’appareils en l’attribuant à un rôle que vous venons de créer.</span><span class="sxs-lookup"><span data-stu-id="4fe80-121">After creating roles, you'll need to create a device group and provide access to the device group by assigning it to a role that you just created.</span></span>

### <a name="permission-options"></a><span data-ttu-id="4fe80-122">Options d’autorisation</span><span class="sxs-lookup"><span data-stu-id="4fe80-122">Permission options</span></span>

- <span data-ttu-id="4fe80-123">**Afficher les données**</span><span class="sxs-lookup"><span data-stu-id="4fe80-123">**View data**</span></span>
    - <span data-ttu-id="4fe80-124">**Opérations de sécurité** : afficher toutes les données des opérations de sécurité dans le portail</span><span class="sxs-lookup"><span data-stu-id="4fe80-124">**Security operations** - View all security operations data in the portal</span></span>
    - <span data-ttu-id="4fe80-125">**Menaces et gestion des vulnérabilités** : afficher Gestion des menaces et des vulnérabilités données de sécurité dans le portail</span><span class="sxs-lookup"><span data-stu-id="4fe80-125">**Threat and vulnerability management** - View threat and vulnerability management data in the portal</span></span>

- <span data-ttu-id="4fe80-126">**Actions de correction actives**</span><span class="sxs-lookup"><span data-stu-id="4fe80-126">**Active remediation actions**</span></span>
    - <span data-ttu-id="4fe80-127">**Opérations de sécurité** : prendre des mesures de réponse, approuver ou ignorer les actions de correction en attente, gérer les listes autorisées/bloquées pour l’automatisation et les indicateurs</span><span class="sxs-lookup"><span data-stu-id="4fe80-127">**Security operations** - Take response actions, approve or dismiss pending remediation actions, manage allowed/blocked lists for automation and indicators</span></span>
    - <span data-ttu-id="4fe80-128">**Menaces et gestion des vulnérabilités - Gestion des exceptions** : créer des exceptions et gérer les exceptions actives</span><span class="sxs-lookup"><span data-stu-id="4fe80-128">**Threat and vulnerability management - Exception handling** - Create new exceptions and manage active exceptions</span></span>
    - <span data-ttu-id="4fe80-129">**Threat and gestion des vulnérabilités - Remediation handling** - Submit new remediation requests, create tickets, and manage existing remediation activities</span><span class="sxs-lookup"><span data-stu-id="4fe80-129">**Threat and vulnerability management - Remediation handling** - Submit new remediation requests, create tickets, and manage existing remediation activities</span></span>

- <span data-ttu-id="4fe80-130">**Examen des alertes** : gérer les alertes, lancer des enquêtes automatisées, exécuter des analyses, collecter des packages d’enquête, gérer les balises d’appareil et télécharger uniquement les fichiers exécutables portables (PE)</span><span class="sxs-lookup"><span data-stu-id="4fe80-130">**Alerts investigation** - Manage alerts, initiate automated investigations, run scans, collect investigation packages, manage device tags, and download only portable executable (PE) files</span></span> 

- <span data-ttu-id="4fe80-131">**Gérer les paramètres** système du portail : configurer les paramètres de stockage, les paramètres SIEM et les paramètres de l’API Intel contre les menaces (s’applique globalement), les paramètres avancés, les téléchargements de fichiers automatisés, les rôles et les groupes d’appareils</span><span class="sxs-lookup"><span data-stu-id="4fe80-131">**Manage portal system settings** - Configure storage settings, SIEM and threat intel API settings (applies globally), advanced settings, automated file uploads, roles and device groups</span></span>

    > [!NOTE]
    > <span data-ttu-id="4fe80-132">Ce paramètre est uniquement disponible dans le rôle d’administrateur Microsoft Defender pour point de terminaison (par défaut).</span><span class="sxs-lookup"><span data-stu-id="4fe80-132">This setting is only available in the Microsoft Defender for Endpoint administrator (default) role.</span></span>

- <span data-ttu-id="4fe80-133">**Gérer les paramètres** de sécurité dans le Centre de sécurité : configurer les paramètres de suppression des alertes, gérer les exclusions de dossiers pour l’automatisation, les appareils intégrés et hors-bord, et gérer les notifications par courrier électronique, gérer le laboratoire d’évaluation</span><span class="sxs-lookup"><span data-stu-id="4fe80-133">**Manage security settings in Security Center** - Configure alert suppression settings, manage folder exclusions for automation, onboard and offboard devices, and manage email notifications, manage evaluation lab</span></span>

- <span data-ttu-id="4fe80-134">**Fonctionnalités de réponse en direct**</span><span class="sxs-lookup"><span data-stu-id="4fe80-134">**Live response capabilities**</span></span>
    - <span data-ttu-id="4fe80-135">**Commandes** de base :</span><span class="sxs-lookup"><span data-stu-id="4fe80-135">**Basic** commands:</span></span>
        - <span data-ttu-id="4fe80-136">Démarrer une session de réponse en direct</span><span class="sxs-lookup"><span data-stu-id="4fe80-136">Start a live response session</span></span>
        - <span data-ttu-id="4fe80-137">Exécuter des commandes de réponse en direct en lecture seule sur un appareil distant (à l’exception de la copie et de l’exécution de fichiers)</span><span class="sxs-lookup"><span data-stu-id="4fe80-137">Perform read only live response commands on remote device (excluding file copy and execution</span></span>
    - <span data-ttu-id="4fe80-138">**Commandes** avancées :</span><span class="sxs-lookup"><span data-stu-id="4fe80-138">**Advanced** commands:</span></span>
        - <span data-ttu-id="4fe80-139">Télécharger un fichier à partir de l’appareil distant via une réponse en direct</span><span class="sxs-lookup"><span data-stu-id="4fe80-139">Download a file from the remote device via live response</span></span>
        - <span data-ttu-id="4fe80-140">Télécharger des fichiers PE et non PE à partir de la page de fichiers</span><span class="sxs-lookup"><span data-stu-id="4fe80-140">Download PE and non-PE files from the file page</span></span>
        - <span data-ttu-id="4fe80-141">Télécharger fichier sur l’appareil distant</span><span class="sxs-lookup"><span data-stu-id="4fe80-141">Upload a file to the remote device</span></span>
        - <span data-ttu-id="4fe80-142">Afficher un script à partir de la bibliothèque de fichiers</span><span class="sxs-lookup"><span data-stu-id="4fe80-142">View a script from the files library</span></span>
        - <span data-ttu-id="4fe80-143">Exécuter un script sur l’appareil distant à partir de la bibliothèque de fichiers</span><span class="sxs-lookup"><span data-stu-id="4fe80-143">Execute a script on the remote device from the files library</span></span>

<span data-ttu-id="4fe80-144">Pour plus d’informations sur les commandes disponibles, voir Examiner les appareils à [l’aide de la réponse Live.](live-response.md)</span><span class="sxs-lookup"><span data-stu-id="4fe80-144">For more information on the available commands, see [Investigate devices using Live response](live-response.md).</span></span>
  
## <a name="edit-roles"></a><span data-ttu-id="4fe80-145">Modifier des rôles</span><span class="sxs-lookup"><span data-stu-id="4fe80-145">Edit roles</span></span>

1. <span data-ttu-id="4fe80-146">Connectez-vous à [Centre de sécurité Microsoft Defender](https://securitycenter.windows.com/) compte avec le rôle Administrateur de sécurité ou Administrateur général attribué.</span><span class="sxs-lookup"><span data-stu-id="4fe80-146">Log in to [Microsoft Defender Security Center](https://securitycenter.windows.com/) using account with Security administrator or Global administrator role assigned.</span></span>

2. <span data-ttu-id="4fe80-147">Dans le volet de navigation, sélectionnez **Paramètres > rôles.**</span><span class="sxs-lookup"><span data-stu-id="4fe80-147">In the navigation pane, select **Settings > Roles**.</span></span>

3. <span data-ttu-id="4fe80-148">Sélectionnez le rôle que vous souhaitez modifier.</span><span class="sxs-lookup"><span data-stu-id="4fe80-148">Select the role you'd like to edit.</span></span>

4. <span data-ttu-id="4fe80-149">Cliquez sur **Modifier**.</span><span class="sxs-lookup"><span data-stu-id="4fe80-149">Click **Edit**.</span></span>

5. <span data-ttu-id="4fe80-150">Modifiez les détails ou les groupes affectés au rôle.</span><span class="sxs-lookup"><span data-stu-id="4fe80-150">Modify the details or the groups that are assigned to the role.</span></span> 

6. <span data-ttu-id="4fe80-151">Cliquez **sur Enregistrer et fermer.**</span><span class="sxs-lookup"><span data-stu-id="4fe80-151">Click **Save and close**.</span></span>

## <a name="delete-roles"></a><span data-ttu-id="4fe80-152">Supprimer des rôles</span><span class="sxs-lookup"><span data-stu-id="4fe80-152">Delete roles</span></span>

1. <span data-ttu-id="4fe80-153">Connectez-vous à [Centre de sécurité Microsoft Defender](https://securitycenter.windows.com/) compte avec le rôle Administrateur de sécurité ou Administrateur général attribué.</span><span class="sxs-lookup"><span data-stu-id="4fe80-153">Log in to [Microsoft Defender Security Center](https://securitycenter.windows.com/) using account with Security administrator or Global administrator role assigned.</span></span>

2. <span data-ttu-id="4fe80-154">Dans le volet de navigation, sélectionnez **Paramètres > rôles.**</span><span class="sxs-lookup"><span data-stu-id="4fe80-154">In the navigation pane, select **Settings > Roles**.</span></span>

3. <span data-ttu-id="4fe80-155">Sélectionnez le rôle que vous souhaitez supprimer.</span><span class="sxs-lookup"><span data-stu-id="4fe80-155">Select the role you'd like to delete.</span></span>

4. <span data-ttu-id="4fe80-156">Cliquez sur le bouton de la déposer et sélectionnez **Supprimer le rôle.**</span><span class="sxs-lookup"><span data-stu-id="4fe80-156">Click the drop-down button and select **Delete role**.</span></span>

## <a name="related-topic"></a><span data-ttu-id="4fe80-157">Rubrique connexe</span><span class="sxs-lookup"><span data-stu-id="4fe80-157">Related topic</span></span>

- [<span data-ttu-id="4fe80-158">Autorisations utilisateur de base pour accéder au portail</span><span class="sxs-lookup"><span data-stu-id="4fe80-158">User basic permissions to access the portal</span></span>](basic-permissions.md)
- [<span data-ttu-id="4fe80-159">Créer et gérer des groupes d’appareils</span><span class="sxs-lookup"><span data-stu-id="4fe80-159">Create and manage device groups</span></span>](machine-groups.md)
