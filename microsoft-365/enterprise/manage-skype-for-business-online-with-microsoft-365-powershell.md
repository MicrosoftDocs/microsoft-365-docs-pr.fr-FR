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
ms.openlocfilehash: ff35463dc0c2e16106432c393b10e31e6bf0a5d2
ms.sourcegitcommit: 22755cebfbfa2c4dc3f8b4f54ccb23636a211ee5
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/15/2020
ms.locfileid: "48477100"
---
# <a name="manage-skype-for-business-online-with-powershell"></a><span data-ttu-id="00724-103">Gestion de Skype Entreprise Online avec PowerShell</span><span class="sxs-lookup"><span data-stu-id="00724-103">Manage Skype for Business Online with PowerShell</span></span>

<span data-ttu-id="00724-104">*Cet article est valable pour Microsoft 365 Entreprise et Office 365 Entreprise.*</span><span class="sxs-lookup"><span data-stu-id="00724-104">*This article applies to both Microsoft 365 Enterprise and Office 365 Enterprise.*</span></span>

<span data-ttu-id="00724-105">Les administrateurs Skype Entreprise Online sont responsables de la gestion des stratégies.</span><span class="sxs-lookup"><span data-stu-id="00724-105">Skype for Business Online administrators are responsible for managing policies.</span></span> <span data-ttu-id="00724-106">Bien que vous puissiez effectuer certaines de ces tâches dans le Centre d’administration Microsoft 365, d’autres sont plus faciles à faire dans PowerShell.</span><span class="sxs-lookup"><span data-stu-id="00724-106">Although you can do some of these tasks in the Microsoft 365 admin center, others are easier to do in PowerShell.</span></span>

## <a name="before-you-start"></a><span data-ttu-id="00724-107">Avant de commencer</span><span class="sxs-lookup"><span data-stu-id="00724-107">Before you start</span></span>

  > [!Note]
   > <span data-ttu-id="00724-108">Le connecteur Skype Entreprise Online fait actuellement partie du dernier module PowerShell Teams.</span><span class="sxs-lookup"><span data-stu-id="00724-108">Skype for Business Online Connector is currently part of the latest Teams PowerShell module.</span></span> <span data-ttu-id="00724-109">Si vous utilisez la version publique la plus récente de PowerShell Teams, vous n’avez pas besoin d’installer le connecteur Skype Entreprise Online.</span><span class="sxs-lookup"><span data-stu-id="00724-109">If you're using the latest Teams PowerShell public release, you don't need to install the Skype for Business Online Connector.</span></span>
   
