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
description: Utilisez ce guide de laboratoire de test pour créer un environnement de test léger pour les tests Microsoft 365 entreprise.
ms.openlocfilehash: 2de0760cef7339f62229575b1e0a54b3c67a4e9f
ms.sourcegitcommit: 27b2b2e5c41934b918cac2c171556c45e36661bf
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/19/2021
ms.locfileid: "50909705"
---
# <a name="the-lightweight-base-configuration"></a><span data-ttu-id="19b41-103">Configuration de base légère</span><span class="sxs-lookup"><span data-stu-id="19b41-103">The lightweight base configuration</span></span>

<span data-ttu-id="19b41-104">*Ce guide de laboratoire de test peut être utilisé à la fois pour Microsoft 365'entreprise et Office 365 Entreprise environnements de test.*</span><span class="sxs-lookup"><span data-stu-id="19b41-104">*This Test Lab Guide can be used for both Microsoft 365 for enterprise and Office 365 Enterprise test environments.*</span></span>

<span data-ttu-id="19b41-105">Cet article explique comment créer un environnement simplifié avec un abonnement Microsoft 365 E5 et un ordinateur exécutant Windows 10 Entreprise.</span><span class="sxs-lookup"><span data-stu-id="19b41-105">This article describes how to create a simplified environment with a Microsoft 365 E5 subscription and a computer running Windows 10 Enterprise.</span></span>

![Environnement de test Microsoft 365 Entreprise léger](../media/lightweight-base-configuration-microsoft-365-enterprise/Phase4.png)

