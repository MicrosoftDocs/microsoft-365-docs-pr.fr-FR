---
title: Sécuriser les fichiers Teams dans un environnement de développement/test
f1.keywords:
- NOCSH
ms.author: josephd
author: JoeDavies-MSFT
manager: laurawi
ms.date: 10/31/2019
audience: ITPro
ms.topic: article
ms.collection:
- Ent_O365
- Strat_O365_Enterprise
ms.service: O365-seccomp
localization_priority: Priority
search.appverid:
- MET150
ms.assetid: 06af70f3-e7dc-4ee2-a385-fb4d61a5e93b
description: 'Résumé : créez des équipes d’équipes Sensible et Hautement confidentiel dans Microsoft Teams pour les fichiers dans un environnement de développement/test.'
ms.openlocfilehash: 7af36e5a3af94297124c6f03cdead514ac941e5b
ms.sourcegitcommit: 3dd9944a6070a7f35c4bc2b57df397f844c3fe79
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/15/2020
ms.locfileid: "42082255"
---
# <a name="secure-teams-for-files-in-a-devtest-environment"></a><span data-ttu-id="bf46a-103">Sécuriser les fichiers Teams dans un environnement de développement/test</span><span class="sxs-lookup"><span data-stu-id="bf46a-103">Secure Teams for files in a dev/test environment</span></span>

<span data-ttu-id="bf46a-104">Cet article fournit des instructions détaillées pour créer un environnement de développement/test qui inclut les équipes sensibles et hautement confidentielles pour la solution [Sécuriser les fichiers dans Microsoft Teams](secure-files-in-teams.md).</span><span class="sxs-lookup"><span data-stu-id="bf46a-104">This article provides step-by-step instructions to create a dev/test environment that includes the sensitive and highly confidential teams for the [Secure files in Microsoft Teams](secure-files-in-teams.md) solution.</span></span>
  
![Équipes Sensibles et Hautement confidentielles dans Microsoft Teams pour les fichiers.](../../media/sensitive-highly-confidential-teams-dev-test.png)
  
<span data-ttu-id="bf46a-106">Utilisez cet environnement de développement/test pour expérimenter et affiner les paramètres de vos besoins spécifiques avant de déployer ces types d’équipes en production.</span><span class="sxs-lookup"><span data-stu-id="bf46a-106">Use this dev/test environment to experiment and fine-tune settings for your specific needs before deploying these types of teams in production.</span></span>
  
## <a name="phase-1-build-out-your-microsoft-365-enterprise-test-environment"></a><span data-ttu-id="bf46a-107">Phase 1 : Créer l’environnement de test Microsoft 365 Entreprise.</span><span class="sxs-lookup"><span data-stu-id="bf46a-107">Phase 1: Build out your Microsoft 365 Enterprise test environment</span></span>

