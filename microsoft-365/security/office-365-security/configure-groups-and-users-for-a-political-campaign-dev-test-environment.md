---
title: Configuration de groupes et d’utilisateurs pour un environnement de développement/test pour une campagne politique
f1.keywords:
- NOCSH
ms.author: josephd
author: JoeDavies-MSFT
manager: laurawi
ms.date: 12/15/2017
audience: ITPro
ms.topic: article
ms.collection:
- Ent_O365
- Strat_O365_Enterprise
ms.service: O365-seccomp
localization_priority: Priority
search.appverid:
- MET150
ms.assetid: 0e22bcf3-bad3-42a4-b44f-276e0cf4790f
description: 'Résumé : Créez des abonnements d’essai Office 365 et Enterprise Mobility + Security (EMS) avec des utilisateurs et des groupes pour un environnement de développement/test de campagne électorale.'
ms.openlocfilehash: a61cc21b67cafd213d47076698929d0aa2644d08
ms.sourcegitcommit: 3dd9944a6070a7f35c4bc2b57df397f844c3fe79
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/15/2020
ms.locfileid: "42083483"
---
# <a name="configure-groups-and-users-for-a-political-campaign-devtest-environment"></a><span data-ttu-id="98a37-103">Configuration de groupes et d’utilisateurs pour un environnement de développement/test pour une campagne électorale</span><span class="sxs-lookup"><span data-stu-id="98a37-103">Configure groups and users for a political campaign dev/test environment</span></span>

 <span data-ttu-id="98a37-104">\*\*Résumé : \*\* Créez des abonnements d’essai Office 365 et Enterprise Mobility + Security (EMS) avec des utilisateurs et des groupes pour un environnement de développement/test de campagne électorale.</span><span class="sxs-lookup"><span data-stu-id="98a37-104">**Summary:** Create Office 365 and Enterprise Mobility + Security (EMS) trial subscriptions with users and groups for a political campaign dev/test environment.</span></span>

<span data-ttu-id="98a37-105">Suivez les instructions de cet article pour créer un environnement de développement/test incluant des comptes d’utilisateurs simplifiés et des groupes pour la solution des [conseils de sécurité Microsoft pour les campagnes électorales, les organisations à but non lucratif et d’autres organisations souples](microsoft-security-guidance-for-political-campaigns-nonprofits-and-other-agile-o.md).</span><span class="sxs-lookup"><span data-stu-id="98a37-105">Use the instructions in this article to create a dev/test environment that includes simplified user accounts and groups for the [Microsoft Security Guidance for Political Campaigns, Nonprofits, and Other Agile Organizations](microsoft-security-guidance-for-political-campaigns-nonprofits-and-other-agile-o.md) solution.</span></span>

## <a name="phase-1-create-your-office-365-devtest-environment"></a><span data-ttu-id="98a37-106">Phase 1 : Création d’un environnement de développement/test Office 365</span><span class="sxs-lookup"><span data-stu-id="98a37-106">Phase 1: Create your Office 365 dev/test environment</span></span>

<span data-ttu-id="98a37-107">Dans cette phase, vous obtenez des abonnements d’essai pour Office 365 E5 et Enterprise Mobility + Security (EMS) E5 pour une entreprise fictive qui représente une campagne électorale.</span><span class="sxs-lookup"><span data-stu-id="98a37-107">In this phase, you obtain trial subscriptions for Office 365 E5 and Enterprise Mobility + Security (EMS) E5 for a fictional organization that represents a political campaign.</span></span>

