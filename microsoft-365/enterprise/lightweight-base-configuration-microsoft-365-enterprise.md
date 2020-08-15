---
title: Configuration de base légère
f1.keywords:
- NOCSH
ms.author: josephd
author: JoeDavies-MSFT
manager: laurawi
ms.date: 11/14/2019
audience: ITPro
ms.topic: article
ms.service: o365-solutions
localization_priority: Normal
ms.collection:
- M365-subscription-management
- Strat_O365_Enterprise
ms.custom:
- Ent_TLGs
- seo-marvel-apr2020
ms.assetid: 6f916a77-301c-4be2-b407-6cec4d80df76
description: Utilisez ce guide de laboratoire de test pour créer un environnement de test léger afin de tester Microsoft 365 pour les entreprises.
ms.openlocfilehash: 5de9e44f83d4c6bbae2b4148ce39ca371ead2d34
ms.sourcegitcommit: 79065e72c0799064e9055022393113dfcf40eb4b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/14/2020
ms.locfileid: "46686777"
---
# <a name="the-lightweight-base-configuration"></a><span data-ttu-id="afa99-103">Configuration de base légère</span><span class="sxs-lookup"><span data-stu-id="afa99-103">The lightweight base configuration</span></span>

<span data-ttu-id="afa99-104">*Ce guide de laboratoire de test peut être utilisé pour les environnements de test Microsoft 365 pour les environnements de test d’entreprise et Office 365.*</span><span class="sxs-lookup"><span data-stu-id="afa99-104">*This Test Lab Guide can be used for both Microsoft 365 for enterprise and Office 365 Enterprise test environments.*</span></span>

<span data-ttu-id="afa99-105">Cet article vous fournit des instructions étape par étape pour créer un environnement simplifié avec un abonnement Microsoft 365 E5 et un ordinateur exécutant Windows 10 Entreprise.</span><span class="sxs-lookup"><span data-stu-id="afa99-105">This article provides you with step-by-step instructions to create a simplified environment with a Microsoft 365 E5 subscription and a computer running Windows 10 Enterprise.</span></span> 

![Environnement de test Microsoft 365 Entreprise léger](../media/lightweight-base-configuration-microsoft-365-enterprise/Phase4.png)

