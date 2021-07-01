---
title: Configurer une équipe avec une isolation des problèmes de sécurité dans un environnement de test/développement
author: JoeDavies-MSFT
f1.keywords:
- NOCSH
ms.author: josephd
manager: laurawi
ms.date: 08/14/2020
audience: ITPro
ms.topic: article
ms.prod: microsoft-365-enterprise
localization_priority: Priority
ms.collection:
- M365-security-compliance
- Strat_O365_Enterprise
- remotework
ms.custom: ''
description: Configurez l’infrastructure et la sécurité qui permettent à vos employés de travailler à distance de n’importe où et à tout moment.
ms.openlocfilehash: c58f0849937d7a807c9969e1651c51b3a9470ba5
ms.sourcegitcommit: 48195345b21b409b175d68acdc25d9f2fc4fc5f1
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/30/2021
ms.locfileid: "53228602"
---
# <a name="configure-a-team-with-security-isolation-in-a-devtest-environment"></a><span data-ttu-id="34c5f-103">Configurer une équipe avec une isolation des problèmes de sécurité dans un environnement de test/développement</span><span class="sxs-lookup"><span data-stu-id="34c5f-103">Configure a team with security isolation in a dev/test environment</span></span>

<span data-ttu-id="34c5f-104">Cet article fournit des instructions pas à pas pour créer une [équipe avec une isolation des problèmes de sécurité](secure-teams-security-isolation.md) dans un environnement de développement/test.</span><span class="sxs-lookup"><span data-stu-id="34c5f-104">This article provides step-by-step instructions to create a [team with security isolation](secure-teams-security-isolation.md) in a dev/test environment.</span></span>

![Configuration de la stratégie d’entreprise pour l’équipe isolée](../media/team-security-isolation-dev-test/team-security-isolation-dev-test-config.png)

<span data-ttu-id="34c5f-106">Utilisez cet environnement de développement/test pour expérimenter et affiner les paramètres de vos besoins spécifiques avant de déployer ce type d’équipe en production.</span><span class="sxs-lookup"><span data-stu-id="34c5f-106">Use this dev/test environment to experiment and fine-tune settings for your specific needs before deploying this type of team in production.</span></span>

## <a name="phase-1-build-out-your-microsoft-365-enterprise-test-environment"></a><span data-ttu-id="34c5f-107">Phase 1 : Créer l’environnement de test Microsoft 365 Entreprise</span><span class="sxs-lookup"><span data-stu-id="34c5f-107">Phase 1: Build out your Microsoft 365 Enterprise test environment</span></span>

<span data-ttu-id="34c5f-108">Si vous souhaitez simplement tester les équipes sensibles et hautement sensibles de manière rapide avec une configuration minimale, suivez les instructions de [Configuration de base](../enterprise/lightweight-base-configuration-microsoft-365-enterprise.md).</span><span class="sxs-lookup"><span data-stu-id="34c5f-108">If you just want to test sensitive and highly sensitive teams in a lightweight way with the minimum requirements, follow the instructions in [Lightweight base configuration](../enterprise/lightweight-base-configuration-microsoft-365-enterprise.md).</span></span>

<span data-ttu-id="34c5f-109">Si vous voulez tester les équipes sensibles et hautement sensibles au sein d’une entreprise simulée, suivez les instructions de [Synchronisation de hachage de mot de passe](../enterprise/password-hash-sync-m365-ent-test-environment.md).</span><span class="sxs-lookup"><span data-stu-id="34c5f-109">If you want to test sensitive and highly sensitive teams in a simulated enterprise, follow the instructions in [Password hash synchronization](../enterprise/password-hash-sync-m365-ent-test-environment.md).</span></span>

> [!NOTE]
> <span data-ttu-id="34c5f-110">Tester une équipe sensible avec une isolation des problèmes de sécurité ne requiert pas d’environnement de test en entreprise simulée, qui utilise un intranet simulé connecté à Internet et la synchronisation d’annuaire pour une forêt Active Directory. Domain Services (AD DS).</span><span class="sxs-lookup"><span data-stu-id="34c5f-110">Testing a team with security isolation does not require the simulated enterprise test environment, which includes a simulated intranet connected to the Internet and directory synchronization for an Active Directory Domain Services (AD DS) forest.</span></span> <span data-ttu-id="34c5f-111">Il est proposé comme option dans cet article afin que vous puissiez tester une équipe avec une isolation des problèmes de sécurité et faire des essais dans un environnement qui représente une organisation classique.</span><span class="sxs-lookup"><span data-stu-id="34c5f-111">It is provided here as an option so that you can test a team with security isolation and experiment with it in an environment that represents a typical organization.</span></span>

