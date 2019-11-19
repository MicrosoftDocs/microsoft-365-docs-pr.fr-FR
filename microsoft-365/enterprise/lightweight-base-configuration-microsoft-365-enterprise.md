---
title: Configuration de base légère
ms.author: josephd
author: JoeDavies-MSFT
manager: laurawi
ms.date: 11/14/2019
audience: ITPro
ms.topic: article
ms.service: o365-solutions
localization_priority: Priority
ms.collection:
- M365-subscription-management
- Strat_O365_Enterprise
ms.custom:
- Ent_TLGs
ms.assetid: 6f916a77-301c-4be2-b407-6cec4d80df76
description: Utilisez ce guide de laboratoire de test pour créer un environnement de test léger destiné aux tests Microsoft 365 Entreprise.
ms.openlocfilehash: fce612000fac79fe9552fa9882d6c48fdacda1c2
ms.sourcegitcommit: ea48c86c727dcd9d4b3b970b14a4260337f158f9
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/18/2019
ms.locfileid: "38694121"
---
# <a name="the-lightweight-base-configuration"></a><span data-ttu-id="2ee12-103">Configuration de base légère</span><span class="sxs-lookup"><span data-stu-id="2ee12-103">The lightweight base configuration</span></span>

<span data-ttu-id="2ee12-104">*Ce Guide de Laboratoire Test peut être utilisé pour les environnements de test Microsoft 365 Enterprise et Office 365 Enterprise.*</span><span class="sxs-lookup"><span data-stu-id="2ee12-104">*This Test Lab Guide can be used for both Microsoft 365 Enterprise and Office 365 Enterprise test environments.*</span></span>

<span data-ttu-id="2ee12-105">Cet article vous fournit des instructions étape par étape pour créer un environnement simplifié avec un abonnement Microsoft 365 E5 et un ordinateur exécutant Windows 10 Entreprise.</span><span class="sxs-lookup"><span data-stu-id="2ee12-105">This article provides you with step-by-step instructions to create a simplified environment with a Microsoft 365 E5 subscription and a computer running Windows 10 Enterprise.</span></span> 

![Environnement de test Microsoft 365 Entreprise léger](media/lightweight-base-configuration-microsoft-365-enterprise/Phase4.png)

