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
localization_priority: Normal
ms.collection: Ent_O365
ms.custom:
- TLG
- Ent_TLGs
ms.assetid: d1795031-beef-49ea-a6fc-5da5450d320d
description: 'Résumé : Configurez un site d’équipe SharePoint Online isolé du reste de l’organisation dans votre environnement de test/dev Microsoft 365.'
ms.technology: mdo
ms.prod: m365-security
ms.openlocfilehash: 103ba1ddb2b5123db80be91f40c4fce8c6e2eb3d
ms.sourcegitcommit: 786f90a163d34c02b8451d09aa1efb1e1d5f543c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/18/2021
ms.locfileid: "50286608"
---
# <a name="isolated-sharepoint-online-team-site-devtest-environment"></a><span data-ttu-id="5dfd9-103">Site d’équipe SharePoint Online isolé dans votre environnement de développement/test</span><span class="sxs-lookup"><span data-stu-id="5dfd9-103">Isolated SharePoint Online team site dev/test environment</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../includes/microsoft-defender-for-office.md)]

<span data-ttu-id="5dfd9-104">**S’applique à**</span><span class="sxs-lookup"><span data-stu-id="5dfd9-104">**Applies to**</span></span>
- [<span data-ttu-id="5dfd9-105">Exchange Online Protection</span><span class="sxs-lookup"><span data-stu-id="5dfd9-105">Exchange Online Protection</span></span>](exchange-online-protection-overview.md)
- [<span data-ttu-id="5dfd9-106">Microsoft Defender pour Office 365 (plan 1)</span><span class="sxs-lookup"><span data-stu-id="5dfd9-106">Microsoft Defender for Office 365 plan 1</span></span>](office-365-atp.md)
- <span data-ttu-id="5dfd9-107">SharePoint Online</span><span class="sxs-lookup"><span data-stu-id="5dfd9-107">SharePoint Online</span></span> 


 <span data-ttu-id="5dfd9-108">**Résumé :** Configurez un site d’équipe SharePoint Online isolé du reste de l’organisation dans votre environnement de test/dev Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="5dfd9-108">**Summary:** Configure a SharePoint Online team site that is isolated from the rest of the organization in your Microsoft 365 dev/test environment.</span></span>

<span data-ttu-id="5dfd9-109">Les sites d’équipe SharePoint Online dans Microsoft 365 sont des emplacements de collaboration à l’aide d’une bibliothèque de documents commune, d’un bloc-notes OneNote et d’autres services.</span><span class="sxs-lookup"><span data-stu-id="5dfd9-109">SharePoint Online team sites in Microsoft 365 are locations for collaboration using a common document library, a OneNote notebook, and other services.</span></span> <span data-ttu-id="5dfd9-110">Dans de nombreux cas, vous souhaitez bénéficier d’un large accès et d’une collaboration entre les départements ou organisations.</span><span class="sxs-lookup"><span data-stu-id="5dfd9-110">In many cases, you want wide access and collaboration across departments or organizations.</span></span> <span data-ttu-id="5dfd9-111">Toutefois, dans certains cas, vous souhaitez contrôler étroitement l’accès et les autorisations pour la collaboration entre un petit groupe de personnes.</span><span class="sxs-lookup"><span data-stu-id="5dfd9-111">However, in some cases, you want to tightly control the access and permissions for collaboration among a small group of people.</span></span>

<span data-ttu-id="5dfd9-112">L’accès aux sites d’équipe SharePoint Online et ce que les utilisateurs peuvent faire sont contrôlés par les groupes et les niveaux d’autorisation SharePoint.</span><span class="sxs-lookup"><span data-stu-id="5dfd9-112">Access to SharePoint Online team sites and what users can do is controlled by SharePoint groups and permission levels.</span></span> <span data-ttu-id="5dfd9-113">Par défaut, les sites SharePoint Online comportent trois niveaux d’accès :</span><span class="sxs-lookup"><span data-stu-id="5dfd9-113">By default, SharePoint Online sites have three levels of access:</span></span>

- <span data-ttu-id="5dfd9-114">Les **membres** peuvent afficher, créer et modifier des ressources sur le site.</span><span class="sxs-lookup"><span data-stu-id="5dfd9-114">**Members**, who can view, create, and modify resources on the site.</span></span>
- <span data-ttu-id="5dfd9-115">Les **propriétaires** ont un contrôle total sur le site, et peuvent même modifier les autorisations.</span><span class="sxs-lookup"><span data-stu-id="5dfd9-115">**Owners**, who have complete control of the site, including the ability to change permissions.</span></span>
- <span data-ttu-id="5dfd9-116">Les **Visiteurs** peuvent uniquement afficher les ressources du site.</span><span class="sxs-lookup"><span data-stu-id="5dfd9-116">**Visitors**, who only can view resources on the site.</span></span>

<span data-ttu-id="5dfd9-117">Cet article vous explique la configuration d’un site d’équipe SharePoint Online isolé pour un projet de recherche secret nommé ProjectX.</span><span class="sxs-lookup"><span data-stu-id="5dfd9-117">This article steps you through the configuration of an isolated SharePoint Online team site for a secret research project named ProjectX.</span></span> <span data-ttu-id="5dfd9-118">Les conditions d’accès requises sont les :</span><span class="sxs-lookup"><span data-stu-id="5dfd9-118">The access requirements are:</span></span>

- <span data-ttu-id="5dfd9-119">Seuls les membres du projet peuvent accéder au site et à son contenu (documents, bloc-notes OneNote, pages), avec des niveaux d’autorisation SharePoint pour éditer et afficher contrôlés via l’appartenance au groupe.</span><span class="sxs-lookup"><span data-stu-id="5dfd9-119">Only members of the project can access the site and its contents (documents, OneNote Notebook, Pages), with edit and view SharePoint permission levels controlled through group membership.</span></span>

