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
description: 'Résumé : utilisez PowerShell pour Microsoft 365 pour gérer des stratégies Skype Entreprise Online, des stratégies par utilisateur et des paramètres de réunion.'
ms.openlocfilehash: aea78d135a5d7ffbb5d8480c549d0fdee88f7d51
ms.sourcegitcommit: 79065e72c0799064e9055022393113dfcf40eb4b
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/14/2020
ms.locfileid: "46690071"
---
# <a name="manage-skype-for-business-online-with-powershell"></a><span data-ttu-id="ac4c1-103">Gestion de Skype Entreprise Online avec PowerShell</span><span class="sxs-lookup"><span data-stu-id="ac4c1-103">Manage Skype for Business Online with PowerShell</span></span>

<span data-ttu-id="ac4c1-104">*Cet article est valable pour Microsoft 365 Entreprise et Office 365 Entreprise.*</span><span class="sxs-lookup"><span data-stu-id="ac4c1-104">*This article applies to both Microsoft 365 Enterprise and Office 365 Enterprise.*</span></span>

<span data-ttu-id="ac4c1-105">L’une des tâches principales de tout administrateur Skype Entreprise Online est de gérer les stratégies.</span><span class="sxs-lookup"><span data-stu-id="ac4c1-105">One of the primary tasks of any Skype for Business Online administrator is managing policies.</span></span> <span data-ttu-id="ac4c1-106">Bien que vous puissiez effectuer certaines de ces tâches dans le Centre d’administration Microsoft 365, d’autres tâches sont beaucoup plus rapides et plus simples à exécuter dans PowerShell.</span><span class="sxs-lookup"><span data-stu-id="ac4c1-106">Although you can accomplish some of these tasks in the Microsoft 365 admin center, other tasks are much quicker and easier in PowerShell.</span></span> 

## <a name="before-you-start"></a><span data-ttu-id="ac4c1-107">Avant de commencer</span><span class="sxs-lookup"><span data-stu-id="ac4c1-107">Before you start</span></span>

