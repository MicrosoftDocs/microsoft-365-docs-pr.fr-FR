---
title: Configurer une équipe avec une isolation des problèmes de sécurité dans un environnement de test/développement
author: JoeDavies-MSFT
f1.keywords:
- NOCSH
ms.author: josephd
manager: laurawi
ms.date: 05/01/2020
audience: ITPro
ms.topic: article
ms.prod: microsoft-365-enterprise
localization_priority: Priority
ms.collection:
- M365-security-compliance
- Strat_O365_Enterprise
- remotework
- M365solutions
ms.custom: ''
description: Configurez l’infrastructure et la sécurité qui permettent à vos employés de travailler à distance de n’importe où et à tout moment.
ms.openlocfilehash: 5c2de3fbb174bdf1dccc8ef8371dca1ae1bfddf0
ms.sourcegitcommit: 9c828bc27cd73a1bb85e9fe38d818190025ebb3f
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/07/2020
ms.locfileid: "44159394"
---
# <a name="configure-a-team-with-security-isolation-in-a-devtest-environment"></a><span data-ttu-id="9353e-103">Configurer une équipe avec une isolation des problèmes de sécurité dans un environnement de test/développement</span><span class="sxs-lookup"><span data-stu-id="9353e-103">Configure a team with security isolation in a dev/test environment</span></span>

<span data-ttu-id="9353e-104">Cet article fournit des instructions pas à pas pour créer une [équipe avec une isolation des problèmes de sécurité](secure-teams-security-isolation.md) dans un environnement de développement/test.</span><span class="sxs-lookup"><span data-stu-id="9353e-104">This article provides step-by-step instructions to create a [team with security isolation](secure-teams-security-isolation.md) in a dev/test environment.</span></span>

![Configuration de la stratégie d’entreprise pour l’équipe isolée](../media/team-security-isolation-dev-test/team-security-isolation-dev-test-config.png)

<span data-ttu-id="9353e-106">Utilisez cet environnement de développement/test pour expérimenter et affiner les paramètres de vos besoins spécifiques avant de déployer ce type d’équipe en production.</span><span class="sxs-lookup"><span data-stu-id="9353e-106">Use this dev/test environment to experiment and fine-tune settings for your specific needs before deploying this type of team in production.</span></span>
  
## <a name="phase-1-build-out-your-microsoft-365-enterprise-test-environment"></a><span data-ttu-id="9353e-107">Phase 1 : Créer l’environnement de test Microsoft 365 Entreprise</span><span class="sxs-lookup"><span data-stu-id="9353e-107">Phase 1: Build out your Microsoft 365 Enterprise test environment</span></span>

