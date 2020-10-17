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
ms.openlocfilehash: 2b8505e142c3c1b87578db7342ed299b95d8c049
ms.sourcegitcommit: 53ff1fe6d6143b0bf011031eea9b85dc01ae4f74
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/16/2020
ms.locfileid: "48487387"
---
# <a name="the-lightweight-base-configuration"></a><span data-ttu-id="ddd88-103">Configuration de base légère</span><span class="sxs-lookup"><span data-stu-id="ddd88-103">The lightweight base configuration</span></span>

<span data-ttu-id="ddd88-104">*Ce guide de laboratoire de test peut être utilisé pour les environnements de test Microsoft 365 pour les environnements de test d’entreprise et Office 365.*</span><span class="sxs-lookup"><span data-stu-id="ddd88-104">*This Test Lab Guide can be used for both Microsoft 365 for enterprise and Office 365 Enterprise test environments.*</span></span>

<span data-ttu-id="ddd88-105">Cet article explique comment créer un environnement simplifié avec un abonnement Microsoft 365 E5 et un ordinateur exécutant Windows 10 entreprise.</span><span class="sxs-lookup"><span data-stu-id="ddd88-105">This article describes how to create a simplified environment with a Microsoft 365 E5 subscription and a computer running Windows 10 Enterprise.</span></span>

![Environnement de test Microsoft 365 Entreprise léger](../media/lightweight-base-configuration-microsoft-365-enterprise/Phase4.png)