<span data-ttu-id="98a37-108">Suivez d’abord les instructions de la **Phase 2** de l’[environnement de développement/test Office 365](https://docs.microsoft.com/office365/enterprise/office-365-dev-test-environment).</span><span class="sxs-lookup"><span data-stu-id="98a37-108">First, follow the instructions in **Phase 2** of the [Office 365 dev/test environment](https://docs.microsoft.com/office365/enterprise/office-365-dev-test-environment).</span></span>

<span data-ttu-id="98a37-109">Ensuite, inscrivez-vous à l’abonnement d’évaluation EMS E5 et ajoutez-le à la même organisation que votre abonnement d’évaluation Office 365.</span><span class="sxs-lookup"><span data-stu-id="98a37-109">Next, sign up for the EMS E5 trial subscription and add it to the same organization as your Office 365 trial subscription.</span></span>

1. <span data-ttu-id="98a37-110">Si nécessaire, connectez-vous au centre d’administration avec les identifiants du compte d’administrateur général de votre abonnement d’essai.</span><span class="sxs-lookup"><span data-stu-id="98a37-110">If needed, sign in to the admin center with the credentials of the global administrator account of your trial subscription.</span></span> <span data-ttu-id="98a37-111">Pour obtenir de l’aide, consultez [Où se connecter à Office 365](https://support.office.com/article/e9eb7d51-5430-4929-91ab-6157c5a050b4).</span><span class="sxs-lookup"><span data-stu-id="98a37-111">For help, see [Where to sign in to Office 365](https://support.office.com/article/e9eb7d51-5430-4929-91ab-6157c5a050b4).</span></span>

2. <span data-ttu-id="98a37-112">Cliquez sur la vignette **Administration**.</span><span class="sxs-lookup"><span data-stu-id="98a37-112">Click the **Admin** tile.</span></span>

3. <span data-ttu-id="98a37-113">Sous l’onglet **Centre d’administration Microsoft 365** de votre navigateur, dans le volet de navigation gauche, cliquez sur **Facturation > Acheter des services**.</span><span class="sxs-lookup"><span data-stu-id="98a37-113">On the **Microsoft 365 admin center** tab in your browser, in the left navigation, click **Billing > Purchase services**.</span></span>

4. <span data-ttu-id="98a37-p102">Dans la page **Acheter des services**, recherchez l’élément **Enterprise Mobility + Security E5**. Pointez votre souris dessus et cliquez sur **Démarrer l’essai gratuit**.</span><span class="sxs-lookup"><span data-stu-id="98a37-p102">On the **Purchase services** page, find the **Enterprise Mobility + Security E5** item. Hover your mouse pointer over it and click **Start free trial**.</span></span>

5. <span data-ttu-id="98a37-116">Dans la page **Confirmer votre commande**, cliquez sur **Essayer maintenant**.</span><span class="sxs-lookup"><span data-stu-id="98a37-116">On the **Confirm your order** page, click **Try now**.</span></span>

6. <span data-ttu-id="98a37-117">Dans la page **Réception de la commande**, cliquez sur **Continuer**.</span><span class="sxs-lookup"><span data-stu-id="98a37-117">On the **Order receipt** page, click **Continue**.</span></span>

<span data-ttu-id="98a37-118">Ensuite, activez la licence EMS E5 pour votre compte Administrateur général.</span><span class="sxs-lookup"><span data-stu-id="98a37-118">Next, enable the EMS E5 license for your global administrator account.</span></span>

1. <span data-ttu-id="98a37-119">Sous l’onglet **Centre d’administration Microsoft 365** de votre navigateur, dans le volet de navigation gauche, cliquez sur **Utilisateurs > Utilisateurs actifs**.</span><span class="sxs-lookup"><span data-stu-id="98a37-119">On the **Microsoft 365 admin center** tab in your browser, in the left navigation, click **Users > Active users**.</span></span>

2. <span data-ttu-id="98a37-120">Cliquez sur votre compte Administrateur général, puis cliquez sur **Modifier** pour les **licences de produit**.</span><span class="sxs-lookup"><span data-stu-id="98a37-120">Click your global administrator account, and then click **Edit** for **Product licenses**.</span></span>

3. <span data-ttu-id="98a37-121">Dans le volet **Licences de produit**, activez la licence de produit pour **Enterprise Mobility + Security E5** en sélectionnant **Activer**, cliquez sur **Enregistrer**, cliquez deux fois sur **Fermer**.</span><span class="sxs-lookup"><span data-stu-id="98a37-121">On the **Product licenses** pane, turn the product license for **Enterprise Mobility + Security E5** to **On**, click **Save,** and then click **Close** twice.</span></span>

## <a name="phase-2-create-and-configure-your-azure-active-directory-ad-groups"></a><span data-ttu-id="98a37-122">Phase 2 : Création et configuration de vos groupes Azure Active Directory (AD)</span><span class="sxs-lookup"><span data-stu-id="98a37-122">Phase 2: Create and configure your Azure Active Directory (AD) groups</span></span>

<span data-ttu-id="98a37-123">Dans cette phase, vous créez et configurez des groupes Azure AD pour votre campagne.</span><span class="sxs-lookup"><span data-stu-id="98a37-123">In this phase, you create and configure the Azure AD groups for your campaign.</span></span>

<span data-ttu-id="98a37-124">Commencez par créer un ensemble de groupes pour une campagne électorale standard avec le portail Azure.</span><span class="sxs-lookup"><span data-stu-id="98a37-124">First, create a set of groups for a typical political campaign with the Azure portal.</span></span>

1. <span data-ttu-id="98a37-p103">Dans un onglet distinct dans votre navigateur, accédez au portail Azure à l’adresse [https://portal.azure.com](https://portal.azure.com). Si nécessaire, connectez-vous avec les informations d’identification du compte Administrateur général de votre abonnement d’essai Office 365 E5.</span><span class="sxs-lookup"><span data-stu-id="98a37-p103">On a separate tab in your browser, go to the Azure portal at [https://portal.azure.com](https://portal.azure.com). If needed, sign in with the credentials of the global administrator account for your Office 365 E5 trial subscription.</span></span>

2. <span data-ttu-id="98a37-127">Dans le portail Azure, cliquez sur **Azure Active Directory > Utilisateurs et groupes > Tous les groupes**.</span><span class="sxs-lookup"><span data-stu-id="98a37-127">In the Azure portal, click **Azure Active Directory > Users and groups > All groups**.</span></span>

3. <span data-ttu-id="98a37-128">Procédez comme suit pour chaque nom de groupe dans cette liste :</span><span class="sxs-lookup"><span data-stu-id="98a37-128">Do the following steps for each group name in this list:</span></span>

   - <span data-ttu-id="98a37-129">Senior and strategic staff</span><span class="sxs-lookup"><span data-stu-id="98a37-129">Senior and strategic staff</span></span>

   - <span data-ttu-id="98a37-130">IT staff</span><span class="sxs-lookup"><span data-stu-id="98a37-130">IT staff</span></span>

   - <span data-ttu-id="98a37-131">Analytics staff</span><span class="sxs-lookup"><span data-stu-id="98a37-131">Analytics staff</span></span>

   - <span data-ttu-id="98a37-132">Regular core staff</span><span class="sxs-lookup"><span data-stu-id="98a37-132">Regular core staff</span></span>

   - <span data-ttu-id="98a37-133">Operations staff</span><span class="sxs-lookup"><span data-stu-id="98a37-133">Operations staff</span></span>

   - <span data-ttu-id="98a37-134">Field staff</span><span class="sxs-lookup"><span data-stu-id="98a37-134">Field staff</span></span>

1. <span data-ttu-id="98a37-135">Dans le panneau **Tous les groupes**, cliquez sur **+ Nouveau groupe**.</span><span class="sxs-lookup"><span data-stu-id="98a37-135">On the **All groups** blade, click **+ New group**.</span></span>

2. <span data-ttu-id="98a37-136">Tapez le nom du groupe de la liste dans **Nom**.</span><span class="sxs-lookup"><span data-stu-id="98a37-136">Type the group name from the list in **Name**.</span></span>

3. <span data-ttu-id="98a37-137">Sélectionnez **Utilisateur dynamique** dans **Appartenance**.</span><span class="sxs-lookup"><span data-stu-id="98a37-137">Select **Dynamic user** in **Membership**.</span></span>

4. <span data-ttu-id="98a37-138">Cliquez sur **Oui** pour **Activer les fonctionnalités Office**.</span><span class="sxs-lookup"><span data-stu-id="98a37-138">Click **Yes** for **Enable Office features**.</span></span>

5. <span data-ttu-id="98a37-139">Cliquez sur **Ajouter une requête dynamique**.</span><span class="sxs-lookup"><span data-stu-id="98a37-139">Click **Add dynamic query**.</span></span>

6. <span data-ttu-id="98a37-140">Dans **Ajouter des utilisateurs où**, sélectionnez **Service**.</span><span class="sxs-lookup"><span data-stu-id="98a37-140">In **Add users where**, select **department**.</span></span>

7. <span data-ttu-id="98a37-141">Dans le champ suivant, sélectionnez **Est égal à**.</span><span class="sxs-lookup"><span data-stu-id="98a37-141">In the next field, select **Equals**.</span></span>

8. <span data-ttu-id="98a37-142">Dans le champ suivant, tapez le nom du groupe de la liste.</span><span class="sxs-lookup"><span data-stu-id="98a37-142">In the next field, type the group name from the list.</span></span>

9. <span data-ttu-id="98a37-143">Cliquez sur **Ajouter une requête**, puis cliquez sur **Créer**.</span><span class="sxs-lookup"><span data-stu-id="98a37-143">Click **Add query**, and then click **Create**.</span></span>

10. <span data-ttu-id="98a37-144">Cliquez sur **Utilisateurs et groupes - Tous les groupes**.</span><span class="sxs-lookup"><span data-stu-id="98a37-144">Click **Users and groups - All groups**.</span></span>

<span data-ttu-id="98a37-145">Ensuite, vous configurez les groupes afin que des licences Office 365 E5 et EMS E5 soient attribuées automatiquement aux membres.</span><span class="sxs-lookup"><span data-stu-id="98a37-145">Next, you configure the groups so that members are automatically assigned Office 365 E5 and EMS E5 licenses.</span></span>

1. <span data-ttu-id="98a37-146">Dans le portail Azure, cliquez sur **Azure Active Directory > Licences > Tous les produits**.</span><span class="sxs-lookup"><span data-stu-id="98a37-146">In the Azure portal, click **Azure Active Directory > Licenses > All products**.</span></span>

2. <span data-ttu-id="98a37-147">Dans la liste, sélectionnez **Enterprise Mobility + Security E5** et **Office 365 Entreprise E5**, puis cliquez sur **+ Affecter**.</span><span class="sxs-lookup"><span data-stu-id="98a37-147">In the list, select **Enterprise Mobility + Security E5** and **Office 365 Enterprise E5**, and then click **+ Assign**.</span></span>

3. <span data-ttu-id="98a37-148">Dans le panneau **Affecter une licence**, cliquez sur **Utilisateurs et groupes**.</span><span class="sxs-lookup"><span data-stu-id="98a37-148">In the **Assign license** blade, click **Users and groups**.</span></span>

4. <span data-ttu-id="98a37-149">Dans la liste des groupes, sélectionnez les éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="98a37-149">In the list of groups, select the following:</span></span>

   - <span data-ttu-id="98a37-150">Analytics staff</span><span class="sxs-lookup"><span data-stu-id="98a37-150">Analytics staff</span></span>

   - <span data-ttu-id="98a37-151">Field staff</span><span class="sxs-lookup"><span data-stu-id="98a37-151">Field staff</span></span>

   - <span data-ttu-id="98a37-152">IT staff</span><span class="sxs-lookup"><span data-stu-id="98a37-152">IT staff</span></span>

   - <span data-ttu-id="98a37-153">Operations staff</span><span class="sxs-lookup"><span data-stu-id="98a37-153">Operations staff</span></span>

   - <span data-ttu-id="98a37-154">Regular core staff</span><span class="sxs-lookup"><span data-stu-id="98a37-154">Regular core staff</span></span>

   - <span data-ttu-id="98a37-155">Senior and strategic staff</span><span class="sxs-lookup"><span data-stu-id="98a37-155">Senior and strategic staff</span></span>

5. <span data-ttu-id="98a37-156">Cliquez sur **Sélectionner**, puis sur **Affecter**.</span><span class="sxs-lookup"><span data-stu-id="98a37-156">Click **Select**, and then click **Assign**.</span></span>

6. <span data-ttu-id="98a37-157">Fermez l’onglet du portail Azure dans votre navigateur.</span><span class="sxs-lookup"><span data-stu-id="98a37-157">Close the Azure portal tab in your browser.</span></span>

## <a name="phase-3-add-your-user-accounts"></a><span data-ttu-id="98a37-158">Phase 3 : Ajout de comptes d’utilisateurs</span><span class="sxs-lookup"><span data-stu-id="98a37-158">Phase 3: Add your user accounts</span></span>

<span data-ttu-id="98a37-159">Dans cette phase, vous ajoutez les comptes d’utilisateurs de l’exemple pour votre campagne politique.</span><span class="sxs-lookup"><span data-stu-id="98a37-159">In this phase, you add the example user accounts for your political campaign.</span></span>

<span data-ttu-id="98a37-160">Pour commencer, [connectez -vous au module PowerShell Azure Active Directory pour le module Graphique](https://docs.microsoft.com/office365/enterprise/powershell/connect-to-office-365-powershell#connect-with-the-azure-active-directory-powershell-for-graph-module).</span><span class="sxs-lookup"><span data-stu-id="98a37-160">First, you [Connect with the Azure Active Directory PowerShell for Graph module](https://docs.microsoft.com/office365/enterprise/powershell/connect-to-office-365-powershell#connect-with-the-azure-active-directory-powershell-for-graph-module).</span></span>

<span data-ttu-id="98a37-161">Ensuite, renseignez le nom de votre organisation, votre emplacement et un mot de passe commun, puis exécutez les commandes suivantes à partir de l’invite de commandes PowerShell ou de l’environnement de script intégré (ISE) :</span><span class="sxs-lookup"><span data-stu-id="98a37-161">Next, you fill in your organization name, your location, and a common password, and then run these commands from the PowerShell command prompt or Integrated Script Environment (ISE):</span></span>

```powershell
$orgName="<organization name, such as contoso for the contoso.onmicrosoft.com trial subscription domain name>"
$location="<the ISO ALPHA2 country code, such as US for the United States>"
$commonPassword="<common password for all the new accounts>"

$PasswordProfile=New-Object -TypeName Microsoft.Open.AzureAD.Model.PasswordProfile
$PasswordProfile.Password=$commonPassword

$deptName="Senior and strategic staff"
$userNames=@("Candidate","ChiefOfStaff","Strategic1")
foreach ($element in $userNames){ New-AzureADUser -DisplayName $element -PasswordProfile $PasswordProfile -UserPrincipalName ($element + "@" + $orgName + ".onmicrosoft.com") -AccountEnabled $true -MailNickName $element -Department $deptName -UsageLocation $location }
$deptName="IT staff"
$userNames=@("ITAdmin1","ITAdmin2")
foreach ($element in $userNames){ New-AzureADUser -DisplayName $element -PasswordProfile $PasswordProfile -UserPrincipalName ($element + "@" + $orgName + ".onmicrosoft.com") -AccountEnabled $true -MailNickName $element -Department $deptName -UsageLocation $location }
$deptName="Analytics staff"
$userNames=@("DataScientist1")
foreach ($element in $userNames){ New-AzureADUser -DisplayName $element -PasswordProfile $PasswordProfile -UserPrincipalName ($element + "@" + $orgName + ".onmicrosoft.com") -AccountEnabled $true -MailNickName $element -Department $deptName -UsageLocation $location }
$deptName="Regular core staff"
$userNames=@("Regular1","Regular2")
foreach ($element in $userNames){ New-AzureADUser -DisplayName $element -PasswordProfile $PasswordProfile -UserPrincipalName ($element + "@" + $orgName + ".onmicrosoft.com") -AccountEnabled $true -MailNickName $element -Department $deptName -UsageLocation $location }
$deptName="Operations staff"
$userNames=@("Operations1")
foreach ($element in $userNames){ New-AzureADUser -DisplayName $element -PasswordProfile $PasswordProfile -UserPrincipalName ($element + "@" + $orgName + ".onmicrosoft.com") -AccountEnabled $true -MailNickName $element -Department $deptName -UsageLocation $location }
$deptName="Field staff"
$userNames=@("FieldConsultant1")
foreach ($element in $userNames){ New-AzureADUser -DisplayName $element -PasswordProfile $PasswordProfile -UserPrincipalName ($element + "@" + $orgName + ".onmicrosoft.com") -AccountEnabled $true -MailNickName $element -Department $deptName -UsageLocation $location }
```

> [!IMPORTANT]
> <span data-ttu-id="98a37-p104">L’utilisation d’un mot de passe commun permet d’automatiser et de faciliter la configuration d’un environnement de développement/test. Il n’est pas recommandé de l’utiliser dans un environnement de production. Lorsque vous vous connectez avec chacun de ces nouveaux comptes d’utilisateur, vous êtes invité à changer le mot de passe.</span><span class="sxs-lookup"><span data-stu-id="98a37-p104">The use of a common password here is for automation and ease of configuration for a dev/test environment. This is not recommended for production subscriptions. As you sign in with each of these new user accounts, you will be prompted to change the password.</span></span>

<span data-ttu-id="98a37-165">Utilisez ces étapes pour vérifier que l’appartenance au groupe dynamique et l’octroi de licence selon le groupe fonctionnent correctement.</span><span class="sxs-lookup"><span data-stu-id="98a37-165">Use these steps to verify that dynamic group membership and group-based licensing are working correctly.</span></span>

1. <span data-ttu-id="98a37-166">Sous l’onglet **Accueil Microsoft Office** de votre navigateur, cliquez sur la vignette **Administration**.</span><span class="sxs-lookup"><span data-stu-id="98a37-166">From the **Microsoft Office Home** tab of your browser, click the **Admin** tile.</span></span>

2. <span data-ttu-id="98a37-167">Dans le nouvel onglet **Centre d’administration Microsoft 365** de votre navigateur, cliquez sur **Utilisateurs**.</span><span class="sxs-lookup"><span data-stu-id="98a37-167">From the new **Microsoft 365 admin center** tab of your browser, click **Users**.</span></span>

3. <span data-ttu-id="98a37-168">Dans la liste des utilisateurs, cliquez sur **Candidat**.</span><span class="sxs-lookup"><span data-stu-id="98a37-168">In the list of users, click **Candidate**.</span></span>

4. <span data-ttu-id="98a37-169">Dans le volet qui répertorie les propriétés du compte d’utilisateur **Candidat**, vérifiez que les situations suivantes sont satisfaites :</span><span class="sxs-lookup"><span data-stu-id="98a37-169">In the pane that lists the properties of the **Candidate** user account, verify that:</span></span>

   - <span data-ttu-id="98a37-170">Il est membre du groupe **Senior and strategic staff** (dans **Appartenances aux groupes**).</span><span class="sxs-lookup"><span data-stu-id="98a37-170">It is a member of the **Senior and strategic staff** group (in **Group memberships**).</span></span>

   - <span data-ttu-id="98a37-171">Les licences **Enterprise Mobility + Security E5** et **Office 365 Entreprise E5** lui ont été affectées (dans **Licences des produits**).</span><span class="sxs-lookup"><span data-stu-id="98a37-171">It has been assigned the **Enterprise Mobility + Security E5** and **Office 365 Enterprise E5** licenses (in **Product licenses**).</span></span>

5. <span data-ttu-id="98a37-172">Fermez le volet du compte d’utilisateur **Candidat**.</span><span class="sxs-lookup"><span data-stu-id="98a37-172">Close the **Candidate** user account pane.</span></span>

## <a name="record-values-for-future-reference"></a><span data-ttu-id="98a37-173">Enregistrez les valeurs, vous en aurez besoin plus tard.</span><span class="sxs-lookup"><span data-stu-id="98a37-173">Record values for future reference</span></span>

<span data-ttu-id="98a37-174">Enregistrez ces valeurs pour utiliser les abonnements aux versions d’évaluation d’Office 365 et d’EMS pour cet environnement de développement/test :</span><span class="sxs-lookup"><span data-stu-id="98a37-174">Record these values for working with the Office 365 and EMS trial subscriptions for this dev/test environment:</span></span>

- <span data-ttu-id="98a37-175">Nom de l’organisation bénéficiant de l’abonnement à la version d’évaluation :</span><span class="sxs-lookup"><span data-stu-id="98a37-175">Your trial subscription organization name:</span></span> ![Souligner](../../media/Common-Images/TableLine.png)

  <span data-ttu-id="98a37-177">Par exemple, pour le nom de domaine de l’abonnement à la version d’évaluation de contoso.onmicrosoft.com, le nom de l’organisation est « contoso ».</span><span class="sxs-lookup"><span data-stu-id="98a37-177">For example, for the trial subscription domain name of contoso.onmicrosoft.com, the organization name is "contoso".</span></span>

- <span data-ttu-id="98a37-178">Le nom de l’administrateur général Office 365 :</span><span class="sxs-lookup"><span data-stu-id="98a37-178">The Office 365 global administrator name:</span></span> ![Souligner](../../media/Common-Images/TableLine.png)<span data-ttu-id="98a37-180">.onmicrosoft.com</span><span class="sxs-lookup"><span data-stu-id="98a37-180">.onmicrosoft.com</span></span>

  <span data-ttu-id="98a37-181">Enregistrez le mot de passe pour ce compte et le mot de passe initial commun pour les autres comptes d’utilisateurs dans un emplacement sécurisé.</span><span class="sxs-lookup"><span data-stu-id="98a37-181">Record the password for this account and the common initial password for the other user accounts in a secure location.</span></span>

## <a name="next-step"></a><span data-ttu-id="98a37-182">Étape suivante</span><span class="sxs-lookup"><span data-stu-id="98a37-182">Next step</span></span>

<span data-ttu-id="98a37-183">Créez les quatre différents types de sites d’équipe SharePoint Online dans cet environnement de développement/test en vous reportant à [Création de sites d’équipe dans un environnement de développement/test dans le cadre d’une campagne électorale](create-team-sites-in-a-political-campaign-dev-test-environment.md).</span><span class="sxs-lookup"><span data-stu-id="98a37-183">Build the four different types of SharePoint Online team sites in this dev/test environment with [Create team sites in a political campaign dev/test environment](create-team-sites-in-a-political-campaign-dev-test-environment.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="98a37-184">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="98a37-184">See also</span></span>

[<span data-ttu-id="98a37-185">Conseils de sécurité Microsoft pour les campagnes électorales, les organisations à but non lucratif et d’autres organisations flexibles</span><span class="sxs-lookup"><span data-stu-id="98a37-185">Microsoft Security Guidance for Political Campaigns, Nonprofits, and Other Agile Organizations</span></span>](microsoft-security-guidance-for-political-campaigns-nonprofits-and-other-agile-o.md)

[<span data-ttu-id="98a37-186">Création de sites d’équipe dans un environnement de développement/test dans le cadre d’une campagne électorale</span><span class="sxs-lookup"><span data-stu-id="98a37-186">Create team sites in a political campaign dev/test environment</span></span>](create-team-sites-in-a-political-campaign-dev-test-environment.md)

[<span data-ttu-id="98a37-187">Guides de laboratoire de test d’adoption cloud</span><span class="sxs-lookup"><span data-stu-id="98a37-187">Cloud adoption Test Lab Guides (TLGs)</span></span>](https://docs.microsoft.com/office365/enterprise/cloud-adoption-test-lab-guides-tlgs)

[<span data-ttu-id="98a37-188">Adoption du cloud et solutions hybrides</span><span class="sxs-lookup"><span data-stu-id="98a37-188">Cloud adoption and hybrid solutions</span></span>](https://docs.microsoft.com/office365/enterprise/cloud-adoption-and-hybrid-solutions)