<span data-ttu-id="afa99-107">Utilisez l’environnement résultant pour tester les fonctionnalités de [Microsoft 365 pour les entreprises](https://www.microsoft.com/microsoft-365/enterprise).</span><span class="sxs-lookup"><span data-stu-id="afa99-107">Use the resulting environment to test the features and functionality of [Microsoft 365 for enterprise](https://www.microsoft.com/microsoft-365/enterprise).</span></span>

![Guides de laboratoire de test pour Microsoft Cloud](../media/m365-enterprise-test-lab-guides/cloud-tlg-icon.png)
  
> [!TIP]
> <span data-ttu-id="afa99-109">Cliquez sur [Microsoft 365 pour la pile de guide de laboratoire de test d’entreprise](../media/m365-enterprise-test-lab-guides/Microsoft365EnterpriseTLGStack.pdf) pour un plan visuel vers tous les Articles de la pile de guide de laboratoire de test Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="afa99-109">Click [Microsoft 365 for enterprise Test Lab Guide Stack](../media/m365-enterprise-test-lab-guides/Microsoft365EnterpriseTLGStack.pdf) for a visual map to all the articles in the Microsoft 365 for enterprise Test Lab Guide stack.</span></span>

## <a name="phase-1-create-your-microsoft-365-e5-subscription"></a><span data-ttu-id="afa99-110">Phase 1 : création de votre abonnement Microsoft 365 E5</span><span class="sxs-lookup"><span data-stu-id="afa99-110">Phase 1: Create your Microsoft 365 E5 subscription</span></span>

<span data-ttu-id="afa99-111">Nous commençons par un abonnement à la version d’évaluation de Microsoft 365 E5, puis nous ajoutons l’abonnement Microsoft 365 E5.</span><span class="sxs-lookup"><span data-stu-id="afa99-111">We start with an Microsoft 365 E5 trial subscription and then add the Microsoft 365 E5 subscription to it.</span></span>

<span data-ttu-id="afa99-112">Pour démarrer votre abonnement d’évaluation Microsoft 365 E5, vous avez besoin d’un nom d’entreprise fictif et d’un nouveau compte Microsoft.</span><span class="sxs-lookup"><span data-stu-id="afa99-112">To start your Microsoft 365 E5 trial subscription, you first need a fictitious company name and a new Microsoft account.</span></span>
  
1. <span data-ttu-id="afa99-p101">Nous vous recommandons d’utiliser une variante du nom d’entreprise Contoso pour le nom de votre entreprise. Il s’agit d’une entreprise fictive utilisée dans le contenu d’exemple de Microsoft. Toutefois, cette étape n’est pas obligatoire. Indiquer le nom fictif de votre entreprise ici :</span><span class="sxs-lookup"><span data-stu-id="afa99-p101">We recommend that you use a variant of the company name Contoso for your company name, which is a fictitious company used in Microsoft sample content, but it isn't required. Record your fictitious company name here:</span></span> ![Trait](../media/Common-Images/TableLine.png)
    
2. <span data-ttu-id="afa99-p102">Pour ouvrir un nouveau compte Microsoft, accédez à [https://outlook.com](https://outlook.com) et créez un compte avec un nouveau compte de messagerie et une nouvelle adresse. Vous utiliserez ce compte pour vous inscrire à Office 365.</span><span class="sxs-lookup"><span data-stu-id="afa99-p102">To sign up for a new Microsoft account, go to [https://outlook.com](https://outlook.com) and create an account with a new email account and address. You will use this account to sign up for Office 365.</span></span>
    
  - <span data-ttu-id="afa99-118">Enregistrez le prénom et le nom de famille utilisés pour votre nouveau compte ici :</span><span class="sxs-lookup"><span data-stu-id="afa99-118">Record the first and last name of your new account here:</span></span> ![Trait](../media/Common-Images/TableLine.png)
    
  - <span data-ttu-id="afa99-120">Enregistrez l’adresse du nouveau compte de messagerie ici :</span><span class="sxs-lookup"><span data-stu-id="afa99-120">Record the new email account address here:</span></span> ![Trait](../media/Common-Images/TableLine.png)<span data-ttu-id="afa99-122">@outlook.com</span><span class="sxs-lookup"><span data-stu-id="afa99-122">@outlook.com</span></span>
    
### <a name="sign-up-for-an-office-365-e5-trial-subscription"></a><span data-ttu-id="afa99-123">Inscription à un abonnement d’évaluation Office 365 E5</span><span class="sxs-lookup"><span data-stu-id="afa99-123">Sign up for an Office 365 E5 trial subscription</span></span>

1. <span data-ttu-id="afa99-124">Ouvrez le navigateur Internet sur votre ordinateur, puis accédez à [https://aka.ms/e5trial](https://aka.ms/e5trial).</span><span class="sxs-lookup"><span data-stu-id="afa99-124">Open the Internet browser on your computer and go to [https://aka.ms/e5trial](https://aka.ms/e5trial).</span></span>
    
2. <span data-ttu-id="afa99-125">Sur la page **Merci d’avoir choisi Office 365 E5**, spécifiez votre nouvelle adresse de compte de messagerie à l’étape 1.</span><span class="sxs-lookup"><span data-stu-id="afa99-125">On the **Thank you for choosing Office 365 E5** page, specify, your new email account address in step 1.</span></span>
3. <span data-ttu-id="afa99-126">À l’étape 2 du processus d’abonnement d’évaluation, tapez les informations demandées, puis procédez à la vérification.</span><span class="sxs-lookup"><span data-stu-id="afa99-126">In step 2 of the trail subscription process, type the requested information, and then perform the verification.</span></span>
4. <span data-ttu-id="afa99-127">À l’étape 3, tapez un nom d’organisation, puis un nom de compte qui sera l’administrateur général de l’abonnement.</span><span class="sxs-lookup"><span data-stu-id="afa99-127">In step 3, type an organization name and then an account name that will be the global admin for the subscription.</span></span> 
5. <span data-ttu-id="afa99-128">À l’étape 4, enregistrer l’URL de la page de connexion ici (sélectionnez-la et copiez-la) :</span><span class="sxs-lookup"><span data-stu-id="afa99-128">For step 4, record the sign-in page here (select and copy):</span></span> ![Trait](../media/Common-Images/TableLine.png) 
6. <span data-ttu-id="afa99-130">Enregistrez l’identifiant utilisateur ici : ![ligne](../media/Common-Images/TableLine.png).onmicrosoft.com</span><span class="sxs-lookup"><span data-stu-id="afa99-130">Record the user ID here: ![Line](../media/Common-Images/TableLine.png).onmicrosoft.com</span></span>  
   <span data-ttu-id="afa99-131">Enregistrez le mot de passe saisi dans un emplacement sécurisé.</span><span class="sxs-lookup"><span data-stu-id="afa99-131">Record the password that you typed in a secure location.</span></span>
   <span data-ttu-id="afa99-132">Cette valeur correspond au **nom de l’administrateur général**.</span><span class="sxs-lookup"><span data-stu-id="afa99-132">This value will be referred to as the **global administrator name**.</span></span>
8. <span data-ttu-id="afa99-133">Sélectionnez **Configurer**.</span><span class="sxs-lookup"><span data-stu-id="afa99-133">Click **Go to Setup**.</span></span>
9. <span data-ttu-id="afa99-134">Dans la configuration d’Office 365 E5, cliquez sur **Continuer à utiliser *votre organisation*.onmicrosoft.com pour la messagerie et la connexion**, puis cliquez sur **Quitter et continuer plus tard**.</span><span class="sxs-lookup"><span data-stu-id="afa99-134">In Office 365 E5 Setup, click **Continue using *your organization*.onmicrosoft.com for email and signing in**, and then click **Exit and continue later**.</span></span>

<span data-ttu-id="afa99-135">Le Centre d’administration Microsoft 365 doit s’afficher.</span><span class="sxs-lookup"><span data-stu-id="afa99-135">You should see the Microsoft 365 admin center.</span></span>
  
<span data-ttu-id="afa99-136">Vous avez créé un abonnement d’évaluation Office 365 pour que votre environnement de développement/test ait un client Azure AD distinct de tout abonnement payant actuellement utilisé.</span><span class="sxs-lookup"><span data-stu-id="afa99-136">We have you create a trial subscription of Office 365 so that your test environment has a separate Azure AD tenant from any paid subscriptions you currently have.</span></span> <span data-ttu-id="afa99-137">Cette séparation signifie que vous pouvez ajouter et supprimer des utilisateurs et groupes dans le client test sans incidence sur vos abonnements de production.</span><span class="sxs-lookup"><span data-stu-id="afa99-137">This separation means you can add and remove users and groups in the test tenant without affecting your production subscriptions.</span></span>
    
## <a name="phase-2-configure-your-office-365-trial-subscription"></a><span data-ttu-id="afa99-138">Phase 2 : configuration de votre abonnement d’évaluation Office 365</span><span class="sxs-lookup"><span data-stu-id="afa99-138">Phase 2: Configure your Office 365 trial subscription</span></span>

<span data-ttu-id="afa99-139">Durant cette phase, configurez votre abonnement en y ajoutant des utilisateurs supplémentaires et assignez-leur des licences Office 365 E5.</span><span class="sxs-lookup"><span data-stu-id="afa99-139">In this phase, you configure your subscription with additional users and assign them Office 365 E5 licenses.</span></span>
  
<span data-ttu-id="afa99-140">Suivez les instructions de la procédure relative à la [connexion à Microsoft 365 avec PowerShell](connect-to-microsoft-365-powershell.md#connect-with-the-azure-active-directory-powershell-for-graph-module) pour vous connecter à votre abonnement à l’aide du module Azure Active Directory PowerShell for Graph de votre ordinateur.</span><span class="sxs-lookup"><span data-stu-id="afa99-140">Use the instructions in [Connect to Microsoft 365 with PowerShell](connect-to-microsoft-365-powershell.md#connect-with-the-azure-active-directory-powershell-for-graph-module) to connect to your subscription with the Azure Active Directory PowerShell for Graph module from your computer.</span></span>
    
<span data-ttu-id="afa99-141">Dans la boîte de dialogue **Demande d’informations d’identification Windows PowerShell**, saisissez le nom de l’administrateur général (exemple : jdoe@contosotoycompany.onmicrosoft.com) et le mot de passe.</span><span class="sxs-lookup"><span data-stu-id="afa99-141">In the **Windows PowerShell Credential Request** dialog box, type the global administrator name (example: jdoe@contosotoycompany.onmicrosoft.com) and password.</span></span>
  
<span data-ttu-id="afa99-142">Entrez le nom de votre organisation (exemple : contosotoycompany) et le code de pays à deux caractères pour indiquer votre emplacement, ainsi qu’un mot de passe de compte commun, puis exécutez les commandes suivantes à partir de l’invite PowerShell :</span><span class="sxs-lookup"><span data-stu-id="afa99-142">Fill in your organization name (example: contosotoycompany), the two-character country code for your location, a common account password, and then run the following commands from the PowerShell prompt:</span></span>

```powershell
$orgName="<organization name>"
$loc="<two-character country code, such as US>"
$commonPW="<common user account password>"
$PasswordProfile=New-Object -TypeName Microsoft.Open.AzureAD.Model.PasswordProfile
$PasswordProfile.Password=$commonPW

$userUPN= "user2@" + $orgName + ".onmicrosoft.com"
New-AzureADUser -DisplayName "User 2" -GivenName User -SurName 2 -UserPrincipalName $userUPN -UsageLocation $loc -AccountEnabled $true -PasswordProfile $PasswordProfile -MailNickName "user2"
$License = New-Object -TypeName Microsoft.Open.AzureAD.Model.AssignedLicense
$License.SkuId = (Get-AzureADSubscribedSku | Where-Object -Property SkuPartNumber -Value "ENTERPRISEPREMIUM" -EQ).SkuID
$LicensesToAssign = New-Object -TypeName Microsoft.Open.AzureAD.Model.AssignedLicenses
$LicensesToAssign.AddLicenses = $License
Set-AzureADUserLicense -ObjectId $userUPN -AssignedLicenses $LicensesToAssign

$userUPN= "user3@" + $orgName + ".onmicrosoft.com"
New-AzureADUser -DisplayName "User 3" -GivenName User -SurName 3 -UserPrincipalName $userUPN -UsageLocation $loc -AccountEnabled $true -PasswordProfile $PasswordProfile -MailNickName "user3"
$License = New-Object -TypeName Microsoft.Open.AzureAD.Model.AssignedLicense
$License.SkuId = (Get-AzureADSubscribedSku | Where-Object -Property SkuPartNumber -Value "ENTERPRISEPREMIUM" -EQ).SkuID
$LicensesToAssign = New-Object -TypeName Microsoft.Open.AzureAD.Model.AssignedLicenses
$LicensesToAssign.AddLicenses = $License
Set-AzureADUserLicense -ObjectId $userUPN -AssignedLicenses $LicensesToAssign

$userUPN= "user4@" + $orgName + ".onmicrosoft.com"
New-AzureADUser -DisplayName "User 4" -GivenName User -SurName 4 -UserPrincipalName $userUPN -UsageLocation $loc -AccountEnabled $true -PasswordProfile $PasswordProfile -MailNickName "user4"
$License = New-Object -TypeName Microsoft.Open.AzureAD.Model.AssignedLicense
$License.SkuId = (Get-AzureADSubscribedSku | Where-Object -Property SkuPartNumber -Value "ENTERPRISEPREMIUM" -EQ).SkuID
$LicensesToAssign = New-Object -TypeName Microsoft.Open.AzureAD.Model.AssignedLicenses
$LicensesToAssign.AddLicenses = $License
Set-AzureADUserLicense -ObjectId $userUPN -AssignedLicenses $LicensesToAssign
```
> [!NOTE]
> <span data-ttu-id="afa99-143">L’utilisation ici d’un mot de passe courant est destinée à l’automatisation et à la simplification de la configuration pour un environnement de test.</span><span class="sxs-lookup"><span data-stu-id="afa99-143">The use of a common password here is for automation and ease of configuration for a test environment.</span></span> <span data-ttu-id="afa99-144">Bien évidemment, cela est hautement déconseillé pour les abonnements de production.</span><span class="sxs-lookup"><span data-stu-id="afa99-144">Obviously, this is highly discouraged for production subscriptions.</span></span> 

### <a name="record-key-information-for-future-reference"></a><span data-ttu-id="afa99-145">Enregistrer les informations clés pour future référence</span><span class="sxs-lookup"><span data-stu-id="afa99-145">Record key information for future reference</span></span>

<span data-ttu-id="afa99-146">Nous vous recommandons d’imprimer cet article afin de consigner les informations dont vous aurez besoin dans cet environnement au cours des 30 jours de votre abonnement à la version d’évaluation Office 365.</span><span class="sxs-lookup"><span data-stu-id="afa99-146">You might want to print this article to record the specific information that you will need for this environment over the 30 days of the Office 365 trial subscription.</span></span> <span data-ttu-id="afa99-147">Vous pouvez facilement étendre l’abonnement d’évaluation pour une période supplémentaire de 30 jours.</span><span class="sxs-lookup"><span data-stu-id="afa99-147">You can easily extend the trail subscription for another 30 days.</span></span> <span data-ttu-id="afa99-148">Pour un environnement de développement/test permanent, créez un nouvel abonnement payant avec un client Azure AD séparé et un nombre réduit de licences.</span><span class="sxs-lookup"><span data-stu-id="afa99-148">For a permanent test environment, create a new paid subscription with a separate Azure AD tenant and a small number of licenses.</span></span>

<span data-ttu-id="afa99-149">Enregistrez les valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="afa99-149">Record these values:</span></span>
  
- <span data-ttu-id="afa99-150">Nom de l’administrateur général :</span><span class="sxs-lookup"><span data-stu-id="afa99-150">global administrator name:</span></span> ![Trait](../media/Common-Images/TableLine.png)<span data-ttu-id="afa99-152">.onmicrosoft.com(à partir de l’étape 6 de la phase 1)</span><span class="sxs-lookup"><span data-stu-id="afa99-152">.onmicrosoft.com (from step 6 of Phase 1)</span></span>
    
    <span data-ttu-id="afa99-153">Enregistrez également le mot de passe de ce compte dans un emplacement sécurisé.</span><span class="sxs-lookup"><span data-stu-id="afa99-153">Also record the password for this account in a secure location.</span></span>
    
- <span data-ttu-id="afa99-154">Nom de l’organisation bénéficiant de l’abonnement à la version d’évaluation :</span><span class="sxs-lookup"><span data-stu-id="afa99-154">Your trial subscription organization name:</span></span> ![Trait](../media/Common-Images/TableLine.png) <span data-ttu-id="afa99-156">(à partir de l’étape 4 de la phase 1)</span><span class="sxs-lookup"><span data-stu-id="afa99-156">(from step 4 of Phase 1)</span></span>
    
- <span data-ttu-id="afa99-157">Pour répertorier les comptes pour Utilisateur 2, Utilisateur 3, Utilisateur 4 et Utilisateur 5, exécutez la commande suivante à partir de l’invite Module Windows Azure Active Directory pour Windows PowerShell :</span><span class="sxs-lookup"><span data-stu-id="afa99-157">To list the accounts for User 2, User 3, User 4, and User 5, run the following command from the Windows Azure Active Directory Module for Windows PowerShell prompt:</span></span>
    
  ```powershell
  Get-AzureADUser | Sort UserPrincipalName | Select UserPrincipalName
  ```

    <span data-ttu-id="afa99-158">Enregistrez les noms de compte ici :</span><span class="sxs-lookup"><span data-stu-id="afa99-158">Record the account names here:</span></span>
    
  - <span data-ttu-id="afa99-159">Nom du compte de l’utilisateur 2 : utilisateur2@</span><span class="sxs-lookup"><span data-stu-id="afa99-159">User 2 account name: user2@</span></span>![Trait](../media/Common-Images/TableLine.png)<span data-ttu-id="afa99-161">.onmicrosoft.com</span><span class="sxs-lookup"><span data-stu-id="afa99-161">.onmicrosoft.com</span></span>
    
  - <span data-ttu-id="afa99-162">Nom du compte de l’utilisateur 3 : utilisateur3@</span><span class="sxs-lookup"><span data-stu-id="afa99-162">User 3 account name: user3@</span></span>![Trait](../media/Common-Images/TableLine.png)<span data-ttu-id="afa99-164">.onmicrosoft.com</span><span class="sxs-lookup"><span data-stu-id="afa99-164">.onmicrosoft.com</span></span>
    
  - <span data-ttu-id="afa99-165">Nom du compte de l’utilisateur 4 : utilisateur4@</span><span class="sxs-lookup"><span data-stu-id="afa99-165">User 4 account name: user4@</span></span>![Trait](../media/Common-Images/TableLine.png)<span data-ttu-id="afa99-167">.onmicrosoft.com</span><span class="sxs-lookup"><span data-stu-id="afa99-167">.onmicrosoft.com</span></span>
    
  - <span data-ttu-id="afa99-168">Nom du compte de l’utilisateur 5 : utilisateur5@</span><span class="sxs-lookup"><span data-stu-id="afa99-168">User 5 account name: user5@</span></span>![Trait](../media/Common-Images/TableLine.png)<span data-ttu-id="afa99-170">.onmicrosoft.com</span><span class="sxs-lookup"><span data-stu-id="afa99-170">.onmicrosoft.com</span></span>
    
    <span data-ttu-id="afa99-171">Enregistrez également les mots de passe communs de ces comptes dans un emplacement sécurisé.</span><span class="sxs-lookup"><span data-stu-id="afa99-171">Also record the common password for these accounts in a secure location.</span></span>
   

### <a name="using-an-office-365-test-environment"></a><span data-ttu-id="afa99-172">Utilisation d’un environnement de test Office 365</span><span class="sxs-lookup"><span data-stu-id="afa99-172">Using an Office 365 test environment</span></span>

<span data-ttu-id="afa99-173">Si vous avez simplement besoin d’un environnement de test Office 365, vous pouvez vous arrêter ici.</span><span class="sxs-lookup"><span data-stu-id="afa99-173">If all you need is an Office 365 test environment, you can stop here.</span></span> 

<span data-ttu-id="afa99-174">Consultez [microsoft 365 pour les guides de laboratoire de test d’entreprise](m365-enterprise-test-lab-guides.md) pour obtenir des guides de laboratoire de test supplémentaires qui s’appliquent à Office 365 et Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="afa99-174">See [Microsoft 365 for enterprise Test Lab Guides](m365-enterprise-test-lab-guides.md) for additional Test Lab Guides that apply to both Office 365 and Microsoft 365.</span></span>
  
## <a name="phase-3-add-a-microsoft-365-e5-trial-subscription"></a><span data-ttu-id="afa99-175">Phase 3 : Ajoutez un abonnement d’évaluation Microsoft 365 E5.</span><span class="sxs-lookup"><span data-stu-id="afa99-175">Phase 3: Add a Microsoft 365 E5 trial subscription</span></span>

<span data-ttu-id="afa99-176">Dans cette phase, vous vous inscrivez pour l’abonnement d’évaluation Microsoft 365 E5 et l’ajoutez à la même organisation que votre abonnement d’évaluation d’Office 365 E5.</span><span class="sxs-lookup"><span data-stu-id="afa99-176">In this phase, you sign up for the Microsoft 365 E5 trial subscription and add it to the same organization as your Office 365 E5 trial subscription.</span></span>
  
<span data-ttu-id="afa99-177">Tout d’abord, ajoutez l’abonnement d’évaluation Microsoft 365 E5 et attribuez une licence Microsoft 365 à votre compte d’administrateur général.</span><span class="sxs-lookup"><span data-stu-id="afa99-177">First, add the Microsoft 365 E5 trial subscription and assign the new Microsoft 365 license to your global administrator account.</span></span>
  
1. <span data-ttu-id="afa99-178">Utilisez une instance privée d’un navigateur Internet pour vous connecter au centre d’administration Microsoft 365 sur [https://admin.microsoft.com](https://admin.microsoft.com)à l’aide de vos informations d’identification de compte d’administrateur général.</span><span class="sxs-lookup"><span data-stu-id="afa99-178">With a private instance of an Internet browser, sign in to the Microsoft 365 admin center at [https://admin.microsoft.com](https://admin.microsoft.com) with your global administrator account credentials.</span></span>
    
2. <span data-ttu-id="afa99-179">Sur la page **Centre d’administration Microsoft 365**, dans le volet de navigation de gauche, cliquez sur **Facturation > Acheter des services**.</span><span class="sxs-lookup"><span data-stu-id="afa99-179">On the **Microsoft 365 admin center** page, in the left navigation, click **Billing > Purchase services**.</span></span>
    
3. <span data-ttu-id="afa99-180">Sur la page **Acheter des services**, cliquez sur **Microsoft 365 E5**, puis cliquez sur **Obtenir une version d’évaluation gratuite**.</span><span class="sxs-lookup"><span data-stu-id="afa99-180">On the **Purchase services** page, click **Microsoft 365 E5**, and then click **Get free trial**.</span></span>

4. <span data-ttu-id="afa99-181">Sur la page **version d’évaluation de Microsoft 365 E5**, choisissez de recevoir un SMS ou un appel, entrez votre numéro de téléphone, puis cliquez sur **envoyer un SMS** ou **m’appeler**.</span><span class="sxs-lookup"><span data-stu-id="afa99-181">On the **Microsoft 365 E5 Trial** page, choose to receive a text or a call, enter your phone number, then click **Text me** or **Call me**.</span></span> <span data-ttu-id="afa99-182">Effectuez la vérification.</span><span class="sxs-lookup"><span data-stu-id="afa99-182">Perform the verification.</span></span>

5. <span data-ttu-id="afa99-183">Dans la page **Confirmer votre commande**, cliquez sur **Essayer maintenant**.</span><span class="sxs-lookup"><span data-stu-id="afa99-183">On the **Confirm your order** page, click **Try now**.</span></span>

6. <span data-ttu-id="afa99-184">Dans la page **Réception de la commande**, cliquez sur **Continuer**.</span><span class="sxs-lookup"><span data-stu-id="afa99-184">On the **Order receipt** page, click **Continue**.</span></span>

7. <span data-ttu-id="afa99-185">Dans l’onglet Centre d’administration Microsoft 365, cliquez sur **Utilisateurs > Utilisateurs actifs**.</span><span class="sxs-lookup"><span data-stu-id="afa99-185">In the Microsoft 365 admin center, click **Users > Active users**.</span></span>

8. <span data-ttu-id="afa99-186">Dans **Utilisateurs actifs**, cliquez sur votre compte d’administrateur.</span><span class="sxs-lookup"><span data-stu-id="afa99-186">In **Active users**, click your administrator account.</span></span>

9. <span data-ttu-id="afa99-187">Cliquez sur **Licences et applications**.</span><span class="sxs-lookup"><span data-stu-id="afa99-187">Click **Licenses and apps**.</span></span>

10. <span data-ttu-id="afa99-188">Désactivez la licence pour Office 365 Entreprise E5 et activez la licence pour Microsoft 365 E5.</span><span class="sxs-lookup"><span data-stu-id="afa99-188">Disable the license for Office 365 Enterprise E5 and enable the license for Microsoft 365 E5.</span></span>

11. <span data-ttu-id="afa99-189">Cliquez sur **Enregistrer les modifications** puis fermez le volet informations sur le compte d’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="afa99-189">Click **Save changes** and then close the user account information pane.</span></span>

<span data-ttu-id="afa99-190">Ensuite, répétez les étapes 8 et 11 de la procédure précédente pour tous vos autres comptes (Utilisateur2, Utilisateur3, Utilisateur4 et Utilisateur5).</span><span class="sxs-lookup"><span data-stu-id="afa99-190">Next, repeat steps 8 through 11 of the previous procedure for all of your other accounts (User 2, User 3, User 4, and User 5).</span></span>
  
> [!NOTE]
> <span data-ttu-id="afa99-191">L’abonnement d’évaluation de Microsoft 365 E5 est de 30 jours.</span><span class="sxs-lookup"><span data-stu-id="afa99-191">The Microsoft 365 E5 trial subscription is 30 days.</span></span> <span data-ttu-id="afa99-192">Pour un environnement de test permanent, convertissez cet abonnement en abonnement payant avec un nombre réduit de licences.</span><span class="sxs-lookup"><span data-stu-id="afa99-192">For a permanent test environment, convert this trial subscription into a paid subscription with a small number of licenses.</span></span> 
  
<span data-ttu-id="afa99-193">Votre environnement de test comporte maintenant :</span><span class="sxs-lookup"><span data-stu-id="afa99-193">Your test environment now has:</span></span>
  
- <span data-ttu-id="afa99-194">Un abonnement d’évaluation de Microsoft 365 E5.</span><span class="sxs-lookup"><span data-stu-id="afa99-194">A Microsoft 365 E5 trial subscription.</span></span>
- <span data-ttu-id="afa99-195">Tous vos comptes d’utilisateur appropriés (l’administrateur général ou tous les cinq comptes d’utilisateur) sont activés pour utiliser Microsoft 365 E5.</span><span class="sxs-lookup"><span data-stu-id="afa99-195">All your appropriate user accounts (either just the global administrator or all five user accounts) are enabled to use Microsoft 365 E5.</span></span>
    
<span data-ttu-id="afa99-196">Voici la configuration obtenue, qui ajoute Microsoft 365 E5.</span><span class="sxs-lookup"><span data-stu-id="afa99-196">Here is your resulting configuration, which adds Microsoft 365 E5.</span></span>
  
![Phase 3 de l’environnement de test Microsoft 365 Entreprise](../media/lightweight-base-configuration-microsoft-365-enterprise/Phase2.png)
  
## <a name="phase-4-create-a-windows-10-enterprise-computer"></a><span data-ttu-id="afa99-198">Phase 4 : Création d’un ordinateur Windows 10 Entreprise</span><span class="sxs-lookup"><span data-stu-id="afa99-198">Phase 4: Create a Windows 10 Enterprise computer</span></span>

<span data-ttu-id="afa99-199">Au cours de cette phase, vous allez créer un ordinateur autonome exécutant Windows 10 Entreprise sous forme d’un ordinateur physique, d’une machine virtuelle ou d’une machine virtuelle Azure.</span><span class="sxs-lookup"><span data-stu-id="afa99-199">In this phase, you create a standalone computer running Windows 10 Enterprise as either a physical computer, a virtual machine, or an Azure virtual machine.</span></span>
  
### <a name="physical-computer"></a><span data-ttu-id="afa99-200">Ordinateur physique</span><span class="sxs-lookup"><span data-stu-id="afa99-200">Physical computer</span></span>

<span data-ttu-id="afa99-p109">Munissez-vous d’un ordinateur personnel et installez Windows 10 Entreprise dessus. Vous pouvez télécharger la version d’évaluation de Windows 10 Entreprise [ici](https://www.microsoft.com/evalcenter/evaluate-windows-10-enterprise).</span><span class="sxs-lookup"><span data-stu-id="afa99-p109">Obtain a personal computer and install Windows 10 Enterprise on it. You can download the Windows 10 Enterprise trial [here](https://www.microsoft.com/evalcenter/evaluate-windows-10-enterprise).</span></span>
  
### <a name="virtual-machine"></a><span data-ttu-id="afa99-203">Machine virtuelle</span><span class="sxs-lookup"><span data-stu-id="afa99-203">Virtual machine</span></span>

<span data-ttu-id="afa99-p110">Créez une machine virtuelle à l’aide de l’hyperviseur de votre choix et installez Windows 10 Entreprise dessus. Vous pouvez télécharger la version d’évaluation de Windows 10 Entreprise [ici](https://www.microsoft.com/evalcenter/evaluate-windows-10-enterprise).</span><span class="sxs-lookup"><span data-stu-id="afa99-p110">Create a virtual machine using the hypervisor of your choice and install Windows 10 Enterprise on it. You can download the Windows 10 Enterprise trial [here](https://www.microsoft.com/evalcenter/evaluate-windows-10-enterprise).</span></span>
  
### <a name="virtual-machine-in-azure"></a><span data-ttu-id="afa99-206">Machine virtuelle dans Azure</span><span class="sxs-lookup"><span data-stu-id="afa99-206">Virtual machine in Azure</span></span>

<span data-ttu-id="afa99-p111">Pour créer une machine virtuelle exécutant Windows 10 dans Microsoft Azure, ***vous devez disposer d’un abonnement Visual Studio*** qui vous permet d’accéder à l’image pour Windows 10 Entreprise. D’autres types d’abonnements Azure, tels que les abonnements d’évaluation et payants, ne permettent pas d’accéder à cette image. Pour obtenir les informations les plus récentes, reportez-vous à l’article [Utilisation d’un client Windows dans Azure pour les scénarios de développement et/ou test](https://docs.microsoft.com/azure/virtual-machines/windows/client-images).</span><span class="sxs-lookup"><span data-stu-id="afa99-p111">To create a Windows 10 virtual machine in Microsoft Azure, ***you must have a Visual Studio-based subscription***, which has access to the image for Windows 10 Enterprise. Other types of Azure subscriptions, such as trial and paid subscriptions, do not have access to this image. For the latest information, see [Use Windows client in Azure for dev/test scenarios](https://docs.microsoft.com/azure/virtual-machines/windows/client-images).</span></span>
  
> [!NOTE]
> <span data-ttu-id="afa99-p112">Les ensembles de commandes suivants utilisent la dernière version d’Azure PowerShell. Reportez-vous à l’article relatif à la [prise en main des cmdlets Azure PowerShell](https://docs.microsoft.com/powershell/azureps-cmdlets-docs/). Ces ensembles de commandes créent une machine virtuelle Windows 10 Entreprise nommée WIN10 ainsi que l’intégralité de son infrastructure requise, y compris un groupe de ressources, un compte de stockage et un réseau virtuel. Si vous connaissez déjà les services d’infrastructure Azure, adaptez ces instructions à votre infrastructure actuellement déployée.</span><span class="sxs-lookup"><span data-stu-id="afa99-p112">The following command sets use the latest version of Azure PowerShell. See [Get started with Azure PowerShell cmdlets](https://docs.microsoft.com/powershell/azureps-cmdlets-docs/). These command sets build a Windows 10 Enterprise virtual machine named WIN10 and all of its required infrastructure, including a resource group, a storage account, and a virtual network. If you are already familiar with Azure infrastructure services, please adapt these instructions to suit your currently deployed infrastructure.</span></span> 
  
<span data-ttu-id="afa99-214">Tout d’abord, lancez une invite Microsoft PowerShell.</span><span class="sxs-lookup"><span data-stu-id="afa99-214">First, start a Microsoft PowerShell prompt.</span></span>
  
<span data-ttu-id="afa99-215">Connectez-vous à votre compte Azure avec la commande suivante.</span><span class="sxs-lookup"><span data-stu-id="afa99-215">Sign in to your Azure account with the following command.</span></span>
  
```powershell
Connect-AzAccount
```

<span data-ttu-id="afa99-216">Obtenez le nom de votre abonnement à l’aide de la commande suivante.</span><span class="sxs-lookup"><span data-stu-id="afa99-216">Get your subscription name using the following command.</span></span>
  
```powershell
Get-AzSubscription | Sort Name | Select Name
```

<span data-ttu-id="afa99-p113">Définissez votre abonnement Azure. Remplacez tout le texte entre guillemets, y compris les caractères \< and >, avec le nom correct.</span><span class="sxs-lookup"><span data-stu-id="afa99-p113">Set your Azure subscription. Replace everything within the quotes, including the \< and > characters, with the correct name.</span></span>
  
```powershell
$subscr="<subscription name>"
Get-AzSubscription -SubscriptionName $subscr | Select-AzSubscription
```

<span data-ttu-id="afa99-p114">Ensuite, créez un nouveau groupe de ressources. Pour déterminer un nom de groupe de ressources unique, utilisez cette commande pour répertorier vos groupes de ressources existants.</span><span class="sxs-lookup"><span data-stu-id="afa99-p114">Next, create a new resource group. To determine a unique resource group name, use this command to list your existing resource groups.</span></span>
  
```powershell
Get-AzResourceGroup | Sort ResourceGroupName | Select ResourceGroupName
```

<span data-ttu-id="afa99-p115">Créez votre groupe de ressources avec ces commandes. Remplacez tout le texte entre guillemets, y compris les caractères \< and >, avec les noms corrects.</span><span class="sxs-lookup"><span data-stu-id="afa99-p115">Create your new resource group with these commands. Replace everything within the quotes, including the \< and > characters, with the correct names.</span></span>
  
```powershell
$rgName="<resource group name>"
$locName="<location name, such as West US>"
New-AzResourceGroup -Name $rgName -Location $locName
```

<span data-ttu-id="afa99-p116">Ensuite, créez une ressource virtuelle et la machine virtuelle WIN10 avec ces commandes. Lorsque vous y êtes invité, indiquez le nom et le mot de passe du compte d’administrateur local pour WIN10, et enregistrez ces informations dans un emplacement sécurisé.</span><span class="sxs-lookup"><span data-stu-id="afa99-p116">Next, you create a new virtual network and the WIN10 virtual machine with these commands. When prompted, provide the name and password of the local administrator account for WIN10 and store these in a secure location.</span></span>
  
```powershell
$corpnetSubnet=New-AzVirtualNetworkSubnetConfig -Name Corpnet -AddressPrefix 10.0.0.0/24
New-AzVirtualNetwork -Name "M365Ent-TestLab" -ResourceGroupName $rgName -Location $locName -AddressPrefix 10.0.0.0/8 -Subnet $corpnetSubnet
$rule1=New-AzNetworkSecurityRuleConfig -Name "RDPTraffic" -Description "Allow RDP to all VMs on the subnet" -Access Allow -Protocol Tcp -Direction Inbound -Priority 100 -SourceAddressPrefix Internet -SourcePortRange * -DestinationAddressPrefix * -DestinationPortRange 3389
New-AzNetworkSecurityGroup -Name Corpnet -ResourceGroupName $rgName -Location $locName -SecurityRules $rule1
$vnet=Get-AzVirtualNetwork -ResourceGroupName $rgName -Name "M365Ent-TestLab"
$nsg=Get-AzNetworkSecurityGroup -Name Corpnet -ResourceGroupName $rgName
Set-AzVirtualNetworkSubnetConfig -VirtualNetwork $vnet -Name Corpnet -AddressPrefix "10.0.0.0/24" -NetworkSecurityGroup $nsg
$vnet | Set-AzVirtualNetwork
$pip=New-AzPublicIpAddress -Name WIN10-PIP -ResourceGroupName $rgName -Location $locName -AllocationMethod Dynamic
$nic=New-AzNetworkInterface -Name WIN10-NIC -ResourceGroupName $rgName -Location $locName -SubnetId $vnet.Subnets[0].Id -PublicIpAddressId $pip.Id
$vm=New-AzVMConfig -VMName WIN10 -VMSize Standard_A2_V2
$cred=Get-Credential -Message "Type the name and password of the local administrator account for WIN10."
$vm=Set-AzVMOperatingSystem -VM $vm -Windows -ComputerName WIN10 -Credential $cred -ProvisionVMAgent -EnableAutoUpdate
$vm=Set-AzVMSourceImage -VM $vm -PublisherName MicrosoftWindowsDesktop -Offer Windows-10 -Skus RS3-Pro -Version "latest"
$vm=Add-AzVMNetworkInterface -VM $vm -Id $nic.Id
$vm=Set-AzVMOSDisk -VM $vm -Name WIN10-TestLab-OSDisk -DiskSizeInGB 128 -CreateOption FromImage
New-AzVM -ResourceGroupName $rgName -Location $locName -VM $vm
```

## <a name="phase-5-join-your-windows-10-computer-to-azure-ad"></a><span data-ttu-id="afa99-225">Phase 5 : Association de votre ordinateur Windows 10 à Azure AD</span><span class="sxs-lookup"><span data-stu-id="afa99-225">Phase 5: Join your Windows 10 computer to Azure AD</span></span>

<span data-ttu-id="afa99-226">Lorsque l’ordinateur physique ou la machine virtuelle avec Windows 10 Entreprise est créée, connectez-vous avec un compte d’administrateur local.</span><span class="sxs-lookup"><span data-stu-id="afa99-226">After the physical or virtual machine with Windows 10 Enterprise is created, sign in with a local administrator account.</span></span>
  
> [!NOTE]
> <span data-ttu-id="afa99-227">Suivez [ces instructions](https://docs.microsoft.com/azure/virtual-machines/windows/connect-logon) pour vous connecter à une machine virtuelle dans Azure.</span><span class="sxs-lookup"><span data-stu-id="afa99-227">For a virtual machine in Azure, connect to it using [these instructions](https://docs.microsoft.com/azure/virtual-machines/windows/connect-logon).</span></span>
  
<span data-ttu-id="afa99-228">Ensuite, associez l’ordinateur WIN10 au client Azure AD de votre abonnement Microsoft 365 E5.</span><span class="sxs-lookup"><span data-stu-id="afa99-228">Next, join the WIN10 computer to the Azure AD tenant of your Microsoft 365 E5 subscription.</span></span>
  
1. <span data-ttu-id="afa99-229">Sur le bureau de l’ordinateur WIN10, cliquez sur **Démarrer > Paramètres > Comptes > Accès Professionnel ou Scolaire > Se connecter**.</span><span class="sxs-lookup"><span data-stu-id="afa99-229">At the desktop of the WIN10 computer, click **Start > Settings > Accounts > Access work or school > Connect**.</span></span>
    
2. <span data-ttu-id="afa99-230">Dans la boîte de dialogue **Configurer un compte professionnel ou scolaire**, cliquez sur **Joindre cet appareil à Azure Active Directory**.</span><span class="sxs-lookup"><span data-stu-id="afa99-230">In the **Set up a work or school account** dialog box, click **Join this device to Azure Active Directory**.</span></span>
    
3. <span data-ttu-id="afa99-231">Dans **Compte professionnel ou scolaire**, saisissez le nom de compte Administrateur général de votre abonnement Microsoft 365 E5, puis cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="afa99-231">In **Work or school account**, type the global administrator account name of your Microsoft 365 E5 subscription, and then click **Next**.</span></span>
    
4. <span data-ttu-id="afa99-232">Dans **Saisie du mot de passe**, saisissez le mot de passe de votre compte Administrateur général, puis cliquez sur **Se connecter**.</span><span class="sxs-lookup"><span data-stu-id="afa99-232">In **Enter password**, type the password for your global administrator account, and then click **Sign in**.</span></span>
    
5. <span data-ttu-id="afa99-233">Lorsque vous devez confirmer qu’il s’agit bien de votre organisation, cliquez sur **Joindre**, puis sur **Terminé**.</span><span class="sxs-lookup"><span data-stu-id="afa99-233">When prompted to make sure this is your organization, click **Join**, and then click **Done**.</span></span>
    
6. <span data-ttu-id="afa99-234">Fermez la fenêtre Paramètres.</span><span class="sxs-lookup"><span data-stu-id="afa99-234">Close the settings window.</span></span>
    
<span data-ttu-id="afa99-235">Installez ensuite les applications Microsoft 365 pour les entreprises sur l’ordinateur WIN10.</span><span class="sxs-lookup"><span data-stu-id="afa99-235">Next, install Microsoft 365 Apps for enterprise on the WIN10 computer.</span></span>
  
1. <span data-ttu-id="afa99-236">Ouvrez le navigateur Microsoft Edge et connectez-vous au [Centre d’administration microsoft 365](https://admin.microsoft.com) avec vos informations d’identification de compte d’administrateur général.</span><span class="sxs-lookup"><span data-stu-id="afa99-236">Open the Microsoft Edge browser and sign in to the [Microsoft 365 admin center](https://admin.microsoft.com) with your global administrator account credentials.</span></span>
    
2. <span data-ttu-id="afa99-237">Dans l’onglet **Accueil Microsoft Office**, cliquez sur **Installer Office**.</span><span class="sxs-lookup"><span data-stu-id="afa99-237">On the **Microsoft Office Home** tab, click **Install Office**.</span></span>
    
3. <span data-ttu-id="afa99-238">Lorsque vous êtes invité à décider de l’action à effectuer, cliquez sur **Exécuter**, puis sur **Oui** pour **Contrôle de compte d’utilisateur**.</span><span class="sxs-lookup"><span data-stu-id="afa99-238">When prompted with what to do, click **Run**, and then click **Yes** for **User Account Control**.</span></span>
    
4. <span data-ttu-id="afa99-p117">Attendez qu’Office termine l’installation. Lorsque le message **Vous voilà prêt !** s’affiche, cliquez deux fois sur **Fermer**.</span><span class="sxs-lookup"><span data-stu-id="afa99-p117">Wait for Office to complete its installation. When you see **You're all set!**, click **Close** twice.</span></span>
    
<span data-ttu-id="afa99-241">Voici votre environnement final.</span><span class="sxs-lookup"><span data-stu-id="afa99-241">Here is your resulting environment.</span></span>

![Phase 5 de l’environnement de test Microsoft 365 Entreprise](../media/lightweight-base-configuration-microsoft-365-enterprise/Phase4.png)

<span data-ttu-id="afa99-243">Cela inclut l’ordinateur WIN10 avec :</span><span class="sxs-lookup"><span data-stu-id="afa99-243">This includes the WIN10 computer that has:</span></span>

- <span data-ttu-id="afa99-244">rejoint le client Azure AD de votre abonnement Microsoft 365 E5 ;</span><span class="sxs-lookup"><span data-stu-id="afa99-244">Joined the Azure AD tenant of your Microsoft 365 E5 subscription.</span></span>
- <span data-ttu-id="afa99-245">été inscrit en tant que périphérique Azure AD dans Microsoft Intune (EMS) ;</span><span class="sxs-lookup"><span data-stu-id="afa99-245">Enrolled as an Azure AD device in Microsoft Intune (EMS).</span></span>
- <span data-ttu-id="afa99-246">Les applications Microsoft 365 pour les entreprises sont-elles installées.</span><span class="sxs-lookup"><span data-stu-id="afa99-246">Has Microsoft 365 Apps for enterprise installed.</span></span>
  
<span data-ttu-id="afa99-247">Vous êtes maintenant prêt à tester les fonctionnalités supplémentaires de [Microsoft 365 pour entreprises](https://www.microsoft.com/microsoft-365/enterprise).</span><span class="sxs-lookup"><span data-stu-id="afa99-247">You are now ready to experiment with additional features of [Microsoft 365 for enterprise](https://www.microsoft.com/microsoft-365/enterprise).</span></span>
  
## <a name="next-steps"></a><span data-ttu-id="afa99-248">Étapes suivantes</span><span class="sxs-lookup"><span data-stu-id="afa99-248">Next steps</span></span>

<span data-ttu-id="afa99-249">Découvrez les nouveaux ensembles de guides pour les tests de laboratoire :</span><span class="sxs-lookup"><span data-stu-id="afa99-249">Explore these additional sets of Test Lab Guides:</span></span>
  
- [<span data-ttu-id="afa99-250">Identité</span><span class="sxs-lookup"><span data-stu-id="afa99-250">Identity</span></span>](m365-enterprise-test-lab-guides.md#identity)
- [<span data-ttu-id="afa99-251">Gestion des appareils mobiles</span><span class="sxs-lookup"><span data-stu-id="afa99-251">Mobile device management</span></span>](m365-enterprise-test-lab-guides.md#mobile-device-management)
- [<span data-ttu-id="afa99-252">Protection des informations</span><span class="sxs-lookup"><span data-stu-id="afa99-252">Information protection</span></span>](m365-enterprise-test-lab-guides.md#information-protection)
   

## <a name="see-also"></a><span data-ttu-id="afa99-253">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="afa99-253">See also</span></span>

[<span data-ttu-id="afa99-254">Microsoft 365 pour les entreprises Guides de laboratoire d'essai</span><span class="sxs-lookup"><span data-stu-id="afa99-254">Microsoft 365 for enterprise Test Lab Guides</span></span>](m365-enterprise-test-lab-guides.md)

[<span data-ttu-id="afa99-255">Vue d’ensemble de Microsoft 365 pour entreprise</span><span class="sxs-lookup"><span data-stu-id="afa99-255">Microsoft 365 for enterprise overview</span></span>](microsoft-365-overview.md)

[<span data-ttu-id="afa99-256">Documentation Microsoft 365 pour entreprise</span><span class="sxs-lookup"><span data-stu-id="afa99-256">Microsoft 365 for enterprise documentation</span></span>](https://docs.microsoft.com/microsoft-365-enterprise/)