<span data-ttu-id="ddd88-107">La création d’un environnement de test léger implique cinq phases :</span><span class="sxs-lookup"><span data-stu-id="ddd88-107">Creating a lightweight test environment involves five phases:</span></span>
- [<span data-ttu-id="ddd88-108">Phase 1 : création de votre abonnement Microsoft 365 E5</span><span class="sxs-lookup"><span data-stu-id="ddd88-108">Phase 1: Create your Microsoft 365 E5 subscription</span></span>](#phase-1-create-your-microsoft-365-e5-subscription)
- [<span data-ttu-id="ddd88-109">Phase 2 : configuration de votre abonnement d’évaluation Office 365</span><span class="sxs-lookup"><span data-stu-id="ddd88-109">Phase 2: Configure your Office 365 trial subscription</span></span>](#phase-2-configure-your-office-365-trial-subscription)
- [<span data-ttu-id="ddd88-110">Phase 3 : Ajoutez un abonnement d’évaluation Microsoft 365 E5.</span><span class="sxs-lookup"><span data-stu-id="ddd88-110">Phase 3: Add a Microsoft 365 E5 trial subscription</span></span>](#phase-3-add-a-microsoft-365-e5-trial-subscription)
- [<span data-ttu-id="ddd88-111">Phase 4 : Création d’un ordinateur Windows 10 Entreprise</span><span class="sxs-lookup"><span data-stu-id="ddd88-111">Phase 4: Create a Windows 10 Enterprise computer</span></span>](#phase-4-create-a-windows-10-enterprise-computer)
- [<span data-ttu-id="ddd88-112">Phase 5 : Association de votre ordinateur Windows 10 à Azure AD</span><span class="sxs-lookup"><span data-stu-id="ddd88-112">Phase 5: Join your Windows 10 computer to Azure AD</span></span>](#phase-5-join-your-windows-10-computer-to-azure-ad)

<span data-ttu-id="ddd88-113">Utilisez l’environnement résultant pour tester les fonctionnalités de [Microsoft 365 pour les entreprises](https://www.microsoft.com/microsoft-365/enterprise).</span><span class="sxs-lookup"><span data-stu-id="ddd88-113">Use the resulting environment to test the features and functionality of [Microsoft 365 for enterprise](https://www.microsoft.com/microsoft-365/enterprise).</span></span>

![Guides de laboratoire de test pour Microsoft Cloud](../media/m365-enterprise-test-lab-guides/cloud-tlg-icon.png)
  
> [!TIP]
> <span data-ttu-id="ddd88-115">Pour obtenir un plan de tous les Articles de la pile de guide de laboratoire de test Microsoft 365 pour Enterprise, voir [Microsoft 365 pour la pile de guide de laboratoire de test d’entreprise](../downloads/Microsoft365EnterpriseTLGStack.pdf).</span><span class="sxs-lookup"><span data-stu-id="ddd88-115">For a visual map to all the articles in the Microsoft 365 for enterprise Test Lab Guide stack, see [Microsoft 365 for enterprise Test Lab Guide Stack](../downloads/Microsoft365EnterpriseTLGStack.pdf).</span></span>

>[!NOTE]
><span data-ttu-id="ddd88-116">Nous vous recommandons d’imprimer cet article afin de consigner les informations dont vous aurez besoin dans cet environnement au cours des 30 jours de votre abonnement à la version d’évaluation Office 365.</span><span class="sxs-lookup"><span data-stu-id="ddd88-116">You might want to print this article to record the specific information that you will need for this environment over the 30 days of the Office 365 trial subscription.</span></span> <span data-ttu-id="ddd88-117">Vous pouvez facilement étendre l’abonnement d’évaluation pour une période supplémentaire de 30 jours.</span><span class="sxs-lookup"><span data-stu-id="ddd88-117">You can easily extend the trail subscription for another 30 days.</span></span> <span data-ttu-id="ddd88-118">Pour un environnement de développement/test permanent, créez un nouvel abonnement payant avec un client Azure AD séparé et un nombre réduit de licences.</span><span class="sxs-lookup"><span data-stu-id="ddd88-118">For a permanent test environment, create a new paid subscription with a separate Azure AD tenant and a small number of licenses.</span></span>

## <a name="phase-1-create-your-microsoft-365-e5-subscription"></a><span data-ttu-id="ddd88-119">Phase 1 : création de votre abonnement Microsoft 365 E5</span><span class="sxs-lookup"><span data-stu-id="ddd88-119">Phase 1: Create your Microsoft 365 E5 subscription</span></span>

<span data-ttu-id="ddd88-120">Nous commençons par un abonnement à la version d’évaluation de Microsoft 365 E5, puis nous ajoutons l’abonnement Microsoft 365 E5.</span><span class="sxs-lookup"><span data-stu-id="ddd88-120">We start with an Microsoft 365 E5 trial subscription and then add the Microsoft 365 E5 subscription to it.</span></span>

>[!NOTE]
><span data-ttu-id="ddd88-121">Nous vous recommandons de créer un abonnement à la version d’évaluation d’Office 365 afin que votre environnement de test dispose d’un client Azure AD distinct de tous les abonnements payants dont vous disposez actuellement.</span><span class="sxs-lookup"><span data-stu-id="ddd88-121">We recommend that you create a trial subscription of Office 365 so that your test environment has a separate Azure AD tenant from any paid subscriptions you currently have.</span></span> <span data-ttu-id="ddd88-122">Cette séparation signifie que vous pouvez ajouter et supprimer des utilisateurs et des groupes dans le client de test sans affecter vos abonnements de production.</span><span class="sxs-lookup"><span data-stu-id="ddd88-122">This separation means that you can add and remove users and groups in the test tenant without affecting your production subscriptions.</span></span>

<span data-ttu-id="ddd88-123">Pour démarrer votre abonnement d’évaluation Microsoft 365 E5, vous avez besoin d’un nom d’entreprise fictif et d’un nouveau compte Microsoft.</span><span class="sxs-lookup"><span data-stu-id="ddd88-123">To start your Microsoft 365 E5 trial subscription, you first need a fictitious company name and a new Microsoft account.</span></span>
  
1. <span data-ttu-id="ddd88-p103">Nous vous recommandons d’utiliser une variante du nom d’entreprise Contoso pour le nom de votre entreprise. Il s’agit d’une entreprise fictive utilisée dans le contenu d’exemple de Microsoft. Toutefois, cette étape n’est pas obligatoire. Indiquer le nom fictif de votre entreprise ici :</span><span class="sxs-lookup"><span data-stu-id="ddd88-p103">We recommend that you use a variant of the company name Contoso for your company name, which is a fictitious company used in Microsoft sample content, but it isn't required. Record your fictitious company name here:</span></span> ![Trait](../media/Common-Images/TableLine.png)
    
2. <span data-ttu-id="ddd88-p104">Pour ouvrir un nouveau compte Microsoft, accédez à [https://outlook.com](https://outlook.com) et créez un compte avec un nouveau compte de messagerie et une nouvelle adresse. Vous utiliserez ce compte pour vous inscrire à Office 365.</span><span class="sxs-lookup"><span data-stu-id="ddd88-p104">To sign up for a new Microsoft account, go to [https://outlook.com](https://outlook.com) and create an account with a new email account and address. You will use this account to sign up for Office 365.</span></span>
    
    - <span data-ttu-id="ddd88-129">Enregistrez le prénom et le nom de famille utilisés pour votre nouveau compte ici :</span><span class="sxs-lookup"><span data-stu-id="ddd88-129">Record the first and last name of your new account here:</span></span> ![Trait](../media/Common-Images/TableLine.png)
    
    - <span data-ttu-id="ddd88-131">Enregistrez l’adresse du nouveau compte de messagerie ici :</span><span class="sxs-lookup"><span data-stu-id="ddd88-131">Record the new email account address here:</span></span> ![Trait](../media/Common-Images/TableLine.png)<span data-ttu-id="ddd88-133">@outlook.com</span><span class="sxs-lookup"><span data-stu-id="ddd88-133">@outlook.com</span></span>
    
### <a name="sign-up-for-an-office-365-e5-trial-subscription"></a><span data-ttu-id="ddd88-134">Inscription à un abonnement d’évaluation Office 365 E5</span><span class="sxs-lookup"><span data-stu-id="ddd88-134">Sign up for an Office 365 E5 trial subscription</span></span>

1. <span data-ttu-id="ddd88-135">Dans votre navigateur, accédez à [https://aka.ms/e5trial](https://aka.ms/e5trial) .</span><span class="sxs-lookup"><span data-stu-id="ddd88-135">In your browser, go to [https://aka.ms/e5trial](https://aka.ms/e5trial).</span></span>
    
2. <span data-ttu-id="ddd88-136">À l’étape 1 de la page **Merci de choisir Office 365 E5** , entrez votre nouvelle adresse de compte de messagerie.</span><span class="sxs-lookup"><span data-stu-id="ddd88-136">In step 1 of the **Thank you for choosing Office 365 E5** page, enter your new email account address.</span></span>
3. <span data-ttu-id="ddd88-137">À l’étape 2 du processus d’abonnement Trail, entrez les informations demandées, puis effectuez la vérification.</span><span class="sxs-lookup"><span data-stu-id="ddd88-137">In step 2 of the trail subscription process, enter the requested information, and then perform the verification.</span></span>
4. <span data-ttu-id="ddd88-138">À l’étape 3, entrez un nom d’organisation, puis un nom de compte qui sera l’administrateur général de l’abonnement.</span><span class="sxs-lookup"><span data-stu-id="ddd88-138">In step 3, enter an organization name and then an account name that will be the global admin for the subscription.</span></span>
5. <span data-ttu-id="ddd88-139">À l’étape 4, enregistrer l’URL de la page de connexion ici (sélectionnez-la et copiez-la) :</span><span class="sxs-lookup"><span data-stu-id="ddd88-139">For step 4, record the sign-in page here (select and copy):</span></span> ![Trait](../media/Common-Images/TableLine.png)
6. <span data-ttu-id="ddd88-141">Enregistrez l’identifiant utilisateur ici : ![ligne](../media/Common-Images/TableLine.png).onmicrosoft.com</span><span class="sxs-lookup"><span data-stu-id="ddd88-141">Record the user ID here: ![Line](../media/Common-Images/TableLine.png).onmicrosoft.com</span></span>  
   <span data-ttu-id="ddd88-142">Enregistrez le mot de passe que vous avez saisi dans un emplacement sécurisé.</span><span class="sxs-lookup"><span data-stu-id="ddd88-142">Record the password that you entered in a secure location.</span></span>
   <span data-ttu-id="ddd88-143">Cette valeur correspond au **nom de l’administrateur général**.</span><span class="sxs-lookup"><span data-stu-id="ddd88-143">This value will be referred to as the **global administrator name**.</span></span>
7. <span data-ttu-id="ddd88-144">Sélectionnez **atteindre le programme d’installation**.</span><span class="sxs-lookup"><span data-stu-id="ddd88-144">Select **Go to Setup**.</span></span>
8. <span data-ttu-id="ddd88-145">Dans le programme d’installation d’Office 365 E5, sélectionnez **continuer à l’aide de *votre organisation*. onmicrosoft.com pour la messagerie et la connexion**, puis sélectionnez **quitter et continuer ultérieurement**.</span><span class="sxs-lookup"><span data-stu-id="ddd88-145">In Office 365 E5 Setup, select **Continue using *your organization*.onmicrosoft.com for email and signing in**, and then select **Exit and continue later**.</span></span>

<span data-ttu-id="ddd88-146">Le Centre d’administration Microsoft 365 doit s’afficher.</span><span class="sxs-lookup"><span data-stu-id="ddd88-146">You should see the Microsoft 365 admin center.</span></span>
    
## <a name="phase-2-configure-your-office-365-trial-subscription"></a><span data-ttu-id="ddd88-147">Phase 2 : configuration de votre abonnement d’évaluation Office 365</span><span class="sxs-lookup"><span data-stu-id="ddd88-147">Phase 2: Configure your Office 365 trial subscription</span></span>

<span data-ttu-id="ddd88-148">Durant cette phase, configurez votre abonnement en y ajoutant des utilisateurs supplémentaires et assignez-leur des licences Office 365 E5.</span><span class="sxs-lookup"><span data-stu-id="ddd88-148">In this phase, you configure your subscription with additional users and assign them Office 365 E5 licenses.</span></span>
  
<span data-ttu-id="ddd88-149">Pour vous connecter à votre abonnement avec le module Azure Active Directory PowerShell pour Graph de votre ordinateur, suivez les instructions fournies dans [se connecter à Microsoft 365 avec PowerShell](connect-to-microsoft-365-powershell.md#connect-with-the-azure-active-directory-powershell-for-graph-module).</span><span class="sxs-lookup"><span data-stu-id="ddd88-149">To connect to your subscription with the Azure Active Directory PowerShell for Graph module from your computer, use the instructions in [Connect to Microsoft 365 with PowerShell](connect-to-microsoft-365-powershell.md#connect-with-the-azure-active-directory-powershell-for-graph-module).</span></span>
    
<span data-ttu-id="ddd88-150">Dans la boîte de dialogue **demande d’informations d’identification Windows PowerShell** , entrez le nom de l’administrateur général (par exemple, *jdoe@contosotoycompany.onmicrosoft.com*) et le mot de passe.</span><span class="sxs-lookup"><span data-stu-id="ddd88-150">In the **Windows PowerShell Credential Request** dialog box, enter the global administrator name (for example, *jdoe@contosotoycompany.onmicrosoft.com*) and password.</span></span>
  
<span data-ttu-id="ddd88-151">Renseignez le nom de votre organisation (par exemple, *contosotoycompany*), le code pays à deux lettres de votre emplacement, un mot de passe de compte courant, puis exécutez les commandes suivantes à partir de l’invite PowerShell :</span><span class="sxs-lookup"><span data-stu-id="ddd88-151">Fill in your organization name (for example, *contosotoycompany*), the two-character country code for your location, a common account password, and then run the following commands from the PowerShell prompt:</span></span>

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
> <span data-ttu-id="ddd88-152">L’utilisation ici d’un mot de passe courant est destinée à l’automatisation et à la simplification de la configuration pour un environnement de test.</span><span class="sxs-lookup"><span data-stu-id="ddd88-152">The use of a common password here is for automation and ease of configuration for a test environment.</span></span> <span data-ttu-id="ddd88-153">Bien évidemment, cela est hautement déconseillé pour les abonnements de production.</span><span class="sxs-lookup"><span data-stu-id="ddd88-153">Obviously, this is highly discouraged for production subscriptions.</span></span> 

### <a name="record-key-information-for-future-reference"></a><span data-ttu-id="ddd88-154">Enregistrer les informations clés pour future référence</span><span class="sxs-lookup"><span data-stu-id="ddd88-154">Record key information for future reference</span></span>

<span data-ttu-id="ddd88-155">Si vous n’avez pas encore enregistré ces valeurs, enregistrez-les maintenant :</span><span class="sxs-lookup"><span data-stu-id="ddd88-155">If you haven't already recorded these values, record them now:</span></span>
  
- <span data-ttu-id="ddd88-156">Nom de l’administrateur général :</span><span class="sxs-lookup"><span data-stu-id="ddd88-156">Global administrator name:</span></span> ![Trait](../media/Common-Images/TableLine.png)<span data-ttu-id="ddd88-158">.onmicrosoft.com(à partir de l’étape 6 de la phase 1)</span><span class="sxs-lookup"><span data-stu-id="ddd88-158">.onmicrosoft.com (from step 6 of Phase 1)</span></span>
    
    <span data-ttu-id="ddd88-159">Enregistrez également le mot de passe de ce compte dans un emplacement sécurisé.</span><span class="sxs-lookup"><span data-stu-id="ddd88-159">Also record the password for this account in a secure location.</span></span>
    
- <span data-ttu-id="ddd88-160">Nom de l’organisation bénéficiant de l’abonnement à la version d’évaluation :</span><span class="sxs-lookup"><span data-stu-id="ddd88-160">Your trial subscription organization name:</span></span> ![Trait](../media/Common-Images/TableLine.png) <span data-ttu-id="ddd88-162">(à partir de l’étape 4 de la phase 1)</span><span class="sxs-lookup"><span data-stu-id="ddd88-162">(from step 4 of Phase 1)</span></span>
    
- <span data-ttu-id="ddd88-163">Pour répertorier les comptes pour Utilisateur 2, Utilisateur 3, Utilisateur 4 et Utilisateur 5, exécutez la commande suivante à partir de l’invite Module Windows Azure Active Directory pour Windows PowerShell :</span><span class="sxs-lookup"><span data-stu-id="ddd88-163">To list the accounts for User 2, User 3, User 4, and User 5, run the following command from the Windows Azure Active Directory Module for Windows PowerShell prompt:</span></span>
    
  ```powershell
  Get-AzureADUser | Sort UserPrincipalName | Select UserPrincipalName
  ```

    <span data-ttu-id="ddd88-164">Enregistrez les noms de compte ici :</span><span class="sxs-lookup"><span data-stu-id="ddd88-164">Record the account names here:</span></span>
    
  - <span data-ttu-id="ddd88-165">Nom du compte de l’utilisateur 2 : utilisateur2@</span><span class="sxs-lookup"><span data-stu-id="ddd88-165">User 2 account name: user2@</span></span>![Trait](../media/Common-Images/TableLine.png)<span data-ttu-id="ddd88-167">.onmicrosoft.com</span><span class="sxs-lookup"><span data-stu-id="ddd88-167">.onmicrosoft.com</span></span>
    
  - <span data-ttu-id="ddd88-168">Nom du compte de l’utilisateur 3 : utilisateur3@</span><span class="sxs-lookup"><span data-stu-id="ddd88-168">User 3 account name: user3@</span></span>![Trait](../media/Common-Images/TableLine.png)<span data-ttu-id="ddd88-170">.onmicrosoft.com</span><span class="sxs-lookup"><span data-stu-id="ddd88-170">.onmicrosoft.com</span></span>
    
  - <span data-ttu-id="ddd88-171">Nom du compte de l’utilisateur 4 : utilisateur4@</span><span class="sxs-lookup"><span data-stu-id="ddd88-171">User 4 account name: user4@</span></span>![Trait](../media/Common-Images/TableLine.png)<span data-ttu-id="ddd88-173">.onmicrosoft.com</span><span class="sxs-lookup"><span data-stu-id="ddd88-173">.onmicrosoft.com</span></span>
    
  - <span data-ttu-id="ddd88-174">Nom du compte de l’utilisateur 5 : utilisateur5@</span><span class="sxs-lookup"><span data-stu-id="ddd88-174">User 5 account name: user5@</span></span>![Trait](../media/Common-Images/TableLine.png)<span data-ttu-id="ddd88-176">.onmicrosoft.com</span><span class="sxs-lookup"><span data-stu-id="ddd88-176">.onmicrosoft.com</span></span>
    
    <span data-ttu-id="ddd88-177">Enregistrez également les mots de passe communs de ces comptes dans un emplacement sécurisé.</span><span class="sxs-lookup"><span data-stu-id="ddd88-177">Also record the common password for these accounts in a secure location.</span></span>
   
### <a name="using-an-office-365-test-environment"></a><span data-ttu-id="ddd88-178">Utilisation d’un environnement de test Office 365</span><span class="sxs-lookup"><span data-stu-id="ddd88-178">Using an Office 365 test environment</span></span>

<span data-ttu-id="ddd88-179">Si vous n’avez besoin que d’un environnement de test Office 365, vous n’avez pas besoin de lire le reste de cet article.</span><span class="sxs-lookup"><span data-stu-id="ddd88-179">If you need only an Office 365 test environment, you do not need to read the rest of this article.</span></span>

<span data-ttu-id="ddd88-180">Pour obtenir des guides de laboratoire de test supplémentaires qui s’appliquent à Office 365 et Microsoft 365, consultez la rubrique [Microsoft 365 pour les guides de laboratoire de test d’entreprise](m365-enterprise-test-lab-guides.md).</span><span class="sxs-lookup"><span data-stu-id="ddd88-180">For additional Test Lab Guides that apply to both Office 365 and Microsoft 365, see [Microsoft 365 for enterprise Test Lab Guides](m365-enterprise-test-lab-guides.md).</span></span>
  
## <a name="phase-3-add-a-microsoft-365-e5-trial-subscription"></a><span data-ttu-id="ddd88-181">Phase 3 : Ajoutez un abonnement d’évaluation Microsoft 365 E5.</span><span class="sxs-lookup"><span data-stu-id="ddd88-181">Phase 3: Add a Microsoft 365 E5 trial subscription</span></span>

<span data-ttu-id="ddd88-182">Dans cette phase, vous vous inscrivez pour l’abonnement d’évaluation Microsoft 365 E5 et l’ajoutez à la même organisation que votre abonnement d’évaluation d’Office 365 E5.</span><span class="sxs-lookup"><span data-stu-id="ddd88-182">In this phase, you sign up for the Microsoft 365 E5 trial subscription and add it to the same organization as your Office 365 E5 trial subscription.</span></span>
  
<span data-ttu-id="ddd88-183">Tout d’abord, ajoutez l’abonnement d’évaluation Microsoft 365 E5 et attribuez une licence Microsoft 365 à votre compte d’administrateur général.</span><span class="sxs-lookup"><span data-stu-id="ddd88-183">First, add the Microsoft 365 E5 trial subscription and assign the new Microsoft 365 license to your global administrator account.</span></span>
  
1. <span data-ttu-id="ddd88-184">Dans une fenêtre privée de navigateur Internet, utilisez les informations d’identification de votre compte d’administrateur général pour vous connecter au centre d’administration Microsoft 365 à l’adresse [https://admin.microsoft.com](https://admin.microsoft.com) .</span><span class="sxs-lookup"><span data-stu-id="ddd88-184">In an internet browser private window, use your global administrator account credentials to sign in to the Microsoft 365 admin center at [https://admin.microsoft.com](https://admin.microsoft.com).</span></span>
    
2. <span data-ttu-id="ddd88-185">Sur la page **Centre d’administration 365 de Microsoft** , dans le volet de navigation de gauche, sélectionnez **facturation > achat de services**.</span><span class="sxs-lookup"><span data-stu-id="ddd88-185">On the **Microsoft 365 admin center** page, in the left navigation, select **Billing > Purchase services**.</span></span>
    
3. <span data-ttu-id="ddd88-186">Sur la page **acheter des services** , sélectionnez **Microsoft 365 E5**, puis sélectionnez **obtenir une version d’évaluation gratuite**.</span><span class="sxs-lookup"><span data-stu-id="ddd88-186">On the **Purchase services** page, select **Microsoft 365 E5**, and then select **Get free trial**.</span></span>

4. <span data-ttu-id="ddd88-187">Sur la page **d’évaluation de Microsoft 365 E5** , vous décidez de recevoir un message texte ou un appel téléphonique, d’entrer votre numéro de téléphone, puis de sélectionner **me texte** ou **m’appeler**.</span><span class="sxs-lookup"><span data-stu-id="ddd88-187">On the **Microsoft 365 E5 Trial** page, decide to receive a text message or a phone call, enter your phone number, and then select **Text me** or **Call me**.</span></span> <span data-ttu-id="ddd88-188">Effectuez la vérification.</span><span class="sxs-lookup"><span data-stu-id="ddd88-188">Perform the verification.</span></span>

5. <span data-ttu-id="ddd88-189">Sur la page **confirmer votre commande** , sélectionnez **essayer maintenant**.</span><span class="sxs-lookup"><span data-stu-id="ddd88-189">On the **Confirm your order** page, select **Try now**.</span></span>

6. <span data-ttu-id="ddd88-190">Sur la page **bon de commande** , sélectionnez **Continuer**.</span><span class="sxs-lookup"><span data-stu-id="ddd88-190">On the **Order receipt** page, select **Continue**.</span></span>

7. <span data-ttu-id="ddd88-191">Dans le centre d’administration 365 de Microsoft, sélectionnez **utilisateurs > utilisateurs actifs**.</span><span class="sxs-lookup"><span data-stu-id="ddd88-191">In the Microsoft 365 admin center, select **Users > Active users**.</span></span>

8. <span data-ttu-id="ddd88-192">Dans **utilisateurs actifs**, sélectionnez votre compte d’administrateur.</span><span class="sxs-lookup"><span data-stu-id="ddd88-192">In **Active users**, select your administrator account.</span></span>

9. <span data-ttu-id="ddd88-193">Sélectionnez **licences et applications**.</span><span class="sxs-lookup"><span data-stu-id="ddd88-193">Select **Licenses and apps**.</span></span>

10. <span data-ttu-id="ddd88-194">Désactivez la licence pour Office 365 Entreprise E5 et activez la licence pour Microsoft 365 E5.</span><span class="sxs-lookup"><span data-stu-id="ddd88-194">Disable the license for Office 365 Enterprise E5 and enable the license for Microsoft 365 E5.</span></span>

11. <span data-ttu-id="ddd88-195">Sélectionnez **enregistrer les modifications**, puis fermez le volet informations sur le compte d’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="ddd88-195">Select **Save changes**, and then close the user account information pane.</span></span>

<span data-ttu-id="ddd88-196">Ensuite, répétez les étapes 8 et 11 de la procédure précédente pour tous vos autres comptes (Utilisateur2, Utilisateur3, Utilisateur4 et Utilisateur5).</span><span class="sxs-lookup"><span data-stu-id="ddd88-196">Next, repeat steps 8 through 11 of the previous procedure for all of your other accounts (User 2, User 3, User 4, and User 5).</span></span>
  
> [!NOTE]
> <span data-ttu-id="ddd88-197">La durée de l’abonnement à la version d’évaluation de Microsoft 365 E5 est de 30 jours.</span><span class="sxs-lookup"><span data-stu-id="ddd88-197">The length of the Microsoft 365 E5 trial subscription is 30 days.</span></span> <span data-ttu-id="ddd88-198">Pour un environnement de test permanent, convertissez cet abonnement en abonnement payant avec un nombre réduit de licences.</span><span class="sxs-lookup"><span data-stu-id="ddd88-198">For a permanent test environment, convert this trial subscription into a paid subscription with a small number of licenses.</span></span>
  
<span data-ttu-id="ddd88-199">Votre environnement de test comporte maintenant :</span><span class="sxs-lookup"><span data-stu-id="ddd88-199">Your test environment now has:</span></span>
  
- <span data-ttu-id="ddd88-200">Un abonnement d’évaluation de Microsoft 365 E5.</span><span class="sxs-lookup"><span data-stu-id="ddd88-200">A Microsoft 365 E5 trial subscription.</span></span>
- <span data-ttu-id="ddd88-201">Tous vos comptes d’utilisateur appropriés (l’administrateur général ou tous les cinq comptes d’utilisateur) sont activés pour utiliser Microsoft 365 E5.</span><span class="sxs-lookup"><span data-stu-id="ddd88-201">All your appropriate user accounts (either just the global administrator or all five user accounts) are enabled to use Microsoft 365 E5.</span></span>
    
<span data-ttu-id="ddd88-202">La configuration obtenue, qui ajoute Microsoft 365 E5, se présente comme suit :</span><span class="sxs-lookup"><span data-stu-id="ddd88-202">Your resulting configuration, which adds Microsoft 365 E5, looks like this:</span></span>
  
![Phase 3 de l’environnement de test Microsoft 365 Entreprise](../media/lightweight-base-configuration-microsoft-365-enterprise/Phase2.png)
  
## <a name="phase-4-create-a-windows-10-enterprise-computer"></a><span data-ttu-id="ddd88-204">Phase 4 : Création d’un ordinateur Windows 10 Entreprise</span><span class="sxs-lookup"><span data-stu-id="ddd88-204">Phase 4: Create a Windows 10 Enterprise computer</span></span>

<span data-ttu-id="ddd88-205">Au cours de cette phase, vous allez créer un ordinateur autonome exécutant Windows 10 Entreprise sous forme d’un ordinateur physique, d’une machine virtuelle ou d’une machine virtuelle Azure.</span><span class="sxs-lookup"><span data-stu-id="ddd88-205">In this phase, you create a standalone computer running Windows 10 Enterprise as either a physical computer, a virtual machine, or an Azure virtual machine.</span></span>
  
### <a name="physical-computer"></a><span data-ttu-id="ddd88-206">Ordinateur physique</span><span class="sxs-lookup"><span data-stu-id="ddd88-206">Physical computer</span></span>

<span data-ttu-id="ddd88-207">Sur un ordinateur personnel, installez Windows 10 entreprise.</span><span class="sxs-lookup"><span data-stu-id="ddd88-207">On a personal computer, install Windows 10 Enterprise.</span></span> <span data-ttu-id="ddd88-208">Vous pouvez télécharger la version d’évaluation de Windows 10 entreprise [ici](https://www.microsoft.com/evalcenter/evaluate-windows-10-enterprise).</span><span class="sxs-lookup"><span data-stu-id="ddd88-208">You can download the Windows 10 Enterprise trial [here](https://www.microsoft.com/evalcenter/evaluate-windows-10-enterprise).</span></span>
  
### <a name="virtual-machine"></a><span data-ttu-id="ddd88-209">Machine virtuelle</span><span class="sxs-lookup"><span data-stu-id="ddd88-209">Virtual machine</span></span>

<span data-ttu-id="ddd88-210">Utilisez l’hyperviseur de votre choix pour créer une machine virtuelle, puis installez Windows 10 entreprise sur celle-ci.</span><span class="sxs-lookup"><span data-stu-id="ddd88-210">Use the hypervisor of your choice to create a virtual machine, and then install Windows 10 Enterprise on it.</span></span> <span data-ttu-id="ddd88-211">Vous pouvez télécharger la version d’évaluation de Windows 10 entreprise [ici](https://www.microsoft.com/evalcenter/evaluate-windows-10-enterprise).</span><span class="sxs-lookup"><span data-stu-id="ddd88-211">You can download the Windows 10 Enterprise trial [here](https://www.microsoft.com/evalcenter/evaluate-windows-10-enterprise).</span></span>
  
### <a name="virtual-machine-in-azure"></a><span data-ttu-id="ddd88-212">Machine virtuelle dans Azure</span><span class="sxs-lookup"><span data-stu-id="ddd88-212">Virtual machine in Azure</span></span>

<span data-ttu-id="ddd88-p111">Pour créer une machine virtuelle exécutant Windows 10 dans Microsoft Azure, ***vous devez disposer d’un abonnement Visual Studio*** qui vous permet d’accéder à l’image pour Windows 10 Entreprise. D’autres types d’abonnements Azure, tels que les abonnements d’évaluation et payants, ne permettent pas d’accéder à cette image. Pour obtenir les informations les plus récentes, reportez-vous à l’article [Utilisation d’un client Windows dans Azure pour les scénarios de développement et/ou test](https://docs.microsoft.com/azure/virtual-machines/windows/client-images).</span><span class="sxs-lookup"><span data-stu-id="ddd88-p111">To create a Windows 10 virtual machine in Microsoft Azure, ***you must have a Visual Studio-based subscription***, which has access to the image for Windows 10 Enterprise. Other types of Azure subscriptions, such as trial and paid subscriptions, do not have access to this image. For the latest information, see [Use Windows client in Azure for dev/test scenarios](https://docs.microsoft.com/azure/virtual-machines/windows/client-images).</span></span>
  
> [!NOTE]
> <span data-ttu-id="ddd88-216">[!REMARQUE] Les ensembles de commandes suivants utilisent la dernière version d'Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="ddd88-216">The following command sets use the latest version of Azure PowerShell.</span></span> <span data-ttu-id="ddd88-217">Reportez-vous à la rubrique relative à la [prise en main des cmdlets Azure PowerShell](https://docs.microsoft.com/powershell/azureps-cmdlets-docs/).</span><span class="sxs-lookup"><span data-stu-id="ddd88-217">See [Get started with Azure PowerShell cmdlets](https://docs.microsoft.com/powershell/azureps-cmdlets-docs/).</span></span> <span data-ttu-id="ddd88-218">Ces ensembles de commandes créent une machine virtuelle Windows 10 Entreprise nommée WIN10 ainsi que l’intégralité de son infrastructure requise, y compris un groupe de ressources, un compte de stockage et un réseau virtuel.</span><span class="sxs-lookup"><span data-stu-id="ddd88-218">These command sets build a Windows 10 Enterprise virtual machine named WIN10 and all of its required infrastructure, including a resource group, a storage account, and a virtual network.</span></span> <span data-ttu-id="ddd88-219">Si vous êtes déjà familiarisé avec les services d’infrastructure Azure, adaptez ces instructions en fonction de votre infrastructure actuellement déployée.</span><span class="sxs-lookup"><span data-stu-id="ddd88-219">If you are already familiar with Azure infrastructure services, adapt these instructions to suit your currently deployed infrastructure.</span></span>
  
<span data-ttu-id="ddd88-220">Tout d’abord, lancez une invite Microsoft PowerShell.</span><span class="sxs-lookup"><span data-stu-id="ddd88-220">First, start a Microsoft PowerShell prompt.</span></span>
  
<span data-ttu-id="ddd88-221">Connectez-vous à votre compte Azure avec cette commande.</span><span class="sxs-lookup"><span data-stu-id="ddd88-221">Sign in to your Azure account with this command.</span></span>
  
```powershell
Connect-AzAccount
```

<span data-ttu-id="ddd88-222">Obtenir le nom de votre abonnement à l’aide de cette commande.</span><span class="sxs-lookup"><span data-stu-id="ddd88-222">Get your subscription name using this  command.</span></span>
  
```powershell
Get-AzSubscription | Sort Name | Select Name
```

<span data-ttu-id="ddd88-223">Définissez votre abonnement Azure.</span><span class="sxs-lookup"><span data-stu-id="ddd88-223">Set your Azure subscription.</span></span> <span data-ttu-id="ddd88-224">Remplacez tout le contenu entre guillemets, y compris les \< and > caractères, par le nom correct.</span><span class="sxs-lookup"><span data-stu-id="ddd88-224">Replace everything within the quotation marks, including the \< and > characters, with the correct name.</span></span>
  
```powershell
$subscr="<subscription name>"
Get-AzSubscription -SubscriptionName $subscr | Select-AzSubscription
```

<span data-ttu-id="ddd88-225">Ensuite, créez un nouveau groupe de ressources.</span><span class="sxs-lookup"><span data-stu-id="ddd88-225">Next, create a new resource group.</span></span> <span data-ttu-id="ddd88-226">Pour déterminer un nom de groupe de ressources unique, utilisez cette commande pour répertorier vos groupes de ressources existants.</span><span class="sxs-lookup"><span data-stu-id="ddd88-226">To determine a unique resource group name, use this command to list your existing resource groups.</span></span>
  
```powershell
Get-AzResourceGroup | Sort ResourceGroupName | Select ResourceGroupName
```

<span data-ttu-id="ddd88-227">Créez votre nouveau groupe de ressources avec ces commandes.</span><span class="sxs-lookup"><span data-stu-id="ddd88-227">Create your new resource group with these commands.</span></span> <span data-ttu-id="ddd88-228">Remplacer tout le contenu entre guillemets, y compris les \< and > caractères, par les noms corrects.</span><span class="sxs-lookup"><span data-stu-id="ddd88-228">Replace everything within the quotation marks, including the \< and > characters, with the correct names.</span></span>
  
```powershell
$rgName="<resource group name>"
$locName="<location name, such as West US>"
New-AzResourceGroup -Name $rgName -Location $locName
```

<span data-ttu-id="ddd88-229">Ensuite, créez un nouveau réseau virtuel et la machine virtuelle WIN10 à l’aide de ces commandes.</span><span class="sxs-lookup"><span data-stu-id="ddd88-229">Next, create a new virtual network and the WIN10 virtual machine with these commands.</span></span> <span data-ttu-id="ddd88-230">Lorsque vous y êtes invité, indiquez le nom et le mot de passe du compte d’administrateur local pour WIN10, et enregistrez ces informations dans un emplacement sécurisé.</span><span class="sxs-lookup"><span data-stu-id="ddd88-230">When prompted, provide the name and password of the local administrator account for WIN10 and store these in a secure location.</span></span>
  
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

## <a name="phase-5-join-your-windows-10-computer-to-azure-ad"></a><span data-ttu-id="ddd88-231">Phase 5 : Association de votre ordinateur Windows 10 à Azure AD</span><span class="sxs-lookup"><span data-stu-id="ddd88-231">Phase 5: Join your Windows 10 computer to Azure AD</span></span>

<span data-ttu-id="ddd88-232">Lorsque l’ordinateur physique ou la machine virtuelle avec Windows 10 Entreprise est créée, connectez-vous avec un compte d’administrateur local.</span><span class="sxs-lookup"><span data-stu-id="ddd88-232">After the physical or virtual machine with Windows 10 Enterprise is created, sign in with a local administrator account.</span></span>
  
> [!NOTE]
> <span data-ttu-id="ddd88-233">Pour une machine virtuelle dans Azure, suivez  [ces instructions](https://docs.microsoft.com/azure/virtual-machines/windows/connect-logon) pour vous y connecter.</span><span class="sxs-lookup"><span data-stu-id="ddd88-233">For a virtual machine in Azure, use  [these instructions](https://docs.microsoft.com/azure/virtual-machines/windows/connect-logon) to connect to it.</span></span>
  
<span data-ttu-id="ddd88-234">Ensuite, associez l’ordinateur WIN10 au client Azure AD de votre abonnement Microsoft 365 E5.</span><span class="sxs-lookup"><span data-stu-id="ddd88-234">Next, join the WIN10 computer to the Azure AD tenant of your Microsoft 365 E5 subscription.</span></span>
  
1. <span data-ttu-id="ddd88-235">Sur le Bureau de l’ordinateur WIN10, sélectionnez **Start > settings > accounts > Access Work ou school > Connect**.</span><span class="sxs-lookup"><span data-stu-id="ddd88-235">On the desktop of the WIN10 computer, select **Start > Settings > Accounts > Access work or school > Connect**.</span></span>
    
2. <span data-ttu-id="ddd88-236">Dans la boîte de dialogue **configurer un compte professionnel ou scolaire** , sélectionnez **joindre cet appareil à Azure Active Directory**.</span><span class="sxs-lookup"><span data-stu-id="ddd88-236">In the **Set up a work or school account** dialog box, select **Join this device to Azure Active Directory**.</span></span>
    
3. <span data-ttu-id="ddd88-237">Dans **compte professionnel ou scolaire**, entrez le nom du compte d’administrateur général de votre abonnement Microsoft 365 E5, puis cliquez sur **suivant**.</span><span class="sxs-lookup"><span data-stu-id="ddd88-237">In **Work or school account**, enter the global administrator account name of your Microsoft 365 E5 subscription, and then select **Next**.</span></span>
    
4. <span data-ttu-id="ddd88-238">Dans **entrer le mot de passe**, entrez le mot de passe de votre compte d’administrateur général, puis sélectionnez **se connecter**.</span><span class="sxs-lookup"><span data-stu-id="ddd88-238">In **Enter password**, enter the password for your global administrator account, and then select **Sign in**.</span></span>
    
5. <span data-ttu-id="ddd88-239">Lorsque vous êtes invité à vous assurer qu’il s’agit de votre organisation, sélectionnez **rejoindre**, puis sélectionnez **Terminer**.</span><span class="sxs-lookup"><span data-stu-id="ddd88-239">When prompted to make sure that this is your organization, select **Join**, and then select **Done**.</span></span>
    
6. <span data-ttu-id="ddd88-240">Fermez la fenêtre Paramètres.</span><span class="sxs-lookup"><span data-stu-id="ddd88-240">Close the settings window.</span></span>
    
<span data-ttu-id="ddd88-241">Ensuite, installez Microsoft 365 apps pour entreprise sur l’ordinateur WIN10 :</span><span class="sxs-lookup"><span data-stu-id="ddd88-241">Next, install Microsoft 365 Apps for enterprise on the WIN10 computer:</span></span>
  
1. <span data-ttu-id="ddd88-242">Ouvrez le navigateur Microsoft Edge et connectez-vous au [Centre d’administration microsoft 365](https://admin.microsoft.com) avec vos informations d’identification de compte d’administrateur général.</span><span class="sxs-lookup"><span data-stu-id="ddd88-242">Open the Microsoft Edge browser and sign in to the [Microsoft 365 admin center](https://admin.microsoft.com) with your global administrator account credentials.</span></span>
    
2. <span data-ttu-id="ddd88-243">Dans l’onglet **Accueil Microsoft Office** , sélectionnez **installer Office**.</span><span class="sxs-lookup"><span data-stu-id="ddd88-243">On the **Microsoft Office Home** tab, select **Install Office**.</span></span>
    
3. <span data-ttu-id="ddd88-244">Lorsque vous y êtes invité, sélectionnez **exécuter**, puis cliquez sur **Oui** pour **le contrôle de compte d’utilisateur**.</span><span class="sxs-lookup"><span data-stu-id="ddd88-244">When prompted with what to do, select **Run**, and then select **Yes** for **User Account Control**.</span></span>
    
4. <span data-ttu-id="ddd88-245">Attendez qu’Office termine l’installation.</span><span class="sxs-lookup"><span data-stu-id="ddd88-245">Wait for Office to complete its installation.</span></span> <span data-ttu-id="ddd88-246">Lorsque vous voyez **tous les jeux !**, sélectionnez **Fermer** deux fois.</span><span class="sxs-lookup"><span data-stu-id="ddd88-246">When you see **You're all set!**, select **Close** twice.</span></span>
    
<span data-ttu-id="ddd88-247">Votre environnement obtenu se présente comme suit :</span><span class="sxs-lookup"><span data-stu-id="ddd88-247">Your resulting environment looks like this:</span></span>

![Phase 5 de l’environnement de test Microsoft 365 Entreprise](../media/lightweight-base-configuration-microsoft-365-enterprise/Phase4.png)

<span data-ttu-id="ddd88-249">Cela inclut l’ordinateur WIN10 avec :</span><span class="sxs-lookup"><span data-stu-id="ddd88-249">This includes the WIN10 computer that has:</span></span>

- <span data-ttu-id="ddd88-250">rejoint le client Azure AD de votre abonnement Microsoft 365 E5 ;</span><span class="sxs-lookup"><span data-stu-id="ddd88-250">Joined the Azure AD tenant of your Microsoft 365 E5 subscription.</span></span>
- <span data-ttu-id="ddd88-251">été inscrit en tant que périphérique Azure AD dans Microsoft Intune (EMS) ;</span><span class="sxs-lookup"><span data-stu-id="ddd88-251">Enrolled as an Azure AD device in Microsoft Intune (EMS).</span></span>
- <span data-ttu-id="ddd88-252">Applications Microsoft 365 pour Enterprise installées.</span><span class="sxs-lookup"><span data-stu-id="ddd88-252">Microsoft 365 Apps for enterprise installed.</span></span>
  
<span data-ttu-id="ddd88-253">Vous êtes maintenant prêt à tester les fonctionnalités supplémentaires de [Microsoft 365 pour entreprises](https://www.microsoft.com/microsoft-365/enterprise).</span><span class="sxs-lookup"><span data-stu-id="ddd88-253">You are now ready to experiment with additional features of [Microsoft 365 for enterprise](https://www.microsoft.com/microsoft-365/enterprise).</span></span>
  
## <a name="next-steps"></a><span data-ttu-id="ddd88-254">Étapes suivantes</span><span class="sxs-lookup"><span data-stu-id="ddd88-254">Next steps</span></span>

<span data-ttu-id="ddd88-255">Découvrez les nouveaux ensembles de guides pour les tests de laboratoire :</span><span class="sxs-lookup"><span data-stu-id="ddd88-255">Explore these additional sets of Test Lab Guides:</span></span>
  
- [<span data-ttu-id="ddd88-256">Identité</span><span class="sxs-lookup"><span data-stu-id="ddd88-256">Identity</span></span>](m365-enterprise-test-lab-guides.md#identity)
- [<span data-ttu-id="ddd88-257">Gestion des appareils mobiles</span><span class="sxs-lookup"><span data-stu-id="ddd88-257">Mobile device management</span></span>](m365-enterprise-test-lab-guides.md#mobile-device-management)
- [<span data-ttu-id="ddd88-258">Protection des informations</span><span class="sxs-lookup"><span data-stu-id="ddd88-258">Information protection</span></span>](m365-enterprise-test-lab-guides.md#information-protection)
   

## <a name="see-also"></a><span data-ttu-id="ddd88-259">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ddd88-259">See also</span></span>

[<span data-ttu-id="ddd88-260">Microsoft 365 pour les entreprises Guides de laboratoire d'essai</span><span class="sxs-lookup"><span data-stu-id="ddd88-260">Microsoft 365 for enterprise Test Lab Guides</span></span>](m365-enterprise-test-lab-guides.md)

[<span data-ttu-id="ddd88-261">Vue d’ensemble de Microsoft 365 pour entreprise</span><span class="sxs-lookup"><span data-stu-id="ddd88-261">Microsoft 365 for enterprise overview</span></span>](microsoft-365-overview.md)

[<span data-ttu-id="ddd88-262">Documentation Microsoft 365 pour entreprise</span><span class="sxs-lookup"><span data-stu-id="ddd88-262">Microsoft 365 for enterprise documentation</span></span>](https://docs.microsoft.com/microsoft-365-enterprise/)