<span data-ttu-id="bf46a-108">Si vous souhaitez simplement tester les équipes sensibles et hautement confidentielles de manière rapide avec une configuration minimale, suivez les instructions de [Configuration de base](https://docs.microsoft.com/microsoft-365/enterprise/lightweight-base-configuration-microsoft-365-enterprise).</span><span class="sxs-lookup"><span data-stu-id="bf46a-108">If you just want to test sensitive and highly confidential teams in a lightweight way with the minimum requirements, follow the instructions in [Lightweight base configuration](https://docs.microsoft.com/microsoft-365/enterprise/lightweight-base-configuration-microsoft-365-enterprise).</span></span>

<span data-ttu-id="bf46a-109">Si vous voulez tester les équipes sensibles et hautement confidentielles au sein d’une entreprise simulée, suivez les instructions de [Synchronisation de hachage de mot de passe](https://docs.microsoft.com/microsoft-365/enterprise/password-hash-sync-m365-ent-test-environment).</span><span class="sxs-lookup"><span data-stu-id="bf46a-109">If you want to test sensitive and highly confidential teams in a simulated enterprise, follow the instructions in [Password hash synchronization](https://docs.microsoft.com/microsoft-365/enterprise/password-hash-sync-m365-ent-test-environment).</span></span>

>[!Note]
><span data-ttu-id="bf46a-110">Tester les équipes sensibles et hautement confidentielles ne requiert pas d’environnement de test en entreprise simulée, qui utilise un intranet simulé connecté à Internet et la synchronisation d’annuaire pour une forêt Active Directory. Domain Services (AD DS).</span><span class="sxs-lookup"><span data-stu-id="bf46a-110">Testing sensitive and highly confidential teams does not require the simulated enterprise test environment, which includes a simulated intranet connected to the Internet and directory synchronization for an Active Directory Domain Services (AD DS) forest.</span></span> <span data-ttu-id="bf46a-111">Ceci est proposé comme option dans cet article afin que vous puissiez tester les équipes sensibles et hautement confidentielles et faire des essais dans un environnement qui représente une organisation classique.</span><span class="sxs-lookup"><span data-stu-id="bf46a-111">It is provided here as an option so that you can test sensitive and highly confidential teams and experiment with it in an environment that represents a typical organization.</span></span>
>
    
## <a name="phase-2-create-and-configure-your-azure-active-directory-ad-groups-and-users"></a><span data-ttu-id="bf46a-112">Phase 2 : Création et configuration de vos groupes et utilisateurs Azure Active Directory (AD)</span><span class="sxs-lookup"><span data-stu-id="bf46a-112">Phase 2: Create and configure your Azure Active Directory (AD) groups and users</span></span>

<span data-ttu-id="bf46a-113">Dans cette phase, vous créez et vous configurez les groupes et les utilisateurs Azure AD de votre organisation fictive.</span><span class="sxs-lookup"><span data-stu-id="bf46a-113">In this phase, you create and configure the Azure AD groups and users for your fictional organization.</span></span>
  
<span data-ttu-id="bf46a-114">Commencez par créer deux groupes pour une organisation standard avec le portail Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="bf46a-114">First, create two groups for a typical organization with the Azure portal.</span></span>
  
1. <span data-ttu-id="bf46a-115">Créez un onglet distinct dans votre navigateur, puis accédez au portail Microsoft Azure sous [https://portal.azure.com](https://portal.azure.com).</span><span class="sxs-lookup"><span data-stu-id="bf46a-115">Create a separate tab in your browser, and then go to the Azure portal at [https://portal.azure.com](https://portal.azure.com).</span></span> <span data-ttu-id="bf46a-116">Si nécessaire, connectez-vous avec les informations d’identification du compte d’administrateur général de votre abonnement ou essai Microsoft 365 E5.</span><span class="sxs-lookup"><span data-stu-id="bf46a-116">If needed, sign in with the credentials of the global administrator account for your Microsoft 365 E5 trial or paid subscription.</span></span>
    
2. <span data-ttu-id="bf46a-117">Dans le portail Azure, cliquez sur **Azure Active Directory > Groupes**.</span><span class="sxs-lookup"><span data-stu-id="bf46a-117">In the Azure portal, click **Azure Active Directory > Groups**.</span></span>
    
3. <span data-ttu-id="bf46a-118">Dans le panneau **Groupes - Tous les groupes**, cliquez sur **+ Nouveau groupe**.</span><span class="sxs-lookup"><span data-stu-id="bf46a-118">On the **Groups - All groups** blade, click **+ New group**.</span></span>
    
4. <span data-ttu-id="bf46a-119">Dans le panneau **Groupe** :</span><span class="sxs-lookup"><span data-stu-id="bf46a-119">On the **Group** blade:</span></span>
    
  - <span data-ttu-id="bf46a-120">Sélectionnez **Sécurité** dans **Type de groupe**.</span><span class="sxs-lookup"><span data-stu-id="bf46a-120">Select **Security** in **Group type**.</span></span>
    
  - <span data-ttu-id="bf46a-121">Tapez **C-Suite** dans le champ **Nom**.</span><span class="sxs-lookup"><span data-stu-id="bf46a-121">Type **C-Suite** in **Name**.</span></span>
    
  - <span data-ttu-id="bf46a-122">Sélectionnez **Affecté** dans le champ **Type d’appartenance**.</span><span class="sxs-lookup"><span data-stu-id="bf46a-122">Select **Assigned** in **Membership type**.</span></span>
      
5. <span data-ttu-id="bf46a-123">Cliquez sur **Créer** et fermez le panneau **Groupe**.</span><span class="sxs-lookup"><span data-stu-id="bf46a-123">Click **Create**, and then close the **Group** blade.</span></span>
    
6.  <span data-ttu-id="bf46a-124">Répétez les étapes 3–5 pour un nouveau groupe appelé **Équipe marketing**.</span><span class="sxs-lookup"><span data-stu-id="bf46a-124">Repeat steps 3-5 for a new group named **Marketing staff**.</span></span>
    
<span data-ttu-id="bf46a-125">Ensuite, configurez l’octroi de licence automatique afin que des licences soient automatiquement attribuées aux membres de vos groupes pour les abonnements Office 365 et EMS.</span><span class="sxs-lookup"><span data-stu-id="bf46a-125">Next, you configure automatic licensing so that members of your groups are automatically assigned licenses for your Office 365 and EMS subscriptions.</span></span>
  
1. <span data-ttu-id="bf46a-126">Dans le portail Azure, cliquez sur **Azure Active Directory > Licences > Tous les produits**.</span><span class="sxs-lookup"><span data-stu-id="bf46a-126">In the Azure portal, click **Azure Active Directory > Licenses > All products**.</span></span>
    
2. <span data-ttu-id="bf46a-127">Dans la liste, sélectionnez **Microsoft 365 Entreprise E5**, puis cliquez sur **Attribuer**.</span><span class="sxs-lookup"><span data-stu-id="bf46a-127">In the list, select **Microsoft 365 Enterprise E5**, and then click **Assign**.</span></span>
    
3. <span data-ttu-id="bf46a-128">Dans le panneau **Affecter une licence**, cliquez sur **Utilisateurs et groupes**.</span><span class="sxs-lookup"><span data-stu-id="bf46a-128">In the **Assign license** blade, click **Users and groups**.</span></span>
    
4. <span data-ttu-id="bf46a-129">Dans la liste des groupes, sélectionnez les éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="bf46a-129">In the list of groups, select the following:</span></span>
    
  - <span data-ttu-id="bf46a-130">C-Suite</span><span class="sxs-lookup"><span data-stu-id="bf46a-130">C-Suite</span></span>
    
  - <span data-ttu-id="bf46a-131">Équipe Marketing</span><span class="sxs-lookup"><span data-stu-id="bf46a-131">Marketing staff</span></span>
    
5. <span data-ttu-id="bf46a-132">Cliquez sur **Sélectionner**, puis sur **Affecter**.</span><span class="sxs-lookup"><span data-stu-id="bf46a-132">Click **Select**, and then click **Assign**.</span></span>
    
6. <span data-ttu-id="bf46a-133">Fermez l’onglet du portail Azure dans votre navigateur.</span><span class="sxs-lookup"><span data-stu-id="bf46a-133">Close the Azure portal tab in your browser.</span></span>
    
<span data-ttu-id="bf46a-134">Ensuite, [connectez -vous au module PowerShell Azure Active Directory pour le module Graphique](https://docs.microsoft.com/office365/enterprise/powershell/connect-to-office-365-powershell#connect-with-the-azure-active-directory-powershell-for-graph-module).</span><span class="sxs-lookup"><span data-stu-id="bf46a-134">Next, you [Connect with the Azure Active Directory PowerShell for Graph module ](https://docs.microsoft.com/office365/enterprise/powershell/connect-to-office-365-powershell#connect-with-the-azure-active-directory-powershell-for-graph-module).</span></span>
  
<span data-ttu-id="bf46a-135">Renseignez le nom de votre organisation, votre emplacement et un mot de passe commun, puis exécutez les commandes suivantes à partir de l’invite de commandes PowerShell ou de l’environnement de script intégré (ISE) pour créer des comptes d’utilisateur et les ajouter à leurs groupes :</span><span class="sxs-lookup"><span data-stu-id="bf46a-135">Fill in your organization name, your location, and a common password, and then run these commands from the PowerShell command prompt or Integrated Script Environment (ISE) to create user accounts and add them to their groups:</span></span>
  
```powershell
$orgName="<organization name, such as contoso for the contoso.onmicrosoft.com trial subscription domain name>"
$location="<the ISO ALPHA2 country code, such as US for the United States>"
$commonPassword="<common password for all the new accounts>"

$PasswordProfile=New-Object -TypeName Microsoft.Open.AzureAD.Model.PasswordProfile
$PasswordProfile.Password=$commonPassword

$groupName="C-Suite"
$userNames=@("CEO","CFO","CIO") 
$groupID=(Get-AzureADGroup | Where { $_.DisplayName -eq $groupName }).ObjectID
ForEach ($element in $userNames){ 
New-AzureADUser -DisplayName $element -PasswordProfile $PasswordProfile -UserPrincipalName ($element + "@" + $orgName + ".onmicrosoft.com") -AccountEnabled $true -MailNickName $element -UsageLocation $location 
Add-AzureADGroupMember -RefObjectId (Get-AzureADUser | Where { $_.DisplayName -eq $element }).ObjectID -ObjectId $groupID
}
$groupName="Marketing staff"
$userNames=@("Marketing1", "Marketing2") 
$groupID=(Get-AzureADGroup | Where { $_.DisplayName -eq $groupName }).ObjectID
ForEach ($element in $userNames){ 
New-AzureADUser -DisplayName $element -PasswordProfile $PasswordProfile -UserPrincipalName ($element + "@" + $orgName + ".onmicrosoft.com") -AccountEnabled $true -MailNickName $element -UsageLocation $location 
Add-AzureADGroupMember -RefObjectId (Get-AzureADUser | Where { $_.DisplayName -eq $element }).ObjectID -ObjectId $groupID
}
```

> [!NOTE]
> <span data-ttu-id="bf46a-136">L’utilisation ici d’un mot de passe courant est pour l’automatisation et la simplicité de configuration pour un environnement de développement et de test.</span><span class="sxs-lookup"><span data-stu-id="bf46a-136">The use of a common password here is for automation and ease of configuration for a dev/test environment.</span></span> <span data-ttu-id="bf46a-137">Bien évidemment, cela est hautement déconseillé pour les abonnements de production.</span><span class="sxs-lookup"><span data-stu-id="bf46a-137">Obviously, this is highly discouraged for production subscriptions.</span></span> 
  
<span data-ttu-id="bf46a-138">Utilisez ces étapes pour vérifier que la gestion des licences basée sur un groupe fonctionne correctement.</span><span class="sxs-lookup"><span data-stu-id="bf46a-138">Use these steps to verify that group-based licensing is working correctly.</span></span>
  
1. <span data-ttu-id="bf46a-139">Sous l’onglet **Accueil Microsoft Office** de votre navigateur, cliquez sur la vignette **Administration**.</span><span class="sxs-lookup"><span data-stu-id="bf46a-139">From the **Microsoft Office Home** tab of your browser, click the **Admin** tile.</span></span>
    
2. <span data-ttu-id="bf46a-140">Sous le nouvel onglet **Centre d’administration Microsoft 365** de votre navigateur, cliquez sur **Utilisateurs**.</span><span class="sxs-lookup"><span data-stu-id="bf46a-140">From the new **Microsoft 365 admin center** tab of your browser, click **Users**.</span></span>
    
3. <span data-ttu-id="bf46a-141">Dans la liste des utilisateurs, cliquez sur **PDG**.</span><span class="sxs-lookup"><span data-stu-id="bf46a-141">In the list of users, click **CEO**.</span></span>
    
4. <span data-ttu-id="bf46a-142">Dans le volet qui affiche les propriétés du compte d’utilisateur **PDG**, vérifiez que les licences **Microsoft 365 Entreprise E5** lui ont été affectées (dans **Licences de produit**).</span><span class="sxs-lookup"><span data-stu-id="bf46a-142">In the pane that lists the properties of the **CEO** user account, verify that it has been assigned the **Microsoft 365 Enterprise E5** license (in **Product licenses**).</span></span>
    
## <a name="phase-3-create-office-365-retention-labels"></a><span data-ttu-id="bf46a-143">Phase 3: Créer des étiquettes de rétention Office 365</span><span class="sxs-lookup"><span data-stu-id="bf46a-143">Phase 3: Create Office 365 retention labels</span></span>

<span data-ttu-id="bf46a-144">Dans cette phase, vous allez créer les étiquettes de rétention correspondant aux différents niveaux de sécurité pour les dossiers de documents du site d’équipe SharePoint sous-jacent.</span><span class="sxs-lookup"><span data-stu-id="bf46a-144">In this phase, you create the retention labels for the different levels of security for underlying SharePoint site documents folders.</span></span>

1. <span data-ttu-id="bf46a-145">Se connecter au[Centre de conformité Microsoft 365](https://compliance.microsoft.com) avec votre compte d’administrateur général.</span><span class="sxs-lookup"><span data-stu-id="bf46a-145">Sign in to the [Microsoft 365 compliance portal](https://compliance.microsoft.com) with your global admin account.</span></span>
    
2. <span data-ttu-id="bf46a-146">Sous l’onglet **Accueil- Conformité Microsoft 365** de votre navigateur, cliquez sur **Classifications > Étiquettes**.</span><span class="sxs-lookup"><span data-stu-id="bf46a-146">From the **Home - Microsoft 365 compliance** tab of your browser, click **Classifications > Labels**.</span></span>
    
3. <span data-ttu-id="bf46a-147">Cliquez sur **Étiquettes de rétention > Créer une étiquette**.</span><span class="sxs-lookup"><span data-stu-id="bf46a-147">Click **Retention labels > Create a label**.</span></span>
    
4. <span data-ttu-id="bf46a-148">Dans le volet**Nommer votre étiquette**, saisissez**Sensible**dans**Nommer votre étiquette**, puis cliquez sur**Suivant**.</span><span class="sxs-lookup"><span data-stu-id="bf46a-148">On the **Name your label** pane, type **Sensitive** in **Name your label**, and then click **Next**.</span></span>

5. <span data-ttu-id="bf46a-149">Sur le volet**descripteurs de plan fichier**, cliquez sur **suivant**.</span><span class="sxs-lookup"><span data-stu-id="bf46a-149">On the **File plan descriptors** pane, click **Next**.</span></span>
    
6. <span data-ttu-id="bf46a-150">Dans le volet**Paramètres d’étiquette**, définissez, si nécessaire, la**Rétention** sur **Activé** puis cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="bf46a-150">On the **Label settings** pane, if needed, set **Retention** to **On**, and then click **Next**.</span></span>
    
7. <span data-ttu-id="bf46a-151">Dans le volet **Vérifier vos paramètres**, cliquez sur **Créer l’étiquette**.</span><span class="sxs-lookup"><span data-stu-id="bf46a-151">On the **Review your settings** pane, click **Create the label**.</span></span>
    
8. <span data-ttu-id="bf46a-152">Répétez les étapes 3-7 pour une étiquette de rétention supplémentaire nommée **hautement confidentiel**.</span><span class="sxs-lookup"><span data-stu-id="bf46a-152">Repeat steps 3-7 for an additional retention label named **Highly Confidential**.</span></span>
    
9. <span data-ttu-id="bf46a-153">Dans le volet **Accueil > Étiquettes**, cliquez sur **Publier des étiquettes**.</span><span class="sxs-lookup"><span data-stu-id="bf46a-153">From the **Home > Labels** pane, click **Publish labels**.</span></span>
    
10. <span data-ttu-id="bf46a-154">Dans le volet **Choisir les étiquettes à publier**, cliquez sur **Choisir les étiquettes à publier**.</span><span class="sxs-lookup"><span data-stu-id="bf46a-154">On the **Choose labels to publish** pane, click **Choose labels to publish**.</span></span>
    
11. <span data-ttu-id="bf46a-155">Dans le volet **Choisir des étiquettes**, cliquez sur **Ajouter** et sélectionnez les quatre étiquettes.</span><span class="sxs-lookup"><span data-stu-id="bf46a-155">On the **Choose labels** pane, click **Add** and select all four labels.</span></span>
    
12. <span data-ttu-id="bf46a-156">Cliquez sur **Terminé**.</span><span class="sxs-lookup"><span data-stu-id="bf46a-156">Click **Done**.</span></span>
    
13. <span data-ttu-id="bf46a-157">Dans le volet **Choisir les étiquettes à publier**, cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="bf46a-157">On the **Choose labels to publish** pane, click **Next**.</span></span>
    
14. <span data-ttu-id="bf46a-158">Dans le volet **Choisir les emplacements**, cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="bf46a-158">On the **Choose locations** pane, click **Next**.</span></span>
    
15. <span data-ttu-id="bf46a-159">Dans le volet **Nom de votre stratégie**, saisissez **Exemple d’organisation** sous **Nom**, puis cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="bf46a-159">On the **Name your policy** pane, type **Example organization** in **Name**, and then click **Next**.</span></span>
    
16. <span data-ttu-id="bf46a-160">Dans le volet **Vérifier vos paramètres**, cliquez sur **Publier les étiquettes**, puis sur **Fermer**.</span><span class="sxs-lookup"><span data-stu-id="bf46a-160">On the **Review your settings** pane, click **Publish labels**, and then click **Close**.</span></span>
    
## <a name="phase-4-create-your-teams"></a><span data-ttu-id="bf46a-161">Phase 4 : créer vos équipes</span><span class="sxs-lookup"><span data-stu-id="bf46a-161">Phase 4: Create your teams</span></span>

<span data-ttu-id="bf46a-162">Au cours de cette phase, vous créez et configurez des équipes sensibles et hautement confidentielles pour votre exemple d’organisation.</span><span class="sxs-lookup"><span data-stu-id="bf46a-162">In this phase, you create and configure sensitive and highly confidential teams for your example organization.</span></span>

### <a name="sensitive-team-for-marketing-campaigns"></a><span data-ttu-id="bf46a-163">Équipe sensible pour les campagnes marketing</span><span class="sxs-lookup"><span data-stu-id="bf46a-163">Sensitive team for marketing campaigns</span></span>

<span data-ttu-id="bf46a-164">Pour créer une équipe de niveau sensible pour les membres du groupe marketing afin de collaborer sur des campagnes marketing en cours :</span><span class="sxs-lookup"><span data-stu-id="bf46a-164">To create a sensitive-level team for members of the marketing group to collaborate on ongoing marketing campaigns:</span></span>

1. <span data-ttu-id="bf46a-165">[Créez une équipe privée](https://support.office.com/article/174adf5f-846b-4780-b765-de1a0a737e2b) avec le nom **Campagnes marketing**.</span><span class="sxs-lookup"><span data-stu-id="bf46a-165">[Create a new private team](https://support.office.com/article/174adf5f-846b-4780-b765-de1a0a737e2b) with the name **Marketing Campaigns**.</span></span>
2. <span data-ttu-id="bf46a-166">Ouvrez l’équipe **Campagnes marketing**.</span><span class="sxs-lookup"><span data-stu-id="bf46a-166">Open the **Marketing Campaigns** team.</span></span>
3.  <span data-ttu-id="bf46a-167">Dans la barre d’outils de l’équipe, cliquez sur **Fichiers**.</span><span class="sxs-lookup"><span data-stu-id="bf46a-167">In the tool bar for the team, click **Files**.</span></span>
4.  <span data-ttu-id="bf46a-168">Cliquez sur les points de suspension, puis sur **Ouvrir dans SharePoint**.</span><span class="sxs-lookup"><span data-stu-id="bf46a-168">Click the ellipsis, and then click **Open in SharePoint**.</span></span>
5.  <span data-ttu-id="bf46a-169">Dans la barre d’outils du site SharePoint sous-jacent, cliquez sur l’icône Paramètres, puis cliquez sur **Autorisations du site**.</span><span class="sxs-lookup"><span data-stu-id="bf46a-169">In the tool bar of the underlying SharePoint site, click the settings icon, and then click **Site permissions**.</span></span>
6.  <span data-ttu-id="bf46a-170">Dans le volet **Autorisations de site**, sous **Paramètres de partage**, cliquez sur **Modifier les paramètres de partage**.</span><span class="sxs-lookup"><span data-stu-id="bf46a-170">In the **Site permissions** pane, under **Sharing Settings**, click **Change sharing settings**.</span></span>
7.  <span data-ttu-id="bf46a-171">Sous **Autorisations de partage**, sélectionnez **Seuls les propriétaires du site peuvent partager des fichiers, des dossiers et le site**, puis cliquez sur **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="bf46a-171">Under **Sharing permissions**, choose **Only site owners can share files, folders, and the site**, and then click **Save**.</span></span>

<span data-ttu-id="bf46a-172">Ensuite, configurez le dossier de documents du site SharePoint sous-jacent Campagnes marketing avec l’étiquette Sensible.</span><span class="sxs-lookup"><span data-stu-id="bf46a-172">Next, configure the documents folder of the underlying Marketing Campaigns SharePoint site for the Sensitive label.</span></span>

1.  <span data-ttu-id="bf46a-173">Sous l’onglet **Campagne marketing - Accueil** de votre navigateur, cliquez sur **Documents**.</span><span class="sxs-lookup"><span data-stu-id="bf46a-173">In the **Marketing Campaigns-Home** tab of your browser, click **Documents**.</span></span>
2.  <span data-ttu-id="bf46a-174">Cliquez sur l’icône des paramètres, puis cliquez sur **Paramètres de la bibliothèque**.</span><span class="sxs-lookup"><span data-stu-id="bf46a-174">Click the settings icon, and then click **Library settings**.</span></span>
3.  <span data-ttu-id="bf46a-175">Sous **Autorisations et gestion**, cliquez sur **Appliquer l’étiquette aux éléments de cette bibliothèque**.</span><span class="sxs-lookup"><span data-stu-id="bf46a-175">Under **Permissions and Management**, click **Apply label to items in this library**.</span></span>
4.  <span data-ttu-id="bf46a-176">Dans **Paramètres - Appliquer l’étiquette**, sélectionnez **Sensible**, puis cliquez sur **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="bf46a-176">In **Settings-Apply Label**, select **Sensitive**, and then click **Save**.</span></span> 

<span data-ttu-id="bf46a-177">Ensuite, configurez une stratégie de protection contre la perte de données qui avertit les utilisateurs quand ils partagent un document sur un site SharePoint sous-jacent avec l’étiquette Sensible, qui inclut le site Campagnes marketing, en dehors de l’organisation.</span><span class="sxs-lookup"><span data-stu-id="bf46a-177">Next, configure a data loss prevention (DLP) policy that notifies users when they share a document on the underlying SharePoint site with the Sensitive label, which includes the Marketing Campaigns site, outside the organization.</span></span>

1. <span data-ttu-id="bf46a-178">Se connecter au[portail de conformité de Microsoft 365](https://compliance.microsoft.com/) avec votre compte d’administrateur général.</span><span class="sxs-lookup"><span data-stu-id="bf46a-178">Sign in to the [Microsoft 365 compliance portal](https://compliance.microsoft.com/) with your global admin account.</span></span>
    
2. <span data-ttu-id="bf46a-179">Sous le nouvel onglet **Conformité Microsoft 365** de votre navigateur, cliquez sur **Stratégie > Protection contre la perte de données**.</span><span class="sxs-lookup"><span data-stu-id="bf46a-179">On the new **Microsoft 365 compliance** tab in your browser, click **Policies > Data loss prevention**.</span></span>
    
3. <span data-ttu-id="bf46a-180">Dans le volet **Accueil > Protection contre la perte de données**, cliquez sur **Créer une stratégie**.</span><span class="sxs-lookup"><span data-stu-id="bf46a-180">In the **Home > Data loss prevention** pane, click **Create a policy**.</span></span>
    
4. <span data-ttu-id="bf46a-181">Dans le volet **Utiliser un modèle ou créer une stratégie personnalisée**, cliquez sur **Personnalisé**, puis sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="bf46a-181">In the **Start with a template or create a custom policy** pane, click **Custom**, and then click **Next**.</span></span>
    
5. <span data-ttu-id="bf46a-182">Dans le volet **Nom de votre stratégie**, saisissez les **sites SharePoint avec étiquette Sensible** sous **Nom**, puis cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="bf46a-182">In the **Name your policy** pane, type **Sensitive label SharePoint sites** in **Name**, and then click **Next**.</span></span>
    
6. <span data-ttu-id="bf46a-183">Dans le volet **Choisir des emplacements**, cliquez sur **Me laisser choisir des emplacements spécifiques**, puis cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="bf46a-183">In the **Choose locations** pane, click **Let me choose specific locations**, and then click **Next**.</span></span>
    
7. <span data-ttu-id="bf46a-184">Dans la liste des emplacements, désactivez les emplacements **Courrier Exchange**, **Comptes OneDrive** et **Messages de conversations et de canaux Teams**, puis cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="bf46a-184">In the list of locations, disable the **Exchange email**, **OneDrive accounts**, and **Teams chat and channel messages** locations, and then click **Next**.</span></span>
    
8. <span data-ttu-id="bf46a-185">Dans le volet **Personnalisez le type de contenu que vous voulez protéger**, cliquez sur **Modifier**.</span><span class="sxs-lookup"><span data-stu-id="bf46a-185">In the **Customize the type of content you want to protect** pane, click **Edit**.</span></span>
    
9. <span data-ttu-id="bf46a-186">Dans le volet **Choisissez les types de contenu à protéger**, cliquez sur **Ajouter** dans la zone déroulante, puis sélectionnez **Étiquettes de rétention**.</span><span class="sxs-lookup"><span data-stu-id="bf46a-186">In the **Choose the types of content to protect** pane, click **Add** in the drop-down box, and then click **Retention labels**.</span></span>
    
10. <span data-ttu-id="bf46a-187">Dans le volet **Étiquettes de rétention**, cliquez sur **Ajouter**, sélectionnez l’étiquette **Sensible**, puis cliquez sur **Ajouter** et sur **Terminé**.</span><span class="sxs-lookup"><span data-stu-id="bf46a-187">In the **Retention labels** pane, click **Add**, select the **Sensitive** label, click **Add**, and then click **Done**.</span></span>
    
11. <span data-ttu-id="bf46a-188">Dans le volet **Choisir les types de contenu à protéger**, cliquez sur **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="bf46a-188">In the **Choose the types of content to protect** pane, click **Save**.</span></span>
    
12. <span data-ttu-id="bf46a-189">Dans le volet **Personnaliser les types d’informations sensibles que vous souhaitez protéger**, cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="bf46a-189">In the **Customize the type of content you want to protect** pane, click **Next**.</span></span>

13. <span data-ttu-id="bf46a-190">Dans le volet **Que faire en cas de détection d’informations sensibles ?**, cliquez sur **Personnaliser l’info-bulle et l’e-mail**.</span><span class="sxs-lookup"><span data-stu-id="bf46a-190">In the **What do you want to do if we detect sensitive info?** pane, click **Customize the tip and email**.</span></span>
    
14. <span data-ttu-id="bf46a-191">Dans le volet **Personnaliser les conseils et les notifications par e-mail de la stratégie**, cliquez sur **Personnaliser le texte de l’info-bulle de la stratégie**.</span><span class="sxs-lookup"><span data-stu-id="bf46a-191">In the **Customize policy tips and email notifications** pane, click **Customize the policy tip text**.</span></span>
    
15. <span data-ttu-id="bf46a-192">Dans la zone de texte, tapez ou collez ce qui suit :</span><span class="sxs-lookup"><span data-stu-id="bf46a-192">In the text box, type or paste in the following:</span></span>
    
  - <span data-ttu-id="bf46a-p104">Pour partager un fichier avec un utilisateur extérieur à l’organisation, téléchargez-le et ouvrez-le. Cliquez sur Fichier > Protéger le document > Chiffrer avec mot de passe, puis indiquez un mot de passe fort. Envoyez le mot de passe par e-mail ou un autre moyen de communication.</span><span class="sxs-lookup"><span data-stu-id="bf46a-p104">To share with a user outside the organization, download the file and then open it. Click File, then Protect Document, and then Encrypt with Password, and then specify a strong password. Send the password in a separate email or other means of communication.</span></span>
    
16. <span data-ttu-id="bf46a-196">Cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="bf46a-196">Click **OK**.</span></span>
    
17. <span data-ttu-id="bf46a-197">Dans le volet Office **Que faire en cas de détection d’informations sensibles ?**, cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="bf46a-197">In the **What do you want to do if we detect sensitive info?** pane, click **Next**.</span></span>
    
18. <span data-ttu-id="bf46a-198">Dans le volet **Voulez-vous activer la stratégie ou d’abord effectuer des tests ?**, cliquez sur **Oui, l’activer maintenant**, puis cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="bf46a-198">In the **Do you want to turn on the policy or test things out first?** pane, click **Yes, turn it on right away**, and then click **Next**.</span></span>
    
19. <span data-ttu-id="bf46a-199">Dans le volet **Vérifier vos paramètres**, cliquez sur **Créer**, puis sur **Fermer**.</span><span class="sxs-lookup"><span data-stu-id="bf46a-199">In the **Review your settings** pane, click **Create**, and then click **Close**.</span></span>

<span data-ttu-id="bf46a-200">Voici la configuration obtenue pour l’équipe Campagnes marketing.</span><span class="sxs-lookup"><span data-stu-id="bf46a-200">Here is the resulting configuration for the Marketing Campaigns team.</span></span>

![Configuration pour l’équipe Campagnes marketing.](../../media/sensitive-team-config-dev-test.png)
  
### <a name="company-strategy-team-site"></a><span data-ttu-id="bf46a-202">Site d’équipe Stratégie d’entreprise</span><span class="sxs-lookup"><span data-stu-id="bf46a-202">Company strategy team site</span></span>

<span data-ttu-id="bf46a-203">Pour créer une équipe de niveau hautement confidentiel pour les membres de l’équipe de leadership senior afin de collaborer sur la stratégie d’entreprise :</span><span class="sxs-lookup"><span data-stu-id="bf46a-203">To create a highly confidential-level team for members of the senior leadership team to collaborate on company strategy:</span></span>

1. <span data-ttu-id="bf46a-204">[Créez une équipe privée](https://support.office.com/article/174adf5f-846b-4780-b765-de1a0a737e2b) avec le nom **Stratégie d’entreprise**.</span><span class="sxs-lookup"><span data-stu-id="bf46a-204">[Create a new private team](https://support.office.com/article/174adf5f-846b-4780-b765-de1a0a737e2b) with the name **Company Strategy**.</span></span>
2. <span data-ttu-id="bf46a-205">Ouvrez l’équipe**stratégie d’entreprise** .</span><span class="sxs-lookup"><span data-stu-id="bf46a-205">Open the **Company Strategy** team.</span></span>
3.  <span data-ttu-id="bf46a-206">Dans la barre d’outils de l’équipe, cliquez sur **Fichiers**.</span><span class="sxs-lookup"><span data-stu-id="bf46a-206">In the tool bar for the team, click **Files**.</span></span>
4.  <span data-ttu-id="bf46a-207">Cliquez sur les points de suspension, puis sur **Ouvrir dans SharePoint**.</span><span class="sxs-lookup"><span data-stu-id="bf46a-207">Click the ellipsis, and then click **Open in SharePoint**.</span></span>
5.  <span data-ttu-id="bf46a-208">Dans la barre d’outils du site SharePoint sous-jacent, cliquez sur l’icône Paramètres, puis cliquez sur **Autorisations du site**.</span><span class="sxs-lookup"><span data-stu-id="bf46a-208">In the tool bar of the underlying SharePoint site, click the settings icon, and then click **Site permissions**.</span></span>
6.  <span data-ttu-id="bf46a-209">Dans le volet **Autorisations de site**, sous **Paramètres de partage**, cliquez sur **Modifier les paramètres de partage**.</span><span class="sxs-lookup"><span data-stu-id="bf46a-209">In the **Site permissions** pane, under **Sharing Settings**, click **Change sharing settings**.</span></span>
7.  <span data-ttu-id="bf46a-210">Sous **Autorisations de partage**, sélectionnez **Seuls les propriétaires du site peuvent partager des fichiers, des dossiers et le site**.</span><span class="sxs-lookup"><span data-stu-id="bf46a-210">Under **Sharing permissions**, choose **Only site owners can share files, folders, and the site**.</span></span>
8.  <span data-ttu-id="bf46a-211">Désactivez **Autoriser les demandes d’accès**, puis cliquez sur **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="bf46a-211">Turn off **Allow access requests**, and then click **Save**.</span></span>

<span data-ttu-id="bf46a-212">Ensuite, configurez le dossier de documents du site SharePoint sous-jacent Stratégie d’entreprise avec l’étiquette Hautement confidentiel.</span><span class="sxs-lookup"><span data-stu-id="bf46a-212">Next, configure the documents folder of the underlying Company Strategy SharePoint site for the Highly Confidential label.</span></span>

1.  <span data-ttu-id="bf46a-213">Sous l’onglet **Stratégie de l’entreprise - Accueil** de votre navigateur, cliquez sur **Documents**.</span><span class="sxs-lookup"><span data-stu-id="bf46a-213">In the **Company Strategy-Home** tab of your browser, click **Documents**.</span></span>
2.  <span data-ttu-id="bf46a-214">Cliquez sur l’icône des paramètres, puis cliquez sur **Paramètres de la bibliothèque**.</span><span class="sxs-lookup"><span data-stu-id="bf46a-214">Click the settings icon, and then click **Library settings**.</span></span>
3.  <span data-ttu-id="bf46a-215">Sous **Autorisations et gestion**, cliquez sur **Appliquer l’étiquette aux éléments de cette bibliothèque**.</span><span class="sxs-lookup"><span data-stu-id="bf46a-215">Under **Permissions and Management**, click **Apply label to items in this library**.</span></span>
4.  <span data-ttu-id="bf46a-216">Dans **Paramètres - Appliquer une étiquette**, sélectionnez **Hautement confidentiel**, puis cliquez sur **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="bf46a-216">In **Settings-Apply Label**, select **Highly Confidential**, and then click **Save**.</span></span> 

<span data-ttu-id="bf46a-217">Ensuite, configurez une stratégie de protection contre la perte de données qui bloque les utilisateurs quand ils partagent un document à l’extérieur de l’organisation sur un site SharePoint sous-jacent avec l’étiquette Hautement confidentiel, qui inclut le site Stratégie de l’entreprise.</span><span class="sxs-lookup"><span data-stu-id="bf46a-217">Next, configure a DLP policy that blocks users when they share a document on an underlying SharePoint site with the Highly Confidential label, which includes the Company Strategy site, outside the organization.</span></span>
  
1. <span data-ttu-id="bf46a-218">Se connecter au[portail de conformité de Microsoft 365](https://compliance.microsoft.com/) avec votre compte d’administrateur général.</span><span class="sxs-lookup"><span data-stu-id="bf46a-218">Sign in to the [Microsoft 365 compliance portal](https://compliance.microsoft.com/) with your global admin.</span></span>
    
2. <span data-ttu-id="bf46a-219">Sous le nouvel onglet **Conformité Microsoft 365** de votre navigateur, cliquez sur **Stratégie > Protection contre la perte de données**.</span><span class="sxs-lookup"><span data-stu-id="bf46a-219">On the new **Microsoft 365 compliance** tab in your browser, click **Policies > Data loss prevention**.</span></span>
    
3. <span data-ttu-id="bf46a-220">Dans le volet **Accueil > Protection contre la perte de données**, cliquez sur **Créer une stratégie**.</span><span class="sxs-lookup"><span data-stu-id="bf46a-220">In the **Home > Data loss prevention** pane, click **Create a policy**.</span></span>
    
4. <span data-ttu-id="bf46a-221">Dans le volet **Utiliser un modèle ou créer une stratégie personnalisée**, cliquez sur **Personnalisé**, puis sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="bf46a-221">In the **Start with a template or create a custom policy** pane, click **Custom**, and then click **Next**.</span></span>
    
5. <span data-ttu-id="bf46a-222">Dans le volet **Nom de votre stratégie**, saisissez les **Sites SharePoint avec étiquette Hautement confidentiel** sous **Nom**, puis cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="bf46a-222">In the **Name your policy** pane, type **Highly Confidential label SharePoint sites** in **Name**, and then click **Next**.</span></span>
    
6. <span data-ttu-id="bf46a-223">Dans le volet **Choisir des emplacements**, cliquez sur **Me laisser choisir des emplacements spécifiques**, puis cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="bf46a-223">In the **Choose locations** pane, click **Let me choose specific locations**, and then click **Next**.</span></span>
    
7. <span data-ttu-id="bf46a-224">Dans la liste des emplacements, désactivez les emplacements **Courrier Exchange**, **Comptes OneDrive** et **Messages de conversations et de canaux Teams**, puis cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="bf46a-224">In the list of locations, disable the **Exchange email**, **OneDrive accounts**, and **Teams chat and channel messages** locations, and then click **Next**.</span></span>
    
8. <span data-ttu-id="bf46a-225">Dans le volet **Personnalisez le type de contenu que vous voulez protéger**, cliquez sur **Modifier**.</span><span class="sxs-lookup"><span data-stu-id="bf46a-225">In the **Customize the type of content you want to protect** pane, click **Edit**.</span></span>
    
9. <span data-ttu-id="bf46a-226">Dans le volet **Choisissez les types de contenu à protéger**, cliquez sur **Ajouter** dans la zone déroulante, puis sélectionnez **Étiquettes de rétention**.</span><span class="sxs-lookup"><span data-stu-id="bf46a-226">In the **Choose the types of content to protect** pane, click **Add** in the drop-down box, and then click **Retention labels**.</span></span>
    
10. <span data-ttu-id="bf46a-227">Dans le volet **Étiquettes de rétention**, cliquez sur **Ajouter**, sélectionnez l’étiquette **Hautement confidentiel**, puis cliquez sur **Ajouter** et sur **Terminé**.</span><span class="sxs-lookup"><span data-stu-id="bf46a-227">In the **Retention labels** pane, click **Add**, select the **Highly Confidential** label, click **Add**, and then click **Done**.</span></span>
    
11. <span data-ttu-id="bf46a-228">Dans le volet **Choisir les types de contenu à protéger**, cliquez sur **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="bf46a-228">In the **Choose the types of content to protect** pane, click **Save**.</span></span>
    
12. <span data-ttu-id="bf46a-229">Dans le volet **Personnaliser les types d’informations sensibles que vous souhaitez protéger**, cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="bf46a-229">In the **Customize the type of content you want to protect** pane, click **Next**.</span></span>

13. <span data-ttu-id="bf46a-230">Dans le volet **Que faire en cas de détection d’informations sensibles ?**, cliquez sur **Personnaliser l’info-bulle et l’e-mail**.</span><span class="sxs-lookup"><span data-stu-id="bf46a-230">In the **What do you want to do if we detect sensitive info?** pane, click **Customize the tip and email**.</span></span>
    
14. <span data-ttu-id="bf46a-231">Dans le volet **Personnaliser les conseils et les notifications par e-mail de la stratégie**, cliquez sur **Personnaliser le texte de l’info-bulle de la stratégie**.</span><span class="sxs-lookup"><span data-stu-id="bf46a-231">In the **Customize policy tips and email notifications** pane, click **Customize the policy tip text**.</span></span>
    
15. <span data-ttu-id="bf46a-232">Dans la zone de texte, tapez ou collez ce qui suit :</span><span class="sxs-lookup"><span data-stu-id="bf46a-232">In the text box, type or paste in the following:</span></span>
    
  - <span data-ttu-id="bf46a-p105">Pour partager un fichier avec un utilisateur extérieur à l’organisation, téléchargez-le et ouvrez-le. Cliquez sur Fichier > Protéger le document > Chiffrer avec mot de passe, puis indiquez un mot de passe fort. Envoyez le mot de passe par e-mail ou un autre moyen de communication.</span><span class="sxs-lookup"><span data-stu-id="bf46a-p105">To share with a user outside the organization, download the file and then open it. Click File, then Protect Document, and then Encrypt with Password, and then specify a strong password. Send the password in a separate email or other means of communication.</span></span>
    
16. <span data-ttu-id="bf46a-236">Cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="bf46a-236">Click **OK**.</span></span>
    
17. <span data-ttu-id="bf46a-237">Dans le volet **Voulez-vous activer la stratégie ou d’abord effectuer des tests ?**, cliquez sur **Oui, l’activer maintenant**, puis cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="bf46a-237">In the **Do you want to turn on the policy or test things out first?** pane, click **Yes, turn it on right away**, and then click **Next**.</span></span>

18. <span data-ttu-id="bf46a-238">Dans le volet **Voulez-vous activer la stratégie ou d’abord effectuer des tests ?**, cliquez sur **Oui, l’activer maintenant**, puis cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="bf46a-238">In the **Do you want to turn on the policy or test things out first?** pane, click **Yes, turn it on right away**, and then click **Next**.</span></span>
    
19. <span data-ttu-id="bf46a-239">Dans le volet **Vérifier vos paramètres**, cliquez sur **Créer**, puis sur **Fermer**.</span><span class="sxs-lookup"><span data-stu-id="bf46a-239">In the **Review your settings** pane, click **Create**, and then click **Close**.</span></span>

<span data-ttu-id="bf46a-240">Suivez [ces instructions](https://docs.microsoft.com/microsoft-365/compliance/encryption-sensitivity-labels) pour configurer une étiquette de confidentialité avec les paramètres suivants :</span><span class="sxs-lookup"><span data-stu-id="bf46a-240">Use [these instructions](https://docs.microsoft.com/microsoft-365/compliance/encryption-sensitivity-labels) to configure a sensitivity label with the following settings:</span></span>

- <span data-ttu-id="bf46a-241">Le nom de l’étiquette est Stratégie de l’entreprise.</span><span class="sxs-lookup"><span data-stu-id="bf46a-241">The name of the label is Company Strategy</span></span>
- <span data-ttu-id="bf46a-242">Le chiffrement est activé</span><span class="sxs-lookup"><span data-stu-id="bf46a-242">Encryption is enabled</span></span>
- <span data-ttu-id="bf46a-243">Le groupe Stratégie de l’entreprise possède des autorisations de co-création</span><span class="sxs-lookup"><span data-stu-id="bf46a-243">The Company Strategy group has Co-Author permissions</span></span>

<span data-ttu-id="bf46a-244">Une fois que vous l’avez créée, publiez la nouvelle étiquette.</span><span class="sxs-lookup"><span data-stu-id="bf46a-244">After creating, publish the new label.</span></span> <span data-ttu-id="bf46a-245">Si vous vous connectez en tant que membre du groupe Stratégie de l’entreprise, la nouvelle étiquette apparaît dans l’option Confidentialité de la barre d’outils Accueil de Word, Excel et PowerPoint.</span><span class="sxs-lookup"><span data-stu-id="bf46a-245">If you sign in as a member of the Company Strategy group, you will see the new label in the Sensitivity option in the Home toolbar of Word, Excel, and PowerPoint.</span></span> <span data-ttu-id="bf46a-246">Sélectionnez l’étiquette Stratégie de l’entreprise à partir de l’option Confidentialité pour affecter l’étiquette à un fichier.</span><span class="sxs-lookup"><span data-stu-id="bf46a-246">Select the Company Strategy label from the Sensitivity option to assign the label to a file.</span></span>

<span data-ttu-id="bf46a-247">Voici la configuration obtenue pour l’équipe Stratégie de l’entreprise.</span><span class="sxs-lookup"><span data-stu-id="bf46a-247">Here is the resulting configuration for the Company Strategy team.</span></span>

![Configuration pour l’équipe Stratégie de l’entreprise.](../../media/highlyconfidential-team-config-dev-test.png) 

<span data-ttu-id="bf46a-249">Les fichiers dans la section documents du site SharePoint Stratégie de l’entreprise sous-jacent sont affectés à l’étiquette de rétention Hautement confidentiel et sont soumis à la stratégie DLP configurée.</span><span class="sxs-lookup"><span data-stu-id="bf46a-249">Files in the documents section of the underlying Company Strategy SharePoint site are assigned the Highly confidential retention label and are subject to the configured DLP policy.</span></span> <span data-ttu-id="bf46a-250">L’étiquette de confidentialité de la Stratégie d’entreprise peut également être attribuée aux fichiers.</span><span class="sxs-lookup"><span data-stu-id="bf46a-250">Files can also have the Company Strategy sensitivity label assigned.</span></span>    
  
## <a name="next-step"></a><span data-ttu-id="bf46a-251">Étape suivante</span><span class="sxs-lookup"><span data-stu-id="bf46a-251">Next step</span></span>

<span data-ttu-id="bf46a-252">Lorsque vous êtes prêt à procéder au déploiement de production, reportez-vous à [Sécuriser les fichiers dans Microsoft Teams](secure-files-in-teams.md) pour obtenir des informations détaillées et des liens vers des articles de déploiement étape par étape.</span><span class="sxs-lookup"><span data-stu-id="bf46a-252">When you are ready for production deployment, see [Secure files in Microsoft Teams](secure-files-in-teams.md) for detailed information and links to step-by-step deployment articles.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="bf46a-253">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="bf46a-253">See Also</span></span>

[<span data-ttu-id="bf46a-254">Adoption du cloud et solutions hybrides</span><span class="sxs-lookup"><span data-stu-id="bf46a-254">Cloud adoption and hybrid solutions</span></span>](https://docs.microsoft.com/office365/enterprise/cloud-adoption-and-hybrid-solutions)
