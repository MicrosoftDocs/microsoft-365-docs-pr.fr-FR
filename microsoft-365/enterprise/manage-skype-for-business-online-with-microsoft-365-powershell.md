---
title: Gestion de Skype Entreprise Online avec PowerShell
ms.author: josephd
author: JoeDavies-MSFT
manager: laurawi
ms.date: 07/17/2020
audience: ITPro
ms.topic: article
ms.service: o365-administration
localization_priority: Priority
ms.collection: Ent_O365
f1.keywords:
- NOCSH
ms.custom: ''
ms.assetid: 054c16e6-9fd1-4e85-a0e6-81788b8410ea
description: Utilisez PowerShell pour Microsoft 365 pour gérer des stratégies Skype Entreprise Online, des stratégies par utilisateur et des paramètres de réunion.
ms.openlocfilehash: 1992edfb6d1c141c7ed4db22064960873b768865
ms.sourcegitcommit: babbba2b5bf69fd3facde2905ec024b753dcd1b3
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/06/2021
ms.locfileid: "50514955"
---
# <a name="manage-skype-for-business-online-with-powershell"></a><span data-ttu-id="bf533-103">Gestion de Skype Entreprise Online avec PowerShell</span><span class="sxs-lookup"><span data-stu-id="bf533-103">Manage Skype for Business Online with PowerShell</span></span>

<span data-ttu-id="bf533-104">*Cet article est valable pour Microsoft 365 Entreprise et Office 365 Entreprise.*</span><span class="sxs-lookup"><span data-stu-id="bf533-104">*This article applies to both Microsoft 365 Enterprise and Office 365 Enterprise.*</span></span>

<span data-ttu-id="bf533-105">Les administrateurs Skype Entreprise Online sont responsables de la gestion des stratégies.</span><span class="sxs-lookup"><span data-stu-id="bf533-105">Skype for Business Online administrators are responsible for managing policies.</span></span> <span data-ttu-id="bf533-106">Bien que vous puissiez effectuer certaines de ces tâches dans le Centre d’administration Microsoft 365, d’autres sont plus faciles à faire dans PowerShell.</span><span class="sxs-lookup"><span data-stu-id="bf533-106">Although you can do some of these tasks in the Microsoft 365 admin center, others are easier to do in PowerShell.</span></span>

## <a name="before-you-start"></a><span data-ttu-id="bf533-107">Avant de commencer</span><span class="sxs-lookup"><span data-stu-id="bf533-107">Before you start</span></span>

  > [!Note]
   > <span data-ttu-id="bf533-108">Le connecteur Skype Entreprise Online fait actuellement partie du dernier module PowerShell Teams.</span><span class="sxs-lookup"><span data-stu-id="bf533-108">Skype for Business Online Connector is currently part of the latest Teams PowerShell module.</span></span> <span data-ttu-id="bf533-109">Si vous utilisez la version publique la plus récente de PowerShell Teams, vous n’avez pas besoin d’installer le connecteur Skype Entreprise Online.</span><span class="sxs-lookup"><span data-stu-id="bf533-109">If you're using the latest Teams PowerShell public release, you don't need to install the Skype for Business Online Connector.</span></span>
   