## <a name="phase-2-create-and-configure-your-azure-active-directory-azure-ad-group-and-users"></a><span data-ttu-id="34c5f-112">Phase 2 : Création et configuration de votre groupe et des utilisateurs Azure Active Directory (AD)</span><span class="sxs-lookup"><span data-stu-id="34c5f-112">Phase 2: Create and configure your Azure Active Directory (Azure AD) group and users</span></span>

<span data-ttu-id="34c5f-113">Dans cette phase, vous créez et vous configurez le groupe et les utilisateurs Azure AD de votre organisation fictive.</span><span class="sxs-lookup"><span data-stu-id="34c5f-113">In this phase, you create and configure an Azure AD group and users for your fictional organization.</span></span>

<span data-ttu-id="34c5f-114">Créez tout d’abord un groupe de sécurité à l’aide du portail Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="34c5f-114">First, create a security group with the Azure portal.</span></span>

1. <span data-ttu-id="34c5f-115">Créez un onglet distinct dans votre navigateur, puis accédez au portail Microsoft Azure sous [https://portal.azure.com](https://portal.azure.com).</span><span class="sxs-lookup"><span data-stu-id="34c5f-115">Create a separate tab in your browser, and then go to the Azure portal at [https://portal.azure.com](https://portal.azure.com).</span></span> <span data-ttu-id="34c5f-116">Si nécessaire, connectez-vous avec les informations d’identification du compte d’administrateur général de votre abonnement ou essai Microsoft 365 E5.</span><span class="sxs-lookup"><span data-stu-id="34c5f-116">If needed, sign in with the credentials of the global administrator account for your Microsoft 365 E5 trial or paid subscription.</span></span>

2. <span data-ttu-id="34c5f-117">Dans le portail Azure, cliquez sur **Azure Active Directory > Groupes**.</span><span class="sxs-lookup"><span data-stu-id="34c5f-117">In the Azure portal, click **Azure Active Directory > Groups**.</span></span>

3. <span data-ttu-id="34c5f-118">Dans le panneau **Groupes - Tous les groupes**, cliquez sur **+ Nouveau groupe**.</span><span class="sxs-lookup"><span data-stu-id="34c5f-118">On the **Groups - All groups** blade, click **+ New group**.</span></span>

4. <span data-ttu-id="34c5f-119">Dans le panneau **Groupe** :</span><span class="sxs-lookup"><span data-stu-id="34c5f-119">On the **Group** blade:</span></span>

  - <span data-ttu-id="34c5f-120">Sélectionnez **Sécurité** dans **Type de groupe**.</span><span class="sxs-lookup"><span data-stu-id="34c5f-120">Select **Security** in **Group type**.</span></span>

  - <span data-ttu-id="34c5f-121">Tapez **C-Suite** dans le champ **Nom**.</span><span class="sxs-lookup"><span data-stu-id="34c5f-121">Type **C-Suite** in **Name**.</span></span>

  - <span data-ttu-id="34c5f-122">Sélectionnez **Affecté** dans le champ **Type d’appartenance**.</span><span class="sxs-lookup"><span data-stu-id="34c5f-122">Select **Assigned** in **Membership type**.</span></span>

5. <span data-ttu-id="34c5f-123">Cliquez sur **Créer** et fermez le panneau **Groupe**.</span><span class="sxs-lookup"><span data-stu-id="34c5f-123">Click **Create**, and then close the **Group** blade.</span></span>

<span data-ttu-id="34c5f-124">Ensuite, configurez la gestion de licences automatique pour que les membres du nouveau groupe **C-Suite** reçoivent automatiquement une licence Microsoft 365 E5.</span><span class="sxs-lookup"><span data-stu-id="34c5f-124">Next, configure automatic licensing so that members of the new **C-Suite** group are automatically assigned a Microsoft 365 E5 license.</span></span>

1. <span data-ttu-id="34c5f-125">Dans le portail Azure, cliquez sur **Azure Active Directory > Licences > Tous les produits**.</span><span class="sxs-lookup"><span data-stu-id="34c5f-125">In the Azure portal, click **Azure Active Directory > Licenses > All products**.</span></span>

2. <span data-ttu-id="34c5f-126">Dans la liste, sélectionnez **Microsoft 365 Entreprise E5**, puis cliquez sur **Attribuer**.</span><span class="sxs-lookup"><span data-stu-id="34c5f-126">In the list, select **Microsoft 365 Enterprise E5**, and then click **Assign**.</span></span>

3. <span data-ttu-id="34c5f-127">Dans le panneau **Affecter une licence**, cliquez sur **Utilisateurs et groupes**.</span><span class="sxs-lookup"><span data-stu-id="34c5f-127">In the **Assign license** blade, click **Users and groups**.</span></span>

4. <span data-ttu-id="34c5f-128">Dans la liste des groupes, sélectionnez le groupe **C-Suite**.</span><span class="sxs-lookup"><span data-stu-id="34c5f-128">In the list of groups, select the **C-Suite** group.</span></span>

5. <span data-ttu-id="34c5f-129">Cliquez sur **Sélectionner**, puis sur **Affecter**.</span><span class="sxs-lookup"><span data-stu-id="34c5f-129">Click **Select**, and then click **Assign**.</span></span>

6. <span data-ttu-id="34c5f-130">Fermez l’onglet du portail Azure dans votre navigateur.</span><span class="sxs-lookup"><span data-stu-id="34c5f-130">Close the Azure portal tab in your browser.</span></span>

<span data-ttu-id="34c5f-131">Ensuite, [connectez-vous avec le module PowerShell Azure Active Directory pour Graph](../enterprise/connect-to-microsoft-365-powershell.md#connect-with-the-azure-active-directory-powershell-for-graph-module).</span><span class="sxs-lookup"><span data-stu-id="34c5f-131">Next, [connect with the Azure Active Directory PowerShell for Graph module](../enterprise/connect-to-microsoft-365-powershell.md#connect-with-the-azure-active-directory-powershell-for-graph-module).</span></span>

<span data-ttu-id="34c5f-132">Renseignez le nom de votre organisation, votre emplacement et un mot de passe commun, puis exécutez les commandes suivantes à partir de l’invite de commandes PowerShell ou de l’environnement de script intégré (ISE) pour créer des comptes d’utilisateur et les ajouter au groupe C-Suite :</span><span class="sxs-lookup"><span data-stu-id="34c5f-132">Fill in your organization name, your location, and a common password, and then run these commands from the PowerShell command prompt or Integrated Script Environment (ISE) to create new user accounts and add them to the C-Suite group:</span></span>

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
> <span data-ttu-id="34c5f-p103">L'utilisation d'un mot de passe commun vise à automatiser et à faciliter la configuration d'un environnement de développement ou de test. Évidemment, cela est fortement déconseillé pour les abonnements de production.</span><span class="sxs-lookup"><span data-stu-id="34c5f-p103">The use of a common password here is for automation and ease of configuration for a dev/test environment. Obviously, this is highly discouraged for production subscriptions.</span></span>

<span data-ttu-id="34c5f-135">Utilisez ces étapes pour vérifier que la gestion des licences basée sur un groupe fonctionne correctement.</span><span class="sxs-lookup"><span data-stu-id="34c5f-135">Use these steps to verify that group-based licensing is working correctly.</span></span>

1. <span data-ttu-id="34c5f-136">Connectez-vous au [Centre d’administration Microsoft 365](https://admin.microsoft.com).</span><span class="sxs-lookup"><span data-stu-id="34c5f-136">Sign in to the [Microsoft 365 admin center](https://admin.microsoft.com).</span></span>

2. <span data-ttu-id="34c5f-137">Sous le nouvel onglet **Centre d’administration Microsoft 365** de votre navigateur, cliquez sur **Utilisateurs**.</span><span class="sxs-lookup"><span data-stu-id="34c5f-137">From the new **Microsoft 365 admin center** tab of your browser, click **Users**.</span></span>

3. <span data-ttu-id="34c5f-138">Dans la liste des utilisateurs, cliquez sur **PDG**.</span><span class="sxs-lookup"><span data-stu-id="34c5f-138">In the list of users, click **CEO**.</span></span>

4. <span data-ttu-id="34c5f-139">Dans le volet qui affiche les propriétés du compte d’utilisateur **PDG**, vérifiez que les licences **Microsoft 365 Entreprise E5** lui ont été affectées dans les **Licences de produit**.</span><span class="sxs-lookup"><span data-stu-id="34c5f-139">In the pane that lists the properties of the **CEO** user account, verify that it has been assigned the **Microsoft 365 Enterprise E5** license in **Product licenses**.</span></span>

## <a name="phase-3-create-your-team"></a><span data-ttu-id="34c5f-140">Phase 3 : créer votre équipe</span><span class="sxs-lookup"><span data-stu-id="34c5f-140">Phase 3: Create your team</span></span>

<span data-ttu-id="34c5f-141">Au cours de cette phase, vous créez et configurez une équipe avec l’isolation des problèmes de sécurité pour les membres de l’équipe de direction afin de collaborer sur la stratégie de l’entreprise.</span><span class="sxs-lookup"><span data-stu-id="34c5f-141">In this phase, you create and configure a team with security isolation for members of the senior leadership team to collaborate on company strategy.</span></span>

<span data-ttu-id="34c5f-142">Veillez tout d’abord à activer [étiquettes de confidentialité pour protéger le contenu de Microsoft Teams, des groupes Office 365 et des sites SharePoint](../compliance/sensitivity-labels-teams-groups-sites.md) avant de passer aux étapes décrites dans cet article.</span><span class="sxs-lookup"><span data-stu-id="34c5f-142">First, enable sensitivity labels to protect content in Microsoft Teams, Office 365 groups, and SharePoint sites before you proceed with the steps in [this article](../compliance/sensitivity-labels-teams-groups-sites.md).</span></span>

<span data-ttu-id="34c5f-143">Ensuite, créez l’équipe :</span><span class="sxs-lookup"><span data-stu-id="34c5f-143">Next, create the team:</span></span>

1. <span data-ttu-id="34c5f-144">Dans Teams, cliquez sur **Teams** sur le côté gauche de l’application, puis cliquez sur **Rejoindre ou créer une équipe** en bas de la liste des équipes.</span><span class="sxs-lookup"><span data-stu-id="34c5f-144">In Teams, click **Teams** on the left side of the app, then click **Join or create a team** at the bottom of the teams list.</span></span>
2. <span data-ttu-id="34c5f-145">Cliquez sur **Créer une équipe** (première carte, coin supérieur gauche).</span><span class="sxs-lookup"><span data-stu-id="34c5f-145">Click **Create team** (first card, top left corner).</span></span>
3. <span data-ttu-id="34c5f-146">Sélectionnez **Créer une équipe à partir de zéro**.</span><span class="sxs-lookup"><span data-stu-id="34c5f-146">Choose **Build a team from scratch**.</span></span>
4. <span data-ttu-id="34c5f-147">Dans la liste **Sensibilité**, conservez la valeur par défaut.</span><span class="sxs-lookup"><span data-stu-id="34c5f-147">In the **Sensitivity** list, keep the default.</span></span>
5. <span data-ttu-id="34c5f-148">Sous **Confidentialité**, cliquez sur **Privée**.</span><span class="sxs-lookup"><span data-stu-id="34c5f-148">Under **Privacy**, click **Private**.</span></span>
6. <span data-ttu-id="34c5f-149">Tapez **Stratégie d’entreprise**, puis cliquez sur **Créer** > **Fermer**.</span><span class="sxs-lookup"><span data-stu-id="34c5f-149">Type **Company Strategy**, and then click **Create** > **Close**.</span></span>

<span data-ttu-id="34c5f-150">Restreignez ensuite la création de canaux privés aux propriétaires du groupe stratégie de l’entreprise.</span><span class="sxs-lookup"><span data-stu-id="34c5f-150">Next, restrict the creation of private channels to owners of the Company Strategy group.</span></span>

1. <span data-ttu-id="34c5f-151">Dans l’équipe, cliquez sur **Autres options**, puis cliquez sur **Gérer l’équipe**.</span><span class="sxs-lookup"><span data-stu-id="34c5f-151">In the team, click **More options**, and then click **Manage team**.</span></span>
2. <span data-ttu-id="34c5f-152">Sous l’onglet **Paramètres**, développez **Autorisations de membre**.</span><span class="sxs-lookup"><span data-stu-id="34c5f-152">On the **Settings** tab, expand **Member permissions**.</span></span>
3. <span data-ttu-id="34c5f-153">Désactivez la case à cocher **Autoriser les membres à créer des canaux privés**.</span><span class="sxs-lookup"><span data-stu-id="34c5f-153">Clear the **Allow members to create private channels** check box.</span></span>

<span data-ttu-id="34c5f-154">Vous devez ensuite configurer une étiquette de confidentialité avec les paramètres suivants :</span><span class="sxs-lookup"><span data-stu-id="34c5f-154">Next, you need to configure a sensitivity label with the following settings:</span></span>

- <span data-ttu-id="34c5f-155">Le nom est stratégie d’entreprise</span><span class="sxs-lookup"><span data-stu-id="34c5f-155">The name is Company Strategy</span></span>
- <span data-ttu-id="34c5f-156">Le chiffrement est activé</span><span class="sxs-lookup"><span data-stu-id="34c5f-156">Encryption is enabled</span></span>
- <span data-ttu-id="34c5f-157">Le groupe Stratégie de l’entreprise possède des autorisations de co-création</span><span class="sxs-lookup"><span data-stu-id="34c5f-157">The Company Strategy group has Co-Author permissions</span></span>

<span data-ttu-id="34c5f-158">Procédez comme suit :</span><span class="sxs-lookup"><span data-stu-id="34c5f-158">Follow these steps:</span></span>

1. <span data-ttu-id="34c5f-159">Ouvrez le [Centre de conformité Microsoft 365](https://compliance.microsoft.com).</span><span class="sxs-lookup"><span data-stu-id="34c5f-159">Open the [Microsoft 365 compliance center](https://compliance.microsoft.com).</span></span>
2. <span data-ttu-id="34c5f-160">Sous **Solutions**, cliquez sur **Protection des informations**.</span><span class="sxs-lookup"><span data-stu-id="34c5f-160">Under **Solutions**, click **Information protection**.</span></span>
3. <span data-ttu-id="34c5f-161">Cliquez sur **Créer une étiquette**.</span><span class="sxs-lookup"><span data-stu-id="34c5f-161">Click **Create a label**.</span></span>
4. <span data-ttu-id="34c5f-162">Tapez **Stratégie d’entreprise** comme nom d’étiquette.</span><span class="sxs-lookup"><span data-stu-id="34c5f-162">Type **Company Strategy** for the label name.</span></span>
5. <span data-ttu-id="34c5f-163">Tapez **Documents de stratégie de la direction de l’entreprise** sous forme d’info-bulle, puis cliquez **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="34c5f-163">Type **Senior leadership company strategy documents** as the tool tip, and then click **Next**.</span></span>
6. <span data-ttu-id="34c5f-164">Sur la page **Chiffrement**, dans le menu déroulant **Chiffrement**, sélectionnez **Appliquer**.</span><span class="sxs-lookup"><span data-stu-id="34c5f-164">On the **Encryption** page, in the **Encryption** dropdown, choose **Apply**.</span></span>
7. <span data-ttu-id="34c5f-165">Pour ajouter des autorisations d’équipe :</span><span class="sxs-lookup"><span data-stu-id="34c5f-165">To add the team permissions:</span></span><br>
  <span data-ttu-id="34c5f-166">a.</span><span class="sxs-lookup"><span data-stu-id="34c5f-166">a.</span></span> <span data-ttu-id="34c5f-167">Cliquez sur **Attribuer des autorisations**.</span><span class="sxs-lookup"><span data-stu-id="34c5f-167">Click **Assign permissions**.</span></span><br>
  <span data-ttu-id="34c5f-168">b.</span><span class="sxs-lookup"><span data-stu-id="34c5f-168">b.</span></span> <span data-ttu-id="34c5f-169">Cliquez sur **Ajouter des utilisateurs ou des groupes**, sélectionnez l’équipe que vous avez créée, puis cliquez sur **Stratégie d’entreprise**, enfin cliquez sur **Ajouter**.</span><span class="sxs-lookup"><span data-stu-id="34c5f-169">Click **Add users or groups**, select **Company Strategy**, and then click **Add**.</span></span><br>
  <span data-ttu-id="34c5f-170">c.</span><span class="sxs-lookup"><span data-stu-id="34c5f-170">c.</span></span> <span data-ttu-id="34c5f-171">Cliquez sur **Choisir les autorisations**.</span><span class="sxs-lookup"><span data-stu-id="34c5f-171">Click **Choose permissions**.</span></span><br>
  <span data-ttu-id="34c5f-172">d.</span><span class="sxs-lookup"><span data-stu-id="34c5f-172">d.</span></span> <span data-ttu-id="34c5f-173">Sélectionnez **Co-auteur** dans la liste déroulante, puis cliquez sur **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="34c5f-173">Choose **Co-Author** from the dropdown list, and then click **Save**.</span></span><br>
8. <span data-ttu-id="34c5f-174">Cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="34c5f-174">Click **Next**.</span></span>
9. <span data-ttu-id="34c5f-175">Dans la page **Marque de contenu**, cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="34c5f-175">On the **Content marking** page, click **Next**.</span></span>
10. <span data-ttu-id="34c5f-176">Dans la page **Paramètres de site et de groupe**, configurez **Paramètres de site et de groupe** sur **Activé**.</span><span class="sxs-lookup"><span data-stu-id="34c5f-176">On the **Site and group settings** page, set **Site and group settings** to **On**.</span></span>
11. <span data-ttu-id="34c5f-177">Dans la liste déroulante **Confidentialité de sites d’équipe Office 365 connectés à un groupe**, sélectionnez **Privé : seuls les membres peuvent accéder au site**.</span><span class="sxs-lookup"><span data-stu-id="34c5f-177">In the **Privacy of Office 365 group-connected team sites** dropdown, choose **Private - only members can access the site**.</span></span>
12. <span data-ttu-id="34c5f-178">Sous **Appareils non gérés**, sélectionnez **Bloquer l’accès**.</span><span class="sxs-lookup"><span data-stu-id="34c5f-178">Under **Unmanaged devices**, choose **Block access**.</span></span>
13. <span data-ttu-id="34c5f-179">Cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="34c5f-179">Click **Next**.</span></span>
14. <span data-ttu-id="34c5f-180">Dans la page **Étiquetage automatique pour les applications Office**, cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="34c5f-180">On the **Auto-labeling for Office apps** page, click **Next**.</span></span>
15. <span data-ttu-id="34c5f-181">Cliquez sur **Envoyer**, puis sur **Terminé**.</span><span class="sxs-lookup"><span data-stu-id="34c5f-181">Click **Submit**, and then click **Done**.</span></span>

<span data-ttu-id="34c5f-182">Ensuite, publiez la nouvelle étiquette en procédant comme suit :</span><span class="sxs-lookup"><span data-stu-id="34c5f-182">Next, publish the new label with these steps:</span></span>

1. <span data-ttu-id="34c5f-183">Dans le Centre de conformité Microsoft 365, dans la page **protection des informations**, sélectionnez l’onglet **Stratégies d’étiquette**.</span><span class="sxs-lookup"><span data-stu-id="34c5f-183">In the Microsoft 365 compliance center, on the **Information protection** page, choose the **Label policies** tab.</span></span>
2. <span data-ttu-id="34c5f-184">Cliquez sur **Publier des étiquettes**.</span><span class="sxs-lookup"><span data-stu-id="34c5f-184">Click **Publish labels**.</span></span>
3. <span data-ttu-id="34c5f-185">Dans la page **Choisir des étiquettes de confidentialité à publier**, cliquez sur **Choisir des étiquettes de confidentialité à publier**.</span><span class="sxs-lookup"><span data-stu-id="34c5f-185">On the **Choose sensitivity labels to publish** page, click **Choose sensitivity labels to publish**.</span></span>
4. <span data-ttu-id="34c5f-186">Sélectionnez **Stratégie d’entreprise**, puis cliquez sur **Ajouter**.</span><span class="sxs-lookup"><span data-stu-id="34c5f-186">Select **Company Strategy**, and then click **Add**.</span></span>
5. <span data-ttu-id="34c5f-187">Cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="34c5f-187">Click **Next**.</span></span>
6. <span data-ttu-id="34c5f-188">Dans la page **Publier pour les utilisateurs et groupes**, cliquez sur **Choisir les utilisateurs et les groupes**.</span><span class="sxs-lookup"><span data-stu-id="34c5f-188">On the **Publish to users and groups** page, click **Choose users and groups**.</span></span>
7. <span data-ttu-id="34c5f-189">Cliquez sur **Ajouter**, puis sélectionnez **Stratégie d’entreprise**.</span><span class="sxs-lookup"><span data-stu-id="34c5f-189">Click **Add**, and then select **Company Strategy**.</span></span>
8. <span data-ttu-id="34c5f-190">Cliquez sur **Ajouter**, puis sur **Terminé**.</span><span class="sxs-lookup"><span data-stu-id="34c5f-190">Click **Add**, and then click **Done**.</span></span>
9. <span data-ttu-id="34c5f-191">Cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="34c5f-191">Click **Next**.</span></span>
10. <span data-ttu-id="34c5f-192">Dans la page Paramètres de stratégie, activez la case à cocher **Les utilisateurs doivent fournir une justification pour supprimer une étiquette ou une étiquette de classification inférieure**, puis cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="34c5f-192">On the Policy settings page, select the **Users must provide justification to remove a label or lower classification label** check box, and then click **Next**.</span></span>
11. <span data-ttu-id="34c5f-193">Tapez **Stratégie d’entreprise** comme nom de stratégie, puis cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="34c5f-193">Type **Company Strategy** for the policy name, and then click **Next**.</span></span>
12. <span data-ttu-id="34c5f-194">Cliquez sur **Envoyer**, puis cliquez sur **Terminé**.</span><span class="sxs-lookup"><span data-stu-id="34c5f-194">Click **Submit** and then click **Done**.</span></span>

<span data-ttu-id="34c5f-195">La **Stratégie d’entreprise** peut prendre un certain temps avant de devenir disponible une fois qu'elle a été publiée.</span><span class="sxs-lookup"><span data-stu-id="34c5f-195">It may take some time for the **Company Strategy** label to become available after it's been published.</span></span>

<span data-ttu-id="34c5f-196">Ensuite, appliquez votre nouvelle étiquette à l’équipe **Stratégie d’entreprise** et mettez à jour le type de lien de partage par défaut pour réduire le risque de partager accidentellement des fichiers et des dossiers avec un public plus large que prévu.</span><span class="sxs-lookup"><span data-stu-id="34c5f-196">Next, apply your new label to the **Company Strategy** team and update the default sharing link type to reduce the risk of accidentally sharing files and folders to a wider audience than intended.</span></span>

1. <span data-ttu-id="34c5f-197">Ouvrez le [Centre d’administration SharePoint](https://admin.microsoft.com/sharepoint).</span><span class="sxs-lookup"><span data-stu-id="34c5f-197">Open the [SharePoint admin center](https://admin.microsoft.com/sharepoint).</span></span>
2. <span data-ttu-id="34c5f-198">Sous **Sites**, cliquez sur **Sites actifs**.</span><span class="sxs-lookup"><span data-stu-id="34c5f-198">Under **Sites**, click **Active sites**.</span></span>
3. <span data-ttu-id="34c5f-199">Cliquez sur la **Stratégie d’entreprise** .</span><span class="sxs-lookup"><span data-stu-id="34c5f-199">Click the **Company Strategy** site.</span></span>
4. <span data-ttu-id="34c5f-200">Sous l’onglet **Stratégies**, sous **Confidentialité**, cliquez sur **Modifier**.</span><span class="sxs-lookup"><span data-stu-id="34c5f-200">On the **Policies** tab, under **Sensitivity**, click **Edit**.</span></span>
5. <span data-ttu-id="34c5f-201">Sélectionnez l’étiquette **Stratégie d’entreprise**, puis cliquez sur **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="34c5f-201">Select the **Company Strategy** label, and then click **Save**.</span></span>
6. <span data-ttu-id="34c5f-202">Sous l’onglet **Stratégies**, sous **Partage externe**, cliquez sur **Modifier**.</span><span class="sxs-lookup"><span data-stu-id="34c5f-202">On the **Policies** tab, under **External sharing**, click **Edit**.</span></span>
5. <span data-ttu-id="34c5f-203">Choisissez **Uniquement les personnes de votre organisation**.</span><span class="sxs-lookup"><span data-stu-id="34c5f-203">Choose **Only people in your organization**.</span></span>
6. <span data-ttu-id="34c5f-204">Sous Type de lien de **Partage par défaut**, désactivez la case à cocher **Identique au paramètre de niveau organisation**, puis sélectionnez **Personnes disposant d’un accès existant**.</span><span class="sxs-lookup"><span data-stu-id="34c5f-204">Under **Default sharing** link type, clear the **Same as organization-level setting** check box, and select **People with existing access**.</span></span>
7. <span data-ttu-id="34c5f-205">Cliquez sur **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="34c5f-205">Click **Save**.</span></span>

<span data-ttu-id="34c5f-206">Ensuite, configurez le partage de sites aux propriétaires uniquement pour l’équipe de **Stratégie d’entreprise**.</span><span class="sxs-lookup"><span data-stu-id="34c5f-206">Next, configure owners-only site sharing for the **Company Strategy** team.</span></span>

1. <span data-ttu-id="34c5f-207">Dans Teams, accédez à l’onglet **Général** de l’équipe de la **Stratégie d’entreprise**.</span><span class="sxs-lookup"><span data-stu-id="34c5f-207">In Teams, navigate to the **General** tab of the **Company Strategy** team.</span></span>
2. <span data-ttu-id="34c5f-208">Dans la barre d’outils de l’équipe, cliquez sur **Fichiers**.</span><span class="sxs-lookup"><span data-stu-id="34c5f-208">In the tool bar for the team, click **Files**.</span></span>
3. <span data-ttu-id="34c5f-209">Cliquez sur les points de suspension, puis sur **Ouvrir dans SharePoint**.</span><span class="sxs-lookup"><span data-stu-id="34c5f-209">Click the ellipsis, and then click **Open in SharePoint**.</span></span>
4. <span data-ttu-id="34c5f-210">Dans la barre d’outils du site SharePoint sous-jacent, cliquez sur l’icône Paramètres, puis cliquez sur **Autorisations du site**.</span><span class="sxs-lookup"><span data-stu-id="34c5f-210">In the tool bar of the underlying SharePoint site, click the settings icon, and then click **Site permissions**.</span></span>
5. <span data-ttu-id="34c5f-211">Dans le volet Autorisations de site, sous le **Site de partage**, cliquez sur **Modifier les modalités de partage par les membres**.</span><span class="sxs-lookup"><span data-stu-id="34c5f-211">In the Site permissions pane, under **Site Sharing**, click **Change how members can share**.</span></span>
6. <span data-ttu-id="34c5f-212">Sous **Autorisations de partage**, sélectionnez **Seuls les propriétaires du site peuvent partager des fichiers, des dossiers et le site**, puis cliquez sur **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="34c5f-212">Under **Sharing permissions**, choose **Only site owners can share files, folders, and the site**, and then click **Save**.</span></span>
7. <span data-ttu-id="34c5f-213">Fermez les volets **Autorisations** et **Paramètres**.</span><span class="sxs-lookup"><span data-stu-id="34c5f-213">Close the **Permissions** and **Settings** panes.</span></span>

<span data-ttu-id="34c5f-214">Si vous vous connectez en tant que membre du groupe **Stratégie d’entreprise**, la nouvelle étiquette apparaît dans l’option **Confidentialité** de la barre d’outils Accueil de Word, Excel et PowerPoint.</span><span class="sxs-lookup"><span data-stu-id="34c5f-214">If you sign in as a member of the Company Strategy group, you will see **Company Strategy** in the **Sensitivity** option in the Home toolbar of Word, Excel, and PowerPoint.</span></span> <span data-ttu-id="34c5f-215">Sélectionnez l’étiquette **Stratégie d’entreprise** à partir de l’option **Confidentialité** pour affecter l’étiquette à un fichier.</span><span class="sxs-lookup"><span data-stu-id="34c5f-215">Select the **Company Strategy** label from the **Sensitivity** option to assign the label to a file.</span></span>

<span data-ttu-id="34c5f-216">Voici la configuration obtenue pour l’équipe Stratégie d’entreprise.</span><span class="sxs-lookup"><span data-stu-id="34c5f-216">Here is the resulting configuration for the Company Strategy team.</span></span>

![Configuration de la stratégie d’entreprise pour l’équipe isolée](../media/team-security-isolation-dev-test/team-security-isolation-dev-test-config.png)

## <a name="next-step"></a><span data-ttu-id="34c5f-218">Étape suivante</span><span class="sxs-lookup"><span data-stu-id="34c5f-218">Next step</span></span>

<span data-ttu-id="34c5f-219">Lorsque vous êtes prêt pour le déploiement en production, consultez ces [instructions de configuration](secure-teams-security-isolation.md).</span><span class="sxs-lookup"><span data-stu-id="34c5f-219">When you're ready for production deployment, see these [configuration instructions](secure-teams-security-isolation.md).</span></span>