<span data-ttu-id="2ee12-107">Utilisez l’environnement que vous aurez créé pour tester les fonctionnalités et le bon fonctionnement de [Microsoft 365 Entreprise](https://www.microsoft.com/microsoft-365/enterprise).</span><span class="sxs-lookup"><span data-stu-id="2ee12-107">Use the resulting environment to test the features and functionality of [Microsoft 365 Enterprise](https://www.microsoft.com/microsoft-365/enterprise).</span></span>

![Guides de laboratoire de test pour Microsoft Cloud](media/m365-enterprise-test-lab-guides/cloud-tlg-icon.png)
  
> [!TIP]
> <span data-ttu-id="2ee12-109">Cliquez [ici](media/m365-enterprise-test-lab-guides/Microsoft365EnterpriseTLGStack.pdf) pour afficher le plan de tous les articles de l’ensemble de guides de laboratoire de test de Microsoft 365 Entreprise.</span><span class="sxs-lookup"><span data-stu-id="2ee12-109">Click [here](media/m365-enterprise-test-lab-guides/Microsoft365EnterpriseTLGStack.pdf) for a visual map to all the articles in the Microsoft 365 Enterprise Test Lab Guide stack.</span></span>

## <a name="phase-1-create-your-office-365-e5-subscription"></a><span data-ttu-id="2ee12-110">Phase 1 : Création de votre abonnement Office 365 E5</span><span class="sxs-lookup"><span data-stu-id="2ee12-110">Phase 1: Create your Office 365 E5 subscription</span></span>

<span data-ttu-id="2ee12-111">Nous allons commencer avec un abonnement d’évaluation Office 365 E5, puis ajouter l’abonnement Microsoft 365 E5 à celui-ci.</span><span class="sxs-lookup"><span data-stu-id="2ee12-111">We start with an Office 365 E5 trial subscription and then add the Microsoft 365 E5 subscription to it.</span></span>

<span data-ttu-id="2ee12-112">Pour démarrer votre abonnement d’évaluation Office 365 E5, vous avez besoin d’un nom d’entreprise fictif et d’un nouveau compte Microsoft.</span><span class="sxs-lookup"><span data-stu-id="2ee12-112">To start your Office 365 E5 trial subscription, you first need a fictitious company name and a new Microsoft account.</span></span>
  
1. <span data-ttu-id="2ee12-p101">Nous vous recommandons d’utiliser une variante du nom d’entreprise Contoso pour le nom de votre entreprise. Il s’agit d’une entreprise fictive utilisée dans le contenu d’exemple de Microsoft. Toutefois, cette étape n’est pas obligatoire. Indiquer le nom fictif de votre entreprise ici : ![](./media/Common-Images/TableLine.png)</span><span class="sxs-lookup"><span data-stu-id="2ee12-p101">We recommend that you use a variant of the company name Contoso for your company name, which is a fictitious company used in Microsoft sample content, but it isn't required. Record your fictitious company name here: ![](./media/Common-Images/TableLine.png)</span></span>
    
2. <span data-ttu-id="2ee12-p102">Pour ouvrir un nouveau compte Microsoft, accédez à [https://outlook.com](https://outlook.com) et créez un compte avec un nouveau compte de messagerie et une nouvelle adresse. Vous utiliserez ce compte pour vous inscrire à Office 365.</span><span class="sxs-lookup"><span data-stu-id="2ee12-p102">To sign up for a new Microsoft account, go to [https://outlook.com](https://outlook.com) and create an account with a new email account and address. You will use this account to sign up for Office 365.</span></span>
    
  - <span data-ttu-id="2ee12-117">Indiquer le prénom et le nom de famille utilisés pour votre nouveau compte ici : ![](./media/Common-Images/TableLine.png)</span><span class="sxs-lookup"><span data-stu-id="2ee12-117">Record the first and last name of your new account here: ![](./media/Common-Images/TableLine.png)</span></span>
    
  - <span data-ttu-id="2ee12-118">Indiquer l’adresse du nouveau compte de messagerie ici : ![](./media/Common-Images/TableLine.png)@outlook.com</span><span class="sxs-lookup"><span data-stu-id="2ee12-118">Record the new email account address here: ![](./media/Common-Images/TableLine.png)@outlook.com</span></span>
    
### <a name="sign-up-for-an-office-365-e5-trial-subscription"></a><span data-ttu-id="2ee12-119">Inscription à un abonnement d’évaluation Office 365 E5</span><span class="sxs-lookup"><span data-stu-id="2ee12-119">Sign up for an Office 365 E5 trial subscription</span></span>

1. <span data-ttu-id="2ee12-120">Ouvrez le navigateur Internet sur votre ordinateur, puis accédez à [https://aka.ms/e5trial](https://aka.ms/e5trial).</span><span class="sxs-lookup"><span data-stu-id="2ee12-120">Open the Internet browser on your computer and go to [https://aka.ms/e5trial](https://aka.ms/e5trial).</span></span>
    
2. <span data-ttu-id="2ee12-121">Sur la page **Bienvenue, nous allons faire connaissance**, indiquez les informations suivantes :</span><span class="sxs-lookup"><span data-stu-id="2ee12-121">On the **Welcome, let's get to know you** page, specify:</span></span>
    
  - <span data-ttu-id="2ee12-122">votre emplacement physique ;</span><span class="sxs-lookup"><span data-stu-id="2ee12-122">Your physical location</span></span>
    
  - <span data-ttu-id="2ee12-123">le prénom et le nom utilisés pour votre nouveau compte Microsoft ;</span><span class="sxs-lookup"><span data-stu-id="2ee12-123">The first and last name of your new Microsoft account</span></span>
    
  - <span data-ttu-id="2ee12-124">votre nouvelle adresse de compte de messagerie ;</span><span class="sxs-lookup"><span data-stu-id="2ee12-124">Your new email account address</span></span>
    
  - <span data-ttu-id="2ee12-125">un numéro de téléphone professionnel ;</span><span class="sxs-lookup"><span data-stu-id="2ee12-125">A business phone number</span></span>
    
  - <span data-ttu-id="2ee12-126">le nom de votre entreprise fictive ;</span><span class="sxs-lookup"><span data-stu-id="2ee12-126">Your fictional company name</span></span>
    
  - <span data-ttu-id="2ee12-127">la taille de votre entreprise (250 à 999 personnes).</span><span class="sxs-lookup"><span data-stu-id="2ee12-127">An organization size of 250-999 people</span></span>
    
3. <span data-ttu-id="2ee12-128">Cliquez sur **Encore une dernière étape**.</span><span class="sxs-lookup"><span data-stu-id="2ee12-128">Click **Just one more step**.</span></span>
    
4. <span data-ttu-id="2ee12-129">Sur la page **Créer votre identifiant utilisateur**, entrez un nom d’utilisateur dérivé de votre nouvelle adresse de messagerie, le nom de votre entreprise fictive après le signe @ (supprimez tous les espaces dans le nom), puis un mot de passe (deux fois) pour ce nouveau compte Office 365. </span><span class="sxs-lookup"><span data-stu-id="2ee12-129">On the **Create your user ID** page, type a user name based on your new email address, your fictional company after the @ sign (remove all spaces in the name), then a password (twice) for this new Office 365 account.</span></span>
    
    <span data-ttu-id="2ee12-130">Enregistrez le mot de passe saisi dans un emplacement sécurisé.</span><span class="sxs-lookup"><span data-stu-id="2ee12-130">Record the password that you typed in a secure location.</span></span>
    
    <span data-ttu-id="2ee12-131">Enregistrez le nom de votre entreprise fictive, ou **nom de l’organisation**, ici : ![](./media/Common-Images/TableLine.png)</span><span class="sxs-lookup"><span data-stu-id="2ee12-131">Record your fictional company name, to be referred to as the **organization name**, here: ![](./media/Common-Images/TableLine.png)</span></span>
    
5. <span data-ttu-id="2ee12-132">Cliquez sur **Créer mon compte**.</span><span class="sxs-lookup"><span data-stu-id="2ee12-132">Click **Create my account**.</span></span>
    
6. <span data-ttu-id="2ee12-p103">Sur la page **Prouvez que vous n’êtes pas un robot.**, tapez le numéro de votre téléphone compatible avec du texte, puis cliquez sur **M’envoyer un SMS**.</span><span class="sxs-lookup"><span data-stu-id="2ee12-p103">On the **Prove. You're. Not. A. Robot.** page, type the phone number of your text-capable phone, and then click **Text me**.</span></span>
    
7. <span data-ttu-id="2ee12-135">Saisissez le code de vérification qui vous été envoyé par message, puis cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="2ee12-135">Type the verification code from the received text message, and then click **Next**.</span></span>
    
8. <span data-ttu-id="2ee12-136">Enregistrez l’URL de la page de connexion ici (sélectionnez-la et copiez-la) : ![](./media/Common-Images/TableLine.png)</span><span class="sxs-lookup"><span data-stu-id="2ee12-136">Record the sign-in page URL here (select and copy): ![](./media/Common-Images/TableLine.png)</span></span>
    
9. <span data-ttu-id="2ee12-137">Enregistrez l’identifiant utilisateur ici (sélectionnez-le et copiez-le) : ![](./media/Common-Images/TableLine.png).onmicrosoft.com</span><span class="sxs-lookup"><span data-stu-id="2ee12-137">Record the user ID here (select and copy): ![](./media/Common-Images/TableLine.png).onmicrosoft.com</span></span>
    
    <span data-ttu-id="2ee12-138">Cette valeur correspond au **nom de l’administrateur général Office 365**.</span><span class="sxs-lookup"><span data-stu-id="2ee12-138">This value will be referred to as the **Office 365 global administrator name**.</span></span>
    
10. <span data-ttu-id="2ee12-139">Cliquez sur le lien **Nous sommes prêts** lorsqu’il s’affiche.</span><span class="sxs-lookup"><span data-stu-id="2ee12-139">When you see **You're ready to go**, click it.</span></span>
    
11. <span data-ttu-id="2ee12-140">Sur la page suivante, attendez qu’Office 365 termine la configuration et que tous les titres soient visibles.</span><span class="sxs-lookup"><span data-stu-id="2ee12-140">On the next page, wait until Office 365 completes setting up and all the tiles are available.</span></span>
    
<span data-ttu-id="2ee12-141">Vous devriez voir la page principale du portail Office 365 à partir de laquelle vous pouvez accéder aux services Office et au Centre d’administration Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="2ee12-141">You should see main Office 365 portal page from which you can access Office services and the Microsoft 365 admin center.</span></span>
  
<span data-ttu-id="2ee12-142">Vous avez créé un abonnement d’évaluation d’Office 365 pour que votre environnement de développement/test ait un client Azure AD distinct de tout abonnement payant que vous utilisez actuellement.</span><span class="sxs-lookup"><span data-stu-id="2ee12-142">We have you create a trial subscription of Office 365 so that your dev/test environment has a separate Azure AD tenant from any paid subscriptions you currently have.</span></span> <span data-ttu-id="2ee12-143">Cette séparation signifie que vous pouvez ajouter et supprimer des utilisateurs et groupes dans le client test sans incidence sur vos abonnements de production.</span><span class="sxs-lookup"><span data-stu-id="2ee12-143">This separation means you can add and remove users and groups in the test tenant without affecting your production subscriptions.</span></span>
    
## <a name="phase-2-configure-your-office-365-trial-subscription"></a><span data-ttu-id="2ee12-144">Phase 2 : configuration de votre abonnement d’évaluation Office 365</span><span class="sxs-lookup"><span data-stu-id="2ee12-144">Phase 2: Configure your Office 365 trial subscription</span></span>

<span data-ttu-id="2ee12-145">Durant cette phase, configurez votre abonnement Office 365 en y ajoutant des utilisateurs supplémentaires et assignez-les aux licences Office 365 E5.</span><span class="sxs-lookup"><span data-stu-id="2ee12-145">In this phase, you configure your Office 365 subscription with additional users and assign them Office 365 E5 licenses.</span></span>
  
<span data-ttu-id="2ee12-146">Suivez les instructions dans [Se connecter à Office 365 PowerShell](https://docs.microsoft.com/office365/enterprise/powershell/connect-to-office-365-powershell#connect-with-the-azure-active-directory-powershell-for-graph-module) pour vous connecter à votre abonnement Office 365 avec le module Graph Azure Active Directory PowerShell à partir de votre ordinateur.</span><span class="sxs-lookup"><span data-stu-id="2ee12-146">Use the instructions in [Connect to Office 365 PowerShell](https://docs.microsoft.com/office365/enterprise/powershell/connect-to-office-365-powershell#connect-with-the-azure-active-directory-powershell-for-graph-module) to connect to your Office 365 subscription with the Azure Active Directory PowerShell for Graph module from your computer.</span></span>
    
<span data-ttu-id="2ee12-147">Dans la boîte de dialogue Demande d’informations d’identification Windows PowerShell, saisissez le nom de l’administrateur général Office 365 (exemple : jdoe@contosotoycompany.onmicrosoft.com) et le mot de passe.</span><span class="sxs-lookup"><span data-stu-id="2ee12-147">In the Windows PowerShell Credential Request dialog box, type the Office 365 global administrator name (example: jdoe@contosotoycompany.onmicrosoft.com) and password.</span></span>
  
<span data-ttu-id="2ee12-148">Entrez le nom de votre organisation (exemple : contosotoycompany) et le code de pays à deux caractères pour indiquer votre emplacement, ainsi qu’un mot de passe de compte commun, puis exécutez les commandes suivantes à partir de l’invite PowerShell :</span><span class="sxs-lookup"><span data-stu-id="2ee12-148">Fill in your organization name (example: contosotoycompany), the two-character country code for your location, a common account password, and then run the following commands from the PowerShell prompt:</span></span>

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
> <span data-ttu-id="2ee12-149">L’utilisation ici d’un mot de passe courant est pour l’automatisation et la simplicité de configuration pour un environnement de développement et de test.</span><span class="sxs-lookup"><span data-stu-id="2ee12-149">The use of a common password here is for automation and ease of configuration for a dev/test environment.</span></span> <span data-ttu-id="2ee12-150">Bien évidemment, cela est hautement déconseillé pour les abonnements de production.</span><span class="sxs-lookup"><span data-stu-id="2ee12-150">Obviously, this is highly discouraged for production subscriptions.</span></span> 

### <a name="record-key-information-for-future-reference"></a><span data-ttu-id="2ee12-151">Enregistrer les informations clés pour future référence</span><span class="sxs-lookup"><span data-stu-id="2ee12-151">Record key information for future reference</span></span>

<span data-ttu-id="2ee12-152">Nous vous recommandons d’imprimer cet article afin de consigner les informations dont vous aurez besoin dans cet environnement au cours des 30 jours de votre abonnement à la version d’évaluation Office 365.</span><span class="sxs-lookup"><span data-stu-id="2ee12-152">You might want to print this article to record the specific information that you will need for this environment over the 30 days of the Office 365 trial subscription.</span></span> <span data-ttu-id="2ee12-153">Vous pouvez facilement étendre l’abonnement d’évaluation pour une période supplémentaire de 30 jours.</span><span class="sxs-lookup"><span data-stu-id="2ee12-153">You can easily extend the trail subscription for another 30 days.</span></span> <span data-ttu-id="2ee12-154">Pour un environnement de développement/test permanent, créez un nouvel abonnement payant avec un client Azure AD séparé et un nombre réduit de licences.</span><span class="sxs-lookup"><span data-stu-id="2ee12-154">For a permanent dev/test environment, create a new paid subscription with a separate Azure AD tenant and a small number of licenses.</span></span>

<span data-ttu-id="2ee12-155">Enregistrez les valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="2ee12-155">Record these values:</span></span>
  
- <span data-ttu-id="2ee12-156">Nom de l’administrateur général Office 365 : ![](./media/Common-Images/TableLine.png).onmicrosoft.com (indiqué à l’étape 9 de la phase 2)</span><span class="sxs-lookup"><span data-stu-id="2ee12-156">Office 365 global administrator name: ![](./media/Common-Images/TableLine.png).onmicrosoft.com (from step 9 of Phase 2)</span></span>
    
    <span data-ttu-id="2ee12-157">Enregistrez également le mot de passe de ce compte dans un emplacement sécurisé.</span><span class="sxs-lookup"><span data-stu-id="2ee12-157">Also record the password for this account in a secure location.</span></span>
    
- <span data-ttu-id="2ee12-158">Nom de l’organisation de l’abonnement d’évaluation : ![](./media/Common-Images/TableLine.png) (indiqué à l’étape 4 de la phase 2)</span><span class="sxs-lookup"><span data-stu-id="2ee12-158">Your trial subscription organization name: ![](./media/Common-Images/TableLine.png) (from step 4 of Phase 2)</span></span>
    
- <span data-ttu-id="2ee12-159">Pour répertorier les comptes pour Utilisateur 2, Utilisateur 3, Utilisateur 4 et Utilisateur 5, exécutez la commande suivante à partir de l’invite Module Windows Azure Active Directory pour Windows PowerShell :</span><span class="sxs-lookup"><span data-stu-id="2ee12-159">To list the accounts for User 2, User 3, User 4, and User 5, run the following command from the Windows Azure Active Directory Module for Windows PowerShell prompt:</span></span>
    
  ```powershell
  Get-AzureADUser | Sort UserPrincipalName | Select UserPrincipalName
  ```

    <span data-ttu-id="2ee12-160">Enregistrez les noms de compte ici :</span><span class="sxs-lookup"><span data-stu-id="2ee12-160">Record the account names here:</span></span>
    
  - <span data-ttu-id="2ee12-161">Nom du compte Utilisateur 2 : user2@![](./media/Common-Images/TableLine.png).onmicrosoft.com</span><span class="sxs-lookup"><span data-stu-id="2ee12-161">User 2 account name: user2@![](./media/Common-Images/TableLine.png).onmicrosoft.com</span></span>
    
  - <span data-ttu-id="2ee12-162">Nom du compte Utilisateur 3 : user3@![](./media/Common-Images/TableLine.png).onmicrosoft.com</span><span class="sxs-lookup"><span data-stu-id="2ee12-162">User 3 account name: user3@![](./media/Common-Images/TableLine.png).onmicrosoft.com</span></span>
    
  - <span data-ttu-id="2ee12-163">Nom du compte Utilisateur 4 : user4@![](./media/Common-Images/TableLine.png).onmicrosoft.com</span><span class="sxs-lookup"><span data-stu-id="2ee12-163">User 4 account name: user4@![](./media/Common-Images/TableLine.png).onmicrosoft.com</span></span>
    
  - <span data-ttu-id="2ee12-164">Nom du compte Utilisateur 5 : user5@![](./media/Common-Images/TableLine.png).onmicrosoft.com</span><span class="sxs-lookup"><span data-stu-id="2ee12-164">User 5 account name: user5@![](./media/Common-Images/TableLine.png).onmicrosoft.com</span></span>
    
    <span data-ttu-id="2ee12-165">Enregistrez également les mots de passe communs de ces comptes dans un emplacement sécurisé.</span><span class="sxs-lookup"><span data-stu-id="2ee12-165">Also record the common password for these accounts in a secure location.</span></span>
   

### <a name="using-an-office-365-devtest-environment"></a><span data-ttu-id="2ee12-166">Utiliser un environnement de développement/test Office 365</span><span class="sxs-lookup"><span data-stu-id="2ee12-166">Using an Office 365 dev/test environment</span></span>

<span data-ttu-id="2ee12-167">Si vous avez simplement besoin d’un environnement Office 365 pour le développement et le test, vous pouvez vous arrêter ici.</span><span class="sxs-lookup"><span data-stu-id="2ee12-167">If all you need is an Office 365 dev/test environment, you can stop here.</span></span> 

<span data-ttu-id="2ee12-168">Pour plus d’informations sur les guides de labo de test, voir [les guides de laboratoire de test Microsoft 365 Entreprise](m365-enterprise-test-lab-guides.md) pour Office 365 et Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="2ee12-168">See [Microsoft 365 Enterprise Test Lab Guides](m365-enterprise-test-lab-guides.md) for additional Test Lab Guides that apply to both Office 365 and Microsoft 365.</span></span>
  
## <a name="phase-3-add-a-microsoft-365-e5-trial-subscription"></a><span data-ttu-id="2ee12-169">Phase 3 : Ajoutez un abonnement d’évaluation Microsoft 365 E5.</span><span class="sxs-lookup"><span data-stu-id="2ee12-169">Phase 3: Add a Microsoft 365 E5 trial subscription</span></span>

<span data-ttu-id="2ee12-170">Dans cette phase, vous vous inscrivez pour l’abonnement d’évaluation Microsoft 365 E5 et l’ajoutez à la même organisation que votre abonnement d’évaluation d’Office 365 E5.</span><span class="sxs-lookup"><span data-stu-id="2ee12-170">In this phase, you sign up for the Microsoft 365 E5 trial subscription and add it to the same organization as your Office 365 E5 trial subscription.</span></span>
  
<span data-ttu-id="2ee12-171">Tout d’abord, ajoutez l’abonnement d’évaluation Microsoft 365 E5 et attribuez une licence Microsoft 365 à votre compte d’administrateur général.</span><span class="sxs-lookup"><span data-stu-id="2ee12-171">First, add the Microsoft 365 E5 trial subscription and assign a Microsoft 365 license to your global administrator account.</span></span>
  
1. <span data-ttu-id="2ee12-172">Utilisez une instance privée d’un navigateur Internet pour vous connecter au centre d’administration Microsoft 365 sur [https://admin.microsoft.com](https://admin.microsoft.com)à l’aide de vos informations d’identification de compte d’administrateur général.</span><span class="sxs-lookup"><span data-stu-id="2ee12-172">With a private instance of an Internet browser, sign in to the Microsoft 365 admin center at [https://admin.microsoft.com](https://admin.microsoft.com) with your global administrator account credentials.</span></span>
    
2. <span data-ttu-id="2ee12-173">Sur la page **Centre d’administration Microsoft 365**, dans le volet de navigation de gauche, cliquez sur **Facturation > Acheter des services**.</span><span class="sxs-lookup"><span data-stu-id="2ee12-173">On the **Microsoft 365 admin center** page, in the left navigation, click **Billing > Purchase services**.</span></span>
    
3. <span data-ttu-id="2ee12-174">Sur la page**acheter des services**, recherchez l’élément **Microsoft 365 E5**.</span><span class="sxs-lookup"><span data-stu-id="2ee12-174">On the **Purchase services** page, find the **Microsoft 365 E5** item.</span></span> <span data-ttu-id="2ee12-175">Pointez votre souris dessus et cliquez sur **Démarrer l’essai gratuit**.</span><span class="sxs-lookup"><span data-stu-id="2ee12-175">Hover your mouse pointer over it and click **Start free trial**.</span></span>

4. <span data-ttu-id="2ee12-176">Sur la page **version d’évaluation de Microsoft 365 E5**, choisissez de recevoir un SMS ou un appel, entrez votre numéro de téléphone, puis cliquez sur **envoyer un SMS** ou **m’appeler**.</span><span class="sxs-lookup"><span data-stu-id="2ee12-176">On the **Microsoft 365 E5 Trial** page, choose to receive a text or a call, enter your phone number, then click **Text me** or **Call me**.</span></span>

5. <span data-ttu-id="2ee12-177">Dans la page **Confirmer votre commande**, cliquez sur **Essayer maintenant**.</span><span class="sxs-lookup"><span data-stu-id="2ee12-177">On the **Confirm your order** page, click **Try now**.</span></span>

6. <span data-ttu-id="2ee12-178">Dans la page **Réception de la commande**, cliquez sur **Continuer**.</span><span class="sxs-lookup"><span data-stu-id="2ee12-178">On the **Order receipt** page, click **Continue**.</span></span>

7. <span data-ttu-id="2ee12-179">Dans le centre d’administration Microsoft 365, cliquez sur **utilisateurs actifs**et votre compte d’administrateur.</span><span class="sxs-lookup"><span data-stu-id="2ee12-179">In the Microsoft 365 admin center, click **Active users**, and then your administrator account.</span></span>

8. <span data-ttu-id="2ee12-180">Cliquez sur **modifier** pour **licences de produits**.</span><span class="sxs-lookup"><span data-stu-id="2ee12-180">Click **Edit** for **Product licenses**.</span></span>

9. <span data-ttu-id="2ee12-181">Désactivez la licence pour Office 365 Entreprise E5 et activer la licence pour Microsoft 365 E5.</span><span class="sxs-lookup"><span data-stu-id="2ee12-181">Turn off the license for Office 365 Enterprise E5 and turn on the license for Microsoft 365 E5.</span></span>

10. <span data-ttu-id="2ee12-182">Cliquez sur **Enregistrer > Fermer > Fermer**.</span><span class="sxs-lookup"><span data-stu-id="2ee12-182">Click **Save > Close > Close**.</span></span>

<span data-ttu-id="2ee12-183">Ensuite, répétez les étapes 8 et 11 de la procédure précédente pour tous vos autres comptes (Utilisateur2, Utilisateur3, Utilisateur4 et Utilisateur5).</span><span class="sxs-lookup"><span data-stu-id="2ee12-183">Next, repeat steps 8 through 11 of the previous procedure for all of your other accounts (User 2, User 3, User 4, and User 5).</span></span>
  
> [!NOTE]
> <span data-ttu-id="2ee12-184">L’abonnement d’évaluation de Microsoft 365 E5 est de 30 jours.</span><span class="sxs-lookup"><span data-stu-id="2ee12-184">The Microsoft 365 E5 trial subscription is 30 days.</span></span> <span data-ttu-id="2ee12-185">Pour un environnement de test permanent, convertissez cet abonnement en abonnement payant avec un nombre réduit de licences.</span><span class="sxs-lookup"><span data-stu-id="2ee12-185">For a permanent test environment, convert this trial subscription to a paid subscription with a small number of licenses.</span></span> 
  
<span data-ttu-id="2ee12-186">Votre environnement de test comporte maintenant :</span><span class="sxs-lookup"><span data-stu-id="2ee12-186">Your test environment now has:</span></span>
  
- <span data-ttu-id="2ee12-187">Un abonnement d’évaluation de Microsoft 365 E5.</span><span class="sxs-lookup"><span data-stu-id="2ee12-187">A Microsoft 365 E5 trial subscription.</span></span>
- <span data-ttu-id="2ee12-188">Tous vos comptes d’utilisateur appropriés (l’administrateur général ou tous les cinq comptes d’utilisateur) sont activés pour utiliser Microsoft 365 E5.</span><span class="sxs-lookup"><span data-stu-id="2ee12-188">All your appropriate user accounts (either just the global administrator or all five user accounts) are enabled to use Microsoft 365 E5.</span></span>
    
<span data-ttu-id="2ee12-189">Voici la configuration qui en résulte, avec ajout de Microsoft 365 E5, qui inclut Office 365 et Enterprise Security + Management (EMS).</span><span class="sxs-lookup"><span data-stu-id="2ee12-189">Here is your resulting configuration, which adds Microsoft 365 E5, which includes both Office 365 and Enterprise Security + Management (EMS).</span></span>
  
![Phase 2 de l’environnement de test Microsoft 365 Entreprise](media/lightweight-base-configuration-microsoft-365-enterprise/Phase2.png)
  
## <a name="phase-4-create-a-windows-10-enterprise-computer"></a><span data-ttu-id="2ee12-191">Phase 4 : Création d’un ordinateur Windows 10 Entreprise</span><span class="sxs-lookup"><span data-stu-id="2ee12-191">Phase 4: Create a Windows 10 Enterprise computer</span></span>

<span data-ttu-id="2ee12-192">Au cours de cette phase, vous allez créer un ordinateur autonome exécutant Windows 10 Entreprise sous forme d’un ordinateur physique, d’une machine virtuelle ou d’une machine virtuelle Azure.</span><span class="sxs-lookup"><span data-stu-id="2ee12-192">In this phase, you create a standalone computer running Windows 10 Enterprise as either a physical computer, a virtual machine, or an Azure virtual machine.</span></span>
  
### <a name="physical-computer"></a><span data-ttu-id="2ee12-193">Ordinateur physique</span><span class="sxs-lookup"><span data-stu-id="2ee12-193">Physical computer</span></span>

<span data-ttu-id="2ee12-p109">Munissez-vous d’un ordinateur personnel et installez Windows 10 Entreprise dessus. Vous pouvez télécharger la version d’évaluation de Windows 10 Entreprise [ici](https://www.microsoft.com/evalcenter/evaluate-windows-10-enterprise).</span><span class="sxs-lookup"><span data-stu-id="2ee12-p109">Obtain a personal computer and install Windows 10 Enterprise on it. You can download the Windows 10 Enterprise trial [here](https://www.microsoft.com/evalcenter/evaluate-windows-10-enterprise).</span></span>
  
### <a name="virtual-machine"></a><span data-ttu-id="2ee12-196">Machine virtuelle</span><span class="sxs-lookup"><span data-stu-id="2ee12-196">Virtual machine</span></span>

<span data-ttu-id="2ee12-p110">Créez une machine virtuelle à l’aide de l’hyperviseur de votre choix et installez Windows 10 Entreprise dessus. Vous pouvez télécharger la version d’évaluation de Windows 10 Entreprise [ici](https://www.microsoft.com/evalcenter/evaluate-windows-10-enterprise).</span><span class="sxs-lookup"><span data-stu-id="2ee12-p110">Create a virtual machine using the hypervisor of your choice and install Windows 10 Enterprise on it. You can download the Windows 10 Enterprise trial [here](https://www.microsoft.com/evalcenter/evaluate-windows-10-enterprise).</span></span>
  
### <a name="virtual-machine-in-azure"></a><span data-ttu-id="2ee12-199">Machine virtuelle dans Azure</span><span class="sxs-lookup"><span data-stu-id="2ee12-199">Virtual machine in Azure</span></span>

<span data-ttu-id="2ee12-p111">Pour créer une machine virtuelle exécutant Windows 10 dans Microsoft Azure, ***vous devez disposer d’un abonnement Visual Studio*** qui vous permet d’accéder à l’image pour Windows 10 Entreprise. D’autres types d’abonnements Azure, tels que les abonnements d’évaluation et payants, ne permettent pas d’accéder à cette image. Pour obtenir les informations les plus récentes, reportez-vous à l’article [Utilisation d’un client Windows dans Azure pour les scénarios de développement et/ou test](https://docs.microsoft.com/azure/virtual-machines/windows/client-images).</span><span class="sxs-lookup"><span data-stu-id="2ee12-p111">To create a Windows 10 virtual machine in Microsoft Azure, ***you must have a Visual Studio-based subscription***, which has access to the image for Windows 10 Enterprise. Other types of Azure subscriptions, such as trial and paid subscriptions, do not have access to this image. For the latest information, see [Use Windows client in Azure for dev/test scenarios](https://docs.microsoft.com/azure/virtual-machines/windows/client-images).</span></span>
  
> [!NOTE]
> <span data-ttu-id="2ee12-p112">Les ensembles de commandes suivants utilisent la dernière version d’Azure PowerShell. Reportez-vous à l’article relatif à la [prise en main des cmdlets Azure PowerShell](https://docs.microsoft.com/powershell/azureps-cmdlets-docs/). Ces ensembles de commandes créent une machine virtuelle Windows 10 Entreprise nommée WIN10 ainsi que l’intégralité de son infrastructure requise, y compris un groupe de ressources, un compte de stockage et un réseau virtuel. Si vous connaissez déjà les services d’infrastructure Azure, adaptez ces instructions à votre infrastructure actuellement déployée.</span><span class="sxs-lookup"><span data-stu-id="2ee12-p112">The following command sets use the latest version of Azure PowerShell. See [Get started with Azure PowerShell cmdlets](https://docs.microsoft.com/powershell/azureps-cmdlets-docs/). These command sets build a Windows 10 Enterprise virtual machine named WIN10 and all of its required infrastructure, including a resource group, a storage account, and a virtual network. If you are already familiar with Azure infrastructure services, please adapt these instructions to suit your currently deployed infrastructure.</span></span> 
  
<span data-ttu-id="2ee12-207">Tout d’abord, lancez une invite Microsoft PowerShell.</span><span class="sxs-lookup"><span data-stu-id="2ee12-207">First, start a Microsoft PowerShell prompt.</span></span>
  
<span data-ttu-id="2ee12-208">Connectez-vous à votre compte Azure avec la commande suivante.</span><span class="sxs-lookup"><span data-stu-id="2ee12-208">Sign in to your Azure account with the following command.</span></span>
  
```powershell
Connect-AzAccount
```

<span data-ttu-id="2ee12-209">Obtenez le nom de votre abonnement à l’aide de la commande suivante.</span><span class="sxs-lookup"><span data-stu-id="2ee12-209">Get your subscription name using the following command.</span></span>
  
```powershell
Get-AzSubscription | Sort Name | Select Name
```

<span data-ttu-id="2ee12-p113">Définissez votre abonnement Azure. Remplacez tout le texte entre guillemets, y compris les caractères \< et >, avec le nom correct.</span><span class="sxs-lookup"><span data-stu-id="2ee12-p113">Set your Azure subscription. Replace everything within the quotes, including the \< and > characters, with the correct name.</span></span>
  
```powershell
$subscr="<subscription name>"
Get-AzSubscription -SubscriptionName $subscr | Select-AzSubscription
```

<span data-ttu-id="2ee12-p114">Ensuite, créez un nouveau groupe de ressources. Pour déterminer un nom de groupe de ressources unique, utilisez cette commande pour répertorier vos groupes de ressources existants.</span><span class="sxs-lookup"><span data-stu-id="2ee12-p114">Next, create a new resource group. To determine a unique resource group name, use this command to list your existing resource groups.</span></span>
  
```powershell
Get-AzResourceGroup | Sort ResourceGroupName | Select ResourceGroupName
```

<span data-ttu-id="2ee12-p115">Créez votre groupe de ressources avec ces commandes. Remplacez tout le texte entre guillemets, y compris les caractères \< et >, par les noms corrects.</span><span class="sxs-lookup"><span data-stu-id="2ee12-p115">Create your new resource group with these commands. Replace everything within the quotes, including the \< and > characters, with the correct names.</span></span>
  
```powershell
$rgName="<resource group name>"
$locName="<location name, such as West US>"
New-AzResourceGroup -Name $rgName -Location $locName
```

<span data-ttu-id="2ee12-p116">Ensuite, créez une ressource virtuelle et la machine virtuelle WIN10 avec ces commandes. Lorsque vous y êtes invité, indiquez le nom et le mot de passe du compte d’administrateur local pour WIN10, et enregistrez ces informations dans un emplacement sécurisé.</span><span class="sxs-lookup"><span data-stu-id="2ee12-p116">Next, you create a new virtual network and the WIN10 virtual machine with these commands. When prompted, provide the name and password of the local administrator account for WIN10 and store these in a secure location.</span></span>
  
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

## <a name="phase-5-join-your-windows-10-computer-to-azure-ad"></a><span data-ttu-id="2ee12-218">Phase 5 : Association de votre ordinateur Windows 10 à Azure AD</span><span class="sxs-lookup"><span data-stu-id="2ee12-218">Phase 5: Join your Windows 10 computer to Azure AD</span></span>

<span data-ttu-id="2ee12-219">Lorsque l’ordinateur physique ou la machine virtuelle avec Windows 10 Entreprise est créée, connectez-vous avec un compte d’administrateur local.</span><span class="sxs-lookup"><span data-stu-id="2ee12-219">After the physical or virtual machine with Windows 10 Enterprise is created, sign in with a local administrator account.</span></span>
  
> [!NOTE]
> <span data-ttu-id="2ee12-220">Suivez [ces instructions](https://docs.microsoft.com/azure/virtual-machines/windows/connect-logon) pour vous connecter à une machine virtuelle dans Azure.</span><span class="sxs-lookup"><span data-stu-id="2ee12-220">For a virtual machine in Azure, connect to it using [these instructions](https://docs.microsoft.com/azure/virtual-machines/windows/connect-logon).</span></span>
  
<span data-ttu-id="2ee12-221">Ensuite, associez l’ordinateur WIN10 au client Azure AD de votre abonnement Microsoft 365 E5.</span><span class="sxs-lookup"><span data-stu-id="2ee12-221">Next, join the WIN10 computer to the Azure AD tenant of your Microsoft 365 E5 subscription.</span></span>
  
1. <span data-ttu-id="2ee12-222">Sur le bureau de l’ordinateur WIN10, cliquez sur **Démarrer > Paramètres > Comptes > Accès Professionnel ou Scolaire > Se connecter**.</span><span class="sxs-lookup"><span data-stu-id="2ee12-222">At the desktop of the WIN10 computer, click **Start > Settings > Accounts > Access work or school > Connect**.</span></span>
    
2. <span data-ttu-id="2ee12-223">Dans la boîte de dialogue **Configurer un compte professionnel ou scolaire**, cliquez sur **Joindre cet appareil à Azure Active Directory**.</span><span class="sxs-lookup"><span data-stu-id="2ee12-223">In the **Set up a work or school account** dialog box, click **Join this device to Azure Active Directory**.</span></span>
    
3. <span data-ttu-id="2ee12-224">Dans **Compte professionnel ou scolaire**, saisissez le nom de compte Administrateur général de votre abonnement Microsoft 365 E5, puis cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="2ee12-224">In **Work or school account**, type the global administrator account name of your Microsoft 365 E5 subscription, and then click **Next**.</span></span>
    
4. <span data-ttu-id="2ee12-225">Dans **Saisie du mot de passe**, saisissez le mot de passe de votre compte Administrateur général, puis cliquez sur **Se connecter**.</span><span class="sxs-lookup"><span data-stu-id="2ee12-225">In **Enter password**, type the password for your global administrator account, and then click **Sign in**.</span></span>
    
5. <span data-ttu-id="2ee12-226">Lorsque vous devez confirmer qu’il s’agit bien de votre organisation, cliquez sur **Joindre**, puis sur **Terminé**.</span><span class="sxs-lookup"><span data-stu-id="2ee12-226">When prompted to make sure this is your organization, click **Join**, and then click **Done**.</span></span>
    
6. <span data-ttu-id="2ee12-227">Fermez la fenêtre Paramètres.</span><span class="sxs-lookup"><span data-stu-id="2ee12-227">Close the settings window.</span></span>
    
<span data-ttu-id="2ee12-228">Ensuite, installez Office 365 ProPlus sur l’ordinateur WIN10.</span><span class="sxs-lookup"><span data-stu-id="2ee12-228">Next, install Office 365 ProPlus on the WIN10 computer.</span></span>
  
1. <span data-ttu-id="2ee12-229">Ouvrez le navigateur Microsoft Edge et connectez-vous au portail Office à l’aide de vos informations d’identification de compte d’administrateur général.</span><span class="sxs-lookup"><span data-stu-id="2ee12-229">Open the Microsoft Edge browser and sign in to the Office portal with your global administrator account credentials.</span></span> <span data-ttu-id="2ee12-230">Pour obtenir de l’aide, consultez [Où se connecter à Office 365](https://support.office.com/Article/Where-to-sign-in-to-Office-365-e9eb7d51-5430-4929-91ab-6157c5a050b4).</span><span class="sxs-lookup"><span data-stu-id="2ee12-230">For help, see [Where to sign in to Office 365](https://support.office.com/Article/Where-to-sign-in-to-Office-365-e9eb7d51-5430-4929-91ab-6157c5a050b4).</span></span>
    
2. <span data-ttu-id="2ee12-231">Dans l’onglet **Accueil Microsoft Office**, cliquez sur **Installer Office**.</span><span class="sxs-lookup"><span data-stu-id="2ee12-231">On the **Microsoft Office Home** tab, click **Install Office**.</span></span>
    
3. <span data-ttu-id="2ee12-232">Lorsque vous êtes invité à décider de l’action à effectuer, cliquez sur **Exécuter**, puis sur **Oui** pour **Contrôle de compte d’utilisateur**.</span><span class="sxs-lookup"><span data-stu-id="2ee12-232">When prompted with what to do, click **Run**, and then click **Yes** for **User Account Control**.</span></span>
    
4. <span data-ttu-id="2ee12-p118">Attendez qu’Office termine l’installation. Lorsque le message **Vous voilà prêt !** s’affiche, cliquez deux fois sur **Fermer**.</span><span class="sxs-lookup"><span data-stu-id="2ee12-p118">Wait for Office to complete its installation. When you see **You're all set!**, click **Close** twice.</span></span>
    
<span data-ttu-id="2ee12-235">Voici votre environnement final.</span><span class="sxs-lookup"><span data-stu-id="2ee12-235">Here is your resulting environment.</span></span>

![Phase 5 de l’environnement de test Microsoft 365 Entreprise](media/lightweight-base-configuration-microsoft-365-enterprise/Phase4.png)

<span data-ttu-id="2ee12-237">Cela inclut l’ordinateur WIN10 avec :</span><span class="sxs-lookup"><span data-stu-id="2ee12-237">This includes the WIN10 computer that has:</span></span>

- <span data-ttu-id="2ee12-238">rejoint le client Azure AD de votre abonnement Microsoft 365 E5 ;</span><span class="sxs-lookup"><span data-stu-id="2ee12-238">Joined the Azure AD tenant of your Microsoft 365 E5 subscription.</span></span>
- <span data-ttu-id="2ee12-239">été inscrit en tant que périphérique Azure AD dans Microsoft Intune (EMS) ;</span><span class="sxs-lookup"><span data-stu-id="2ee12-239">Enrolled as an Azure AD device in Microsoft Intune (EMS).</span></span>
- <span data-ttu-id="2ee12-240">installé Office 365 ProPlus.</span><span class="sxs-lookup"><span data-stu-id="2ee12-240">Has Office 365 ProPlus installed.</span></span>
  
<span data-ttu-id="2ee12-241">Vous êtes désormais prêt à profiter des fonctionnalités supplémentaires de [Microsoft 365 Entreprise](https://www.microsoft.com/microsoft-365/enterprise).</span><span class="sxs-lookup"><span data-stu-id="2ee12-241">You are now ready to experiment with additional features of [Microsoft 365 Enterprise](https://www.microsoft.com/microsoft-365/enterprise).</span></span>
  
## <a name="next-steps"></a><span data-ttu-id="2ee12-242">Étapes suivantes</span><span class="sxs-lookup"><span data-stu-id="2ee12-242">Next steps</span></span>

<span data-ttu-id="2ee12-243">Découvrez les nouveaux ensembles de guides pour les tests de laboratoire :</span><span class="sxs-lookup"><span data-stu-id="2ee12-243">Explore these additional sets of Test Lab Guides:</span></span>
  
- [<span data-ttu-id="2ee12-244">Identité</span><span class="sxs-lookup"><span data-stu-id="2ee12-244">Identity</span></span>](m365-enterprise-test-lab-guides.md#identity)
- [<span data-ttu-id="2ee12-245">Gestion des appareils mobiles</span><span class="sxs-lookup"><span data-stu-id="2ee12-245">Mobile device management</span></span>](m365-enterprise-test-lab-guides.md#mobile-device-management)
- [<span data-ttu-id="2ee12-246">Protection des informations</span><span class="sxs-lookup"><span data-stu-id="2ee12-246">Information protection</span></span>](m365-enterprise-test-lab-guides.md#information-protection)
   

## <a name="see-also"></a><span data-ttu-id="2ee12-247">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2ee12-247">See also</span></span>

[<span data-ttu-id="2ee12-248">Guides de laboratoire de test Microsoft 365 Entreprise</span><span class="sxs-lookup"><span data-stu-id="2ee12-248">Microsoft 365 Enterprise Test Lab Guides</span></span>](m365-enterprise-test-lab-guides.md)

[<span data-ttu-id="2ee12-249">Déployer Microsoft 365 Entreprise</span><span class="sxs-lookup"><span data-stu-id="2ee12-249">Deploy Microsoft 365 Enterprise</span></span>](deploy-microsoft-365-enterprise.md)

[<span data-ttu-id="2ee12-250">Documentation Microsoft 365 Entreprise</span><span class="sxs-lookup"><span data-stu-id="2ee12-250">Microsoft 365 Enterprise documentation</span></span>](https://docs.microsoft.com/microsoft-365-enterprise/)
