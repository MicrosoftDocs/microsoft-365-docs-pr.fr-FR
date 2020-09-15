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
ms.openlocfilehash: d50f35d7d5e81622eb8dfc3bbf8328a8c43e9676
ms.sourcegitcommit: aeb94601a81db3ead8610c2f36cff30eb9fe10e7
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/10/2020
ms.locfileid: "47430033"
---
# <a name="manage-skype-for-business-online-with-powershell"></a><span data-ttu-id="99b3d-103">Gestion de Skype Entreprise Online avec PowerShell</span><span class="sxs-lookup"><span data-stu-id="99b3d-103">Manage Skype for Business Online with PowerShell</span></span>

<span data-ttu-id="99b3d-104">*Cet article est valable pour Microsoft 365 Entreprise et Office 365 Entreprise.*</span><span class="sxs-lookup"><span data-stu-id="99b3d-104">*This article applies to both Microsoft 365 Enterprise and Office 365 Enterprise.*</span></span>

<span data-ttu-id="99b3d-105">Les administrateurs Skype Entreprise Online sont responsables de la gestion des stratégies.</span><span class="sxs-lookup"><span data-stu-id="99b3d-105">Skype for Business Online administrators are responsible for managing policies.</span></span> <span data-ttu-id="99b3d-106">Bien que vous puissiez effectuer certaines de ces tâches dans le Centre d’administration Microsoft 365, d’autres sont plus faciles à faire dans PowerShell.</span><span class="sxs-lookup"><span data-stu-id="99b3d-106">Although you can do some of these tasks in the Microsoft 365 admin center, others are easier to do in PowerShell.</span></span>

## <a name="before-you-start"></a><span data-ttu-id="99b3d-107">Avant de commencer</span><span class="sxs-lookup"><span data-stu-id="99b3d-107">Before you start</span></span>

<span data-ttu-id="99b3d-108">Téléchargez et installez le [module Skype Entreprise Online Windows PowerShell](https://www.microsoft.com/download/details.aspx?id=39366), puis redémarrez votre ordinateur.</span><span class="sxs-lookup"><span data-stu-id="99b3d-108">Download and install the [Skype for Business Online Windows PowerShell module](https://www.microsoft.com/download/details.aspx?id=39366), and then restart your computer.</span></span>


## <a name="connect-using-skype-for-business-online-admin-credentials"></a><span data-ttu-id="99b3d-109">Se connecter à l’aide des informations d’identification de l’administrateur Skype Entreprise Online</span><span class="sxs-lookup"><span data-stu-id="99b3d-109">Connect using Skype for Business Online admin credentials</span></span>

1. <span data-ttu-id="99b3d-110">Ouvrez une fenêtre d’invite de commandes Windows PowerShell et exécutez les commandes suivantes :</span><span class="sxs-lookup"><span data-stu-id="99b3d-110">Open a Windows PowerShell command prompt window and run the following commands:</span></span>
    
   ```powershell
   Import-Module SkypeOnlineConnector
   $userCredential = Get-Credential
   $sfbSession = New-CsOnlineSession -Credential $userCredential
   Import-PSSession $sfbSession
   ```

2. <span data-ttu-id="99b3d-111">Dans la boîte de dialogue **Demande d’informations d’identification Windows PowerShell**, saisissez le nom et le mot de passe de votre compte d'administrateur Skype Entreprise Online, puis sélectionnez **OK**.</span><span class="sxs-lookup"><span data-stu-id="99b3d-111">In the **Windows PowerShell Credential Request** dialog box, type your Skype for Business Online administrator account name and password, and then select **OK**.</span></span>


## <a name="connect-using-an-admin-account-with-multi-factor-authentication"></a><span data-ttu-id="99b3d-112">Se connecter à l’aide d’un compte d’administrateur avec l’authentification multifacteur</span><span class="sxs-lookup"><span data-stu-id="99b3d-112">Connect using an admin account with multi-factor authentication</span></span>

1. <span data-ttu-id="99b3d-113">Ouvrez une fenêtre d’invite de commandes Windows PowerShell et exécutez les commandes suivantes :</span><span class="sxs-lookup"><span data-stu-id="99b3d-113">Open a Windows PowerShell command prompt window, and run the following commands:</span></span>

   ```powershell
   Import-Module SkypeOnlineConnector
   $sfbSession = New-CsOnlineSession
   Import-PSSession $sfbSession
   ```

2. <span data-ttu-id="99b3d-114">Lorsque vous y êtes invité par la commande **New-CsOnlineSession**, entrez le nom de votre compte d'administrateur Skype Entreprise Online.</span><span class="sxs-lookup"><span data-stu-id="99b3d-114">When prompted by the **New-CsOnlineSession** command, enter your Skype for Business Online administrator account name.</span></span>

3. <span data-ttu-id="99b3d-115">Dans la boîte de dialogue **Vous connecter à votre compte**, tapez votre mot de passe d’administrateur Skype Entreprise Online, puis sélectionnez **Connexion**.</span><span class="sxs-lookup"><span data-stu-id="99b3d-115">In the **Sign in to your account** dialog box, type your Skype for Business Online administrator password and select **Sign in**.</span></span>

4. <span data-ttu-id="99b3d-116">Dans la boîte de dialogue **Vous connecter à votre compte** , suivez les instructions d’ajout d’informations d’authentification, telles qu’un code de vérification, puis sélectionnez **Vérifier**.</span><span class="sxs-lookup"><span data-stu-id="99b3d-116">In the **Sign in to your account** dialog box, follow the instructions to add authentication information, such as a verification code, and then select **Verify**.</span></span>

<span data-ttu-id="99b3d-117">Pour plus d’informations, consultez :</span><span class="sxs-lookup"><span data-stu-id="99b3d-117">For more information, see:</span></span>
  
- [<span data-ttu-id="99b3d-118">Gestion des stratégies Skype Entreprise Online avec PowerShell</span><span class="sxs-lookup"><span data-stu-id="99b3d-118">Manage Skype for Business Online policies with PowerShell</span></span>](manage-skype-for-business-online-policies-with-microsoft-365-powershell.md)
    
- [<span data-ttu-id="99b3d-119">Affectation de stratégies Skype Entreprise Online propres à chaque utilisateur avec PowerShell</span><span class="sxs-lookup"><span data-stu-id="99b3d-119">Assign per-user Skype for Business Online policies with PowerShell</span></span>](assign-per-user-skype-for-business-online-policies-with-microsoft-365-powershell.md)
    
## <a name="see-also"></a><span data-ttu-id="99b3d-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="99b3d-120">See also</span></span>

[<span data-ttu-id="99b3d-121">Gestion de Microsoft 365 à l’aide de PowerShell</span><span class="sxs-lookup"><span data-stu-id="99b3d-121">Manage Microsoft 365 with PowerShell</span></span>](manage-microsoft-365-with-microsoft-365-powershell.md)
  
[<span data-ttu-id="99b3d-122">Prise en main de PowerShell pour Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="99b3d-122">Get started with PowerShell for Microsoft 365</span></span>](getting-started-with-microsoft-365-powershell.md)

[<span data-ttu-id="99b3d-123">Références sur l’applet de commande Skype Entreprise PowerShell</span><span class="sxs-lookup"><span data-stu-id="99b3d-123">Skype for Business PowerShell cmdlet references</span></span>](https://docs.microsoft.com/powershell/module/skype/?view=skype-ps)
