---
title: 'Configurer des groupes et des utilisateurs : environnement de développement/test pour une campagne politique'
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
localization_priority: Priority
search.appverid:
- MET150
ms.assetid: 0e22bcf3-bad3-42a4-b44f-276e0cf4790f
description: 'Résumé : Créez des abonnements d’essai Office 365 et Enterprise Mobility + Security (EMS) avec des utilisateurs et des groupes pour un environnement de développement/test de campagne électorale.'
ms.custom: seo-marvel-apr2020
ms.technology: mdo
ms.prod: m365-security
ms.openlocfilehash: 2e21cdfb0aabbdb10397d6d16c879756449a498e
ms.sourcegitcommit: dcb97fbfdae52960ae62b6faa707a05358193ed5
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/25/2021
ms.locfileid: "51203938"
---
# <a name="configure-groups-and-users-for-a-political-campaign-devtest-environment"></a><span data-ttu-id="2785b-103">Configuration de groupes et d’utilisateurs pour un environnement de développement/test pour une campagne électorale</span><span class="sxs-lookup"><span data-stu-id="2785b-103">Configure groups and users for a political campaign dev/test environment</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../includes/microsoft-defender-for-office.md)]

<span data-ttu-id="2785b-104">**S’applique à**</span><span class="sxs-lookup"><span data-stu-id="2785b-104">**Applies to**</span></span>
- [<span data-ttu-id="2785b-105">Microsoft Defender pour Office 365 Plan 2</span><span class="sxs-lookup"><span data-stu-id="2785b-105">Microsoft Defender for Office 365 plan 2</span></span>](defender-for-office-365.md)

 <span data-ttu-id="2785b-106">**Résumé :** Créez des abonnements d’essai Office 365 et Enterprise Mobility + Security (EMS) avec des utilisateurs et des groupes pour un environnement de développement/test de campagne électorale.</span><span class="sxs-lookup"><span data-stu-id="2785b-106">**Summary:** Create Office 365 and Enterprise Mobility + Security (EMS) trial subscriptions with users and groups for a political campaign dev/test environment.</span></span>

<span data-ttu-id="2785b-107">Suivez les instructions de cet article pour créer un environnement de développement/test incluant des comptes d’utilisateurs simplifiés et des groupes pour la solution des [conseils de sécurité Microsoft pour les campagnes électorales, les organisations à but non lucratif et d’autres organisations souples](microsoft-security-guidance-for-political-campaigns-nonprofits-and-other-agile-o.md).</span><span class="sxs-lookup"><span data-stu-id="2785b-107">Use the instructions in this article to create a dev/test environment that includes simplified user accounts and groups for the [Microsoft Security Guidance for Political Campaigns, Nonprofits, and Other Agile Organizations](microsoft-security-guidance-for-political-campaigns-nonprofits-and-other-agile-o.md) solution.</span></span>

## <a name="phase-1-create-your-office-365-devtest-environment"></a><span data-ttu-id="2785b-108">Phase 1 : Création d’un environnement de développement/test Office 365</span><span class="sxs-lookup"><span data-stu-id="2785b-108">Phase 1: Create your Office 365 dev/test environment</span></span>

<span data-ttu-id="2785b-109">Dans cette phase, vous obtenez des abonnements d’essai pour Office 365 E5 et Enterprise Mobility + Security (EMS) E5 pour une entreprise fictive qui représente une campagne électorale.</span><span class="sxs-lookup"><span data-stu-id="2785b-109">In this phase, you obtain trial subscriptions for Office 365 E5 and Enterprise Mobility + Security (EMS) E5 for a fictional organization that represents a political campaign.</span></span>

<span data-ttu-id="2785b-110">Tout d’abord, suivez les instructions de **Phase 2** de [la configuration de base légère](../../enterprise/lightweight-base-configuration-microsoft-365-enterprise.md).</span><span class="sxs-lookup"><span data-stu-id="2785b-110">First, follow the instructions in **Phase 2** of [The lightweight base configuration](../../enterprise/lightweight-base-configuration-microsoft-365-enterprise.md).</span></span>