<span data-ttu-id="ac4c1-108">Téléchargez et installez le [module Connecteur Skype Entreprise Online](https://www.microsoft.com/download/details.aspx?id=39366), puis redémarrez votre ordinateur.</span><span class="sxs-lookup"><span data-stu-id="ac4c1-108">Download and install the [Skype for Business Online Connector module](https://www.microsoft.com/download/details.aspx?id=39366), and then restart your computer.</span></span>


## <a name="connect-using-a-skype-for-business-online-administrator-account-name-and-password"></a><span data-ttu-id="ac4c1-109">Connectez-vous à l’aide du nom et du mot de passe du compte d'administrateur Skype Entreprise Online</span><span class="sxs-lookup"><span data-stu-id="ac4c1-109">Connect using a Skype for Business Online administrator account name and password</span></span>

1. <span data-ttu-id="ac4c1-110">Ouvrez l’invite de commandes Windows PowerShell et exécutez les commandes suivantes :</span><span class="sxs-lookup"><span data-stu-id="ac4c1-110">Open a Windows PowerShell command prompt and run the following commands:</span></span> 
    
   ```powershell
   Import-Module SkypeOnlineConnector
   $userCredential = Get-Credential
   $sfbSession = New-CsOnlineSession -Credential $userCredential
   Import-PSSession $sfbSession
   ```

2. <span data-ttu-id="ac4c1-111">Dans la boîte de dialogue **Demande d’informations d’identification Windows PowerShell**, saisissez le nom et le mot de passe de votre compte d'administrateur Skype Entreprise Online, puis cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="ac4c1-111">In the **Windows PowerShell Credential Request** dialog box, type your Skype for Business Online administrator account name and password, and then click **OK**.</span></span>


## <a name="connect-using-a-skype-for-business-online-administrator-account-with-multi-factor-authentication"></a><span data-ttu-id="ac4c1-112">Connectez-vous à l’aide du compte d'administrateur Skype Entreprise Online avec l’authentification multifacteur</span><span class="sxs-lookup"><span data-stu-id="ac4c1-112">Connect using a Skype for Business Online administrator account with multi-factor authentication</span></span>

1. <span data-ttu-id="ac4c1-113">Ouvrez l’invite de commandes Windows PowerShell et exécutez les commandes suivantes :</span><span class="sxs-lookup"><span data-stu-id="ac4c1-113">Open a Windows PowerShell command prompt and run the following commands:</span></span>

   ```powershell
   Import-Module SkypeOnlineConnector
   $sfbSession = New-CsOnlineSession
   Import-PSSession $sfbSession
   ```

2. <span data-ttu-id="ac4c1-114">Lorsque vous y êtes invité par la commande **New-CsOnlineSession**, entrez le nom de votre compte d'administrateur Skype Entreprise Online.</span><span class="sxs-lookup"><span data-stu-id="ac4c1-114">When prompted by the **New-CsOnlineSession** command, enter your Skype for Business Online administrator account name.</span></span>

3. <span data-ttu-id="ac4c1-115">Dans la boîte de dialogue **Vous connecter à votre compte**, tapez votre mot de passe d’administrateur Skype Entreprise Online, puis cliquez sur **Connexion**.</span><span class="sxs-lookup"><span data-stu-id="ac4c1-115">In the **Sign in to your account** dialog box, type your Skype for Business Online administrator password, and then click **Sign in**.</span></span>

4. <span data-ttu-id="ac4c1-116">Suivez les instructions de la boîte de dialogue **Vous connecter à votre compte** pour fournir des informations d’authentification supplémentaires, telles qu’un code de vérification, puis cliquez sur **Vérifier**.</span><span class="sxs-lookup"><span data-stu-id="ac4c1-116">Follow the instructions in the **Sign in to your account** dialog box to provide additional authentication information, such as a verification code, and then click **Verify**.</span></span>

<span data-ttu-id="ac4c1-117">Pour plus d’informations, voir les rubriques suivantes :</span><span class="sxs-lookup"><span data-stu-id="ac4c1-117">For more information, see the following topics:</span></span>
  
- [<span data-ttu-id="ac4c1-118">Gestion des stratégies Skype Entreprise Online avec PowerShell</span><span class="sxs-lookup"><span data-stu-id="ac4c1-118">Manage Skype for Business Online policies with PowerShell</span></span>](manage-skype-for-business-online-policies-with-microsoft-365-powershell.md)
    
- [<span data-ttu-id="ac4c1-119">Affectation de stratégies Skype Entreprise Online propres à chaque utilisateur avec PowerShell</span><span class="sxs-lookup"><span data-stu-id="ac4c1-119">Assign per-user Skype for Business Online policies with PowerShell</span></span>](assign-per-user-skype-for-business-online-policies-with-microsoft-365-powershell.md)
    
## <a name="see-also"></a><span data-ttu-id="ac4c1-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ac4c1-120">See also</span></span>

[<span data-ttu-id="ac4c1-121">Gestion de Microsoft 365 à l’aide de PowerShell</span><span class="sxs-lookup"><span data-stu-id="ac4c1-121">Manage Microsoft 365 with PowerShell</span></span>](manage-microsoft-365-with-microsoft-365-powershell.md)
  
[<span data-ttu-id="ac4c1-122">Prise en main de PowerShell pour Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="ac4c1-122">Getting started with PowerShell for Microsoft 365</span></span>](getting-started-with-microsoft-365-powershell.md)

[<span data-ttu-id="ac4c1-123">Références sur l’applet de commande Skype Entreprise PowerShell</span><span class="sxs-lookup"><span data-stu-id="ac4c1-123">Skype for Business PowerShell cmdlet references</span></span>](https://docs.microsoft.com/powershell/module/skype/?view=skype-ps)