<span data-ttu-id="9353e-108">Si vous souhaitez simplement tester les équipes sensibles et hautement sensibles de manière rapide avec une configuration minimale, suivez les instructions de [Configuration de base](https://docs.microsoft.com/microsoft-365/enterprise/lightweight-base-configuration-microsoft-365-enterprise).</span><span class="sxs-lookup"><span data-stu-id="9353e-108">If you just want to test sensitive and highly sensitive teams in a lightweight way with the minimum requirements, follow the instructions in [Lightweight base configuration](https://docs.microsoft.com/microsoft-365/enterprise/lightweight-base-configuration-microsoft-365-enterprise).</span></span>

<span data-ttu-id="9353e-109">Si vous voulez tester les équipes sensibles et hautement sensibles au sein d’une entreprise simulée, suivez les instructions de [Synchronisation de hachage de mot de passe](https://docs.microsoft.com/microsoft-365/enterprise/password-hash-sync-m365-ent-test-environment).</span><span class="sxs-lookup"><span data-stu-id="9353e-109">If you want to test sensitive and highly sensitive teams in a simulated enterprise, follow the instructions in [Password hash synchronization](https://docs.microsoft.com/microsoft-365/enterprise/password-hash-sync-m365-ent-test-environment).</span></span>

>[!Note]
><span data-ttu-id="9353e-110">Tester une équipe sensible avec une isolation des problèmes de sécurité ne requiert pas d’environnement de test en entreprise simulée, qui utilise un intranet simulé connecté à Internet et la synchronisation d’annuaire pour une forêt Active Directory. Domain Services (AD DS).</span><span class="sxs-lookup"><span data-stu-id="9353e-110">Testing an team with security isolation does not require the simulated enterprise test environment, which includes a simulated intranet connected to the Internet and directory synchronization for an Active Directory Domain Services (AD DS) forest.</span></span> <span data-ttu-id="9353e-111">Il est proposé comme option dans cet article afin que vous puissiez tester une équipe avec une isolation des problèmes de sécurité et faire des essais dans un environnement qui représente une organisation classique.</span><span class="sxs-lookup"><span data-stu-id="9353e-111">It is provided here as an option so that you can test a team with security isolation and experiment with it in an environment that represents a typical organization.</span></span>
>
    
## <a name="phase-2-create-and-configure-your-azure-active-directory-ad-group-and-users"></a><span data-ttu-id="9353e-112">Phase 2 : Création et configuration de votre groupe et des utilisateurs Azure Active Directory (AD)</span><span class="sxs-lookup"><span data-stu-id="9353e-112">Phase 2: Create and configure your Azure Active Directory (AD) group and users</span></span>

<span data-ttu-id="9353e-113">Dans cette phase, vous créez et vous configurez le groupe et les utilisateurs Azure AD de votre organisation fictive.</span><span class="sxs-lookup"><span data-stu-id="9353e-113">In this phase, you create and configure an Azure AD group and users for your fictional organization.</span></span>
  
<span data-ttu-id="9353e-114">Créez tout d’abord un groupe de sécurité à l’aide du portail Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="9353e-114">First, create a security group with the Azure portal.</span></span>
  
1. <span data-ttu-id="9353e-115">Créez un onglet distinct dans votre navigateur, puis accédez au portail Microsoft Azure sous [https://portal.azure.com](https://portal.azure.com).</span><span class="sxs-lookup"><span data-stu-id="9353e-115">Create a separate tab in your browser, and then go to the Azure portal at [https://portal.azure.com](https://portal.azure.com).</span></span> <span data-ttu-id="9353e-116">Si nécessaire, connectez-vous avec les informations d’identification du compte d’administrateur général de votre abonnement ou essai Microsoft 365 E5.</span><span class="sxs-lookup"><span data-stu-id="9353e-116">If needed, sign in with the credentials of the global administrator account for your Microsoft 365 E5 trial or paid subscription.</span></span>
    
2. <span data-ttu-id="9353e-117">Dans le portail Azure, cliquez sur **Azure Active Directory > Groupes**.</span><span class="sxs-lookup"><span data-stu-id="9353e-117">In the Azure portal, click **Azure Active Directory > Groups**.</span></span>
    
3. <span data-ttu-id="9353e-118">Dans le panneau **Groupes - Tous les groupes**, cliquez sur **+ Nouveau groupe**.</span><span class="sxs-lookup"><span data-stu-id="9353e-118">On the **Groups - All groups** blade, click **+ New group**.</span></span>
    
4. <span data-ttu-id="9353e-119">Dans le panneau **Groupe** :</span><span class="sxs-lookup"><span data-stu-id="9353e-119">On the **Group** blade:</span></span>
    
  - <span data-ttu-id="9353e-120">Sélectionnez **Sécurité** dans **Type de groupe**.</span><span class="sxs-lookup"><span data-stu-id="9353e-120">Select **Security** in **Group type**.</span></span>
    
  - <span data-ttu-id="9353e-121">Tapez **C-Suite** dans le champ **Nom**.</span><span class="sxs-lookup"><span data-stu-id="9353e-121">Type **C-Suite** in **Name**.</span></span>
    
  - <span data-ttu-id="9353e-122">Sélectionnez **Affecté** dans le champ **Type d’appartenance**.</span><span class="sxs-lookup"><span data-stu-id="9353e-122">Select **Assigned** in **Membership type**.</span></span>
      
5. <span data-ttu-id="9353e-123">Cliquez sur **Créer** et fermez le panneau **Groupe**.</span><span class="sxs-lookup"><span data-stu-id="9353e-123">Click **Create**, and then close the **Group** blade.</span></span>
    
<span data-ttu-id="9353e-124">Ensuite, configurez la gestion de licences automatique pour que les membres du nouveau groupe **C-Suite** reçoivent automatiquement une licence Microsoft 365 E5.</span><span class="sxs-lookup"><span data-stu-id="9353e-124">Next, configure automatic licensing so that members of the new **C-Suite** group is automatically assigned a Microsoft 365 E5 license.</span></span>
  
1. <span data-ttu-id="9353e-125">Dans le portail Azure, cliquez sur **Azure Active Directory > Licences > Tous les produits**.</span><span class="sxs-lookup"><span data-stu-id="9353e-125">In the Azure portal, click **Azure Active Directory > Licenses > All products**.</span></span>
    
2. <span data-ttu-id="9353e-126">Dans la liste, sélectionnez **Microsoft 365 Entreprise E5**, puis cliquez sur **Attribuer**.</span><span class="sxs-lookup"><span data-stu-id="9353e-126">In the list, select **Microsoft 365 Enterprise E5**, and then click **Assign**.</span></span>
    
3. <span data-ttu-id="9353e-127">Dans le panneau **Affecter une licence**, cliquez sur **Utilisateurs et groupes**.</span><span class="sxs-lookup"><span data-stu-id="9353e-127">In the **Assign license** blade, click **Users and groups**.</span></span>
    
4. <span data-ttu-id="9353e-128">Dans la liste des groupes, sélectionnez le groupe **C-Suite**.</span><span class="sxs-lookup"><span data-stu-id="9353e-128">In the list of groups, select the **C-Suite** group.</span></span>
    
5. <span data-ttu-id="9353e-129">Cliquez sur **Sélectionner**, puis sur **Affecter**.</span><span class="sxs-lookup"><span data-stu-id="9353e-129">Click **Select**, and then click **Assign**.</span></span>
    
6. <span data-ttu-id="9353e-130">Fermez l’onglet du portail Azure dans votre navigateur.</span><span class="sxs-lookup"><span data-stu-id="9353e-130">Close the Azure portal tab in your browser.</span></span>
    
<span data-ttu-id="9353e-131">Ensuite, [connectez-vous avec le module PowerShell Azure Active Directory pour Graph](https://docs.microsoft.com/office365/enterprise/powershell/connect-to-office-365-powershell#connect-with-the-azure-active-directory-powershell-for-graph-module).</span><span class="sxs-lookup"><span data-stu-id="9353e-131">Next, [connect with the Azure Active Directory PowerShell for Graph module](https://docs.microsoft.com/office365/enterprise/powershell/connect-to-office-365-powershell#connect-with-the-azure-active-directory-powershell-for-graph-module).</span></span>
  
<span data-ttu-id="9353e-132">Renseignez le nom de votre organisation, votre emplacement et un mot de passe commun, puis exécutez les commandes suivantes à partir de l’invite de commandes PowerShell ou de l’environnement de script intégré (ISE) pour créer des comptes d’utilisateur et les ajouter au groupe C-Suite :</span><span class="sxs-lookup"><span data-stu-id="9353e-132">Fill in your organization name, your location, and a common password, and then run these commands from the PowerShell command prompt or Integrated Script Environment (ISE) to create new user accounts and add them to the C-Suite group:</span></span>
  
```powershell
$orgName="<organization name, such as contoso-test for the contoso-test.onmicrosoft.com trial subscription domain name>"
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
```

> [!NOTE]
> <span data-ttu-id="9353e-133">L’utilisation ici d’un mot de passe courant est pour l’automatisation et la simplicité de configuration pour un environnement de développement et de test.</span><span class="sxs-lookup"><span data-stu-id="9353e-133">The use of a common password here is for automation and ease of configuration for a dev/test environment.</span></span> <span data-ttu-id="9353e-134">Bien évidemment, cela est hautement déconseillé pour les abonnements de production.</span><span class="sxs-lookup"><span data-stu-id="9353e-134">Obviously, this is highly discouraged for production subscriptions.</span></span> 
  
<span data-ttu-id="9353e-135">Utilisez ces étapes pour vérifier que la gestion des licences basée sur un groupe fonctionne correctement.</span><span class="sxs-lookup"><span data-stu-id="9353e-135">Use these steps to verify that group-based licensing is working correctly.</span></span>
  
1. <span data-ttu-id="9353e-136">Connectez-vous au [Centre d’administration Microsoft 365](https://admin.microsoft.com).</span><span class="sxs-lookup"><span data-stu-id="9353e-136">Sign in to the [Microsoft 365 admin center](https://admin.microsoft.com).</span></span>
    
2. <span data-ttu-id="9353e-137">Sous le nouvel onglet **Centre d’administration Microsoft 365** de votre navigateur, cliquez sur **Utilisateurs**.</span><span class="sxs-lookup"><span data-stu-id="9353e-137">From the new **Microsoft 365 admin center** tab of your browser, click **Users**.</span></span>
    
3. <span data-ttu-id="9353e-138">Dans la liste des utilisateurs, cliquez sur **PDG**.</span><span class="sxs-lookup"><span data-stu-id="9353e-138">In the list of users, click **CEO**.</span></span>
    
4. <span data-ttu-id="9353e-139">Dans le volet qui affiche les propriétés du compte d’utilisateur **PDG**, vérifiez que les licences **Microsoft 365 Entreprise E5** lui ont été affectées dans les **Licences de produit**.</span><span class="sxs-lookup"><span data-stu-id="9353e-139">In the pane that lists the properties of the **CEO** user account, verify that it has been assigned the **Microsoft 365 Enterprise E5** license in **Product licenses**.</span></span>
    
## <a name="phase-3-create-your-team"></a><span data-ttu-id="9353e-140">Phase 3 : créer votre équipe</span><span class="sxs-lookup"><span data-stu-id="9353e-140">Phase 3: Create your team</span></span>

<span data-ttu-id="9353e-141">Au cours de cette phase, vous créez et configurez une équipe avec l’isolation des problèmes de sécurité pour les membres de l’équipe de direction afin de collaborer sur la stratégie de l’entreprise.</span><span class="sxs-lookup"><span data-stu-id="9353e-141">In this phase, you create and configure a team with security isolation for members of the senior leadership team to collaborate on company strategy.</span></span>

<span data-ttu-id="9353e-142">Veillez tout d’abord à activer [étiquettes de confidentialité pour protéger le contenu de Microsoft Teams, des groupes Office 365 et des sites SharePoint](https://docs.microsoft.com/microsoft-365/compliance/sensitivity-labels-teams-groups-sites) avant de passer aux étapes décrites dans cet article.</span><span class="sxs-lookup"><span data-stu-id="9353e-142">First, enable sensitivity labels to protect content in Microsoft Teams, Office 365 groups, and SharePoint sites before you proceed with the steps in [this article](https://docs.microsoft.com/microsoft-365/compliance/sensitivity-labels-teams-groups-sites).</span></span>

<span data-ttu-id="9353e-143">Ensuite, créez l’équipe :</span><span class="sxs-lookup"><span data-stu-id="9353e-143">Next, create the team:</span></span>

1. <span data-ttu-id="9353e-144">Dans Teams, cliquez sur **Teams** sur le côté gauche de l’application, puis cliquez sur **Rejoindre ou créer une équipe** en bas de la liste des équipes.</span><span class="sxs-lookup"><span data-stu-id="9353e-144">In Teams, click **Teams** on the left side of the app, then click **Join or create a team** at the bottom of the teams list.</span></span>
2. <span data-ttu-id="9353e-145">Cliquez sur **Créer une équipe** (première carte, coin supérieur gauche).</span><span class="sxs-lookup"><span data-stu-id="9353e-145">Click **Create team** (first card, top left corner).</span></span>
3. <span data-ttu-id="9353e-146">Sélectionnez **Créer une équipe à partir de zéro**.</span><span class="sxs-lookup"><span data-stu-id="9353e-146">Choose **Build a team from scratch**.</span></span>
4. <span data-ttu-id="9353e-147">Dans la liste **Sensibilité**, conservez la valeur par défaut.</span><span class="sxs-lookup"><span data-stu-id="9353e-147">In the **Sensitivity** list, keep the default.</span></span>
5. <span data-ttu-id="9353e-148">Sous **Confidentialité**, cliquez sur **Privée**.</span><span class="sxs-lookup"><span data-stu-id="9353e-148">Under **Privacy**, click **Private**.</span></span>
6. <span data-ttu-id="9353e-149">Tapez **Stratégie d’entreprise**, puis cliquez sur **Créer** > **Fermer**.</span><span class="sxs-lookup"><span data-stu-id="9353e-149">Type **Company Strategy**, and then click **Create** > **Close**.</span></span>

<span data-ttu-id="9353e-150">Vous devez ensuite configurer une étiquette de confidentialité avec les paramètres suivants :</span><span class="sxs-lookup"><span data-stu-id="9353e-150">Next, you need to configure a sensitivity label with the following settings:</span></span>

- <span data-ttu-id="9353e-151">Le nom de l’étiquette est Stratégie de l’entreprise.</span><span class="sxs-lookup"><span data-stu-id="9353e-151">The name of the label is Company Strategy</span></span>
- <span data-ttu-id="9353e-152">Le chiffrement est activé</span><span class="sxs-lookup"><span data-stu-id="9353e-152">Encryption is enabled</span></span>
- <span data-ttu-id="9353e-153">Le groupe Stratégie de l’entreprise possède des autorisations de co-création</span><span class="sxs-lookup"><span data-stu-id="9353e-153">The Company Strategy group has Co-Author permissions</span></span>

<span data-ttu-id="9353e-154">Procédez comme suit :</span><span class="sxs-lookup"><span data-stu-id="9353e-154">Follow these steps:</span></span>

1. <span data-ttu-id="9353e-155">Ouvrez le [Centre de conformité Microsoft 365](https://compliance.microsoft.com).</span><span class="sxs-lookup"><span data-stu-id="9353e-155">Open the [Microsoft 365 compliance center](https://compliance.microsoft.com).</span></span>
2. <span data-ttu-id="9353e-156">Sous **Solutions**, cliquez sur **Protection des informations**.</span><span class="sxs-lookup"><span data-stu-id="9353e-156">Under **Solutions**, click **Information protection**.</span></span>
3. <span data-ttu-id="9353e-157">Cliquez sur **Créer une étiquette**.</span><span class="sxs-lookup"><span data-stu-id="9353e-157">Click **Create a label**.</span></span>
4. <span data-ttu-id="9353e-158">Tapez **Stratégie d’entreprise** comme nom d’étiquette.</span><span class="sxs-lookup"><span data-stu-id="9353e-158">Type **Company Strategy** for the label name.</span></span>
5. <span data-ttu-id="9353e-159">Tapez **Documents de stratégie de la direction de l’entreprise** sous forme d’info-bulle, puis cliquez **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="9353e-159">Type **Senior leadership company strategy documents** as the tool tip, and then click **Next**.</span></span>
6. <span data-ttu-id="9353e-160">Sur la page **Chiffrement**, dans le menu déroulant **Chiffrement**, sélectionnez **Appliquer**.</span><span class="sxs-lookup"><span data-stu-id="9353e-160">On the **Encryption** page, in the **Encryption** dropdown, choose **Apply**.</span></span>
7. <span data-ttu-id="9353e-161">Pour ajouter des autorisations d’équipe :</span><span class="sxs-lookup"><span data-stu-id="9353e-161">To add the team permissions:</span></span><br>
  <span data-ttu-id="9353e-162">a.</span><span class="sxs-lookup"><span data-stu-id="9353e-162">a.</span></span> <span data-ttu-id="9353e-163">Cliquez sur **Attribuer des autorisations**.</span><span class="sxs-lookup"><span data-stu-id="9353e-163">Click **Assign permissions**.</span></span><br>
  <span data-ttu-id="9353e-164">b.</span><span class="sxs-lookup"><span data-stu-id="9353e-164">b.</span></span> <span data-ttu-id="9353e-165">Cliquez sur **Ajouter des utilisateurs ou des groupes**, sélectionnez l’équipe que vous avez créée, puis cliquez sur **Stratégie d’entreprise**, enfin cliquez sur **Ajouter**.</span><span class="sxs-lookup"><span data-stu-id="9353e-165">Click **Add users or groups**, select **Company Strategy**, and then click **Add**.</span></span><br>
  <span data-ttu-id="9353e-166">c.</span><span class="sxs-lookup"><span data-stu-id="9353e-166">c.</span></span> <span data-ttu-id="9353e-167">Cliquez sur **Choisir les autorisations**.</span><span class="sxs-lookup"><span data-stu-id="9353e-167">Click **Choose permissions**.</span></span><br>
  <span data-ttu-id="9353e-168">d.</span><span class="sxs-lookup"><span data-stu-id="9353e-168">d.</span></span> <span data-ttu-id="9353e-169">Sélectionnez **Co-auteur** dans la liste déroulante, puis cliquez sur **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="9353e-169">Choose **Co-Author** from the dropdown list, and then click **Save**.</span></span><br>
8. <span data-ttu-id="9353e-170">Cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="9353e-170">Click **Next**.</span></span>
9. <span data-ttu-id="9353e-171">Dans la page **Marque de contenu**, cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="9353e-171">On the **Content marking** page, click **Next**.</span></span>
10. <span data-ttu-id="9353e-172">Dans la page **Paramètres de site et de groupe**, configurez **Paramètres de site et de groupe** sur **Activé**.</span><span class="sxs-lookup"><span data-stu-id="9353e-172">On the **Site and group settings** page, set **Site and group settings** to **On**.</span></span>
11. <span data-ttu-id="9353e-173">Dans la liste déroulante **Confidentialité de sites d’équipe Office 365 connectés à un groupe**, sélectionnez **Privé : seuls les membres peuvent accéder au site**.</span><span class="sxs-lookup"><span data-stu-id="9353e-173">In the **Privacy of Office 365 group-connected team sites** dropdown, choose **Private - only members can access the site**.</span></span>
12. <span data-ttu-id="9353e-174">Sous **Appareils non gérés**, sélectionnez **Bloquer l’accès**.</span><span class="sxs-lookup"><span data-stu-id="9353e-174">Under **Unmanaged devices**, choose **Block access**.</span></span>
13. <span data-ttu-id="9353e-175">Cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="9353e-175">Click **Next**.</span></span>
14. <span data-ttu-id="9353e-176">Dans la page **Étiquetage automatique pour les applications Office**, cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="9353e-176">On the **Auto-labeling for Office apps** page, click **Next**.</span></span>
15. <span data-ttu-id="9353e-177">Cliquez sur **Envoyer**, puis sur **Terminé**.</span><span class="sxs-lookup"><span data-stu-id="9353e-177">Click **Submit**, and then click **Done**.</span></span>

<span data-ttu-id="9353e-178">Ensuite, publiez la nouvelle étiquette en procédant comme suit :</span><span class="sxs-lookup"><span data-stu-id="9353e-178">Next, publish the new label with these steps:</span></span> 

1. <span data-ttu-id="9353e-179">Dans le Centre de conformité Microsoft 365, dans la page **protection des informations**, sélectionnez l’onglet **Stratégies d’étiquette**.</span><span class="sxs-lookup"><span data-stu-id="9353e-179">In the Microsoft 365 compliance center, on the **Information protection** page, choose the **Label policies** tab.</span></span>
2. <span data-ttu-id="9353e-180">Cliquez sur **Publier des étiquettes**.</span><span class="sxs-lookup"><span data-stu-id="9353e-180">Click **Publish labels**.</span></span>
3. <span data-ttu-id="9353e-181">Dans la page **Choisir des étiquettes de confidentialité à publier**, cliquez sur **Choisir des étiquettes de confidentialité à publier**.</span><span class="sxs-lookup"><span data-stu-id="9353e-181">On the **Choose sensitivity labels to publish** page, click **Choose sensitivity labels to publish**.</span></span>
4. <span data-ttu-id="9353e-182">Sélectionnez **Stratégie d’entreprise**, puis cliquez sur **Ajouter**.</span><span class="sxs-lookup"><span data-stu-id="9353e-182">Select **Company Strategy**, and then click **Add**.</span></span>
5. <span data-ttu-id="9353e-183">Cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="9353e-183">Click **Next**.</span></span>
6. <span data-ttu-id="9353e-184">Dans la page **Publier pour les utilisateurs et groupes**, cliquez sur **Choisir les utilisateurs et les groupes**.</span><span class="sxs-lookup"><span data-stu-id="9353e-184">On the **Publish to users and groups** page, click **Choose users and groups**.</span></span>
7. <span data-ttu-id="9353e-185">Cliquez sur **Ajouter**, puis sélectionnez **Stratégie d’entreprise**.</span><span class="sxs-lookup"><span data-stu-id="9353e-185">Click **Add**, and then select **Company Strategy**.</span></span>
8. <span data-ttu-id="9353e-186">Cliquez sur **Ajouter**, puis sur **Terminé**.</span><span class="sxs-lookup"><span data-stu-id="9353e-186">Click **Add**, and then click **Done**.</span></span>
9. <span data-ttu-id="9353e-187">Cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="9353e-187">Click **Next**.</span></span>
10. <span data-ttu-id="9353e-188">Dans la page Paramètres de stratégie, activez la case à cocher **Les utilisateurs doivent fournir une justification pour supprimer une étiquette ou une étiquette de classification inférieure**, puis cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="9353e-188">On the Policy settings page, select the **Users must provide justification to remove a label or lower classification label** check box, and then click **Next**.</span></span>
11. <span data-ttu-id="9353e-189">Tapez **Stratégie d’entreprise** comme nom de stratégie, puis cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="9353e-189">Type **Company Strategy** for the policy name, and then click **Next**.</span></span>
12. <span data-ttu-id="9353e-190">Cliquez sur **Envoyer**, puis cliquez sur **Terminé**.</span><span class="sxs-lookup"><span data-stu-id="9353e-190">Click **Submit** and then click **Done**.</span></span>

<span data-ttu-id="9353e-191">La **Stratégie d’entreprise** peut prendre un certain temps avant de devenir disponible une fois qu'elle a été publiée.</span><span class="sxs-lookup"><span data-stu-id="9353e-191">It may take some time for the **Company Strategy** label to become available after it's been published.</span></span>

<span data-ttu-id="9353e-192">Ensuite, appliquez votre nouvelle étiquette à l’équipe **Stratégie d’entreprise** et mettez à jour le type de lien de partage par défaut pour réduire le risque de partager accidentellement des fichiers et des dossiers avec un public plus large que prévu.</span><span class="sxs-lookup"><span data-stu-id="9353e-192">Next, apply your new label to the **Company Strategy** team and update the default sharing link type to reduce the risk of accidentally sharing files and folders to a wider audience than intended.</span></span> 

1. <span data-ttu-id="9353e-193">Ouvrez le [Centre d’administration SharePoint](https://admin.microsoft.com/sharepoint).</span><span class="sxs-lookup"><span data-stu-id="9353e-193">Open the [SharePoint admin center](https://admin.microsoft.com/sharepoint).</span></span>
2. <span data-ttu-id="9353e-194">Sous **Sites**, cliquez sur **Sites actifs**.</span><span class="sxs-lookup"><span data-stu-id="9353e-194">Under **Sites**, click **Active sites**.</span></span>
3. <span data-ttu-id="9353e-195">Cliquez sur la**Stratégie d’entreprise** .</span><span class="sxs-lookup"><span data-stu-id="9353e-195">Click the **Company Strategy** site.</span></span>
4. <span data-ttu-id="9353e-196">Sous l’onglet **Stratégies**, sous **Confidentialité**, cliquez sur **Modifier**.</span><span class="sxs-lookup"><span data-stu-id="9353e-196">On the **Policies** tab, under **Sensitivity**, click **Edit**.</span></span>
5. <span data-ttu-id="9353e-197">Sélectionnez l’étiquette **Stratégie d’entreprise**, puis cliquez sur **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="9353e-197">Select the **Company Strategy** label, and then click **Save**.</span></span>
6. <span data-ttu-id="9353e-198">Sous l’onglet **Stratégies**, sous **Partage externe**, cliquez sur **Modifier**.</span><span class="sxs-lookup"><span data-stu-id="9353e-198">On the **Policies** tab, under **External sharing**, click **Edit**.</span></span>
5. <span data-ttu-id="9353e-199">Choisissez**Uniquement les personnes de votre organisation**.</span><span class="sxs-lookup"><span data-stu-id="9353e-199">Choose **Only people in your organization**.</span></span>
6. <span data-ttu-id="9353e-200">Sous Type de lien de **Partage par défaut**, désactivez la case à cocher **Identique au paramètre de niveau organisation**, puis sélectionnez **Personnes disposant d’un accès existant**.</span><span class="sxs-lookup"><span data-stu-id="9353e-200">Under **Default sharing** link type, clear the **Same as organization-level setting** check box, and select **People with existing access**.</span></span>
7. <span data-ttu-id="9353e-201">Cliquez sur **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="9353e-201">Click **Save**.</span></span>

<span data-ttu-id="9353e-202">Ensuite, configurez le partage de sites aux propriétaires uniquement pour l’équipe de **Stratégie d’entreprise**.</span><span class="sxs-lookup"><span data-stu-id="9353e-202">Next, configure owners-only site sharing for the **Company Strategy** team.</span></span>

1. <span data-ttu-id="9353e-203">Dans Teams, accédez à l’onglet **Général** de l’équipe de la **Stratégie d’entreprise**.</span><span class="sxs-lookup"><span data-stu-id="9353e-203">In Teams, navigate to the **General** tab of the **Company Strategy** team.</span></span>
2. <span data-ttu-id="9353e-204">Dans la barre d’outils de l’équipe, cliquez sur **Fichiers**.</span><span class="sxs-lookup"><span data-stu-id="9353e-204">In the tool bar for the team, click **Files**.</span></span>
3. <span data-ttu-id="9353e-205">Cliquez sur les points de suspension, puis sur **Ouvrir dans SharePoint**.</span><span class="sxs-lookup"><span data-stu-id="9353e-205">Click the ellipsis, and then click **Open in SharePoint**.</span></span>
4. <span data-ttu-id="9353e-206">Dans la barre d’outils du site SharePoint sous-jacent, cliquez sur l’icône Paramètres, puis cliquez sur **Autorisations du site**.</span><span class="sxs-lookup"><span data-stu-id="9353e-206">In the tool bar of the underlying SharePoint site, click the settings icon, and then click **Site permissions**.</span></span>
5. <span data-ttu-id="9353e-207">Dans le volet Autorisations de site, sous le **Site de partage**, cliquez sur **Modifier les modalités de partage par les membres**.</span><span class="sxs-lookup"><span data-stu-id="9353e-207">In the Site permissions pane, under **Site Sharing**, click **Change how members can share**.</span></span>
6. <span data-ttu-id="9353e-208">Sous **Autorisations de partage**, sélectionnez **Seuls les propriétaires du site peuvent partager des fichiers, des dossiers et le site**, puis cliquez sur **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="9353e-208">Under **Sharing permissions**, choose **Only site owners can share files, folders, and the site**, and then click **Save**.</span></span>
7. <span data-ttu-id="9353e-209">Fermez les volets **Autorisations** et **Paramètres**.</span><span class="sxs-lookup"><span data-stu-id="9353e-209">Close the **Permissions** and **Settings** panes.</span></span>

<span data-ttu-id="9353e-210">Si vous vous connectez en tant que membre du groupe **Stratégie d’entreprise**, la nouvelle étiquette apparaît dans l’option **Confidentialité** de la barre d’outils Accueil de Word, Excel et PowerPoint.</span><span class="sxs-lookup"><span data-stu-id="9353e-210">If you sign in as a member of the Company Strategy group, you will see **Company Strategy** in the **Sensitivity** option in the Home toolbar of Word, Excel, and PowerPoint.</span></span> <span data-ttu-id="9353e-211">Sélectionnez l’étiquette **Stratégie d’entreprise** à partir de l’option **Confidentialité** pour affecter l’étiquette à un fichier.</span><span class="sxs-lookup"><span data-stu-id="9353e-211">Select the **Company Strategy** label from the **Sensitivity** option to assign the label to a file.</span></span>

<span data-ttu-id="9353e-212">Voici la configuration obtenue pour l’équipe Stratégie d’entreprise.</span><span class="sxs-lookup"><span data-stu-id="9353e-212">Here is the resulting configuration for the Company Strategy team.</span></span>

![Configuration de la stratégie d’entreprise pour l’équipe isolée](../media/team-security-isolation-dev-test/team-security-isolation-dev-test-config.png)

<span data-ttu-id="9353e-214">Les fichiers de l’équipe peuvent avoir l’étiquette de confidentialité Stratégie d’entreprise attribuée par les membres du groupe Stratégie d’entreprise.</span><span class="sxs-lookup"><span data-stu-id="9353e-214">Files in the team can have the Company Strategy sensitivity label assigned by the members of the Company Strategy group.</span></span> <span data-ttu-id="9353e-215">Voici un exemple.</span><span class="sxs-lookup"><span data-stu-id="9353e-215">Here is an example.</span></span>

![Exemple de fichier disposant d’une étiquette de confidentialité Stratégie d’entreprise appliquée](../media/team-security-isolation-dev-test/team-security-isolation-dev-test-config-example.png)
 
## <a name="next-step"></a><span data-ttu-id="9353e-217">Étape suivante</span><span class="sxs-lookup"><span data-stu-id="9353e-217">Next step</span></span>

<span data-ttu-id="9353e-218">Lorsque vous êtes prêt à procéder au déploiement de la production, consultez [Configurer une équipe avec l’isolation des problèmes de sécurité](secure-teams-security-isolation.md) pour obtenir des informations de configuration détaillées.</span><span class="sxs-lookup"><span data-stu-id="9353e-218">When you are ready for production deployment, see [Configure a team with security isolation](secure-teams-security-isolation.md) for detailed configuration information.</span></span>