<span data-ttu-id="2785b-111">Ensuite, inscrivez-vous à l’abonnement d’évaluation EMS E5 et ajoutez-le à la même organisation que votre abonnement d’évaluation.</span><span class="sxs-lookup"><span data-stu-id="2785b-111">Next, sign up for the EMS E5 trial subscription and add it to the same organization as your trial subscription.</span></span>

1. <span data-ttu-id="2785b-112">Si nécessaire, connectez-vous au centre d’administration avec les identifiants du compte d’administrateur général de votre abonnement d’essai.</span><span class="sxs-lookup"><span data-stu-id="2785b-112">If needed, sign in to the admin center with the credentials of the global administrator account of your trial subscription.</span></span> <span data-ttu-id="2785b-113">Pour obtenir de l’aide, consultez [Où se connecter](https://support.microsoft.com/office/e9eb7d51-5430-4929-91ab-6157c5a050b4).</span><span class="sxs-lookup"><span data-stu-id="2785b-113">For help, see [Where to sign in](https://support.microsoft.com/office/e9eb7d51-5430-4929-91ab-6157c5a050b4).</span></span>

2. <span data-ttu-id="2785b-114">Cliquez sur la vignette **Administration**.</span><span class="sxs-lookup"><span data-stu-id="2785b-114">Click the **Admin** tile.</span></span>

3. <span data-ttu-id="2785b-115">Sous l’onglet **Centre d’administration Microsoft 365** de votre navigateur, dans le volet de navigation gauche, cliquez sur **Facturation > Acheter des services**.</span><span class="sxs-lookup"><span data-stu-id="2785b-115">On the **Microsoft 365 admin center** tab in your browser, in the left navigation, click **Billing > Purchase services**.</span></span>

4. <span data-ttu-id="2785b-p102">Dans la page **Acheter des services**, recherchez l’élément **Enterprise Mobility + Security E5**. Pointez votre souris dessus et cliquez sur **Démarrer l’essai gratuit**.</span><span class="sxs-lookup"><span data-stu-id="2785b-p102">On the **Purchase services** page, find the **Enterprise Mobility + Security E5** item. Hover your mouse pointer over it and click **Start free trial**.</span></span>

5. <span data-ttu-id="2785b-118">Dans la page **Confirmer votre commande**, cliquez sur **Essayer maintenant**.</span><span class="sxs-lookup"><span data-stu-id="2785b-118">On the **Confirm your order** page, click **Try now**.</span></span>

6. <span data-ttu-id="2785b-119">Dans la page **Réception de la commande**, cliquez sur **Continuer**.</span><span class="sxs-lookup"><span data-stu-id="2785b-119">On the **Order receipt** page, click **Continue**.</span></span>

<span data-ttu-id="2785b-120">Ensuite, activez la licence EMS E5 pour votre compte Administrateur général.</span><span class="sxs-lookup"><span data-stu-id="2785b-120">Next, enable the EMS E5 license for your global administrator account.</span></span>

1. <span data-ttu-id="2785b-121">Sous l’onglet **Centre d’administration Microsoft 365** de votre navigateur, dans le volet de navigation gauche, cliquez sur **Utilisateurs > Utilisateurs actifs**.</span><span class="sxs-lookup"><span data-stu-id="2785b-121">On the **Microsoft 365 admin center** tab in your browser, in the left navigation, click **Users > Active users**.</span></span>

2. <span data-ttu-id="2785b-122">Cliquez sur votre compte Administrateur général, puis cliquez sur **Modifier** pour les **licences de produit**.</span><span class="sxs-lookup"><span data-stu-id="2785b-122">Click your global administrator account, and then click **Edit** for **Product licenses**.</span></span>

3. <span data-ttu-id="2785b-123">Dans le volet **Licences de produit**, activez la licence de produit pour **Enterprise Mobility + Security E5** en sélectionnant **Activer**, cliquez sur **Enregistrer**, cliquez deux fois sur **Fermer**.</span><span class="sxs-lookup"><span data-stu-id="2785b-123">On the **Product licenses** pane, turn the product license for **Enterprise Mobility + Security E5** to **On**, click **Save,** and then click **Close** twice.</span></span>

## <a name="phase-2-create-and-configure-your-azure-active-directory-ad-groups"></a><span data-ttu-id="2785b-124">Phase 2 : Création et configuration de vos groupes Azure Active Directory (AD)</span><span class="sxs-lookup"><span data-stu-id="2785b-124">Phase 2: Create and configure your Azure Active Directory (AD) groups</span></span>

<span data-ttu-id="2785b-125">Dans cette phase, vous créez et configurez des groupes Azure AD pour votre campagne.</span><span class="sxs-lookup"><span data-stu-id="2785b-125">In this phase, you create and configure the Azure AD groups for your campaign.</span></span>

<span data-ttu-id="2785b-126">Commencez par créer un ensemble de groupes pour une campagne électorale standard avec le portail Azure.</span><span class="sxs-lookup"><span data-stu-id="2785b-126">First, create a set of groups for a typical political campaign with the Azure portal.</span></span>

1. <span data-ttu-id="2785b-127">Dans un nouvel onglet de votre navigateur, accédez au portail Azure sous <https://portal.azure.com>.</span><span class="sxs-lookup"><span data-stu-id="2785b-127">On a separate tab in your browser, go to the Azure portal at <https://portal.azure.com>.</span></span> <span data-ttu-id="2785b-128">Si nécessaire, connectez-vous avec les informations d’identification du compte d’administrateur général de votre abonnement d’essai Office 365 E5.</span><span class="sxs-lookup"><span data-stu-id="2785b-128">If needed, sign in with the credentials of the global administrator account for your Office 365 E5 trial subscription.</span></span>

2. <span data-ttu-id="2785b-129">Dans le portail Azure, cliquez sur **Azure Active Directory > Utilisateurs et groupes > Tous les groupes**.</span><span class="sxs-lookup"><span data-stu-id="2785b-129">In the Azure portal, click **Azure Active Directory > Users and groups > All groups**.</span></span>

3. <span data-ttu-id="2785b-130">Procédez comme suit pour chaque nom de groupe dans cette liste :</span><span class="sxs-lookup"><span data-stu-id="2785b-130">Do the following steps for each group name in this list:</span></span>

   - <span data-ttu-id="2785b-131">Senior and strategic staff</span><span class="sxs-lookup"><span data-stu-id="2785b-131">Senior and strategic staff</span></span>

   - <span data-ttu-id="2785b-132">IT staff</span><span class="sxs-lookup"><span data-stu-id="2785b-132">IT staff</span></span>

   - <span data-ttu-id="2785b-133">Analytics staff</span><span class="sxs-lookup"><span data-stu-id="2785b-133">Analytics staff</span></span>

   - <span data-ttu-id="2785b-134">Regular core staff</span><span class="sxs-lookup"><span data-stu-id="2785b-134">Regular core staff</span></span>

   - <span data-ttu-id="2785b-135">Operations staff</span><span class="sxs-lookup"><span data-stu-id="2785b-135">Operations staff</span></span>

   - <span data-ttu-id="2785b-136">Field staff</span><span class="sxs-lookup"><span data-stu-id="2785b-136">Field staff</span></span>

1. <span data-ttu-id="2785b-137">Dans le panneau **Tous les groupes**, cliquez sur **+ Nouveau groupe**.</span><span class="sxs-lookup"><span data-stu-id="2785b-137">On the **All groups** blade, click **+ New group**.</span></span>

2. <span data-ttu-id="2785b-138">Tapez le nom du groupe de la liste dans **Nom**.</span><span class="sxs-lookup"><span data-stu-id="2785b-138">Type the group name from the list in **Name**.</span></span>

3. <span data-ttu-id="2785b-139">Sélectionnez **Utilisateur dynamique** dans **Appartenance**.</span><span class="sxs-lookup"><span data-stu-id="2785b-139">Select **Dynamic user** in **Membership**.</span></span>

4. <span data-ttu-id="2785b-140">Cliquez sur **Oui** pour **Activer les fonctionnalités Office**.</span><span class="sxs-lookup"><span data-stu-id="2785b-140">Click **Yes** for **Enable Office features**.</span></span>

5. <span data-ttu-id="2785b-141">Cliquez sur **Ajouter une requête dynamique**.</span><span class="sxs-lookup"><span data-stu-id="2785b-141">Click **Add dynamic query**.</span></span>

6. <span data-ttu-id="2785b-142">Dans **Ajouter des utilisateurs où**, sélectionnez **Service**.</span><span class="sxs-lookup"><span data-stu-id="2785b-142">In **Add users where**, select **department**.</span></span>

7. <span data-ttu-id="2785b-143">Dans le champ suivant, sélectionnez **Est égal à**.</span><span class="sxs-lookup"><span data-stu-id="2785b-143">In the next field, select **Equals**.</span></span>

8. <span data-ttu-id="2785b-144">Dans le champ suivant, tapez le nom du groupe de la liste.</span><span class="sxs-lookup"><span data-stu-id="2785b-144">In the next field, type the group name from the list.</span></span>

9. <span data-ttu-id="2785b-145">Cliquez sur **Ajouter une requête**, puis cliquez sur **Créer**.</span><span class="sxs-lookup"><span data-stu-id="2785b-145">Click **Add query**, and then click **Create**.</span></span>

10. <span data-ttu-id="2785b-146">Cliquez sur **Utilisateurs et groupes - Tous les groupes**.</span><span class="sxs-lookup"><span data-stu-id="2785b-146">Click **Users and groups - All groups**.</span></span>

<span data-ttu-id="2785b-147">Ensuite, vous configurez les groupes afin que des licences Office 365 E5 et EMS E5 soient attribuées automatiquement aux membres.</span><span class="sxs-lookup"><span data-stu-id="2785b-147">Next, you configure the groups so that members are automatically assigned Office 365 E5 and EMS E5 licenses.</span></span>

1. <span data-ttu-id="2785b-148">Dans le portail Azure, cliquez sur **Azure Active Directory > Licences > Tous les produits**.</span><span class="sxs-lookup"><span data-stu-id="2785b-148">In the Azure portal, click **Azure Active Directory > Licenses > All products**.</span></span>

2. <span data-ttu-id="2785b-149">Dans la liste, sélectionnez **Enterprise Mobility + Security E5** et **Office 365 Entreprise E5**, puis cliquez sur **+ Affecter**.</span><span class="sxs-lookup"><span data-stu-id="2785b-149">In the list, select **Enterprise Mobility + Security E5** and **Office 365 Enterprise E5**, and then click **+ Assign**.</span></span>

3. <span data-ttu-id="2785b-150">Dans le panneau **Affecter une licence**, cliquez sur **Utilisateurs et groupes**.</span><span class="sxs-lookup"><span data-stu-id="2785b-150">In the **Assign license** blade, click **Users and groups**.</span></span>

4. <span data-ttu-id="2785b-151">Dans la liste des groupes, sélectionnez les éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="2785b-151">In the list of groups, select the following:</span></span>

   - <span data-ttu-id="2785b-152">Analytics staff</span><span class="sxs-lookup"><span data-stu-id="2785b-152">Analytics staff</span></span>

   - <span data-ttu-id="2785b-153">Field staff</span><span class="sxs-lookup"><span data-stu-id="2785b-153">Field staff</span></span>

   - <span data-ttu-id="2785b-154">IT staff</span><span class="sxs-lookup"><span data-stu-id="2785b-154">IT staff</span></span>

   - <span data-ttu-id="2785b-155">Operations staff</span><span class="sxs-lookup"><span data-stu-id="2785b-155">Operations staff</span></span>

   - <span data-ttu-id="2785b-156">Regular core staff</span><span class="sxs-lookup"><span data-stu-id="2785b-156">Regular core staff</span></span>

   - <span data-ttu-id="2785b-157">Senior and strategic staff</span><span class="sxs-lookup"><span data-stu-id="2785b-157">Senior and strategic staff</span></span>

5. <span data-ttu-id="2785b-158">Cliquez sur **Sélectionner**, puis sur **Affecter**.</span><span class="sxs-lookup"><span data-stu-id="2785b-158">Click **Select**, and then click **Assign**.</span></span>

6. <span data-ttu-id="2785b-159">Fermez l’onglet du portail Azure dans votre navigateur.</span><span class="sxs-lookup"><span data-stu-id="2785b-159">Close the Azure portal tab in your browser.</span></span>

## <a name="phase-3-add-your-user-accounts"></a><span data-ttu-id="2785b-160">Phase 3 : Ajout de comptes d’utilisateurs</span><span class="sxs-lookup"><span data-stu-id="2785b-160">Phase 3: Add your user accounts</span></span>

<span data-ttu-id="2785b-161">Dans cette phase, vous ajoutez les comptes d’utilisateurs de l’exemple pour votre campagne politique.</span><span class="sxs-lookup"><span data-stu-id="2785b-161">In this phase, you add the example user accounts for your political campaign.</span></span>

<span data-ttu-id="2785b-162">Pour commencer, [connectez -vous au module PowerShell Azure Active Directory pour le module Graphique](../../enterprise/connect-to-microsoft-365-powershell.md).</span><span class="sxs-lookup"><span data-stu-id="2785b-162">First, you [Connect with the Azure Active Directory PowerShell for Graph module](../../enterprise/connect-to-microsoft-365-powershell.md).</span></span>

<span data-ttu-id="2785b-163">Ensuite, renseignez le nom de votre organisation, votre emplacement et un mot de passe commun, puis exécutez les commandes suivantes à partir de l’invite de commandes PowerShell ou de l’environnement de script intégré (ISE) :</span><span class="sxs-lookup"><span data-stu-id="2785b-163">Next, you fill in your organization name, your location, and a common password, and then run these commands from the PowerShell command prompt or Integrated Script Environment (ISE):</span></span>

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
> <span data-ttu-id="2785b-p104">L’utilisation d’un mot de passe commun permet d’automatiser et de faciliter la configuration d’un environnement de développement/test. Il n’est pas recommandé de l’utiliser dans un environnement de production. Lorsque vous vous connectez avec chacun de ces nouveaux comptes d’utilisateur, vous êtes invité à changer le mot de passe.</span><span class="sxs-lookup"><span data-stu-id="2785b-p104">The use of a common password here is for automation and ease of configuration for a dev/test environment. This is not recommended for production subscriptions. As you sign in with each of these new user accounts, you will be prompted to change the password.</span></span>

<span data-ttu-id="2785b-167">Utilisez ces étapes pour vérifier que l’appartenance au groupe dynamique et l’octroi de licence selon le groupe fonctionnent correctement.</span><span class="sxs-lookup"><span data-stu-id="2785b-167">Use these steps to verify that dynamic group membership and group-based licensing are working correctly.</span></span>

1. <span data-ttu-id="2785b-168">Sous l’onglet **Accueil Microsoft Office** de votre navigateur, cliquez sur la vignette **Administration**.</span><span class="sxs-lookup"><span data-stu-id="2785b-168">From the **Microsoft Office Home** tab of your browser, click the **Admin** tile.</span></span>

2. <span data-ttu-id="2785b-169">Dans le nouvel onglet **Centre d’administration Microsoft 365** de votre navigateur, cliquez sur **Utilisateurs**.</span><span class="sxs-lookup"><span data-stu-id="2785b-169">From the new **Microsoft 365 admin center** tab of your browser, click **Users**.</span></span>

3. <span data-ttu-id="2785b-170">Dans la liste des utilisateurs, cliquez sur **Candidat**.</span><span class="sxs-lookup"><span data-stu-id="2785b-170">In the list of users, click **Candidate**.</span></span>

4. <span data-ttu-id="2785b-171">Dans le volet qui répertorie les propriétés du compte d’utilisateur **Candidat**, vérifiez que les situations suivantes sont satisfaites :</span><span class="sxs-lookup"><span data-stu-id="2785b-171">In the pane that lists the properties of the **Candidate** user account, verify that:</span></span>

   - <span data-ttu-id="2785b-172">Il est membre du groupe **Senior and strategic staff** (dans **Appartenances aux groupes**).</span><span class="sxs-lookup"><span data-stu-id="2785b-172">It is a member of the **Senior and strategic staff** group (in **Group memberships**).</span></span>

   - <span data-ttu-id="2785b-173">Les licences **Enterprise Mobility + Security E5** et **Office 365 Entreprise E5** lui ont été affectées (dans **Licences des produits**).</span><span class="sxs-lookup"><span data-stu-id="2785b-173">It has been assigned the **Enterprise Mobility + Security E5** and **Office 365 Enterprise E5** licenses (in **Product licenses**).</span></span>

5. <span data-ttu-id="2785b-174">Fermez le volet du compte d’utilisateur **Candidat**.</span><span class="sxs-lookup"><span data-stu-id="2785b-174">Close the **Candidate** user account pane.</span></span>

## <a name="record-values-for-future-reference"></a><span data-ttu-id="2785b-175">Enregistrez les valeurs, vous en aurez besoin plus tard.</span><span class="sxs-lookup"><span data-stu-id="2785b-175">Record values for future reference</span></span>

<span data-ttu-id="2785b-176">Enregistrez ces valeurs pour utiliser les abonnements aux versions d’évaluation d’Office 365 et d’EMS pour cet environnement de développement/test :</span><span class="sxs-lookup"><span data-stu-id="2785b-176">Record these values for working with the Office 365 and EMS trial subscriptions for this dev/test environment:</span></span>

- <span data-ttu-id="2785b-177">Nom de l’organisation bénéficiant de l’abonnement à la version d’évaluation :</span><span class="sxs-lookup"><span data-stu-id="2785b-177">Your trial subscription organization name:</span></span> ![Souligner](../../media/Common-Images/TableLine.png)

  <span data-ttu-id="2785b-179">Par exemple, pour le nom de domaine de l’abonnement à la version d’évaluation de contoso.onmicrosoft.com, le nom de l’organisation est « contoso ».</span><span class="sxs-lookup"><span data-stu-id="2785b-179">For example, for the trial subscription domain name of contoso.onmicrosoft.com, the organization name is "contoso".</span></span>

- <span data-ttu-id="2785b-180">Nom d’administrateur général :</span><span class="sxs-lookup"><span data-stu-id="2785b-180">The global administrator name:</span></span> ![Souligner](../../media/Common-Images/TableLine.png)<span data-ttu-id="2785b-182">.onmicrosoft.com</span><span class="sxs-lookup"><span data-stu-id="2785b-182">.onmicrosoft.com</span></span>

  <span data-ttu-id="2785b-183">Enregistrez le mot de passe pour ce compte et le mot de passe initial commun pour les autres comptes d’utilisateurs dans un emplacement sécurisé.</span><span class="sxs-lookup"><span data-stu-id="2785b-183">Record the password for this account and the common initial password for the other user accounts in a secure location.</span></span>

## <a name="next-step"></a><span data-ttu-id="2785b-184">Étape suivante</span><span class="sxs-lookup"><span data-stu-id="2785b-184">Next step</span></span>

<span data-ttu-id="2785b-185">Créez les quatre différents types de sites d’équipe SharePoint Online dans cet environnement de développement/test en vous reportant à [Création de sites d’équipe dans un environnement de développement/test dans le cadre d’une campagne électorale](create-team-sites-in-a-political-campaign-dev-test-environment.md).</span><span class="sxs-lookup"><span data-stu-id="2785b-185">Build the four different types of SharePoint Online team sites in this dev/test environment with [Create team sites in a political campaign dev/test environment](create-team-sites-in-a-political-campaign-dev-test-environment.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="2785b-186">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2785b-186">See also</span></span>

[<span data-ttu-id="2785b-187">Conseils de sécurité Microsoft pour les campagnes électorales, les organisations à but non lucratif et d’autres organisations flexibles</span><span class="sxs-lookup"><span data-stu-id="2785b-187">Microsoft Security Guidance for Political Campaigns, Nonprofits, and Other Agile Organizations</span></span>](microsoft-security-guidance-for-political-campaigns-nonprofits-and-other-agile-o.md)

[<span data-ttu-id="2785b-188">Création de sites d’équipe dans un environnement de développement/test dans le cadre d’une campagne électorale</span><span class="sxs-lookup"><span data-stu-id="2785b-188">Create team sites in a political campaign dev/test environment</span></span>](create-team-sites-in-a-political-campaign-dev-test-environment.md)

[<span data-ttu-id="2785b-189">Guides de laboratoire de test d’adoption cloud</span><span class="sxs-lookup"><span data-stu-id="2785b-189">Cloud adoption Test Lab Guides (TLGs)</span></span>](../../enterprise/cloud-adoption-test-lab-guides-tlgs.md)

[<span data-ttu-id="2785b-190">Adoption du cloud et solutions hybrides</span><span class="sxs-lookup"><span data-stu-id="2785b-190">Cloud adoption and hybrid solutions</span></span>](/office365/enterprise/cloud-adoption-and-hybrid-solutions)