<span data-ttu-id="bf533-110">Installer le [module PowerShell Teams](https://docs.microsoft.com/microsoftteams/teams-powershell-install).</span><span class="sxs-lookup"><span data-stu-id="bf533-110">Install the [Teams PowerShell module](https://docs.microsoft.com/microsoftteams/teams-powershell-install).</span></span>


## <a name="connect-using-admin-credentials"></a><span data-ttu-id="bf533-111">Se connecter à l’aide des informations d’identification d’administrateur</span><span class="sxs-lookup"><span data-stu-id="bf533-111">Connect using admin credentials</span></span>

1. <span data-ttu-id="bf533-112">Ouvrez une fenêtre d’invite de commandes Windows PowerShell et exécutez les commandes suivantes :</span><span class="sxs-lookup"><span data-stu-id="bf533-112">Open a Windows PowerShell command prompt window and run the following commands:</span></span>
    
   ```powershell
   Import-Module MicrosoftTeams
   $userCredential = Get-Credential
   Connect-MicrosoftTeams -Credential $userCredential
   ```

2. <span data-ttu-id="bf533-113">Dans la boîte de dialogue **Demande d’informations d’identification Windows PowerShell**, saisissez le nom et le mot de passe de votre compte d'administrateur, puis sélectionnez **OK**.</span><span class="sxs-lookup"><span data-stu-id="bf533-113">In the **Windows PowerShell Credential Request** dialog box, type your administrator account name and password, and then select **OK**.</span></span>


## <a name="connect-using-an-admin-account-with-multi-factor-authentication"></a><span data-ttu-id="bf533-114">Se connecter à l’aide d’un compte d’administrateur avec l’authentification multifacteur</span><span class="sxs-lookup"><span data-stu-id="bf533-114">Connect using an admin account with multi-factor authentication</span></span>

1. <span data-ttu-id="bf533-115">Ouvrez une fenêtre d’invite de commandes Windows PowerShell et exécutez les commandes suivantes :</span><span class="sxs-lookup"><span data-stu-id="bf533-115">Open a Windows PowerShell command prompt window, and run the following commands:</span></span>

   ```powershell
   Import-Module MicrosoftTeams
   Connect-MicrosoftTeams
   ```

2. <span data-ttu-id="bf533-116">Lorsque vous y êtes invité, entrez le nom utilisateur de votre compte d'administrateur Skype Entreprise Online.</span><span class="sxs-lookup"><span data-stu-id="bf533-116">When prompted enter your Skype for Business Online administrator account name.</span></span>

3. <span data-ttu-id="bf533-117">Dans la boîte de dialogue **Vous connecter à votre compte**, tapez votre mot de passe d’administrateur Skype Entreprise Online, puis sélectionnez **Connexion**.</span><span class="sxs-lookup"><span data-stu-id="bf533-117">In the **Sign in to your account** dialog box, type your Skype for Business Online administrator password and select **Sign in**.</span></span>

4. <span data-ttu-id="bf533-118">Dans la boîte de dialogue **Vous connecter à votre compte** , suivez les instructions d’ajout d’informations d’authentification, telles qu’un code de vérification, puis sélectionnez **Vérifier**.</span><span class="sxs-lookup"><span data-stu-id="bf533-118">In the **Sign in to your account** dialog box, follow the instructions to add authentication information, such as a verification code, and then select **Verify**.</span></span>

<span data-ttu-id="bf533-119">Pour plus d’informations, consultez :</span><span class="sxs-lookup"><span data-stu-id="bf533-119">For more information, see:</span></span>
  
- [<span data-ttu-id="bf533-120">Gestion des stratégies Skype Entreprise Online avec PowerShell</span><span class="sxs-lookup"><span data-stu-id="bf533-120">Manage Skype for Business Online policies with PowerShell</span></span>](manage-skype-for-business-online-policies-with-microsoft-365-powershell.md)
    
- [<span data-ttu-id="bf533-121">Affectation de stratégies Skype Entreprise Online propres à chaque utilisateur avec PowerShell</span><span class="sxs-lookup"><span data-stu-id="bf533-121">Assign per-user Skype for Business Online policies with PowerShell</span></span>](assign-per-user-skype-for-business-online-policies-with-microsoft-365-powershell.md)
    
## <a name="see-also"></a><span data-ttu-id="bf533-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="bf533-122">See also</span></span>

[<span data-ttu-id="bf533-123">Gestion de Microsoft 365 à l’aide de PowerShell</span><span class="sxs-lookup"><span data-stu-id="bf533-123">Manage Microsoft 365 with PowerShell</span></span>](manage-microsoft-365-with-microsoft-365-powershell.md)
  
[<span data-ttu-id="bf533-124">Prise en main de PowerShell pour Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="bf533-124">Get started with PowerShell for Microsoft 365</span></span>](getting-started-with-microsoft-365-powershell.md)

[<span data-ttu-id="bf533-125">Références sur l’applet de commande Skype Entreprise PowerShell</span><span class="sxs-lookup"><span data-stu-id="bf533-125">Skype for Business PowerShell cmdlet references</span></span>](https://docs.microsoft.com/powershell/module/skype/?view=skype-ps)