<span data-ttu-id="00724-110">Installer le [module PowerShell Teams](https://docs.microsoft.com/microsoftteams/teams-powershell-install).</span><span class="sxs-lookup"><span data-stu-id="00724-110">Install the [Teams PowerShell module](https://docs.microsoft.com/microsoftteams/teams-powershell-install).</span></span>


## <a name="connect-using-admin-credentials"></a><span data-ttu-id="00724-111">Se connecter à l’aide des informations d’identification d’administrateur</span><span class="sxs-lookup"><span data-stu-id="00724-111">Connect using admin credentials</span></span>

1. <span data-ttu-id="00724-112">Ouvrez une fenêtre d’invite de commandes Windows PowerShell et exécutez les commandes suivantes :</span><span class="sxs-lookup"><span data-stu-id="00724-112">Open a Windows PowerShell command prompt window and run the following commands:</span></span>
    
   ```powershell
   Import-Module MicrosoftTeams
   $userCredential = Get-Credential
   $sfbSession = New-CsOnlineSession -Credential $userCredential
   Import-PSSession $sfbSession
   ```

2. <span data-ttu-id="00724-113">Dans la boîte de dialogue **Demande d’informations d’identification Windows PowerShell**, saisissez le nom et le mot de passe de votre compte d'administrateur, puis sélectionnez **OK**.</span><span class="sxs-lookup"><span data-stu-id="00724-113">In the **Windows PowerShell Credential Request** dialog box, type your administrator account name and password, and then select **OK**.</span></span>


## <a name="connect-using-an-admin-account-with-multi-factor-authentication"></a><span data-ttu-id="00724-114">Se connecter à l’aide d’un compte d’administrateur avec l’authentification multifacteur</span><span class="sxs-lookup"><span data-stu-id="00724-114">Connect using an admin account with multi-factor authentication</span></span>

1. <span data-ttu-id="00724-115">Ouvrez une fenêtre d’invite de commandes Windows PowerShell et exécutez les commandes suivantes :</span><span class="sxs-lookup"><span data-stu-id="00724-115">Open a Windows PowerShell command prompt window, and run the following commands:</span></span>

   ```powershell
   Import-Module MicrosoftTeams
   $sfbSession = New-CsOnlineSession
   Import-PSSession $sfbSession
   ```

2. <span data-ttu-id="00724-116">Lorsque vous y êtes invité par la commande **New-CsOnlineSession**, entrez le nom de votre compte d'administrateur Skype Entreprise Online.</span><span class="sxs-lookup"><span data-stu-id="00724-116">When prompted by the **New-CsOnlineSession** command, enter your Skype for Business Online administrator account name.</span></span>

3. <span data-ttu-id="00724-117">Dans la boîte de dialogue **Vous connecter à votre compte**, tapez votre mot de passe d’administrateur Skype Entreprise Online, puis sélectionnez **Connexion**.</span><span class="sxs-lookup"><span data-stu-id="00724-117">In the **Sign in to your account** dialog box, type your Skype for Business Online administrator password and select **Sign in**.</span></span>

4. <span data-ttu-id="00724-118">Dans la boîte de dialogue **Vous connecter à votre compte** , suivez les instructions d’ajout d’informations d’authentification, telles qu’un code de vérification, puis sélectionnez **Vérifier**.</span><span class="sxs-lookup"><span data-stu-id="00724-118">In the **Sign in to your account** dialog box, follow the instructions to add authentication information, such as a verification code, and then select **Verify**.</span></span>

<span data-ttu-id="00724-119">Pour plus d’informations, consultez :</span><span class="sxs-lookup"><span data-stu-id="00724-119">For more information, see:</span></span>
  
- [<span data-ttu-id="00724-120">Gestion des stratégies Skype Entreprise Online avec PowerShell</span><span class="sxs-lookup"><span data-stu-id="00724-120">Manage Skype for Business Online policies with PowerShell</span></span>](manage-skype-for-business-online-policies-with-microsoft-365-powershell.md)
    
- [<span data-ttu-id="00724-121">Affectation de stratégies Skype Entreprise Online propres à chaque utilisateur avec PowerShell</span><span class="sxs-lookup"><span data-stu-id="00724-121">Assign per-user Skype for Business Online policies with PowerShell</span></span>](assign-per-user-skype-for-business-online-policies-with-microsoft-365-powershell.md)
    
## <a name="see-also"></a><span data-ttu-id="00724-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="00724-122">See also</span></span>

[<span data-ttu-id="00724-123">Gestion de Microsoft 365 à l’aide de PowerShell</span><span class="sxs-lookup"><span data-stu-id="00724-123">Manage Microsoft 365 with PowerShell</span></span>](manage-microsoft-365-with-microsoft-365-powershell.md)
  
[<span data-ttu-id="00724-124">Prise en main de PowerShell pour Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="00724-124">Get started with PowerShell for Microsoft 365</span></span>](getting-started-with-microsoft-365-powershell.md)

[<span data-ttu-id="00724-125">Références sur l’applet de commande Skype Entreprise PowerShell</span><span class="sxs-lookup"><span data-stu-id="00724-125">Skype for Business PowerShell cmdlet references</span></span>](https://docs.microsoft.com/powershell/module/skype/?view=skype-ps)
