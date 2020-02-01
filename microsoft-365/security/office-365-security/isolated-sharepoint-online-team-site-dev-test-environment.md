---
title: Site d’équipe SharePoint Online isolé dans votre environnement de développement/test
f1.keywords:
- NOCSH
ms.author: josephd
author: JoeDavies-MSFT
manager: laurawi
ms.date: 12/15/2017
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.collection: Ent_O365
ms.custom:
- TLG
- Ent_TLGs
ms.assetid: d1795031-beef-49ea-a6fc-5da5450d320d
description: 'Résumé : configurez un site d’équipe SharePoint Online isolé du reste de l’organisation dans votre environnement de développement/test Office 365.'
ms.openlocfilehash: 49443a5dd6b2c93e6bd7817c09747d49b163cabd
ms.sourcegitcommit: 1c91b7b24537d0e54d484c3379043db53c1aea65
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/29/2020
ms.locfileid: "41599121"
---
# <a name="isolated-sharepoint-online-team-site-devtest-environment"></a><span data-ttu-id="9e1ab-103">Site d’équipe SharePoint Online isolé dans votre environnement de développement/test</span><span class="sxs-lookup"><span data-stu-id="9e1ab-103">Isolated SharePoint Online team site dev/test environment</span></span>

 <span data-ttu-id="9e1ab-104">**Résumé :** Configurez un site d’équipe SharePoint Online isolé du reste de l’organisation dans votre environnement de développement/test Office 365.</span><span class="sxs-lookup"><span data-stu-id="9e1ab-104">**Summary:** Configure a SharePoint Online team site that is isolated from the rest of the organization in your Office 365 dev/test environment.</span></span>

<span data-ttu-id="9e1ab-105">Les sites d’équipe SharePoint Online dans Office 365 sont des emplacements de collaboration à l’aide d’une bibliothèque de documents commune, d’un bloc-notes OneNote et d’autres services.</span><span class="sxs-lookup"><span data-stu-id="9e1ab-105">SharePoint Online team sites in Office 365 are locations for collaboration using a common document library, a OneNote notebook, and other services.</span></span> <span data-ttu-id="9e1ab-106">Dans de nombreux cas, vous souhaitez bénéficier d’un large accès et d’une collaboration entre les départements ou organisations.</span><span class="sxs-lookup"><span data-stu-id="9e1ab-106">In many cases, you want wide access and collaboration across departments or organizations.</span></span> <span data-ttu-id="9e1ab-107">Toutefois, dans certains cas, vous souhaitez contrôler étroitement l’accès et les autorisations de collaboration entre un petit groupe de personnes.</span><span class="sxs-lookup"><span data-stu-id="9e1ab-107">However, in some cases, you want to tightly control the access and permissions for collaboration among a small group of people.</span></span>

<span data-ttu-id="9e1ab-108">L’accès aux sites d’équipe SharePoint Online et ce que les utilisateurs peuvent faire sont contrôlés par les groupes SharePoint et les niveaux d’autorisation.</span><span class="sxs-lookup"><span data-stu-id="9e1ab-108">Access to SharePoint Online team sites and what users can do is controlled by SharePoint groups and permission levels.</span></span> <span data-ttu-id="9e1ab-109">Par défaut, les sites SharePoint Online comportent trois niveaux d’accès :</span><span class="sxs-lookup"><span data-stu-id="9e1ab-109">By default, SharePoint Online sites have three levels of access:</span></span>

- <span data-ttu-id="9e1ab-110">Les **membres** peuvent afficher, créer et modifier des ressources sur le site.</span><span class="sxs-lookup"><span data-stu-id="9e1ab-110">**Members**, who can view, create, and modify resources on the site.</span></span>

- <span data-ttu-id="9e1ab-111">Les **propriétaires** ont un contrôle total sur le site, et peuvent même modifier les autorisations.</span><span class="sxs-lookup"><span data-stu-id="9e1ab-111">**Owners**, who have complete control of the site, including the ability to change permissions.</span></span>

- <span data-ttu-id="9e1ab-112">Les **Visiteurs** peuvent uniquement afficher les ressources du site.</span><span class="sxs-lookup"><span data-stu-id="9e1ab-112">**Visitors**, who only can view resources on the site.</span></span>

<span data-ttu-id="9e1ab-113">Cet article décrit la configuration d’un site d’équipe SharePoint Online isolé pour un projet de recherche secrète nommé ProjectX.</span><span class="sxs-lookup"><span data-stu-id="9e1ab-113">This article steps you through the configuration of an isolated SharePoint Online team site for a secret research project named ProjectX.</span></span> <span data-ttu-id="9e1ab-114">Les conditions d’accès sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="9e1ab-114">The access requirements are:</span></span>

- <span data-ttu-id="9e1ab-115">Seuls les membres du projet peuvent accéder au site et à son contenu (documents, bloc-notes OneNote, pages), avec des niveaux d’autorisation SharePoint pour éditer et afficher contrôlés via l’appartenance au groupe.</span><span class="sxs-lookup"><span data-stu-id="9e1ab-115">Only members of the project can access the site and its contents (documents, OneNote Notebook, Pages), with edit and view SharePoint permission levels controlled through group membership.</span></span>

- <span data-ttu-id="9e1ab-116">Seuls le créateur du site et les membres d’un groupe d’administrateurs du site peuvent effectuer l’administration du site, y compris la modification des autorisations au niveau du site.</span><span class="sxs-lookup"><span data-stu-id="9e1ab-116">Only the site creator and members of an Admins group for the site can perform site administration, which includes modifying site-level permissions.</span></span>

<span data-ttu-id="9e1ab-117">Il existe trois phases de configuration d’un site d’équipe SharePoint Online isolé dans votre environnement de développement/test Office 365 :</span><span class="sxs-lookup"><span data-stu-id="9e1ab-117">There are three phases to setting up an isolated SharePoint Online team site in your Office 365 dev/test environment:</span></span>