- <span data-ttu-id="5dfd9-120">Seuls le créateur du site et les membres d’un groupe d’administrateurs du site peuvent effectuer l’administration du site, y compris la modification des autorisations au niveau du site.</span><span class="sxs-lookup"><span data-stu-id="5dfd9-120">Only the site creator and members of an Admins group for the site can perform site administration, which includes modifying site-level permissions.</span></span>

<span data-ttu-id="5dfd9-121">Il existe trois phases pour la configuration d’un site d’équipe SharePoint Online isolé dans votre environnement de développement/test Microsoft 365 :</span><span class="sxs-lookup"><span data-stu-id="5dfd9-121">There are three phases to setting up an isolated SharePoint Online team site in your Microsoft 365 dev/test environment:</span></span>

1. <span data-ttu-id="5dfd9-122">Créez l’environnement dev/test Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="5dfd9-122">Create the Microsoft 365 dev/test environment.</span></span>

2. <span data-ttu-id="5dfd9-123">Créez les utilisateurs et groupes pour ProjectX.</span><span class="sxs-lookup"><span data-stu-id="5dfd9-123">Create the users and groups for ProjectX.</span></span>

3. <span data-ttu-id="5dfd9-124">Créez un site d’équipe SharePoint Online ProjectX et isolez-le.</span><span class="sxs-lookup"><span data-stu-id="5dfd9-124">Create a new ProjectX SharePoint Online team site and isolate it.</span></span>