<span data-ttu-id="19b41-107">La création d’un environnement de test léger implique cinq phases :</span><span class="sxs-lookup"><span data-stu-id="19b41-107">Creating a lightweight test environment involves five phases:</span></span>
- [<span data-ttu-id="19b41-108">Phase 1 : Créer votre abonnement Microsoft 365 E5 abonnement</span><span class="sxs-lookup"><span data-stu-id="19b41-108">Phase 1: Create your Microsoft 365 E5 subscription</span></span>](#phase-1-create-your-microsoft-365-e5-subscription)
- [<span data-ttu-id="19b41-109">Phase 2 : configuration de votre abonnement d’évaluation Office 365</span><span class="sxs-lookup"><span data-stu-id="19b41-109">Phase 2: Configure your Office 365 trial subscription</span></span>](#phase-2-configure-your-office-365-trial-subscription)
- [<span data-ttu-id="19b41-110">Phase 3 : Ajoutez un abonnement d’évaluation Microsoft 365 E5.</span><span class="sxs-lookup"><span data-stu-id="19b41-110">Phase 3: Add a Microsoft 365 E5 trial subscription</span></span>](#phase-3-add-a-microsoft-365-e5-trial-subscription)
- [<span data-ttu-id="19b41-111">Phase 4 : Création d’un ordinateur Windows 10 Entreprise</span><span class="sxs-lookup"><span data-stu-id="19b41-111">Phase 4: Create a Windows 10 Enterprise computer</span></span>](#phase-4-create-a-windows-10-enterprise-computer)
- [<span data-ttu-id="19b41-112">Phase 5 : Association de votre ordinateur Windows 10 à Azure AD</span><span class="sxs-lookup"><span data-stu-id="19b41-112">Phase 5: Join your Windows 10 computer to Azure AD</span></span>](#phase-5-join-your-windows-10-computer-to-azure-ad)

<span data-ttu-id="19b41-113">Utilisez l’environnement résultant pour tester les fonctionnalités de Microsoft 365 [entreprise.](https://www.microsoft.com/microsoft-365/enterprise)</span><span class="sxs-lookup"><span data-stu-id="19b41-113">Use the resulting environment to test the features and functionality of [Microsoft 365 for enterprise](https://www.microsoft.com/microsoft-365/enterprise).</span></span>

![Guides de laboratoire de test pour Microsoft Cloud](../media/m365-enterprise-test-lab-guides/cloud-tlg-icon.png)
  
> [!TIP]
> <span data-ttu-id="19b41-115">Pour obtenir une carte visuelle de tous les articles de la pile Microsoft 365 guide de laboratoire de test pour entreprise, voir Microsoft 365 [for enterprise Test Lab Guide Stack](../downloads/Microsoft365EnterpriseTLGStack.pdf).</span><span class="sxs-lookup"><span data-stu-id="19b41-115">For a visual map to all the articles in the Microsoft 365 for enterprise Test Lab Guide stack, see [Microsoft 365 for enterprise Test Lab Guide Stack](../downloads/Microsoft365EnterpriseTLGStack.pdf).</span></span>

>[!NOTE]
><span data-ttu-id="19b41-116">Nous vous recommandons d’imprimer cet article afin de consigner les informations dont vous aurez besoin dans cet environnement au cours des 30 jours de votre abonnement à la version d’évaluation Office 365.</span><span class="sxs-lookup"><span data-stu-id="19b41-116">You might want to print this article to record the specific information that you will need for this environment over the 30 days of the Office 365 trial subscription.</span></span> <span data-ttu-id="19b41-117">Vous pouvez facilement étendre l’abonnement d’évaluation pour une période supplémentaire de 30 jours.</span><span class="sxs-lookup"><span data-stu-id="19b41-117">You can easily extend the trail subscription for another 30 days.</span></span> <span data-ttu-id="19b41-118">Pour un environnement de développement/test permanent, créez un nouvel abonnement payant avec un client Azure AD séparé et un nombre réduit de licences.</span><span class="sxs-lookup"><span data-stu-id="19b41-118">For a permanent test environment, create a new paid subscription with a separate Azure AD tenant and a small number of licenses.</span></span>

## <a name="phase-1-create-your-microsoft-365-e5-subscription"></a><span data-ttu-id="19b41-119">Phase 1 : Créer votre abonnement Microsoft 365 E5 abonnement</span><span class="sxs-lookup"><span data-stu-id="19b41-119">Phase 1: Create your Microsoft 365 E5 subscription</span></span>

<span data-ttu-id="19b41-120">Nous commençons par un abonnement Microsoft 365 E5 d’essai, puis nous y ajoutons Microsoft 365 E5'abonnement.</span><span class="sxs-lookup"><span data-stu-id="19b41-120">We start with an Microsoft 365 E5 trial subscription and then add the Microsoft 365 E5 subscription to it.</span></span>

>[!NOTE]
><span data-ttu-id="19b41-121">Nous vous recommandons de créer un abonnement d’essai de Office 365 afin que votre environnement de test dispose d’un client Azure AD distinct de tous les abonnements payants dont vous disposez actuellement.</span><span class="sxs-lookup"><span data-stu-id="19b41-121">We recommend that you create a trial subscription of Office 365 so that your test environment has a separate Azure AD tenant from any paid subscriptions you currently have.</span></span> <span data-ttu-id="19b41-122">Cette séparation signifie que vous pouvez ajouter et supprimer des utilisateurs et des groupes dans le client test sans affecter vos abonnements de production.</span><span class="sxs-lookup"><span data-stu-id="19b41-122">This separation means that you can add and remove users and groups in the test tenant without affecting your production subscriptions.</span></span>

<span data-ttu-id="19b41-123">Pour démarrer votre abonnement d’évaluation Microsoft 365 E5, vous avez besoin d’un nom d’entreprise fictif et d’un nouveau compte Microsoft.</span><span class="sxs-lookup"><span data-stu-id="19b41-123">To start your Microsoft 365 E5 trial subscription, you first need a fictitious company name and a new Microsoft account.</span></span>
  
1. <span data-ttu-id="19b41-p103">Nous vous recommandons d’utiliser une variante du nom d’entreprise Contoso pour le nom de votre entreprise. Il s’agit d’une entreprise fictive utilisée dans le contenu d’exemple de Microsoft. Toutefois, cette étape n’est pas obligatoire. Indiquer le nom fictif de votre entreprise ici :</span><span class="sxs-lookup"><span data-stu-id="19b41-p103">We recommend that you use a variant of the company name Contoso for your company name, which is a fictitious company used in Microsoft sample content, but it isn't required. Record your fictitious company name here:</span></span> ![Trait](../media/Common-Images/TableLine.png)
    
2. <span data-ttu-id="19b41-p104">Pour ouvrir un nouveau compte Microsoft, accédez à [https://outlook.com](https://outlook.com) et créez un compte avec un nouveau compte de messagerie et une nouvelle adresse. Vous utiliserez ce compte pour vous inscrire à Office 365.</span><span class="sxs-lookup"><span data-stu-id="19b41-p104">To sign up for a new Microsoft account, go to [https://outlook.com](https://outlook.com) and create an account with a new email account and address. You will use this account to sign up for Office 365.</span></span>
    
    - <span data-ttu-id="19b41-129">Enregistrez le prénom et le nom de famille utilisés pour votre nouveau compte ici :</span><span class="sxs-lookup"><span data-stu-id="19b41-129">Record the first and last name of your new account here:</span></span> ![Trait](../media/Common-Images/TableLine.png)
    
    - <span data-ttu-id="19b41-131">Enregistrez l’adresse du nouveau compte de messagerie ici :</span><span class="sxs-lookup"><span data-stu-id="19b41-131">Record the new email account address here:</span></span> ![Trait](../media/Common-Images/TableLine.png)<span data-ttu-id="19b41-133">@outlook.com</span><span class="sxs-lookup"><span data-stu-id="19b41-133">@outlook.com</span></span>
    
### <a name="sign-up-for-an-office-365-e5-trial-subscription"></a><span data-ttu-id="19b41-134">Inscription à un abonnement d’évaluation Office 365 E5</span><span class="sxs-lookup"><span data-stu-id="19b41-134">Sign up for an Office 365 E5 trial subscription</span></span>

1. <span data-ttu-id="19b41-135">Dans votre navigateur, allez à [https://aka.ms/e5trial](https://aka.ms/e5trial) .</span><span class="sxs-lookup"><span data-stu-id="19b41-135">In your browser, go to [https://aka.ms/e5trial](https://aka.ms/e5trial).</span></span>
    
2. <span data-ttu-id="19b41-136">À l’étape 1 de la page Merci d’avoir choisi **Office 365 E5,** entrez votre nouvelle adresse de compte de messagerie.</span><span class="sxs-lookup"><span data-stu-id="19b41-136">In step 1 of the **Thank you for choosing Office 365 E5** page, enter your new email account address.</span></span>
3. <span data-ttu-id="19b41-137">À l’étape 2 du processus d’abonnement de piste, entrez les informations demandées, puis effectuez la vérification.</span><span class="sxs-lookup"><span data-stu-id="19b41-137">In step 2 of the trail subscription process, enter the requested information, and then perform the verification.</span></span>
4. <span data-ttu-id="19b41-138">À l’étape 3, entrez un nom d’organisation, puis un nom de compte qui sera l’administrateur global de l’abonnement.</span><span class="sxs-lookup"><span data-stu-id="19b41-138">In step 3, enter an organization name and then an account name that will be the global admin for the subscription.</span></span>
5. <span data-ttu-id="19b41-139">À l’étape 4, enregistrer l’URL de la page de connexion ici (sélectionnez-la et copiez-la) :</span><span class="sxs-lookup"><span data-stu-id="19b41-139">For step 4, record the sign-in page here (select and copy):</span></span> ![Trait](../media/Common-Images/TableLine.png)
6. <span data-ttu-id="19b41-141">Enregistrez l’identifiant utilisateur ici : ![ligne](../media/Common-Images/TableLine.png).onmicrosoft.com</span><span class="sxs-lookup"><span data-stu-id="19b41-141">Record the user ID here: ![Line](../media/Common-Images/TableLine.png).onmicrosoft.com</span></span>  
   <span data-ttu-id="19b41-142">Enregistrez le mot de passe que vous avez entré dans un emplacement sécurisé.</span><span class="sxs-lookup"><span data-stu-id="19b41-142">Record the password that you entered in a secure location.</span></span>
   <span data-ttu-id="19b41-143">Cette valeur correspond au **nom de l’administrateur général**.</span><span class="sxs-lookup"><span data-stu-id="19b41-143">This value will be referred to as the **global administrator name**.</span></span>
7. <span data-ttu-id="19b41-144">Sélectionnez **Aller au programme d’installation.**</span><span class="sxs-lookup"><span data-stu-id="19b41-144">Select **Go to Setup**.</span></span>
8. <span data-ttu-id="19b41-145">In Office 365 E5 Setup, select **Continue using your *organization*.onmicrosoft.com for email and signing in,** and then select **Exit and continue later**.</span><span class="sxs-lookup"><span data-stu-id="19b41-145">In Office 365 E5 Setup, select **Continue using *your organization*.onmicrosoft.com for email and signing in**, and then select **Exit and continue later**.</span></span>

<span data-ttu-id="19b41-146">Le Centre d’administration Microsoft 365 doit s’afficher.</span><span class="sxs-lookup"><span data-stu-id="19b41-146">You should see the Microsoft 365 admin center.</span></span>
    
## <a name="phase-2-configure-your-office-365-trial-subscription"></a><span data-ttu-id="19b41-147">Phase 2 : configuration de votre abonnement d’évaluation Office 365</span><span class="sxs-lookup"><span data-stu-id="19b41-147">Phase 2: Configure your Office 365 trial subscription</span></span>

<span data-ttu-id="19b41-148">Durant cette phase, configurez votre abonnement en y ajoutant des utilisateurs supplémentaires et assignez-leur des licences Office 365 E5.</span><span class="sxs-lookup"><span data-stu-id="19b41-148">In this phase, you configure your subscription with additional users and assign them Office 365 E5 licenses.</span></span>
  
<span data-ttu-id="19b41-149">Pour vous connecter à votre abonnement avec le module Azure Active Directory PowerShell pour Graph à partir de votre ordinateur, utilisez les instructions de Connecter pour [Microsoft 365 avec PowerShell.](connect-to-microsoft-365-powershell.md#connect-with-the-azure-active-directory-powershell-for-graph-module)</span><span class="sxs-lookup"><span data-stu-id="19b41-149">To connect to your subscription with the Azure Active Directory PowerShell for Graph module from your computer, use the instructions in [Connect to Microsoft 365 with PowerShell](connect-to-microsoft-365-powershell.md#connect-with-the-azure-active-directory-powershell-for-graph-module).</span></span>
    
<span data-ttu-id="19b41-150">Dans la **boîte Windows PowerShell demande d’informations** d’identification, entrez le nom de l’administrateur général *(par* exemple, jdoe@contosotoycompany.onmicrosoft.com ) et le mot de passe.</span><span class="sxs-lookup"><span data-stu-id="19b41-150">In the **Windows PowerShell Credential Request** dialog box, enter the global administrator name (for example, *jdoe@contosotoycompany.onmicrosoft.com*) and password.</span></span>
  
<span data-ttu-id="19b41-151">Remplissez le nom de votre organisation (par exemple, *contosotoycompany*), le code de pays à deux caractères de votre emplacement, un mot de passe de compte commun, puis exécutez les commandes suivantes à partir de l’invite PowerShell :</span><span class="sxs-lookup"><span data-stu-id="19b41-151">Fill in your organization name (for example, *contosotoycompany*), the two-character country code for your location, a common account password, and then run the following commands from the PowerShell prompt:</span></span>

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
> <span data-ttu-id="19b41-152">L’utilisation ici d’un mot de passe courant est destinée à l’automatisation et à la simplification de la configuration pour un environnement de test.</span><span class="sxs-lookup"><span data-stu-id="19b41-152">The use of a common password here is for automation and ease of configuration for a test environment.</span></span> <span data-ttu-id="19b41-153">Bien évidemment, cela est hautement déconseillé pour les abonnements de production.</span><span class="sxs-lookup"><span data-stu-id="19b41-153">Obviously, this is highly discouraged for production subscriptions.</span></span> 

### <a name="record-key-information-for-future-reference"></a><span data-ttu-id="19b41-154">Enregistrer les informations clés pour future référence</span><span class="sxs-lookup"><span data-stu-id="19b41-154">Record key information for future reference</span></span>

<span data-ttu-id="19b41-155">Si vous n’avez pas encore enregistré ces valeurs, enregistrez-les maintenant :</span><span class="sxs-lookup"><span data-stu-id="19b41-155">If you haven't already recorded these values, record them now:</span></span>
  
- <span data-ttu-id="19b41-156">Nom de l’administrateur général :</span><span class="sxs-lookup"><span data-stu-id="19b41-156">Global administrator name:</span></span> ![Trait](../media/Common-Images/TableLine.png)<span data-ttu-id="19b41-158">.onmicrosoft.com(à partir de l’étape 6 de la phase 1)</span><span class="sxs-lookup"><span data-stu-id="19b41-158">.onmicrosoft.com (from step 6 of Phase 1)</span></span>
    
    <span data-ttu-id="19b41-159">Enregistrez également le mot de passe de ce compte dans un emplacement sécurisé.</span><span class="sxs-lookup"><span data-stu-id="19b41-159">Also record the password for this account in a secure location.</span></span>
    
- <span data-ttu-id="19b41-160">Nom de l’organisation bénéficiant de l’abonnement à la version d’évaluation :</span><span class="sxs-lookup"><span data-stu-id="19b41-160">Your trial subscription organization name:</span></span> ![Trait](../media/Common-Images/TableLine.png) <span data-ttu-id="19b41-162">(à partir de l’étape 4 de la phase 1)</span><span class="sxs-lookup"><span data-stu-id="19b41-162">(from step 4 of Phase 1)</span></span>
    
- <span data-ttu-id="19b41-163">Pour répertorier les comptes pour Utilisateur 2, Utilisateur 3, Utilisateur 4 et Utilisateur 5, exécutez la commande suivante à partir de l’invite Module Windows Azure Active Directory pour Windows PowerShell :</span><span class="sxs-lookup"><span data-stu-id="19b41-163">To list the accounts for User 2, User 3, User 4, and User 5, run the following command from the Windows Azure Active Directory Module for Windows PowerShell prompt:</span></span>
    
  ```powershell
  Get-AzureADUser | Sort UserPrincipalName | Select UserPrincipalName
  ```

    <span data-ttu-id="19b41-164">Enregistrez les noms de compte ici :</span><span class="sxs-lookup"><span data-stu-id="19b41-164">Record the account names here:</span></span>
    
  - <span data-ttu-id="19b41-165">Nom du compte de l’utilisateur 2 : utilisateur2@</span><span class="sxs-lookup"><span data-stu-id="19b41-165">User 2 account name: user2@</span></span>![Trait](../media/Common-Images/TableLine.png)<span data-ttu-id="19b41-167">.onmicrosoft.com</span><span class="sxs-lookup"><span data-stu-id="19b41-167">.onmicrosoft.com</span></span>
    
  - <span data-ttu-id="19b41-168">Nom du compte de l’utilisateur 3 : utilisateur3@</span><span class="sxs-lookup"><span data-stu-id="19b41-168">User 3 account name: user3@</span></span>![Trait](../media/Common-Images/TableLine.png)<span data-ttu-id="19b41-170">.onmicrosoft.com</span><span class="sxs-lookup"><span data-stu-id="19b41-170">.onmicrosoft.com</span></span>
    
  - <span data-ttu-id="19b41-171">Nom du compte de l’utilisateur 4 : utilisateur4@</span><span class="sxs-lookup"><span data-stu-id="19b41-171">User 4 account name: user4@</span></span>![Trait](../media/Common-Images/TableLine.png)<span data-ttu-id="19b41-173">.onmicrosoft.com</span><span class="sxs-lookup"><span data-stu-id="19b41-173">.onmicrosoft.com</span></span>
    
  - <span data-ttu-id="19b41-174">Nom du compte de l’utilisateur 5 : utilisateur5@</span><span class="sxs-lookup"><span data-stu-id="19b41-174">User 5 account name: user5@</span></span>![Trait](../media/Common-Images/TableLine.png)<span data-ttu-id="19b41-176">.onmicrosoft.com</span><span class="sxs-lookup"><span data-stu-id="19b41-176">.onmicrosoft.com</span></span>
    
    <span data-ttu-id="19b41-177">Enregistrez également les mots de passe communs de ces comptes dans un emplacement sécurisé.</span><span class="sxs-lookup"><span data-stu-id="19b41-177">Also record the common password for these accounts in a secure location.</span></span>
   
### <a name="using-an-office-365-test-environment"></a><span data-ttu-id="19b41-178">Utilisation d’un environnement de test Office 365</span><span class="sxs-lookup"><span data-stu-id="19b41-178">Using an Office 365 test environment</span></span>

<span data-ttu-id="19b41-179">Si vous n’avez besoin Office 365 environnement de test, vous n’avez pas besoin de lire le reste de cet article.</span><span class="sxs-lookup"><span data-stu-id="19b41-179">If you need only an Office 365 test environment, you do not need to read the rest of this article.</span></span>

<span data-ttu-id="19b41-180">Pour obtenir des guides de laboratoire de test supplémentaires qui s’appliquent à Office 365 et Microsoft 365, voir Microsoft 365 guides de laboratoire de test pour [entreprise.](m365-enterprise-test-lab-guides.md)</span><span class="sxs-lookup"><span data-stu-id="19b41-180">For additional Test Lab Guides that apply to both Office 365 and Microsoft 365, see [Microsoft 365 for enterprise Test Lab Guides](m365-enterprise-test-lab-guides.md).</span></span>
  
## <a name="phase-3-add-a-microsoft-365-e5-trial-subscription"></a><span data-ttu-id="19b41-181">Phase 3 : Ajoutez un abonnement d’évaluation Microsoft 365 E5.</span><span class="sxs-lookup"><span data-stu-id="19b41-181">Phase 3: Add a Microsoft 365 E5 trial subscription</span></span>

<span data-ttu-id="19b41-182">Dans cette phase, vous vous inscrivez pour l’abonnement d’évaluation Microsoft 365 E5 et l’ajoutez à la même organisation que votre abonnement d’évaluation d’Office 365 E5.</span><span class="sxs-lookup"><span data-stu-id="19b41-182">In this phase, you sign up for the Microsoft 365 E5 trial subscription and add it to the same organization as your Office 365 E5 trial subscription.</span></span>
  
<span data-ttu-id="19b41-183">Tout d’abord, ajoutez l’abonnement d’évaluation Microsoft 365 E5 et attribuez une licence Microsoft 365 à votre compte d’administrateur général.</span><span class="sxs-lookup"><span data-stu-id="19b41-183">First, add the Microsoft 365 E5 trial subscription and assign the new Microsoft 365 license to your global administrator account.</span></span>
  
1. <span data-ttu-id="19b41-184">Dans une fenêtre privée de navigateur Internet, utilisez vos informations d’identification de compte d’administrateur général pour vous Microsoft 365 centre d’administration à l’adresse [https://admin.microsoft.com](https://admin.microsoft.com) .</span><span class="sxs-lookup"><span data-stu-id="19b41-184">In an internet browser private window, use your global administrator account credentials to sign in to the Microsoft 365 admin center at [https://admin.microsoft.com](https://admin.microsoft.com).</span></span>
    
2. <span data-ttu-id="19b41-185">Dans la page **Microsoft 365 centre d’administration,** dans le navigation de gauche, sélectionnez **Facturation > acheter des services.**</span><span class="sxs-lookup"><span data-stu-id="19b41-185">On the **Microsoft 365 admin center** page, in the left navigation, select **Billing > Purchase services**.</span></span>
    
3. <span data-ttu-id="19b41-186">Dans la page **Acheter des services,** **sélectionnez Microsoft 365 E5,** puis **sélectionnez Obtenir une version d’essai gratuite.**</span><span class="sxs-lookup"><span data-stu-id="19b41-186">On the **Purchase services** page, select **Microsoft 365 E5**, and then select **Get free trial**.</span></span>

4. <span data-ttu-id="19b41-187">Dans la page **Microsoft 365 E5** d’essai, décidez de recevoir un SMS ou un  appel téléphonique, entrez votre numéro de téléphone, puis sélectionnez M’envoyer un sms ou **m’appeler.**</span><span class="sxs-lookup"><span data-stu-id="19b41-187">On the **Microsoft 365 E5 Trial** page, decide to receive a text message or a phone call, enter your phone number, and then select **Text me** or **Call me**.</span></span> <span data-ttu-id="19b41-188">Effectuez la vérification.</span><span class="sxs-lookup"><span data-stu-id="19b41-188">Perform the verification.</span></span>

5. <span data-ttu-id="19b41-189">Dans la page **Confirmer votre commande,** **sélectionnez Essayer maintenant.**</span><span class="sxs-lookup"><span data-stu-id="19b41-189">On the **Confirm your order** page, select **Try now**.</span></span>

6. <span data-ttu-id="19b41-190">Dans la page **Reçu de** commande, sélectionnez **Continuer.**</span><span class="sxs-lookup"><span data-stu-id="19b41-190">On the **Order receipt** page, select **Continue**.</span></span>

7. <span data-ttu-id="19b41-191">Dans le centre Microsoft 365' administration, sélectionnez **Utilisateurs > utilisateurs actifs.**</span><span class="sxs-lookup"><span data-stu-id="19b41-191">In the Microsoft 365 admin center, select **Users > Active users**.</span></span>

8. <span data-ttu-id="19b41-192">Dans **les utilisateurs actifs,** sélectionnez votre compte d’administrateur.</span><span class="sxs-lookup"><span data-stu-id="19b41-192">In **Active users**, select your administrator account.</span></span>

9. <span data-ttu-id="19b41-193">Sélectionnez **licences et applications.**</span><span class="sxs-lookup"><span data-stu-id="19b41-193">Select **Licenses and apps**.</span></span>

10. <span data-ttu-id="19b41-194">Désactivez la licence pour Office 365 Entreprise E5 et activez la licence pour Microsoft 365 E5.</span><span class="sxs-lookup"><span data-stu-id="19b41-194">Disable the license for Office 365 Enterprise E5 and enable the license for Microsoft 365 E5.</span></span>

11. <span data-ttu-id="19b41-195">Sélectionnez **Enregistrer les modifications,** puis fermez le volet d’informations du compte d’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="19b41-195">Select **Save changes**, and then close the user account information pane.</span></span>

<span data-ttu-id="19b41-196">Ensuite, répétez les étapes 8 et 11 de la procédure précédente pour tous vos autres comptes (Utilisateur2, Utilisateur3, Utilisateur4 et Utilisateur5).</span><span class="sxs-lookup"><span data-stu-id="19b41-196">Next, repeat steps 8 through 11 of the previous procedure for all of your other accounts (User 2, User 3, User 4, and User 5).</span></span>
  
> [!NOTE]
> <span data-ttu-id="19b41-197">La durée de l’Microsoft 365 E5 d’essai est de 30 jours.</span><span class="sxs-lookup"><span data-stu-id="19b41-197">The length of the Microsoft 365 E5 trial subscription is 30 days.</span></span> <span data-ttu-id="19b41-198">Pour un environnement de test permanent, convertissez cet abonnement en abonnement payant avec un nombre réduit de licences.</span><span class="sxs-lookup"><span data-stu-id="19b41-198">For a permanent test environment, convert this trial subscription into a paid subscription with a small number of licenses.</span></span>
  
<span data-ttu-id="19b41-199">Votre environnement de test comporte maintenant :</span><span class="sxs-lookup"><span data-stu-id="19b41-199">Your test environment now has:</span></span>
  
- <span data-ttu-id="19b41-200">Un abonnement d’évaluation de Microsoft 365 E5.</span><span class="sxs-lookup"><span data-stu-id="19b41-200">A Microsoft 365 E5 trial subscription.</span></span>
- <span data-ttu-id="19b41-201">Tous vos comptes d’utilisateur appropriés (l’administrateur général ou tous les cinq comptes d’utilisateur) sont activés pour utiliser Microsoft 365 E5.</span><span class="sxs-lookup"><span data-stu-id="19b41-201">All your appropriate user accounts (either just the global administrator or all five user accounts) are enabled to use Microsoft 365 E5.</span></span>
    
<span data-ttu-id="19b41-202">Votre configuration résultante, qui ajoute des Microsoft 365 E5, se ressemble à ceci :</span><span class="sxs-lookup"><span data-stu-id="19b41-202">Your resulting configuration, which adds Microsoft 365 E5, looks like this:</span></span>
  
![Phase 3 de l’environnement de test Microsoft 365 Entreprise](../media/lightweight-base-configuration-microsoft-365-enterprise/Phase2.png)
  
## <a name="phase-4-create-a-windows-10-enterprise-computer"></a><span data-ttu-id="19b41-204">Phase 4 : Création d’un ordinateur Windows 10 Entreprise</span><span class="sxs-lookup"><span data-stu-id="19b41-204">Phase 4: Create a Windows 10 Enterprise computer</span></span>

<span data-ttu-id="19b41-205">Au cours de cette phase, vous allez créer un ordinateur autonome exécutant Windows 10 Entreprise sous forme d’un ordinateur physique, d’une machine virtuelle ou d’une machine virtuelle Azure.</span><span class="sxs-lookup"><span data-stu-id="19b41-205">In this phase, you create a standalone computer running Windows 10 Enterprise as either a physical computer, a virtual machine, or an Azure virtual machine.</span></span>
  
### <a name="physical-computer"></a><span data-ttu-id="19b41-206">Ordinateur physique</span><span class="sxs-lookup"><span data-stu-id="19b41-206">Physical computer</span></span>

<span data-ttu-id="19b41-207">Sur un ordinateur personnel, installez Windows 10 Entreprise.</span><span class="sxs-lookup"><span data-stu-id="19b41-207">On a personal computer, install Windows 10 Enterprise.</span></span> <span data-ttu-id="19b41-208">Vous pouvez télécharger la version Windows 10 Entreprise [d’essai ici.](https://www.microsoft.com/evalcenter/evaluate-windows-10-enterprise)</span><span class="sxs-lookup"><span data-stu-id="19b41-208">You can download the Windows 10 Enterprise trial [here](https://www.microsoft.com/evalcenter/evaluate-windows-10-enterprise).</span></span>
  
### <a name="virtual-machine"></a><span data-ttu-id="19b41-209">Machine virtuelle</span><span class="sxs-lookup"><span data-stu-id="19b41-209">Virtual machine</span></span>

<span data-ttu-id="19b41-210">Utilisez l’hyperviseur de votre choix pour créer une machine virtuelle, puis installez-Windows 10 Entreprise dessus.</span><span class="sxs-lookup"><span data-stu-id="19b41-210">Use the hypervisor of your choice to create a virtual machine, and then install Windows 10 Enterprise on it.</span></span> <span data-ttu-id="19b41-211">Vous pouvez télécharger la version Windows 10 Entreprise [d’essai ici.](https://www.microsoft.com/evalcenter/evaluate-windows-10-enterprise)</span><span class="sxs-lookup"><span data-stu-id="19b41-211">You can download the Windows 10 Enterprise trial [here](https://www.microsoft.com/evalcenter/evaluate-windows-10-enterprise).</span></span>
  
### <a name="virtual-machine-in-azure"></a><span data-ttu-id="19b41-212">Machine virtuelle dans Azure</span><span class="sxs-lookup"><span data-stu-id="19b41-212">Virtual machine in Azure</span></span>

<span data-ttu-id="19b41-p111">Pour créer une machine virtuelle exécutant Windows 10 dans Microsoft Azure, ***vous devez disposer d’un abonnement Visual Studio*** qui vous permet d’accéder à l’image pour Windows 10 Entreprise. D’autres types d’abonnements Azure, tels que les abonnements d’évaluation et payants, ne permettent pas d’accéder à cette image. Pour obtenir les informations les plus récentes, reportez-vous à l’article [Utilisation d’un client Windows dans Azure pour les scénarios de développement et/ou test](/azure/virtual-machines/windows/client-images).</span><span class="sxs-lookup"><span data-stu-id="19b41-p111">To create a Windows 10 virtual machine in Microsoft Azure, ***you must have a Visual Studio-based subscription***, which has access to the image for Windows 10 Enterprise. Other types of Azure subscriptions, such as trial and paid subscriptions, do not have access to this image. For the latest information, see [Use Windows client in Azure for dev/test scenarios](/azure/virtual-machines/windows/client-images).</span></span>
  
> [!NOTE]
> <span data-ttu-id="19b41-216">[!REMARQUE] Les ensembles de commandes suivants utilisent la dernière version d'Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="19b41-216">The following command sets use the latest version of Azure PowerShell.</span></span> <span data-ttu-id="19b41-217">Reportez-vous à la rubrique relative à la [prise en main des cmdlets Azure PowerShell](/powershell/azureps-cmdlets-docs/).</span><span class="sxs-lookup"><span data-stu-id="19b41-217">See [Get started with Azure PowerShell cmdlets](/powershell/azureps-cmdlets-docs/).</span></span> <span data-ttu-id="19b41-218">Ces ensembles de commandes créent une machine virtuelle Windows 10 Entreprise nommée WIN10 ainsi que l’intégralité de son infrastructure requise, y compris un groupe de ressources, un compte de stockage et un réseau virtuel.</span><span class="sxs-lookup"><span data-stu-id="19b41-218">These command sets build a Windows 10 Enterprise virtual machine named WIN10 and all of its required infrastructure, including a resource group, a storage account, and a virtual network.</span></span> <span data-ttu-id="19b41-219">Si vous êtes déjà familiarisé avec les services d’infrastructure Azure, adaptez ces instructions en fonction de votre infrastructure actuellement déployée.</span><span class="sxs-lookup"><span data-stu-id="19b41-219">If you are already familiar with Azure infrastructure services, adapt these instructions to suit your currently deployed infrastructure.</span></span>
  
<span data-ttu-id="19b41-220">Tout d’abord, lancez une invite Microsoft PowerShell.</span><span class="sxs-lookup"><span data-stu-id="19b41-220">First, start a Microsoft PowerShell prompt.</span></span>
  
<span data-ttu-id="19b41-221">Connectez-vous à votre compte Azure avec cette commande.</span><span class="sxs-lookup"><span data-stu-id="19b41-221">Sign in to your Azure account with this command.</span></span>
  
```powershell
Connect-AzAccount
```

<span data-ttu-id="19b41-222">Obtenez le nom de votre abonnement à l’aide de cette commande.</span><span class="sxs-lookup"><span data-stu-id="19b41-222">Get your subscription name using this  command.</span></span>
  
```powershell
Get-AzSubscription | Sort Name | Select Name
```

<span data-ttu-id="19b41-223">Définissez votre abonnement Azure.</span><span class="sxs-lookup"><span data-stu-id="19b41-223">Set your Azure subscription.</span></span> <span data-ttu-id="19b41-224">Remplacez tout le texte entre guillemets, y compris les \< and > caractères, par le nom correct.</span><span class="sxs-lookup"><span data-stu-id="19b41-224">Replace everything within the quotation marks, including the \< and > characters, with the correct name.</span></span>
  
```powershell
$subscr="<subscription name>"
Get-AzSubscription -SubscriptionName $subscr | Select-AzSubscription
```

<span data-ttu-id="19b41-p114">Ensuite, créez un nouveau groupe de ressources. Pour déterminer un nom de groupe de ressources unique, utilisez cette commande pour répertorier vos groupes de ressources existants.</span><span class="sxs-lookup"><span data-stu-id="19b41-p114">Next, create a new resource group. To determine a unique resource group name, use this command to list your existing resource groups.</span></span>
  
```powershell
Get-AzResourceGroup | Sort ResourceGroupName | Select ResourceGroupName
```

<span data-ttu-id="19b41-227">Créez votre nouveau groupe de ressources avec ces commandes.</span><span class="sxs-lookup"><span data-stu-id="19b41-227">Create your new resource group with these commands.</span></span> <span data-ttu-id="19b41-228">Remplacez tout le texte entre guillemets, y compris les \< and > caractères, par les noms corrects.</span><span class="sxs-lookup"><span data-stu-id="19b41-228">Replace everything within the quotation marks, including the \< and > characters, with the correct names.</span></span>
  
```powershell
$rgName="<resource group name>"
$locName="<location name, such as West US>"
New-AzResourceGroup -Name $rgName -Location $locName
```

<span data-ttu-id="19b41-229">Ensuite, créez un réseau virtuel et la machine virtuelle WIN10 avec ces commandes.</span><span class="sxs-lookup"><span data-stu-id="19b41-229">Next, create a new virtual network and the WIN10 virtual machine with these commands.</span></span> <span data-ttu-id="19b41-230">Lorsque vous y êtes invité, indiquez le nom et le mot de passe du compte d’administrateur local pour WIN10, et enregistrez ces informations dans un emplacement sécurisé.</span><span class="sxs-lookup"><span data-stu-id="19b41-230">When prompted, provide the name and password of the local administrator account for WIN10 and store these in a secure location.</span></span>
  
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

## <a name="phase-5-join-your-windows-10-computer-to-azure-ad"></a><span data-ttu-id="19b41-231">Phase 5 : Association de votre ordinateur Windows 10 à Azure AD</span><span class="sxs-lookup"><span data-stu-id="19b41-231">Phase 5: Join your Windows 10 computer to Azure AD</span></span>

<span data-ttu-id="19b41-232">Lorsque l’ordinateur physique ou la machine virtuelle avec Windows 10 Entreprise est créée, connectez-vous avec un compte d’administrateur local.</span><span class="sxs-lookup"><span data-stu-id="19b41-232">After the physical or virtual machine with Windows 10 Enterprise is created, sign in with a local administrator account.</span></span>
  
> [!NOTE]
> <span data-ttu-id="19b41-233">Pour une machine virtuelle dans Azure, utilisez  [ces instructions](/azure/virtual-machines/windows/connect-logon) pour vous y connecter.</span><span class="sxs-lookup"><span data-stu-id="19b41-233">For a virtual machine in Azure, use  [these instructions](/azure/virtual-machines/windows/connect-logon) to connect to it.</span></span>
  
<span data-ttu-id="19b41-234">Ensuite, associez l’ordinateur WIN10 au client Azure AD de votre abonnement Microsoft 365 E5.</span><span class="sxs-lookup"><span data-stu-id="19b41-234">Next, join the WIN10 computer to the Azure AD tenant of your Microsoft 365 E5 subscription.</span></span>
  
1. <span data-ttu-id="19b41-235">Sur le bureau de l’ordinateur WIN10, sélectionnez Démarrer > Paramètres > Comptes > Accès au travail **ou à l'> Connecter .**</span><span class="sxs-lookup"><span data-stu-id="19b41-235">On the desktop of the WIN10 computer, select **Start > Settings > Accounts > Access work or school > Connect**.</span></span>
    
2. <span data-ttu-id="19b41-236">Dans la **boîte de dialogue Configurer un compte** scolaire ou scolaire, sélectionnez Joindre cet appareil à **Azure Active Directory**.</span><span class="sxs-lookup"><span data-stu-id="19b41-236">In the **Set up a work or school account** dialog box, select **Join this device to Azure Active Directory**.</span></span>
    
3. <span data-ttu-id="19b41-237">Dans **le compte scolaire ou de travail,** entrez le nom du compte d’administrateur général de votre abonnement Microsoft 365 E5, puis sélectionnez **Suivant.**</span><span class="sxs-lookup"><span data-stu-id="19b41-237">In **Work or school account**, enter the global administrator account name of your Microsoft 365 E5 subscription, and then select **Next**.</span></span>
    
4. <span data-ttu-id="19b41-238">Dans **Entrer le mot de** passe, entrez le mot de passe de votre compte d’administrateur général, puis sélectionnez Se **connectez.**</span><span class="sxs-lookup"><span data-stu-id="19b41-238">In **Enter password**, enter the password for your global administrator account, and then select **Sign in**.</span></span>
    
5. <span data-ttu-id="19b41-239">Lorsque vous êtes invité à vous assurer qu’il s’agit de votre organisation, sélectionnez **Rejoindre,** puis **terminé**.</span><span class="sxs-lookup"><span data-stu-id="19b41-239">When prompted to make sure that this is your organization, select **Join**, and then select **Done**.</span></span>
    
6. <span data-ttu-id="19b41-240">Fermez la fenêtre Paramètres.</span><span class="sxs-lookup"><span data-stu-id="19b41-240">Close the settings window.</span></span>
    
<span data-ttu-id="19b41-241">Ensuite, installez Applications Microsoft 365 pour les grandes entreprises sur l’ordinateur WIN10 :</span><span class="sxs-lookup"><span data-stu-id="19b41-241">Next, install Microsoft 365 Apps for enterprise on the WIN10 computer:</span></span>
  
1. <span data-ttu-id="19b41-242">Ouvrez le Microsoft Edge et connectez-vous au Centre [d’administration Microsoft 365](https://admin.microsoft.com) avec vos informations d’identification de compte d’administrateur général.</span><span class="sxs-lookup"><span data-stu-id="19b41-242">Open the Microsoft Edge browser and sign in to the [Microsoft 365 admin center](https://admin.microsoft.com) with your global administrator account credentials.</span></span>
    
2. <span data-ttu-id="19b41-243">Sous **l’Microsoft Office Accueil,** **sélectionnez Installer Office**.</span><span class="sxs-lookup"><span data-stu-id="19b41-243">On the **Microsoft Office Home** tab, select **Install Office**.</span></span>
    
3. <span data-ttu-id="19b41-244">Lorsque vous y avez été invité, sélectionnez **Exécuter,** puis Oui **pour** **le contrôle de compte d’utilisateur.**</span><span class="sxs-lookup"><span data-stu-id="19b41-244">When prompted with what to do, select **Run**, and then select **Yes** for **User Account Control**.</span></span>
    
4. <span data-ttu-id="19b41-245">Attendez qu’Office termine l’installation.</span><span class="sxs-lookup"><span data-stu-id="19b41-245">Wait for Office to complete its installation.</span></span> <span data-ttu-id="19b41-246">Lorsque vous voyez **que tout est prêt !**, sélectionnez Fermer **deux** fois.</span><span class="sxs-lookup"><span data-stu-id="19b41-246">When you see **You're all set!**, select **Close** twice.</span></span>
    
<span data-ttu-id="19b41-247">Votre environnement résultant se ressemble à ceci :</span><span class="sxs-lookup"><span data-stu-id="19b41-247">Your resulting environment looks like this:</span></span>

![Phase 5 de l’environnement de test Microsoft 365 Entreprise](../media/lightweight-base-configuration-microsoft-365-enterprise/Phase4.png)

<span data-ttu-id="19b41-249">Cela inclut l’ordinateur WIN10 avec :</span><span class="sxs-lookup"><span data-stu-id="19b41-249">This includes the WIN10 computer that has:</span></span>

- <span data-ttu-id="19b41-250">rejoint le client Azure AD de votre abonnement Microsoft 365 E5 ;</span><span class="sxs-lookup"><span data-stu-id="19b41-250">Joined the Azure AD tenant of your Microsoft 365 E5 subscription.</span></span>
- <span data-ttu-id="19b41-251">été inscrit en tant que périphérique Azure AD dans Microsoft Intune (EMS) ;</span><span class="sxs-lookup"><span data-stu-id="19b41-251">Enrolled as an Azure AD device in Microsoft Intune (EMS).</span></span>
- <span data-ttu-id="19b41-252">Applications Microsoft 365 pour les grandes entreprises installé.</span><span class="sxs-lookup"><span data-stu-id="19b41-252">Microsoft 365 Apps for enterprise installed.</span></span>
  
<span data-ttu-id="19b41-253">Vous êtes maintenant prêt à tester des fonctionnalités supplémentaires de [Microsoft 365 entreprise.](https://www.microsoft.com/microsoft-365/enterprise)</span><span class="sxs-lookup"><span data-stu-id="19b41-253">You are now ready to experiment with additional features of [Microsoft 365 for enterprise](https://www.microsoft.com/microsoft-365/enterprise).</span></span>
  
## <a name="next-steps"></a><span data-ttu-id="19b41-254">Étapes suivantes</span><span class="sxs-lookup"><span data-stu-id="19b41-254">Next steps</span></span>

<span data-ttu-id="19b41-255">Découvrez les nouveaux ensembles de guides pour les tests de laboratoire :</span><span class="sxs-lookup"><span data-stu-id="19b41-255">Explore these additional sets of Test Lab Guides:</span></span>
  
- [<span data-ttu-id="19b41-256">Identité</span><span class="sxs-lookup"><span data-stu-id="19b41-256">Identity</span></span>](m365-enterprise-test-lab-guides.md#identity)
- [<span data-ttu-id="19b41-257">Gestion des appareils mobiles</span><span class="sxs-lookup"><span data-stu-id="19b41-257">Mobile device management</span></span>](m365-enterprise-test-lab-guides.md#mobile-device-management)
- [<span data-ttu-id="19b41-258">Protection des informations</span><span class="sxs-lookup"><span data-stu-id="19b41-258">Information protection</span></span>](m365-enterprise-test-lab-guides.md#information-protection)
   

## <a name="see-also"></a><span data-ttu-id="19b41-259">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="19b41-259">See also</span></span>

[<span data-ttu-id="19b41-260">Microsoft 365 pour les entreprises Guides de laboratoire d'essai</span><span class="sxs-lookup"><span data-stu-id="19b41-260">Microsoft 365 for enterprise Test Lab Guides</span></span>](m365-enterprise-test-lab-guides.md)

[<span data-ttu-id="19b41-261">Vue d’ensemble de Microsoft 365 pour entreprise</span><span class="sxs-lookup"><span data-stu-id="19b41-261">Microsoft 365 for enterprise overview</span></span>](microsoft-365-overview.md)

[<span data-ttu-id="19b41-262">Documentation Microsoft 365 Entreprise</span><span class="sxs-lookup"><span data-stu-id="19b41-262">Microsoft 365 for enterprise documentation</span></span>](/microsoft-365-enterprise/)