1. <span data-ttu-id="9e1ab-118">Créez l’environnement de développement/test Office 365.</span><span class="sxs-lookup"><span data-stu-id="9e1ab-118">Create the Office 365 dev/test environment.</span></span>

2. <span data-ttu-id="9e1ab-119">Créez les utilisateurs et groupes pour ProjectX.</span><span class="sxs-lookup"><span data-stu-id="9e1ab-119">Create the users and groups for ProjectX.</span></span>

3. <span data-ttu-id="9e1ab-120">Créez un site d’équipe SharePoint Online ProjectX et isolez-le.</span><span class="sxs-lookup"><span data-stu-id="9e1ab-120">Create a new ProjectX SharePoint Online team site and isolate it.</span></span>

> [!TIP]
> <span data-ttu-id="9e1ab-121">Cliquez [ici](https://aka.ms/catlgstack) pour afficher le plan de tous les articles de l’ensemble de guides de laboratoire de test de Microsoft Cloud.</span><span class="sxs-lookup"><span data-stu-id="9e1ab-121">Click [here](https://aka.ms/catlgstack) for a visual map to all the articles in the One Microsoft Cloud Test Lab Guide stack.</span></span>

## <a name="phase-1-build-out-your-lightweight-or-simulated-enterprise-office-365-devtest-environment"></a><span data-ttu-id="9e1ab-122">Phase 1 : Créer votre environnement de développement/test Office 365 en mode léger ou pour entreprise simulée</span><span class="sxs-lookup"><span data-stu-id="9e1ab-122">Phase 1: Build out your lightweight or simulated enterprise Office 365 dev/test environment</span></span>

<span data-ttu-id="9e1ab-123">Si vous souhaitez simplement créer un site d’équipe SharePoint Online isolé avec la configuration minimale requise, suivez les instructions des phases 2 et 3 de l’environnement de [développement/test Office 365](https://docs.microsoft.com/office365/enterprise/office-365-dev-test-environment).</span><span class="sxs-lookup"><span data-stu-id="9e1ab-123">If you just want to create an isolated SharePoint Online team site in a lightweight way with the minimum requirements, follow the instructions in phases 2 and 3 of [Office 365 dev/test environment](https://docs.microsoft.com/office365/enterprise/office-365-dev-test-environment).</span></span>

<span data-ttu-id="9e1ab-124">Si vous souhaitez créer un site d’équipe SharePoint Online isolé dans une configuration d’entreprise simulée, suivez les instructions de [DirSync pour votre environnement de développement/test Office 365](https://docs.microsoft.com/office365/enterprise/dirsync-for-your-office-365-dev-test-environment).</span><span class="sxs-lookup"><span data-stu-id="9e1ab-124">If you want to create an isolated SharePoint Online team site in a simulated enterprise configuration, follow the instructions in [DirSync for your Office 365 dev/test environment](https://docs.microsoft.com/office365/enterprise/dirsync-for-your-office-365-dev-test-environment).</span></span>

> [!NOTE]
> <span data-ttu-id="9e1ab-125">La création d’un site SharePoint Online isolé ne nécessite pas l’environnement de développement/test d’entreprise simulé, qui inclut un intranet simulé connecté à Internet et la synchronisation d’annuaires pour une forêt des services de domaine Active Directory (AD DS).</span><span class="sxs-lookup"><span data-stu-id="9e1ab-125">Creating an isolated SharePoint Online site does not require the simulated enterprise dev/test environment, which includes a simulated intranet connected to the Internet and directory synchronization for a Active Directory Domain Services (AD DS) forest.</span></span> <span data-ttu-id="9e1ab-126">Il est proposé comme option dans cet article afin que vous puissiez tester un site SharePoint Online isolé et faire des essais dans un environnement qui représente une organisation classique.</span><span class="sxs-lookup"><span data-stu-id="9e1ab-126">It is provided here as an option so that you can test an isolated SharePoint Online site and experiment with it in an environment that represents a typical organization.</span></span>

## <a name="phase-2-create-user-accounts-and-access-groups"></a><span data-ttu-id="9e1ab-127">Phase 2 : créer des comptes d’utilisateurs et des groupes d’accès</span><span class="sxs-lookup"><span data-stu-id="9e1ab-127">Phase 2: Create user accounts and access groups</span></span>

<span data-ttu-id="9e1ab-128">Utilisez les instructions de [connexion à office 365 PowerShell](https://docs.microsoft.com/office365/enterprise/powershell/connect-to-office-365-powershell) pour vous connecter à votre abonnement final Office 365 avec votre compte d’administrateur général à partir de :</span><span class="sxs-lookup"><span data-stu-id="9e1ab-128">Use the instructions in [Connect to Office 365 PowerShell](https://docs.microsoft.com/office365/enterprise/powershell/connect-to-office-365-powershell) to connect to your Office 365 trail subscription with your global administrator account from:</span></span>

- <span data-ttu-id="9e1ab-129">Votre ordinateur (pour l’environnement de développement/test Office 365 léger).</span><span class="sxs-lookup"><span data-stu-id="9e1ab-129">Your computer (for the lightweight Office 365 dev/test environment).</span></span>

- <span data-ttu-id="9e1ab-130">La machine virtuelle CLIENT1 (pour l’environnement de développement/test Office 365 d’entreprise simulé).</span><span class="sxs-lookup"><span data-stu-id="9e1ab-130">The CLIENT1 virtual machine (for the simulated enterprise Office 365 dev/test environment).</span></span>

<span data-ttu-id="9e1ab-131">Pour créer les nouveaux groupes d’accès pour le site d’équipe SharePoint Online ProjectX, exécutez les commandes suivantes à partir de l’invite du module Windows Azure Active Directory pour Windows PowerShell :</span><span class="sxs-lookup"><span data-stu-id="9e1ab-131">To create the new access groups for the ProjectX SharePoint Online team site, run these commands from the Windows Azure Active Directory Module for Windows PowerShell prompt:</span></span>

```powershell
$groupName="ProjectX-Members"
$groupDesc="People allowed to collaborate for ProjectX."
New-MsolGroup -DisplayName $groupName -Description $groupDesc
$groupName="ProjectX-Admins"
$groupDesc="People allowed to administer SharePoint for ProjectX."
New-MsolGroup -DisplayName $groupName -Description $groupDesc
$groupName="ProjectX-Viewers"
$groupDesc="People allowed to view the SharePoint resources for ProjectX."
New-MsolGroup -DisplayName $groupName -Description $groupDesc
```

<span data-ttu-id="9e1ab-132">Entrez le nom de votre organisation (exemple : contosotoycompany) et le code de pays à deux caractères pour indiquer votre emplacement, puis exécutez les commandes suivantes à partir de l’invite Module Windows Azure Active Directory pour Windows PowerShell :</span><span class="sxs-lookup"><span data-stu-id="9e1ab-132">Fill in your organization name (example: contosotoycompany), the two-character country code for your location, and then run the following commands from the Windows Azure Active Directory Module for Windows PowerShell prompt:</span></span>

```powershell
$orgName="<organization name>"
$loc="<two-character country code, such as US>"
$licAssignment= $orgName + ":ENTERPRISEPREMIUM"
$userName= "designer@" + $orgName + ".onmicrosoft.com"
New-MsolUser -DisplayName "Lead Designer" -FirstName Lead -LastName Designer -UserPrincipalName $userName -UsageLocation $loc -LicenseAssignment $licAssignment -ForceChangePassword $false
```

<span data-ttu-id="9e1ab-133">À partir de la zone de la commande **New-MsolUser**, notez le mot de passe généré pour le compte Responsable de la conception et enregistrez-le dans un emplacement sécurisé.</span><span class="sxs-lookup"><span data-stu-id="9e1ab-133">From the display of the **New-MsolUser** command, note the generated password for the Lead Designer account and record it in a safe location.</span></span>

<span data-ttu-id="9e1ab-134">Exécutez les commandes suivantes à partir de l’invite Module Windows Azure Active Directory pour Windows PowerShell :</span><span class="sxs-lookup"><span data-stu-id="9e1ab-134">Run the following commands from the Windows Azure Active Directory Module for Windows PowerShell prompt:</span></span>

```powershell
$userName= "researcher@" + $orgName + ".onmicrosoft.com"
New-MsolUser -DisplayName "Lead Researcher" -FirstName Lead -LastName Researcher -UserPrincipalName $userName -UsageLocation $loc -LicenseAssignment $licAssignment -ForceChangePassword $false
```

<span data-ttu-id="9e1ab-135">À partir de la zone de la commande **New-MsolUser**, notez le mot de passe généré pour le compte Responsable de la recherche et enregistrez-le dans un emplacement sécurisé.</span><span class="sxs-lookup"><span data-stu-id="9e1ab-135">From the display of the **New-MsolUser** command, note the generated password for the Lead Researcher account and record it in a safe location.</span></span>

<span data-ttu-id="9e1ab-136">Exécutez les commandes suivantes à partir de l’invite Module Windows Azure Active Directory pour Windows PowerShell :</span><span class="sxs-lookup"><span data-stu-id="9e1ab-136">Run the following commands from the Windows Azure Active Directory Module for Windows PowerShell prompt:</span></span>

```powershell
$userName= "devvp@" + $orgName + ".onmicrosoft.com"
New-MsolUser -DisplayName "Development VP" -FirstName Development -LastName VP -UserPrincipalName $userName -UsageLocation $loc -LicenseAssignment $licAssignment -ForceChangePassword $false
```

<span data-ttu-id="9e1ab-137">À partir de la zone de la commande **New-MsolUser**, notez le mot de passe généré pour le compte VP du développement et enregistrez-le dans un emplacement sécurisé.</span><span class="sxs-lookup"><span data-stu-id="9e1ab-137">From the display of the **New-MsolUser** command, note the generated password for the Development VP account and record it in a safe location.</span></span>

<span data-ttu-id="9e1ab-138">Ensuite, pour ajouter les nouveaux comptes aux nouveaux groupes d’accès, exécutez les commandes PowerShell suivantes à partir de l’invite du module Windows Azure Active Directory pour Windows PowerShell :</span><span class="sxs-lookup"><span data-stu-id="9e1ab-138">Next, to add the new accounts to the new access groups, run these PowerShell commands from the Windows Azure Active Directory Module for Windows PowerShell prompt:</span></span>

```powershell
$grpName="ProjectX-Members"
$userUPN="designer@" + $orgName + ".onmicrosoft.com"
Add-MsolGroupMember -GroupObjectId (Get-MsolGroup | Where { $_.DisplayName -eq $grpName }).ObjectID -GroupMemberObjectId (Get-MsolUser | Where { $_.UserPrincipalName -eq $userUPN }).ObjectID -GroupMemberType "User"
$userUPN="researcher@" + $orgName + ".onmicrosoft.com"
Add-MsolGroupMember -GroupObjectId (Get-MsolGroup | Where { $_.DisplayName -eq $grpName }).ObjectID -GroupMemberObjectId (Get-MsolUser | Where { $_.UserPrincipalName -eq $userUPN }).ObjectID -GroupMemberType "User"
$grpName="ProjectX-Admins"
Add-MsolGroupMember -GroupObjectId (Get-MsolGroup | Where { $_.DisplayName -eq $grpName }).ObjectID -GroupMemberObjectId (Get-MsolUser | Where { $_.UserPrincipalName -eq $userCredential.UserName }).ObjectID -GroupMemberType "User"
$grpName="ProjectX-Viewers"
$userUPN="devvp@" + $orgName + ".onmicrosoft.com"
Add-MsolGroupMember -GroupObjectId (Get-MsolGroup | Where { $_.DisplayName -eq $grpName }).ObjectID -GroupMemberObjectId (Get-MsolUser | Where { $_.UserPrincipalName -eq $userUPN }).ObjectID -GroupMemberType "User"
```

<span data-ttu-id="9e1ab-139">Résultats</span><span class="sxs-lookup"><span data-stu-id="9e1ab-139">Results:</span></span>

- <span data-ttu-id="9e1ab-140">Le groupe d’accès ProjectX-membres contient les comptes d’utilisateur concepteur de prospects et chercheur de prospect</span><span class="sxs-lookup"><span data-stu-id="9e1ab-140">The ProjectX-Members access group contains the Lead Designer and Lead Researcher user accounts</span></span>

- <span data-ttu-id="9e1ab-141">Le groupe d’accès ProjectX-administrateurs contient le compte d’administrateur général pour votre abonnement à la version d’évaluation</span><span class="sxs-lookup"><span data-stu-id="9e1ab-141">The ProjectX-Admins access group contains the global administrator account for your trial subscription</span></span>

- <span data-ttu-id="9e1ab-142">Le groupe d’accès ProjectX-visualisers contient le compte d’utilisateur VP du développement.</span><span class="sxs-lookup"><span data-stu-id="9e1ab-142">The ProjectX-Viewers access group contains the Development VP user account</span></span>

<span data-ttu-id="9e1ab-143">La figure 1 présente les groupes d’accès et leur appartenance.</span><span class="sxs-lookup"><span data-stu-id="9e1ab-143">Figure 1 shows the access groups and their membership.</span></span>

<span data-ttu-id="9e1ab-144">**Figure 1**</span><span class="sxs-lookup"><span data-stu-id="9e1ab-144">**Figure 1**</span></span>

![Les groupes Office 365 et leur appartenance pour un site de groupe SharePoint Online isolé](../media/5b7373b9-2a80-4880-afe5-63ffb17237e6.png)

## <a name="phase-3-create-a-new-projectx-sharepoint-online-team-site-and-isolate-it"></a><span data-ttu-id="9e1ab-146">Phase 3 : créer un nouveau site d’équipe ProjectX SharePoint Online et l’isoler</span><span class="sxs-lookup"><span data-stu-id="9e1ab-146">Phase 3: Create a new ProjectX SharePoint Online team site and isolate it</span></span>

<span data-ttu-id="9e1ab-147">Pour créer un site d’équipe SharePoint Online pour ProjectX, procédez comme suit :</span><span class="sxs-lookup"><span data-stu-id="9e1ab-147">To create a SharePoint Online team site for ProjectX, do the following:</span></span>

1. <span data-ttu-id="9e1ab-148">À l’aide d’un navigateur sur votre ordinateur local (configuration légère) ou sur CLIENT1 (configuration d’entreprise simulée), connectez-vous au portail[https://admin.microsoft.com](https://admin.microsoft.com)Office 365 () à l’aide de votre compte d’administrateur général.</span><span class="sxs-lookup"><span data-stu-id="9e1ab-148">Using a browser on either your local computer (lightweight configuration) or on CLIENT1 (simulated enterprise configuration), sign in to the Office 365 portal ([https://admin.microsoft.com](https://admin.microsoft.com)) using your global administrator account.</span></span>

2. <span data-ttu-id="9e1ab-149">Dans la liste des mosaïques, cliquez sur **SharePoint**.</span><span class="sxs-lookup"><span data-stu-id="9e1ab-149">In the list of tiles, click **SharePoint**.</span></span>

3. <span data-ttu-id="9e1ab-150">Dans le nouvel onglet SharePoint de votre navigateur, cliquez sur **+ Créer un site**.</span><span class="sxs-lookup"><span data-stu-id="9e1ab-150">On the new SharePoint tab in your browser, click **+ Create site**.</span></span>

4. <span data-ttu-id="9e1ab-151">Dans **Nom du site d’équipe**, saisissez **ProjectX**.</span><span class="sxs-lookup"><span data-stu-id="9e1ab-151">In **Team site name**, type **ProjectX**.</span></span> <span data-ttu-id="9e1ab-152">Dans **paramètres de confidentialité**, sélectionnez **privé-seuls les membres peuvent accéder à ce site**.</span><span class="sxs-lookup"><span data-stu-id="9e1ab-152">In **Privacy settings**, select **Private - only members can access this site**.</span></span>

5. <span data-ttu-id="9e1ab-153">Dans **Description du site d’équipe**, saisissez **Site SharePoint pour ProjectX**, puis cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="9e1ab-153">In **Team site description**, type **SharePoint site for ProjectX**, and then click **Next**.</span></span>

6. <span data-ttu-id="9e1ab-154">Dans le volet **Qui voulez-vous ajouter ?**, cliquez sur **Terminer**.</span><span class="sxs-lookup"><span data-stu-id="9e1ab-154">On the **Who do you want to add**? pane, click **Finish**.</span></span>

7. <span data-ttu-id="9e1ab-155">Dans le nouvel onglet **ProjectX-Accueil** de votre navigateur, dans la barre d’outils, cliquez sur l’icône des paramètres, puis sur **Autorisations du site**.</span><span class="sxs-lookup"><span data-stu-id="9e1ab-155">On the new **ProjectX-Home** tab in your browser, in the tool bar, click the settings icon, and then click **Site permissions**.</span></span>

8. <span data-ttu-id="9e1ab-156">Dans le volet **Autorisations du site**, cliquez sur **Paramètres d’autorisations avancés**.</span><span class="sxs-lookup"><span data-stu-id="9e1ab-156">In the **Site permissions** pane, click **Advanced permissions settings**.</span></span>

9. <span data-ttu-id="9e1ab-157">Dans le nouvel onglet **Autorisations : Projet X** de votre navigateur, cliquez sur **Paramètres de demande d’accès**.</span><span class="sxs-lookup"><span data-stu-id="9e1ab-157">In the new **Permissions: Project X** tab in your browser, click **Access Request Settings**.</span></span>

10. <span data-ttu-id="9e1ab-158">Dans la boîte de dialogue **Paramètres de demande d’accès**, désactivez les cases à cocher **Autoriser les membres à partager le site et les fichiers et dossiers individuels** et **Autoriser les demandes d’accès** (afin que les trois cases à cocher soient désactivées), puis cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="9e1ab-158">In the **Access Requests Settings** dialog box, clear **Allow members to share the site and individual files and folders** and **Allow access requests** (so that all three check boxes are cleared), and then click **OK**.</span></span>

11. <span data-ttu-id="9e1ab-159">Cliquez sur **Membres de ProjectX** dans la liste.</span><span class="sxs-lookup"><span data-stu-id="9e1ab-159">Click **ProjectX Members** in the list.</span></span>

12. <span data-ttu-id="9e1ab-160">Dans la page **Personnes et groupes**, cliquez sur **Nouveau**.</span><span class="sxs-lookup"><span data-stu-id="9e1ab-160">On the **People and Groups** page, click **New**.</span></span>

13. <span data-ttu-id="9e1ab-161">Dans la boîte de dialogue **Partager**, saisissez **ProjectX-Membres**, sélectionnez-le, puis cliquez sur **Partager**.</span><span class="sxs-lookup"><span data-stu-id="9e1ab-161">In the **Share** dialog box, type **ProjectX-Members**, select it, and then click **Share**.</span></span>

14. <span data-ttu-id="9e1ab-162">Cliquez sur le bouton de retour de votre navigateur.</span><span class="sxs-lookup"><span data-stu-id="9e1ab-162">Click the back button on your browser.</span></span>

15. <span data-ttu-id="9e1ab-163">Cliquez sur **Propriétaires de ProjectX** dans la liste.</span><span class="sxs-lookup"><span data-stu-id="9e1ab-163">Click **ProjectX Owners** in the list.</span></span>

16. <span data-ttu-id="9e1ab-164">Dans la page **Personnes et groupes**, cliquez sur **Nouveau**.</span><span class="sxs-lookup"><span data-stu-id="9e1ab-164">On the **People and Groups** page, click **New**.</span></span>

17. <span data-ttu-id="9e1ab-165">Dans la boîte de dialogue **Partager**, saisissez **ProjectX-Administrateurs**, sélectionnez-le, puis cliquez sur **Partager**.</span><span class="sxs-lookup"><span data-stu-id="9e1ab-165">In the **Share** dialog box, type **ProjectX-Admins**, select it, and then click **Share**.</span></span>

18. <span data-ttu-id="9e1ab-166">Cliquez sur le bouton de retour de votre navigateur.</span><span class="sxs-lookup"><span data-stu-id="9e1ab-166">Click the back button on your browser.</span></span>

19. <span data-ttu-id="9e1ab-167">Cliquez sur **Visiteurs de ProjectX** dans la liste.</span><span class="sxs-lookup"><span data-stu-id="9e1ab-167">Click **ProjectX Visitors** in the list.</span></span>

20. <span data-ttu-id="9e1ab-168">Dans la page **Personnes et groupes**, cliquez sur **Nouveau**.</span><span class="sxs-lookup"><span data-stu-id="9e1ab-168">On the **People and Groups** page, click **New**.</span></span>

21. <span data-ttu-id="9e1ab-169">Dans la boîte de dialogue **Partager**, saisissez **ProjectX-Utilisateurs**, sélectionnez-le, puis cliquez sur **Partager**.</span><span class="sxs-lookup"><span data-stu-id="9e1ab-169">In the **Share** dialog box, type **ProjectX-Viewers**, select it, and then click **Share**.</span></span>

22. <span data-ttu-id="9e1ab-170">Fermez l’onglet **Personnes et groupes** de votre navigateur, cliquez sur l’onglet **ProjectX-Accueil** de votre navigateur, puis fermez le volet **Autorisations du site**.</span><span class="sxs-lookup"><span data-stu-id="9e1ab-170">Close the **People and Groups** tab in your browser, click the **ProjectX-Home** tab in your browser, and then close the **Site permissions** pane.</span></span>

<span data-ttu-id="9e1ab-171">Voici les résultats de la configuration des autorisations :</span><span class="sxs-lookup"><span data-stu-id="9e1ab-171">Here are the results of configuring permissions:</span></span>

- <span data-ttu-id="9e1ab-172">Le groupe SharePoint membres de ProjectX contient uniquement le groupe d’accès ProjectX membres (qui contient uniquement les comptes d’utilisateur de concepteur de prospect et de chercheur de Prospect) et le groupe ProjectX (qui contient uniquement le compte d’utilisateur d’administrateur général).</span><span class="sxs-lookup"><span data-stu-id="9e1ab-172">The ProjectX Members SharePoint group contains only the ProjectX-Members access group (which contains only the Lead Designer and Lead Researcher user accounts) and the ProjectX group (which contains only the global administrator user account).</span></span>

- <span data-ttu-id="9e1ab-173">Le groupe SharePoint propriétaires ProjectX contient uniquement le groupe d’accès ProjectX-administrateurs (qui contient uniquement le compte d’utilisateur de l’administrateur général).</span><span class="sxs-lookup"><span data-stu-id="9e1ab-173">The ProjectX Owners SharePoint group contains only the ProjectX-Admins access group (which contains only the global administrator user account).</span></span>

- <span data-ttu-id="9e1ab-174">Le groupe SharePoint visiteurs ProjectX contient uniquement le groupe d’accès ProjectX-affiche (qui contient uniquement le compte d’utilisateur VP du développement).</span><span class="sxs-lookup"><span data-stu-id="9e1ab-174">The ProjectX Visitors SharePoint group contains only the ProjectX-Viewers access group (which contains only the Development VP user account).</span></span>

- <span data-ttu-id="9e1ab-175">Les membres ne peuvent pas modifier les autorisations au niveau du site (cette opération peut être uniquement effectuée par les membres du groupe ProjectX-Administrateurs).</span><span class="sxs-lookup"><span data-stu-id="9e1ab-175">Members cannot modify site-level permissions (this can only be done by members of the ProjectX-Admins group).</span></span>

- <span data-ttu-id="9e1ab-176">Les autres comptes d’utilisateurs ne peuvent pas accéder au site ni à ses ressources, ni demander l’accès au site.</span><span class="sxs-lookup"><span data-stu-id="9e1ab-176">Other user accounts cannot access the site or its resources or request access to the site.</span></span>

<span data-ttu-id="9e1ab-177">La figure 2 présente les groupes SharePoint et leur appartenance.</span><span class="sxs-lookup"><span data-stu-id="9e1ab-177">Figure 2 shows the SharePoint groups and their membership.</span></span>

<span data-ttu-id="9e1ab-178">**Figure 2**</span><span class="sxs-lookup"><span data-stu-id="9e1ab-178">**Figure 2**</span></span>

![Groupes SharePoint Online et leur appartenance pour un site de groupe SharePoint Online isolé](../media/595abff4-64f9-49de-a37a-c70c6856936b.png)

<span data-ttu-id="9e1ab-180">Nous allons maintenant illustrer l’accès à l’aide du compte d’utilisateur du Concepteur sénior :</span><span class="sxs-lookup"><span data-stu-id="9e1ab-180">Now let's demonstrate access using the Lead Designer user account:</span></span>

1. <span data-ttu-id="9e1ab-181">Fermez l’onglet **ProjectX-Accueil** dans votre navigateur, puis cliquez sur l’onglet **Accueil Microsoft Office** du navigateur.</span><span class="sxs-lookup"><span data-stu-id="9e1ab-181">Close the **ProjectX-Home** tab in your browser, and then click the **Microsoft Office Home** tab in your browser.</span></span>

2. <span data-ttu-id="9e1ab-182">Cliquez sur le nom de votre administrateur général, puis cliquez sur **Déconnexion**.</span><span class="sxs-lookup"><span data-stu-id="9e1ab-182">Click the name of your global administrator, and then click **Sign out**.</span></span>

3. <span data-ttu-id="9e1ab-183">Connectez-vous au portail Office 365 ([https://admin.microsoft.com](https://admin.microsoft.com)) à l’aide du nom de compte du concepteur de prospect et de son mot de passe.</span><span class="sxs-lookup"><span data-stu-id="9e1ab-183">Sign in to the Office 365 portal ([https://admin.microsoft.com](https://admin.microsoft.com)) using the Lead Designer account name and its password.</span></span>

4. <span data-ttu-id="9e1ab-184">Dans la liste des vignettes, cliquez sur **SharePoint**.</span><span class="sxs-lookup"><span data-stu-id="9e1ab-184">In the list of tiles, click **SharePoint**.</span></span>

5. <span data-ttu-id="9e1ab-185">Dans le nouvel onglet **SharePoint** de votre navigateur, tapez **ProjectX** dans la zone de recherche, activez la recherche, puis cliquez sur le site d’équipe **ProjectX** .</span><span class="sxs-lookup"><span data-stu-id="9e1ab-185">On the new **SharePoint** tab in your browser, type **ProjectX** in the search box, activate the search, and then click the **ProjectX** team site.</span></span> <span data-ttu-id="9e1ab-186">Un nouvel onglet doit apparaître dans votre navigateur pour le site d’équipe ProjectX.</span><span class="sxs-lookup"><span data-stu-id="9e1ab-186">You should see a new tab in your browser for the ProjectX team site.</span></span>

6. <span data-ttu-id="9e1ab-p107">Cliquez sur l’icône des paramètres. Notez qu’il n’existe pas d’option pour **Autorisations du site**. Cela est correct puisque seuls les membres du groupe ProjectX-Administrateurs peuvent modifier les autorisations sur le site</span><span class="sxs-lookup"><span data-stu-id="9e1ab-p107">Click the settings icon. Notice that there is no option for **Site Permissions**. This is correct because only the members of the ProjectX-Admins group can modify permissions on the site</span></span>

7. <span data-ttu-id="9e1ab-190">Ouvrez le bloc-notes ou un éditeur de texte de votre choix.</span><span class="sxs-lookup"><span data-stu-id="9e1ab-190">Open Notepad or a text editor of your choice.</span></span>

8. <span data-ttu-id="9e1ab-191">Copiez l’URL du site d’équipe ProjectX et collez-la dans une nouvelle ligne dans le bloc-notes ou dans votre éditeur de texte.</span><span class="sxs-lookup"><span data-stu-id="9e1ab-191">Copy the URL of the ProjectX team site and paste it on a new line in Notepad or your text editor.</span></span>

9. <span data-ttu-id="9e1ab-192">Dans le nouvel onglet **ProjectX-Accueil** de votre navigateur, cliquez sur **Documents**.</span><span class="sxs-lookup"><span data-stu-id="9e1ab-192">On the new **ProjectX-Home** tab in your browser, click **Documents**.</span></span>

10. <span data-ttu-id="9e1ab-193">Copiez l’URL du dossier de documents ProjectX et collez-la dans une nouvelle ligne dans le bloc-notes ou dans votre éditeur de texte.</span><span class="sxs-lookup"><span data-stu-id="9e1ab-193">Copy the URL of the ProjectX documents folder and paste it on a new line in Notepad or your text editor.</span></span>

11. <span data-ttu-id="9e1ab-194">Dans le nouvel onglet **ProjectX-Documents** de votre navigateur, cliquez sur **Nouveau > Document Word**.</span><span class="sxs-lookup"><span data-stu-id="9e1ab-194">On the new **ProjectX-Documents** tab in your browser, click **New > Word document**.</span></span>

12. <span data-ttu-id="9e1ab-195">Tapez du texte sur la page, attendez que l’état indique **enregistré**, cliquez sur le bouton précédent de votre navigateur, puis actualisez la page.</span><span class="sxs-lookup"><span data-stu-id="9e1ab-195">Type some text on the page, wait for the status to indicate **Saved**, click the back button on your browser, and then refresh the page.</span></span> <span data-ttu-id="9e1ab-196">Vous devriez voir un nouveau **Document.docx** dans le dossier **Documents**.</span><span class="sxs-lookup"><span data-stu-id="9e1ab-196">You should see a new **Document.docx** in the **Documents** folder.</span></span>

13. <span data-ttu-id="9e1ab-197">Cliquez sur les points de suspension du document **Document.docx**, puis sur **Obtenir un lien**.</span><span class="sxs-lookup"><span data-stu-id="9e1ab-197">Click the ellipsis for the **Document.docx** document, and then click **Get a link**.</span></span>

14. <span data-ttu-id="9e1ab-198">Copiez l’URL dans la boîte de dialogue **partager « document. docx »** et collez-la dans une nouvelle ligne dans le bloc-notes ou dans votre éditeur de texte, puis fermez la boîte de dialogue **« document. docx » de partage** .</span><span class="sxs-lookup"><span data-stu-id="9e1ab-198">Copy the URL in the **Share 'Document.docx'** dialog box and paste it on a new line in Notepad or your text editor, and then close the **Share 'Document.docx'** dialog box.</span></span>

15. <span data-ttu-id="9e1ab-199">Fermez les onglets **ProjectX-Documents** et **SharePoint** dans votre navigateur, puis cliquez sur l’onglet **Accueil Microsoft Office**.</span><span class="sxs-lookup"><span data-stu-id="9e1ab-199">Close the **ProjectX-Documents** and **SharePoint** tabs in your browser, and then click the **Microsoft Office Home** tab.</span></span>

16. <span data-ttu-id="9e1ab-200">Cliquez sur le nom **Responsable de la conception**, puis cliquez sur **Déconnexion**.</span><span class="sxs-lookup"><span data-stu-id="9e1ab-200">Click the **Lead Designer** name, and then click **Sign out**.</span></span>

<span data-ttu-id="9e1ab-201">Nous allons maintenant illustrer l’accès à l’aide du compte d’utilisateur VP du développement :</span><span class="sxs-lookup"><span data-stu-id="9e1ab-201">Now let's demonstrate access using the Development VP user account:</span></span>

1. <span data-ttu-id="9e1ab-202">Connectez-vous au portail Office 365 ([https://admin.microsoft.com](https://admin.microsoft.com)) à l’aide du nom de compte VP du développement et de son mot de passe.</span><span class="sxs-lookup"><span data-stu-id="9e1ab-202">Sign in to the Office 365 portal ([https://admin.microsoft.com](https://admin.microsoft.com)) using the Development VP account name and its password.</span></span>

2. <span data-ttu-id="9e1ab-203">Dans la liste des vignettes, cliquez sur **SharePoint**.</span><span class="sxs-lookup"><span data-stu-id="9e1ab-203">In the list of tiles, click **SharePoint**.</span></span>

3. <span data-ttu-id="9e1ab-204">Dans le nouvel onglet **SharePoint** de votre navigateur, tapez **ProjectX** dans la zone de recherche, activez la recherche, puis cliquez sur le site d’équipe **ProjectX** .</span><span class="sxs-lookup"><span data-stu-id="9e1ab-204">On the new **SharePoint** tab in your browser, type **ProjectX** in the search box, activate the search, and then click the **ProjectX** team site.</span></span> <span data-ttu-id="9e1ab-205">Un nouvel onglet doit apparaître dans votre navigateur pour le site d’équipe ProjectX.</span><span class="sxs-lookup"><span data-stu-id="9e1ab-205">You should see a new tab in your browser for the ProjectX team site.</span></span>

4. <span data-ttu-id="9e1ab-206">Cliquez sur **Documents**, puis sur le fichier **Document.docx**.</span><span class="sxs-lookup"><span data-stu-id="9e1ab-206">Click **Documents**, and then click the **Document.docx** file.</span></span>

5. <span data-ttu-id="9e1ab-p110">Dans l’onglet **Document.docx** de votre navigateur, essayez de modifier le texte. Vous devriez voir un message indiquant **Ce document est en lecture seule.** Ceci est dû au fait que le compte d’utilisateur VP du développement comporte seulement des autorisations d’affichage pour le site.</span><span class="sxs-lookup"><span data-stu-id="9e1ab-p110">In the **Document.docx** tab in your browser, try to modify the text. You should see a message stating **This document is read-only.** This is expected because the Development VP user account only has view permissions for the site.</span></span>

6. <span data-ttu-id="9e1ab-210">Fermer les onglets **Document.docx**, **ProjectX-Documents** et **SharePoint** de votre navigateur.</span><span class="sxs-lookup"><span data-stu-id="9e1ab-210">Close the **Document.docx**, **ProjectX-Documents**, and **SharePoint** tabs in your browser.</span></span>

7. <span data-ttu-id="9e1ab-211">Cliquez sur l’onglet **Accueil Microsoft Office**, sur le nom **VP du développement**, puis sur **Déconnexion**.</span><span class="sxs-lookup"><span data-stu-id="9e1ab-211">Click the **Microsoft Office Home** tab, click the **Development VP** name, and then click **Sign out**.</span></span>

<span data-ttu-id="9e1ab-212">À présent, nous allons illustrer l’accès à un compte d’utilisateur qui n’a pas d’autorisations :</span><span class="sxs-lookup"><span data-stu-id="9e1ab-212">Now let's demonstrate access with a user account that has no permissions:</span></span>

1. <span data-ttu-id="9e1ab-213">Connectez-vous au portail Office 365 ([https://admin.microsoft.com](https://admin.microsoft.com)) à l’aide du nom de compte utilisateur 3 et de son mot de passe.</span><span class="sxs-lookup"><span data-stu-id="9e1ab-213">Sign in to the Office 365 portal ([https://admin.microsoft.com](https://admin.microsoft.com)) using the User 3 account name and its password.</span></span>

2. <span data-ttu-id="9e1ab-214">Dans la liste des mosaïques, cliquez sur **SharePoint**.</span><span class="sxs-lookup"><span data-stu-id="9e1ab-214">In the list of tiles, click **SharePoint**.</span></span>

3. <span data-ttu-id="9e1ab-p111">	Dans le nouvel onglet *\*SharePoint** de votre navigateur, saisissez *\*ProjectX** dans la zone de recherche, puis activez la recherche. Vous devriez voir le message *\*Aucun résultat ne correspond à votre recherche.**</span><span class="sxs-lookup"><span data-stu-id="9e1ab-p111">On the new **SharePoint** tab in your browser, type **ProjectX** in the search box and then activate the search. You should see the message **Nothing here matches your search.**</span></span>

4. <span data-ttu-id="9e1ab-p112">À partir de l’instance ouverte du bloc-notes ou de votre éditeur de texte, copiez l’URL du site ProjectX dans la barre d’adresses de votre navigateur, puis appuyez sur **Entrée**. Vous devriez voir une page **Accès refusé**.</span><span class="sxs-lookup"><span data-stu-id="9e1ab-p112">From the open instance of Notepad or your text editor, copy the URL for the ProjectX site into the address bar of your browser and press **Enter**. You should see an **Access Denied** page.</span></span>

5. <span data-ttu-id="9e1ab-p113">À partir du bloc-notes ou votre éditeur de texte, copiez l’URL du dossier Documents ProjectX dans la barre d’adresses de votre navigateur, puis appuyez sur **Entrée**. Vous devriez voir une page **Accès refusé**.</span><span class="sxs-lookup"><span data-stu-id="9e1ab-p113">From Notepad or your text editor, copy the URL for the ProjectX Documents folder into the address bar of your browser and press **Enter**. You should see an **Access Denied** page.</span></span>

6. <span data-ttu-id="9e1ab-p114">À partir du bloc-notes ou votre éditeur de texte, copiez l’URL du fichier Documents.docx dans la barre d’adresses de votre navigateur, puis appuyez sur **Entrée**. Vous devriez voir une page **Accès refusé**.</span><span class="sxs-lookup"><span data-stu-id="9e1ab-p114">From Notepad or your text editor, copy the URL for the Documents.docx file into the address bar of your browser and press **Enter**. You should see an **Access Denied** page.</span></span>

7. <span data-ttu-id="9e1ab-223">Fermez l’onglet **SharePoint** de votre navigateur, cliquez sur l’onglet **Accueil Microsoft Office**, sur le nom **Utilisateur 3**, puis sur **Déconnexion**.</span><span class="sxs-lookup"><span data-stu-id="9e1ab-223">Close the **SharePoint** tab in your browser, click the **Microsoft Office Home** tab, click the **User 3** name, and then click **Sign out**.</span></span>

<span data-ttu-id="9e1ab-224">Votre site SharePoint Online isolé est maintenant prêt pour votre expérience supplémentaire.</span><span class="sxs-lookup"><span data-stu-id="9e1ab-224">Your isolated SharePoint Online site is now ready for your additional experimentation.</span></span>

## <a name="next-step"></a><span data-ttu-id="9e1ab-225">Étape suivante</span><span class="sxs-lookup"><span data-stu-id="9e1ab-225">Next Step</span></span>

<span data-ttu-id="9e1ab-226">Lorsque vous souhaitez déployer un site d'équipe SharePoint Online isolé en production, lisez la procédure détaillée dans la rubrique [Conception d'un site d'équipe SharePoint Online isolé](design-an-isolated-sharepoint-online-team-site.md).</span><span class="sxs-lookup"><span data-stu-id="9e1ab-226">When you are ready to deploy an isolated SharePoint Online team site in production, see the step-by-step design considerations in [Design an isolated SharePoint Online team site](design-an-isolated-sharepoint-online-team-site.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="9e1ab-227">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9e1ab-227">See Also</span></span>

[<span data-ttu-id="9e1ab-228">Sites d'équipe SharePoint Online isolés</span><span class="sxs-lookup"><span data-stu-id="9e1ab-228">Isolated SharePoint Online team sites</span></span>](isolated-sharepoint-online-team-sites.md)

[<span data-ttu-id="9e1ab-229">Guides de laboratoire de test d’adoption cloud</span><span class="sxs-lookup"><span data-stu-id="9e1ab-229">Cloud adoption Test Lab Guides (TLGs)</span></span>](https://docs.microsoft.com/office365/enterprise/cloud-adoption-test-lab-guides-tlgs)

[<span data-ttu-id="9e1ab-230">Environnement de développement/test de configuration de base</span><span class="sxs-lookup"><span data-stu-id="9e1ab-230">Base Configuration dev/test environment</span></span>](https://docs.microsoft.com/office365/enterprise/base-configuration-dev-test-environment)

[<span data-ttu-id="9e1ab-231">Environnement de développement/test Office 365</span><span class="sxs-lookup"><span data-stu-id="9e1ab-231">Office 365 dev/test environment</span></span>](https://docs.microsoft.com/office365/enterprise/office-365-dev-test-environment)

[<span data-ttu-id="9e1ab-232">Adoption du cloud et solutions hybrides</span><span class="sxs-lookup"><span data-stu-id="9e1ab-232">Cloud adoption and hybrid solutions</span></span>](https://docs.microsoft.com/office365/enterprise/cloud-adoption-and-hybrid-solutions)