> [!TIP]
> <span data-ttu-id="5dfd9-125">Cliquez [ici](https://aka.ms/catlgstack) pour afficher le plan de tous les articles de l’ensemble de guides de laboratoire de test de One Microsoft Cloud.</span><span class="sxs-lookup"><span data-stu-id="5dfd9-125">Click [here](https://aka.ms/catlgstack) for a visual map to all the articles in the One Microsoft Cloud Test Lab Guide stack.</span></span>

## <a name="phase-1-build-out-your-lightweight-or-simulated-enterprise-microsoft-365-devtest-environment"></a><span data-ttu-id="5dfd9-126">Phase 1 : Créer votre environnement de développement/test Microsoft 365 d’entreprise léger ou simulé</span><span class="sxs-lookup"><span data-stu-id="5dfd9-126">Phase 1: Build out your lightweight or simulated enterprise Microsoft 365 dev/test environment</span></span>

<span data-ttu-id="5dfd9-127">Si vous souhaitez simplement créer un site d’équipe SharePoint Online isolé avec une configuration minimale requise, suivez les instructions des phases 2 et 3 de la configuration de [base légère.](../../enterprise/lightweight-base-configuration-microsoft-365-enterprise.md)</span><span class="sxs-lookup"><span data-stu-id="5dfd9-127">If you just want to create an isolated SharePoint Online team site in a lightweight way with the minimum requirements, follow the instructions in phases 2 and 3 of [The lightweight base configuration](../../enterprise/lightweight-base-configuration-microsoft-365-enterprise.md).</span></span>

<span data-ttu-id="5dfd9-128">Si vous souhaitez créer un site d’équipe SharePoint Online isolé dans une configuration d’entreprise simulée, suivez les instructions de la synchronisation de hachage de mot de passe pour votre environnement de [test Microsoft 365.](../../enterprise/password-hash-sync-m365-ent-test-environment.md)</span><span class="sxs-lookup"><span data-stu-id="5dfd9-128">If you want to create an isolated SharePoint Online team site in a simulated enterprise configuration, follow the instructions in [Password hash synchronization for your Microsoft 365 test environment](../../enterprise/password-hash-sync-m365-ent-test-environment.md).</span></span>

> [!NOTE]
> <span data-ttu-id="5dfd9-129">La création d’un site SharePoint Online isolé ne nécessite pas l’environnement de développement/test d’entreprise simulé, qui inclut un intranet simulé connecté à Internet et la synchronisation d’annuaires pour une forêt AD DS (Active Directory Domain Services).</span><span class="sxs-lookup"><span data-stu-id="5dfd9-129">Creating an isolated SharePoint Online site does not require the simulated enterprise dev/test environment, which includes a simulated intranet connected to the Internet and directory synchronization for a Active Directory Domain Services (AD DS) forest.</span></span> <span data-ttu-id="5dfd9-130">Il est proposé comme option dans cet article afin que vous puissiez tester un site SharePoint Online isolé et faire des essais dans un environnement qui représente une organisation classique.</span><span class="sxs-lookup"><span data-stu-id="5dfd9-130">It is provided here as an option so that you can test an isolated SharePoint Online site and experiment with it in an environment that represents a typical organization.</span></span>

## <a name="phase-2-create-user-accounts-and-access-groups"></a><span data-ttu-id="5dfd9-131">Phase 2 : Création de comptes d’utilisateurs et de groupes d’accès</span><span class="sxs-lookup"><span data-stu-id="5dfd9-131">Phase 2: Create user accounts and access groups</span></span>

<span data-ttu-id="5dfd9-132">Utilisez les instructions de connexion à [Office 365 PowerShell](../../enterprise/connect-to-microsoft-365-powershell.md) pour vous connecter à votre abonnement d’essai avec votre compte d’administrateur général à partir de :</span><span class="sxs-lookup"><span data-stu-id="5dfd9-132">Use the instructions in [Connect to Office 365 PowerShell](../../enterprise/connect-to-microsoft-365-powershell.md) to connect to your trial subscription with your global administrator account from:</span></span>

- <span data-ttu-id="5dfd9-133">Votre ordinateur (pour l’environnement dev/test Microsoft 365 léger).</span><span class="sxs-lookup"><span data-stu-id="5dfd9-133">Your computer (for the lightweight Microsoft 365 dev/test environment).</span></span>

- <span data-ttu-id="5dfd9-134">La machine virtuelle CLIENT1 (pour l’environnement de développement/test Microsoft 365 d’entreprise simulée).</span><span class="sxs-lookup"><span data-stu-id="5dfd9-134">The CLIENT1 virtual machine (for the simulated enterprise Microsoft 365 dev/test environment).</span></span>

<span data-ttu-id="5dfd9-135">Pour créer les groupes d’accès pour le site d’équipe SharePoint Online ProjectX, exécutez les commandes Windows Azure module Active Directory pour Windows PowerShell invite :</span><span class="sxs-lookup"><span data-stu-id="5dfd9-135">To create the new access groups for the ProjectX SharePoint Online team site, run these commands from the Windows Azure Active Directory Module for Windows PowerShell prompt:</span></span>

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

<span data-ttu-id="5dfd9-136">Entrez le nom de votre organisation (exemple : contosotoycompany) et le code de pays à deux caractères pour indiquer votre emplacement, puis exécutez les commandes suivantes à partir de l’invite Module Windows Azure Active Directory pour Windows PowerShell :</span><span class="sxs-lookup"><span data-stu-id="5dfd9-136">Fill in your organization name (example: contosotoycompany), the two-character country code for your location, and then run the following commands from the Windows Azure Active Directory Module for Windows PowerShell prompt:</span></span>

```powershell
$orgName="<organization name>"
$loc="<two-character country code, such as US>"
$licAssignment= $orgName + ":ENTERPRISEPREMIUM"
$userName= "designer@" + $orgName + ".onmicrosoft.com"
New-MsolUser -DisplayName "Lead Designer" -FirstName Lead -LastName Designer -UserPrincipalName $userName -UsageLocation $loc -LicenseAssignment $licAssignment -ForceChangePassword $false
```

<span data-ttu-id="5dfd9-137">À partir de la zone de la commande **New-MsolUser**, notez le mot de passe généré pour le compte Responsable de la conception et enregistrez-le dans un emplacement sécurisé.</span><span class="sxs-lookup"><span data-stu-id="5dfd9-137">From the display of the **New-MsolUser** command, note the generated password for the Lead Designer account and record it in a safe location.</span></span>

<span data-ttu-id="5dfd9-138">Exécutez les commandes suivantes à partir de l’invite Module Windows Azure Active Directory pour Windows PowerShell :</span><span class="sxs-lookup"><span data-stu-id="5dfd9-138">Run the following commands from the Windows Azure Active Directory Module for Windows PowerShell prompt:</span></span>

```powershell
$userName= "researcher@" + $orgName + ".onmicrosoft.com"
New-MsolUser -DisplayName "Lead Researcher" -FirstName Lead -LastName Researcher -UserPrincipalName $userName -UsageLocation $loc -LicenseAssignment $licAssignment -ForceChangePassword $false
```

<span data-ttu-id="5dfd9-139">À partir de la zone de la commande **New-MsolUser**, notez le mot de passe généré pour le compte Responsable de la recherche et enregistrez-le dans un emplacement sécurisé.</span><span class="sxs-lookup"><span data-stu-id="5dfd9-139">From the display of the **New-MsolUser** command, note the generated password for the Lead Researcher account and record it in a safe location.</span></span>

<span data-ttu-id="5dfd9-140">Exécutez les commandes suivantes à partir de l’invite Module Windows Azure Active Directory pour Windows PowerShell :</span><span class="sxs-lookup"><span data-stu-id="5dfd9-140">Run the following commands from the Windows Azure Active Directory Module for Windows PowerShell prompt:</span></span>

```powershell
$userName= "devvp@" + $orgName + ".onmicrosoft.com"
New-MsolUser -DisplayName "Development VP" -FirstName Development -LastName VP -UserPrincipalName $userName -UsageLocation $loc -LicenseAssignment $licAssignment -ForceChangePassword $false
```

<span data-ttu-id="5dfd9-141">À partir de la zone de la commande **New-MsolUser**, notez le mot de passe généré pour le compte VP du développement et enregistrez-le dans un emplacement sécurisé.</span><span class="sxs-lookup"><span data-stu-id="5dfd9-141">From the display of the **New-MsolUser** command, note the generated password for the Development VP account and record it in a safe location.</span></span>

<span data-ttu-id="5dfd9-142">Ensuite, pour ajouter les nouveaux comptes aux nouveaux groupes d’accès, exécutez ces commandes PowerShell à partir de l’invite Windows Azure Module Active Directory pour Windows PowerShell suivante :</span><span class="sxs-lookup"><span data-stu-id="5dfd9-142">Next, to add the new accounts to the new access groups, run these PowerShell commands from the Windows Azure Active Directory Module for Windows PowerShell prompt:</span></span>

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

<span data-ttu-id="5dfd9-143">Résultats :</span><span class="sxs-lookup"><span data-stu-id="5dfd9-143">Results:</span></span>

- <span data-ttu-id="5dfd9-144">Le groupe ProjectX-Members'accès au client contient les comptes d’utilisateur Responsable de la conception et Responsable de la recherche</span><span class="sxs-lookup"><span data-stu-id="5dfd9-144">The ProjectX-Members access group contains the Lead Designer and Lead Researcher user accounts</span></span>

- <span data-ttu-id="5dfd9-145">Le groupe ProjectX-Admins'accès au client contient le compte d’administrateur général de votre abonnement d’essai</span><span class="sxs-lookup"><span data-stu-id="5dfd9-145">The ProjectX-Admins access group contains the global administrator account for your trial subscription</span></span>

- <span data-ttu-id="5dfd9-146">Le groupe ProjectX-Viewers'accès au client contient le compte d’utilisateur VP de développement</span><span class="sxs-lookup"><span data-stu-id="5dfd9-146">The ProjectX-Viewers access group contains the Development VP user account</span></span>

<span data-ttu-id="5dfd9-147">La figure 1 montre les groupes d’accès et leur appartenance.</span><span class="sxs-lookup"><span data-stu-id="5dfd9-147">Figure 1 shows the access groups and their membership.</span></span>

<span data-ttu-id="5dfd9-148">**Figure 1**:</span><span class="sxs-lookup"><span data-stu-id="5dfd9-148">**Figure 1**:</span></span>

![Les groupes Microsoft 365 et leur appartenance à un site de groupe SharePoint Online isolé](../../media/5b7373b9-2a80-4880-afe5-63ffb17237e6.png)

## <a name="phase-3-create-a-new-projectx-sharepoint-online-team-site-and-isolate-it"></a><span data-ttu-id="5dfd9-150">Phase 3 : Créer un site d’équipe ProjectX SharePoint Online et l’isoler</span><span class="sxs-lookup"><span data-stu-id="5dfd9-150">Phase 3: Create a new ProjectX SharePoint Online team site and isolate it</span></span>

<span data-ttu-id="5dfd9-151">Pour créer un site d’équipe SharePoint Online pour ProjectX, vous pouvez :</span><span class="sxs-lookup"><span data-stu-id="5dfd9-151">To create a SharePoint Online team site for ProjectX, do the following:</span></span>

1. <span data-ttu-id="5dfd9-152">À l’aide d’un navigateur sur votre ordinateur local (configuration légère) ou sur CLIENT1 (configuration d’entreprise simulée), connectez-vous au Centre d’administration Microsoft 365 () à l’aide de votre compte d’administrateur <https://admin.microsoft.com> général.</span><span class="sxs-lookup"><span data-stu-id="5dfd9-152">Using a browser on either your local computer (lightweight configuration) or on CLIENT1 (simulated enterprise configuration), sign in to the Microsoft 365 admin center (<https://admin.microsoft.com>) using your global administrator account.</span></span>

2. <span data-ttu-id="5dfd9-153">Dans la liste des mosaïques, cliquez sur **SharePoint**.</span><span class="sxs-lookup"><span data-stu-id="5dfd9-153">In the list of tiles, click **SharePoint**.</span></span>

3. <span data-ttu-id="5dfd9-154">Dans le nouvel onglet SharePoint de votre navigateur, cliquez sur **+ Créer un site**.</span><span class="sxs-lookup"><span data-stu-id="5dfd9-154">On the new SharePoint tab in your browser, click **+ Create site**.</span></span>

4. <span data-ttu-id="5dfd9-155">Dans **Nom du site d’équipe**, saisissez **ProjectX**.</span><span class="sxs-lookup"><span data-stu-id="5dfd9-155">In **Team site name**, type **ProjectX**.</span></span> <span data-ttu-id="5dfd9-156">Dans **les paramètres de confidentialité,** **sélectionnez Privé - seuls les membres peuvent accéder à ce site.**</span><span class="sxs-lookup"><span data-stu-id="5dfd9-156">In **Privacy settings**, select **Private - only members can access this site**.</span></span>

5. <span data-ttu-id="5dfd9-157">Dans **Description du site d’équipe**, saisissez **Site SharePoint pour ProjectX**, puis cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="5dfd9-157">In **Team site description**, type **SharePoint site for ProjectX**, and then click **Next**.</span></span>

6. <span data-ttu-id="5dfd9-158">Dans le volet **Qui voulez-vous ajouter ?**, cliquez sur **Terminer**.</span><span class="sxs-lookup"><span data-stu-id="5dfd9-158">On the **Who do you want to add**? pane, click **Finish**.</span></span>

7. <span data-ttu-id="5dfd9-159">Dans le nouvel onglet **ProjectX-Accueil** de votre navigateur, dans la barre d’outils, cliquez sur l’icône des paramètres, puis sur **Autorisations du site**.</span><span class="sxs-lookup"><span data-stu-id="5dfd9-159">On the new **ProjectX-Home** tab in your browser, in the tool bar, click the settings icon, and then click **Site permissions**.</span></span>

8. <span data-ttu-id="5dfd9-160">Dans le volet **Autorisations du site**, cliquez sur **Paramètres d’autorisations avancés**.</span><span class="sxs-lookup"><span data-stu-id="5dfd9-160">In the **Site permissions** pane, click **Advanced permissions settings**.</span></span>

9. <span data-ttu-id="5dfd9-161">Dans le nouvel onglet **Autorisations : Projet X** de votre navigateur, cliquez sur **Paramètres de demande d’accès**.</span><span class="sxs-lookup"><span data-stu-id="5dfd9-161">In the new **Permissions: Project X** tab in your browser, click **Access Request Settings**.</span></span>

10. <span data-ttu-id="5dfd9-162">Dans la boîte de dialogue **Paramètres de demande d’accès**, désactivez les cases à cocher **Autoriser les membres à partager le site et les fichiers et dossiers individuels** et **Autoriser les demandes d’accès** (afin que les trois cases à cocher soient désactivées), puis cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="5dfd9-162">In the **Access Requests Settings** dialog box, clear **Allow members to share the site and individual files and folders** and **Allow access requests** (so that all three check boxes are cleared), and then click **OK**.</span></span>

11. <span data-ttu-id="5dfd9-163">Cliquez sur **Membres de ProjectX** dans la liste.</span><span class="sxs-lookup"><span data-stu-id="5dfd9-163">Click **ProjectX Members** in the list.</span></span>

12. <span data-ttu-id="5dfd9-164">Dans la page **Personnes et groupes**, cliquez sur **Nouveau**.</span><span class="sxs-lookup"><span data-stu-id="5dfd9-164">On the **People and Groups** page, click **New**.</span></span>

13. <span data-ttu-id="5dfd9-165">Dans la boîte de dialogue **Partager**, saisissez **ProjectX-Membres**, sélectionnez-le, puis cliquez sur **Partager**.</span><span class="sxs-lookup"><span data-stu-id="5dfd9-165">In the **Share** dialog box, type **ProjectX-Members**, select it, and then click **Share**.</span></span>

14. <span data-ttu-id="5dfd9-166">Cliquez sur le bouton de retour de votre navigateur.</span><span class="sxs-lookup"><span data-stu-id="5dfd9-166">Click the back button on your browser.</span></span>

15. <span data-ttu-id="5dfd9-167">Cliquez sur **Propriétaires de ProjectX** dans la liste.</span><span class="sxs-lookup"><span data-stu-id="5dfd9-167">Click **ProjectX Owners** in the list.</span></span>

16. <span data-ttu-id="5dfd9-168">Dans la page **Personnes et groupes**, cliquez sur **Nouveau**.</span><span class="sxs-lookup"><span data-stu-id="5dfd9-168">On the **People and Groups** page, click **New**.</span></span>

17. <span data-ttu-id="5dfd9-169">Dans la boîte de dialogue **Partager**, saisissez **ProjectX-Administrateurs**, sélectionnez-le, puis cliquez sur **Partager**.</span><span class="sxs-lookup"><span data-stu-id="5dfd9-169">In the **Share** dialog box, type **ProjectX-Admins**, select it, and then click **Share**.</span></span>

18. <span data-ttu-id="5dfd9-170">Cliquez sur le bouton de retour de votre navigateur.</span><span class="sxs-lookup"><span data-stu-id="5dfd9-170">Click the back button on your browser.</span></span>

19. <span data-ttu-id="5dfd9-171">Cliquez sur **Visiteurs de ProjectX** dans la liste.</span><span class="sxs-lookup"><span data-stu-id="5dfd9-171">Click **ProjectX Visitors** in the list.</span></span>

20. <span data-ttu-id="5dfd9-172">Dans la page **Personnes et groupes**, cliquez sur **Nouveau**.</span><span class="sxs-lookup"><span data-stu-id="5dfd9-172">On the **People and Groups** page, click **New**.</span></span>

21. <span data-ttu-id="5dfd9-173">Dans la boîte de dialogue **Partager**, saisissez **ProjectX-Utilisateurs**, sélectionnez-le, puis cliquez sur **Partager**.</span><span class="sxs-lookup"><span data-stu-id="5dfd9-173">In the **Share** dialog box, type **ProjectX-Viewers**, select it, and then click **Share**.</span></span>

22. <span data-ttu-id="5dfd9-174">Fermez l’onglet **Personnes et groupes** de votre navigateur, cliquez sur l’onglet **ProjectX-Accueil** de votre navigateur, puis fermez le volet **Autorisations du site**.</span><span class="sxs-lookup"><span data-stu-id="5dfd9-174">Close the **People and Groups** tab in your browser, click the **ProjectX-Home** tab in your browser, and then close the **Site permissions** pane.</span></span>

<span data-ttu-id="5dfd9-175">Voici les résultats de la configuration des autorisations :</span><span class="sxs-lookup"><span data-stu-id="5dfd9-175">Here are the results of configuring permissions:</span></span>

- <span data-ttu-id="5dfd9-176">Le groupe SharePoint Membres ProjectX contient uniquement le groupe d’accès ProjectX-Members (qui contient uniquement les comptes d’utilisateur Responsable de la conception et Responsable de la recherche) et le groupe ProjectX (qui contient uniquement le compte d’utilisateur Administrateur général).</span><span class="sxs-lookup"><span data-stu-id="5dfd9-176">The ProjectX Members SharePoint group contains only the ProjectX-Members access group (which contains only the Lead Designer and Lead Researcher user accounts) and the ProjectX group (which contains only the global administrator user account).</span></span>

- <span data-ttu-id="5dfd9-177">Le groupe SharePoint Propriétaires ProjectX contient uniquement le groupe ProjectX-Admins d’accès principal (qui contient uniquement le compte d’utilisateur Administrateur général).</span><span class="sxs-lookup"><span data-stu-id="5dfd9-177">The ProjectX Owners SharePoint group contains only the ProjectX-Admins access group (which contains only the global administrator user account).</span></span>

- <span data-ttu-id="5dfd9-178">Le groupe SharePoint Visiteurs ProjectX contient uniquement le ProjectX-Viewers d’accès principal (qui contient uniquement le compte d’utilisateur VP de développement).</span><span class="sxs-lookup"><span data-stu-id="5dfd9-178">The ProjectX Visitors SharePoint group contains only the ProjectX-Viewers access group (which contains only the Development VP user account).</span></span>

- <span data-ttu-id="5dfd9-179">Les membres ne peuvent pas modifier les autorisations au niveau du site (cette opération peut être uniquement effectuée par les membres du groupe ProjectX-Administrateurs).</span><span class="sxs-lookup"><span data-stu-id="5dfd9-179">Members cannot modify site-level permissions (this can only be done by members of the ProjectX-Admins group).</span></span>

- <span data-ttu-id="5dfd9-180">Les autres comptes d’utilisateurs ne peuvent pas accéder au site ni à ses ressources, ni demander l’accès au site.</span><span class="sxs-lookup"><span data-stu-id="5dfd9-180">Other user accounts cannot access the site or its resources or request access to the site.</span></span>

<span data-ttu-id="5dfd9-181">La figure 2 présente les groupes SharePoint et leur appartenance.</span><span class="sxs-lookup"><span data-stu-id="5dfd9-181">Figure 2 shows the SharePoint groups and their membership.</span></span>

<span data-ttu-id="5dfd9-182">**Figure 2**</span><span class="sxs-lookup"><span data-stu-id="5dfd9-182">**Figure 2**</span></span>

![Les groupes SharePoint Online et leur appartenance à un site de groupe SharePoint Online isolé](../../media/595abff4-64f9-49de-a37a-c70c6856936b.png)

<span data-ttu-id="5dfd9-184">Maintenant, nous allons montrer l’accès à l’aide du compte d’utilisateur Concepteur de lead :</span><span class="sxs-lookup"><span data-stu-id="5dfd9-184">Now let's demonstrate access using the Lead Designer user account:</span></span>

1. <span data-ttu-id="5dfd9-185">Fermez l’onglet **ProjectX-Accueil** dans votre navigateur, puis cliquez sur l’onglet **Accueil Microsoft Office** du navigateur.</span><span class="sxs-lookup"><span data-stu-id="5dfd9-185">Close the **ProjectX-Home** tab in your browser, and then click the **Microsoft Office Home** tab in your browser.</span></span>

2. <span data-ttu-id="5dfd9-186">Cliquez sur le nom de votre administrateur général, puis cliquez sur **Déconnexion**.</span><span class="sxs-lookup"><span data-stu-id="5dfd9-186">Click the name of your global administrator, and then click **Sign out**.</span></span>

3. <span data-ttu-id="5dfd9-187">Connectez-vous au Centre d’administration Microsoft 365 ( ) à l’aide du nom de compte Responsable de la conception <https://admin.microsoft.com> et de son mot de passe.</span><span class="sxs-lookup"><span data-stu-id="5dfd9-187">Sign in to the Microsoft 365 admin center (<https://admin.microsoft.com>) using the Lead Designer account name and its password.</span></span>

4. <span data-ttu-id="5dfd9-188">Dans la liste des vignettes, cliquez sur **SharePoint**.</span><span class="sxs-lookup"><span data-stu-id="5dfd9-188">In the list of tiles, click **SharePoint**.</span></span>

5. <span data-ttu-id="5dfd9-189">Sous le nouvel **onglet SharePoint** de votre navigateur, tapez **ProjectX** dans la zone de recherche, activez la recherche, puis cliquez sur le site d’équipe **ProjectX.**</span><span class="sxs-lookup"><span data-stu-id="5dfd9-189">On the new **SharePoint** tab in your browser, type **ProjectX** in the search box, activate the search, and then click the **ProjectX** team site.</span></span> <span data-ttu-id="5dfd9-190">Vous devriez voir un nouvel onglet dans votre navigateur pour le site d’équipe ProjectX.</span><span class="sxs-lookup"><span data-stu-id="5dfd9-190">You should see a new tab in your browser for the ProjectX team site.</span></span>

6. <span data-ttu-id="5dfd9-p107">Cliquez sur l’icône des paramètres. Notez qu’il n’existe pas d’option pour **Autorisations du site**. Cela est correct puisque seuls les membres du groupe ProjectX-Administrateurs peuvent modifier les autorisations sur le site</span><span class="sxs-lookup"><span data-stu-id="5dfd9-p107">Click the settings icon. Notice that there is no option for **Site Permissions**. This is correct because only the members of the ProjectX-Admins group can modify permissions on the site</span></span>

7. <span data-ttu-id="5dfd9-194">Ouvrez le bloc-notes ou un éditeur de texte de votre choix.</span><span class="sxs-lookup"><span data-stu-id="5dfd9-194">Open Notepad or a text editor of your choice.</span></span>

8. <span data-ttu-id="5dfd9-195">Copiez l’URL du site d’équipe ProjectX et collez-la sur une nouvelle ligne dans le Bloc-notes ou dans votre éditeur de texte.</span><span class="sxs-lookup"><span data-stu-id="5dfd9-195">Copy the URL of the ProjectX team site and paste it on a new line in Notepad or your text editor.</span></span>

9. <span data-ttu-id="5dfd9-196">Dans le nouvel onglet **ProjectX-Accueil** de votre navigateur, cliquez sur **Documents**.</span><span class="sxs-lookup"><span data-stu-id="5dfd9-196">On the new **ProjectX-Home** tab in your browser, click **Documents**.</span></span>

10. <span data-ttu-id="5dfd9-197">Copiez l’URL du dossier de documents ProjectX et collez-la dans une nouvelle ligne dans le bloc-notes ou dans votre éditeur de texte.</span><span class="sxs-lookup"><span data-stu-id="5dfd9-197">Copy the URL of the ProjectX documents folder and paste it on a new line in Notepad or your text editor.</span></span>

11. <span data-ttu-id="5dfd9-198">Dans le nouvel onglet **ProjectX-Documents** de votre navigateur, cliquez sur **Nouveau > Document Word**.</span><span class="sxs-lookup"><span data-stu-id="5dfd9-198">On the new **ProjectX-Documents** tab in your browser, click **New > Word document**.</span></span>

12. <span data-ttu-id="5dfd9-199">Tapez du texte sur la page, attendez que l’état indique **Enregistré,** cliquez sur le bouton Retour de votre navigateur, puis actualisez la page.</span><span class="sxs-lookup"><span data-stu-id="5dfd9-199">Type some text on the page, wait for the status to indicate **Saved**, click the back button on your browser, and then refresh the page.</span></span> <span data-ttu-id="5dfd9-200">Vous devriez voir un nouveau **Document.docx** dans le dossier **Documents**.</span><span class="sxs-lookup"><span data-stu-id="5dfd9-200">You should see a new **Document.docx** in the **Documents** folder.</span></span>

13. <span data-ttu-id="5dfd9-201">Cliquez sur les points de suspension du document **Document.docx**, puis sur **Obtenir un lien**.</span><span class="sxs-lookup"><span data-stu-id="5dfd9-201">Click the ellipsis for the **Document.docx** document, and then click **Get a link**.</span></span>

14. <span data-ttu-id="5dfd9-202">Copiez l’URL dans la boîte de dialogue Partager « **Document.docx** » et collez-la sur une nouvelle ligne dans le Bloc-notes ou dans votre éditeur de texte, puis fermez la boîte de dialogue Partager « **Document.docx** ».</span><span class="sxs-lookup"><span data-stu-id="5dfd9-202">Copy the URL in the **Share 'Document.docx'** dialog box and paste it on a new line in Notepad or your text editor, and then close the **Share 'Document.docx'** dialog box.</span></span>

15. <span data-ttu-id="5dfd9-203">Fermez les onglets **ProjectX-Documents** et **SharePoint** dans votre navigateur, puis cliquez sur l’onglet **Accueil Microsoft Office**.</span><span class="sxs-lookup"><span data-stu-id="5dfd9-203">Close the **ProjectX-Documents** and **SharePoint** tabs in your browser, and then click the **Microsoft Office Home** tab.</span></span>

16. <span data-ttu-id="5dfd9-204">Cliquez sur le nom **Responsable de la conception**, puis cliquez sur **Déconnexion**.</span><span class="sxs-lookup"><span data-stu-id="5dfd9-204">Click the **Lead Designer** name, and then click **Sign out**.</span></span>

<span data-ttu-id="5dfd9-205">Maintenant, nous allons montrer l’accès à l’aide du compte d’utilisateur VP de développement :</span><span class="sxs-lookup"><span data-stu-id="5dfd9-205">Now let's demonstrate access using the Development VP user account:</span></span>

1. <span data-ttu-id="5dfd9-206">Connectez-vous au Centre d’administration Microsoft 365 ( ) à l’aide du nom du compte VP de <https://admin.microsoft.com> développement et de son mot de passe.</span><span class="sxs-lookup"><span data-stu-id="5dfd9-206">Sign in to the Microsoft 365 admin center (<https://admin.microsoft.com>) using the Development VP account name and its password.</span></span>

2. <span data-ttu-id="5dfd9-207">Dans la liste des vignettes, cliquez sur **SharePoint**.</span><span class="sxs-lookup"><span data-stu-id="5dfd9-207">In the list of tiles, click **SharePoint**.</span></span>

3. <span data-ttu-id="5dfd9-208">Sous le nouvel **onglet SharePoint** de votre navigateur, tapez **ProjectX** dans la zone de recherche, activez la recherche, puis cliquez sur le site d’équipe **ProjectX.**</span><span class="sxs-lookup"><span data-stu-id="5dfd9-208">On the new **SharePoint** tab in your browser, type **ProjectX** in the search box, activate the search, and then click the **ProjectX** team site.</span></span> <span data-ttu-id="5dfd9-209">Vous devriez voir un nouvel onglet dans votre navigateur pour le site d’équipe ProjectX.</span><span class="sxs-lookup"><span data-stu-id="5dfd9-209">You should see a new tab in your browser for the ProjectX team site.</span></span>

4. <span data-ttu-id="5dfd9-210">Cliquez sur **Documents**, puis sur le fichier **Document.docx**.</span><span class="sxs-lookup"><span data-stu-id="5dfd9-210">Click **Documents**, and then click the **Document.docx** file.</span></span>

5. <span data-ttu-id="5dfd9-p110">Dans l’onglet **Document.docx** de votre navigateur, essayez de modifier le texte. Vous devriez voir un message indiquant **Ce document est en lecture seule.** Ceci est dû au fait que le compte d’utilisateur VP du développement comporte seulement des autorisations d’affichage pour le site.</span><span class="sxs-lookup"><span data-stu-id="5dfd9-p110">In the **Document.docx** tab in your browser, try to modify the text. You should see a message stating **This document is read-only.** This is expected because the Development VP user account only has view permissions for the site.</span></span>

6. <span data-ttu-id="5dfd9-214">Fermer les onglets **Document.docx**, **ProjectX-Documents** et **SharePoint** de votre navigateur.</span><span class="sxs-lookup"><span data-stu-id="5dfd9-214">Close the **Document.docx**, **ProjectX-Documents**, and **SharePoint** tabs in your browser.</span></span>

7. <span data-ttu-id="5dfd9-215">Cliquez sur l’onglet **Accueil Microsoft Office**, sur le nom **VP du développement**, puis sur **Déconnexion**.</span><span class="sxs-lookup"><span data-stu-id="5dfd9-215">Click the **Microsoft Office Home** tab, click the **Development VP** name, and then click **Sign out**.</span></span>

<span data-ttu-id="5dfd9-216">Maintenant, nous allons montrer l’accès avec un compte d’utilisateur qui n’a pas d’autorisations :</span><span class="sxs-lookup"><span data-stu-id="5dfd9-216">Now let's demonstrate access with a user account that has no permissions:</span></span>

1. <span data-ttu-id="5dfd9-217">Connectez-vous au Centre d’administration Microsoft 365 ( ) à l’aide du nom de <https://admin.microsoft.com> compte Utilisateur 3 et de son mot de passe.</span><span class="sxs-lookup"><span data-stu-id="5dfd9-217">Sign in to the Microsoft 365 admin center (<https://admin.microsoft.com>) using the User 3 account name and its password.</span></span>

2. <span data-ttu-id="5dfd9-218">Dans la liste des mosaïques, cliquez sur **SharePoint**.</span><span class="sxs-lookup"><span data-stu-id="5dfd9-218">In the list of tiles, click **SharePoint**.</span></span>

3. <span data-ttu-id="5dfd9-p111">	Dans le nouvel onglet *\*SharePoint** de votre navigateur, saisissez *\*ProjectX** dans la zone de recherche, puis activez la recherche. Vous devriez voir le message *\*Aucun résultat ne correspond à votre recherche.**</span><span class="sxs-lookup"><span data-stu-id="5dfd9-p111">On the new **SharePoint** tab in your browser, type **ProjectX** in the search box and then activate the search. You should see the message **Nothing here matches your search.**</span></span>

4. <span data-ttu-id="5dfd9-p112">À partir de l’instance ouverte du bloc-notes ou de votre éditeur de texte, copiez l’URL du site ProjectX dans la barre d’adresses de votre navigateur, puis appuyez sur **Entrée**. Vous devriez voir une page **Accès refusé**.</span><span class="sxs-lookup"><span data-stu-id="5dfd9-p112">From the open instance of Notepad or your text editor, copy the URL for the ProjectX site into the address bar of your browser and press **Enter**. You should see an **Access Denied** page.</span></span>

5. <span data-ttu-id="5dfd9-p113">À partir du bloc-notes ou votre éditeur de texte, copiez l’URL du dossier Documents ProjectX dans la barre d’adresses de votre navigateur, puis appuyez sur **Entrée**. Vous devriez voir une page **Accès refusé**.</span><span class="sxs-lookup"><span data-stu-id="5dfd9-p113">From Notepad or your text editor, copy the URL for the ProjectX Documents folder into the address bar of your browser and press **Enter**. You should see an **Access Denied** page.</span></span>

6. <span data-ttu-id="5dfd9-p114">À partir du bloc-notes ou votre éditeur de texte, copiez l’URL du fichier Documents.docx dans la barre d’adresses de votre navigateur, puis appuyez sur **Entrée**. Vous devriez voir une page **Accès refusé**.</span><span class="sxs-lookup"><span data-stu-id="5dfd9-p114">From Notepad or your text editor, copy the URL for the Documents.docx file into the address bar of your browser and press **Enter**. You should see an **Access Denied** page.</span></span>

7. <span data-ttu-id="5dfd9-227">Fermez l’onglet **SharePoint** de votre navigateur, cliquez sur l’onglet **Accueil Microsoft Office**, sur le nom **Utilisateur 3**, puis sur **Déconnexion**.</span><span class="sxs-lookup"><span data-stu-id="5dfd9-227">Close the **SharePoint** tab in your browser, click the **Microsoft Office Home** tab, click the **User 3** name, and then click **Sign out**.</span></span>

<span data-ttu-id="5dfd9-228">Votre site SharePoint Online isolé est maintenant prêt pour votre expérimentation supplémentaire.</span><span class="sxs-lookup"><span data-stu-id="5dfd9-228">Your isolated SharePoint Online site is now ready for your additional experimentation.</span></span>

## <a name="next-step"></a><span data-ttu-id="5dfd9-229">Étape suivante</span><span class="sxs-lookup"><span data-stu-id="5dfd9-229">Next Step</span></span>

<span data-ttu-id="5dfd9-230">Lorsque vous souhaitez déployer un site d'équipe SharePoint Online isolé en production, lisez la procédure détaillée dans la rubrique [Conception d'un site d'équipe SharePoint Online isolé](design-an-isolated-sharepoint-online-team-site.md).</span><span class="sxs-lookup"><span data-stu-id="5dfd9-230">When you are ready to deploy an isolated SharePoint Online team site in production, see the step-by-step design considerations in [Design an isolated SharePoint Online team site](design-an-isolated-sharepoint-online-team-site.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="5dfd9-231">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5dfd9-231">See Also</span></span>

[<span data-ttu-id="5dfd9-232">Sites d'équipe SharePoint Online isolés</span><span class="sxs-lookup"><span data-stu-id="5dfd9-232">Isolated SharePoint Online team sites</span></span>](isolated-sharepoint-online-team-sites.md)

[<span data-ttu-id="5dfd9-233">Guides de laboratoire de test d’adoption cloud</span><span class="sxs-lookup"><span data-stu-id="5dfd9-233">Cloud adoption Test Lab Guides (TLGs)</span></span>](../../enterprise/cloud-adoption-test-lab-guides-tlgs.md)

[<span data-ttu-id="5dfd9-234">Configuration de base d’entreprise simulée</span><span class="sxs-lookup"><span data-stu-id="5dfd9-234">The simulated enterprise base configuration</span></span>](../../enterprise/simulated-ent-base-configuration-microsoft-365-enterprise.md)

[<span data-ttu-id="5dfd9-235">Configuration de base légère</span><span class="sxs-lookup"><span data-stu-id="5dfd9-235">The lightweight base configuration</span></span>](../../enterprise/lightweight-base-configuration-microsoft-365-enterprise.md)

[<span data-ttu-id="5dfd9-236">Centre de solutions et d'architecture Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="5dfd9-236">Microsoft 365 solution and architecture center</span></span>](../../solutions/index.yml)